---
title: Creación de categorías
description: Puede crear tantas subcategorías adicionales como sea necesario, según la profundidad de menú máxima establecida en la configuración.
exl-id: 8ba5fc1a-3bf2-4a29-bbc3-709fc0ad7497
feature: Catalog Management, Categories
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1099'
ht-degree: 0%

---

# Creación de categorías

La estructura de categorías del catálogo es similar a un árbol invertido, con la raíz en la parte superior. Cada sección del árbol se puede expandir y contraer. Las categorías deshabilitadas u ocultas aparecen atenuadas. Las categorías del primer nivel (debajo de [raíz](category-root.md)) aparecen normalmente como opciones en la [menú principal](navigation-top.md). Puede crear tantas subcategorías adicionales como sea necesario, según la profundidad de menú máxima establecida en la configuración. Las categorías se pueden arrastrar y soltar en otras ubicaciones del árbol. El número de ID de categoría aparece entre paréntesis después del nombre de la categoría en la parte superior de la página.

Para un sitio web con varios [tiendas](../stores-purchase/stores.md#add-stores), puede crear una categoría raíz diferente para cada almacén que defina el conjunto de categorías que se usa para [navegación superior](navigation-top.md).

![Árbol de categorías](./assets/category-selected.png){width="700" zoomable="yes"}

## Prácticas recomendadas

Siga estas prácticas recomendadas cuando planifique y cree categorías.

### Estructura de categoría

La estructura de las categorías del menú principal puede afectar a la experiencia del cliente y al rendimiento. Como práctica recomendada, debe identificar una categoría de nivel superior global y evitar que otras categorías tengan el mismo nombre. Por ejemplo, en lugar de tener varias categorías para &quot;Niños&quot; organizadas en diferentes departamentos, como `Clothing/Kids`, `Shoes/Kids`, `Accessories/Kids`. Puede ser más eficiente crear la categoría principal de nivel superior `Kids`y, a continuación, cree las subcategorías que sean necesarias. Sea coherente con la estructura de categorías y utilice el mismo método para todos los tipos de productos del catálogo.

### Reglas empresariales y automatización

Tenga en cuenta la estructura de categorías y los valores de atributo disponibles cuando utilice la lógica empresarial para mostrar elementos similares en una página del catálogo o para configurar una promoción personalizada, un proceso automatizado o criterios de búsqueda. Por ejemplo, si especifica &quot;grupo&quot; como categoría principal, los resultados pueden incluir productos mixtos que no sean apropiados para el sexo y la edad. Sin embargo, si coincide con una subcategoría específica de polos, los resultados son más estrechos y es probable que atraigan a un cliente específico. Los resultados pueden ser aún más específicos cuando se combinan con otros valores de atributo dirigidos a un cliente específico. Tenga en cuenta el número de productos que deben filtrarse y recuperarse al hacer referencia a una ruta de categoría específica. La diferencia en los resultados puede ser dramática. Tenga en cuenta los diferentes resultados devueltos por las siguientes rutas de categoría:

- `[Category:  All Products/Shirts/Father's Day/Polos/Sale]`
- `[Category Path: Men/Shirts/Polos]`
- `[Child Category: Polos]`

Es importante definir claramente las relaciones categóricas, como:

- categoría principal
- subcategoría
- ruta de categoría

Defina también cualquier palabra clave y atributo asociado, como:

- disponibilidad
- precio venta
- marca
- talla
- color

## Paso 1: Crear una categoría

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Establecer **[!UICONTROL Store View]** para determinar dónde debe estar disponible la nueva categoría.

1. En el árbol de categorías, seleccione la categoría principal de la nueva categoría.

   El nivel principal está un nivel por encima de la nueva categoría.

   Si está empezando desde el principio sin datos, puede que solo haya dos categorías en la lista: _Categoría predeterminada_, que es la raíz, y un _Categoría de ejemplo_

1. Haga clic **[!UICONTROL Add Subcategory]**.

## Paso 2: Completar la información básica

1. Si desea que la categoría esté disponible inmediatamente en la tienda, establezca **[!UICONTROL Enable Category]** hasta `Yes`.

1. Para incluir la categoría en [navegación superior](navigation-top.md), configurado **[!UICONTROL Include in Menu]** hasta `Yes`.

1. Introduzca el **[!UICONTROL Category Name]**.

   ![Información básica de la categoría](./assets/catalog-categories-currently-active.png){width="500" zoomable="yes"}

1. click **[!UICONTROL Save]** y continuar.

## Paso 3: Completar el contenido de la categoría

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Content]** sección.

   ![Contenido de categoría](./assets/category-content.png){width="600" zoomable="yes"}

1. Para mostrar una **[!UICONTROL Category Image]** en la parte superior de la página, puede cargar su propia imagen o utilizar una imagen que exista en el [Almacenamiento de medios](../content-design/media-storage.md).

   - Para cargar su propia imagen, haga clic en **[!UICONTROL Upload]** y elija la imagen que desea que represente la categoría.

   - Para utilizar imágenes de Media Storage, haga clic en **[!UICONTROL Select from Gallery]** y seleccione la imagen que desea que represente la categoría.

   >[!NOTE]
   >
   >Dentro de la Galería multimedia, también puede utilizar la variable [Integración de Adobe Stock](../content-design/adobe-stock.md) para buscar una imagen adecuada, haga clic en **[!UICONTROL Search Adobe Stock]**.

1. Para **[!UICONTROL Description]**, introduzca el texto u otro contenido que desee que aparezca en la página de aterrizaje de categoría.

   Para obtener más información, consulte [Contenido de categoría](categories-content-settings.md).

