---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL Braintree]'
description: Revise la configuración de la sección [!UICONTROL Braintree] en la página [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] del administrador de Commerce.
exl-id: cf08bc4d-8d88-45e7-af71-f1ff90023766
feature: Configuration, Payments
source-git-commit: 5488a0a991f497059ea39fbbc8a08fd8f546e1ac
workflow-type: tm+mt
source-wordcount: '2603'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Braintree]

>[!IMPORTANT]
>
>**Migración a Commerce 2.4:**<br/>
>Para las versiones de Adobe Commerce y Magento Open Source anteriores a la 2.4.0, se recomendó que los comerciantes instalaran y configuraran la extensión oficial de integración de pagos de Braintree desde el [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=braintree) para reemplazar la integración principal. A partir de la versión 2.4.0, la extensión de se incluye ahora en la versión principal.
><br/><br/>
>Al migrar a Commerce 2.4, los comerciantes deben desinstalar la extensión distribuida en Marketplace (`paypal/module-braintree` o `gene/module-braintree`) y actualizar las personalizaciones de código para utilizar el área de nombres `PayPal_Braintree` en lugar de `Magento_Braintree`. Los ajustes de configuración de la extensión agrupada para Commerce y la extensión distribuida en el Commerce Marketplace se mantienen. Los pagos realizados con esas versiones de la extensión se capturan, anulan o devuelven con normalidad.
><br/><br/>
>Si actualiza a Commerce 2.4.0 y no utiliza la extensión de Commerce Marketplace recomendada en la versión 2.3.x anterior, la función de varias direcciones no funciona con la versión 2.4.0 de Braintree. Cuando un comprador selecciona _enviar a varias direcciones_ , el método de pago del Braintree no aparece. La extensión de Commerce Marketplace recomendada anteriormente para 2.3.x tiene este problema de varias direcciones.

{{config}}

## [!UICONTROL Basic Braintree Settings]

![Configuración básica del Braintree](./assets/payment-methods-braintree-basic-config.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Title] | Vista de tienda | Valor predeterminado: `Credit Card` (Braintree) |
| [!UICONTROL Environment] | Vista de tienda | Opciones: `Sandbox` / `Production` |
| [!UICONTROL Payment Action] | Vista de tienda | Determina la acción realizada por el Braintree cuando se procesa un pago. Opciones: <br/>**`Authorize`**- Los fondos de la tarjeta de crédito del cliente están autorizados, pero no se transfieren desde la cuenta. Se crea un pedido en el administrador de la tienda. Más tarde puede capturar la venta y crear una factura.<br/>**`Intent Sale`** (anteriormente `Authorize and Capture` en versiones anteriores): el Braintree autoriza y captura los fondos de la tarjeta de crédito del cliente, y se crean un pedido y una factura en el administrador de la tienda. |
| [!UICONTROL Sandbox Merchant ID] | Vista de tienda | Este es el identificador único de toda la cuenta de puerta de enlace de la zona protegida. También conocido como _ID público_ o _ID de producción_, su ID de comerciante es diferente para sus puertas de enlace de producción y de zona protegida. Este campo aparece cuando el campo _[!UICONTROL Environment]_está establecido en `Sandbox`. |
| [!UICONTROL Sandbox Public Key] | Vista de tienda | Identificador público específico del usuario que restringe el acceso a los datos cifrados. Cada usuario asociado con la puerta de enlace del Braintree de la zona protegida tiene su propia clave pública de la zona protegida. Este campo aparece cuando el campo _[!UICONTROL Environment]_está establecido en `Sandbox`. |
| [!UICONTROL Sandbox Private Key] | Vista de tienda | Identificador privado específico del usuario que restringe el acceso a los datos cifrados. Cada usuario asociado con la puerta de enlace del Braintree de la zona protegida tiene su propia clave privada para la zona protegida. Este campo aparece cuando el campo _[!UICONTROL Environment]_está establecido en `Sandbox`. |
| [!UICONTROL Merchant ID] | Vista de tienda | Este es el identificador único de toda la cuenta de puerta de enlace, incluidas las cuentas de varios comerciantes que pueden estar en la puerta de enlace. También conocido como _ID público_ o _ID de producción_, su ID de comerciante es diferente para sus puertas de enlace de producción y de zona protegida. Este campo aparece cuando el campo _[!UICONTROL Environment]_está establecido en `Production`. |
| [!UICONTROL Public Key] | Vista de tienda | Identificador público específico del usuario que restringe el acceso a los datos cifrados. Cada usuario asociado con la puerta de enlace de Braintree tiene su propia clave pública. Este campo aparece cuando el campo _[!UICONTROL Environment]_está establecido en `Production`. |
| [!UICONTROL Private Key] | Vista de tienda | Identificador privado específico del usuario que restringe el acceso a los datos cifrados. Cada usuario asociado con la puerta de enlace de Braintree tiene su propia clave privada. Este campo aparece cuando el campo _[!UICONTROL Environment]_está establecido en `Production`. |
| [!UICONTROL Enable Card Payments] | Sitio web | Determina si el método de pago con tarjeta de crédito del Braintree está disponible para los clientes como método de pago. Opciones: `Yes` / `No` |
| [!UICONTROL Enable Vault for Card Payments] | Sitio web | Cuando está activada, proporciona almacenamiento seguro para la información de pago del cliente, de modo que los clientes no tienen que volver a introducir la información de su tarjeta de crédito para cada compra. Opciones: `Yes` / `No` |
| [!UICONTROL Enable Vault CVV Reverification] | Sitio web | Cuando está activada, la validación se realiza para la configuración de reglas CVV en su Cuenta de Braintree. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Braintree Settings]

