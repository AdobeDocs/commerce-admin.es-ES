---
title: Compartir un [!DNL Commerce] account
description: Obtenga información sobre cómo conceder acceso limitado a su [!DNL Commerce] cuenta para otros [!DNL Commerce] titulares de cuenta.
exl-id: adc4fed4-89f4-4b0c-811c-fcf6f94dbc22
feature: User Account
source-git-commit: ec634ebedd43b8bbc6b4a3e5079035b055740f2d
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---

# Compartir un [!DNL Commerce] account

Su [!DNL Commerce] La cuenta de contiene información que puede poner a disposición de empleados y proveedores de servicios de confianza que le ayudan a administrar el sitio. Como titular de la cuenta principal, tiene autoridad para conceder acceso limitado a otros [!DNL Commerce] titulares de cuenta. El acceso compartido se puede revocar, pero no se puede transferir de un usuario a otro.

El [!DNL Commerce] El equipo de asistencia no tiene acceso a la cuenta y no puede configurar el acceso compartido para usted. Solo el titular de la cuenta principal con los permisos adecuados puede configurar el acceso compartido. Al compartir el acceso a la cuenta, toda la información confidencial, como el historial de facturación o la información de la tarjeta de crédito, permanece protegida y nunca está disponible para otros usuarios.

>[!NOTE]
>
>Todas las acciones que realicen los usuarios con acceso compartido son responsabilidad exclusiva del titular de la cuenta principal. El Adobe de no se responsabiliza por las acciones realizadas por los usuarios que han compartido el acceso a su cuenta.

![Configuración de acceso compartido](./assets/shared-access.png){width="600" zoomable="yes"}

## Configuración de una cuenta compartida

1. Antes de empezar, obtenga la siguiente información de la [!DNL Commerce] cuenta de la **nuevo concesionario de acceso compartido**:

   - El usuario ya debe haberse registrado para obtener una cuenta en account.adobe.com y haber iniciado sesión a través de account.magento.com.
   - El `MAGE ID/Account ID (MAG00XXXXXXX)` se muestra en la esquina superior izquierda de la _[!UICONTROL Magento]_pestaña, justo encima de **Cerrar sesión**vínculo.
   - El `Email` dirección asociada a la cuenta.

1. Inicie sesión en su [[!DNL Commerce] account](commerce-account-create.md).

1. En el panel de navegación izquierdo, haga clic en **[!UICONTROL Shared Access]**.

1. Clic **[!UICONTROL Add New User]**.

   ![Añadir un nuevo usuario](./assets/shared-access-add.png){width="600" zoomable="yes"}

1. En [!UICONTROL _New User Information]_, haga lo siguiente:

   - Introduzca el **[!UICONTROL Account ID]** del nuevo usuario [!DNL Commerce] cuenta.
   - Introduzca el **[!UICONTROL Email]** dirección asociada a la del nuevo usuario [!DNL Commerce] cuenta.

   ![Nueva información de usuario](./assets/shared-new-user.png){width="600"}

1. En _[!UICONTROL Shared Information]_, haga lo siguiente:

   - Para identificar la cuenta compartida, introduzca un **[!UICONTROL Share Name]**. Este nombre es para referencia interna y solo es visible para usted y la persona con la que comparte su cuenta.

     Una práctica recomendada es utilizar el nombre de su organización como [!UICONTROL Share Name]. No utilice un nombre que comience por `CLOUD SHARED ACCESS FROM MAG XYX`.
   - Si desea compartir su información de contacto personal con el nuevo usuario, escriba **[!UICONTROL Your Email]** y **[!UICONTROL Your Phone]**.

1. En _[!UICONTROL Grant Account Permissions]_, seleccione la casilla de verificación de cada [!DNL Commerce] producto y servicio que desea compartir.

   ![Conceder permisos a la cuenta](./assets/shared-permissions.png){width="600"}

1. Clic **[!UICONTROL Create Shared Access]**.

   La nueva información del usuario aparece en la _[!UICONTROL Manage Permissions]_de la página Acceso compartido y se envía al nuevo usuario una invitación por correo electrónico con instrucciones para acceder a la cuenta compartida.

   ![Administración de permisos para acceso compartido](./assets/shared-manage-permissions.png){width="600" zoomable="yes"}

