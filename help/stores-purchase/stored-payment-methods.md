---
title: Métodos de pago almacenados
description: Descubra cómo los clientes pueden utilizar los métodos de pago almacenados en su tienda de Commerce.
exl-id: 5e264f84-1891-4ee9-8ebe-55ac9c93ab8c
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Métodos de pago almacenados

Los clientes con acceso a una cámara acorazada segura para almacenar información de pago pueden acelerar el proceso de pago sin ingresar la información de su tarjeta de crédito cada vez. Si [Compra instantánea](checkout-instant-purchase.md) está habilitada, los clientes pueden evitar el proceso de cierre de compra en dos pasos y realizar el pedido desde la página del producto.

Se requiere un método de pago que admita un almacén seguro, como [Braintree](braintree.md). Cuando se activa un depósito seguro en la configuración del método de pago, los clientes tienen la opción, durante el cierre de compra, de guardar la información de su tarjeta de crédito como un método de pago almacenado. Los clientes pueden administrar los métodos de pago almacenados desde su panel de cuentas.

![Métodos de pago almacenados](./assets/customer-account-stored-payment-methods.png){width="700" zoomable="yes"}

## Agregar método de pago almacenado al finalizar la compra

1. Desde la tienda, el cliente va a la página de detalles del producto.

1. Añade un producto al carro de compras.

1. Continúa en la página de cierre de compra.

1. Completa el paso _Envío_.

1. Selecciona el método de pago **[!UICONTROL Braintree Credit Card]**.

1. Rellena los datos de la tarjeta de crédito.

1. Selecciona la casilla de verificación **[!UICONTROL Save for later use]**.

1. Clics **[!UICONTROL Place Order]**.

El método de pago guardado se muestra en la pestaña _[!UICONTROL Stored Payment Methods]_&#x200B;del panel del cliente.

## Eliminar un método de pago almacenado

El cliente no puede editar los métodos de pago almacenados que haya añadido anteriormente; solo se pueden eliminar. Esta acción no se puede deshacer.

1. En la barra lateral de su cuenta, el cliente selecciona **[!UICONTROL Stored Payment Methods]**.

1. Busca el movimiento de método de pago que se va a eliminar.

1. Clics **[!UICONTROL Delete]**.

1. Para confirmar la acción, haga clic en **[!UICONTROL OK]**.
