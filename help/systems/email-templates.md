---
title: Plantillas de correo electrónico
description: Obtenga información sobre las plantillas de correo electrónico y cómo puede utilizarlas para apoyar las comunicaciones con sus clientes y reforzar su marca.
exl-id: dfe28c77-607e-41e4-b872-3a07bcd67962
feature: Communications, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1151'
ht-degree: 0%

---

# Plantillas de correo electrónico

Las plantillas de correo electrónico definen el diseño, el contenido y el formato de los mensajes automatizados enviados desde su tienda. Se denominan correos electrónicos transaccionales porque cada uno está asociado a un tipo específico de transacción o evento.

Commerce incluye un conjunto de plantillas de correo electrónico adaptables que se activan mediante varios eventos que tienen lugar durante el funcionamiento de la tienda. Cada plantilla está optimizada para cualquier tamaño de pantalla y se puede ver desde el escritorio, así como en tabletas y dispositivos móviles. Hay varias plantillas de correo electrónico preparadas relacionadas con actividades de clientes, ventas, alertas de productos, acciones de administración y mensajes del sistema que puedes [personalizar](email-template-custom.md) para que reflejen tu marca.

Los clientes de correo electrónico de texto sin formato y HTML pueden procesar los correos electrónicos de Commerce. Puede haber alguna variación entre los clientes en la forma en que se procesan los correos electrónicos.

## Prepare su logotipo de correo electrónico

Los logotipos se pueden guardar como cualquiera de los siguientes tipos de archivo. Los logotipos con fondos transparentes se pueden guardar como archivos .GIF o .PNG.

- JPG/JPEG
- GIF
- PNG

Hay dimensiones especificadas en la plantilla de encabezado. Sin embargo, para garantizar que el logotipo se represente correctamente en dispositivos de alta resolución, la imagen cargada debe tener un tamaño tres veces superior. Normalmente, la ilustración del logotipo original se crea como una imagen vectorial, por lo que se puede ampliar sin perder resolución. La imagen se puede guardar en uno de los formatos de imagen de mapa de bits admitidos.

<!-- ![Logo 3X display size](./assets/email-logo-third-size.png)-->

Para aprovechar el espacio vertical limitado en el encabezado, asegúrese de recortar la imagen para eliminar cualquier espacio desperdiciado en la parte superior o inferior. Al editar la imagen, tenga cuidado de conservar la relación de aspecto del logotipo, de modo que la altura y la anchura cambien de tamaño proporcionalmente.

Como regla general, puede hacer que una imagen sea más pequeña que la original, pero no más grande sin perder resolución. Al tomar una imagen pequeña y ampliarla en un editor fotográfico, se reduce la resolución de la imagen. Por ejemplo, si las dimensiones de visualización del logotipo son de 168 píxeles de ancho por 48 píxeles de alto en la plantilla de encabezado, la imagen cargada debe ser de 504 píxeles de ancho por 144 píxeles de alto.

| Dimension de logotipo | 1 x (tamaño de visualización) | 3 x (tamaño de imagen) |
|----------|----|----|
| Anchura: | 168 px | 504 px |
| Altura: | 48 px | 144 px |

{style="table-layout:auto"}

## Configurar plantillas de correo electrónico

