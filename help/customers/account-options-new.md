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

En la sección _[!UICONTROL Create New Account Options]_&#x200B;de la configuración, las opciones básicas de la cuenta se combinan con opciones más avanzadas relacionadas con la validación de ID de IVA y las integraciones personalizadas. Las siguientes instrucciones cubren únicamente las opciones utilizadas con más frecuencia. Para obtener más información acerca de las asignaciones automáticas de grupos de clientes, consulte [Validación de IVA](../stores-purchase/vat.md).

![Crear nuevas opciones de cuenta](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## Configurar las opciones básicas de cuenta de cliente

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Customer Configuration]**.

1. Expanda la sección **[!UICONTROL Create New Account Options]**:

   ![Crear nueva configuración predeterminada de opciones de cuenta](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. Defina cada una de las opciones según la experiencia del cliente que necesite admitir en su tienda:

   - Establezca **[!UICONTROL Default Group]** en el grupo de clientes que se asigna a los clientes nuevos cuando se crea una cuenta.

   - Si tiene un número de _Impuesto al valor agregado_ y desea que sea visible para los clientes, establezca **[!UICONTROL Show VAT Number on Storefront]** en `Yes`.

   - Para requerir el correo electrónico de un cliente durante la creación de la orden de administración para un cliente, establezca **[!UICONTROL Email is required field for Admin order creation]** en `Yes`.

   - Escriba **[!UICONTROL Default Email Domain]** para la tienda, como `mystore.com`

   - Establezca **[!UICONTROL Default Welcome Email]** en la plantilla que se usa para el correo electrónico de bienvenida enviado a los nuevos clientes.

   - Para requerir que los clientes confirmen su solicitud de abrir una cuenta en su tienda, establezca **[!UICONTROL Require Emails Confirmation]** en `Yes`. A continuación, configure **[!UICONTROL Confirmation Link Email]** en la plantilla que se usa para el correo electrónico de confirmación.

     >[!NOTE]
     >
     >A partir de la versión 2.4.7, los clientes deben volver a introducir su correo electrónico y contraseña para iniciar sesión en su cuenta después de la confirmación del correo electrónico, independientemente del explorador.

   - Establezca **[!UICONTROL Welcome Email]** en la plantilla que se usa para el mensaje de bienvenida que se envía después de que se confirme la cuenta.

   - Establezca **[!UICONTROL Default Welcome Email without Password]** en la plantilla que se usa cuando se crea una cuenta de cliente que aún no tiene una contraseña. Por ejemplo, una cuenta de cliente creada desde el Administrador aún no tiene asignada una contraseña.

   - Establezca **[!UICONTROL Email Sender]** en el contacto de tienda que aparece como remitente del correo electrónico de bienvenida.

   - Para requerir que los clientes confirmen su solicitud de abrir una cuenta en su tienda, establezca **[!UICONTROL Require Emails Confirmation]** en `Yes`. A continuación, configure **[!UICONTROL Confirmation Link Email]** en la plantilla que se usa para el correo electrónico de confirmación.

   ![Crear nuevas opciones de cuenta con IVA habilitado](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

   Para obtener información detallada sobre cada una de las opciones disponibles en este conjunto de opciones de configuración, consulte la _Referencia de configuración[&#128279;](../configuration-reference/customers/customer-configuration.md) de Crear nuevas opciones de cuenta_.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
