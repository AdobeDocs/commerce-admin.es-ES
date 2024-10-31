---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Reward Points]'
description: Revise la configuración en la página [!UICONTROL Customers] &gt; [!UICONTROL Reward Points] del administrador de Commerce.
exl-id: 0b7f8806-74c5-4467-87da-0faae50f164b
feature: Configuration, Rewards
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Reward Points]

{{ee-feature}}

{{config}}

>[!NOTE]
>
>Se requiere la configuración de [Tasas de cambio de recompensa](../../merchandising-promotions/reward-exchange-rates.md) para que los clientes y administradores puedan canjear los puntos de recompensa durante el cierre de compra.

## [!UICONTROL Reward Points]

![Puntos de recompensa](./assets/reward-points-reward-points.png)<!-- zoom -->

<!-- [Reward Points](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Reward Points Functionality] | Global | Activa o desactiva los puntos de recompensa. Opciones: `Yes` / `No`. |
| [!UICONTROL Enable Reward Points Functionality on Storefront] | Sitio web | Cuando está activada, los clientes pueden obtener puntos a través de sus actividades y canjearlos al cerrar la compra. Si está desactivado, solo los usuarios administradores pueden asignar y canjear puntos en nombre de los clientes. Opciones: `Yes` / `No`. |
| [!UICONTROL Customers May See Reward Points History] | Sitio web | Cuando se habilita, los clientes pueden ver un historial detallado con cada acumulación, canje y caducidad de puntos de recompensa en su panel de cuentas. Opciones: `Yes` / `No` |
| [!UICONTROL Reward Points Balance Redemption Threshold] | Sitio web | Exige a los clientes que alcancen un saldo de puntos mínimo antes de que puedan canjearlos por pedidos. Déjelo en blanco si no hay mínimo. |
| [!UICONTROL Cap Reward Points Balance At] | Sitio web | Impide que los clientes acumulen más puntos de este saldo máximo. Déjelo en blanco si no desea ningún máximo. |
| [!UICONTROL Reward Points Expire in (days)] | Sitio web | Indica la duración de los puntos de recompensa en días. Cada lote de puntos obtenidos durante las distintas actividades tiene una duración diferente. Cada lote en el historial de puntos de recompensa indica el número de días restantes antes de que expiren los puntos. El historial se puede ver desde el panel de cuentas del cliente, si está activado, y desde el Administrador. Déjelo en blanco si no desea caducar. |
| [!UICONTROL Reward Points Expiry Calculation] | Sitio web | Determina el método utilizado para determinar cuándo caducan los puntos de recompensa. Opciones: <br/>**`Static`**: determina la duración restante de los puntos de recompensa en función del número de días establecido en la configuración. Si el límite de caducidad de la configuración cambia, la fecha de caducidad de los puntos existentes no cambia.<br/>**`Dynamic`** - Calcula el número de días restantes cada vez que aumenta el saldo de puntos de recompensa. Si el límite de caducidad de la configuración cambia, los cálculos de caducidad de todos los puntos existentes se actualizan en consecuencia. |
| [!UICONTROL Refund Reward Points Automatically] | Global | Determina si los puntos de recompensa disponibles se reembolsan automáticamente. Opciones: `Yes` / `No` |
| [!UICONTROL Deduct Reward Points from Refund Amount Automatically] | Global | Esto determina si los puntos de recompensa obtenidos a través de compras se anulan total o parcialmente en el reembolso del pedido, cuando esta función está habilitada. Solo se ven afectados los puntos de recompensa del pedido que los obtuvo cuando se reembolsa ese pedido. Opciones: `Yes` / `No`. |
| [!UICONTROL Landing Page] | Vista de tienda | Especifica la página de CMS donde se explica el programa de puntos de recompensa. Aparecerá un enlace a la página predeterminada de Recompensas en las ubicaciones de su tienda, donde podrá obtener puntos. |

{style="table-layout:auto"}

## [!UICONTROL Actions for Acquiring Reward Points by Customers]

![Acciones para la adquisición de puntos de recompensa por parte de clientes](./assets/reward-points-actions-for-acquiring.png)<!-- zoom -->