![Configuración avanzada del Braintree](./assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Vault Title] | Sitio web | Título descriptivo de referencia que identifica el almacén donde se almacena la información de la tarjeta del cliente. |
| [!UICONTROL Merchant Account ID] | Sitio web | El ID de la cuenta de comerciante que se asociará con las transacciones de Braintree desde este sitio web. Si se deja en blanco, se utiliza la cuenta de comerciante predeterminada de la cuenta de Braintree. |
| [!UICONTROL Enable Checkout Express Payments] | Sitio web | Proporciona una experiencia de pago más rápida con las opciones de Pago exprés al principio del proceso de pago, que incluyen PayPal, PayAfter, Apple Pay y Google Pay. Opciones: `Yes` / `No` |
| [!UICONTROL Skip Fraud Checks on Admin Orders] | Sitio web | Evita que la transacción se envíe para su evaluación como parte de [!DNL Advanced Fraud Tools] comprobaciones, en pedidos realizados a través del administrador solo cuando se establece en `Yes`.<br/>Opciones: `Yes` / `No` |
| [!UICONTROL Bypass Fraud Protection Threshold] | Sitio web | Se omiten `Advanced Fraud Protection` comprobaciones cuando se alcanza o supera el valor de umbral. Si deja este campo en blanco, se deshabilita esta opción. |
| [!UICONTROL Debug] | Sitio web | Determina si las comunicaciones entre el sistema Braintree y el almacén se graban en un archivo de registro. Opciones: `Yes` / `No` |
| [!UICONTROL CVV Verification] | Sitio web | Determina si los clientes deben proporcionar el código de seguridad de tres dígitos desde el reverso de una tarjeta de crédito. Opciones: `Yes` / `No` |
| [!UICONTROL Send Card Line Items] | Sitio web | Envíe los elementos de línea de carro de compras para todas las formas de pago. Opciones: `Yes` / `No` |
| [!UICONTROL Credit Card Types] | Sitio web | Especifica cada tarjeta de crédito que acepta como pago a través del Braintree. Mantenga presionado `Ctrl` (o `Command` en Mac) para seleccionar una combinación de tarjetas. Opciones: `American Express` / `Visa` / `MasterCard` / `Discover` / `JCB` / `Diners` / `Maestro International` |
| [!UICONTROL Sort Order] | Sitio web | Determina el pedido en el que el Braintree aparece con otras formas de pago durante el cierre de compra. |

