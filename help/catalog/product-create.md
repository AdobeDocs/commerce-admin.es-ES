---
title: Crear un producto
description: Obtenga información sobre los tipos de productos que puede crear para su catálogo.
exl-id: ff90bf8a-a64d-403f-bd09-5c8167a36f0b
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/c4lf97N0NptqaySmZ5QEr9O81Ftjc9b6-7IiVMimMWU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
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
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 689
ht-degree: 0%

---

# Crear un producto

Elegir un tipo de producto es una de las primeras cosas que debe hacer para crear un producto. Si acaba de empezar a crear su catálogo de productos, puede crear algunos productos de muestra para experimentar con cada tipo de producto. Además de los tipos de productos básicos, el término _producto complejo_ se utiliza a veces para referirse a productos con varias opciones, como un producto configurable que está disponible en varios colores y tamaños.

>[!NOTE]
>
>Para obtener más información, consulte el catálogo [navigation](navigation.md), cómo configurar [categorías](categories.md) y [atributos](product-attributes.md), y las [opciones de URL](catalog-urls.md) del catálogo que están disponibles. Después de comprender estos conceptos, la manera más eficiente de agregar muchos productos al catálogo es [importarlos](../systems/data-import.md) desde un archivo CSV.

![Página de producto en la tienda](./assets/storefront-product-page.png){width="700" zoomable="yes"}

## Tipos de productos

**[Producto simple](product-create-simple.md)**: un producto simple es un artículo físico con un único SKU. Los productos simples tienen diversos precios y controles de entrada que permiten vender variaciones del producto. Se pueden utilizar productos simples en asociación con productos agrupados, agrupados y configurables.

**[Producto configurable](product-create-configurable.md)**: un producto configurable parece ser un único producto con listas de opciones para cada variación. Sin embargo, cada opción representa un producto independiente y sencillo con un SKU distinto, lo que permite realizar un seguimiento del inventario para cada variación.

**[Producto agrupado](product-create-grouped.md)**: un producto agrupado presenta varios productos independientes como grupo. Puede ofrecer variaciones de un solo producto o agruparlas para una promoción. Los productos se pueden comprar por separado o en grupo.

**[Productos virtuales](product-create-virtual.md)**: un producto virtual no es un producto tangible y se suele usar para productos como servicios, suscripciones, suscripciones, garantías y suscripciones. Los productos virtuales se pueden utilizar en asociación con productos agrupados y agrupados.

**[Producto agrupado](product-create-bundle.md)**: un producto agrupado permite a los clientes &quot;crear el suyo propio&quot; a partir de una variedad de opciones. El paquete puede ser una cesta de regalo, un ordenador o cualquier otra cosa que se pueda personalizar. Cada elemento del paquete es un producto independiente independiente.

**[Producto descargable](product-create-downloadable.md)**: un producto descargable digitalmente consta de uno o más archivos descargados. Los archivos pueden residir en el servidor o proporcionarse como direcciones URL a cualquier otro servidor.

**[Tarjeta regalo](product-gift-card-create.md)** - ([Solo Adobe Commerce](../landing/home.md#product-editions)) Existen tres tipos de tarjetas regalo. Las tarjetas de regalo _virtuales_ se envían por correo electrónico. Se envían tarjetas regalo _físicas_ al destinatario. _Tarjetas regalo_ combinadas que son una combinación de tarjetas físicas y virtuales. Cada uno tiene un código único que se canjea durante el cierre de compra. Las tarjetas de regalo también se pueden incluir en un producto agrupado.

## Configuración del producto

La configuración y los atributos de productos utilizados con más frecuencia se muestran en la parte superior de la página, seguidos de los atributos personalizados. Cualquier otra configuración de producto se encuentra en secciones ampliables en la parte inferior de la página.

![Configuración del producto](./assets/product-settings.png){width="600" zoomable="yes"}

| Configuración | Descripción |
|--- |--- |
| [[!UICONTROL Sources]](../inventory-management/sources-assign-per-product.md) | (Cuando [[!DNL Inventory Management]](../inventory-management/introduction.md) está habilitado) Enumera los orígenes desde los que se puede distribuir el producto. |
| [[!UICONTROL Content]](product-content.md) | Se utiliza para introducir y editar la descripción principal del producto que aparece en la página de producto de la tienda. |
| [[!UICONTROL Configurations]](product-configurations.md) | Enumera cualquier variación existente del producto y se puede utilizar para generar variaciones que se utilizarán con el tipo de producto configurable. |
| [[!UICONTROL Product Reviews]](settings-advanced-product-reviews.md) | Enumera todas las revisiones que los clientes han enviado para el producto. |
| [[!UICONTROL Search Engine Optimization]](product-search-engine-optimization.md) | Especifica la clave URL y los campos de metadatos que los motores de búsqueda utilizan para indexar el producto. |
| [[!UICONTROL Related Products, Up-Sells, and Cross-Sells]](related-products-up-sells-cross-sells.md) | Se utiliza para configurar bloques promocionales simples en la tienda que presenten una selección de productos adicionales que puedan ser de interés para el cliente. |
| [[!UICONTROL Customizable Options]](settings-advanced-custom-options.md) | Agrega opciones personalizables a un producto. |
| [[!UICONTROL Product in Websites]](settings-basic-websites.md) | Identifica cada sitio web donde está disponible el producto, según la jerarquía de la tienda. |
| [[!UICONTROL Design]](settings-advanced-design.md) | Se utiliza para aplicar una temática diferente a la página del producto, cambiar el diseño de la columna, determinar dónde aparecen las opciones del producto e introducir código XML personalizado. |
| [[!UICONTROL Gift options]](product-gift-options.md) | Se utiliza para habilitar o deshabilitar una opción de mensaje de regalo durante el cierre de compra en el nivel de producto. |
| [[!UICONTROL Product In Shared Catalogs]](../b2b/catalog-shared.md) | ![Adobe Commerce B2B](../assets/b2b.svg) (disponible solo con [Adobe Commerce B2B](../b2b/introduction.md)) Permite mantener catálogos compartidos con precios personalizados para diferentes empresas. |
| [[!UICONTROL Downloadable Information]](product-create-downloadable.md#step-5-complete-the-downloadable-information) | Se utiliza para definir los parámetros de la descarga del producto. |

{style="table-layout:auto"}

## Precios avanzados e inventario

Para acceder a la configuración avanzada de precios e inventario, haga clic en el vínculo debajo de **[!UICONTROL Price]** y **[!UICONTROL Quantity]**. Para obtener más información, consulte [Administración de precios](pricing-advanced.md) y [Inventory management](../inventory-management/introduction.md).
