---
title: Creación de un pedido
description: Obtenga información sobre cómo crear un pedido para un cliente en el Administrador de comercio.
exl-id: 8a766a5b-55d6-4d78-859e-38937e0183d3
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 1%

---

# Creación de un pedido

Para los clientes registrados que necesiten asistencia, puede crear un pedido completo directamente desde el administrador. El _[!UICONTROL Create New Order]_Este formulario incluye toda la información necesaria para el proceso normal de cierre de compra, con resúmenes de actividad en el panel de control de la cuenta del cliente.

![Creación de un pedido para un cliente](./assets/create-new-order.png){width="700" zoomable="yes"}

## Paso 1: Crear un pedido

1. En el _Administrador_ barra lateral, haga clic en **[!UICONTROL Customers]**.

1. Busque al cliente en la cuadrícula.

1. En el _Acción_ , haga clic en **[!UICONTROL Edit]**.

1. En el encabezado del espacio de trabajo, haga clic en **[!UICONTROL Create Order]**.

   ![Encabezado de Workspace](./assets/order-create-buttons.png){width="700" zoomable="yes"}

   También puede crear un pedido en la [Ordenar espacio de trabajo](orders.md#orders-workspace) haciendo clic en **[!UICONTROL Create New Order]**.

## Paso 2: Añadir productos

Si la tienda tiene varias vistas, elija la vista de la tienda en la que se va a realizar el pedido.

### Añadir productos del [!UICONTROL Customer's Activities] barra lateral

Puede transferir artículos al carro de compras desde la lista de artículos deseados de un cliente o desde cualquier artículo que haya visto, comparado o pedido recientemente.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) una de las siguientes secciones:

   - **[!UICONTROL Wish List]**
   - **[!UICONTROL Last Ordered Items]**
   - **[!UICONTROL Products in Comparison List]**
   - **[!UICONTROL Recently Compared Products]**
   - **[!UICONTROL Recently Viewed Products]**

1. Seleccione la casilla de verificación de cada producto en el panel izquierdo.

1. Desplácese hacia abajo y haga clic **[!UICONTROL Update Changes]**.

   El elemento aparece en el formulario de pedido.

   ![Añadir al carro](./assets/create-order-add-wishlist.png){width="600" zoomable="yes"}

### Añadir productos del catálogo

1. Haga clic **[!UICONTROL Add Products]**.

   ![Añadir productos](./assets/account-add-wishlist-product.png){width="600" zoomable="yes"}

1. En la cuadrícula, seleccione la casilla de verificación de cada producto que se agregará al carro de compras e introduzca la **[!UICONTROL Qty]** que se va a comprar.

   ![Seleccionar productos](./assets/create-order-from-catalog.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >La cuadrícula de selección de productos siempre muestra los precios base regulares de los productos, sin descuentos ni reglas de precio de grupo o carro de compras aplicadas. El precio final del producto solo se calcula cuando el producto se añade a un pedido/carro de compras.

1. Configure las opciones de producto disponibles:

   - Haga clic **[!UICONTROL Configure]**.

   - Complete las opciones según sea necesario.

   - Haga clic **[!UICONTROL OK]**.

   - Clic **[!UICONTROL Add Selected Product(s) to Order]** para actualizar el carro de compras.

1. Si un producto está configurado para [opciones de regalo](../catalog/product-gift-options.md), configure las opciones según sea necesario.

1. Anular el precio de un artículo si es necesario:

   - Seleccione el **[!UICONTROL Custom Price]** y escriba el nuevo precio en el siguiente cuadro.

   - Para actualizar los totales del carro de compras, haga clic en **[!UICONTROL Update Items and Quantities]**.

   ![Precio personalizado](./assets/create-order-custom-price.png){width="600" zoomable="yes"}

1. Complete las siguientes secciones según sea necesario para el pedido:

   - [!UICONTROL Order Currency]
   - [!UICONTROL Apply Coupon Codes / Gift Card Code]
   - [!UICONTROL Payment Method]
   - [!UICONTROL Shipping Method]
   - [!UICONTROL Order Comments]

>[!NOTE]
>
>Consulte la [Guía de servicios de pago](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/create-order.html) para obtener más información acerca de los métodos de pago que admiten esta funcionalidad cuando se instala y configura la extensión de servicios de pago.

## Paso 3: Enviar el pedido

Haga clic **[!UICONTROL Submit Order]**.

Se envía una confirmación al cliente, que puede ver los detalles del pedido desde su cuenta.
