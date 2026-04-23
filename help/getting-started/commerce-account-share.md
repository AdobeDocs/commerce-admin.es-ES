---
title: Compartir una [!DNL Commerce] cuenta
description: Aprenda a conceder acceso limitado a su cuenta de  [!DNL Commerce] para otros titulares de la cuenta de [!DNL Commerce] .
exl-id: adc4fed4-89f4-4b0c-811c-fcf6f94dbc22
feature: User Account
source-git-commit: 593bad9ca83e96a145beeceb0265e0080e5f7930
workflow-type: tm+mt
source-wordcount: '957'
ht-degree: 0%

---

# Compartir una cuenta de [!DNL Commerce]

Su cuenta de [!DNL Commerce] contiene información que puede poner a disposición de empleados y proveedores de servicios de confianza que le ayuden a administrar el sitio. Al compartir el acceso a la cuenta, toda la información confidencial, como el historial de facturación o la información de la tarjeta de crédito, permanece protegida y nunca está disponible para otros usuarios.

El titular de la cuenta principal tiene autoridad para otorgar acceso limitado a otros titulares de la cuenta [!DNL Commerce]. El acceso compartido se puede revocar, pero no transferir. Para ``Cloud Shared Access from MAG[XYZ]`` entradas, el registro de usuario **no se puede eliminar aquí**, pero el acceso **aún se puede revocar**.

Solo el titular de la cuenta principal con los permisos adecuados puede otorgar formalmente el acceso compartido. Si el titular de la cuenta principal ya no tiene acceso o ha abandonado la compañía, el cliente debe usar el [proceso de transferencia de cuenta de Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-transfer) para pasar la propiedad a un nuevo contacto. Aunque el equipo de soporte de Commerce puede suplantar al cliente en situaciones limitadas, el cliente debe configurar el acceso compartido para reducir el riesgo de seguridad y responsabilidad.


![Configuración de acceso compartido](./assets/shared-access.png){width="600" zoomable="yes"}

La sección Historial de Facturación muestra solamente las facturas antiguas que se crearon antes de un cambio en el sistema de facturación. If you don’t see any newer invoices listed, those invoices have been transitioned to the new system and are not accessible from this view.

>[!IMPORTANT]
>
>All actions taken by users with shared access are the sole responsibility of the primary account holder. Adobe is not responsible for any actions taken by users who have shared access to your account.

## Set up a shared account

1. Antes de empezar, obtenga la siguiente información de la cuenta [!DNL Commerce] del **nuevo beneficiario de acceso compartido**:

   - El usuario ya debe haberse registrado para obtener una cuenta en account.adobe.com y haber iniciado sesión a través de account.magento.com. Consulte [Crear una cuenta de Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create#create-a-commerce-account) para obtener más información.
   - The `MAGE ID/Account ID (MAG00XXXXXXX)` is displayed in the upper-left corner of the _[!UICONTROL Magento]_tab, just above the **Log Out**link.
   - The `Email` address that is associated with the account.

1. Log in to your [[!DNL Commerce] account](commerce-account-create.md).

1. In the left navigation panel, click **[!UICONTROL Shared Access]**.

1. Click **[!UICONTROL Add New User]**.

   ![Agregar nuevo usuario](./assets/shared-access-add.png){width="600" zoomable="yes"}

1. En [!UICONTROL _New User Information]_, haga lo siguiente:

   - Escriba **[!UICONTROL Account ID]** de la cuenta [!DNL Commerce] del nuevo usuario.
   - Escriba la dirección **[!UICONTROL Email]** asociada a la cuenta [!DNL Commerce] del nuevo usuario.

   ![Nueva información de usuario](./assets/shared-new-user.png){width="600"}

1. En _[!UICONTROL Shared Information]_, haga lo siguiente:

   - Para identificar la cuenta compartida, escriba un **[!UICONTROL Share Name]**. Este nombre es para referencia interna y solo es visible para usted y la persona con la que comparte su cuenta.

     Una práctica recomendada es utilizar su nombre de organización como [!UICONTROL Share Name]. No utilice un nombre que comience por `CLOUD SHARED ACCESS FROM MAG XYX`.
   - Si desea compartir su información de contacto personal con el nuevo usuario, escriba **[!UICONTROL Your Email]** y **[!UICONTROL Your Phone]**.

1. En _[!UICONTROL Grant Account Permissions]_, active la casilla de verificación de cada producto y servicio [!DNL Commerce] que desee compartir.

   ![Grant the account permissions](./assets/shared-permissions.png){width="600"}

1. Click **[!UICONTROL Create Shared Access]**.

   The new user information appears in the _[!UICONTROL Manage Permissions]_section of the Shared Access page, and an email invitation with instructions to access the shared account is sent to the new user.

   ![Manage permissions for shared access](./assets/shared-manage-permissions.png){width="600" zoomable="yes"}

>[!NOTE]
>
>No es necesario compartir el acceso a _[!UICONTROL Security Tool]_: cualquier usuario con un ID de MAGE puede configurar la herramienta de exploración de seguridad con su propia cuenta. Solo necesitan los privilegios necesarios para realizar cambios en el sitio y comprobar la propiedad del dominio mediante uno de los [métodos necesarios](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security-scan)).

