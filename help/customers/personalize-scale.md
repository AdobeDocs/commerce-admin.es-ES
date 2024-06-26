---
title: Cree experiencias atractivas y personalizadas a escala
description: Descubra las funciones de Adobe [!DNL Commerce] le permite crear una experiencia personalizada para sus compradores.
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 728a1fdb413009a00377cd8205dde93cd4feadc8
workflow-type: tm+mt
source-wordcount: '1808'
ht-degree: 0%

---

# Cree experiencias atractivas y personalizadas a escala

Adobe [!DNL Commerce] le ofrece un potente kit de herramientas para personalizar cada punto de contacto del cliente, lo que aumenta la participación del comprador, la conversión y los ingresos.

En este artículo, aprenderá lo siguiente:

- ¿Qué es la personalización?
- ¿Qué datos necesito para conseguir la personalización?
- ¿Cómo funciona el Adobe [!DNL Commerce] ¿Desbloquear personalización?
- Casos de uso de personalización disponibles

## ¿Qué es la personalización?

La personalización implica adaptar los aspectos de la experiencia de compra de cada cliente para satisfacer sus necesidades, contexto y preferencias únicos. La personalización no se limita al contenido del sitio ni a recomendar los productos que mejor se ajustan a sus necesidades, sino que abarca todos los puntos de contacto del recorrido del cliente, incluidos los siguientes:

- **Campañas y comunicaciones** : Entrega de mensajes relevantes y coherentes a través de campañas y comunicaciones
- **Descubrimiento de productos** - Mostrar los productos adecuados a los clientes adecuados en el momento adecuado
- **Promociones y ofertas** : promociones y ofertas de objetivos para dirigir a cada cliente a la conversión
- **Experiencias de contenido** - Adaptar el contenido del sitio para que se sienta hiper relevante para cada cliente y su recorrido

![Tipos de personalización](assets/types-personalization.png){width="700" zoomable="yes"}

Aunque estos tipos de experiencias personalizadas pueden parecer alcanzables para un pequeño subconjunto de clientes, personalizando a escala para miles o millones de clientes en cada punto de contacto y canal, todo en tiempo real puede parecer imposible. En las secciones siguientes, aprenderá a hacer Adobes [!DNL Commerce] y Adobe Experience Cloud pueden ayudarle.

## ¿Qué datos necesito para conseguir la personalización?

Una personalización eficaz requiere un contexto o señales que proporcionan información sobre los clientes que luego se pueden utilizar para modificar su experiencia. La siguiente tabla proporciona los distintos tipos de datos y la función que tienen en Adobe [!DNL Commerce] juega en apoyar la recopilación y activación de esos datos.