<!-- [Actions for Acquiring Reward Points by Customers](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Purchase] | Sitio web | Determina si se obtienen puntos de recompensa por las compras en función de las [tasas de cambio de recompensa](../../merchandising-promotions/reward-exchange-rates.md) configuradas. Opciones: `Yes` / `No` |
| [!UICONTROL Registration] | Sitio web | Especifica el número de puntos obtenidos al abrir una cuenta de cliente. |
| [!UICONTROL Newsletter Signup] | Sitio web | Especifica el número de puntos obtenidos por los clientes registrados que se suscriben a un boletín informativo. (Los puntos no están disponibles para suscripciones de invitados). Si un cliente cancela la suscripción y luego se vuelve a suscribir, no se obtienen puntos por la segunda suscripción. |
| [!UICONTROL Converting Invitation to Customer] | Sitio web | Especifica el número de puntos obtenidos por un cliente que envía una invitación cuando el destinatario abre una cuenta de cliente. |
| [!UICONTROL Invitation to Customer Conversions Quantity Limit] | Sitio web | Limita el número de conversiones de invitación que se pueden utilizar para obtener puntos para el cliente que envía la invitación. Déjelo en blanco si no hay límite. |
| [!UICONTROL Converting Invitation to Order] | Sitio web | Especifica el número de puntos obtenidos por un cliente que envía una invitación cuando el destinatario realiza un pedido inicial. |
| [!UICONTROL Invitation to Order Conversions Quantity Limit] | Sitio web | Limita el número de conversiones de pedidos que pueden obtener puntos para la persona que envía la invitación. Si está en blanco, no hay límite máximo. |
| [!UICONTROL Invitation Conversion to Order Reward] | Sitio web | Indica la frecuencia con la que un cliente puede ganar puntos de recompensa cuando los invitados realizan compras. Opciones: <br/>**`Each`**- El cliente recibe puntos de recompensa por cada pedido facturado realizado por el invitado. Los puntos de recompensa se otorgan de acuerdo con las tasas de cambio establecidas para la combinación requerida de un sitio web y un grupo de clientes.<br/>**`First`** - El cliente recibe puntos de recompensa solamente por el primer pedido facturado realizado por los invitados. Si más de un invitado se registra y realiza un pedido, solo la cantidad del primer pedido se convierte en puntos de recompensa y se concede al cliente. |
| [!UICONTROL Review Submission] | Sitio web | Determina el número de puntos obtenidos por un cliente que envía una revisión aprobada para su publicación. |
| [!UICONTROL Rewarded Reviews Submission Quantity Limit] | Sitio web | Limita el número de críticas que se pueden usar para obtener puntos por cliente. Déjelo en blanco si no hay límite. |

{style="table-layout:auto"}

## [!UICONTROL Email Notification Settings]

![Configuración de notificación por correo electrónico](./assets/reward-points-email-notification-settings.png)<!-- zoom -->

<!-- [Email Notification Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Email Sender] | Vista de tienda | Determina el contacto de tienda que aparece como remitente de los correos electrónicos de actualización de saldo y notificación de caducidad. |
| [!UICONTROL Subscribe Customers by Default] | Global | Determina el estado de suscripción predeterminado de los clientes para los correos electrónicos de actualización de saldo y notificaciones de caducidad. |
| [!UICONTROL Balance Update Email] | Vista de tienda | Determina la plantilla utilizada para la notificación que se envía a los clientes cada vez que se actualiza su saldo de puntos. Plantilla predeterminada: `Reward Points Balance Update` |
| [!UICONTROL Reward Points Expiry Warning Email] | Vista de tienda | Determina la plantilla del correo electrónico que reciben los clientes cuando se alcanza el límite de advertencia de caducidad para un lote de puntos. Plantilla predeterminada: `Reward Points Expiry Warning` |
| [!UICONTROL Expiry Warning before (days)] | Global | Especifica el número de días antes de la caducidad del punto para enviar la notificación. Déjelo en blanco para no enviar notificaciones de caducidad. La notificación no se envía si el número de días introducido es mayor que la duración restante de los puntos. |

{style="table-layout:auto"}
