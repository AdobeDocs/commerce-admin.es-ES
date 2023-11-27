---
title: Configuración del producto - [!UICONTROL Design]
description: Para un producto, la variable [!UICONTROL Design] La configuración de le permite aplicar una temática diferente a una página de producto y cambiar el diseño.
exl-id: 8606ddc7-ca81-4503-94e5-a8276506c0a1
feature: Catalog Management, Products, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Configuración del producto - [!UICONTROL Design]

El _[!UICONTROL Design]_La configuración de permite aplicar una temática diferente a la página del producto, cambiar el diseño de la columna, determinar dónde aparecen las opciones del producto e introducir código XML personalizado.

![Diseño](./assets/product-design-ee.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Cuando se asigna el mismo producto a varias categorías con diferentes configuraciones de diseño para cada categoría, se recomienda configurar **[!UICONTROL Use Categories Path for Product URLs]** = `Yes` en el [Opciones de configuración de optimización del motor de búsqueda](../configuration-reference/catalog/catalog.md#search-engine-optimization). Para acceder a esta configuración, vaya a  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**, expanda **[!UICONTROL Catalog]**y elija **[!UICONTROL Catalog]**debajo de en el panel izquierdo y, a continuación, expanda la **[!UICONTROL Search Engine Optimization]**de la página.

| Campo | [Ámbito](../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|---|---|----|
| [!UICONTROL Theme] | Vista de tienda | ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Permite aplicar una temática diferente al producto. Opciones: (todas las temáticas disponibles) |
| [!UICONTROL Layout] | Vista de tienda | Le permite aplicar un método diferente [layout](../content-design/page-layout.md) a la página de producto. Opciones: <br/>**[!UICONTROL No layout updates]**: De forma predeterminada, las actualizaciones de diseño no están disponibles para la página del producto.<br/>**[!UICONTROL Empty]** : le permite definir su propio diseño, como una página de 4 columnas. (Requiere conocimientos de XML). <br/>**[!UICONTROL 1 column]**: aplica un diseño de una columna a la página del producto.<br/>**[!UICONTROL 2 columns with left bar]** : aplica un diseño de dos columnas con una barra lateral izquierda a la página del producto. <br/>**[!UICONTROL 2 columns with right bar]**: aplica un diseño de dos columnas con una barra lateral derecha a la página del producto.<br/>**[!UICONTROL 3 columns]** : aplica un diseño de tres columnas a la página del producto. <br/>**[!UICONTROL Page -- Full Width]**- (Requiere [[!DNL Page Builder]](../page-builder/introduction.md)) Aplica el diseño de ancho completo para páginas de CMS a la página de producto.<br/>**[!UICONTROL Category -- Full Width]** - (Requiere [!DNL Page Builder]) Aplica el diseño de ancho completo para las páginas de categoría a la página de producto. <br/>**[!UICONTROL Product -- Full Width]**- (Requiere [!UICONTROL Page Builder]) Aplica el diseño de ancho completo para las páginas de producto a la página de producto. |
| [!UICONTROL Display Product Options In] | Vista de tienda | Determina dónde aparecen las opciones del producto en la página del producto. Opciones: `Product Info Column` / `Block after Info Column` |
| [!UICONTROL Custom Layout Update] | Vista de tienda | Se utiliza para acceder a las opciones para actualizar un diseño personalizado en la página del producto. |

{style="table-layout:auto"}
