---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Tax]'
description: Revise la configuración en la página [!UICONTROL Sales] &gt; [!UICONTROL Tax] del administrador de Commerce.
exl-id: eb929a6c-adb2-45ac-b6ec-6239938355bf
feature: Configuration, Taxes
source-git-commit: f95e6d22f83b518c64b254f0d98147e3c6ebaf42
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Tax]

>[!NOTE]
>
>Las versiones 2.4.0 a 2.4.3 de Adobe Commerce y Magento Open Source incluían la extensión desarrollada por el proveedor Vertex que se utilizó para integrarse con [!UICONTROL Vertex Cloud]. A partir de la versión 2.4.4, esta extensión ya no se integra con la versión principal y debe instalarse y actualizarse desde el Commerce Marketplace. Marketplace también proporciona acceso a la documentación actual proporcionada por el desarrollador de extensiones.
><br><br>
>Si tiene la extensión agrupada habilitada y configurada, debe actualizar el archivo composer.json como parte del proceso de actualización de la versión 2.4.4 y administrar las actualizaciones de extensión que se realicen. Consulte [Actualizar módulos y extensiones](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) en la _Guía de actualización_ para obtener más información.

{{config}}

## [!UICONTROL Tax Classes]

![Clases de impuestos](./assets/tax-tax-classes.png)<!-- zoom -->

Para obtener más información acerca de cómo cambiar esta configuración, consulte [Clases de impuestos](../../stores-purchase/tax-class.md) en la _Guía de tiendas y compras_.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Tax Class for Shipping] | Sitio web | Identifica la clase de impuesto que se utiliza para el envío. Las opciones incluyen todas las clases de impuestos de productos disponibles: `None` / `Taxable Goods` / `Shipping` / `Tax Exempt` |
| [!UICONTROL Tax Class for Gift Options] | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) Identifica la clase de impuesto predeterminada que se usa para las opciones de regalo. |
| [!UICONTROL Default Tax Class for Product] | Global | Identifica la clase de impuestos predeterminada que se utiliza para los productos. |
| [!UICONTROL Default Tax Class for Customer] | Global | Identifica la clase de impuestos predeterminada que se utiliza para los clientes. |

{style="table-layout:auto"}

## [!UICONTROL Calculation Settings]

![Configuración del cálculo](./assets/tax-calculation-settings.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | Sitio web | Determina el método utilizado para calcular el impuesto de un pedido. Opciones:<br/>**`Unit Price`**- Los cálculos de impuestos se basan en el precio unitario de cada producto.<br/>**`Row Total`** - Los cálculos de impuestos se basan en el total del elemento de línea. <br/>**`Total`**- Los cálculos de impuestos se basan en el total del pedido.<br/><br/>_ **&#x200B; Nota:**&#x200B;_Si hay una extensión de cálculo de impuestos instalada desde Marketplace, como _Vertex Cloud_, el servicio de extensión aparece como una opción. |
| [!UICONTROL Tax Calculation Based On] | Sitio web | Determina si el cálculo de impuestos se basa en la dirección de envío, la dirección de facturación o el origen de envío. Opciones: `Shipping Address` / `Billing Address` / `Shipping Origin` |
| [!UICONTROL Catalog Prices] | Sitio web | Determina si los precios de catálogo incluyen o excluyen impuestos. Opciones: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Shipping Prices] | Sitio web | Determina en los precios de envío si se incluyen o excluyen impuestos. Opciones: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Apply Customer Tax] | Sitio web | Determina si el impuesto se aplica antes o después de un descuento. Opciones: `Before Discount` / `After Discount` |
| [!UICONTROL Apply Discount on Prices] | Sitio web | Determina si los precios de descuento incluyen o excluyen impuestos. Opciones: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Apply Tax On] | Sitio web | Determina si el impuesto se aplica al precio original o a un precio personalizado, si está disponible. Opciones: `Custom price if available` / `Original price only` |
| [!UICONTROL Enable Cross Border Trade] | Sitio web | Cuando está activada, aplica precios consistentes a través de las fronteras de regiones con diferentes tasas de impuestos. Opciones: `Yes` / `No` <br/><br/>**_Nota:_**&#x200B;El uso del comercio transfronterizo ajusta el margen de beneficio por tasa de impuestos. |

{style="table-layout:auto"}

## [!UICONTROL Default Tax Destination Calculation]

