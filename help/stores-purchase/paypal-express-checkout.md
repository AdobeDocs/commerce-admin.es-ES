---
title: Pago y envío con PayPal Express
description: Aprenda a configurar el Pago y envío de PayPal Express como una solución de pago en línea en su tienda.
exl-id: 0cd90306-cf47-4a5f-8994-6ae96904ae2f
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '3113'
ht-degree: 0%

---

# Pago y envío con PayPal Express

PayPal Express Checkout ayuda a aumentar las ventas al ofrecer a tus clientes la posibilidad de pagar con tarjeta de crédito o desde la seguridad de sus cuentas personales de PayPal. Durante el proceso de pago y envío, se redirige al cliente al sitio seguro de PayPal para que complete la información de pago. A continuación, el cliente se devuelve a su tienda para completar el resto del proceso de pago. Al elegir Pago y envío exprés, se agrega el conocido botón PayPal a tu tienda, que se ha informado que aumenta las ventas.

>[!IMPORTANT]
>
>**Requisitos de PSD2:** <br/>
>A partir del 14 de septiembre de 2019, los bancos europeos podrían rechazar los pagos que no cumplan [PSD 2](../getting-started/compliance-payment-services-directive.md) requisitos. PayPal Express Checkout no necesita realizar ninguna acción para cumplir con PSD2 porque PayPal gestiona todos los requisitos.

Los clientes con cuentas PayPal actuales pueden realizar una compra en un solo paso haciendo clic en _[!UICONTROL Check out with PayPal]_botón. El Pago y envío exprés puede utilizarse como solución independiente o con una de las soluciones todo en uno de PayPal. Si ya aceptas tarjetas de crédito en línea, puedes ofrecer el Pago Exprés como una opción extra para atraer nuevos clientes que prefieran pagar con PayPal.

>[!NOTE]
>
>PayPal tiene compatibilidad obsoleta con la venta de productos digitales a través del proceso de pago y envío de PayPal Express y recomienda que utilice cualquiera de estas opciones [PayPal Payments Standard](paypal-payments-standard.md) u otra pasarela de pago de PayPal para procesar cualquier pedido que incluya [productos virtuales](../catalog/product-create-virtual.md).

## Requisitos

- Comerciante: [Cuenta PayPal empresarial][1]
- Cliente: [Cuenta personal de PayPal][2]

## Flujo de trabajo de cierre rápido

A diferencia de otras formas de pago, PayPal Express Checkout permite al cliente realizar el check out al principio del flujo de trabajo de checkout habitual desde la página del producto, el mini cart y el carrito de compra.

1. **El cliente realiza un pedido** - El cliente hace clic o pulsa el botón _[!UICONTROL Check out with PayPal]_botón.
1. **Se redirige al cliente al sitio de PayPal** - Se redirige al cliente al sitio de PayPal para completar la transacción.
1. **El cliente inicia sesión en su cuenta PayPal** - El cliente debe iniciar sesión en su cuenta PayPal para completar la transacción. El sistema de pago utiliza la información de facturación y envío de su cuenta PayPal.
1. **El cliente vuelve a la página de cierre de compra** - Se redirige al cliente a la página de cierre de compra de su tienda para revisar el pedido.
1. **El cliente realiza un pedido** - El cliente realiza el pedido y la información del pedido se envía a PayPal.
1. **PayPal cancela la transacción** - PayPal recibe el pedido y liquida la transacción.

>[!NOTE]
>
>PayPal Express Checkout no admite pedidos con direcciones múltiples.

## Cierre de compra en contexto

PayPal&#39;s _Cierre de compra en contexto_ hace que sea más fácil que nunca pagar en línea. Los clientes nunca pierden de vista su tienda durante este pago simplificado sin problemas con un clic o dos. La desprotección en contexto funciona igual de bien en equipos Mac y PC, y ofrece una experiencia coherente en equipos de escritorio, tabletas y dispositivos móviles. Para obtener más información, consulte [Cierre de compra en contexto en el cierre de compra rápido][5].

