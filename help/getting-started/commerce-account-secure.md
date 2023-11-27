---
title: Proteja su [!DNL Commerce] account
description: Aprenda a utilizar la autenticación de doble factor para proteger su [!DNL Commerce] cuenta.
exl-id: 4847b5cb-a93a-40d0-8c31-c30afa27c0ce
feature: User Account
source-git-commit: fff3464c9da50927bbe9773a17b0f6858360d788
workflow-type: tm+mt
source-wordcount: '1688'
ht-degree: 0%

---

# Proteja su [!DNL Commerce] account

La autenticación de doble factor (TFA o 2FA) es una capa adicional de seguridad para proteger mejor su [!DNL Commerce] de acceso no autorizado. Para completar el proceso de inicio de sesión, TFA requiere un _segundo factor_ además del nombre de usuario y las credenciales de contraseña estándar. Este segundo factor adopta la forma de códigos de verificación temporales que se generan continuamente mediante una aplicación TFA instalada en su dispositivo móvil y emparejada con su [!DNL Commerce] cuenta.

Con TFA habilitado, su cuenta es más segura. Un usuario no autorizado no puede iniciar sesión a menos que tenga sus credenciales de nombre de usuario y contraseña (primer factor) y un código de verificación válido de la aplicación TFA en su dispositivo personal (segundo factor).

>[!NOTE]
>
>La autenticación de doble factor que protege al _Administrador_ de su tienda tiene una configuración separada. Para obtener más información, consulte [Autenticación de doble factor](../systems/security-two-factor-authentication.md).

## Antes de empezar

Para usar TFA, debes tener una aplicación TFA instalada en tu dispositivo personal (como tu smartphone, tablet, computadora). Hay muchos disponibles, pero algunas opciones populares y gratuitas incluyen:

- Google Authenticator (iOS, Android™, BlackBerry®)

- Autor (iOS, Android™)

- Microsoft® Authenticator (iOS, Android™, Windows Phone)

## Habilitar autenticación de doble factor

1. Inicie sesión en su [[!DNL Commerce] account][1]{:target=&quot;_blank&quot;}.

1. En el panel de navegación izquierdo, seleccione **[!UICONTROL Account Settings]**, y luego seleccione **[!UICONTROL Two-factor Authentication]**.

   ![Habilitar TFA](./assets/2fa-enable.png){width="600" zoomable="yes"}

1. Seleccionar **[!UICONTROL Enable]** para iniciar el proceso de configuración de autenticación de doble factor.

1. Introduzca el **[!UICONTROL Verification Code]** enviado a su correo electrónico y seleccione **[!UICONTROL Verify Code]** para continuar.

   ![Introduzca el código de verificación](./assets/2fA-verification-code-prompt.png){width="400"}

1. Abra la aplicación de autenticación de doble factor que descargó e instaló en su dispositivo personal.

1. En el [!UICONTROL SETUP TWO-FACTOR AUTHENTICATION] del formulario, utilice el **[!UICONTROL Setup Code]** para agregar Adobe Commerce a la aplicación TFA.

   ![Añadir Adobe Commerce a la aplicación TFA](./assets/commerce-account-2fa-setup-app.png){width="400"}

   Puede agregar el código escaneando el código QR usando la aplicación TFA o ingresándolo manualmente. Este código empareja su aplicación de TFA con su [!DNL Commerce] y permite a los permisos generar la aplicación TFA para generar códigos de verificación para el acceso seguro a la cuenta.

1. Complete la configuración.

   - En el [!UICONTROL SETUP TWO FACTOR-AUTHENTICATION] , introduzca el código de verificación desde la aplicación de autenticación de doble factor.

   - Seleccionar **[!UICONTROL Verify Code]**.

   >[!NOTE]
   >
   >Por motivos de seguridad, los códigos de verificación de la aplicación TFA caducan y se regeneran continuamente. **_Siempre_** utilice el código que se muestra actualmente.