## [!UICONTROL Braintree Webhooks Settings]

![Configuración de Webhooks de Braintree](./assets/payment-methods-braintree-webhooks-config.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable Webhook] | Sitio web | Para habilitar la funcionalidad de webhook para la protección contra fraudes, pagos ACH, métodos de pago locales y disputas. Opciones: `Yes` / `No` |
| [!UICONTROL Fraud Protection URL] | Sitio web | Agregue esta URL a su cuenta de Braintree como [!UICONTROL Webhook Destination URL]. **Esta dirección URL debe ser segura y de acceso público.** |
| [!UICONTROL Fraud Protection Approve Order Status] | Sitio web | Cuando el Braintree aprueba la protección contra el fraude, el estado del pedido seleccionado se asigna al pedido de Commerce. Este estado se usa para actualizar el estado del pedido donde se usa el método de pago ACH y cuando se mueve a `SETTLED` en Braintree. |
| [!UICONTROL Fraud Protection Reject Order Status] | Sitio web | Cuando el Braintree rechaza la protección contra el fraude, el estado del pedido seleccionado se asigna al pedido de Commerce. Este estado se usa para actualizar el estado del pedido donde se usa el método de pago ACH y cuando `SETTLEMENT` es `DECLINED` en Braintree. |

{style="table-layout:auto"}

## [!UICONTROL Country Specific Settings]

![Configuración específica de país](./assets/payment-methods-braintree-country-specific-config.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Payment from Applicable Countries] | Sitio web | Determina si acepta pagos procesados por Braintree de todos los países o sólo de países específicos. Opciones: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Sitio web | Si procede, indica los países específicos desde los que acepta pagos procesados por el Braintree. |
| [!UICONTROL Country Specific Credit Card Types] | Sitio web | Identifica las tarjetas de crédito aceptadas por país para los pagos procesados por el Braintree. Se guarda un registro para cada país. Opciones: <br/>**`Country`**- Elija el país.<br/>**`Allowed Card Types`** - Selecciona cada tarjeta de crédito que se acepte del país como pago mediante Braintree. <br/>**`Add`**- Agregar una línea para permitir tarjetas de crédito para un país diferente.<br/>**`Action`** - Elimina el registro de tarjetas de crédito permitidas para el país. |

{style="table-layout:auto"}

## [!UICONTROL ACH through Braintree]

![ACH mediante Braintree](./assets/payment-methods-braintree-ach-config.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enabled ACH Direct Debit] | Sitio web | Determina si [!DNL ACH Direct Debit] se incluye como método de pago mediante Braintree. Opciones: `Yes` / `No` |
| [!UICONTROL Enable Vault for ACH Direct Debit] | Sitio web | Los clientes pueden almacenar o depositar su método de pago mediante domiciliación bancaria ACH de un solo uso para uso futuro. Una vez que los datos de pago se han guardado, el cliente puede utilizar el método de pago de domiciliación bancaria ACH sin volver a introducir datos ni volver a autenticar su información de pago. Opciones: `Yes` / `No` |
| [!UICONTROL Sort Order] | Sitio web | Determina el pedido que [!DNL ACH Direct Debit] se enumera con otras formas de pago durante el cierre de compra. |

{style="table-layout:auto"}

## [!UICONTROL Apple Pay through Braintree]

