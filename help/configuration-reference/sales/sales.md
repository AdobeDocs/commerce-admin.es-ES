---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Sales]'
description: Revise la configuración de en [!UICONTROL Sales] &gt; [!UICONTROL Sales] de la administración de Commerce.
exl-id: 29091aab-e608-4e68-a6fe-f2808c78581c
feature: Configuration, Orders
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '1168'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Sales]

{{config}}

## [!UICONTROL General]

![General](./assets/sales-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/marketing/sales-documents-ref-id.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Hide Customer IP] | Vista de tienda | Determina si la dirección IP del cliente aparece en pedidos, facturas, envíos y notas de abono. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Checkout Totals Sort Order]

![Orden de totales de cierre](./assets/sales-checkout-totals-sort-order.png)<!-- zoom -->

<!-- [Checkout Totals Sort Order](https://docs.magento.com/user-guide/sales/checkout-totals-sort-order.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Subtotal] | Sitio web | Número que determina cuándo se calcula el subtotal en relación con otros totales de pago y envío. Valor predeterminado: `10` |
| [!UICONTROL Discount] | Sitio web | Un número que determina cuándo se calcula el descuento en relación con otros totales de pago y envío. Valor predeterminado: `20` |
| [!UICONTROL Shipping] | Sitio web | Un número que determina cuándo se calcula el envío en relación con otros totales de pago y envío. Valor predeterminado: `30` |
| [!UICONTROL Tax] | Sitio web | Número que determina cuándo se calculan los impuestos en relación con otros totales de pago y envío. Valor predeterminado: `40` |
| [!UICONTROL Fixed Product Tax] | Sitio web | Número que determina cuándo se calcula el impuesto sobre productos fijos en relación con otros totales de cierre de compra. Valor predeterminado: `50` |
| [!UICONTROL Grand Total] | Sitio web | Número que determina cuándo se calcula el total general en relación con otros totales de cierre de compra. Valor predeterminado: `100` |

{style="table-layout:auto"}

## [!UICONTROL Reorder]

![Reordenar](./assets/sales-reorder.png)<!-- zoom -->

<!-- [Reorder](https://docs.magento.com/user-guide/sales/reorders-allow.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Allow Reorder] | Vista de tienda | Determina si los clientes pueden reordenar desde sus cuentas. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Allow Zero Grand Total]

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Allow Zero Grand Total for Credit Memo] | Vista de tienda | Determina la posibilidad de crear una nota de abono con un total general cero. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Invoice and Packing Slip Design]

![Diseño de facturas y albaranes](./assets/sales-invoice-packing-slip-design.png)<!-- zoom -->

