---
title: Cumplimiento de la ley de cookies
description: Para mantenerse al día con la legislación en muchos países sobre el uso de cookies, Adobe Commerce y Magento Open Source ofrecen a los comerciantes una selección de métodos para obtener el consentimiento del cliente.
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: 04e8fe7cf303f434bab748df447eef8ac1097196
workflow-type: tm+mt
source-wordcount: '1825'
ht-degree: 0%

---

# Cumplimiento de la ley de cookies

Las cookies son pequeños archivos que se guardan en el equipo de cada visitante del sitio y que se utilizan como lugares de retención temporales para la información. La información que se guarda en las cookies se utiliza para personalizar la experiencia de compra, vincular a los visitantes con sus carros de compras, medir los patrones de tráfico y mejorar la eficacia de las promociones. Para mantenerse al día con la legislación en muchos países sobre el uso de cookies, Adobe Commerce y Magento Open Source ofrecen a los comerciantes una selección de métodos para obtener el consentimiento del cliente. Para obtener una lista de las cookies predeterminadas de Adobe Commerce y Magento Open Source, consulte [Referencia de cookies](#default-cookies).

>[!NOTE]
>
>Si modifica la configuración de privacidad predeterminada de [Google](../merchandising-promotions/google-tools.md#google-privacy-settings) para cumplir con el [Reglamento general de protección de datos](compliance-gdpr.md), no es necesario obtener el consentimiento del usuario para el uso de cookies de Google Analytics.

## Modo de restricción de cookies

Cuando el modo de restricción de cookies está habilitado, los visitantes de su tienda reciben una notificación avisando que se necesitan cookies para realizar operaciones con todas las funciones. Según la temática, el mensaje podría aparecer encima del encabezado, debajo del pie de página o en otro lugar de la página. El mensaje se vincula a su política de privacidad para obtener más información y anima a los visitantes a hacer clic en el botón Permitir para dar su consentimiento. Una vez concedido el consentimiento, el mensaje desaparece.

Su [política de privacidad](privacy-policy.md)) debe incluir el nombre de su tienda y la información de contacto, así como explicar el propósito de cada cookie que usa su tienda. Para obtener más información, consulte [Referencia de cookies](#default-cookies).

>[!NOTE]
>
>Si cambia la clave URL de la política de privacidad, también debe crear una reescritura de URL personalizada para redirigir el tráfico a la nueva clave URL. De lo contrario, el vínculo del mensaje Modo de restricción de cookies devuelve `404 Page Not Found`.

![Ejemplo de tienda - aviso de restricción de cookies](./assets/storefront-cookie-restriction-message.png){width="600"}

### Paso 1: Habilitar el modo de restricción de cookies

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel de navegación izquierdo bajo **[!UICONTROL General]**, elija **[!UICONTROL Web]**.

1. Expanda la sección **[!UICONTROL Default Cookie Settings]** y haga lo siguiente:

   ![Configuración web - configuración de cookies predeterminada](./assets/web-default-cookie-settings.png){width="600"}

   - Escriba **[!UICONTROL Cookie Lifetime]** en segundos.

   - Si desea que las cookies estén disponibles para otras carpetas, escriba **[!UICONTROL Cookie Path]**. Para que las cookies estén disponibles en cualquier parte del sitio, escriba una barra diagonal (`/`). Este valor solo puede contener la ruta de la cookie y **_no puede_** contener ningún otro parámetro de cookie.

   - Para que las cookies estén disponibles para un subdominio, escriba el nombre de subdominio en el campo **[!UICONTROL Cookie Domain]** (`subdomain.yourdomain.com`). Para que las cookies estén disponibles para todos los subdominios, escriba el nombre de dominio precedido de un punto (`.yourdomain.com`). Este valor solo puede contener el dominio de la cookie y **_no puede_** contener ningún otro parámetro de cookie.

   - Para evitar que los lenguajes de scripts, como JavaScript, obtengan acceso a las cookies, asegúrese de que **Usar solo HTTP** está establecido en `Yes`.

   - Establezca **[!UICONTROL Cookie Restriction Mode]** en `Yes`.

     Si es necesario, desmarque la casilla de verificación y haga clic en **[!UICONTROL OK]** para confirmar el cambio de ámbito.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

1. Cuando se le pida que actualice la caché, haga clic en el vínculo **[!UICONTROL Cache Management]** en el mensaje del sistema y actualice cada caché no válida.

### Paso 2: Actualizar la política de privacidad

Actualice la [política de privacidad](privacy-policy.md) para que refleje la información que recopila su compañía y cómo se utiliza.

## Cookies predeterminadas

Las cookies predeterminadas de Adobe Commerce y Magento Open Source se clasifican como Exentas/No exentas para ayudar a los comerciantes a cumplir con los requisitos de las regulaciones de privacidad como el [RGPD](compliance-gdpr.md). Los comerciantes deben utilizar esta información como guía y consultar con asesores legales para actualizar sus políticas de privacidad y cookies como parte de una estrategia integral de cumplimiento de la regulación de privacidad.

[!DNL Commerce] usa las siguientes cookies &quot;listas para usar&quot; para instalaciones locales y en la nube. Estas cookies pueden ser necesarias para la funcionalidad que solicita explícitamente el cliente. Para obtener más información acerca de la duración de las cookies de sesión, consulte [Duración de la sesión](../customers/customer-online-options.md).

Algunas de estas cookies pueden proporcionar opciones de configuración, incluida la activación o desactivación, según sea necesario.

### Cookies de funcionalidad solicitadas (exentas)

#### `add_to_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Registra el SKU, el nombre, el precio y la cantidad del producto que se quitó del carro de compras. Permite a los Google Analytics saber cuándo se ha agregado un producto al carro de compras.

#### `guest-view`

Vincula un pedido de invitado a un invitado (porque no hay cuenta para invitado).

#### `login_redirect`

Guarda la URL de redireccionamiento para dirigir al usuario si el inicio de sesión y el registro de usuarios se realizan correctamente. Guarda la página en la que se encontraba un usuario antes de iniciar sesión (para determinar la ubicación a la que regresará después de iniciar sesión).

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Almacena el contenido del banner localmente para mejorar el rendimiento. El contenido del titular es cualquier contenido que un comerciante mostraría en su sitio web.

#### `mage-messages`

Rastrea mensajes de error y otras notificaciones que se muestran al usuario, como el mensaje de consentimiento de cookies y varios mensajes de error. El mensaje se elimina de la cookie después de mostrarse al comprador. No existe una opción para deshabilitar esta cookie. Así es como se comunica la información única al usuario, como los mensajes de error.

#### `product_data_storage` (almacenamiento local)

Almacena la configuración de los datos de producto utilizados para utilizar las funciones &quot;Vistos recientemente&quot; y &quot;Comparar productos&quot;. Almacena la configuración específica de un usuario (por ejemplo, si ha visto recientemente un producto o si ha comparado productos).

#### `recently_compared_product` (almacenamiento local)

Almacena los ID de productos de productos comparados recientemente.

#### `recently_compared_product_previous` (almacenamiento local)

Almacena los ID de productos de productos comparados anteriormente para facilitar la navegación.

#### `recently_viewed_product` (almacenamiento local)

Almacena los ID de productos de productos vistos recientemente para facilitar la navegación.

#### `recently_viewed_product_previous` (almacenamiento local)

Almacena los ID de productos de productos vistos recientemente para facilitar la navegación.

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) permite a los Google Analytics saber cuándo se ha eliminado un producto de un carro de compras.

#### `stf`

Registra la hora en que el módulo SendFriend ([Enviar correo electrónico a un amigo](../stores-purchase/email-a-friend.md)) envía los mensajes. Cuando un comprador envía un vínculo a un producto, esta cookie registra una marca de tiempo y mantiene un recuento.

#### `X-Magento-Vary`

Indica cuándo se debe proporcionar una nueva versión de una página desde la caché. Admite el rendimiento del sitio web.

#### `form_key`

Mecanismo de seguridad que contiene un valor generado aleatoriamente para evitar ataques de falsificación de solicitud en sitios múltiples (CSRF), al ayudar a determinar si una solicitud procede de una fuente auténtica o de un actor incorrecto. Se trata de una práctica estándar en la industria para evitar ataques de CSRF.

#### `mage-cache-sessid`

Útil para determinar cuándo limpiar el almacenamiento local en el explorador después de la caducidad de la sesión. Se utiliza para determinar si se debe limpiar el almacenamiento local. La falta de esta cookie déclencheur la limpieza del almacenamiento local.

#### `mage-cache-storage`

Almacenamiento local de contenido específico del visitante que habilita las funciones de comercio electrónico. No se usa de forma predeterminada, pero cuando se usa, se usa para acelerar el cierre de compra, de modo que la información básica del usuario esté disponible cuando alguien se marcha y vuelve.

#### `mage-cache-storage-section-invalidation`

Almacena información relacionada con las secciones de la página que deben invalidarse y eliminarse.

#### `persistent_shopping_cart`

Almacena el ID de clave de un carro de compras persistente para permitir la restauración del carro de compras para un comprador anónimo.

#### `private_content_version`

Adjunta un número y una hora aleatorios y únicos a las páginas con contenido de cliente para evitar que se almacenen en la caché del servidor. Se configura en varios lugares: en PHP, en JavaScript como cookie y en JavaScript para almacenamiento local.

#### `section_data_ids`

Almacena información específica del cliente relacionada con las acciones iniciadas por el comprador, como la visualización de la lista de deseos y la información de cierre de compra.

#### `store`

Registra la vista o configuración regional de la tienda seleccionada por el comprador.

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce): almacenamiento local para la funcionalidad de banner. Banner significa que el sitio web general contiene toda la información mostrada al comprador.