![Demostración de pago y envío en contexto de PayPal](./assets/storefront-paypal-in-context.png){width="700" zoomable="yes"}

[_Demostración de pago y envío en contexto de PayPal_][6]

Al configurar la tienda para [!DNL PayPal Express Checkout], puede activar esta opción.

## Configurar tu cuenta PayPal

Antes de configurar el Pago y envío de PayPal Express en el Administrador de comercio, debes configurar tu cuenta de comerciante en el sitio web de PayPal.

1. Inicia sesión en tu cuenta PayPal Advanced en [manager.paypal.com][3].

1. Ir a **[!UICONTROL Service Settings]** > **[!UICONTROL Hosted Checkout Pages]** > **[!UICONTROL Set Up]** y realice la siguiente configuración:

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. Haga clic **[!UICONTROL Save Changes]**.

1. Configurar otro usuario (recomendado por PayPal):

   - Ir a [manager.paypal.com][3] e inicie sesión en su cuenta de.

   - Para configurar otro usuario, siga las instrucciones.

   - Haga clic **[!UICONTROL Update]**.

## Configuración del cierre de compra de PayPal Express en Commerce

Puede tener dos soluciones de PayPal activas al mismo tiempo: Pago y envío exprés de PayPal, además de una solución todo en uno. Si activa una solución diferente, la utilizada anteriormente se desactiva automáticamente.

>[!NOTE]
>
>Clic **[!UICONTROL Save Config]** en cualquier momento para guardar su progreso.

### Paso 1: Inicio de la configuración

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Payment Methods]**.

1. Si la instalación tiene varios sitios web, tiendas o vistas, establezca **[!UICONTROL Store View]** vaya a la vista de tienda en la que desee aplicar esta configuración.

1. En el _[!UICONTROL Merchant Location]_, seleccione la **[!UICONTROL Merchant Country]**dónde se encuentra su empresa.

   Esta configuración determina la selección de soluciones de PayPal que aparecen en la configuración.

   ![País comerciante](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. En _[!UICONTROL Recommended Solutions]_, haga clic en **[!UICONTROL Configure]**para **[!UICONTROL PayPal Express Checkout]**.

   ![Configurar Pago y envío de PayPal Express](./assets/paypal-express-checkout.png){width="600"}

### Paso 2: Activar y conectar tu cuenta PayPal

1. Si es necesario, expanda ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Required PayPal Settings]** sección.

   ![Conecta tu cuenta PayPal](./assets/paypal-express-required.png){width="600" zoomable="yes"}

1. Conecte su cuenta para pruebas o producción:

   - Para el modo de prueba (desarrollo), haga clic en **[!UICONTROL Sandbox Credentials]** e introduzca su [Zona protegida de PayPal][7] credenciales.
   - Para el modo de producción, haga clic en **[!UICONTROL Connect with PayPal]** e introduzca sus credenciales de cuenta de producción.

   Cuando valide la conexión, puede continuar.

1. Establecer **[!UICONTROL Enable this Solution]** hasta `Yes`.

