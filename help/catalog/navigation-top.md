---
title: Navegación superior
description: Aprenda a definir el menú principal de una tienda, que funciona como un directorio para los diferentes departamentos.
exl-id: 8b71fe73-2716-4820-9e57-4cb1e6888132
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# Navegación superior

El menú principal de su tienda es como un directorio para los diferentes departamentos de su tienda. Cada opción representa una categoría diferente de productos. La posición y presentación de la navegación superior pueden variar según la temática, pero su funcionamiento es básicamente el mismo.

![Navegación superior](./assets/storefront-top-navigation.png){width="700" zoomable="yes"}

La estructura de categorías del catálogo puede influir en el grado de indexación del sitio por parte de los motores de búsqueda. Cuanto más profundamente anidada esté una categoría, menos probable es que se indexe completamente. Por lo general, el uso de entre uno y tres niveles visibles es el más eficaz. El [categoría raíz](category-root.md) cuenta como el primer nivel, aunque no aparece en el menú. La configuración determina el número máximo de niveles disponibles en la navegación superior. Además, podría haber un límite en la cantidad de niveles de menú que admite el tema de la tienda. Por ejemplo, la temática de ejemplo de Luma admite hasta cinco niveles, incluida la raíz.

## Recuento de niveles de menú

| Elemento | Descripción |
|--- |--- |
| Nivel 1 | El primer nivel es la categoría raíz, que en los datos de ejemplo se denomina &quot;Categoría predeterminada&quot;. La raíz es un contenedor para el menú y su nombre no aparece como una opción en el menú. |
| Nivel 2 | En una pantalla de escritorio, la navegación superior es el menú principal que aparece en la parte superior de la página. En un dispositivo móvil, el menú principal suele aparecer como un menú emergente de opciones. Las opciones de segundo nivel de la tienda de Luma son las siguientes _Novedades de la versión_, _Mujer_, _Hombres_, _Engranaje_, _Formación_, y _Venta_. |
| Nivel 3 | El tercer nivel aparece debajo de cada opción del menú principal. Por ejemplo, en _Mujer_, las opciones de tercer nivel son _Tops_ y _Parte inferior_. |
| Nivel 4 | Las opciones de cuarto nivel son subcategorías que salen de una opción de tercer nivel. Por ejemplo, en _Tops_, las opciones de menú del cuarto nivel son _Chaquetas_, _Sudaderas y sudaderas_, _Tees_, y _Sujetadores y tanques_. |

{style="table-layout:auto"}

## Configuración de la navegación superior

Para que una categoría aparezca en la barra de navegación superior de una tienda, completa los siguientes pasos:

### Paso 1: Crear una categoría

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Establezca un **[!UICONTROL Store View]** para determinar dónde debe estar disponible la nueva categoría.

1. En el árbol de categorías, seleccione la categoría principal de la nueva categoría.

   Si está empezando desde el principio sin datos, puede que solo haya dos categorías en la lista: _Categoría predeterminada_, que es la raíz, y un _Categoría de ejemplo_.

1. Haga clic **[!UICONTROL Add Subcategory]**.

1. Complete la información básica con la siguiente configuración:

   - **[!UICONTROL Enable Category]** establezca en `Yes`
   - **[!UICONTROL Include in Menu]** establezca en `Yes`

1. En conjunto de configuración de visualización **[!UICONTROL Anchor]** hasta `Yes`.

1. Complete cualquier otro elemento necesario [configuración de categoría](category-create.md).

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

Para una instalación multitienda, se puede asignar un menú principal diferente como [categoría raíz](category-root.md) para cada [almacenar](../stores-purchase/stores.md#add-stores).

### Paso 2: Establecer la profundidad de la navegación superior

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Expanda el **[!UICONTROL Category Top Navigation]** sección.

   ![Navegación superior por categorías](../configuration-reference/catalog/assets/catalog-category-top-navigation.png){width="600" zoomable="yes"}

   Debido a que la profundidad de la navegación superior tiene un [ámbito de configuración](../getting-started/websites-stores-views.md#scope-settings), la configuración se aplica a todos los sitios web, tiendas y vistas de tiendas de la instalación de Commerce. El _[!UICONTROL Category Top Navigation]_La sección de configuración de solo está disponible cuando_[!UICONTROL Store View]_ en la esquina superior izquierda, se establece en `Default Config`.

   Para ver una lista detallada de estas opciones, consulte [Navegación superior por categorías](../configuration-reference/catalog/catalog.md#layered-navigation) en el _Referencia de configuración_.

1. Para limitar el número de subcategorías que aparecen en la barra de navegación superior, introduzca el número de **[!UICONTROL Maximal Depth]**.

   El valor predeterminado es `0`, que no impone un límite al número de niveles de subcategoría.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.
