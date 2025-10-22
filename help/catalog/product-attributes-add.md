---
title: Añadir atributos a un producto
description: Obtenga información sobre cómo añadir atributos a los productos del catálogo.
exl-id: 1f92807a-2362-48a2-8d3a-4aef90a5671f
feature: Catalog Management, Products
source-git-commit: 45d69ccc1a5a6a7b8d072465c19829a76dde826d
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 0%

---

# Añadir atributos a un producto

Aunque los atributos se administran principalmente desde el menú [Tiendas](../stores-purchase/stores-menu.md), también puede agregar nuevos atributos _sobre la marcha_ mientras trabaja en un producto. Puede elegir de la lista de atributos existentes o crear un atributo. El nuevo atributo se agrega al [conjunto de atributos](../catalog/attribute-sets.md) en el que se basa el producto.

## Paso 1: Añadir un atributo

1. Abra el producto en modo de edición.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Attribute]**.

   ![Nuevo producto con conjunto de atributos predeterminado](./assets/product-attribute-add.png){width="600" zoomable="yes"}

1. Para agregar un atributo existente al producto, use los [controles de filtro](../getting-started/admin-grid-controls.md) para encontrar el atributo en la cuadrícula y haga lo siguiente:

   - Seleccione la casilla de verificación de la primera columna de cada atributo que desee añadir.

   - Haga clic en **[!UICONTROL Add Selected]**.

   ![Seleccionar un atributo](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

1. Para definir un nuevo atributo, haga clic en **[!UICONTROL Create New Attribute]** y complete los elementos del paso 2.

## Paso 2: Describir las propiedades básicas de los atributos

![Propiedades de atributo](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

1. En _[!UICONTROL Attribute Properties]_, escriba un **[!UICONTROL Attribute Label]**&#x200B;para identificar el atributo.

1. Establezca **[!UICONTROL Catalog Input Type for Store Owner]** en el tipo de [control de entrada](attributes-input-types.md) que se utilizará para la entrada de datos.

   Si el atributo se usa para un [producto configurable](product-create-configurable.md), elija `Dropdown`. Luego, establezca **[!UICONTROL Required]** en `Yes`.

1. Para los tipos de entrada `Dropdown` y `Multiple Select`, haga lo siguiente:

   - En **[!UICONTROL Values]**, haga clic en **[!UICONTROL Add Value]**.

   - Introduzca el primer valor que desee que aparezca en la lista.

     Puede introducir un valor para el administrador y una traducción del valor para cada vista de tienda. Si solo tiene una vista de tienda, solo puede introducir el valor Admin, que también se utiliza para la tienda.

   - Haga clic en **[!UICONTROL Add Value]** y repita el paso anterior para cada opción que desee incluir en la lista.

   - Seleccione **[!UICONTROL Is Default]** para usar la opción como valor predeterminado.

   ![Valores](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

1. Si desea que el cliente elija una opción antes de poder comprar el producto, establezca **[!UICONTROL Required]** en `Yes`.

## Paso 3: describir las propiedades avanzadas (opcional)

![Propiedades de atributo avanzadas](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. Escriba un **[!UICONTROL Attribute Code]** único en caracteres en minúsculas y sin espacios.

1. Establezca **[!UICONTROL Scope]** para indicar en qué parte de la jerarquía de la tienda se puede utilizar el atributo.

   Si el atributo se usa para un [producto configurable](product-create-configurable.md), elija `Global`.

1. Si este atributo se aplica solamente a este producto, establezca **[!UICONTROL Unique Value]** en `Yes`.

1. Para ejecutar una prueba de validez de los datos introducidos en un campo de texto, establezca **[!UICONTROL Input Validation for Store Owner]** en el tipo de datos que debe contener el campo.

   Este campo no está disponible para tipos de entrada con valores seleccionados. La validación de entrada se puede utilizar para cualquiera de las siguientes opciones:

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![Validación de entrada](./assets/product-attribute-input-validation.png){width="500"}

1. Si desea poder incluir el atributo como una columna en la cuadrícula Productos, establezca **[!UICONTROL Add to Column Options]** en `Yes`.

1. Si desea poder filtrar la cuadrícula _[!UICONTROL Products]_&#x200B;por esta columna, establezca **[!UICONTROL Use in Filter Options]**&#x200B;en `Yes`.

## Paso 4: introducir la etiqueta de campo

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Manage titles]**.

1. Escriba un(a) **[!UICONTROL Title]** para utilizarlo como etiqueta en el campo.

   Si la tienda está disponible en diferentes idiomas, puede introducir un título traducido para cada vista.

   ![Administrar títulos](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   > Si planea utilizar este atributo como faceta en Live Search, debe especificar una etiqueta específica de la tienda. Sin ella, es posible que el nombre del atributo no se muestre correctamente en la página de configuración de faceta. Para actualizar la configuración, edite manualmente la etiqueta con la opción [editar en la lista de facetas de Live Search](https://experienceleague.adobe.com/es/docs/commerce/live-search/live-search-admin/facets/facets-add#step-2-edit-facet-properties-optional) en la _Guía de Live Search_.

## Paso 5: Describir las propiedades de la tienda

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Storefront Properties]**.

   ![Propiedades de tienda](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

1. Para que el atributo esté disponible para la búsqueda, establezca **[!UICONTROL Use in Search]** en `Yes`.

1. Para incluir el atributo en la comparación de productos, establezca **[!UICONTROL Comparable on Storefront]** en `Yes`.

1. Para incluir atributos de lista desplegable, selección múltiple o precio en la navegación por capas, establezca **[!UICONTROL Use in Search Results Layered Navigation]** en uno de los siguientes:

   - `Filterable (with results)`: la navegación por capas incluye solo los filtros para los que se pueden encontrar productos coincidentes. Cualquier valor de atributo que ya se aplique a todos los productos mostrados en la lista no aparece como un filtro disponible. Los valores de atributo con un recuento de cero (0) coincidencias de producto también se omiten de la lista de filtros disponibles.<br/><br/>La lista filtrada de productos incluye solamente los productos que coinciden con el filtro. La lista de productos se actualiza únicamente si los filtros seleccionados cambian lo que se muestra.

   - `Filterable (no results)`: la navegación por capas incluye filtros para todos los valores de atributo disponibles y sus recuentos de productos, incluidos los productos con cero (0) coincidencias de productos. Si el valor del atributo es una muestra, el valor aparece como un filtro, pero se tachará.

   >[!NOTE]
   >
   >Cuando la configuración de _[!UICONTROL Use in Search]_&#x200B;está establecida en `No`, no se muestra la configuración de&#x200B;_[!UICONTROL Use in Search Results Layered Navigation]_ y no se usa el atributo de producto en la búsqueda con ningún valor de configuración de [!UICONTROL Use in Layered Navigation].

1. Para usar el atributo en la navegación por capas en las páginas de resultados de búsqueda, establezca **[!UICONTROL Use in Search Results Layered Navigation]** en `Yes` e introduzca un número en el campo **[!UICONTROL Position]**.

   El número de posición indica la posición relativa del atributo dentro del bloque de navegación por capas.

   >[!NOTE]
   >
   >El campo _[!UICONTROL Position]_&#x200B;está atenuado de forma predeterminada y debe guardar el atributo para poder modificar esta configuración.

1. Para usar el atributo en las reglas de precios, establezca **[!UICONTROL Use for Promo Rule Conditions]** en `Yes`.

1. Para permitir que se dé formato al texto con HTML, establezca **[!UICONTROL Allow HTML Tags on Storefront]** en `Yes`.

   Esta configuración hace que el editor de WYSIWYG esté disponible al editar el campo.

1. Para incluir el atributo en la página de productos, establezca **[!UICONTROL Visible on Catalog Pages on Storefront]** en `Yes`.

1. Complete la siguiente configuración según la temática:

   - Para incluir el atributo en los listados de productos, establezca **[!UICONTROL Used in Product Listing]** en `Yes`.

   - Para usar el atributo como parámetro de ordenación para las listas de productos, establezca **[!UICONTROL Used for Sorting in Product Listing]** en `Yes`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Attribute]**.
