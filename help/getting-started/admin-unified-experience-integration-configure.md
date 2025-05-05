---
title: Configuración de la integración de Experience Cloud para el administrador de Commerce
description: Obtenga información sobre cómo configurar un proyecto de Commerce para habilitar el acceso de administrador mediante Experience Cloud.
hide: false
hidefromtoc: false
feature: Integration
role: Admin, Leader
exl-id: b2522d25-8255-4219-98b5-4b764430dea2
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 0%

---

# Configuración de la integración de Experience Cloud con el administrador de Commerce

Empiece a utilizar la integración de Experience Cloud con el administrador de Commerce configurando la aplicación de Commerce para utilizar las extensiones de Commerce Admin Unified Experience y Commerce Events.


## Requisitos previos

- Adobe Commerce debe estar configurado para usar [autenticación IMS de Adobe](../getting-started/adobe-ims-config.md)
- Aprovisionamiento de cuentas y permisos: los administradores deben tener un [perfil empresarial de Adobe](https://helpx.adobe.com/enterprise/kb/introducing-adobe-profiles.html#:~:text=Adobe%20profiles%20help%20you%20manage,under%20the%20same%20email%20address) con acceso a los siguientes recursos para configurar la integración de Experience Cloud:
   - [Adobe Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html): agregue y administre cuentas de usuario y desarrollador de Adobe para la organización
   - [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/getting-started/): acceso de desarrollador o administrador del sistema para crear proyectos de App Builder y generar las credenciales de conexión y la configuración de proyecto para usar el servicio de Adobe I/O Events
   - [Proyecto de Commerce en la nube](https://experienceleague.adobe.com/docs/commerce-cloud-service/start/onboarding.html#get-started-with-the-project-web-interface): instale los módulos necesarios y configure el servidor de aplicaciones de Commerce mediante la CLI de Adobe Commerce
   - [Administrador de Commerce](https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html): actualice la configuración de la tienda y administre las cuentas de usuario de Commerce

## Información general de configuración

Habilite la integración realizando las siguientes tareas:

1. [Compruebe el entorno de Commerce y la configuración de la aplicación](#check-the-commerce-environment-and-application-configuration).

1. [Habilite la extensión Commerce Admin Unified Experience](#enable-the-commerce-admin-unified-experience-extension).

1. [Configurar Adobe I/O Events para Commerce](#set-up-adobe-io-events).

1. [Probar la integración](#test-the-integration).

## Compruebe el entorno de Commerce y la configuración de la aplicación

Antes de configurar la integración de Experience Cloud, compruebe que su proyecto y la aplicación de Commerce cumplen los requisitos.

1. En la estación de trabajo local, cambie al directorio del proyecto para su proyecto de Commerce.

1. Consulte la rama de entorno para que la instancia se integre con Experience Cloud.

1. Compruebe que Adobe IMS está activado.

   - Utilice la [URL de acceso SSH](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html) para que el entorno se conecte al servidor de aplicaciones de Commerce.

   - Desde la línea de comandos, utilice la CLI de Adobe Commerce para comprobar el estado del módulo IMS.

     ```bash
     bin/magento admin:adobe-ims:status
     ```

   Si el módulo no está habilitado, [actívelo usando la organización y las credenciales para el proyecto de integración de IMS](../getting-started/adobe-ims-config.md#step-3-enable-the-adminadobeims-module).

1. Compruebe que el usuario administrador puede iniciar sesión en el administrador de Commerce con su Adobe ID.

   - Vaya a la URL de administración de Commerce.

   - Si ha iniciado sesión, cierre la sesión.

   - Asegúrese de que se redirige al usuario administrador para que inicie sesión con su Adobe ID.

     ![Adobe Commerce inició sesión con Adobe ID](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

1. En el directorio del proyecto en la nube de la estación de trabajo local, compruebe que la extensión Commerce Admin Unified Experience esté instalada.

   ```bash
   composer show *unified-experience*
   ```

   Si la extensión está instalada, Composer devuelve el nombre y la descripción de la extensión.

   ```
   magento/module-unified-experience <version> Commerce module responsible for integration with Adobe Experience Cloud
   ```

   Si la extensión no está instalada, utilice Composer para instalarla. A continuación, confirme los cambios y vuelva a implementar el entorno de la nube.

   ```
   composer require magento/module-unified-experience
   composer update
   ```

## Habilitar la experiencia unificada de administración de Commerce

Habilite la extensión Commerce Admin Unified Experience y, a continuación, inicie sesión mediante Experience Cloud.

>[!NOTE]
>
>Estas instrucciones muestran cómo un administrador de proyectos de Commerce Cloud puede habilitar la extensión mediante la CLI de Adobe Commerce. Los usuarios administradores de Commerce también pueden habilitar la extensión actualizando [las opciones de configuración de la tienda Commerce](admin-unified-experience-integration-manage.md#from-the-commerce-admin).

1. Desde el directorio raíz del entorno de su proyecto en la nube en su estación de trabajo local, use la [herramienta CLI de magento en la nube](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/dev-tools/cloud-cli/cloud-cli-overview.html) para iniciar sesión en el servidor de aplicaciones de Commerce.

   ```bash
   magento-cloud ssh
   ```

1. Habilite la extensión `magento/module-unified-experience` mediante la CLI de Adobe Commerce:

   ```bash
   bin/magento config:set admin/unified_experience/enabled 1
   Admin Unified Experience integration is enabled
   ```

1. Borre la caché.

   ```bash
   bin/magento cache:clean
   ```

## Configuración de Adobe I/O Events para Commerce

Cuando la integración de Experience Cloud está habilitada, el servicio Adobe I/O Events envía datos de evento de Commerce a Experience Cloud para administrar el acceso de administrador a los proyectos de Commerce. La configuración del servicio requiere habilitar la extensión de Adobe I/O Events para Commerce (`magento/commerce-eventing`) y configurar el servicio de Adobe I/O Events en el administrador.

### Habilitar eventos de Commerce

Habilite la extensión de eventos de Commerce (`magento/commerce-eventing`) para enviar datos de evento personalizados de la aplicación de Commerce al servicio de Adobe I/O Events.

>[!NOTE]
>
>En Commerce 2.4.6 y versiones posteriores, la extensión Eventos de Commerce se instala de forma predeterminada. Para proyectos de Commerce con Commerce 2.4.5, use primero Composer para [instalar la extensión](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce) y después habilitarla.

1. Desde el entorno de desarrollo de proyectos de Commerce local, agregue la configuración siguiente al archivo `.magento.env.yaml`.

   ```yaml
   stage:
     global:
       ENABLE_EVENTING: true
     deploy:
       CRON_CONSUMERS_RUNNER:
         cron_run: true
         max_messages: 0
         consumers: []
   ```

1. Agregue, confirme e implemente el(la) `.magento.env.yaml file` actualizado(a) en el entorno de nube.

>[!TIP]
>
>Para obtener más información sobre la configuración y administración de variables de entorno mediante el archivo `.magento.env.yaml`, vea [Configurar variables de entorno para la implementación](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/configure-env-yaml.html).

### Configuración de la integración de eventos de Commerce

Configure la integración de eventos de Commerce realizando las siguientes tareas. Para obtener instrucciones detalladas, consulte la documentación para desarrolladores de [Adobe I/O Events for Commerce](https://developer.adobe.com/commerce/extensibility/events/project-setup/).

1. [Cree un proyecto App Builder](https://developer.adobe.com/commerce/extensibility/events/project-setup/) para recibir datos de evento de la instancia Commerce.

   Necesita credenciales y datos de configuración del proyecto de App Builder para configurar la integración en el administrador de Commerce.

1. Configure Adobe Commerce para que utilice Adobe I/O Events.

   - [Actualice la configuración del almacén para el servicio Adobe I/O Events](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#begin-configuring-events-on-commerce).

   - [Configure un proveedor de eventos para enviar eventos de Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#create-an-event-provider-and-complete-the-commerce-configuration).

1. [Actualice el proyecto de App Builder para recibir datos de evento de la instancia de Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#subscribe-and-register-events).

   No registrar ni suscribirse a eventos desde la instancia de Commerce. El registro de eventos se inserta en el proyecto App Builder al configurar el proveedor de eventos para la aplicación Commerce.

   Después de conectar el proveedor de eventos al proyecto de App Builder, suscríbase al evento `observer.uex_commerce_instance_update` y guarde los cambios.

1. Para establecer la conexión, envíe un evento al consumidor a través del proveedor de eventos.

   - Desde la línea de comandos del directorio local del proyecto en la nube, [use SSH para conectarse al servidor de aplicaciones de Commerce](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment).

     ```bash
     magento-cloud ssh
     ```

   - Envíe datos de evento comprobando el estado de la extensión de experiencia unificada del administrador mediante la CLI de Adobe Commerce.

     ```bash
     bin/magento bin/magento admin:uex:status
     ```

### Prueba de la integración

Compruebe que un administrador de Commerce puede iniciar sesión en Experience Cloud para ver los proyectos de Commerce disponibles y acceder a la administración y tienda de cada proyecto.

1. [Inicie sesión en Experience Cloud](https://experiencecloud.adobe.com/library) con Adobe ID y la organización asociada a la instancia de Commerce.

   ![Acceder a proyectos de Commerce desde la página de inicio de Experience Cloud](./assets/admin-uex-home-page.png){width="600" zoomable="yes"}

1. Ver los proyectos de Commerce disponibles seleccionando **[!UICONTROL Commerce]**.

   ![Espacio de trabajo de proyectos de Commerce para Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="600" zoomable="yes"}

1. Abra el Administrador de una instancia seleccionando **[!UICONTROL Open]**.

   ![Vista de administrador de Commerce con la integración de Experience Cloud habilitada](./assets/admin-dashboard.png){width="600" zoomable="yes"}

1. Compruebe que puede realizar las tareas de administración según lo esperado.

   Los flujos de trabajo en el administrador de Commerce deben seguir el mismo proceso. Si experimenta cambios o errores en el flujo de trabajo después de habilitar la integración de Experience Cloud, póngase en contacto con el administrador del sistema de Commerce o [envíe un ticket de asistencia de Adobe](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket).

Después de configurar la integración de Experience Cloud, compruebe que las cuentas de administrador están aprovisionadas correctamente para acceder a los proyectos de Commerce a través de Experience Cloud. Consulte [Administrar usuarios administradores](/help/getting-started/admin-unified-experience-integration-manage.md#manage-admin-user-accounts).
