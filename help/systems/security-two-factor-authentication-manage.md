---
title: Administración de la autenticación de doble factor
description: Obtenga información sobre cómo administrar la autenticación de doble factor y restablecer los autenticadores para los usuarios administradores.
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# Administración de la autenticación de doble factor

Los usuarios que no puedan iniciar sesión en _Admin_ con autenticación de doble factor (2FA) pueden intentar sincronizar o solucionar el problema. También puede restablecer los autenticadores asociados con la cuenta. Cuando se restablece, el usuario debe volver a iniciar sesión y volver a configurar los autenticadores necesarios.

Si tiene problemas para iniciar sesión con 2FA, tenga en cuenta lo siguiente:

- Algunas aplicaciones móviles incluyen opciones de sincronización. Esta opción vuelve a conectar la aplicación y el servidor y sincroniza la configuración horaria del dispositivo y el servidor.
- Revocar un dispositivo o restablecer un autenticador puede ayudar a los usuarios a conectarse.
- Borrar la caché web y las cookies para la instalación de Adobe Commerce o Magento Open Source también puede ayudar. Los autenticadores, como Google, utilizan cookies generadas para guardar el acceso y la duración. Borre las cookies de su explorador específico y almacene el dominio.
- Bloquear cookies impide que algunos autenticadores, como [!DNL Google Authenticator], completen el proceso de verificación. Agregue a su explorador una regla que permita las cookies para la instalación de Adobe Commerce.

Para restablecer los autenticadores desde la línea de comandos y obtener información más avanzada sobre solución de problemas, consulte [Autenticación de doble factor](https://developer.adobe.com/commerce/testing/functional-testing-framework/two-factor-authentication/) en la documentación para desarrolladores.

**_Para restablecer los autenticadores de una cuenta de usuario:_**

>[!NOTE]
>
>Para restablecer los proveedores de 2FA para otros usuarios, debe ser un _administrador_ con `All` permisos o tener `Custom` permisos para su rol con [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth] y [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users] seleccionados. Para obtener más información, consulte [Funciones de usuario](permissions-user-roles.md).

1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Seleccione el usuario y abra la cuenta en modo de edición.

1. Desplácese hacia abajo hasta la sección _[!UICONTROL Current User Identity Verification]_&#x200B;e introduzca su contraseña.

1. En el panel izquierdo, haga clic en **[!UICONTROL 2FA]**.

1. En la sección _[!UICONTROL Configuration reset]_, haga clic en **[!UICONTROL Reset]**&#x200B;y **[!UICONTROL OK]**&#x200B;para confirmar.

   ![Cuenta de usuario - habilitar 2FA](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}

   Si el usuario desea restaurar los métodos 2FA necesarios en su cuenta, debe volver a configurar cada uno desde la página _Iniciar sesión_.

1. Una vez finalizado, haga clic en **[!UICONTROL Save User]**.