## Access a shared account

Las siguientes instrucciones se escriben desde la perspectiva de un usuario compartido que recibe una invitación a una cuenta compartida.

1. Cuando reciba una invitación a una cuenta compartida, siga las instrucciones del mensaje de correo electrónico para iniciar sesión en su propia cuenta de [!DNL Commerce].

   El panel de navegación izquierdo de su cuenta tiene una nueva ficha _[!UICONTROL Shared with me]_. El control_[!UICONTROL Switch Accounts]_ de la esquina superior derecha tiene opciones para `My Account` y el nombre de la cuenta compartida.

   ![Compartido conmigo](./assets/shared-with-me.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >   Si no ve el control _[!UICONTROL Switch Accounts]_, póngase en contacto con el titular de la cuenta principal y confirme que ha escrito la [información de cuenta](#set-up-a-shared-account) correcta.


1. Para obtener acceso a la cuenta compartida, establezca **[!UICONTROL Switch Accounts]** en el nombre de la cuenta compartida.

   ![Cambiar a la cuenta compartida](./assets/shared-switch.png){width="600" zoomable="yes"}

   La cuenta compartida muestra un mensaje de bienvenida e información de contacto. El panel de navegación izquierdo incluye sólo los elementos que tiene permiso para utilizar.

1. Para conectar la cuenta compartida al Centro de ayuda, haga clic en **[!UICONTROL Support]** en el panel de navegación izquierdo de la cuenta compartida.

   ![Support](./assets/shared-support.png){width="600" zoomable="yes"}

   You can use the [Adobe Commerce Help Center](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview) from the shared account to search for articles and troubleshooting information, find patches for known issues, and create support tickets.

   >[!NOTE]
   >
   >After receiving shared access, to [submit a Support case](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) on Experience League, make sure that you first select the Organization name that ends in &quot;([!DNL Commerce])&quot; in the left column.

1. To return to your own account, click **Back** in your browser controls and set **[!UICONTROL Switch Accounts]** to `My Account`.

## Revoke shared access

1. Inicie sesión en su cuenta de Commerce.

1. In the left navigation panel, click **[!UICONTROL Shared Access]**.

1. Find the account to be revoked under _[!UICONTROL Managing Users & Permissions]_and click **[!UICONTROL Delete]**.

   >[!NOTE]
   >
   > If  **[!UICONTROL Delete]** is not displayed, check whether the **[!UICONTROL Share Name]** contains the naming pattern  `Cloud Shared Access from MAG0XYZ`. If the account has that [naming pattern and cannot be deleted](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users), this is because the Shared Access was created by an API, and not directly from the [Commerce account](https://account.magento.com/).
   > 
   > If it cannot be deleted, simply have the Account Owner modify the Shared Access account and under Grant Account Permissions, uncheck every item. After that update, the user will no longer be able to access any account resources.
   > ![imagen](https://git.corp.adobe.com/AdobeDocs/commerce-admin.en/assets/38345/55f383e5-89c7-4832-bada-f765b522f4b5)
   >
   > Además, asegúrese de que los usuarios se eliminen del proyecto para que ya no reciban notificaciones por correo electrónico: [Los integrantes anteriores del equipo reciben notificaciones por correo electrónico de Adobe Commerce Cloud](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails)


1. Cuando se le pida que confirme, haga clic en **[!UICONTROL Delete User]**.

>[!NOTE]
>
>No puede eliminar usuarios con el nombre compartido de _Acceso compartido en la nube de MAG[XYZ]_ en esta interfaz. Consulte [¿Cómo eliminar usuarios a los que se les concedió acceso compartido a través de un proyecto de Cloud?](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users).

## Lectura relacionada

[Solución de problemas de acceso compartido](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/shared-access-troubleshooting)

