---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL PayPal Payments Standard]'
description: Revise los ajustes de configuración en la [!UICONTROL PayPal Payments Standard] en la sección [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] de la administración de Commerce.
exl-id: 846d9b6f-92b9-4610-b894-625f67f4cff8
feature: Configuration, Payments
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '1314'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Payments Standard]

>[!IMPORTANT]
>
>**Requisitos de PSD2:**<br/>
>A partir del 14 de septiembre de 2019, los bancos europeos podrían rechazar los pagos que no cumplan [PSD 2](../../getting-started/compliance-payment-services-directive.md) requisitos. No se necesita ninguna acción para [!DNL PayPal Payments Standard] para cumplir con PSD2 porque todos los requisitos son manejados por PayPal.

{{config}}

## [!UICONTROL Required Settings]

![Configuración requerida](./assets/payment-methods-paypal-payments-standard-required.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | Sitio web | (Opcional) Cualquier dirección de correo electrónico asociada a su cuenta comercial de PayPal. Las direcciones de correo electrónico distinguen entre mayúsculas y minúsculas y deben coincidir exactamente con las direcciones de la cuenta. |
| [!UICONTROL Partner] | Sitio web | Su ID de socio de PayPal, si corresponde. |
| [!UICONTROL Vendor] | Sitio web | Nombre de inicio de sesión de usuario de PayPal. |
| Usuario | Sitio web | El ID de otro usuario en tu cuenta PayPal. |
| [!UICONTROL Password] | Sitio web | La contraseña asociada a tu cuenta de PayPal. |
| [!UICONTROL Test Mode] | Sitio web | Cuando está activado, ejecuta PayPal Payments Pro en un entorno de prueba. Desactive el modo de prueba cuando esté listo para &quot;publicar&quot; en el modo de producción. Opciones: `Yes` / `No` |
| [!UICONTROL Use Proxy] | Sitio web | Se puede utilizar un proxy para redirigir el tráfico cuando el cortafuegos del servidor impide el acceso directo al servidor de PayPal. Si procede, identifica el servidor proxy utilizado para establecer la conexión con el servidor PayPal. Opciones: `Yes` / `No` <br/><br/>Si está activada, defina las siguientes opciones: <br/>**`Proxy Host`**- La dirección IP del host proxy.<br/>**`Proxy Port`** - El número del puerto proxy. |
| [!UICONTROL Enable this Solution] | Sitio web | Determina si PayPal Payments Pro está disponible para tus clientes como forma de pago. |
| [!UICONTROL Enable PayPal Credit] | Sitio web | Determina si el crédito de PayPal está disponible para los clientes como una opción de pago. |

{:style=&quot;table-layout:auto&quot;}

## Anunciar crédito de PayPal

![Anunciar crédito de PayPal](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | Sitio web | El identificador de publicador asociado a tu cuenta de crédito de PayPal. |
| [!UICONTROL Get Publisher ID from PayPal] |  | Obtiene tu identificador de publicador de PayPal. |
| [!UICONTROL Home Page] | Sitio web | Determina la posición y el tamaño del [!DNL PayPal Credit] titular de la página principal. Opciones: <br/>**`Display`**- Determina si un [!DNL PayPal Credit] El banner se muestra en la página de inicio de la tienda. Opciones: `Yes` / `No`<br/>**`Position`** - Determina la posición del [!DNL PayPal Credit] titular de la página principal. Opciones: `Header (center)` / `Sidebar (right)` <br/>**`Size`**- Determina el tamaño del [!DNL PayPal Credit] titular de la página principal. Opciones: `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | Sitio web | Determina la posición y el tamaño del [!DNL PayPal Credit] titular en páginas de categoría. Opciones: (igual que para [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | Sitio web | Determina la posición y el tamaño del [!DNL PayPal Credit] titular en páginas de producto. Opciones: (igual que para [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | Sitio web | Determina la posición y el tamaño del [!DNL PayPal Credit] titular de la página del carro de compras. Opciones: (igual que para [!UICONTROL Home Page]) |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Basic Settings - PayPal Payments Standard]

![Configuración básica](./assets/paypal-standard-basic-settings.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Title] | Vista de tienda | Un nombre que identifica PayPal Payments Pro como forma de pago durante el proceso de pago. |
| [!UICONTROL Sort Order] | Vista de tienda | Un número que determina el orden en el que PayPal Payments Pro aparece cuando se pone en venta con otros métodos de pago durante el proceso de pago. |
| [!UICONTROL Payment Action] | Sitio web | Determina la acción realizada por PayPal cuando se envía un pedido. Opciones: <br/>**`Authorization`**- Aprueba la compra, pero suspende los fondos. La cantidad no se retira hasta que sea &quot;capturada&quot; por el comerciante.<br/>**`Sale`** - El importe de la compra se autoriza y se retira inmediatamente de la cuenta del cliente. |
| [!UICONTROL Credit Card Settings] |  |  |
| [!UICONTROL Allowed Credit Cart Types] | Sitio web | Determina las tarjetas de crédito disponibles para los clientes durante el cierre de compra. Seleccione cada tarjeta compatible. Opciones: `American Express` (requiere un acuerdo adicional) / `Visa` / `MasterCard` / `Discover` / `JCB` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Advanced Settings]

![Configuración avanzada](./assets/payment-methods-paypal-payment-standard-advanced.png)<!-- zoom -->

| Campo | Ámbito | Descripción |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | Vista de tienda | Determina si Pago y envío mediante PayPal Express aparece como una opción de pago en el carro de compras. Opciones: `Yes` (recomendado) / `No` |
| [!UICONTROL Payment Action Applicable From] | Sitio web | Determina el intervalo de la selección de país aplicable. Opciones: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | Sitio web | Identifica cada país desde el que se acepta el pago. Solo los clientes con una dirección de facturación en un país seleccionado pueden realizar compras con esta forma de pago. |
| [!UICONTROL Debug Mode] | Sitio web | Registra los mensajes enviados entre tu tienda y el sistema de pago PayPal en un archivo de registro. Opciones: `Yes` / `No` <br/><br/>**_Nota:_**El archivo de registro se almacena en el servidor y solo pueden acceder a él los desarrolladores. De acuerdo con las normas de seguridad de datos PCI, la información de la tarjeta de crédito no se registra en el archivo de registro. |
| [!UICONTROL Enable SSL Verification] | Sitio web | Habilita la verificación del certificado de seguridad del host. Opciones: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Sitio web | Muestra un resumen completo de los artículos de línea del carro de compras del cliente en el sitio de PayPal. Opciones: `Yes` / `No` |
| [!UICONTROL Transfer Shipping Options] | Sitio web | Incluye hasta diez opciones de envío en el sitio de PayPal. Opciones: `Yes` / `No` |
| [!UICONTROL Shortcut Buttons Flavor] | Vista de tienda | Determina el tipo de imagen utilizada para el botón de aceptación de PayPal. Opciones: <br/>**`Dynamic`**- (Recomendado) Muestra una imagen que se puede cambiar dinámicamente desde el servidor de PayPal.<br/>**`Static`** - Muestra una imagen estática que no se puede cambiar dinámicamente. |
| [!UICONTROL Enable PayPal Guest Checkout] | Sitio web | Permite a los clientes que no tengan cuentas de PayPal realizar compras con el Pago y envío de PayPal Express. Opciones: `Yes` / `No` |
| [!UICONTROL Require Customer's Billing Address] | Sitio web | Determina si se requiere la dirección de facturación del cliente. Opciones: `Yes` / `No` / `For Virtual Quotes Only` |
| [!UICONTROL Billing Agreement Signup] | Sitio web | Determina si los clientes pueden entrar en una [contrato facturación](../../stores-purchase/paypal-billing-agreements.md) con tu tienda. Opciones: <br/>**`Auto`**- El cliente puede suscribirse a un contrato de facturación durante el Pago y envío exprés.<br/>**`Ask Customer`** - Se pregunta al cliente si desea suscribirse a un acuerdo de facturación. <br/>**`Never`**- Los clientes no tienen la opción de suscribirse a un acuerdo de facturación. |
| [!UICONTROL Skip Order Review Step] | Sitio web | Determina si los clientes pueden completar la transacción desde el sitio de PayPal o si deben regresar a su tienda y completar el paso de revisión de pedidos antes de enviar el pedido. Opciones: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Billing Agreement Setting]

![Configuración del contrato de facturación](./assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png)<!-- zoom -->

| Campo | Ámbito | Descripción |
|--- |--- |--- |
| [!UICONTROL Enabled] | Sitio web | Cuando se habilita, los acuerdos de facturación aparecen a los clientes como una opción de pago durante el cierre de compra. Opciones: `Yes` / `No` |
| [!UICONTROL Title] | Vista de tienda | La etiqueta de la opción de acuerdo de facturación de PayPal que aparece como una opción de pago durante el cierre de compra. |
| [!UICONTROL Sort Order] | Vista de tienda | Determina el orden en que se enumeran los acuerdos de facturación con otros métodos de pago durante el cierre de compra. |
| [!UICONTROL Payment Action] | Sitio web | Determina cómo gestiona PayPal la transacción: Opciones: <br/>**`Authorization`**- Aprueba la compra, pero suspende los fondos. La cantidad no se retira hasta que sea &quot;capturada&quot; por el comerciante.<br/>**`Sale`** - El importe de la compra se autoriza y se retira inmediatamente de la cuenta del cliente. |
| [!UICONTROL Payment Applicable From] | Sitio web | Determina el intervalo de la selección de país aplicable. Opciones: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | Sitio web | Identifica cada país desde el que se acepta el pago. Solo los clientes con una dirección de facturación en un país seleccionado pueden realizar compras con esta forma de pago. |
| [!UICONTROL Debug Mode] | Sitio web | Registra la comunicación con el sistema de pago en un archivo de registro. Opciones: `Yes` / `No` <br/><br/>**_Nota:_**El archivo de registro se almacena en el servidor y solo pueden acceder a él los desarrolladores. De acuerdo con las normas de seguridad de datos PCI, la información de la tarjeta de crédito no se registra en el archivo de registro. |
| [!UICONTROL Enable SSL Verification] | Sitio web | Habilita un paso de verificación para que garantice que la transacción se realice a través de un canal SSL cifrado. Opciones: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Sitio web | Cuando está activada, muestra un resumen de los artículos de línea del carro de compras en la página de pagos de PayPal. Opciones: `Yes` / `No` |
| [!UICONTROL Allow in Billing Agreement Wizard] | Sitio web | Cuando está activada, los clientes pueden iniciar un acuerdo de facturación desde el panel de su cuenta de cliente. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Settlement Report Settings]

![Configuración del informe de liquidación](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Login] | Sitio web | Nombre de usuario necesario para iniciar sesión en el servidor FTP seguro de PayPal. |
| [!UICONTROL Password] | Sitio web | La contraseña necesaria para iniciar sesión en el servidor FTP seguro de PayPal. |
| [!UICONTROL Sandbox Mode] | Sitio web | Cuando está habilitado, ejecuta informes en un entorno de prueba antes de &quot;activarse&quot; en el entorno de producción. Opciones: `Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | Sitio web | Dirección URL donde se administran los informes de liquidación. Valor predeterminado: `reports.paypal.com` |
| [!UICONTROL Custom Path] | Sitio web | La ruta en la que se guardan los informes de liquidación en el servidor. Valor predeterminado: `/ppreports/outgoing` |
| [!UICONTROL Scheduled Fetching] |  |  |
| [!UICONTROL Enable Automatic Fetching] | Sitio web | Cuando está activado, obtiene los informes de liquidación automáticamente según lo programado. Opciones: `Yes` / `No` |
| [!UICONTROL Schedule] | Global | Determina la frecuencia con la que PayPal genera los informes de liquidación. Opciones: `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | Global | Determina la hora, los minutos y el segundo en que se generan los informes de liquidación. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Frontend Experience Settings]

![Configuración de experiencia de front-end](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | Vista de tienda | Determina el logotipo de PayPal que aparecerá en tu tienda. Hay cuatro estilos básicos en dos tamaños. Opciones: `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| [!UICONTROL PayPal Merchant Pages Style] |  |  |
| [!UICONTROL Page Style] | Vista de tienda | Determina el aspecto de la página de comerciante de PayPal. Valores permitidos: <br/>**`paypal`**- Utiliza el estilo de página PayPal.<br/>**`primary`** : Utiliza el estilo de página que identificó como el estilo &quot;principal&quot; en el perfil de la cuenta. <br/>**`your_custom_value`**: Utiliza un estilo de página de pago personalizado, que se especifica en el perfil de la cuenta. |
| [!UICONTROL Header Image URL] | Vista de tienda | Dirección URL de la imagen que aparece en la esquina superior izquierda de la página de cierre de compra. El tamaño máximo es de 750 x 90 píxeles. <br/><br/>**_Nota:_**PayPal recomienda que la imagen se almacene en un servidor seguro (https). De lo contrario, el navegador del cliente puede advertir que &quot;la página contiene elementos seguros y no seguros&quot;. |
| [!UICONTROL Header Image Background Color] | Vista de tienda | Los seis caracteres [color hexadecimal](https://en.wikipedia.org/wiki/Web_colors) código para el color de fondo del encabezado en la página de cierre de compra. Puede escribir el código en mayúsculas y minúsculas. |
| [!UICONTROL Header Image Border Color] | Vista de tienda | El código de color hexadecimal de seis caracteres para el borde de dos píxeles alrededor del encabezado. |
| [!UICONTROL Page Background Color] | Vista de tienda | El código de color hexadecimal de seis caracteres para el color de fondo de la página de pago que aparece detrás del encabezado y del formulario de pago. |

{:style=&quot;table-layout:auto&quot;}
