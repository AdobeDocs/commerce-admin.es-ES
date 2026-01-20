---
title: Extensiones de Adobe
description: Revise la información sobre las extensiones para Adobe Commerce y Magento Open Source publicadas por Adobe.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 36c91007d21834b49351c8b53c617e442deebaa0
workflow-type: tm+mt
source-wordcount: '1356'
ht-degree: 0%

---

# Extensiones de Adobe

Este tema proporciona información sobre las extensiones PHP para Adobe Commerce y Magento Open Source que publica Adobe.

Las extensiones agregan funciones, funcionalidades, servicios e integraciones al administrador y a la tienda. Algunas de estas extensiones se desarrollan mediante contribuciones de la comunidad de Magento Open Source. Algunas extensiones se instalan de forma predeterminada y otras requieren una instalación independiente.

+++Más información sobre la ampliación de Adobe Commerce

Adobe proporciona dos enfoques principales para ampliar o personalizar sus proyectos de Adobe Commerce:

- Extensibilidad en proceso: Utiliza código personalizado y extensiones que se ejecutan dentro del proceso de aplicación de Adobe Commerce como extensiones PHP. Este enfoque tradicional permite una integración profunda, pero requiere una administración cuidadosa durante las actualizaciones.

- Extensibilidad fuera de proceso: utiliza código personalizado y aplicaciones que funcionan de forma independiente del software principal. Este enfoque moderno ayuda a reducir el coste total de propiedad al:

   - Simplificación de las actualizaciones, ya que las extensiones están disociadas del núcleo
   - Proporciona a los desarrolladores más control sobre los métodos y el tiempo de implementación
   - Permite la ampliación y el mantenimiento independientes de los componentes de extensión.

