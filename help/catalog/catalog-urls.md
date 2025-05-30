---
title: Direcciones URL del catálogo y del producto
description: Obtenga información sobre los tipos de formato de URL de los productos de catálogo y cómo configurarlos.
exl-id: 47405dc6-9b5e-4ca8-87eb-5a222de40793
feature: Catalog Management, Products, Search, Categories
source-git-commit: 1edab49fd8d52a1b7414eb207a21c5c03200e75e
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 0%

---

# Direcciones URL del catálogo y del producto

Las direcciones URL que asigna a productos y categorías desempeñan un papel importante a la hora de determinar el grado de indexación del sitio por parte de los motores de búsqueda. Antes de empezar a crear el catálogo, tenga en cuenta las opciones disponibles. Para ver el formato de URL actual, vaya a la tienda y navegue hasta cualquier producto del catálogo. El formato de la dirección URL depende de la configuración actual y del método que utilice para encontrar la página.

## Formatos de URL

### URL dinámica

Se crea una dirección URL dinámica _sobre la marcha_ que puede incluir una cadena de consulta con variables para el identificador del producto, el criterio de ordenación y la página donde se realizó la solicitud. Cuando un cliente busca un producto en su tienda, la URL resultante puede tener un aspecto similar al siguiente:

- `http://mystore.com/catalogsearch/result/?q=racer+back`
- `http://mystore.com/women/tops-women.html?style_general=135`

### URL estática

Una dirección URL estática es una dirección fija para una página específica. Se puede mostrar una dirección URL estática en un formato compatible con el motor de búsqueda o en una que haga referencia a productos y categorías por ID. Estas direcciones URL incluyen palabras que las personas pueden utilizar para buscar un producto y requieren que se habiliten las reescrituras de servidores web. Los archivos con direcciones URL estáticas se utilizan habitualmente para páginas de productos y categorías, páginas de contenido y [recursos de temas](../content-design/theme-assets.md).

- `http://mystore.com/antonia-racer-tank.html`

## Componentes de URL

### Clave de URL

La clave URL es la parte de una dirección URL estática que describe el producto o la categoría. Al crear un producto o una categoría, se genera automáticamente una clave URL inicial basada en el nombre. Para cambiar la clave de URL, consulte la sección [Optimización del motor de búsqueda](product-search-engine-optimization.md) de la información del producto.

>[!NOTE]
>
>De forma predeterminada, los caracteres especiales acentuados se sustituyen automáticamente por sus versiones normales no acentuadas en la clave URL. Por ejemplo, `ñ` se reemplaza automáticamente por `n`. Este comportamiento se puede deshabilitar estableciendo la opción de configuración _[!UICONTROL Search Engine Optimization: Apply transliteration for product URL]_&#x200B;en `No`. Consulte [Configurar las direcciones URL del catálogo](#configure-catalog-urls).

La clave de URL debe constar de caracteres en minúsculas con guiones no finales entre estos caracteres para separar las palabras. No se permiten guiones al principio o al final de la clave URL. Una clave de URL &quot;fácil de usar para los motores de búsqueda&quot; y bien diseñada puede incluir el nombre del producto y las palabras clave para mejorar la forma en que los motores de búsqueda lo indexan. La clave URL se puede configurar para crear un redireccionamiento automático si cambia la clave URL.

>[!NOTE]
>
>Para ampliar las personalizaciones de URL, como las URL localizadas, consulte [Reescrituras de URL](../merchandising-promotions/url-rewrite.md) para obtener más información.

### Sufijo de HTML

El catálogo se puede configurar para incluir o excluir el sufijo como parte de las direcciones URL de categorías y productos. Existen varias razones por las que las personas pueden elegir utilizar o omitir el sufijo. Algunos creen que el sufijo ya no sirve para ningún propósito útil, y que las páginas sin un sufijo son indexadas de manera más efectiva por los motores de búsqueda. Sin embargo, es posible que su empresa tenga un formato estandarizado para las direcciones URL que requieran un sufijo.

