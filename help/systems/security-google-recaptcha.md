---
title: Google reCAPTCHA
description: Obtenga información sobre cómo configurar Google reCAPTCHA para el acceso de administrador y varias acciones de tienda iniciadas por clientes registrados.
exl-id: c3b53702-0882-4ac4-9cf5-39fefc90005e
role: Admin
feature: Configuration, Security
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '1061'
ht-degree: 0%

---

# Google reCAPTCHA

[Google reCAPTCHA](https://developers.google.com/recaptcha) garantiza que un ser humano, en lugar de un equipo (o &quot;bot&quot;), interactúe con su sitio web. A diferencia de Adobe Commerce estándar y Magento Open Source [CAPTCHA](security-captcha.md), Google reCAPTCHA proporciona seguridad mejorada con una selección de diferentes opciones y métodos de visualización. Encontrará información adicional sobre el tráfico del sitio web en el panel de su cuenta de Google reCAPTCHA.

Google reCAPTCHA se configura por separado para el administrador y la tienda.

- Para el administrador, se puede usar Google reCAPTCHA en la página [Iniciar sesión](../getting-started/admin-signin.md) y cuando un usuario solicite un restablecimiento de contraseña. Si el Commerce [CAPTCHA](security-captcha.md) estándar también está habilitado, Google reCAPTCHA se puede usar al mismo tiempo sin ningún problema.

- Para la tienda, se puede usar Google reCAPTCHA para iniciar sesión en una [cuenta de cliente](../customers/customer-sign-in.md), enviar un mensaje desde la página de [Contáctenos](../getting-started/store-details.md#contact-us-form) y en muchas otras ubicaciones de tiendas.

  ![Google reCAPTCHA - inicio de sesión del cliente](./assets/customer-account-login-recaptcha.png){width="700" zoomable="yes"}

Google reCAPTCHA se puede implementar de varias formas:

- _reCAPTCHA v3 invisible_: utiliza un algoritmo para valorar las interacciones del usuario y determina la probabilidad de que el usuario sea humano en función de una puntuación.

- _reCAPTCHA v2 invisible_: realiza una verificación en segundo plano sin la interacción del usuario. Los usuarios y clientes se verifican automáticamente, pero es posible que tengan que seleccionar imágenes específicas para completar un desafío.

- _reCAPTCHA v2 (&quot;No soy un robot&quot;)_ — Valida las solicitudes con la casilla de verificación _&quot;No soy un robot&quot;_.

>[!IMPORTANT]
>
>Antes de configurar Google reCAPTCHA, asegúrese de que el archivo `PHP.ini` incluya la siguiente configuración: `allow_url_fopen = 1`. Esto puede requerir la asistencia del desarrollador. Consulte [Configuración de PHP requerida](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html?lang=es){:target="_blank"} en la Guía de instalación.

## Paso 1: Generar claves reCAPTCHA de Google

Google reCAPTCHA requiere un par de claves API para habilitarlo. Puede obtener estas claves de forma gratuita a través del sitio reCAPTCHA. Antes de generar las claves, debe conocer el tipo de reCAPTCHA que desea utilizar.

1. Abra la página Google reCAPTCHA e inicie sesión en su cuenta.

1. Para **[!UICONTROL Label]**, escriba un nombre para identificar las claves para la referencia interna.

   Necesita un conjunto de claves para cada tipo de reCAPTCHA que se utilice en la instalación de Adobe Commerce o Magento Open Source. Por ejemplo: `Commerce Invisible`

1. Para **[!UICONTROL reCAPTCHA type]**, elija el método que desee usar.

   - _reCAPTCHA v3 invisible_
   - _reCAPTCHA v2 invisible_
   - _reCAPTCHA v2 (&quot;No soy un robot&quot;)_

1. Para **[!UICONTROL Domain]**, escribe el dominio de tu tienda. Por ejemplo: mystore.com

   Si tiene varios almacenes con distintos dominios, introduzca cada dominio en una línea independiente.

   - Añada el dominio de almacén y los subdominios.
   - Puede agregar `localhost`, otros dominios de VM local y dominios de ensayo según sea necesario para realizar pruebas.

1. Seleccione la casilla para **[!UICONTROL Accept the reCAPTCHA Terms of Service]**.

1. (Opcional) Seleccione la casilla de verificación **[!UICONTROL Send alerts to owners]** para enviar una notificación si Google detecta problemas o tráfico sospechoso.

1. Haga clic en **[!UICONTROL Submit]** para completar el registro y recibir las claves.

   >[!IMPORTANT]
   >
   >No todas las claves son aplicables a todos los tipos de reCAPTCHA, y su aplicación incorrecta podría provocar un comportamiento inesperado. Por ejemplo, las claves reCAPTCHA de Google generadas para reCAPTCHA v2 &quot;No soy un robot&quot; no funcionan con _reCAPTCHA v2 invisible_ y podrían bloquear la funcionalidad donde reCAPTCHA está habilitado.

## Paso 2: Configuración de Google reCAPTCHA para el administrador

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."}

1. Inicie sesión en su cuenta de administrador.

1. En la barra lateral de Administración, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En la esquina superior derecha, establezca **[!UICONTROL Store View]** en `Default Config`.

1. En el panel izquierdo, expanda **[!UICONTROL Security]** y haga clic en **[!UICONTROL Google reCAPTCHA Admin Panel]**.

   >[!NOTE]
   >
   >Desactive la casilla de verificación **[!UICONTROL Use system value]** para cada campo que desee configurar.

1. Para usar _[!DNL reCAPTCHA v2 ("I am not a robot")]_, expanda la sección **[!UICONTROL reCAPTCHA v2 ("I am not a robot")]**&#x200B;y haga lo siguiente:

   - Para **[!UICONTROL Google API Website Key]**, introduzca la clave del sitio web que se creó para este tipo de reCAPTCHA al registrar su cuenta de Google reCAPTCHA.

   - Para **[!UICONTROL Google API Secret Key]**, introduzca la clave secreta asociada a su cuenta de Google reCAPTCHA.

   - Para **[!UICONTROL Size]**, elija el tamaño del cuadro reCAPTCHA de Google que desea que aparezca. Opciones: `Normal (default)` / `Compact`

   - Para **[!UICONTROL Theme]**, elija el tema que desea usar para aplicar estilo al cuadro reCAPTCHA de Google. Opciones: `Light Theme (default)` / `Dark Theme`

   - Para **[!UICONTROL Language Code]**, introduzca el código de dos caracteres para especificar el [idioma que se usa para el texto y los mensajes de Google reCAPTCHA](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 - &quot;No soy un robot&quot;](../configuration-reference/security/assets/recaptcha-admin-v2-not-robot.png){width="600" zoomable="yes"}

1. Para usar _[!DNL reCAPTCHA v2 Invisible]_, expanda la sección **[!UICONTROL reCAPTCHA v2 Invisible]**&#x200B;y haga lo siguiente:

   - Para **[!UICONTROL Google API Website Key]**, introduzca la clave del sitio web que se creó para este tipo de reCAPTCHA al registrar su cuenta de Google reCAPTCHA.

   - Para **[!UICONTROL Google API Secret Key]**, introduzca la clave secreta asociada a su cuenta de Google reCAPTCHA.

   - Para **[!UICONTROL Invisible Badge Position]**, elija la posición del distintivo que se utilizará en cada página. Opciones: `Inline` / `Bottom Right` / `Bottom Left`

   - Para **[!UICONTROL Theme]**, elija el tema que se utilizará para aplicar estilo al cuadro reCAPTCHA de Google. Opciones: `Light Theme (default)` / `Dark Theme`

   - Para **[!UICONTROL Language Code]**, escriba un código de dos caracteres que especifique el [idioma que se usa para el texto y los mensajes de Google reCAPTCHA](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 invisible](../configuration-reference/security/assets/recaptcha-admin-v2-invisible.png){width="600" zoomable="yes"}

1. Para usar _[!DNL reCAPTCHA v3 Invisible]_, expanda la sección **[!UICONTROL reCAPTCHA v3 Invisible]**&#x200B;y haga lo siguiente:

   - Para **[!UICONTROL Google API Website Key]**, introduzca la clave del sitio web que se creó para este tipo de reCAPTCHA al registrar su cuenta de Google reCAPTCHA.

   - Para **[!UICONTROL Google API Secret Key]**, introduzca la clave secreta asociada a su cuenta de Google reCAPTCHA.

   - Escriba **[!UICONTROL Minimum Score Threshold]** para identificar cuándo se marca la interacción de un usuario como un riesgo potencial; donde 1.0 es una interacción típica del usuario y 0.0 es probablemente un bot. Predeterminado: `0.5`

   - Para **[!UICONTROL Invisible Badge Position]**, elija la posición que se usará en cada página. Opciones: `Inline` / `Bottom Right` / `Bottom Left`

   - Para **[!UICONTROL Theme]**, elija el tema que se utilizará para aplicar estilo al cuadro reCAPTCHA de Google. Opciones: `Light Theme (default)` / `Dark Theme`

   - Para **[!UICONTROL Language Code]**, escriba un código de dos caracteres que especifique el [idioma que se usa para el texto y los mensajes de Google reCAPTCHA](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v3 invisible](../configuration-reference/security/assets/recaptcha-admin-v3-invisible.png){width="600" zoomable="yes"}

1. Expanda **[!UICONTROL reCAPTCHA Validation Failure Messages]** e introduzca los mensajes que aparecerán en el Administrador si la validación falla o no se puede completar.

   ![mensajes de error reCAPTCHA](../configuration-reference/security/assets/recaptcha-admin-failure-messages.png){width="600" zoomable="yes"}

1. Expanda la sección **[!UICONTROL Admin Panel]** y configure lo siguiente según sea necesario:

   - Establezca **[!UICONTROL Enable for Login]** en el tipo de reCAPTCHA que desee utilizar para la página de inicio de sesión de administrador.

   - Establezca **[!UICONTROL Enable for Forgot Password]** en el tipo de reCAPTCHA que desee utilizar para las solicitudes de restablecimiento de contraseña.

   ![opciones de administración reCAPTCHA](../configuration-reference/security/assets/recaptcha-admin-panel.png){width="600" zoomable="yes"}

## Paso 3: Configuración de Google reCAPTCHA para la tienda

1. En el panel izquierdo bajo _[!UICONTROL Security]_, elija **[!UICONTROL Google reCAPTCHA Storefront]**.

1. Complete la sección para cada tipo de reCAPTCHA que desee utilizar en la tienda.

   Consulte la información en _Paso 2: Configuración de Google reCAPTCHA para el administrador_ para obtener detalles sobre las opciones de cada tipo de reCAPTCHA.

1. Expanda **[!UICONTROL reCAPTCHA Validation Failure Messages]** e introduzca los mensajes que aparecerán en la tienda si la validación falla o no se puede completar.

1. Expanda la sección **[!UICONTROL Storefront]**.

   >[!NOTE]
   >
   >Desactive la casilla de verificación **[!UICONTROL Use system value]** para cada campo que desee configurar.

1. Establezca cada campo de ubicación de tienda en el tipo de reCAPTCHA que ha configurado para utilizar.

   - [!UICONTROL Enable for Customer Login]
   - [!UICONTROL Enable for Forgot Password]
   - [!UICONTROL Enable for Create New Customer Account]
   - [!UICONTROL Enable for Edit Customer Account]
   - [!UICONTROL Enable for Create New Company Account] ![Adobe Commerce B2B](../assets/b2b.svg) (disponible solo con Adobe Commerce B2B)
   - [!UICONTROL Enable for Contact Us]
   - [!UICONTROL Enable for Product Review]
   - [!UICONTROL Enable for Newsletter Subscription]
   - [!UICONTROL Enable for Gift Card] ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)
   - [!UICONTROL Enable for Invitation Create Account]
   - [!UICONTROL Enable for Send To Friend]
   - [!UICONTROL Enable for Checkout/Placing Order]
   - [!UICONTROL Enable for Wishlist Sharing]
   - [!UICONTROL Enable for Coupon Codes]
   - [!UICONTROL Enable for PayPal PayflowPro payment form]

   ![Configuración de opciones de tienda](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## Paso 4: guardar la configuración

1. Una vez completada la configuración, haga clic en **[!UICONTROL Save Config]**.

1. En el mensaje que aparece en la parte superior del área de trabajo, haga clic en **[!UICONTROL Cache Management]** y actualice cada caché no válida.
