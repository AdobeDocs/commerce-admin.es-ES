---
title: Configuración de autenticación de doble factor para cuentas de usuario
description: Obtenga información sobre cómo configurar la autenticación de doble factor durante el inicio de sesión inicial del administrador y autenticar su identidad mediante una aplicación de dispositivo compatible.
exl-id: 1ea7f09e-4753-40fa-b9d4-376ba5d8f58f
role: Admin, User
feature: Configuration, Security, User Account
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# Configuración de autenticación de doble factor para cuentas de usuario

Estas instrucciones muestran cómo configurar la autenticación de doble factor durante el inicio de sesión inicial en Adobe Commerce o Magento Open Source y cómo autenticar su identidad mediante las siguientes aplicaciones y dispositivos.

Para obtener instrucciones completas, consulte [Inicio de sesión de administrador](../getting-started/admin-signin.md).

>[!NOTE]
>
>Las tiendas que han habilitado la autenticación [!DNL Adobe Identity Management Services] (IMS) tienen Adobe Commerce nativo y Magento Open Source 2FA deshabilitado. Los usuarios administradores que han iniciado sesión en su instancia de Commerce con sus credenciales de Adobe no necesitan volver a autenticarse en muchas tareas de administración. La autenticación la gestiona Adobe IMS cuando el usuario administrador inicia sesión en su sesión actual. Ver [[!DNL Adobe Identity Management Service] (IMS) Descripción general de la integración](../getting-started/adobe-ims-integration-overview.md).

## [!DNL Google Authenticator]

### Paso 1: Configurar [!DNL Google Authenticator]

1. Escriba las credenciales de su cuenta e inicie sesión en _Admin_. Aparece una nueva pantalla de autenticador con un código QR.

1. Abra la aplicación **[!UICONTROL Google Authenticator]** en su dispositivo móvil.

1. Haga clic en el signo más ( **+** ) para agregar una entrada y alinear el cuadro rojo con el código QR para escanear con la cámara del smartphone.

1. Cuando el teléfono reconozca el código QR y agregue una entrada, escribe ese código de 6 dígitos en el campo _Admin_ **[!UICONTROL Authenticator code]**.

1. Una vez finalizado, haga clic en **[!UICONTROL Confirm]**.

   ![Código QR de Google Authenticator](./assets/storefront-2fa-google-qrcode.png){width="300"}

### Paso 2: Iniciar sesión con [!DNL Google Authenticator]

1. Escriba las credenciales de su cuenta e inicie sesión en Commerce _Admin_.

   ![Autenticador de Google - iniciando sesión](./assets/storefront-2fa-google-code.png){width="300"}

1. Abra [!DNL Google Authenticator] en su dispositivo móvil.

1. Cuando se le solicite, introduzca el código de autenticación de seis dígitos.

1. Para guardar la autenticación para futuros inicios de sesión, marque la casilla de verificación **[!UICONTROL Trust this device, do not ask again]**.

1. Una vez finalizado, haga clic en **[!UICONTROL Confirm]**.

## [!DNL Duo Security]

