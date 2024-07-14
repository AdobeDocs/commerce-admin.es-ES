---
title: Producto agrupado
description: Aprenda a crear un producto agrupado que consta de productos independientes simples que se presentan como un grupo.
exl-id: af42b7fc-27f2-4c5a-b504-a70a324fae76
feature: Catalog Management, Products
source-git-commit: 140930df515d1e0604b18a4ebf689254b9487b53
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 0%

---

# Producto agrupado

Un producto agrupado consiste en productos independientes simples que se presentan como un grupo. Puede ofrecer variaciones de un solo producto o agruparlas por temporada o tema. La presentación de un producto agrupado puede crear un incentivo para que los clientes compren artículos adicionales. Un producto agrupado proporciona una manera sencilla de ofrecer variaciones de un producto y enumerarlas todas en la misma página.

Por ejemplo, puede vender artículos planos de stock abiertos y enumerar todos los tipos de utensilios que se utilizan en un lugar formal. Algunos pueden pedir varios tenedores para ensaladas, tenedores para pescado, tenedores para la cena, cuchillos para la cena, cuchillos para pescado, cuchillos para mantequilla, cucharas de sopa y cucharas de postre. Otros clientes pueden pedir un tenedor, un cuchillo y una cuchara sencillos. Los clientes pueden pedir cualquier número de cada artículo como deseen.

Aunque se presentan como un grupo, cada producto del grupo se compra como un artículo independiente. En el carro de compras, cada artículo y la cantidad comprada se muestran como un artículo de línea independiente.

Las siguientes instrucciones muestran el proceso de creación de un producto agrupado mediante una [plantilla de producto](attribute-sets.md), los campos obligatorios y la configuración básica. Cada campo obligatorio está marcado con un asterisco rojo (`*`). Cuando termine los conceptos básicos, puede completar el resto de la configuración del producto según sea necesario.

![Producto agrupado](./assets/product-grouped.png){width="700" zoomable="yes"}

## Paso 1: Elija el tipo de producto

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. En el menú _[!UICONTROL Add Product]_( ![Flecha de menú](../assets/icon-menu-down-arrow-red.png){width="25"} ) de la esquina superior derecha, elija **[!UICONTROL Grouped Product]**.

   ![Agregar producto agrupado](./assets/product-add-grouped.png){width="700" zoomable="yes"}

## Paso 2: Selección del conjunto de atributos

Para elegir el [conjunto de atributos](attribute-sets.md) que se usa como plantilla para el producto, siga uno de estos procedimientos:

- Para buscar, escriba el nombre de **[!UICONTROL Attribute Set]**.
- En la lista, elija el conjunto de atributos que desea utilizar.

El formulario se actualiza para reflejar el cambio.

