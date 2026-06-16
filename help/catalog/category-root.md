---
title: Categoría y jerarquía raíz
description: Obtenga información acerca de la jerarquía de categorías y la categoría raíz, que actúa como contenedor para el menú principal del árbol de categorías.
exl-id: b419cb45-4fe5-42c4-be20-667c7e1e4354
feature: Catalog Management, Categories, Site Navigation
TQID: https://experienceleague.adobe.com/nkUEOu8IqMM21waPwmkp76YckH6cToL6MiaSK--klho
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 437
ht-degree: 0%

---

# Categoría y jerarquía raíz

Los productos del menú principal están determinados por la categoría raíz asignada al [almacén](../stores-purchase/stores.md#add-stores). La categoría raíz es básicamente un contenedor para el menú principal del árbol de categorías. Puede crear una categoría raíz con un conjunto de productos completamente nuevo o copiar productos de una categoría raíz existente. La categoría raíz se puede asignar a la tienda actual o a cualquier otra tienda del mismo sitio web.

![Diagrama de jerarquía de catálogo](./assets/catalog-hierarchy-scope.svg){width="550"}

Desde el Administrador, la estructura de categorías es similar a un árbol invertido, con la raíz en la parte superior. La raíz tiene un nombre, pero no una clave de URL, y no aparece en la [navegación superior](navigation-top.md) del almacén. Todas las demás categorías del menú se anidan debajo de la raíz. Como la categoría raíz es el nivel más alto del catálogo, la tienda solo puede tener una categoría raíz activa a la vez. Sin embargo, puede crear categorías raíz adicionales para estructuras de catálogo alternativas y tiendas diferentes.

En el siguiente ejemplo se muestra cómo crear una categoría raíz y asignarla a un almacén diferente.

## Paso 1: Crear una categoría raíz

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. A la izquierda, haga clic en **[!UICONTROL Add Root Category]**.

   ![Nueva categoría raíz](./assets/category-root-ee.png){width="600" zoomable="yes"}

1. Escriba un **[!UICONTROL Category Name]**.

   El nombre que elija se asignará inicialmente a todas las vistas de tienda.

1. Si desea añadir productos al catálogo desde el catálogo actual, haga lo siguiente:

   - Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección _Productos de la categoría_.

   - Use los [filtros de búsqueda](../getting-started/admin-grid-controls.md) para encontrar los productos que desea y marque la casilla de verificación de cada producto que desee copiar en el nuevo catálogo.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

## Paso 2: Creación del menú principal

1. A la izquierda, seleccione la nueva categoría raíz que creó en el paso anterior.

1. Para crear la [estructura de categorías](category-create.md) para el menú principal, haga clic en **[!UICONTROL Add Subcategory]** y siga las instrucciones.

## Paso 3: Asignar la categoría raíz al almacén

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. En la columna _Tiendas_ de la cuadrícula, haga clic en el almacén al que desee asignar el nuevo catálogo.

1. Establezca **[!UICONTROL Root Category]** en la nueva categoría raíz que creó.

1. Asegúrese de que la tienda tenga un **[!UICONTROL Default Store View]** asignado.

   El almacén debe tener al menos una [vista del almacén](../stores-purchase/store-views.md).

1. Una vez finalizado, haga clic en **[!UICONTROL Save Store]**.

1. Para comprobar que la tienda tiene un catálogo nuevo, haga lo siguiente:

   - En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

     Los productos que se hayan copiado al nuevo catálogo aparecerán en la cuadrícula.

   - Para comprobar que el nuevo catálogo y el menú principal funcionan correctamente, visite la tienda.
