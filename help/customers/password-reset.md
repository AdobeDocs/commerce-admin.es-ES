---
title: Restablecer contraseñas de cliente
description: Los clientes suelen restablecer sus contraseñas desde la tienda, pero un administrador de la tienda puede iniciar un restablecimiento de contraseña o un inicio de sesión forzado desde el administrador.
exl-id: bca1ef3e-2bc6-4146-ac86-d6c58c8995e4
feature: Customers, Configuration, Security
TQID: https://experienceleague.adobe.com/yzGC0T8unOSE-sZkE4PRHM6xMVX68qD6fARb-OSUB0U
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
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 393
ht-degree: 0%

---

# Restablecer contraseñas de cliente

Los clientes suelen restablecer sus contraseñas desde la tienda haciendo clic en _[!UICONTROL Forgot Your Password?]_. Sin embargo, el administrador del almacén puede iniciar un restablecimiento de contraseña o un inicio de sesión forzado desde el administrador.

| Función | Descripción |
| --- | --- |
| Restablecer contraseña | Se envía un correo electrónico de restablecimiento de contraseña directamente a la cuenta de correo electrónico del cliente. El administrador del almacén no puede obtener acceso a la contraseña del cliente. |
| Forzar inicio de sesión | Revoca los tokens de acceso de OAuth asociados a la cuenta del cliente. Esto solo se puede usar con cuentas de cliente a las que se les hayan asignado tokens de OAuth, como parte de una integración de API web [integration](../systems/integrations.md). Para obtener más información, consulte [Autenticación basada en OAuth](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) en la documentación para desarrolladores. <br/><br/>Las cuentas de cliente estándar creadas desde la tienda o desde el administrador no tienen tokens de OAuth. |

{style="table-layout:auto"}

## Restablecer una contraseña desde la tienda

1. En la página de inicio de sesión, el cliente hace clic en **[!UICONTROL Forgot Your Password?]**.

1. Cuando se le solicite, escribe **[!UICONTROL Email Address]** que está asociado con su cuenta y hace clic en **[!UICONTROL Reset My Password]**.

   ![Olvidé su contraseña](assets/forgot-password.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >Si la dirección de correo electrónico introducida coincide con la asociada a la cuenta, el cliente recibe un correo electrónico de confirmación de restablecimiento de contraseña con un vínculo para restablecer su contraseña.

1. Cuando llega el correo electrónico, el cliente hace clic en el vínculo _restablecer contraseña_ e introduce su **[!UICONTROL New Password]** cuando se le solicita.

1. Vuelve a escribirlo para confirmar y hace clic en **[!UICONTROL Reset Password]**.

   >[!IMPORTANT]
   >
   >La nueva contraseña debe tener seis o más caracteres de longitud sin espacios. Cuando reciban la confirmación de que la contraseña se ha actualizado, podrán utilizar la nueva contraseña para iniciar sesión en su cuenta. De manera predeterminada, el vínculo _restablecer contraseña_ es válido durante 24 horas.

## Restablecer una contraseña desde el administrador

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Busque la cuenta de cliente en la cuadrícula y haga clic en **[!UICONTROL Edit]** en la columna _Acción_.

1. En el conjunto de opciones de la parte superior de la página, haga clic en **[!UICONTROL Reset Password]**.

   El número de solicitudes de restablecimiento de contraseña permitidas en una hora se establece en el tema [configuración](../configuration-reference/customers/customer-configuration.md).

## Revocar tokens de OAuth de un cliente

>[!IMPORTANT]
>
>No continúe a menos que tenga una comprensión completa de la autenticación de API.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Busque la cuenta de cliente en la cuadrícula y haga clic en **[!UICONTROL Edit]** en la columna _Acción_.

1. En el conjunto de opciones de la parte superior de la página, haga clic en **[!UICONTROL Force Sign In]**.

1. Cuando se le pida que confirme, haga clic en **Aceptar**.
