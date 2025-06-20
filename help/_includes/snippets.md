---
title: Fragmentos
description: Se han reutilizado notas y elementos visuales para anotar una función o página que se aplica a una edición específica
source-git-commit: 0ffeaa42e0207322da1b55a9fd6b6b2cf24ff4ba
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 0%

---

# Fragmentos

## Función de solo EE {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Función Adobe Commerce" src="../assets/adobe-logo.svg" width="20" height="20" /> Característica exclusiva solamente en Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=es#product-editions">Más información</a>)</td></tr>
</table>

## Función exclusiva de B2B {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Función Adobe Commerce B2B" src="../assets/b2b.svg" width="20" height="20" /> Característica exclusiva disponible solo con <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=es">Adobe Commerce B2B</a></td></tr>
</table>

## Función de solo CE {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Función Magento Open Source" src="../assets/open-source.svg" width="20" height="20" /> Se requiere un método alternativo para Magento Open Source (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=es#product-editions">Más información</a>)</td></tr>
</table>

## Nota de autenticación de administración de IMS {#ims-admin-note}

>[!NOTE]
>
>Los comerciantes de Adobe Commerce que tengan un Adobe ID y deseen un inicio de sesión optimizado en los productos de Adobe Commerce y Adobe Business pueden integrar la autenticación de Commerce Admin con el flujo de trabajo de autenticación IMS de Adobe. Una vez habilitada esta integración en la tienda Commerce, los usuarios administradores deben usar sus credenciales de Adobe, no sus credenciales de cuenta de Commerce, para iniciar sesión. Consulte [Información general sobre la integración de Adobe Commerce con Adobe IMS](/help/getting-started/adobe-ims-integration-overview.md).

## Nota de las API GTag {#gtag-api-note}

>[!NOTE]
>
>A partir de la versión 2.4.5, la integración de servicios de Google se actualiza para admitir el uso de las API de GTag. GTag es un mecanismo unificado para la integración con la funcionalidad de Google para páginas web y admite las funciones y oportunidades más recientes para el seguimiento y la administración de contenido mediante los servicios de Google.

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
>Las reglas de precios se procesan automáticamente con otras reglas del sistema. La frecuencia de procesamiento depende de la [configuración de cron](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html?lang=es). Cuando cree una regla de precios, deje tiempo suficiente para que entre en el sistema. Cuando esté seguro de que está en el sistema, pruebe la regla.

## Ajustes de configuración {#config}

Para acceder a las opciones de configuración de la tienda, elige **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;en la barra lateral de_ Admin _.

## Desaprobación de API de UPS {#ups-api}

>[!IMPORTANT]
>
>A partir de junio de 2024, los comerciantes de Adobe Commerce ya no podrán realizar transacciones con la integración actual de UPS. Esto se debe a que las API de United Parcel Service (UPS) utilizadas por la integración nativa de Adobe Commerce no admiten actualmente el modelo de seguridad OAuth 2.0 requerido. Para habilitar la integración, [cree una aplicación en la plataforma para desarrolladores de UPS](https://developer.ups.com/get-started) para obtener las credenciales necesarias para OAuth 2.0. Use las nuevas credenciales como `username` y `password` en la configuración de envío de UPS de Commerce. Para obtener más información acerca del cambio del modelo de seguridad, consulte [Guía de migración de claves de acceso al portal para desarrolladores_](https://developer.ups.com/oauth-developer-guide). <br/>
>
>Los comerciantes deben [aplicar una actualización de parche de calidad](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html?lang=es) a su almacén para migrar de la API de SOAP a la API RESTful, que admite los protocolos de autenticación OAuth 2.0.


## Documentación disponible {#docs-links}

| Recurso de documentación | Descripción |
|----------------------- | ----------- |
| [Guías del usuario administrador de Adobe Commerce 2.4](../landing/home.md) | Documentación y recursos para comerciantes que trabajan en el administrador. |
| [Servicios para la documentación de Adobe Commerce](https://experienceleague.adobe.com/docs/commerce/user-guides/home.html?lang=es) | Documentación para ofrecer compatibilidad con una colección de servicios de comercialización que ayudan a los comerciantes a integrar componentes clave de su negocio en su tienda. |
| [Guía de infraestructura de Commerce en la nube](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html?lang=es) | Procedimientos paso a paso para implementar Adobe Commerce en una plataforma en la nube administrada y automatizada. |
| [Guías operativas de Adobe Commerce 2.4](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html?lang=es) | Documentación del sistema sobre los conceptos, procesos, herramientas y prácticas recomendadas para desarrollar, implementar y mantener Adobe Commerce en proyectos en la nube y locales. |
| [Documentación para desarrolladores de Adobe Commerce 2.4](https://developer.adobe.com/commerce/docs) | Documentación centrada en el desarrollador que se utiliza para personalizar Adobe Commerce e integrarla con sistemas de terceros. |

{style="table-layout:auto"}

## Compatibilidad B2B {#b2b-compatibility}

>[!IMPORTANT]
>
>Adobe Commerce B2B versión 1.4.2+ es compatible con PHP 8.2. Si actualiza la instancia de Commerce a la versión 2.4.7 o posterior, asegúrese de que la instancia utiliza la versión 8.2 de PHP para mantener la compatibilidad con la versión B2B de Adobe Commerce. Además, la versión B2B 1.4.2 o posterior no es compatible con [GraphQL Application Server](https://experienceleague.adobe.com/es/docs/commerce-operations/performance-best-practices/concepts/application-server).
