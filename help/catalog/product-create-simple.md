---
title: Producto sencillo
description: Aprenda a crear un producto simple que se pueda vender individualmente o como parte de un producto agrupado, configurable o agrupado.
exl-id: 3ac9b28d-3929-4fd6-97ca-145ea6d6897c
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---

# Producto sencillo

Una de las claves para aprovechar el poder de los tipos de productos es aprender cuándo utilizar un producto simple e independiente. Un producto simple se puede vender por separado o como parte de un producto agrupado, configurable o agrupado. Un producto simple con opciones personalizadas a veces se denomina _producto compuesto_.

Las siguientes instrucciones muestran el proceso de creación de un producto simple mediante una [plantilla de producto](attribute-sets.md), campos obligatorios y configuración básica. Cada campo obligatorio está marcado con un asterisco rojo (`*`). Cuando termine los conceptos básicos, puede completar el resto de la configuración del producto según sea necesario.

![Producto sencillo](./assets/product-simple.png){width="700" zoomable="yes"}

## Paso 1: Elija el tipo de producto

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. En el _[!UICONTROL Add Product]_( ![Flecha de menú](../assets/icon-menu-down-arrow-red.png){width="25"} ) en la parte superior derecha, seleccione **[!UICONTROL Simple Product]**.

   ![Añadir producto simple](./assets/product-add-simple.png){width="700" zoomable="yes"}

## Paso 2: Selección del conjunto de atributos

Para elegir el [conjunto de atributos](attribute-sets.md) que se utiliza como plantilla para el producto:

- Haga clic en en **[!UICONTROL Attribute Set]** e introduzca la totalidad o parte del nombre del conjunto de atributos.

- En la lista mostrada, elija el conjunto de atributos que desea utilizar.

El formulario se actualiza para reflejar el cambio.

![Elegir conjunto de atributos](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Paso 3: complete la configuración necesaria

1. Introduzca el **[!UICONTROL Product Name]**.

1. Aceptar el valor predeterminado **[!UICONTROL SKU]** que se basa en el nombre del producto o introduzca otro.

1. Introduzca el producto **[!UICONTROL Price]**.

1. Dado que el producto aún no está listo para publicar, configure el **[!UICONTROL Enable Product]** opción para `No`.

1. click **[!UICONTROL Save]** y continuar.

   Cuando se guarda el producto, la variable [Vista de tienda](introduction.md#product-scope) el selector aparece en la esquina superior izquierda.

1. Elija la **[!UICONTROL Store View]** donde vaya a estar disponible el producto.

   ![Elija la vista de la tienda](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Paso 4: completar la configuración básica

1. Establecer **[!UICONTROL Tax Class]** a uno de los siguientes:

   - `None`
   - `Taxable Goods`
   - `Refund Adjustments`
   - `Gift Options`
   - `Order Gift Wrapping`
   - `Item Gift Wrapping`
   - `Printed Gift Card`
   - `Reward Points`
   - `VAT Reduced`
   - `VAT Standard`

1. Introduzca el **[!UICONTROL Quantity]** del producto que está en stock.

   De forma predeterminada, **[!UICONTROL Stock Status]** se establece en `In Stock`.

   >[!NOTE]
   >
   >Si activa [Inventory management](../inventory-management/introduction.md), los comerciantes de origen único establecen la cantidad en esta sección. Los comerciantes de varios orígenes agregan orígenes y cantidades en la sección Orígenes. Consulte lo siguiente _Asignación de Orígenes y Cantidades (Inventory management)_ sección.

1. Introduzca el **[!UICONTROL Weight]** del producto.

1. Aceptar el valor predeterminado **[!UICONTROL Visibility]** configuración de `Catalog, Search`.

1. Para asignar _[!UICONTROL Categories]_para seleccionar el producto, haga clic en **[!UICONTROL Select…]**y realice una de las acciones siguientes:

   **Elija una categoría existente**:

   - Empiece a escribir en el cuadro hasta que encuentre una coincidencia.

   - Seleccione la casilla de verificación de cada categoría que se va a asignar.

   **Crear una categoría**:

   - Haga clic **[!UICONTROL New Category]**.

   - Introduzca el **[!UICONTROL Category Name]** y elija la **[!UICONTROL Parent Category]**, que determina su posición en la estructura de menú.

   - Haga clic **[!UICONTROL Create Category]**.

1. Para incluir el producto en la lista de [nuevos productos](../content-design/widget-new-products-list.md), seleccione la **[!UICONTROL Set Product as New]** casilla de verificación

1. Elija la **[!UICONTROL Country of Manufacture]**.

Puede haber atributos individuales adicionales que describan el producto. La selección varía según el conjunto de atributos y puede completarla más adelante.

### Asignación de orígenes y cantidades ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## Paso 5: Completar la información del producto

Desplácese hacia abajo y complete la información de las siguientes secciones según sea necesario:

- [Contenido](product-content.md)
- [Imágenes y vídeos](product-images-and-video.md)
- [Productos relacionados, ampliación de ventas y ventas cruzadas](related-products-up-sells-cross-sells.md)
- [Optimización del motor de búsqueda](product-search-engine-optimization.md)
- [Opciones personalizables](settings-advanced-custom-options.md)
- [Productos en sitios web](settings-basic-websites.md)
- [Diseño](settings-advanced-design.md)
- [Opciones de regalo](product-gift-options.md)

## Paso 6: Publicar el producto

1. Si está listo para publicar el producto en el catálogo, configure el **[!UICONTROL Enable Product]** cambiar a `Yes`.

1. Realice una de las siguientes acciones:

   - **Método 1:** Guardar y previsualizar

      - En la esquina superior derecha, haga clic en **[!UICONTROL Save]**.

      - Para ver el producto en tu tienda, elige **[!UICONTROL Customer View]** en el _Administrador_ (![Flecha de menú](../assets/icon-menu-down-arrow-black.png)) menú.

     La tienda se abre en una nueva pestaña del explorador.

     ![Vista de cliente](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Método 2:** Guardar y cerrar

     En el _[!UICONTROL Save]_ ( ![Flecha de menú](../assets/icon-menu-down-arrow-red.png){width="25"} ), seleccione **[!UICONTROL Save & Close]**.

## Cosas que recordar

- Los productos simples se pueden incluir en tipos de producto configurables, paquetes y agrupados.

- La configuración de producto simple anula las configuraciones de producto configurables para un producto específico.

- Un producto simple puede tener opciones personalizadas con varios tipos de entrada, lo que permite vender muchas variaciones de productos desde un único SKU.
