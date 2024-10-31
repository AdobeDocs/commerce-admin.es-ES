---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Invitations]'
description: Revise la configuración en la página [!UICONTROL Customers] &gt; [!UICONTROL Invitations] del administrador de Commerce.
exl-id: edafeaed-9c4f-4d9f-b35c-381ae5f43b67
feature: Configuration, Promotions/Events
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Invitations]

{{ee-feature}}

{{config}}

## [!UICONTROL General]

![General](./assets/invitations-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/events/invitations#enable-invitations-for-your-store) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable Invitations Functionality] | Global | Determina si el módulo Invitaciones está habilitado. Opciones: `Yes` / `No` |
| [!UICONTROL Enable Invitations on Frontend] | Sitio web | Determina si se pueden administrar las invitaciones desde la tienda. Opciones: `Yes` / `No` |
| [!UICONTROL Referred Customer Group] | Vista de tienda | Determina el grupo de clientes del invitado. Opciones: <br/>**`Same as Inviter`**: las invitadas se asignan automáticamente al mismo grupo de clientes que los clientes que las invitaron.<br/>**`Default Customer Group from Configuration`** - Las invitadas tienen automáticamente el [grupo de clientes](../../customers/customer-groups.md) predeterminado. |
| [!UICONTROL New Accounts Registration] | Vista de tienda | Determina cómo los invitados pueden crear una cuenta. Opciones: <br/>**`By Invitation Only`**- Los invitados deben seguir el vínculo del mensaje de correo electrónico de invitación para crear una cuenta.<br/>**`Available to All`** - Los invitados pueden usar el formulario de registro de cuenta que está disponible en la tienda. |
| [!UICONTROL Allow Customers to Add Custom Message to Invitation Email] | Vista de tienda | Determina si hay un campo en el formulario de invitación en el que el invitado puede agregar un mensaje personalizado que se envía al invitado por correo electrónico. Esto no afecta a la capacidad del administrador de añadir un mensaje a una invitación. Opciones: `Yes` / `No`. |
| [!UICONTROL Max Invitations Allowed to be Sent at One Time] | Vista de tienda | Determina el número máximo de invitaciones que el invitado puede enviar a la vez. Se envía una invitación diferente a cada dirección de correo electrónico que el invitado incluya en el formulario. Esto protege los recursos del servidor al evitar que se envíen grandes cantidades de invitaciones a la vez, lo que reduce la probabilidad de que las invitaciones se envíen como correo no deseado. |

{style="table-layout:auto"}

## [!UICONTROL Email]

![Correo electrónico](./assets/invitations-email.png)<!-- zoom -->

<!-- [Email](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/events/invitations#enable-invitations-for-your-store) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Customer Invitation Email Sender] | Vista de tienda | Determina el remitente del correo electrónico que reciben los invitados cuando se envía un mensaje de correo electrónico de invitación. Valor predeterminado: `General Contact` |
| [!UICONTROL Customer Invitation Email Template] | Vista de tienda | Determina la plantilla del correo electrónico que reciben los invitados cuando se envía un mensaje de correo electrónico de invitación. Plantilla predeterminada: `Customer Invitation` |

{style="table-layout:auto"}