1. Para habilitar [Pago y envío en contexto de PayPal](#in-context-checkout):

   - Establecer **[!UICONTROL Enable In-Context Checkout Experience]** hasta `Yes`.

   - Introduce tu PayPal **[!UICONTROL Merchant Account ID]**.

     El identificador de tu cuenta de comerciante se encuentra en el perfil de tu cuenta comercial de PayPal.

>[!NOTE]
>
>[Crédito de PayPal](paypal.md#paypal-credit-and-pay-later) está activada de forma predeterminada para esta opción de pago.

### Paso 3: Completa la configuración de PayPal necesaria

1. Si es necesario, expanda ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Express Checkout]** sección.

   ![Configuración requerida para Pago y envío mediante PayPal Express](./assets/paypal-express-settings.png){width="600" zoomable="yes"}

1. (Opcional) Introduzca el **[!UICONTROL Email Associated with PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >Las direcciones de correo electrónico distinguen entre mayúsculas y minúsculas. Para recibir el pago, la dirección de correo electrónico que introduzcas debe coincidir con la especificada en tu cuenta comercial de PayPal.

   Si no tienes una cuenta PayPal, pulsa **[!UICONTROL Start accepting payments via PayPal]**.

1. Establecer **[!UICONTROL API Authentication Methods]** a uno de los siguientes:

   - `API Signature` - Este método de autenticación de PayPal es el más fácil de implementar, y se basa en su nombre de usuario, contraseña y una cadena única de caracteres y números que identifica su cuenta. Las credenciales de la firma API no caducan.
   - `API Certificate` - Este método de autenticación de PayPal es más seguro, se basa en su nombre de usuario, contraseña y un certificado descargable. Las credenciales de la API caducan al cabo de tres años y deben renovarse.

   Si es necesario, complete lo siguiente:

   - **[!UICONTROL API Username]**
   - **[!UICONTROL API Password]**
   - **[!UICONTROL API Signature]**

1. Si utiliza credenciales de la cuenta de zona protegida, establezca **[!UICONTROL Sandbox Mode]** hasta `Yes`.

   Al probar la configuración en una zona protegida, utilice solo [números de tarjeta de crédito][4] que recomienda PayPal. Cuando esté listo para ir a producción, vuelva a la configuración y establezca el modo de entorno limitado en `No` y conéctese a su cuenta de PayPal de producción.

1. Si su sistema utiliza un servidor proxy para establecer la conexión entre Commerce y el sistema de pago de PayPal, establezca **[!UICONTROL API Uses Proxy]** hasta `Yes` y complete lo siguiente:

   - **[!UICONTROL Proxy Host]**
   - **[!UICONTROL Proxy Port]**

Al final de esta secuencia de pasos, se completa la configuración de PayPal necesaria. Puede continuar con la Configuración básica y avanzada o hacer clic en **[!UICONTROL Save Config]** y volver más tarde para ajustar la configuración

### Paso 4: Configurar el crédito de PayPal publicitario / Anunciar PayPal PayAfter (opcional)

A partir de la versión 2.4.3, PayPal PayAfter es compatible con las implementaciones que incluyen PayPal. Esta función permite a los compradores pagar un pedido en cuotas quincenales en lugar de pagar el importe completo en el momento de la compra. La experiencia de crédito de PayPal está en desuso.

Establecer **[!UICONTROL Enable PayPal PayLater Experience]** a uno de los siguientes:

- `Yes` - Para configurar Anunciar PayPal PayAfter
- `No` - Para configurar el crédito de PayPal publicitario

>[!NOTE]
>
>El **[!UICONTROL Enable PayPal PayLater Experience]** La configuración no desactiva la [!DNL PayPal PayLater] función y no se elimina **_[!UICONTROL PayPal PayLater]_** botones de la tienda. Para deshabilitar ambas **_[!UICONTROL PayPal PayLater]_** y **_[!UICONTROL PayPal Credit]_** botones de la tienda, se debe seleccionar la opción `PayPal Credit` valor para **[!UICONTROL Disable Funding Options]** configuración ([!UICONTROL Advanced Settings] bajo [!UICONTROL Frontend Experience Settings]).

#### Anunciar crédito de PayPal

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Advertise PayPal Credit]** sección.

1. Para obtener la información de la cuenta, haga clic en **[!UICONTROL Get Publisher ID from PayPal]** y siga las instrucciones.

1. Introduzca su **[!UICONTROL Publisher ID]**.

   ![Anunciar crédito de PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Home Page]** sección.

1. Para colocar un banner en la página, establezca **[!UICONTROL Display]** hasta `Yes`.

1. Establecer **[!UICONTROL Position]** a uno de los siguientes:

   - `Header (center)`
   - `Sidebar (right)`

1. Establecer **[!UICONTROL Size]** a uno de los siguientes:

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

   ![Ajustes de la página de inicio de crédito de PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) Utilice las secciones restantes y repita los pasos anteriores:

   - [!UICONTROL Catalog Category Page]
   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]