| Tipos de datos | Datos De Tienda (Eventos De Comportamiento) | Datos del back office (eventos del lado del servidor) | Datos de segmentos y perfil del cliente |
|---|---|---|---|
| **Definición** | Clics o acciones que los clientes realizan en el sitio. | Información sobre el ciclo de vida y detalles de cada pedido (anterior y actual). | Quiénes son sus compradores y para qué segmentos cumplen los requisitos. |
| **Eventos capturados por Adobe Commerce** | [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#pageview)<br>[productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)<br>[searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchrequestsent)<br>[searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchresponsereceived)<br>[addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtocart)<br>[openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#opencart)<br>[signIn](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signin)<br>[signOut](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signout)<br>[startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#startcheckout)<br>[completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#completecheckout)<br>[createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#createrequisitionlist)<br>[addToRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtorequisitionlist)<br>[removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#removefromrequisitionlist) | **Estado del pedido**:<br>[orderPlayed](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderplaced)<br>[orderItemsReturnedInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsreturnedinitiated)<br>[orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsshipped)<br>[orderCanceled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#ordercancelled)<br>[**Historial de pedidos**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/fundamentals/connect-data#send-historical-order-data):<br>- SKU, nombre, cantidad de precio, descuento<br>- Categoría de producto<br>- Importe, tipo y divisa del pago<br>- Método de envío e importe<br>- ID de reembolso, importe, moneda<br>- Motivo de devolución, condición, resolución<br>- Dirección<br>- Correo electrónico | [**Registro de perfil**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord): (Nombre, Sexo, Dirección, Estado de fidelidad, Número de teléfono, Dirección de correo electrónico)<br>**Estado de cuenta**:<br>[accountCreated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountcreated)<br>[accountUpdated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountupdated)<br>[accountDeleted](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountdeleted) |

Con todo esto rico, de primera parte [!DNL Commerce] , está listo para segmentar y personalizar la experiencia de cada comprador. En la siguiente sección, aprenderá cómo [!DNL Commerce] y Adobe Experience Cloud le ayudan a crear experiencias personalizadas y los casos de uso que puede activar.

## ¿Cómo funciona el Adobe [!DNL Commerce] ¿Habilitar la personalización?

Adobe [!DNL Commerce] El uso compartido de datos le permite recopilar y compartir los tipos de datos de la tabla anterior con otros productos de Adobe Experience Cloud para potenciar perfiles y audiencias de clientes unificados, campañas personalizadas y análisis y perspectivas enriquecidos.

![Flujo de datos hasta el perímetro del Experience Platform](assets/commerce-edge.png){width="700" zoomable="yes"}

Adobe [!DNL Commerce] Compartir datos incluye dos componentes clave:

1. [Conexión de datos](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview): comparta datos de perfil de tienda, back office y cliente desde el Adobe [!DNL Commerce] a la red perimetral de Adobe Experience Platform para su uso en todas las aplicaciones de Adobe Experience Cloud, incluidas:

   - [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview): vincule los datos de los clientes de diferentes fuentes (ERP, CRM, POS) a perfiles unificados y cree segmentos basados en reglas o en IA.
   - [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started): inicie recorridos omnicanal personalizados, incluidas campañas de correo electrónico, SMS, notificaciones push y mucho más.
   - [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) y [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview): obtenga información sobre el cliente y la empresa.
   - [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro): Pruebe y optimice contenido, productos recomendados, ofertas, navegación y mucho más.

1. [[!DNL Audience Activation]](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation): uso [!DNL Real-Time CDP] audiencias para personalizar bloques de contenido dinámico, promociones y reglas de producto relacionadas en su Adobe [!DNL Commerce] sitio.

### Experiencias de tienda personalizadas en cualquier canal a escala

Adobe [!DNL Commerce] puede aprovechar una tienda de alto rendimiento, llamada [Edge Delivery Services](https://experienceleague.adobe.com/developer/commerce/storefront/), para ofrecer experiencias personalizadas en todos sus canales, con las capacidades de IA en el núcleo y la velocidad como base.

Con los Edge Delivery Services, puede:

- **Crear contenido personalizado**: utilice la creación basada en documentos y la experimentación nativa con variaciones de texto e imagen de IA generativa para personalizar la experiencia a escala. Utilice la creación de contenido de Assets y de IA generativa para producir imágenes de productos y marketing a escala.

- **Generar variaciones**: permite a los autores de contenido utilizar la IA generativa para crear grandes volúmenes de informes personalizados controlados por IA [variaciones de contenido de texto e imagen](https://experienceleague.adobe.com/en/docs/experience-manager-learn/sites/generative-ai/generate-variations) con Adobe Firefly.

- **Implementar mediante la tienda de Edge Delivery Services**: contenido en Edge y funciones de Commerce con componentes integrados para crear experiencias de compra personalizadas para sus audiencias.

- **COMMERCE y ADOBE EXPERIENCE MANAGER ASSETS**: Creación de recursos de producto de IA generativa y variaciones a escala. Cree, entregue y supervise la entrega de contenido en cualquier canal.

![Página de complementos: Detalles del producto](assets/drop-in.png){width="700" zoomable="yes"}

### Personalización lista para usar: Introducción al Adobe nativo [!DNL Commerce] características

Adobe [!DNL Commerce] ofrece una potente personalización con sus funciones nativas listas para usar. En la tabla siguiente se describe [!DNL Commerce] funciones que puede activar inmediatamente para empezar a utilizar el recorrido de personalización.

| Categoría | Funciones |
|---|---|
| Descubrimiento personalizado de productos | [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview): personalice y optimice los resultados de búsqueda en función de las acciones de comportamiento en el sitio y las afinidades de un comprador con la búsqueda basada en IA.<br>[Comercialización inteligente de categorías](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch): clasificación de productos impulsada por IA en páginas de categoría según las acciones y afinidades de comportamiento en el sitio de un comprador.<br>[Product Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview): recomendaciones de productos con tecnología de IA basadas en el comportamiento, las tendencias y las afinidades de los compradores.<br>[Reglas de producto relacionadas](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules): defina reglas personalizadas para mostrar los productos del catálogo y así impulsar la venta cruzada y la mejora. |
| Contenido personalizado del sitio | [Bloques de contenido dinámico](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks): muestre bloques de contenido personalizados, por ejemplo titulares, basados en segmentos de clientes en Adobe Commerce. |
| Ofertas y promociones personalizadas | [Reglas de precio de carrito](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart): aplique descuentos a los artículos del carro de compras en función de un conjunto de condiciones, incluidos los segmentos de clientes en los Adobes [!DNL Commerce]. |
| Perspectivas y medición | [Adobe [!DNL Commerce] Inteligencia](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started): Comprenda cómo funcionan las estrategias de personalización y mejore con el tiempo. |

## Casos de uso de personalización principales

Adobe [!DNL Commerce] Los clientes de utilizan funciones integradas y comparten datos con Adobe Experience Cloud para una variedad de casos de uso. En las siguientes secciones se destacan los casos de uso principales y se describe cómo se implementan mediante el Adobe [!DNL Commerce] Solo o [!DNL Commerce] además de aplicaciones de Experience Cloud.

### Campañas y comunicaciones personalizadas

| Caso de uso | Solución |
|---|---|
| **Carro de compras abandonado y exploración** : Envíe un correo electrónico de renovación de la participación o una notificación personalizados cuando un cliente abandone el carro de compras o la sesión de navegación después de mostrar una alta participación | **Adobe [!DNL Commerce] Solo**:<br>[Recordatorios de correo electrónico](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules)<br>**Adobe [!DNL Commerce] con Adobe Journey Optimizer**:<br>[!DNL Commerce] Los datos de sirven como déclencheur para un recorrido de abandono omnicanal. Personalice ese recorrido en función de los atributos del cliente, lo que abandonó, otros comportamientos de compra y compras anteriores.<br>Commerce con Adobe Journey Optimizer y Real-Time CDP: adapte las campañas de abandono en función de perfiles de cliente unificados y audiencias administradas centralmente; por ejemplo, para crear una audiencia con una tasa de abandono alta. |
| **Creación centralizada de audiencias** : Cree audiencias basadas en reglas o potenciadas por IA basadas en el comportamiento en el sitio, las compras anteriores, los atributos de perfil, las afinidades de categoría, el estado de lealtad, el valor para el cliente y más | **Adobe [!DNL Commerce] Solo**:<br>Recopilar información del perfil del cliente cuando [!DNL Commerce] los clientes crean cuentas. Crear basado en reglas [segmentos del cliente](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/segments/customer-segments) y grupos de clientes para personalizar contenido y promociones.<br>**Adobe [!DNL Commerce] con Adobe Real-Time CDP**:<br> [Perfiles unificados](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home) desde fuentes de datos y canales; audiencias basadas en reglas o potenciadas por IA. |
| **Oferta personalizada de correo electrónico/SMS basada en el comportamiento del comprador** : envíe ofertas personalizadas a los clientes por correo electrónico segmentado en función de las compras anteriores y del comportamiento del comprador; por ejemplo, envíe ofertas para productos o categorías que los clientes hayan visto o con los que hayan participado. | **Adobe [!DNL Commerce] Solo**:<br>Exportar datos para utilizarlos con soluciones de automatización de marketing.<br>**Adobe [!DNL Commerce] con Adobe Journey Optimizer y Real-Time CDP**:<br>[!DNL Commerce] Los datos de sirven como déclencheur para ofertas de correo electrónico o SMS y proporcionan señales (comportamientos del comprador) que se pueden personalizar en función de. Real-Time CDP no es obligatorio, pero generalmente estas ofertas y campañas se crean en torno a audiencias, que se crearían y administrarían dentro de Real-Time CDP. |
| **Venta cruzada o superior de productos/marcas compatibles** : Si un cliente compra un producto o marca que es compatible o indica una alta afinidad hacia otro producto o marca, envíe una campaña (correo electrónico/SMS) para impulsar la conversión de ventas cruzadas. | **Adobe [!DNL Commerce] Solo**:<br>Usar Adobe [!DNL Commerce] [Product Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) para recomendar productos específicos en el sitio. También puede utilizar [Reglas de producto relacionadas](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) para sugerir otros productos.<br>**[!DNL Commerce] con [!DNL Target]**:<br>Adobe [!DNL Target] también tiene un motor de recomendación de productos integrado con potentes funciones, como la afinidad de la categoría. Se puede utilizar para realizar ventas cruzadas o adicionales.<br>**[!DNL Commerce] con Adobe Journey Optimizer**:<br>Uso [!DNL Target] o [!DNL Commerce] para determinar los productos que se van a recomendar, realice el envío mediante Adobe Journey Optimizer. |

### Experiencias del sitio personalizadas

| Caso de uso | Solución |
|---|---|
| **Contenido personalizado del sitio** : personalice los titulares del sitio y otro contenido de la página en función de las acciones del comprador, como la navegación por productos y las afinidades de categorías. Implemente contenido que se adapte mejor a los resultados de las pruebas A/B o a los objetivos empresariales. | **Adobe [!DNL Commerce] Solo**:<br>Implementar segmentos específicos [bloques de contenido dinámico](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks).<br>**[!DNL Commerce] con Real-Time CDP **:<br>Uso [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) implementar bloques de contenido dinámico específicos para audiencias que respondan a acciones en tiempo real y datos unificados de perfil del cliente, al tiempo que se administran perfiles y audiencias de forma centralizada en Real-Time CDP.<br>**[!DNL Commerce] con[!DNL Target]**:<br>Personalice cada parte de la experiencia del sitio, incluido el contenido, los elementos de navegación, los diseños de página completa y mucho más mediante el Adobe [!DNL Commerce] datos en Adobe [!DNL Target]. Contenido de prueba A/B, seleccione e implemente automáticamente contenido ganador para cada cliente.<br>**[!DNL Commerce] con AEM Assets **:<br>Almacene todo el contenido en Adobe Experience Manager Assets. Acceda de forma nativa a ese contenido desde Adobe Commerce. Utilice IA generativa para crear variaciones de contenido y personalizarlas para diferentes segmentos o audiencias. |
| **Oferta in situ personalizada basada en el comportamiento** - Personalice las promociones en función de las acciones del comprador, como la navegación por productos y las afinidades de categorías. Implemente la siguiente mejor oferta en función de los resultados de las pruebas A/B o los objetivos empresariales. | **Adobe [!DNL Commerce] Solo**:<br>Implementación de catálogos específicos de segmentos y [reglas de precios de carrito](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart).<br>**Adobe [!DNL Commerce] con Real-Time CDP**:<br>Uso [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) para implementar ofertas específicas de audiencia mientras se administran centralmente perfiles/audiencias en Real-Time CDP.<br>**Commerce con[!DNL Target]**: Utilice el offer decisioning para determinar qué oferta implementar, qué prueba A/B o qué objetivos empresariales guiar para las ofertas implementadas en Adobe Commerce. |

### Analytics y perspectivas

| Caso de uso | Solución |
|---|---|
| **Comportamiento del cliente por canal** : Comprenda los matices de cómo los clientes se relacionan con cada canal (web, en persona, aplicación, etc.) para afectar a las estrategias de marketing de cada canal; comprenda el canal del comprador y las debilidades en la experiencia del cliente. | **Adobe [!DNL Commerce] Solo**:<br>[Adobe [!DNL Commerce] Inteligencia](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) proporciona análisis enriquecidos en el entorno digital [!DNL Commerce] canal, pero no entre canales o partes más amplias del recorrido del cliente.<br>**Adobe [!DNL Commerce] con Customer Journey Analytics**:<br>[!DNL Commerce] fuentes de datos paneles de datos para obtener detalles completos y detallados sobre todas las etapas de la experiencia del cliente (en todos los canales). Comprenda cada punto de contacto y el embudo más amplio para identificar los puntos débiles del recorrido del cliente en los que estos pueden caer. |
| **Tendencias de compra** : Comprenda los comportamientos de compra a lo largo de un periodo de tiempo específico (por ejemplo, análisis de la cesta de compras, análisis de productos) para identificar tendencias, estacionalidad y optimizar el marketing en función de los patrones de compra históricos. | **Adobe [!DNL Commerce] Solo**:<br>[Adobe [!DNL Commerce] Inteligencia](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) proporciona análisis enriquecidos en el entorno digital [!DNL Commerce] canal, pero no entre canales o partes más amplias del recorrido del cliente.<br>**Adobe [!DNL Commerce] con Customer Journey Analytics**:<br>[!DNL Commerce] fuentes de datos paneles de datos para obtener detalles completos y detallados sobre todas las etapas de la experiencia del cliente (en todos los canales). Comprenda cada punto de contacto y el embudo más amplio para identificar los puntos débiles del recorrido del cliente en los que estos pueden caer. |

## Casos de uso de ejemplo

- Descubra cómo puede utilizar Adobe Journey Optimizer para lo siguiente [enviar un correo electrónico de carro de compras abandonado](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/using-ajo).
- Obtenga información sobre cómo [creación de una audiencia en Real-Time CDP](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/create-audience) para informar una regla de precio de carro de compras en Adobe [!DNL Commerce].
