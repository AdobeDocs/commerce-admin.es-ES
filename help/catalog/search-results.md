---
title: Resultados de búsqueda
description: Obtenga información sobre cómo configurar el modo en que los productos coinciden con los criterios de búsqueda introducidos en el cuadro Búsqueda rápida o en el formulario Búsqueda avanzada.
exl-id: c721fb3b-ee31-4d2b-b4ea-9ae2c80aa800
feature: Catalog Management, Search
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 0%

---

# Resultados de búsqueda

>[!NOTE]
>
>Esta página describe la funcionalidad de búsqueda estándar que podría diferir de [Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html).

La lista _Resultados de búsqueda_ incluye todos los productos que coinciden con los criterios de búsqueda especificados en el cuadro Búsqueda rápida o en el formulario Búsqueda avanzada. Cada lista de productos del catálogo tiene esencialmente los mismos controles. La única diferencia es que uno es el resultado de una consulta de búsqueda y la otra diferencia es el resultado de [navegación](navigation.md).

Los resultados pueden tener el formato de una cuadrícula o lista y ordenarse por una selección de atributos. Los controles de paginación aparecen si hay más productos de los que caben en la página. Utilice estos controles para desplazarse de una página a otra. El número de registros por página viene determinado por la configuración de front-end del catálogo. Para obtener más información, vea [Listados de productos](navigation-product-listings.md).

Con **Elasticsearch**:

- No hay compatibilidad predeterminada para la búsqueda por el sufijo. Por ejemplo, la búsqueda por SKU puede no devolver el resultado esperado si la palabra clave contiene solo la parte final del SKU.
- Solo se admite de serie la búsqueda por prefijo (búsqueda de palabras clave parcial) para los atributos de producto `name` y `sku`. Todos los demás atributos del producto se buscan por la palabra clave completa, con la coincidencia exacta.
- Los resultados de búsqueda para los atributos de producto `name` y `sku` se basan en la relevancia, no en la coincidencia exacta. Las coincidencias más relevantes, como un _Nombre del producto_ o _SKU_ que coinciden exactamente, se enumeran primero. Para buscar una coincidencia exacta, el cliente puede utilizar comillas dobles en la consulta de búsqueda. Por ejemplo, una consulta de búsqueda `WSH12-32-Red` puede devolver varios productos, ordenados por la relevancia. Pero una consulta de búsqueda `"WSH12-32-Red"` devuelve solamente un producto con **_exactamente_** coincidente con `sku`.

![Resultados de búsqueda con controles de paginación](./assets/storefront-search-results-shorts.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>Debido al anuncio de fin de soporte de Elasticsearch 7 para agosto de 2023, se recomienda que todos los clientes de Adobe Commerce migren al motor de búsqueda OpenSearch 2.x. Para obtener información sobre cómo migrar el motor de búsqueda durante la actualización del producto, consulte [Migración a OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) en la _Guía de actualización_.

## Asignación de palabras clave para ampliar los resultados de búsqueda

Esta técnica utiliza un atributo para crear una asociación basada en palabras clave entre dos productos, de modo que una búsqueda de cualquiera de ellos devuelva resultados para ambos. Puede utilizar la asignación de palabras clave para promocionar un producto en los resultados de búsqueda donde de otra manera no aparecería.

![Resultados de búsqueda con asignación de palabras clave](./assets/storefront-search-results-extended.png){width="700" zoomable="yes"}

El siguiente ejemplo utiliza la asignación de palabras clave basada en SKU. Cuando se introduce un SKU en el cuadro de búsqueda, ambos productos aparecen en los resultados. Se asignan los SKU de los siguientes productos configurables, en lugar de los SKU de las variaciones de productos:

- Montana Wind Jacket (MJ03)
- Chaz Sudadera con capucha Kangaroo (MH01)

### Paso 1: Crear un atributo

1. En la lista _[!UICONTROL Products]_, abra `Montana Wind Jacket` (MJ03) en modo de edición.
1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Attribute]**.
1. En la página _Seleccionar atributo_, haga clic en **[!UICONTROL Create New Attribute]**.
1. Complete las propiedades del atributo como se indica a continuación:

   **[!UICONTROL Attribute Properties]**

   - [!UICONTROL Attribute Label] - `Search Keywords`
   - [!UICONTROL Catalog Input Type for Store Owner] - `Text Field`

   **[!UICONTROL Advanced Attribute Properties]**

   - [!UICONTROL Add to Column Options] - `Yes` (predeterminado)
   - [!UICONTROL Use in Filter Options] - `Yes` (predeterminado)

   **[!UICONTROL Storefront Properties]**

   - [!UICONTROL Use in Search] - `Yes`
   - [!UICONTROL Visible on Catalog Pages in the Storefront] - `No`
   - [!UICONTROL Used in Product Listings] - `No`

