---
title: Tipos de productos
description: Descubra cómo [!DNL Inventory Management] admite la administración de inventario y pedidos para todos los tipos de productos de Adobe Commerce y Magento Open Source.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/3F5vZOseQC7ILpL0j-ksjWP-GW7c0gUN9Zy7hylzzHU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-wordcount: 213
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
