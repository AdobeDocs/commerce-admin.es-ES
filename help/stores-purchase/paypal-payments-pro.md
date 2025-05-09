---
title: PayPal Payments Pro
description: Aprenda a configurar PayPal Payments Pro como solución de pago en línea en su tienda.
exl-id: 9cc5c3a6-d471-4198-85a2-c4cf9dfd378b
feature: Payments
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '2257'
ht-degree: 0%

---

# PayPal Payments Pro

[PayPal Payments Pro][3] te ofrece todas las ventajas de una cuenta comercial y una puerta de enlace de pago en una sola vez, además de la capacidad de crear tu propia experiencia de pago totalmente personalizada. PayPal Express Checkout se activa automáticamente con PayPal Payments Pro, por lo que puedes acceder a más de 110 millones de usuarios activos de PayPal.

![PayPal Payments Pro mostrado en el minicarrito](./assets/storefront-mini-cart-payments-pro-racer-tank.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>**Requisitos de PSD2:** <br/>
>A partir del 14 de septiembre de 2019, los bancos europeos podrían rechazar los pagos que no cumplan los requisitos de [PSD2](../getting-started/compliance-payment-services-directive.md). Para cumplir con PSD2, PayPal Payments Pro debe estar integrado con un complemento de terceros.

>[!NOTE]
>
>Actualmente, PayPal Payments Pro está disponible en EE. UU., Reino Unido y Canadá.

## Requisitos

- [Cuenta comercial de PayPal][1] (con pagos directos activado)

## Flujo de trabajo de retirada

1. **El cliente va al cierre de compra** - El cliente agrega productos al carro de compras y pulsa o hace clic en _Continuar con el cierre de compra_.|
1. **El cliente elige la forma de pago** - Durante el proceso de pago, el cliente elige la opción _Pago directo mediante PayPal_ e introduce la información de la tarjeta de crédito.
   - Si paga con PayPal Payments Pro, el cliente permanece en su sitio durante el proceso de pago.
   - Si pagas con PayPal Express Checkout, se redirige al cliente al sitio de PayPal para completar la transacción.

A petición del cliente, el administrador de la tienda también puede crear un pedido desde el administrador y procesar la transacción con PayPal Payments Pro.

## Flujo de trabajo de procesamiento de pedidos

1. **Pedido realizado** - El pedido puede ser procesado por el administrador de tu tienda o desde tu cuenta comercial de PayPal.

1. **[!UICONTROL Payment Action]**: la acción de pago especificada en la configuración se aplica al pedido. Las opciones incluyen:

   - **Autorizar** - Commerce crea un pedido de ventas con el estado _Procesando_. En este caso, la cantidad de dinero que se va a autorizar está pendiente de aprobación.
   - **Venta**: Commerce crea un pedido de venta y una factura.
   - **Capturar**: PayPal transfiere el importe del pedido desde el saldo del cliente, la cuenta bancaria o la tarjeta de crédito a la cuenta de comerciante.

1. **Facturación**: se crea una factura en Commerce después de que PayPal envíe un mensaje de notificación de pago instantáneo a Commerce.

   Asegúrate de que las notificaciones de pago instantáneo estén activadas en tu cuenta de PayPal.

   >[!NOTE]
   >
   >Si es necesario, se puede facturar parcialmente un pedido para una cantidad de productos especificada. Para cada factura parcial enviada, se crea una transacción de captura independiente con un ID único y se genera una factura independiente.

   Las transacciones de pago solo de autorización se cierran solo después de capturar el importe completo del pedido.

   Un pedido puede anularse en línea en cualquier momento hasta que el importe del pedido se haya facturado por completo.

1. **Devuelve**: si el cliente devuelve los productos comprados y solicita un reembolso, como con la captura del importe del pedido y la creación de la factura, puede crear un reembolso en línea desde el administrador o desde su cuenta comercial de PayPal.

## Configurar tu cuenta PayPal

Antes de configurar PayPal Payments Pro en Commerce, debes configurar tu cuenta comercial en el sitio web de PayPal.

1. Inicia sesión en tu [cuenta comercial de PayPal](https://manager.paypal.com/).

1. En el menú Administrador de PayPal, seleccione **[!UICONTROL Service Settings]**.

1. En **[!UICONTROL Hosted Checkout Pages]**, haga clic en **[!UICONTROL Set Up]**.

1. En **[!UICONTROL Choose your settings]**, establezca **[!UICONTROL Transaction Process Mode]** en `Live`.

1. En **[!UICONTROL Display options on payment page]**, establezca **[!UICONTROL Cancel URL Method]** en `POST`.

1. En **[!UICONTROL Billing Information]**, active las casillas de verificación del código de seguridad de la tarjeta **[!UICONTROL CSC]** para los campos obligatorios y editables.

1. En **[!UICONTROL Payment Confirmation]**, establezca **[!UICONTROL Return URL Method]** en `POST`.

1. En **[!UICONTROL Security Options]**, configure lo siguiente:

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. Haga clic en **[!UICONTROL Save Changes]**.

1. En el menú _Administrador de PayPal_, elige **[!UICONTROL Service Settings]** y en _Páginas de pago y envío hospedadas_, elige **[!UICONTROL Customize]**.

1. Elija **[!UICONTROL Layout C]**.

   El diseño C solo muestra los campos de tarjeta de crédito y débito, y puede enmarcarse en su sitio o utilizarse como ventana emergente independiente. El tamaño se fija en 490 x 565 píxeles, con espacio adicional para mensajes de error. En algunos sistemas, esta configuración corrige un problema con la redirección transparente.

1. Haga clic en **[!UICONTROL Save and Publish]**.

1. En el menú Administrador de PayPal, seleccione **[!UICONTROL Account Administration]**. En **[!UICONTROL Manage Security]**, haga clic en **[!UICONTROL Transaction Settings]**.

1. Establezca **[!UICONTROL Allow reference transactions]** en `Yes`.

1. Haga clic en **[!UICONTROL Confirm]**.

   >[!NOTE]
   >
   >Si tiene varios sitios web de Commerce, debe crear una cuenta PayPal Payments Pro independiente para cada uno.

1. Configurar otro usuario (recomendado por PayPal):

   - En la segunda fila del menú principal, haga clic en **[!UICONTROL Manage Users]**.

   - Para agregar otro usuario a la cuenta, haga clic en **[!UICONTROL Add User]**. El vínculo se encuentra justo encima del título Administrar usuarios.

   - Rellene los campos obligatorios de las siguientes secciones del formulario _[!UICONTROL Add User]_:

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - Haga clic en **[!UICONTROL Update]**.

1. Asegúrate de cerrar la sesión de tu cuenta PayPal.

## Configuración de PayPal Payments Pro en Commerce

>[!NOTE]
>
>Puedes tener dos soluciones de PayPal activas al mismo tiempo: [Pago y envío exprés de PayPal](paypal-express-checkout.md), además de cualquiera de las [soluciones todo en uno](paypal.md#paypal-all-in-one-payment-solutions). Si cambia las soluciones de pago, la que se usaba anteriormente se desactiva automáticamente.

>[!TIP]
>
>Haga clic en **[!UICONTROL Save Config]** en cualquier momento para guardar el progreso.

### Paso 1: Inicio de la configuración

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Payment Methods]**.

1. Si la instalación de Commerce tiene varios sitios web, tiendas o vistas, establezca **[!UICONTROL Store View]** en la vista de tienda en la que desee aplicar esta configuración.

1. En la sección _[!UICONTROL Merchant Location]_, seleccione **[!UICONTROL Merchant Country]**&#x200B;donde se encuentra su empresa.

   Esta configuración determina la selección de soluciones de PayPal que aparecen en la configuración.

   ![País Comercial](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Expanda **[!UICONTROL PayPal All-in-One Payment Solution]** y haga clic en **[!UICONTROL Configure]** para **[!UICONTROL Payments Pro]**.

   ![Pagos mediante PayPal Pro](./assets/paypal-payments-pro.png){width="600" zoomable="yes"}

### Paso 2: Completa la configuración de PayPal necesaria

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Payments Pro and Express Checkout]**.

   ![Configuración necesaria de PayPal Payments Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-required.png){width="600" zoomable="yes"}

1. (Opcional) Escriba **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >Las direcciones de correo electrónico distinguen entre mayúsculas y minúsculas. Para recibir el pago, la dirección de correo electrónico debe coincidir con la especificada en tu cuenta comercial de PayPal.

   Si no tiene una cuenta PayPal, haga clic en **[!UICONTROL Start accepting payments via PayPal]**.

1. Introduzca una de las siguientes credenciales que utiliza para iniciar sesión en su cuenta de comerciante de PayPal:

   - **[!UICONTROL Partner]**: tu ID de socio de PayPal.
   - **[!UICONTROL Vendor]**: tu nombre de inicio de sesión de usuario de PayPal.
   - **[!UICONTROL User]**: el ID de otro usuario que está configurado en tu cuenta PayPal.

1. Escribe el **[!UICONTROL Password]** que está asociado con tu cuenta PayPal.

1. Para ejecutar transacciones de prueba, establezca **[!UICONTROL Test Mode]** en `Yes`.

   Al probar la configuración en una zona protegida, usa solo [números de tarjeta de crédito][2] recomendados por PayPal. Cuando esté listo para ir a producción, vuelva a la configuración y establezca el modo de prueba en `No`.

1. Si su sistema utiliza un servidor proxy para establecer la conexión con el sistema PayPal, establezca **[!UICONTROL Use Proxy]** en `Yes` y haga lo siguiente:

   - Escriba la dirección IP de **[!UICONTROL Proxy Host]**.

   - Escriba el número de puerto de **[!UICONTROL Proxy Port]**.

   Se utiliza un proxy cuando el cortafuegos del servidor impide el acceso directo al servidor de PayPal. En tal caso, se utiliza un servidor de terceros para transmitir el tráfico.

1. Establezca **[!UICONTROL Enable this Solution]** en `Yes`.

1. Si quieres ofrecer [crédito de PayPal](paypal.md#paypal-credit-and-pay-later) a tus clientes, establece **[!UICONTROL Enable PayPal Credit]** en `Yes`.

1. Si desea almacenar de forma segura los datos de pago o de tarjeta de crédito del cliente, de modo que los clientes no tengan que volver a especificar la información de pago cada vez, establezca **[!UICONTROL Vault Enabled]** en `Yes`.

### Paso 3: Configurar el crédito de PayPal / Anunciar PayPal PayAfter (opcional)

A partir de la versión 2.4.3, PayPal PayAfter es compatible con las implementaciones que incluyen PayPal. Esta función permite a los compradores pagar un pedido en cuotas quincenales en lugar de pagar el importe completo en el momento de la compra. La experiencia de crédito de PayPal está en desuso.

Establezca **[!UICONTROL Enable PayPal PayLater Experience]** en una de las siguientes opciones:

- `Yes` - Para configurar Anunciar PayPal PayAfter
- `No` - Para configurar el crédito de PayPal publicitario

#### Anunciar crédito de PayPal

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Advertise PayPal Credit]**.

   ![Anunciar crédito de PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. Para obtener la información de su cuenta, haga clic en **[!UICONTROL Get Publisher ID from PayPal]** y siga las instrucciones.

1. Escriba su **[!UICONTROL Publisher ID]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Home Page]**.

   ![Anunciar la configuración de la página de inicio de crédito de PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. Para colocar un banner en la página, establezca **[!UICONTROL Display]** en `Yes`.

1. Establezca **[!UICONTROL Position]** en una de las siguientes opciones:

   - `Header (center)`
   - `Sidebar (right)`

1. Establezca **[!UICONTROL Size]** en una de las siguientes opciones:

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) las secciones restantes y repita los pasos anteriores:

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### Anunciar PayPal PayAfter

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Advertise PayPal PayLater]**.

1. Establezca **[!UICONTROL Enable PayPal PayLater]** en `Yes`.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Home Page]**.

   ![Anunciar la configuración de la página de inicio de crédito de PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. Para colocar un banner en la página, establezca **[!UICONTROL Display]** en `Yes`.

1. Establezca **[!UICONTROL Position]** en una de las siguientes opciones:

   - `Header (center)`
   - `Sidebar`

1. Establezca **[!UICONTROL Style Layout]** en una de las siguientes opciones:

   - `Text`
   - `Flex`

1. Solo para [!UICONTROL Style Layout] **[!UICONTROL Text]**, establezca **[!UICONTROL Logo Type]** en uno de los siguientes:

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. Solo para [!UICONTROL Style Layout] **[!UICONTROL Text]**, establezca **[!UICONTROL Logo Position]** en uno de los siguientes:

   - `Left`
   - `Right`
   - `Top`

1. Solo para [!UICONTROL Style Layout] **[!UICONTROL Text]**, establezca **[!UICONTROL Text Color]** en uno de los siguientes:

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. Solo para [!UICONTROL Style Layout] **[!UICONTROL Text]**, establezca **[!UICONTROL Text Size]** en uno de los siguientes:

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. Solo para [!UICONTROL Style Layout] **[!UICONTROL Flex]**, establezca **[!UICONTROL Ratio]** en uno de los siguientes:

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. Solo para [!UICONTROL Style Layout] **[!UICONTROL Flex]**, establezca **[!UICONTROL Color]** en uno de los siguientes:

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) las secciones restantes y repita los pasos anteriores:

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### Paso 4: completar la configuración básica

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Basic Settings - PayPal Payments Pro]**.

   ![Configuración básica de PayPal Payment Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-basic-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Title]**, introduce un título que identifique PayPal Payments Pro durante el proceso de pago y envío.

   Se recomienda usar el título _Tarjeta de débito o crédito_.

