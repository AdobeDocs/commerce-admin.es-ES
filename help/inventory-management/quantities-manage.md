---
title: Administrar cantidades de inventario
description: Información general sobre los procedimientos administrativos para asignar orígenes y cantidades por origen para productos nuevos y existentes en [!DNL Inventory Management].
exl-id: b3d4a4c0-725a-4e62-854f-efb6a5709f73
feature: Inventory, Products
TQID: 'https://experienceleague.adobe.com/ykiHTLnzZGtJrRdp2wZvlL7YLbEb7iAiYlcbY8K7IX8'
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
source-wordcount: '325'
ht-degree: 0%
---
# Administrar cantidades de inventario

Siga estas directrices para asignar orígenes y cantidades para productos nuevos o existentes.

Al crear productos, asigne orígenes y cantidades durante la creación del producto. Consulte [Crear un producto](../catalog/product-create.md) para obtener instrucciones completas. Estas páginas incluyen información de un solo origen y de varios orígenes para orígenes y cantidades por origen.

Al obtener acceso por primera vez a un(a) [!DNL Commerce] actualizado(a) con [!DNL Inventory Management], todos los productos y cantidades se asignan a la Source predeterminada. Al importar nuevos productos a través del archivo .csv, también se asignan al Source predeterminado.

Los comerciantes de uno o varios orígenes pueden actualizar los orígenes, las cantidades de inventario y los umbrales por producto o por lote.

- Los comerciantes de un solo origen pueden actualizar las cantidades de productos para la Source predeterminada. Esta cantidad es el número total de productos disponibles para la venta.

- Los comerciantes de varios orígenes pueden asignar varios orígenes y cantidades por producto para cada ubicación (almacenes, tiendas, distribuidores directos entre otros). Se recomienda agregar orígenes antes de establecer importes de inventario de productos.

Al añadir orígenes y cantidades a los productos, puede ver las cantidades a través de la cuadrícula de productos. Si tiene un número elevado de orígenes, pase el ratón sobre _[!UICONTROL Quantity per Source]_para ver la lista completa y desplazable de orígenes con cantidades actuales.

![Cantidades de productos por origen](assets/inventory-product-quantity.png){width="600" zoomable="yes"}

Tiene las siguientes opciones para asignar un inventario a los productos:

- [Asignación de fuentes por producto](sources-assign-per-product.md): asigne fuentes manualmente por producto en su catálogo.

- [Asignación de cantidades por producto](quantities-assign-per-product.md) - Agregue cantidades de inventario disponible a sus productos por origen. Esta información es específica para comerciantes de varias fuentes.

- [Asignación y desasignación masiva de orígenes](bulk-assignment.md) - Asignar orígenes a productos seleccionados como una acción masiva. Utilice la opción [Transferir inventario a Source](inventory-transfer.md) si desea transferir el inventario y eliminar el origen.

- [Transferencia de inventario a Source](inventory-transfer.md) - Transferencia masiva de todo el inventario de un origen a un origen de destino.

- [Importación y exportación de cantidades](inventory-import-export.md) - Utilice las características de importación y exportación para actualizar varias SKU de producto con orígenes y cantidades de inventario.
