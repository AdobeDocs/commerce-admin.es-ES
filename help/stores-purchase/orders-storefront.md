---
title: Administración de pedidos de tienda
description: Descubra cómo los clientes pueden ver y administrar su historial de pedidos en la tienda de Commerce.
exl-id: 85d953e6-f5a1-4a5e-a6ef-36b9cf6988bb
feature: Orders, Storefront
source-git-commit: c13a4b730ed70ed4829cc20b13c2723137dcbb3a
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Administración de pedidos de tienda

Los clientes tienen acceso a todos sus pedidos desde su cuenta. Los pedidos se pueden ver, filtrar, rastrear y volver a enviar como nuevos pedidos. Según el estado del pedido, los clientes pueden imprimir sus pedidos, facturas, envíos y registros de devolución.

## Filtrar pedidos

{{b2b-feature}}

Los resultados iniciales de _[!UICONTROL My Orders]_también contienen pedidos coincidentes de usuarios subordinados de todos los sitios web dentro de la instancia de comercio. Un cliente asociado a una cuenta de compañía puede filtrar la lista de pedidos para buscar rápidamente registros en los resultados. Para mostrar las opciones de filtro, el cliente hace clic en **[!UICONTROL Filter]**y luego en **[!UICONTROL Close]**para ocultar los filtros.

![Mis pedidos](./assets/account-dashboard-my-orders-b2b.png){width="700" zoomable="yes"}

| Filtrar | Descripción |
| ------ | ----------- |
| [!UICONTROL SKU or Product Name] | Introduce un SKU o un nombre de producto. |
| [!UICONTROL Order Number] | Puede ser un número de pedido completo o parcial. |
| [!UICONTROL Order Status] | Elige un valor del menú desplegable para filtrar por estado. |
| [!UICONTROL Invoice Number] | Introduce un número de factura completo o parcial. |
| [!UICONTROL Order Date] | Establece uno o ambos campos de fecha para filtrar por fecha de pedido. |
| [!UICONTROL Created by] | Filtra los pedidos de la compañía por el creador del pedido. |
| [!UICONTROL Order Total] | Establece los valores mínimo, máximo o ambos para filtrar por total de pedido. |

## Ver un pedido

Un cliente encuentra el pedido en la lista y hace clic en **[!UICONTROL View Order]**. Desde el orden abierto, pueden realizar cualquiera de las siguientes acciones:

![Ver pedido](./assets/customer-account-order-items-ordered.png){width="700" zoomable="yes"}

### Ver productos pedidos recientemente

El bloque **[!UICONTROL Recent Orders]** se muestra en la barra lateral y en la página **[!UICONTROL My Account]** para los clientes que iniciaron sesión después de realizar un pedido. Muestra cinco productos de la última compra.

El cliente puede leer productos al carro de compras seleccionando los productos y haciendo clic en **[!UICONTROL Add to Cart]**. También pueden ver el último pedido haciendo clic en **[!UICONTROL View all]**, que redirige a la página _[!UICONTROL My Account]_y al bloque **[!UICONTROL Recent Orders]**.

### Imprimir pedido

1. El cliente hace clic en **[!UICONTROL Print Order]**.

1. Sigue las instrucciones del cuadro de diálogo Imprimir para completar la impresión.

### Imprimir facturas

1. En la ficha **[!UICONTROL Invoices]**, el cliente hace clic en una de las siguientes opciones:

   - **[!UICONTROL Print All Invoices]**

   - **[!UICONTROL Print Invoice]**

   ![Facturas](./assets/customer-account-order-invoices.png){width="700" zoomable="yes"}

1. Utiliza el diálogo Imprimir para completar la impresión.

### Imprimir envíos

1. En la ficha **[!UICONTROL Order Shipments]**, el cliente hace clic en una de las siguientes opciones:

   - **[!UICONTROL Print All Shipments]**

   - **[!UICONTROL Print Shipment]**

   ![Imprimir todos los envíos](./assets/customer-account-order-shipments.png){width="700" zoomable="yes"}

1. Utiliza el diálogo Imprimir para completar la impresión.

### Seguimiento de un envío

1. En la ficha **[!UICONTROL Order Shipments]**, haga clic en **[!UICONTROL Track this Shipment]**.

   Cualquier información de seguimiento disponible aparece en una ventana emergente.

1. Cuando esté listo, el cliente hace clic en **[!UICONTROL Close Window]**.

### Imprimir reembolsos

