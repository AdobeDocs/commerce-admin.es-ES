---
title: Información general de Visual Merchandiser
description: Obtenga información acerca de las herramientas de Visual Merchandiser que le permiten colocar productos y determinar qué productos aparecen en la lista de categorías.
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Visual Merchandiser

{{ee-feature}}

_Visual Merchandiser_ es un conjunto de herramientas avanzadas que le permite colocar productos y aplicar condiciones que determinan qué productos aparecen en la lista de categorías. El resultado puede ser una selección dinámica de productos que se ajusta a los cambios en el catálogo. Puede trabajar en _modo visual_, que muestra cada producto como un mosaico en una cuadrícula, o para trabajar desde una lista de productos de la categoría. Las mismas herramientas están disponibles en cada modo y puede utilizar los botones de la esquina superior derecha para alternar entre cada tipo de visualización.

![Productos de categoría en la vista de mosaico](./assets/category-products-visual-with-stock.png){width="600" zoomable="yes"}

## Obtener acceso a Visual Merchandiser

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Desplácese por el árbol de categorías y haga clic en la categoría que desee editar.

1. Desplácese hacia abajo y expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Products in Category]**.

1. Haga clic en el botón _Ver como mosaicos_ ( ![Ver como mosaicos](../assets/icon-view-tiles.png) ) para mostrar los productos como una cuadrícula.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Category]**.

## Cambiar la posición de un producto

1. Use el [criterio de ordenación](../catalog/navigation-product-listings.md) para ver el producto que desea mover.

   - **Método 1: Arrastrar y soltar**

     Coge el control _Arrastrar_ (![Arrastrar icono](../assets/icon-move.png)) en la esquina superior derecha del mosaico del producto y suelta el producto en su posición. El número de cada producto se ajusta para reflejar la nueva posición.

   - **Método 2: establecer valor de posición**

     En el controlador _Position_ (![Position field](../assets/control-position.png)) del mosaico del producto, escriba el número en el que desea que aparezca el producto. Escriba `0` para colocar el producto al principio de la lista.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Category]**.

>[!NOTE]
>
>En una instalación limpia, Adobe Commerce reserva el id. de categoría `2` para el catálogo raíz del almacén predeterminado. Visual Merchandiser sólo puede utilizar categorías con un número de identificador de `3` o superior.

## Controles de Workspace

| Control | Descripción |
|--- |--- |
| ![Icono de lista de vista](../assets/icon-view-list.png) | Ver como lista |
| ![Ver como icono de mosaico](../assets/icon-view-tiles.png) | Ver como mosaicos |
| ![Conmutar coincidencia por regla - no](../assets/toggle-no.png) | Coincidencia por regla: no |
| ![Conmutar coincidencia por regla - sí](../assets/toggle-yes.png) | Coincidencia por regla: sí |
| ![Icono de mover](../assets/icon-move.png) | Arrastrar |
| ![Controlador de posición](../assets/control-position.png) | Posición |
| ![Quitar del icono de categoría](../assets/icon-delete-x.png) | Eliminar de la categoría |
| ![Elementos por control de página](../assets/control-items-per-page.png) | Vista por página |
| ![Cambiar visualización de página](../assets/control-page-display.png) | Ir al siguiente/anterior |

{style="table-layout:auto"}
