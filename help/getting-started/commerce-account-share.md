---
title: Compartir una [!DNL Commerce] cuenta
description: Aprenda a conceder acceso limitado a su cuenta de  [!DNL Commerce] para otros titulares de la cuenta de [!DNL Commerce] .
exl-id: adc4fed4-89f4-4b0c-811c-fcf6f94dbc22
feature: User Account
TQID: https://experienceleague.adobe.com/A98obp-6T8JgE0yCm0TmxpRslEq2Cb-5m53rBfxzfhg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1078
ht-degree: 0%

---

# Compartir una cuenta de [!DNL Commerce]

Su cuenta de [!DNL Commerce] contiene información que puede poner a disposición de empleados y proveedores de servicios de confianza que le ayuden a administrar el sitio. Al compartir el acceso a la cuenta, toda la información confidencial, como el historial de facturación o la información de la tarjeta de crédito, permanece protegida y nunca está disponible para otros usuarios.

El titular de la cuenta principal tiene autoridad para otorgar acceso limitado a otros titulares de la cuenta [!DNL Commerce]. El acceso compartido se puede revocar, pero no transferir. Para ``Cloud Shared Access from MAG[XYZ]`` entradas, el registro de usuario **no se puede eliminar aquí**, pero el acceso **aún se puede revocar**.