1. Si ofrece varias formas de pago, ingrese un número para **[!UICONTROL Sort Order]** a fin de determinar la secuencia en que PayPal Payments Pro aparece cuando se enumera con otras formas de pago durante el cierre de compra.

   Este número es relativo a las otras formas de pago. (`0` = primero, `1` = segundo, `2` = tercero, etc.)

1. Establezca **[!UICONTROL Payment Action]** en una de las siguientes opciones:

   - `Authorization` - Aprueba la compra, pero suspende los fondos. La cantidad no se retira hasta que el comerciante _la capture_.
   - `Sale`: el importe de la compra se autoriza y se retira inmediatamente de la cuenta del cliente.

1. Para **[!UICONTROL Credit Card Settings]**, selecciona las tarjetas de crédito que aceptas para el pago en tu tienda.

   Para seleccionar varias tarjetas, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada una de ellas.

   >[!NOTE]
   >
   >American Express requiere un acuerdo adicional.

### Paso 5: Completar la configuración avanzada

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Advanced Settings]**.

   ![Configuración avanzada de PayPal Payments Pro](./assets/paypal-payments-pro-advanced-settings.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Payment Applicable From]** en una de las siguientes opciones:

   - `All Allowed Countries`: los clientes de todos los [países](../getting-started/store-details.md#country-options) especificados en la configuración de su tienda pueden usar este método de pago.
   - `Specific Countries` - Después de elegir esta opción, aparece la lista _[!UICONTROL Payment from Specific Countries]_. Mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y seleccione cada país de la lista donde los clientes pueden realizar compras en su tienda.

1. Para escribir comunicaciones con el sistema de pago en el archivo de registro, establezca **[!UICONTROL Debug Mode]** en `Yes`.

   >[!NOTE]
   >
   >De acuerdo con las normas de seguridad de datos PCI, la información de la tarjeta de crédito no se registra en el archivo de registro.

1. Para habilitar la comprobación de la autenticidad del host, establezca **[!UICONTROL Enable SSL Verification]** en `Yes`.

1. Para requerir que los clientes escriban un código CVV, establezca **[!UICONTROL Require CVV Entry]** en `Yes`.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL CVV and AVS Settings]**.

