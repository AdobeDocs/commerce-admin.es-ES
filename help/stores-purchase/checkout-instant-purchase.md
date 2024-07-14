---
title: Compra instantánea
description: Obtenga información acerca de la compra instantánea y cómo puede proporcionar un cierre de compra rápido para las cuentas de cliente registradas.
exl-id: f299f364-d7e3-4567-8c7b-955129011a19
feature: Checkout
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# Compra instantánea

_Compra instantánea_ permite a los clientes acelerar el proceso de cierre de compra mediante la información guardada en su cuenta. Cuando está habilitado, aparece el botón _Compra instantánea_ debajo del botón _Agregar al carro_ en la página del producto para los clientes que cumplan con los requisitos.

![Página de producto con la opción de compra instantánea ](./assets/storefront-checkout-instant-purchase.png){width="700" zoomable="yes"}

## Requisitos del cliente

- El cliente [ha iniciado sesión](../customers/customer-sign-in.md) en su cuenta.

- La cuenta de cliente tiene [dirección de facturación y envío predeterminada](../customers/account-dashboard-address-book.md).

- Hay al menos un [método de envío](delivery.md) disponible para el país especificado en la dirección de envío predeterminada.

- La cuenta de cliente tiene un método de pago [almacenado](../stores-purchase/stored-payment-methods.md) con el Vault habilitado.

  Los siguientes métodos de pago se pueden utilizar para proporcionar acceso seguro a la información guardada de la tarjeta de crédito:

   - [Tarjetas de crédito de Braintree](braintree.md) (la compra instantánea no se puede usar con tarjetas de crédito de Braintree si 3D Secure está habilitado).
   - [Braintree con PayPal activado](braintree.md)
   - [PayPal Payflow Pro](paypal-payflow-pro.md)

## Compra instantánea en la tienda

1. En la tienda, el cliente va a la página del producto del artículo que se va a comprar.

1. Selecciona las opciones requeridas y hace clic en **[!UICONTROL Instant Purchase]**.

   ![Cuadro de diálogo de confirmación para confirmar la compra instantánea](./assets/storefront-checkout-instant-purchase-confirmation.png){width="500" zoomable="yes"}

1. Revisa la información de **[!UICONTROL Instant Purchase Confirmation]** y hace clic en **[!UICONTROL OK]** para completar la transacción.

   Un mensaje de confirmación y un número de pedido aparecen en la parte superior de la página del producto.

## Configuración de compra instantánea

### Paso 1: Abrir la página de configuración

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

### Paso 2: Configuración del almacén de métodos de pago

Puede utilizar la compra instantánea con Braintree o Servicios de pago para Adobe Commerce y Magento Open Source. Debe habilitarse el depósito antes de que un comprador pueda utilizar la función de compra instantánea.

Obtenga información sobre cómo configurar el método de pago y habilitar el depósito para Braintree o Servicios de pago:

- [Braintree](braintree.md)
- [Documentación de servicios de pago](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html)

### Paso 3: Activar compra instantánea

1. En el panel izquierdo bajo la sección _[!UICONTROL Sales]_, elija **[!UICONTROL Sales]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Instant Purchase]**.

1. Si este cambio es para una vista de tienda específica, [elija la vista de tienda](../configuration-reference/scope-change.md#set-the-scope) donde se aplica la configuración.

   Cuando se le solicite, haga clic en **[!UICONTROL OK]** para continuar.

1. Establezca **[!UICONTROL Enabled]** en `Yes`.

1. Escriba el(la) **[!UICONTROL Button Text]** que desea que aparezca en el botón.

   El texto del botón se puede cambiar para cada vista de tienda o idioma. De manera predeterminada, el texto del botón es `Instant Purchase`.

   ![Configuración - opciones de compra instantánea](../configuration-reference/sales/assets/sales-instant-purchase.png){width="600" zoomable="yes"}

   Para obtener una descripción detallada de cada una de estas opciones de configuración, consulte [Compra instantánea](../configuration-reference/sales/sales.md#instant-purchase) en la _Guía de referencia de configuración_.

1. Haga clic en **[!UICONTROL Save Config]**.

1. Cuando se le pida que actualice la caché, haga clic en **[!UICONTROL Cache Management]** en el mensaje del sistema y siga las instrucciones para vaciar la caché.