La configuración determina el logotipo que aparece en la plantilla de encabezado predeterminada y cualquier plantilla [header](email-template-custom.md#header-template) y [footer](email-template-custom.md#footer-template) personalizada que desee usar para los mensajes de correo electrónico transaccionales enviados desde sus tiendas.

![Diseño de correo electrónico transaccional](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

Para obtener una lista detallada de las opciones de configuración, consulte [_Correos electrónicos transaccionales_](../content-design/configuration.md) en la _Guía de contenido y diseño_.

## Paso 1. Cargar el logotipo

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Busque la vista de tienda que desea configurar y haga clic en **[!UICONTROL Edit]** en la columna _[!UICONTROL Action]_.

1. En _[!UICONTROL Other Settings]_, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Transactional Emails]**.

1. Para cargar su **[!UICONTROL Logo Image]** preparado, haga clic en **[!UICONTROL Upload]** y seleccione el archivo de su sistema.

1. Para **[!UICONTROL Logo Image Alt]**, escriba un texto alternativo para identificar la imagen.

1. Escriba **[!UICONTROL Logo Width]** y **[!UICONTROL Logo Height]** en píxeles.

   Escriba cada valor como un número, sin la abreviatura `px`. Estos valores hacen referencia a las dimensiones de visualización del logotipo en el encabezado y no al tamaño real de la imagen.

## Paso 2. Elija las plantillas de encabezado y pie de página

Si tiene plantillas personalizadas de encabezado y pie de página para su tienda o para diferentes tiendas, puede especificar qué plantillas se usan para cada una, según el [ámbito](../getting-started/websites-stores-views.md#scope-settings) de la configuración. De lo contrario, se utilizan las plantillas predeterminadas. Para obtener más información, consulte [Personalizar plantillas de correo electrónico](email-template-custom.md).

1. Elija **[!UICONTROL Header Template]** para usar en todos los mensajes de correo electrónico transaccionales.

1. Elija **[!UICONTROL Footer Template]** para usar en todos los mensajes de correo electrónico transaccionales.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Lista de plantillas de correo electrónico

La lista de plantillas de correo electrónico se organiza alfabéticamente por módulo.

### [!DNL Amazon_Payment]

| Plantilla | Ruta de configuración |
|--- |--- |
| `Hard-declined Authorization` | n/a |
| `Soft-declined Authorization` | n/a |

{style="table-layout:auto"}

### [!DNL Magento_Checkout]

| Plantilla | Ruta de configuración |
|--- |--- |
| `Payment Failed` | **Página:** [!UICONTROL Sales] > [[!UICONTROL Checkout]](../configuration-reference/sales/checkout.md)<br/>**Sección:** [!UICONTROL Payment Failed Emails]<br/>**Campo:** [!UICONTROL Payment Failed Template] |

{style="table-layout:auto"}

### [!DNL Magento_Company]

![Adobe Commerce B2B](../assets/b2b.svg) (disponible solo con Adobe Commerce B2B)

| Plantilla | Ruta de configuración |
|--- |--- |
| `Assign Company Admin` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sección:** [!UICONTROL Customer-Related Emails]<br/>**Campo:** [!UICONTROL Default 'Assign Company Admin' Email] |
| `Assign Company to Customer` | **Página:** [!UICONTROL Customers] > [Configuración de la compañía ](../configuration-reference/customers/company-configuration.md)<br/>**Sección:** [!UICONTROL Customer-Related Emails] <br/>**Campo:** [!UICONTROL Default 'Assign Company to Customer' Email] |
| `Company Admin Changed to Member` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sección:** [!UICONTROL Customer-Related Emails]<br/>**Campo:** [!UICONTROL Default 'Company Admin Changed To Member' Email] |
| `Company Admin Set Inactive` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sección:** [!UICONTROL Customer-Related Emails]<br/>**Campo:** [!UICONTROL Default 'Customer Status Inactive' Email] |
| `Company Invite` | n/a |
| `Company Registration Request` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sección:** [!UICONTROL Email Options - Company Registration]<br/>**Campo:** [!UICONTROL Default Company Registration Email] |
| `Company Status Active1` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sección:** [!UICONTROL Company Status Change]<br/>**Campo:** [!UICONTROL Default 'Company Status Change To Active 1" Email] |
| `Company Status Active2` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sección:** [!UICONTROL Company Status Change]<br/>**Campo:** [!UICONTROL Default 'Company Status Change To Active 2" Email] |
| `Company Status Blocked` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sección:** [!UICONTROL Company Status Change]<br/>**Campo:** [!UICONTROL Default 'Company Status Change To Blocked" Email] |
| `Company Status Pending Approval` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sección:** [!UICONTROL Company Status Change]<br/>**Campo:** [!UICONTROL Default 'Company Status Change To Pending Approval" Email] |
| `Company Status Rejected` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sección:** [!UICONTROL Company Status Change]<br/>**Campo:** [!UICONTROL Default 'Company Status Change To Rejected" Email] |
| `Customer Status Active` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sección:** [!UICONTROL Customer-Related Emails]<br/>**Campo:** [!UICONTROL Default 'Customer Status Active' Email] |
| `Customer Status Inactive` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sección:** [!UICONTROL Customer-Related Emails]<br/>**Campo:** [!UICONTROL Default 'Company Admin Inactive' Email] |
| `Sales Representative Assigned to Company` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sección:** [!UICONTROL Customer-Related Emails]<br/>**Campo:** [!UICONTROL Default 'Sales Rep Assigned' Email] |

{style="table-layout:auto"}

### [!DNL Magento_CompanyCredit]

![Adobe Commerce B2B](../assets/b2b.svg) (disponible solo con Adobe Commerce B2B)

| Plantilla | Ruta de configuración |
|--- |--- |
| `Credit Limit Allocated` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sección:** [!UICONTROL Company Credit]<br/>**Campo:** [!UICONTROL Allocated Email Template] |
| `Credit Limit Updated` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sección:** [!UICONTROL Company Credit]<br/>**Campo:** [!UICONTROL Updated Email Template] |
| `Credit Reimbursed` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sección:** [!UICONTROL Company Credit]<br/>**Campo:** [!UICONTROL Reimbursed Email Template] |
| `Order Refunded to Company Credit` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sección:** [!UICONTROL Company Credit]<br/>**Campo:** [!UICONTROL Refunded Email Template] |
| `Order Reverted to Company Credit` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sección:** [!UICONTROL Company Credit]<br/>**Campo:** [!UICONTROL Reverted Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Contact]

| Plantilla | Ruta de configuración |
|--- |--- |
| `Contact Form` | **Página:** [!UICONTROL General] > [[!UICONTROL Contacts]](../configuration-reference/general/contacts.md)<br/>**Sección:** [!UICONTROL Email Options]<br/>**Campo:** [!UICONTROL Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Customer]

| Plantilla | Ruta de configuración |
|--- |--- |
| `Change Email` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sección:** [!UICONTROL Account Information Options]<br/>**Campo:** [!UICONTROL Change Email Template] |
| Cambiar correo electrónico y contraseña | **Página:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sección:** [!UICONTROL Account Information Options]<br/>**Campo:** [!UICONTROL Change Email and Password Template] |
| `Forgot Password` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sección:** [!UICONTROL Password Options]<br/>**Campo:** Plantilla de correo electrónico olvidada |
| `New Account` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sección:** [!UICONTROL Create New Account Options]<br/>**Campo:** Correo electrónico de bienvenida predeterminado |
| `New Account (Magento/luma)` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sección:** [!UICONTROL Create New Account Options]<br/>**Campo:** Correo electrónico de bienvenida predeterminado |
| `New Account Confirmation Key` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sección:** [!UICONTROL Create New Account Options]<br/>**Campo:** Correo electrónico de vínculo de confirmación |
| `New Account Confirmed` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sección:** [!UICONTROL Create New Account Options]<br/>**Campo:** Correo electrónico de bienvenida |
| `New Account Without Password` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sección:** [!UICONTROL Create New Account Options]<br/>**Campo:** Correo electrónico de bienvenida predeterminado sin contraseña |
| `Remind Password` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sección:** [!UICONTROL Password Options]<br/>**Campo:** Plantilla de correo electrónico de recordatorio |
| `Reset Password` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sección:** [!UICONTROL Password Options] <br/>**Campo:** Restablecer plantilla de contraseña |

{style="table-layout:auto"}

### [!DNL Magento_CustomerBalance]

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

| Plantilla | Ruta de configuración |
|--- |--- |
| `Store Credit Update` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sección:** [!UICONTROL Store Credit Options]<br/>**Campo:** [!UICONTROL Store Credit Update Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Directory]

| Plantilla | Ruta de configuración |
|--- |--- |
| `Currency Update Warnings` | **Página:** [!UICONTROL General] > [[!UICONTROL Currency Setup]](../configuration-reference/general/currency-setup.md)<br/>**Sección:** [!UICONTROL Scheduled Import Settings]<br/>**Campo:** [!UICONTROL Error Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Email]

| Plantilla | Ruta de configuración |
|--- |--- |
| `Footer` | n/a |
| `Footer (Magento/luma)` | n/a |
| `Header` | n/a |

{style="table-layout:auto"}

### [!UICONTROL Magento_GiftCard]

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

| Plantilla | Ruta de configuración |
|--- |--- |
| `Gift Card(s) Purchase` | **Página:** [!UICONTROL Sales] > [[!UICONTROL Gift Cards]](../catalog/product-gift-card-create.md)<br/>**Sección:** [!UICONTROL Gift Card Email Settings]<br/>**Campo:** [!UICONTROL Gift Card Notification Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_GiftCardAccount]

| Plantilla | Ruta de configuración |
|--- |--- |
| `Gift Card Code/Balance` | **Página:** [!UICONTROL Sales] > [[!UICONTROL Gift Cards]](../catalog/product-gift-card-create.md)<br/>**Sección:** [!UICONTROL Email Sent from Gift Card Account Management]<br/>**Campo:** [!UICONTROL Gift Card Template] |

{style="table-layout:auto"}

### [!DNL Magento_GiftRegistry]

| Plantilla | Ruta de configuración |
|--- |--- |
| `New Registry` | **Página:** [!UICONTROL &#x200B; Customers] > [[!UICONTROL &#x200B; Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**Sección:** [!UICONTROL Owner Notification]<br/>**Campo:** [!UICONTROL Email Template] |
| `Registry Sharing` | **Página:** [!UICONTROL &#x200B; Customers] > [[!UICONTROL &#x200B; Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**Sección:** [!UICONTROL Gift Registry Sharing]<br/>**Campo:** [!UICONTROL Email Template] |
| `Registry Update` | **Página:** [!UICONTROL &#x200B; Customers] > [[!UICONTROL &#x200B; Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**Sección:** [!UICONTROL Gift Registry Update]<br/>**Campo:** [!UICONTROL Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_InventoryInStorePickupSales]

| Plantilla | Ruta de configuración |
|--- |--- |
| `Order is Ready for Pickup` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL Order Ready For Pickup in Store]<br/>**Campo:** [!UICONTROL Order Ready For Pickup Email Template] |
| `Order is Ready for Pickup For Guest` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL Order Ready For Pickup in Store]<br/>**Campo:** [!UICONTROL Order Ready For Pickup Email Template for Guest] |

{style="table-layout:auto"}

### [!DNL Magento_Invitation]

| Plantilla | Ruta de configuración |
|--- |--- |
| `Customer Invitation` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Invitation]](../configuration-reference/customers/invitations.md)<br/>**Sección:** [!UICONTROL Email]<br/>**Campo:** [!UICONTROL Customer Invitation Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_NegotiableQuote]

![Adobe Commerce B2B](../assets/b2b.svg) (disponible solo con Adobe Commerce B2B)

| Plantilla | Ruta de configuración |
|--- |--- |
| `Declined Quote` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL Quote]<br/>**Campo:** [!UICONTROL Declined Quote Template (to Buyer)] |
| `Expiration Date Reset` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL Quote]<br/>**Campo:** [!UICONTROL Expiration Date Reset] | **Página:** [!UICONTROL Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL Quote]<br/>**Campo:** [!UICONTROL Order Ready For Pickup Email Template] |
| `Expiration Warning` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL Quote]<br/>**Campo:** [!UICONTROL Quote Expiration (in 48 hrs)] |
| `Expiration Warning1` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL Quote]<br/>**Campo:** [!UICONTROL Quote Expiration (in 24 hrs)] |
| `New Quote` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL Quote]<br/>**Campo:** [!UICONTROL New Quote Template (to Seller)] |
| `Updated Quote` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL Quote]<br/>**Campo:** [!UICONTROL Updated Quote Template (to Seller)] |

