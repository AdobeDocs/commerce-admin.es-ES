---
title: Información general de Visual Merchandiser
description: Obtenga información acerca de las herramientas de Visual Merchandiser que le permiten colocar productos y determinar qué productos aparecen en la lista de categorías.
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Visual Merchandiser

{{ee-feature}}

El _Visual Merchandiser_ es un conjunto de herramientas avanzadas que le permiten colocar productos y aplicar condiciones que determinan qué productos aparecen en la lista de categorías. El resultado puede ser una selección dinámica de productos que se ajusta a los cambios en el catálogo. Puede trabajar en _modo visual_, que muestra cada producto como un mosaico en una cuadrícula o para trabajar desde una lista de productos de la categoría. Las mismas herramientas están disponibles en cada modo y puede utilizar los botones de la esquina superior derecha para alternar entre cada tipo de visualización.

![Productos de categoría en la vista de mosaico](./assets/category-products-visual-with-stock.png){width="600" zoomable="yes"}

## Obtener acceso a Visual Merchandiser

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Desplácese por el árbol de categorías y haga clic en la categoría que desee editar.

1. Desplazarse hacia abajo y expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Products in Category]** sección.

1. Haga clic en _Ver como mosaicos_ ( ![Ver como mosaicos](../assets/icon-view-tiles.png) ) para mostrar los productos en forma de cuadrícula.

1. Cuando termine, haga clic en **[!UICONTROL Save Category]**.

## Cambiar la posición de un producto

1. Utilice el [criterio de ordenación](../catalog/navigation-product-listings.md) para ver el producto que desea mover.

   - **Método 1: arrastrar y soltar**

     Coja el _Arrastrar_ (![Icono de arrastrar](../assets/icon-move.png)) control en la esquina superior derecha del mosaico del producto y suelte el producto en su posición. El número de cada producto se ajusta para reflejar la nueva posición.

   - **Método 2: Establecer valor de posición**

     En el _Posición_ controlador (![Campo de posición](../assets/control-position.png)) en el mosaico del producto, introduzca el número en el que desea que aparezca el producto. Entrar `0` para colocar el producto en la parte superior de la lista.

1. Cuando termine, haga clic en **[!UICONTROL Save Category]**.

>[!NOTE]
>
>En una instalación limpia, Adobe Commerce reserva el ID de categoría `2` para el catálogo raíz del almacén predeterminado. Visual Merchandiser sólo puede utilizar categorías con un número de identificador de `3` o superior.

## Controles de Workspace

| Control | Descripción |
|--- |--- |
| ![Icono Ver lista](../assets/icon-view-list.png) | Ver como lista |
| ![Ver como icono de mosaico](../assets/icon-view-tiles.png) | Ver como mosaicos |
| ![Conmutar coincidencia por regla - no](../assets/toggle-no.png) | Coincidencia por regla: no |
| ![Conmutar Coincidencia por regla: sí](../assets/toggle-yes.png) | Coincidencia por regla: sí |
| ![Icono Mover](../assets/icon-move.png) | Arrastrar |
| ![Controlador de posición](../assets/control-position.png) | Posición |
| ![Icono Eliminar de la categoría](../assets/icon-delete-x.png) | Eliminar de la categoría |
| ![Elementos por control de página](../assets/control-items-per-page.png) | Vista por página |
| ![Cambiar visualización de página](../assets/control-page-display.png) | Ir al siguiente/anterior |

{style="table-layout:auto"}
