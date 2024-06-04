---
title: '[!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront]'
description: Revise la configuración de en [!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront] del Administrador de Commerce.
exl-id: 6c03ee68-7421-4c74-bdc1-0855f088b7f9
feature: Configuration, Security
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1283'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront]

>[!IMPORTANT]
>
>Antes de poder configurar Google reCAPTCHA, debe asegurarse de que su `PHP.ini` incluye la siguiente configuración: `allow_url_fopen = 1`. Esto puede requerir la asistencia del desarrollador. Consulte [Configuración de PHP](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) en el _Guía de instalación_.

{{config}}

Para obtener más información sobre el uso de Google reCAPTCHA para proteger su tienda, consulte Google [reCAPTCHA](../../systems/security-google-recaptcha.md) en el _Guía de sistemas de administración_.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 (&quot;No soy un robot&quot;)](./assets/recaptcha-storefront-v2-not-robot.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--|--|--|
| [!UICONTROL Google API Website Key] | Sitio web | Clave del sitio web que se crea al registrar la cuenta de Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Sitio web | La clave secreta asociada a su cuenta de Google reCAPTCHA. |
| [!UICONTROL Size] | Sitio web | El tamaño del cuadro reCAPTCHA de Google que aparece cuando un cliente inicia sesión en su cuenta. Opciones: `Normal` (predeterminado) / `Compact` |
| [!UICONTROL Theme] | Sitio web | Determina el estilo del cuadro reCAPTCHA de Google. Opciones: `Light Theme` (predeterminado) / `Dark Theme` |
| [!UICONTROL Language Code] | Vista de tienda | El [código de dos caracteres](https://developers.google.com/recaptcha/docs/language) que especifica el idioma que se utiliza para el texto y la mensajería reCAPTCHA de Google. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 invisible](./assets/recaptcha-storefront-v2-invisible.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--|--|--|
| [!UICONTROL Google API Website Key] | Sitio web | Clave del sitio web que se crea al registrar la cuenta de Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Sitio web | La clave secreta asociada a su cuenta de Google reCAPTCHA. |
| [!UICONTROL Invisible Badge Position] | Sitio web | La posición del distintivo reCAPTCHA invisible en cada página. Opciones: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Global | Determina el estilo del cuadro reCAPTCHA de Google. Opciones: `Light Theme` (predeterminado) / `Dark Theme` |
| [!UICONTROL Language Code] | Vista de tienda | A [código de dos caracteres](https://developers.google.com/recaptcha/docs/language) que especifica el idioma que se utiliza para el texto y la mensajería reCAPTCHA de Google. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 invisible](./assets/recaptcha-storefront-v3-invisible.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--|--|--|
| [!UICONTROL Google API Website Key] | Sitio web | Clave del sitio web que se crea al registrar la cuenta de Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Sitio web | La clave secreta asociada a su cuenta de Google reCAPTCHA. |
| [!UICONTROL Minimum Score Threshold] | Global | La puntuación mínima que identifica una interacción de usuario como un riesgo potencial, donde 1,0 es una interacción de usuario típica y 0,0 es probablemente un bot. Predeterminado: `0.5` |
| [!UICONTROL Invisible Badge Position] | Sitio web | La posición del distintivo reCAPTCHA invisible en cada página. Opciones: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Sitio web | Determina el estilo del cuadro reCAPTCHA de Google. Opciones: `Light Theme` (predeterminado) / `Dark Theme` |
| [!UICONTROL Language Code] | Vista de tienda | A [código de dos caracteres](https://developers.google.com/recaptcha/docs/language) que especifica el idioma que se utiliza para el texto y la mensajería reCAPTCHA de Google. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![Mensajes de error](./assets/recaptcha-storefront-failure-messages.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | Vista de tienda | El mensaje que se muestra en la tienda si la verificación falla. Texto predeterminado: `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | Vista de tienda | El mensaje que se muestra en la tienda si reCAPTCHA no devuelve un resultado de verificación. Texto predeterminado: `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![Tienda](./assets/recaptcha-storefront.png)<!-- zoom -->

>[!NOTE]
>
>El tipo de reCAPTCHA que elija debe coincidir con el tipo asociado a la clave de API de su cuenta de Google reCAPTCHA.

>[!WARNING]
>
>Cuando se utiliza la versión 3 de reCAPTCHA, un usuario auténtico con una puntuación baja no puede continuar. Para la versión 2, un usuario auténtico con una puntuación baja recibe un desafío. Considere detenidamente si los usuarios genuinos con una puntuación baja deben tener la oportunidad de resolver un desafío (versión 2) o de ser bloqueados (versión 3).

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--|--|--|
| [!UICONTROL Enable for Customer Login] | Sitio web | Especifica el tipo de reCAPTCHA que se utiliza cuando los clientes [iniciar sesión](../../customers/customer-sign-in.md) a sus cuentas. Opciones:<br/>**`No`**- (predeterminado) No valida la solicitud de inicio de sesión.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Requiere que el usuario seleccione _No soy un robot_ casilla de verificación <br />**`Invisible reCAPTCHA v2`**: valida el comportamiento del usuario en segundo plano sin requerir interacciones en función de la puntuación.<br/>**`Invisible reCAPTCHA v3`** : (recomendado) valida el comportamiento del usuario en segundo plano en función de la puntuación de interacción. |
| [!UICONTROL Enable for Forgot Password] | Sitio web | Especifica el tipo de reCAPTCHA que se utiliza cuando los clientes solicitan una [restablecimiento de contraseña](../../customers/password-reset.md). Opciones:<br/>**`No`**- (predeterminado) No valida la solicitud de restablecimiento de contraseña.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Requiere que el usuario seleccione _No soy un robot_ casilla de verificación <br />**`Invisible reCAPTCHA v2`**: valida el comportamiento del usuario en segundo plano sin requerir interacciones en función de la puntuación.<br/>**`Invisible reCAPTCHA v3`** : (recomendado) valida el comportamiento del usuario en segundo plano en función de la puntuación de interacción. |
| [!UICONTROL Enable for Create New Customer Account] | Sitio web | Especifica el tipo de reCAPTCHA que se utiliza cuando el cliente se suscribe a un [nueva cuenta](../../customers/account-create.md). Opciones:<br/>**`No`**- (predeterminado) No valida la solicitud de cuenta.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Requiere que el usuario seleccione _No soy un robot_ casilla de verificación <br />**`Invisible reCAPTCHA v2`**: valida el comportamiento del usuario en segundo plano sin requerir interacciones en función de la puntuación.<br/>**`Invisible reCAPTCHA v3`** : (recomendado) valida el comportamiento del usuario en segundo plano en función de la puntuación de interacción. |
| [!UICONTROL Enable for Edit Customer Account] | Sitio web | Especifica el tipo de reCAPTCHA que se utiliza cuando el cliente cambia su [información de cuenta](../../customers/account-dashboard-account-information.md). Opciones:<br/>**`No`**- (predeterminado) No valida la solicitud de cuenta.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Requiere que el usuario seleccione _No soy un robot_ casilla de verificación <br />**`Invisible reCAPTCHA v2`**: valida el comportamiento del usuario en segundo plano sin requerir interacciones en función de la puntuación.<br/>**`Invisible reCAPTCHA v3`** : (recomendado) valida el comportamiento del usuario en segundo plano en función de la puntuación de interacción. |
| [!UICONTROL Enable for Create New Company Account] | Sitio web | ![Adobe Commerce B2B](../../assets/b2b.svg) (Disponible solo con Adobe Commerce B2B) Especifica el tipo de reCAPTCHA que se utiliza cuando se crea un nuevo [cuenta de empresa](../../b2b/account-company-create.md) se ha creado. Opciones:<br/>**`No`**- (predeterminado) No valida la solicitud de cuenta.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Requiere que el usuario seleccione _No soy un robot_ casilla de verificación <br />**`Invisible reCAPTCHA v2`**: valida el comportamiento del usuario en segundo plano sin requerir interacciones en función de la puntuación.<br/>**`Invisible reCAPTCHA v3`** : (recomendado) valida el comportamiento del usuario en segundo plano en función de la puntuación de interacción. |
| [!UICONTROL Enable for Contact Us] | Sitio web | Especifica el tipo de reCAPTCHA que se utiliza para enviar un mensaje desde el [Contáctenos.](../../getting-started/store-details.md#contact-us-form) de su tienda. Opciones:<br/>**`No`**- (predeterminado) No valida la solicitud de mensaje.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Requiere que el usuario seleccione _No soy un robot_ casilla de verificación <br />**`Invisible reCAPTCHA v2`**: valida el comportamiento del usuario en segundo plano sin requerir interacciones en función de la puntuación.<br/>**`Invisible reCAPTCHA v3`** : (recomendado) valida el comportamiento del usuario en segundo plano en función de la puntuación de interacción. |
| [!UICONTROL Enable for Product Review] | Sitio web | Especifica el tipo de reCAPTCHA que se utiliza cuando los clientes envían una [reseña del producto](../../merchandising-promotions/product-reviews.md). Opciones:<br/>**`No`**- (predeterminado) No valida la solicitud de revisión del producto.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Requiere que el usuario seleccione _No soy un robot_ casilla de verificación <br />**`Invisible reCAPTCHA v2`**: valida el comportamiento del usuario en segundo plano sin requerir interacciones en función de la puntuación.<br/>**`Invisible reCAPTCHA v3`** : (recomendado) valida el comportamiento del usuario en segundo plano en función de la puntuación de interacción. |
| [!UICONTROL Enable for Newsletter Subscription] | Sitio web | Especifica el tipo de reCAPTCHA invisible que se utiliza cuando los clientes se suscriben a un [suscripción al boletín informativo](../../merchandising-promotions/newsletter-subscribers.md). Opciones:<br/>**`No`**- (predeterminado) No valida la solicitud de suscripción al boletín informativo.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Requiere que el usuario seleccione _No soy un robot_ casilla de verificación <br />**`Invisible reCAPTCHA v2`**: valida el comportamiento del usuario en segundo plano sin requerir interacciones en función de la puntuación.<br/>**`Invisible reCAPTCHA v3`** : (recomendado) valida el comportamiento del usuario en segundo plano en función de la puntuación de interacción. |
| [!UICONTROL Enable for Gift Card] | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Solo Adobe Commerce) Especifica el tipo de reCAPTCHA que se utiliza cuando los clientes escriben un [tarjeta regalo](../../catalog/product-gift-card-create.md) código. Opciones:<br/>**`No`**- (predeterminado) No valida el envío del código de la tarjeta regalo.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Requiere que el usuario seleccione _No soy un robot_ casilla de verificación <br />**`Invisible reCAPTCHA v2`**: valida el comportamiento del usuario en segundo plano sin requerir interacciones según la puntuación.<br/>**`Invisible reCAPTCHA v3`** : (recomendado) valida el comportamiento del usuario en segundo plano en función de la puntuación de interacción. |
| [!UICONTROL Enable for Invitation Create Account] | Sitio web | Especifica el tipo de reCAPTCHA que se utiliza cuando los clientes envían una creación de cuenta [invitación](../../merchandising-promotions/invitations.md) código. Opciones:<br/>**`No`**- (predeterminado) No valida el envío del correo electrónico de invitación.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Requiere que el usuario seleccione _No soy un robot_ casilla de verificación <br />**`Invisible reCAPTCHA v2`**: valida el comportamiento del usuario en segundo plano sin requerir interacciones según la puntuación.<br/>**`Invisible reCAPTCHA v3`** : (recomendado) valida el comportamiento del usuario en segundo plano en función de la puntuación de interacción. |
| [!UICONTROL Enable for Send to Friend] | Sitio web | Especifica el tipo de reCAPTCHA que se utiliza cuando los clientes [compartir un producto](../../stores-purchase/email-a-friend.md) con un amigo. Opciones:<br/>**`No`**: (predeterminado) no valida el envío de correo electrónico.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Requiere que el usuario seleccione _No soy un robot_ casilla de verificación <br />**`Invisible reCAPTCHA v2`**: valida el comportamiento del usuario en segundo plano sin requerir interacciones en función de la puntuación.<br/>**`Invisible reCAPTCHA v3`** : (recomendado) valida el comportamiento del usuario en segundo plano en función de la puntuación de interacción. |
| [!UICONTROL Enable for Wishlist Sharing] | Sitio web | Especifica el tipo de reCAPTCHA que se utiliza cuando los clientes [compartir una lista de deseos](../../stores-purchase/wishlist-storefront.md#share-the-wish-list). Opciones:<br/>**`No`**: (predeterminado) no valida el envío de mensajes y correos electrónicos.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Requiere que el usuario seleccione _No soy un robot_ casilla de verificación <br />**`Invisible reCAPTCHA v2`**: valida el comportamiento del usuario en segundo plano sin requerir interacciones según la puntuación.<br/>**`Invisible reCAPTCHA v3`** : (recomendado) valida el comportamiento del usuario en segundo plano en función de la puntuación de interacción. |
| [!UICONTROL Enable for Coupon Codes] | Sitio web | Especifica el tipo de reCAPTCHA que se utiliza cuando los clientes escriben una [código de cupón](../../merchandising-promotions/price-rules-cart-coupon.md). Opciones:<br/>**`No`**: (predeterminado) No valida el envío del código de cupón.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Requiere que el usuario seleccione _No soy un robot_ casilla de verificación <br />**`Invisible reCAPTCHA v2`**: valida el comportamiento del usuario en segundo plano sin requerir interacciones según la puntuación.<br/>**`Invisible reCAPTCHA v3`** : (recomendado) valida el comportamiento del usuario en segundo plano en función de la puntuación de interacción. |
| [!UICONTROL Enable for PayPal Payflow Pro payment form] | Sitio web | Especifica el tipo de reCAPTCHA que se utiliza cuando los clientes pagan una compra con [PayPal Payflow Pro](../../stores-purchase/paypal-payflow-pro.md). Opciones:<br/>**`No`**- (predeterminado) No valida la solicitud de restablecimiento de contraseña.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Requiere que el usuario seleccione _No soy un robot_ casilla de verificación <br />**`Invisible reCAPTCHA v2`**: valida el comportamiento del usuario en segundo plano sin requerir interacciones en función de la puntuación.<br/>**`Invisible reCAPTCHA v3`** : (recomendado) valida el comportamiento del usuario en segundo plano en función de la puntuación de interacción. |

{style="table-layout:auto"}
