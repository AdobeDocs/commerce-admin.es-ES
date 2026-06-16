---
title: '[!DNL Inventory Management] referencia de CLI'
description: Obtenga información acerca de los comandos proporcionados por el módulo  [!DNL Inventory Management] para administrar los datos de inventario y la configuración.
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
TQID: https://experienceleague.adobe.com/jdlLgwIe50ExZ2giXBiGf5cG8L4DQDZe4psbB16F5JE
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 858
ht-degree: 0%

---

# [!DNL Inventory Management] referencia de CLI

[!DNL Inventory Management] proporciona comandos para administrar los datos de inventario y las opciones de configuración.

Estos comandos incluyen:

- Comprobación y resolución de incoherencias de reservas que afectan a la cantidad vendible
- Adición de geocódigos para el algoritmo de prioridad de distancia

## Resolver incoherencias en las reservas

En las reservas se establece una retención de cantidad vendible para SKU de productos por stock. Cuando envía, añade productos, cancela o devuelve un pedido, las reservas de compensación entran para colocar o borrar estas retenciones.

[!DNL Inventory Management] proporciona dos comandos para comprobar y resolver las incoherencias en las reservas:

- [`inventory:reservation:list-inconsistencies`](#list-inconsistencies-command)
- [`inventory:reservation:create-compensations`](#create-compensations-command)

### Causas de incoherencias en la reserva

[!DNL Inventory Management] genera reservas para eventos clave:

- Colocación del pedido (reserva inicial)
- Envío de pedido (reserva de compensación)
- Reembolso, pedido o emisión de una nota de crédito (reserva de compensación)
- Cancelación del pedido (reserva de compensación)

Las incoherencias en la reserva pueden producirse cuando:

- [!DNL Inventory Management] pierde la reserva inicial e introduce demasiadas compensaciones de reserva (lo que compensa en exceso y genera importes incoherentes)
- [!DNL Inventory Management] coloca correctamente la reserva inicial, pero pierde las reservas compensatorias.

Puede revisar y comprobar las reservas manualmente en la tabla `inventory_reservation`.

Las siguientes configuraciones y eventos pueden causar incoherencias en la reserva:

- **Actualizar a la versión 2.3.x con pedidos que no se encuentran en estado final (Completado, Cancelado o Cerrado).** [!DNL Inventory Management] crea reservas compensatorias para estos pedidos, pero no introduce ni tiene la reserva inicial que deduce de la cantidad vendible. Se recomienda utilizar estos comandos después de actualizar a Adobe Commerce o Magento Open Source v2.3.x desde 2.1.x o 2.2.x. Si tiene pedidos pendientes, los comandos actualizan correctamente la cantidad vendible y las reservas para las ventas y la satisfacción de pedidos.
- **No administra existencias y más tarde cambia esta configuración.** Puede empezar a usar 2.3.x con **[!UICONTROL Manage Stock]** establecido en `No` en la configuración. [!DNL Commerce] no realiza reservas en eventos de envío y colocación de pedidos. Si posteriormente habilita la configuración **[!UICONTROL Manage Stock]** y se crean algunos pedidos, la cantidad vendible se dañaría con una reserva de compensación al administrar y cumplir ese pedido.
- **Reasigna las existencias de un sitio web mientras los pedidos se envían a ese sitio web**. La reserva inicial se introduce para el stock inicial y todas las reservas de compensación se introducen en el nuevo stock.
- **Es posible que el total de todas las reservas no se resuelva en `0`.** Todas las reservas en el ámbito de un pedido en estado final (Completado, Cancelado, Cerrado) deben resolverse en `0`, borrando todas las retenciones de cantidad vendible.

### Enumerar incoherencias, comando

El comando `list-inconsistencies` detecta y enumera todas las incoherencias en la reserva. Utilice las opciones de comando para comprobar sólo los pedidos completados o incompletos, o todos.

```bash
bin/magento inventory:reservation:list-inconsistencies
```

Opciones de comando:

- `-c`, `--complete-orders` - Devuelve incoherencias para pedidos completados. Las reservas incorrectas pueden seguir en espera para pedidos completados.
- `-i`, `--incomplete-orders`: devuelve incoherencias para pedidos incompletos (enviados parcialmente, no enviados). Las reservas incorrectas pueden contener una cantidad vendible excesiva o insuficiente para los pedidos.
- `-b`, `--bunch-size` - Define cuántos pedidos cargar a la vez.
- `-r`, `--raw`: salida sin procesar.

Las respuestas que utilizan `-r` devuelven en formato `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>`:

- El ID de pedido indica el ámbito de la incoherencia.
- SKU indica el producto con la incoherencia.
- Cantidad establece el importe que se va a introducir para la compensación de reserva.
- ID de stock define el ámbito de stock, que utiliza las reservas para calcular la cantidad vendible.

Ejemplos:

```bash
bin/magento inventory:reservation:list-inconsistencies

Inconsistencies found on following entries:
Order 172:
- Product bike-123 should be compensated by +2.000000 for stock 1
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r

172:bike-123:+2.000000:1
```

Si no se encuentran problemas, devuelve este mensaje: No se encontraron incoherencias en el pedido.

### Crear compensaciones, comando

El comando `create-compensations` crea reservas de compensación. Según el problema, se crean nuevas reservas para realizar o liberar una retención de cantidad vendible.

Para crear reservas, proporcione compensaciones con el formato `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>`, como `172:bike-123:+2.000000:1`.

```bash
bin/magento inventory:reservation:create-compensations
```

Opción de comando:

- `-r`, `--raw` - Devuelve el resultado sin procesar.

Si el formato de la solicitud es incorrecto, se muestra el siguiente mensaje:

```
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

A medida que el comando crea reservas, muestra mensajes que indican las actualizaciones por SKU, pedido y existencias.

```bash
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

Si el SKU de una entrada de compensación incluye espacios, escríbalo entre comillas.

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### Detectar incoherencias y crear compensaciones

Puede detectar incoherencias y crear compensaciones inmediatamente utilizando una barra vertical para ejecutar `list-inconsistencies` y `create-compensations`. Utilice la opción de comando `-r` para generar y enviar los datos sin procesar a `create-compensations`.

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

Respuesta de ejemplo:

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

```
Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
- Product bikehat-456 was compensated by +1.000000 for stock 1
```

Una vez completadas las actualizaciones, ejecute el comando list para comprobar lo siguiente:

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```
No order inconsistencies were found.
```

También puede canalizar los comandos para detectar incoherencias y crear compensaciones solo para pedidos incompletos (`-i`) o completos (`-c`).

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## Importar geocódigos

[!DNL Inventory Management] proporciona el algoritmo de prioridad de distancia [Distance Priority](distance-priority-algorithm.md), que ayuda a determinar la mejor opción para enviar un pedido completo o parcial. El algoritmo utiliza información GPS o geocódigos para calcular la distancia entre el origen (un almacén u otra ubicación física) de cada artículo de un pedido y la dirección de envío. En función de estos resultados, el algoritmo recomienda qué fuente se debe utilizar para enviar cada artículo del pedido.

El comerciante selecciona el proveedor de los datos de GPS o geocódigo necesarios para calcular las distancias:

- **Google MAP** usa los servicios de [Google Maps Platform](https://mapsplatform.google.com/) para calcular la distancia y el tiempo entre la dirección de destino de envío y las ubicaciones de origen. Esta opción requiere un plan de facturación de Google y puede incurrir en cargos a través de Google.

- **Cálculo sin conexión** calcula la distancia usando datos descargados de [geonames.org](https://www.geonames.org/) e importados a Commerce con un comando. Esta opción es gratuita.

Para importar geocódigos para el cálculo sin conexión:

Escriba el comando siguiente con una lista separada por espacios de [códigos de país ISO-3166 alpha2](https://www.geonames.org/countries/):

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

Por ejemplo:

```bash
bin/magento inventory-geonames:import us ca gb de
```

El sistema descarga e importa los datos de geocódigos en la base de datos y, a continuación, muestra el mensaje `Importing <country code>: OK`.
