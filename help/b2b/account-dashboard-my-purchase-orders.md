---
title: "[!UICONTROL My Purchase Orders]"
description: Obtenga información sobre los pedidos de compra y cómo las empresas pueden utilizarlos para administrar sus compras.
exl-id: b7348bc8-b874-4642-a372-530883d9d94c
feature: B2B, Companies, Purchase Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# [!UICONTROL My Purchase Orders]

Cuando los pedidos de compra están [habilitados para una compañía](purchase-order-flow.md), cualquier pedido de un cliente que haya iniciado sesión en una cuenta de usuario de la compañía se crea automáticamente como un pedido de compra. Los usuarios de la compañía con los permisos necesarios pueden crear, editar y eliminar PC que creen, junto con los PC creados por usuarios subordinados.

![Mis pedidos de compra](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Los pedidos de compra crean una _instantánea_ de los precios de los artículos, los descuentos y los precios de envío en el momento en que se creó el pedido. Si el precio de un artículo cambia después de crear el pedido, se utiliza el precio original.

## Administrar pedidos de compra

Desde la página _Ver pedido de compra_, el cliente puede administrar la OC, según sus [permisos de función](account-company-roles-permissions.md).

- Para ver la OC, haga clic en **[!UICONTROL View]**.
- Para ver los comentarios sobre el PC, haga clic en la ficha **[!UICONTROL Comments]**.
- Para ver un historial de pedidos completo, haga clic en la ficha **[!UICONTROL History Log]**.

>[!IMPORTANT]
>
>Si un artículo de un pedido de compra está agotado, o tiene una cantidad insuficiente disponible, cuando el pedido de compra se convierte en un pedido real, se produce un error. Si los pedidos no satisfechos están activados, el pedido se procesa normalmente.

## Nuevo pedido de compra a partir de pedido de compra existente

Si el cliente tiene un pedido de compra existente y desea añadir nuevos artículos, puede generar un pedido de compra duplicado con nuevos productos añadidos al nuevo pedido de compra. El cliente completa los siguientes pasos:

1. En la página _Mi pedido de compra_, el cliente localiza el pedido de compra y hace clic en el vínculo **[!UICONTROL View]**.

1. El cliente hace clic en **[!UICONTROL Add Items to Shopping Cart]**.

   La página Carro de compras se abre con todos los artículos enumerados.

1. Realiza adiciones o cambios.

1. (Opcional) Utiliza **[!UICONTROL Custom Reference Number]** para agregar un número de factura/pedido interno al pedido.

1. Sigue el flujo de trabajo de cierre de compra normal y hace clic en **[!UICONTROL Place Purchase Order]**.

Si tienen artículos en el carro de compras al hacer clic en _[!UICONTROL Add Items to Shopping Cart]_, el sistema muestra un cuadro de diálogo. Este cuadro de diálogo les permite elegir entre combinar los artículos del carro de compras con los nuevos artículos o reemplazar los artículos del carro de compras con los artículos del pedido de compra.

El pedido de compra original se puede cerrar si ya no es necesario.

## Aprobaciones de pedidos de compra

Para un cliente designado como aprobador según la estructura de la compañía o el rol de compañía asignado, la página de panel _[!UICONTROL My Purchase Orders]_muestra la pestaña **[!UICONTROL Requires My Approval]**. El cliente hace clic en esta pestaña para revisar los pedidos que están esperando su aprobación. El contador muestra cuántas solicitudes están a la espera de aprobación.

Después de hacer clic en **[!UICONTROL View]** para un pedido de compra y revisar los detalles, el aprobador puede hacer clic en **[!UICONTROL Approve]** o **[!UICONTROL Reject]**.

### Aprobación/rechazo masivo

A partir de Adobe Commerce 2.4.1, los aprobadores pueden aprobar o rechazar varios pedidos de compra al mismo tiempo.

1. En la página _[!UICONTROL My Purchase Order]_, hace clic en la ficha **[!UICONTROL Requires My Approval]**.

1. Seleccione la casilla de verificación de cada pedido de compra que se va a aprobar o rechazar.

1. Hace clic en **[!UICONTROL Approve Selected]** o **[!UICONTROL Reject Selected]**.

Un cliente solo puede seleccionar los pedidos de compra con un estado que permita una acción. Los administradores de la empresa pueden realizar aprobaciones o rechazos masivos de cualquier pedido de compra activo en su empresa.