1. En la ficha **Reembolsos**, el cliente hace clic en una de las siguientes opciones:

   - **Imprimir todos los reembolsos**

   - **Reembolso por impresión**

   ![Reembolsos](./assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

1. Utiliza el diálogo Imprimir para completar la impresión.

Los repedidos están disponibles para los clientes cuando la opción de configuración [_Permitir reordenar_](reorders-allow.md) está habilitada.

Un cliente puede iniciar la funcionalidad de reordenar para un pedido específico desde dos páginas:

- Página Mis pedidos
- Página Vista de pedidos

## Reordenamientos

El vínculo _[!UICONTROL Reorder]_se muestra en la lista con pedidos cerca del vínculo_[!UICONTROL View]_.

![Reordenar vínculo en la página Mi pedido](./assets/account-dashboard-reorder.png){width="700" zoomable="yes"}

**Caso 1.** Todos los productos del pedido están disponibles para reordenar

Se redirige al cliente al carro de compras y se agregan todos los productos al carro de compras.

**Caso 2.** Algunos/todos los productos del pedido no están disponibles para reordenar

>[!NOTE]
>
>Es posible reordenar `Not Visible Individually` productos.

El vínculo _[!UICONTROL Reorder]_no aparece en las páginas_[!UICONTROL My Orders]_ y _[!UICONTROL View Order]_.

![Mi página de pedidos](./assets/account-dashboard-reorder-grid.png){width="700" zoomable="yes"}

>[!TIP]
>
>Si el carro de compras no está vacío y el cliente hace clic en **[!UICONTROL Reorder]** (desde la página [!UICONTROL My Orders] o [!UICONTROL Order View]), los productos existentes permanecen en el carro de compras con los productos de repedido agregados.

## Cancelar pedidos

Cancelar está disponible para los clientes cuando la opción de configuración [_Permitir cancelación_](cancel-allow.md) está habilitada.

Un cliente puede iniciar la funcionalidad de cancelación para un pedido específico desde tres páginas:

- Página Mis pedidos
- Página Vista de pedidos
- Página Mi cuenta

El vínculo _[!UICONTROL Cancel Order]_se muestra cerca del vínculo_[!UICONTROL Reorder]_. Si el pedido no se puede cancelar, no se muestra el vínculo.

![Cancelar vínculo en la página Mi pedido](./assets/account-dashboard-cancel.png){width="700" zoomable="yes"}

Para realizar la cancelación, el cliente:

1. Clics **[!UICONTROL Cancel Order]**

1. Proporciona un motivo de cancelación

   ![Cancelar motivos de pedido](./assets/cancel-order-reasons.png){width="700" zoomable="yes"}

   Puede personalizar los motivos de cancelación en la página [_Permitir cancelación_](cancel-allow.md).

1. Clics **[!UICONTROL Confirm]**

   ![Cancelar en la página Mi pedido](./assets/cancel-order.png){width="700" zoomable="yes"}

   Después de la cancelación, los pedidos que estaban en estado _[!UICONTROL Pending]_, cambian al estado_[!UICONTROL Canceled]_, los pedidos que estaban en estado _[!UICONTROL Processing]_, cambian al estado_[!UICONTROL Closed]_ y se procesa un reembolso.

   Cuando finaliza la cancelación, se envía un correo electrónico al cliente.

   ![Cancelar correo electrónico de pedido](./assets/cancel-order-email.png){width="700" zoomable="yes"}

   La información de cancelación se agrega al historial de pedidos del cliente. Aparece dentro de las notas del pedido y en la pestaña historial de comentarios.

   ![Cancelar notas de pedidos](./assets/cancel-order-notes.png){width="700" zoomable="yes"}

   ![Cancelar historial de comentarios](./assets/cancel-order-comments.png){width="700" zoomable="yes"}

   Si, por algún motivo, la solicitud ha cambiado a un estado que no se puede cancelar y el cliente no ha actualizado la página, seguirá apareciendo el vínculo para cancelar la solicitud. Sin embargo, cuando intentan cancelar, aparece un mensaje de error.

   ![Mensaje de error de cancelación de pedido](./assets/cancel-order-error-message.png){width="700" zoomable="yes"}

   Después de actualizar la página, puede ver que el pedido ya se ha completado, por lo que la cancelación no ha funcionado.

   ![Cancelar pedido después de actualizar](./assets/cancel-order-after-refresh.png){width="700" zoomable="yes"}
