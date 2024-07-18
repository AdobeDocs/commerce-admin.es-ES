---
title: Instalar la extensión  [!DNL Adobe Commerce B2B]
description: Aprenda a instalar el  [!DNL Adobe Commerce B2B] metapackage.
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: 53c3b6c9fa9c152e6619528a43580b0acc71a2a5
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---


# Instalar la extensión [!DNL Adobe Commerce B2B]

La extensión B2B de Adobe Commerce `magento/extension-b2b` está disponible para todas las versiones compatibles de Adobe Commerce. Se instala después de instalar Adobe Commerce.


## Requisitos

- [Adobe Commerce](https://business.adobe.com/products/magento/magento-commerce.html), todas las versiones compatibles
- PHP 8.1/8.2/8.3
- [!DNL Composer]

## Plataformas compatibles

- Adobe Commerce en infraestructura en la nube (ECE)
- Adobe Commerce local (EE)

## Pasos de instalación

>[!BEGINSHADEBOX]

**Requisitos previos**

- Acceda a [repo.magento.com](https://repo.magento.com/) para descargar la extensión. Para obtener la generación de claves y los derechos necesarios, consulta [Obtener tus claves de autenticación](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

  Guarde las claves de autenticación para la instalación definiéndolas globalmente en el directorio [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home). O bien, guárdelos en un archivo [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) en el directorio raíz de la aplicación de Adobe Commerce.

- [Versión compatible de la extensión B2B](https://experienceleague.adobe.com/en/docs/commerce-operations/release/product-availability)- Determine la versión más reciente de la extensión B2B compatible con la versión implementada de Adobe Commerce.

- Consulte las notas de la versión para obtener la información más actual acerca de la compatibilidad de versiones, actualizaciones o cambios que pueden afectar a los requisitos de instalación o actualización.

   - [Notas de la versión B2B](release-notes.md)
   - [Notas de la versión de Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/release/versions)

>[!ENDSHADEBOX]

Instale la extensión B2B (`magento/b2b-extension`) mediante Composer. La extensión es un metapaquete de compositor que incluye la colección de módulos que habilitan las capacidades B2B para una instancia de Adobe Commerce. Para obtener una lista de los módulos incluidos, consulte [Paquetes B2B](packages.md).

>[!BEGINTABS]

>[!TAB Infraestructura en la nube]

>[!TIP]
>
>Al instalar Adobe Commerce B2B en la infraestructura en la nube, Adobe recomienda implementar la aplicación de Adobe Commerce en un entorno de integración o ensayo antes de comenzar.

Adobe recomienda trabajar en una rama de desarrollo al añadir la extensión B2B al proyecto. Si no tiene una rama, consulte [Crear una rama para desarrollo](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches). Al instalar la extensión B2B, el nombre de la extensión `Magento_B2b` se inserta automáticamente en el archivo `app/etc/config.php`. No es necesario editar el archivo directamente.

**Para instalar la extensión B2B**:

1. En la estación de trabajo local, cambie al directorio del proyecto.

1. Cree o desproteja una rama de desarrollo.

1. Agregue la extensión B2B a la sección `require` del archivo `composer.json`.

   ```bash
   composer require magento/extension-b2b --no-update
   ```

1. Actualice las dependencias del proyecto.

   ```bash
   composer update
   ```

1. Agregar, confirmar y enviar cambios de código.

   ```bash
   git add -A
   ```

   ```bash
   git commit -m "Install the B2B extension."
   ```

   ```bash
   git push origin <branch-name>
   ```

   >[!NOTE]
   >
   >Al insertar actualizaciones en el entorno de la nube de, se inicia el proceso de implementación de la nube de Commerce para aplicar los cambios. Compruebe el estado de implementación desde el [registro de implementación](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process). Si encuentra errores de implementación, consulte [Error al recuperar del componente](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment).

1. Una vez finalizada la generación y la implementación, utilice SSH para iniciar sesión en el entorno remoto y comprobar que la extensión B2B está instalada y habilitada.

   ```bash
   bin/magento module:status Magento_B2b
   ```

   Un nombre de extensión usa el formato: `<VendorName>_<ComponentName>`.

   Respuesta de ejemplo:

   ```
   Magento_B2b : Module is enabled
   ```

>[!TAB Local]

1. En el directorio raíz de la aplicación de Adobe Commerce, actualice `composer.json` para agregar las dependencias para la extensión B2B:

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   Si se produce un error, por ejemplo:

   ```
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Compruebe la ortografía del paquete, la restricción de versión y que el paquete está disponible y coincide con el requisito de estabilidad mínima (estable).

1. Si se le solicita, escriba sus [claves de autenticación](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

   Su _clave pública_ es su nombre de usuario; su _clave privada_ es su contraseña. Si ha almacenado las claves pública y privada en `auth.json`, no se le pedirá que se autentique.

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
   >En el modo Producción, podría recibir un mensaje dirigido a `Please rerun Magento compile command`. Introduzca los comandos para completar la instalación. Adobe Commerce no le pide que ejecute el comando de compilación en modo de desarrollador.

>[!ENDTABS]

Después de completar la instalación, configure e inicie los consumidores de mensajes.

## Consumidores de mensajes

La extensión Adobe Commerce B2B utiliza MySQL para la administración de colas de mensajes. En la tabla siguiente se enumeran los consumidores de mensajes que admiten las capacidades B2B. Después de instalar la extensión, inicie los consumidores de mensajes para las funciones B2B necesarias para su tienda de Commerce.

| Consumidor | Descripción |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | Actualiza el precio de cada producto en un catálogo compartido. Necesario cuando la opción [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) está habilitada en las opciones de configuración de Admin System. |
| `sharedCatalogUpdateCategoryPermissions` | Actualiza las categorías asignadas a una categoría de catálogo compartido. Necesario cuando la opción [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) está habilitada en las opciones de configuración de Admin System. |
| `negotiableQuotePriceUpdate` | Actualiza los precios de las ofertas negociables. Necesario cuando la opción [**[!UICONTROL Quotes]**](quotes.md) está habilitada en las opciones de configuración de Admin System. |
| `purchaseorder.toorder` | Convierte el pedido de compra en pedido. Necesario cuando la opción [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) está habilitada en las opciones de configuración de Admin System. |
| `purchaseorder.transactional.email` | Enviar correos electrónicos de pedidos de compra. Necesario cuando la opción [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) está habilitada en las opciones de configuración de Admin System. |
| `purchaseorder.validation` | Valida el pedido de compra con [reglas de aprobación](account-dashboard-approval-rules.md) relevantes. Necesario cuando la opción [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) está habilitada en las opciones de configuración de Admin System. |
| `quoteItemCleaner` | Elimina las ofertas de precios no válidas o inactivas cuando un producto se elimina del catálogo o del carro de compras. Necesario cuando la opción [**[!UICONTROL Quotes]**](quotes.md) está habilitada en las opciones de configuración de Admin System. |
| `inventoryQtyCounter` | Corrige de forma asíncrona el índice de existencias después de realizar un pedido o de eliminar un producto. Necesario cuando la opción [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) está habilitada para Inventory management en las opciones de configuración de administración. Consulte [Prácticas recomendadas de rendimiento](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update). |
| `async.operations.all` | Crea mensajes para cada tarea individual de una [operación masiva](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/), como importar o exportar artículos, cambiar precios a escala masiva y asignar productos a un almacén. Necesario cuando la opción [**Operaciones masivas de administración**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) para [!DNL Inventory Management] está establecida en **Ejecutar asincrónicamente** en los ajustes de configuración del sistema de administración. |

{style="table-layout:auto"}

>[!NOTE]
>
>Para obtener una lista de todos los consumidores de mensajes de Adobe Commerce, consulte [Consumidores de colas de mensajes](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/consumers) en la _Guía de configuración_.

### Configuración de consumidores de mensajes

Evite posibles problemas o retrasos en el procesamiento agregando los siguientes parámetros al [iniciar los consumidores de mensajes](#start-message-consumers) para las capacidades B2B.

- `--max-messages <value>`: especifica el número máximo de mensajes que cada consumidor debe procesar antes de finalizar (predeterminado = 10000). Aunque el Adobe no lo recomienda, puede utilizar 0 para evitar que el consumidor finalice. La práctica recomendada para una aplicación PHP es reiniciar los procesos de larga ejecución para evitar posibles fugas de memoria.

- `--batch-size <value>`: permite limitar los recursos del sistema consumidos por los consumidores (CPU, memoria). El uso de lotes más pequeños reduce el uso de recursos y, por lo tanto, ralentiza el procesamiento.  Si se especifica, los mensajes de una cola se consumen en lotes de `<value>` cada uno. Esta opción solo se aplica al consumidor de lotes. Si `--batch-size` no está definido, el consumidor por lotes recibe todos los mensajes disponibles en una cola.

Para obtener información acerca de opciones de configuración adicionales, vea [Specific-configuration](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#specific-configuration).

### Iniciar consumidores de mensajes

Para habilitar operaciones asincrónicas para las capacidades B2B, debe iniciar varios consumidores de mensajes.

1. Enumerar los consumidores de mensajes disponibles:

   ```bash
   bin/magento queue:consumers:list
   ```

   El comando devuelve los consumidores de mensajes disponibles, incluidos todos los [consumidores de mensajes B2B](#message-consumers).

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
>Para ejecutarlo en segundo plano, agregue `&` al comando, vuelva a un símbolo del sistema y continúe ejecutando comandos. Por ejemplo: `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`.

Para obtener más información, consulte [Administrar colas de mensajes](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues) en la _Guía de configuración_.

### Añadir consumidores de mensajes a cron

Puede automatizar la programación de ejecución para los consumidores de mensajes `SharedCatalogUpdateCategoryPermissions` y `SharedCatalogUpdatePrice` agregando la programación al archivo de configuración de cron [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management).

```
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

También puede configurar programaciones para consumidores de mensajes desde [Configuración de almacenamiento](../systems/cron.md) en el Administrador.

## Habilitar funciones B2B en el administrador

Después de instalar la extensión B2B de Adobe Commerce e iniciar los consumidores de mensajes, también debe [habilitar las características B2B en el administrador](enable-basic-features.md).

