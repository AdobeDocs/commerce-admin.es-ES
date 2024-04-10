---
title: Navegación por capas
description: Descubra cómo la navegación por capas facilita a los compradores la búsqueda de productos en función de la categoría, el intervalo de precios o cualquier otro atributo disponible.
exl-id: 5f17528a-3593-449c-a044-98736a4ae913
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 99049260b4ff490845affd1c98fa4d2536edebd7
workflow-type: tm+mt
source-wordcount: '1303'
ht-degree: 0%

---

# Navegación por capas

>[!NOTE]
>
>La navegación por capas estándar descrita en esta sección difiere de la navegación filtrada por Live Search con [facetas](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/facets/facets.html).

La navegación por capas facilita la búsqueda de productos en función de la categoría, el intervalo de precios o cualquier otro atributo disponible. La navegación por capas suele aparecer en la columna izquierda de los resultados de búsqueda y las páginas de categoría y, a veces, en la página de inicio. La navegación estándar incluye un _Comprar por_ lista de categorías y rango de precios. Puede configurar la visualización de la navegación por capas, incluido el recuento de productos y el intervalo de precios.

![Navegación por niveles por categoría y precio](./assets/navigation-layered-basic.png){width="700" zoomable="yes"}

## Atributos filtrables

>[!NOTE]
>
>Los requisitos de atributos filtrables que se describen en este tema son diferentes para [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html). Para obtener más información, consulte [Facetas](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/facets/facets.html).

La navegación por capas se puede utilizar para buscar productos por categoría o por atributo. Por ejemplo, cuando un comprador elige la categoría Hombres/Pantalones cortos de la barra de navegación superior, los resultados iniciales incluyen todos los productos de la categoría. La lista se puede filtrar aún más eligiendo un estilo, un clima, un color, un material, un patrón o un precio específicos, o una combinación de valores. Los atributos filtrables aparecen en una sección en expansión que enumera cada valor de atributo. Como opción, la lista de productos con resultados coincidentes se puede configurar para incluir productos con o sin coincidencia.

Las propiedades del atributo, combinadas con el tipo de entrada del producto, determinan qué atributos se pueden utilizar para la navegación por capas. La navegación por capas solo está disponible para [_anclaje_](categories-display-settings.md) categorías, pero también se puede agregar a las páginas de resultados de búsqueda. El **Tipo de entrada de catálogo del propietario de la tienda** La propiedad de cada atributo debe establecerse en `Yes/No`, `Dropdown`, `Multiple Select`, o `Price`. Para que los atributos sean filtrables, la variable **Uso en la navegación por capas** La propiedad de cada debe establecerse en `Filterable (with results)` o `Filterable (no results)`.

_Ejemplo: Atributos filtrables con resultados_

![Atributos filtrables en la navegación por capas](./assets/storefront-layered-navigation-filtered.png){width="700" zoomable="yes"}

_Ejemplo: Valores de muestra filtrables mostrados sin resultado_

![Valor de muestra filtrable sin resultados](./assets/storefront-product-attribute-filter-no-results.png){width="700" zoomable="yes"}

