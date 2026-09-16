---
title: Redirecciones de término de búsqueda y enrutamiento de tiendas
description: Obtenga información sobre cómo elegir redirecciones de términos de búsqueda, reescrituras de URL, reglas de Live Search o enrutamiento de tiendas por implementación para Adobe Commerce y Edge Delivery Services.
feature: Merchandising, Search
role: Admin, User
level: Intermediate
topic: Commerce, Administration
autotag-review: '2026-09-10T17:42:01.349Z'
TQID: 'https://experienceleague.adobe.com/Vxw3B0zOzLZfAm3qn8gJKHGSNtVhkN2Bfmcauhj0sdM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 67a00b294f1946da5795cd8fb7ea9fac1c80edcd
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%
---
# Redirecciones de término de búsqueda y enrutamiento de tiendas

Las redirecciones de términos de búsqueda, las redirecciones de URL y la comercialización de búsquedas resuelven diferentes problemas. Utilice esta guía para elegir la funcionalidad correcta para la búsqueda estándar de [!DNL Adobe Commerce], [!DNL Live Search] y [!DNL Commerce Storefront] con tecnología de [!DNL Edge Delivery Services].

## Comprender los tipos de redirección

Estas capacidades difieren en los déclencheur del comportamiento y en lo que ve el comprador:

* Una **redirección de término de búsqueda** envía a un comprador que introduce un término de búsqueda específico a una página designada.

* Una **redirección de URL** envía una solicitud de una URL antigua a una nueva URL, normalmente con una respuesta HTTP 301 o 302. La barra de direcciones del explorador cambia a la nueva dirección URL.

* **La comercialización de búsqueda** cambia qué productos aparecen, o su pedido, en los resultados de búsqueda sin cambiar la dirección URL solicitada.

* Una **reescritura de URL** asigna una URL a otra en el servidor. La herramienta de reescritura de URL [!DNL Adobe Commerce] crea una redirección permanente (301) para la URL antigua. Para obtener más información, consulte [reescrituras de URL](url-rewrite.md).

## Elija una capacidad de enrutamiento

Siga estas directrices para identificar la capacidad que coincide con sus necesidades:

| Requisito | Capacidad recomendada |
| --- | --- |
| Enviar una consulta específica desde la búsqueda estándar [!DNL Adobe Commerce] a una página | Configure un término de búsqueda en [Administrar términos de búsqueda](../catalog/search-terms.md), si es compatible. |
| Cambiar la clasificación o visibilidad del producto en los resultados de búsqueda | Usar [!DNL Live Search] [sinónimos](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/synonyms/synonyms) o [reglas de comercialización](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/rules/rules-add). |
| Redireccionar un producto, categoría o dirección URL de CMS antiguos | Utilice la herramienta Commerce [Reescritura de URL](url-rewrite.md) cuando se aplique a su implementación. |
| Redirigir una ruta de acceso de [!DNL Edge Delivery Services] | Utilizar enrutamiento de tienda o CDN. |
| Conservar direcciones URL heredadas después de una migración de tienda | Cree y pruebe una asignación de redireccionamiento de URL de heredada a nueva. |

## Búsqueda estándar de Commerce

Con la búsqueda en el catálogo estándar, puede configurar un término de búsqueda para abrir una página de contenido, una página de categoría, una página de producto o una página externa donde la implementación admita esta capacidad. Utilícelo cuando una consulta ingresada por el comprador, como `gift cards` o `returns`, deba abrir una campaña o página informativa.

Para crear o actualizar este tipo de redireccionamiento, consulte [Administrar términos de búsqueda](../catalog/search-terms.md). La configuración de término de búsqueda es independiente de la herramienta de reescritura de URL porque el déclencheur es la consulta del comprador, no una URL existente.

>[!NOTE]
>
>Confirme que la tienda utiliza la búsqueda en el catálogo estándar y admite redirecciones de términos de búsqueda nativas. El comportamiento y la configuración disponible pueden diferir para [!DNL Live Search], [!DNL Adobe Commerce as a Cloud Service] o una tienda sin encabezado.

## Redirecciones y reescrituras de URL

Utilice una reescritura de URL cuando el origen sea una URL existente en lugar de un término de búsqueda introducido por el comprador. Algunos ejemplos comunes son las redirecciones:

* Una URL de producto antigua a una nueva URL de producto.

* Una URL de categoría retirada a una URL de categoría de reemplazo.

* Una URL de página CMS obsoleta que lleva a una nueva URL de página de contenido.