{style="table-layout:auto"}

### [!DNL Magento_Newsletter]

| Plantilla | Ruta de configuración |
|--- |--- |
| `Subscription Confirmation` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**Sección:** [!UICONTROL &#x200B; Subscription Options]<br/>**Campo:** [!UICONTROL Confirmation Email Template] |
| `Subscription Success` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**Sección:** [!UICONTROL &#x200B; Subscription Options]<br/>**Campo:** [!UICONTROL Success Email Template] |
| `Unsubscription Success` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**Sección:** [!UICONTROL &#x200B; Subscription Options]<br/>**Campo:** [!UICONTROL Unsubscription Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_ProductAlert]

| Plantilla | Ruta de configuración |
|--- |--- |
| `Cron Error Warning` | **Página:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**Sección:** [!UICONTROL Product Alerts Run Settings]<br/>**Campo:** [!UICONTROL Error Email Template] |
| `Price Alert` | **Página:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**Sección:** [!UICONTROL Product Alerts]<br/>**Campo:** [!UICONTROL Price Alert Email Template] |
| `Stock Alert` | **Página:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**Sección:** [!UICONTROL Product Alerts]<br/>**Campo:** [!UICONTROL Stock Alert Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_PurchaseOrder]

| Plantilla | Ruta de configuración |
|--- |--- |
| `Approved Purchase Order` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL Purchase Order Approval]<br/>**Campo:** [!UICONTROL Approved Purchase Order] |
| `Approved, requires payment` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL Purchase Order Approval]<br/>**Campo:** [!UICONTROL Approved, requires payment details (to Buyer)] |
| `Comment added to Purchase Order` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL Purchase Order Approval]<br/>**Campo:** [!UICONTROL Comment added to Purchase Order] |
| `Created and Auto-approved Purchase Order` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL Purchase Order Approval]<br/>**Campo:** [!UICONTROL Created and Automatically approved Purchase Order (to Buyer)] |
| `Created and automatically approved, requires payment details` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL Purchase Order Approval]<br/>**Campo:** [!UICONTROL Created and automatically approved, requires payment details (to Buyer)] |
| `Created and requires Approval Purchase Order` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL Purchase Order Approval]<br/>**Campo:** [!UICONTROL Created and requires Approval Purchase Order (to Buyer)] |
| `Error creating Order from Purchase Order` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL Purchase Order Approval]<br/>**Campo:** [!UICONTROL Error creating Order from Purchase Order (to Buyer)] |
| `Purchase Order requires Approval` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL Purchase Order Approval]<br/>**Campo:** [!UICONTROL Purchase Order requires Approval (to Approver)] |
| `Rejected Purchase Order` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL Purchase Order Approval]<br/>**Campo:** [!UICONTROL Rejected Purchase Order (to Buyer)] |

