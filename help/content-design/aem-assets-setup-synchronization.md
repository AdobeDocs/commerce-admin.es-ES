---
title: Configuración de la integración
description: Obtenga información sobre cómo conectar los proyectos de Adobe Commerce y Experience Manager Assets para habilitar la sincronización de recursos entre estos dos sistemas.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: 8db3e4b039ed8e020a1a2400e400df01c34f1943
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# Configuración de la integración

Configure la integración conectando Commerce a la instancia de AEM Assets y seleccionando la estrategia de coincidencia para la sincronización de recursos.

Después de identificar el proyecto de AEM Assets, seleccione la regla de coincidencia para sincronizar los recursos entre Adobe Commerce y los AEM Assets.

- **[!UICONTROL Match by product SKU]**: regla predeterminada que coincide con el SKU de los metadatos del recurso con el [SKU del producto de Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/glossary#sku) para garantizar que los recursos estén asociados con los productos correctos.

- **[!UICONTROL Custom match]**: regla de coincidencia para escenarios más complejos o requisitos empresariales específicos que requieren una lógica de coincidencia personalizada. La implementación de la coincidencia personalizada requiere el desarrollo de código personalizado en Adobe Developer App Builder para definir cómo se comparan los recursos con los productos. Próximamente más detalles...

Para la configuración inicial, usa la regla predeterminada *Coincidir con el SKU del producto*.

## Requisitos previos

- [Instalación del paquete de AEM Assets](aem-assets-configure-aem.md)

- [Instale paquetes de Adobe Commerce](aem-assets-configure-commerce.md) para agregar la extensión y generar las credenciales y conexiones necesarias para usar la extensión.

- Cree un ticket de asistencia para solicitar la habilitación de AEM Assets para la integración de Commerce. En el ticket, incluya **[!UICONTROL Program ID]**, **[!UICONTROL Environment ID]** y **[!UICONTROL IMS Org ID]** para el entorno de creación de AEM Assets que desea conectar a Commerce.

  >[!TIP]
  >
  > (Opcional) Proporcione **[!UICONTROL Asset Selector IMS Client ID]** si está disponible. Consulte [ImsAuthProps](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app) en la documentación de *Selector de AEM Assets*.

## Configuración de la conexión

1. Obtenga el proyecto [Entorno de creación de AEM Assets](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) y el ID de entorno.

   1. Abra la consola AEM Sites y seleccione **[!UICONTROL Assets]**.

   1. Copie y guarde los identificadores de proyecto y entorno desde la dirección URL:<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`
1. En el Administrador de Commerce, abra la configuración Integración de AEM Assets.

   1. Vaya a **[!UICONTROL Store]** > Configuración > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**.

      La integración de ![AEM Assets habilitó la integración](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. Introduzca el entorno de AEM Assets **[!UICONTROL Program ID]** y **[!UICONTROL Environment ID]**.

   Edite los valores de configuración eliminando la selección de *[!UICONTROL Use system value]*.

1. Escriba **[!UICONTROL Asset Selector IMS Client ID]**, si está disponible.

   [Asset Selector IMS Client ID](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app#ims-auth-props) es requerido por [!UICONTROL Assets Selector], una característica de AEM Assets que permite a los usuarios incrustar recursos visuales directamente en páginas de productos de Commerce.

1. Seleccione [[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment) para autenticar solicitudes entre Commerce y el servicio de coincidencia de recursos.

1. Establezca **[!UICONTROL Integration enabled]** en `Yes` para permitir que Commerce acepte actualizaciones entrantes de los AEM Assets.

   Después de habilitar la integración, hay opciones de configuración adicionales disponibles para especificar criterios coincidentes de recursos.

1. Defina la regla de coincidencia para la sincronización de recursos.

   1. Seleccione **[!UICONTROL Match by product SKU]** o **[!UICONTROL Custom match (Requires App Builder)]**.

   1. Agregue el nombre de campo de metadatos [AEM Assets](aem-assets-configure-aem.md#configure-metadata) definido para las SKU de productos Commerce en el campo **[!UICONTROL Match by product SKU attribute name]**, `commerce:skus` por ejemplo.

1. Seleccione **[!UICONTROL Save Config]** para aplicar actualizaciones e iniciar la sincronización de recursos.

   La actualización de configuración crea un déclencheur con el proceso de sincronización inicial, lo que permite a Commerce aceptar las actualizaciones entrantes de los AEM Assets. El tiempo necesario para la sincronización depende del volumen de recursos y de las configuraciones específicas. La integración aprovecha los procesos automatizados para minimizar el tiempo necesario para la sincronización.

### Configuración de la URL del dominio personalizado

Si un comerciante establece un [nombre de dominio personalizado](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/custom-domain-names/add-custom-domain-name){target=_blank} en su panel de AEM, es necesario agregar esta **URL de dominio personalizado** en Commerce para que la integración de AEM Assets pueda utilizarlo.

1. Vaya a **[!UICONTROL Store]** > Configuración > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**.

   La integración de ![AEM Assets habilitó la integración](assets/aem-assets-view.png){width="600" zoomable="yes"}

1. Agregue la **URL de dominio personalizado** al campo **[!UICONTROL Asset Custom Domain]**.

1. Haga clic en **[!UICONTROL Save Config]** para aplicar actualizaciones e iniciar la sincronización de recursos.

## Siguiente paso

[Uso de AEM Assets con Commerce](aem-assets-manage.md)
