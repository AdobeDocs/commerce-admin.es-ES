---
title: Cumplimiento de la ley de cookies
description: Para mantenerse al día con la legislación en muchos países sobre el uso de cookies, Adobe Commerce y Magento Open Source ofrecen a los comerciantes una selección de métodos para obtener el consentimiento del cliente.
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: ae43d97bb3031a06ce6a0211ee304aae53e4eb08
workflow-type: tm+mt
source-wordcount: '2105'
ht-degree: 0%

---

# Cumplimiento de la ley de cookies

Las cookies son pequeños archivos que se guardan en el equipo de cada visitante del sitio y que se utilizan como lugares de retención temporales para la información. La información que se guarda en las cookies se utiliza para personalizar la experiencia de compra, vincular a los visitantes con sus carros de compras, medir los patrones de tráfico y mejorar la eficacia de las promociones. Para mantenerse al día con la legislación en muchos países sobre el uso de cookies, Adobe Commerce y Magento Open Source ofrecen a los comerciantes una selección de métodos para obtener el consentimiento del cliente. Para obtener una lista de las cookies predeterminadas de Adobe Commerce y Magento Open Source, consulte [Referencia de cookies](#default-cookies).

>[!NOTE]
>
>Si modifica la configuración de privacidad predeterminada de [Google](../merchandising-promotions/google-tools.md#google-privacy-settings) para cumplir con el [Reglamento general de protección de datos](compliance-gdpr.md), no es necesario obtener el consentimiento del usuario para el uso de cookies de Google Analytics.

## Método 1: consentimiento implícito

El consentimiento implícito significa que los visitantes de su tienda tienen una comprensión clara de que las cookies son una parte necesaria de las operaciones y, al utilizar su sitio, han concedido indirectamente permiso para utilizarlas. La clave para obtener el consentimiento implícito es proporcionar suficiente información para que un visitante tome una decisión informada. Muchas tiendas muestran un mensaje en la parte superior de todas las páginas estándar que proporciona una breve descripción de cómo se utilizan las cookies, con un vínculo a la política de privacidad de la tienda. La política de privacidad debe describir el tipo de información que recopila su tienda y cómo se utiliza.

## Método 2: consentimiento expresado

Para utilizar su tienda en _modo de restricción de cookies_, los visitantes deben expresar su consentimiento antes de guardar las cookies en sus equipos. A menos que se conceda el consentimiento, muchas funciones de su tienda no están disponibles. Por ejemplo, si Google Analytics está disponible para su tienda, solo se puede invocar después de que el visitante haya concedido permiso para utilizar cookies.

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

1. Cuando se le pida que actualice la caché, haga clic en el vínculo **[!UICONTROL Cache Management]** en el mensaje del sistema. A continuación, actualice cada caché no válida.

### Paso 2: Actualizar la política de privacidad

Actualice la [política de privacidad](privacy-policy.md) para que refleje la información que recopila su compañía y cómo se utiliza.

## Cookies predeterminadas

Las cookies predeterminadas de Adobe Commerce y Magento Open Source se clasifican como Exentas / No Exentas para ayudar a los comerciantes a cumplir con los requisitos de las regulaciones de privacidad como el [RGPD](compliance-gdpr.md). Los comerciantes deben utilizar esta información como guía y consultar con asesores legales para actualizar sus políticas de privacidad y cookies como parte de una estrategia integral de cumplimiento de la regulación de privacidad.

[!DNL Commerce] usa las siguientes cookies &quot;listas para usar&quot; para instalaciones locales y en la nube. Estas cookies pueden ser necesarias para la funcionalidad que solicita explícitamente el cliente. Para obtener más información sobre la duración de las cookies de sesión, consulte [Duración de la sesión](../customers/customer-online-options.md).

Algunas de estas cookies pueden proporcionar opciones de configuración, incluida la activación o desactivación, según sea necesario.

### Cookies de funcionalidad solicitadas (exentas)


#### `add_to_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) usado por el administrador de etiquetas de Google. Registra el SKU, el nombre, el precio y la cantidad del producto que se han eliminado del carro de compras y hace que la información esté disponible para su futura integración mediante scripts de terceros.

#### `guest-view`

Almacena el ID de pedido que los compradores invitados utilizan para recuperar su estado de pedido. Vista de pedidos de invitado. Se utiliza en _[!DNL Orders and Returns]_widgets.

- ¿Es seguro? No
- Solo HTTP: Sí
- Directiva de caducidad: Sesión
- Módulo: `Magento_Sales`

#### `login_redirect`

Conserva la página de destino que se cargaba antes de indicar al cliente que iniciara sesión. Se usa una redirección de inicio de sesión con el minicarrito para los clientes que iniciaron sesión si la opción de configuración [Mostrar minicarrito](../stores-purchase/cart-configuration.md#mini-cart) está establecida en `Yes`.

- ¿Es seguro? No
- Solo HTTP: No
- Directiva de caducidad: Sesión
- Módulo: `Magento_Customer`

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Almacena el contenido del banner localmente para mejorar el rendimiento.

#### `mage-messages`

Rastrea mensajes de error y otras notificaciones que se muestran al usuario, como el mensaje de consentimiento de cookies y varios mensajes de error. El mensaje se elimina de la cookie después de mostrarse al comprador.

No existe una opción para deshabilitar esta cookie.

- ¿Es seguro? No
- Solo HTTP: No
- Política de caducidad: Duración 1 año. Se borra en el front-end cuando se muestra el mensaje al usuario.
- Módulo: `Magento_Theme`

#### `mage-translation-storage` (almacenamiento local)

Almacena contenido traducido cuando el comprador lo solicita. Se utiliza cuando [Estrategia de traducción](../configuration-reference/advanced/developer.md) está configurada como &quot;Diccionario (traducción en la tienda)&quot;.

- ¿Es seguro? No
- Solo HTTP: No
- Directiva de caducidad: según las reglas de almacenamiento local
- Módulo: `Magento_Translation`

#### `mage-translation-file-version` (almacenamiento local)

Registra la versión de las traducciones en el almacenamiento local. Se usa cuando [Estrategia de traducción](../configuration-reference/advanced/developer.md) está configurada como `Dictionary (Translation on Storefront side)`.

- ¿Es seguro? No
- Solo HTTP: No
- Directiva de caducidad: según las reglas de almacenamiento local
- Módulo: `Magento_Translation`

#### `product_data_storage` (almacenamiento local)

Almacena la configuración de los datos de producto relacionados con productos vistos o comparados recientemente.

- ¿Es seguro? No
- Solo HTTP: No
- Directiva de caducidad: según las reglas de almacenamiento local
- Módulo: `Magento_Catalog`

#### `recently_compared_product` (almacenamiento local)

Almacena los ID de productos de productos comparados recientemente.

- ¿Es seguro? No
- Solo HTTP: No
- Directiva de caducidad: según las reglas de almacenamiento local
- Módulo: `Magento_Catalog`

#### `recently_compared_product_previous` (almacenamiento local)

Almacena los ID de productos de productos comparados anteriormente para facilitar la navegación.

- ¿Es seguro? No
- Solo HTTP: No
- Directiva de caducidad: según las reglas de almacenamiento local
- Módulo: `Magento_Catalog`

#### `recently_viewed_product` (almacenamiento local)

Almacena los ID de productos de productos vistos recientemente para facilitar la navegación.

- ¿Es seguro? No
- Solo HTTP: No
- Directiva de caducidad: según las reglas de almacenamiento local
- Módulo: `Magento_Catalog`

#### `recently_viewed_product_previous` (almacenamiento local)

Almacena los ID de productos de productos vistos recientemente para facilitar la navegación.

- ¿Es seguro? No
- Solo HTTP: No
- Directiva de caducidad: según las reglas de almacenamiento local
- Módulo: `Magento_Catalog`

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) usado por [Google Tag Manager](../merchandising-promotions/google-tag-manager.md). Registra el SKU del producto, el nombre, el precio y la cantidad añadida al carro de compras, y hace que la información esté disponible para una futura integración mediante scripts de terceros.

#### `stf`

Registra la hora en que el módulo SendFriend ([Enviar correo electrónico a un amigo](../stores-purchase/email-a-friend.md)) envía los mensajes.

- ¿Es seguro? Sí
- Solo HTTP: Sí
- Directiva de caducidad: Sesión
- Módulo: `Magento_SendFriend`

#### `X-Magento-Vary`

Ajuste de configuración que mejora el rendimiento al utilizar el almacenamiento en caché de contenido estático de Barniz.

- ¿Es seguro? Sí
- Solo HTTP: Sí
- Política de caducidad: basada en la configuración de PHP session.cookie_lifetime
- Módulo: `Magento_PageCache`

#### `form_key`

Una medida de seguridad que anexa una cadena aleatoria a todos los envíos de formularios para proteger los datos de la falsificación de solicitudes entre sitios (CSRF).

- ¿Es seguro? No
- Solo HTTP: No
- Política de caducidad:
   - PHP: Basado en la configuración de PHP session.cookie_lifetime
   - JS: Session
- Módulo: Caché de páginas

#### `mage-cache-sessid`

El valor de esta cookie almacena en déclencheur la limpieza del almacenamiento de caché local. Cuando la aplicación back-end elimina la cookie, el administrador limpia el almacenamiento local y establece el valor de la cookie en `true`.

- ¿Es seguro? No
- Solo HTTP: No
- Directiva de caducidad: Sesión
- Módulo: `Magento_Customer`

#### `mage-cache-storage`

Almacenamiento local de contenido específico del visitante que habilita las funciones de comercio electrónico.

- ¿Es seguro? No
- Solo HTTP: No
- Directiva de caducidad: Sesión
- Módulo: `Magento_Customer`, `Magento_Persistent`

#### `mage-cache-storage` (almacenamiento local)

Almacenamiento local de contenido específico del visitante que habilita las funciones de comercio electrónico.

- ¿Es seguro? No
- Solo HTTP: No
- Directiva de caducidad: Sesión
- Módulo: `Magento_Customer`, `Magento_Persistent`, `Magento_NegotiableQuote`

#### `mage-cache-storage-section-invalidation` (almacenamiento local)

Fuerza el almacenamiento local de secciones de contenido específicas que deben invalidarse.

- ¿Es seguro? No
- Solo HTTP: No
- Directiva de caducidad: por almacenamiento local
- Módulo: `Magento_Customer`

#### `persistent_shopping_cart`

Almacena la clave (ID) del carro de compras persistente para permitir la restauración del carro de compras para un comprador anónimo.

- ¿Es seguro? Sí
- Solo HTTP: Sí
- Directiva de caducidad: según la configuración de [Carro de compras persistente](../stores-purchase/cart-persistent.md) - Duración de la persistencia (segundos)
- Módulo: `Magento_Persistent`

#### `private_content_version`

Adjunta un número y una hora aleatorios y únicos a las páginas con contenido de cliente para evitar que se almacenen en la caché del servidor.

Se configura en varios lugares: en PHP, en JavaScript como cookie y en JavaScript para almacenamiento local.

Solo para HTTP=`Yes` (basado en la solicitud), significa que la cookie es segura si se configura durante una solicitud HTTPS y no segura si se configura durante una solicitud HTTP.

- ¿Es seguro? `Yes` (según solicitud), `No`
- Solo HTTP: `No`
- Directiva de caducidad: según la configuración de [Carro de compras persistente](../stores-purchase/cart-persistent.md) - Duración de la persistencia (segundos)
   - PHP: `1` año / `315360000s` (diez años)
   - JS: `1` día
   - Almacenamiento local JS: por reglas de almacenamiento local (para siempre)
- Módulo: `Magento_PageCache`, `Magento_Customer`

#### `section_data_ids`

Almacena información específica del cliente relacionada con las acciones iniciadas por el comprador, como la visualización de la lista de deseos y la información de cierre de compra.

- ¿Es seguro? `No`
- Solo HTTP: `No`
- Directiva de caducidad: `Session`
- Módulo: `Magento_Customer`

#### `store`

Registra la vista de tienda o la configuración regional específica seleccionada por el comprador.

- ¿Es seguro? `No`
- Solo HTTP: `Yes`
- Directiva de caducidad: `1` año
- Módulo: `Magento_Store`

#### `mage-banners-cache-storage` - almacenamiento local

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce): almacenamiento local para la funcionalidad de banner.

- ¿Es seguro? `No`
- Solo HTTP: `No`
- Directiva de caducidad: según las reglas de almacenamiento local
- Módulo: `Magento_Banner`

## Cookies de Google Analytics

Las siguientes cookies se usan cuando [Google Analytics](../merchandising-promotions/google-analytics.md) o Google Universal Analytics están totalmente habilitados para su instalación. Para deshabilitar estas cookies para cumplir con las normas de privacidad, consulte [Configuración de privacidad de Google](../merchandising-promotions/google-tools.md#google-privacy-settings). Para obtener más información, consulte Uso de cookies de [Google Analytics en sitios web][1].

### Cookies de Google Universal Analytics: no exentas

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Bibliotecas JavaScript: `gtag.js` y `analytics.js`

- `_ga`: distingue a los visitantes del sitio.
- `_gid`: distingue a los visitantes del sitio.
- `gat`: se usa para limitar la tasa de solicitudes.
- `dc_gtm_<property-id>`: Acelera la tasa de solicitudes cuando los Google Analytics se implementan con [Google Tag Manager](../merchandising-promotions/google-tag-manager.md).
- `AMP_TOKEN`: contiene un token que se puede usar para recuperar un ID de cliente del servicio de ID de cliente de AMP. Otros valores posibles incluyen exclusión, solicitud de vuelo o un error al recuperar un ID de cliente del servicio de ID de cliente de AMP.
- `_gac_<property-id>`: contiene información relacionada con la campaña para el usuario. Las etiquetas de conversión de Google AdWords leen esta cookie si Google Analytics está vinculado a tu cuenta de [AdWords][2].

### Cookies de Google Analytics - no exentas

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Biblioteca JavaScript: `ga.js`

- `__utma`: distingue entre compradores y sesiones. Esta cookie se crea cuando se ejecuta la biblioteca de JavaScript y no hay ninguna cookie `__utma` existente. La cookie se actualiza cada vez que se envían datos a los Google Analytics.
- `__utmt`: se usa para limitar la tasa de solicitudes.
- `__utmb`: Determina nuevas sesiones o visitas. Esta cookie se crea cuando se ejecuta la biblioteca de JavaScript y no hay ninguna cookie `__utmb` existente. La cookie se actualiza cada vez que se envían datos a los Google Analytics.
- `_utmz`: guarda el origen de tráfico o la campaña que explica cómo llegó el comprador al sitio. La cookie se crea cuando se ejecuta la biblioteca de JavaScript y se actualiza cada vez que se envían datos a los Google Analytics.
- `__utmv`: Almacena datos de variables personalizadas de nivel de visitante. Esta cookie se crea cuando un desarrollador utiliza el método `_setCustomVar` con una variable personalizada de nivel de visitante. Esta cookie se actualiza cada vez que se envían datos a los Google Analytics.

## Cookies de Recommendations del producto

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Los clientes de Product Recommendations utilizan las siguientes cookies para Adobe Commerce. Estas cookies se instalan con el [módulo DataServices](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html).

- `mg_dnt`: le permite [restringir la recopilación de datos de Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/developer/setting-cookie.html) si tiene código personalizado para administrar el consentimiento de cookies en su sitio.
- `user_allowed_save_cookie`: se usa para [modo de restricción de cookies](#cookie-restriction-mode).
- `authentication_flag`: indica si un comprador ha iniciado sesión o ha cerrado sesión. Esta cookie se actualiza al mismo tiempo que la cookie `dataservices_customer_id`.
- `dataservices_customer_id`: indica si un comprador ha iniciado sesión o ha cerrado sesión. Esta cookie contiene el ID único del cliente en el sistema.
- `dataservices_customer_group`: indica el grupo de un cliente. Esta cookie se almacena como [sha1](https://en.wikipedia.org/wiki/SHA-1) suma de comprobación del ID de grupo del cliente.
- `dataservices_cart_id`: identifica las acciones del carro de compras de un comprador. Esta cookie contiene el ID único de carro de compras del cliente en el sistema.
- `dataservices_product_context`: identifica las interacciones de productos de un comprador. Esta cookie contiene el ID de cotización único del cliente en el sistema.

## Cookies adicionales

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Las siguientes cookies están configuradas para los clientes de Adobe Commerce. Estas cookies se instalan con el [módulo DataServices](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html).

- `mg`: configurado por el rastreador de JavaScript de Snowplow. Encontrará más información en la [documentación de Snowplow](https://docs.snowplow.io/docs/collecting-data/collecting-from-own-applications/javascript-trackers/javascript-tracker/javascript-tracker-v3/tracker-setup/initialization-options).
- `com.adobe.alloy.getTld`: dado el nombre de host de la página web actual, este es el dominio de primer nivel que no es un &quot;sufijo público&quot; como se describe en https://publicsuffix.org. Básicamente, este es el dominio de primer nivel que puede aceptar cookies. Esta cookie forma parte del [SDK web de Alloy](https://github.com/adobe/alloy).

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
