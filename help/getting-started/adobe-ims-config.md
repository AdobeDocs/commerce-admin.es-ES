---
title: Configuración de la integración de administración de Commerce con ID
description: Siga este procedimiento opcional para integrar los inicios de sesión de cuenta de usuario de administrador de Adobe Commerce con Adobe ID.
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
source-git-commit: 8589444a126c82f033c5b852b20493d1cf83c338
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---

# Configuración de la integración de administración de Commerce con Adobe ID

{{ee-feature}}

Esta integración es compatible con los comerciantes de Commerce con usuarios administradores que tengan un Adobe ID y que deseen optimizar el inicio de sesión en los productos empresariales de Adobe Commerce y Adobe. Es opcional y se habilita en función de cada instancia. Solo los flujos de trabajo de usuarios administradores se ven afectados cuando está habilitada. 

>[!IMPORTANT]
>
>Los usuarios administradores deben guardar sus credenciales de administrador de Commerce (nombre de usuario y contraseña) y las credenciales de 2FA antes de habilitar esta integración. Estas credenciales son necesarias si la integración de IMS está desactivada.

## Requisitos previos

* Adobe Commerce 2.4.5 o posterior
* Una cuenta de Adobe.com con acceso a [Adobe Admin Console](https://adminconsole.adobe.com/).

El administrador que configura esta integración necesita las siguientes credenciales durante la activación del módulo:

* ID de organización (obtenido de [Adobe Admin Console](https://adminconsole.adobe.com/)), que debe tener al menos 24 caracteres de longitud. El usuario autenticado debe pertenecer a esta organización de IMS. Para obtener información sobre cómo encontrar tu ID de organización, consulta [Organizaciones en Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=es).
* 2FA debe aplicarse en el nivel de organización en Adobe Admin Console para habilitar el módulo. Compruebe [configuración de autenticación](https://helpx.adobe.com/es/enterprise/using/authentication-settings.html#two-step-verification).
* ID de cliente
* Secreto de cliente
* El ID de cliente y el secreto de cliente están disponibles después de recuperar las claves de API de [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/credentials/).

Los usuarios administradores de Commerce deben crear una cuenta con un Adobe ID para iniciar sesión.

## Pasos generales

* Obtener el identificador de organización de Adobe de [Adobe Admin Console](https://adminconsole.adobe.com/)
* Genere un nuevo proyecto, claves de API de IMS y secreto a partir de [Adobe Developer Console](https://developer.adobe.com/)
* Configuración de usuarios de Adobe Commerce en Adobe Admin Console
* Habilite el módulo `AdminAdobeIms`.

Una integración correcta requiere que todos los usuarios de Adobe Commerce tengan cuentas de usuario de administrador con el mismo nombre y dirección de correo electrónico principal. Si no existe una cuenta de usuario de administrador coincidente, un usuario con los permisos necesarios (normalmente asignado a la función de administrador) debe [crear manualmente la cuenta de usuario de administrador](../systems/permissions-users-all.md#create-a-user) con el mismo nombre y correo electrónico.

## Configuración de la integración

Una vez que un administrador o desarrollador con acceso al sistema haya completado los siguientes pasos, el botón _[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_&#x200B;se mostrará en la página de inicio de sesión de administrador de Commerce para todos los usuarios administradores.

### Paso 1: Obtención del ID de organización de Adobe

Se requiere la pertenencia a al menos una organización de IMS para habilitar esta función. Si tiene un Adobe ID, pertenece al menos a una organización de Adobe de forma predeterminada. Inicie sesión en [Adobe Admin Console](https://adminconsole.adobe.com/) para recuperar su ID de organización.

### Paso 2: Generar un nuevo proyecto, claves de API de IMS y secreto

Para crear proyectos para una organización, la cuenta de administrador de Adobe de la organización debe tener la función de administrador del sistema o desarrollador. Consulte la [Guía de Developer Console](https://developer.adobe.com/developer-console/docs/guides/projects/).

1. Inicie sesión en [Adobe Developer Console](https://developer.adobe.com/).
1. Vaya a la ficha **[!UICONTROL Projects]** (adobe.io/projects) y haga clic en **[!UICONTROL Create a new project]**.
1. Haga clic en **[!UICONTROL Add API]** en la página de proyecto recién creada.
1. Seleccione **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**.
1. Seleccione **[!UICONTROL Oauth 2.0 Web]**.
1. Especifique **[!UICONTROL Redirect URI]**: `https://<commerce_base_url>/`
1. Especifique **[!UICONTROL Redirect URI pattern]**: `https://<commerce_base_url>/.*`

   Evite los puntos del nombre de host anteponiendo `\\` a los puntos. Añadir un comodín al final de la URL admite la clave secreta de administrador de Adobe Commerce.

1. Haga clic en **[!UICONTROL Save configured API]**.
1. Copie las claves [!UICONTROL Client ID] y [!UICONTROL Client Secret] del proyecto creado.

### Paso 3: Configuración de los usuarios de Adobe Commerce en Adobe Admin Console

Antes de habilitar la integración, compruebe que cada cuenta de usuario de administrador de Adobe Commerce tenga una cuenta de IMS de Adobe correspondiente. Los usuarios de Adobe Commerce deben pertenecer a una organización específica de Adobe para iniciar sesión con un Adobe ID.

>[!TIP]
>
>Puede crear varias cuentas de usuario cargando la información de usuario desde un archivo CSV. Consulte [Administrar varios usuarios](https://helpx.adobe.com/es/enterprise/using/bulk-upload-users.html).

1. En [Adobe Admin Console](https://helpx.adobe.com/es/enterprise/using/admin-console.html), vaya a **[!UICONTROL Users]** > **[!UICONTROL Users]**.

1. Haga clic en **[!UICONTROL Add User]**.

1. Introduzca la dirección de correo electrónico del usuario.

   Si procede, el tipo de ID recomendado se rellena automáticamente. Puede cambiar esta configuración a uno de los ID de producto de la lista, que se basa en el plan de compra de su organización.

   Puede agregar hasta diez usuarios a la vez. Para agregar más, repita los pasos anteriores después de guardar los cambios.

1. Haga clic en **[!UICONTROL Save]**.

El usuario se agrega y se muestra en la lista [!UICONTROL Users].

### Paso 4: Habilitar el módulo AdminAdobeIms

El módulo `AdminAdobeIms` es responsable de la integración de Adobe Commerce/Adobe IMS. Después de configurar el nuevo proyecto y copiar el identificador de organización, el identificador de cliente y el secreto de cliente, puede habilitar el módulo `AdminAdobeIms`.

Escriba `bin/magento admin:adobe-ims:enable`. Se le pedirá que introduzca los siguientes parámetros. Utilice los valores que se generaron durante la creación del proyecto.

* ID de organización
* ID de cliente
* Secreto de cliente
* Habilitado para 2FA

Adobe Commerce muestra un mensaje que indica si la habilitación se realizó correctamente o no.

Después de habilitar correctamente esta función, puede realizar la transición de otras cuentas de usuario de Adobe Commerce a cuentas de IMS de Adobe. Los usuarios de Adobe Commerce deben pertenecer a la organización de Adobe configurada para iniciar sesión con un Adobe ID.
