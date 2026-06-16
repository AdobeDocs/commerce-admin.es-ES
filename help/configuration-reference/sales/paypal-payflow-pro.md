---
title: '[!UICONTROL Sales] > [!UICONTROL Payment Methods] >  [!UICONTROL PayPal Payflow Pro]'
description: Revise la configuración en la sección [!UICONTROL PayPal Payflow Pro] de la página [!UICONTROL Sales] > [!UICONTROL Payment Methods] del administrador de Commerce.
exl-id: 2aae038b-15c0-452a-98bc-4d97efbb60f6
feature: Configuration, Payments
TQID: https://experienceleague.adobe.com/SovV7EIi-4M4i17HIInBHNaqum-YLSpGEnpfO-0ykAs
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 621
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] >  [!UICONTROL PayPal Payflow Pro]

>[!IMPORTANT]
>
>**Requisitos de PSD2:** <br/>
>A partir del 14 de septiembre de 2019, los bancos europeos podrían rechazar los pagos que no cumplan los requisitos de [PSD2](../../getting-started/compliance-payment-services-directive.md). Para cumplir con PSD2, [!DNL PayPal Payflow Pro] debe estar integrado con [!DNL Cardinal Commerce]. Para obtener más información, consulta [3-D Secure for Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

{{config}}

## [!UICONTROL Required Settings]

![Configuración requerida](./assets/paypal-payflow-pro-settings.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | Sitio web | (Opcional) Cualquier dirección de correo electrónico asociada a su cuenta comercial de PayPal. Las direcciones de correo electrónico distinguen entre mayúsculas y minúsculas y deben coincidir exactamente con las direcciones de la cuenta. |
| [!UICONTROL Partner] | Sitio web | Su ID de socio de PayPal, si corresponde. |
| [!UICONTROL Vendor] | Sitio web | Nombre de inicio de sesión de usuario de PayPal. |
| Usuario | Sitio web | El ID de otro usuario en tu cuenta PayPal. |
| [!UICONTROL Password] | Sitio web | La contraseña asociada a tu cuenta de PayPal. |
| [!UICONTROL Test Mode] | Sitio web | Cuando está activado, ejecuta PayPal Payflow Pro en un entorno de prueba. Desactive el modo de prueba cuando esté listo para &quot;publicar&quot; en el modo de producción. Opciones: `Yes` / `No` |
| [!UICONTROL Use Proxy] | Sitio web | Se puede utilizar un proxy para redirigir el tráfico cuando el cortafuegos del servidor impide el acceso directo al servidor de PayPal. Si procede, identifica el servidor proxy utilizado para establecer la conexión con el servidor PayPal. Opciones: `Yes` / `No` <br/><br/>Si está habilitado, establezca las opciones de proxy: <br/>**`Proxy Host`**- La dirección IP del host proxy.<br/>**`Proxy Port`**: número del puerto proxy. |
| [!UICONTROL Enable this Solution] | Sitio web | Determina si PayPal Payflow Pro está disponible para tus clientes como forma de pago. |
| [!UICONTROL Enable PayPal Credit] | Sitio web | Determina si el crédito de PayPal está disponible para los clientes como una opción de pago. |

{style="table-layout:auto"}

## [!UICONTROL Advertise PayPal Credit]

![Anunciar crédito de PayPal](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | Sitio web | El identificador de publicador asociado a tu cuenta de crédito de PayPal. |
| [!UICONTROL Get Publisher ID from PayPal] |  | Obtiene tu identificador de publicador de PayPal. |
| [!UICONTROL Home Page] | Sitio web | Determina la posición y el tamaño del titular [!DNL PayPal Credit] en la página principal. Opciones: <br/>**`Display`**: determina si se muestra un titular de [!DNL PayPal Credit] en la página principal de la tienda. Opciones: `Yes` / `No`<br/>**`Position`** - Determina la posición del titular [!DNL PayPal Credit] en la página principal. Opciones: encabezado (centro) / barra lateral (derecha) <br/>**`Size`**: determina el tamaño del titular [!DNL PayPal Credit] en la página principal. Opciones: `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | Sitio web | Determina la posición y el tamaño del titular [!DNL PayPal Credit] en las páginas de categoría. Opciones: (igual que para [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | Sitio web | Determina la posición y el tamaño del titular [!DNL PayPal Credit] en las páginas de productos. Opciones: (igual que para [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | Sitio web | Determina la posición y el tamaño del titular [!DNL PayPal Credit] en la página del carro de compras. Opciones: (igual que para [!UICONTROL Home Page]) |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings - PayPal Payflow Pro]

![Configuración básica](./assets/payment-methods-paypal-payflow-pro-basic-settings.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Title] | Vista de tienda | Un nombre que identifica a PayPal Payflow Pro como una forma de pago durante el proceso de pago. |
| [!UICONTROL Sort Order] | Vista de tienda | Un número que determina el orden en el que PayPal Payflow Pro aparece cuando aparece con otros métodos de pago durante el pago. |
| [!UICONTROL Payment Action] | Sitio web | Determina la acción realizada por PayPal cuando se envía un pedido. Opciones: <br/>**`Authorization`**- Aprueba la compra, pero suspende los fondos. La cantidad no se retira hasta que sea &quot;capturada&quot; por el comerciante.<br/>**`Sale`**: el importe de la compra se autoriza y se retira inmediatamente de la cuenta del cliente. |
| **[!UICONTROL Credit Card Settings]** |  |  |
| [!UICONTROL Allowed Credit Cart Types] | Sitio web | Determina las tarjetas de crédito disponibles para los clientes durante el cierre de compra. Seleccione cada tarjeta compatible. Opciones: `American Express` (requiere un acuerdo adicional) / `Visa` / `MasterCard` / `Discover` / `JCB` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![Configuración avanzada](./assets/payment-methods-paypal-payflow-pro-advanced-settings.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| Mostrar en el carro de compras | Vista de tienda | Determina si Pago y envío mediante PayPal Express aparece como una opción de pago en el carro de compras. Opciones: Sí (recomendado) / No |
| [!UICONTROL Payment Action Applicable From] | Sitio web | Determina el intervalo de la selección de país aplicable. Opciones: Todos los países permitidos / Países específicos |
| [!UICONTROL Countries Payment Applicable From] | Sitio web | Identifica cada país desde el que se acepta el pago. Solo los clientes con una dirección de facturación en un país seleccionado pueden realizar compras con esta forma de pago. |
| [!UICONTROL Debug Mode] | Sitio web | Registra los mensajes enviados entre tu tienda y el sistema de pago PayPal en un archivo de registro. Opciones: `Yes` / `No` <br/><br/>**_Nota:_** El archivo de registro está almacenado en el servidor y solo son accesibles para los desarrolladores. De acuerdo con las normas de seguridad de datos PCI, la información de la tarjeta de crédito no se registra en el archivo de registro. |
| [!UICONTROL Enable SSL Verification] | Sitio web | Habilita la verificación del certificado de seguridad del host. Opciones: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Sitio web | Muestra un resumen completo de los artículos de línea del carro de compras del cliente en el sitio de PayPal. Opciones: `Yes` / `No` |
| [!UICONTROL Skip Order Review Step] | Sitio web | Determina si los clientes pueden completar la transacción desde el sitio de PayPal o si deben regresar a su tienda y completar el paso de revisión de pedidos antes de enviar el pedido. Opciones: `Yes` / `No` |

{style="table-layout:auto"}
