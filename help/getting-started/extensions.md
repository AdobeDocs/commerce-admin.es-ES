---
title: Extensiones desde el Adobe
description: Revise la información sobre las extensiones para Adobe Commerce y Magento Open Source publicadas por Adobe.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: c22ad5c3220f14588131d6b29a88dab3c5347681
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 0%

---

# Extensiones desde el Adobe

En este tema se proporciona información sobre las extensiones para Adobe Commerce y Magento Open Source que se lanzan por Adobe. Las extensiones agregan funciones, funcionalidades, servicios e integraciones al administrador y a la tienda. Algunas de estas extensiones se desarrollan mediante contribuciones de la Comunidad Magento Open Source. Algunas extensiones requieren una instalación independiente y otras se instalan de forma predeterminada.

## Extensiones instaladas

Hay algunas extensiones que se instalan automáticamente con Adobe Commerce o Magento Open Source.

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) proporciona una mejor gestión de stock y envíos en una o varias ubicaciones y canales de ventas con protección de cierre de compra simultáneo y algoritmos de conciliación de envíos. Realice un seguimiento de las cantidades de inventario, proporcione cantidades precisas de stock vendible a los clientes y realice envíos según las recomendaciones o selecciones manuales para controlar todo el inventario. Configure las opciones de administración de forma global, por origen y por producto.

