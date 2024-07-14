---
title: Ordenar productos de categoría
description: Aprenda a definir el posicionamiento de productos en una categoría manualmente o aplicando un criterio de ordenación predefinido.
exl-id: 09c66a5d-57d4-4e78-a8d8-e3047c1bd35a
feature: Catalog Management, Categories, Products
source-git-commit: 14c3eb7d54776382bfa196efdac446d42c8dc940
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Ordenar productos de categoría

{{ee-feature}}

La posición de los productos en una categoría se puede especificar manualmente arrastrando y soltando los productos en la posición o aplicando un criterio de ordenación predefinido. De forma predeterminada, los productos se pueden ordenar por nivel de stock, edad, color, nombre, SKU y precio. La ordenación automática anula el orden de clasificación actual y restablece las posiciones de arrastrar y soltar establecidas manualmente. El criterio de ordenación de colores y el nivel mínimo de existencias que pueden ser necesarios para que los productos se incluyan en la lista se establecen en la configuración de [Visual Merchandiser](../configuration-reference/catalog/visual-merchandiser.md).

>[!NOTE]
>
>En las páginas de categoría, `Out of stock` productos siempre se muestran **_después de_** `In Stock` productos en la lista de productos con todos los tipos de clasificación.

Puede configurar las opciones de categoría por separado para cada [vista de tienda](../stores-purchase/stores.md#add-stores) para determinar la selección de productos, su posición relativa en la lista y los atributos disponibles para las reglas de categoría. Sin embargo, hay un único criterio de ordenación **_global_** y una posición de producto en el catálogo, y se comparten en [vistas de tiendas](../stores-purchase/store-views.md), tiendas y sitios web.

## Paso 1: establecer el ámbito de la configuración

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Si es necesario, elija el **[!UICONTROL Store View]** donde se aplica la configuración.

   Para una instalación de varias tiendas, la configuración _[!UICONTROL Store View]_aplica el criterio de ordenación a todas las vistas disponibles en la tienda.

1. En el árbol de categorías de la izquierda, elija la categoría que desea editar.

   ![Árbol de categorías](./assets/category-selected.png){width="700" zoomable="yes"}

## Paso 2: Ordenar los productos

>[!NOTE]
>
>Al ordenar una categoría por un atributo de producto, los productos con los mismos valores de atributo también se ordenan por su _[!UICONTROL Product ID]_en orden ascendente.

En la sección _[!UICONTROL Products in Category]_, haga clic en el icono de mosaicos ( ![Ver mosaicos](../assets/icon-view-tiles.png) ) para mostrar los mosaicos del producto en una cuadrícula. Utilice el método manual o automático para ordenar los productos.

![Mosaicos de productos](./assets/category-products-tiles.png){width="600" zoomable="yes"}

### Método 1: orden manual

1. Establezca **[!UICONTROL Sort Order]** según sus preferencias.

   ![Orden](./assets/category-edit-sort-order.png){width="600" zoomable="yes"}

1. Para aplicar el nuevo orden, haga clic en **[!UICONTROL Sort]**.

1. Para guardar el orden, haga clic en **[!UICONTROL Save Category]**.

1. Cuando se le solicite, actualice los indexadores no válidos.

### Método 2: ordenación automática

1. Establecer **[!UICONTROL Match products by rule]** (![Alternar sí](../assets/toggle-yes.png)) a `Yes`.


1. Establezca **[!UICONTROL Automatic Sorting]** según sus preferencias.

1. Para crear una regla de categoría, siga las instrucciones del paso siguiente.

## Paso 3: Crear una regla de categoría

1. Establecer **[!UICONTROL Match products by rule]** (![Alternar sí](../assets/toggle-yes.png)) a `Yes`.

1. Haga clic en **[!UICONTROL Add Condition]**.

1. Elija **[!UICONTROL Attribute]** que es la base de la condición.

1. Establezca **[!UICONTROL Operator]** en una de las siguientes opciones:

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. Escriba el **[!UICONTROL Value]** apropiado.

   ![Condición de categoría](./assets/category-rule-create.png){width="600" zoomable="yes"}

1. Para agregar otra condición, haga clic en **[!UICONTROL Add Condition]** y repita el proceso.

## Paso 4: guardar, actualizar y verificar

1. Una vez finalizado, haga clic en **[!UICONTROL Save Category]**.

1. Cuando se le pida que actualice la caché, haga clic en **[!UICONTROL Cache Management]** y actualice cada caché no válida.

1. En la tienda, compruebe que las reglas de selección, ordenación y categoría de productos funcionan correctamente.

   Si debe realizar ajustes, cambie la configuración e inténtelo de nuevo.