![Cálculo de destino de impuestos predeterminado](./assets/tax-default-tax-destination-calculation.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Default Country] | Vista de tienda | Determina el país en el que se basan los cálculos de impuestos. |
| [!UICONTROL Default State] | Vista de tienda | Determina el estado en el que se basan los cálculos de impuestos. Un asterisco (*) puede funcionar como comodín para indicar todos los estados dentro del país seleccionado. |
| [!UICONTROL Default Post Code] | Vista de tienda | Identifica el código postal en el que se basan los cálculos de impuestos. Un asterisco (*) puede funcionar como comodín para indicar todos los códigos postales dentro del estado seleccionado. |

{style="table-layout:auto"}

## [!UICONTROL Price Display Settings]

![Configuración de visualización de precios](./assets/tax-price-display-settings.png)<!-- zoom -->

Para obtener más información acerca de cómo cambiar esta configuración, consulte [Configurar la configuración de visualización de precios](../../stores-purchase/display-settings.md#configure-price-display-settings) en la _Guía de tiendas y compras_.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Display Product Prices in Catalog] | Vista de tienda | Determina si los precios de productos publicados en el catálogo incluyen o excluyen impuestos, o muestran dos versiones del precio; una con y otra sin impuestos. Opciones: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` <br/><br/>**_Nota:_**&#x200B;Si establece el campo Mostrar precios de productos en `Including Tax`, el impuesto solo aparecerá si hay una regla fiscal que coincida con el origen del impuesto o si hay una dirección de cliente que coincida con la regla fiscal. Los eventos que pueden almacenar en déclencheur una coincidencia incluyen la creación de cuentas de cliente, el inicio de sesión o el uso de la herramienta de estimación de impuestos y envíos en el carro de compras. |
| [!UICONTROL Display Shipping Prices] | Vista de tienda | Determina si los precios de envío incluyen o excluyen impuestos, o muestran dos versiones del precio de envío; una con y otra sin impuestos. Opciones: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart Display Settings]

![Configuración de visualización del carro de compras](./assets/tax-shopping-cart-display-settings.png)<!-- zoom -->

Para obtener más información acerca de cómo cambiar esta configuración, consulte [Configurar la configuración de la pantalla del carro de compras](../../stores-purchase/display-settings.md#step-2-configure-shopping-cart-display-settings) en la _Guía de tiendas y experiencia de compra_.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Display Prices] | Vista de tienda | Determina si los precios del carro de compras incluyen o excluyen impuestos, o si muestran dos versiones del precio; una con y otra sin impuestos. Opciones: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Subtotal|Store View] | Determina si el subtotal del carro de compras incluye o excluye impuestos, o muestra dos versiones del subtotal; una con y otra sin impuestos. Opciones: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | Vista de tienda | Determina si el importe de envío del carro de compras incluye o excluye impuestos, o muestra dos versiones del importe de envío; una con y otra sin impuestos. Opciones: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Additionally Show Order Total Without Tax] | Vista de tienda | Determina si se muestra una línea adicional con el importe total general sin impuestos en el carro de compras. Opciones: `Yes` / `No` |
| [!UICONTROL Display Full Tax Summary] | Vista de tienda | Determina si el carro de compras incluye un resumen de impuestos completo. Opciones: `Yes` / `No` |
| [!UICONTROL Display Zero Tax Subtotal] | Vista de tienda | Determina si el carro de compras incluye un subtotal de impuestos cuando el impuesto es cero. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

![Configuración de visualización de pedidos, facturas y notas de abono](./assets/tax-orders-invoices-credit-memos-display-settings.png)<!-- zoom -->

Para obtener más información acerca de cómo cambiar esta configuración, consulte [Configurar los valores de pedido, factura y abono](../../stores-purchase/display-settings.md#step-3-configure-order-invoice-and-credit-memo-display-settings) en la _Guía de tiendas y compras_.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Display Prices] | Vista de tienda | Determina si los precios de los documentos de venta incluyen o excluyen impuestos, o si cada documento muestra dos versiones del precio; una con y otra sin impuestos. Opciones: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Subtotal] | Vista de tienda | Determina si el subtotal de los documentos de ventas incluye o excluye impuestos, o si cada documento muestra dos versiones del subtotal; una con impuestos y otra sin impuestos. Opciones: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | Vista de tienda | Determina si el importe de envío de los documentos de venta incluye o excluye impuestos, o si cada documento muestra dos versiones del subtotal; una con impuestos y otra sin impuestos. Opciones: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Additionally Show Order Total Without Tax] | Vista de tienda | Determina si se muestra una línea adicional con el importe total general sin impuestos en los documentos de ventas. Opciones: `Yes` / `No` |
| [!UICONTROL Display Full Tax Summary] | Vista de tienda | Determina si aparece el resumen completo de impuestos en los documentos de ventas. Opciones: `Yes` / `No` |
| [!UICONTROL Display Zero Tax Subtotal] | Vista de tienda | Determina la sección de subtotales de los documentos de ventas que aparece cuando no se cobra ningún impuesto. Opciones: `Yes` / `No` |
| [!UICONTROL Display Gift Wrapping Prices] | Vista de tienda | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) Determina si los precios de los envoltorios para regalos están incluidos en el subtotal. Opciones: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Printed Card Prices] | Vista de tienda | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) Determina si los precios de las tarjetas impresas están incluidos en el subtotal. Opciones: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |

{style="table-layout:auto"}

## [!UICONTROL Fixed Product Taxes]

![Impuesto de producto fijo](./assets/tax-fixed-product-taxes.png)<!-- zoom -->

Para obtener más información acerca de cómo cambiar esta configuración, consulte [Impuesto sobre productos fijos (FPT)](../../stores-purchase/fixed-product-tax.md) en la _Guía de compras y tiendas_.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable FPT] | Sitio web | Determina si FTP está disponible. Opciones: `Yes` / `No` |
| [!UICONTROL Display Prices in Product Lists] | Sitio web | Controla la visualización de FTP en listas de productos. Opciones:<br/> **`Including FPT Only`** - Los precios mostrados incluyen impuestos fijos sobre el producto. El importe de FTP no se muestra por separado.<br/>**`Including FPT and FPT description`**- Los precios mostrados incluyen impuestos fijos sobre el producto. El importe de FTP se muestra por separado.<br/>**`Excluding FPT. Including FPT description and final price`** - Los precios mostrados no incluyen impuestos fijos sobre los productos. El importe de FTP se muestra por separado.<br/>**`Excluding FPT`**- Los precios mostrados no incluyen impuestos fijos sobre los productos. El importe de FTP no se muestra por separado. |
| [!UICONTROL Display Prices On Product View Page] | Sitio web | Controla la visualización de FTP en la página del producto. Opciones:<br/> **`Including FPT Only`** - Los precios mostrados incluyen impuestos fijos sobre el producto. El importe de FTP no se muestra por separado.<br/>**`Including FPT and FPT description`**- Los precios mostrados incluyen impuestos fijos sobre el producto. El importe de FTP se muestra por separado.<br/>**`Excluding FPT. Including FPT description and final price`** - Los precios mostrados no incluyen impuestos fijos sobre los productos. El importe de FTP se muestra por separado.<br/>**`Excluding FPT`**- Los precios mostrados no incluyen impuestos fijos sobre los productos. El importe de FTP no se muestra por separado. |
| [!UICONTROL Display Prices in Sales Modules] | Sitio web | Controla la visualización de FPT en el carro de compras y durante el cierre de compra. Opciones:<br/> **`Including FPT Only`** - Los precios mostrados incluyen impuestos fijos sobre el producto. El importe de FTP no se muestra por separado.<br/>**`Including FPT and FPT description`**- Los precios mostrados incluyen impuestos fijos sobre el producto. El importe de FTP se muestra por separado.<br/>**`Excluding FPT. Including FPT description and final price`** - Los precios mostrados no incluyen impuestos fijos sobre los productos. El importe de FTP se muestra por separado.<br/>**`Excluding FPT`**- Los precios mostrados no incluyen impuestos fijos sobre los productos. El importe de FTP no se muestra por separado. |
| [!UICONTROL Display Prices in Emails] | Sitio web | Controla la visualización de FTP en el correo electrónico. Opciones:<br/> **`Including FPT Only`** - Los precios mostrados incluyen impuestos fijos sobre el producto. El importe de FTP no se muestra por separado.<br/>**`Including FPT and FPT description`**- Los precios mostrados incluyen impuestos fijos sobre el producto. El importe de FTP se muestra por separado.<br/>**&#x200B; Excluyendo FTP. Incluyendo descripción de FTP y precio final &#x200B;**- Los precios mostrados no incluyen impuestos fijos sobre los productos. El importe de FTP se muestra por separado.<br/>**`Excluding FPT`** - Los precios mostrados no incluyen impuestos fijos sobre los productos. El importe de FTP no se muestra por separado. |
| [!UICONTROL Apply Tax to FPT] | Sitio web | Determina si el impuesto se aplica al importe FTP. Opciones: `Yes` / `No` |
| [!UICONTROL Include FPT in Subtotal] | Sitio web | Determina si FTP está incluido en el subtotal del carro de compras. Opciones: <br/>**`Yes`**- Incluye FTP en el subtotal del carro de compras.<br/>**`No`** - FTP no se incluye en el subtotal y se coloca después del subtotal en el carro de compras. |

{style="table-layout:auto"}
