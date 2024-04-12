---
title: Administración de caché
description: Aprenda a utilizar las herramientas de administración de caché, que proporcionan una manera sencilla de mejorar el rendimiento del sitio.
exl-id: c87f85ca-81b9-4cbf-9817-3d779397eefd
feature: Cache, System
source-git-commit: fdf04be69754d0209772d9ceb244e3808f3b61d3
workflow-type: tm+mt
source-wordcount: '1821'
ht-degree: 0%

---

# Administración de caché

El sistema de administración de caché de Magento Open Source y Adobe Commerce proporciona una forma sencilla de mejorar el rendimiento del sitio. Siempre que una caché requiera una actualización, se mostrará una notificación con un vínculo a [!UICONTROL Cache Management] para completar la actualización.

![Guardar atributo de producto: actualizar mensaje de caché](./assets/product-attribute-save-msg-update-cache.png){width="500"}

El _[!UICONTROL Cache Management]_Esta página muestra el estado de cada caché principal y su etiqueta asociada. Los botones grandes de la esquina superior derecha pueden utilizarse para vaciar la caché o el almacenamiento en caché todo incluido. En la parte inferior de la página, los botones adicionales le permiten vaciar la caché de imágenes de producto del catálogo y la caché de JavaScript/CSS.

>[!IMPORTANT]
>
>Cuando se cambian las entidades del catálogo, puede afectar a otras páginas e invalidar varias memorias caché simultáneamente. Al revisar la página de administración de caché, podía ver elementos no válidos que requerían actualización cuando se _**no editado directamente**_. Por ejemplo, esta invalidación se produce cuando edita cualquier producto del catálogo asignado a cualquier categoría o cuando cambia cualquier regla de producto relacionada.

Después de borrar una caché, actualice siempre el explorador para asegurarse de que puede ver los archivos más recientes. Al borrar la caché de Commerce, no se borra la caché del explorador web. Es posible que tenga que borrar la caché del explorador para ver el contenido actualizado.

