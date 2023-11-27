---
title: Configuración de la integración de administración de Commerce con ID
description: Siga este procedimiento opcional para integrar los inicios de sesión de cuenta de usuario de administrador de Adobe Commerce con Adobe ID.
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
source-git-commit: 20b2560ce2b8071c740907292544519f8b1c3ddf
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 1%

---

# Configuración de la integración de administración de Commerce con Adobe ID

{{ee-feature}}

Esta integración es compatible con los comerciantes de Commerce y con los usuarios administradores que tienen un Adobe ID y que desean optimizar el inicio de sesión en los productos de Adobe Commerce y Adobe Business. Es opcional y se habilita en función de cada instancia. Solo los flujos de trabajo de usuarios administradores se ven afectados cuando está habilitada. 

>[!IMPORTANT]
>
>Los usuarios administradores deben guardar sus credenciales de administración de Commerce (nombre de usuario y contraseña) y sus credenciales de 2FA antes de habilitar esta integración. Estas credenciales son necesarias si la integración de IMS está desactivada.

## Requisitos previos

* Adobe Commerce 2.4.5 o posterior
* Una cuenta de Adobe.com con acceso a [Adobe Admin Console](https://adminconsole.adobe.com/).

El administrador que configura esta integración necesita las siguientes credenciales durante la activación del módulo:

* ID de organización (obtenido de) [Adobe Admin Console](https://adminconsole.adobe.com/)), que debe tener al menos 24 caracteres de longitud. El usuario autenticado debe pertenecer a esta organización de IMS. Para obtener información sobre cómo encontrar su ID de organización, consulte [Organizaciones en Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).
* 2FA debe aplicarse en el nivel de organización en Adobe Admin Console para habilitar el módulo. Marque [Configuración de autenticación](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification).
* ID de cliente
* Secreto de cliente
* El ID de cliente y el secreto de cliente están disponibles después de recuperar las claves de API del [Consola de Adobe Developer](https://developer.adobe.com/developer-console/docs/guides/credentials/).

Los usuarios administradores de Commerce deben crear una cuenta con un Adobe ID para iniciar sesión.

## Pasos generales

* Obtención del ID de organización de Adobe del [Adobe Admin Console](https://adminconsole.adobe.com/)
* Genere un nuevo proyecto, claves de API de IMS y secreto a partir de [Consola de Adobe Developer](https://developer.adobe.com/)
* Habilite la `AdminAdobeIms` módulo
* Configure a los usuarios de Adobe Commerce en Adobe Admin Console.

Una integración correcta requiere que todos los usuarios de Adobe Commerce tengan cuentas de usuario de administrador con el mismo nombre y dirección de correo electrónico principal. Si no existe una cuenta de usuario Administrador que coincida, un usuario con los permisos necesarios (normalmente asignados a la función Administrador) debe hacerlo manualmente [crear la cuenta de usuario de administrador](../systems/permissions-users-all.md#create-a-user) con el mismo nombre y correo electrónico.

## Configuración de la integración

Una vez que un administrador o desarrollador con acceso al sistema haya completado los siguientes pasos, la variable _[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_El botón se muestra en la página de inicio de sesión de administración de Commerce para todos los usuarios administradores.

### Paso 1: Obtención del ID de organización de Adobe

Se requiere la pertenencia a al menos una organización de IMS para habilitar esta función. Si tiene una Adobe ID, pertenece al menos a una organización de Adobe de forma predeterminada. Inicie sesión en [Adobe Admin Console](https://adminconsole.adobe.com/) para recuperar su ID de organización.

### Paso 2: Generar un nuevo proyecto, claves de API de IMS y secreto

Para crear proyectos para una organización, la cuenta Administrador de Adobe de la organización debe tener la función Administrador del sistema o Desarrollador. Consulte la [Guía de Developer Console](https://developer.adobe.com/developer-console/docs/guides/projects/).

1. Iniciar sesión en [Consola de Adobe Developer](https://developer.adobe.com/).
1. Vaya a la **[!UICONTROL Projects]** (adobe.io/projects) y haga clic en **[!UICONTROL Create a new project]**.
1. Clic **[!UICONTROL Add API]** en la página Proyecto recién creada.
1. Seleccionar **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**.
1. Seleccionar **[!UICONTROL Oauth 2.0 Web]**.
1. Especifique el **[!UICONTROL Redirect URI]**: `https://<hostname>/`
1. Especifique el **[!UICONTROL Redirect URI pattern]**: `https://<hostname>/.*`

   Evite los puntos del nombre de host anteponiendo a los puntos `\\`. Añadir un comodín al final de la URL admite la clave secreta de administrador de Adobe Commerce.

1. Haga clic **[!UICONTROL Save configured API]**.
1. Copie el [!UICONTROL Client ID] y [!UICONTROL Client Secret] claves del proyecto creado.

### Paso 3: Habilitar el módulo AdminAdobeIms

El `AdminAdobeIms` es responsable de la integración de Adobe Commerce/Adobe IMS. Después de configurar el nuevo proyecto y copiar el ID de organización, el ID de cliente y el secreto de cliente, puede habilitar el `AdminAdobeIms` módulo.

Entrar `bin/magento admin:adobe-ims:enable`. Se le pedirá que introduzca los siguientes parámetros. Utilice los valores que se generaron durante la creación del proyecto.

* ID de organización
* ID de cliente
* Secreto de cliente
* Habilitado para 2FA

Adobe Commerce muestra un mensaje que indica si la habilitación se realizó correctamente o no.

Después de habilitar correctamente esta función, puede realizar la transición de otras cuentas de usuario de Adobe Commerce a cuentas de IMS de Adobe. Los usuarios de Adobe Commerce deben pertenecer a la organización de Adobe configurada para iniciar sesión con un Adobe ID.

### Paso 4: Configuración de los usuarios de Adobe Commerce en Adobe Admin Console

Después de habilitar correctamente esta función, puede realizar la transición de otras cuentas de usuario de Adobe Commerce a cuentas de IMS de Adobe. Los usuarios de Adobe Commerce deben pertenecer al menos a una organización de Adobe para iniciar sesión con un Adobe ID.

1. En el [Admin Console](https://helpx.adobe.com/es/enterprise/using/admin-console.html), vaya a **[!UICONTROL Users]**  > **[!UICONTROL Users]**.

1. Haga clic **[!UICONTROL Add User]**.

1. Introduzca la dirección de correo electrónico del usuario.

   Si procede, el tipo de ID recomendado se rellena automáticamente. Puede cambiar esta configuración a uno de los ID de producto de la lista, que se basa en el plan de compra de su organización.

   Puede agregar hasta diez usuarios a la vez. Para agregar más, repita los pasos anteriores después de guardar los cambios.

1. Haga clic **[!UICONTROL Save]**.

El usuario se añade y se muestra en la [!UICONTROL Users] lista.
