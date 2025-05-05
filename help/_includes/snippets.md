---
title: Snippets
description: Reused notes and visual elements to note a feature or page applying to a specific edition
source-git-commit: e82b979ee2c5f51caba6a2aa416c5f20dbce110a
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%

---

# Snippets

## EE only feature {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Función Adobe Commerce" src="../assets/adobe-logo.svg" width="20" height="20" /> Característica exclusiva solamente en Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Más información</a>)</td></tr>
</table>

## B2B only feature {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Adobe Commerce B2B feature" src="../assets/b2b.svg" width="20" height="20" /> Exclusive feature available only with <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=en">Adobe Commerce B2B</a></td></tr>
</table>

## Función de solo CE {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Función Magento Open Source" src="../assets/open-source.svg" width="20" height="20" /> Se requiere un método alternativo para Magento Open Source (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Más información</a>)</td></tr>
</table>

## Nota de autenticación de administración de IMS {#ims-admin-note}

>[!NOTE]
>
>Los comerciantes de Adobe Commerce que tengan un Adobe ID y deseen un inicio de sesión optimizado en los productos de Adobe Commerce y Adobe Business pueden integrar la autenticación de Commerce Admin con el flujo de trabajo de autenticación IMS de Adobe. Una vez habilitada esta integración en la tienda Commerce, los usuarios administradores deben usar sus credenciales de Adobe, no sus credenciales de cuenta de Commerce, para iniciar sesión. Consulte [Información general sobre la integración de Adobe Commerce con Adobe IMS](/help/getting-started/adobe-ims-integration-overview.md).

## Nota de las API GTag {#gtag-api-note}

>[!NOTE]
>
>A partir de la versión 2.4.5, la integración de servicios de Google se actualiza para admitir el uso de las API de GTag. GTag es un mecanismo unificado para la integración con la funcionalidad de Google para páginas web y admite las funciones y oportunidades más recientes para el seguimiento y la administración de contenido mediante los servicios de Google. Para obtener más información, consulte la [documentación para desarrolladores de Google Analytics](https://developers.google.com/analytics/devguides/collection/gtagjs).

## Reescribir URL omitir nota automáticamente {#url-rewrite-skip}

>[!NOTE]
>
>When automatic redirects are enabled and you save a category, all product and category rewrites are generated in real time and stored in rewrite tables by default. This process could result in significant performance issues for categories with many assigned products. The solution is to change this default and skip the generation of category/products URL rewrites of products for category save. In this case, product rewrites are generated only for the canonical product URL. Consulte [Redirecciones automáticas de productos](/help/merchandising-promotions/url-redirect-product-automatic.md) para obtener más información.

## Nota de parámetros de reescritura de URL {#url-rewrite-params}

>[!IMPORTANT]
>
>En el proceso de redirección, todos los parámetros de GET especificados en la dirección URL se eliminan por motivos de seguridad.

## Nueva regla de precios {#new-price-rule}

>[!NOTE]
>
>Las reglas de precios se procesan automáticamente con otras reglas del sistema. Processing frequency depends on the [cron configuration](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html). When you create a price rule, allow enough time for it to get into the system. WHen you are sure it is in the system, test the rule.

## Configuration settings {#config}

To access the store configuration settings, choose **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;from the_ Admin _sidebar.

## UPS API deprecation {#ups-api}

>[!IMPORTANT]
>
>A partir de junio de 2024, los comerciantes de Adobe Commerce ya no podrán realizar transacciones con la integración actual de UPS. Esto se debe a que las API de United Parcel Service (UPS) utilizadas por la integración nativa de Adobe Commerce no admiten actualmente el modelo de seguridad OAuth 2.0 requerido. Para habilitar la integración, [cree una aplicación en la plataforma para desarrolladores de UPS](https://developer.ups.com/get-started) para obtener las credenciales necesarias para OAuth 2.0. Use las nuevas credenciales como `username` y `password` en la configuración de envío de UPS de Commerce. Para obtener más información acerca del cambio del modelo de seguridad, consulte [Guía de migración de claves de acceso al portal para desarrolladores_](https://developer.ups.com/oauth-developer-guide). <br/>
>
>Los comerciantes deben [aplicar una actualización de parche de calidad](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html) a su almacén para migrar de la API de SOAP a la API RESTful, que admite los protocolos de autenticación OAuth 2.0.


## Documentación disponible {#docs-links}

| Recurso de documentación | Descripción |
|----------------------- | ----------- |
| [Adobe Commerce 2.4 Admin User Guides](../landing/home.md) | Documentation and resources for merchants working in the Admin. |
| [Services for Adobe Commerce Documentation](https://experienceleague.adobe.com/docs/commerce/user-guides/home.html) | Documentación para ofrecer compatibilidad con una colección de servicios de comercialización que ayudan a los comerciantes a integrar componentes clave de su negocio en su tienda. |
| [Guía de infraestructura de Commerce en la nube](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | Step-by-step procedures for deploying Adobe Commerce on a managed, automated hosting cloud platform. |
| [Adobe Commerce 2.4 Operational Guides](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | Systems documentation about the concepts, processes, tools, and best practices to develop, deploy, and maintain Adobe Commerce on Cloud and on-premises projects. |
| [Adobe Commerce 2.4 Developer Documentation](https://developer.adobe.com/commerce/docs) | Developer-focused documentation used to customize Adobe Commerce and integrate with third-party systems. |

{style="table-layout:auto"}

## Compatibilidad B2B {#b2b-compatibility}

>[!IMPORTANT]
>
>Adobe Commerce B2B versión 1.4.2+ es compatible con PHP 8.2. Si actualiza la instancia de Commerce a la versión 2.4.7 o posterior, asegúrese de que la instancia utiliza la versión 8.2 de PHP para mantener la compatibilidad con la versión B2B de Adobe Commerce. Además, la versión B2B 1.4.2 o posterior no es compatible con [GraphQL Application Server](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).
