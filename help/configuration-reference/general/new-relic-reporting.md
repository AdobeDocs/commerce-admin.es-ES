---
title: '[!UICONTROL General] &gt; [!UICONTROL New Relic Reporting]'
description: Revise la configuración de en [!UICONTROL General] &gt; [!UICONTROL New Relic Reporting] de la administración de Commerce.
exl-id: d6bf4810-81a3-420d-abc9-9b87c1e92551
feature: Configuration, System, Reporting
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 4%

---

# [!UICONTROL General] > [!UICONTROL New Relic Reporting]

{{config}}

## [!UICONTROL General]

![General](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/reports/new-relic-reporting.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | Vista de tienda | Determina si la tienda se puede utilizar con [!DNL New Relic] Informes. Opciones: `Yes` / `No` |
| [!UICONTROL New Relic API URL] | Vista de tienda | Dirección URL donde se implementan las API de New Relic. Por ejemplo: `https://api.newrelic.com/deployments.xml` |
| URL de API de perspectivas | Vista de tienda | Dirección URL donde se implementan las API de Insights. Utilice el símbolo de porcentaje (%) para representar su ID de cuenta. Por ejemplo: `https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | Vista de tienda | El ID de cuenta asignado a su [!DNL New Relic] cuenta. |
| [!UICONTROL New Relic Application ID] | Vista de tienda | El ID de aplicación asignado a su [!DNL New Relic] cuenta para la integración de Commerce. |
| [!UICONTROL New Relic API Key] | Vista de tienda | La clave que se le ha asignado para obtener acceso al [!DNL New Relic] API. |
| [!UICONTROL Insights API Key] | Vista de tienda | La clave asignada para obtener acceso a Insights. |
| [!UICONTROL New Relic Application Name] | Vista de tienda | El nombre que ha asignado a su [!DNL New Relic] integración. |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | Vista de tienda | Opción para enviar a New Relic los datos de informes recopilados para la tienda y el administrador como aplicaciones independientes. Esta opción requiere un nombre escrito para [!UICONTROL New Relic Application Name]. La función anexa el nombre de la aplicación con un guion bajo a los datos recopilados de la aplicación. Por ejemplo: `MyStore_Adminhtml`, `MyStore_frontend` |

{style="table-layout:auto"}

## [!UICONTROL Cron]

![Cron](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://docs.magento.com/user-guide/system/cron.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | Vista de tienda | Determina si [!DNL New Relic] los informes se pueden ejecutar según lo programado con [Cron](../../systems/cron.md). Opciones: `Yes` / `No` |

{style="table-layout:auto"}
