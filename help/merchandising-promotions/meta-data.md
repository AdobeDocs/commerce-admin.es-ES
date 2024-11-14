---
title: Metadatos
description: Obtenga información sobre cómo introducir metadatos con muchas palabras clave para mejorar la forma en que los motores de búsqueda indexan el sitio de Commerce.
exl-id: 2acc1523-9da6-4e6f-8e4f-607603a61559
feature: Merchandising, Search
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# Metadatos

Tu tienda está cargada de lugares donde puedes introducir metadatos con palabras clave para mejorar la forma en que los motores de búsqueda indexan tu sitio. Al configurar la tienda, es posible que introduzca metadatos preliminares con la intención de finalizarlos más adelante. Con el tiempo, puede ajustar los metadatos para que se centren en los patrones de compra y las preferencias de sus clientes.

![Configuración del producto - Optimización del motor de búsqueda](./assets/product-basic-settings-search-engine-optimization-yoga-strap.png){width="700" zoomable="yes"}

## Meta title

El metatítulo aparece en la barra de título y en la pestaña del navegador y en los listados de resultados de búsqueda. El metatítulo debe ser exclusivo de la página y tener menos de 70 caracteres de longitud.

![Ejemplo de tienda - meta title](./assets/storefront-home-page-meta-title.png){width="600"}

## Meta keywords

Aunque algunos motores de búsqueda ignoran las palabras clave meta, otros las siguen usando. La práctica recomendada actual es incorporar palabras clave de alto valor en el meta título y la meta descripción.

![Búsqueda en explorador web: palabras clave meta](./assets/storefront-meta-description.png){width="500"}

## Meta descripción

Las metadescripciones proporcionan una breve descripción de la página para las listas de resultados de búsqueda. Lo ideal es que una metadescripción tenga entre 150 y 160 caracteres de longitud, aunque el campo acepta hasta 255 caracteres.

## Fragmentos enriquecidos

Los fragmentos enriquecidos proporcionan información detallada para las listas de resultados de búsqueda y otras aplicaciones. De manera predeterminada, el marcado de datos estructurado basado en el estándar [schema.org][1] se agrega a la plantilla de producto de la tienda. Como resultado, hay más información disponible para que los motores de búsqueda la incluyan como _fragmentos enriquecidos_ en las listas de productos.

## Metaetiqueta canónica

Algunos motores de búsqueda penalizan los sitios web que tienen varias direcciones URL que apuntan al mismo contenido. La metaetiqueta canónica indica a los motores de búsqueda qué página indexar cuando varias URL tienen contenido idéntico o similar. El uso de la metaetiqueta canónica puede mejorar la clasificación del sitio y agregar vistas de página. La metaetiqueta canónica se coloca en el bloque `<head>` de una página de producto o categoría. Proporciona un vínculo a la dirección URL preferida, por lo que los motores de búsqueda le otorgan mayor peso.

### Ejemplo 1: La ruta de categoría crea direcciones URL duplicadas

Por ejemplo, si el catálogo está configurado para incluir la ruta de la categoría en las direcciones URL de los productos, la tienda genera varias direcciones URL que apuntan a la misma página de productos.

    http://mystore.com/gear/bags/driven-backpack.html
    http://mystore.com/driven-backpack.html

### Ejemplo 2: URL completa de la página de categoría

Cuando se habilitan las metaetiquetas canónicas para categorías, la página de categoría de la tienda incluye una URL canónica a la URL de categoría completa:

    http://mystore.com/gear/bags/

### Ejemplo 3: URL completa de la página del producto

Cuando las metaetiquetas canónicas para productos están habilitadas, la página de producto incluye una URL canónica a la clave dominio-nombre/url-producto porque las claves de URL del producto son únicas globalmente.

    http://mystore.com/driven-backpack.html

Si también incluye la ruta de la categoría en las direcciones URL del producto, la dirección URL canónica permanece como nombre de dominio/clave de URL del producto. Sin embargo, también se puede acceder al producto mediante su dirección URL completa, que incluye la categoría. Por ejemplo, si la clave de URL del producto es `driven-backpack` y se asigna a la categoría Engranaje > Bolsas, se puede acceder al producto mediante cualquiera de las direcciones URL.

Puede evitar ser penalizado por los motores de búsqueda omitiendo la categoría de la URL o utilizando la metaetiqueta canónica para dirigir a los motores de búsqueda a indexar por producto o categoría. Como práctica recomendada, se recomienda habilitar las metaetiquetas canónicas tanto para categorías como para productos.

### Habilitar la metaetiqueta canónica

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **Optimización del motor de búsqueda**.

   Para cambiar cualquier valor de campo, primero debe desactivar la casilla de verificación **Usar valor del sistema** después de cada campo.

   ![Configuración del catálogo: optimización del motor de búsqueda](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Si desea que los motores de búsqueda indicen solo las páginas de categoría que utilizan la ruta de categoría completa, haga lo siguiente:

   - Establezca **Usar metaetiqueta de vínculo canónico para las categorías** en `Yes`.

   - Establezca **Usar metaetiqueta de vínculo canónico para productos** en `No`.

1. Si desea que los motores de búsqueda indexen páginas de producto únicamente con el formato nombre de dominio/clave de URL de producto, haga lo siguiente:

   - Establezca **Usar metaetiqueta de vínculo canónico para productos** en `Yes`.

   - Establezca **Usar metaetiqueta de vínculo canónico para las categorías** en `No`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Demostración de metadatos

Vea este vídeo para obtener más información sobre la administración de metadatos de SEO:

>[!VIDEO](https://video.tv.adobe.com/v/343750?quality=12&learn=on)

[1]: https://schema.org/
