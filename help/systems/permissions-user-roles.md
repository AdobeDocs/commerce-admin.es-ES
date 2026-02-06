---
title: Funciones de usuario
description: Obtenga información sobre cómo crear funciones de usuario y los permisos asociados para administrar el acceso a las funciones de administración.
exl-id: a70f74d4-72b4-4639-a67d-9fc13df65924
feature: Admin Workspace, Roles/Permissions, Security
source-git-commit: dff29b7c3a95d4a0ae5ce16819c41a4560b477c4
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# Funciones de usuario

Para conceder a alguien acceso restringido al administrador, el primer paso es crear una función que tenga el nivel adecuado de permisos. Una vez guardada la función, puede agregar nuevos usuarios y asignar la función restringida para concederles acceso limitado al administrador.

![Administrador - funciones de usuario](./assets/permissions-role-grid.png){width="600" zoomable="yes"}

## Definir una función

1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add New Role]**.

1. Complete los pasos para definir la función:

### Paso 1: Añadir el nombre de la función

1. En _[!UICONTROL Role Information]_, escriba un **[!UICONTROL Role Name]**&#x200B;descriptivo.

1. En _[!UICONTROL Current User Identity Verification]_, escriba su contraseña.

   ![Permisos del sistema - información de función](./assets/permissions-role-info.png){width="600" zoomable="yes"}

### Paso 2: Asignación de recursos

>[!IMPORTANT]
>
>Al asignar recursos, asegúrese de deshabilitar el acceso a la herramienta Permisos si está limitando el acceso a una función determinada. De lo contrario, los usuarios pueden modificar sus propios permisos.

