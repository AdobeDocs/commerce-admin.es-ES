---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Checkout]'
description: Revise la configuración en la página [!UICONTROL Sales] &gt; [!UICONTROL Checkout] del administrador de Commerce.
exl-id: a912beb0-37a9-407b-83bd-dc6cd0554dc4
feature: Configuration, Checkout
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Checkout]

{{config}}

## [!UICONTROL Checkout Options]

![Opciones de cierre de compra](./assets/checkout-checkout-options.png)<!-- zoom -->

<!--[Checkout Options](https://experienceleague.adobe.com/es/docs/commerce-admin/stores-sales/point-of-purchase/checkout/checkout-process#checkout-options) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|------------------------------------------------------------------|--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Guest Checkout Login] | Vista de tienda | Active esta configuración para permitir que los usuarios no autenticados (tienda y API) consulten si ya hay una dirección de correo electrónico asociada a una cuenta de cliente. Esto se puede utilizar para mejorar el flujo de trabajo de cierre de compra de los invitados mostrando un mensaje de inicio de sesión si la dirección de correo electrónico introducida ya está registrada en una cuenta de cliente, pero cuesta exponer la información a usuarios no autenticados.  Opciones: `Yes` / `No` |
| [!UICONTROL Enable Onepage Checkout] | Vista de tienda | Determina si [Cierre de compra de una página](../../stores-purchase/checkout-process.md#checkout-options) es el formato de cierre de compra predeterminado. Opciones: `Yes` / `No` |
| [!UICONTROL Allow Guest Checkout] | Vista de tienda | Determina si los invitados pueden pasar por [pago y envío sin registrar](../../stores-purchase/checkout-guest.md) una cuenta en tu tienda. Opciones: `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | Vista de tienda | Determina si los clientes deben aceptar los [Términos y condiciones](../../stores-purchase/terms-and-conditions.md) de la venta antes de realizar una compra. Opciones: `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | Vista de tienda | Determina la ubicación de la dirección de facturación durante el cierre de compra. Opciones: `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | Vista de tienda | Determina el número máximo de elementos que pueden aparecer en _Resumen de pedidos_ durante el cierre de compra. El valor predeterminado es `10`. |
| [!UICONTROL Enable Address Search] | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) Determina si los clientes pueden usar la funcionalidad [búsqueda de direcciones](../../stores-purchase/checkout-address-search.md) para los pasos Envío y Revisión y pagos. Cuando esté habilitada, utilice el Límite de número de direcciones del cliente para establecer el número de direcciones guardadas necesarias para activar esta funcionalidad durante el cierre de compra. Opciones: `Yes` / `No` |
| Límite de número de direcciones de clientes | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce): cuando la búsqueda de direcciones está habilitada, determina el número de direcciones guardadas necesarias para activar esta funcionalidad durante la desprotección. Cuando el número de direcciones guardadas del cliente cumple o supera este número, solo se representa la dirección predeterminada en los pasos _Envío_ y _Revisión y pagos_. El cliente puede utilizar una función de búsqueda para cambiar la dirección seleccionada. El valor predeterminado es `10`. |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart]

![Carro de compras](./assets/checkout-shopping-cart.png)<!-- zoom -->

<!--[Shopping Cart](https://experienceleague.adobe.com/es/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Quote Lifetime (days)] | Sitio web | Determina la duración [de un precio cotizado](../../stores-purchase/cart-configuration.md#quote-lifetime), en días. |
| [!UICONTROL After Adding a Product Redirect to Shopping Cart] | Vista de tienda | Determina si la [página del carro de compras aparece](../../stores-purchase/cart-configuration.md#redirect-to-cart) inmediatamente después de agregar un producto al carro de compras. Opciones: `Yes` / `No` |
| [!UICONTROL Number of Items to Display Pager] | Vista de tienda | Determina la cantidad de artículos en el carro de compras antes de activar el localizador. Valor predeterminado: `20` |
| [!UICONTROL Show Cross-sell Items in the Shopping Cart] | Vista de tienda | Indica si se muestran [artículos de venta cruzada](../../catalog/related-products-up-sells-cross-sells.md#cross-sells) en el carro de compras, lo que proporciona opciones de venta adicionales a los clientes. Opciones: `Yes` (predeterminado) / `No` |
| [!UICONTROL Grouped Product Image] | Vista de tienda | Determina la imagen en miniatura [thumbnail](../../stores-purchase/cart-configuration.md#cart-thumbnails) que aparece para un [producto agrupado](../../catalog/product-create-grouped.md) en el carro de compras. Opciones: `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Configurable Product Image] | Vista de tienda | Determina la imagen en miniatura [thumbnail](../../stores-purchase/cart-configuration.md#cart-thumbnails) que aparece para un producto configurable en el carro de compras. Opciones: `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Preview Quote Lifetime (minutes)] | Vista de tienda | Determina la antigüedad máxima del presupuesto en minutos cuando se obtiene una vista previa del carro de compras. |
| [!UICONTROL Enable Clear Shopping Cart] | Sitio web | Determina si el carro de compras muestra la opción para que los usuarios borren el contenido del carro en una sola acción. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL My Cart Link]

![Vínculo de mi carro de compras](./assets/checkout-my-cart-link.png)<!-- zoom -->

<!-- [*My Cart Link*](https://experienceleague.adobe.com/es/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#mini-cart) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Display Cart Summary] | Sitio web | Determina el valor que aparece entre paréntesis después del vínculo Mi carro de compras. Opciones: `Display number of items in cart` / `Display item quantities` |

{style="table-layout:auto"}

## Minicarrito

![Minicarrito](./assets/checkout-mini-cart.png)<!-- zoom -->

<!-- [*Mini Cart*](https://experienceleague.adobe.com/es/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#mini-cart) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Display Mini Cart] | Vista de tienda | Determina si el minicarrito aparece en las páginas de una tienda cuando se hace clic en el icono del carrito en el encabezado. La visualización del minicarrito depende del tema. Opciones: `Yes` / `No` |
| [!UICONTROL Number of Items to Display Scrollbar] | Vista de tienda | Determina el número de elementos que pueden aparecer en el minicarrito antes de activar la barra de desplazamiento. Predeterminado: `5` |
| [!UICONTROL Maximum Number of Items to Display] | Vista de tienda | Determina el número máximo de elementos que pueden aparecer en el minicarrito. Predeterminado: `10` |

{style="table-layout:auto"}

## [!UICONTROL Payment Failed Emails]

![Correos electrónicos con errores de pago](./assets/checkout-payment-failed-emails.png)<!-- zoom -->

<!-- [*Payment Failed Emails*](https://experienceleague.adobe.com/es/docs/commerce-admin/stores-sales/point-of-purchase/checkout/checkout-payment-failed-emails) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Payment Failed Email Receiver] | Vista de tienda | Identifica al contacto de la tienda que recibe los correos electrónicos con errores de pago. Receptor predeterminado: `General Contact` |
| [!UICONTROL Payment Failed Email Sender] | Vista de tienda | Identifica el contacto de tienda que aparece como el remitente del mensaje de los correos electrónicos con errores de pago. Remitente predeterminado: `General Contact` |
| [!UICONTROL Payment Failed Template] | Vista de tienda | Identifica la plantilla que se utiliza para los correos electrónicos con errores de pago. Plantilla predeterminada: `Payment Failed` |
| [!UICONTROL Send Payment Failed Copy To] | Vista de tienda | Proporciona la dirección de correo electrónico de cualquier persona que desee recibir una copia de un correo electrónico de error en el pago. Separe las direcciones con comas. |
| [!UICONTROL Send Payment Failed Copy Method] | Vista de tienda | Indica el método de correo electrónico utilizado para enviar la copia. Opciones: <br />**`Bcc`**: envía una copia de cortesía oculta incluyendo el destinatario en el encabezado del mismo correo electrónico que se envía al cliente. El destinatario CCO no es visible para el cliente.<br />**`Separate Email`** - Envía la copia como un correo electrónico independiente. |

{style="table-layout:auto"}
