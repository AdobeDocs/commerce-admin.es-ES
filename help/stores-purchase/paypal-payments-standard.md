---
title: PayPal Payments Standard
description: Aprenda a configurar PayPal Payments Standard como solución de pago en línea en su tienda.
exl-id: b4024dac-34d7-4f1a-ad9d-0fc406194609
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2073'
ht-degree: 0%

---

# PayPal Payments Standard

[PayPal Payments Standard][4] es la forma más sencilla de aceptar pagos en línea. Puedes ofrecer a tus clientes la comodidad del pago con tarjeta de crédito y PayPal simplemente añadiendo un botón de pago y envío a tu tienda.

>[!NOTE]
>
>Para los comerciantes fuera de los Estados Unidos, se llama _PayPal Website Payments Standard_.

Con PayPal Payments Standard, puedes deslizar tarjetas de crédito en dispositivos móviles. No hay cuota mensual y puedes recibir el pago a través de eBay. Las tarjetas de crédito compatibles incluyen Visa, MasterCard, Discover y American Express. Además, los clientes pueden pagar directamente desde sus cuentas personales de PayPal. PayPal Payments Standard está disponible en todos los países de la lista de referencia mundial de PayPal.

>[!IMPORTANT]
>
>**Requisitos de PSD2:** <br/>
>A partir del 14 de septiembre de 2019, los bancos europeos podrían rechazar los pagos que no cumplan [PSD 2](../getting-started/compliance-payment-services-directive.md) requisitos. PayPal Payments Standard no debe llevar a cabo ninguna acción para cumplir con PSD2, ya que PayPal gestiona todos los requisitos.

## Requisitos del comerciante

- [Cuenta comercial de PayPal][1]

## Flujo de trabajo de retirada

Para los clientes, PayPal Payments Standard es un proceso de un solo paso si la información de la tarjeta de crédito de sus cuentas personales de PayPal está actualizada.

1. **Pedido de lugares del cliente** - El cliente hace clic o pulsa el botón _Pagar ahora_ para completar la compra.

1. **PayPal procesa la transacción** - Se redirige al cliente al sitio de PayPal para completar la transacción.

## Configurar PayPal Payments Standard

>[!NOTE]
>
>PayPal Payments Standard no se puede utilizar simultáneamente con ningún otro método de PayPal, incluido el Pago y envío exprés. Si cambia las soluciones de pago, la utilizada anteriormente queda desactivada.

>[!TIP]
>
>Clic **[!UICONTROL Save Config]** en cualquier momento para guardar su progreso.

### Paso 1: Inicio de la configuración

Este método de configuración supone que ya tienes una cuenta PayPal.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Payment Methods]**.

1. Si la instalación de Commerce tiene varios sitios web, tiendas o vistas, configure **[!UICONTROL Store View]** vaya a la vista de tienda en la que desee aplicar esta configuración.

