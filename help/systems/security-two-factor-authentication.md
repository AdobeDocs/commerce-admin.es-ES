---
title: Autenticación de doble factor (2FA)
description: Obtenga información acerca de la compatibilidad con la autenticación de doble factor para garantizar la seguridad del sistema y de los datos.
exl-id: d9eb3dd6-4a7b-411a-ac08-0441803cd59a
role: Admin
feature: Configuration, Security, User Account
source-git-commit: c391a3eef8be0dd45cc8a499b63bcb0fc32640aa
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 0%

---

# Autenticación de doble factor (2FA)

El Commerce _Administrador_ para la instalación de Adobe Commerce o Magento Open Source que proporciona acceso a su tienda, pedidos y datos de clientes. Para evitar el acceso no autorizado a sus datos, seleccione todos los usuarios que intenten iniciar sesión en _Administrador_ debe completar un proceso de autenticación para verificar su identidad.

>[!NOTE]
>
>Esta implementación de la autenticación de doble factor (2FA) se aplica al _Administrador_ solo, y no está disponible para cuentas de cliente. La autenticación de doble factor que protege su cuenta de Commerce tiene una configuración independiente. Para obtener más información, vaya a [Proteja su cuenta de Commerce](../getting-started/commerce-account-secure.md).

La autenticación de doble factor se utiliza ampliamente y es común generar códigos de acceso para diferentes sitios web en la misma aplicación. Esta autenticación adicional garantiza que solo usted pueda iniciar sesión en su cuenta de usuario. Si pierde la contraseña o un bot la adivina, la autenticación de doble factor agrega una capa de protección. Por ejemplo, puede utilizar Google Authenticator para generar códigos para el administrador de su tienda, su cuenta de Commerce y la cuenta de Google.

![Configuración de seguridad para iphone - 2FA](./assets/google-authenticator-iphone.png){width="300"}

Adobe Commerce admite métodos 2FA de varios proveedores. Algunos requieren la instalación de una aplicación que genere una contraseña de un solo uso (OTP) que los usuarios introduzcan al iniciar sesión para verificar su identidad. Los dispositivos de segundo factor universal (U2F) se parecen a un llavero y generan una clave única para verificar la identidad. Otros dispositivos verifican la identidad cuando se insertan en un puerto USB. Como administrador del almacén, puede requerir uno o más de los métodos 2FA disponibles para verificar la identidad del usuario. La configuración de 2FA se aplica a todos los sitios web y tiendas asociados con la instalación de Adobe Commerce.

La primera vez que un usuario inicia sesión en _Administrador_, deben configurar cada [2FA](../configuration-reference/security/2fa.md) método que necesita y compruebe su identidad mediante la aplicación o el dispositivo asociado. Después de esta configuración inicial, el usuario debe autenticarse con uno de los métodos configurados cada vez que inicia sesión. La información 2FA de cada usuario se registra en su _Administrador_ cuenta y se puede [restablecer](security-two-factor-authentication-manage.md) si es necesario. Para obtener más información sobre el proceso de inicio de sesión, vaya a [_Administrador_ Iniciar sesión](../getting-started/admin-signin.md).

>[!NOTE]
>
>Las tiendas que han habilitado la autenticación de Adobe Identity Management Services (IMS) tienen Adobe Commerce nativo y el Magento Open Source 2FA deshabilitado. Los usuarios administradores que han iniciado sesión en su instancia de Commerce con sus credenciales de Adobe no necesitan volver a autenticarse en muchas tareas de administración. La autenticación la gestiona Adobe IMS cuando el usuario administrador inicia sesión en su sesión actual. Consulte [Información general sobre la integración de Adobe Identity Management Service (IMS)](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

Puedes ver esto [demostración en vídeo](https://video.tv.adobe.com/v/339104?quality=12&learn=on) para obtener una descripción general de la autenticación de doble factor en el administrador.

## Configure los proveedores 2FA necesarios

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Security]** y elija **[!UICONTROL 2FA]**.

1. En el _[!UICONTROL General]_, seleccione los proveedores que desea utilizar.

   | Proveedor | Función |
   |--- |--- |
   | [!UICONTROL Google Authenticator] | Genera una contraseña de un solo uso en la aplicación para la autenticación de usuarios. |
   | [!UICONTROL Duo Security] | Proporciona notificaciones push y SMS. |
   | [!UICONTROL Authy] | Genera un código de seis dígitos dependiente del tiempo y ofrece protección o token SMS o de llamada de voz 2FA. |
   | [!UICONTROL U2F Devices (Yubikey and others)] | Utiliza un dispositivo físico para autenticarse, como [[!DNL YubiKey]](https://www.yubico.com/). |

   Para seleccionar varios métodos, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada elemento.

1. Complete la configuración de cada método 2FA requerido.

   ![Configuración de seguridad: 2FA](../configuration-reference/security/assets/2fa-general.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

   La primera vez que los usuarios inicien sesión en _Administrador_, deben configurar cada método 2FA requerido. Después de esta configuración inicial, deben autenticarse con uno de los métodos configurados cada vez que inician sesión.

## Configuración de proveedor 2FA

Complete la configuración de cada método 2FA que necesite.

### Google

Para cambiar la duración de la disponibilidad de la contraseña de un solo uso (OTP) durante el inicio de sesión, borre la etiqueta **[!UICONTROL Use system value]** casilla de verificación A continuación, introduzca el número de segundos que desea que dure la **[!UICONTROL OTP Window]** para que sea válido.

>[!NOTE]
>
>En Adobe Commerce 2.4.7 y versiones posteriores, el ajuste de configuración de la ventana OTP controla cuánto tiempo (en segundos) acepta el sistema una contraseña única (OTP) de un administrador una vez caducada. Este valor debe ser inferior a 30 segundos. La configuración predeterminada del sistema es `1`.<br><br> En la versión 2.4.6, la configuración de la ventana OTP determina el número de códigos OTP pasados y futuros que siguen siendo válidos. Un valor de `1` indica que el código OTP actual más un código en el pasado y un código en el futuro siguen siendo válidos en cualquier momento.

### [!DNL Duo Security]

Introduzca las siguientes credenciales de su cuenta de Duo Security:

- Clave de integración
- Clave secreta
- Nombre de host API

![Configuración de seguridad: Duo](../configuration-reference/security/assets/2fa-duo-security.png){width="600" zoomable="yes"}

### [!DNL Authy]

1. Introduzca la clave de API desde la [!DNL Authy] cuenta.

1. Para cambiar el mensaje predeterminado que aparece durante la autenticación, borre la **[!UICONTROL Use system value]** casilla de verificación A continuación, introduzca la variable **[!UICONTROL OneTouch Message]** que desea que aparezca.

   ![Configuración de seguridad: autoridad](../configuration-reference/security/assets/2fa-authy.png){width="600" zoomable="yes"}

### Dispositivos U2F ([!DNL Yubikey] y otros)

El dominio de almacén se utiliza de forma predeterminada durante el proceso de autenticación. Para utilizar un dominio personalizado para los desafíos de autenticación, borre la **[!UICONTROL Use system value]** casilla de verificación A continuación, introduzca la variable **[!UICONTROL WebAPi Challenge Domain]**.

![Configuración de seguridad - Dispositivos U2F](../configuration-reference/security/assets/2fa-u2f-key.png){width="600" zoomable="yes"}
