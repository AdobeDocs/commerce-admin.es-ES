---
title: Notificación de error de pago
description: Obtenga información sobre cómo configurar las comunicaciones por correo electrónico para un método de pago que no complete una transacción.
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
feature: Payments, Communications
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Notificación de error de pago

Se envía una notificación al contacto de tienda o a un usuario administrador designado si el método de pago seleccionado durante el cierre de compra no consigue completar la transacción.

## Paso 1: Actualizar la plantilla de correo electrónico

Asegúrese de haber actualizado la plantilla de correo electrónico necesaria para reflejar su marca. Para obtener una lista completa de plantillas, consulte [Lista de plantillas de correo electrónico](../systems/email-templates.md#email-template-list).

## Paso 2: Configuración de los correos electrónicos con errores de pago

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Checkout]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Payment Failed Emails]**.

   ![Correos electrónicos con errores de pago](../configuration-reference/sales/assets/checkout-payment-failed-emails.png){width="600" zoomable="yes"}

1. Defina las opciones para los correos electrónicos con errores de pago:

   - Establezca **[!UICONTROL Payment Failed Email Sender]** en el contacto de tienda que aparece como el remitente del mensaje.
   - Establezca **[!UICONTROL Payment Failed Email Receiver]** en el contacto de tienda que debe recibir notificaciones de transmisiones de correo electrónico con errores.
   - Establece **[!UICONTROL Payment Failed Template]** en la plantilla que se usa para el correo electrónico que se envía cuando falla el método de pago durante el cierre de compra.

1. Para **[!UICONTROL Send Payment Failed Email Copy To]**, escriba la dirección de correo electrónico de cualquier persona que vaya a recibir una copia de la notificación de error en el pago.

   Si envía una copia a varios destinatarios, separe cada dirección con una coma.

1. Establezca **[!UICONTROL Payment Failed Copy Method]** en una de las siguientes opciones:

   - `Bcc` - Envía una _copia de cortesía a ciegas_ incluyendo el destinatario en el encabezado del mismo correo electrónico que se envía al cliente. El destinatario CCO no es visible para el cliente.
   - `Separate Email` - Envía la copia como un correo electrónico independiente.

1. Haga clic en **[!UICONTROL Save Config]**.
