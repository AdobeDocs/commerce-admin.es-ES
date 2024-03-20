---
title: Personalización a escala
description: Descubra qué funciones de Adobe Commerce le permiten crear una experiencia personalizada para sus compradores.
feature: Customers, Storefront, Personalization
source-git-commit: a4eeda918adcb74ad5e7008b80eff703fa15e878
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 0%

---

# Personalización a escala

&#x200B;La personalización a escala permite a las empresas personalizar la experiencia de compra para cada punto de contacto del cliente en función del contexto inmediato y el comportamiento observado anteriormente. El objetivo es presentar cada vez la experiencia más relevante y personalizada posible.

Para comprender las ventajas de ofrecer una experiencia de compra personalizada, descargue el [_Introducción a la personalización a escala_](https://business.adobe.com/resources/reports/getting-started-with-personalization-at-scale.html) informe.

La creación de una experiencia de compra personalizada requiere que conozca el tipo de datos necesarios para comprender el contexto del cliente. A partir de ahí, aprenderá las funciones de Adobe Commerce que utilizan esos datos para desbloquear las perspectivas de los clientes que necesita para crear la experiencia de compra personalizada.

La siguiente imagen ilustra los conceptos involucrados en la personalización de la experiencia de compra:

![Creación de una canalización de personalización](assets/personalization-journey.png){width="700" zoomable="yes"}

Este artículo analiza cada uno de los conceptos anteriores con más detalle.

## ¿Cómo personaliza la experiencia de compra?

La personalización exitosa comienza con el contexto del cliente. En esta sección, aprenderá sobre los tipos de datos disponibles para ayudarle a crear el contexto del cliente.

### Datos de tienda

Los datos de tienda, también denominados datos de comportamiento o del explorador, pueden revelar información sobre cómo los compradores interactúan con el sitio. Por ejemplo:

- ¿Qué productos y categorías son los que más les interesan a mis compradores?
- ¿En qué tipo de búsquedas participan más mis compradores?
- ¿Mis compradores están agregando productos al carro de compras y luego lo abandonan?
- ¿Mis compradores utilizan un explorador de escritorio o móvil?

Los siguientes eventos de tienda capturan datos que pueden ayudarle a responder a estas preguntas:

- [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [signIn](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [signOut](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)

### Datos de back office

Los datos de back office, también denominados datos del lado del servidor, pueden revelar información sobre el ciclo de vida del pedido. Por ejemplo:

- ¿Hay productos que se compran con mayor frecuencia según la temporada?
- ¿Mis compradores devuelven productos?
- ¿Cómo puedo calcular el valor de cliente de por vida?

Los siguientes eventos de back office capturan datos que pueden ayudarle a responder a estas preguntas:

- [orderPlayed](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsReturnedInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderCanceled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

### Datos de perfiles y segmentos del cliente

Los datos de perfil del cliente pueden revelar perspectivas sobre quiénes son sus compradores y para qué segmentos cumplen los requisitos. Por ejemplo:

- Nombre
- Sexo
- Dirección
- Estado de fidelización
- Número de teléfono
- Correo electrónico
- Estado de fidelización
- Número de teléfono
- Correo electrónico
- Idoneidad para las actualizaciones
- Compradores de canales cruzados
- Perspectivas de nuevos productos
- Miembros fieles de oro, plata o bronce

Los siguientes eventos de perfil capturan datos que pueden ayudarle a responder a estas preguntas:

- [Registro de perfil](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord)
- [accountCreated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [accountUpdated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [accountDeleted](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

Los datos de tienda, back office y perfil forman la base del contexto de cliente y pedido de Commerce, que le ayuda a saber qué productos están viendo sus clientes y, en última instancia, a comprar. A continuación, puede segmentar sus intereses y personalizar su experiencia. En la siguiente sección, aprenderá en qué tipos de experiencias personalizadas puede participar con sus compradores.

## Tipos de experiencias personalizadas

Los datos de contexto de cliente y pedido en Commerce alimentan los siguientes tipos de experiencias personalizadas:

| Experiencia | Descripción |
|---|---|
| **Descubrimiento de productos** | Contiene servicios de comercialización que [implementado como SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas). Son funciones que le permiten utilizar datos de comportamiento, atributos de producto y niveles de inventario para personalizar automáticamente la detección de productos en los resultados de búsqueda, las recomendaciones de productos y las páginas de exploración. Todas estas funciones utilizan [ADOBE SENSEI AI](https://business.adobe.com/products/sensei/adobe-sensei.html). |
| **Contenido del sitio** | Se refiere a la capacidad de implementar bloques de contenido dinámico personalizados en función de la navegación del cliente actual por el sitio. |
| **Ofertas y campañas** | Permite implementar contenido promocional personalizado basado en datos de segmentos. |
| **Medición** | Utiliza la inteligencia de datos para comprender mejor su negocio, incluidos los ingresos, el rendimiento de los canales y los productos, las promociones, etc. |

En las dos secciones siguientes, aprenderá a utilizar estos datos para crear experiencias personalizadas en [Adobe Experience Platform](#using-commerce-data-in-adobe-experience-platform) y en [funciones nativas de Commerce](#using-commerce-data-in-native-commerce-features).

## Uso de datos de Commerce en Adobe Experience Platform

Para crear una experiencia personalizada para sus compradores en todos los canales, envíe sus datos de comercio a Experience Platform Edge Network mediante el [[!DNL Data Connection]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview) extensión.

![Flujo de datos hasta el perímetro del Experience Platform](assets/commerce-edge.png){width="700" zoomable="yes"}

En la imagen anterior, los datos de perfil de la tienda, el back office y el cliente se envían al perímetro del Experience Platform mediante un SDK, API y un conector de origen. No es necesario que comprenda completamente cómo funcionan estos fragmentos, ya que la extensión gestiona la complejidad del uso compartido de datos por usted. Cuando los datos de evento se encuentran en el perímetro de, puede extraer esos datos en otras aplicaciones de Experience Platform.

La siguiente tabla resalta algunas de las aplicaciones Experience Platform disponibles y cómo utilizan esas aplicaciones los datos de Commerce.

| Experiencia | Aplicación | Uso de los datos de Commerce |
|---|---|---|
| **Contenido del sitio** | [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview) | Los datos de Adobe Commerce alimentan los perfiles unificados de los clientes, con datos de vinculación de Real-Time CDP de varias fuentes (ERP, CRM, CMS, POS) en perfiles únicos. Real-Time CDP también puede crear segmentos basados en reglas y en IA para utilizarlos después en todo el conjunto de soluciones de marketing. También puede utilizar las audiencias de Real-Time CDP para personalizar bloques de contenido, promociones y reglas de producto relacionadas. Consulte [[!DNL Audience Activation]](../customers/audience-activation.md) para obtener más información&#x200B; |
|  | [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro) | Los datos de Adobe Commerce se pueden activar en el Adobe [!DNL Target] para pruebas, optimización y creación de páginas de aterrizaje dinámicas. Puede personalizar el orden en que se muestra el contenido en una página, como descripciones, especificaciones, revisiones y productos recomendados basados en los datos de Commerce enviados. |
| **Ofertas y campañas** | [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started) | Los datos de comportamiento y de back-office de Adobe Commerce pueden servir de déclencheur para recorridos omnicanal personalizados, incluidas campañas de correo electrónico, SMS, notificaciones push y mucho más&#x200B; |
| **Medición** | [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview) y [Cliente [!DNL Journey Analytics]](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) | Commerce envía datos de la tienda y del back-office al cliente [!DNL Journey Analytics] (y solo datos de tienda para el Adobe) [!DNL Analytics]) para permitir un análisis más completo más allá de las métricas básicas en Adobe Commerce Intelligence, como ingresos, productos y promociones&#x200B;. |

Para obtener más información sobre cómo puede enviar los datos de Commerce al Experience Platform, consulte [Conexión de datos](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview).

## Uso de datos de Commerce en funciones nativas de Commerce

En la siguiente sección, aprenderá a utilizar funciones nativas de Commerce, como Product Recommendations y Live Search, para crear una experiencia de compra personalizada. También obtendrá información sobre una función llamada [!DNL Audience Activation], que utiliza datos de un producto disponible en el Experience Platform llamado Real-Time CDP, como se ha mencionado [anteriormente](#using-commerce-data-in-adobe-experience-platform). Aunque Real-Time CDP no es nativo de Commerce, su información se puede ingerir en Commerce a través del [[!DNL Audience Activation]](../customers/audience-activation.md) extensión.

La siguiente tabla resalta las funciones de Commerce disponibles para convertir los datos de contexto de clientes y pedidos de Commerce en perspectivas procesables.

| Experiencia | Función | Descripción |
|---|---|---|
| **Descubrimiento de productos** | [Live Search](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/guide-overview) | Utiliza algoritmos de clasificación de IA para personalizar y optimizar los resultados de búsqueda en función de las acciones de comportamiento en el sitio de un comprador, lo que aumenta la relevancia y la conversión de la búsqueda. |
|  | [Product Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) | Muestra recomendaciones de productos impulsadas por IA en función del comportamiento del comprador, las tendencias, la similitud del producto y mucho más. Cuando se combinan con su catálogo de Adobe Commerce, las recomendaciones de productos ofrecen una experiencia muy atractiva, relevante y personalizada. |
|  | [Comercialización por categorías](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch) | Desde el administrador de Live Search, la comercialización de categorías utiliza IA para clasificar automáticamente la secuencia de productos en cada página de categoría a fin de aumentar la relevancia y la conversión para cada comprador. Puede crear y administrar reglas con tecnología de IA para volver a clasificar automáticamente la secuenciación de productos en las páginas de categoría según las acciones y afinidades del comprador. |
| **Contenido del sitio** | [Bloques dinámicos basados en funciones nativas de Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | Le permite ofrecer contenido personalizado del sitio en función de la lógica configurada en las reglas de precios y los segmentos del cliente. |
|  | [Bloques dinámicos informados por audiencias de Real-Time CDP](../customers/audience-activation.md) | Permite a los comerciantes ofrecer contenido personalizado del sitio en función de las audiencias configuradas en Real-Time CDP. |
| **Ofertas y campañas** | [Reglas de precios del carrito](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart) | Permite aplicar descuentos a artículos del carro de compras en función de un conjunto de condiciones. |
|  | [Bloques dinámicos basados en funciones nativas de Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | Permite mostrar promociones de banner personalizadas basadas en segmentos de clientes configurados de forma nativa en Commerce. |
|  | [Bloques dinámicos informados por audiencias de Real-Time CDP](../customers/audience-activation.md) | Permite mostrar promociones personalizadas basadas en audiencias configuradas en Real-Time CDP. |
| **Medición** | [Adobe Commerce Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) | (anteriormente conocida como Magento Business Intelligence) es una plataforma de la nube que proporciona perspectivas de prácticas recomendadas para ayudarle a tomar decisiones basadas en datos y a tomar acciones claras e informadas. Adobe Commerce Intelligence puede analizar los datos para ayudarle a responder a preguntas sobre el crecimiento de los pedidos, el comportamiento de los clientes y la eficacia de las estrategias promocionales. |
