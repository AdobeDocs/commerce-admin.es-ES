---
title: Invitaciones a eventos
description: Aprenda cómo los clientes pueden enviar y ver invitaciones a eventos y ventas privadas desde el panel de sus cuentas de cliente.
exl-id: 6a9123a0-bdb4-4cd6-99cd-658f728aa90c
feature: Promotions/Events, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# Invitaciones a eventos

{{ee-feature}}

Cuando las invitaciones están habilitadas, los clientes pueden enviar y ver invitaciones desde el panel de sus cuentas de cliente. El correo electrónico de invitación incluye un vínculo a la página de inicio de sesión de cliente de la tienda.

## Mis invitaciones

El _[!UICONTROL My Invitations]_de la cuenta del cliente enumera todas las invitaciones enviadas por el cliente. Los clientes pueden enviar invitaciones a amigos y familiares para eventos en tiendas, registros de regalos, listas de deseos, etc.

![Mis invitaciones](./assets/account-dashboard-my-invitations.png){width="700" zoomable="yes"}

### Flujo de trabajo de invitación

1. **El cliente prepara las invitaciones**: desde el panel de cuentas, el cliente prepara la lista de destinatarios y completa la invitación. Se puede incluir un mensaje personalizado, según la configuración.
1. **El cliente envía invitaciones**: cuando está listo, el cliente hace clic en el _[!UICONTROL Send Invitations]_botón.
1. **El sistema gestiona la transmisión**: el sistema envía invitaciones en lotes, según el número establecido en la configuración.
1. **El cliente monitoriza la respuesta**: el cliente supervisa el estado de cada invitación desde el panel de cuentas, como `Sent`, `Accepted`, o `Canceled`.

### Enviar una invitación

1. En la barra lateral de su cuenta en la tienda, el cliente elige **[!UICONTROL My Invitations]**.

1. En el _Mi invitación_ página, clics **[!UICONTROL Send Invitation]**.

1. Define el nuevo elemento de invitación:

   - Completa la información de correo electrónico.

   - (Opcional) Crea una invitación de varias direcciones haciendo clic en **+** y añadir otra dirección de correo electrónico.

     Una sola invitación tiene un límite de cinco direcciones de correo electrónico.

   - (Opcional) Escribe un mensaje complementario.

1. Cuando termine, haga clic en **[!UICONTROL Send Invitation]**.

Se envía una notificación de invitación a la dirección de correo electrónico del usuario invitado con un vínculo de instrucciones para configurar la cuenta.

>[!NOTE]
>
>Un usuario solo puede enviar una invitación a una dirección de correo electrónico específica. Al intentar reenviar una invitación a la misma dirección de correo electrónico, se muestra un mensaje de error y la invitación no se envía.

## Habilitar invitaciones para tu tienda

La configuración de invitación habilita las invitaciones para la tienda y determina cómo se envían.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Invitations]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL General]** sección.

   ![Configuración de clientes: invitaciones y opciones generales](../configuration-reference/customers/assets/invitations-general.png){width="600" zoomable="yes"}

1. Establecer **[!UICONTROL Enable Invitations Functionality]** hasta `Yes`.

1. Para permitir que los clientes administren invitaciones desde la tienda, establezca **Habilitar invitaciones en tienda** hasta `Yes`.

1. Establecer **[!UICONTROL Referred Customer Group]** a uno de los siguientes:

   - `Same as Inviter`
   - `Default Customer Group from Configuration`

1. Establecer **[!UICONTROL New Accounts Registration]** a uno de los siguientes:

   - `By Invitation Only`
   - `Available to All`

1. Hasta **[!UICONTROL Allow Customers to Add Custom Message to Invitation Email]**, seleccione `Yes`.

1. Para limitar el número de invitaciones que se pueden enviar al mismo tiempo, escriba el número en la **[!UICONTROL Max Invitations Allowed to be Sent at One Time]** field.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Email]** y haga lo siguiente:

   ![Configuración de clientes: opciones de correo electrónico de invitaciones](../configuration-reference/customers/assets/invitations-email.png){width="600" zoomable="yes"}

   - Seleccione la identidad del almacén que se utilizará como **[!UICONTROL Customer Invitation Email Sender]**.

   - Seleccione el **[!UICONTROL Customer Invitation Email Template]** se utiliza para las invitaciones enviadas.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Envíe y administre invitaciones en Admin

En el [Informes de ventas privados](../getting-started/private-sales-reports.md) , puede ver el número de invitaciones enviadas durante un periodo especificado o los clientes a los que ha enviado invitaciones.

### Cree una invitación en el Admin

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Invitations]**.

1. En la siguiente pantalla, introduzca direcciones de correo electrónico para invitar a nuevos clientes, añada un mensaje personalizado, elija un remitente y seleccione un grupo de invitados.

   Si tiene varias vistas de tienda, use el **[!UICONTROL Send From]** para especificar la vista de tienda desde la que se envía una invitación.

   ![Información de invitaciones](./assets/create-invitation-page.png){width="700" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

### Descartar invitaciones para una sola entidad

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Busque la invitación necesaria mediante filtros y ábrala en modo de edición.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Discard Invitation]**.

1. Para confirmar la acción, haga clic en **[!UICONTROL OK]**.

### Descartar invitaciones para varias entidades

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Busque y seleccione las invitaciones que desea descartar.

1. En la parte superior izquierda, utilice el **[!UICONTROL Actions]** menú para elegir **[!UICONTROL Discard Selected]** y haga clic en **[!UICONTROL Submit]**.

1. Para confirmar la acción, haga clic en **[!UICONTROL OK]**.

### Descripciones de campos

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Select] | Seleccione la casilla de verificación para seleccionar las invitaciones que deben estar sujetas a una acción o utilice el control de selección en el encabezado de la columna. Opciones: `Select All` /` Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL ID] | El número de ID interno de una invitación |
| [!UICONTROL Email] | Una dirección de correo electrónico del cliente correspondiente |
| [!UICONTROL Invitee] | Correo electrónico del usuario invitado |
| [!UICONTROL Sent] | Fecha y hora en la que se envió la invitación |
| [!UICONTROL Registered] | Hora y datos del registro de un cliente |
| [!UICONTROL Status] | Estado de la invitación. Opciones: `Sent` / `Not Sent` / `Accepted` / `Discarded` |
| [!UICONTROL Valid Website] | El sitio web correspondiente |
| [!UICONTROL Invitee Group] | Un grupo de clientes de un invitado |

{style="table-layout:auto"}
