---
title: Crear un producto
description: Obtenga información sobre los tipos de productos que puede crear para su catálogo.
exl-id: ff90bf8a-a64d-403f-bd09-5c8167a36f0b
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

---

# Crear un producto

Elegir un tipo de producto es una de las primeras cosas que debe hacer para crear un producto. Si acaba de empezar a crear su catálogo de productos, puede crear algunos productos de muestra para experimentar con cada tipo de producto. Además de los tipos de productos básicos, el término _producto complejo_ a veces se utiliza para referirse a productos con varias opciones, como un producto configurable que está disponible en varios colores y tamaños.

>[!NOTE]
>
>Para obtener más información, consulte el catálogo [navegación](navigation.md), cómo se configura [categorías](categories.md) y [atributos](product-attributes.md)y el catálogo [Opciones de URL](catalog-urls.md) que están disponibles. Después de comprender estos conceptos, la forma más eficaz de agregar muchos productos al catálogo es [importar](../systems/data-import.md) desde un archivo CSV.

![Página de productos en la tienda](./assets/storefront-product-page.png){width="700" zoomable="yes"}

## Tipos de productos

**[Producto sencillo](product-create-simple.md)** - Un producto simple es un artículo físico con un solo SKU. Los productos simples tienen diversos precios y controles de entrada que permiten vender variaciones del producto. Se pueden utilizar productos simples en asociación con productos agrupados, agrupados y configurables.

**[Producto configurable](product-create-configurable.md)** - Un producto configurable parece ser un único producto con listas de opciones para cada variación. Sin embargo, cada opción representa un producto independiente y sencillo con un SKU distinto, lo que permite realizar un seguimiento del inventario para cada variación.

**[Producto agrupado](product-create-grouped.md)** - Un producto agrupado presenta múltiples productos independientes como un grupo. Puede ofrecer variaciones de un solo producto o agruparlas para una promoción. Los productos se pueden comprar por separado o en grupo.

**[Productos virtuales](product-create-virtual.md)** - Un producto virtual no es un producto tangible y se utiliza normalmente para productos como servicios, suscripciones, garantías y suscripciones. Los productos virtuales se pueden utilizar en asociación con productos agrupados y agrupados.

**[Paquete de productos](product-create-bundle.md)**  - Un paquete de productos permite a los clientes &quot;construir su propio&quot; a partir de una variedad de opciones. El paquete puede ser una cesta de regalo, un ordenador o cualquier otra cosa que se pueda personalizar. Cada elemento del paquete es un producto independiente independiente.

**[Producto descargable](product-create-downloadable.md)** - Un producto descargable digitalmente consta de uno o más archivos que se descargan. Los archivos pueden residir en el servidor o proporcionarse como direcciones URL a cualquier otro servidor.

**[Tarjeta regalo](product-gift-card-create.md)** - ([Adobe Commerce](../landing/home.md#product-editions) solo) Hay tres tipos de tarjetas de regalo. _Virtual_ las tarjetas regalo se envían por correo electrónico. _Físico_ las tarjetas regalo se envían al destinatario. _Combinado_ tarjetas regalo que son una combinación de virtual y físico. Cada uno tiene un código único que se canjea durante el cierre de compra. Las tarjetas de regalo también se pueden incluir en un producto agrupado.

## Configuración del producto

La configuración y los atributos de productos utilizados con más frecuencia se muestran en la parte superior de la página, seguidos de los atributos personalizados. Cualquier otra configuración de producto se encuentra en secciones ampliables en la parte inferior de la página.

![Configuración del producto](./assets/product-settings.png){width="600" zoomable="yes"}

| Configuración | Descripción |
|--- |--- |
| [[!UICONTROL Sources]](../inventory-management/sources-assign-per-product.md) | (Cuándo [[!DNL Inventory Management]](../inventory-management/introduction.md) está activada) Muestra los orígenes desde los que se puede distribuir el producto. |
| [[!UICONTROL Content]](product-content.md) | Se utiliza para introducir y editar la descripción principal del producto que aparece en la página de producto de la tienda. |
| [[!UICONTROL Configurations]](product-configurations.md) | Enumera cualquier variación existente del producto y se puede utilizar para generar variaciones que se utilizarán con el tipo de producto configurable. |
| [[!UICONTROL Product Reviews]](settings-advanced-product-reviews.md) | Enumera todas las revisiones que los clientes han enviado para el producto. |
| [[!UICONTROL Search Engine Optimization]](product-search-engine-optimization.md) | Especifica la clave URL y los campos de metadatos que los motores de búsqueda utilizan para indexar el producto. |
| [[!UICONTROL Related Products, Up-Sells, and Cross-Sells]](related-products-up-sells-cross-sells.md) | Se utiliza para configurar bloques promocionales simples en la tienda que presenten una selección de productos adicionales que puedan ser de interés para el cliente. |
| [[!UICONTROL Customizable Options]](settings-advanced-custom-options.md) | Agrega opciones personalizables a un producto. |
| [[!UICONTROL Product in Websites]](settings-basic-websites.md) | Identifica cada sitio web donde está disponible el producto, según la jerarquía de la tienda. |
| [[!UICONTROL Design]](settings-advanced-design.md) | Se utiliza para aplicar una temática diferente a la página del producto, cambiar el diseño de la columna, determinar dónde aparecen las opciones del producto e introducir código XML personalizado. |
| [[!UICONTROL Gift options]](product-gift-options.md) | Se utiliza para habilitar o deshabilitar una opción de mensaje de regalo durante el cierre de compra en el nivel de producto. |
| [[!UICONTROL Product In Shared Catalogs]](../b2b/catalog-shared.md) | ![Adobe Commerce B2B](../assets/b2b.svg) (Disponible con [Adobe Commerce B2B](../b2b/introduction.md) (solo) Permite mantener los catálogos compartidos con precios personalizados para diferentes empresas. |
| [[!UICONTROL Downloadable Information]](product-create-downloadable.md#step-5-complete-the-downloadable-information) | Se utiliza para definir los parámetros de la descarga del producto. |

{style="table-layout:auto"}

## Precios avanzados e inventario

Para acceder a la configuración avanzada de precios e inventario, haga clic en el siguiente enlace **[!UICONTROL Price]** y **[!UICONTROL Quantity]**. Para obtener más información, consulte [Administración de precios](pricing-advanced.md) y [Inventory management](../inventory-management/introduction.md).