1. En el _[!UICONTROL Merchant Location]_, seleccione la **[!UICONTROL Merchant Country]**dónde se encuentra su empresa.

   Esta configuración determina la selección de soluciones de PayPal que aparecen en la configuración.

   ![País Comerciante](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Expandir **[!UICONTROL PayPal All-in-One Payment Solutions]** y haga clic en **[!UICONTROL Configure]** para **[!UICONTROL Payments Standard]**.

   ![PayPal Payments Standard](./assets/paypal-payments-standard.png){width="700" zoomable="yes"}

### Paso 2: Activar y conectar tu cuenta PayPal

![Configuración de PayPal Payments Standard](./assets/paypal-payments-display.png){width="600" zoomable="yes"}

1. Conecte su cuenta para pruebas o producción:

   - Para el modo de prueba (desarrollo), haga clic en **[!UICONTROL Sandbox Credentials]** e introduzca su [Zona protegida de PayPal][3] credenciales.
   - Para el modo de producción, haga clic en **[!UICONTROL Connect with PayPal]** e introduzca sus credenciales de cuenta de producción.

   Cuando valide la conexión, puede continuar.

1. Establecer **[!UICONTROL Enable this Solution]** hasta `Yes`.

1. Si desea ofrecer [Crédito de PayPal](paypal.md#paypal-credit-and-pay-later) a sus clientes, configure **[!UICONTROL Enable PayPal Credit]** hasta `Yes`.

### Paso 3: Completar la configuración de normas de pago

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Payments Standard]** sección.

   ![Configuración requerida](../configuration-reference/sales/assets/payment-methods-paypal-payments-standard-required.png){width="600" zoomable="yes"}

1. Introduzca el **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

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

   Al probar la configuración en una zona protegida, utilice solo [números de tarjeta de crédito][2] que recomienda PayPal. Cuando esté listo para ir a producción, vuelva a la configuración y establezca el modo de entorno limitado en `No` y conéctese a su cuenta de PayPal de producción.

1. Si su sistema utiliza un servidor proxy para establecer la conexión entre Adobe Commerce o Magento Open Source y el sistema de pago de PayPal, establezca **[!UICONTROL API Uses Proxy]** hasta `Yes` y complete lo siguiente:

   - **[!UICONTROL Proxy Host]**
   - **[!UICONTROL Proxy Port]**

### Paso 4: Configurar el crédito de PayPal publicitario / Anunciar PayPal PayAfter (opcional)

A partir de la versión 2.4.3, PayPal PayAfter es compatible con las implementaciones que incluyen PayPal. Esta función permite a los compradores pagar un pedido en cuotas quincenales en lugar de pagar el importe completo en el momento de la compra. La experiencia de crédito de PayPal está en desuso.

Establecer **[!UICONTROL Enable PayPal PayLater Experience]** a uno de los siguientes:

- `Yes` - Para configurar Anunciar PayPal PayAfter
- `No` - Para configurar el crédito de PayPal publicitario

#### Anunciar crédito de PayPal

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Advertise PayPal Credit]** sección.

   ![Ajustes de la página de inicio de crédito de PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

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

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) Utilice las secciones restantes y repita los pasos anteriores:

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### Anunciar PayPal PayAfter

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Advertise PayPal PayLater]** sección.

1. Establecer **[!UICONTROL Enable PayPal PayLater]** hasta `Yes`.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Home Page]** sección.

   ![Ajustes de la página de inicio de crédito de PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

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

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) Utilice las secciones restantes y repita los pasos anteriores:

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **Paso de pago y envío**
   - **[!UICONTROL Catalog Category Page]**

### Paso 5: completar la configuración básica

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Basic Settings - PayPal Website Payments Standard]** sección.

   ![Configuración básica](./assets/paypal-payments-basic.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Title]**, introduce un título que identifique esta forma de pago durante el proceso de pago.

   Se recomienda utilizar el título _PayPal_ para todas las vistas de tiendas.

1. Si ofreces varias formas de pago, introduce un número para **[!UICONTROL Sort Order]** para determinar la secuencia en la que PayPal Payments Standard aparece cuando se enumera con las demás formas de pago.

   Este número es relativo a las otras formas de pago. (`0` = primero, `1` = segundo, `2` = tercero, etc.)

1. Establecer **[!UICONTROL Payment Action]** a uno de los siguientes:

   - `Authorization` - Aprueba la compra y suspende los fondos. La cantidad no se retira hasta que sea capturada por el comerciante.
   - `Sale` - El importe de la compra se autoriza y se retira inmediatamente de la cuenta del cliente.

1. Para mostrar el _[!UICONTROL Check out with PayPal]_botón en la página de producto, establecer **[!UICONTROL Display on Product Details Page]**hasta `Yes`.

### Paso 6: Completar la configuración avanzada

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Advanced Settings]** sección.

   ![Configuración avanzada](../configuration-reference/sales/assets/payment-methods-paypal-payment-standard-advanced.png){width="600" zoomable="yes"}

1. Para que el Estándar de pagos de PayPal esté disponible tanto en el carro de compras como en el minicarrito, establezca **[!UICONTROL Display on Shopping Cart]** hasta `Yes`.

