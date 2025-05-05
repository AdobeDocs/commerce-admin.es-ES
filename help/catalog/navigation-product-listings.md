---
title: Listados de productos
description: Obtenga información sobre cómo modificar la configuración de la lista de productos, que determina cuántos productos aparecen por página y qué atributo se utiliza para ordenarla.
exl-id: 3779d9db-4adb-473b-b9c9-ad066f50b549
feature: Catalog Management, Products, Page Content
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Listados de productos

Los listados de productos se pueden configurar para que aparezcan de forma predeterminada como una lista o cuadrícula. También puede determinar cuántos productos aparecen por página y qué atributo se utiliza para ordenar la lista. La lista de productos incluye un conjunto de controles que se pueden utilizar para ordenar los productos, cambiar el formato de la lista, ordenar por atributo y avanzar de una página a otra.

>[!NOTE]
>
>Al ordenar una categoría por un atributo de producto, los productos con los mismos valores de atributo también se ordenan por su _[!UICONTROL Product ID]_&#x200B;en orden ascendente.

![Productos mostrados como una cuadrícula](./assets/storefront-catalog-page.png){width="700" zoomable="yes"}

## Configurar listados de productos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Storefront]**.

   ![Opciones de configuración de tienda](../configuration-reference/catalog/assets/catalog-storefront.png){width="600" zoomable="yes"}

   Para obtener una lista detallada de estas opciones, consulte [Storefront](../configuration-reference/catalog/catalog.md#storefront) en la _Referencia de configuración_.

   >[!NOTE]
   >
   >Para mostrar correctamente los productos y sus precios según la clasificación de _productos por precio_, asegúrese de que la configuración del precio que se muestra en la [configuración de impuestos sobre ventas](../configuration-reference/sales/tax.md) tenga el mismo valor (`Excluding Tax` **o** `Including Tax`). Para _[!UICONTROL Calculation Settings]_, compruebe el valor **[!UICONTROL Catalog Prices]**. Y para&#x200B;_[!UICONTROL Price Display Settings]_, compruebe el valor **[!UICONTROL Display Product Prices in Catalog]**. Si estos tienen valores diferentes, es posible que los filtros de precio de la navegación por capas no filtren y ordenen correctamente los productos por precio.

1. Establezca el valor predeterminado **[!UICONTROL List Mode]** en uno de los siguientes:

   - `Grid Only`
   - `List Only`
   - `Grid (default) / List`
   - `List (default / Grid`

1. Para **[!UICONTROL Products per Page on Grid Allowed Values]**, escriba el número de productos que desea que aparezcan por página cuando se muestren en formato de cuadrícula.

   Para introducir una selección de valores, separe cada número con una coma.

1. Para **[!UICONTROL Products per Page on Grid Default Value]**, introduzca el número predeterminado de productos que aparecerán en la cuadrícula por página.

1. Para **[!UICONTROL Products per Page on List Allowed Values]**, escriba el número de productos que desea que aparezcan por página cuando se muestren en formato de lista.

   Para introducir una selección de valores, separe cada número con una coma.

1. Para **[!UICONTROL Products per page on List Default Value]**, introduzca el número predeterminado de productos que aparecen en la lista, por página.

1. Establezca **[!UICONTROL Product Listing Sorted by]** en el atributo predeterminado que se utilizó inicialmente para ordenar la lista.

1. Para dar a los clientes la opción de enumerar todos los productos, establezca **[!UICONTROL Allow All Products on Page]** en `Yes`.

1. Si desea conservar toda la configuración de paginación a medida que los clientes naveguen por las listas de catálogos, establezca **[!UICONTROL Remember Category Pagination]** en `Yes`.

   Al habilitar esta configuración, se garantiza que el número de productos mostrados en una lista o cuadrícula se mantenga a medida que los compradores navegan de una categoría a otra. De forma predeterminada, este campo está establecido en `No` porque utiliza más almacenamiento de caché y puede afectar a la forma en que los motores de búsqueda indexan las páginas.

1. Si usa un [catálogo plano](catalog-flat.md) (**no recomendado**), haga lo siguiente:

   - Para mostrar un listado de productos de categoría plana, establezca **[!UICONTROL Use Flat Catalog Category]** en `Yes`.

   - Para mostrar una lista de productos plana, establezca **[!UICONTROL Use Flat Catalog Product]** en `Yes`.

1. Si desea permitir referencias dinámicas para recursos de medios en direcciones URL de categorías y productos, establezca **[!UICONTROL Allow Dynamic Media URLs in Products and Categories]** en `Yes`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Controles de página

| Control | Descripción |
|--- |--- |
| [!UICONTROL View As] | Muestra los productos en formato de cuadrícula o lista. |
| [!UICONTROL Sort By] | Cambia el orden de la lista. |
| [!UICONTROL Show Per Page] | Determina cuántos productos aparecen por página. |
| Vínculos de paginación | Vínculos de navegación a otras páginas. |

{style="table-layout:auto"}

## Controles de paginación

La configuración de Paginación aparece en la parte superior e inferior de la lista y controla el formato de los vínculos de paginación para las listas de productos. Puede establecer el número de vínculos que aparecen en el control y configurar los vínculos Next y Previous. Para que aparezcan los vínculos de paginación, debe haber más productos en la lista de los permitidos por página en la configuración de la lista de productos.

![Controles de paginación](./assets/storefront-pagination-controls.png){width="700" zoomable="yes"}

### Controles de paginación de tienda

| Control | Descripción |
|--- |--- |
| ![Cuadrícula de visualización](./assets/controls-pagination-list-grid.png) | [!UICONTROL View As] - Muestra la lista en formato de cuadrícula o lista. |
| ![Ordenar por](./assets/control-pagination-sort-by.png) | [!UICONTROL Sort By] - Cambia el orden de la lista. La propiedad de tienda _[!UICONTROL Used for Sorting in Product Listing]_&#x200B;determina qué [atributos de producto](../catalog/product-attributes.md) se pueden usar para ordenar la lista. |
| ![Mostrar por página](./assets/control-pagination-show-per-page.png) | [!UICONTROL Show Per Page]: determina cuántos productos aparecen por página. |
| ![Vínculos de paginación](./assets/control-pagination.png) | Vínculos de paginación: vínculos de navegación a otras páginas. |

{style="table-layout:auto"}

### Configuración de los controles de paginación

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Busque la vista de tienda que desea configurar y, en la columna **[!UICONTROL Action]**, haga clic en **[!UICONTROL Edit]**.

1. En **[!UICONTROL Other Settings]**, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Pagination]**.

   ![Paginación](./assets/config-design-pagination.png){width="600" zoomable="yes"}

   Para obtener más información acerca de esta configuración, vea [Configuración de diseño](../content-design/configuration.md).

1. Para **[!UICONTROL Pagination Frame]**, escriba el número de vínculos que desea que aparezcan en el control de paginación.

1. Para **[!UICONTROL Pagination Frame Skip]**, introduzca el número de vínculos que desea saltar antes de mostrar el siguiente conjunto de vínculos en el control de paginación.

   Por ejemplo, si el marco de paginación tiene cinco vínculos y desea ir a los cinco vínculos siguientes, ¿cuántos vínculos desea saltar? Si establece el valor en cuatro (`4`), el último vínculo del conjunto anterior es el primer vínculo del conjunto siguiente.

1. Para **[!UICONTROL Anchor Text for Previous]**, escriba el texto que desea que aparezca para el vínculo Anterior.

   Déjelo en blanco para utilizar la flecha predeterminada.

1. Para **[!UICONTROL Anchor Text for Next]**, escriba el texto que desea que aparezca para el vínculo Siguiente. Déjelo en blanco para utilizar la flecha predeterminada.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Configuration]**.
