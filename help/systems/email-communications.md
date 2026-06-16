---
title: Configurar comunicaciones por correo electrónico
description: Obtenga información sobre cómo configurar las comunicaciones por correo electrónico, incluido el enrutamiento del correo electrónico devuelto o las respuestas a una dirección de correo electrónico específica.
exl-id: 7e62e9c5-f214-4fd5-becc-99dcb093cd5c
feature: Communications, Configuration
TQID: https://experienceleague.adobe.com/0spSxu59rF2KomOWVI5iR9pcg2r-VLm-GiXvJvatnww
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 310
ht-degree: 0%

---

# Configurar comunicaciones por correo electrónico

La _configuración de envío de correo_ le permite enrutar el correo electrónico devuelto o las respuestas a una dirección específica. Si el almacén se está ejecutando en un servidor SMTP o Windows, puede comprobar la configuración del host y del puerto.

>[!IMPORTANT]
>
>**Aviso de seguridad** Todos los comerciantes deben establecer inmediatamente su configuración de envío de correo para protegerse contra un posible ataque de ejecución de código remoto identificado recientemente. Hasta que se resuelva este problema, es muy recomendable que evite usar [!DNL Sendmail] para comunicaciones por correo electrónico. En _[!UICONTROL Mail Sending Settings]_, asegúrese de que_[!UICONTROL Set Return Path]_ está establecido en `No`.

Para obtener una lista detallada de las opciones de configuración, consulte [_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md) en la _Referencia de configuración_.

## Configurar comunicaciones por correo electrónico

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL System]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Mail Sending Settings]** y haga lo siguiente:

   ![Configuración avanzada: configuración de envío de correo](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - Si es necesario, establezca **[!UICONTROL Disable Email Communications]** en `No`.

   - Para **[!UICONTROL Transport]**, elija el tipo de transporte para las comunicaciones por correo electrónico desde el almacén: `Sendmail` o `SMTP`

   - Si se ejecuta en un servidor SMTP o Windows, compruebe la siguiente configuración:

      - **[!UICONTROL Host]** - `localhost` u otro

      - **[!UICONTROL Port (25)]** - `25` u otro

   - Para **[!UICONTROL Set Return Path]**, elija una de las siguientes opciones:

      - `No` - (Medida de seguridad recomendada) Las rutas devolvieron correo electrónico a la dirección de correo electrónico predeterminada de la tienda.
      - `Yes` - Rutas devolvió un correo electrónico a la dirección de correo electrónico predeterminada de la tienda.
      - `Specified` - Rutas devolvió un correo electrónico a la dirección de correo electrónico especificada en **[!UICONTROL Return Path Email]**.

   - Si se ejecuta en un servidor SMTP, configure la conexión:

      - **[!UICONTROL Username]** - Escriba el nombre de usuario de inicio de sesión para el servidor SMTP.
      - **[!UICONTROL Password]** - Escriba la contraseña para el inicio de sesión del servidor SMTP.
      - **[!UICONTROL Auth]** - Elija el tipo de autenticación para la conexión del servidor SMTP: `NONE`, `PLAIN` o `LOGIN`
      - **[!UICONTROL SSL]** - Elija el tipo de verificación para el certificado de seguridad del servidor: `SSL` o `TLS`

     ![Configuración avanzada: configuración de envío de correo](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Sales Emails]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL General Settings]**.

1. Establezca **[!UICONTROL Asynchronous sending]** en `Enable`.

   ![Configuración de ventas - configuración general de correo electrónico](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   Para obtener una lista detallada de las opciones de configuración, consulte [_Opciones generales_](../configuration-reference/sales/sales-emails.md) en la _Referencia de configuración_.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
