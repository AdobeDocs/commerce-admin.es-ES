---
title: Producto sencillo
description: Aprenda a crear un producto simple que se pueda vender individualmente o como parte de un producto agrupado, configurable o agrupado.
exl-id: 3ac9b28d-3929-4fd6-97ca-145ea6d6897c
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Producto sencillo

Una de las claves para aprovechar el poder de los tipos de productos es aprender cuándo utilizar un producto simple e independiente. Un producto simple se puede vender por separado o como parte de un producto agrupado, configurable o agrupado. A veces, un producto simple con opciones personalizadas se denomina _producto compuesto_.

Las siguientes instrucciones muestran el proceso de creación de un producto simple mediante una [plantilla de producto](attribute-sets.md), los campos obligatorios y la configuración básica. Cada campo obligatorio está marcado con un asterisco rojo (`*`). Cuando termine los conceptos básicos, puede completar el resto de la configuración del producto según sea necesario.

![Producto simple](./assets/product-simple.png){width="700" zoomable="yes"}

## Paso 1: Elija el tipo de producto

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. En el menú _[!UICONTROL Add Product]_( ![Flecha del menú](../assets/icon-menu-down-arrow-red.png){width="25"} ) en la esquina superior derecha, elija **[!UICONTROL Simple Product]**.

   ![Agregar producto simple](./assets/product-add-simple.png){width="700" zoomable="yes"}

## Paso 2: Selección del conjunto de atributos

Para elegir el [conjunto de atributos](attribute-sets.md) que se usa como plantilla para el producto:

- Haga clic en el campo **[!UICONTROL Attribute Set]** e introduzca la totalidad o parte del nombre del conjunto de atributos.

- En la lista mostrada, elija el conjunto de atributos que desea utilizar.

El formulario se actualiza para reflejar el cambio.

![Elegir conjunto de atributos](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Paso 3: complete la configuración necesaria

1. Escriba **[!UICONTROL Product Name]**.

1. Acepte el valor predeterminado **[!UICONTROL SKU]** basado en el nombre del producto o escriba otro.

1. Escriba el producto **[!UICONTROL Price]**.

1. Dado que el producto aún no está listo para publicarse, establezca la opción **[!UICONTROL Enable Product]** en `No`.

1. haga clic en **[!UICONTROL Save]** y continúe.

   Cuando se guarda el producto, aparece el selector [Vista de tienda](introduction.md#product-scope) en la esquina superior izquierda.

1. Elija el **[!UICONTROL Store View]** en el que el producto estará disponible.

   ![Elija la vista de la tienda](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Paso 4: completar la configuración básica

1. Establezca **[!UICONTROL Tax Class]** en una de las siguientes opciones:

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

1. Escriba el **[!UICONTROL Quantity]** del producto que está en stock.

   De manera predeterminada, **[!UICONTROL Stock Status]** está establecido en `In Stock`.

   >[!NOTE]
   >
   >Si habilitas [Inventory management](../inventory-management/introduction.md), los comerciantes de Source único establecerán la cantidad en esta sección. Varios comerciantes de Source agregan orígenes y cantidades en la sección Orígenes. Consulte la siguiente sección _Asignar orígenes y cantidades (Inventory management)_.

1. Escriba **[!UICONTROL Weight]** del producto.

1. Acepte la configuración predeterminada **[!UICONTROL Visibility]** de `Catalog, Search`.

1. Para asignar _[!UICONTROL Categories]_&#x200B;al producto, haga clic en el cuadro **[!UICONTROL Select…]**&#x200B;y realice una de las acciones siguientes:

   **Elija una categoría existente**:

   - Empiece a escribir en el cuadro hasta que encuentre una coincidencia.

   - Seleccione la casilla de verificación de cada categoría que se va a asignar.

   **Crear una categoría**:

   - Haga clic en **[!UICONTROL New Category]**.

   - Escriba **[!UICONTROL Category Name]** y elija **[!UICONTROL Parent Category]**, que determina su posición en la estructura de menú.

   - Haga clic en **[!UICONTROL Create Category]**.

1. Para incluir el producto en la lista de [nuevos productos](../content-design/widget-new-products-list.md), seleccione la casilla de verificación **[!UICONTROL Set Product as New]**.

1. Elija **[!UICONTROL Country of Manufacture]**.

Puede haber atributos individuales adicionales que describan el producto. La selección varía según el conjunto de atributos y puede completarla más adelante.

### Asignar orígenes y cantidades ([!DNL Inventory Management])

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

## Paso 6: Publish del producto

1. Si está listo para publicar el producto en el catálogo, establezca el modificador **[!UICONTROL Enable Product]** en `Yes`.

1. Realice una de las siguientes acciones:

   - **Método 1:** Guardar y previsualizar

      - En la esquina superior derecha, haga clic en **[!UICONTROL Save]**.

      - Para ver el producto en tu tienda, elige **[!UICONTROL Customer View]** en el menú _Administrador_ (![Flecha de menú](../assets/icon-menu-down-arrow-black.png)).

     La tienda se abre en una nueva pestaña del explorador.

     ![Vista del cliente](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Método 2:** Guardar y cerrar

     En el menú _[!UICONTROL Save]_( ![flecha de menú](../assets/icon-menu-down-arrow-red.png){width="25"} ), elija **[!UICONTROL Save & Close]**.

## Cosas que recordar

- Los productos simples se pueden incluir en tipos de producto configurables, paquetes y agrupados.

- La configuración de producto simple anula las configuraciones de producto configurables para un producto específico.

- Un producto simple puede tener opciones personalizadas con varios tipos de entrada, lo que permite vender muchas variaciones de productos desde un único SKU.