![Apple Pay mediante Braintree](./assets/payment-methods-braintree-applepay-config.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable ApplePay through Braintree] | Sitio web | Determina si Apple Pay se incluye como forma de pago a través del Braintree. Opciones: `Yes` / `No` <br/><br/> El dominio debe estar [comprobado primero en la cuenta de Braintree](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3). |
| [!UICONTROL Enable Vault for ApplePay] | Sitio web | Los clientes pueden depositar o almacenar su método de pago de Apple Pay para uso futuro. Una vez que los datos de pago se han guardado, el cliente puede utilizar Apple Pay sin tener que volver a introducir los datos ni volver a autenticar su información de pago. Opciones: `Yes` / `No` |
| [!UICONTROL Payment Action] | Sitio web | Determina la acción realizada por el Braintree cuando se procesa un pago. Opciones: <br/>**`Authorize`**- Los fondos de la tarjeta del cliente están autorizados, pero no se transfieren desde la cuenta del cliente. Se crea un pedido en el administrador de la tienda. Más tarde puede capturar la venta y crear una factura.<br/>**`Intent Sale`**: el Braintree autoriza y captura los fondos de la tarjeta del cliente, y se crean un pedido y una factura en el administrador de la tienda. **_Nota:_** Esto era `Authorize and Capture` en 2.3.x y versiones anteriores. |
| [!UICONTROL Merchant Name] | Vista de tienda | Etiqueta que se muestra a los clientes en la ventana emergente ApplePay. |
| [!UICONTROL Sort Order] | Sitio web | Determina el pedido en el que Apple Pay aparece junto con otras formas de pago durante el proceso de pago. |

{style="table-layout:auto"}

## [!UICONTROL Local Payment Methods]

![Métodos de pago locales](./assets/payment-methods-braintree-local-payment-config.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enabled Local Payment Methods] | Sitio web | Determina si el método de pago local se incluye como método de pago mediante Braintree. Opciones: `Yes` / `No` |
| [!UICONTROL Title] | Sitio web | Etiqueta que aparece en la sección de método de pago de cierre de compra. Valor predeterminado: `Local Payments` |
| [!UICONTROL Fallback Button Text] | Sitio web | Introduzca el texto que se utilizará para el botón que aparece en la página del Braintree de reserva que lleva a los clientes de vuelta al sitio web. Valor predeterminado: `Complete Checkout` |
| [!UICONTROL Redirect on Fail] | Sitio web | Especifica la dirección URL a la que se debe redirigir a los clientes cuando se cancelan las transacciones de métodos de pago locales, se producen errores o se producen errores. Debe ser la página de pago y envío (por ejemplo, `https://www.domain.com/checkout#payment`). |
| [!UICONTROL Allowed Payment Method] | Sitio web | Seleccione el método de pago local que desea activar. Opciones: `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` (aún no es compatible) |
| [!UICONTROL Sort Order] | Sitio web | Determina el pedido en el que se muestra el Método de pago local con otros métodos de pago durante el cierre de compra. |

{style="table-layout:auto"}

>[!NOTE]
>
>La extensión de Braintree empaquetada no admite todos los métodos de pago locales enumerados en la [documentación de desarrollador de Braintree](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview). Se están desarrollando otros métodos de pago locales que se admitirán en futuras versiones.

## [!UICONTROL GooglePay through Braintree]

![GooglePay mediante Braintree](./assets/payment-methods-braintree-googlepay-config.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enabled GooglePay through Braintree] | Sitio web | Determina si el pago de [!DNL Google Pay] se incluye como una forma de pago a través del Braintree. Opciones: `Yes` / `No` |
| [!UICONTROL Enable Vault for GooglePay] | Sitio web | Los clientes pueden depositar o almacenar su método de pago de Google Pay para uso futuro. Una vez que los datos de pago se han guardado, el cliente puede utilizar Google Pay sin tener que volver a introducir los datos ni volver a autenticar su información de pago. Opciones: `Yes` / `No` |
| [!UICONTROL Payment Action] | Sitio web | Determina la acción realizada por el Braintree cuando se procesa un pago. Opciones: <br/>**`Authorize`**- Los fondos de la tarjeta del cliente están autorizados, pero no se transfieren desde la cuenta del cliente. Se crea un pedido en el administrador de la tienda. Más tarde puede capturar la venta y crear una factura.<br/>**`Intent Sale`**: el Braintree autoriza y captura los fondos de la tarjeta del cliente, y se crean un pedido y una factura en el administrador de la tienda. **_Nota:_** Esto era `Authorize and Capture` en 2.3.x y versiones anteriores. |
| [!UICONTROL Button Color] | Sitio web | Determina el color del botón [!DNL Google Pay]. Opciones: `White` / `Black` |
| [!UICONTROL Merchant ID] | Vista de tienda | El ID proporcionado por Google debe introducirse aquí. |
| [!UICONTROL Accepted Cards] | Sitio web | Seleccione el tipo de tarjetas que puede usar un cliente para realizar un pedido con [!DNL Google Pay]. |
| [!UICONTROL Sort Order] | Sitio web | Determina el pedido en el que Google Pay aparece junto con otras formas de pago durante el proceso de pago. |

