---
title: Requisitos previos de descubrimiento de productos AI
description: Revise los requisitos para el enriquecimiento del catálogo y el enriquecimiento de PDP, e instale la extensión de enriquecimiento compartido en Adobe Commerce en la infraestructura en la nube o en línea.
role: Admin, Developer
source-git-commit: 9e234eb68fe34171d9e5cf95e8cdab5c31825492
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 0%
---
# Requisitos previos

Antes de usar Enriquecimiento del catálogo o Enriquecimiento de PDP, confirme los requisitos aplicables a cada implementación y, a continuación, complete la configuración de su plataforma de Commerce.

## Requisitos para todas las implementaciones {#all-deployments}

| Requisito | Se aplica a | Detalles |
| --- | --- | --- |
| Optimizar en Edge | Enriquecimiento de PDP | Requerido. Optimizar en Edge ofrece los datos de productos enriquecidos a los agentes de IA. Consulte la guía [Optimizar en Edge](https://experienceleague.adobe.com/es/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn). |
| Reenvío de registros | Ambos flujos de trabajo | Opcional. Habilita recomendaciones de enriquecimiento basadas en tráfico auténtico. Sin ella, aún puede seleccionar productos o páginas de productos manualmente. Consulte la [Guía de reenvío de registros](https://experienceleague.adobe.com/es/docs/brand-visibility/using/log-forwarding/log-forwarding-overview). |
| Escaparate rastreable | Enriquecimiento del catálogo | Necesario para recomendaciones basadas en rastrees. Los bots agénticos y orientados a LLM deben poder acceder a las páginas de productos. |
| Acceso de [!DNL Adobe Admin Console] | Enriquecimiento del catálogo | Requerido. Durante la instalación, [!DNL Adobe Commerce] comprueba si su organización ha firmado el controlador GenAI o se ha excluido de los servicios de IA subyacentes. |

<!--
TBD (SME): The Optimize at Edge guide is a Brand Visibility reference, not a Commerce setup guide. Add Commerce-specific Optimize at Edge setup instructions (this might be automated by GA).
TBD (SME): Confirm whether the Admin Console and GenAI rider check also applies to PDP enrichment.
-->

## Configurar la plataforma de Commerce {#set-up}

>[!BEGINTABS]

>[!TAB Commerce en infraestructura de nube o local]

Para [!DNL Adobe Commerce] en la infraestructura en la nube o en línea, instale la extensión de enriquecimiento compartido, que permite el enriquecimiento del catálogo y el enriquecimiento de PDP.

**Antes de comenzar:**

- [!DNL Adobe Commerce] 2.4.7 o posterior en PHP 8.3 o posterior. Ver [Notas de la versión](release-notes.md).
- Una organización [!DNL Adobe IMS]. Si su organización no tiene ninguna, consulte la [descripción general de la integración de Adobe IMS](https://experienceleague.adobe.com/es/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview). El enriquecimiento del catálogo utiliza el token de acceso de IMS del usuario administrador que ha iniciado sesión. El inicio de sesión solo con un nombre de usuario y una contraseña de Commerce no proporciona este token.
- Acceso desde la línea de comandos al servidor de aplicaciones de Commerce y permiso para descargar paquetes de `repo.magento.com`.

**Instalar y comprobar:**

1. Si ni [!DNL Live Search] ni [!DNL Product Recommendations] están habilitados, agregue [!DNL Catalog Service] desde el directorio del proyecto de Commerce:

   ```bash
   composer require magento/catalog-service --no-update
   composer update magento/catalog-service
   ```

   [!DNL Catalog Service] se instala automáticamente con [!DNL Live Search] y [!DNL Product Recommendations], así que omita este paso si alguno de los servicios está habilitado.

1. Si aún no está configurado para otro servicio de Commerce, configure [Commerce Services Connector](https://experienceleague.adobe.com/es/docs/commerce/user-guides/integration-services/saas) con claves de API y un espacio de datos SaaS.

1. Añada la extensión de enriquecimiento compartida:

   ```bash
   composer require magento/module-catalog-enrichment --no-update
   composer update magento/module-catalog-enrichment
   ```

1. Implemente los cambios:

   - **Infraestructura en la nube:** Confirme y envíe los cambios a `composer.json` y `composer.lock`.
   - **Local:** Actualice la aplicación y borre la caché:

     ```bash
     bin/magento setup:upgrade
     bin/magento cache:clean
     ```

1. En el Administrador, vaya a **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Feed Sync Status]** y confirme que Commerce exporta los datos del catálogo.

   El número de registros de producto enviados correctamente debe coincidir con los registros de origen, sin errores ni envíos en espera. Para los registros con errores, revise los detalles del error, resuelva el problema y programe una resincronización para los registros afectados.

1. Vaya a **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Management Dashboard]** y confirme que los datos de catálogo esperados están disponibles en [!DNL Catalog Service].

Para obtener detalles de estado y solucionar problemas, consulte [Supervisar el estado de las fuentes de datos](/help/systems/data-feed-sync-status.md#monitor-data-feed-status).

>[!TAB Adobe Commerce as a Cloud Service]

Para [!DNL Adobe Commerce as a Cloud Service], la instalación de [!DNL Catalog Service], el enriquecimiento del catálogo y el enriquecimiento de PDP se administran durante el aprovisionamiento de la cuenta.

Complete los [requisitos para todas las implementaciones](#all-deployments) que se aplican a los flujos de trabajo que planea utilizar.

<!-- TBD (SME): Confirm whether merchants on Adobe Commerce as a Cloud Service should verify catalog data on the Data Management Dashboard, and whether the IMS and Admin Console requirements apply. -->

>[!ENDTABS]

## Siguiente paso {#next-step}

[Configure las opciones de enriquecimiento](settings.md) para conectar su instancia de Commerce al descubrimiento de productos de IA.
