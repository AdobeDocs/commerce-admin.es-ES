---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL Payment Services]'
description: Revise los ajustes de configuración en la [!UICONTROL Payment Services] en la sección [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] de la administración de Commerce.
exl-id: 255b7bd8-1d32-4393-9eba-43dc7754c752
feature: Configuration, Payments
source-git-commit: aafda7f534f4170825edb7c163e4221df2f205bb
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Payment Services]



Payment Services proporciona una solución de autoservicio llave en mano, que incluye pruebas de zona protegida y una configuración sencilla para proporcionar un procesamiento de pagos sólido y seguro. Para obtener más información, consulte la [_Guía del usuario de Payment Services_](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

Para acceder a los ajustes de configuración de Payment Services, en _Administrador_ barra lateral ir a **[!UICONTROL Sales]** > **[!UICONTROL Payment Services]** y haga clic en **[!UICONTROL Settings]**.

![Configuración de servicios de pago](assets/payment-services-menu-small.png){zoomable: no, anchura: 400px}

>[!NOTE]
>
>Para utilizar la configuración heredada en lugar de [Configuración](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/configure/settings.html), consulte [Configuración heredada](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/configure/configure-admin.html).

## [!UICONTROL General]

![Configuración general](assets/payments-general-settings.png){zoomable: yes, width: 600px}

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|---|---|---|
| [!UICONTROL Enable] | sitio web | Habilitar o deshabilitar [!DNL Payment Services] para su sitio web. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Payment mode] | vista de tienda | Defina el método o el entorno para su tienda. Opciones: [!UICONTROL Sandbox] / [!UICONTROL Production] |
| [!UICONTROL Sandbox Merchant ID] | vista de tienda | El ID de comerciante de la zona protegida, que se genera automáticamente durante la incorporación a la zona protegida. |
| [!UICONTROL Production Merchant ID] | vista de tienda | Su ID de comerciante de producción, que se genera automáticamente durante la incorporación a la zona protegida. |
| [!UICONTROL Soft Descriptor] | sitio web o vista de tienda | Añada un descriptor temporal a sus sitios web y vistas de tiendas para añadir información a las transacciones de clientes que delimitan marcas, tiendas o líneas de productos. El [!UICONTROL Use website] Esta opción aplica cualquier descriptor temporal agregado en el nivel de sitio web. El [!UICONTROL Use default] La opción aplica cualquier descriptor temporal agregado como predeterminado. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Credit card fields]

![Configuración del campo de tarjeta de crédito](assets/payments-ccfields-settings.png){zoomable: yes, width: 600px}

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|---|---|---|
| [!UICONTROL Title] | vista de tienda | Añade el texto que se mostrará como el título de esta opción de pago en la vista Método de pago durante el cierre de compra. Opciones: [!UICONTROL text field] |
| [!UICONTROL Payment Action] | sitio web | El [acción de pago](payment-methods.md#payment-actions) para el método de pago especificado. Opciones: [!UICONTROL Authorize] / [!UICONTROL Authorize and Capture] |
| [!UICONTROL 3DS Secure authentication] | sitio web | Habilitar o deshabilitar [Autenticación segura en 3DS](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/security-compliance/security.html#3ds). Opciones: [!UICONTROL Always] / [!UICONTROL When Required] / [!UICONTROL Off] |
| [!UICONTROL Show on checkout page] | sitio web | Habilitar o deshabilitar los campos de tarjeta de crédito para mostrar en la página de cierre de compra. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Vault enabled] | vista de tienda | Habilitar o deshabilitar [depósito de tarjetas de crédito](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/payments-checkout/vaulting.html). Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show vaulted payment methods in Admin] | vista de tienda | Habilite o deshabilite la capacidad para que el comerciante complete pedidos de clientes en Admin [uso de un método de pago abovedado](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/payments-checkout/vaulting.html). Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Debug Mode] | sitio web | Habilite o deshabilite el modo de depuración. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Payment buttons]

![Configuración de botones de pago de PayPal](assets/payments-ppbuttons-settings.png){zoomable: yes, width: 600px}

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|---|---|---|
| [!UICONTROL Title] | vista de tienda | Agrega el texto que se mostrará como título para esta opción de pago en la vista Método de pago durante el cierre de compra. |
| [!UICONTROL Payment Action] | sitio web | El [acción de pago](payment-methods.md#payment-actions){target="_blank"} para el método de pago especificado. Opciones: [!UICONTROL Authorize] / [!UICONTROL Authorize and Capture] |
| [!UICONTROL Show PayPal buttons on checkout page] | vista de tienda | Habilitar o deshabilitar [!DNL PayPal Smart Buttons] en la página de cierre de compra. Opciones: [!UICONTROL  Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons on product detail page] | vista de tienda | Habilitar o deshabilitar [!DNL PayPal Smart Buttons] en la página de detalles del producto. Opciones: [!UICONTROL  Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons in mini-cart preview] | vista de tienda | Habilitar o deshabilitar [!DNL PayPal Smart Buttons] en la vista previa del minicarrito. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons on cart page] | vista de tienda | Habilitar o deshabilitar [!DNL PayPal Smart Buttons] en la página del carro de compras. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Pay Later button] | vista de tienda | Activar o desactivar la aparición de la opción de pago posterior en la que se muestran los botones de pago. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Pay Later Message] | sitio web | Habilite o deshabilite la mensajería Pagar más tarde en el carro de compras, la página del producto, el minicarrito y durante el flujo de cierre de compra. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show Venmo button] | vista de tienda | Activa o desactiva la opción de pago Venmo donde se muestran los botones de pago. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show Apple Pay button] | vista de tienda | Activa o desactiva la opción de pago de Apple Pay donde se muestran los botones de pago. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Credit and Debit card button] | vista de tienda | Activa o desactiva la opción de pago con tarjeta de crédito y débito donde se muestran los botones de pago. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Debug Mode] | sitio web | Habilite o deshabilite el modo de depuración. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL PayPal Smart Button Styling]

![Configuración de estilo de botones de pago PayPal](assets/payments-buttonstyle-settings.png){zoomable: yes, width: 600px}

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Layout] | Vista de tienda | Definir el estilo del diseño de los botones de pago. Opciones: [!UICONTROL Vertical] / [!UICONTROL Horizontal] |
| [!UICONTROL Tagline] | Vista de tienda | Habilitar/deshabilitar el lema. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Color] | Vista de tienda | Defina el color de los botones de pago. Opciones: [!UICONTROL Blue] / [!UICONTROL Gold] / [!UICONTROL Silver] / [!UICONTROL White] / [!UICONTROL Black] |
| [!UICONTROL Shape] | Vista de tienda | Definir la forma de los botones de pago. Opciones: [!UICONTROL Rectangular] / [!UICONTROL Pill] |
| [!UICONTROL Responsive Button Height] | Vista de tienda | Define si los botones de pago utilizan una altura predeterminada. Opciones: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Height] | Vista de tienda | Definir la altura de los botones de pago. Valor predeterminado: ninguno |
| [!UICONTROL Label] | Vista de tienda | Definir la etiqueta que aparece en los botones de pago. Opciones: [!UICONTROL PayPal] / [!UICONTROL Checkout] / [!UICONTROL Buynow] / [!UICONTROL Pay] / [!UICONTROL Installment] |

{:style=&quot;table-layout:auto&quot;}
