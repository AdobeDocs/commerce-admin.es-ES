---
title: Cree experiencias atractivas y personalizadas a escala
description: Conozca qué funciones de Adobe [!DNL Commerce] le permiten crear una experiencia personalizada para sus compradores.
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '1808'
ht-degree: 0%

---

# Cree experiencias atractivas y personalizadas a escala

Adobe [!DNL Commerce] le ofrece un potente conjunto de herramientas para personalizar cada punto de contacto de cliente, lo que aumenta la participación del comprador, la conversión y los ingresos.

En este artículo, aprenderá lo siguiente:

- ¿Qué es la personalización?
- ¿Qué datos necesito para conseguir la personalización?
- ¿Cómo desbloquea la personalización Adobe [!DNL Commerce]?
- Casos de uso de personalización disponibles

## ¿Qué es la personalización?

Personalization significa adaptar aspectos de la experiencia de compra de cada cliente para satisfacer sus necesidades, contexto y preferencias únicos. Personalization no se limita al contenido del sitio ni a recomendar los productos que mejor se ajustan a sus necesidades, sino que abarca todos los puntos de contacto del recorrido del cliente, incluidos los siguientes:

- **Campañas y comunicaciones**: entrega mensajes relevantes y coherentes a través de campañas y comunicaciones
- **Descubrimiento de productos**: se muestran los productos adecuados a los clientes adecuados en el momento adecuado
- **Promociones y ofertas**: promociones y ofertas de destino para lograr que cada cliente realice la conversión
- **Experiencias de contenido**: adapte el contenido del sitio para que se sienta hiper relevante para cada cliente y su recorrido

![Tipos de Personalization](assets/types-personalization.png){width="700" zoomable="yes"}

Aunque estos tipos de experiencias personalizadas pueden parecer alcanzables para un pequeño subconjunto de clientes, personalizando a escala para miles o millones de clientes en cada punto de contacto y canal, todo en tiempo real puede parecer imposible. En las secciones siguientes, aprenderá cómo Adobe [!DNL Commerce] y Adobe Experience Cloud pueden ayudarle.

## ¿Qué datos necesito para conseguir la personalización?

Una personalización eficaz requiere un contexto o señales que proporcionan información sobre los clientes que luego se pueden utilizar para modificar su experiencia. La siguiente tabla proporciona los distintos tipos de datos y la función que Adobe [!DNL Commerce] desempeña en la compatibilidad de la recopilación y activación de esos datos.