#### `PHPSESSID`

Rastrea sesiones de usuario en la tienda. Son los compradores que usan los productos finales.

#### `admin`

Rastrea sesiones de usuario en el lado del administrador.

#### `loggedOutReasonCode`

Se establece cuando un usuario administrador está bloqueado tras un determinado número de intentos de contraseña fallidos.

#### `section_data_clean`

Se establece cuando un usuario cambia de vista de tienda. La presencia de esta cookie déclencheur a JavaScript a volver a cargar determinadas secciones de la página para reflejar la vista de tienda correcta.

#### `lang`

Establecido indirectamente por el módulo Admin Analytics. Se utiliza solo en un área administrativa de una tienda. No aplicable a los compradores.

#### `s_fid`

Establecido indirectamente por el módulo Admin Analytics. Marca de fecha y hora del ID único de visitante de reserva. Se usa para identificar a un visitante único si la cookie estándar `s_vi` no está disponible debido a las restricciones de cookies de terceros. Se utiliza solo en un área administrativa de una tienda. No aplicable a los compradores.

#### `s_cc`

Establecido indirectamente por el módulo Admin Analytics. El código JavaScript lo establece y lo lee para determinar si las cookies están habilitadas. Se utiliza solo en un área administrativa de una tienda. No aplicable a los compradores.