#### Anunciar PayPal PayAfter

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Advertise PayPal PayLater]** sección.

1. Establecer **[!UICONTROL Enable PayPal PayLater]** hasta `Yes`.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Home Page]** sección.

1. Para colocar un banner en la página, establezca **[!UICONTROL Display]** hasta `Yes`.

1. Establecer **[!UICONTROL Position]** a uno de los siguientes:

   - `Header (center)`
   - `Sidebar`

1. Establecer **[!UICONTROL Style Layout]** a uno de los siguientes:

   - `Text`
   - `Flex`

1. Para [!UICONTROL Style Layout] **[!UICONTROL Text]** sólo, establecer **[!UICONTROL Logo Type]** a uno de los siguientes:

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. Para [!UICONTROL Style Layout] **[!UICONTROL Text]** sólo, establecer **[!UICONTROL Logo Position]** a uno de los siguientes:

   - `Left`
   - `Right`
   - `Top`

1. Para [!UICONTROL Style Layout] **[!UICONTROL Text]** sólo, establecer **[!UICONTROL Text Color]** a uno de los siguientes:

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. Para [!UICONTROL Style Layout] **[!UICONTROL Text]** sólo, establecer **[!UICONTROL Text Size]** a uno de los siguientes:

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. Para [!UICONTROL Style Layout] **[!UICONTROL Flex]** sólo, establecer **[!UICONTROL Ratio]** a uno de los siguientes:

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. Para [!UICONTROL Style Layout] **[!UICONTROL Flex]** sólo, establecer **[!UICONTROL Color]** a uno de los siguientes:

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

   ![Ajustes de la página de inicio de crédito de PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) Utilice las secciones restantes y repita los pasos anteriores:

   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]
   - [!UICONTROL Checkout Payment Step]
   - [!UICONTROL Catalog Category Page]

### Paso 5: completar la configuración básica

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Basic Settings - PayPal Express Checkout]** sección.

   ![Configuración básica](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Title]**, introduce un título que identifique esta forma de pago durante el proceso de pago.

   Se recomienda utilizar el título _PayPal_ para todas las vistas de tiendas.

1. Si ofreces varias formas de pago, introduce un número para **[!UICONTROL Sort Order]** para determinar la secuencia en la que aparece Pago y envío de PayPal Express cuando se pone en venta con las otras formas de pago.

   Este número es relativo a las otras formas de pago. (`0` = primero, `1` = segundo, `2` = tercero, etc.)

1. Establecer **[!UICONTROL Payment Action]** a uno de los siguientes:

   - `Authorization` - Aprueba la compra y suspende los fondos. El importe no se retira hasta que se _capturado_ por el comerciante.
   - `Sale` - El importe de la compra se autoriza y se retira inmediatamente de la cuenta del cliente.
   - `Order` - El importe del pedido no se registra ni se autoriza en el saldo del cliente, la cuenta bancaria o la tarjeta de crédito en PayPal. La acción de pago del pedido representa un acuerdo entre el sistema de pago de PayPal y el comerciante. Permite al comerciante capturar uno o más importes hasta el total pedido desde la cuenta de comprador del cliente, durante un periodo de hasta 29 días. Una vez ordenados los fondos, el comerciante puede capturarlos en cualquier momento durante el siguiente período de 29 días. La captura del importe del pedido solo se puede realizar desde el administrador de comercio creando una o más facturas.

1. Para mostrar el _[!UICONTROL Check out with PayPal]_botón en la página de producto, establecer **[!UICONTROL Display on Product Details Page]**hasta `Yes`.

