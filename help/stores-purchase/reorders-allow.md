---
title: Permitir reordenamientos
description: Aprenda a proporcionar funciones de reorganización a sus clientes.
exl-id: 9fe4c4fb-8596-4fd0-a93b-927ebdfc0c94
feature: Orders, Storefront
TQID: https://experienceleague.adobe.com/comSKludWZnDkDjdZyhi4-9WNAE9scH3dgSce08IyJo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 432
ht-degree: 0%

---

# Permitir reordenamientos

Cuando está habilitada, los repedidos se pueden realizar directamente desde la cuenta del cliente o desde el pedido original en _Admin_. Los repedidos están habilitados de forma predeterminada.

![Vínculo de reorden de cliente en el administrador](./assets/customer-reorder.png){width="700" zoomable="yes"}

## Criterios para activar el repedido en un pedido

- La opción de configuración _Permitir reordenar_ debe estar habilitada.

- Si el pedido está en estado `Hold` o `Payment Review`, la opción de reordenar está deshabilitada.

- Si alguno de los artículos del pedido no está disponible, está agotado o deshabilitado, la opción de reordenar está deshabilitada en la tienda.

- Un _administrador_ puede reordenar incluso si alguno de los elementos está agotado o deshabilitado.

## Configurar para permitir nuevos pedidos de clientes

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Sales]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Reorder]**.

   ![Reordenar opciones](../configuration-reference/sales/assets/sales-reorder.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Allow Reorder]** en `Yes`.

   Esta configuración habilita la funcionalidad de reordenar desde la cuenta de cliente en la tienda o la lista de pedidos en el Administrador.

1. Haga clic en **[!UICONTROL Save Config]**.

## Reordenar desde la tienda

Un cliente puede iniciar la funcionalidad de reordenar para un pedido específico desde dos páginas:

- _Mis pedidos_ página

- _Vista de pedidos_ página

### Mis pedidos

El botón _Reordenar_ siempre se muestra en la lista con Pedidos (incluso si no todos los productos del pedido están disponibles para reordenar).

![Ejemplo de tienda - Página Mis pedidos](./assets/my-order-page-view.png){width="700" zoomable="yes"}

**Caso 1.** Todos los productos del pedido están **disponibles** para reordenar

Se redirige al usuario al carro de compras y se agregan todos los productos a este

![Carro de compras](./assets/shopping-cart-page.png){width="700" zoomable="yes"}

**Caso 2.** Algunos/todos los productos del pedido están **no disponibles** para reordenar

>[!NOTE]
>
>Es posible reordenar `Not Visible Individually` productos.

El botón _Reordenar_ no aparece en las páginas _Mis pedidos_ y _Ver pedido_.

![Mis pedidos página 1](./assets/my-orders-view-page1.png){width="700" zoomable="yes"}

### Página de vista de pedidos

**Caso 1.** Todos los productos del pedido están disponibles para reordenar

Se redirige al usuario al carro de compras y se agregan todos los productos a este

**Caso 2.** Algunos/todos los productos del pedido están **no disponibles** para reordenar

>[!NOTE]
>
>Es posible reordenar `Not Visible Individually` productos.

El botón _Reordenar_ no aparece en las páginas _Mis pedidos_ y _Ver pedido_.

![Página de detalles del pedido](./assets/order-view-page.png){width="700" zoomable="yes"}

### El carro no está vacío

Si el carro de compras no está vacío y el usuario hace clic en **[!UICONTROL Reorder]** (desde la página _Mis pedidos_ o _Vista de pedidos_), los productos existentes permanecerán en el carro de compras con los productos de repedido agregados.

![Reordenar elementos](./assets/shopping-cart-view1.png){width="700" zoomable="yes"}

## Reordenar desde el administrador

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Busque el pedido y abra en el modo **[!UICONTROL View]**.

1. Haga clic en **[!UICONTROL Reorder]**, que se muestra en la barra de botones superior.

   ![Detalles del pedido en el administrador](./assets/order-view-admin.png){width="600" zoomable="yes"}

   Después de hacer clic en **[!UICONTROL Reorder]**, la página _Crear nuevo pedido_ se abrirá con la opción de reordenar productos.

   ![Crear pedido](./assets/create-reorder-page.png){width="600" zoomable="yes"}

1. Rellene todos los campos obligatorios según sea necesario.

1. Para enviar la solicitud, haga clic en **[!UICONTROL Submit Order]**.