{style="table-layout:auto"}

### [!DNL Magento_Reminder]

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

| Plantilla | Ruta de configuración |
|--- |--- |
| `Promotion Notification/Reminder` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Promotions]](../configuration-reference/customers/promotions.md)<br/>**Sección:** [!UICONTROL Automated Email Reminder Rules]<br/>**Campo:** [!UICONTROL Reminder Email Sender] |

{style="table-layout:auto"}

### [!DNL Magento_Reward]

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

| Plantilla | Ruta de configuración |
|--- |--- |
| `Balance Update` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Reward Points]](../configuration-reference/customers/reward-points.md)<br/>**Sección:** [!UICONTROL Email Notification Settings]<br/>**Campo:** [!UICONTROL Balance Update Email] |
| `Points Expiry Warning` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Reward Points]](../configuration-reference/customers/reward-points.md)<br/>**Sección:** [!UICONTROL Email Notification Settings]<br/>**Campo:** [!UICONTROL Reward Points Expiry Warning Email] |

{style="table-layout:auto"}

### [!DNL Magento_Rma]

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

| Plantilla | Ruta de configuración |
|--- |--- |
| `New RMA` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL &#x200B; RMA]<br/>**Campo:** [!UICONTROL RMA Email Template] |
| `New RMA for Guest` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL &#x200B; RMA]<br/>**Campo:** [!UICONTROL RMA Email Template for Guest] |
| `RMA Admin Comments` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL &#x200B; RMA Admin Comments]<br/>**Campo:** [!UICONTROL RMA Comment Email Template] |
| `RMA Admin Comments for Guest` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL &#x200B; RMA Admin Comments]<br/>**Campo:** [!UICONTROL RMA Comment Email Template for Guest] |
| `RMA Authorization` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL &#x200B; RMA Authorization]<br/>**Campo:** [!UICONTROL RMA Authorization Email Template] |
| `RMA Authorization for Guest` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL &#x200B; RMA Authorization]<br/>**Campo:** [!UICONTROL RMA Authorization Email Template for Guest] |
| `RMA Customer Comments` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sección:** [!UICONTROL RMA Customer Comments]<br/>**Campo:** [!DNL RMA Comment Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Sales]

