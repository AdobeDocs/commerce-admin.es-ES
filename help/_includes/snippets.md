---
title: Fragmentos
description: Se han reutilizado notas y elementos visuales para anotar una función o página que se aplica a una edición específica
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Fragmentos

## Función de solo EE {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Función Adobe Commerce" src="../assets/adobe-logo.svg" width="20" height="20" /> Función exclusiva solo en Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Más información</a>)</td></tr>
</table>

## Función exclusiva de B2B {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Función B2B para Adobe Commerce" src="../assets/b2b.svg" width="20" height="20" /> Función exclusiva disponible solo con <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=en">B2B para Adobe Commerce</a></td></tr>
</table>

## Función de solo CE {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="función de Magento Open Source" src="../assets/open-source.svg" width="20" height="20" /> Se requiere un método alternativo para el Magento Open Source (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Más información</a>)</td></tr>
</table>

## Nota de autenticación de administración de IMS {#ims-admin-note}

>[!NOTE]
>
>Los comerciantes de Adobe Commerce que tengan un Adobe ID y deseen un inicio de sesión optimizado en los productos de Adobe Commerce y Adobe Business pueden integrar la autenticación de Commerce Admin con el flujo de trabajo de autenticación de IMS de Adobe. Una vez habilitada esta integración en la tienda de Commerce, los usuarios administradores deben usar sus credenciales de Adobe para iniciar sesión, no sus credenciales de cuenta de Commerce. Consulte [Información general sobre la integración de Adobe Commerce con Adobe IMS](/help/getting-started/adobe-ims-integration-overview.md).

## Nota de las API GTag {#gtag-api-note}

>[!NOTE]
>
>A partir de la versión 2.4.5, la integración de servicios de Google se actualiza para admitir el uso de las API de GTag. GTag es un mecanismo unificado para la integración con la funcionalidad de Google para páginas web y admite las funciones y oportunidades más recientes para el seguimiento y la administración de contenido mediante los servicios de Google. Para obtener más información, consulte la [Documentación para desarrolladores de Google Analytics](https://developers.google.com/analytics/devguides/collection/gtagjs).

## Reescribir URL omitir nota automáticamente {#url-rewrite-skip}

>[!NOTE]
>
>Cuando se habilitan las redirecciones automáticas y se guarda una categoría, todas las reescrituras de productos y categorías se generan en tiempo real y se almacenan en tablas de reescritura de forma predeterminada. Este proceso podría provocar problemas de rendimiento significativos en las categorías con muchos productos asignados. La solución consiste en cambiar este valor predeterminado y omitir la generación de reescrituras de categoría/productos mediante URL de productos para guardar la categoría. En este caso, las reescrituras de productos se generan solo para la URL del producto canónico. Consulte [Redirecciones automáticas de productos](/help/merchandising-promotions/url-redirect-product-automatic.md) para obtener más información.

## Nota de parámetros de reescritura de URL {#url-rewrite-params}

>[!IMPORTANT]
>
>En el proceso de redirección, todos los parámetros de GET especificados en la dirección URL se eliminan por motivos de seguridad.

## Nueva regla de precios {#new-price-rule}

>[!NOTE]
>
>Las reglas de precios se procesan automáticamente con otras reglas del sistema. La frecuencia de procesamiento depende del [configuración de cron](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html). Cuando cree una regla de precios, deje tiempo suficiente para que entre en el sistema. Cuando esté seguro de que está en el sistema, pruebe la regla.

## Ajustes de configuración {#config}

Para acceder a las opciones de configuración de la tienda, elija **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**desde el_ Administrador _barra lateral.

## Desaprobación de API de UPS {#ups-api}

>[!IMPORTANT]
>
>A partir de junio de 2024, los comerciantes de Adobe Commerce ya no podrán realizar transacciones con la integración actual de UPS. Esto se debe a que las API de United Parcel Service (UPS) utilizadas por la integración nativa de Adobe Commerce no admiten actualmente el modelo de seguridad OAuth 2.0 requerido. Para obtener más información, consulte [_Guía de migración de claves de acceso al portal para desarrolladores_](https://developer.ups.com/oauth-developer-guide). <br/>
>
>Los comerciantes deben [aplicar una actualización de parche de calidad](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html) a su almacén para migrar de la API de SOAP a la API de RESTful, que admite protocolos de autenticación OAuth 2.0.


## Documentación disponible {#docs-links}

| Recurso de documentación | Descripción |
|----------------------- | ----------- |
| [Documentación de Adobe Commerce 2.4 Merchant](../landing/home.md) | Documentación centrada en el comerciante para Adobe Commerce y Magento Open Source |
| [Servicios para la documentación de Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) | Documentación para ofrecer compatibilidad con una colección de servicios que ayudan a los comerciantes a integrar componentes clave de su negocio en su tienda. |
| [Guía de Commerce en la infraestructura de Cloud](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | Procedimientos paso a paso para implementar Adobe Commerce en una plataforma en la nube administrada y automatizada. |
| [Guías operativas de Adobe Commerce 2.4](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | Documentación del sistema sobre los conceptos, procesos, herramientas y prácticas recomendadas para desarrollar, implementar y mantener proyectos implementados en plataformas Adobe Commerce y de Magento Open Source. |
| [Documentación para desarrolladores de Adobe Commerce 2.4](https://developer.adobe.com/commerce/docs) | Documentación centrada en el desarrollador que se utiliza para crear y personalizar Adobe Commerce o Magento Open Source |

{style="table-layout:auto"}