{style="table-layout:auto"}

## [!UICONTROL Venmo through Braintree]

![Venmo a través del Braintree](./assets/payment-methods-braintree-venmo-config.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable Venmo through Braintree] | Sitio web | Determina si [!DNL Venmo] se incluye como método de pago mediante Braintree. Opciones: `Yes` / `No` |
| [!UICONTROL Enable Vault for Venmo] | Sitio web | Los clientes pueden depositar su método de pago Venmo para uso futuro. Una vez que los detalles de pago se hayan guardado, el cliente podrá usar el método de pago Venmo sin tener que volver a introducir los datos o volver a autenticar su información de pago. Opciones: `Yes` / `No` |
| [!UICONTROL Payment Action] | Sitio web | Determina la acción realizada por el Braintree cuando se procesa un pago. Opciones: <br/>**`Authorize`**- Los fondos de la tarjeta del cliente están autorizados, pero no se transfieren desde la cuenta del cliente. Se crea un pedido en el administrador de la tienda. Más tarde puede capturar la venta y crear una factura.<br/>**`Intent Sale`**: el Braintree autoriza y captura los fondos de la tarjeta del cliente, y se crean un pedido y una factura en el administrador de la tienda. **_Nota:_** Esto fue _Autorizar y capturar_ en 2.3.x y versiones anteriores. |
| [!UICONTROL Sort Order] | Sitio web | Determina el pedido en el que Venmo aparece junto con otras formas de pago durante el cierre de compra. |

{style="table-layout:auto"}

## [!UICONTROL PayPal through Braintree]

