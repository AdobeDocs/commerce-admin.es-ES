---
title: Asignar orígenes de inventario por producto
description: Asigne uno o más orígenes de [!DNL Inventory Management] a un producto en el Administrador antes de establecer umbrales y cantidades por origen.
exl-id: 7e47be25-633e-4f5d-bb61-0d9e79b6dbad
feature: Inventory, Products
last-update: 2023-10-26
TQID: 'https://experienceleague.adobe.com/Wjx3w6Z-oNALxNRHw65BZDeCzka3BQvtg-m4a9kp-Y8'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: 8dc0e58b-adf0-51bb-8db5-bb36e3e656fb
    internal-label: Inventory
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 15f1e2ee152fb047443da68dec2cc69551e6c7a0
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%
---
# Asignación de fuentes por producto

Antes de modificar cantidades y configuraciones, debe asignar [orígenes](sources-manage.md) a los productos.

{{$include /help/_includes/unassign-source.md}}

## Asignación de fuentes a un producto

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Abra un producto en modo _Editar_.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Sources]**.

   Esta sección le permite modificar el origen, actualizar las cantidades de inventario y mucho más.

   >[!NOTE]
   >
   >Actualmente, solo los productos simples, configurables, virtuales, descargables y agrupados admiten varias fuentes. Los productos agrupados se pueden crear y administrar con solo las etiquetas predeterminadas Source y Stock.

   ![Sección de fuentes de productos](assets/inventory-product-sources-before.png){width="600" zoomable="yes"}

1. Para agregar un origen, haga clic en **[!UICONTROL Assign Sources]**.

1. En la página _[!UICONTROL Assign Sources]_, active la casilla de verificación situada junto a cada origen que desee asignar al producto.

   ![Producto - asignar orígenes](assets/inventory-product-assign-sources.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Done]** para agregar los orígenes.

1. Realice una de las siguientes acciones para guardar:

   - Haga clic en **[!UICONTROL Save]**.
   - En el menú _[!UICONTROL Save]_(![flecha de menú](../assets/icon-menu-down-arrow-red.png)), elija **[!UICONTROL Save & Close]**.

Después de asignar orígenes, actualice la [cantidad de inventario](quantities-assign-per-product.md) para cada origen de producto.

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
