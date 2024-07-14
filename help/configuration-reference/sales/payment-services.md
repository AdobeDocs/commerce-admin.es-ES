---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL Payment Services]'
description: Revise las opciones de configuración en la sección [!UICONTROL Payment Services] de la página [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] del administrador de Commerce.
exl-id: 255b7bd8-1d32-4393-9eba-43dc7754c752
feature: Configuration, Payments
source-git-commit: bf166c1debd7f10a4d988d231a1a47f32c4cea9e
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Payment Services]



Payment Services proporciona una solución de autoservicio llave en mano, que incluye pruebas de zona protegida y una configuración sencilla para proporcionar un procesamiento de pagos sólido y seguro. Para obtener más información, consulte la [_Guía del usuario de servicios de pago_](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

Para acceder a los ajustes de configuración de Payment Services, en la barra lateral de _Admin_, ve a **[!UICONTROL Sales]** > **[!UICONTROL Payment Services]** y haz clic en **[!UICONTROL Settings]**.

![Configuración de servicios de pago](assets/payment-services-menu-small.png){width="400"}

>[!NOTE]
>
>Para usar la configuración heredada en lugar de [Configuración](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/configure/settings.html), consulte [Configuración heredada](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/configure/configure-admin.html).

## [!UICONTROL General]

![Configuración general](assets/payments-general-settings.png){width="600" zoomable="yes"}

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|---|---|---|
| [!UICONTROL Enable] | sitio web | Habilite o deshabilite [!DNL Payment Services] para su sitio web. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Payment mode] | vista de tienda | Defina el método o el entorno para su tienda. Opciones: [!UICONTROL Sandbox] / [!UICONTROL Production] |
| [!UICONTROL Sandbox Merchant ID] | vista de tienda | El ID de comerciante de la zona protegida, que se genera automáticamente durante la incorporación a la zona protegida. |
| [!UICONTROL Production Merchant ID] | vista de tienda | Su ID de comerciante de producción, que se genera automáticamente durante la incorporación a la zona protegida. |
| [!UICONTROL Soft Descriptor] | sitio web o vista de tienda | Añada un descriptor temporal a los sitios web y a las vistas de tienda que proporcione información sobre transacciones de clientes y defina marcas, tiendas o líneas de productos. La opción [!UICONTROL Use website] aplica cualquier descriptor flexible agregado en el nivel de sitio web. La opción [!UICONTROL Use default] aplica cualquier descriptor flexible agregado como predeterminado. |

{style="table-layout:auto"}

## [!UICONTROL Credit card fields]

![Configuración del campo de la tarjeta de crédito](assets/payments-ccfields-settings.png){width="600" zoomable="yes"}

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|---|---|---|
| [!UICONTROL Title] | vista de tienda | Añade el texto que se mostrará como el título de esta opción de pago en la vista Método de pago durante el cierre de compra. |
| [!UICONTROL Payment Action] | sitio web | La [acción de pago](payment-methods.md#payment-actions) para el método de pago especificado. Opciones: [!UICONTROL Authorize] / [!UICONTROL Authorize and Capture] |
| [!UICONTROL 3DS Secure authentication] | sitio web | Habilitar o deshabilitar la [autenticación segura de 3DS](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/security-compliance/security.html#3ds). Opciones: [!UICONTROL Always] / [!UICONTROL When Required] / [!UICONTROL Off] |
| [!UICONTROL Show on checkout page] | sitio web | Habilitar o deshabilitar los campos de tarjeta de crédito para mostrar en la página de cierre de compra. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Vault enabled] | vista de tienda | Habilitar o deshabilitar el depósito de [tarjetas de crédito](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/payments-checkout/vaulting.html). Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show vaulted payment methods in Admin] | vista de tienda | Habilite o deshabilite la capacidad para completar pedidos de clientes del administrador [mediante un método de pago abovedado](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/payments-checkout/vaulting.html). Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Debug Mode] | sitio web | Habilite o deshabilite el modo de depuración. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |

{style="table-layout:auto"}

## [!UICONTROL Payment buttons]

![Configuración de botones de pago de PayPal](assets/payments-ppbuttons-settings.png){width="600" zoomable="yes"}

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|---|---|---|
| [!UICONTROL Title] | vista de tienda | Agrega el texto que se mostrará como título para esta opción de pago en la vista Método de pago durante el cierre de compra. |
| [!UICONTROL Payment Action] | sitio web | La [acción de pago](payment-methods.md#payment-actions){target="_blank"} para el método de pago especificado. Opciones: [!UICONTROL Authorize] / [!UICONTROL Authorize and Capture] |
| [!UICONTROL Show PayPal buttons on checkout page] | vista de tienda | Habilitar o deshabilitar [!DNL PayPal Smart Buttons] en la página de cierre de compra. Opciones: [!UICONTROL  Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons on product detail page] | vista de tienda | Habilite o deshabilite [!DNL PayPal Smart Buttons] en la página de detalles del producto. Opciones: [!UICONTROL  Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons in mini-cart preview] | vista de tienda | Habilite o deshabilite [!DNL PayPal Smart Buttons] en la vista previa del minicarrito. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons on cart page] | vista de tienda | Habilite o deshabilite [!DNL PayPal Smart Buttons] en la página del carro de compras. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Pay Later button] | vista de tienda | Activar o desactivar la aparición de la opción de pago posterior en la que se muestran los botones de pago. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Pay Later Message] | sitio web | Habilite o deshabilite la mensajería Pagar más tarde en el carro de compras, la página del producto, el minicarrito y durante el flujo de cierre de compra. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show Venmo button] | vista de tienda | Activa o desactiva la opción de pago Venmo donde se muestran los botones de pago. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show Apple Pay button] | vista de tienda | Activa o desactiva la opción de pago de Apple Pay donde se muestran los botones de pago. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Credit and Debit card button] | vista de tienda | Activa o desactiva la opción de pago con tarjeta de crédito y débito donde se muestran los botones de pago. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Debug Mode] | sitio web | Habilite o deshabilite el modo de depuración. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |

{style="table-layout:auto"}

## [!UICONTROL PayPal Smart Button Styling]

![Configuración de estilo de botones de pago de PayPal](assets/payments-buttonstyle-settings.png){width="600" zoomable="yes"}

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Layout] | Vista de tienda | Definir el estilo del diseño de los botones de pago. Opciones: [!UICONTROL Vertical] / [!UICONTROL Horizontal] |
| [!UICONTROL Tagline] | Vista de tienda | Habilitar/deshabilitar el lema. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Color] | Vista de tienda | Defina el color de los botones de pago. Opciones: [!UICONTROL Blue] / [!UICONTROL Gold] / [!UICONTROL Silver] / [!UICONTROL White] / [!UICONTROL Black] |
| [!UICONTROL Shape] | Vista de tienda | Definir la forma de los botones de pago. Opciones: [!UICONTROL Rectangular] / [!UICONTROL Pill] |
| [!UICONTROL Responsive Button Height] | Vista de tienda | Define si los botones de pago utilizan una altura predeterminada. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Height] | Vista de tienda | Definir la altura de los botones de pago. Valor predeterminado: ninguno |
| [!UICONTROL Label] | Vista de tienda | Definir la etiqueta que aparece en los botones de pago. Opciones: [!UICONTROL PayPal] / [!UICONTROL Checkout] / [!UICONTROL Buynow] / [!UICONTROL Pay] / [!UICONTROL Installment] |

{style="table-layout:auto"}