1. Para incluir un bloque de contenido en la página de aterrizaje de categoría, elija **[!UICONTROL CMS Block]** que desea que aparezca.

1. click **[!UICONTROL Save]** y continuar.

## Paso 4: Completar la configuración de visualización

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Display Setting]** sección.

   ![Configuración de visualización](./assets/category-display-settings.png){width="600" zoomable="yes"}

   Para obtener más información sobre estas opciones, consulte Para obtener más información sobre estas opciones, consulte  [Configuración de visualización](categories-display-settings.md).

1. Establecer **[!UICONTROL Display Mode]** a uno de los siguientes:

   - `Products Only`
   - `Static Block Only`
   - `Static Block and Products`

1. Si desea que la página de categoría incluya la variable _`Filter by Attribute`_sección de navegación por capas, definir **[!UICONTROL Anchor]**hasta `Yes`.

1. Para el **[!UICONTROL Available Product Listing Sort By]** , seleccione uno o varios valores disponibles para que los clientes ordenen la lista.

   De forma predeterminada, se incluyen todos los valores disponibles. Anule la selección de **[!UICONTROL Use All]** para cambiar las selecciones. Por ejemplo, los valores pueden incluir:

   - `Position`
   - `Product Name`
   - `Price`

1. Para establecer el criterio de ordenación predeterminado de la categoría, elija **[!UICONTROL Default Product Listing Sort By]** valor.

1. Para cambiar la navegación por capas predeterminada [escalón de precios](navigation-layered.md#configure-price-navigation) , haga lo siguiente:

   - Anule la selección de **[!UICONTROL Use Config Settings]** casilla de verificación

   - Introduzca el valor que se utilizará como paso de precio incremental para la navegación por capas.

1. Clic **[!UICONTROL Save]** y continuar.

## Paso 5: Completar la configuración de optimización del motor de búsqueda

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Search Engine Optimization Settings]** sección.

   ![Optimización del motor de búsqueda](./assets/categories-search-engine-optimization.png){width="600" zoomable="yes"}

   Para obtener más información sobre estas opciones, consulte [Optimización del motor de búsqueda](categories-search-engine-optimization.md).

1. Complete lo siguiente [metadatos](../merchandising-promotions/meta-data.md) para la categoría:

   - [!UICONTROL Meta Title]
   - [!UICONTROL Meta Keywords]
   - [!UICONTROL Meta Description]

1. Clic **[!UICONTROL Save]** y continuar.

## Paso 6: Elija los productos en la categoría

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Products in Category]** sección.

   ![Productos en la categoría](./assets/category-products-in-category.png){width="600" zoomable="yes"}

   Para obtener más información sobre estas opciones, consulte [Productos en la categoría](categories-product-assignments.md).

1. Si es necesario, utilice el [filtros](../getting-started/admin-grid-controls.md) para encontrar los productos.

   Para mostrar todos los registros que aún no están incluidos en la categoría, establezca el selector de registros de la primera columna en `No` y haga clic en **[!UICONTROL Search]**.

1. En la primera columna, seleccione la casilla de verificación de cada producto que desee incluir en la categoría.

1. Clic **[!UICONTROL Save]** y continuar.

## Paso 7: Establecer los permisos de la categoría

{{ee-feature}}

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Category Permissions]** sección.

1. Para una instalación de varios sitios, elija la **[!UICONTROL Website]** donde se aplican los permisos de categoría.

1. Elija la **[!UICONTROL Customer Group]** donde se aplican los permisos de categoría.

   ![B2B para Adobe Commerce](../assets/b2b.svg) ([B2B para Adobe Commerce](../b2b/introduction.md) (solo) Si es necesario, puede elegir una **[!UICONTROL Shared Catalog]** en su lugar.

1. Establezca los siguientes permisos según sea necesario:

   - [!UICONTROL Browsing Category]
   - [!UICONTROL Display Product Prices]
   - [!UICONTROL Add to Cart]

1. Para agregar otra regla de permisos, haga clic en **[!UICONTROL New Permission]** y repita el proceso.

   ![Permisos de categoría](./assets/category-create-permissions.png){width="600" zoomable="yes"}

## Paso 8: Completar la configuración de diseño

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Design]** sección.

1. Ajuste la configuración de diseño según sea necesario:

   - ([B2B para Adobe Commerce](../b2b/introduction.md) (Solo ) Para aplicar la configuración de diseño de la categoría principal a esta categoría, establezca **[!UICONTROL Use Parent Category Settings]** hasta `Yes`.

   - Para cambiar el diseño de las páginas de categorías, elija la **[!UICONTROL Theme]** que desee aplicar.

   - Para cambiar el diseño de columna de las páginas de categoría, elija la **[!UICONTROL Layout]** que desee aplicar.

   - Para introducir un código personalizado, introduzca un código XML válido en la **[!UICONTROL Layout Update XML]** cuadro.

   - Para utilizar el mismo diseño para las páginas de producto, configure **[!UICONTROL Apply Design to Products]** hasta `Yes`.

   ![Configuración de diseño](./assets/category-design.png){width="600" zoomable="yes"}

1. ![Magento Open Source](../assets/open-source.svg) (Solo Magento Open Source) Para programar la actualización de diseño para un período de tiempo específico, haga lo siguiente:

   - Expanda el _[!UICONTROL Schedule Design Update]_sección.

   - Utilizar el calendario (![Icono de calendario](../assets/icon-calendar.png)) para elegir la Programación de actualización **[!UICONTROL from]** y **[!UICONTROL to]** fechas.

   ![Actualización de diseño programada](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save]**.
