---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Gift Registry]'
description: Revise la configuración en la página [!UICONTROL Customers] &gt; [!UICONTROL Gift Registry] del administrador de Commerce.
exl-id: c5153c4e-897a-41d2-bde1-8483855d1a37
feature: Configuration, Gift
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 1%

---

# [!UICONTROL Customers] > [!UICONTROL Gift Registry]

{{ee-feature}}

{{config}}

Para obtener información detallada sobre el uso de esta configuración para habilitar los registros de regalos para los clientes de la tienda, consulte [Configurar registros de regalos](../../merchandising-promotions/gift-registry-configure.md). Para obtener información acerca de cómo incluir la búsqueda en el Registro de regalos en la tienda, vea [Agregar búsqueda en el Registro de regalos](../../merchandising-promotions/gift-registry-search.md).

## [!UICONTROL General Options]

![Opciones generales](./assets/gift-registry-general-options.png)<!-- zoom -->

<!-- [General Options](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable Gift Registry] | Vista de tienda | Determina si hay registros de regalos disponibles. Opciones: <br/>**`Yes`**- Habilita los registros de regalos para la vista de tienda seleccionada. La pestaña Registro de regalos aparece en el panel de cuentas de los clientes registrados.<br/>**`No`** - Los registros de regalos no están disponibles para la vista de la tienda. |
| [!UICONTROL Maximum Registrants] | Vista de tienda | Establece el número de personas que un cliente puede agregar a un registro de regalos. El cliente comparte el registro de regalos con cada solicitante de registro. En la tienda, el botón _Agregar registrante_ está disponible para los clientes hasta que alcancen el número máximo. |

{style="table-layout:auto"}

## [!UICONTROL Owner Notification]

![Notificación de propietario](./assets/gift-registry-owner-notification.png)<!-- zoom -->

<!-- [Owner Notification](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Email Template] | Vista de tienda | Determina la plantilla utilizada para el correo electrónico de notificación de propietario que se envía cuando se crea un registro de regalos. Plantilla predeterminada: Notificación del propietario del registro de regalos |
| [!UICONTROL Email Sender] | Vista de tienda | Identifica al [contacto de tienda](../../getting-started/store-details.md#store-email-addresses) que aparece como remitente del correo electrónico de notificación del propietario del registro de regalos. Valor predeterminado: `General Contact` |

{style="table-layout:auto"}

## Uso compartido del registro de regalos

![Uso compartido del registro de regalos](./assets/gift-registry-gift-registry-sharing.png)<!-- zoom -->

<!-- Gift Registry Sharing](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Email Template] | Vista de tienda | Determina la plantilla utilizada para el correo electrónico de uso compartido del registro de regalos que se envía cuando se crea un registro de regalos. Cuando el propietario hace clic en _Compartir registro de regalos_, el correo electrónico se envía a cada destinatario. Plantilla predeterminada: `Gift Registry Sharing` |
| [!UICONTROL Email Sender] | Vista de tienda | Identifica al [contacto de tienda](../../getting-started/store-details.md#store-email-addresses) que aparece como remitente del correo electrónico de uso compartido del Registro de regalos. Valor predeterminado: `General Contact` |
| [!UICONTROL Maximum Sent Emails Threshold] | Vista de tienda | Número máximo de mensajes de notificación de correo electrónico de uso compartido del Registro de regalos que se pueden enviar a la vez. |

{style="table-layout:auto"}

## [!UICONTROL Gift Registry Update]

![Actualización del Registro de regalos](./assets/gift-registry-gift-registry-update.png)<!-- zoom -->

<!-- [Gift Registry Update](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Email Template] | Vista de tienda | Determina la plantilla utilizada para el correo electrónico de actualización del registro de regalos que se envía al propietario del registro de regalos cuando se realiza una compra en el registro de regalos. La actualización incluye información sobre el artículo y la cantidad comprados, pero no incluye el nombre de la persona que realizó el pedido. Plantilla predeterminada: `Gift Registry Update` |
| [!UICONTROL Email Sender] | Vista de tienda | Identifica al [contacto de tienda](../../getting-started/store-details.md#store-email-addresses) que aparece como remitente del correo electrónico de actualización del registro de regalos. Valor predeterminado: `General Contact` |

{style="table-layout:auto"}
