---
title: '[!UICONTROL Advanced] &gt; [!UICONTROL Admin]'
description: Revise la configuración en la página [!UICONTROL Advanced] &gt; [!UICONTROL Admin] del administrador de Commerce.
exl-id: 546b8d01-9611-4415-ab2b-29be560316f5
role: Admin
feature: Configuration, Admin Workspace
source-git-commit: e05d13f79ceb2fe24c1931fefb48317ebd36d1fc
workflow-type: tm+mt
source-wordcount: '1209'
ht-degree: 0%

---

# Avanzadas > Administración

{{config}}

## [!UICONTROL Admin User Emails]

![Correos electrónicos de usuarios administradores](./assets/admin-admin-user-emails.png)<!-- zoom -->

Para obtener más información acerca de cómo cambiar esta configuración, vea [Contraseña olvidada y restablecer correo electrónico](../../systems/permissions-users-all.md#forgotten-password-and-reset-emails).

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|---------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Forgot Password Email Template] | Global | Identifica la plantilla de correo electrónico que se utiliza para el mensaje que se envía cuando un usuario administrador olvida su contraseña. Plantilla predeterminada: `Forgot Admin Password` |
| [!UICONTROL Forgot and Reset Email Sender] | Global | Identifica al contacto de la tienda que aparece como remitente del correo electrónico _Olvidé la contraseña_. Remitente predeterminado: `General Contact`<br/>Otras opciones de remitente: `Sales Representative`, `Customer Support`, `Custom Email` |
| [!UICONTROL User Notification Template] | Global | Determina la plantilla de correo electrónico que se utiliza de forma predeterminada para las notificaciones a los administradores. Plantilla predeterminada: `User Notification` |

{style="table-layout:auto"}

## [!UICONTROL Startup Page]

![Página de inicio](./assets/admin-startup-page.png)<!-- zoom -->

