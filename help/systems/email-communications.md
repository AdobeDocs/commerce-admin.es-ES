---
title: Configurar comunicaciones por correo electrónico
description: Obtenga información sobre cómo configurar las comunicaciones por correo electrónico, incluido el enrutamiento del correo electrónico devuelto o las respuestas a una dirección de correo electrónico específica.
exl-id: 7e62e9c5-f214-4fd5-becc-99dcb093cd5c
feature: Communications, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Configurar comunicaciones por correo electrónico

La _configuración de envío de correo_ le permite enrutar el correo electrónico devuelto o las respuestas a una dirección específica. Si el almacén se está ejecutando en un servidor SMTP o Windows, puede comprobar la configuración del host y del puerto.

>[!IMPORTANT]
>
>**Aviso de seguridad** Todos los comerciantes deben establecer inmediatamente su configuración de envío de correo para protegerse contra un posible ataque de ejecución de código remoto identificado recientemente. Hasta que se resuelva este problema, es muy recomendable que evite usar [!DNL Sendmail] para comunicaciones por correo electrónico. En _[!UICONTROL Mail Sending Settings]_, asegúrese de que&#x200B;_[!UICONTROL Set Return Path]_ está establecido en `No`.

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
