---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Catalog]'
description: Revise la configuración en la página [!UICONTROL Catalog] &gt; [!UICONTROL Catalog] del administrador de Commerce.
exl-id: fc25ae80-aaa7-42c4-bba2-f03d3caa7970
feature: Configuration, Catalog Management
source-git-commit: 20f97d6ab391b7f5675d6790ab2ec5d24e9dda21
workflow-type: tm+mt
source-wordcount: '3261'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Catalog]

{{config}}

## [!UICONTROL Product Fields Auto-Generation]

![Generación automática de campos de producto](./assets/catalog-product-fields-auto-generation.png)<!-- zoom -->

<!-- [Product Fields Auto-Generation](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/product-workspace#default-field-values) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Mask for SKU] | Global | Determina el valor predeterminado del campo SKU en función de los valores de marcador de posición de otros campos y cualquier texto adicional introducido. Marcador de posición predeterminado: <br/>Nombre de producto: `{{name}}` |
| [!UICONTROL Mask for Meta Title] | Global | Determina el valor predeterminado del campo MetaTitle en función de los valores de marcador de posición de otros campos y del texto adicional que se escriba. Marcador de posición predeterminado: <br/>Nombre de producto: `{{name}}` |
| [!UICONTROL Mask for Meta Keywords] | Global | Determina el valor predeterminado del campo _Meta Keywords_ en función de los valores de marcador de posición de otros campos y cualquier texto adicional que se escriba. Marcador de posición predeterminado: <br/>Nombre de producto: `{{name}}` |
| [!UICONTROL Mask for Meta Description] | Global | Determina el valor predeterminado del campo Meta descripción en función de los valores de marcador de posición de otros campos y cualquier texto adicional que se introduzca. Marcador de posición predeterminado: <br/>Nombre del producto - `{{name}}` <br/>Descripción - `{{description}}` |

{style="table-layout:auto"}

## [!UICONTROL Product Reviews]

![Críticas de productos](./assets/catalog-product-reviews.png)<!-- zoom -->

<!-- [Product Reviews](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/product-reviews/product-reviews) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enabled] | Vista de tienda | Habilita las críticas de producto. Opciones: `Yes` / `No` |
| [!UICONTROL Allow Guests to Write Reviews] | Sitio web | Determina si los clientes deben abrir una cuenta en la tienda para poder escribir críticas de productos. |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![Tienda](./assets/catalog-storefront.png)<!-- zoom -->

<!-- [Storefront](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/navigation/navigation-product-listings) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL List Mode] | Vista de tienda | Determina el formato de la lista de resultados de búsqueda. Opciones: <br/>**`Grid Only`**- Da formato a la lista como una cuadrícula de filas y columnas. Cada producto aparece en una sola celda de la cuadrícula.<br/>**`List Only`**: da formato a la lista con cada producto en una fila independiente. <br/>**`Grid (default / List)`**: de forma predeterminada, los productos aparecen en la vista Cuadrícula y se pueden cambiar a la vista Lista.<br/>**`List (default / Grid)`**: de forma predeterminada, los productos aparecen en la vista de lista y se pueden cambiar a la vista de cuadrícula. |
| [!UICONTROL Products per Page on Grid Allowed Values] | Vista de tienda | Determina el número de productos mostrados en la vista de cuadrícula. Para proporcionar una selección de opciones, introduzca varios valores separados por comas. |
| [!UICONTROL Products per Page on Grid Default Value] | Vista de tienda | Determina el número de productos mostrados por página de forma predeterminada en la vista de cuadrícula. |
| [!UICONTROL Products per Page on List Allowed Values] | Vista de tienda | Determina el número de productos mostrados en la vista de lista. Para proporcionar una selección de opciones, introduzca varios valores separados por comas. |
| [!UICONTROL Products per Page on List Default Value] | Vista de tienda | Determina el número de productos mostrados por página de forma predeterminada en la vista de lista. |
| Lista de productos Ordenar por | Vista de tienda | Determina el criterio de ordenación de la lista de resultados de búsqueda. La selección de opciones está determinada por la Configuración de visualización de la categoría y los atributos disponibles que se han establecido en `Used for Sorting in Product Listing`. El valor predeterminado es `Use All Available Attributes` y generalmente incluye Mejor valor, Nombre y Precio. Esta configuración no se aplica al [!DNL Live Search] [widget de página de lista de productos](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Allow All Products per Page] | Vista de tienda | Si se establece en `Yes`, incluye la opción `ALL` en el control &quot;Mostrar por página&quot;. |
| [!UICONTROL Remember Category Pagination] | Global | Si se establece en `Yes`, los valores de paginación de categoría actuales se guardan cuando los clientes navegan de una categoría a otra en [listados de productos](../../catalog/navigation-product-listings.md). Guardar el valor utiliza más almacenamiento en caché y puede afectar a la forma en que los motores de búsqueda indexan las páginas. Opciones: `Yes` / `No` (predeterminado) |
| [!UICONTROL Use Flat Catalog Category] | Global | Habilita la [estructura de categoría plana](../../catalog/catalog-flat.md) (no se recomienda). Opciones: `Yes` / `No` |
| [!UICONTROL Use Flat Catalog Product] | Global | Habilita la estructura de producto plana. (no recomendado) Opciones: `Yes` / `No` |
| [!UICONTROL Swatches per Product] | Vista de tienda | Determina el número de muestras disponibles para cada producto. Predeterminado: `16` |
| [!UICONTROL Show Swatches in Product List] | Vista de tienda | Determina si las muestras aparecen en la lista de productos. Opciones: `Yes` / `No` |
| [!UICONTROL Show Swatch Tooltip] | Vista de tienda | Determina si aparece la información de objeto de la muestra. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Alerts]

