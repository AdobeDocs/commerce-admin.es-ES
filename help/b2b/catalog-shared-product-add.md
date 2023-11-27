---
title: Añadir productos a un catálogo compartido
description: Obtenga información sobre cómo añadir productos a un catálogo compartido, ya sea de forma individual o en grupos por categoría.
exl-id: c88b46b4-cea8-4f65-b7e4-6681bab64d41
feature: B2B, Companies, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# Añadir productos a un catálogo compartido

Los productos se pueden añadir a un catálogo compartido de forma individual o en grupos de varios productos por categoría.

Se deben cumplir los siguientes requisitos para que un producto complejo (como paquete, agrupado o configurable) sea visible desde la tienda en un catálogo compartido:

- Todo [productos asociados](../catalog/product-configurations.md) Las opciones y deben asignarse al mismo catálogo compartido y activarse en el catálogo principal.
- Para [configurable](../catalog/product-create-configurable.md) y [agrupado](../catalog/product-create-grouped.md) productos, solo están visibles los productos asociados habilitados.
- Para un [paquete](../catalog/product-create-bundle.md) , todas las opciones deben estar incluidas en el catálogo compartido.

  ![Seleccionar productos para el catálogo](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## Método 1: añadir un solo producto

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Para el producto en la cuadrícula que desea agregar, vaya a _[!UICONTROL Action]_y haga clic en **[!UICONTROL Edit]**.

1. Desplazarse hacia abajo, expandir ![Selector de expansión](../assets/icon-display-expand.png) el _[!UICONTROL Product in Shared Catalogs]_y haga lo siguiente:

   - Seleccione la casilla de verificación de cada catálogo compartido en el que debe aparecer el producto. Para seleccionar todos los catálogos, haga clic en **[!UICONTROL Select all]**.

     ![Producto en catálogos compartidos](./assets/shared-catalog-assign-from-product.png){width="600" zoomable="yes"}

     El nombre de cada catálogo seleccionado aparece en la _[!UICONTROL Shared Catalogs]_field.

     ![Catálogos compartidos asignados](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

   - Clic **[!UICONTROL Done]** para guardar la configuración.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

## Método 2: añadir varios productos

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Para el catálogo compartido en la cuadrícula, vaya a _[!UICONTROL Action]_y seleccione **[!UICONTROL Set Pricing and Structure]**.

1. En el árbol de categorías, realice una de las acciones siguientes:

   - Para incluir todos los productos, haga clic en **[!UICONTROL Select all]** o marque la casilla de verificación de la categoría principal.
   - Para incluir categorías específicas de productos, seleccione la casilla de verificación de cada categoría que desee incluir.
   - Para incluir o excluir un producto individual, seleccione o anule la selección de la casilla de verificación del producto.

   La notación debajo de cada categoría en el árbol muestra el número de productos de la categoría que están actualmente incluidos en el catálogo compartido. La notación debajo de [categoría raíz](../catalog/category-root.md) muestra el número total de productos de todas las categorías seleccionadas actualmente para el catálogo compartido.

1. Para ver los productos de la categoría en la cuadrícula, haga clic en el nombre de la categoría en el árbol.

   Cuando se selecciona una categoría, ocurre lo siguiente:

   - La opción de la primera columna de la cuadrícula se establece en `On` para cada producto seleccionado.
   - Si un producto está asignado a varias categorías y se omite en una de ellas, permanecerá disponible a través de las demás categorías y hasta [búsqueda en el catálogo](../catalog/search.md).
   - El sistema establece automáticamente [Permisos de categoría](../catalog/category-permissions.md) hasta `Allow` para los productos seleccionados.
