---
title: '[!UICONTROL General] &gt; [!UICONTROL New Relic Reporting]'
description: Revise la configuración en la página [!UICONTROL General] &gt; [!UICONTROL New Relic Reporting] del administrador de Commerce.
exl-id: d6bf4810-81a3-420d-abc9-9b87c1e92551
feature: Configuration, System, Reporting
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL New Relic Reporting]

{{config}}

>[!NOTE]
>Estas opciones de configuración no se aplican a Adobe Commerce en la infraestructura de la nube.
>
>Si está en el plan Pro, New Relic ya está [preconfigurado y habilitado de manera predeterminada](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). Si se encuentra en el plan inicial, debe completar los [pasos de configuración de New Relic](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) que forman parte del proceso de instalación.

## [!UICONTROL General]

![General](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/en/docs/commerce-admin/start/reporting/new-relic-reporting) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | Vista de tienda | Determina si la tienda se puede usar con los informes de [!DNL New Relic]. Opciones: `Yes` / `No` |
| [!UICONTROL New Relic API URL] | Vista de tienda | Dirección URL donde se implementan las API de New Relic. Por ejemplo: `https://api.newrelic.com/deployments.xml` |
| URL de API de perspectivas | Vista de tienda | Dirección URL donde se implementan las API de Insights. Utilice el símbolo de porcentaje (%) para representar su ID de cuenta. Por ejemplo: `https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | Vista de tienda | Identificador de cuenta asignado a su cuenta de [!DNL New Relic]. |
| [!UICONTROL New Relic Application ID] | Vista de tienda | Identificador de aplicación asignado a su cuenta de [!DNL New Relic] para la integración de Commerce. |
| [!UICONTROL New Relic API Key] | Vista de tienda | La clave que se le asignó para obtener acceso a la API [!DNL New Relic]. |
| [!UICONTROL Insights API Key] | Vista de tienda | La clave asignada para obtener acceso a Insights. |
| [!UICONTROL New Relic Application Name] | Vista de tienda | El nombre que asignó a su integración con [!DNL New Relic]. |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | Vista de tienda | Opción para enviar a New Relic los datos de informes recopilados para la tienda y el administrador como aplicaciones independientes. Esta opción requiere un nombre escrito para [!UICONTROL New Relic Application Name]. La función anexa el nombre de la aplicación con un guion bajo a los datos recopilados de la aplicación. Por ejemplo: `MyStore_Adminhtml`, `MyStore_frontend` |

{style="table-layout:auto"}

## [!UICONTROL Cron]

![Cron](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/tools/cron) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | Vista de tienda | Determina si [!DNL New Relic] informes se pueden ejecutar según lo programado con [Cron](../../systems/cron.md). Opciones: `Yes` / `No` |

{style="table-layout:auto"}