1. Una vez finalizado, haga clic en **[!UICONTROL Save Attribute]**.

   El atributo se agrega al conjunto de atributos del producto.

### Paso 2: Asignación del primer producto

1. En la página de configuración del producto, desplácese hacia abajo y expanda la sección _[!UICONTROL Attributes]_.
1. En el campo **[!UICONTROL Search Keywords]**, introduzca la SKU `MH01` que se debe asignar a este producto.

   Puede introducir varios SKU separados por un espacio en el campo Buscar palabras clave. En este ejemplo, solo se introduce uno.

   ![Sección de atributos con palabra clave de búsqueda](./assets/search-keywords-attribute.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.
1. Vaya a **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**&#x200B;y actualice **[!UICONTROL Page Cache]**.

### Paso 3: Asignación del segundo producto

1. En la lista _[!UICONTROL Products]_, abra `Chaz Kangaroo Hoodie` (MH01) en modo de edición.
1. Desplácese hacia abajo y expanda la sección **[!UICONTROL Attributes]**.
1. En el campo **[!UICONTROL Search Keywords]**, introduzca la SKU del otro producto, `MJ03`.
1. Haga clic en **[!UICONTROL Save]**.
1. Vaya a **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**&#x200B;y actualice **[!UICONTROL Page Cache]**.

### Paso 4: Probarlo en la tienda

1. Vaya a la tienda e introduzca `MJ03` en el cuadro _Búsqueda rápida_.
1. Compruebe que ambos productos se devuelven en la lista de resultados de búsqueda.

## Búsqueda ponderada

A los atributos de producto que están habilitados para la búsqueda en el catálogo se les puede asignar un peso para darles un valor más alto en los resultados de búsqueda. Los atributos con un peso mayor se devuelven antes que los atributos con un peso menor. Por ejemplo, si hay dos atributos en el sistema, _color_ con una ponderación de búsqueda de 3 y _description_ con una ponderación de búsqueda de 1. Una búsqueda de la palabra _red_ devuelve una lista de productos con un valor de atributo de color de `red` en la parte superior de los resultados de búsqueda y devuelve productos con descripciones que contienen la palabra _red_ en la parte inferior de los resultados de búsqueda. En este ejemplo, el atributo `color` tiene un peso definido mayor que el atributo `description`.

>[!IMPORTANT]
>
>La ordenación por relevancia se ve afectada por **_varios_** criterios y relaciones entre ellos **_al mismo tiempo_**. [!UICONTROL Search Weight] es solo uno de esos criterios. Esto significa que, a veces, los atributos con una ponderación de búsqueda menor pueden seguir teniendo más relevancia que los atributos con una ponderación de búsqueda mayor. Otros criterios pueden incluir el número de coincidencias en cualquier atributo determinado, la posición del término de búsqueda encontrado y la estructura general del texto antes y después de un término de búsqueda.

**_Para establecer las propiedades de peso de búsqueda de un atributo:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Busque el atributo en la lista y ábralo en modo de edición.

1. En el panel izquierdo, elija **[!UICONTROL Storefront Properties]** y haga lo siguiente:

   - Para incluir el atributo en las consultas de búsqueda, establezca **[!UICONTROL Use in Search]** en `Yes`.

   - Para establecer el valor de búsqueda del atributo, establezca **[!UICONTROL Search Weight]** en un número del 1 al 10, donde `10` tiene la prioridad más alta. Si no se escribe ningún valor, todos los atributos tienen de manera predeterminada una ponderación de búsqueda de `1`.

   ![Peso de búsqueda](./assets/search-weight.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Attribute]**.
