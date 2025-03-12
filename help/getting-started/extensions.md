---
title: Extensiones de Adobe
description: Revise la información sobre las extensiones para Adobe Commerce y Magento Open Source publicadas por Adobe.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 0%

---

# Extensiones de Adobe

En este tema se proporciona información acerca de las extensiones para Adobe Commerce y Magento Open Source publicadas por Adobe. Las extensiones agregan funciones, funcionalidades, servicios e integraciones al administrador y a la tienda. Algunas de estas extensiones se desarrollan mediante contribuciones de la comunidad de Magento Open Source. Algunas extensiones requieren una instalación independiente y otras se instalan de forma predeterminada.

## Extensiones instaladas

Hay algunas extensiones que se instalan automáticamente con Adobe Commerce o Magento Open Source.

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) proporciona una administración mejorada de existencias y envíos en una o varias ubicaciones y canales de ventas con protección de cierre de compra y algoritmos de coincidencia de envíos simultáneos. Realice un seguimiento de las cantidades de inventario, proporcione cantidades precisas de stock vendible a los clientes y realice envíos según las recomendaciones o selecciones manuales para controlar todo el inventario. Configure las opciones de administración de forma global, por origen y por producto.

>[!NOTE]
>
>Esta extensión se desarrolló como parte del proyecto [[!DNL Inventory Management]](https://github.com/magento/inventory) (anteriormente MSI) a través del programa de ingeniería de la comunidad.

[!DNL Inventory Management] se instala con todas las características habilitadas de manera predeterminada. No se requieren pasos adicionales para habilitar estas características de inventario. Para obtener más información acerca de las capacidades de [!DNL Inventory Management], consulte la [[!DNL Inventory Management] Guía del usuario](../inventory-management/guide-overview.md).

### Braintree

PayPal y Gene Commerce desarrollaron juntos la extensión oficial de Braintree para las tiendas Commerce 2.4.x. Con una experiencia de pago y envío mejorada diseñada para impulsar la conversión, las actualizaciones incluyen opciones de PayAfter que muestran automáticamente mensajes y botones PayAfter relevantes a los consumidores mientras compran y durante el pago.

Esta extensión se instala de manera predeterminada, pero requiere una [cuenta de Braintree](https://www.braintreepayments.com/) y que la configuración del administrador esté habilitada en su tienda. Para determinar las tarifas que se aplican al usar Braintree para procesar tus transacciones, comprueba los [precios de Braintree](https://www.braintreepayments.com/braintree-pricing).

Para obtener información acerca de la configuración de Braintree en el administrador, consulte el tema [Braintree](../stores-purchase/braintree.md) en la _Guía de ventas y compras_.

### Google reCAPTCHA

Google reCAPTCHA proporciona un nivel de seguridad mayor tanto para la tienda como para la IU del administrador que el disponible con el CAPTCHA estándar y le permite:

- Compruebe cuándo los clientes crean cuentas, recuperan contraseñas, inician sesión en sus cuentas o se ponen en contacto con la compañía.
- Mejore la seguridad cuando los usuarios administradores inicien sesión.

Reduce los posibles errores de los usuarios al introducir un código Captcha y fomenta la conversión al carro de compras sin añadir obstáculos durante el cierre de compra. [Habilite y configure reCAPTCHA](../systems/security-google-recaptcha.md) mediante comprobaciones invisibles o interactivas para mejorar el acceso seguro al administrador y tienda de [!DNL Commerce].

### Autenticación de doble factor

El administrador de [!DNL Commerce] proporciona acceso completo a su tienda, pedidos y datos de clientes. [La autenticación de doble factor](../systems/security-two-factor-authentication.md) (2FA o TFA) mejora la seguridad al requerir autenticación adicional, más allá del nombre de inicio de sesión y la contraseña estándar, para tener acceso al administrador de [!DNL Commerce] desde todos los dispositivos. La extensión admite varios autenticadores, incluidas las claves Google Authenticator, Authenticator, [!DNL Duo] y U2F. Esta autenticación solo se aplica a los usuarios administradores. No está disponible para cuentas de cliente de tienda.

Estas funciones están habilitadas de forma predeterminada. Cada usuario administrador debe instalar y configurar uno de los autenticadores admitidos.

>[!NOTE]
>
>Las tiendas Adobe Commerce que han habilitado la autenticación de Adobe Identity Management Services (IMS) para el administrador tienen Commerce 2FA nativo deshabilitado. Los usuarios que han iniciado sesión en el administrador con sus credenciales de Adobe no necesitan volver a autenticarse en muchas tareas de administración. La autenticación la gestiona Adobe IMS cuando el usuario administrador inicia sesión en su sesión actual. Consulte [Información general sobre la integración de Adobe Identity Management Service (IMS)](./adobe-ims-integration-overview.md).

## Extensiones para añadir

[[!DNL Commerce Marketplace]](https://marketplace.magento.com/) es el recurso de comercio electrónico global para aplicaciones y servicios que expanden soluciones de [!DNL Commerce] con nuevas características y funcionalidades potentes. Adobe lanza varias extensiones a través de [!DNL Marketplace] que se pueden instalar y configurar en su tienda de Adobe Commerce o Magento Open Source para proporcionar integraciones y capacidades mejoradas.

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) solo Adobe Commerce

La extensión [!DNL Live Search] conecta su tienda con el servicio Live Search, una plataforma de búsqueda gratuita de Adobe Commerce que permite a los vendedores ofrecer a los clientes una experiencia de búsqueda mejorada con IA. Adobe Sensei, faceteado inteligente, creado con inteligencia artificial de Adobe, ayuda a los comerciantes a hacer más con menos al eliminar el trabajo manual de faceteado/filtrado.

Consulte la [Guía del usuario de Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/guide-overview.html) para obtener más información.

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) solo Adobe Commerce

La extensión [!DNL Product Recommendations] conecta su tienda con el servicio Product Recommendations, una potente herramienta de marketing que puede utilizar para aumentar las conversiones, los ingresos y la participación. [!DNL Product Recommendations] fue creado por Adobe Commerce y es impulsado por su inteligencia artificial, Adobe Sensei, que ha sido probada para que pueda generar participación y conversión de manera segura. Esta función elimina el trabajo manual necesario para hacer recomendaciones de productos relevantes a cada comprador.

Consulte la [[!DNL Product Recommendations] Guía del usuario](https://experienceleague.adobe.com/docs/commerce/product-recommendations/guide-overview.html?lang=en) para obtener más información.

### [!DNL Catalog Service]

[!DNL Catalog Service] le permite ofrecer a los clientes una experiencia de producto optimizada a la vez que aumenta el rendimiento, mejora la escalabilidad y aumenta las conversiones. Consulte la [[!DNL Catalog Service] Guía del usuario](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html) para obtener más información.

### [!DNL Payment Services]

[!DNL Payment services] para Adobe Commerce y Magento Open Source es una solución de pago totalmente integrada que simplifica el proceso de administración de pagos y brinda a sus clientes la oportunidad de pagar a su manera. Concilie de forma segura todos los datos de pagos y transacciones dentro del administrador de Adobe Commerce, lo que le permite administrar pedidos y pagos en un solo lugar mientras realiza un cierre de compra sin problemas. Consulte la [[!DNL Payment Services] Guía del usuario](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html) para obtener más información.

### [!DNL Store Fulfillment]

La satisfacción de pedidos de la tienda para Adobe Commerce y Magento Open Source permite una experiencia de cliente superior en línea, recogida en tienda (BOPIS) y maximiza la productividad de los empleados al proporcionar un flujo de trabajo de satisfacción de pedidos completo habilitado a través de un dispositivo móvil. Consulte la [[!DNL Store Fulfillment] Guía del usuario](https://experienceleague.adobe.com/docs/commerce/store-fulfillment/guide-overview.html) para obtener más información.

### [!DNL Amazon Sales Channel]

[!DNL Amazon Sales Channel] para Adobe Commerce le permite integrar su base de datos de listados de Amazon Seller Central con su catálogo de productos [!DNL Commerce] y administrar sus listados y ventas de Amazon en el administrador de Commerce. Consulte la [[!DNL Amazon Sales] Guía del usuario](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html) para obtener más información.

### [!DNL Channel Manager]

[!DNL Channel Manager] le permite aumentar las ventas, llegar a nuevos clientes, optimizar las operaciones y ahorrar tiempo al integrar un catálogo de productos de Adobe Commerce o Magento Open Source con Walmart Marketplace. Después de instalar y configurar la extensión, su personal puede administrar los listados, el inventario, los pedidos, las devoluciones y los reembolsos de Walmart Marketplace sin problemas desde [!DNL Commerce Admin]. Consulte la [[!DNL Channel Manager] Guía del usuario](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html) para obtener más información.
