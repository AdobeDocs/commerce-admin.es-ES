---
title: Datos de Meta
description: Obtenga información sobre cómo introducir metadatos con muchas palabras clave para mejorar la forma en que los motores de búsqueda indexan el sitio de Commerce.
exl-id: 2acc1523-9da6-4e6f-8e4f-607603a61559
feature: Merchandising, Search
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
TQID: https://experienceleague.adobe.com/hl0i6mlFJY5r5bIWNG6gQMGlWQMmaWOWBnt8pCpKT50
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 747
ht-degree: 0%

---

# Datos de Meta

>[!TIP]
>
>Para Adobe Commerce as a Cloud Service, consulte las [directrices de metadatos](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/metadata/?lang=es) en la documentación de Commerce Storefront

Tu tienda está cargada de lugares donde puedes introducir metadatos con palabras clave para mejorar la forma en que los motores de búsqueda indexan tu sitio. Al configurar la tienda, es posible que introduzca metadatos preliminares con la intención de finalizarlos más adelante. Con el tiempo, puede ajustar los metadatos para que se centren en los patrones de compra y las preferencias de sus clientes.

![Configuración del producto - Optimización del motor de búsqueda](./assets/product-basic-settings-search-engine-optimization-yoga-strap.png){width="700" zoomable="yes"}

## Título de Meta

El metatítulo aparece en la barra de título y en la pestaña del navegador y en los listados de resultados de búsqueda. El metatítulo debe ser exclusivo de la página y tener menos de 70 caracteres de longitud.

![Ejemplo de tienda - meta title](./assets/storefront-home-page-meta-title.png){width="600"}

## Palabras clave Meta

Aunque algunos motores de búsqueda ignoran las palabras clave meta, otros las siguen usando. La práctica recomendada actual es incorporar palabras clave de alto valor en el meta título y la meta descripción.

![Búsqueda en explorador web: palabras clave meta](./assets/storefront-meta-description.png){width="500"}

## Descripción de Meta

Las descripciones de Meta proporcionan una breve descripción de la página para las listas de resultados de búsqueda. Lo ideal es que una metadescripción tenga entre 150 y 160 caracteres de longitud, aunque el campo acepta hasta 255 caracteres.

## Fragmentos enriquecidos

Los fragmentos enriquecidos proporcionan información detallada para las listas de resultados de búsqueda y otras aplicaciones. De manera predeterminada, el marcado de datos estructurado basado en el estándar [schema.org](https://schema.org/) se agrega a la plantilla de producto de la tienda. Como resultado, hay más información disponible para que los motores de búsqueda la incluyan como _fragmentos enriquecidos_ en las listas de productos.

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

   - Establezca **Usar etiqueta Meta de vínculo canónico para las categorías** en `Yes`.

   - Establezca **Usar etiqueta Meta de vínculo canónico para productos** en `No`.

1. Si desea que los motores de búsqueda indexen páginas de producto únicamente con el formato nombre de dominio/clave de URL de producto, haga lo siguiente:

   - Establezca **Usar etiqueta Meta de vínculo canónico para productos** en `Yes`.

   - Establezca **Usar etiqueta Meta de vínculo canónico para las categorías** en `No`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Demostración de datos de Meta

Vea este vídeo para obtener más información sobre la administración de metadatos de SEO:

>[!VIDEO](https://video.tv.adobe.com/v/3411825?captions=spa&quality=12&learn=on)