| Plantilla | Ruta de configuración |
|--- |--- |
| `Credit Memo Update` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Credit Memo Contents]<br/>**Campo:** [!UICONTROL Credit Memo Comment Email Template] |
| `Credit Memo Update (Magento/luma)` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Credit Memo Comments]<br/>**Campo:** [!UICONTROL Credit Memo Comment Email Template] |
| `Credit Memo Update for Guest` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Credit Memo Comments]<br/>**Campo:** [!UICONTROL Credit Memo Comment Email Template for Guest] |
| `Credit Memo Update for Guest (Magento/luma)` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Credit Memo Comments]<br/>**Campo:** [!UICONTROL Credit Memo Comment Email Template for Guest] |
| `Invoice Update` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Invoice Comments]<br/>**Campo:** [!UICONTROL Invoice Comment Email Template] |
| `Invoice Update (Magento/luma)` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Invoice Comments]<br/>**Campo:** [!UICONTROL Invoice Comment Email Template] |
| `Invoice Update for Guest` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Invoice Comments]<br/>**Campo:** [!UICONTROL Invoice Comment Email Template for Guest] |
| `Invoice Update for Guest (Magento/luma)` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Invoice Comments]<br/>**Campo:** [!UICONTROL Invoice Comment Email Template for Guest] |
| `New Credit Memo` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Credit Memo]<br/>**Campo:** [!UICONTROL Credit Memo Email Template] |
| `New Credit Memo (Magento/luma)` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]]../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Credit Memo]<br/>**Campo:** [!UICONTROL Credit Memo Email Template] |
| `New Credit Memo for Guest` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Credit Memo]<br/>**Campo:** [!UICONTROL Credit Memo Email Template for Guest] |
| `New Credit Memo for Guest (Magento/luma)` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Credit Memo]<br/>**Campo:** [!UICONTROL Credit Memo Email Template for Guest] |
| `New Invoice` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Invoice]<br/>**Campo:** [!UICONTROL Invoice Email Template] |
| `New Invoice (Magento/luma)` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Invoice]<br/>**Campo:** [!UICONTROL Invoice Email Template] |
| `New Invoice for Guest` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Invoice]<br/>**Campo:** [!UICONTROL Invoice Email Template for Guest] |
| `New Invoice for Guest (Magento/luma)` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Invoice]<br/>**Campo:** [!UICONTROL Invoice Email Template for Guest] |
| `New Order` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Order]<br/>**Campo:** [!UICONTROL New Order Confirmation Template] |
| `New Order (Magento/luma)` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Order]<br/>**Campo:** [!UICONTROL New Order Confirmation Template] |
| `New Order for Guest` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Order]<br/>**Campo:** [!UICONTROL New Order Confirmation Template for Guest] |
| `New Order for Guest (Magento/luma)` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Order]<br/>**Campo:** [!UICONTROL New Order Confirmation Template for Guest] |
| `New Shipment` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Shipment]<br/>**Campo:** [!UICONTROL Shipment Email Template] |
| `New Shipment (Magento/luma)` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Shipment]<br/>**Campo:** [!UICONTROL Shipment Email Template] |
| `New Shipment for Guest` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Shipment]<br/>**Campo:** [!UICONTROL Shipment Email Template for Guest] |
| `New Shipment for Guest (Magento/luma)` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Shipment]<br/>**Campo:** [!UICONTROL Shipment Email Template for Guest] |
| `Order Update` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Order Comments]<br/>**Campo:** [!UICONTROL Order Comment Email Template] |
| `Order Update (Magento/luma)` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Order Comments]<br/>**Campo:** [!UICONTROL Order Comment Email Template] |
| `Order Update for Guest` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Order Comments]<br/>**Campo:** [!UICONTROL Order Comment Email Template for Guest] |
| `Order Update for Guest (Magento/luma)` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Order Comments]<br/>**Campo:** [!UICONTROL Order Comment Email Template for Guest] |
| `Shipment Update` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Shipment Comments]<br/>**Campo:** [!UICONTROL Shipment Comment Email Template] |
| `Shipment Update (Magento/luma)` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Shipment Comments]<br/>**Campo:** [!UICONTROL Shipment Comment Email Template] |
| `Shipment Update for Guest` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Shipment Comments]<br/>**Campo:** [!UICONTROL Shipment Comment Email Template for Guest] |
| `Shipment Update for Guest (Magento/luma)` | **Página:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sección:** [!UICONTROL Shipment Comments]<br/>**Campo:** [!UICONTROL Shipment Comment Email Template for Guest] |