>[!NOTE]
>
>No es necesario compartir el acceso al _[!UICONTROL Security Tool]_: Cualquier usuario con un ID de MAGE puede configurar la herramienta de exploración de seguridad con su propia cuenta. Solo necesitan los privilegios necesarios para realizar cambios en el sitio y verificar la propiedad del dominio mediante uno de los [métodos necesarios](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security-scan)).

## Acceso a una cuenta compartida

Las siguientes instrucciones se escriben desde la perspectiva de un usuario compartido que recibe una invitación a una cuenta compartida.

1. Cuando reciba una invitación a una cuenta compartida, siga las instrucciones del correo electrónico para iniciar sesión en la suya propia [!DNL Commerce] cuenta.

   El panel de navegación izquierdo de su cuenta tiene un nuevo _[!UICONTROL Shared with me]_pestaña. El_[!UICONTROL Switch Accounts]_ el control de la esquina superior derecha tiene opciones para `My Account` y el nombre de la cuenta compartida.

   ![Compartido conmigo](./assets/shared-with-me.png){width="600" zoomable="yes"}

1. Para obtener acceso a la cuenta compartida, establezca **[!UICONTROL Switch Accounts]** al nombre de la cuenta compartida.

   ![Cambiar a la cuenta compartida](./assets/shared-switch.png){width="600" zoomable="yes"}

   La cuenta compartida muestra un mensaje de bienvenida e información de contacto. El panel de navegación izquierdo incluye sólo los elementos que tiene permiso para utilizar.

1. Para conectar la cuenta compartida al Centro de ayuda, haga clic en **[!UICONTROL Support]** en el panel de navegación izquierdo de la cuenta compartida.

   ![Asistencia](./assets/shared-support.png){width="600" zoomable="yes"}

   Puede usar el complemento [Centro de ayuda de Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview.html) desde la cuenta compartida para buscar artículos e información sobre resolución de problemas, buscar parches para problemas conocidos y crear vales de soporte.

   >[!NOTE]
   >
   >Después de recibir el acceso compartido, el usuario debe iniciar sesión en su [[!DNL Commerce] account](https://account.magento.com/customer/account/login), vaya a _Acceso compartido_ y haga clic en **[!UICONTROL Support]** pestaña. Esta acción solo es necesaria la primera vez para garantizar que la variable [Base de conocimiento de asistencia de Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview.html) se ha configurado correctamente mediante la variable `SSO` llamada.

1. Para volver a su propia cuenta, haga clic en **Atrás** en los controles del navegador y establezca **[!UICONTROL Switch Accounts]** hasta `My Account`.

## Revocar acceso compartido

1. Inicie sesión en su cuenta de Commerce.

1. En el panel de navegación izquierdo, haga clic en **[!UICONTROL Shared Access]**.

1. Busque la cuenta que desea revocar en _[!UICONTROL Managing Users & Permissions]_y haga clic en **[!UICONTROL Delete]**.

   >[!NOTE]
   >
   > If  **[!UICONTROL Delete]** no se muestra, compruebe si la variable **[!UICONTROL Share Name]** empieza por `Cloud Shared Access from MAG XYZ`. No puede eliminar cuentas con eso [patrón de nomenclatura](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users).
   > 
   > Si es así, pídale al propietario de la cuenta que modifique la cuenta de acceso compartido para borrar los permisos de la cuenta. Después de esta actualización, el usuario no podrá acceder a ningún recurso de la cuenta.
   >
   > Además, asegúrese de que los usuarios se eliminen del proyecto para que ya no reciban notificaciones por correo electrónico: [Los antiguos integrantes del equipo reciben correos electrónicos de notificación de Adobe Commerce Cloud](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails.html)


1. Cuando se le pida que confirme, haga clic en **[!UICONTROL Delete User]**.

>[!NOTE]
>
>No puede eliminar usuarios con el nombre compartido de _Acceso compartido en la nube desde MAG[XYZ]_ en esta interfaz. Consulte [¿Cómo eliminar a los usuarios a los que se les concedió acceso compartido a través de un proyecto de Cloud?](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#remove-cloud-shared-access-users).
