---
title: Introducción a los sistemas de administración
description: Obtenga información sobre los sistemas, herramientas y funciones que el administrador de la tienda puede utilizar para administrar de forma eficaz los sitios, los datos, las integraciones y los usuarios administradores.
exl-id: 52792a89-8f6f-4230-9a04-e193b3943410
source-git-commit: 5517bb16a8f7c8aa2f9f057df773f142302a69c7
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Introducción a los sistemas de administración

El administrador de la tienda es el back office seguro donde los comerciantes configuran productos y promociones, administran pedidos y realizan otras tareas administrativas. Todas las tareas de configuración básicas y las operaciones de administración de tiendas se realizan desde el administrador. También hay funciones que proporcionan compatibilidad con varias funciones de tienda que los administradores pueden administrar para sus organizaciones.

## Variables y comunicaciones con los clientes

Las variables son fragmentos de información que se pueden crear una vez y utilizar en varios lugares. Su tienda incluye muchas variables predefinidas que se pueden usar fácilmente para personalizar las plantillas de [correo electrónico](email-templates.md) y [boletín](../merchandising-promotions/newsletter-template.md), así como otros tipos de [contenido](../content-design/introduction.md#content). También puede crear variables personalizadas para incorporar información específica para sus necesidades.

- [Variables predefinidas](variables-predefined.md)
- [Variables personalizadas](variables-custom.md)

Una de las tareas a completar antes de lanzar su tienda es revisar las plantillas de correo electrónico que se utilizan para todas las comunicaciones enviadas desde su tienda para asegurarse de que reflejen su marca. Esto incluye la personalización de las plantillas de correo electrónico y [newsletter](../merchandising-promotions/newsletter-template.md), y las facturas y los albaranes de PDF. También incluye la personalización del contenido con variables y [etiquetas de marcado](markup-tags.md).

## Gestión de operaciones

El administrador también admite varias tareas para que los administradores de sistemas administren los usuarios administradores dentro de su organización y operen la tienda. Estas incluyen las siguientes herramientas:

- **Cuentas de usuario y permisos de administrador** - Administrar cuentas de usuario [de administrador](permissions-users-all.md), así como las [funciones y permisos](permissions-user-roles.md) asociados que controlan su acceso a los sitios y áreas funcionales del administrador.
- **Sesiones de administración y restricciones de sitios web**: revise las prácticas recomendadas de [seguridad](security.md), y aprenda a administrar sesiones de administración y credenciales, implementar CAPTCHA y administrar restricciones de sitios web.
- [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."} **Herramientas del sistema**: realice operaciones de administración rutinarias de [índice](index-management.md) y [caché](cache-management.md), [realice copias de seguridad](backups.md) del sistema, administre [operaciones programadas](data-scheduled-import-export.md) y use una variedad de [herramientas para desarrolladores](developer-tools.md).
- **Transferencia de datos** - Usa las herramientas de [transferencia de datos](data-transfer.md) para importar y exportar datos, así como para administrar datos de productos, precios, clientes y tasas de impuestos.
- **Integraciones**: establezca la ubicación de las credenciales de OAuth y redirija la URL para [integraciones de terceros](integrations.md), e identifique los recursos de API disponibles.
- **Registros de acciones** - ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Accede a los registros ([registros de acciones](action-log.md)) para los cambios realizados por los usuarios administradores que trabajan en tu tienda.
- [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."} **Herramientas de soporte** - ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) [Informes del sistema](support.md#access-system-reports)) están diseñadas para identificar problemas conocidos en su sistema. Pueden utilizarse como recurso durante los procesos de desarrollo y optimización, y como herramienta de diagnóstico para ayudar a nuestro equipo de asistencia a identificar y resolver problemas.