1. Establecer **[!UICONTROL Payment from Applicable Countries]** a uno de los siguientes:

   - `All Allowed Countries` - Clientes de todos [países](../getting-started/store-details.md#country-options) especificado en la configuración de tu tienda puede utilizar este método de pago.
   - `Specific Countries` - Después de elegir esta opción, la variable _[!UICONTROL Payment from Specific Countries]_aparece una lista. Para seleccionar varios países, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

1. Para registrar las comunicaciones con el sistema de pago en el fichero de registro, defina **[!UICONTROL Debug Mode]** hasta `Yes`.

   >[!NOTE]
   >
   >El archivo de registro se almacena en el servidor y solo pueden acceder a él los desarrolladores. De acuerdo con las normas de seguridad de datos PCI, la información de la tarjeta de crédito no se registra en el archivo de registro.

1. Para habilitar la verificación SSL, establezca **[!UICONTROL Enable SSL Verification]** hasta `Yes`.

1. Para mostrar un resumen de cada artículo de línea en el pedido de la página de pagos de PayPal, establece **[!UICONTROL Transfer Cart Line Items]** hasta `Yes`.

   Para incluir hasta diez opciones de envío en el resumen, defina **[!UICONTROL Transfer Shipping Options]** hasta `Yes`. (Esta opción sólo aparece si los elementos de línea están configurados para transferir.)

1. Para determinar el tipo de imagen que se utiliza para el botón de aceptación de PayPal, establezca **[!UICONTROL Shortcut Buttons Flavor]** a uno de los siguientes:

   - `Dynamic` - (Recomendado) Muestra una imagen que se puede cambiar dinámicamente desde el servidor de PayPal.
   - `Static` - Muestra una imagen específica que no se puede cambiar dinámicamente.

1. Para permitir que los clientes que no tengan una cuenta PayPal puedan realizar una compra con este método, configure **[!UICONTROL Enable PayPal Guest Checkout]** hasta `Yes`.

1. Establecer **[!UICONTROL Require Customer's Billing Address]** a uno de los siguientes:

   - `Yes` - Requiere la dirección de facturación del cliente para todas las compras.
   - `No` - No requiere la dirección de facturación del cliente para ninguna compra.
   - `For Virtual Quotes Only` : Requiere la dirección de facturación del cliente solo para presupuestos virtuales.

1. Para permitir que un cliente introduzca una [Acuerdo de facturación de PayPal](paypal-billing-agreements.md) con su tienda cuando no haya acuerdos de facturación activos disponibles en la cuenta del cliente, establezca **[!UICONTROL Billing Agreement Signup]** a uno de los siguientes:

   - `Auto` - El cliente puede firmar un acuerdo de facturación durante el flujo de Pago Express o utilizar otro método de pago.
   - `Ask Customer` - El cliente puede decidir si desea celebrar un acuerdo de facturación durante el flujo de trabajo de cierre de compra exprés.
   - `Never` - El cliente no puede firmar un acuerdo de facturación durante el flujo de trabajo de cierre de compra exprés.

   >[!NOTE]
   >
   >Los comerciantes deben solicitar la Asistencia técnica del comerciante de PayPal para habilitar los acuerdos de facturación en sus cuentas. El _Suscripción al contrato de facturación_ Este parámetro solo se puede activar después de que PayPal confirme que los contratos de facturación están activados en tu cuenta de comerciante.

1. Para permitir que el cliente complete la transacción desde el sitio de PayPal sin volver a su tienda para la revisión del pedido, establezca **[!UICONTROL Skip Order Review Step]** hasta `Yes`.

### Paso 7: Complete y guarde los ajustes de configuración

1. Complete las siguientes secciones, según sea necesario para su tienda:

   - [Configuración del acuerdo de facturación de PayPal](#paypal-billing-agreement-settings)
   - [Configuración del informe de liquidación](#settlement-report-settings)
   - [Configuración de experiencia de front-end](#frontend-experience-settings)

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

   - Para ejecutar informes de prueba antes de publicar el cierre de compra exprés en el sitio, establezca **[!UICONTROL Sandbox Mode]** hasta `Yes`.

   - Introduzca el **[!UICONTROL Custom Endpoint Hostname or IP Address]**.

     El valor predeterminado es `reports.paypal.com`.

   - Introduzca el **[!UICONTROL Custom Path]** donde se guardan los informes.

     El valor predeterminado es `/ppreports/outgoing`.

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

Utilice el _[!UICONTROL Frontend Experience Settings]_para elegir qué logotipos de PayPal aparecen en el sitio y personalizar el aspecto de las páginas de comerciantes de PayPal.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Frontend Experience Settings]** sección.

   ![Configuración de experiencia de front-end](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. Seleccione el **[!UICONTROL PayPal Product Logo]** que deseas que aparezca en el bloque de PayPal de tu tienda.

   Los logotipos de PayPal están disponibles en cuatro estilos y dos tamaños:

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. Para personalizar el aspecto de las páginas de comerciantes de PayPal:

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

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[3]: https://developer.paypal.com/docs/api-basics/sandbox/
[4]: https://developer.paypal.com/docs/paypal-payments-standard/mobile-paypal-payments-standard/