![PayPal a través del Braintree](./assets/payment-methods-braintree-paypal-config.png){width="550" zoomable="yes"}

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable PayPal through Braintree] | Sitio web | Determina si PayPal se incluye como forma de pago a través del Braintree. Opciones: `Yes` / `No` |
| [!UICONTROL Enable PayPal Credit through Braintree] | Sitio web | Determina si el crédito de PayPal se incluye como forma de pago a través del Braintree. Opciones: `Yes` / `No`. Este campo se hace visible cuando `Enable PayPal through Braintree` se establece en `Yes` |
| [!UICONTROL Enable PayPal PayLater through Braintree] | Sitio web | Determina si PayPal PayAfter se incluye como forma de pago a través del Braintree. Opciones: `Yes` / `No`. Este campo se hace visible cuando `Enable PayPal through Braintree` se establece en `Yes` |
| [!UICONTROL Title] | Vista de tienda | La etiqueta que identifica a PayPal a través del Braintree a los clientes durante el cierre de compra. Valor predeterminado: `PayPal` |
| [!UICONTROL Vault Enabled] | Sitio web | Cuando está activada, proporciona almacenamiento seguro para la información de pago del cliente, de modo que los clientes no tienen que volver a introducir su información de PayPal para cada compra. Opciones: `Yes` / `No` |
| [!UICONTROL Send Cart Line Items for PayPal] | Sitio web | Envíe los artículos de línea (artículos de pedido) a PayPal junto con las tarjetas de regalo, el envoltorio para artículos, el envoltorio para regalos para pedidos, el crédito de tienda, el envío y los impuestos como artículos de línea. Opciones: `Yes` / `No` |
| [!UICONTROL Sort Order] | Sitio web | Un número que determina el orden en el que PayPal a través del Braintree aparece junto con otros métodos de pago durante el proceso de pago. |
| [!UICONTROL Override Merchant Name] | Vista de tienda | Un nombre alternativo que se puede usar para identificar al comerciante en cada vista de tienda. |
| [!UICONTROL Payment Action] | Sitio web | Determina la acción realizada por PayPal a través del Braintree cuando se procesa un pago. Opciones: <br/>**`Authorize`**- Los fondos de la tarjeta del cliente están autorizados, pero no se transfieren desde la cuenta del cliente. Se crea un pedido en el administrador de la tienda. Más tarde puede capturar la venta y crear una factura.<br/>**`Authorize and Capture`**: PayPal autoriza y captura los fondos de la tarjeta del cliente a través de Braintree, y se crea un pedido y una factura en el administrador de la tienda. |
| [!UICONTROL Payment from Applicable Countries] | Sitio web | Determina si acepta pagos procesados por PayPal a través de un Braintree de todos los países o solo de países específicos. Opciones: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Sitio web | Si procede, indica los países específicos desde los que acepta pagos procesados por el Braintree. |
| [!UICONTROL Require Customer's Billing Address] | Sitio web | Determina si la dirección de facturación del cliente es necesaria para enviar un pedido. Opciones: `Yes` / `No` |
| [!UICONTROL Debug] | Sitio web | Determina si las comunicaciones entre PayPal a través del sistema de Braintree y su tienda están registradas en un archivo de registro. Opciones: `Yes` / `No` |
| [!UICONTROL Display on Shopping Cart] | Sitio web | Determina si el botón PayPal aparece en el [minicarrito](../../stores-purchase/cart-configuration.md#mini-cart) y en la página del [carro de compras](../../stores-purchase/cart.md). Opciones: `Yes` / `No` |

{style="table-layout:auto"}

>[!NOTE]
>
>Se puede habilitar **[!DNL PayPal Credit]** o **[!DNL PayPal PayLater]**. Ambos métodos no se pueden habilitar al mismo tiempo.

### [!UICONTROL Styling]

![Estilo PayPal](./assets/payment-methods-braintree-paypal-styling.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Location] | Sitio web | Determina dónde se muestran los botones y mensajes de PayPal en la tienda. Opciones: `Mini-Cart and Cart Page` / `Checkout Page` / `Product Page` |

{style="table-layout:auto"}

**[!UICONTROL Mini-Cart and Cart Page]**

La opción y la configuración de esta sección varían según la configuración del campo _[!UICONTROL Location]_.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL PayPal Button Type] | Sitio web | Establece el botón en uno de los tres tipos: `PayPal Button` / `PayPal Pay Later Button` / `PayPal Credit Button` |

**[!UICONTROL PayPal Button]**

Las opciones y la configuración de esta sección varían según el tipo de botón seleccionado en el campo _[!UICONTROL PayPal Button Type]_.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Show PayPal Button] | Sitio web | Determina la ubicación del botón PayPal en la ubicación seleccionada. Opciones: `Yes` / `No` |
| [!UICONTROL Button Label] | Sitio web | Determina la etiqueta del botón PayPal. Opciones: `Paypal` / `Checkout` / `Buy Now` / `Pay` |
| [!UICONTROL Color] | Sitio web | Determina el color del botón PayPal. Opciones: `Blue` / `Black` / `Gold` / `Silver` |
| [!UICONTROL Shape] | Sitio web | Determina la forma del botón PayPal. Opciones: `Pill` / `Rectangle` |
| [!UICONTROL Size(Deprecated)] | Sitio web | Determina el tamaño del botón PayPal. Opciones: `Medium` / `Large` / `Responsive` |

{style="table-layout:auto"}

>[!NOTE]
>
>El campo de configuración **[!DNL Size(Deprecated)]** está obsoleto y no se usa para aplicar estilo a los botones de PayPal.

