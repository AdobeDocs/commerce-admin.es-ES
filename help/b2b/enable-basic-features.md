---
title: Activar funciones B2B
description: Obtenga información acerca de la activación de funciones B2B en su tienda Adobe Commerce, incluidas las cuentas de empresa, los métodos de pago y envío predeterminados, los pedidos de compra y las aprobaciones de pedidos.
exl-id: aed203ef-f39b-4f7e-b32f-ded53eca09a8
feature: B2B, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '1629'
ht-degree: 0%

---

# Activar funciones B2B

De forma predeterminada, todas las funciones B2B se desactivan inicialmente. Un administrador de tienda puede habilitar o deshabilitar las funciones B2B según sea necesario para las tiendas de comercio. Para obtener una lista completa de los ajustes de configuración de B2B, consulte [Referencia de configuración de funciones B2B](../configuration-reference/general/b2b-features.md).

Al habilitar la compatibilidad para las empresas de los clientes, se habilitan automáticamente las siguientes funciones B2B adicionales:

- [!DNL Shared Catalog]

  Admite la configuración de precios personalizada para diferentes empresas y también habilita permisos de categoría para todas las tiendas.

- [!DNL Enable Shared Catalog direct products price assigning]

  Mejora el rendimiento del sitio al almacenar únicamente los productos asignados a un catálogo compartido en el índice de precios. Habilitar esta función es una práctica recomendada para los comerciantes que tienen muchos catálogos compartidos para administrar los precios personalizados para diferentes empresas.

- [!DNL B2B Quotes]

  Permite a los vendedores y compradores de la empresa negociar precios.

- [!DNL B2B default payment and shipping methods]

  Determina la selección de opciones de pago y envío disponibles para los compradores B2B en la tienda.

Los ajustes de configuración de estas funciones solo están visibles cuando [!DNL Enable Company] se establece en `Yes`.

B2B [!DNL Quick Order] y [!DNL Requisition List] Las funciones de se pueden activar y desactivar de forma independiente.

## Configuración de funciones B2B

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   Si tiene una instalación de varios sitios, configure el **[!UICONTROL Store View]** en la esquina superior izquierda del sitio web donde se aplica la configuración.

1. En el panel izquierdo, debajo de _[!UICONTROL General]_, elija **[!UICONTROL B2B Features]**:

   ![Configuración B2B: general](./assets/b2b-features.png){width="600"}

   - Permitir que los clientes administren sus propias cuentas de compañía y habilitar la compatibilidad con funciones B2B adicionales mediante la configuración de **[!UICONTROL Enable Company]**  hasta `Yes`.

     Al activar la asistencia técnica de la empresa, se activan automáticamente el catálogo compartido, la oferta B2B, los métodos de pago B2B y los métodos de envío B2B.

   - Para permitir que los clientes e invitados realicen pedidos rápidamente en función del SKU o el nombre del producto, establezca **[!UICONTROL Enable Quick Order]** hasta `Yes`.

   - Para permitir que los clientes creen y gestionen listas de solicitudes desde su panel de control de cuentas, establezca **[!UICONTROL Enable Requisition List]** hasta `Yes`.

     También puede [configuración del número máximo de listas](configure-requisition-lists.md) un cliente puede tener para su cuenta.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Configuración de métodos de envío y pago B2B predeterminados

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Default B2B Payment Methods]** sección.

1. Para establecer los métodos de pago predeterminados para los pedidos B2B, establezca **[!UICONTROL Applicable Payment Methods]** a uno de los siguientes:

   - `All Payment Methods`

   - `Selected Payment Methods`

     Para la opción específica, seleccione la **[!UICONTROL Payment Methods]** que desea poner a disposición de sus clientes manteniendo pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) mientras hace clic en cada opción.

   La lista de [métodos de pago](../configuration-reference/sales/payment-methods.md) muestra qué opciones están habilitadas o deshabilitadas actualmente en tu tienda. Además de los métodos de pago estándar, la lista también incluye lo siguiente:

   - No se requiere información de pago
   - [Pago a cuenta](#configure-payment-on-account)
   - Cuentas almacenadas
   - Tarjetas almacenadas

   ![Configuración B2B: configuración de método de pago por defecto](./assets/b2b-features-default-payment-methods.png){width="600"}

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Default B2B Shipping Methods]** sección.

1. Para especificar los métodos de envío predeterminados para los pedidos B2B, establezca **[!UICONTROL Applicable Shipping Methods]** a uno de los siguientes:

   - `All Shipping Methods`
   - `Selected Shipping Methods`

     Para la opción específica, seleccione la **[!UICONTROL Shipping Methods]** que desea poner a disposición de sus clientes manteniendo pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) mientras hace clic en cada opción.

     La lista de métodos de envío muestra los que están actualmente [activado o desactivado](../configuration-reference/sales/delivery-methods.md).

   ![Configuración B2B: métodos de envío predeterminados](./assets/b2b-features-shipping-methods.png){width="600"}

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Configurar opciones de correo electrónico de empresa

