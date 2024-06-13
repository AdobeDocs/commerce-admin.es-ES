---
title: Instale el [!DNL Adobe Commerce B2B] extensión
description: Obtenga información sobre cómo instalar el [!DNL Adobe Commerce B2B] metapaquete.
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: be36742aa1214e7e8e7f343051336cd3635099f4
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---


# Instale el [!DNL Adobe Commerce B2B] extensión

La extensión Adobe Commerce B2B, `magento/extension-b2b` está disponible para todas las versiones compatibles de Adobe Commerce. Se instala después de instalar Adobe Commerce.


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

- Acceso a [repo.magento.com](https://repo.magento.com/) para descargar la extensión de. Para obtener la generación de claves y los derechos necesarios, consulte [Obtener las claves de autenticación](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

  Guarde las claves de autenticación para la instalación definiéndolas globalmente en su [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) directorio. O bien, guárdelos en una [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) en el directorio raíz de la aplicación de Adobe Commerce.

- [Versión compatible de la extensión B2B](https://experienceleague.adobe.com/en/docs/commerce-operations/release/product-availability): determine la versión más reciente de la extensión B2B compatible con la versión de Adobe Commerce implementada.

- Consulte las notas de la versión para obtener la información más actual acerca de la compatibilidad de versiones, actualizaciones o cambios que pueden afectar a los requisitos de instalación o actualización.

   - [Notas de la versión B2B](release-notes.md)
   - [Notas de la versión de Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/release/versions)

>[!ENDSHADEBOX]

Instale la extensión B2B (`magento/b2b-extension`) con Composer. La extensión es un metapaquete de compositor que incluye la colección de módulos que habilitan las capacidades B2B para una instancia de Adobe Commerce. Para ver una lista de los módulos incluidos, consulte [Paquetes B2B](packages.md).

>[!BEGINTABS]

>[!TAB Infraestructura en nube]

>[!TIP]
>
>Al instalar Adobe Commerce B2B en la infraestructura en la nube, Adobe recomienda implementar la aplicación de Adobe Commerce en un entorno de integración o ensayo antes de comenzar.

Adobe recomienda trabajar en una rama de desarrollo al añadir la extensión B2B al proyecto. Si no tiene una rama, consulte [Crear una rama para desarrollo](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches). Al instalar la extensión B2B, la variable `Magento_B2b` nombre de extensión se inserta automáticamente en `app/etc/config.php` archivo. No es necesario editar el archivo directamente.

**Para instalar la extensión B2B**:

1. En la estación de trabajo local, cambie al directorio del proyecto.

1. Cree o desproteja una rama de desarrollo.

1. Añada la extensión B2B a `require` de la sección `composer.json` archivo.

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
   >Al insertar actualizaciones en el entorno de la nube de, se inicia el proceso de implementación de la nube de Commerce para aplicar los cambios. Compruebe el estado de implementación desde el [implementar registro](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process). Si encuentra errores de implementación, consulte [Recuperar de un error de componente](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment).

1. Una vez finalizada la generación y la implementación, utilice SSH para iniciar sesión en el entorno remoto y comprobar que la extensión B2B está instalada y habilitada.

   ```bash
   bin/magento module:status Magento_B2b
   ```

   Un nombre de extensión utiliza el formato: `<VendorName>_<ComponentName>`.

   Respuesta de ejemplo:

   ```terminal
   Magento_B2b : Module is enabled
   ```

>[!TAB On-Premise]

1. En el directorio raíz de la aplicación de Adobe Commerce, actualice el `composer.json` para añadir las dependencias para la extensión B2B:

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   Si se produce un error, por ejemplo:

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Compruebe la ortografía del paquete, la restricción de versión y que el paquete está disponible y coincide con el requisito de estabilidad mínima (estable).

1. Si se le solicita, introduzca su [claves de autenticación](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

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

>[!ENDTABS]

Después de completar la instalación, configure e inicie los consumidores de mensajes.

## Consumidores de mensajes

La extensión Adobe Commerce B2B utiliza MySQL para la administración de colas de mensajes. En la tabla siguiente se enumeran los consumidores de mensajes que admiten las capacidades B2B. Después de instalar la extensión, inicie los consumidores de mensajes para las funciones B2B necesarias para su tienda de Commerce.

| Consumidor | Descripción |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | Actualiza el precio de cada producto en un catálogo compartido. Necesario cuando el [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) está activada en los ajustes de configuración del sistema de administración. |
| `sharedCatalogUpdateCategoryPermissions` | Actualiza las categorías asignadas a una categoría de catálogo compartido. Necesario cuando el [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) está activada en los ajustes de configuración del sistema de administración. |
| `negotiableQuotePriceUpdate` | Actualiza los precios de las ofertas negociables. Necesario cuando el [**[!UICONTROL Quotes]**](quotes.md) está activada en los ajustes de configuración del sistema de administración. |
| `purchaseorder.toorder` | Convierte el pedido de compra en pedido. Necesario cuando el [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) está activada en los ajustes de configuración del sistema de administración. |
| `purchaseorder.transactional.email` | Enviar correos electrónicos de pedidos de compra. Necesario cuando el [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) está activada en los ajustes de configuración del sistema de administración. |
| `purchaseorder.validation` | Valida el pedido de compra con los datos relevantes [reglas de aprobación](account-dashboard-approval-rules.md). Necesario cuando el [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) está activada en los ajustes de configuración del sistema de administración. |
| `quoteItemCleaner` | Elimina las ofertas de precios no válidas o inactivas cuando un producto se elimina del catálogo o del carro de compras. Necesario cuando el [**[!UICONTROL Quotes]**](quotes.md) está activada en los ajustes de configuración del sistema de administración. |
| `inventoryQtyCounter` | Corrige de forma asíncrona el índice de existencias después de realizar un pedido o de eliminar un producto. Necesario cuando el [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) está activada para Inventory management en las opciones de configuración de administración. Consulte [Prácticas recomendadas de rendimiento](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update). |
| `async.operations.all` | Crea mensajes para cada tarea individual de un [operación en masa](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/) como importar o exportar artículos, cambiar precios a escala masiva y asignar productos a un almacén. Necesario cuando el [**Operaciones masivas de administración**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) opción para [!DNL Inventory Management] se establece en **Ejecutar asincrónicamente** en los ajustes de configuración del sistema de administración. |

{style="table-layout:auto"}

>[!NOTE]
>
>Para obtener una lista de todos los consumidores de mensajes de Adobe Commerce, consulte [Consumidores de cola de mensajes](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/consumers) en el _Guía de configuración_.

### Configuración de consumidores de mensajes

Para evitar posibles problemas o retrasos en el procesamiento, agregue los siguientes parámetros cuando [inicio del mensaje consumidores](#start-message-consumers) para las capacidades B2B.

- `--max-messages <value>`— especifica el número máximo de mensajes que cada consumidor debe procesar antes de finalizar (valor por defecto = 10000). Aunque el Adobe no lo recomienda, puede utilizar 0 para evitar que el consumidor finalice. La práctica recomendada para una aplicación PHP es reiniciar los procesos de larga ejecución para evitar posibles fugas de memoria.

- `--batch-size <value>`— Permite limitar los recursos del sistema consumidos por los consumidores (CPU, memoria). El uso de lotes más pequeños reduce el uso de recursos y, por lo tanto, ralentiza el procesamiento.  Si se especifica, los mensajes de una cola se consumen en lotes de `<value>` cada uno. Esta opción solo se aplica al consumidor de lotes. If `--batch-size` no está definida, el consumidor por lotes recibe todos los mensajes disponibles en una cola.

Para obtener más información sobre las opciones de configuración adicionales, consulte [Specific-configuration](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#specific-configuration).

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

Para obtener más información, consulte [Administrar colas de mensajes](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues) en el _Guía de configuración_.

### Añadir consumidores de mensajes a cron

Puede automatizar la programación de ejecución de `SharedCatalogUpdateCategoryPermissions` y `SharedCatalogUpdatePrice` consumidores de mensajes añadiendo la programación al archivo de configuración de cron [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management).

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

También puede configurar programaciones para consumidores de mensajes desde el [Ajustes de configuración de tienda](../systems/cron.md) en el Administrador.

## Habilitar funciones B2B en el administrador

Después de instalar la extensión Adobe Commerce B2B e iniciar los consumidores de mensajes, también debe [habilitar las funciones B2B en el administrador](enable-basic-features.md).

