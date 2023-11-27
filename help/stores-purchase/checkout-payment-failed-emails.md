---
title: Notificación de error de pago
description: Obtenga información sobre cómo configurar las comunicaciones por correo electrónico para un método de pago que no complete una transacción.
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
feature: Payments, Communications
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Notificación de error de pago

Se envía una notificación al contacto de tienda o a un usuario administrador designado si el método de pago seleccionado durante el cierre de compra no consigue completar la transacción.

## Paso 1: Actualizar la plantilla de correo electrónico

Asegúrese de haber actualizado la plantilla de correo electrónico necesaria para reflejar su marca. Para obtener una lista completa de las plantillas, consulte [Lista de plantillas de correo electrónico](../systems/email-templates.md#email-template-list).

## Paso 2: Configuración de los correos electrónicos con errores de pago

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Checkout]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Payment Failed Emails]** sección.

   ![Correos electrónicos con errores de pago](../configuration-reference/sales/assets/checkout-payment-failed-emails.png){width="600" zoomable="yes"}

1. Defina las opciones para los correos electrónicos con errores de pago:

   - Establecer **[!UICONTROL Payment Failed Email Sender]** al contacto de tienda que aparece como el remitente del mensaje.
   - Establecer **[!UICONTROL Payment Failed Email Receiver]** al contacto de tienda que va a recibir la notificación de las transmisiones de correo electrónico fallidas.
   - Establecer **[!UICONTROL Payment Failed Template]** a la plantilla que se utiliza para el correo electrónico que se envía cuando el método de pago falla durante el cierre de compra.

1. Para **[!UICONTROL Send Payment Failed Email Copy To]**, introduzca la dirección de correo electrónico de cualquier persona que vaya a recibir una copia de la notificación de error en el pago.

   Si envía una copia a varios destinatarios, separe cada dirección con una coma.

1. Establecer **[!UICONTROL Payment Failed Copy Method]** a uno de los siguientes:

   - `Bcc` - Envía un _copia de cortesía oculta_ al incluir el destinatario en el encabezado del mismo correo electrónico que se envía al cliente. El destinatario CCO no es visible para el cliente.
   - `Separate Email` : envía la copia como un correo electrónico independiente.

1. Haga clic **[!UICONTROL Save Config]**.
