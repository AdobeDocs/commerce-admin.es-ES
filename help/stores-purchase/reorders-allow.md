---
title: Permitir reordenamientos
description: Aprenda a proporcionar funciones de reorganización a sus clientes.
exl-id: 9fe4c4fb-8596-4fd0-a93b-927ebdfc0c94
feature: Orders, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Permitir reordenamientos

Cuando está activada, los repedidos se pueden realizar directamente desde la cuenta del cliente o desde el pedido original en la _Administrador_. Los repedidos están habilitados de forma predeterminada.

![Vínculo de reorganización del cliente en Admin](./assets/customer-reorder.png){width="700" zoomable="yes"}

## Criterios para activar el repedido en un pedido

- El _Permitir reordenar_ La opción de configuración debe estar activada.

- Si el orden está en `Hold` o en `Payment Review` estado, la opción de reordenar está desactivada.

- Si alguno de los artículos del pedido no está disponible, está agotado o deshabilitado, la opción de reordenar está deshabilitada en la tienda.

- Un _Administrador_ puede reordenar incluso si alguno de los elementos está agotado o deshabilitado.

## Configurar para permitir nuevos pedidos de clientes

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Sales]** debajo.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Reorder]** sección.

   ![Reordenar opciones](../configuration-reference/sales/assets/sales-reorder.png){width="600" zoomable="yes"}

1. Establecer **[!UICONTROL Allow Reorder]** hasta `Yes`.

   Esta configuración habilita la funcionalidad de reordenar desde la cuenta de cliente en la tienda o la lista de pedidos en el Administrador.

1. Haga clic **[!UICONTROL Save Config]**.

## Reordenar desde la tienda

Un cliente puede iniciar la funcionalidad de reordenar para un pedido específico desde dos páginas:

- _Mis pedidos_ página

- _Vista de pedidos_ página

### Mis pedidos

El _Reordenar_ El botón siempre se muestra en la lista con Pedidos (incluso si todos los productos del pedido no están disponibles para reordenarlos).

![Ejemplo de tienda: página Mis pedidos](./assets/my-order-page-view.png){width="700" zoomable="yes"}

**Caso 1.** Todos los productos del pedido son **disponible** para reordenar

Se redirige al usuario al carro de compras y se agregan todos los productos a este

![Carro de compras](./assets/shopping-cart-page.png){width="700" zoomable="yes"}

**Caso 2.** Algunos/todos los productos del pedido son **no disponible** para reordenar

>[!NOTE]
>
>Es posible realizar un nuevo pedido `Not Visible Individually` productos.

El _Reordenar_ El botón no aparece en _Mis pedidos_ y _Ver pedido_ páginas.

![Mis pedidos página 1](./assets/my-orders-view-page1.png){width="700" zoomable="yes"}

### Página de vista de pedidos

**Caso 1.** Todos los productos del pedido están disponibles para reordenar

Se redirige al usuario al carro de compras y se agregan todos los productos a este

**Caso 2.** Algunos/todos los productos del pedido son **no disponible** para reordenar

>[!NOTE]
>
>Es posible realizar un nuevo pedido `Not Visible Individually` productos.

El _Reordenar_ El botón no aparece en _Mis pedidos_ y _Ver pedido_ páginas.

![Página de detalles del pedido](./assets/order-view-page.png){width="700" zoomable="yes"}

### El carro no está vacío

Si el carro de compras no está vacío y el usuario hace clic en **[!UICONTROL Reorder]** (desde el _Mis pedidos_  o _Vista de pedidos_ ), los productos existentes permanecen en el carro de compras con los productos de repedido agregados.

![Reordenar elementos](./assets/shopping-cart-view1.png){width="700" zoomable="yes"}

## Reordenar desde el administrador

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Busque el pedido y abra en **[!UICONTROL View]** modo.

1. Clic **[!UICONTROL Reorder]** que se muestra en la barra de botones superior.

   ![Detalles del pedido en el administrador](./assets/order-view-admin.png){width="600" zoomable="yes"}

   Después de hacer clic en **[!UICONTROL Reorder]**, el _Crear nuevo pedido_ se abre la página con reordenar productos.

   ![Crear reordenar](./assets/create-reorder-page.png){width="600" zoomable="yes"}

1. Rellene todos los campos obligatorios según sea necesario.

1. Para enviar la solicitud, haga clic en **[!UICONTROL Submit Order]**.