El [representante comercial](account-company-manage.md#assign-a-sales-representative) que se asigna como contacto principal de una compañía se configura de forma predeterminada como remitente de muchos mensajes de correo electrónico automatizados enviados a la compañía.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Company Configuration]**.

1. Si es necesario, establezca **[!UICONTROL Store View]** a la vista de tienda para definir el [ámbito](../getting-started/websites-stores-views.md#scope-settings) de la configuración.

1. Complete la **[!UICONTROL Company Registration]** sección:

   >[!NOTE]
   >
   >Borre la **[!UICONTROL Use system value]** para que el campo se pueda editar.

   - Establecer **[!UICONTROL Company Registration Email Recipient]** a la [contacto de tienda](../getting-started/store-details.md#store-email-addresses) a quien se notificará cuando se reciba una nueva solicitud de registro de empresa.

   - Para **[!UICONTROL Send Company Registration Email Copy To]**, introduzca la dirección de correo electrónico de cada persona que vaya a recibir una copia de la notificación de registro. Separe varias direcciones de correo electrónico con una coma.

   - Para determinar cómo se envía la copia de la notificación, establezca **Método Enviar copia de correo electrónico** a uno de los siguientes:

      - `Bcc` - Envía un _copia de cortesía oculta_ al incluir el destinatario en el encabezado del mismo correo electrónico que se envía al cliente. El destinatario CCO no es visible para el cliente.
      - `Separate Email` : envía la copia como un correo electrónico independiente.

   - Si ha preparado una plantilla de correo electrónico para utilizarla en lugar de la predeterminada, establezca **[!UICONTROL Default Company Registration Email]** al nombre de la plantilla. De forma predeterminada, la variable `Company Registration Request` se utiliza la plantilla.

     ![Configuración de clientes: registro de empresa](./assets/company-email-options-company-registration.png){width="600"}

1. Complete la **[!UICONTROL Customer-Related Emails]** sección:

   Si ha preparado plantillas de correo electrónico alternativas para utilizarlas en lugar de las predeterminadas, elija la plantilla que desee utilizar para cada una de las siguientes opciones:

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![Configuración de clientes: correos electrónicos relacionados con clientes](./assets/company-email-options-customer-related-emails.png){width="600"}

1. Complete la **[!UICONTROL Company Status Change]** sección:

   - Para **[!UICONTROL Send Company Status Change Email Copy To]**, introduzca la dirección de correo electrónico de cada persona que vaya a recibir una copia de la notificación de cambio de estado. Separe varias direcciones de correo electrónico con una coma.

   - Para determinar cómo se envía la copia de la notificación, establezca **Método Enviar copia de correo electrónico** a uno de los siguientes:

      - `Bcc` - Envía un _copia de cortesía oculta_ al incluir el destinatario en el encabezado del mismo correo electrónico que se envía al cliente. El destinatario CCO no es visible para el cliente.
      - `Separate Email` : envía la copia como un correo electrónico independiente.

   - Si ha preparado una plantilla de correo electrónico que se utilizará cuando el estado de la empresa cambie de `Pending Approval` hasta `Active`, configurado **[!UICONTROL Default 'Company Status Change to Active 1' Email]** al nombre de la plantilla. De forma predeterminada, la variable `Company Status Active 1` se utiliza la plantilla.

   - Si ha preparado una plantilla de correo electrónico que se utilizará cuando el estado de la empresa cambie de `Rejected` o `Blocked` hasta `Active`, configurado **[!UICONTROL Default 'Company Status Change to Active 2' Email]** al nombre de la plantilla. De forma predeterminada, la variable `Company Status Active 2` se utiliza la plantilla.

   - Si ha preparado una plantilla de correo electrónico que se utilizará cuando el estado de la empresa cambie a `Rejected`, configurado **[!UICONTROL Default 'Company Status Change to Rejected' Email]** al nombre de la plantilla. De forma predeterminada, la variable `Company Status Rejected` se utiliza la plantilla.

   - Si ha preparado una plantilla de correo electrónico que se utilizará cuando el estado de la empresa cambie a `Blocked`, configurado **[!UICONTROL Default 'Company Status Change to Blocked' Email]** al nombre de la plantilla. De forma predeterminada, la variable `Company Status Blocked` se utiliza la plantilla.

   - Si ha preparado una plantilla de correo electrónico que se utilizará cuando el estado de la empresa cambie a `Pending Approval`, configurado **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** al nombre de la plantilla. De forma predeterminada, la variable `Company Status Pending Approval` se utiliza la plantilla.

   ![Configuración de clientes: cambio de estado de la empresa](./assets/company-email-options-company-status-change.png){width="600"}

1. Complete la **[!UICONTROL Company Credit Emails]** sección:

   - Establecer **[!UICONTROL Company Credit Change Email Sender]** a la [contacto de tienda](../getting-started/store-details.md#store-email-addresses) a quien se notificará cuando se realice un cambio en el límite de crédito asignado a una empresa. De forma predeterminada, la notificación se envía a _Representante de ventas_.

   - Para **[!UICONTROL Send Company Credit Change Email Copy To]**, introduzca la dirección de correo electrónico de cada persona que vaya a recibir una copia de la notificación de cambio de crédito. Separe varias direcciones de correo electrónico con una coma.

   - Para determinar cómo se envía la copia de la notificación, establezca **Método Enviar copia de correo electrónico** a uno de los siguientes:

      - `Bcc` - Envía un _copia de cortesía oculta_ al incluir el destinatario en el encabezado del mismo correo electrónico que se envía al cliente. El destinatario CCO no es visible para el cliente.
      - `Separate Email` : envía la copia como un correo electrónico independiente.

   - Si ha preparado plantillas de correo electrónico para utilizarlas en lugar de los valores predeterminados, elija la plantilla para cada una de las siguientes notificaciones que se envían al administrador de la empresa.

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![Configuración de clientes: correos electrónicos de crédito de empresa](./assets/company-email-options-company-credit.png){width="600"}

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Configuración de aprobación de pedidos

La capacidad de realizar un seguimiento del procesamiento de pedidos y de los pedidos de compra proporciona a los administradores de la empresa control sobre las acciones de los compradores de la empresa. La funcionalidad de aprobación de pedidos está disponible cuando el administrador de una tienda activa la función de pedidos de compra.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL General]** y elija **[!UICONTROL B2B Features]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Order Approval Configuration]** sección.

   ![Configuración de aprobación de pedidos](./assets/b2b-features-order-approval.png){width="600"}

1. Para permitir que las empresas creen sus propios pedidos de compra, establezca **[!UICONTROL Enable Purchase Orders]** hasta `Yes`.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

   La función de pedidos de compra está habilitada en el nivel de sitio web. Para habilitar este tipo de pedido para una empresa, haga lo mismo con la configuración adecuada en cada [perfil de empresa](account-company-manage.md).

## Configuración de pedidos de compra

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Busque la empresa en la lista y haga clic en **[!UICONTROL Edit]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Advanced Settings]** sección.

1. Establecer **[!UICONTROL Enable Purchase Orders]** hasta `Yes`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

Después de la activación, la variable **[!UICONTROL Approval Rules]** se muestra en la tienda [Tablero de cuentas](../customers/account-dashboard.md) para un administrador de empresa.

>[!NOTE]
>
>El administrador de la empresa debe otorgar el acceso a la orden de compra en la tienda en función de lo siguiente [permisos de función de usuario de compañía](account-company-roles-permissions.md).

## Configuración del pago a cuenta

Pago a cuenta es un método de pago sin conexión que permite a las empresas realizar compras hasta el límite de crédito especificado en su perfil. El pago a cuenta se puede habilitar a nivel global o por empresa, y solo aparece durante el cierre de compra si está habilitado. Cuándo _Pago a cuenta_ se utiliza como método de pago, aparece un mensaje en la parte superior del pedido que indica el estado de la cuenta. Para configurar este método de pago para una empresa específica, consulte [Administrar cuentas de empresa](account-company-manage.md).

>[!NOTE]
>
>No se admite el pago a cuenta para pedidos con [varias direcciones de envío](../stores-purchase/shipping-settings.md#multiple-addresses) y no aparece entre las opciones de pago de estos pedidos.

Para habilitar el pago a cuenta en la tienda:

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Payment Methods]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Payment on Account]** sección.

   ![Pago a cuenta](./assets/payment-methods-payment-on-account.png){width="600"}

   >[!NOTE]
   >
   >Si es necesario, anule primero la selección del **[!UICONTROL Use system value]** para cambiar esta configuración.