Adobe Commerce ofrece estrategias y herramientas para admitir ambos tipos de extensibilidad. Para obtener más información, consulte [Extensibilidad de Adobe Commerce](https://developer.adobe.com/commerce/extensibility/).

+++

## Extensiones de Adobe instaladas de forma predeterminada

Las siguientes extensiones de Adobe se incluyen con Adobe Commerce y se instalan automáticamente con la aplicación de Adobe Commerce. Algunas extensiones requieren una configuración o habilitación adicional en el administrador, tal como se indica en la descripción de la extensión.

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

## Extensiones de Adobe que requieren instalación

Adobe ofrece extensiones adicionales que deben instalarse por separado con Composer. Estas extensiones están disponibles a través de diferentes canales:

- Acceso al repositorio (repo.magento.com)

  Las siguientes extensiones requieren el aprovisionamiento de cuentas y credenciales para la instalación. Póngase en contacto con su representante de cuentas de Adobe para obtener ayuda.

   - [Adobe Commerce B2B](#adobe-commerce-b2b)
   - [Integración de AEM Assets para Commerce](#assets-integration-for-commerce)

- Adobe Commerce Marketplace

  Las siguientes extensiones de Adobe son de acceso público en [marketplace.magento.com](https://marketplace.magento.com). Estas extensiones están disponibles sin coste adicional.

   - [Live Search](#live-search)
   - [Recomendaciones de productos](#product-recommendations)
   - [Servicio de catálogo](#catalog-service)
   - [Servicios de pago](#payment-services)

### [!DNL Adobe Commerce B2B]

![Solo Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce requiere una licencia por separado.

[!DNL Adobe Commerce B2B] es una extensión integrada que transforma las tiendas Commerce estándar en plataformas integrales de empresa a empresa. Permite a las empresas administrar estructuras organizativas complejas con varios compradores, funciones personalizadas y permisos de compra en cuentas de empresa unificadas. Las funciones clave incluyen catálogos y precios específicos de la empresa, presupuestos negociables, gestión de pedidos de compra, listas de solicitudes y funciones de pedidos rápidos. La solución admite modelos B2B y B2C en una sola instancia, lo que la hace flexible para diversas necesidades comerciales. La extensión requiere una licencia independiente y se integra perfectamente con las funciones principales de Adobe Commerce para proporcionar una solución completa de comercio electrónico B2B.

Para obtener más información, póngase en contacto con su representante de cuentas de Adobe. Para obtener detalles de implementación y pasos de configuración, consulte la [[!DNL B2B for Adobe Commerce] Guía del usuario](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=es).

### [!DNL AEM Assets Integration for Commerce]

![Solo Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce también requiere licencias para Adobe Experience Manager (AEM) Assets y AEM Dynamic Media.

[!DNL AEM Assets Integration for Commerce] conecta Adobe Commerce con el sistema de administración de recursos digitales (DAM) de Adobe Experience Manager para proporcionar un control centralizado de todos los recursos digitales. Esta integración permite la sincronización automatizada de recursos, las actualizaciones en tiempo real y la reutilización eficiente de contenidos en las tiendas de comercio. Al combinar las sólidas capacidades de administración de recursos de AEM con Commerce, las empresas se benefician de los flujos de trabajo optimizados, las experiencias de marca coherentes y la entrega de medios optimizada a través de una infraestructura basada en la nube.

Para obtener más información, póngase en contacto con su representante de cuentas de Adobe. Para obtener detalles de implementación y pasos de configuración, consulte la [[!DNL Assets Integration] Guía del usuario](../content-design/aem-assets-integration.md).

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) solo Adobe Commerce

Live Search es una función exclusiva de Adobe Commerce que proporciona una solución de búsqueda con tecnología de IA con funcionalidad de búsqueda en tiempo real. Ofrece resultados relevantes y rápidos con miniaturas de productos mientras los compradores escriben, junto con facetas inteligentes que ajustan automáticamente los filtros en función del comportamiento de compra. La solución incluye funcionalidades de comercialización para impulsar y enterrar productos, administración de sinónimos y análisis de búsqueda. Incluido con Adobe Commerce sin costo adicional, [!DNL Live Search] reemplaza la funcionalidad de búsqueda predeterminada con una experiencia de búsqueda basada en SaaS más sofisticada. Requiere una configuración mínima para empezar.

Para obtener detalles de implementación y requisitos técnicos, consulte la [Guía del usuario de Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=es).

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) solo Adobe Commerce

[!DNL Product Recommendations] es una característica exclusiva de Adobe Commerce con tecnología de IA de Adobe que ofrece sugerencias de productos personalizadas en todo el recorrido de compras de los clientes. La solución analiza el comportamiento del comprador y las relaciones del producto en tiempo real para generar automáticamente recomendaciones relevantes que no requieran reglas de comercialización manuales. Este enfoque basado en IA ayuda a aumentar las tasas de conversión y el potencial de ingresos, a la vez que crea experiencias de descubrimiento de productos más atractivas para los compradores.

Para obtener detalles de implementación y prácticas recomendadas, consulte la [[!DNL Product Recommendations] Guía del usuario](https://experienceleague.adobe.com/docs/commerce/product-recommendations/overview.html?lang=es).

### [!DNL Catalog Service]

[!BADGE Compatible]{type=Informative tooltip="Admitido"} instalaciones de Adobe Commerce y Magento Open Source

[!DNL Catalog Service] es una solución de alto rendimiento para Adobe Commerce y Magento Open Source que proporciona acceso optimizado a los datos del catálogo a través de los extremos de GraphQL. Mantiene una base de datos sincronizada independiente para los detalles del producto y la información relacionada, omitiendo la comunicación directa con la aplicación para ofrecer tiempos de carga de página más rápidos. El servicio es especialmente valioso para páginas de detalles de productos, listados de categorías y páginas de resultados de búsqueda, lo que lo hace ideal para implementaciones de comercio tradicionales y sin encabezado.

Para obtener instrucciones de configuración y detalles técnicos, consulte la [[!DNL Catalog Service] Guía del usuario](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html?lang=es).

>[!NOTE]
>
>Los servicios de catálogo se instalan automáticamente cuando Live Search o Recomendaciones de productos están habilitados. No es necesario realizar la instalación manual.

### [!DNL Payment Services]

[!BADGE Compatible]{type=Informative tooltip="Admitido"} instalaciones de Adobe Commerce y Magento Open Source

[!DNL Payment Services] es una solución de pago lista para usar para tiendas Adobe Commerce y Magento Open Source que proporciona capacidades completas de procesamiento de pagos. El servicio integra la funcionalidad de pasarela de pago seguro con protección contra fraude integrada, a la vez que ofrece múltiples opciones de pago, incluidas tarjetas de crédito/débito, PayPal, Venmo (EE.UU.) y planes PayAfter. Incluye informes unificados de transacciones y gestión de pedidos a través de la interfaz de administración de Commerce, lo que facilita a los comerciantes el seguimiento de pagos, la administración del flujo de efectivo y la reconciliación de datos financieros en un solo lugar.

Para ver los pasos de configuración detallados y las opciones de pago, consulte la [[!DNL Payment Services] Guía del usuario](https://experienceleague.adobe.com/es/docs/commerce/payment-services/overview).