| Tipos de datos | Datos De Tienda (Eventos De Comportamiento) | Datos del back office (eventos del lado del servidor) | Datos de segmentos y perfil del cliente |
|---|---|---|---|
| **Definición** | Clics o acciones que los clientes realizan en el sitio. | Información sobre el ciclo de vida y detalles de cada pedido (anterior y actual). | Quiénes son sus compradores y para qué segmentos cumplen los requisitos. |
| **Eventos capturados por Adobe Commerce** | [pageView](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#pageview)<br>[productPageView](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events)<br>[searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#searchrequestsent)<br>[searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#searchresponsereceived)<br>[addToCart](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#addtocart)<br>[openCart](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#opencart)<br>[signIn](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#signin)<br>[signOut](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#signout)<br>[startCheckout](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#startcheckout)<br>[completeCheckout](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#completecheckout)<br>[createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#createrequisitionlist)<br>[addToRequisitionList](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#addtorequisitionlist)<br>[removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#removefromrequisitionlist) | **Estado del pedido**:<br>[orderPlayed](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#orderplaced)<br>[orderItemsReturnedInitiated](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#orderitemsreturnedinitiated)<br>[orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#orderitemsshipped)<br>[orderCanceled](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#ordercancelled)<br>[**Historial del pedido**](https://experienceleague.adobe.com/en/docs/commerce/data-connection/fundamentals/connect-data#send-historical-order-data):<br>- SKU, nombre, cantidad del precio, descuento<br>- Categoría del producto<br>- Importe del pago, tipo, divisa<br>- Método de envío e importe<br>- ID del reembolso, importe, divisa de devolución<br>- Motivo, condición, resolución<br>- Dirección<br>- Correo electrónico | [**Registro de perfil**](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-profilerecord): (Nombre, Sexo, Dirección, Estado de fidelidad, Número de teléfono, Dirección de correo electrónico)<br>**Estado de la cuenta**:<br>[accountCreated](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#accountcreated)<br>[accountUpdated](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#accountupdated)<br>[accountDeleted](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#accountdeleted) |

Con todos estos datos enriquecidos de [!DNL Commerce] de origen, está listo para personalizar y segmentar la experiencia de cada comprador. En la siguiente sección, aprenderá cómo [!DNL Commerce] y Adobe Experience Cloud le ayudan a crear experiencias personalizadas y los casos de uso que puede activar.

## ¿Cómo habilita la personalización Adobe [!DNL Commerce]?

El uso compartido de datos de Adobe [!DNL Commerce] le permite recopilar y compartir los tipos de datos de la tabla anterior con otros productos de Adobe Experience Cloud para potenciar los perfiles y audiencias unificados de los clientes, las campañas personalizadas y los análisis y perspectivas enriquecidos.

![Flujo de datos al perímetro de Experience Platform](assets/commerce-edge.png){width="700" zoomable="yes"}

El uso compartido de datos de Adobe [!DNL Commerce] incluye dos componentes clave:

1. [Conexión de datos](https://experienceleague.adobe.com/en/docs/commerce/data-connection/overview): comparta datos de tienda, back office y perfil de cliente de Adobe [!DNL Commerce] con la red perimetral de Adobe Experience Platform para usarlos en aplicaciones de Adobe Experience Cloud, entre ellas:

   - [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview): vincule los datos del cliente de diferentes fuentes (ERP, CRM, POS) a perfiles unificados y cree segmentos basados en reglas o en IA.
   - [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started): inicia recorridos omnicanal personalizados, como campañas por correo electrónico, SMS, notificaciones push y mucho más.
   - [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) y [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview): obtenga información sobre el cliente y la empresa.
   - [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro): Pruebe y optimice contenido, productos recomendados, ofertas, navegación y mucho más.

1. [[!DNL Audience Activation]](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation): Use las audiencias de [!DNL Real-Time CDP] para personalizar bloques de contenido dinámico, promociones y reglas de producto relacionadas en el sitio de Adobe [!DNL Commerce].

### Experiencias de tienda personalizadas en cualquier canal a escala

Adobe [!DNL Commerce] puede aprovechar una tienda de alto rendimiento, llamada [Edge Delivery Services](https://experienceleague.adobe.com/developer/commerce/storefront/), para ofrecer experiencias personalizadas en todos tus canales, con capacidades de IA en el núcleo y velocidad como base.

Con Edge Delivery Services, puede:

- **Cree contenido personalizado**: use la creación basada en documentos y la experimentación nativa con variaciones de texto e imagen de inteligencia artificial generativa para personalizar la experiencia a escala. Utilice la creación de contenido de Assets e IA generativa para producir imágenes de productos y marketing a escala.

- **Generar variaciones**: permite a los autores de contenido utilizar IA generativa para crear grandes volúmenes de [variaciones de contenido de texto e imagen](https://experienceleague.adobe.com/en/docs/experience-manager-learn/sites/generative-ai/generate-variations) personalizadas impulsadas por IA con Adobe Firefly.

- **Implementar a través de Edge Delivery Services Storefront**: Contenido en las capacidades de Edge y Commerce con componentes desplegables para crear experiencias de compra personalizadas para sus audiencias.

- **Commerce y Adobe Experience Manager Assets**: creación de recursos de productos de IA generativa y variaciones a escala. Cree, entregue y supervise la entrega de contenido en cualquier canal.

![Colocaciones: página de detalles del producto](assets/drop-in.png){width="700" zoomable="yes"}

### Personalization de serie: Introducción a las características nativas de Adobe [!DNL Commerce]

Adobe [!DNL Commerce] ofrece una personalización potente con sus funciones nativas listas para usarse. En la tabla siguiente se describen [!DNL Commerce] características que puede activar inmediatamente para comenzar con el recorrido de personalización.

| Categoría | Funciones |
|---|---|
| Descubrimiento personalizado de productos | [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview): personalice y optimice los resultados de búsqueda en función de las acciones de comportamiento y afinidades del comprador en el sitio con la búsqueda con tecnología de IA.<br>[Comercialización inteligente de categorías](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/category-merch): clasificación de productos basada en IA en páginas de categorías según las acciones y afinidades de comportamiento de un comprador en el sitio.<br>[Recomendaciones de productos](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview): recomendaciones de productos con tecnología de IA basadas en el comportamiento, las tendencias y las afinidades de los compradores.<br>[Reglas de producto relacionadas](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules): defina reglas personalizadas para mostrar los productos del catálogo a fin de impulsar la venta cruzada y la mejora. |
| Contenido personalizado del sitio | [Bloques de contenido dinámico](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks): Muestre bloques de contenido personalizados, por ejemplo, banners, basados en segmentos de clientes en Adobe Commerce. |
| Ofertas y promociones personalizadas | [Reglas de precio del carro de compras](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart): aplique descuentos a los artículos del carro de compras en función de un conjunto de condiciones, incluidos los segmentos de clientes en Adobe [!DNL Commerce]. |
| Perspectivas y medición | [Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started): comprenda cómo funcionan y mejoran sus estrategias de personalización con el tiempo. |

## Casos de uso de personalización principales

Los clientes de Adobe [!DNL Commerce] están usando funcionalidades integradas y compartiendo datos con Adobe Experience Cloud para una variedad de casos de uso. Las secciones siguientes resaltan los casos de uso principales y describen cómo se implementan usando solo Adobe [!DNL Commerce] o [!DNL Commerce] además de las aplicaciones de Experience Cloud.

### Campañas y comunicaciones personalizadas

| Caso de uso | Solución |
|---|---|
| **Carro de compras y exploración abandonados**: envíe un correo electrónico o una notificación de renovación de la participación personalizada cuando un cliente abandone el carro de compras o la sesión de exploración después de mostrar una participación alta | **Solo Adobe [!DNL Commerce]**:<br>[Recordatorios de correo electrónico](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules)<br>**Adobe [!DNL Commerce] con Adobe Journey Optimizer**:<br>[!DNL Commerce] datos sirve como déclencheur para un recorrido de abandono omnicanal. Personalice ese recorrido en función de los atributos del cliente, lo que abandonó, otros comportamientos de compra y compras anteriores.<br>Commerce con Adobe Journey Optimizer y Real-Time CDP: adapte las campañas de abandono en función de perfiles unificados de clientes y audiencias administradas centralmente, por ejemplo creando una audiencia con una tasa de abandono alta. |
| **Creación centralizada de audiencias**: cree audiencias basadas en reglas o en IA según el comportamiento en el sitio, las compras anteriores, los atributos de perfil, las afinidades de categoría, el estado de lealtad, el valor para el cliente y más | **Solo Adobe [!DNL Commerce]**:<br>Recopile información de perfil de cliente cuando los clientes de [!DNL Commerce] creen cuentas. Cree [segmentos de clientes](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/segments/customer-segments) y grupos de clientes basados en reglas para personalizar el contenido y las promociones.<br>**Adobe [!DNL Commerce] con Adobe Real-Time CDP**:<br> [Perfiles unificados](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home) de fuentes de datos y canales; audiencias basadas en reglas o potenciadas por IA. |
| **Oferta de correo electrónico/SMS personalizada según el comportamiento del comprador**: envía ofertas personalizadas a los clientes por correo electrónico segmentado en función de las compras anteriores y del comportamiento del comprador; por ejemplo, envía ofertas para productos o categorías que los clientes hayan visto o con los que hayan participado. | **Solo [!DNL Commerce] de Adobe**:<br>Exporte datos para usarlos con soluciones de automatización de marketing.<br>**Adobe [!DNL Commerce] con Adobe Journey Optimizer y Real-Time CDP**:<br>[!DNL Commerce] los datos sirven como déclencheur para ofertas de correo electrónico o SMS y proporciona señales (comportamientos de comprador) que se pueden personalizar en función de. Real-Time CDP no es obligatorio, pero generalmente estas ofertas y campañas se crean en torno a audiencias, que se crearían y administrarían dentro de Real-Time CDP. |
| **Productos y marcas compatibles con las ventas cruzadas o adicionales**: si un cliente compra un producto o marca que es compatible o indica una alta afinidad hacia otro producto o marca, envíe una campaña (correo electrónico/SMS) para impulsar la conversión de ventas cruzadas. | **Solo [!DNL Commerce] de Adobe**:<br>Use Adobe [!DNL Commerce] [Product Recommendations](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview) para recomendar productos específicos en el sitio. También puede usar [Reglas de producto relacionadas](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) para sugerir otros productos.<br>**[!DNL Commerce] con [!DNL Target]**:<br>Adobe [!DNL Target] también tiene un motor de recomendaciones de productos integrado con capacidades potentes, como la afinidad de la categoría. Se puede utilizar para realizar ventas cruzadas o adicionales.<br>**[!DNL Commerce] con Adobe Journey Optimizer**:<br>Use [!DNL Target] o [!DNL Commerce] para determinar los productos que se recomendarán y luego entreguen mediante Adobe Journey Optimizer. |

### Experiencias del sitio personalizadas

| Caso de uso | Solución |
|---|---|
| **Contenido personalizado del sitio**: personalice los titulares del sitio y otro contenido de la página en función de las acciones del comprador, como la exploración de productos y las afinidades de categorías. Implemente contenido que se adapte mejor a los resultados de las pruebas A/B o a los objetivos empresariales. | **Solo Adobe [!DNL Commerce]**:<br>Implementa [bloques de contenido dinámico específicos del segmento](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks).<br>**[!DNL Commerce] con Real-Time CDP &#x200B;**:<br>Use [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) para implementar bloques de contenido dinámico específicos de la audiencia que respondan a acciones en tiempo real y a datos unificados del perfil del cliente, mientras administra perfiles y audiencias de forma centralizada en Real-Time CDP.<br>**[!DNL Commerce] con[!DNL Target]**:<br>Personalice todas las partes de la experiencia del sitio, incluido el contenido, los elementos de navegación, los diseños de página completa y mucho más, utilizando los datos de Adobe [!DNL Commerce] en Adobe [!DNL Target]. Contenido de prueba A/B, seleccione e implemente automáticamente contenido ganador para cada cliente.<br>**[!DNL Commerce] con AEM Assets &#x200B;**:<br>Almacena todo tu contenido en Adobe Experience Manager Assets. Acceda de forma nativa a ese contenido desde Adobe Commerce. Utilice IA generativa para crear variaciones de contenido y personalizarlas para diferentes segmentos o audiencias. |
| **Oferta personalizada en el sitio basada en el comportamiento**: personalice las promociones según las acciones del comprador, como la exploración de productos y las afinidades de categorías. Implemente la siguiente mejor oferta en función de los resultados de las pruebas A/B o los objetivos empresariales. | **Solo Adobe [!DNL Commerce]**:<br>Implementar reglas de precio de carro de compras y catálogo específicos de segmentos[.](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart)<br>**Adobe [!DNL Commerce] con Real-Time CDP**:<br>Use [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) para implementar ofertas específicas para audiencias, mientras administra perfiles/audiencias de forma centralizada en Real-Time CDP.<br>**Commerce con[!DNL Target]**: utilice Offer Decisioning para determinar qué oferta implementar, prueba A/B o establecer objetivos comerciales para guiar las ofertas implementadas en Adobe Commerce. |

### Analytics y perspectivas

| Caso de uso | Solución |
|---|---|
| **Comportamiento del cliente por canal**: comprenda los matices de cómo los clientes interactúan con cada canal (web, en persona, aplicación, etc.) para afectar a las estrategias de marketing de cada canal; comprenda el canal del comprador y las debilidades en la experiencia del cliente. | **Solo Adobe [!DNL Commerce]**:<br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) proporciona análisis enriquecidos en el canal digital [!DNL Commerce], pero no en canales o partes más amplias del recorrido del cliente.<br>**Adobe [!DNL Commerce] con Customer Journey Analytics**:<br>[!DNL Commerce] paneles de datos de fuentes de datos para obtener información detallada completa sobre todas las etapas de la experiencia del cliente (en todos los canales). Comprenda cada punto de contacto y el embudo más amplio para identificar los puntos débiles del recorrido del cliente en los que estos pueden caer. |
| **Tendencias de compra**: comprenda los comportamientos de compra a lo largo de un lapso de tiempo específico (por ejemplo, análisis de la cesta de la compra, análisis de productos) para identificar tendencias, estacionalidad y optimizar el marketing en función de los patrones de compra históricos. | **Solo Adobe [!DNL Commerce]**:<br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) proporciona análisis enriquecidos en el canal digital [!DNL Commerce], pero no en canales o partes más amplias del recorrido del cliente.<br>**Adobe [!DNL Commerce] con Customer Journey Analytics**:<br>[!DNL Commerce] paneles de datos de fuentes de datos para obtener información detallada completa sobre todas las etapas de la experiencia del cliente (en todos los canales). Comprenda cada punto de contacto y el embudo más amplio para identificar los puntos débiles del recorrido del cliente en los que estos pueden caer. |

## Casos de uso de ejemplo

- Aprenda a usar Adobe Journey Optimizer para [enviar un correo electrónico sobre el carro de compras abandonado](https://experienceleague.adobe.com/en/docs/commerce/data-connection/use-cases/using-ajo).
- Aprenda a [crear una audiencia en Real-Time CDP](https://experienceleague.adobe.com/en/docs/commerce/data-connection/use-cases/create-audience) para informar sobre una regla de precio del carro de compras en Adobe [!DNL Commerce].
