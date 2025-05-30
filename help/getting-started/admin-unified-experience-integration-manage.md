---
title: Administración de la integración de Experience Cloud
description: Obtenga información sobre cómo administrar la integración de Experience Cloud y solucionar problemas
hide: false
hidefromtoc: false
feature: Integration
exl-id: 451bf2e1-7c38-40be-a7c1-aaf0fe9f486c
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%

---

# Administración de la integración de Experience Cloud

Después de la activación inicial, administre el estado de la integración de Experience Cloud habilitando o deshabilitando la extensión de Commerce Admin Unified Experience.

- Si la extensión Commerce Admin Unified Experience está habilitada y las cuentas de administrador están [aprovisionadas correctamente](#manage-admin-user-accounts), los administradores de Commerce pueden ver los proyectos de Commerce disponibles en Adobe Experience Cloud y acceder a ellos. Los administradores aún pueden acceder a proyectos individuales utilizando la URL de administración para el entorno de proyecto de Commerce.

- Si la extensión Commerce Admin Unified Experience está deshabilitada, el acceso a través de Experience Cloud está deshabilitado. Los administradores deben iniciar sesión en proyectos individuales utilizando la URL de administración para el entorno de proyecto de Commerce.

>[!WARNING]
>
>Si la integración de Adobe Identity Management Service (IMS) está desactivada, la integración de Experience Cloud se desactiva automáticamente.

## Administrar la integración desde el administrador

1. En Commerce Admin, abra el menú Configuración de tienda seleccionando **[!UICONTROL Stores]** en el menú de navegación de la izquierda y, a continuación, seleccione **[!UICONTROL Configuration]**.

1. En el menú Configuración, seleccione **[!UICONTROL Advanced > Admin]** y, a continuación, expanda **[!UICONTROL Unified Experience option]**.

   ![Configuración del almacén de administración para la integración con Experience Cloud](./assets/admin-uex-manage-settings.png){width="600" zoomable="yes"}

1. Habilite o deshabilite la integración seleccionando el valor **[!UICONTROL Enable]**.

1. Cambie el nombre del proyecto que se muestra en el área de trabajo de Commerce Projects agregando o actualizando el valor **[!UICONTROL Project Name]**.

1. Guarde la configuración.

1. Borre la caché.

## Administre la integración utilizando la CLI de Adobe Commerce

Los administradores del sistema de Commerce con acceso de administrador al proyecto de nube de Commerce pueden utilizar los comandos CLI de Adobe Commerce para administrar la integración de Experience Cloud.

1. Desde el entorno de desarrollo local, inicie sesión en el proyecto de la nube.

   ```bash
   magento-cloud login
   ```

1. Desde el directorio raíz del entorno del proyecto en la nube, conéctese al servidor de aplicaciones de Commerce.

   ```bash
   ssh magento-cloud
   ```

1. Compruebe el estado de la extensión de la experiencia unificada del administrador:

   ```bash
   bin/magento admin:uex:status
   ```

1. Cambie el estado de la extensión para desactivar la integración

   - **Habilitar**—`bin/magento config:set admin/unified_experience/enabled 1`

   - **Deshabilitar**—`bin/magento config:set admin/unified_experience/enabled 0`

## Administrar cuentas de usuario de administrador

Todos los usuarios administradores de Commerce deben tener una cuenta de administrador en la instancia de Commerce y una cuenta de usuario de Adobe (Adobe ID) para acceder a los productos y servicios de Adobe. Ambas cuentas deben estar asociadas con la misma dirección de correo electrónico.

- **Cuenta de administrador de Commerce**—[Administrar usuarios de administrador de Commerce](../systems/permissions-users-all.md) del administrador de la instancia de Commerce. Las cuentas de usuario para los administradores de Commerce deben tener asignada la función Administrador.

  Los administradores de sistemas del proyecto Commerce pueden usar [SSH para conectarse al entorno remoto](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html?lang=es#connect-to-a-remote-environment) y usar los comandos `admin:user:create` y `admin:user:unlock` de Commerce CLI para agregar o desbloquear cuentas de usuario de administrador.

- **Cuenta de usuario de Adobe**: un administrador de la organización de Adobe asociada a la instancia de Commerce debe iniciar sesión en Adobe Admin Console y agregar Adobe ID para cada administrador de Commerce a la organización. A continuación, deben asignar derechos y permisos de producto para acceder a la aplicación de Commerce. Consulte [Configuración de usuarios de Adobe Commerce en Adobe Admin Console](adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console).

Los administradores que gestionan la configuración de la integración de Experience Cloud desde Adobe Developer Console deben tener una cuenta de usuario de Adobe con acceso de administrador del sistema o desarrollador.

>[!NOTE]
>
>Una Adobe ID es una cuenta creada a través de Adobe que es necesaria para acceder a productos y servicios a través de Experience Cloud. Los administradores de Commerce que no tengan un Adobe ID pueden [crear una cuenta gratuita](https://helpx.adobe.com/es/manage-account/using/create-update-adobe-id.html) con la misma dirección de correo electrónico que usan para iniciar sesión en el administrador de Commerce.
