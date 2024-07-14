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

El [representante de ventas](account-company-manage.md) asignado como contacto principal de una compañía está configurado de manera predeterminada como remitente de muchos mensajes de correo electrónico automatizados enviados a la compañía.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Company Configuration]**.

1. Si es necesario, establezca **[!UICONTROL Store View]** en la vista de almacén para definir el [ámbito](../getting-started/websites-stores-views.md#scope-settings) de la configuración.

1. Complete la sección **[!UICONTROL Company Registration]**:

   >[!NOTE]
   >
   >Desactive la casilla **[!UICONTROL Use system value]** para poder editar el campo.

   - Establezca **[!UICONTROL Company Registration Email Recipient]** en el [contacto de tienda](../getting-started/store-details.md#store-email-addresses) al que se le notificará cuando se reciba una nueva solicitud de registro de empresa.

   - En el campo **[!UICONTROL Send Company Registration Email Copy To]**, escriba la dirección de correo electrónico de cada persona que vaya a recibir una copia de la notificación de registro. Separe varias direcciones de correo electrónico con una coma.

   - Para determinar cómo se envía la copia de la notificación, establezca **[!UICONTROL Send Email Copy Method]** en una de las siguientes opciones:

      - `Bcc` - Envía una _copia de cortesía a ciegas_ incluyendo el destinatario en el encabezado del mismo correo electrónico que se envía al cliente. El destinatario CCO no es visible para el cliente.
      - `Separate Email` - Envía la copia como un correo electrónico independiente.

   - Si ha preparado una plantilla de correo electrónico que se va a utilizar en lugar de la predeterminada, establezca **[!UICONTROL Default Company Registration Email]** en el nombre de la plantilla. De manera predeterminada, se utiliza la plantilla `Company Registration Request`.

     ![Configuración de clientes - registro de empresa](./assets/company-email-options-company-registration.png){width="600" zoomable="yes"}

1. Complete la sección **[!UICONTROL Customer-Related Emails]**:

   Si ha preparado plantillas de correo electrónico alternativas para utilizarlas en lugar de las predeterminadas, elija la plantilla que desee utilizar para cada una de las siguientes opciones:

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![Configuración de clientes - correos electrónicos relacionados con clientes](./assets/company-email-options-customer-related-emails.png){width="600" zoomable="yes"}

1. Complete la sección **[!UICONTROL Company Status Change]**:

   - Establezca **[!UICONTROL Company Status Change for Email Recipient]** en el [contacto de tienda](../getting-started/store-details.md#store-email-addresses) al que se le notificará cuando cambie el estado de una compañía.

   - En el campo **[!UICONTROL Send Company Status Change Email Copy To]**, escriba la dirección de correo electrónico de cada persona que vaya a recibir una copia de la notificación de cambio de estado. Separe varias direcciones de correo electrónico con una coma.

   - Para determinar cómo se envía la copia de la notificación, establezca **[!UICONTROL Send Email Copy Method]** en una de las siguientes opciones:

      - `Bcc` - Envía una _copia de cortesía a ciegas_ incluyendo el destinatario en el encabezado del mismo correo electrónico que se envía al cliente. El destinatario CCO no es visible para el cliente.
      - `Separate Email` - Envía la copia como un correo electrónico independiente.

   - Si tiene una plantilla de correo electrónico preparada que se va a usar en lugar de la predeterminada cuando el estado de la compañía cambie de `Pending Approval` a `Active`, establezca **[!UICONTROL Default 'Company Status Change to Active 1' Email]** en esa plantilla. De manera predeterminada, se utiliza la plantilla `Company Status Active 1`.

   - Si tiene una plantilla de correo electrónico preparada que se va a usar en lugar de la predeterminada cuando el estado de la compañía cambie de `Rejected` o `Blocked` a `Active`, establezca **[!UICONTROL Default 'Company Status Change to Active 2' Email]** en esa plantilla. De manera predeterminada, se utiliza la plantilla `Company Status Active 2`.

   - Si tiene una plantilla de correo electrónico preparada que se va a usar en lugar de la predeterminada cuando el estado de la compañía cambia a `Rejected`, establezca **[!UICONTROL Default 'Company Status Change to Rejected' Email]** en esa plantilla. De manera predeterminada, se utiliza la plantilla `Company Status Rejected`.

   - Si tiene una plantilla de correo electrónico preparada que se va a usar en lugar de la predeterminada cuando el estado de la compañía cambia a `Blocked`, establezca **[!UICONTROL Default 'Company Status Change to Blocked' Email]** en esa plantilla. De manera predeterminada, se utiliza la plantilla `Company Status Blocked`.

   - Si tiene una plantilla de correo electrónico preparada que se va a usar en lugar de la predeterminada cuando el estado de la compañía cambia a `Pending Approval`, establezca **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** en esa plantilla. De manera predeterminada, se utiliza la plantilla `Company Status Pending Approval`.

     ![Configuración de clientes - cambio de estado de la compañía](./assets/company-email-options-company-status-change.png){width="600" zoomable="yes"}

1. Complete la sección **[!UICONTROL Company Credit Emails]**:

   - Establezca **[!UICONTROL Company Credit Change Email Sender]** en el [contacto de tienda](../getting-started/store-details.md#store-email-addresses) al que se le notificará cuando se realice un cambio en el límite de crédito asignado a una compañía. De manera predeterminada, la notificación se envía a _Representante de ventas_.

   - En el campo **[!UICONTROL Send Company Credit Change Email Copy To]**, escriba la dirección de correo electrónico de cada persona que vaya a recibir una copia de la notificación de cambio de crédito. Separe varias direcciones de correo electrónico con una coma.

   - Para determinar cómo se envía la copia de la notificación, establezca **[!UICONTROL Send Email Copy Method]** en una de las siguientes opciones:

      - `Bcc` - Envía una _copia de cortesía a ciegas_ incluyendo el destinatario en el encabezado del mismo correo electrónico que se envía al cliente. El destinatario CCO no es visible para el cliente.
      - `Separate Email` - Envía la copia como un correo electrónico independiente.

   - Si ha preparado plantillas de correo electrónico para utilizarlas en lugar de los valores predeterminados, elija la plantilla para cada una de las siguientes notificaciones que se envían al administrador de la empresa.

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![Configuración de clientes - correos electrónicos de crédito de la compañía](./assets/company-email-options-company-credit.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
