---
title: Configurar registros de regalos
description: Obtenga información sobre cómo habilitar los registros de regalos y configurar las notificaciones de correo electrónico relacionadas.
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
TQID: https://experienceleague.adobe.com/a7DRiAPSkWhBIPdXPXnH3HB1uw9d4WY4vXOtfgg9kRY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 358
ht-degree: 0%

---

# Configurar registros de regalos

{{ee-feature}}

Antes de poder ofrecer registros de regalos a sus clientes, debe habilitar los registros de regalos y configurar las notificaciones de correo electrónico relacionadas. Adobe Commerce envía las siguientes notificaciones por correo electrónico en respuesta a los eventos del flujo de trabajo del registro de regalos.

- Cuando se crea un nuevo registro de regalos, se envía un correo electrónico al propietario con un vínculo al registro que se puede compartir.
- Opcionalmente, la tienda puede enviar una notificación con un vínculo al registro de regalos a los amigos y familiares del propietario del registro de regalos.
- Se notifica al propietario cuando se compran artículos en el registro de regalos, pero no se indica el comprador.

Adobe Commerce tiene plantillas predefinidas para cada uno de estos mensajes de correo electrónico que se pueden personalizar para su marca.

## Paso 1. Activar registros de regalos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Gift Registry]**

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL General Options]** y haga lo siguiente:

   ![Configuración de clientes - Registro general de regalos](../configuration-reference/customers/assets/gift-registry-general-options.png){width="600" zoomable="yes"}

   - El Registro de regalos está habilitado de forma predeterminada. Si es necesario, establezca **[!UICONTROL Enable Gift Registry]** en `Yes`.

   - Para **[!UICONTROL Maximum Registrants]**, escriba el número máximo de personas que pueden ser invitadas a participar en un evento del registro de regalos.

## Paso 2. Configurar notificaciones por correo electrónico

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Owner Notification]** y haga lo siguiente:

   ![Configuración de clientes - notificación al propietario del registro de regalos](../configuration-reference/customers/assets/gift-registry-owner-notification.png){width="600" zoomable="yes"}

   - Elija el **[!UICONTROL Email Template]** que notifica a los propietarios del registro de regalos cuando se crean sus registros.

   - Elija el [contacto de tienda](../getting-started/store-details.md#store-email-addresses) que aparece como **[!UICONTROL Email Sender]** del mensaje.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Gift Registry Sharing]** y haga lo siguiente:

   ![Configuración de clientes - uso compartido del registro de regalos](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png){width="600" zoomable="yes"}

   - Elija el **[!UICONTROL Email Template]** que notifica a los destinatarios del registro de regalos cuando se comparte un registro con ellos.

   - Elija el identificador de almacén que aparece como **[!UICONTROL Email Sender]** del mensaje.

   - Para **[!UICONTROL Maximum Sent Emails Threshold]**, escriba el número máximo de correos electrónicos que se pueden enviar al mismo tiempo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Gift Registry Update]** y haga lo siguiente:

   ![Configuración de clientes - actualización del registro de regalos](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png){width="600" zoomable="yes"}

   - Elija el **[!UICONTROL Email Template]** que notifica a los propietarios del registro de regalos de los cambios realizados en el registro.

   - Elija el identificador de almacén que aparece como **[!UICONTROL Email Sender]** del mensaje.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

1. Cuando se le solicite, actualice la caché.

   Una vez que se actualiza la caché, el Registro de regalos aparece en el menú Tiendas en Otras configuraciones y está disponible en las cuentas de los clientes.