1. Para determinar cuándo se debe rechazar una transacción cuando el sistema de verificación de direcciones identifica una discrepancia, especifique cómo manejar cada uno de los siguientes escenarios:

   - Para rechazar una transacción basada en una discordancia de calle no coincidente, establezca **[!UICONTROL AVS Street Does Not Match]** en `Yes`.

   - Para rechazar una transacción basada en un código postal que no coincide, establezca **[!UICONTROL AVS Zip Does Not Match]** en `Yes`.

   - Para rechazar una transacción basada en un identificador de país que no coincide, establezca **[!UICONTROL International AVS Indicator Does Not Match]** en `Yes`.

   - Para rechazar una transacción basada en un código CVV no coincidente, establezca **[!UICONTROL International Card Security Code Does Not Match]** en `Yes`.

   ![Configuración requerida de PayPal Payments Pro - CVV y AVS](./assets/paypal-payments-pro-cvv-avs-settings.png){width="600" zoomable="yes"}

1. Complete las siguientes secciones, según sea necesario para su tienda:

   - [Configuración del informe de liquidación](#settlement-report-settings)
   - [Configuración de experiencia de front-end](#frontend-experience-settings)

#### Configuración del informe de liquidación

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Settlement Report Settings]**.

   ![Configuración del informe de liquidación de PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL SFTP Credentials]**, haga lo siguiente:

   - Si te has registrado en el servidor FTP seguro de PayPal, introduce las siguientes credenciales de inicio de sesión en el SFTP:

      - Iniciar sesión
      - Contraseña

   - Para ejecutar informes de prueba antes de publicar Payments Pro en su sitio, establezca **[!UICONTROL Sandbox Mode]** en `Yes`.

   - Escriba **[!UICONTROL Custom Endpoint Hostname or IP Address]**.

     De manera predeterminada, el valor es `reports.paypal.com`.

   - Escriba **[!UICONTROL Custom Path]** donde se guardan los informes.

     De manera predeterminada, el valor es `/ppreports/outgoing`.

1. Para generar informes de acuerdo con una programación, complete la configuración de **[!UICONTROL Scheduled Fetching]**:

   - Establezca **[!UICONTROL Enable Automatic Fetching]** en `Yes`.

   - Establezca **[!UICONTROL Schedule]** en una de las siguientes opciones:

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPal conserva cada informe durante 45 días.

   - Establezca **[!UICONTROL Time of Day]** a las horas, minutos y segundos en que desea que se generen los informes.

#### Configuración de experiencia de front-end

Use _[!UICONTROL Frontend Experience Settings]_&#x200B;para elegir los logotipos de PayPal que aparecerán en el sitio y personalizar el aspecto de las páginas de comerciantes de PayPal.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Frontend Experience Settings]**.

   ![Configuración de experiencia de front-end](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. Seleccione el(la) **[!UICONTROL PayPal Product Logo]** que desea que aparezca en el bloque de PayPal de su tienda.

   Los logotipos de PayPal están disponibles en cuatro estilos y dos tamaños:

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. Para personalizar el aspecto de las páginas de comerciantes de PayPal, haga lo siguiente:

   - Escriba el nombre de **[!UICONTROL Page Style]** que desea aplicar a sus páginas de comerciante de PayPal:

      - `paypal`: utiliza el estilo de página de PayPal.
      - `primary`: utiliza el estilo de página que identificó como estilo _principal_ en el perfil de la cuenta.
      - `your_custom_value`: utiliza un estilo de página de pago personalizado, que se especifica en el perfil de la cuenta.

   - Para **[!UICONTROL Header Image URL]**, escriba la dirección URL de la imagen que desea que aparezca en la esquina superior izquierda de la página de pago. El tamaño máximo de archivo es de 750 píxeles de ancho por 90 píxeles de alto.

     >[!NOTE]
     >
     >PayPal recomienda que la imagen resida en un servidor seguro (https). De lo contrario, un explorador podría advertir que _la página contiene elementos seguros y no seguros_.

   - Para establecer el color de las páginas, escriba el código hexadecimal de seis caracteres, sin el símbolo `#`, para cada uno de los siguientes elementos:

      - **[!UICONTROL Header Background Color]** - Color de fondo del encabezado de la página de pago.
      - **[!UICONTROL Header Border Color]** - Color para borde de dos píxeles alrededor del encabezado.
      - **[!UICONTROL Page Background Color]**: color de fondo de la página de pago y alrededor del encabezado y del formulario de pago.

### Paso 6: Completa la configuración básica de Pago y envío de PayPal Express

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Basic Settings - PayPal Express Checkout]**.

   ![Configuración básica de cierre de compra rápido](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Title]**, escribe un título que identifique este método de pago durante el cierre de compra.

   Se recomienda configurar el título en _PayPal_ para cada vista de tienda.

1. Si ofrece varias formas de pago, ingrese un número para **[!UICONTROL Sort Order]** a fin de determinar la secuencia en que se mostrará el proceso de pago y envío de PayPal Express cuando aparezca junto con las otras formas de pago.

   Este número es relativo a las otras formas de pago. (`0` = primero, `1` = segundo, `2` = tercero, etc.)

1. Establezca **[!UICONTROL Payment Action]** en una de las siguientes opciones:

   - `Authorization` - Aprueba la compra y suspende los fondos. La cantidad no se retira hasta que el comerciante _la capture_.
   - `Sale`: el importe de la compra se autoriza y se retira inmediatamente de la cuenta del cliente.

1. Para mostrar el botón _[!UICONTROL Check out with PayPal]_&#x200B;en la página de productos, establezca **[!UICONTROL Display on Product Details Page]**&#x200B;en `Yes`.

### Paso 7: Completa la configuración avanzada de Pago y envío de PayPal Express

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Advanced Settings]**.

   ![Configuración avanzada de cierre de compra rápido](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Display on Shopping Cart]** en `Yes`.

