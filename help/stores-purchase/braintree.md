---
title: Braintree
description: Aprenda a configurar Braintree como una solución de pago en línea en su tienda.
exl-id: 781b385f-926e-4047-b7da-6f7c090d75d8
feature: Payments
source-git-commit: bb083698aff1da145bbb661307148c9223d5b545
workflow-type: tm+mt
source-wordcount: '2873'
ht-degree: 0%

---

# Braintree

>[!IMPORTANT]
>
>Si necesita ayuda con cargos inesperados en su tarjeta, visita la Página cancelar suscripción [&#128279;](https://helpx.adobe.com/manage-account/using/cancel-subscription.html) para obtener ayuda.

Braintree ofrece un experiencia de pago totalmente personalizable con detección de fraude e integración PayPal. Es compatible con [!DNL Apple Pay], [!DNL Google Pay], ACH, Venmo y métodos de pago locales. Braintree reduce la carga de cumplimiento PCI para los comerciantes porque la transacción se realiza en el sistema Braintree. La integración de Braintree Payments es desarrollada por [GENE Commerce](https://www.gene.co.uk/gene-braintree-payments/).

>[!NOTE]
>
>Si está actualizando a la versión 2.4.x desde una versión anterior de Adobe Commerce o Magento Open Source con la extensión Braintree de Commerce Marketplace instalada, consulte las [notas de actualización 2.4](#24-upgrade-notes) al final de esta página.


## Paso 1: Consiga sus credenciales de Braintree

Vaya a [Braintree Payments][1] y regístrese para obtener una cuenta.

## Paso 2: completar la configuración básica

1. En la barra lateral _Administración_ , ve a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Payment Methods]**.

   - Si la instalación de Commerce tiene varios sitios web, tiendas o vistas, elija **[!UICONTROL Store View]** en la esquina superior izquierda donde se aplica la configuración.

   - En la sección _[!UICONTROL Merchant Location]_, compruebe que **[!UICONTROL Merchant Country]**&#x200B;está establecido en la ubicación de su empresa.

1. En _[!UICONTROL Recommended Solutions]_, en la sección_[!UICONTROL Braintree Payments] (por [GENE Commerce](https://www.gene.co.uk/gene-braintree-payments/) v4.7.0 - [Notas de la versión](https://support.gene.co.uk/support/solutions/articles/35000278668)_, haga clic en **[!UICONTROL Configure]**.

   ![Configurar Braintree](./assets/braintree-payments.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Title]**, escribe un título que identifique a Braintree como una opción de pago durante el cierre de compra.

1. Establecer **[!UICONTROL Environment]** operativo actual para las transacciones de Braintree en `Sandbox` o `Production`

   Al probar la configuración en una zona protegida, use solamente [números de tarjeta de crédito][2] recomendados por Braintree. Cuando esté listo para ir a producción con Braintree, establezca **[!UICONTROL Environment]** en `Production`.

   ![Configuración de credenciales básicas](../configuration-reference/sales/assets/payment-methods-braintree-basic-config.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Payment Action]** en una de las siguientes opciones:

   - `Authorize Only` - Aprueba la compra y suspende los fondos. El importe no se retira de la cuenta bancaria del cliente hasta que el comerciante _capture_ la venta.|
   - `Intent Sale`: el importe de la compra se autoriza y se retira inmediatamente de la cuenta del cliente. **_Nota:_** Este valor era _Autorizar y capturar_ en 2.3.x y versiones anteriores.|

1. Escriba **[!UICONTROL Sandbox Merchant ID / Merchant ID]** desde su cuenta de Braintree.

1. Introduzca las siguientes credenciales de su cuenta de Braintree:

   - **[!UICONTROL Sandbox Public Key / Public Key]**
   - **[!UICONTROL Sandbox Private Key / Private Key]**

   >[!NOTE]
   >
   >Hay campos independientes para los entornos **(espacio aislado y producción)**, y los demás campos se representan en función del entorno seleccionado.

1. Antes de guardar la configuración, haga clic en **[!UICONTROL Validate Credentials]** para validar las credenciales.

1. Establezca **[!UICONTROL Enable Card Payments]** en `Yes`.

1. Si desea poder almacenar la información de los clientes de forma segura, de modo que los clientes no tengan que volver a introducirla cada vez que realicen una compra, establezca **[!UICONTROL Enable Vault for Card Payments]** en `Yes`.

1. Si desea que un cliente verifique el número CVV de su tarjeta abovedada en cada compra, establezca **[!UICONTROL Enable Vault CVV Re-verification]** en `Yes`.

## Paso 3: Completar la configuración avanzada

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Advanced Braintree Settings]**.

   ![Advanced Settings](../configuration-reference/sales/assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

1. For **[!UICONTROL Vault Title]**, enter a descriptive title for your reference that identifies the vault where your customer card information is stored.

1. Enter the **[!UICONTROL Merchant Account ID]** from your Braintree account.

   If you don&#39;t specify the merchant account to be used, Braintree processes the transaction using your default merchant account.

1. Para ofrecer una experiencia de pago y envío más rápida con las opciones de Pago exprés al comienzo del proceso de pago, incluidas PayPal, PayAfter, Apple Pay y Google Pay, establezca **[!UICONTROL Enable Checkout Express Payments]** en `Yes`.

1. Si desea evitar que la transacción se envíe para su evaluación como parte de las comprobaciones de las herramientas de fraude avanzado, en los pedidos realizados a través del administrador, establezca **[!UICONTROL Skip Fraud Checks on Admin Orders]** en `Yes`.

1. Establezca **[!UICONTROL Bypass Fraud Protection Threshold]** de modo que se omitan las comprobaciones `Advanced Fraud Protection` cuando se alcance o supere el umbral.

   Si deja este campo en blanco, se deshabilita esta opción.

1. Si desea que el sistema guarde un archivo de registro de interacciones entre su tienda y Braintree, establezca **[!UICONTROL Debug]** en `Yes`.

1. Para exigir a los clientes que proporcionen el código de seguridad de tres dígitos del reverso de una tarjeta de crédito, establezca **[!UICONTROL CVV Verification]** en `Yes`.

   Si usas la verificación CVV, asegúrate de habilitar AVS y/o CVV en la sección _Configuración/Procesamiento_ de tu cuenta de Braintree.

1. Para enviar los elementos de línea de carro de compras para todos los métodos de pago, establezca **[!UICONTROL Send Card Line Items]** en `Yes`.

1. Para **[!UICONTROL Credit Card Types]**, selecciona cada tarjeta de crédito que tu tienda acepte como pago a través de Braintree.

   Para seleccionar varios tipos de tarjetas, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

1. Para **[!UICONTROL Sort Order]**, introduce un número para determinar la secuencia en la que Braintree aparece cuando aparece junto con otros métodos de pago durante el cierre de compra.

## Paso 4: Completar la configuración del webhook de Braintree

![Configuración de Webhooks de Braintree](../configuration-reference/sales/assets/payment-methods-braintree-webhooks-config.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Enable Webhook]** en `Yes` para habilitar la funcionalidad de webhook para la protección contra fraudes, pagos ACH y métodos de pago locales.

1. Copie la dirección URL en el campo **[!UICONTROL Fraud Protection URL]** y agréguela a su cuenta de Braintree como _[!UICONTROL Webhook Destination URL]_.

   >[!IMPORTANT]
   >
   >Esta URL debe ser segura y accesible públicamente.

1. Establezca el campo **[!UICONTROL Fraud Protection Approve Order Status]** para determinar cuándo Braintree aprueba la protección contra el fraude.

   El estado del pedido seleccionado se asigna al pedido de Commerce.

1. Establezca el campo **[!UICONTROL Fraud Protection Reject Order Status]** para determinar cuándo Braintree rechaza la protección contra el fraude.

   El estado del pedido seleccionado se asigna al pedido de Commerce.

## Paso 5: Completar la configuración específica de un país

1. Establezca **[!UICONTROL Payment from Applicable Countries]** en una de las siguientes opciones:

   - `All Allowed Countries`: los clientes de todos los [países](../getting-started/store-details.md#country-options) especificados en la configuración de su tienda pueden usar este método de pago.
   - `Specific Countries` - Después de elegir esta opción, aparece la lista _[!UICONTROL Payment from Specific Countries]_. Mantén pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y selecciona cada país de la lista donde los clientes pueden realizar compras desde tu tienda.

   ![Configuración específicos por país](../configuration-reference/sales/assets/payment-methods-braintree-country-specific-config.png){width="600" zoomable="yes"}

1. Para configurar **[!UICONTROL Country Specific Credit Card Types]**:

   - Haga clic en **[!UICONTROL Add]**.

   - Establezca **[!UICONTROL Country]** y elija cada **[!UICONTROL Allowed Credit Card Type]**.

   - Repita el proceso para identificar las tarjetas de crédito que se aceptan en cada país.

## Paso 6: Completar la ACH mediante la configuración de Braintree

![ACH mediante Braintree](../configuration-reference/sales/assets/payment-methods-braintree-ach-config.png){width="600" zoomable="yes"}

1. Para incluir ACH como opción de pago con Braintree, establezca **[!UICONTROL Enable ACH Direct Debit]** en `Yes`.

1. Los clientes pueden almacenar su método de pago de débito directo ACH de un solo uso y tienda para su uso futuro. Una vez almacenado, los clientes pueden reutilizar el débito directo ACH sin necesidad de volver a ingresar o autenticar su información de pago si está configurado **[!UICONTROL Enable Vault for ACH Direct Debit]** en `Yes`.

1. Para **[!UICONTROL Sort Order]**, ingrese un número para determinar la Secuencia en la que aparece la opción de pago Braintree ACH cuando aparece junto con otras opciones de pago durante el proceso de pago.

## Paso 7: completar [!UICONTROL Apple Pay] mediante la configuración de Braintree

![Configuración de ApplePay mediante Braintree](../configuration-reference/sales/assets/payment-methods-braintree-applepay-config.png){width="600" zoomable="yes"}

1. Para incluir [!DNL Apple Pay] como opción de pago con Braintree, establezca **[!UICONTROL Enable ApplePay through Braintree]** en `Yes`.

   Asegúrate de [comprobar primero tu nombre de dominio](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3) en tu cuenta de Braintree.

1. Si desea poder almacenar la información de los clientes de forma segura, de modo que los clientes no tengan que volver a introducirla cada vez que realicen una compra con Apple Pay, establezca **[!UICONTROL Enable Vault for ApplePay]** en `Yes`.

1. Establezca **[!UICONTROL Payment Action]** en una de las siguientes opciones:

   - `Authorize Only` - Aprueba la compra y suspende los fondos. La cantidad no se retira de la cuenta bancaria del cliente hasta que el comerciante _capture_ la venta.
   - `Intent Sale`: el importe de la compra se autoriza y se retira inmediatamente de la cuenta del cliente.

1. Para **[!UICONTROL Merchant Name]**, escriba un texto que especifique la etiqueta que se mostrará a los clientes en el cuadro de diálogo Apple Pay.

1. Para **[!UICONTROL Sort Order]**, escriba un número para determinar la secuencia en la que aparece la opción de pago [!DNL Apple Pay] cuando se enumera con otras opciones de pago durante el cierre de compra.

## Paso 8: Completa la configuración de los métodos de pago locales

1. Para incluir métodos de pago locales como opción de pago con Braintree, establezca **[!UICONTROL Enable Local Payment Methods]** en `Yes`.

1. Para **[!UICONTROL Title]**, escriba el texto que se usará para la etiqueta que aparece en la sección de método de pago de pago (valor predeterminado: `Local Payments`).

1. Para **[!UICONTROL Fallback Button Text]**, escriba el texto que se usará para el botón que aparece en la página de reserva de Braintree para devolver al cliente al sitio web (por ejemplo, `Complete Checkout`).

1. Para **[!UICONTROL Redirect on Fail]**, escriba la dirección URL a la que se debe redirigir a los clientes cuando se cancelen, fallen o encuentren errores en las transacciones de métodos de pago locales. Debe ser la página de pago y envío (por ejemplo, `https://www.domain.com/checkout#payment`).

1. Para **[!UICONTROL Allowed Payment Methods]**, selecciona el método de pago local que se habilitará.

   Opciones: `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` (aún no es compatible)

   ![Configuración de métodos de pago locales](../configuration-reference/sales/assets/payment-methods-braintree-local-payment-config.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >La extensión agrupada de Braintree no admite todos los métodos de pago locales enumerados en la [documentación para desarrolladores de Braintree](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview). Se están desarrollando otros métodos de pago locales que se admitirán en futuras versiones.

1. Para **[!UICONTROL Sort Order]**, escribe un número para determinar la secuencia en la que aparece el método de pago local cuando se enumera con otras opciones de pago durante el cierre de compra.

## Paso 9: Completar [!DNL Google Pay] mediante la configuración de Braintree

![Google Pay mediante Braintree](../configuration-reference/sales/assets/payment-methods-braintree-googlepay-config.png){width="600" zoomable="yes"}

1. Para incluir [!DNL Google Pay] como opción de pago con Braintree, establezca **[!UICONTROL Enable GooglePay Through Braintree]** en `Yes`.

1. Si desea poder almacenar la información de los clientes de forma segura, de modo que los clientes no tengan que volver a introducirla cada vez que realicen una compra con Google Pay, establezca **[!UICONTROL Enable Vault for GooglePay]** en `Yes`.

1. Establezca **[!UICONTROL Payment Action]** en una de las siguientes opciones:

   - `Authorize Only` - Aprueba la compra y suspende los fondos. La cantidad no se retira de la cuenta bancaria del cliente hasta que el comerciante _capture_ la venta.
   - `Intent Sale`: el importe de la compra se autoriza y se retira inmediatamente de la cuenta del cliente.

1. Establezca **[!UICONTROL Button Color]** para determinar el color del botón [!DNL Google Pay]: `White` o `Black`

1. Para **[!UICONTROL Merchant ID]**, ingrese su MerchantID (proporcionado por Google).

1. Para **[!UICONTROL Accepted Cards]**, seleccione el tipo de tarjetas que un cliente puede usar para realizar un pedido con [!DNL Google Pay].

   Opciones: `Visa` / `MasterCard` / `AMEX` / `Discover` / `JCB`

1. Para **[!UICONTROL Sort Order]**, escriba un número para determinar la secuencia en la que [!DNL Google Pay] aparece cuando se enumera con otras opciones de pago durante el cierre de compra.

## Paso 10: Completar Venmo a través de la configuración de Braintree

1. Para incluir Venmo como opción de pago con Braintree, establezca **[!UICONTROL Enable Venmo through Braintree]** en `Yes`.

1. Establezca **[!UICONTROL Enable Vault for Venmo]** en `Yes` para habilitar el uso de un almacén seguro para almacenar la cuenta de Venmo de los clientes, de modo que los clientes no tengan que volver a iniciar sesión en su cuenta de Venmo para futuras transacciones.

   ![Venmo a través de Braintree](../configuration-reference/sales/assets/payment-methods-braintree-venmo-config.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Payment Action]** en una de las siguientes opciones:

   - `Authorize Only` - Aprueba la compra y suspende los fondos. La cantidad no se retira de la cuenta bancaria del cliente hasta que el comerciante _capture_ la venta.
   - `Intent Sale`: el importe de la compra se autoriza y se retira inmediatamente de la cuenta del cliente.

1. Para **[!UICONTROL Sort Order]**, ingrese un número para determinar la secuencia en la que Venmo aparece cuando se enumera con otras opciones de pago durante el cierre de compra.

## Paso 11: Completa la configuración de PayPal mediante Braintree

![PayPal a través de la configuración de Braintree 1](../configuration-reference/sales/assets/payment-methods-braintree-paypal-config-1.png){width="550" zoomable="yes"}

1. Para incluir PayPal como una opción de pago con Braintree, establece **[!UICONTROL Enable PayPal through Braintree]** en `Yes`.

1. Especifica tu forma de pago con PayPal mediante Braintree:

   >[!NOTE]
   >
   >Se puede habilitar **[!DNL PayPal Credit]** o **[!DNL PayPal PayLater]**. Ambos métodos no se pueden habilitar al mismo tiempo.

   - Para incluir [!DNL PayPal Credit] como opción de pago con Braintree, establezca **[!UICONTROL Enable PayPal Credit through Braintree]** en `Yes`.

     Cuando **la opción Habilitar PayPal a través de Braintree** está establecida en `Yes`, solo aparece este campo.

     >[!NOTE]
     >
     >PayPal crédito solo está disponible en los Estados Unidos y el Reino Unido. PayPal crédito se desactiva si el valor seleccionado para el _[!UICONTROL Merchant Country]_&#x200B;campo no `US` es o `UK`.

   - Para incluir [!DNL PayPal PayLater] como opción de pago con Braintree, establezca en **[!UICONTROL Enable PayPal PayLater through Braintree]** `Yes`.

     Cuando **[!UICONTROL Enable PayPal PayLater through Braintree]** se establece en `Yes`, solo aparece este campo.

     Puede mostrar la mensajería PayAfter en su sitio para ofertas como _Pagar en 3_, que permite a los clientes pagar con tres pagos mensuales sin intereses. La integración de Braintree puede mostrar mensajes en el sitio para promocionar esta función. No puede promocionar ofertas de PayAfter con ningún otro contenido, marketing o materiales.

1. Para **[!UICONTROL Title]**, escribe un título que identifique la opción de pago por PayPal de Braintree durante el proceso de pago y envío.

1. Establece **[!UICONTROL Vault Enabled]** en `Yes` para habilitar el uso de un almacén seguro para almacenar la cuenta PayPal de los clientes. La cuenta PayPal abovedada se puede utilizar para transacciones futuras, lo que reduce el número de pasos para los clientes.

1. Configúrelo **[!UICONTROL Send Cart Line Items for PayPal]** para `Yes` enviar los elementos de línea (artículos del pedido) a PayPal junto con las tarjetas de regalo, el envoltorio para regalos para artículos, el envoltorio para regalos para pedidos, el crédito de la tienda, el envío y los impuestos como elementos de línea.

1. Para **[!UICONTROL Sort Order]**, ingrese un número para determinar la Secuencia en la que aparece la opción de pago PayPal Braintree cuando aparece junto con otras opciones de pago durante el cierre de compra.

1. Para mostrar el nombre del comerciante de forma distinta a la definida en la [configuración de tienda](../getting-started/store-details.md#store-information), escriba el nombre en el campo **[!UICONTROL Override Merchant Name]** tal como desea que aparezca.

1. Establezca **[!UICONTROL Payment Action]** en una de las siguientes opciones:

   - `Authorize Only` - Aprueba la compra y suspende los fondos. La cantidad no se retira de la cuenta bancaria del cliente hasta que el comerciante _capture_ la venta.
   - `Authorize and Capture`: el importe de la compra se autoriza y se retira inmediatamente de la cuenta del cliente.

1. Establezca **[!UICONTROL Payment from Applicable Countries]** en una de las siguientes opciones para las transacciones de Braintree procesadas por PayPal:

   - `All Allowed Countries`: los clientes de todos los [países](../getting-started/store-details.md#country-options) especificados en la configuración de su tienda pueden usar este método de pago.
   - `Specific Countries` - Después de elegir esta opción, aparece la lista _[!UICONTROL Payment from Specific Countries]_. Mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y seleccione cada país de la lista donde los clientes pueden realizar compras en su tienda.

   ![PayPal a través de la configuración de Braintree 2](../configuration-reference/sales/assets/payment-methods-braintree-paypal-config-2.png){width="550" zoomable="yes"}

1. Para requerir que los clientes proporcionen una dirección de facturación, establezca **[!UICONTROL Require Customer's Billing Address]** en `Yes`.

   >[!NOTE]
   >
   >Asistencia técnica de PayPal debe activar esta función en tu cuenta.

1. Para omitir la página de revisión de pedidos de PayPal Express, establezca **[!UICONTROL Skip Order Review Step]** en `Yes`.

   For customers paying with PayPal Express: If you want customers to be redirected to a review page before completing payment, set this to `No`. If you&#39;d prefer customers to skip the review page, set it to `Yes`.

1. To save a log file of interactions between your store and PayPal through Braintree, set **[!UICONTROL Debug]** to `Yes`.

1. To display the PayPal button on both the mini cart and shopping cart page, set **[!UICONTROL Display on Shopping Cart]** to `Yes`.

1. To send package tracking information to PayPal, set **[!UICONTROL Send Package Tracking]** to `Yes`.

   Package tracking information will be sent to PayPal for PayPal transactions/orders only. Debe habilitar el campo de configuración [!UICONTROL Send Cart Line Items for PayPal] para que la característica [!UICONTROL Package Tracking] funcione correctamente.

1. Para notificar a un comprador o pagador por PayPal de las actualizaciones de seguimiento de paquetes, establece **[!UICONTROL Use PayPal's "Notify Payer" functionality]** en `Yes`.

## Paso 12: Establecer la configuración de estilo

1. Para **[!UICONTROL Location]**, elija dónde se representan los botones y los mensajes de PayPal: `Mini-Cart and Cart Page`, `Checkout Page` o `Product Page`

   ![Configuración de estilo de PayPal](../configuration-reference/sales/assets/payment-methods-braintree-paypal-styling.png){width="600" zoomable="yes"}

### [!UICONTROL Mini-Cart and Cart Page]

Las opciones y la configuración de esta sección varían según la configuración del campo _[!UICONTROL Location]_.

1. Establezca **[!UICONTROL PayPal Button Type]** en uno de los tres tipos de botones: `PayPal Button` / `PayPal Pay Later Button` / `PayPal Credit Button`

**[!UICONTROL PayPal Button]**

Las opciones y la configuración de esta sección varían según el tipo de botón seleccionado en el campo _[!UICONTROL PayPal Button Type]_.

1. Para mostrar el botón PayPal en la tienda de la ubicación seleccionada, establece **[!UICONTROL Show PayPal Button]** en `Yes`.

1. Para **[!UICONTROL Button Label]**, selecciona la etiqueta de botón PayPal: `Paypal`, `Checkout`, `Buynow` o `Pay`

1. Para **[!UICONTROL Color]**, selecciona el color del botón de PayPal: `Blue`, `Black`, `Gold` o `Silver`

1. Para **[!UICONTROL Shape]**, seleccione la forma de botón PayPal: `Pill` o `Rectangle`

1. Para **[!UICONTROL Size (Deprecated)]**, selecciona el tamaño del botón PayPal: `Medium`, `Large` o `Responsive`

>[!NOTE]
>
>El campo de configuración **[!DNL Size(Deprecated)]** está obsoleto y no se usa para aplicar estilo a los botones de PayPal.

Cuando estas opciones están definidas, puedes ver la vista previa de los botones de PayPal. Hay controles que puede utilizar para aplicar la configuración o restablecer los valores:

- Para almacenar la configuración de estilo seleccionada para los botones y la mensajería PayAfter y aplicarla a la ubicación actual y al tipo de botón actual, haga clic en **[!UICONTROL Apply]**.

- Para almacenar la configuración de estilo seleccionada para los valores de botones y mensajes de PayAfter y aplicarlos a todos los tipos y ubicaciones de botones, haga clic en **[!UICONTROL Apply to All Buttons]**.

- Para devolver la configuración de estilo a los valores predeterminados recomendados para los botones y la mensajería PayAfter y aplicarlos a todos los tipos y ubicaciones de botones, haga clic en **[!UICONTROL Reset to Recommended Defaults]**.

## Paso 13: Pagar más tarde por mensajería

**[!UICONTROL Product Page]**

![Mensaje de pago posterior - Configuración de la página del producto](../configuration-reference/sales/assets/payment-methods-braintree-paylater-messaging-product.png){width="600" zoomable="yes"}

1. Para mostrar mensajes de [!DNL Pay Later] en la tienda de la página de productos, establezca **[!UICONTROL Show PayLater Messaging]** en `Yes`.

   Muestra la mensajería Pagar más tarde para las ofertas disponibles. Se aplican restricciones. Ver [documentación de PayPal](https://developer.paypal.com/studio/checkout/pay-later/us).

1. Para **[!UICONTROL Message Layout]**, seleccione el diseño de mensaje [!DNL Pay Later]: `Text` o `Flex`

1. Para **[!UICONTROL Logo]**, seleccione el tipo de logotipo de PayPal: `Inline`, `Primary`, `Alternative` o `None`

1. Para **[!UICONTROL Logo Position]**, selecciona la posición del logotipo de PayPal: `Left`, `Right` o `Top`

1. Para **[!UICONTROL Text Color]**, seleccione el color de texto del mensaje [!DNL PayLater]: `Black`, `White`, `Monochrome` o `Grayscale`

**[!UICONTROL Cart]**

![Mensaje de pago posterior - Configuración de la página del carro de compras](../configuration-reference/sales/assets/payment-methods-braintree-paylater-messaging-cart.png){width="600" zoomable="yes"}

1. Para mostrar mensajes de [!DNL Pay Later] en la tienda en la página del minicarrito o el carrito, establezca **[!UICONTROL Show PayLater Messaging]** en `Yes`.

   Muestra la mensajería Pagar más tarde para las ofertas disponibles. Se aplican restricciones. Ver [documentación de PayPal](https://developer.paypal.com/studio/checkout/pay-later/us).

1. Para **[!UICONTROL Message Layout]**, seleccione el diseño de mensaje [!DNL Pay Later]: `Text` o `Flex`

1. Para **[!UICONTROL Logo]**, seleccione el tipo de logotipo PayPal: `Inline`, `Primary`, `Alternative`, o `None`

1. Para **[!UICONTROL Logo Position]**, seleccione la posición del logotipo PayPal: `Left`, `Right`o `Top`

1. Para **[!UICONTROL Text Color]**, seleccione el color del texto del [!DNL PayLater] mensaje: `Black`, `White`, `Monochrome`, o `Grayscale`

**[!UICONTROL Checkout]**

![Pagar más tarde Enviar mensaje: configuración del Página de cierre de compra](../configuration-reference/sales/assets/payment-methods-braintree-paylater-messaging-checkout.png){width="600" zoomable="yes"}

1. Para mostrar mensajes de [!DNL Pay Later] en la tienda al finalizar la compra, establece **[!UICONTROL Show PayLater Messaging]** en `Yes`.

   Muestra la mensajería Pagar más tarde para las ofertas disponibles. Se aplican restricciones. Ver [documentación de PayPal](https://developer.paypal.com/studio/checkout/pay-later/us).

1. Para **[!UICONTROL Text Align]**, seleccione la alineación de texto para el mensaje [!DNL Pay Later]: `Text`, `Center` o `Right`

1. For **[!UICONTROL Text Color]**, select the [!DNL Pay Later] message text color: `Black`, `White`

## Step 14: Complete the 3D verification settings

1. If you want to add a verification step for customers using credit cards that are enrolled in a verification program (such as _Verified by VISA_), set **[!UICONTROL 3D Secure Verification]** to `Yes`.

   During the process, the transaction amount that is submitted for verification is checked against the amount that is sent for authorization.

2. To always challenge the 3D Secure request for all transactions, set **[!UICONTROL Always request 3DS]** to `Yes`.

3. Para **[!UICONTROL Threshold Amount]**, introduzca la cantidad mínima de pedido necesaria para almacenar en déclencheur la verificación 3D.

4. Establezca **[!UICONTROL Verify for Applicable Countries]** en una de las siguientes opciones:

   - `All Allowed Countries` - Customers from all [countries](../getting-started/store-details.md#country-options) specified in your store configuration can use this payment method.
   - `Specific Countries` - After choosing this option, the _[!UICONTROL Verify for Specific Countries]_&#x200B;list appears. Hold down the Ctrl key (PC) or the Command key (Mac) and select each country in the list where customers can make purchases from your store.

   ![Configuración de verificación 3D](../configuration-reference/sales/assets/payment-methods-braintree-3d-secure-verify-config.png){width="600" zoomable="yes"}

## Paso 15: Configurar los descriptores dinámicos de Braintree

Los siguientes descriptores se utilizan para identificar compras en extractos de tarjetas de crédito de clientes. Puede reducir el número de recargos identificando claramente la empresa asociada con cada compra. Si los descriptores dinámicos no están habilitados para su cuenta, póngase en contacto con el soporte de Braintree.

![Descriptores dinámicos](../configuration-reference/sales/assets/payment-methods-braintree-dynamic-config.png){width="600" zoomable="yes"}

1. Enter the dynamic descriptor for the **[!UICONTROL Name]**, **[!UICONTROL Phone]**, and **[!UICONTROL URL]** according to these guidelines:

   - **[!UICONTROL Name]** - There are two parts to the name descriptor, which are separated by an asterisk (*). Por ejemplo:

     `company*myproduct`

     The first part of the descriptor identifies the company or DBA, and the second part identifies the product. The length of the `company` and `product` parts of the descriptor can be allocated in the following ways, for a combined length of up to 22 characters.

     **_Characters in name descriptor_**

     _Opción 1:_ `Company` debe tener tres caracteres, `Product` puede tener hasta 18 caracteres

     _Opción 2:_ `Company` debe tener siete caracteres, `Product` puede tener hasta 14 caracteres

     _Opción 3_: `Company` debe tener 12 caracteres, `Product` puede tener hasta nueve caracteres

   - **[!UICONTROL Phone]**: el descriptor de teléfono debe tener entre 10 y 14 caracteres de longitud y solo puede incluir números, guiones, paréntesis y puntos. Por ejemplo:

     `9999999999`

     `(999) 999-9999`

     `999.999.9999`

   - **[!UICONTROL URL]**: el descriptor de URL representa su nombre de dominio y puede contener hasta 13 caracteres. Por ejemplo:

     `company.com`

1. Una vez completada la configuración de Braintree, haga clic en **[!UICONTROL Save Config]**.

## Notas de la actualización de 2.4

A partir de Adobe Commerce y Magento Open Source 2.4.0, la extensión de Braintree se incluye en la versión. Si está migrando a Commerce 2.4.x desde una versión anterior a la 2.4.0 que tenga instalada la extensión de Marketplace Braintree, debe desinstalar esa extensión (`paypal/module-braintree` o `gene/module-braintree`) y actualizar las personalizaciones de código para utilizar el espacio de nombres `PayPal_Braintree` en lugar de `Magento_Braintree`. Los ajustes de configuración de la extensión principal del paquete Commerce Braintree Payments y la extensión distribuida en Commerce Marketplace persisten y los pagos realizados con esas versiones anteriores se pueden capturar, anular o reembolsar como de costumbre.

[1]: https://www.braintreepayments.com/
[2]: https://developers.braintreepayments.com/reference/general/testing/php
