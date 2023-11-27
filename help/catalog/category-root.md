---
title: Categoría y jerarquía raíz
description: Obtenga información acerca de la jerarquía de categorías y la categoría raíz, que actúa como contenedor para el menú principal del árbol de categorías.
exl-id: b419cb45-4fe5-42c4-be20-667c7e1e4354
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# Categoría y jerarquía raíz

Los productos del menú principal están determinados por la categoría raíz asignada al [almacenar](../stores-purchase/stores.md#add-stores). La categoría raíz es básicamente un contenedor para el menú principal del árbol de categorías. Puede crear una categoría raíz con un conjunto de productos completamente nuevo o copiar productos de una categoría raíz existente. La categoría raíz se puede asignar a la tienda actual o a cualquier otra tienda del mismo sitio web.

![Diagrama de jerarquía de catálogo](./assets/catalog-hierarchy-scope.svg){width="550"}

Desde el Administrador, la estructura de categorías es similar a un árbol invertido, con la raíz en la parte superior. La raíz tiene un nombre, pero no una clave de URL, y no aparece en [navegación superior](navigation-top.md) de la tienda. Todas las demás categorías del menú se anidan debajo de la raíz. Como la categoría raíz es el nivel más alto del catálogo, la tienda solo puede tener una categoría raíz activa a la vez. Sin embargo, puede crear categorías raíz adicionales para estructuras de catálogo alternativas y tiendas diferentes.

En el siguiente ejemplo se muestra cómo crear una categoría raíz y asignarla a un almacén diferente.

## Paso 1: Crear una categoría raíz

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. A la izquierda, haga clic en **[!UICONTROL Add Root Category]**.

   ![Nueva categoría raíz](./assets/category-root-ee.png){width="600" zoomable="yes"}

1. Introduzca una **[!UICONTROL Category Name]**.

   El nombre que elija se asignará inicialmente a todas las vistas de tienda.

1. Si desea añadir productos al catálogo desde el catálogo actual, haga lo siguiente:

   - Expandir ![Selector de expansión](../assets/icon-display-expand.png) el _Productos en la categoría_ sección.

   - Utilice el [filtros de búsqueda](../getting-started/admin-grid-controls.md) para buscar los productos que desea y marque la casilla de verificación de cada producto que desea copiar en el nuevo catálogo.

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

## Paso 2: Creación del menú principal

1. A la izquierda, seleccione la nueva categoría raíz que creó en el paso anterior.

1. Para crear el [estructura de categorías](category-create.md) para el menú principal, haga clic en **[!UICONTROL Add Subcategory]** y siga las instrucciones.

## Paso 3: Asignar la categoría raíz al almacén

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. En el _Tiendas_ de la cuadrícula, haga clic en el almacén que desee asignar al nuevo catálogo.

1. Establecer **[!UICONTROL Root Category]** a la nueva categoría raíz que ha creado.

1. Asegúrese de que la tienda tenga un **[!UICONTROL Default Store View]** asignado.

   El almacén debe tener al menos uno [vista de tienda](../stores-purchase/store-views.md).

1. Cuando termine, haga clic en **[!UICONTROL Save Store]**.

1. Para comprobar que la tienda tiene un catálogo nuevo, haga lo siguiente:

   - En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

     Los productos que se hayan copiado al nuevo catálogo aparecerán en la cuadrícula.

   - Para comprobar que el nuevo catálogo y el menú principal funcionan correctamente, visite la tienda.