<!-- [Invoice and Packing Slip Design](https://docs.magento.com/user-guide/marketing/sales-document-pdf-logo.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Logo for PDF Print-outs] | Vista de tienda | Identifica el archivo de logotipo que aparece en la cabecera de facturas de PDF y albaranes. Tipos de archivo permitidos: <br/>JPG/JPEG <br/>TIF/TIFF <br/>PNG |
| [!UICONTROL Logo for HTML Print View] | Vista de tienda | Identifica el archivo de logotipo que aparece en la cabecera de la vista de impresión de HTML de facturas y albaranes. Tipos de archivo permitidos: <br/>JPG /JPEG <br/>GIF <br/>PNG |
| [!UICONTROL Address] | Vista de tienda | La dirección del almacén tal como desea que aparezca en facturas y albaranes. |

{style="table-layout:auto"}

## [!UICONTROL Minimum Order Amount]

![Cantidad mínima del pedido](./assets/sales-minimum-order-amount.png)<!-- zoom -->

<!-- [Minimum Order Amount](https://docs.magento.com/user-guide/sales/cart-minimum-order-amount.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable] | Sitio web | Determina si se ha establecido una cantidad mínima de pedido para la ubicación. Opciones: `Yes` / `No` |
| [!UICONTROL Minimum Amount] | Sitio web | Especifica el subtotal mínimo, el pedido después de aplicar los descuentos. |
| [!UICONTROL Include Discount Amount] | Sitio web | Determina si el importe mínimo del pedido incluye descuentos aplicados. Opciones: `Yes` / `No` |
| [!UICONTROL Include Tax to Amount] | Sitio web | Determina si el importe mínimo del pedido incluye impuestos. Opciones: `Yes` / `No` |
| [!UICONTROL Description Message] | Vista de tienda | Determina el mensaje que aparece en la parte superior del carro de compras cuando el total del carro es menor que la cantidad mínima del pedido. Si se deja en blanco, aparecerá el siguiente mensaje predeterminado: `Minimum order amount is $[minimum_amount]` |
| [!UICONTROL Error to Show in Shopping Cart] | Vista de tienda | Determina el mensaje que aparece en el minicarro o en el vínculo de cierre de compra cuando la cantidad del pedido es inferior a la cantidad mínima requerida. Si se deja en blanco, aparece un mensaje predeterminado. |
| [!UICONTROL Validate Each Address Separately in Multi-address Checkout] | Sitio web | Para pedidos de varios artículos, determina si los artículos de pedido que van a direcciones independientes cumplen con la cantidad mínima de pedido. Opciones: `Yes` / `No` |
| [!UICONTROL Multi-address Description Message] | Vista de tienda | Para pedidos de varias direcciones, determina el mensaje que aparece en el carro de compras si los artículos enviados a una dirección son inferiores a la cantidad mínima de pedido. |
| [!UICONTROL Multi-address Error to Show in Shopping Cart] | Vista de tienda | Para pedidos de varias direcciones, determina el mensaje que aparece en el minicarro o en el vínculo de cierre de compra cuando la cantidad del pedido es inferior a la cantidad mínima requerida. Si se deja en blanco, aparece un mensaje predeterminado. |

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![Tablero](./assets/sales-dashboard.png)<!-- zoom -->

<!-- [Dashboard](https://docs.magento.com/user-guide/stores/admin-dashboard.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Use Aggregated Data] | Global | Determina si se utilizan datos de ventas agregados en tiempo real para generar informes de instantáneas de tablero. Si tiene que procesar una gran cantidad de datos, se puede mejorar el rendimiento desactivando la visualización de datos en tiempo real. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Orders Cron Settings]

![Configuración de pedidos de Cron](./assets/sales-orders-cron-settings.png)<!-- zoom -->

<!-- [Orders Cron Settings](https://docs.magento.com/user-guide/system/cron.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Pending Payment Order Lifetime] | Sitio web | Determina la duración de los pedidos pendientes en minutos. Configuración predeterminada: `480` minutos (8 horas) |

{style="table-layout:auto"}

## [!UICONTROL Gift Options]

![Opciones de regalo](./assets/sales-gift-options.png)<!-- zoom -->

<!-- [Gift Options](https://docs.magento.com/user-guide/sales/gift-options.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Allow Gift Messages on Order Level] | Sitio web | Especifique si se puede añadir un mensaje de regalo para todo el pedido. |
| [!UICONTROL Allow Gift Messages on Order Items] | Sitio web | Especifique si se puede añadir un mensaje de regalo para un artículo de pedido individual. |
| [!UICONTROL Allow Gift Wrapping on Order Level] | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Solo Adobe Commerce) Especifique si se puede añadir un envoltorio para regalos para todo el pedido. |
| [!UICONTROL Allow Gift Wrapping for Order Items] | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Solo Adobe Commerce) Especifique si se puede añadir un envoltorio para regalos para el artículo de pedido individual. |
| [!UICONTROL Allow Gift Receipt] | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Solo Adobe Commerce) Especifique si se puede añadir un recibo de regalo para el pedido. |
| [!UICONTROL Allow Printed Card] | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Solo Adobe Commerce) Especifique si se puede añadir una tarjeta impresa para el pedido. |
| [!UICONTROL Default Price for Printed Card] | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Solo Adobe Commerce) Especifique el precio predeterminado para la tarjeta impresa. |

{style="table-layout:auto"}

## [!UICONTROL Minimum Advertised Price]

![Precio Mínimo Anunciado](./assets/sales-minimum-advertised-price.png)<!-- zoom -->

