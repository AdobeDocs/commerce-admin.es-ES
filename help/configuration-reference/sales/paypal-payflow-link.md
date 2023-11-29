---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL PayPal Payflow Link]'
description: Revise los ajustes de configuración en la [!UICONTROL PayPal Payflow Link] en la sección [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] de la administración de Commerce.
exl-id: 5ea30b22-e251-4d93-be2c-d34138ef2f7d
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1330'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Payflow Link]

>[!IMPORTANT]
>
>**Requisitos de PSD2:** <br/>
>A partir del 14 de septiembre de 2019, los bancos europeos podrían rechazar los pagos que no cumplan [PSD 2](../../getting-started/compliance-payment-services-directive.md) requisitos. Para cumplir con el PSD 2, [!DNL PayPal Payflow Link] debe integrarse con [!DNL Cardinal Commerce]. Para obtener más información, consulte [3-D Secure for Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

{{config}}

## [!UICONTROL Required Settings]

![Configuración requerida](./assets/paypal-payflow-link-settings.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | Sitio web | (Opcional) Cualquier dirección de correo electrónico asociada a su cuenta comercial de PayPal. Las direcciones de correo electrónico distinguen entre mayúsculas y minúsculas y deben coincidir exactamente con las direcciones de la cuenta. |
| [!UICONTROL Partner] | Sitio web | Su ID de socio de PayPal, si corresponde. |
| [!UICONTROL Vendor] | Sitio web | Nombre de inicio de sesión de usuario de PayPal. |
| Usuario | Sitio web | El ID de un usuario extra en tu cuenta PayPal. Si no hay otros usuarios en la red, escriba su ID de proveedor o comerciante. |
| [!UICONTROL Password] | Sitio web | La contraseña asociada a tu cuenta de PayPal. |
| [!UICONTROL Test Mode] | Sitio web | Cuando está activado, ejecuta PayPal Payflow Pro en un entorno de prueba. Desactive el modo de prueba cuando esté listo para &quot;publicar&quot; en el modo de producción. Opciones: `Yes` / `No` |
| [!UICONTROL Use Proxy] | Sitio web | Se puede utilizar un proxy para redirigir el tráfico cuando el cortafuegos del servidor impide el acceso directo al servidor de PayPal. Si procede, identifica el servidor proxy utilizado para establecer la conexión con el servidor PayPal. Opciones: `Yes` / `No` <br/><br/>Si está activado, defina las opciones de proxy: <br/>**`Proxy Host`**- La dirección IP del host proxy.<br/>**`Proxy Port`** - El número del puerto proxy. |
| [!UICONTROL Enable Payflow Link] | Sitio web | Determina si PayPal Payflow Link está disponible para tus clientes como forma de pago. |
| [!UICONTROL Enable Express Checkout] | Sitio web | Determina si Pago y envío rápido de PayPal está disponible para tus clientes como forma de pago. |
| [!UICONTROL Enable PayPal Credit] | Sitio web | Determina si el crédito de PayPal está disponible para los clientes como una opción de pago. |

{style="table-layout:auto"}

## [!UICONTROL Advertise PayPal Credit]

![Anunciar crédito de PayPal](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | Sitio web | El identificador de publicador asociado a tu cuenta de crédito de PayPal. |
| [!UICONTROL Get Publisher ID from PayPal] |  | Obtiene tu identificador de publicador de PayPal. |
| [!UICONTROL Home Page] | Sitio web | Determina la posición y el tamaño del [!DNL PayPal Credit] titular de la página principal. Opciones: <br/>**`Display`**- Determina si un[!DNL PayPal Credit] El banner se muestra en la página de inicio de la tienda. Opciones: `Yes` / `No`<br/>**`Position`** - Determina la posición del [!DNL PayPal Credit] titular de la página principal. Opciones: Encabezado (centro) / Barra lateral (derecha) <br/>**`Size`**- Determina el tamaño del [!DNL PayPal Credit] titular de la página principal. Opciones: `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | Sitio web | Determina la posición y el tamaño del [!DNL PayPal Credit] titular en páginas de categoría. Opciones: (igual que para [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | Sitio web | Determina la posición y el tamaño del [!DNL PayPal Credit] titular en páginas de producto. Opciones: (igual que para [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | Sitio web | Determina la posición y el tamaño del [!DNL PayPal Credit] titular de la página del carro de compras. Opciones: (igual que para [!UICONTROL Home Page]) |

{style="table-layout:auto"}

### [!UICONTROL Basic Settings]

![Configuración básica](./assets/payment-methods-paypal-payflow-link-basic-settings.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Title] | Vista de tienda | Un nombre que identifica el vínculo de flujo de pago de PayPal como una forma de pago durante el pago. |
| [!UICONTROL Sort Order] | Vista de tienda | Un número que determina el orden en el que aparece PayPal Payflow Link cuando se pone en venta con otras formas de pago durante el proceso de pago. |
| [!UICONTROL Payment Action] | Sitio web | Determina la acción realizada por PayPal cuando se envía un pedido. Opciones: <br/>**`Authorization`**- Aprueba la compra, pero suspende los fondos. La cantidad no se retira hasta que sea &quot;capturada&quot; por el comerciante.<br/>**`Sale`** - El importe de la compra se autoriza y se retira inmediatamente de la cuenta del cliente. |

{style="table-layout:auto"}

### [!UICONTROL Advanced Settings]

![Configuración avanzada](./assets/payment-methods-paypal-payflow-link-advanced-settings.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Payment Applicable From] | Sitio web | Determina el intervalo de la selección de país aplicable. Opciones: Todos los países permitidos / Países específicos |
| [!UICONTROL Countries Payment Applicable From] | Sitio web | Identifica cada país desde el que se acepta el pago. Solo los clientes con una dirección de facturación en un país seleccionado pueden realizar compras con esta forma de pago. |
| [!UICONTROL Debug Mode] | Sitio web | Registra los mensajes enviados entre su tienda y el sistema de pago en un archivo de registro. Opciones: `Yes` / `No` <br/><br/>**_Nota:_**El archivo de registro se almacena en el servidor y solo pueden acceder a él los desarrolladores. De acuerdo con las normas de seguridad de datos PCI, la información de la tarjeta de crédito no se registra en el archivo de registro. |
| [!UICONTROL Enable SSL Verification] | Sitio web | Determina si el canal seguro del host está verificado antes de que se realice una transacción. Opciones: `Yes` / `No` |
| [!UICONTROL CVV Entry is Editable] | Sitio web | Determina si el cliente puede editar el CVV después de introducirlo. Opciones: `Yes` / `No` |
| [!UICONTROL Require CVV Entry] | Sitio web | Determina si los clientes deben ingresar el código CVV desde el reverso de su tarjeta de crédito. Opciones: `Yes` / `No` |
| [!UICONTROL Send Email Confirmation] | Sitio web | Determina si el cliente recibe una confirmación de pago por correo electrónico. Opciones: `Yes` / `No` |
| [!UICONTROL URL Method for Cancel  URL and Return URL] | Sitio web | Determina el método que se utiliza para intercambiar información con el servidor de PayPal durante una transacción. Opciones: <br/>**`GET`**: recupera información que es el resultado de un proceso. (Este es el método predeterminado).<br/>**`POST`** : envía un bloque de datos, como los datos introducidos en un formulario, al proceso de gestión de datos. |

{style="table-layout:auto"}

## [!UICONTROL Settlement Report Settings]

![Configuración del informe de liquidación](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| **[!UICONTROL SFTP Credentials]** |  |  |
| [!UICONTROL Login] | Sitio web | Nombre de usuario necesario para iniciar sesión en el servidor FTP seguro de PayPal. |
| [!UICONTROL Password] | Sitio web | La contraseña necesaria para iniciar sesión en el servidor FTP seguro de PayPal. |
| [!UICONTROL Sandbox Mode] | Sitio web | Cuando está habilitado, ejecuta informes en un entorno de prueba antes de &quot;activarse&quot; en el entorno de producción. Opciones: `Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | Sitio web | Dirección URL donde se administran los informes de liquidación. Valor predeterminado: `reports.paypal.com` |
| [!UICONTROL Custom Path] | Sitio web | La ruta en la que se guardan los informes de liquidación en el servidor. Valor predeterminado: `/ppreports/outgoing` |
| **[!UICONTROL Scheduled Fetching]** |  |  |
| [!UICONTROL Enable Automatic Fetching] | Sitio web | Cuando está activado, obtiene los informes de liquidación automáticamente según lo programado. Opciones: `Yes` / `No` |
| [!UICONTROL Schedule] | Global | Determina la frecuencia con la que PayPal genera los informes de liquidación. Opciones: `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | Global | Determina la hora, los minutos y el segundo en que se generan los informes de liquidación. |

{style="table-layout:auto"}

## [!UICONTROL Frontend Experience Settings]

![Configuración de experiencia de front-end](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | Vista de tienda | Determina el logotipo de PayPal que aparecerá en tu tienda. Hay cuatro estilos básicos en dos tamaños. Opciones: `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| Estilo de páginas de comerciante de PayPal |  |  |
| [!UICONTROL Page Style] | Vista de tienda | Determina el aspecto de la página de comerciante de PayPal. Valores permitidos: <br/>**`paypal`**- Utiliza el estilo de página PayPal.<br/>**`primary`** : Utiliza el estilo de página que identificó como el estilo &quot;principal&quot; en el perfil de la cuenta. <br/>**`your_custom_value`**: Utiliza un estilo de página de pago personalizado, que se especifica en el perfil de la cuenta. |
| [!UICONTROL Header Image URL] | Vista de tienda | Dirección URL de la imagen que aparece en la esquina superior izquierda de la página de cierre de compra. El tamaño máximo es de 750 x 90 píxeles. <br/><br/>**_Nota:_**PayPal recomienda que la imagen se almacene en un servidor seguro (https). De lo contrario, el navegador del cliente puede advertir que &quot;la página contiene elementos seguros y no seguros&quot;. |
| [!UICONTROL Header Image Background Color] | Vista de tienda | Los seis caracteres [color hexadecimal](https://en.wikipedia.org/wiki/Web_colors) código para el color de fondo del encabezado en la página de cierre de compra. Puede escribir el código en mayúsculas y minúsculas. |
| [!UICONTROL Header Image Border Color] | Vista de tienda | El código de color hexadecimal de seis caracteres para el borde de dos píxeles alrededor del encabezado. |
| [!UICONTROL Page Background Color] | Vista de tienda | El código de color hexadecimal de seis caracteres para el color de fondo de la página de pago que aparece detrás del encabezado y del formulario de pago. |

{style="table-layout:auto"}

### [!UICONTROL Basic Settings - PayPal Express Checkout]

![Configuración básica de pago y envío de PayPal Express](./assets/payment-methods-paypal-payflow-link-express-checkout-basic-settings.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Title] | Vista de tienda | Un nombre que identifica el método de pago Pago y envío de PayPal Express durante el pago y envío. |
| [!UICONTROL Sort Order] | Vista de tienda | Un número que determina el orden en el que aparece Pago y envío de PayPal Express cuando se pone en venta con otros métodos de pago durante el pago. Entrar `0` en la parte superior de la lista. |
| [!UICONTROL Payment Action] | Sitio web | Determina la acción realizada por PayPal cuando recibe un pedido. Opciones: <br/>**`Authorization`**- Aprueba la compra, pero suspende los fondos. La cantidad no se retira hasta que sea &quot;capturada&quot; por el comerciante.<br/>**`Sale`** - El importe de la compra se autoriza y se retira inmediatamente de la cuenta del cliente. <br/>**`Order`**- Representa un acuerdo con PayPal que permite al comerciante capturar una o más cantidades hasta el total pedido desde la cuenta de comprador del cliente, en un período de tiempo definido. Esto puede tardar hasta 29 días. Se deben generar una o más facturas desde el administrador de Commerce para capturar los fondos. |
| [!UICONTROL URL Display on Product Details Page] | Vista de tienda | Determina si aparece el botón &quot;Finalizar compra con PayPal&quot; en las páginas de productos. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Advanced Settings - PayPal Express Checkout]

![Configuración avanzada](./assets/payment-methods-paypal-payflow-link-express-checkout-advanced-settings.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | Vista de tienda | Determina si Pago y envío mediante PayPal Express aparece como una opción de pago en el carro de compras. Opciones: Sí (recomendado) / No |
| [!UICONTROL Payment Action Applicable From] | Sitio web | Determina el intervalo de la selección de país aplicable. Opciones: Todos los países permitidos / Países específicos |
| [!UICONTROL Countries Payment Applicable From] | Sitio web | Identifica cada país desde el que se acepta el pago. Solo los clientes con una dirección de facturación en un país seleccionado pueden realizar compras con esta forma de pago. |
| [!UICONTROL Debug Mode] | Sitio web | Registra los mensajes enviados entre tu tienda y el sistema de pago PayPal en un archivo de registro. Opciones: `Yes` / `No` <br/><br/>**_Nota:_**El archivo de registro se almacena en el servidor y solo pueden acceder a él los desarrolladores. De acuerdo con las normas de seguridad de datos PCI, la información de la tarjeta de crédito no se registra en el archivo de registro. |
| [!UICONTROL Enable SSL Verification] | Sitio web | Habilita la verificación del certificado de seguridad del host. Opciones: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Sitio web | Muestra un resumen completo de los artículos de línea del carro de compras del cliente en el sitio de PayPal. Opciones: `Yes` / `No` |
| [!UICONTROL Skip Order Review Step] | Sitio web | Determina si los clientes pueden completar la transacción desde el sitio de PayPal o si deben regresar a su tienda y completar el paso de revisión de pedidos antes de enviar el pedido. Opciones: `Yes` / `No` |

{style="table-layout:auto"}
