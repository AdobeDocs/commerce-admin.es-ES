---
title: Configuración del producto - [!UICONTROL Design]
description: Para un producto, la configuración de [!UICONTROL Design] le permite aplicar un tema diferente a una página de producto y cambiar el diseño.
exl-id: 8606ddc7-ca81-4503-94e5-a8276506c0a1
feature: Catalog Management, Products, Page Content
TQID: https://experienceleague.adobe.com/u6VzZ9TiovuSopBcBjmpQTKl3pzh3DoXXzpr8akWp-8
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fcid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 284
ht-degree: 0%

---

# Configuración del producto - [!UICONTROL Design]

La configuración de _[!UICONTROL Design]_permite aplicar un tema diferente a la página del producto, cambiar el diseño de la columna, determinar dónde aparecen las opciones del producto e introducir código XML personalizado.

![Diseño](./assets/product-design-ee.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Cuando se asigna el mismo producto a varias categorías con diferentes configuraciones de diseño para cada categoría, se recomienda establecer **[!UICONTROL Use Categories Path for Product URLs]** = `Yes` en las [opciones de configuración de optimización del motor de búsqueda](../configuration-reference/catalog/catalog.md#search-engine-optimization). Para obtener acceso a esta configuración, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**, expanda **[!UICONTROL Catalog]**y elija **[!UICONTROL Catalog]**debajo en el panel izquierdo y, a continuación, expanda la sección **[!UICONTROL Search Engine Optimization]**en la página.

| Campo | [Ámbito](../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|---|---|----|
| [!UICONTROL Theme] | Vista de tienda | ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Permite aplicar un tema diferente al producto. Opciones: (todas las temáticas disponibles) |
| [!UICONTROL Layout] | Vista de tienda | Permite aplicar un [diseño](../content-design/page-layout.md) diferente a la página del producto. Opciones: <br/>**[!UICONTROL No layout updates]**: de forma predeterminada, las actualizaciones de diseño no están disponibles para la página del producto.<br/>**[!UICONTROL Empty]**: permite definir su propio diseño, como una página de 4 columnas. (Requiere conocimientos de XML.) <br/>**[!UICONTROL 1 column]**: aplica un diseño de una columna a la página del producto.<br/>**[!UICONTROL 2 columns with left bar]**: aplica un diseño de dos columnas con una barra lateral izquierda a la página del producto. <br/>**[!UICONTROL 2 columns with right bar]**: aplica un diseño de dos columnas con una barra lateral derecha a la página del producto.<br/>**[!UICONTROL 3 columns]**: aplica un diseño de tres columnas a la página del producto. <br/>**[!UICONTROL Page -- Full Width]**- (Requiere [[!DNL Page Builder]](../page-builder/introduction.md)) Aplica el diseño de ancho completo para las páginas de CMS a la página de producto.<br/>**[!UICONTROL Category -- Full Width]** - (Requiere [!DNL Page Builder]) Aplica el diseño de ancho completo para las páginas de categoría a la página de producto. <br/>**[!UICONTROL Product -- Full Width]**- (Requiere [!UICONTROL Page Builder]) Aplica el diseño de ancho completo para páginas de producto a la página de producto. |
| [!UICONTROL Display Product Options In] | Vista de tienda | Determina dónde aparecen las opciones del producto en la página del producto. Opciones: `Product Info Column` / `Block after Info Column` |
| [!UICONTROL Custom Layout Update] | Vista de tienda | Se utiliza para acceder a las opciones para actualizar un diseño personalizado en la página del producto. |

{style="table-layout:auto"}
