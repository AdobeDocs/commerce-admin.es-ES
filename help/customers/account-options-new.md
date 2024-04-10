---
title: Nuevas opciones de cuenta de cliente
description: Obtenga información acerca de las opciones de configuración para nuevas cuentas de cliente en su tienda.
exl-id: aa19f0e2-ffbe-433d-8bd5-c14700b67b37
feature: Customers, Configuration
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Nuevas opciones de cuenta de cliente

En el _[!UICONTROL Create New Account Options]_de la configuración, las opciones básicas de la cuenta se combinan con opciones más avanzadas relacionadas con la validación de ID de IVA y las integraciones personalizadas. Las siguientes instrucciones cubren únicamente las opciones utilizadas con más frecuencia. Para obtener más información sobre las asignaciones automáticas de grupos de clientes, consulte [Validación de IVA](../stores-purchase/vat.md).

![Crear nuevas opciones de cuenta](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## Configurar las opciones básicas de cuenta de cliente

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Customer Configuration]**.

1. Expanda el **[!UICONTROL Create New Account Options]** sección:

   ![Configuración predeterminada de Crear nuevas opciones de cuenta](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. Defina cada una de las opciones según la experiencia del cliente que necesite admitir en su tienda:

   - Establecer **[!UICONTROL Default Group]** al grupo de clientes que se asigna a los clientes nuevos cuando se crea una cuenta.

   - Si tiene un _Impuesto sobre el valor añadido_ número y desea que sea visible para los clientes, establezca **[!UICONTROL Show VAT Number on Storefront]** hasta `Yes`.

   - Para requerir el correo electrónico de un cliente durante la creación de la orden de administración para un cliente, establezca **[!UICONTROL Email is required field for Admin order creation]** hasta `Yes`.

   - Introduzca el **[!UICONTROL Default Email Domain]** para el almacén, como `mystore.com`

   - Establecer **[!UICONTROL Default Welcome Email]** a la plantilla que se utiliza para el correo electrónico de bienvenida enviado a los nuevos clientes.

   - Para exigir a los clientes que confirmen su solicitud de abrir una cuenta en la tienda, configure **[!UICONTROL Require Emails Confirmation]** hasta `Yes`. A continuación, establezca **[!UICONTROL Confirmation Link Email]** a la plantilla que se utiliza para el correo electrónico de confirmación.

     >[!NOTE]
     >
     >A partir de la versión 2.4.7, los clientes deben volver a introducir su correo electrónico y contraseña para iniciar sesión en su cuenta después de la confirmación del correo electrónico, independientemente del explorador.

   - Establecer **[!UICONTROL Welcome Email]** a la plantilla que se utiliza para el mensaje de bienvenida que se envía después de confirmar la cuenta.

   - Establecer **[!UICONTROL Default Welcome Email without Password]** a la plantilla que se utiliza cuando se crea una cuenta de cliente que aún no tiene una contraseña. Por ejemplo, una cuenta de cliente creada desde el Administrador aún no tiene asignada una contraseña.

   - Establecer **[!UICONTROL Email Sender]** al contacto de tienda que aparece como remitente del correo electrónico de bienvenida.

   - Para exigir a los clientes que confirmen su solicitud de abrir una cuenta en la tienda, configure **[!UICONTROL Require Emails Confirmation]** hasta `Yes`. A continuación, establezca **[!UICONTROL Confirmation Link Email]** a la plantilla que se utiliza para el correo electrónico de confirmación.

   ![Crear nuevas opciones de cuenta con IVA activado](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

   Para obtener información detallada sobre cada una de las opciones disponibles en este conjunto de opciones de configuración, consulte la _Crear nuevas opciones de cuenta_ [referencia de configuración](../configuration-reference/customers/customer-configuration.md).

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.