Encontrará información técnica adicional acerca del almacenamiento en caché de Adobe Commerce en el [Resumen de caché](https://developer.adobe.com/commerce/frontend-core/guide/caching/){:target=&quot;_blank&quot;} en el _Guía de desarrollo de Commerce Frontend_.

Acceda a la _[!UICONTROL Cache Management]_haciendo una de las siguientes acciones:

- Haga clic en **[!UICONTROL Cache Management]** en el mensaje situado encima del espacio de trabajo.
- En el _Administrador_ barra lateral, vaya a **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

![Administración de caché](./assets/cache-management-invalid.png){width="700" zoomable="yes"}

## Prácticas recomendadas para el almacenamiento en caché

La reindexación y el almacenamiento en caché tienen diferentes propósitos en Commerce. [Índices](index-management.md) rastree la información de la base de datos para obtener un mayor rendimiento de búsqueda, una recuperación de datos más rápida para tiendas, etc. Las cachés guardan los datos cargados, las imágenes, los formatos y similares para aumentar el rendimiento al cargar y acceder a la tienda.

- Vaciar siempre la caché después de instalar extensiones/módulos. Puede instalar una o varias extensiones y vaciar la caché.
- Vacíe la caché después de instalar Commerce. Para instalaciones nuevas, también debe reindexar.
- Vacíe la caché después de actualizar de una versión de código abierto o de Commerce a otra.
- Al vaciar las cachés, tenga en cuenta el tipo de caché y programe el vaciado durante las horas de menor actividad. Por ejemplo, elija una hora en la que pocos clientes utilicen el sitio, como tarde por la noche o temprano por la mañana. Borrar tipos de caché durante la demanda máxima puede aumentar la carga en el administrador y hacer que el sitio se desactive hasta que se complete la operación.
- Cuándo [reindexación](index-management.md), no es necesario vaciar la caché.

## Recursos de rol de administración de caché

Puede asignar acceso a acciones de mantenimiento de caché específicas a los usuarios por función, incluidas las opciones para ver, alternar y vaciar cachés. El Adobe recomienda habilitar las acciones de vaciado solo para usuarios de nivel de administrador. Proporcionar acceso a todas las funciones de administración de caché puede afectar el rendimiento de su tienda.

![Recursos de funciones: administración de caché](./assets/permissions-role-resources-cache-management.png){width="600" zoomable="yes"}

Para obtener información sobre la asignación de recursos para conceder acceso a las cuentas de usuario de administrador, consulte [Recursos de roles](permissions-user-roles.md#role-resources). Los siguientes recursos controlan el acceso a las herramientas de administración de caché:

- [!UICONTROL Clean Cache Actions]

   - [!UICONTROL Flush Cache Storage]
   - [!UICONTROL Flush Magento Cache]

- [!UICONTROL Cache Type Management]

   - [!UICONTROL Toggle Cache Type]
   - [!UICONTROL Refresh Cache Type]

- [!UICONTROL Additional Cache Management]

   - [!UICONTROL Catalog Images Cache]
   - [!UICONTROL Flush Js/Css]
   - [!UICONTROL Flush Static Files]

## Actualizar cachés específicas

1. Para que se actualice cada caché, active la casilla al principio de la fila.

1. Establecer **[!UICONTROL Actions]** hasta `Refresh` y haga clic en **[!UICONTROL Submit]**.

## Realización de actualización masiva de acciones

1. Para seleccionar un grupo de cachés, establezca **[!UICONTROL Mass Actions]** a uno de los siguientes:

   - `Select All`
   - `Select Visible`

1. Seleccione la casilla de verificación de cada caché que desee actualizar.

1. Establecer **[!UICONTROL Actions]** hasta `Refresh` y haga clic en **[!UICONTROL Submit]**.

## Vaciar la memoria caché de imágenes del producto

1. En _[!UICONTROL Additional Cache Management]_, haga clic en **[!UICONTROL Flush Catalog Images Cache]**para borrar los archivos de imagen de producto generados previamente.

   El `Image cache was cleaned` Este mensaje aparece en la parte superior del espacio de trabajo.

1. Borre la caché del explorador.

## Vaciar la caché de JavaScript/CSS

1. En _[!UICONTROL Additional Cache Management]_, borre los archivos JavaScript y CSS que se hayan combinado en un solo archivo haciendo clic en **[!UICONTROL Flush JavaScript/CSS Cache]**.

   El `The JavaScript/CSS cache has been cleaned` Este mensaje aparece en la parte superior del espacio de trabajo.

1. Borre la caché del explorador.

## Vaciar utilizando la línea de comandos

Los administradores del sistema y los desarrolladores con acceso al servidor de aplicaciones de Commerce también pueden administrar la configuración de la caché y la caché desde la línea de comandos utilizando la CLI de Commerce. Consulte [Administrar la caché](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-cache#clean-and-flush-cache-types){:target=&quot;_blank&quot;} en el _Guía de configuración_.

## Controles

| Control | Descripción |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Mass Actions] | Selecciona la casilla de verificación de varias cachés. Opciones: <br/>**[!UICONTROL Select All]**— selecciona la casilla de verificación de todas las cachés.<br/>** Anular selección de todo **— borra la casilla de verificación de todas las cachés.<br/>**[!UICONTROL Select Visible]** — selecciona la casilla de todas las cachés visibles. <br/>**[!UICONTROL Unselect Visible]**— borra la casilla de todas las cachés visibles. |
| [!UICONTROL Actions] | Determina la acción que se aplicará a todas las cachés seleccionadas. Opciones: <br/>**[!UICONTROL Enable]**— activa todas las cachés seleccionadas.<br/>**[!UICONTROL Disable]** — Deshabilita todas las cachés seleccionadas. <br/>**[!UICONTROL Refresh]**— actualiza todas las cachés seleccionadas. |
| [!UICONTROL Submit] | Aplica la acción a todas las cachés seleccionadas. |

{style="table-layout:auto"}

### Botones

| Botón | Descripción |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Flush Magento Cache] | Elimina todos los elementos de la caché de Commerce predeterminada (`var/cache`), según sus etiquetas de comercio asociadas. |
| [!UICONTROL Flush Cache Storage] | Elimina todos los elementos de la caché, independientemente de la etiqueta de comercio. Si el sistema utiliza una ubicación de caché alternativa, los archivos en caché utilizados por otras aplicaciones se eliminan en el proceso. |
| [!UICONTROL Flush Catalog Images Cache] | Elimina todas las imágenes de catálogo almacenadas en, cuyo tamaño y marca de agua se han cambiado automáticamente `media/catalog/product/cache`. Si las imágenes cargadas recientemente no se reflejan en el catálogo, intente vaciar el catálogo y actualizar el explorador. |
| [!UICONTROL Flush JavaScript/CSS Cache] | Elimina la copia combinada de los archivos JavaScript y CSS de la caché. Si los cambios recientes en la hoja de estilo o JavaScript no se reflejan en el almacén, intente vaciar la caché de JavaScript/CSS y actualizar el explorador. |
| [!UICONTROL Flush Static Files Cache] | Elimina los archivos de vista preprocesados y los archivos estáticos. |

{style="table-layout:auto"}

### Cachés

El [!UICONTROL Cache Management] Esta página enumera los tipos de caché que puede administrar desde el Administrador con su estado actual. En esta sección se describen los tipos de caché predeterminados que admite Adobe Commerce. El _Etiqueta de caché_ y _ID de caché_ Las columnas describen los valores utilizados en el código de la aplicación Commerce:

- `cache_type_id` define el identificador único de un tipo de caché.

- `%CACHE_TYPE_TAG%` define la etiqueta única que se utilizará en el ámbito de tipo de caché.

Los desarrolladores e integradores de sistemas utilizan estos valores para configurar y administrar el almacenamiento en caché al personalizar o integrar con Adobe Commerce, por ejemplo desarrollando integraciones mediante las API de GraphQL. El `cache type id` también se utiliza para la administración de caché desde la línea de comandos del servidor de aplicaciones mediante la CLI de Commerce. Por ejemplo, ` bin/magento cache:status config` muestra el estado actual de la caché de configuración.

>[!NOTE]
>
>Los desarrolladores e integradores de sistemas pueden personalizar y ampliar el sistema de administración de caché de Commerce para admitir módulos e integraciones personalizados. Para obtener más información, consulte [Configurar almacenamiento en caché](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cache/caching-overview) en el _Guía de configuración de Adobe Commerce_.

<!-- prettier-ignore -->

#### Detalles de lista de caché

| Caché | Descripción | Etiqueta de caché | ID de caché |
|-------|------------|----------|----------|
| [!UICONTROL Configuration] | Commerce recopila la configuración XML de todos los módulos, la combina y guarda el resultado combinado en la caché.<br>**[!UICONTROL System]**-  `config.xml`,`local.xml`<br>**[!UICONTROL Module]** - `config.xml`<br><br>Esta caché también contiene la configuración específica del almacén almacenada en el sistema de archivos y en la base de datos. Limpie o vacíe este tipo de caché después de modificar los archivos de configuración. | `CONFIG` | `config` |
| [!UICONTROL Layouts] | Diseños de página compilados, es decir, los componentes de diseño de todos los componentes. Limpie o vacíe este tipo de caché después de modificar los archivos de diseño. | `LAYOUT_GENERAL_CACHE_TAG` | `layout` |
| [!UICONTROL Blocks HTML output] | Fragmentos de página del HTML por bloque. Limpie o vacíe este tipo de caché después de modificar la capa de visualización. | `BLOCK_HTML` | `block_html` |
| [!UICONTROL Collections Data] | Recopilar archivos de datos que almacenan los resultados de las consultas de base de datos. Si es necesario, Commerce limpia esta caché automáticamente, pero los desarrolladores de terceros pueden colocar cualquier dato en cualquier segmento de la caché. Limpie o vacíe este tipo de caché si el módulo personalizado utiliza una lógica que genere entradas de caché que Commerce no pueda limpiar. | `COLLECTION_DATA` | `collections` |
| [!UICONTROL Reflections] | Borra los datos de reflexión de la interfaz de API, que generalmente se generan durante el tiempo de ejecución. | `REFLECTION` | `reflection` |
| `Database DDL operations` | Esquema de base de datos. Si es necesario, Commerce limpia esta caché automáticamente, pero los desarrolladores de terceros pueden colocar cualquier dato en cualquier segmento de la caché. Limpie o vacíe este tipo de caché después de realizar cambios personalizados en el esquema de la base de datos. (En otras palabras, estas son actualizaciones que Commerce no se hace a sí mismo). Una forma de actualizar el esquema de la base de datos automáticamente es utilizar la configuración de Magento:db-schema:comando upgrade. | `DB_DDL` | `db_ddl` |
| [!UICONTROL Compiled Config] | Resultados de la compilación del código. | `COMPILED_CONFIG` | `compiled_config` |
| [!UICONTROL Webhooks Response Cache] | Almacena en caché las respuestas a solicitudes de webhook. Para obtener más información, consulte la [Guía de webhooks](https://developer.adobe.com/commerce/extensibility/webhooks/release-notes/#enhancements-2) en la documentación para desarrolladores de Commerce. | `WEBHOOKS_RESPONSE` | `webhooks_response` |
| [!UICONTROL EAV types and attributes] | Almacena en caché la declaración de tipos de entidad para los metadatos relacionados con los atributos de valor de atributo de entidad (EAV). Los atributos incluyen etiquetas de tienda, vínculos a código PHP relacionado, renderización de atributos, ajustes de búsqueda, etc. Normalmente no es necesario limpiar ni vaciar este tipo de caché. | `EAV` | `eav` |
| [!UICONTROL Customer Notification] | Notificaciones temporales que aparecen en la interfaz de usuario. | `CUSTOMER_NOTIFICATION` | `customer_notification` |
| [!UICONTROL GraphQL Query Resolver Results] | Almacena en caché los resultados de las resoluciones de consultas de GraphQL para entidades de cliente, página CMS, bloque CMS y galería de medios de productos. Mantenga esta caché habilitada para mejorar el rendimiento de GraphQL. | `GRAPHQL_QUERY_RESOLVER_RESULT` | `graphql_query_resolver_result` |
| [!UICONTROL Integrations Configuration] | Archivo de configuración de integración. Limpie o vacíe esta caché después de cambiar o agregar integraciones. | `INTEGRATION` | `config_integration` |
| [!UICONTROL Integrations API Configuration] | Configuración de las API de integración compilada para integraciones de tienda. | `INTEGRATION_API_CONFIG` | `config_integration_api` |
| [!UICONTROL Admin UI SDK Cache] | Almacena en caché las personalizaciones para el administrador. Consulte [Configuración y pruebas de administración](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/configuration/) en el _Guía del SDK de IU de administración_. | `ADMIN_UI_SDK` | `admin_ui_sdk` |
| [!UICONTROL Page Cache] | Almacenamiento en caché de página completa. | `FPC` | `full_page` |
| [!UICONTROL Target Rule] | Índice de reglas de Target | `TARGET_RULE` | `target_rule` |
| [!UICONTROL Web Services Configuration] | Almacenamiento en caché de la estructura API web. | `WEBSERVICE` | `config_webservice` |
| [!UICONTROL Translations] | Archivos de traducción. | `TRANSLATE` | `translate` |

{style="table-layout:auto"}

## Almacenamiento en caché de página completa

Adobe Commerce y Magento Open Source utilizan el almacenamiento en caché de página completa en el servidor para mostrar rápidamente las páginas de categoría, producto y CMS. El almacenamiento en caché de páginas completas mejora el tiempo de respuesta y reduce la carga en el servidor. Sin almacenamiento en caché, es posible que cada página necesite ejecutar bloques de código y recuperar información de la base de datos. Sin embargo, con el almacenamiento en caché de página completa habilitado, una página completamente generada se puede leer directamente desde la caché.

>[!NOTE]
>
>Se recomienda que [Caché de barniz](https://varnish-cache.org/){:target=&quot;_blank&quot;} solo se puede usar en entornos de producción.

El contenido en caché se puede utilizar para procesar solicitudes de tipos de visitas similares. Como resultado, las páginas mostradas a un visitante ocasional pueden diferir de las páginas mostradas a un cliente. Con el fin de almacenar en caché, cada visita es de uno de los tres tipos siguientes:

- `Non-sessioned` - Durante una visita sin sesión, el comprador ve las páginas, pero no interactúa con la tienda. El sistema almacena en caché el contenido de cada página visualizada y la sirve a otros compradores sin sesión.
- `Sessioned` : Durante una visita con sesión, a los compradores que interactúan con la tienda se les asigna un ID de sesión. Las interacciones incluyen actividades como comparar productos o agregar productos al carro de compras. Solo ese comprador utiliza las páginas en caché que se generan durante la sesión.
- `Customer` : Las sesiones de clientes se crean para clientes que inician sesión y compran con su cuenta registrada. Durante la sesión, se pueden presentar a los clientes ofertas especiales, promociones y precios según el grupo de clientes asignado.

Para obtener información técnica, consulte [Configurar y utilizar barniz](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/varnish/config-varnish.html){:target=&quot;_blank&quot;} y [Utilice Redis para la página de Commerce y la caché predeterminada](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-pg-cache.html){:target=&quot;_blank&quot;} en el _Guía de configuración_.

**_Para configurar la caché de página completa:_**

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL System]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Full Page Cache]** sección.

   ![Configuración avanzada: caché de página completa](../configuration-reference/advanced/assets/system-full-page-cache.png){width="600" zoomable="yes"}

1. Establecer **[!UICONTROL Caching Application]** a uno de los siguientes:

   - `Built-in Application`
   - `Varnish Caching`

1. Para establecer el tiempo de espera para la caché de la página, introduzca el **[!UICONTROL TTL for public content]**. (El valor predeterminado es `86400`)

1. Para especificar el número máximo de [controladores de diseño](https://developer.adobe.com/commerce/frontend-core/guide/layouts/#layout-handles) para procesar en [`{BASE-URL}/page_cache/block/esi`](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/use-varnish-esi.html) Punto final HTTP, introduzca la **[!UICONTROL Handles param size]**. Restringir el tamaño puede mejorar la seguridad y el rendimiento. (El valor predeterminado es `100`)

1. Si utiliza Barniz, complete el **[!UICONTROL Varnish Configuration]** como sigue:

   - **[!UICONTROL Access list]** : introduzca las direcciones IP que pueden depurar la configuración de Barniz para generar un archivo de configuración. Separe las distintas entradas con comas. El valor predeterminado es `localhost`.

   - **[!UICONTROL Backend host]** : introduzca la dirección IP del host back-end que genera los archivos de configuración. El valor predeterminado es `localhost`.

   - **[!UICONTROL Backend port]** : identifique el puerto back-end que se utiliza para generar archivos de configuración. El valor predeterminado es: `8080`.

   - **[!UICONTROL Grace period]** : especifique el número de segundos que se utilizarán como periodo de gracia para generar archivos de configuración. Consulte [Configuración avanzada de barniz](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/config-varnish-advanced.html) en el _Guía de configuración_.

   - Para exportar la configuración como `varnish.vcl` , haga clic en el botón correspondiente a la versión de Barniz que utilice.

   ![Configuración avanzada: barniz de caché de página completa](../configuration-reference/advanced/assets/system-full-page-cache-varnish.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.
