---
title: Añadir atributos a un producto
description: Obtenga información sobre cómo añadir atributos a los productos del catálogo.
exl-id: 1f92807a-2362-48a2-8d3a-4aef90a5671f
feature: Catalog Management, Products
source-git-commit: 99049260b4ff490845affd1c98fa4d2536edebd7
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---

# Añadir atributos a un producto

Aunque los atributos se administran principalmente desde el [Tiendas](../stores-purchase/stores-menu.md) , también puede añadir nuevos atributos _sobre la marcha_ mientras se trabaja en un producto. Puede elegir de la lista de atributos existentes o crear un atributo. El nuevo atributo se añade a la variable [conjunto de atributos](../catalog/attribute-sets.md) en el que se basa el producto.

## Paso 1: Añadir un atributo

1. Abra el producto en modo de edición.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Attribute]**.

   ![Nuevo producto con conjunto de atributos predeterminado](./assets/product-attribute-add.png){width="600" zoomable="yes"}

1. Para añadir un atributo existente al producto, utilice el [controles de filtro](../getting-started/admin-grid-controls.md) para buscar el atributo en la cuadrícula, haga lo siguiente:

   - Seleccione la casilla de verificación de la primera columna de cada atributo que desee añadir.

   - Clic **[!UICONTROL Add Selected]**.

   ![Seleccionar un atributo](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

1. Para definir un nuevo atributo, haga clic en **[!UICONTROL Create New Attribute]** y complete los elementos del paso 2.

## Paso 2: Describir las propiedades básicas de los atributos

![Propiedades de atributo](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

1. En _[!UICONTROL Attribute Properties]_, introduzca un **[!UICONTROL Attribute Label]**para identificar el atributo.

1. Establecer **[!UICONTROL Catalog Input Type for Store Owner]** al tipo de [control de entrada](attributes-input-types.md) para la entrada de datos.

   Si el atributo se utiliza para una [producto configurable](product-create-configurable.md), elija `Dropdown`. A continuación, establezca **[!UICONTROL Required]** hasta `Yes`.

1. Para `Dropdown` y `Multiple Select` tipos de entrada, haga lo siguiente:

   - En **[!UICONTROL Values]**, haga clic en **[!UICONTROL Add Value]**.

   - Introduzca el primer valor que desee que aparezca en la lista.

     Puede introducir un valor para el administrador y una traducción del valor para cada vista de tienda. Si solo tiene una vista de tienda, solo puede introducir el valor Admin, que también se utiliza para la tienda.

   - Clic **[!UICONTROL Add Value]** y repita el paso anterior para cada opción que desee incluir en la lista.

   - Seleccionar **[!UICONTROL Is Default]** para utilizar la opción como valor predeterminado.

   ![Valores](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

1. Si desea exigir al cliente que elija una opción antes de poder comprar el producto, configure **[!UICONTROL Required]** hasta `Yes`.

## Paso 3: describir las propiedades avanzadas (opcional)

![Propiedades de atributo avanzadas](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. Introduzca un único **[!UICONTROL Attribute Code]** en minúsculas y sin espacios.

1. Establecer **[!UICONTROL Scope]** para indicar en qué parte de la jerarquía de la tienda se puede utilizar el atributo.

   Si el atributo se utiliza para una [producto configurable](product-create-configurable.md), elija `Global`.

1. Si este atributo solo se aplica a este producto, establezca **[!UICONTROL Unique Value]** hasta `Yes`.

1. Para ejecutar una prueba de validez de cualquier dato introducido en un campo de texto, establezca **[!UICONTROL Input Validation for Store Owner]** al tipo de datos que debe contener el campo.

   Este campo no está disponible para tipos de entrada con valores seleccionados. La validación de entrada se puede utilizar para cualquiera de las siguientes opciones:

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![Validación de entrada](./assets/product-attribute-input-validation.png){width="500"}

1. Si desea poder incluir el atributo como una columna en la cuadrícula Productos, establezca **[!UICONTROL Add to Column Options]** hasta `Yes`.

1. Si desea poder filtrar el _[!UICONTROL Products]_cuadrícula por esta columna, establecer **[!UICONTROL Use in Filter Options]**hasta `Yes`.

## Paso 4: introducir la etiqueta de campo

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Manage titles]** sección.

1. Introduzca una **[!UICONTROL Title]** se utilizará como etiqueta para el campo.

   Si la tienda está disponible en diferentes idiomas, puede introducir un título traducido para cada vista.

   ![Administrar títulos](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## Paso 5: Describir las propiedades de la tienda

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Storefront Properties]** sección.

   ![Propiedades de tienda](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

1. Para que el atributo esté disponible para la búsqueda, establezca **[!UICONTROL Use in Search]** hasta `Yes`.

1. Para incluir el atributo en la comparación de productos, establezca **[!UICONTROL Comparable on Storefront]** hasta `Yes`.

1. Para incluir atributos de lista desplegable, de selección múltiple o de precio en la navegación por capas, establezca **[!UICONTROL Use in Search Results Layered Navigation]** a uno de los siguientes:

   - `Filterable (with results)` - La navegación por capas incluye solo los filtros para los que se pueden encontrar productos coincidentes. Cualquier valor de atributo que ya se aplique a todos los productos mostrados en la lista no aparece como un filtro disponible. Los valores de atributo con un recuento de cero (0) coincidencias de producto también se omiten de la lista de filtros disponibles.<br/><br/>La lista filtrada de productos incluye solo los productos que coinciden con el filtro. La lista de productos se actualiza únicamente si los filtros seleccionados cambian lo que se muestra.

   - `Filterable (no results)` : La navegación por capas incluye filtros para todos los valores de atributos disponibles y sus recuentos de productos, incluidos los productos con cero (0) coincidencias de productos. Si el valor del atributo es una muestra, el valor aparece como un filtro, pero se tachará.

   >[!NOTE]
   >
   >Si la variable _[!UICONTROL Use in Search]_se establece en `No`, el_[!UICONTROL Use in Search Results Layered Navigation]_ no se muestra y el atributo de producto no se utiliza en la búsqueda con ningún [!UICONTROL Use in Layered Navigation] valor de configuración.

1. Para utilizar el atributo en la navegación por capas en las páginas de resultados de búsqueda, establezca **[!UICONTROL Use in Search Results Layered Navigation]** hasta `Yes` e introduzca un número en la **[!UICONTROL Position]** field.

   El número de posición indica la posición relativa del atributo dentro del bloque de navegación por capas.

   >[!NOTE]
   >
   >El _[!UICONTROL Position]_El campo está atenuado de forma predeterminada y debe guardar el atributo para poder modificar esta configuración.

1. Para utilizar el atributo en reglas de precios, establezca **[!UICONTROL Use for Promo Rule Conditions]** hasta `Yes`.

1. Para permitir que el texto tenga formato de HTML, establezca **[!UICONTROL Allow HTML Tags on Storefront]** hasta `Yes`.

   Esta configuración hace que el editor WYSIWYG esté disponible al editar el campo.

1. Para incluir el atributo en la página del producto, defina **[!UICONTROL Visible on Catalog Pages on Storefront]** hasta `Yes`.

1. Complete la siguiente configuración según la temática:

   - Para incluir el atributo en las listas de productos, defina **[!UICONTROL Used in Product Listing]** hasta `Yes`.

   - Para utilizar el atributo como parámetro de ordenación para las listas de productos, establezca **[!UICONTROL Used for Sorting in Product Listing]** hasta `Yes`.

1. Cuando termine, haga clic en **[!UICONTROL Save Attribute]**.