**[!UICONTROL PayLater Messaging]**

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Show PayLater Messaging] | Sitio web | Activa la mensajería PayAfter en la ubicación seleccionada. Opciones: `Yes` / `No`. Cuando está habilitado, muestra mensajes de PayAfter para las ofertas disponibles ([se aplican restricciones](https://developer.paypal.com/docs/checkout/pay-later/us/)). |
| [!UICONTROL Message Layout] | Sitio web | Determina el diseño del mensaje Paylater. Opciones: `Text` / `Flex` |
| [!UICONTROL Logo] | Sitio web | Determina el tipo de logotipo utilizado para el botón PayPal. Opciones: `Inline` / `Primary` / `Alternative` / `None` |
| [!UICONTROL Logo Position] | Sitio web | Determina la posición del logotipo del botón PayPal. Opciones: `Left` / `Right` / `Top` |
| [!UICONTROL Text Color] | Sitio web | Determina el color de texto del botón PayPal. Opciones: `Black` / `White` / `Monochrome` / `Grayscale` |

{style="table-layout:auto"}

Cuando estas opciones están definidas, puedes ver la vista previa de los botones de PayPal y los mensajes de PayAfter. Hay controles que puede utilizar para aplicar la configuración o restablecer los valores:

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Apply] | Sitio web | Almacena la configuración de estilo seleccionada para los botones y la mensajería PayAfter y los aplica a la ubicación y el tipo de botón actuales. |
| [!UICONTROL Apply to All Buttons] | Sitio web | Almacena la configuración de estilo seleccionada para los valores de botones y mensajes de PayAfter y los aplica a todos los tipos y ubicaciones de botones. |
| [!UICONTROL Reset to Recommended Defaults] | Sitio web | Devuelve la configuración de estilo a los valores predeterminados recomendados para los botones y la mensajería PayAfter y los aplica a todos los tipos y ubicaciones de botones. |

{style="table-layout:auto"}

## Configuración de verificación de seguridad 3d

![Configuración de verificación segura en 3D](./assets/payment-methods-braintree-3d-secure-verify-config.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL 3D Secure Verification] | Sitio web | Determina si una transacción debe pasar un proceso de verificación adicional cuando el cliente está inscrito en un programa como _Verificado por VISA_. Opciones: `Yes` / `No` |
| [!UICONTROL Always request 3DS] | Sitio web | Desafíe la petición 3D Secure siempre para todas las transacciones. Opciones: `Yes` / `No` |
| [!UICONTROL Threshold Amount] | Sitio web | Determina la cantidad de pedido máxima autorizada para procesar en un único pedido. El Braintree rechaza la autorización si el importe del pedido supera este umbral. |
| [!UICONTROL Verify for Applicable Countries] | Sitio web | Determina los países en los que se debe comprobar el pago. Opciones: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Verify for Specific Countries] | Sitio web | Si procede, indica los países específicos desde los que debe verificarse el pago por parte del Braintree. |

{style="table-layout:auto"}

## [!UICONTROL Dynamic Descriptors]

![Descriptores dinámicos](./assets/payment-methods-braintree-dynamic-config.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Name] | Vista de tienda | El descriptor Nombre consta de dos partes, separadas por un asterisco (*). La primera parte del descriptor identifica la compañía o DBA y la segunda parte identifica el producto. Por ejemplo: `company*myproduct` <br/><br/>La longitud de las partes Empresa y Producto del descriptor se puede asignar de las siguientes maneras, para una longitud combinada de hasta 22 caracteres: <br/>**`Option 1`**- La compañía debe tener tres caracteres / El producto puede tener hasta 18 caracteres<br/>**`Option 2`** - La compañía debe tener siete caracteres / El producto puede tener hasta 14 caracteres <br/>**`Option 3`**- La compañía debe tener 12 caracteres / El producto puede tener hasta nueve caracteres |
| [!UICONTROL Phone] | Vista de tienda | El descriptor de teléfono debe tener entre diez y 14 caracteres de longitud y solo puede incluir números, guiones, paréntesis y puntos. Por ejemplo: `9999999999` `(999) 999-9999` `999.999.9999` |
| [!UICONTROL URL] | Vista de tienda | El descriptor de URL representa su nombre de dominio y puede contener hasta 13 caracteres. Por ejemplo: `company.com` |

{style="table-layout:auto"}
