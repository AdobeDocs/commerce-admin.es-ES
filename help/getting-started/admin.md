---
title: ¿Qué es el administrador?
description: Obtenga información acerca del administrador de [!DNL Commerce], el lugar donde los comerciantes configuran productos y promociones, administran pedidos y realizan otras tareas administrativas.
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
TQID: https://experienceleague.adobe.com/A0DuYohA907-EHXQ6fyy2Sz83Y6cFZ7PDY5SmtBa14Y
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
    internal-label: Accessibility
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
last-update: 2026-10-26
source-git-commit: 4cfd19db9b6689cf05be301b0c68018a42b8f7ec
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%
---
# ¿Qué es el administrador?

Su tienda _Admin_ es el back office protegido por contraseña donde usted, como comerciante, configura productos y promociones, administra pedidos y realiza otras tareas administrativas. Todas las tareas de configuración básicas y las operaciones de administración de tiendas se realizan desde _Admin_.

{{$include /help/_includes/admin-unified-experience-note.md}}

Para mayor seguridad, el inicio de sesión de _Admin_ está protegido por [autenticación de doble factor](../systems/security-two-factor-authentication.md) y se puede configurar para requerir un [CAPTCHA](../systems/security-captcha.md). Para obtener más información, ve a [Configuración de Admin Security](../systems/security-admin.md).

![Barra lateral de administración y panel](./assets/admin-dashboard.png){width="700" zoomable="yes"}

Las credenciales iniciales de [inicio de sesión](admin-signin.md) se configuraron durante la instalación de Adobe Commerce o Magento Open Source. Si olvida su contraseña, se puede enviar una contraseña temporal a la dirección de correo electrónico asociada a la cuenta. Para aumentar la seguridad, configure el almacén de modo que requiera un nombre de usuario que distinga mayúsculas de minúsculas y una contraseña segura.

Además de la cuenta de usuario Administrador predeterminada, su empresa puede crear [cuentas adicionales](../systems/permissions-users-all.md) que necesite para administrar las cuentas de cliente de tienda y soporte técnico. Cada cuenta puede asociarse con una [función](../systems/permissions-user-roles.md) y un nivel de acceso específicos, según lo que _necesite saber_ de la empresa. La dirección de correo electrónico asociada con cada cuenta de usuario de administrador debe ser única.

{{ims-admin-note}}

## Recopilación de datos de uso

La primera vez que inicie sesión en _Admin_, se le pedirá que conceda permiso a Adobe para recopilar datos de uso de todos los usuarios administradores. Al permitir que los administradores recopilen los datos de uso, Adobe puede mejorar la experiencia de uso del administrador de Adobe Commerce y de los productos y servicios relacionados.

![Permitir la recopilación de datos de uso de administración](./assets/admin-usage-data.png){width="600"}

Los usuarios individuales no se identifican en los datos de uso. Su configuración de recopilación de datos se puede cambiar en cualquier momento desde la configuración de [Uso de administración](../configuration-reference/advanced/admin.md#admin-usage).

Para Adobe Commerce, permitir la recopilación de datos también habilita la _Guía interna del producto_, que está diseñada para ofrecer contenido interactivo al _administrador_. Proporciona ayuda, información sobre herramientas, guías de introducción, información de incorporación, anuncios de funcionalidades, etc.