![Elegir plantilla](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

Si no existen los atributos necesarios, puede agregar nuevos atributos al crear un producto:

- En la esquina superior derecha, haga clic en **[!UICONTROL Add Attribute]**.
- Definir un nuevo atributo (consulte [Agregar un atributo a un producto](product-attributes-add.md)).

  ![Nuevo atributo](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

Para agregar un atributo existente al producto, use los [controles de filtro](../getting-started/admin-grid-controls.md) para encontrar el atributo en la cuadrícula y haga lo siguiente:

- Seleccione la casilla de verificación de la primera columna de cada atributo que desee añadir.
- Haga clic en **[!UICONTROL Add Selected]**.

## Paso 3: complete la configuración necesaria

1. Escriba **[!UICONTROL Product Name]**.

1. Acepte el valor predeterminado **[!UICONTROL SKU]** basado en el nombre del producto o escriba otro.

   Tenga en cuenta que el campo **[!UICONTROL Quantity]** no está disponible porque el valor se deriva de los productos individuales que conforman el grupo.

   Un producto agrupado no tiene su propio precio en el catálogo. El precio del producto agrupado se deriva del precio de los productos individuales incluidos en el grupo.

1. Dado que el producto aún no está listo para publicarse, establezca **[!UICONTROL Enable Product]** en `No` ( ![Alternar no](../assets/toggle-no.png) ).

1. Haga clic en **[!UICONTROL Save]** y continúe.

   Cuando se guarda el producto, el nombre aparece en la parte superior de la página y el selector de [Vista de tienda](introduction.md#product-scope) aparece en la esquina superior izquierda.

1. Elija el **[!UICONTROL Store View]** en el que el producto estará disponible.

   ![Elegir vista de tienda](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Paso 4: completar la configuración básica

1. Acepte la configuración **[!UICONTROL Stock Status]** de `In Stock`.

1. Para asignar **[!UICONTROL Categories]** al producto, haga clic en el cuadro **[!UICONTROL Select…]** y realice una de las acciones siguientes:

   **Elija una categoría existente:**

   - Empiece a escribir en el cuadro hasta que encuentre una coincidencia.

   - Seleccione la casilla de verificación de la categoría que se va a asignar.

   **Crear una categoría:**

   - Haga clic en **[!UICONTROL New Category]**.

   - Escriba **[!UICONTROL Category Name]** y elija **[!UICONTROL Parent Category]**, que determina su posición en la estructura de menú.

   - Haga clic en **[!UICONTROL Create Category]**.

1. Acepte la configuración de **[!UICONTROL Visibility]** de `Catalog, Search`.

1. Para incluir el producto en la [lista de nuevos productos](../content-design/widget-new-products-list.md), elige las fechas de **[!UICONTROL Set Product as New]** **[!UICONTROL from]** y **[!UICONTROL to]** en el calendario.

1. Elija **[!UICONTROL Country of Manufacture]**.

   Puede haber atributos individuales adicionales que describan el producto. La selección varía según el conjunto de atributos y puede completarlos más adelante.

## Paso 5: Agregar productos al grupo

1. Desplácese hasta la sección **[!UICONTROL Grouped Products]** y haga clic en **[!UICONTROL Add Products to Group]**.

   ![Productos agrupados](./assets/product-grouped-products.png){width="600" zoomable="yes"}

1. Si es necesario, use los [filtros](../getting-started/admin-grid-controls.md) para encontrar los productos que desea incluir en el grupo.

1. En la lista, active la casilla de verificación de cada elemento que desee incluir en el grupo.

   >[!NOTE]
   >
   >Solo los productos simples, descargables y virtuales sin opciones configurables pueden agruparse como productos secundarios. Otros tipos de productos no aparecen en la lista de selección.

   ![Agregar productos seleccionados](./assets/product-grouped-add-products.png){width="600" zoomable="yes"}

1. Para agregarlos al grupo de productos, haga clic en **[!UICONTROL Add Selected Products]**.

   Los productos seleccionados aparecen en la sección _[!UICONTROL Grouped Products]_.

   Para los comerciantes de Multi Source con [Inventory management](../inventory-management/sources-stocks.md), la cuadrícula incluye una columna **[!UICONTROL Quantity per Source]** con cada origen asignado y la cantidad de existencias del inventario.

   ![Productos en el grupo](./assets/product-grouped-grouped-products-section.png){width="600" zoomable="yes"}

1. Escriba un **[!UICONTROL Default Quantity]** para cualquiera de los elementos.

1. Para cambiar el orden de los productos, agarra el icono _Cambiar orden_ ( ![Controlador de posición](../assets/icon-sort-order.png) ) en la primera columna y arrastra el producto a la nueva posición en la lista.

1. Para quitar un producto del grupo, haga clic en **[!UICONTROL Remove]**.

## Paso 5: Completar la información del producto

Rellene la información de las secciones siguientes según sea necesario:

- [Contenido](product-content.md)
- [Imágenes y vídeos](product-images-and-video.md)
- [Optimización del motor de búsqueda](product-search-engine-optimization.md)
- [Productos relacionados, ampliación de ventas y ventas cruzadas](related-products-up-sells-cross-sells.md)
- [Opciones personalizables](settings-advanced-custom-options.md)
- [Productos en sitios web](settings-basic-websites.md)
- [Diseño](settings-advanced-design.md)
- [Opciones de regalo](product-gift-options.md)

## Paso 6: Publish del producto

1. Si está listo para publicar el producto en el catálogo, establezca **[!UICONTROL Enable Product]** en `Yes`.

1. Realice una de las siguientes acciones:

   **Método 1:** Guardar y previsualizar

   - En la esquina superior derecha, haga clic en **[!UICONTROL Save]**.

   - Para ver el producto en tu tienda, elige **[!UICONTROL Customer View]** en el menú _Administrador_ ( ![Flecha de menú](../assets/icon-menu-down-arrow-black.png) ).

     La tienda se abre en una nueva pestaña del explorador.

     ![Vista del cliente](./assets/product-admin-customer-view.png){width="700" zoomable="yes"}

   **Método 2:** Guardar y cerrar

   - En el menú _[!UICONTROL Save]_( ![flecha de menú](../assets/icon-menu-down-arrow-red.png){width="25"} ), elija **[!UICONTROL Save & Close]**.

## Paso 7: Configurar las miniaturas del carro de compras (opcional)

Si tiene una imagen diferente para cada producto del grupo, puede definir la configuración para que utilice la imagen correcta en la miniatura del carro de compras.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Checkout]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en **[!UICONTROL Shopping Cart]**.

   Para obtener una lista detallada de estas opciones de configuración, consulte [Carro de compras](../configuration-reference/sales/checkout.md#shopping-cart) en la _Referencia de configuración_.

1. Establezca **[!UICONTROL Grouped Product Image]** en `Product Thumbnail Itself`.

   ![Carro de compras](./assets/config-sales-cart-grouped-product.png){width="600" zoomable="yes"}

   Si es necesario, anule la selección de la casilla de verificación **[!UICONTROL Use system value]** para establecer esta opción.

1. Haga clic en **[!UICONTROL Save Config]**.

## Cosas que recordar

- Un producto agrupado es esencialmente una colección de productos asociados simples.

- Los productos secundarios agrupados pueden ser productos simples, descargables o virtuales **[!UICONTROL without custom options]**.

- Cada artículo comprado aparece individualmente en el carro de compras, en lugar de como parte del grupo.

- Un producto agrupado no tiene su propio precio en el catálogo. El precio del producto agrupado se deriva del precio de los productos individuales incluidos en el grupo.

- La imagen en miniatura del carro de compras se puede configurar para que muestre la imagen del producto principal agrupado o del producto asociado.
