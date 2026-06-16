---
title: Administración de la autenticación de doble factor
description: Obtenga información sobre cómo administrar la autenticación de doble factor y restablecer los autenticadores para los usuarios administradores.
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
TQID: https://experienceleague.adobe.com/aE-36667-f0E4GSXDjZZmFUkS3wa-xTLUMbVtjwS6qk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 336
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

1. Desplácese hacia abajo hasta la sección _[!UICONTROL Current User Identity Verification]_e introduzca su contraseña.

1. En el panel izquierdo, haga clic en **[!UICONTROL 2FA]**.

1. En la sección _[!UICONTROL Configuration reset]_, haga clic en **[!UICONTROL Reset]**y **[!UICONTROL OK]**para confirmar.

   ![Cuenta de usuario - habilitar 2FA](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}

   Si el usuario desea restaurar los métodos 2FA necesarios en su cuenta, debe volver a configurar cada uno desde la página _Iniciar sesión_.

1. Una vez finalizado, haga clic en **[!UICONTROL Save User]**.