1. Guarde el **[!UICONTROL Recovery Codes]** se presenta en un lugar seguro y accesible.

   ![Almacenar códigos de recuperación](./assets/commerce-account-2fa-store-recovery-codes.png){width="400"}

   Si no puede proporcionar un código de verificación al iniciar sesión en su [!DNL Commerce] Para recuperar el acceso a la cuenta, debe utilizar un código de recuperación.

   Cada código de recuperación solo se puede utilizar una vez, pero puede [generar](#generate-new-recovery-codes) nuevas. Los códigos de recuperación distinguen entre mayúsculas y minúsculas.

1. Seleccione la casilla de verificación de confirmación y seleccione **[!UICONTROL Submit]** para continuar.

1. Para asegurarse de que puede recuperar el acceso a su cuenta, introduzca un **[!UICONTROL Recovery Email]**.

   Esta dirección de correo electrónico es necesaria si no puede generar un código de verificación a partir de la aplicación de autenticación de doble factor y no tiene acceso a un código de recuperación generado previamente que no se utilice.

   Una vez cada 24 horas, puede generar y enviar un código de recuperación temporal a la dirección de correo electrónico de recuperación designada. Utilice este código para recuperar el acceso a la cuenta.

   >[!IMPORTANT]
   >
   >Mantenga el acceso a su cuenta de correo electrónico de recuperación. De lo contrario, no podrá utilizar los códigos de recuperación temporales enviados a esa cuenta.

   ![Establecer correo electrónico de recuperación](./assets/commerce-account-2fa-set-recovery-email.png){width="400"}

1. Seleccione la casilla de verificación de confirmación y seleccione **[!UICONTROL Submit]** para completar el proceso de configuración de autenticación de doble factor.

   - Se envía una notificación a la dirección de correo electrónico asociada con su [!DNL Commerce] cuenta para confirmar que ha habilitado correctamente la autenticación de doble factor.

   - Se envía una notificación a la cuenta de correo electrónico de recuperación para confirmar la configuración.

>[!TIP]
>
>Si pierde su dispositivo personal o consigue uno nuevo, puede [cambie su aplicación de autenticación de doble factor](#change-your-two-factor-authentication-application) y generar nuevos códigos de recuperación.

## Iniciar sesión con un código de verificación

1. Vaya a la [!DNL Commerce] [inicio de sesión de cuenta][1]{:target=&quot;_blank&quot;}.

1. Introduzca las credenciales de nombre de usuario y contraseña y, a continuación, seleccione **[!UICONTROL Login]**.

1. Introduzca el **[!UICONTROL Verification Code]** se muestra en la aplicación de autenticación de doble factor cuando se le solicita.

   ![Introducir código de verificación](./assets/commerce-account-2fa-login-verification-code.png){width="600"}

1. Seleccionar **[!UICONTROL Submit]** para completar el proceso de inicio de sesión.

## Inicie sesión con un código de recuperación

1. Vaya a la [!DNL Commerce] [inicio de sesión de cuenta][1]{:target=&quot;_blank&quot;}.

1. Introduzca las credenciales de nombre de usuario y contraseña y, a continuación, seleccione **[!UICONTROL Login]**.

1. Seleccionar **[!UICONTROL Use recovery code]** para omitir el símbolo del sistema del código de verificación.

1. Introducir un no utilizado **[!UICONTROL Recovery Code]** cuando se le solicite.

   ![Introducir código de recuperación](./assets/2fa-recovery-code.png){width="600"}

1. Seleccionar **[!UICONTROL Submit]** para completar el proceso de inicio de sesión.

## Inicie sesión con el correo electrónico de recuperación

1. Inicie sesión en su [[!DNL Commerce] account][1]{:target=&quot;_blank&quot;}.

1. Introduzca las credenciales de nombre de usuario y contraseña y, a continuación, seleccione **[!UICONTROL Login]**.

1. Seleccionar **[!UICONTROL Use recovery code]** para omitir el símbolo del sistema del código de verificación.

1. Para obtener un código de recuperación temporal por correo electrónico, seleccione la **[!UICONTROL recovery email]** vínculo.

   ![Usar correo electrónico de recuperación](./assets/2fa-recovery-email.png){width="600"}

1. Abra la cuenta de correo electrónico de recuperación para obtener el código temporal y, a continuación, introduzca el código en los campos designados.

1. Seleccionar **[!UICONTROL Submit]** para completar el proceso de inicio de sesión.

Después de usar un código de recuperación temporal para acceder a su cuenta, [generar nuevos códigos de recuperación](#generate-new-recovery-codes) y guárdelos para evitar más problemas de acceso a la cuenta.

## Ver los códigos de recuperación

1. Vaya a la [!DNL Commerce] [inicio de sesión de cuenta][1]{:target=&quot;_blank&quot;}.

1. Introduzca las credenciales de nombre de usuario y contraseña y, a continuación, seleccione **[!UICONTROL Login]**.

1. Complete el proceso de inicio de sesión utilizando uno de los métodos de autenticación de doble factor descritos anteriormente.

1. En el panel de navegación izquierdo, seleccione **[!UICONTROL Account Settings]**, y luego seleccione **[!UICONTROL Two-factor Authentication]**.

   ![Configuración de 2FA](./assets/commerce-account-2fa-manage.png){width="600" zoomable="yes"}

1. Para ver los códigos de recuperación generados previamente, seleccione **Ver códigos de recuperación**.

1. Introduzca el **[!UICONTROL Verification Code]** enviado a su correo electrónico y seleccione **[!UICONTROL Verify Code]** para continuar.

   ![Introducir código de verificación](./assets/2fA-verification-code-prompt.png){width="400"}

1. Guarde el **Códigos de recuperación** se presenta en un lugar seguro y accesible.

   Si no puede proporcionar un código de verificación para iniciar sesión en su [!DNL Commerce] Cuenta de, el uso de un código de recuperación es la única manera de recuperar el acceso a la cuenta.

   Cada código de recuperación es de un solo uso, pero siempre puede [generar](#generate-new-recovery-codes) nuevas. Los códigos de recuperación distinguen entre mayúsculas y minúsculas.

   ![Ver códigos de recuperación](./assets/2fa-view-recovery.png){width="400"}

1. Seleccione la casilla de verificación de confirmación y seleccione **[!UICONTROL Submit]** para cerrar el cuadro de diálogo.

## Generar nuevos códigos de recuperación

1. Vaya a la [!DNL Commerce] [inicio de sesión de cuenta][1]{:target=&quot;_blank&quot;}.

1. Introduzca las credenciales de nombre de usuario y contraseña y, a continuación, seleccione **[!UICONTROL Login]**.

1. Complete el proceso de inicio de sesión utilizando uno de los métodos de autenticación de doble factor descritos anteriormente.

1. En el panel de navegación izquierdo, seleccione **[!UICONTROL Account Settings]**, y luego seleccione **[!UICONTROL Two-factor Authentication]**.

1. Para generar nuevos códigos de recuperación generados previamente, seleccione **Generar nuevos códigos de recuperación**.

1. Introduzca el **[!UICONTROL Verification Code]** enviado a su correo electrónico y seleccione **[!UICONTROL Verify Code]** para continuar.

1. Guarde el **Códigos de recuperación** se presenta en un lugar seguro y accesible.

   Si no puede proporcionar un código de verificación al iniciar sesión en su [!DNL Commerce] Cuenta de, el uso de un código de recuperación es la única manera de recuperar el acceso a la cuenta.

   Todos los códigos de recuperación generados anteriormente ahora se representan como no válidos y deben descartarse (solo funciona el conjunto actual de códigos de recuperación generados). Los códigos de recuperación distinguen entre mayúsculas y minúsculas.

1. Seleccione la casilla de verificación de confirmación y seleccione **[!UICONTROL Submit]** para cerrar el cuadro de diálogo.

## Cambiar el correo electrónico de recuperación

1. Vaya a la [!DNL Commerce] [inicio de sesión de cuenta][1]{:target=&quot;_blank&quot;}.

1. Introduzca las credenciales de nombre de usuario y contraseña y, a continuación, seleccione **[!UICONTROL Login]**.

1. Complete el proceso de inicio de sesión utilizando uno de los métodos de autenticación de doble factor descritos anteriormente.

1. En el panel de navegación izquierdo, seleccione **[!UICONTROL Account Settings]**, y luego seleccione **[!UICONTROL Two-factor Authentication]**.

1. Seleccionar **Cambiar correo electrónico de recuperación** para cambiar el correo electrónico de recuperación registrado en la cuenta.

1. Introduzca el **[!UICONTROL Verification Code]** enviado a su correo electrónico y seleccione **[!UICONTROL Verify Code]** para continuar.

1. Para garantizar que puede recuperar el acceso a su cuenta, escriba un **Correo electrónico de recuperación**.

   Esta dirección de correo electrónico es necesaria si no puede generar un código de verificación a partir de la aplicación de autenticación de doble factor y no tiene acceso a un código de recuperación generado previamente que no se utilice.

   Una vez cada 24 horas, puede generar y enviar un código de recuperación temporal a la dirección de correo electrónico de recuperación designada. Puede utilizar este código para recuperar el acceso a la cuenta.

   >[!IMPORTANT]
   >
   >Mantenga el acceso a su cuenta de correo electrónico de recuperación. De lo contrario, no podrá utilizar los códigos de recuperación temporales enviados a esa cuenta.

1. Seleccione la casilla de verificación de confirmación y seleccione **[!UICONTROL Submit]** para cerrar el cuadro de diálogo.

   El sistema envía una notificación por correo electrónico al correo electrónico de recuperación que designó para confirmar que esa dirección de correo electrónico concreta está archivada como correo electrónico de recuperación para recibir códigos de recuperación temporales.

## Cambiar la aplicación de autenticación de doble factor

1. Vaya a la [!DNL Commerce] [inicio de sesión de cuenta][1]{:target=&quot;_blank&quot;}.

1. Introduzca las credenciales de nombre de usuario y contraseña y, a continuación, seleccione **[!UICONTROL Login]**.

1. Complete el proceso de inicio de sesión utilizando uno de los métodos de autenticación de doble factor descritos anteriormente.

1. En el panel de navegación izquierdo, seleccione **[!UICONTROL Account Settings]**, y luego seleccione **[!UICONTROL Two-factor Authentication]**.

1. Seleccionar **Cambiar aplicación de TFA** para utilizar una aplicación TFA diferente con su cuenta magento.com.

1. Introduzca el **[!UICONTROL Verification Code]** enviado a su correo electrónico y seleccione **[!UICONTROL Verify Code]** para continuar.

1. Abra la aplicación de autenticación de doble factor en su dispositivo personal.

1. Introduzca el **Código de configuración** en la aplicación de autenticación de doble factor.

   Puede añadir el código escaneando el código QR usando la aplicación TFA o introduciéndolo manualmente. Este código empareja su aplicación de TFA con su [!DNL Commerce] y habilita los permisos para que la aplicación TFA genere códigos de verificación para el acceso seguro a la cuenta.

   >[!NOTE]
   >
   >Por motivos de seguridad, los códigos de verificación de la aplicación TFA caducan y se regeneran continuamente. **_Siempre_** utilice el código que se muestra actualmente.

1. Con la aplicación TFA ahora asociada con su [!DNL Commerce] cuenta, introduzca el **[!UICONTROL Verification Code]** se muestra en la aplicación TFA y seleccione **[!UICONTROL Verify Code]** para continuar.

1. Guarde el **Códigos de recuperación** se presenta en un lugar seguro y accesible.

   Si no puede proporcionar un código de verificación al iniciar sesión en su [!DNL Commerce] cuenta, la única manera de recuperar el acceso a la cuenta es utilizar un código de recuperación.

   Cada código de recuperación es de un solo uso, pero siempre puede [generar](#generate-new-recovery-codes) nuevas. Los códigos de recuperación distinguen entre mayúsculas y minúsculas. Los códigos de recuperación distinguen entre mayúsculas y minúsculas.

1. Seleccione la casilla de verificación para confirmar y seleccionar **[!UICONTROL Submit]** para continuar.

1. Para garantizar que puede recuperar el acceso a su cuenta, escriba un **Correo electrónico de recuperación**.

   Esta dirección de correo electrónico es necesaria si no puede generar un código de verificación a partir de la aplicación de autenticación de doble factor y no tiene acceso a un código de recuperación generado previamente que no se utilice.

   Una vez cada 24 horas, puede generar y enviar un código de recuperación temporal a la dirección de correo electrónico de recuperación designada. Utilice este código para recuperar el acceso a la cuenta.

   >[!IMPORTANT]
   >
   >Mantenga el acceso a su cuenta de correo electrónico de recuperación. De lo contrario, no podrá utilizar los códigos de recuperación temporales enviados a esa cuenta.

1. Seleccione la casilla de verificación de confirmación y seleccione **[!UICONTROL Submit]** para completar el proceso de configuración de autenticación de doble factor.

   Se envía una notificación por correo electrónico al correo electrónico de recuperación que designó para confirmar que una dirección de correo electrónico en particular está archivada como correo electrónico de recuperación para recibir un código de recuperación temporal.

## Deshabilitar la autenticación de doble factor

>[!IMPORTANT]
>
>Si la directiva de seguridad de la organización requiere autenticación multifactor en las cuentas de Adobe Commerce, no puede deshabilitar la autenticación de doble factor.

1. Vaya a la [!DNL Commerce] [inicio de sesión de cuenta][1]{:target=&quot;_blank&quot;}.

1. Introduzca las credenciales de nombre de usuario y contraseña y, a continuación, seleccione **[!UICONTROL Login]**.

1. Complete el proceso de inicio de sesión utilizando uno de los métodos de autenticación de doble factor descritos anteriormente.

1. En el panel de navegación izquierdo, seleccione **[!UICONTROL Account Settings]** y seleccione **[!UICONTROL Two-factor Authentication]** debajo.

1. Seleccionar **[!UICONTROL Disable]** para comenzar el proceso de desactivación de TFA.

1. Introduzca el **[!UICONTROL Verification Code]** enviado a su correo electrónico y seleccione **[!UICONTROL Verify Code]** para continuar.

1. Seleccione la casilla de verificación de confirmación y seleccione **[!UICONTROL Submit]** para completar la desactivación para la autenticación de doble factor.

   El sistema envía un correo electrónico de confirmación indicando que TFA se ha desactivado en su [!DNL Commerce] cuenta.

   ![Deshabilitar TFA](./assets/2fa-disable.png){width="400"}

[1]: https://account.magento.com/customer/account/login
