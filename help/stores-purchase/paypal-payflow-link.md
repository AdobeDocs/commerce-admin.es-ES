---
title: Vínculo de flujo de pago PayPal
description: Aprenda a configurar PayPal Payflow Link como solución de pago en línea en su tienda.
exl-id: dba4057e-1fea-4a23-8594-cc85f619d664
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2172'
ht-degree: 0%

---

# Vínculo de flujo de pago PayPal

PayPal Payflow Link solo está disponible para comerciantes de Estados Unidos y Canadá. Los clientes no tienen que tener una cuenta personal de PayPal e introducir la información de su tarjeta de crédito en un formulario alojado por PayPal. La información nunca se almacena en el servidor de Adobe Commerce o de Magento Open Source. El vínculo de flujo de pago no se puede utilizar para pedidos creados desde el administrador.

Las notas de abono son compatibles con los reembolsos en línea y sin conexión. Sin embargo, no se admiten varios reembolsos en línea.

>[!IMPORTANT]
>
>**Requisitos de PSD2:** <br/>
>A partir del 14 de septiembre de 2019, los bancos europeos podrían rechazar los pagos que no cumplan [PSD 2](../getting-started/compliance-payment-services-directive.md) requisitos. Para cumplir con PSD2, PayPal Payflow Link debe estar integrado con Cardinal Commerce. Para obtener más información, consulte [3-D Secure for Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

## Requisitos

- [Cuenta comercial de PayPal][1] La pasarela PayPal Payflow Pro vincula la cuenta de comerciante en PayPal con el sitio web del comerciante, actuando como pasarela y cuenta de comerciante.

- Si administra varios sitios web de Commerce, debe tener una cuenta de comerciante de PayPal independiente para cada sitio web.

## Flujo de trabajo del cliente

1. **El cliente va al cierre de compra** - Durante el proceso de pago, el cliente elige pagar con el enlace PayPal Payflow e introduce la información de la tarjeta de crédito. El cliente no tiene que tener una cuenta personal de PayPal.
1. **El cliente elige Pagar ahora** - El cliente pulsa el botón Pagar ahora para enviar el pedido.
1. **El cliente introduce la información de tarjeta de crédito** - El cliente introduce la información de la tarjeta de crédito en un formulario alojado en PayPal. Si el cliente hace clic _Cancelar pago_ , el cliente vuelve a la fase de información de pago del cierre de compra y el estado del pedido cambia a _Cancelado_.
1. **El cliente envía el pedido** - La información de la tarjeta de crédito se envía directamente a PayPal y no se conserva en ningún lugar del sitio de comercio.

## Flujo de trabajo de pedidos

1. **PayPal recibe una solicitud** - PayPal recibe la solicitud del cliente para pagar ahora.
1. **PayPal verifica la información de pago** - PayPal verifica la información de la tarjeta de crédito y asigna el estado apropiado:
   - **Pago verificado:** Si se verifica, la variable _Pendiente de pago_ El estado se asigna inicialmente al pedido hasta que se liquida la transacción.
   - **Procesando** - La transacción se realizó correctamente.
   - **Pendiente de pago** - El sistema no recibió una respuesta de PayPal.
   - **Cancelado** - La transacción no tuvo éxito por alguna razón.
   - **Sospecha de fraude** - La transacción no pasó algunos de los [Filtros de fraude de PayPal](paypal.md#paypal-fraud-management-filters). El sistema recibe la respuesta de PayPal de que el servicio de fraude está revisando la transacción.
   - **Cancelar pago:** Si el cliente hace clic _Cancelar pago_ , el cliente vuelve a la fase de información de pago del cierre de compra y el estado del pedido cambia a _Cancelado_.
1. **Se redirige al cliente a la página de confirmación**  - Si la transacción se completa correctamente, se redirige al cliente a la página de confirmación de pedido de su tienda. Si la transacción falla por cualquier motivo, aparece un mensaje de error en la página de pago y se indica al cliente que repita el proceso de pago. PayPal gestiona estas situaciones.
1. **El comerciante cumple la orden** - El comerciante factura y envía el pedido como de costumbre.

## Configurar tu cuenta PayPal

1. Inicie sesión en su [Cuenta comercial de PayPal][2].

1. Configure las variables [Páginas de cierre de compra alojadas][4] Usar el Administrador de PayPal con la siguiente configuración:

   - En **[!UICONTROL Security Options]**, complete la siguiente configuración:

     **[!UICONTROL AVS]**: `No`

     **[!UICONTROL CSC]**: `No`

     **[!UICONTROL Enable Secure Token]**: `Yes`

   - Elegir **[!UICONTROL Customize]** y, a continuación, elija **[!UICONTROL Layout C]**.

     El diseño C solo muestra los campos de tarjeta de crédito y débito, y puede enmarcarse en su sitio o utilizarse como ventana emergente independiente. El tamaño se fija en 490 x 565 píxeles, con espacio adicional para mensajes de error. En algunos sistemas, esta configuración corrige un problema con la redirección transparente.

1. Cuando haya completado la configuración, haga clic en **[!UICONTROL Save and Publish]**.

1. Configurar un usuario adicional (recomendado por PayPal):

   - En la segunda fila del menú principal, haga clic en **[!UICONTROL Manage Users]**.

   - Para agregar otro usuario a la cuenta, haga clic en **[!UICONTROL Add User]**.

   - Rellene los campos obligatorios en las siguientes secciones de la _Añadir usuario_ formulario:

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - Haga clic **[!UICONTROL Update]**.

## Configuración del vínculo de flujo de pago de PayPal

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

1. Expandir **[!UICONTROL PayPal Payment Gateways]** (si es necesario) y haga clic en **[!UICONTROL Configure]** para **[!UICONTROL Payflow Link]**.

   ![Vínculo de flujo de pago: Configurar](./assets/payflow-link.png){width="600" zoomable="yes"}

### Paso 2: Completa la configuración de PayPal necesaria

![Configuración de PayPal requerida: vínculo de flujo de pago de PayPal](./assets/payflow-required-link.png){width="600" zoomable="yes"}

1. (Opcional) Introduzca el **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >Las direcciones de correo electrónico distinguen entre mayúsculas y minúsculas. Para recibir el pago, la dirección de correo electrónico debe coincidir con la especificada en tu cuenta comercial de PayPal.

1. Introduzca una de las siguientes credenciales que utiliza para iniciar sesión en su cuenta de comerciante de PayPal:

   - **[!UICONTROL Partner]** - Tu ID de socio de PayPal.
   - **[!UICONTROL User]** - El ID de otro usuario que esté configurado en tu cuenta PayPal.
   - **[!UICONTROL Vendor]** - Tu nombre de usuario de PayPal.

1. Introduzca el **[!UICONTROL Password]** que está asociado con tu cuenta PayPal.

1. Para ejecutar transacciones de prueba, establezca **[!UICONTROL Test Mode]** hasta `Yes`.

   Al probar la configuración en una zona protegida, utilice solo [números de tarjeta de crédito][3] que recomienda PayPal. Cuando esté listo para ir a producción, vuelva a la configuración y establezca el Modo de prueba en `No`.

1. Si su sistema utiliza un servidor proxy para establecer la conexión con el sistema PayPal, establezca **[!UICONTROL Test Mode]** hasta `Yes` y haga lo siguiente:

   - Introduzca la dirección IP del **[!UICONTROL Proxy Host]**.

   - Introduzca el número de puerto del **[!UICONTROL Proxy Port]**.

     Se utiliza un proxy cuando el cortafuegos del servidor impide el acceso directo al servidor de PayPal. En tal caso, se utiliza un servidor de terceros para transmitir el tráfico.

1. Establecer **[!UICONTROL Enable Payflow Link]** hasta `Yes`.

1. Si desea activar [Pago y envío con PayPal Express](paypal-express-checkout.md) opciones para clientes, definir **[!UICONTROL Enable Express Checkout]** hasta `Yes`.

1. Si desea ofrecer [Crédito de PayPal](paypal.md#paypal-credit-and-pay-later) a sus clientes, configure **[!UICONTROL Enable PayPal Credit]** hasta `Yes`.

### Paso 3: Configurar el crédito de PayPal / Anunciar PayPal PayAfter (opcional)

A partir de la versión 2.4.3, PayPal PayAfter es compatible con las implementaciones que incluyen PayPal. Esta función permite a los compradores pagar un pedido en cuotas quincenales en lugar de pagar el importe completo en el momento de la compra. La experiencia de crédito de PayPal está en desuso.

Establecer **[!UICONTROL Enable PayPal PayLater Experience]** a uno de los siguientes:

- `Yes` - Para configurar Anunciar PayPal PayAfter
- `No` - Para configurar el crédito de PayPal publicitario

#### Anunciar crédito de PayPal

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Advertise PayPal Credit]** sección.

   ![Anunciar crédito de PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. Para obtener la información de la cuenta, haga clic en **[!UICONTROL Get Publisher ID from PayPal]** y siga las instrucciones.

1. Introduzca su **[!UICONTROL Publisher ID]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Home Page]** sección.

   ![Ajustes de la página de inicio de crédito de PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

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

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) Utilice las secciones restantes y repita los pasos anteriores para la configuración de la página principal:

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
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### Paso 4: completar la configuración básica

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Basic Settings - PayPal Payflow Link]** sección.

   ![Configuración básica: vínculo PayPal Payflow](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-basic-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Title]**, introduce un título que identifique el vínculo de Payflow de PayPal durante el proceso de pago.

   Se recomienda utilizar el título _Tarjeta de débito o crédito_.

1. Si ofreces varias formas de pago, introduce un número para **[!UICONTROL Sort Order]** para determinar la secuencia en la que aparece Vínculo de flujo de pago cuando se enumera con los demás métodos de pago.

   Este número es relativo a las otras formas de pago. (`0` = primero, `1` = segundo, `2` = tercero, etc.)

1. Establecer **[!UICONTROL Payment Action]** a uno de los siguientes:

   - `Authorization` - Aprueba la compra y suspende los fondos. La cantidad no se retira hasta que sea capturada por el comerciante.
   - `Sale` - El importe de la compra se autoriza y se retira inmediatamente de la cuenta del cliente.

### Paso 5: Completar la configuración avanzada

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Advanced Settings]** sección.

   ![Configuración avanzada - PayPal Payflow Link](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-advanced-settings.png){width="600" zoomable="yes"}