[!DNL Duo] ofrece una versión de prueba gratuita y cargos según el número de usuarios asociados a la cuenta. Siga sus [instrucciones para configurar su cuenta y descargar la aplicación](https://duo.com/product/multi-factor-authentication-mfa/duo-mobile-app).

### Paso 1: Configurar [!DNL Duo Security]

1. Escriba las credenciales de su cuenta e inicie sesión en _Admin_.

1. Cuando aparezca la página de instalación de [!DNL Duo], haga clic en **[!UICONTROL Get Started]** y haga lo siguiente:

   ![Ejemplo de tienda - Configuración de Duo](./assets/storefront-2fa-duo-setup-options.png){width="300"}

1. Seleccione la opción. Puede elegir Touch ID, Duo Mobile, Security Key o Phone Number. En este ejemplo se muestra la opción Duo Mobile o Phone Number.

1. Cuando se le solicite, escriba su número de teléfono y haga clic en **[!UICONTROL Continue]**.

   Confirme la propiedad enviando y verificando la contraseña en el número de teléfono.

1. Cuando se le pida que instale [!DNL Duo Mobile] para su tipo de teléfono, haga clic en **[!UICONTROL I have Duo Mobile]**.

1. Abra [!DNL Duo Mobile] y escanee el código QR para sincronizar el autenticador con Adobe Commerce. Cuando se completa la activación, aparece una marca de verificación.

1. Puede agregar más dispositivos (si es necesario) u omitir. La configuración se ha completado y puede iniciar sesión con Duo.

   ![Acciones de verificación Duo](./assets/storefront-2fa-duo-setup-complete.png){width="300"}

### Paso 2: Iniciar sesión con [!DNL Duo Security]

El siguiente ejemplo muestra las opciones de `Ask me to choose an authenticator method`:

1. Cuando se le solicite, escriba sus credenciales de _Admin_ para iniciar sesión.

   ![Duo - iniciando sesión](./assets/storefront-2fa-duo-auth.png){width="300"}

1. Elija Iniciar sesión con Duo para obtener una notificación push en la aplicación Duo Mobile, iniciar sesión con Touch ID o continuar con otra opción que haya configurado durante la configuración.

1. Apruebe la solicitud desde la aplicación Duo/ Touch ID/ Mensaje de texto y su sesión se iniciará correctamente.

   ![Duo - iniciando sesión](./assets/storefront-2fa-duo-success.png){width="300"}

## [!DNL Authy]

[!DNL Authy] ofrece su aplicación y servicio sin cargo a los usuarios. Siga las instrucciones para descargar y configurar la aplicación para su dispositivo o explorador. Para obtener más información, consulte la [[!DNL Authy] documentación](https://authy.com/features/setup/).

### Paso 1: Configuración de la autoridad

1. Escriba las credenciales de su cuenta e inicie sesión en _Admin_.

   ![[!DNL Authy] registro](./assets/storefront-2fa-authy-auth.png){width="300"}

1. Cuando se le pida que se registre en Authy, haga lo siguiente:

   - Seleccione su país.

   - Introduzca su número de teléfono.

   - Seleccione **[!UICONTROL Verification method]**: `SMS` o `Call Me`

   Haga clic en **[!UICONTROL Continue]**. Se envía un mensaje al teléfono a través de un mensaje de texto SMS o una llamada.

1. Escriba el código de verificación que recibió y haga clic en **[!UICONTROL Verify]**.

1. Una vez finalizado, haga clic en **[!UICONTROL Confirm]**.

   ![[!DNL Authy] código de verificación](./assets/storefront-2fa-authy-verify.png){width="300"}

### Paso 2: Iniciar sesión con [!DNL Authy]

1. Escriba las credenciales de su cuenta e inicie sesión en _Admin_.

   ![[!DNL Authy] - iniciando sesión](./assets/storefront-2fa-authy-access.png){width="300"}

1. Elija uno de los siguientes métodos para autenticarse:

   - `Use one touch` — envía una alerta a su aplicación [!DNL Authy]. En la aplicación, acepte el acceso.
   - `Use authy token`: solicita escribir un código desde su aplicación [!DNL Authy].

1. Si tiene problemas para iniciar sesión, elija el método que desee utilizar para recibir el código. A continuación, escriba el código que recibirá para obtener acceso a _Admin_.

   La aplicación incluye estos métodos de emergencia adicionales.

   - `Send me a code via SMS`: se envía un mensaje SMS de texto al dispositivo móvil configurado.
   - `Send me a code via phone call`: el usuario recibe una llamada telefónica con un código.

   Su cuenta se verifica y abre.

## U2F ([!DNL Yubikey] y otros dispositivos)

Siga las instrucciones del proveedor de soluciones para configurar el dispositivo U2F. Para obtener más información, consulte la documentación del proveedor, como [[!DNL YubiKey]](https://support.yubico.com/hc/en-us/articles/360013790339-Getting-Started-with-Your-YubiKey) por [!UICONTROL Yubico].

1. Escriba las credenciales de su cuenta e inicie sesión en _Admin_.

   ![acceso a la clave U2F](./assets/storefront-2fa-u2f.png){width="300"}

1. Presione el botón de la tecla.

   La autenticación déclencheur inmediatamente y abre _Admin_.

1. Inserte **[!UICONTROL U2F key]** en un puerto USB del equipo.
