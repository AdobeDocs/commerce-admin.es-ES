---
title: Configurar correo electrónico de empresa
description: Obtenga información acerca de las opciones de correo electrónico y las plantillas utilizadas para enviar comunicaciones para cuentas de empresa.
exl-id: fd61c0c6-0887-4ff2-8002-906ff615bad9
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 0%

---

# Configurar opciones de correo electrónico de empresa

El [representante comercial](account-company-manage.md) que se asigna como contacto principal de una compañía se configura de forma predeterminada como remitente de muchos mensajes de correo electrónico automatizados enviados a la compañía.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Company Configuration]**.

1. Si es necesario, establezca **[!UICONTROL Store View]** a la vista de tienda para definir el [ámbito](../getting-started/websites-stores-views.md#scope-settings) de la configuración.

1. Complete la **[!UICONTROL Company Registration]** sección:

   >[!NOTE]
   >
   >Borre la **[!UICONTROL Use system value]** para que el campo se pueda editar.

   - Establecer **[!UICONTROL Company Registration Email Recipient]** a la [contacto de tienda](../getting-started/store-details.md#store-email-addresses) a quien se notificará cuando se reciba una nueva solicitud de registro de empresa.

   - En el **[!UICONTROL Send Company Registration Email Copy To]** , introduzca la dirección de correo electrónico de cada persona que vaya a recibir una copia de la notificación de registro. Separe varias direcciones de correo electrónico con una coma.

   - Para determinar cómo se envía la copia de la notificación, establezca **[!UICONTROL Send Email Copy Method]** a uno de los siguientes:

      - `Bcc` - Envía un _copia de cortesía oculta_ al incluir el destinatario en el encabezado del mismo correo electrónico que se envía al cliente. El destinatario CCO no es visible para el cliente.
      - `Separate Email` : envía la copia como un correo electrónico independiente.

   - Si ha preparado una plantilla de correo electrónico para utilizarla en lugar de la predeterminada, establezca **[!UICONTROL Default Company Registration Email]** al nombre de la plantilla. De forma predeterminada, la variable `Company Registration Request` se utiliza la plantilla.

     ![Configuración de clientes: registro de empresa](./assets/company-email-options-company-registration.png){width="600" zoomable="yes"}

1. Complete la **[!UICONTROL Customer-Related Emails]** sección:

   Si ha preparado plantillas de correo electrónico alternativas para utilizarlas en lugar de las predeterminadas, elija la plantilla que desee utilizar para cada una de las siguientes opciones:

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![Configuración de clientes: correos electrónicos relacionados con clientes](./assets/company-email-options-customer-related-emails.png){width="600" zoomable="yes"}

1. Complete la **[!UICONTROL Company Status Change]** sección:

   - Establecer **[!UICONTROL Company Status Change for Email Recipient]** a la [contacto de tienda](../getting-started/store-details.md#store-email-addresses) a quien se notificará cuando cambie el estado de una empresa.

   - En el **[!UICONTROL Send Company Status Change Email Copy To]** , introduzca la dirección de correo electrónico de cada persona que vaya a recibir una copia de la notificación de cambio de estado. Separe varias direcciones de correo electrónico con una coma.

   - Para determinar cómo se envía la copia de la notificación, establezca **[!UICONTROL Send Email Copy Method]** a uno de los siguientes:

      - `Bcc` - Envía un _copia de cortesía oculta_ al incluir el destinatario en el encabezado del mismo correo electrónico que se envía al cliente. El destinatario CCO no es visible para el cliente.
      - `Separate Email` : envía la copia como un correo electrónico independiente.

   - Si tiene una plantilla de correo electrónico preparada que se utilizará en lugar de la predeterminada cuando el estado de la empresa cambie de `Pending Approval` hasta `Active`, configurado **[!UICONTROL Default 'Company Status Change to Active 1' Email]** a esa plantilla. De forma predeterminada, la variable `Company Status Active 1` se utiliza la plantilla.

   - Si tiene una plantilla de correo electrónico preparada que se utilizará en lugar de la predeterminada cuando el estado de la empresa cambie de `Rejected` o `Blocked` hasta `Active`, configurado **[!UICONTROL Default 'Company Status Change to Active 2' Email]** a esa plantilla. De forma predeterminada, la variable `Company Status Active 2` se utiliza la plantilla.

   - Si tiene una plantilla de correo electrónico preparada que se utilizará en lugar de la predeterminada cuando el estado de la empresa cambie a `Rejected`, configurado **[!UICONTROL Default 'Company Status Change to Rejected' Email]** a esa plantilla. De forma predeterminada, la variable `Company Status Rejected` se utiliza la plantilla.

   - Si tiene una plantilla de correo electrónico preparada que se utilizará en lugar de la predeterminada cuando el estado de la empresa cambie a `Blocked`, configurado **[!UICONTROL Default 'Company Status Change to Blocked' Email]** a esa plantilla. De forma predeterminada, la variable `Company Status Blocked` se utiliza la plantilla.

   - Si tiene una plantilla de correo electrónico preparada que se utilizará en lugar de la predeterminada cuando el estado de la empresa cambie a `Pending Approval`, configurado **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** a esa plantilla. De forma predeterminada, la variable `Company Status Pending Approval` se utiliza la plantilla.

     ![Configuración de clientes: cambio de estado de la empresa](./assets/company-email-options-company-status-change.png){width="600" zoomable="yes"}

1. Complete la **[!UICONTROL Company Credit Emails]** sección:

   - Establecer **[!UICONTROL Company Credit Change Email Sender]** a la [contacto de tienda](../getting-started/store-details.md#store-email-addresses) a quien se notificará cuando se realice un cambio en el límite de crédito asignado a una empresa. De forma predeterminada, la notificación se envía a _Representante de ventas_.

   - En el **[!UICONTROL Send Company Credit Change Email Copy To]** , introduzca la dirección de correo electrónico de cada persona que va a recibir una copia de la notificación de cambio de crédito. Separe varias direcciones de correo electrónico con una coma.

   - Para determinar cómo se envía la copia de la notificación, establezca **[!UICONTROL Send Email Copy Method]** a uno de los siguientes:

      - `Bcc` - Envía un _copia de cortesía oculta_ al incluir el destinatario en el encabezado del mismo correo electrónico que se envía al cliente. El destinatario CCO no es visible para el cliente.
      - `Separate Email` : envía la copia como un correo electrónico independiente.

   - Si ha preparado plantillas de correo electrónico para utilizarlas en lugar de los valores predeterminados, elija la plantilla para cada una de las siguientes notificaciones que se envían al administrador de la empresa.

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![Configuración de clientes: correos electrónicos de crédito de empresa](./assets/company-email-options-company-credit.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.