1. Si la acción de pago está configurada en `Order`, complete lo siguiente

   - **[!UICONTROL Authorization Honor Period (days)]** - Determina durante cuánto tiempo es válida la autorización principal. El valor debe ser igual al valor correspondiente de su cuenta comercial de PayPal. El valor predeterminado de tu cuenta de PayPal es `3`. Para aumentar este número, debes ponerte en contacto con PayPal. La autorización deja de ser válida a las 23:49 (hora del Pacífico, EE. UU.) del último día.

   - **[!UICONTROL Order Valid Period (days)]** - Determina durante cuánto tiempo es válido el pedido. Cuando el pedido deja de ser válido, ya no puede crear facturas para él. Especifique un valor igual al valor Período de validez del pedido en su cuenta comercial de PayPal. El valor predeterminado de tu cuenta de PayPal es `29`. Para cambiar este número, debes ponerte en contacto con PayPal.

   - **[!UICONTROL Number of Child Authorizations]** - Especifica el número máximo de autorizaciones para un único pedido, lo que determina el número máximo de facturas parciales en línea que puede crear para un pedido. Este valor debe ser igual a la configuración correspondiente de tu cuenta de PayPal. El número predeterminado de autorizaciones para niños en tu cuenta PayPal es `1`. Para aumentar este número, debes ponerte en contacto con PayPal.

