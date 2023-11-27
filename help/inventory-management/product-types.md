---
title: Tipos de productos
description: Descubra cómo [!DNL Inventory Management] admite la administración de inventario y pedidos para todos los tipos de productos de Adobe Commerce y Magento Open Source.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# Tipos de productos

[!DNL Inventory Management] admite la administración de inventario y pedidos para todos los tipos de productos en Adobe Commerce y Magento Open Source: simple, configurable, virtual, descargable, paquete y agrupado. Las opciones y los requisitos pueden variar según el tipo de producto para las fuentes, las existencias y el envío.

- [Comerciantes de un solo origen](merchant-sourcing.md#single-source-merchants) crear y actualizar la configuración y las cantidades del producto sin necesidad de actualizaciones adicionales. Todos los productos creados y recién importados se asignan automáticamente al origen y al stock predeterminados, disponibles inmediatamente para los clientes si están activados y en stock.

- [Comerciantes de varias fuentes](merchant-sourcing.md#multi-source-merchants) asignar orígenes, cantidades por origen y configuración durante o después de la creación del producto. [!DNL Commerce] asigna todos los productos recién importados al origen predeterminado, lo que requiere ediciones adicionales para asignar orígenes y cantidades.

| Tipo de producto | Algoritmo de selección de origen y envío |
|--|--|
| [[!UICONTROL Simple]](../catalog/product-create-simple.md){target="_blank"} | Admite recomendaciones y anulaciones de SSA durante el envío. |
| [[!UICONTROL Configurable]](../catalog/product-create-configurable.md){target="_blank"} | Admite recomendaciones y anulaciones de SSA durante el envío. |
| [[!UICONTROL Virtual]](../catalog/product-create-virtual.md){target="_blank"} | Siempre usa la recomendación de SSA. El sistema ejecuta el algoritmo de forma implícita cuando crea facturas y siempre utiliza los resultados sugeridos.<br/>No puede ajustar estos resultados. |
| [[!UICONTROL Downloadable]](../catalog/product-create-downloadable.md){target="_blank"} | Siempre usa la recomendación de SSA. El sistema ejecuta el algoritmo de forma implícita cuando crea facturas y siempre utiliza los resultados sugeridos. <br/>No puede ajustar estos resultados. |
| [[!UICONTROL Bundle]](../catalog/product-create-bundle.md){target="_blank"} | Admite recomendaciones y anulaciones de SSA durante el envío. |
| [[!UICONTROL Grouped]](../catalog/product-create-grouped.md){target="_blank"} | Admite recomendaciones y anulaciones de SSA durante el envío. |
