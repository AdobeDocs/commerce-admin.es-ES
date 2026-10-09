---
title: Asignación y cancelación de asignación de origen de inventario masivo
description: Utilice la acción por lotes Asignar fuentes en el Administrador para asignar o cancelar la asignación de [!DNL Inventory Management] fuentes para muchos productos a la vez.
exl-id: 1f1e81a5-fb06-46b7-84ca-7feea4942093
feature: Inventory, Products
last-update: 2023-06-28
TQID: 'https://experienceleague.adobe.com/H8UQh7quyOeDq6-hSmf83fzUuJkuSLv0i2dezX-GKRA'
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
source-wordcount: '333'
ht-degree: 0%
---
# Asignación y cancelación de asignación de origen masivo

Use la herramienta _Asignar fuentes_ para agregar una o más fuentes a sus productos. La herramienta ayuda a crear y asignar fuentes personalizadas a sus existencias predeterminadas o existencias personalizadas y a preparar nuevas ubicaciones e inventarios.

Después de agregar nuevas fuentes personalizadas, puede agregar [cantidades de inventario por producto](quantities-assign-per-product.md) o para varios productos a través del administrador o mediante la [característica de importación](inventory-import-export.md).

![Agregar orígenes de inventario para los productos seleccionados](assets/inventory-bulk-assign-sources.gif)

## Asignación de orígenes y cantidades

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Seleccione los productos para los que desea modificar las fuentes.

   Busque los productos y marque las casillas de verificación correspondientes.

1. Haga clic en el menú **[!UICONTROL Actions]** en la parte superior y elija **[!UICONTROL Assign Inventory Source]**.

1. Haga clic en **[!UICONTROL OK]** en el cuadro de diálogo de confirmación.

1. Para todos los orígenes que desee agregar a los productos, active las casillas de verificación.

1. Haga clic en **[!UICONTROL Assign Sources]**.

   ![Seleccionar productos para agregar orígenes](assets/inventory-bulk-assign-sources-summary.png){width="600" zoomable="yes"}

Las fuentes se añaden a los productos con una cantidad de inventario de 0. Puede agregar [cantidades de inventario](quantities-assign-per-product.md) por origen.

## Desasignar orígenes y cantidades

Al anular la asignación de un origen a partir de un producto, se indica que el producto ya no está almacenado en esa ubicación. Este proceso borra por completo todos los datos de inventario del origen asignado actualmente al producto. Si desea mover el inventario existente a una nueva ubicación, considere la posibilidad de usar la opción _Transferir inventario_.

{{$include /help/_includes/unassign-source.md}}

Se recomienda completar todos los pedidos y envíos de esos productos antes de eliminar el origen.

![Anular la asignación de orígenes a los productos seleccionados](assets/inventory-bulk-unassign-sources.gif)

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Seleccione los productos para los que desea modificar las fuentes.

   Busque los productos y marque las casillas de verificación correspondientes.

1. Haga clic en el menú **[!UICONTROL Actions]** en la parte superior y elija **[!UICONTROL Unassign Inventory Source]**.

1. Haga clic en **[!UICONTROL OK]** en el cuadro de diálogo de confirmación.

1. Seleccione el origen que desea eliminar de los productos.

   La página muestra una alerta que indica que al anular la asignación se eliminan todos los datos de origen y cantidad específicos del producto.

1. Haga clic en **[!UICONTROL Unassign Sources]**.

   ![Quitar orígenes de productos seleccionados](assets/inventory-bulk-unassign-sources-summary.png){width="600" zoomable="yes"}

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