### Paso 6: Completar la configuración avanzada

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Advanced Settings]** sección.

   ![Configuración avanzada: Pago y envío de PayPal Express](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. Establecer **[!UICONTROL Display on Shopping Cart]** hasta `Yes`.

1. Establecer **[!UICONTROL Payment Applicable From]** a uno de los siguientes:

   - `All Allowed Countries` - Los clientes de todos los países especificados en la configuración de su tienda pueden utilizar este método de pago.
   - `Specific Countries` : Después de elegir esta opción, el _[!UICONTROL Payment from Specific Countries]_aparece una lista. Para seleccionar varios países, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada elemento.

1. Para escribir comunicaciones con el sistema de pago en el fichero de registro, defina **[!UICONTROL Debug Mode]** hasta `Yes`.

   El archivo de registro de Pagos avanzados de PayPal es `_payflow_advanced.log`.

   >[!NOTE]
   >
   >De acuerdo con las normas de seguridad de datos PCI, la información de la tarjeta de crédito no se registra en el archivo de registro.

1. Para habilitar la verificación de autenticidad del host, establezca **[!UICONTROL Enable SSL Verification]** hasta `Yes`.

1. Para mostrar un resumen completo del pedido del cliente por artículo de línea desde el sitio de PayPal, establezca **[!UICONTROL Transfer Cart Line Items]** hasta `Yes`.

1. Para incluir hasta diez opciones de envío en el resumen, defina **[!UICONTROL Transfer Shipping Options]** hasta `Yes`. (Esta opción sólo aparece si los elementos de línea están configurados para transferir.)

1. Para determinar el tipo de imagen utilizada para el botón de aceptación de PayPal, establezca **[!UICONTROL Shortcut Buttons Flavor]** a uno de los siguientes:

   - `Dynamic` - (Recomendado) Muestra una imagen que se puede cambiar dinámicamente desde el servidor de PayPal.
   - `Static` - Muestra una imagen específica que no se puede cambiar dinámicamente.

1. Para permitir que los clientes sin cuentas de PayPal puedan realizar compras con este método, configure **[!UICONTROL Enable PayPal Guest Checkout]** hasta `Yes`.

1. Establecer **[!UICONTROL Require Customer's Billing Address]** a uno de los siguientes:

   - `Yes` - Requiere la dirección de facturación del cliente para todas las compras.
   - `No` - No requiere la dirección de facturación del cliente para ninguna compra.
   - `For Virtual Quotes Only` : Requiere la dirección de facturación del cliente solo para presupuestos virtuales.

   >[!NOTE]
   >
   >Esta función debe habilitarse para la cuenta de comerciante mediante el servicio de asistencia técnica de PayPal.

1. (Opcional) Configure las variables **[!UICONTROL Billing Agreement Signup]** para permitir que los clientes firmen un [contrato facturación](paypal-billing-agreements.md) con su tienda en el sistema de pago de PayPal cuando no haya acuerdos de facturación activos disponibles en la cuenta del cliente:

   - `Auto` - El cliente puede firmar un acuerdo de facturación durante el flujo de Pago y envío exprés o utilizar otro método de pago.
   - `Ask Customer` : El cliente puede decidir si firma un acuerdo de facturación durante el flujo de cierre de compra exprés.
   - `Never` - El cliente no puede firmar un acuerdo de facturación durante el flujo de cierre de compra exprés.

   >[!NOTE]
   >
   >Los comerciantes deben preguntar [Asistencia técnica de PayPal Merchant](https://developer.paypal.com/support/) para habilitar los acuerdos de facturación en sus cuentas. El _Suscripción al contrato de facturación_ El parámetro solo se activa después de que PayPal confirme que los contratos de facturación están activados en tu cuenta de comerciante.

1. Para permitir que el cliente complete la transacción desde el sitio de PayPal sin volver a su tienda para la revisión del pedido, establezca **[!UICONTROL Skip Order Review Step]** hasta `Yes`.

1. Complete las secciones adicionales que necesite para su tienda:

   - [Configuración del contrato de facturación PayPal](#paypal-billing-agreement-settings)
   - [Configuración del informe de liquidación](#settlement-report-settings)
   - [Configuración de experiencia de front-end](#frontend-experience-settings)
   - [Personalizar botones inteligentes](#customize-smart-buttons)
   - [Funciones](#features)

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

#### Configuración del acuerdo de facturación de PayPal

A [contrato facturación](paypal-billing-agreements.md) es un acuerdo de venta entre el comerciante y el cliente autorizado por PayPal para su uso con varios pedidos. Durante el proceso de cierre de compra, la opción de pago Acuerdo de facturación solo aparece para los clientes que ya han formalizado un acuerdo de facturación con su compañía. Una vez que PayPal autoriza el acuerdo, el sistema de pago emite un ID de referencia único para identificar cada pedido asociado con el acuerdo. Al igual que en un pedido de compra, no hay límite en el número de acuerdos de facturación que un cliente puede establecer con su compañía.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL PayPal Billing Agreement Settings]** sección.

   ![Configuración del contrato de facturación](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png){width="600" zoomable="yes"}

1. Establecer **[!UICONTROL Enabled]** hasta `Yes`.

1. Para **[!UICONTROL Title]**, introduzca un título que identifique el método del acuerdo de facturación de PayPal durante el cierre de compra.

1. Si ofrece varios métodos de pago, introduzca un número en la **[!UICONTROL Sort Order]** para determinar la secuencia en la que aparece el acuerdo de facturación cuando se enumera con otros métodos de pago durante el cierre de compra.

1. Establecer **[!UICONTROL Payment Action]** a uno de los siguientes:

   - `Authorization` - Aprueba la compra y suspende los fondos. La cantidad no se retira hasta que sea &quot;capturada&quot; por el comerciante.
   - `Sale` - El importe de la compra se autoriza y se retira inmediatamente de la cuenta del cliente.

1. Establecer **[!UICONTROL Payment Applicable From]** a uno de los siguientes:

   - `All Allowed Countries` - Los clientes de todos los países especificados en la configuración de su tienda pueden utilizar este método de pago.
   - `Specific Countries` : Después de elegir esta opción, el _[!UICONTROL Payment from Specific Countries]_aparece una lista. Para seleccionar varios países, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada uno de ellos.

1. Para registrar las comunicaciones con el sistema de pago en el fichero de registro, defina **[!UICONTROL Debug Mode]** hasta `Yes`.

   >[!NOTE]
   >
   >El archivo de registro se almacena en el servidor y solo pueden acceder a él los desarrolladores. De acuerdo con las normas de seguridad de datos PCI, la información de la tarjeta de crédito no se registra en el archivo de registro.

1. Para habilitar la verificación SSL, establezca **[!UICONTROL Enable SSL Verification]** hasta `Yes`.

1. Para mostrar un resumen de cada artículo de línea en el pedido del cliente en su página de pagos de PayPal, establezca **[!UICONTROL Transfer Cart Line Items]** hasta `Yes`.

1. Para permitir que los clientes inicien un acuerdo de facturación desde el panel de su cuenta de cliente, establezca **[!UICONTROL Allow in Billing Agreement Wizard]** hasta `Yes`.

#### Configuración del informe de liquidación

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Settlement Report Settings]** sección.

   ![Configuración del informe de liquidación](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL SFTP Credentials]**, haga lo siguiente:

   - Si se ha registrado en el servidor FTP seguro de PayPal, introduzca las siguientes credenciales de inicio de sesión en el SFTP:

      - Iniciar sesión
      - Contraseña

   - Para ejecutar informes de prueba antes de _puesta en marcha_ con Pago y envío exprés en el sitio, establezca **[!UICONTROL Sandbox Mode]** hasta `Yes`.

   - Introduzca el **[!UICONTROL Custom Endpoint Hostname or IP Address]**.

     De forma predeterminada, el valor es: `reports.paypal.com`

   - Introduzca el **[!UICONTROL Custom Path]** donde se guardan los informes.

     De forma predeterminada, el valor es: `/ppreports/outgoing`

1. Para generar informes de acuerdo con una programación, complete la **[!UICONTROL Scheduled Fetching]** configuración:

   - Establecer **[!UICONTROL Enable Automatic Fetching]** hasta `Yes`.

   - Establecer **[!UICONTROL Schedule]** a uno de los siguientes:

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPal conserva cada informe durante 45 días.

   - Establecer **[!UICONTROL Time of Day]** a la hora, los minutos y el segundo en que desea que se generen los informes.

#### Configuración de experiencia de front-end

Utilice la Configuración de experiencia de front-end para elegir qué logotipos de PayPal aparecen en el sitio y personalizar el aspecto de las páginas de comerciantes de PayPal.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Frontend Experience Settings]** sección.

   ![Configuración de experiencia de front-end](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. Seleccione el **[!UICONTROL PayPal Product Logo]** que deseas que aparezca en el bloque de PayPal de tu tienda.

   Los logotipos de PayPal están disponibles en cuatro estilos y dos tamaños:

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. Para personalizar el aspecto de las páginas de comerciantes de PayPal, haga lo siguiente:

   - Introduzca el nombre del **[!UICONTROL Page Style]** que desee aplicar a sus páginas de comerciante de PayPal:

      - `paypal` - Utiliza el estilo de página PayPal.
      - `primary` : Utiliza el estilo de página identificado como. _principal_ Estilo de en el perfil de la cuenta.
      - `your_custom_value` : Utiliza un estilo de página de pago personalizado, que se especifica en el perfil de la cuenta.

   - Para **[!UICONTROL Header Image URL]**, introduzca la dirección URL de la imagen que desea que aparezca en la esquina superior izquierda de la página de pago. El tamaño máximo de archivo es de 750 píxeles de ancho por 90 píxeles de alto.

     >[!NOTE]
     >
     >PayPal recomienda que la imagen resida en un servidor seguro (https). De lo contrario, un explorador puede advertir que _la página contiene elementos seguros y no seguros_.

   - Para establecer el color de las páginas, escriba el código hexadecimal de seis caracteres, sin el `#` símbolo, para cada una de las siguientes opciones:

      - **[!UICONTROL Header Background Color]** - Color de fondo del encabezado de la página de pago.
      - **[!UICONTROL Header Border Color]** - Color del borde de dos píxeles alrededor del encabezado.
      - **[!UICONTROL Page Background Color]** - Color de fondo para la página de pago y alrededor de la cabecera y el formulario de pago.

#### Personalizar botones inteligentes

El _Botones de pago inteligentes_ Esta función permite personalizar el botón PayPal, que se puede mostrar en las páginas Cierre de compra, Detalles del producto, Carro de compras y Minicarro de compras. El estudio interno de PayPal sugiere que las opciones predeterminadas son muy reconocibles y podrían dar lugar a un aumento de las tasas de compra, pero es posible que sus valores predeterminados no coincidan con el estilo de su tienda. Puede elegir:

- Tamaño, color y forma del botón de PayPal
- Texto que aparece en el botón PayPal
- El diseño, cuando se muestran varios botones (horizontal o vertical)

Para personalizar botones, expanda ![Selector de expansión](../assets/icon-display-expand.png) Realice cada una de las siguientes secciones y ajuste la configuración:

- **[!UICONTROL Checkout Page]**
- **[!UICONTROL Product Pages]**
- **[!UICONTROL Cart Page]**
- **[!UICONTROL Mini Cart]**

![Configuración de página de cierre](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings2.png){width="600" zoomable="yes"}

**_Para configurar la visualización del botón para cada tipo de página:_**

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) la sección.

1. Establecer **[!UICONTROL Customize Button]** hasta `Yes`.

1. Para definir el texto que PayPal muestra en el botón Pago inteligente, establece **[!UICONTROL Label]** a uno de los siguientes:

   - `Checkout` - Pago y envío mediante PayPal
   - `Pay` - Pago y envío mediante PayPal
   - `Buy Now` - Comprar ahora con PayPal
   - `PayPal` - PayPal
   - `Installment`  - PayPal
   - `Credit` - Crédito de PayPal

1. Establecer **[!UICONTROL Layout]** a uno de los siguientes:

   - `Vertical` - (Predeterminado) Muestra los botones inteligentes de PayPal verticalmente. El comprador debe iniciar sesión en PayPal o crear una cuenta PayPal, independientemente de si **[!UICONTROL Enable Guest Checkout]** está seleccionado.
   - `Horizontal` - Muestra los botones inteligentes de PayPal horizontalmente. Cuándo **[!UICONTROL Enable Guest Checkout]** está seleccionado, la variable **[!UICONTROL Pay with Debit Card or Credit Card]** El botón aparece en la ventana emergente de PayPal. En caso contrario, el comprador debe iniciar sesión en PayPal o crear una cuenta PayPal.

1. Establecer **[!UICONTROL Size]** a uno de los siguientes:

   - `Medium` - 250 por 35 píxeles.
   - `Large` - 350 por 40 píxeles.
   - `Responsive` - (Predeterminado) Se ajusta a la anchura del contenedor. La anchura mínima es de 100 píxeles y la anchura máxima es de 500 píxeles. La altura se ajusta dinámicamente en función de la anchura.

1. Establecer **[!UICONTROL Shape]** a uno de los siguientes:

   - `Pill` - (Predeterminado) El botón tiene forma de píldora (largo en el centro y curvado en los extremos).
   - `Rectangle` - Forma cuadrada, sin curvas, en un rectángulo.

1. Establecer **[!UICONTROL Color]** a uno de los siguientes:

   - `Gold` (Predeterminado)
   - `Blue`
   - `Silver`
   - `Black`

#### Funciones

La configuración de funciones permite desactivar determinadas funciones relacionadas con esta solución de PayPal.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Features]** sección.

   ![Configuración de página de cierre](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings3.png){width="600" zoomable="yes"}

1. Configure las variables **[!UICONTROL Disable Funding Options]** para determinar qué otras opciones de financiación de PayPal se muestran en la _Finalizar compra_ página.

   Las opciones seleccionadas no se muestran en la _Finalizar compra_ página. Las opciones no seleccionadas se muestran únicamente si PayPal admite la divisa de la tienda y la ubicación del comprador. Las opciones incluyen:

   - Crédito de PayPal
   - Venmo
   - Iconos de tarjeta de crédito de pago y envío de PayPal
   - Elektronisches Lastschriftverfahren - alemán ELV

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypal.com/webapps/mpp/buying-online
[3]: https://manager.paypal.com/
[4]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[5]: https://www.paypal.com/rs/webapps/mpp/express-checkout
[6]: https://demo.paypal.com/us/demo/navigation?merchant=bigbox&amp;amp;page=incontextProductCheckout
[7]: https://developer.paypal.com/docs/api-basics/sandbox/