Como el sufijo está controlado por la configuración del sistema, nunca debe escribirlo directamente en la clave URL de una categoría o producto. (Esto da como resultado un sufijo doble al final de la dirección URL). Tanto si decide utilizar el sufijo como si no, sea coherente y utilice la misma configuración para todas las páginas de productos y categorías. Estos son ejemplos de direcciones URL con un sufijo y sin él.

#### URL con sufijo de HTML

- `http://mystore.com/helena-hooded-fleece.html`
- `http://mystore.com/helena-hooded-fleece.htm`

#### URL sin sufijo de HTML

- `http://mystore.com/helena-hooded-fleece`

### Ruta de categoría

Puede configurar las direcciones URL del producto para incluir o excluir la ruta de la categoría en función de sus preferencias. De forma predeterminada, la ruta de la categoría no se incluye en las direcciones URL de los productos. Sin embargo, las categorías anidadas siempre mostrarán la ruta de categoría completa en sus direcciones URL en la tienda, lo que garantiza claridad y coherencia en la navegación de categorías. Los siguientes ejemplos muestran la misma dirección URL del producto con y sin la ruta de la categoría.

#### URL del producto con ruta de categoría

- `http://mystore.com/women/tops-women/hoodies-and-sweatshirts-women/helena-hooded-fleece.html`

#### URL del producto sin ruta de categoría

- `http://mystore.com/helena-hooded-fleece.html`

Para evitar que los motores de búsqueda indexen varias URL que conducen al mismo contenido, puede excluir la ruta de la categoría de la URL. Otro método es utilizar una metaetiqueta canónica para que los motores de búsqueda sepan qué direcciones URL indexar y cuáles ignorar. De forma predeterminada, Commerce no incluye la ruta de categoría en las direcciones URL de los productos.

## Configuración de direcciones URL del catálogo

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Search Engine Optimizations]** y establezca las opciones:

   - Establezca **[!UICONTROL Product URL Suffix]** en `html` o `htm`. Introduzca el sufijo sin un punto, ya que se aplica automáticamente.

   - Establezca **[!UICONTROL Category URL Suffix]** en `html` o `htm`. Introduzca el sufijo sin un punto, ya que se aplica automáticamente.

   - Establezca **[!UICONTROL Use Categories Path for Product URLs]** según sus preferencias.

   ![Optimización del motor de búsqueda](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   Para obtener una lista detallada de estas opciones, consulte [Optimización del motor de búsqueda](../configuration-reference/catalog/catalog.md#search-engine-optimization) en la _Referencia de configuración_.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

1. Cuando se le solicite, haga clic en el vínculo **[!UICONTROL Cache Management]** en el mensaje del sistema y actualice la caché no válida.

   ![Actualizar caché](./assets/msg-cache-management.png){width="450" zoomable="yes"}

   Para obtener más información acerca de estas opciones, vea [Actualizar cachés](../systems/cache-management.md#refresh-specific-caches).

## Configurar el formato de URL del catálogo

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL General]** y elija **[!UICONTROL Web]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Url Options]** y establezca las opciones:

![Web > Opciones generales](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

| Campo | [Ámbito](../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Add Store Code to URLs] | Global | Si las reescrituras del servidor web están habilitadas, al habilitar esta configuración se inserta el código de tienda de la vista actual en la dirección URL. Opciones: `Yes` / `No` |
| [!UICONTROL Auto-redirect to Base URL] | Global | (En configuraciones de tienda única) Si hay un vínculo roto en el sitio, esto redirige el tráfico a la dirección URL base en lugar de a una página con el mensaje &quot;404 Page Not Found&quot;. Opciones: `No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br /><br />**_Importante!_**&#x200B;No use el redireccionamiento automático a la dirección URL base para configuraciones de varias tiendas. |
| [!UICONTROL Catalog media URL format] | Global | Define el formato de URL asignado a productos y categorías. Opciones: <br />**[!UICONTROL Unique hash per image variant (Legacy mode)]**- Define el nombre de archivo convertido como un valor hash único.<br />**[!UICONTROL Image optimization based on query parameters]**: define el proceso de [optimización de imágenes](../content-design/media-gallery-image-optimization.md) en función de los parámetros de consulta. |

{style="table-layout:auto"}