1. Establezca **[!UICONTROL Role Scopes]** en una de las siguientes opciones:

   - `All`
   - `Custom`

   Si se establece en `Custom` para una instalación de varios sitios, active la casilla de verificación del sitio web y el almacén donde se va a utilizar el rol.

   ![Recursos de función de usuario - ámbito personalizado](./assets/permissions-role-scope-custom.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Los usuarios con un ámbito de rol `Custom` no pueden crear sitios web y categorías, asignar productos a categorías o editar productos en el ámbito _[!UICONTROL All Store Views]_&#x200B;cuando se les asigna a tiendas restringidas. Estos usuarios no pueden realizar otras_ acciones globales _que afecten a ámbitos en los que no tengan acceso.

1. En _[!UICONTROL Roles Resources]_, establezca **[!UICONTROL Resource Access]**&#x200B;en `Custom`.

   >[!NOTE]
   >
   >Si se requiere Autenticación de doble factor (2FA) para iniciar sesión en el administrador, asegúrese de habilitar el recurso `Permissions` > `Two Factor Auth` para este rol. De lo contrario, los usuarios recién creados con este ámbito de función `Custom` no podrán configurar 2FA cuando accedan al administrador por primera vez.

1. En la estructura de árbol **[!UICONTROL Resource]**, seleccione la casilla de verificación de cada capacidad de administración a la que el rol puede acceder.

   Para crear un rol de administrador con acceso a la configuración de impuestos, seleccione los recursos de ventas/impuestos y de sistema/impuestos. Si configura un sitio web para una región que difiere de su [punto de origen de envío](../stores-purchase/shipping-settings.md#point-of-origin) predeterminado, debe permitir el acceso a los recursos de sistema/envío para el rol. La configuración de envío determina la tasa de impuestos de la tienda que se utiliza para los precios del catálogo.

   ![Recursos de funciones de usuario asignados](./assets/permissions-role-resources-product.png){width="600" zoomable="yes"}

   La lista de permisos disponibles puede incluir opciones adicionales para extensiones agrupadas e instaladas. Al seleccionar el permiso más alto para cada función, se asignan todos los permisos disponibles para el usuario.

   >[!NOTE]
   >
   >Un usuario administrador debe tener permisos de **[!UICONTROL Sales / Archive]** para el ámbito de su rol con el fin de ver las _[!UICONTROL Invoices]_,_[!UICONTROL Credit Memos]_ y _[!UICONTROL Shipments]_, así como [fichas](../stores-purchase/order-processing.md).

1. Una vez finalizado, haga clic en **[!UICONTROL Save Role]**.

   La función aparece ahora en la cuadrícula y se puede asignar a cuentas de usuario.

## Asignar una función a los usuarios

1. En la cuadrícula _[!UICONTROL Roles]_, abra el registro en modo de edición.

1. En _[!UICONTROL Current User Identity Verification]_, escriba la contraseña de su cuenta de usuario.

1. En el panel izquierdo, elija **[!UICONTROL Role Users]**.

   La opción _[!UICONTROL Role Users]_&#x200B;solo aparece después de guardar un nuevo rol.

   ![Cuentas de usuario asignadas al rol](./assets/permissions-role-users.png){width="600" zoomable="yes"}

1. Para buscar un registro de usuario específico, haga lo siguiente:

   - Escriba el valor en el filtro de búsqueda en la parte superior de una columna y presione **Entrar**.

   - Cuando esté listo para volver a la lista completa, haga clic en **[!UICONTROL Reset Filter]**.

1. Seleccione la casilla de verificación de los usuarios que se van a asignar al rol.

1. Haga clic en **[!UICONTROL Save Role]**.

## Editar una función

1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. Localice la función con filtros encima de la cuadrícula y haga clic en el nombre de la función.

1. Realice los cambios necesarios.

   Revise los pasos para crear una función de usuario para obtener información acerca de la configuración de la función.

1. Cuando se le pida, introduzca su contraseña para confirmar su identidad.

1. Haga clic en **[!UICONTROL Save Role]**.

## Eliminar un rol

1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. Localice la función con filtros sobre la cuadrícula y ábrala en modo de edición.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Delete Role]**.

1. Para confirmar la acción, haga clic en **[!UICONTROL OK]**.

## Demostración de funciones de usuario

Vea este vídeo para obtener más información sobre la administración de funciones de usuario:

>[!VIDEO](https://video.tv.adobe.com/v/3443510?captions=spa&quality=12&learn=on)

## Recursos de roles

Se puede asignar acceso a los siguientes recursos a una función personalizada. Consulte la página vinculada para obtener más información sobre las funciones asociadas a cada recurso.

![Adobe Commerce](../assets/adobe-logo.svg) - Solo Adobe Commerce

![Adobe Commerce B2B](../assets/b2b.svg) - Disponible solo con Adobe Commerce B2B

| Recurso |   |   |
| --- | --- | --- |
| [`Dashboard`](../getting-started/admin-dashboard.md) |  |  |
| [`Sales`](../stores-purchase/sales-menu.md) | [`Operations`](../stores-purchase/orders.md) |  |
|  | [`Quotes`](../b2b/quotes.md) ![Adobe Commerce B2B](../assets/b2b.svg) <br/>[`Orders`](../stores-purchase/orders.md)<br/>[`Invoices`](../stores-purchase/invoices.md)<br/>[`Shipments`](../stores-purchase/shipments.md)<br/>[`Credit Memos`](../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../stores-purchase/returns.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Transactions`](../stores-purchase/transactions.md) |
|  | [`Archive`](action-log-archive.md)![Adobe Commerce] |  |
|  | [`Shopping Cart Management`](../stores-purchase/cart.md) |  |
| [`Catalog`](../catalog/catalog-menu.md) | [`Category Permissions`](../catalog/categories.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Inventory`](../inventory-management/introduction.md) | [`Products`](../catalog/products-list.md)<br/>[`Categories`](../catalog/categories.md) |
|  | [`Shared Catalog`](../b2b/catalog-shared-create.md) ![Adobe Commerce B2B](../assets/b2b.svg) | [`Manage Shared Catalog`](../b2b/catalog-shared-manage.md) |
| [`Customers`](../customers/guide-overview.md) | [`All Customers`](../customers/customers-all.md)<br/>[`Now Online`](../customers/now-online.md)<br/>[`Customer Groups`](../customers/customer-groups.md)<br/>[`Segments`](../customers/customer-segments.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Login as Customer`](../customers/login-as-customer.md) | `Allow Login as Customer Button`<br/>`View Login as Customer Log` ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Companies`](../b2b/account-companies.md) ![Adobe Commerce B2B](../assets/b2b.svg) | [`Manage Companies`](../b2b/account-company-manage.md) <br/>`Add New Company` <br/>`Delete Company` <br/>`Reimburse Balance` |
| [`Carts`](../stores-purchase/shopping-assisted-cart-manage.md) | [`Manage carts`](../stores-purchase/shopping-assisted-cart-manage.md) |  |
| [`My Account`](../customers/account-dashboard-my-account.md) |  |  |
| [`Marketing`](../merchandising-promotions/marketing-menu.md) | [`Promotions`](../merchandising-promotions/marketing-menu.md#uicontrol-promotions) | [`Catalog Price Rule`](../merchandising-promotions/price-rules-catalog.md) <br/>[`Cart Price Rules`](../merchandising-promotions/price-rules-cart.md) <br/>[`Related Products Rules`](../merchandising-promotions/product-related-rules.md)![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Gift Card Accounts`](../stores-purchase/product-gift-card-accounts.md) ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Private Sales`](../merchandising-promotions/events-private-sales.md) ![Adobe Commerce](../assets/adobe-logo.svg) | [`Events`](../merchandising-promotions/event-create.md) <br/>[`Invitations`](../merchandising-promotions/invitations.md) |
|  | `Communications` | [`Email Templates`](email-templates.md) <br/>[`Newsletter Template`](../merchandising-promotions/newsletter-template.md) <br/>[`Newsletter Queue`](../merchandising-promotions/newsletter-queue.md) <br/>[`Newsletter Subscribers`](../merchandising-promotions/newsletter-subscribers.md) <br/>[`Email Reminders`](../merchandising-promotions/email-reminder-rules.md) |
|  | `Sales Channel` | [`Amazon Sales Channel`](https://experienceleague.adobe.com/docs/commerce-channels/amazon/overview.html?lang=es) |
|  | [`SEO & Search`](../merchandising-promotions/marketing-menu.md#uicontrol-seo--search) | [`Search Terms`](../catalog/search-terms.md) <br/>[`Search Synonyms`](../catalog/search-terms.md#search-synonyms) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`URL Rewrites`](../merchandising-promotions/url-rewrite-custom.md) <br/>[`Site Map`](../merchandising-promotions/sitemap-xml.md) |
|  | [`User Content`](../merchandising-promotions/product-reviews-moderate.md) | [`All Reviews`](../merchandising-promotions/product-reviews.md) <br/>[`Pending Reviews`](../merchandising-promotions/product-reviews-moderate.md) <br/> |  |
| [`Content`](../content-design/content-menu.md) | [`Elements`](../content-design/content-menu.md#uicontrol-elements)) | [`Pages`](../content-design/pages.md)<br/>[`Hierarchy`](../content-design/page-hierarchy.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Blocks`](../content-design/blocks.md)<br/>[`Dynamic Blocks`](../content-design/dynamic-blocks.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Widgets`](../content-design/widgets.md)<br/>[`Media Gallery`](../content-design/media-gallery.md) |  |
|  | [`Design`](../content-design/introduction.md#design) | [`Themes`](../content-design/themes.md)<br/>[`Schedule`](../content-design/schedule.md) |  |
|  | [Ensayo de contenido](../content-design/content-staging.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br /> |  |
| [`Reports`](../getting-started/reports-menu.md) | [`Marketing`](../getting-started/marketing-reports.md) | `Shopping Cart`<br />[`Search Terms`](../catalog/search-terms.md#search-terms-report)<br />`Newsletter Problem Reports` |  |
|  | [`Reviews`](../getting-started/review-reports.md)<br /> |  |
|  | [`Sales`](../getting-started/sales-reports.md) |  |
|  | `System Insights` ![Adobe Commerce](../assets/adobe-logo.svg) | [`Site-Wide Analysis Tool`](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html?lang=es) |
|  | [`Customers`](../getting-started/customer-reports.md)<br/>[`Products`](../getting-started/product-reports.md)<br/>[`Private Sales`](../getting-started/private-sales-reports.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br />[`Statistics`](../getting-started/reports-menu.md#uicontrol-statistics)<br />[`Business Intelligence`](../getting-started/business-intelligence.md) |  |
| [`Stores`](../stores-purchase/stores.md) | [`Settings`](../stores-purchase/stores-menu.md) | [`All Stores`](../stores-purchase/stores.md)<br/>[`Configuration`](../configuration-reference/guide-overview.md)<br/>[`Terms and Conditions`](../stores-purchase/terms-and-conditions.md)<br/>[`Order Status`](../stores-purchase/order-status.md) |  |
|  | [`Inventory`](../inventory-management/sources-stocks.md) | [`Sources`](../inventory-management/sources-manage.md)<br/>[`Stocks`](../inventory-management/stocks-manage.md) |  |
|  | [`Taxes`](../stores-purchase/taxes.md) |  |  |
|  | [`Currency`](../stores-purchase/currency.md) | [`Currency Rates`](../stores-purchase/currency-update.md)<br/>[`Currency Symbols`](../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) |  |
|  | [`Attributes`](../catalog/product-attributes.md) | [`Product`](../catalog/attribute-product-create.md)<br/>[`Update Attributes`](../catalog/attribute-product-create.md)<br/>[`Attribute Set`](../catalog/attribute-sets.md)<br/>[`Ratings`](../merchandising-promotions/product-reviews.md#create-custom-ratings) |
|  | [`Other Settings`](../stores-purchase/stores-menu.md) | [`Customer Groups`](../customers/customer-groups.md) |
| [`System`](system-menu.md) | [`Data Transfer`](data-transfer.md) | [`Import`](data-import.md)<br/>[`Export`](data-export.md)<br/>[`Import/Export Tax Rates`](data-transfer-tax-rates.md)<br/>[`Import History`](data-import.md#import-history) |  |
|  | [`Magento Connect`](../getting-started/commerce-marketplace.md) | `Connect Manager`<br/>`Package Extensions` |  |
|  | [`Tools`](system-menu.md#tools) | [`Cache Management`](cache-management.md)<br/>[`Backups`](backups.md)<br/>[`Index Management`](index-management.md)<br/>[`Change Indexer Mode`](index-management.md) |  |
|  | [`Permissions`](permissions.md) | [`All Users`](permissions-users-all.md)<br/>[`Locked Users`](permissions-users-all.md#locked-users)<br/>[`User Roles`](permissions-user-roles.md) |
| [`Action Log`](action-log.md)![Adobe Commerce](../assets/adobe-logo.svg) | [`Report`](action-log.md)<br/>[`Archive`](action-log-archive.md) |
|  | [`Other Settings`](system-menu.md) | [`Notifications`](notifications.md)<br/>[`Custom Variables`](variables-custom.md)<br/>[`Manage Encryption Key`](encryption-key.md) |  |
| [`Global Search`](../getting-started/admin-workspace.md#workspace-search) |  |  |

{style="table-layout:auto"}