#### `apt.sid`

Establecido por la biblioteca PX de Gainsight utilizado indirectamente por el módulo Admin Analytics. El propósito de esta cookie es permitir el seguimiento continuado del ID de sesión en el dominio de nivel superior del producto y se utiliza como ID de referencia para la sesión activa. Se utiliza solo en un área administrativa de una tienda. No aplicable a los compradores.

#### `apt.uid`

Establecido por la biblioteca PX de Gainsight utilizado indirectamente por el módulo Admin Analytics. El propósito de esta cookie es permitir el seguimiento continuado del ID en el dominio de nivel superior del producto y se utiliza como ID de referencia para la entidad del usuario. Se utiliza solo en un área administrativa de una tienda. No aplicable a los compradores.

#### `s_sq`

Establecido indirectamente por el módulo Admin Analytics. Lo utiliza la función de ClickMap que recopila datos sobre dónde y en qué hacen clic los visitantes. Almacena información de cada clic. Se utiliza solo en un área administrativa de una tienda. No aplicable a los compradores.

#### `pagebuilder_modal_dismissed`

La establece el módulo Page Builder. Contiene un indicador que evita que las solicitudes posteriores pidan a un administrador que confirme la apertura de una acción determinada si el administrador las descartó explícitamente antes. Se utiliza solo en un área administrativa de una tienda. No aplicable a los compradores.

#### `pagebuilder_template_apply_confirm`

La establece el módulo Page Builder. Contiene un indicador que evita que las solicitudes posteriores pidan a un administrador que confirme la apertura de una acción determinada si el administrador las descartó explícitamente antes. Se utiliza solo en un área administrativa de una tienda. No aplicable a los compradores.

#### `accordion-{VARIABLE}-{VARIABLE}`

Se utiliza como parte de la implementación de la funcionalidad de pestañas solo en un área administrativa de una tienda. No aplicable a los compradores.

## Cookies de Recommendations del producto

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Los clientes de Product Recommendations utilizan las siguientes cookies para Adobe Commerce. Estas cookies se instalan con el [módulo DataServices](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure).

- `mg_dnt`: le permite [restringir la recopilación de datos de Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/developer/setting-cookie) si tiene código personalizado para administrar el consentimiento de cookies en su sitio.
- `user_allowed_save_cookie`: se usa para [modo de restricción de cookies](#cookie-restriction-mode).
- `authentication_flag`: indica si un comprador ha iniciado sesión o ha cerrado sesión. Esta cookie se actualiza al mismo tiempo que la cookie `dataservices_customer_id`.
- `dataservices_customer_id`: indica si un comprador ha iniciado sesión o ha cerrado sesión. Esta cookie contiene el ID único del cliente en el sistema.
- `dataservices_customer_group`: indica el grupo de un cliente. Esta cookie se almacena como [sha1](https://en.wikipedia.org/wiki/SHA-1) suma de comprobación del ID de grupo del cliente.
- `dataservices_cart_id`: identifica las acciones del carro de compras de un comprador. Esta cookie contiene el ID único de carro de compras del cliente en el sistema.
- `dataservices_product_context`: identifica las interacciones de productos de un comprador. Esta cookie contiene el ID de cotización único del cliente en el sistema.

## Cookies adicionales

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Las siguientes cookies están configuradas para los clientes de Adobe Commerce. Estas cookies se instalan con el [módulo DataServices](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure).

- `mg`: configurado por el rastreador de JavaScript de Snowplow. Encontrará más información en la [documentación de Snowplow](https://docs.snowplow.io/docs/collecting-data/collecting-from-own-applications/javascript-trackers/web-tracker/tracker-setup/initialization-options).
- `com.adobe.alloy.getTld`: dado el nombre de host de la página web actual, este es el dominio de primer nivel que no es un &quot;sufijo público&quot; como se describe en https://publicsuffix.org. Básicamente, este es el dominio de primer nivel que puede aceptar cookies. Esta cookie forma parte del [SDK web de Alloy](https://github.com/adobe/alloy).

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