Para obtener más información sobre cómo cambiar esta configuración, consulte [Cambiar la página de inicio](../../getting-started/admin-dashboard.md#change-the-startup-page) en la _Guía de introducción_.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|---------------------------|------------------------------------------------------------------------|------------------------------------------------------------------|
| [!UICONTROL Startup Page] | Global | Determina la página de aterrizaje de administración que aparece después de iniciar sesión. |

{style="table-layout:auto"}

### [!UICONTROL Startup Page] opciones

| Área |                                                                                                                                                                                                                                                                                                                                                                           | Opción |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`Dashboard`](../../getting-started/admin-dashboard.md) |                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `Sales` | `Operations` | [`Quotes`](../../b2b/quotes.md) ![Adobe Commerce B2B](../../assets/b2b.svg) <br/>[`Orders`](../../stores-purchase/orders.md)<br/>[`Invoices`](../../stores-purchase/invoices.md)<br/>[`Shipments`](../../stores-purchase/shipments.md)<br/>[`Credit Memos`](../../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../../stores-purchase/returns.md) ![Adobe Commerce](../../assets/adobe-logo.svg) </span><br/>[`Transactions`](../../stores-purchase/transactions.md)<br/>`Braintree Virtual Terminal` |
| `Catalog` | [`Inventory`](../../inventory-management/introduction.md) | [`Products`](../../catalog/products-list.md)<br/>[`Categories`](../../catalog/categories.md)<br/>[`Shared Catalog`](../../b2b/catalog-shared-create.md) ![Adobe Commerce B2B](../../assets/b2b.svg) |
| `Customers` | [`All Customers`](../../customers/customers-all.md)<br/>[`Now Online`](../../customers/now-online.md)<br/>[`Customer Groups`](../../customers/customer-groups.md)<br/>[`Segments`](../../customers/customer-segments.md) ![Adobe Commerce](../../assets/adobe-logo.svg) <br/>[`Companies`](../../b2b/account-companies.md)![Adobe Commerce B2B](../../assets/b2b.svg) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `Marketing` | `Promotions` | [`Catalog Price Rule`](../../merchandising-promotions/price-rules-catalog.md) <br/>[`Cart Price Rules`](../../merchandising-promotions/price-rules-cart.md)) <br/>[`Related Products Rules`](../../merchandising-promotions/product-related-rules.md) ![Adobe Commerce](../../assets/adobe-logo.svg) <br/>[`Gift Card Accounts`](../../stores-purchase/product-gift-card-accounts.md) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | [`Private Sales`](../../merchandising-promotions/events-private-sales.md) ![Adobe Commerce](../../assets/adobe-logo.svg) | [`Events`](../../merchandising-promotions/event-configure.md) <br/>[`Invitations`](../../merchandising-promotions/invitations.md) |
|                                                         | `Communications` | [`Email Templates`](../../systems/email-templates.md) <br/>[`Newsletter Template`](../../merchandising-promotions/newsletter-template.md) <br/>[`Newsletter Queue`](../../merchandising-promotions/newsletter-queue.md) <br/>[`Newsletter Subscribers`](../../merchandising-promotions/newsletter-subscribers.md) <br/>[`Email Reminders`](../../merchandising-promotions/email-reminder-rules.md) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | `SEO & Search` | [`Search Terms`](../../catalog/search-terms.md) <br/>[`Search Synonyms`](../../catalog/search-terms.md#search-synonyms) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`URL Rewrites`](../../merchandising-promotions/url-rewrite.md) <br/>[`Site Map`](../../merchandising-promotions/sitemap-xml.md) |
|                                                         | [`User Content`](../../catalog/settings-advanced-product-reviews.md) | [`All Reviews`](../../catalog/settings-advanced-product-reviews.md) <br/>[`Pending Reviews`](../../merchandising-promotions/product-reviews-moderate.md) <br/> |
| `Content` | `Elements` | [`Pages`](../../content-design/pages.md)<br/>[`Hierarchy`](../../content-design/page-hierarchy.md) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`Blocks`](../../content-design/blocks.md)<br/>[`Dynamic Blocks`](../../content-design/dynamic-blocks.md) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`Widgets`](../../content-design/widgets.md)<br/>[`Media Gallery`](../../content-design/media-storage.md) |
|                                                         | `Design` | [`Configuration`](../../content-design/configuration.md)<br/>[`Themes`](../../content-design/themes.md)<br/>[`Schedule`](../../content-design/schedule.md) |
|                                                         | `Content Staging` ![Adobe Commerce](../../assets/adobe-logo.svg)<br /> | [Tablero](../../content-design/content-staging.md) |
| `Reports` | [`Marketing`](../../getting-started/marketing-reports.md) | `Products in Cart`<br />`Search Terms`<br />`Abandoned Carts`<br />`Newsletter Problem Reports` |
|                                                         | [`Reviews`](../../getting-started/review-reports.md) | `By Customer`<br/> `By Products`<br/> |
|                                                         | [`Sales`](../../getting-started/sales-reports.md) | `Orders`<br/>`Tax`<br/>`Invoiced`<br/>`Shipping`<br/>`Refunds`<br/>`Coupons`<br/>`PayPal Settlement`<br/>`Braintree Settlement` |
|                                                         | `System Insights` | [`Site-Wide Analysis Tool`](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | [`Customers`](../../getting-started/customer-reports.md) | `Order Total`<br/>`Order Count`<br/>`New`<br/>`Wish Lists`<br/>`Segments`<br/> |
|                                                         | [`Products`](../../getting-started/product-reports.md) | `Views`<br/>`Bestsellers`<br/>`Low Stock`<br/>`Ordered`<br/>`Downloads` |
|                                                         | [`Private Sales`](../../getting-started/private-sales-reports.md) ![Adobe Commerce](../../assets/adobe-logo.svg) | `Invitations`<br/>`Invited Customers`<br/>`Conversions` |
|                                                         | `Statistics` | [`Refresh Statistics`](../../getting-started/sales-reports.md#refresh-statistics) |
|                                                         | [`Business Intelligence`](../../getting-started/business-intelligence.md) | `Advanced Reporting`<br/>`BI Essentials`<br/> |
|                                                         | `Customer Engagement` | `Dashboard`<br/>`Importer Status`<br/>`Automation Enrollment`<br/>`Campaign Sends`<br/>`SMS Sends`<br/>`Cron Tasks`<br/>`Log Viewer`<br/>`Abandoned Carts` |
| `Stores` | `Settings` | [`All Stores`](../../stores-purchase/stores.md)<br/>[`Configuration`](../../configuration-reference/guide-overview.md)<br/>[`Terms and Conditions`](../../stores-purchase/terms-and-conditions.md)<br/>[`Order Status`](../../stores-purchase/order-status.md) |
|                                                         | [`Inventory`](../../inventory-management/introduction.md) | [`Sources`](../../inventory-management/sources-stocks.md#sources)<br/>[`Stocks`](../../inventory-management/sources-stocks.md#stocks) |
|                                                         | [`Taxes`](../../stores-purchase/taxes.md) | [`Tax Rules`](../../stores-purchase/tax-rules.md)<br/>[`Tax Zones and Rates`](../../stores-purchase/tax-zones-rates.md) |
|                                                         | [`Currency`](../../stores-purchase/currency.md) | [`Currency Rates`](../../stores-purchase/currency-configuration.md)<br/>[`Currency Symbols`](../../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) |
|                                                         | `Attributes` | [`Customer`](../../systems/data-attributes-customer.md)<br/>[`Customer Address`](../../systems/data-attributes-customer.md#customer-addresses)<br/>[`Product`](../../systems/data-attributes-product.md)<br/>[`Attribute Set`](../../catalog/attribute-sets.md)<br/>[`Returns`](../../stores-purchase/attributes-returns.md)<br/>[`Ratings`](../../merchandising-promotions/product-reviews.md#create-custom-ratings) |
|                                                         | `Other Settings` | [`Reward Exchange Rates`](../../merchandising-promotions/reward-exchange-rates.md)<br/>[`Gift Wrapping`](../../stores-purchase/cart-configuration.md#gift-wrap)<br/>[`Gift Registry`](../../merchandising-promotions/gift-registry-create.md) |
| `System` | [`Data Transfer`](../../systems/data-transfer.md) | [`Import`](../../systems/data-import.md)<br/>[`Export`](../../systems/data-export.md)<br/>[`Import/Export Tax Rates`](../../systems/data-transfer-tax-rates.md)<br/>[`Import History`](../../systems/data-import.md#import-history)<br/>[`Scheduled Import/Export`](../../systems/data-scheduled-import-export.md) |
|                                                         | `Extensions` | [`Integrations`](../../systems/integrations.md) |
|                                                         | `Tools` | [`Cache Management`](../../systems/cache-management.md)<br/>[`Index Management`](../../systems/index-management.md) |
|                                                         | `Support` | [`System Report`](../../systems/support.md#system-reports) |
|                                                         | `Permissions` | [`All Users`](../../systems/permissions-users-all.md)<br/>[`Locked Users`](../../systems/permissions-users-all.md#locked-users)<br/>[`User Roles`](../../systems/permissions-user-roles.md) |
|                                                         | `Action Log` ![Adobe Commerce](../../assets/adobe-logo.svg) | [`Report`](../../systems/action-log.md)<br/>[`Archive`](../../systems/action-log-archive.md)<br/>[`Bulk Actions`](../../systems/action-log-bulk-actions.md) |
|                                                         | `Other Settings` | [`Notifications`](../../systems/notifications.md)<br/>[`Custom Variables`](../../systems/variables-custom.md)<br/>[`Manage Encryption Key`](../../systems/encryption-key.md) |
| `Find Partners & Extensions` |                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

{style="table-layout:auto"}

<!-- Feature still in development 
## [!UICONTROL Unified Experience]

![Store Configuration for Unified Experience](./assets/admin-uex-configuration.png)

The [!UICONTROL Unified Experience] option is available in Adobe Commerce deployments that have the Commerce Admin Unified Experience extension loaded. This extension enables integration with Experience Cloud to streamline cross-application workflows between Commerce and other Experience Cloud solutions. See [Adobe Experience Cloud Integration for Commerce Admin](../../getting-started/admin-unified-experience-integration-overview.md).

| Field        | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Description                                                                                                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Enable       | Global                                                                 | Determines if the Commerce instance uses the Experience Cloud integration. Before enabling this feature, review the [requirements and configuration instructions](../../getting-started/admin-unified-experience-integration-overview.md). Options: Yes/No.                                                                                                                    |
| Project Name | Global                                                                 | Identifies the instance in the Experience Cloud Commerce Projects workspace when the Unified Experience is enabled. The name can contain only alphanumeric characters and spaces. Defaults to the [cloud environment name](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-architecture.html?lang=en#pro-environment-architecture). |

{style="table-layout:auto"}

-->

## [!UICONTROL Admin Base URL]

![URL de base de administración](./assets/admin-admin-base-url.png)<!-- zoom -->

Para obtener más información acerca de cómo configurar estas opciones, consulte [Configurar la dirección URL base](../../stores-purchase/store-urls.md#configure-the-base-url) en la _Guía de tiendas y compras_.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|------------------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Use Custom Admin URL] | Global | Determina si se utiliza una dirección URL personalizada para acceder al administrador. Opciones: `Yes` / `No` |
| [!UICONTROL Custom Admin URL] | Global | Especifica una dirección URL personalizada para acceder al administrador. De forma predeterminada, la URL de administración es la misma que la URL base.<br/>**Importante:** La dirección URL del administrador debe estar en la misma instalación de Commerce y tener la misma raíz de documento que la tienda. |
| [!UICONTROL Use Custom Admin Path] | Global | Determina si se utiliza una ruta personalizada para acceder al administrador. La ruta predeterminada es `admin`. Opciones: `Yes` / `No` |
| [!UICONTROL Custom Admin Path] | Global | Cambia el nombre de la ruta de administración predeterminada a algo difícil de adivinar. Escriba el nombre de la ruta personalizada en caracteres en minúsculas. Por ejemplo: `aardvark` |

{style="table-layout:auto"}

## [!UICONTROL Security]

![Seguridad](./assets/admin-security.png)<!-- zoom -->

Para obtener más información sobre cómo configurar estas opciones, consulte [Configurar la seguridad de administración](../../systems/security-admin.md) en la _Guía de sistemas de administración_.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Admin Account Sharing] | Vista de tienda | Determina si un usuario administrador puede iniciar sesión en la misma cuenta simultáneamente desde distintos dispositivos. Opciones: <br/>**`Yes`**: permite varias sesiones activas desde la misma cuenta de administrador.<br/>**`No`** - Permite solamente una sesión activa por cuenta de administrador. |
| [!UICONTROL Password Reset Protection Type] | Vista de tienda | Determina el método que se utiliza para administrar las solicitudes de restablecimiento de contraseña. Opciones: <br/>**`By IP and Email`**: la contraseña se puede restablecer en línea después de recibir una respuesta de la notificación y enviarla a la dirección de correo electrónico asociada a la cuenta de administrador.<br/>**`By IP`** - La contraseña se puede restablecer en línea sin confirmación adicional. <br/>**`By Email`**: la contraseña solo se puede restablecer respondiendo por correo electrónico a la notificación que se envía a la dirección de correo electrónico asociada a la cuenta de administrador.<br/>**`None`**: solo el administrador del almacén puede restablecer la contraseña. |
| [!UICONTROL Recovery Link Expiration Period (hours)] | Global | Determina el número de horas que un vínculo de recuperación de contraseña sigue siendo válido. |
| [!UICONTROL Max Number of Password Reset Requests] | Vista de tienda | Determina la cantidad máxima de solicitudes de contraseña que se pueden enviar por hora. |
| [!UICONTROL Min Time Between Password Reset Requests] | Vista de tienda | Determina el número mínimo de minutos entre solicitudes de restablecimiento de contraseña. |
| [!UICONTROL Add Secret Key to URLs] | Global | Cuando está activada, añade una clave secreta a la URL del administrador como medida de precaución frente a posibles ataques. Opciones: `Yes` / `No` |
| [!UICONTROL Login Is Case Sensitive] | Global | Determina si las credenciales de inicio de sesión introducidas por un usuario deben coincidir con las mayúsculas y minúsculas de las almacenadas. Opciones: `Yes` / `No` |
| [!UICONTROL Admin Session Lifetime (seconds)] | Global | Determina la duración de una sesión de administrador en segundos. |
| [!UICONTROL Maximum Login Failures to Lockout Account] | Global | Determina la cantidad de veces que los usuarios administradores pueden intentar iniciar sesión antes de que se bloqueen sus cuentas. Si el campo está vacío, no se establece ningún mínimo. Valor predeterminado: `6` |
| [!UICONTROL Lockout Time (minutes)] | Global | Determina la cantidad de minutos que una cuenta de administrador está bloqueada antes de que el usuario pueda intentar iniciar sesión de nuevo. Valor predeterminado: `30` |
| [!UICONTROL Password Lifetime (days)] | Global | Determina el número de días antes de que caduque una contraseña de administrador. Si el campo está vacío, no se establece ningún período de duración. Valor predeterminado: `90` |
| [!UICONTROL Password Change] | Global | Determina si los usuarios administradores deben cambiar sus contraseñas. Opciones: <br/>**`Forced`**- Requiere que los usuarios administradores cambien sus contraseñas después de configurar la cuenta.<br/>**`Recommended`** - Recomienda que los usuarios administradores cambien sus contraseñas después de configurar la cuenta. |

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![Tablero](./assets/admin-dashboard.png)<!-- zoom -->

Para obtener más información sobre cómo configurar estas opciones, consulte [Panel de administración](../../getting-started/admin-dashboard.md) en la _Guía de introducción_.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|----------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Charts] | Global | Determina si el tablero incluye un gráfico generado a partir de los datos de ventas actuales. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Grids]

![Cuadrículas de administración](./assets/admin-admin-grids.png)<!-- zoom -->

Para obtener más información sobre cómo configurar estas opciones, consulte [Limitar la visualización del producto](../../catalog/products-list.md#limit-product-display) en la _Guía de administración de catálogos_.

>[!NOTE]
>
>Para mejorar el rendimiento de los catálogos grandes, se recomienda limitar el número de productos que se muestran en la cuadrícula.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|-----------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Limit Number of Products in Grid] | Global | Determina si el número de productos mostrados en la cuadrícula está limitado al valor _[!UICONTROL Records Limit]_. Opciones: `Yes` / `No` |
| [!UICONTROL Records Limit] | Global | Establece el límite de número de productos en la cuadrícula de productos. El valor mínimo predeterminado es `20000`. |

## [!UICONTROL CAPTCHA]

![CAPTCHA](./assets/admin-captcha.png)<!-- zoom -->

Para obtener más información sobre cómo configurar estas opciones, consulte [CAPTCHA](../../systems/security-captcha.md) en la _Guía de sistemas de administración_.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|-------------------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable CAPTCHA in Admin] | Global | Habilita CAPTCHA para el inicio de sesión del administrador. Opciones: `Yes` / `No` |
| [!UICONTROL Font] | Global | Determina la fuente utilizada para mostrar el CAPTCHA. Para agregar su propia fuente, coloque el archivo de fuente en el mismo directorio que la instancia de Commerce y agregue la declaración al archivo config.xml en `app/code/Magento/Captcha/etc` Fuente predeterminada: ` LinLibertine` |
| [!UICONTROL Forms] | Global | Determina los formularios donde se utiliza CAPTCHA. Opciones: `Admin Login` / `Admin Forgot Password` |
| [!UICONTROL Displaying Mode] | Global | Determina cuándo aparecerá el CAPTCHA. Opciones: <br/>**`Always`**- siempre se requiere CAPTCHA para iniciar sesión.<br/>**`After number of attempts to login`** - Muestra el campo [!UICONTROL Number of Unsuccessful Attempts to Login]. Introduzca el número de intentos de inicio de sesión permitidos. Un valor de 0 (cero) es similar a establecer el Modo de visualización en Siempre. Esta opción no cubre los formularios Olvidé la contraseña y Crear usuario. Si CAPTCHA está habilitado y configurado para aparecer, siempre se incluye en el formulario.<br />**Nota**: Para hacer un seguimiento del número de intentos de inicio de sesión erróneos, se cuenta cada intento de inicio de sesión en una dirección de correo electrónico y desde una dirección IP. El número máximo de intentos de inicio de sesión permitidos desde la misma dirección IP es de 1000. Esta limitación se aplica solamente cuando CAPTCHA está habilitado. |
| [!UICONTROL Number of Unsuccessful Attempts to Login] | Global | Determina la cantidad de veces que una persona puede intentar iniciar sesión antes de que se bloquee la cuenta. Para realizar un seguimiento del número de intentos de inicio de sesión erróneos, el sistema realiza un seguimiento de los intentos desde una dirección de correo electrónico desde una sola dirección IP. El número máximo de intentos permitidos desde la misma dirección IP es de 1000. Esta limitación se aplica solo si CAPTCHA está habilitado. |
| [!UICONTROL CAPTCHA Timeout (minutes)] | Global | Determina la duración del CAPTCHA actual. Cuando caduca el CAPTCHA, el usuario debe volver a cargar la página. |
| [!UICONTROL Number of Symbols] | Global | Determina el número de símbolos que se utilizan en el CAPTCHA. El valor máximo permitido es `8`. También puede especificar un rango, por ejemplo, `5-8`. |
| [!UICONTROL Symbols Used in CAPTCHA] | Global | Determina qué símbolos se utilizarán en el CAPTCHA. Solo se permiten letras (a-z y A-Z) y números (0-9). El conjunto predeterminado de símbolos sugeridos en el campo excluye los símbolos de aspecto similar como i, l o 1. La visualización de estos símbolos en CAPTCHA reduce las posibilidades de que un usuario reconozca el CAPTCHA correctamente. |
| [!UICONTROL Case Sensitive] | Global | Determina si los caracteres utilizados en el CAPTCHA distinguen entre mayúsculas y minúsculas. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Actions Logging]

{{ee-feature}}

![Registro de acciones de administración](./assets/admin-actions-logging.png)<!-- zoom -->

Para obtener más información sobre cómo configurar estas opciones, consulte [Archivo de registro de acciones](../../systems/action-log-archive.md) en la _Guía de sistemas de administración_.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|-----------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Actions] | Global | Activa el registro de acciones para cada una de las acciones seleccionadas: <br/>`Admin My Account` <br/>`Admin Permission Roles` <br/>`Admin Permission Users` <br/>`Admin Sign In` <br/>`CMS Blocks` <br/>`CMS Hierarchy` <br/>`CMS Pages` <br/>`Cache Management` <br/>`Cart Price Rules` <br/>`Catalog Attributes` <br/>`Catalog Categories` <br/>`Catalog Events` <br/>`Catalog Price Rules` <br/>`Catalog Product Tax Classes` <br/>`Catalog Product Templates` <br/>`Catalog Products` <br/>`Catalog Ratings` <br/>`Catalog Reviews` <br/>`Catalog Search` <br/>`Checkout Terms and Conditions` <br/>`Companies` <br/>`Company Credit` <br/>`Custom Variables` <br/>`Customer Groups` <br/>`Customer Invitations` <br/>`Customer Tax Classes` <br/>`Customers` <br/>`Design Configuration` <br/>`Gift Card Accounts` <br/>`Gift Registry Entity` <br/>`Gift Registry Type` <br/>`Index Management` <br/>`Login as a Customer` <br/>`Manage Currency Rates` <br/>`Manage Customer Address Attributes` <br/>`Manage Customer Attributes` <br/>`Manage Design` <br/>`Manage Dynamic Blocks` <br/>`Manage Segments` <br/>`Manage Store Views` <br/>`Manage Stores` <br/>`Manage Websites` <br/>`Negotiable Quotes` <br/>`Newsletter Queue` <br/>`Newsletter Subscribers` <br/>`Newsletter Templates` <br/>`PayPal Settlement Reports` <br/>`Reports` <br/> `Reward Points Rates` <br/>`Rule-Based Product Relations` <br/>`Sales Archive` <br/>`Sales Credit Memos` <br/>`Sales Invoices` <br/>`Sales Order Status` <br/>`Sales Orders` <br/>`Sales Shipments` <br/>`Shared Catalog` <br/>`Shopping Cart Management` <br/>`Store Credit` <br/>`System Backups` <br/>`System Configuration` <br/>`Tax Rates` <br/>`Tax Rules` <br/>`Transactional Emails` <br/>`URL Rewrites` <br/>`Widget` <br/>`XML Sitemap` |

{style="table-layout:auto"}

## [!UICONTROL Admin Usage]

![Uso de administrador](./assets/admin-usage.png)<!-- zoom -->

Para obtener más información sobre cómo configurar estas opciones, consulte [Recopilación de datos de uso](../../getting-started/admin.md#usage-data-collection) en la _Guía de introducción_.

| Campo | Ámbito | Descripción |
|------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Admin Usage Tracking] | Global | Concede permiso a Adobe para recopilar datos de uso del administrador con el fin de mejorar la experiencia de uso de _Admin_, y de productos y servicios relacionados. Al permitir la recopilación de datos, también se habilita la _Guía interna del producto_, que está diseñada para ofrecer contenido interactivo como ayuda, información sobre herramientas, guías de introducción, información de incorporación, anuncios de características y más al _administrador_. Los administradores individuales no se identifican en los datos de uso. Opciones:<br />**`Yes`**- Permite la recopilación de datos y habilita la _Guía interna del producto_.<br />**`No`** - No permite la recopilación de datos ni habilita la _Guía interna del producto_. |

{style="table-layout:auto"}