{style="table-layout:auto"}

### [!DNL Magento_ScheduledImportExport]

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

| Plantilla | Ruta de configuración |
|--- |--- |
| `Export Failed` | **Página:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**Sección:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**Campo:** [!UICONTROL Export Failed Template] |
| `File History Clean Failed` | **Página:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**Sección:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**Campo:** [!UICONTROL Error Email Template] |
| `Import Failed` | **Página:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**Sección:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**Campo:** [!UICONTROL Import Failed Template] |

{style="table-layout:auto"}

### [!DNL Magento_SendFriend]

| Plantilla | Ruta de configuración |
|--- |--- |
| `Send Product Link to Friend` | **Página:** [!UICONTROL Catalog] > [[!UICONTROL Email to a Friend]](../configuration-reference/catalog/email-to-a-friend.md)<br/>**Sección:** [!UICONTROL Email Templates]<br/>**Campo:** [!UICONTROL Select Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Sitemap]

| Plantilla | Ruta de configuración |
|--- |--- |
| `Sitemap Generation Settings` | **Página:** [!UICONTROL Catalog] > [[!UICONTROL XML Sitemap]](../configuration-reference/catalog/xml-sitemap.md)<br/>**Sección:** [!UICONTROL Generation Settings]<br/>**Campo:** [!UICONTROL Error Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_TwoFactorAuth]

| Plantilla | Ruta de configuración |
|--- |--- |
| `2FA Configuration Required by User` | n/a |
| `2FA Configuration Required for the Application` | n/a |

{style="table-layout:auto"}

### [!DNL Magento_User]

| Plantilla | Ruta de configuración |
|--- |--- |
| `Forgot Admin Password` | **Página:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**Sección:** [!UICONTROL Admin User Emails]<br/>**Campo:** Plantilla de correo electrónico de contraseña olvidada |
| `User Notification` | **Página:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**Sección:** [!UICONTROL Admin User Emails]<br/>**Campo:** Plantilla de notificación de usuario |
| `New User Notification` | **Página:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**Sección:** [!UICONTROL Admin User Emails]<br/>**Campo:** [!UICONTROL New User Notification Template] |

{style="table-layout:auto"}

### [!DNL Magento_Wishlist]

| Plantilla | Ruta de configuración |
|--- |--- |
| `Magento Wish List Sharing` | **Página:** [!UICONTROL Customers] > [[!UICONTROL Wish List]](../configuration-reference/customers/wishlist.md)<br/>**Sección:** [!UICONTROL Share Options]<br/>**Campo:** [!UICONTROL Email Template] |

{style="table-layout:auto"}
