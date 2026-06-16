---
title: Añadir productos a un catálogo compartido
description: Obtenga información sobre cómo añadir productos a un catálogo compartido, ya sea de forma individual o en grupos por categoría.
exl-id: c88b46b4-cea8-4f65-b7e4-6681bab64d41
feature: B2B, Companies, Catalog Management
TQID: https://experienceleague.adobe.com/f-5xQDov-Q3tfYw8MBDQPinimUIUkGe-q2Nfzm8L9ps
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
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
source-wordcount: 402
ht-degree: 0%

---

# Añadir productos a un catálogo compartido

Los productos se pueden añadir a un catálogo compartido de forma individual o en grupos de varios productos por categoría.

Se deben cumplir los siguientes requisitos para que un producto complejo (como paquete, agrupado o configurable) sea visible desde la tienda en un catálogo compartido:

- Todos los [productos asociados](../catalog/product-configurations.md) y las opciones deben asignarse al mismo catálogo compartido y habilitarse en el catálogo principal.
- Para los productos [configurables](../catalog/product-create-configurable.md) y [agrupados](../catalog/product-create-grouped.md), solo están visibles los productos asociados habilitados.
- Para un producto [bundle](../catalog/product-create-bundle.md), todas las opciones deben estar incluidas en el catálogo compartido.

  ![Seleccionar productos para el catálogo](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## Método 1: añadir un solo producto

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Para el producto en la cuadrícula que desea agregar, vaya a la columna _[!UICONTROL Action]_&#x200B;y haga clic en **[!UICONTROL Edit]**.

1. Desplácese hacia abajo, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección _[!UICONTROL Product in Shared Catalogs]_&#x200B;y haga lo siguiente:

   - Seleccione la casilla de verificación de cada catálogo compartido en el que debe aparecer el producto. Para elegir todos los catálogos, haga clic en **[!UICONTROL Select all]**.

     ![Producto en catálogos compartidos](./assets/shared-catalog-assign-from-product.png){width="600" zoomable="yes"}

     El nombre de cada catálogo seleccionado aparece en el campo _[!UICONTROL Shared Catalogs]_.

     ![Catálogos compartidos asignados](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

   - Haga clic en **[!UICONTROL Done]** para guardar la configuración.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

## Método 2: añadir varios productos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Para el catálogo compartido en la cuadrícula, vaya a la columna _[!UICONTROL Action]_&#x200B;y seleccione **[!UICONTROL Set Pricing and Structure]**.

1. En el árbol de categorías, realice una de las acciones siguientes:

   - Para incluir todos los productos, haga clic en **[!UICONTROL Select all]** o seleccione la casilla de verificación de la categoría principal.
   - Para incluir categorías específicas de productos, seleccione la casilla de verificación de cada categoría que desee incluir.
   - Para incluir o excluir un producto individual, seleccione o anule la selección de la casilla de verificación del producto.

   La notación debajo de cada categoría en el árbol muestra el número de productos de la categoría que están actualmente incluidos en el catálogo compartido. La anotación debajo de [categoría raíz](../catalog/category-root.md) muestra el número total de productos de todas las categorías que están seleccionadas actualmente para el catálogo compartido.

1. Para ver los productos de la categoría en la cuadrícula, haga clic en el nombre de la categoría en el árbol.

   Cuando se selecciona una categoría, ocurre lo siguiente:

   - La opción de la primera columna de la cuadrícula se establece en `On` para cada producto seleccionado.
   - Si un producto está asignado a varias categorías y se omite en una de ellas, permanecerá disponible a través de las demás categorías y mediante [búsqueda en el catálogo](../catalog/search.md).
   - El sistema establece automáticamente [Permisos de categoría](../catalog/category-permissions.md) en `Allow` para los productos seleccionados.
