---
title: Configuración del producto - [!UICONTROL Product Reviews]
description: Para un producto, la configuración de [!UICONTROL Product Reviews] proporciona acceso a las revisiones enviadas para el producto y edita el estado de las revisiones pendientes.
exl-id: 9328c9f5-dcd4-4837-8902-39dc48cb8151
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Configuración del producto - [!UICONTROL Product Reviews]

La sección _[!UICONTROL Product Reviews]_enumera todas las revisiones que los clientes han enviado sobre el producto. Esta sección aparece con la otra información del producto solo después de guardar un nuevo producto por primera vez. Para obtener más información, consulte [Críticas de productos](../merchandising-promotions/product-reviews.md).

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
