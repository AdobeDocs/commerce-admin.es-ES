---
title: Métodos de pago almacenados
description: Descubra cómo los clientes pueden utilizar los métodos de pago almacenados en su tienda de Commerce.
exl-id: 5e264f84-1891-4ee9-8ebe-55ac9c93ab8c
feature: Payments
TQID: https://experienceleague.adobe.com/dYEYXgEIp83AKhHepfDQVNR9YBUQGbJ7B2zu8UTM-I4
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 226
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

El método de pago guardado se muestra en la pestaña _[!UICONTROL Stored Payment Methods]_del panel del cliente.

## Eliminar un método de pago almacenado

El cliente no puede editar los métodos de pago almacenados que haya añadido anteriormente; solo se pueden eliminar. Esta acción no se puede deshacer.

1. En la barra lateral de su cuenta, el cliente selecciona **[!UICONTROL Stored Payment Methods]**.

1. Busca el movimiento de método de pago que se va a eliminar.

1. Clics **[!UICONTROL Delete]**.

1. Para confirmar la acción, haga clic en **[!UICONTROL OK]**.