Las siguientes instrucciones muestran cómo configurar la navegación básica por capas con atributos que se pueden filtrar. Para obtener información sobre la navegación por capas avanzada con pasos de precio, consulte [Navegación de precios](navigation-layered.md#configure-price-navigation).

## Paso 1: Configurar las propiedades del atributo

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Examine o utilice la búsqueda filtrada para buscar un atributo en la lista y abrirlo en modo de edición.

   ![Introduzca términos de búsqueda por columna para utilizar la búsqueda filtrada](./assets/attribute-search.png){width="700" zoomable="yes"}

1. En el panel izquierdo, elija **[!UICONTROL Storefront Properties]** y establecer **[!UICONTROL Use In Layered Navigation]** a uno de los siguientes:

   - `Filterable (with results)` - La navegación por capas incluye solo los filtros para los que se pueden encontrar productos coincidentes. Cualquier valor de atributo que ya se aplique a todos los productos mostrados en la lista debe aparecer como filtro disponible. Los valores de atributo con un recuento de cero (0) coincidencias de producto se omiten de la lista de filtros disponibles. La lista filtrada incluye solo los productos que coinciden con el filtro. La lista de productos se actualiza únicamente si los filtros seleccionados cambian lo que se muestra.

   - `Filterable (no results)` : La navegación por capas incluye filtros para todos los valores de atributos disponibles y sus recuentos de productos, incluidos los productos con cero (0) coincidencias de productos. Si el valor del atributo es una muestra, el valor aparece como un filtro, pero se tachará. Esta opción no admite el filtrado por niveles de precio y no afecta a los filtros de precio.

1. Establecer **[!UICONTROL Use In Search Results Layered Navigation]** hasta `Yes`.

   ![Propiedades de tienda](./assets/attribute-storefront-properties.png){width="600" zoomable="yes"}

1. Repita estos pasos para cada atributo que desee incluir en la navegación por capas.

>[!NOTE]
>
>Si la variable _[!UICONTROL Use in Search]_se establece en `No`, el_[!UICONTROL Use in Search Results Layered Navigation]_ no se muestra y el atributo de producto no se utiliza en la búsqueda con ningún [!UICONTROL Use in Layered Navigation] valor de configuración.

>[!NOTE]
>
>El [!UICONTROL Position] El campo está atenuado de forma predeterminada, por lo que debe guardar el atributo antes de poder modificar esta configuración.

## Paso 2: Hacer de la categoría un anclaje

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. En el árbol de categorías, seleccione la categoría en la que desea utilizar la navegación por capas.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Display Settings]** sección y conjunto **[!UICONTROL Anchor]** hasta `Yes`.

   ![Configuración de visualización de categoría](./assets/category-layered-navigation-anchor.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save]**.

## Paso 3: Prueba de los resultados

Para probar la configuración, visite su tienda y vaya a la categoría desde el menú principal. La selección de atributos filtrables aparece en la navegación por capas de la página de categoría.

Busque, filtre y revise los productos mostrados.

## Eliminación de valores de atributos filtrables de la navegación por capas

La navegación por capas incluye filtros para todos los valores de atributos disponibles y sus recuentos de productos, incluidos los productos con cero (0) coincidencias de productos (como se muestra en la siguiente imagen).

![Visualización de cero filtros](./assets/filterable-attributes-on-plp.png){width="700" zoomable="yes"}

Este resultado puede dificultar que los clientes seleccionen un producto preferido y no es necesario mostrar valores de atributo con 0 productos en el front-end.

Puede seguir los siguientes pasos para eliminar de la navegación por capas los valores de atributos que se pueden filtrar con 0 productos:

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Examine o utilice la búsqueda filtrada para buscar un atributo en la lista y abrirlo en modo de edición.

1. En _[!UICONTROL Attribute Information]_, haga clic en **[!UICONTROL Storefront Properties]**.

1. Para **[!UICONTROL Layered Navigation]**, elija `Filterable (with results)`.

   ![Sección Información de Atributos](./assets/storefront-properties-tab.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save Attribute]**.

## Navegación de precios

