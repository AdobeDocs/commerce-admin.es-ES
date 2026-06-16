---
title: Inicio de sesión del cliente
description: La función de inicio de sesión del cliente en la tienda permite un fácil acceso a las cuentas de los clientes.
exl-id: eadcc15a-a052-4213-a818-d5b248d974d2
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/WuMuGVXByzb0PlpkKHnJCT-s7ToHtb1odvTu18LxB-I
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 383
ht-degree: 0%

---

# Inicio de sesión del cliente

Los clientes tienen fácil acceso a sus cuentas desde todas las páginas de su tienda. Según la [configuración](../customers/account-options-new.md), los clientes pueden ser redirigidos a su panel de cuentas o seguir comprando después de iniciar sesión en sus cuentas.

Si [CAPTCHA](../systems/security-captcha.md) está habilitado en la configuración, la persona debe completar correctamente una prueba que verifique que es humana antes de obtener acceso a sus cuentas.

Cuando los clientes olvidan sus contraseñas, se envía un vínculo de restablecimiento a la dirección de correo electrónico asociada a la cuenta. La configuración de [Opciones de contraseña](../customers/password-options.md) controla la experiencia del cliente en los intentos de inicio de sesión:

- El número de veces que un cliente puede intentar introducir una contraseña
- El número de minutos entre intentos
- Número total de intentos antes de bloquear la cuenta
- La duración del bloqueo

![Vínculo de inicio de sesión en el encabezado de la tienda](assets/storefront-sign-in-create-account.png){width="700" zoomable="yes"}

## Iniciar sesión en una cuenta de cliente

1. En el encabezado de la tienda, el cliente hace clic en **[!UICONTROL Sign in]**.

   ![Inicio de sesión de cliente](assets/login.png){width="700" zoomable="yes"}

1. Escribe su dirección **[!UICONTROL Email]** y **[!UICONTROL Password]**.

1. Clics **[!UICONTROL Sign in]**.

   >[!IMPORTANT]
   >
   >Si no puede recordar su contraseña, el cliente puede hacer clic en **[!UICONTROL Forgot Your Password?]** y seguir las [instrucciones](../customers/password-reset.md) para restablecer la contraseña.

## Establezca el redireccionamiento al tablero de cuentas después del inicio de sesión del cliente

Puede configurar la tienda para redirigir a los clientes a su panel de cuentas después de que inicien sesión o para que puedan seguir comprando.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Customer Configuration]**.

1. Expanda la sección **[!UICONTROL Login Options]**.

1. Establezca **[!UICONTROL Redirect Customer to Account Dashboard after Logging in]** en una de las siguientes opciones:

   - `Yes`: el tablero de cuentas aparece cuando los clientes inician sesión en sus cuentas.
   - `No`: los clientes pueden seguir comprando después de iniciar sesión en sus cuentas.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Iniciar sesión con Amazon

En las tiendas con una integración configurada de [!DNL Amazon Pay] y [!DNL Login with Amazon], los clientes pueden iniciar sesión en su cuenta de comprador de Amazon.

1. En el encabezado de la tienda, el cliente hace clic en **[!UICONTROL Sign in]**.

1. Clics **[!UICONTROL Login with Amazon]**.

   ![Iniciar sesión con Amazon](assets/amazon-pay.png){width="700" zoomable="yes"}

1. Cuando se le pide que inicie sesión, el cliente introduce **[!UICONTROL email address]** y **[!UICONTROL password]** para su cuenta de comprador de Amazon.

   ![Introduciendo credenciales de Amazon](assets/amazon-popup1.png){width="700" zoomable="yes"}

1. Para conceder permiso a Amazon para compartir la siguiente información de su cuenta con la tienda al procesar las compras, haz clic en **Aceptar**.

   - Nombre
   - Correo electrónico
   - Direcciones de envío

   ![Conceder permiso para compartir datos](assets/amazon-popup2.png){width="700" zoomable="yes"}

## Cerrar sesión en una cuenta de cliente

1. En la esquina superior derecha junto a _[!UICONTROL Welcome, Customer Name!]_, el cliente hace clic en el selector de menú&#x200B;**[!UICONTROL v]**.

1. Elija **[!UICONTROL Sign Out]**.

Después de cerrar la sesión, se redirige al cliente a la página principal.