>[!NOTE]
>
>Esta extensión se desarrolló como parte de la [[!DNL Inventory Management]](https://github.com/magento/inventory) (anteriormente MSI) a través del programa Community Engineering.

[!DNL Inventory Management] se instala con todas las funciones habilitadas de forma predeterminada. No se requieren pasos adicionales para habilitar estas características de inventario. Para obtener más información sobre [!DNL Inventory Management] funciones, consulte las [[!DNL Inventory Management] Guía del usuario](../inventory-management/guide-overview.md).

### Braintree

PayPal y Gene Commerce juntos desarrollaron la extensión oficial de Braintree para las tiendas de Commerce 2.4.x. Con una experiencia de pago y envío mejorada diseñada para impulsar la conversión, las actualizaciones incluyen opciones de PayAfter que muestran automáticamente mensajes y botones PayAfter relevantes a los consumidores mientras compran y durante el pago.

Esta extensión se instala de forma predeterminada, pero requiere un [cuenta de Braintree](https://www.braintreepayments.com/) Configuración de y en el Administrador que se activará en la tienda. Para determinar las tarifas aplicables al utilizar Braintree para procesar sus transacciones, consulte la [precio de Braintree](https://www.braintreepayments.com/braintree-pricing).

Para obtener información sobre la configuración del Braintree en Admin, consulte la [Braintree](../stores-purchase/braintree.md) tema en la _Guía de ventas y experiencia de compra_.

### Google reCAPTCHA

Google reCAPTCHA proporciona un nivel de seguridad mayor tanto para la tienda como para la IU del administrador que el disponible con el CAPTCHA estándar y le permite:

- Compruebe cuándo los clientes crean cuentas, recuperan contraseñas, inician sesión en sus cuentas o se ponen en contacto con la compañía.
- Mejore la seguridad cuando los usuarios administradores inicien sesión.

Reduce los posibles errores de los usuarios al introducir un código Captcha y fomenta la conversión al carro de compras sin añadir obstáculos durante el cierre de compra. [Habilitar y configurar reCAPTCHA](../systems/security-google-recaptcha.md) mediante comprobaciones invisibles o interactivas para mejorar el acceso seguro al [!DNL Commerce] Administrador y tienda.

### Autenticación de doble factor

El [!DNL Commerce] El administrador proporciona acceso completo a su tienda, pedidos y datos de clientes. [Autenticación de doble factor](../systems/security-two-factor-authentication.md) (2FA o TFA) mejora la seguridad al requerir autenticación adicional, más allá del nombre de inicio de sesión y la contraseña estándar, para acceder al [!DNL Commerce] Administrador desde todos los dispositivos. La extensión admite varios autenticadores, incluidos Google Authenticator, Authenticator, [!DNL Duo]y las teclas U2F. Esta autenticación solo se aplica a los usuarios administradores. No está disponible para cuentas de cliente de tienda.

Estas funciones están habilitadas de forma predeterminada. Cada usuario administrador debe instalar y configurar uno de los autenticadores admitidos.

>[!NOTE]
>
>Las tiendas Adobe Commerce que han habilitado la autenticación de Adobe de los servicios de Identity Management (IMS) para el administrador tienen Commerce 2FA nativo deshabilitado. Los usuarios que han iniciado sesión en el administrador con sus credenciales de Adobe no necesitan volver a autenticarse en muchas tareas de administración. La autenticación la gestiona Adobe IMS cuando el usuario administrador inicia sesión en su sesión actual. Consulte [Información general sobre la integración de Adobe Identity Management Service (IMS)](./adobe-ims-integration-overview.md).

## Extensiones para añadir

El [[!DNL Commerce Marketplace]](https://marketplace.magento.com/) es el recurso de comercio electrónico global para aplicaciones y servicios que se expanden. [!DNL Commerce] soluciones con potentes nuevas funciones y funcionalidades. Adobe lanza varias extensiones a través de la [!DNL Marketplace] que se pueden instalar y configurar en su tienda de Adobe Commerce o Magento Open Source para proporcionar integraciones y funciones mejoradas.

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) Solo Adobe Commerce

El [!DNL Live Search] Esta extensión conecta su tienda con el servicio Live Search, una plataforma de búsqueda gratuita de Adobe Commerce que permite a los vendedores ofrecer a los clientes una experiencia de búsqueda mejorada con IA. Adobe Sensei, faceteado inteligente, creado con inteligencia artificial de Adobe, ayuda a los comerciantes a hacer más con menos eliminando el trabajo manual de faceteado/filtrado.

Consulte la [Guía del usuario de Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html) para obtener más información.

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) Solo Adobe Commerce

El [!DNL Product Recommendations] La extensión de conecta su tienda al servicio Product Recommendations, una potente herramienta de marketing que puede utilizar para aumentar las conversiones, los ingresos y la participación. [!DNL Product Recommendations] fue creado por Adobe Commerce y está impulsado por su inteligencia artificial probada en pruebas, Adobe Sensei, para que pueda impulsar la participación y la conversión de forma segura. Esta función elimina el trabajo manual necesario para hacer recomendaciones de productos relevantes a cada comprador.

Consulte la [[!DNL Product Recommendations] Guía del usuario](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html?lang=en) para obtener más información.

### [!DNL Catalog Service]

El [!DNL Catalog Service] le permite ofrecer a los clientes una experiencia de producto optimizada a la vez que aumenta el rendimiento, mejora la escalabilidad y aumenta las conversiones. Consulte la [[!DNL Catalog Service] Guía del usuario](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html) para obtener más información.

### [!DNL Payment Services]

[!DNL Payment services] para Adobe Commerce y Magento Open Source es una solución de pago totalmente integrada que simplifica el proceso de gestión de pagos y ofrece a sus clientes la oportunidad de pagar a su manera. Concilie de forma segura todos los datos de pagos y transacciones dentro del administrador de Adobe Commerce, lo que le permite administrar pedidos y pagos en un solo lugar mientras realiza un cierre de compra sin problemas. Consulte la [[!DNL Payment Services] Guía del usuario](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html) para obtener más información.

### [!DNL Quick Checkout]

[!DNL Quick Checkout] para Adobe Commerce ofrece una experiencia de cierre de compra perfecta diseñada para convertir a los clientes que solo vienen una vez en titulares de cuentas fieles.
Consulte la [[!DNL Quick Checkout] Guía del usuario](https://experienceleague.adobe.com/docs/commerce-merchant-services/quick-checkout/overview.html) para obtener más información.

### [!DNL Store Fulfillment]

La satisfacción de pedidos de la tienda para Adobe Commerce y Magento Open Source permite una experiencia de cliente superior de compra en línea, recogida en tienda (BOPIS) y maximiza la productividad de los empleados al proporcionar un flujo de trabajo de satisfacción de pedidos completo habilitado a través de un dispositivo móvil. Consulte la [[!DNL Store Fulfillment] Guía del usuario](https://experienceleague.adobe.com/docs/commerce-merchant-services/store-fulfillment/guide-overview.html) para obtener más información.

### [!DNL Amazon Sales Channel]

El [!DNL Amazon Sales Channel] para Adobe Commerce permite integrar la base de datos de anuncios de la Central de vendedores de Amazon con su [!DNL Commerce] catálogo de productos y administre sus anuncios y ventas de Amazon en el Administrador de comercio. Consulte la [[!DNL Amazon Sales] Guía del usuario](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html) para obtener más información.

### [!DNL Channel Manager]

[!DNL Channel Manager] le permite aumentar las ventas, llegar a nuevos clientes, agilizar las operaciones y ahorrar tiempo mediante la integración de un catálogo de productos Adobe Commerce o de Magento Open Source con Walmart Marketplace. Después de instalar y configurar la extensión, su personal puede administrar los listados, el inventario, los pedidos, las devoluciones y los reembolsos de Walmart Marketplace sin problemas desde el [!DNL Commerce Admin]. Consulte la [[!DNL Channel Manager] Guía del usuario](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html) para obtener más información.