>[!NOTE]
>
>La configuración de navegación de precios descrita en este tema difiere para [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

La navegación de precios se puede utilizar para distribuir productos por rango de precios en la navegación por capas. También puede dividir cada intervalo en intervalos. Existen varias formas de calcular la navegación de precios:

- Automático (Igualar intervalos de precios)
- Automático (ecualizar recuentos de productos)
- Manual

Con los dos primeros métodos, los pasos de navegación se calculan automáticamente. El método manual permite especificar un límite de división para los intervalos de precio. El siguiente ejemplo muestra la diferencia entre los pasos de navegación de precios de 10 y 100.

La división iterativa proporciona la mejor distribución de productos entre rangos de precios. Con la división iterativa, después de elegir el rango de 0,00 a 99 dólares, el cliente puede explorar en profundidad varios subrangos de precios. La división del intervalo de precios se detiene cuando el número de productos alcanza el umbral establecido por el límite de división de intervalo.

## Ejemplo: Pasos de navegación de precios

| Paso de precio por 10 | Paso de precio por 100 |
|----------|--------|
| $20.00 - $29.99 (1) | $0.00 - $99.99 (4) |
| 30,00 $ - 39,99 $ (2) | DE 100 A 199,99 $ (5) |
| $70.00 - $79.99 (1) | $400.00 - $499.99 (2) |
| 100,00 $ - 109,99 $ (1) | $700.00 y superior (1) |
| 120,00 $ - 129,99 $ (2) |   |
| 150,00 $ - 159,99 $ (1) |   |
| 180,00 $ - 189,99 $ (1) |   |
| $420.00 - $429.99 (1) |   |
| $440.00 - $449.99 (1) |   |
| $710.00 y superior (1) |   |

{style="table-layout:auto"}

## Configuración de la navegación de precios

>[!IMPORTANT]
>
>Para mostrar correctamente los productos y sus precios según _filtros de precio_ en la navegación por capas, asegúrese de que los ajustes del precio se muestran en la [Configuración de impuestos](../configuration-reference/sales/tax.md) tienen el mismo valor (`Excluding Tax` **o** `Including Tax`). Para el _[!UICONTROL Calculation Settings]_, marque la **[!UICONTROL Catalog Prices]**valor. Y para_[!UICONTROL Price Display Settings]_, marque la **[!UICONTROL Display Product Prices in Catalog]** valor. Si estos tienen valores diferentes, es posible que los filtros de precio de la navegación por capas no filtren y ordenen correctamente los productos por precio.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el _Navegación por capas_ sección.

   De forma predeterminada, **[!UICONTROL Display Product Count]** se establece en `Yes`. Si es necesario, anule la selección del **[!UICONTROL Use system value]** para cambiar esta configuración.

   ![Navegación por capas](../configuration-reference/catalog/assets/layered-navigation.png){width="600" zoomable="yes"}

   Para obtener una lista detallada de estas opciones de configuración, consulte [Navegación por capas](../configuration-reference/catalog/catalog.md#layered-navigation) en el _Referencia de configuración_.

1. Establecer **[!UICONTROL Price Navigation Steps Calculation]** para uno de los métodos de las secciones siguientes.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

### Método 1: Automático (igualar intervalos de precios)

Salir **[!UICONTROL Price Navigation Steps Calculation]** establezca en `Automatic (Equalize Price Ranges)` (valor predeterminado). Esta configuración utiliza el algoritmo estándar para la navegación de precios.

### Método 2: automático (igualar los recuentos de productos)

>[!TIP]
>
>Si es necesario, anule primero la selección del **[!UICONTROL Use system value]** para cambiar esta configuración.

1. Establecer **[!UICONTROL Price Navigation Steps Calculation]** hasta `Automatic (equalize product counts)`.

1. Para mostrar un solo precio cuando hay varios productos con el mismo precio, establezca **[!UICONTROL Display Price Interval as One Price]** hasta `Yes`.

1. Para **[!UICONTROL Interval Division Limit]**, introduzca el umbral para el número de productos dentro de un rango de precios.

   El rango no se puede dividir más allá de este límite. El valor predeterminado es `9`.

   ![Automático (igualar recuentos de productos)](../configuration-reference/catalog/assets/layered-navigation-equalize-product-counts.png){width="600" zoomable="yes"}

### Método 3: manual

>[!NOTE]
>
>Si es necesario, anule primero la selección del **[!UICONTROL Use system value]** para cambiar esta configuración.

1. Establecer **[!UICONTROL Price Navigation Steps Calculation]** hasta `Manual`.

1. Introduzca un valor que determine el **[!UICONTROL Default Price Navigation Step]**.

1. Introduzca el **[!UICONTROL Maximum Number of Price Intervals]** permitido, hasta `100`.

   ![Manual](../configuration-reference/catalog/assets/layered-navigation-manual.png){width="600" zoomable="yes"}

## Configuración de la navegación por capas

>[!NOTE]
>
>La configuración estándar descrita en esta página difiere para [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

La configuración de navegación por capas determina si aparece un recuento de productos entre paréntesis después de cada atributo y el tamaño del cálculo del paso que se utiliza en la navegación de precios.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda _[!UICONTROL Catalog]_y elija **[!UICONTROL Catalog]**debajo.

1. Expanda el _[!UICONTROL Layered Navigation]_sección.

   >[!NOTE]
   >
   >Si es necesario, anule primero la selección del **[!UICONTROL Use system value]** para cambiar esta configuración.

1. Para mostrar el número de productos encontrados para cada atributo, establezca **[!UICONTROL Display Product Count]** hasta `Yes`.

1. Establecer **[!UICONTROL Price Navigation Step Calculation]** hasta `Automatic (equalize price ranges)`.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.