Solo el titular de la cuenta principal con los permisos adecuados puede otorgar formalmente el acceso compartido. Si el titular de la cuenta principal ya no tiene acceso o ha abandonado la compañía, el cliente debe usar el [proceso de transferencia de cuenta de Commerce](https://experienceleague.adobe.com/es/docs/commerce-admin/start/commerce-account/commerce-account-transfer) para pasar la propiedad a un nuevo contacto. Aunque el equipo de soporte de Commerce puede suplantar al cliente en situaciones limitadas, el cliente debe configurar el acceso compartido para reducir el riesgo de seguridad y responsabilidad.


![Configuración de acceso compartido](./assets/shared-access.png){width="600" zoomable="yes"}

La sección Historial de Facturación muestra solamente las facturas antiguas que se crearon antes de un cambio en el sistema de facturación. Si no ve ninguna factura más reciente en la lista, significa que esas facturas se han transferido al nuevo sistema y no se puede acceder a ellas desde esta vista.

>[!IMPORTANT]
>
>Todas las acciones que realicen los usuarios con acceso compartido son responsabilidad exclusiva del titular de la cuenta principal. Adobe no se responsabiliza de las acciones realizadas por los usuarios que han compartido el acceso a su cuenta.

## Configuración de una cuenta compartida

1. Antes de empezar, obtenga la siguiente información de la cuenta [!DNL Commerce] del **nuevo beneficiario de acceso compartido**:

   - El usuario ya debe haberse registrado para obtener una cuenta en account.adobe.com y haber iniciado sesión a través de account.magento.com. Consulte [Crear una cuenta de Commerce](https://experienceleague.adobe.com/es/docs/commerce-admin/start/commerce-account/commerce-account-create#create-a-commerce-account) para obtener más información.
   - `MAGE ID/Account ID (MAG00XXXXXXX)` se muestra en la esquina superior izquierda de la ficha _[!UICONTROL Magento]_, justo encima del vínculo **Cerrar sesión**.
   - La dirección `Email` asociada con la cuenta.

1. Inicie sesión en su [[!DNL Commerce] cuenta](commerce-account-create.md).

1. En el panel de navegación izquierdo, haga clic en **[!UICONTROL Shared Access]**.

1. Haga clic en **[!UICONTROL Add New User]**.

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

   ![Conceder permisos a la cuenta](./assets/shared-permissions.png){width="600"}

1. Haga clic en **[!UICONTROL Create Shared Access]**.

   La nueva información de usuario aparece en la sección _[!UICONTROL Manage Permissions]_&#x200B;de la página Acceso compartido y se envía al nuevo usuario una invitación por correo electrónico con instrucciones para acceder a la cuenta compartida.

   ![Administrar permisos para acceso compartido](./assets/shared-manage-permissions.png){width="600" zoomable="yes"}

>[!NOTE]
>
>No es necesario compartir el acceso a _[!UICONTROL Security Tool]_: cualquier usuario con un ID de MAGE puede configurar la herramienta de exploración de seguridad con su propia cuenta. Solo necesitan los privilegios necesarios para realizar cambios en el sitio y comprobar la propiedad del dominio mediante uno de los [métodos necesarios](https://experienceleague.adobe.com/es/docs/commerce-admin/systems/security/security-scan)).

## Acceso a una cuenta compartida

Las siguientes instrucciones se escriben desde la perspectiva de un usuario compartido que recibe una invitación a una cuenta compartida.

1. Cuando reciba una invitación a una cuenta compartida, siga las instrucciones del mensaje de correo electrónico para iniciar sesión en su propia cuenta de [!DNL Commerce].

   El panel de navegación izquierdo de su cuenta tiene una nueva ficha _[!UICONTROL Shared with me]_. El control&#x200B;_[!UICONTROL Switch Accounts]_ de la esquina superior derecha tiene opciones para `My Account` y el nombre de la cuenta compartida.

   ![Compartido conmigo](./assets/shared-with-me.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >   Si no ve el control _[!UICONTROL Switch Accounts]_, póngase en contacto con el titular de la cuenta principal y confirme que ha escrito la [información de cuenta](#set-up-a-shared-account) correcta.


1. Para obtener acceso a la cuenta compartida, establezca **[!UICONTROL Switch Accounts]** en el nombre de la cuenta compartida.

   ![Cambiar a la cuenta compartida](./assets/shared-switch.png){width="600" zoomable="yes"}

   La cuenta compartida muestra un mensaje de bienvenida e información de contacto. El panel de navegación izquierdo incluye sólo los elementos que tiene permiso para utilizar.

1. Para conectar la cuenta compartida al Centro de ayuda, haga clic en **[!UICONTROL Support]** en el panel de navegación izquierdo de la cuenta compartida.

   ![Asistencia](./assets/shared-support.png){width="600" zoomable="yes"}

   Puede usar el [Centro de ayuda de Adobe Commerce](https://experienceleague.adobe.com/es/docs/commerce-knowledge-base/kb/overview) de la cuenta compartida para buscar artículos e información de solución de problemas, buscar parches para problemas conocidos y crear vales de soporte técnico.

   >[!NOTE]
   >
   >Después de recibir acceso compartido, para [enviar un caso de soporte técnico](https://experienceleague.adobe.com/es/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) en Experience League, asegúrese de seleccionar primero el nombre de la organización que termina en &quot;([!DNL Commerce])&quot; en la columna izquierda.

1. Para volver a su cuenta, haga clic en **Atrás** en los controles del explorador y establezca **[!UICONTROL Switch Accounts]** en `My Account`.

## Revocar acceso compartido

1. Inicie sesión en su cuenta de Commerce.

1. En el panel de navegación izquierdo, haga clic en **[!UICONTROL Shared Access]**.

1. Busque la cuenta que desea revocar en _[!UICONTROL Managing Users & Permissions]_&#x200B;y haga clic en **[!UICONTROL Delete]**.

   >[!NOTE]
   >
   > Si no se muestra **[!UICONTROL Delete]**, compruebe si **[!UICONTROL Share Name]** contiene el patrón de nombres `Cloud Shared Access from MAG0XYZ`. Si la cuenta tiene ese [patrón de nomenclatura y no se puede eliminar](https://experienceleague.adobe.com/es/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users), esto se debe a que el acceso compartido se creó mediante una API y no directamente desde la [cuenta de Commerce](https://account.magento.com/).
   > 
   > Si no se puede eliminar, haga que el propietario de la cuenta modifique la cuenta de acceso compartido y en Conceder permisos de cuenta, desactive todos los elementos. Después de esta actualización, el usuario ya no podrá acceder a ningún recurso de la cuenta.
   > ![imagen](https://git.corp.adobe.com/AdobeDocs/commerce-admin.en/assets/38345/55f383e5-89c7-4832-bada-f765b522f4b5)
   >
   > Además, asegúrese de que los usuarios se eliminen del proyecto para que ya no reciban notificaciones por correo electrónico: [Los integrantes anteriores del equipo reciben notificaciones por correo electrónico de Adobe Commerce Cloud](https://experienceleague.adobe.com/es/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails)


1. Cuando se le pida que confirme, haga clic en **[!UICONTROL Delete User]**.

>[!NOTE]
>
>No puede eliminar usuarios con el nombre compartido de _Acceso compartido en la nube de MAG[XYZ]_ en esta interfaz. Consulte [¿Cómo eliminar usuarios a los que se les concedió acceso compartido a través de un proyecto de Cloud?](https://experienceleague.adobe.com/es/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users).

## Lectura relacionada

[Solución de problemas de acceso compartido](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/shared-access-troubleshooting)

