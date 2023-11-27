---
title: '[!DNL Inventory Management] Referencia de CLI'
description: Obtenga información acerca de los comandos proporcionados por [!DNL Inventory Management] para administrar los datos de inventario y las opciones de configuración.
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---

# [!DNL Inventory Management] Referencia de CLI

[!DNL Inventory Management] proporciona comandos para administrar los datos de inventario y las opciones de configuración.

Estos comandos incluyen:

- Comprobación y resolución de incoherencias de reservas que afectan a la cantidad vendible
- Adición de geocódigos para el algoritmo de prioridad de distancia

## Resolver incoherencias en las reservas

En las reservas se establece una retención de cantidad vendible para SKU de productos por stock. Cuando envía, añade productos, cancela o devuelve un pedido, las reservas de compensación entran para colocar o borrar estas retenciones.

[!DNL Inventory Management] proporciona dos comandos para comprobar y resolver incoherencias en las reservas:

- [`inventory:reservation:list-inconsistencies`](#list-inconsistencies-command)
- [`inventory:reservation:create-compensations`](#create-compensations-command)

### Causas de incoherencias en la reserva

[!DNL Inventory Management] genera reservas para eventos clave:

- Colocación del pedido (reserva inicial)
- Envío de pedido (reserva de compensación)
- Reembolso, pedido o emisión de una nota de crédito (reserva de compensación)
- Cancelación del pedido (reserva de compensación)

Las incoherencias en la reserva pueden producirse cuando:

- [!DNL Inventory Management] pierde la reserva inicial e introduce demasiadas compensaciones de reserva (compensaciones excesivas que conducen a importes incoherentes)
- [!DNL Inventory Management] coloca correctamente la reserva inicial, pero pierde las reservas compensatorias.

Puede revisar y comprobar las reservas manualmente en `inventory_reservation` tabla.

Las siguientes configuraciones y eventos pueden causar incoherencias en la reserva:

- **Actualice a la versión 2.3.x con pedidos que no estén en estado final (completo, cancelado o cerrado).** [!DNL Inventory Management] crea reservas compensatorias para estos pedidos, pero no introduce ni tiene la reserva inicial que deduce de la cantidad vendible. Se recomienda utilizar estos comandos después de actualizar a Adobe Commerce o Magento Open Source v2.3.x desde 2.1.x o 2.2.x. Si tiene pedidos pendientes, los comandos actualizan correctamente la cantidad vendible y las reservas para las ventas y la satisfacción de pedidos.
- **No gestiona las existencias y más adelante cambia esta configuración.** Puede empezar a utilizar 2.3.x con **[!UICONTROL Manage Stock]** establezca en `No` en la configuración de. [!DNL Commerce] no realiza reservas en eventos de envío y colocación de pedidos. Si más adelante habilita la variable **[!UICONTROL Manage Stock]** y se crean algunos pedidos, la cantidad vendible se dañaría con la reserva de compensación cuando gestione y cumpla ese pedido.
- **Usted reasigna las acciones para un sitio web mientras los pedidos se envían a ese sitio web**. La reserva inicial se introduce para el stock inicial y todas las reservas de compensación se introducen en el nuevo stock.
- **El total de todas las reservas puede no resolverse en `0`.** Todas las reservas en el ámbito de un pedido en estado final (completo, cancelado, cerrado) deben resolverse en `0`, borrando todas las retenciones de cantidad vendible.

### Enumerar incoherencias, comando

El `list-inconsistencies` El comando detecta y enumera todas las incoherencias de la reserva. Utilice las opciones de comando para comprobar sólo los pedidos completados o incompletos, o todos.

```bash
bin/magento inventory:reservation:list-inconsistencies
```

Opciones de comando:

- `-c`, `--complete-orders` - Devuelve incoherencias para pedidos completados. Las reservas incorrectas pueden seguir en espera para pedidos completados.
- `-i`, `--incomplete-orders` - Devuelve incoherencias para pedidos incompletos (parcialmente enviados, no enviados). Las reservas incorrectas pueden contener una cantidad vendible excesiva o insuficiente para los pedidos.
- `-b`, `--bunch-size` - Define cuántos pedidos se cargarán a la vez.
- `-r`, `--raw` - Salida en bruto.

Respuestas mediante `-r` volver en `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` formato:

- El ID de pedido indica el ámbito de la incoherencia.
- SKU indica el producto con la incoherencia.
- Cantidad establece el importe que se va a introducir para la compensación de reserva.
- ID de stock define el ámbito de stock, que utiliza las reservas para calcular la cantidad vendible.

Ejemplos:

```terminal
bin/magento inventory:reservation:list-inconsistencies

Inconsistencies found on following entries:
Order 172:
- Product bike-123 should be compensated by +2.000000 for stock 1
```

```terminal
bin/magento inventory:reservation:list-inconsistencies -r

172:bike-123:+2.000000:1
```

Si no se encuentran problemas, devuelve este mensaje: No se encontraron incoherencias en el pedido.

### Crear compensaciones, comando

El `create-compensations` El comando crea reservas de compensación. Según el problema, se crean nuevas reservas para realizar o liberar una retención de cantidad vendible.

Para crear reservas, proporcione compensaciones con el formato `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` como `172:bike-123:+2.000000:1`.

```bash
bin/magento inventory:reservation:create-compensations
```

Opción de comando:

- `-r`, `--raw` - Devuelve la salida sin procesar.

Si el formato de la solicitud es incorrecto, se muestra el siguiente mensaje:

```terminal
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

A medida que el comando crea reservas, muestra mensajes que indican las actualizaciones por SKU, pedido y existencias.

```terminal
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

Si el SKU de una entrada de compensación incluye espacios, escríbalo entre comillas.

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### Detectar incoherencias y crear compensaciones

Puede detectar incoherencias y crear compensaciones inmediatamente utilizando una barra vertical para ejecutar tanto la variable `list-inconsistencies` y `create-compensations`. Utilice el `-r` opción de comando para generar y enviar los datos sin procesar a `create-compensations`.

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

Respuesta de ejemplo:

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

```terminal
Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
- Product bikehat-456 was compensated by +1.000000 for stock 1
```

Una vez completadas las actualizaciones, ejecute el comando list para comprobar lo siguiente:

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```terminal
No order inconsistencies were found.
```

También puede canalizar los comandos para detectar incoherencias y crear compensaciones solo para incompletos (`-i`) o completa (`-c`) pedidos.

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## Importar geocódigos

[!DNL Inventory Management] proporciona el [Algoritmo de prioridad de distancia](distance-priority-algorithm.md), que ayuda a determinar la mejor opción para enviar un pedido completo o parcial. El algoritmo utiliza información GPS o geocódigos para calcular la distancia entre el origen (un almacén u otra ubicación física) de cada artículo de un pedido y la dirección de envío. En función de estos resultados, el algoritmo recomienda qué fuente se debe utilizar para enviar cada artículo del pedido.

El comerciante selecciona el proveedor de los datos de GPS o geocódigo necesarios para calcular las distancias:

- **MAPA DE GOOGLE** utiliza [Plataforma de mapas de Google](https://mapsplatform.google.com/) servicios para calcular la distancia y el tiempo entre la dirección de destino de envío y las ubicaciones de origen. Esta opción requiere un plan de facturación de Google y puede incurrir en cargos a través de Google.

- **Cálculo sin conexión** calcula la distancia utilizando los datos descargados de [geonames.org](https://www.geonames.org/) e importado en Commerce con un comando. Esta opción es gratuita.

Para importar geocódigos para el cálculo sin conexión:

Introduzca el siguiente comando con una lista separada por espacios de [Códigos de país ISO-3166 alpha2](https://www.geonames.org/countries/):

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

Por ejemplo:

```bash
bin/magento inventory-geonames:import us ca gb de
```

El sistema descarga e importa los datos de geocódigos en la base de datos y, a continuación, muestra el mensaje  `Importing <country code>: OK`.