1. Establezca **[!UICONTROL Payment Applicable From]** en una de las siguientes opciones:

   - `All Allowed Countries`: los clientes de todos los [países](../getting-started/store-details.md#country-options) especificados en la configuración de su tienda pueden usar este método de pago.
   - `Specific Countries` - Después de elegir esta opción, aparece la lista _[!UICONTROL Payment from Specific Countries]_. Para seleccionar varios países, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada elemento.

1. Para escribir comunicaciones con el sistema de pago en el archivo de registro, establezca **[!UICONTROL Debug Mode]** en `Yes`.

   >[!NOTE]
   >
   >De acuerdo con las normas de seguridad de datos PCI, la información de la tarjeta de crédito no se registra en el archivo de registro.

1. Para habilitar la comprobación de la autenticidad del host, establezca **[!UICONTROL Enable SSL Verification]** en `Yes`.

1. Para mostrar un resumen completo del pedido del cliente por artículo de línea del sitio de PayPal, establezca **[!UICONTROL Transfer Cart Line Items]** en `Yes`.

1. Para permitir que el cliente complete la transacción desde el sitio de PayPal sin volver a su tienda para la revisión de pedidos, establezca **[!UICONTROL Skip Order Review Step]** en `Yes`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[3]: https://developer.paypal.com/docs/paypal-payments-pro/
