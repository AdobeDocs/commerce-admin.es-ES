---
title: Introducción a los sistemas de administración
description: Obtenga información sobre los sistemas, herramientas y funciones que el administrador de la tienda puede utilizar para administrar de forma eficaz los sitios, los datos, las integraciones y los usuarios administradores.
exl-id: 52792a89-8f6f-4230-9a04-e193b3943410
TQID: https://experienceleague.adobe.com/E-6P-9RyoWsRXfdnU-nT4sEMLd3Pmlkynvd1q2Dqpms
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: cc250cf1-34eb-4863-80d0-d170d45ea067
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 471
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
- [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."} **Herramientas del sistema**: realice operaciones de administración rutinarias de [índice](index-management.md) y [caché](cache-management.md), [realice copias de seguridad](backups.md) del sistema, administre [operaciones programadas](data-scheduled-import-export.md) y use una variedad de [herramientas para desarrolladores](developer-tools.md).
- **Transferencia de datos** - Usa las herramientas de [transferencia de datos](data-transfer.md) para importar y exportar datos, así como para administrar datos de productos, precios, clientes y tasas de impuestos.
- **Integraciones**: establezca la ubicación de las credenciales de OAuth y redirija la URL para [integraciones de terceros](integrations.md), e identifique los recursos de API disponibles.
- **Registros de acciones** - ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Accede a los registros ([registros de acciones](action-log.md)) para los cambios realizados por los usuarios administradores que trabajan en tu tienda.
- [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."} **Herramientas de soporte** - ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) [Informes del sistema](support.md#access-system-reports)) están diseñadas para identificar problemas conocidos en su sistema. Pueden utilizarse como recurso durante los procesos de desarrollo y optimización, y como herramienta de diagnóstico para ayudar a nuestro equipo de asistencia a identificar y resolver problemas.
