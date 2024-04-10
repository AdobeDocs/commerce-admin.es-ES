---
title: Configurar la búsqueda en el catálogo
description: Aprenda a configurar la búsqueda en el catálogo de su tienda.
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# Configurar la búsqueda en el catálogo

Existen dos variaciones de la configuración de Búsqueda en el catálogo. El primer método describe la configuración disponible cuando [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) está instalado. El segundo método describe los ajustes de configuración para Adobe Commerce nativo con [Elasticsearch][1]{:target=&quot;_blank&quot;}.

## Método 1: Adobe Commerce con [!DNL Live Search]

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Catalog Search]** sección.

   ![Búsqueda en el catálogo de Live Search](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   Para ver una lista detallada de estas opciones, consulte [Adobe Commerce con Live Search](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) en el _Referencia de configuración_.

1. Para limitar la longitud y el número de palabras del texto de la consulta de búsqueda, defina un valor para **[!UICONTROL Minimal Query Length]** y **[!UICONTROL Maximum Query Length]**.

1. Para limitar la cantidad de resultados de búsqueda populares que se almacenarán en caché para obtener respuestas más rápidas, establezca una cantidad para **[!UICONTROL Number of top search results to cache]**.

   El valor predeterminado es `100`. Introducción de un valor de `0` almacena en caché todos los términos y resultados de búsqueda cuando se introducen por segunda vez.

1. Para cambiar el número máximo de líneas disponibles para los resultados devueltos en el [tienda pop over](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html), introduzca una diferente **[!UICONTROL Autocomplete Limit]** valor.

   Restringir el número de líneas mejora el rendimiento de las búsquedas y reduce el tamaño de la lista devuelta. El valor predeterminado es `8` líneas.

## Método 2: comercio con Elasticsearch

>[!IMPORTANT]
>
>Debido a la [!DNL Elasticsearch 7] anuncio de fin de soporte para agosto de 2023, se recomienda que todos los clientes de Adobe Commerce migren al motor de búsqueda OpenSearch 2.x. Para obtener información sobre la migración del motor de búsqueda durante la actualización del producto, consulte [Migración a OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) en el _Guía de actualización_.

### Paso 1: Configurar las opciones generales de búsqueda

>[!NOTE]
>
>Con Elasticsearch, no hay compatibilidad predeterminada para la búsqueda por el sufijo. Por ejemplo, la búsqueda por SKU puede no devolver el resultado esperado si la palabra clave contiene solo la parte final del SKU.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Catalog Search]** sección.

   ![Configuración del Elasticsearch](../configuration-reference/catalog/assets/catalog-search-elasticsearch.png){width="600" zoomable="yes"}

   Para obtener más información sobre estas opciones, consulte [Adobe Commerce con Elasticsearch](../configuration-reference/catalog/catalog.md#adobe-commerce-with-elasticsearch) en el _Referencia de configuración_.

1. Para limitar la longitud y el número de palabras del texto de la consulta de búsqueda, defina un valor para **[!UICONTROL Minimal Query Length]** y **[!UICONTROL Maximum Query Length]**.

   >[!IMPORTANT]
   >
   >El valor establecido para este rango mínimo y máximo debe ser compatible con el rango correspondiente establecido en la configuración del motor de búsqueda del Elasticsearch. Por ejemplo, si establece estos valores en `2` y `300` en Commerce, actualice los valores correspondientes en el motor de búsqueda.

1. Para limitar la cantidad de resultados de búsqueda populares que se almacenarán en caché para obtener respuestas más rápidas, establezca una cantidad para **[!UICONTROL Number of top search results to cache]**.

   El valor predeterminado es `100`. Introducción de un valor de `0` almacena en caché todos los términos y resultados de búsqueda cuando se introducen por segunda vez.

1. Si desea habilitar o deshabilitar el indizador EAV de productos, establezca el **[!UICONTROL Enable EAV Indexer]**.

   Esta función mejora la velocidad de indexación y restringe el uso del indexador por extensiones de terceros.

1. Para limitar el número máximo de resultados de búsqueda que se mostrarán para el completado automático de búsqueda, defina una cantidad para **[!UICONTROL Autocomplete Limit]**.

   Restringir esta cantidad aumenta el rendimiento de las búsquedas y reduce el tamaño de la lista mostrada. El valor predeterminado es `8`.

### Paso 2: Configuración de la conexión del Elasticsearch

>[!IMPORTANT]
>
>El **[!UICONTROL Search Engine]**, **[!UICONTROL Elasticsearch Server Hostname]**, **[!UICONTROL Elasticsearch Server Port]**, **[!UICONTROL Elasticsearch Index Prefix]**, **[!UICONTROL Enable Elasticsearch HTTP Auth]**, y **[!UICONTROL Elasticsearch Server Timeout]** Los campos de se configuraron al instalar o actualizar Commerce. Estos valores solo deben cambiarse al actualizar o modificar el Elasticsearch.

1. Para **[!UICONTROL Search Engine]**, acepte el valor predeterminado `Elasticsearch 7`.

   Se requiere el Elasticsearch 7.6.x para todas las instalaciones de Commerce.

1. Para **[!UICONTROL Elasticsearch Server Hostname]**, acepte el valor predeterminado que se configuró al instalar Commerce.

   En este ejemplo, el valor predeterminado es `elasticsearch.internal`.

1. Para **[!UICONTROL Elasticsearch Server Port]**, acepte el valor predeterminado que se configuró al instalar Commerce.

   En este ejemplo, el valor predeterminado es `9200`.

1. Para **[!UICONTROL Elasticsearch Index Prefix]**, introduzca un prefijo para identificar el índice del Elasticsearch.

   El valor predeterminado es `magento2`.

1. Para utilizar la autenticación HTTP para solicitar un nombre de usuario y una contraseña para acceder al servidor Elasticsearch, establezca **[!UICONTROL Enable Elasticsearch HTTP Auth]** hasta `Yes`.

1. Para **[!UICONTROL Elasticsearch Server Timeout]**, introduzca el número de segundos antes de que se agote el tiempo de espera del sistema.

   El valor predeterminado es `15`.

1. Para comprobar la configuración, haga clic en **[!UICONTROL Test Connection]**.

### Paso 3: Configurar sugerencias y recomendaciones

>[!NOTE]
>
>Las sugerencias y recomendaciones de búsqueda pueden afectar al rendimiento del servidor.

1. Para ofrecer recomendaciones, establezca **[!UICONTROL Enable Search Recommendations]** hasta `Yes` y haga lo siguiente:

   - Para **[!UICONTROL Search Recommendation Count]**, introduzca el número de recomendaciones que desea ofrecer.

   - Para mostrar el número de resultados encontrados para cada recomendación, establezca **[!UICONTROL Show Results Count for Each Recommendation]** hasta `Yes`.

1. Establecer **[!UICONTROL Enable Search Suggestions]** hasta `Yes` y haga lo siguiente:

   - Para **[!UICONTROL Search Suggestions Count]**, introduzca el número de sugerencias de búsqueda que desea ofrecer.

   - Para mostrar el número de resultados encontrados para cada sugerencia, establezca **[!UICONTROL Show Results for Each Suggestion]** hasta `Yes`.

### Paso 4: Configurar los términos mínimos de coincidencia

Para controlar el número mínimo de términos de la consulta que los resultados de la búsqueda deben coincidir para la devolución, especifique un valor para **[!UICONTROL Minimum Terms to Match]**. Especificar este valor garantiza una relevancia óptima de los resultados para los compradores. Para ver una lista de los valores aceptados, consulte [parámetro minimum_should_match](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-minimum-should-match.html) en la documentación del Elasticsearch.

Cuando termine, haga clic en **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/search/overview-search.html