<!-- [Minimum Advertised Price](https://docs.magento.com/user-guide/catalog/product-price-minimum-advertised.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable MAP] | Sitio web | Activa el precio mínimo anunciado para su tienda. Opciones: `Yes` / `No` |
| [!UICONTROL Display Actual Price] | Sitio web | Determina si el cliente puede ver el precio real de un producto. Opciones: <br/>**`In Cart`**- Muestra el precio real del producto en el carro de compras.<br/>**`Before Order Confirmation`** : Muestra el precio real del producto al final del proceso de cierre de compra, justo antes de que se confirme el pedido. <br/>**`On Gesture`**- Muestra el precio real del producto en una ventana emergente cuando el cliente hace clic en &quot;Click for price&quot; o &quot;What&#39;s this?&quot; vínculo. |
| [!UICONTROL Default Popup Text Message] | Vista de tienda | El mensaje de texto que aparece cuando el cliente selecciona el vínculo &quot;Clic por precio&quot; de una lista de categorías o una página de vista de productos. |
| [!UICONTROL Default "What's This" Text Message] | Vista de tienda | El mensaje de texto que aparece cuando el cliente hace clic en &quot;¿Qué es esto?&quot; desde la página de vista del producto. |
| [!UICONTROL Manufacturer's Suggested Retail Price] | Global | El precio al por menor sugerido por el fabricante (MSRP). |

{style="table-layout:auto"}

## [!UICONTROL Multicoupon Settings]

{{ee-feature}}

![Configuración de multicupón](./assets/sales-multicoupon-settings.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Maximum number of coupons per order] | Sitio web | Determina el número máximo de cupones permitidos por pedido |

{style="table-layout:auto"}

## [!UICONTROL Order by SKU Settings]

{{ee-feature}}

![Ordenar por configuración de SKU](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

<!-- [Order by SKU Settings](https://docs.magento.com/user-guide/customers/account-dashboard-order-by-sku.html) -->

![Configuración de pedido por SKU para el grupo de clientes](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable Order by SKU on My Account in Storefront] | Sitio web | Determina si Ordenar por SKU está disponible en el panel de cuentas del cliente. Opciones: <br/>**`Yes, for Everyone`**: la pestaña Ordenar por SKU aparece en el panel de cuentas de todos los clientes.<br/>**`Yes, for Specified Customer Groups`** : la pestaña Ordenar por SKU aparece en el panel de cuentas para los miembros de grupos especificados o de un catálogo compartido. <br/>**`No`**- La pestaña Ordenar por SKU no está disponible en la cuenta del cliente. |
| [!UICONTROL Customer Groups] | Sitio web | Determina los grupos de clientes. Opciones: `General` / `Retailer` / `Wholesale` |

{style="table-layout:auto"}

## [!UICONTROL Instant Purchase]

![Compra instantánea](./assets/sales-instant-purchase.png)<!-- zoom -->

<!-- [Instant Purchase](https://docs.magento.com/user-guide/sales/checkout-instant-purchase.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enabled] | Vista de tienda | Activa la compra instantánea para la vista de tienda si el método de pago, como Braintree, tiene activado el Vault. Opciones: `Yes` / `No` |
| [!UICONTROL Button Text] | Vista de tienda | Especifica el texto que aparece en el botón Compra instantánea. El texto predeterminado es `Instant Purchase`. |

{style="table-layout:auto"}

## [!UICONTROL Rate Limiting]

![Limitación de velocidad](assets/sales-rate-limiting.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--------------------------------------------------------|--- |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable rate limiting for placing orders] | Vista de tienda | Determina si se utiliza la limitación de velocidad para realizar pedidos desde la vista de tienda (el valor predeterminado es `No`). Opciones: `Yes` / `No`. |
| [!UICONTROL Requests limit per authenticated customer] | Vista de tienda | El número de solicitudes de compra que un cliente autenticado puede realizar durante el periodo. El límite predeterminado es `10`. |
| [!UICONTROL Requests limit per guest] | Vista de tienda | Número de solicitudes de compra que un cliente no autenticado puede realizar durante el período especificado. El valor predeterminado es `50`. |
| [!UICONTROL Counter resets in a ...] | Vista de tienda | Período de tiempo durante el cual un cliente autenticado/no autenticado puede realizar un determinado número de solicitudes de compra (el valor predeterminado es `Minute`). Opciones: `Minute` / `Hour` /`Day` |

{style="table-layout:auto"}

## [!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]

{{ee-feature}}

![Pedidos, Facturas, Envíos, Archivado de Notas de Abono](./assets/sales-orders-invoices-shipments-credit-memos-archiving.png)<!-- zoom -->

Para obtener más información sobre cómo cambiar esta configuración, consulte [Configuración del archivo de pedidos](../../stores-purchase/order-archive.md#configure-the-order-archive) en el _Guía de experiencia de compra y tienda_.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable Archiving] | Global | Determina si el archivado está habilitado. Opciones: `Yes` / `No` |
| [!UICONTROL Archive Orders Purchased] | Global | Determina el número de días que transcurren antes de que se archive un pedido completado. Valor predeterminado: `30` |
| [!UICONTROL Order  Statuses to be Archived] | Global | Determina el [status](../../stores-purchase/order-status.md) de pedidos para archivar. De forma predeterminada, se archivan los pedidos con un estado Completo o Cerrado. Opciones: `Pending` / `Processing` / `Suspected Fraud` / `Complete` / `Closed` / `Canceled` / `On Hold` |

{style="table-layout:auto"}

## [!UICONTROL RMA Settings]

{{ee-feature}}

![Configuración de RMA](./assets/sales-rma-settings.png)<!-- zoom -->

Para obtener más información sobre cómo cambiar esta configuración, consulte [Configuración de devoluciones](../../stores-purchase/rma-configure.md) en el _Guía de experiencia de compra y tienda_.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable RMA on Storefront] | Sitio web | Determina si los clientes pueden crear y ver solicitudes de RMA desde la tienda. La autorización de devolución de material se puede aplicar tanto a pedidos nuevos como existentes. De forma predeterminada, RMA no está activada para la tienda. Opciones: `Yes` / `No` |
| [!UICONTROL Enable RMA on Product Level] | Sitio web | Determina el valor predeterminado para el campo Habilitar RMA en la información del producto. |
| [!UICONTROL Use Store Address] | Sitio web | Determina el nombre y la dirección de contacto que se utilizan para los envíos de la mercancía devuelta. Opciones: <br/>**`Yes`**- Utiliza el [Punto de origen](../../stores-purchase/shipping-settings.md#point-of-origin) Dirección de Configuración de envío.<br/>**`No`** : abre el formulario de direcciones para que pueda introducir una dirección alternativa. |

{style="table-layout:auto"}