1. Establecer **[!UICONTROL Payment Applicable From]** a uno de los siguientes:

   - `All Allowed Countries` - Clientes de todos [países](../getting-started/store-details.md#country-options) especificado en la configuración de tu tienda puede utilizar este método de pago.
   - `Specific Countries` : Después de elegir esta opción, el _[!UICONTROL Payment from Specific Countries]_aparece una lista. Mantenga pulsada la tecla Ctrl y seleccione cada país de la lista donde los clientes puedan realizar compras en su tienda.

1. Para escribir comunicaciones con el sistema de pago en el fichero de registro, defina **[!UICONTROL Debug Mode]** hasta `Yes`.

   >[!NOTE]
   >
   >De acuerdo con las normas de seguridad de datos PCI, la información de la tarjeta de crédito no se registra en el archivo de registro.

1. Para habilitar la verificación de autenticidad del host, establezca **[!UICONTROL Enable SSL Verification]** hasta `Yes`.

1. Si desea que el cliente pueda corregir la entrada del código de seguridad CVV de tres dígitos desde el reverso de una tarjeta de crédito, establezca **[!UICONTROL CVV Entry is Editable]** hasta `Yes`.

1. Para exigir a los clientes que introduzcan un código CVV, establezca **[!UICONTROL Require CVV Entry]** hasta `Yes`.

1. Para enviar una confirmación del pago al cliente, configure **[!UICONTROL Send Email Confirmation]** hasta `Yes`.

1. Para determinar el método que se utiliza para intercambiar información con el servidor de PayPal durante una transacción, establezca el **[!UICONTROL URL method for Cancel URL and Return URL]** a uno de los siguientes:

   - `GET` : recupera información que es el resultado de un proceso (método predeterminado).
   - `POST` : proporciona un bloque de datos, como los datos introducidos en un formulario, a un proceso de administración de datos.

   El _URL de cancelación_ y _URL de retorno_ consulte la página donde el cliente vuelve después de completar o cancelar la parte de pago del proceso de pago en el servidor de PayPal

1. Complete las siguientes secciones, según sea necesario para su tienda:

   - [Configuración del informe de liquidación](#settlement-report-settings)
   - [Configuración de experiencia de front-end](#frontend-experience-settings)

#### Configuración del informe de liquidación

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Settlement Report Settings]** sección.

   ![Configuración del informe de liquidación - PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

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

   ![Configuración de experiencia de front-end - PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

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

### Paso 6: Completa la configuración básica de Pago y envío de PayPal Express

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Basic Settings - PayPal Express Checkout]** sección.

   ![Configuración básica](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Title]**, introduce un título que identifique esta forma de pago durante el proceso de pago.

   Configuración del título en _PayPal_ se recomienda para cada vista de tienda.

1. Si ofreces varias formas de pago, introduce un número para **[!UICONTROL Sort Order]** para determinar la secuencia en la que aparece Pago y envío de PayPal Express cuando se pone en venta con las otras formas de pago.

   Este número es relativo a las otras formas de pago. (`0` = primero, `1` = segundo, `2` = tercero, etc.)

1. Establecer **[!UICONTROL Payment Action]** a uno de los siguientes:

   - `Authorization` - Aprueba la compra y suspende los fondos. El importe no se retira hasta que se _capturado_ por el comerciante.
   - `Sale` - El importe de la compra se autoriza y se retira inmediatamente de la cuenta del cliente.

1. Para mostrar el _[!UICONTROL Check out with PayPal]_botón en la página de producto, establecer **[!UICONTROL Display on Product Details Page]**hasta `Yes`.

### Paso 7: Completa la configuración avanzada de Pago y envío de PayPal Express

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Advanced Settings]** sección.

   ![Configuración avanzada](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. Establecer **[!UICONTROL Display on Shopping Cart]** hasta `Yes`.

1. Establecer **[!UICONTROL Payment Applicable From]** a uno de los siguientes:

   - `All Allowed Countries` - Los clientes de todos los países especificados en la configuración de su tienda pueden utilizar este método de pago.
   - `Specific Countries` : Después de elegir esta opción, el _[!UICONTROL Payment from Specific Countries]_aparece una lista. Para seleccionar varios países, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada elemento.

1. Para escribir comunicaciones con el sistema de pago en el fichero de registro, defina **[!UICONTROL Debug Mode]** hasta `Yes`.

   >[!NOTE]
   >
   >De acuerdo con las normas de seguridad de datos PCI, la información de la tarjeta de crédito no se registra en el archivo de registro.

1. Para habilitar la verificación de autenticidad del host, establezca **[!UICONTROL Enable SSL Verification]** hasta `Yes`.

1. Para mostrar un resumen completo del pedido del cliente por artículo de línea desde el sitio de PayPal, establezca **[!UICONTROL Transfer Cart Line Items]** hasta `Yes`.

1. Para permitir que el cliente complete la transacción desde el sitio de PayPal sin volver a su tienda para la revisión del pedido, establezca **[!UICONTROL Skip Order Review Step]** hasta `Yes`.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/integration-guide/configure-hosted-checkout/#configuring-hosted-pages-using-paypal-manager