Para implementaciones que admiten la herramienta de reescritura de URL, vaya a **[!UICONTROL Marketing]** > **[!UICONTROL SEO & Search]** > **[!UICONTROL URL Rewrites]** para crear la redirección. Para obtener instrucciones paso a paso, consulte [reescrituras de URL](url-rewrite.md).

>[!NOTE]
>
>El tema [URL reescribe](url-rewrite.md) se aplica solo a PaaS. Para [!DNL Adobe Commerce as a Cloud Service] o una tienda [!DNL Edge Delivery Services], usa la guía de enrutamiento para esa tienda en su lugar.

## Live Search

[!DNL Live Search] reemplaza la experiencia de búsqueda predeterminada en tiendas y proporciona capacidades como sinónimos, facetas y reglas de comercialización.

Use [!DNL Live Search] cuando necesite cambiar la relevancia de búsqueda, la clasificación del producto o la visibilidad del producto. Utilice sinónimos cuando palabras diferentes deban devolver productos similares. Utilice reglas de comercialización cuando los productos deban aumentarse, enterrarse o clasificarse de forma diferente.

El comportamiento de búsqueda [!DNL Live Search] no debe tratarse como un reemplazo desplegable para cada configuración de término de búsqueda nativa de Commerce. Cuando una consulta debe navegar a una página de contenido o campaña, implemente la redirección en la capa de tienda o de enrutamiento de Edge que recibe la solicitud. Para obtener más información, consulte la [[!DNL Live Search] documentación](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview).

## Edge Delivery Services

Para una tienda con tecnología de [!DNL Edge Delivery Services], administra las redirecciones en la capa de tienda o de enrutamiento de Edge. No dé por hecho que la URL de administrador de [!DNL Adobe Commerce] vuelve a escribir para controlar cada solicitud.

Cuando utilice la creación de documentos, mantenga las asignaciones de redireccionamiento en la configuración de redireccionamiento del sitio. Para las redirecciones que deben ejecutarse antes de que una solicitud alcance el origen, utilice la configuración de CDN o Edge adecuada. Para obtener instrucciones de optimización de los motores de búsqueda relacionadas, consulte [Directrices de optimización de los motores de búsqueda para Commerce Storefront](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/).

## Migrar desde Luma

Trate la migración de redireccionamiento como parte de la migración de tienda. Conservar el recorrido del cliente y la intención de SEO y, a continuación, volver a implementar el enrutamiento para la tienda de destino.

Antes de cambiar el tráfico a la nueva tienda:

1. Exportar e inventariar las URL de Luma y las páginas de aterrizaje de término de búsqueda existentes.

1. Clasifique cada elemento como una regla de redireccionamiento de términos de búsqueda, redireccionamiento de URL o comercialización.

1. Asigne cada URL heredada a su nueva ruta de tienda.

1. Implemente cada redirección en la capa que recibe la solicitud.

1. Pruebe códigos de estado, parámetros de consulta, direcciones URL canónicas, rutas de configuración regional y bucles de redirección.

1. Monitorice los registros y análisis después del inicio para ver las URL heredadas no resueltas.

## Solución de problemas de redirecciones

Realice las siguientes comprobaciones cuando una redirección no se comporte como se espera en [!DNL Adobe Commerce] vistas de búsqueda, enrutamiento de tienda y tienda.

| Problema | Qué comprobar |
| --- | --- |
| Un término de búsqueda no se redirige | Confirme que la tienda utiliza la búsqueda estándar en el catálogo, que la consulta de búsqueda coincide con el término configurado y que el término de búsqueda se asigna a la vista de tienda correcta. Si [!DNL Live Search] está habilitado, verifique que el redireccionamiento se implemente en la capa de la tienda o del borde. |
| Una redirección funciona en Luma pero no en Edge Delivery Services | Confirme que la redirección está configurada en la capa de enrutamiento de CDN o tienda [!DNL Edge Delivery Services]. [!DNL Adobe Commerce] Es posible que las reescrituras de URL de administrador no reciban la solicitud. |
| Live Search devuelve resultados en lugar de redirecciones | Usar reglas [!DNL Live Search] para la clasificación y visibilidad de productos. Para navegar a una página de contenido o de campaña, configure el redireccionamiento en la capa de tienda o de Edge. |
| Una redirección funciona en una vista de tienda, pero no en otra | Compruebe la vista de tienda asignada al término de búsqueda o a la regla URL. Pruebe la ruta de configuración regional completa y la consulta en cada vista de tienda afectada. |

## Más ayuda sobre este tema

* [Información general de SEO y prácticas recomendadas](seo-overview.md)

* [¿Qué es la tienda?](../getting-started/storefront.md)

* [Administrar términos de búsqueda](../catalog/search-terms.md)

* [Reescrituras de URL](url-rewrite.md)