![Alertas de producto](./assets/catalog-product-alerts.png)<!-- zoom -->

<!-- [Product Alerts](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/product-alerts/alert-setup) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Allow Alerts When Product Price Changes] | Vista de tienda | Determina si hay alertas por correo electrónico disponibles para los cambios de precio del producto. Opciones: `Yes` / `No` |
| [!UICONTROL Price Alert Email Template] | Vista de tienda | Identifica la plantilla que se usa para las alertas de correo electrónico de cambio de precio de productos. Plantilla predeterminada: `Product price alert` |
| [!UICONTROL Allow Alert When Product Comes Back in Stock] | Sitio web | Determina si los clientes pueden optar por recibir una alerta cuando el producto vuelva a estar disponible. Opciones: `Yes` / `No` |
| [!UICONTROL Stock Alert Email Template] | Vista de tienda | Identifica la plantilla que se utiliza para las notificaciones por correo electrónico de alertas de stock. Plantilla predeterminada: `Product stock alert` |
| [!UICONTROL Alert Email Sender] | Vista de tienda | Determina el contacto de la tienda que aparece como el remitente del mensaje de correo electrónico de alerta del producto. Opciones: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email` |

{style="table-layout:auto"}

## [!UICONTROL Product Alerts Run Settings]

![Configuración de ejecución de alertas de producto](./assets/catalog-product-alerts-run-settings.png)<!-- zoom -->

<!-- [Product Alerts Run Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/product-alerts/alert-setup) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Frequency] | Global | Elija la frecuencia con la que se envían las alertas de productos. Opciones: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Start Time] | Global | Elija a qué hora del día se inicia el proceso de alerta de producto. Este tiempo debe ser posterior a cualquier actualización de precio o inventario. |
| [!UICONTROL Error Email Recipient] | Global | Identifique la dirección de correo electrónico de la persona (normalmente un administrador de tienda) que debe recibir una notificación por correo electrónico cuando se produce un error en el proceso de alerta de producto. |
| [!UICONTROL Error Email Sender] | Global | Seleccione la función con la que el correo electrónico es `from`. |
| [!UICONTROL Error Email Template] | Global | Seleccione la plantilla de correo electrónico que se utilizará para las notificaciones de error de alertas de producto. |

{style="table-layout:auto"}

## [!UICONTROL Product Image Placeholders]

![Marcadores de posición de imagen del producto](./assets/catalog-product-image-placeholders.png)<!-- zoom -->

<!-- [Product Image Placeholders](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/digital-assets/product-image-config#image-placeholders) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Base Image] | Vista de tienda | Identifica el archivo de marcador de posición elegido para la imagen base. |
| [!UICONTROL Small Image] | Vista de tienda | Identifica el archivo de marcador de posición elegido para la imagen pequeña. |
| [!UICONTROL Swatch] | Vista de tienda | Identifica el archivo de marcador de posición elegido para la muestra. |
| [!UICONTROL Thumbnail] | Vista de tienda | Identifica el archivo de marcador de posición elegido para la miniatura. |
| [!UICONTROL Choose File] |  | Se desplaza al archivo y lo sube como imagen de marcador de posición para el tipo. |

{style="table-layout:auto"}

## [!UICONTROL Recently Viewed/Compared Products]

![Productos vistos/comparados recientemente](./assets/catalog-recently-viewed-and-compared-products.png)<!-- zoom -->

<!-- Recently Viewed/Compared Products](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/shopper-tools/products-viewed-compared) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Synchronize widget products with backend storage] | Global | Determina la sincronización de la información del widget de productos, como el ID de productos, con la base de datos. Esto permite reutilizar la información en otros dispositivos. |
| [!UICONTROL Show for Current] | Sitio web | Limita los productos mostrados al sitio web actual. Opciones: `Website` / `Store` / `Store View` |
| [!UICONTROL Default Recently Viewed Products Count] | Vista de tienda | Determina el número máximo de productos visualizados recientemente que aparecen en la lista. |
| [!UICONTROL Default Recently Compared Products Count] | Vista de tienda | Determina el número máximo de productos comparados recientemente que aparecen en la lista. |
| [!UICONTROL Lifetime of products in Recently Viewed Widget] | Global | Determina cuánto tiempo, en segundos, se muestran los productos visualizados en la lista visualizada recientemente. |
| [!UICONTROL Lifetime of products in Recently Compared Widget] | Global | Determina cuánto tiempo, en segundos, se muestran los productos comparados en la lista comparados recientemente. |

{style="table-layout:auto"}

## [!UICONTROL Product Video]

![Vídeos del producto](./assets/catalog-product-video.png)<!-- zoom -->

<!-- [Product Videos](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/digital-assets/product-video) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL YouTube API key] | Vista de tienda | Especifica la clave de API necesaria para conectarse al servidor de YouTube. |
| [!UICONTROL Autostart base video] | Vista de tienda | Para iniciar automáticamente el vídeo después de que se cargue la página, establezca en `Yes`. |
| [!UICONTROL Show related video] | Vista de tienda | Para mostrar vídeos relacionados, establézcalo en `Yes`. |
| [!UICONTROL Auto restart video] | Vista de tienda | Para habilitar la reproducción automática del vídeo, establezca en `Yes`. |

{style="table-layout:auto"}

## [!UICONTROL Price]

![Precio](./assets/catalog-price.png)<!-- zoom -->

<!--Price](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/pricing/catalog-price-scope) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Catalog Price Scope] | Global | Determina el ámbito de la moneda base. Opciones: `Global` / `Website` |
| [!UICONTROL Default Product Price] | Global | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) Define el precio predeterminado del producto, si corresponde. |

{style="table-layout:auto"}

## [!UICONTROL Layered Navigation]

>[!NOTE]
>
>La configuración de búsqueda estándar descrita en esta sección difiere para [Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html).

<!-- [Layered Navigation - Automatic (equalize price ranges)](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/navigation/navigation-layered#configure-layered-navigation) -->

![Navegación por capas - Automática (igualar intervalos de precios)](./assets/layered-navigation-equalize-price-range.png)<!-- zoom -->

![Navegación por capas - Automática (igualar recuentos de productos)](./assets/layered-navigation-equalize-product-counts.png)<!-- zoom -->

![Navegación por capas - Manual](./assets/layered-navigation-manual.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Display Product Count] | Vista de tienda | Determina si el recuento de productos aparece después de cada atributo, intervalo de precios y categoría. Opciones: `Yes` / `No` |
| [!UICONTROL Price Navigation Step Calculation] | Vista de tienda | Determina el método usado para determinar el [paso de navegación de precios](../../catalog/navigation-layered.md#configure-price-navigation)). Opciones: <br/>`Automatic (equalize price ranges)` - Basa el cálculo en el rango de precios de los productos del grupo. <br/>`Automatic (equalize product counts)` - Basa el cálculo en el número de productos del grupo. Establece un umbral para el número mínimo de productos en el grupo, para evitar que se dividan en grupos más pequeños. <br/>`Manual`: utiliza el límite de división que ha especificado para los intervalos de precios. |
| [!UICONTROL Default Price Navigation Step] | Vista de tienda | Determina el número de productos que se incluyen en cada paso. |
| [!UICONTROL Maximum Number of Price Intervals] | Vista de tienda | Establece un límite para el número de intervalos de precios que aparecen en la navegación por capas. |

{style="table-layout:auto"}

## [!UICONTROL Category Permissions]

{{ee-feature}}

![Permisos de categoría](./assets/catalog-category-permissions.png)<!-- zoom -->

<!-- [Category Permissions](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/categories/category-permissions) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable] | Global | Activa las restricciones de categoría. De forma predeterminada, el uso de esta función restringe todas las categorías. Opciones: `Yes` / `No` |
| [!UICONTROL Allow Browsing Category] | Sitio web | Determina quién puede examinar las categorías. Opciones: <br/>`Yes, for Everyone`: permite a todos los visitantes y clientes examinar la categoría. <br/>`Yes, for Specified Customer Groups`: permite que solo los miembros de los grupos de clientes seleccionados examinen la categoría. <br/>`No, Redirect to Landing Page`: deniega el acceso a la categoría y redirige a la página seleccionada. |
| [!UICONTROL Display Product Prices] | Sitio web | Controla la visualización de los precios del producto para la categoría. Opciones: <br/>`Yes, for Everyone`: permite que todos vean el precio de los productos de la categoría. <br/>`Yes, for Specified Customer Groups` - Permite que solamente los miembros de los grupos de clientes seleccionados vean el precio de los productos en la categoría. <br/>`No`: desactiva la visualización de los precios de productos para la categoría. |
| [!UICONTROL Allow Adding to Cart] | Sitio web | Determina quién puede comprar productos de la categoría. Opciones: <br/>`Yes, for Everyone`: permite a todos colocar productos de la categoría en sus carros de compras. <br/>`Yes, for Specified Customer Groups`: permite que solo los miembros de los grupos de clientes seleccionados coloquen productos de la categoría en sus carros de compras. <br/>`No`: no permite que nadie coloque productos de la categoría en sus carros de compras. |
| [!UICONTROL Disallow Catalog Search by] | Sitio web | Identifica los grupos de clientes a los que no se les permite buscar productos en la categoría. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Optimization]

![Optimización del motor de búsqueda](./assets/catalog-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/settings/product-search-engine-optimization) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Popular Search Terms] | Vista de tienda | Determina si _Términos de búsqueda populares_ se han implementado en el almacén. Esta configuración no se aplica a las tiendas que usan [Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html). Opciones: `Enable` / `Disable` |
| [!UICONTROL Product URL Suffix] | Vista de tienda | Determina si se aplica un sufijo, como html o htm, a las direcciones URL del producto. Si se utiliza, no incluya un punto antes del sufijo, ya que se aplica automáticamente. |
| [!UICONTROL Category URL Suffix] | Vista de tienda | Determina si se aplica un sufijo, como html o htm, a las direcciones URL de categoría. Si se utiliza, no incluya un punto antes del sufijo, ya que se aplica automáticamente. |
| [!UICONTROL Use Categories Path for Product URLs] | Vista de tienda | Determina si las rutas de categoría se incluyen en las direcciones URL de los productos en la tienda. Si lo hace, varias direcciones URL apuntarán a la misma página, lo que podría afectar a la clasificación de búsqueda. Para obtener más información, consulte [metaetiqueta canónica](../../merchandising-promotions/meta-data.md#canonical-meta-tag). |
| [!UICONTROL Create Permanent Redirect for URLs if URL Key Changed] | Vista de tienda | Determina si se crea automáticamente una redirección permanente cada vez que cambia una clave URL. Cuando se implementa, la casilla de verificación Crear redireccionamiento personalizado para la URL antigua debajo del campo Clave de URL del producto está seleccionada de forma predeterminada. Opciones: `Yes` / `No` |
| [!UICONTROL Generate "category/product" URL Rewrites] | Global | Determina si Adobe Commerce genera datos y los guarda en tablas de reescritura cuando un usuario guarda una categoría que contiene muchos productos asignados.  <br/><br/>Cambiar esta opción no afecta a la forma en que se resuelven las direcciones URL de productos en Adobe Commerce, ya que el sistema resuelve automáticamente las direcciones URL de productos independientemente de esta configuración. <br/><br/>Opciones: `Yes` / `No` <br/><br/>**_Importante:_**Guardar estos datos generados en una tabla de reescrituras de URL puede degradar el rendimiento. Consulte [Redirecciones automáticas de productos](../../merchandising-promotions/url-redirect-product-automatic.md) para obtener más información. |
| [!UICONTROL Apply transliteration for product URL] | Vista de tienda | Determina si se aplica la transliteración al crear o actualizar direcciones URL de productos. Opciones: `Yes` / `No`. El valor predeterminado es `Yes`. <br/><br/>En determinados casos de uso, debe deshabilitar la transliteración. Por ejemplo, si tiene una tienda en línea en chino, las prácticas recomendadas de SEO recomiendan que las direcciones URL de los productos coincidan con el nombre del producto. Al establecer la opción en `No`, se pueden usar caracteres chinos en las direcciones URL del producto en lugar de un equivalente ASCII. |
| [!UICONTROL Page Title Separator] | Vista de tienda | Identifica el carácter que separa el nombre de categoría y la subcategoría en la barra de título del explorador. |
| [!UICONTROL Use Canonical Link Meta Tag for Categories] | Vista de tienda | Si hay varias direcciones URL que apuntan a la misma página de categoría, esta opción utiliza una metaetiqueta canónica para identificar la dirección URL de categoría que los motores de búsqueda deben indexar. La dirección URL incluye un nombre completo para la categoría mediante la etiqueta meta. Esto reduce el contenido duplicado y mejora la SEO. Opciones: `Yes` / `No` |
| [!UICONTROL Use Canonical Link Meta Tag for Products] | Vista de tienda | Si hay varias direcciones URL que apuntan a la misma página de producto, esta opción utiliza una metaetiqueta canónica para identificar la dirección URL del producto que los motores de búsqueda deben indexar. La dirección URL incluye un nombre completo para el producto mediante la etiqueta meta. Esto reduce el contenido duplicado y mejora la SEO. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Category Top Navigation]

![Navegación superior por categorías](./assets/catalog-category-top-navigation.png)<!-- zoom -->

<!-- Category Top Navigation](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/navigation/navigation-top) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Maximal Depth] | Global | Determina el número de niveles de subcategoría en la navegación superior. El valor predeterminado de `0` no impone ningún límite al número de niveles. |

{style="table-layout:auto"}

## [!UICONTROL Catalog Search]

Puede configurar la búsqueda en el catálogo utilizando [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html) o los servicios de motor de búsqueda de terceros compatibles con Adobe Commerce. Siga las instrucciones de instalación.

### Adobe Commerce con [!DNL Live Search]

Cuando Live Search está instalado, la búsqueda en el catálogo incluye las siguientes opciones de configuración:

![Búsqueda en el catálogo de Live Search](./assets/catalog-search-live-search.png)<!-- zoom -->

<!-- [Catalog Search for Live Search](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/search/search-configuration) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Minimal Query Length] | Vista de tienda | Número mínimo de caracteres permitidos en una búsqueda en el catálogo. El valor establecido para esta opción debe ser compatible con el rango correspondiente establecido en las configuraciones del motor de búsqueda de Elasticsearch. Por ejemplo, si establece este valor en `2` en Adobe Commerce, actualice el valor en el motor de búsqueda. |
| [!UICONTROL Maximum Query Length] | Vista de tienda | Número máximo de caracteres permitidos en una búsqueda en el catálogo. El valor establecido para esta opción debe ser compatible con el rango correspondiente establecido en las configuraciones del motor de búsqueda de Elasticsearch. Por ejemplo, si establece este valor en 300 en Adobe Commerce, actualice el valor en el motor de búsqueda. |
| [!UICONTROL Number of top search results to cache] | Vista de tienda | El número de términos de búsqueda y resultados populares que se almacenarán en caché para obtener respuestas más rápidas. Si se introduce un valor de `0`, se almacenarán en la memoria caché todos los términos de búsqueda y resultados cuando se introduzcan por segunda vez. Valor predeterminado: `100` |
| [!UICONTROL Autocomplete Limit] | Vista de tienda | Determina el número máximo de líneas disponibles en la página [ventana emergente de tienda]. El valor predeterminado se puede cambiar cuando Live Search está instalado y actualizar más tarde cambiando esta configuración. Valor predeterminado: `8` |

{style="table-layout:auto"}

### Motores de búsqueda de terceros

Adobe Commerce es compatible con OpenSearch y Elasticsearch. Las versiones de Adobe Commerce 2.3.7-p3, 2.4.3-p2 y 2.4.4 y posteriores admiten el servicio OpenSearch. Elasticsearch 7.11 y versiones posteriores no son compatibles con Adobe Commerce en proyectos de infraestructura en la nube. Elasticsearch sigue siendo compatible con las instalaciones locales.

>[!IMPORTANT]
>
>- Debido al anuncio de fin de soporte de Elasticsearch 7 para agosto de 2023, Adobe recomienda que todos los clientes de Adobe Commerce migren al motor de búsqueda OpenSearch 2.x. Para obtener información sobre cómo migrar el motor de búsqueda durante una actualización, consulte [Migración a OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) en la _Guía de actualización_.
>- En las versiones 2.4.4 y 2.4.3-p2, todos los campos etiquetados como Elasticsearch también se aplican a OpenSearch. Cuando se introdujo la compatibilidad con Elasticsearch 8.x en la versión 2.4.6, se crearon nuevas etiquetas para distinguir entre las configuraciones de Elasticsearch y OpenSearch. Sin embargo, las opciones de configuración para ambos son las mismas.

![Opciones de configuración de búsqueda en el catálogo](./assets/catalog-search-opensearch.png){zoomable="yes"}

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Minimal Query Length] | Vista de tienda | Número mínimo de caracteres permitidos en una búsqueda en el catálogo. El valor establecido para esta opción debe ser compatible con el rango correspondiente establecido en la configuración de OpenSearch o Elasticsearch. Por ejemplo, si establece este valor en `2` en Adobe Commerce, también debe actualizar el valor en la configuración del motor de búsqueda. Valor predeterminado: `3` |
| [!UICONTROL Maximum Query Length] | Vista de tienda | Número máximo de caracteres permitidos en una búsqueda en el catálogo. El valor establecido para esta opción debe ser compatible con el rango correspondiente establecido en la configuración de OpenSearch o Elasticsearch. Por ejemplo, si establece este valor en `300` en Adobe Commerce, debe actualizar el valor en la configuración del motor de búsqueda. Valor predeterminado: `128` |
| [!UICONTROL Number of top search results to cache] | Vista de tienda | El número de términos de búsqueda y resultados populares que se almacenarán en caché para obtener respuestas más rápidas. Si se introduce un valor de `0`, se almacenarán en la memoria caché todos los términos de búsqueda y resultados cuando se introduzcan por segunda vez. Valor predeterminado: `100` |
| [!UICONTROL Enable EAV Indexer] | Global | Determina si se habilita o deshabilita el indizador EAV del producto. Esta función mejora la velocidad de indexación y restringe el uso del indexador por extensiones de terceros. Opción predeterminada: `Yes` para habilitado |
| [!UICONTROL Autocomplete Limit] | Vista de tienda | Número máximo de consultas de búsqueda que se mostrarán debajo del campo de búsqueda para autocompletar búsqueda. Restringir esta cantidad aumenta el rendimiento de las búsquedas y reduce el tamaño de la lista mostrada. Valor predeterminado: `8` |
| Motor de búsqueda | Global | Identifica el motor de búsqueda necesario para procesar las solicitudes de datos de catálogo. Las opciones de configuración del motor de búsqueda son las mismas para OpenSearch y Elasticsearch. Opciones: `OpenSearch` o `Elasticsearch` |
| [!UICONTROL OpenSearch Server Hostname] | Global | Especifica el nombre del servidor host OpenSearch o Elasticsearch. |
| [!UICONTROL OpenSearch Server Port] | Global | Especifica el número del puerto del servidor utilizado por OpenSearch o Elasticsearch. Valor predeterminado: `9200` |
| [!UICONTROL OpenSearch Index Prefix] | Global | Asigna un prefijo para identificar el índice de OpenSearch o Elasticsearch. Valor predeterminado: `magento2` |
| [!UICONTROL Enable OpenSearch HTTP Auth] | Global | Si está habilitado, utiliza la autenticación HTTP para solicitar un nombre de usuario y una contraseña antes de acceder al servidor de OpenSearch o Elasticsearch. Opciones: `Yes` / `No` |
| [!UICONTROL OpenSearch HTTP Username] | Global | Cuando _Habilitar autenticación HTTP de Elasticsearch_ está establecido en `Yes`, especifica el nombre de usuario para la autenticación HTTP de OpenSearch o Elasticsearch. |
| [!UICONTROL OpenSearch HTTP Password] | Global | Cuando _Habilitar autenticación HTTP de Elasticsearch_ está establecido en `Yes`, especifica la contraseña para la autenticación HTTP de OpenSearch o Elasticsearch. |
| [!UICONTROL OpenSearch Server Timeout] | Global | Determina el número de segundos antes de que se agote el tiempo de espera de una solicitud al servidor OpenSearch o Elasticsearch. Valor predeterminado: `15` |
| [!UICONTROL Test Connection] |  | Valida la conexión de OpenSearch o Elasticsearch. |
| [!UICONTROL Enable Search Recommendations] | Vista de tienda | Determina si se ofrecen recomendaciones de búsqueda cuando una búsqueda no devuelve resultados y aparece en la sección `Related search terms` de la página de resultados de búsqueda. Opciones: `Yes` / `No` <br/>Cuando se establece en Yes, se muestran opciones adicionales para _[!UICONTROL Search Recommendations Count]_y_[!UICONTROL Shows Results Count for Each Recommendation]_. |
| [!UICONTROL Search Recommendations Count] | Vista de tienda | Especifica el número de términos de búsqueda ofrecidos como recomendaciones. De forma predeterminada, no se muestran más de cinco. |
| [!UICONTROL Show Results Count for Each Recommendation] | Vista de tienda | Cuando se establece en `Yes`, el número de productos encontrados para la recomendación de búsqueda propuesta se muestra entre corchetes. Opciones: `Yes` / `No` |
| [!UICONTROL Enable Search Suggestions] | Vista de tienda | Determina si aparecen sugerencias de búsqueda para errores ortográficos comunes. Cuando está habilitada, se ofrecen sugerencias de búsqueda para cualquier solicitud que no devuelva resultados y que aparezca en la sección `Did you mean` de la página **Resultados de búsqueda**. Las sugerencias de búsqueda pueden afectar al rendimiento de la búsqueda. Cuando se establece en `Yes`, se muestran opciones adicionales para Habilitar recomendaciones de búsqueda y campos asociados. Opciones: `Yes` / `No` |
| [!UICONTROL Search Suggestions Count] | Vista de tienda | Determina el número de sugerencias de búsqueda que se ofrecen. Por ejemplo: `2` |
| [!UICONTROL Show Results Count for Each Suggestion] | Vista de tienda | Determina si se muestra el número de resultados de búsqueda para cada sugerencia. Según el tema, el número suele aparecer entre corchetes después de la sugerencia. Opciones: `Yes` / `No` |
| [!UICONTROL Minimum Terms to Match] | Vista de tienda | Especifica un valor que corresponde al número de términos de la consulta con el que deben coincidir los resultados de la búsqueda para que se devuelvan. Esto garantiza una relevancia óptima de los resultados para los compradores. Los valores porcentuales se correlacionan con un número y, si es necesario, se redondean hacia abajo y se utilizan como el número mínimo de términos que deben coincidir en la consulta. El valor puede ser un entero negativo o positivo, un porcentaje negativo o positivo, una combinación de los dos o varias combinaciones. Para obtener más información, consulte [minimum_should_match_parameter](https://opensearch.org/docs/latest/query-dsl/minimum-should-match/) en la documentación de OpenSearch. |

## [!UICONTROL Downloadable Product Options]

![Opciones de producto descargables](./assets/catalog-downloadable-product-options.png)<!-- zoom -->

<!-- [Downloadable Product Options](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/types/product-create-downloadable#configure-the-download-options) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Order Item Status to Enable Downloads] | Sitio web | Determina el estado de un pedido antes de que las descargas estén disponibles. Opciones: `Pending` / `Invoiced` |
| [!UICONTROL Default Maximum Number of Downloads] | Sitio web | Determina el número predeterminado de descargas disponibles para un cliente. |
| [!UICONTROL Shareable] | Sitio web | Determina si los clientes deben iniciar sesión en sus cuentas para acceder al vínculo de descarga. Opciones: <br/>**Sí**: permite enviar el vínculo por correo electrónico, que luego se puede compartir con otros usuarios. <br/>**No**: requiere que los clientes inicien sesión en sus cuentas para acceder al vínculo de descarga. |
| [!UICONTROL Default Sample Title] | Vista de tienda | Título predeterminado para todos los archivos de ejemplo. |
| [!UICONTROL Default Link Title] | Vista de tienda | El vínculo predeterminado para todos los títulos descargables. |
| [!UICONTROL Opens Links in New Window] | Sitio web | Determina si el vínculo de descarga se abre en una nueva ventana del explorador. Opciones: `Yes` / `No` |
| [!UICONTROL Use Content Disposition] | Vista de tienda | Determina cómo se envía el vínculo al contenido descargable, como datos adjuntos de correo electrónico o como vínculo en línea en una ventana del explorador. Opciones: <br/>**`Attachment`**: el vínculo de descarga se entrega como archivo adjunto de correo electrónico.<br/>**`Inline`**: el vínculo de descarga se entrega como un vínculo en línea en una página web. |
| [!UICONTROL Disable Guest Checkout if Cart Contains Downloadable Items] | Sitio web | Determina si los invitados que compran productos descargables deben registrarse para obtener una cuenta e iniciar sesión para completar el proceso de cierre de compra. Opciones: <br/>**`Yes`**: si el carro contiene productos descargables, el invitado debe registrarse para obtener una cuenta o iniciar sesión en una cuenta existente para completar la compra.<br/>**`No`**: el vínculo de descarga se entrega como un vínculo en línea en el cuerpo del mensaje de correo electrónico.  <br/> _**Nota:**_ El cierre de compra de invitado solo está disponible para productos de descarga si Compartible está establecido en `Yes`. |

{style="table-layout:auto"}

## [!UICONTROL Date & Time Custom Options]

![Opciones personalizadas de fecha y hora](./assets/catalog-date-time-custom-options.png)<!-- zoom -->

<!-- Date & Time Custom Options](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/product-attributes/attributes-input-types#date-and-time-options) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Use JavaScript Calendar] | Vista de tienda | Determina si el calendario de JavaScript se utiliza como control de entrada para los campos de fecha. Opciones: `Yes` / `No` <br/>Si se establece en `No`, aparecerá una lista desplegable independiente para cada parte del campo de fecha. |
| [!UICONTROL Date Fields Order] | Vista de tienda | Establece el orden de los tres campos de fecha. Opciones: `Day` / `Month` / `Year` |
| [!UICONTROL Time Format] | Vista de tienda | Establece el formato de hora en un reloj de 12 o 24 horas. Opciones: `12h AM/PM` / `24h` |
| [!UICONTROL Year Range] | Vista de tienda | Define el intervalo de años inicial y final que aparecen en el campo _Year_. El valor debe introducirse en formato AAAA. |

{style="table-layout:auto"}

## [!UICONTROL Catalog Events]

{{ee-feature}}

![Eventos de catálogo](./assets/catalog-events.png)<!-- zoom -->

<!-- [Catalog Events](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/events/events-private-sales) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable Catalog Events Functionality] | Sitio web | Determina si el módulo Eventos está habilitado. |
| [!UICONTROL Enable Catalog Event Widget on Frontend] | Vista de tienda | Determina si el widget de evento está disponible en la tienda. Este es un bloque estático con información sobre los eventos del sitio. |
| [!UICONTROL Number of Events to be Displayed in the Event Slider Widget] | Vista de tienda | Determina el número de eventos que aparecen en el widget de deslizador de eventos de las páginas de categorías. Para invalidar, use la variable `limit="x"`. |
| [!UICONTROL Events to Scroll per Click in Event Slider Widget] | Vista de tienda | Determina el número de eventos que aparecen en el widget de deslizador de eventos de las páginas de CMS como, por ejemplo, la página de inicio. Para invalidar, use la variable `scroll="x"`. |

{style="table-layout:auto"}

## [!UICONTROL Rule-Based Product Relations]

{{ee-feature}}

![Relaciones de producto basadas en reglas](./assets/catalog-rule-based-product-relations.png)<!-- zoom -->

<!-- [Rule-Based Product Relations](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Maximum Number of Products in Related Products List] | Global | Determina el número máximo de productos que pueden aparecer en la lista _Productos relacionados_. |
| [!UICONTROL Show Related Products] | Global | Determina qué lista de productos relacionados aparece en la tienda. Puede ser la lista seleccionada manualmente en Información del producto, la lista generada en respuesta a una regla de relación de productos o una combinación de ambas. Opciones: `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Related Products List] | Global | Determina el orden en que aparecen los productos de la lista _Productos relacionados_. Opciones: `Do not rotate` / `Shuffle` |
| [!UICONTROL Maximum Number of Products in Cross-Sell Product List] | Global | Determina el número máximo de productos que pueden aparecer en la lista de venta cruzada. |
| [!UICONTROL Show Cross-Sell Products] | Global | Determina qué lista de productos de venta cruzada aparece en la tienda. Puede ser la lista seleccionada manualmente en Información del producto, la lista generada en respuesta a una regla de relación de productos o una combinación de ambas. Opciones: `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Cross-Sell Products List] | Global | Determina el orden en que aparecen los productos en la lista Productos de venta cruzada. Opciones: no girar / mezclar |
| [!UICONTROL Maximum Number of Products in Upsell Product List] | Global | Determina el número máximo de productos que pueden aparecer en la lista _Ampliar venta de productos_. |
| [!UICONTROL Show Upsell Products] | Global | Determina qué lista de productos de mejora de ventas aparece en la tienda. Puede ser la lista seleccionada manualmente en Información del producto, la lista generada en respuesta a una regla de relación de productos o una combinación de ambas. Opciones: `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Upsell Product List] | Global | Determina el orden en que aparecen los productos en la lista Ampliar venta de productos. Opciones: `Do not rotate` / `Shuffle` |

{style="table-layout:auto"}
