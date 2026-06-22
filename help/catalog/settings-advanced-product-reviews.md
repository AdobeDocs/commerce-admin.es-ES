---
title: Configuración del producto - [!UICONTROL Product Reviews]
description: Para un producto, la configuración de [!UICONTROL Product Reviews] proporciona acceso a las revisiones enviadas para el producto y edita el estado de las revisiones pendientes.
exl-id: 9328c9f5-dcd4-4837-8902-39dc48cb8151
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/GdeAB8bT8WjR9vSGjuD-h5I3O6vYNxyaaUQYAjjy8ME
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
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
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 212
ht-degree: 0%

---

# Configuración del producto - [!UICONTROL Product Reviews]

La sección _[!UICONTROL Product Reviews]_&#x200B;enumera todas las revisiones que los clientes han enviado sobre el producto. Esta sección aparece con la otra información del producto solo después de guardar un nuevo producto por primera vez. Para obtener más información, consulte [Críticas de productos](../merchandising-promotions/product-reviews.md).

![Críticas de productos](./assets/product-review.png){width="600" zoomable="yes"}

## Referencia de campo

| Campo | Descripción |
|--- |--- |
| [!UICONTROL ID] | ID numérico único generado para la entrada de revisión del producto |
| [!UICONTROL Created] | Fecha de publicación de la revisión |
| [!UICONTROL Status] | Estado de revisión (`Pending`, `Approved` o `Not Approved`) |
| [!UICONTROL Title] | Revisar título |
| [!UICONTROL Nickname] | El apodo del usuario que dejó la revisión |
| [!UICONTROL Review] | Opinión del cliente sobre el producto actual |
| [!UICONTROL Visibility] | Visibilidad en reseñas de tiendas |
| [!UICONTROL Type] | Tipo de usuario que dejó la revisión (`Guest` o `Customer`) |
| [!UICONTROL Product] | Nombre del producto revisado |
| [!UICONTROL SKU] | La única unidad de stock asignada al producto |
| [!UICONTROL Action] | Abre el producto en modo de edición |

{style="table-layout:auto"}

## Moderar revisiones para un producto específico

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Busque el producto y ábralo en modo de edición.

1. Desplácese hasta la sección _[!UICONTROL Product Reviews]_.

1. Haga clic en **[!UICONTROL Edit]** para obtener una revisión de producto con el estado `Pending` a fin de ver y editar los detalles.

1. Definir estado para revisión:

   - Para aprobar una revisión pendiente, seleccione `Approved`.
   - Para rechazar una revisión, seleccione `Not Approved`.
   - Puede volver a cambiar el estado de la revisión a `Pending` en cualquier momento.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Review]**.

Las críticas con los estados `Pending` y `Not Approved` no se muestran en la tienda.

