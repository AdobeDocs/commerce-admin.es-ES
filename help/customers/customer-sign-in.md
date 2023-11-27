---
title: Inicio de sesión del cliente
description: La función de inicio de sesión del cliente en la tienda permite un fácil acceso a las cuentas de los clientes.
exl-id: eadcc15a-a052-4213-a818-d5b248d974d2
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Inicio de sesión del cliente

Los clientes tienen fácil acceso a sus cuentas desde todas las páginas de su tienda. Según la variable [configuración](../customers/account-options-new.md)Por lo tanto, los clientes pueden ser redirigidos a su panel de cuentas o continuar comprando después de iniciar sesión en sus cuentas.

If [CAPTCHA](../systems/security-captcha.md) está habilitado en la configuración de, la persona debe completar correctamente una prueba que verifique que es humana antes de obtener acceso a sus cuentas.

Cuando los clientes olvidan sus contraseñas, se envía un vínculo de restablecimiento a la dirección de correo electrónico asociada a la cuenta. El [Opciones de contraseña](../customers/password-options.md) controla la experiencia del cliente en los intentos de inicio de sesión:

- El número de veces que un cliente puede intentar introducir una contraseña
- El número de minutos entre intentos
- Número total de intentos antes de bloquear la cuenta
- La duración del bloqueo

![Vínculo de inicio de sesión en el encabezado de la tienda](assets/storefront-sign-in-create-account.png){width="700" zoomable="yes"}

## Iniciar sesión en una cuenta de cliente

1. En el encabezado de la tienda, el cliente hace clic en **[!UICONTROL Sign in]**.

   ![Inicio de sesión del cliente](assets/login.png){width="700" zoomable="yes"}

1. Introduce su **[!UICONTROL Email]** dirección y **[!UICONTROL Password]**.

1. Clics **[!UICONTROL Sign in]**.

   >[!IMPORTANT]
   >
   >Si no puede recordar su contraseña, el cliente puede hacer clic en **[!UICONTROL Forgot Your Password?]** y siga las [instrucciones](../customers/password-reset.md) para restablecer la contraseña.

## Establezca el redireccionamiento al tablero de cuentas después del inicio de sesión del cliente

Puede configurar la tienda para redirigir a los clientes a su panel de cuentas después de que inicien sesión o para que puedan seguir comprando.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Customer Configuration]**.

1. Expanda el **[!UICONTROL Login Options]** sección.

1. Establecer **[!UICONTROL Redirect Customer to Account Dashboard after Logging in]** a uno de los siguientes:

   - `Yes` : El panel de cuentas aparece cuando los clientes inician sesión en sus cuentas.
   - `No` : Los clientes pueden seguir comprando después de iniciar sesión en sus cuentas.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Iniciar sesión con Amazon

Para tiendas con un configurado [!DNL Amazon Pay] y [!DNL Login with Amazon] integración, los clientes pueden iniciar sesión en su cuenta de comprador de Amazon.

1. En el encabezado de la tienda, el cliente hace clic en **[!UICONTROL Sign in]**.

1. Clics **[!UICONTROL Login with Amazon]**.

   ![Iniciar sesión con Amazon](assets/amazon-pay.png){width="700" zoomable="yes"}

1. Cuando se le solicita que inicie sesión, el cliente introduce el **[!UICONTROL email address]** y **[!UICONTROL password]** para su cuenta de comprador de Amazon.

   ![Introducción de credenciales de Amazon](assets/amazon-popup1.png){width="700" zoomable="yes"}

1. Para conceder permiso a Amazon para compartir la siguiente información de su cuenta con la tienda al procesar las compras, haga clic en **Okay**.

   - Nombre
   - Correo electrónico
   - Direcciones de envío

   ![Conceder permiso para compartir datos](assets/amazon-popup2.png){width="700" zoomable="yes"}

## Cerrar sesión en una cuenta de cliente

1. En la esquina superior derecha junto a  _[!UICONTROL Welcome, Customer Name!]_, el cliente hace clic en **[!UICONTROL v]**selector de menú.

1. Elegir **[!UICONTROL Sign Out]**.

Después de cerrar la sesión, se redirige al cliente a la página principal.
