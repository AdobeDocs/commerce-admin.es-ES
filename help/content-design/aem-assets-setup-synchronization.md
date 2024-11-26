---
title: Habilitar sincronización de recursos
description: Obtenga información sobre cómo conectar los proyectos de Adobe Commerce y Experience Manager Assets para habilitar la sincronización de recursos entre estos dos sistemas.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: e069f0a99ed9289b22cafe06fe2f787912cbba23
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# Habilitar sincronización de recursos

AEM Durante el proceso de habilitación, registre el ID de inquilino para el proyecto mediante el ID de programa y entorno para el entorno de creación de. Estos ID identifican el proyecto de AEM Assets al que se está conectando y proporcionan las credenciales para habilitar la comunicación entre Commerce y los entornos de AEM Assets.

AEM Después de identificar el proyecto de recursos de la, seleccione la regla coincidente para sincronizar los recursos entre Adobe Commerce y los AEM Assets.

- **[!UICONTROL Match by product SKU]**: regla predeterminada que coincide con el SKU de los metadatos del recurso con el [SKU del producto de Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/operational-playbook/glossary#sku) para garantizar que los recursos estén asociados con los productos correctos.

- **[!UICONTROL Custom match]**: regla de coincidencia para escenarios más complejos o requisitos empresariales específicos que requieren una lógica de coincidencia personalizada. La implementación de la coincidencia personalizada requiere el desarrollo de código personalizado en Adobe Developer App Builder para definir cómo se comparan los recursos con los productos. Próximamente más detalles...

Para la incorporación inicial, usa la regla predeterminada *Coincidir con el SKU del producto*.

## Requisitos previos

- [AEM Configuración de Experience Manager Assets para administrar recursos de Commerce](#aem-assets-configure-aem)
- [Instale y configure la integración de AEM Assets para Commerce](#aem-assets-configure-commerce.md) a fin de agregar la extensión y generar las credenciales y conexiones necesarias para usar la extensión.

## Configuración de la conexión

1. Obtenga el proyecto [Entorno de creación de AEM Assets](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) y el ID de entorno.

   1. Abra la consola AEM Sites y seleccione **[!UICONTROL Assets]**.

   1. Copie y guarde los identificadores de proyecto y entorno desde la dirección URL: <br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|

1. En el Administrador de Commerce, abra la configuración Integración de AEM Assets.

   1. Vaya a **[!UICONTROL Store]** > Configuración > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**.

      La integración de ![AEM Assets habilitó la integración](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. Introduzca el entorno de AEM Assets **[!UICONTROL Program ID]** y **[!UICONTROL Environment ID]**.

1. Escriba el **[!UICONTROL Asset Selector IMS Client ID].

   El [ID de IMS](../getting-started/adobe-ims-config.md) le permite integrar AEM Assets con Page Builder.

1. Seleccione [[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)** para autenticar solicitudes entre Commerce y el servicio de coincidencia de recursos.

1. Permitir que Commerce acepte actualizaciones entrantes de AEM Assets estableciendo **[!UICONTROL Integration enabled]** en `Yes`.

   Después de activar la integración, configure la regla de coincidencia de recursos.

   ![Integración de AEM Assets selecciona la regla de coincidencia de recursos](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Defina la regla de coincidencia para la sincronización de recursos.

   1. Seleccione **[!UICONTROL Match by product SKU]**.

   1. Agregue el nombre de campo de metadatos [AEM Assets](aem-assets-configure-aem.md#configure-metadata) definido para las SKU de productos Commerce en el campo **[!UICONTROL Match by product SKU attribute name]**, `commerce:skus` por ejemplo.

   ![Integración de AEM Assets selecciona la regla de coincidencia de recursos](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Seleccione **[!UICONTROL Save Config]** para aplicar actualizaciones e iniciar la sincronización de recursos
