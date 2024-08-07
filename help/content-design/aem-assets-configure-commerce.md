---
title: Instalación y configuración de la integración de Experience Manager Assets
description: Obtenga información sobre cómo instalar y configurar  [!DNL AEM Assets Integration for Adobe Commerce]
feature: CMS, Media
exl-id: 2f8b3165-354d-4b7b-a46e-1ff46af553aa
source-git-commit: da98c253d0d3f773551c7b58b5eedbb1db622ac6
workflow-type: tm+mt
source-wordcount: '1261'
ht-degree: 0%

---

# Instalación y configuración de la integración de AEM Assets para Commerce

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Instale y configure la integración de AEM Assets para Commerce añadiendo la extensión a la aplicación de Commerce, conectándose a los servicios SaaS de Commerce, al servicio Eventos de Adobe I/O electrónico y conectándose al SaaS de Commerce.

## Requisitos del sistema

**Requisitos de software**

- Adobe Commerce 2.4.5+
- PHP 8.1, 8.2, 8.3
- Compositor: 2.x

**Requisitos de configuración**

- Adobe Commerce debe estar configurado para usar [autenticación IMS de Adobe](/help/getting-started/adobe-ims-config.md).
- Aprovisionamiento de cuentas y permisos
   - [Administrador de proyectos en la nube de Commerce](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access): instale las extensiones necesarias y configure el servidor de aplicaciones de Commerce desde el administrador o la línea de comandos
   - [Administrador de Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/start/guide-overview): actualice la configuración de la tienda y administre las cuentas de usuario de Commerce

## Información general de configuración

Habilite la integración realizando las siguientes tareas:

1. [Instale la extensión AEM Assets Integration (`aem-assets-integration`)](#install-the-aem-assets-integration-extension).
1. [Configure Commerce Service Connector](#configure-the-commerce-services-connector) para conectar su instancia de Adobe Commerce y con los servicios que permiten la transmisión de datos entre Adobe Commerce y AEM Assets.
1. [Configuración de eventos de Adobe I/O para Commerce](#configure-adobe-io-events-for-commerce)
1. [Obtener credenciales de autenticación para el acceso a API](#get-authentication-credentials-for-api-access)

## Instalación de la extensión de AEM Assets Integration

>[!BEGINSHADEBOX]

**Requisito previo**

- Acceda a [repo.magento.com](https://repo.magento.com/admin/dashboard) para instalar la extensión. Para obtener la generación de claves y los derechos necesarios, consulta [Obtener tus claves de autenticación](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys). Para instalaciones en la nube, consulte la [Guía de Commerce en infraestructura en la nube](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/authentication-keys)

- Acceso a la línea de comandos del servidor de aplicaciones de Adobe Commerce.

>[!ENDSHADEBOX]

Instale la última versión de la extensión AEM Assets Integration (`aem-assets-integration`) en un Adobe Commerce que ejecute Adobe Commerce 2.4.4 o posterior. AEM La integración de recursos de la se entrega como un metapaquete de composición desde el repositorio [repo.magento.com](https://repo.magento.com/admin/dashboard).

>[!BEGINTABS]

>[!TAB Infraestructura en la nube]

Utilice este método para instalar la extensión [!DNL AEM Assets Integration] para una instancia de Commerce Cloud.

1. En la estación de trabajo local, cambie al directorio del proyecto para su proyecto de Adobe Commerce en la nube.

   >[!NOTE]
   >
   >Para obtener información sobre cómo administrar los entornos de proyecto de Commerce localmente, consulte [Administración de ramas con la CLI](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) en la _Guía del usuario de Adobe Commerce on Cloud Infrastructure_.

1. Consulte la rama de entorno para actualizar con la CLI de Adobe Commerce Cloud.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Añada la extensión AEM Assets Integration for Commerce.

   ```shell
   composer require "magento/aem-assets-integration" "<version-tbd>" --no-update
   ```

1. Actualizar dependencias del paquete.

   ```shell
   composer update "magento/aem-assets-integration"
   ```

1. Confirme y envíe los cambios de código para los archivos `composer.json` y `composer.lock`.

1. Agregue, confirme e inserte los cambios de código para los archivos `composer.json` y `composer.lock` en el entorno de nube.

   ```shell
   git add -A
   git commit -m "Install AEM Assets Integration extension for Adobe Commerce"
   git push origin <branch-name>
   ```

   Al insertar las actualizaciones, se inicia el [proceso de implementación en la nube de Commerce](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) para aplicar los cambios. Compruebe el estado de implementación desde el [registro de implementación](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

>[!TAB Local]

Utilice este método para instalar la extensión [!DNL AEM Assets Integration] para una instancia local.

1. Use el Compositor para añadir la extensión AEM Assets Integration for Commerce a su proyecto:

   ```shell
   composer require "magento/aem-assets-integration" --no-update
   ```

1. Actualice las dependencias e instale la extensión:

   ```shell
   composer update  "magento/aem-assets-integration"
   ```

1. Actualizar Adobe Commerce:

   ```shell
   bin/magento setup:upgrade
   ```

1. Borre la caché:

   ```shell
   bin/magento cache:clean
   ```

   >[!TIP]
   >
   >En algunos casos, especialmente al implementar en producción, puede que desee evitar borrar el código compilado, ya que puede tardar algún tiempo. Asegúrese de realizar una copia de seguridad del sistema antes de realizar cualquier cambio.

>[!ENDTABS]

## Configuración de Commerce Services Connector

Commerce Services Connector permite la sincronización de datos y la comunicación entre la instancia de Commerce, el servicio del motor de reglas de recursos y otros servicios de soporte.

>[!NOTE]
>
>La configuración del Conector de servicios de Commerce es un proceso único necesario para usar [Servicios SaaS de Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#availableservices). Si ya ha configurado el conector para otro servicio, puede ver la configuración existente desde el administrador de Commerce seleccionando **[!UICONTROL Systems]** > [!UICONTROL Services] > **[!UICONTROL Commerce Services Connector]**.

Para transmitir datos entre la instancia de Adobe Commerce y los servicios que habilitan la integración de AEM Assets, configure el conector de servicios de Commerce con lo siguiente:

- Configure la instancia de Commerce con las claves de API de producción y de zona protegida para la autenticación.
- Especifique un espacio de datos (identificador SaaS) para el almacenamiento seguro en la nube.
- Inicie sesión en la misma organización de IMS que utiliza para acceder a AEM Assets y establecer la conexión entre su conjunto de datos y Adobe Experience Platform.

Para obtener instrucciones detalladas, consulte [Conector de servicios de Commerce](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#organizationid).

Al configurar Commerce Services Connector, el sistema genera los ID de proyecto y base de datos SaaS. Necesita estos identificadores durante el proceso de incorporación del inquilino.

![Id. de espacio de datos y proyecto SaaS para la integración de AEM Assets](assets/aem-saas-project-config.png){width="600" zoomable="yes"}

## Configuración de eventos de Adobe I/O para Commerce

La integración de AEM Assets utiliza el servicio Eventos de Adobe I/O para enviar datos de evento personalizados entre la instancia de Commerce y el Experience Cloud. Los datos de evento se utilizan para coordinar los flujos de trabajo de la integración de AEM Assets.

>[!BEGINSHADEBOX]

**Requisito previo**

- Asegúrese de que RabbitMQ esté habilitado y atento a eventos.
   - [Configuración de RabbitMQ para Adobe Commerce local](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)
   - [Configuración de RabbitMQ para Adobe Commerce en la infraestructura en la nube](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)

>[!ENDSHADEBOX]

>[!NOTE]
>
>Para obtener información detallada sobre los eventos de Adobe I/O para Commerce, consulte la documentación de [Eventos de Adobe I/O para Commerce](https://developer.adobe.com/commerce/extensibility/events/) en el sitio de Adobe Developer.

La configuración requiere los siguientes pasos.

1. Habilite el módulo Eventos de Commerce configurando los eventos de Adobe I/O en el servidor de aplicaciones y en el administrador.
1. Habilite la sincronización de datos entre Adobe Commerce y AEM Assets mediante la API del servicio del motor de reglas de Assets para configurar la conexión.
1. Habilite la integración de AEM Assets en el Administrador.

### Habilitar el marco de eventos de Commerce

Habilite el marco de trabajo de eventos de Commerce siguiendo las instrucciones del entorno en el que se implementa el proyecto de Commerce.

>[!BEGINTABS]

>[!TAB Infraestructura en la nube]

1. Habilite el servicio Eventos de Adobe I/O desde el menú [!DNL Store Settings Configuration].

   1. Desde el administrador, vaya a **[!UICONTROL Stores]** > [!UICONTROL Settings] > **[!UICONTROL Configuration]** > **[!UICONTROL Adobe Services]** > **Eventos de Adobe I/O**.

   1. Expandir **[!UICONTROL Commerce events]**.

   1. Establezca **[!UICONTROL Enabled]** en `Yes`.

      ![Configuración de administración de Commerce de eventos de Adobe I/O: habilitar eventos de Commerce](assets/aem-enable-io-event-admin-config.png){width="600" zoomable="yes"}

      >[!NOTE]
      >
      >[Habilite cron](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#check-cron-and-message-queue-configuration) para que Commerce pueda enviar eventos a los extremos de la API a fin de administrar la comunicación y los flujos de trabajo para la integración.

1. Actualice la configuración del proyecto en la nube.

   1. Agregue el archivo `app/etc/config.php` a su repositorio de trabajo:

   ```shell
   git add app/etc/config.php
   ```

   1. Ejecute el comando `composer info magento/ece-tools` para determinar su versión de ece-tools. Si la versión es menor que `2002.1.13`, [actualice a la versión más reciente](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/dev-tools/ece-tools/update-package).

   1. Habilitar eventos en el archivo `.magento.env.yaml`:

      ```yaml
      stage:
         global:
            ENABLE_EVENTING: true
      ```

   1. Transfiera y envíe los archivos actualizados al entorno de Cloud.

>[!TAB Local]

1. Habilite el servicio Eventos de Adobe I/O desde el menú [!DNL Store Settings Configuration].

   1. Desde el administrador, vaya a **[!UICONTROL Stores]** > [!UICONTROL Settings] > **[!UICONTROL Configuration]** > **[!UICONTROL Adobe Services]** > **Eventos de Adobe I/O**.

   1. Expandir **[!UICONTROL Commerce events]**.

   1. Establezca **[!UICONTROL Enabled]** en `Yes`.

      ![Configuración de administración de Commerce de eventos de Adobe I/O: habilitar eventos de Commerce](assets/aem-enable-io-event-admin-config.png){width="600" zoomable="yes"}

      >[!NOTE]
      >
      >[Habilite los trabajos cron](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#check-cron-and-message-queue-configuration) para que Commerce AEM pueda enviar eventos para administrar la comunicación y los flujos de trabajo entre los recursos de los recursos y Commerce.

>[!ENDTABS]

## Obtener credenciales de autenticación para el acceso a API

La integración de AEM Assets para Commerce requiere credenciales de autenticación de OAuth para permitir el acceso de la API a la instancia de Commerce. Necesita estas credenciales para registrar el proyecto de Commerce con el servicio del motor de reglas de Assets durante la incorporación del inquilino y para enviar solicitudes de API para administrar recursos entre Adobe Commerce y AEM Assets.

Para generar las credenciales, agregue la integración a la instancia de Commerce y actívela.

### Añadir la integración al entorno de Commerce

1. Desde el administrador, ve a **Sistema** > Extensiones > **Integraciones** y luego haz clic en **Agregar nueva integración**.

1. Introduzca información sobre la integración.

   En la sección **General**, solo especifique la integración **Nombre** y **Correo electrónico**. Utilice el correo electrónico para una cuenta de Adobe IMS con acceso a la organización en la que se implementan Commerce y Experience Manager Assets.

   ![Integración de AEM Assets para la configuración de administración de Commerce](assets/aem-add-commerce-integration.png){width="600" zoomable="yes"}

1. Comprueba tu identidad haciendo clic en **Confirmar identidad**.

   El sistema comprueba su identidad autenticándose en el Experience Cloud con su ID de Adobe.

1. Configure los recursos de API.

   1. En el panel izquierdo, haga clic en **[!UICONTROL API]**.
E
   1. Seleccione el medio externo **[!UICONTROL Catalog > Inventory > Products > External Media]**.

   ![Configuración de integración de administración para recursos de API](assets/aem-commerce-integration-api-resources.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save]**.

### Generar credenciales

En la página Integraciones, genere las credenciales de autenticación de OAuth haciendo clic en **Activar** para la integración de Assets. Necesita estas credenciales para registrar el proyecto de Commerce con el servicio del motor de reglas de Assets y enviar solicitudes de API para administrar recursos entre Adobe Commerce y AEM Assets.

1. En la página Integraciones, genere las credenciales haciendo clic en **[!UICONTROL Activate]**.

   ![Activar la configuración de Commerce para la integración de Assets](assets/aem-activate-commerce-integration.png){width="600" zoomable="yes"}

1. Guarde las credenciales de la clave del consumidor y el token de acceso para usarlos más adelante.

![Credenciales de OAuth para autenticar solicitudes de API](./assets/aem-commerce-integration-credentials.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Done]**.

>[!NOTE]
>
>También puede generar credenciales de autenticación mediante las API de Adobe Commerce. Para obtener más información sobre este proceso y sobre la autenticación basada en OAuth para Adobe Commerce, consulte [Autenticación basada en OAuth](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) en la documentación de Adobe Developer.
