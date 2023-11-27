---
title: Instale el [!DNL B2B for Adobe Commerce] extensión
description: Obtenga información sobre cómo instalar el [!DNL B2B for Adobe Commerce] metapaquete.
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: e57aa4e8919c2de5341c4b8363197d6380bbb0f6
workflow-type: tm+mt
source-wordcount: '973'
ht-degree: 0%

---


# Instale el [!DNL B2B for Adobe Commerce] extensión

La extensión B2B para Adobe Commerce solo está disponible para Adobe Commerce v2.2.0 o posterior. Se instala después de instalar Adobe Commerce.

Instale la versión más reciente de la extensión B2B compatible con la versión de Adobe Commerce implementada.

>[!NOTE]
>
>Estas instrucciones de instalación se aplican a Adobe Commerce implementado en las instalaciones. Para instalar la extensión B2B para proyectos de Commerce implementados en la infraestructura en la nube, consulte la [Guía de infraestructura de Commerce Cloud](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/b2b-module.html).

## Requisitos

- Adobe Commerce versión 2.3.x o posterior
- [Versión compatible de la extensión B2B](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html#compatibility)
- Válido [claves de autenticación](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) para descargar extensiones de Adobe Commerce.

  Guarde las claves de autenticación para la instalación definiéndolas globalmente en su [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) directorio. O bien, guárdelos en una [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) en el directorio raíz de la aplicación de Adobe Commerce.

Antes de instalar o actualizar la extensión B2B, consulte las notas de la versión para obtener la información más actual acerca de la compatibilidad de versiones, actualizaciones o cambios que puedan afectar a los requisitos de instalación o actualización.

- [Notas de la versión B2B](release-notes.md)
- [Notas de la versión de Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html?lang=en)

## Pasos de instalación

1. En el directorio raíz de la aplicación de Adobe Commerce, actualice el `composer.json` para añadir las dependencias para la extensión B2B:

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   Si se produce un error, por ejemplo:

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Compruebe la ortografía del paquete, la restricción de versión y que el paquete está disponible y coincide con el requisito de estabilidad mínima (estable).

1. Si se le solicita, introduzca su [claves de autenticación](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

   Su _clave pública_ es su nombre de usuario; su _clave privada_ es su contraseña. Si ha almacenado sus claves pública y privada en `auth.json`, no se le pedirá que se autentique.

1. Ejecute los siguientes comandos una vez que Composer haya terminado de actualizar los módulos:

   ```bash
   bin/magento setup:upgrade
   ```

   ```bash
   bin/magento setup:di:compile
   ```

   ```bash
   bin/magento setup:static-content:deploy -f
   ```

   ```bash
   bin/magento cache:clean
   ```

   >[!NOTE]
   >
   >En el modo de producción, podría recibir un mensaje a `Please rerun Magento compile command`. Introduzca los comandos para completar la instalación. Adobe Commerce no le pide que ejecute el comando de compilación en modo de desarrollador.

Después de completar la instalación, configure e inicie los consumidores de mensajes, lo que incluye [especificación de parámetros para consumidores de mensajes](#configure-message-consumers).

## Consumidores de mensajes

La extensión B2B para Adobe Commerce utiliza MySQL para la administración de colas de mensajes. En la tabla siguiente se enumeran los consumidores de mensajes que admiten las capacidades B2B. Después de instalar la extensión, inicie los consumidores de mensajes para las funciones B2B necesarias para su tienda de Commerce.

| Consumidor | Descripción |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | Actualiza el precio de cada producto en un catálogo compartido. Necesario cuando el [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) está activada en las opciones de configuración del sistema de administración. |
| `sharedCatalogUpdateCategoryPermissions` | Actualiza las categorías asignadas a una categoría de catálogo compartido. Necesario cuando el [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) está activada en las opciones de configuración del sistema de administración. |
| `negotiableQuotePriceUpdate` | Actualiza los precios de las ofertas negociables. Necesario cuando el [**[!UICONTROL Quotes]**](quotes.md) está activada en las opciones de configuración del sistema de administración. |
| `purchaseorder.toorder` | Convierte el pedido de compra en pedido. Necesario cuando el [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) está activada en las opciones de configuración del sistema de administración. |
| `purchaseorder.transactional.email` | Enviar correos electrónicos de pedidos de compra. Necesario cuando el [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) está activada en las opciones de configuración del sistema de administración. |
| `purchaseorder.validation` | Valida el pedido de compra con los datos relevantes [reglas de aprobación](account-dashboard-approval-rules.md). Necesario cuando el [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) está activada en las opciones de configuración del sistema de administración. |
| `quoteItemCleaner` | Elimina las ofertas de precios no válidas o inactivas cuando un producto se elimina del catálogo o del carro de compras. Necesario cuando el [**[!UICONTROL Quotes]**](quotes.md) está activada en las opciones de configuración del sistema de administración. |
| `inventoryQtyCounter` | Corrige de forma asíncrona el índice de existencias después de realizar un pedido o de eliminar un producto. Necesario cuando el [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) está activada para Inventory management en las opciones de configuración de administración. Consulte [Prácticas recomendadas de rendimiento](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/configuration.html#deferred-stock-update). |
| `async.operations.all` | Crea mensajes para cada tarea individual de un [operación en masa](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/), como importar o exportar artículos, cambiar los precios a escala masiva y asignar productos a un almacén. Necesario cuando el [**Operaciones masivas de administración**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) opción para [!DNL Inventory Management] se establece en **Ejecutar asincrónicamente** en los ajustes de configuración del sistema de administración. |

{style="table-layout:auto"}

>[!NOTE]
>
>Para obtener una lista de todos los consumidores de mensajes de Adobe Commerce, consulte [Consumidores de cola de mensajes](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/consumers.html) en el _Guía de configuración_.

### Configuración de consumidores de mensajes

Para evitar posibles problemas o retrasos en el procesamiento, agregue los siguientes parámetros cuando [inicio del mensaje consumidores](#start-message-consumers) para las capacidades B2B.

- `--max-messages <value>`— especifica el número máximo de mensajes que cada consumidor debe procesar antes de finalizar (valor por defecto = 10000). Aunque no lo recomendamos, puede utilizar 0 para evitar que el consumidor finalice. La práctica recomendada para una aplicación PHP es reiniciar los procesos de larga ejecución para evitar posibles fugas de memoria.

- `--batch-size <value>`— Permite limitar los recursos del sistema consumidos por los consumidores (CPU, memoria). El uso de lotes más pequeños reduce el uso de recursos y, por lo tanto, ralentiza el procesamiento.  Si se especifica, los mensajes de una cola se consumen en lotes de `<value>` cada uno. Esta opción solo se aplica al consumidor de lotes. If `--batch-size` no está definida, el consumidor por lotes recibe todos los mensajes disponibles en una cola.

Para obtener más información sobre las opciones de configuración adicionales, consulte [Specific-configuration](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#specific-configuration).

### Iniciar consumidores de mensajes

Para habilitar operaciones asincrónicas para las capacidades B2B, debe iniciar varios consumidores de mensajes.

1. Enumerar los consumidores de mensajes disponibles:

   ```bash
   bin/magento queue:consumers:list
   ```

   El comando devuelve los consumidores de mensajes disponibles, incluidos todos los [Consumidores de mensajes B2B](#message-consumers).

1. Inicie cada consumidor por separado:

   ```bash
   bin/magento queue:consumers:start [--max-messages=<value>] [--batch-size=<value>] <consumer_name>
   ```

   Por ejemplo:

   ```bash
   bin/magento queue:consumers:start quoteItemCleaner
   ```

>[!TIP]
>
>Para ejecutarlo en segundo plano, añada `&` para ejecutar el comando, vuelva al símbolo del sistema y siga ejecutando los comandos. Por ejemplo: `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`.

Para obtener más información, consulte [Administrar colas de mensajes](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) en el _Guía de configuración_.

### Añadir consumidores de mensajes a cron

Tiene la opción de automatizar la programación de ejecución de `SharedCatalogUpdateCategoryPermissions` y `SharedCatalogUpdatePrice` consumidores de mensajes añadiendo la programación al archivo de configuración de cron [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#process-management).

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

También puede configurar programaciones para consumidores de mensajes desde el [Ajustes de configuración de tienda](../systems/cron.md) en el Administrador.

## Habilitar funciones B2B en el administrador

Después de instalar la extensión B2B para Adobe Commerce e iniciar los consumidores de mensajes, también debe [habilitar las funciones B2B en el administrador](enable-basic-features.md).
