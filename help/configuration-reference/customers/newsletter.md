---
title: '[!UICONTROL Customers] > [!UICONTROL Newsletter]'
description: Revise la configuración en la página [!UICONTROL Customers] > [!UICONTROL Newsletter] del administrador de Commerce.
exl-id: a97003ca-985e-47fa-9ff3-677e05ef3729
feature: Configuration, Customers, Communications
TQID: 'https://experienceleague.adobe.com/rqG5WOxVnMnlKTSiSHYgl-3Q5Yy4nIKWOjAev35UYHA'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 22bad240-8308-569b-a9d5-578f1ff890ca
    internal-label: Customers
  - id: bb03f6c4-cab9-560e-9d02-5816e1808d17
    internal-label: Communications
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 2%
---
# [!UICONTROL Customers] > [!UICONTROL Newsletter]

{{config}}

>[!NOTE]
>
>El boletín forma parte de los instrumentos de marketing que permiten enviar a los clientes noticias, descuentos y otros correos electrónicos de marketing. Los clientes registrados pueden administrar su suscripción desde su [panel de cuentas](../../customers/account-dashboard-my-account.md).

## [!UICONTROL General Options]

![Opciones generales](./assets/newsletter-general-options.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enabled] | Vista de tienda | Determina si los boletines están habilitados para el ámbito de vista de tienda. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Subscription Options]

![Opciones de suscripción](./assets/newsletter-subscription-options.png)<!-- zoom -->

<!-- [Subscription Options](https://experienceleague.adobe.com/es/docs/commerce-admin/marketing/communications/newsletters/newsletters) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Allow Guest Subscription] | Vista de tienda | Determina si los invitados no registrados pueden suscribirse a un boletín informativo. Opciones: `Yes` / `No` |
| [!UICONTROL Need to Confirm] | Vista de tienda | Determina si se deben confirmar las solicitudes de suscripción. Este método de doble inclusión es una medida de validación que evita que las personas se suscriban sin su consentimiento. Opciones: `Yes` / `No` |
| [!UICONTROL Confirmation Email Sender] | Vista de tienda | Identifica el contacto de tienda que aparece como el remitente del correo electrónico enviado para confirmar una solicitud de suscripción. |
| [!UICONTROL Confirmation Email Template] | Vista de tienda | Determina la plantilla de correo electrónico utilizada para la notificación enviada para confirmar una solicitud de suscripción a un boletín informativo. Plantilla predeterminada: `Newsletter subscription confirmation` |
| Remitente de correo electrónico correcto | Vista de tienda | Identifica el contacto de tienda que aparece como el remitente del correo electrónico enviado a los usuarios que se suscribieron correctamente a un boletín informativo. |
| [!UICONTROL Success Email Template] | Vista de tienda | Determina la plantilla de correo electrónico utilizada para la notificación enviada a los suscriptores de un boletín informativo. Plantilla predeterminada: `Newsletter subscription success` |
| [!UICONTROL Unsubscription Email Sender] | Vista de tienda | Identifica el contacto de tienda que aparece como el remitente del correo electrónico enviado a quienes solicitan finalizar su suscripción al boletín informativo. |
| [!UICONTROL Unsubscription Email Template] | Vista de tienda | Determina la plantilla de correo electrónico utilizada para la notificación enviada a los usuarios que solicitan finalizar su suscripción al boletín informativo. Plantilla predeterminada: `Newsletter unsubscription success` |

{style="table-layout:auto"}
