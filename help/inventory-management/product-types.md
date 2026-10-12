---
title: Tipos de productos
description: Descubra cómo [!DNL Inventory Management] admite la administración de inventario y pedidos para todos los tipos de productos de Adobe Commerce y Magento Open Source.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
TQID: 'https://experienceleague.adobe.com/3F5vZOseQC7ILpL0j-ksjWP-GW7c0gUN9Zy7hylzzHU'
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
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%
---
# Tipos de productos

[!DNL Inventory Management] admite la administración de inventario y pedidos para todos los tipos de productos en Adobe Commerce y Magento Open Source: simple, configurable, virtual, descargable, agrupado y agrupado. Las opciones y los requisitos pueden variar según el tipo de producto para las fuentes, las existencias y el envío.

- [Comerciantes de un solo origen](merchant-sourcing.md#single-source-merchants) crean y actualizan la configuración y las cantidades del producto sin necesidad de actualizaciones adicionales. Todos los productos creados y recién importados se asignan automáticamente a la Source predeterminada y a la Stock predeterminada, disponibles inmediatamente para los clientes si están activados y en stock.

- [Comerciantes de varios orígenes](merchant-sourcing.md#multi-source-merchants) asignan orígenes, cantidades por origen y configuraciones durante o después de la creación del producto. [!DNL Commerce] asigna todos los productos recién importados a la Source predeterminada, lo que requiere ediciones adicionales para asignar orígenes y cantidades.

| Tipo de producto | Algoritmo de selección de envíos y Source |
|--|--|
| [[!UICONTROL Simple]](../catalog/product-create-simple.md){target="_blank"} | Admite recomendaciones y anulaciones de SSA durante el envío. |
| [[!UICONTROL Configurable]](../catalog/product-create-configurable.md){target="_blank"} | Admite recomendaciones y anulaciones de SSA durante el envío. |
| [[!UICONTROL Virtual]](../catalog/product-create-virtual.md){target="_blank"} | Siempre usa la recomendación de SSA. El sistema ejecuta el algoritmo de forma implícita cuando crea facturas y siempre utiliza los resultados sugeridos.<br/>No puede ajustar estos resultados. |
| [[!UICONTROL Downloadable]](../catalog/product-create-downloadable.md){target="_blank"} | Siempre usa la recomendación de SSA. El sistema ejecuta el algoritmo de forma implícita cuando crea facturas y siempre utiliza los resultados sugeridos. <br/>No puede ajustar estos resultados. |
| [[!UICONTROL Bundle]](../catalog/product-create-bundle.md){target="_blank"} | Admite recomendaciones y anulaciones de SSA durante el envío. |
| [[!UICONTROL Grouped]](../catalog/product-create-grouped.md){target="_blank"} | Admite recomendaciones y anulaciones de SSA durante el envío. |
