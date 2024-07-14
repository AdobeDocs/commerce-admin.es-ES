---
title: Guía de referencia de configuración
description: Revise la información descriptiva de todas las opciones de configuración del almacén de administración de Commerce organizadas por las pestañas de configuración, páginas y secciones.
exl-id: b0359ba4-3643-4355-9154-adfedb369ec3
source-git-commit: 323ea635286fcb9a2bcc7f4f56b32c1518a7beef
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Guía de referencia de configuración

Esta guía está destinada a comerciantes y administradores de sistemas que trabajan en Adobe Commerce o Magento Open Source. Proporciona información de referencia para todas las opciones de configuración de tienda a las que se accede desde la barra lateral _Admin_ en **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

No cubre detalles sobre las capacidades de Adobe Commerce y Magento Open Source ni procedimientos para la configuración de la tienda.

Esta guía se organiza según la configuración de navegación izquierda:

| Pestaña Configuración | Fichas secundarias |
| ----------------- | ---------- |
| **[!UICONTROL General]** <br/><br/>Las secciones de configuración de _[!UICONTROL General]_determinan los parámetros de almacén, las direcciones URL, el tema, la moneda, las direcciones de correo electrónico, los contactos de almacén, el editor y el informe de tablero. | - [[!UICONTROL General]](./general/general.md)<br>- [[!UICONTROL B2B Features]](./general/b2b-features.md)<br>- [[!UICONTROL Web]](./general/web.md)<br>- [[!UICONTROL Currency Setup]](./general/currency-setup.md)<br>- [[!UICONTROL Store Email Addresses]](./general/store-email-addresses.md)<br>- [[!UICONTROL Contacts]](./general/contacts.md)<br>- [[!UICONTROL Reports]](./general/reports.md)<br>- [[!UICONTROL Content Management]](./general/content-management.md)<br>- [[!UICONTROL New Relic Reporting]](./general/new-relic-reporting.md)<br>- [[!UICONTROL Advanced Reporting]](./general/advanced-reporting.md) |
| **[!UICONTROL Catalog]** <br/><br/>Las opciones de configuración de _[!UICONTROL Catalog]_determinan la configuración del producto y del inventario, controlan el mapa del sitio y la generación de fuentes RSS, y especifican la plantilla de correo electrónico que se usa para compartir productos con amigos. | - [[!UICONTROL Catalog]](./catalog/catalog.md)<br>- [[!UICONTROL Visual Merchandiser]](./catalog/visual-merchandiser.md)<br>- [[!UICONTROL Inventory]](./catalog/inventory.md)<br>- [[!UICONTROL XML Sitemap]](./catalog/xml-sitemap.md)<br>- [[!UICONTROL RSS Feeds]](./catalog/rss-feeds.md)<br>- [[!UICONTROL Email to a Friend]](./catalog/email-to-a-friend.md) |
| **[!UICONTROL Security]** <br/><br/>Las opciones de configuración de _[!UICONTROL Security]_controlan la seguridad del almacén, la autenticación de doble factor y la característica reCAPTCHA de Google. | - [[!UICONTROL 2FA]](./security/2fa.md)<br>- [[!UICONTROL Google reCAPTCHA Admin Panel]](./security/google-recaptcha-admin.md)<br>- [[!UICONTROL Google reCAPTCHA Storefront]](./security/google-recaptcha-storefront.md)<br>- [[!UICONTROL Security.txt]](./security/security-txt.md) |
| **[!UICONTROL Customers]** <br/><br/>Las opciones de configuración de _[!UICONTROL Customers]_establecen las opciones básicas de inicio de sesión y cuenta de cliente, la configuración de la newsletter, la lista de deseos y el formato de los códigos de cupones generados automáticamente. | - [[!UICONTROL Login as Customer]](./customers/login-as-customer.md)<br>- [[!UICONTROL Newsletter]](./customers/newsletter.md)<br>- [[!UICONTROL Company Configuration]](./customers/company-configuration.md)<br>- [[!UICONTROL Customer Configuration]](./customers/customer-configuration.md)<br>- [[!UICONTROL Requisition Lists]](./customers/requisition-lists.md)<br>- [[!UICONTROL Wish List]](./customers/wishlist.md)<br>- [[!UICONTROL Invitations]](./customers/invitations.md)<br>- [[!UICONTROL Reward Points]](./customers/reward-points.md)<br>- [[!UICONTROL Promotions]](./customers/promotions.md)<br>- [[!UICONTROL Gift Registry]](./customers/gift-registry.md)<br>- [[!UICONTROL Persistent Shopping Cart]](./customers/persistent-shopping-cart.md) |
| **[!UICONTROL Sales]** <br/><br/>Las opciones de configuración de _[!UICONTROL Sales]_determinan la configuración de pago y envío, las opciones de pago y envío, las impresiones de correo electrónico de ventas y PDF y la configuración de la API de Google. | - [[!UICONTROL Sales]](./sales/sales.md)<br>- [[!UICONTROL Sales Emails]](./sales/sales-emails.md)<br>- [[!UICONTROL Quotes]](./sales/quotes.md)<br>- [[!UICONTROL PDF Print-outs]](./sales/pdf-print-outs.md)<br>- [[!UICONTROL Tax]](./sales/tax.md)<br>- [[!UICONTROL Checkout]](./sales/checkout.md)<br>- [[!UICONTROL Shipping Settings]](./sales/shipping-settings.md)<br>- [[!UICONTROL Multishipping Settings]](./sales/multishipping-settings.md)<br>- [[!UICONTROL Delivery Methods]](./sales/delivery-methods.md)<br>- [[!UICONTROL Google API]](./sales/google-api.md)<br>- [[!UICONTROL 3D Secure]](./sales/3d-secure.md)<br>- [[!UICONTROL Gift Cards]](./sales/gift-cards.md)<br>- [[!UICONTROL Payment Methods]](./sales/payment-methods.md) |
| **[!UICONTROL Sales Channels]** <br/><br/>Cuando se instala la extensión [!DNL Amazon Sales Channel], la configuración de _[!UICONTROL Sales Channels]_controla las operaciones de integración automatizada con el almacén de Amazon. | - [[!UICONTROL Global Settings]](sales-channels.md) |
| **[!UICONTROL Services]** <br/><br/>Las opciones de configuración de _[!UICONTROL Services]_determinan las opciones de integración de la API de Commerce SOAP, incluidas las API de y OAuth, que se encuentran en la versión de. | - [[!UICONTROL Web API]](./services/magento-web-api.md)<br>- [[!UICONTROL Commerce Services]](./services/saas.md)<br>- [[!UICONTROL OAuth]](./services/oauth.md) |
| **[!UICONTROL Advanced]** <br/><br/>Las opciones de configuración de _[!UICONTROL Advanced]_determinan las opciones predeterminadas de administración, varias opciones de configuración del sistema, controles avanzados de módulo y herramientas para desarrolladores. | - [[!UICONTROL Admin]](./advanced/admin.md)<br>- [[!UICONTROL System]](./advanced/system.md)<br>- [[!UICONTROL Developer]](./advanced/developer.md) |

{style="table-layout:auto"}

No cubre detalles sobre las capacidades de Adobe Commerce y Magento Open Source ni procedimientos para la configuración de la tienda.

## Documentación disponible

{{docs-links}}