1. Para permitir el pago a cuenta, configure **[!UICONTROL Enabled]** hasta `Yes`.

1. Introduzca una **[!UICONTROL Title]** que identifica la forma de pago durante el cierre de compra, o bien puede aceptar la `Payment on Account` título predeterminado.

1. Si las solicitudes suelen esperar la aprobación, acepte el valor predeterminado **[!UICONTROL New Order Status]** as `Pending` hasta que se apruebe.

   Si lo prefiere, puede utilizar el `Processing` o `Suspected Fraud` estado de los nuevos pedidos con esta forma de pago.

1. Establecer **[!UICONTROL Payment from Applicable Countries]** a uno de los siguientes:

   - `All Allowed Countries` - Clientes de todos [países](../getting-started/store-details.md#country-options) especificado en la configuración de tu tienda puede utilizar este método de pago.
   - `Specific Countries` - Después de elegir esta opción, la variable _[!UICONTROL Payment from Specific Countries]_aparece una lista. Para seleccionar varios países, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

1. Establecer **[!UICONTROL Minimum Order Total]** y **[!UICONTROL Maximum Order Total]** a los importes de pedido necesarios para cumplir los requisitos de este método de pago.

   >[!NOTE]
   >
   >Una solicitud cualifica si el total se encuentra entre los valores totales mínimo o máximo, o si coincide exactamente con ellos.

1. Introduzca una **[!UICONTROL Sort Order]** número que establece la posición de este artículo en la lista de métodos de pago que se muestra durante el pago y envío.

   El valor es relativo a los otros métodos de pago. (`0` = primero, `1` = segundo, `2` = tercero, etc.)

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.
