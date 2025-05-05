---
title: Configurar la búsqueda en el catálogo
description: Aprenda a configurar la búsqueda en el catálogo de su tienda.
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 0%

---

# Configurar la búsqueda en el catálogo

Existen dos variaciones de la configuración de Búsqueda en el catálogo. El primer método describe la configuración disponible cuando está instalado [Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=es). El segundo método describe las opciones de configuración para Adobe Commerce nativo con [OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html?lang=es){:target="_blank"}.

>[!NOTE]
>
>Para los proyectos de infraestructura en la nube, consulte las instrucciones adicionales en la [_Guía de infraestructura en la nube de Commerce_](https://experienceleague.adobe.com/es/docs/commerce-cloud-service/user-guide/configure/service/opensearch).

## Método 1: Adobe Commerce con [!DNL Live Search]

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Catalog Search]**.

   ![Búsqueda en el catálogo de Live Search](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   Para obtener una lista detallada de estas opciones, consulte [Adobe Commerce con Live Search](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) en la _Referencia de configuración_.

1. Para limitar la longitud y el número de palabras del texto de la consulta de búsqueda, establezca un valor para **[!UICONTROL Minimal Query Length]** y **[!UICONTROL Maximum Query Length]**.

1. Para limitar la cantidad de resultados de búsqueda populares que se almacenarán en caché para obtener respuestas más rápidas, establezca una cantidad para **[!UICONTROL Number of top search results to cache]**.

   El valor predeterminado es `100`. Si se introduce un valor de `0`, se almacenarán en la memoria caché todos los términos de búsqueda y resultados cuando se introduzcan por segunda vez.

1. Para cambiar el número máximo de líneas disponibles para los resultados devueltos en la [ventana emergente de la tienda](https://experienceleague.adobe.com/docs/commerce/live-search/live-search-storefront/quick-tour.html?lang=es), escriba un valor de **[!UICONTROL Autocomplete Limit]** diferente.

   Restringir el número de líneas mejora el rendimiento de las búsquedas y reduce el tamaño de la lista devuelta. El valor predeterminado es `8` líneas.

## Método 2: Commerce con OpenSearch

>[!IMPORTANT]
>
>- Debido al anuncio de fin de soporte de [!DNL Elasticsearch 7] para agosto de 2023, se recomienda que todos los clientes de Adobe Commerce migren al motor de búsqueda OpenSearch 2.x. Para obtener información sobre cómo migrar el motor de búsqueda durante la actualización del producto, consulte [Migración a OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html?lang=es) en la _Guía de actualización_.
>- En las versiones 2.4.4 y 2.4.3-p2, todos los campos etiquetados como Elasticsearch también se aplican a OpenSearch. Cuando se introdujo la compatibilidad con Elasticsearch 8.x en la versión 2.4.6, se crearon nuevas etiquetas para distinguir entre las configuraciones de Elasticsearch y OpenSearch. Sin embargo, las opciones de configuración para ambos son las mismas.

### Paso 1: Configurar las opciones generales de búsqueda

>[!NOTE]
>
>Con OpenSearch y Elasticsearch, no hay compatibilidad predeterminada para la búsqueda por el sufijo. Por ejemplo, la búsqueda por SKU puede no devolver el resultado esperado si la palabra clave contiene solo la parte final del SKU.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Catalog Search]**.

   ![Configuración del motor de búsqueda](../configuration-reference/catalog/assets/catalog-search-opensearch.png){zoomable="yes"}

   Para obtener más información sobre estas opciones, consulte [Adobe Commerce con búsqueda nativa](../configuration-reference/catalog/catalog.md#adobe-commerce-with-native-search) en la _Referencia de configuración_.

1. Para limitar la longitud y el número de palabras del texto de la consulta de búsqueda, establezca un valor para **[!UICONTROL Minimal Query Length]** y **[!UICONTROL Maximum Query Length]**.

   >[!IMPORTANT]
   >
   >El valor establecido para este rango mínimo y máximo debe ser compatible con el rango correspondiente establecido en la configuración del motor de búsqueda. Por ejemplo, si establece estos valores en `2` y `300` en Commerce, actualice los valores correspondientes en el motor de búsqueda.

1. Para limitar la cantidad de resultados de búsqueda populares que se almacenarán en caché para obtener respuestas más rápidas, establezca una cantidad para **[!UICONTROL Number of top search results to cache]**.

   El valor predeterminado es `100`. Si se introduce un valor de `0`, se almacenarán en la memoria caché todos los términos de búsqueda y resultados cuando se introduzcan por segunda vez.

1. Si desea habilitar o deshabilitar el indizador EAV del producto, establezca **[!UICONTROL Enable EAV Indexer]**.

   Esta función mejora la velocidad de indexación y restringe el uso del indexador por extensiones de terceros.

1. Para limitar el número máximo de resultados de búsqueda que se mostrarán para el completado automático de búsqueda, establezca una cantidad para **[!UICONTROL Autocomplete Limit]**.

   Restringir esta cantidad aumenta el rendimiento de las búsquedas y reduce el tamaño de la lista mostrada. El valor predeterminado es `8`.

### Paso 2: Configurar la conexión de OpenSearch

>[!IMPORTANT]
>
>Los campos **[!UICONTROL Search Engine]**, **[!UICONTROL OpenSearch Server Hostname]**, **[!UICONTROL OpenSearch Server Port]**, **[!UICONTROL OpenSearch Index Prefix]**, **[!UICONTROL Enable OpenSearch HTTP Auth]** y **[!UICONTROL OpenSearch Server Timeout]** se configuraron al instalar o actualizar Commerce. Estos valores solo deben cambiarse al actualizar o modificar OpenSearch.

1. Para **[!UICONTROL Search Engine]**, seleccione `OpenSearch`.

1. Para **[!UICONTROL OpenSearch Server Hostname]**, acepte el valor predeterminado que se configuró al instalar Commerce.

1. Para **[!UICONTROL OpenSearch Server Port]**, acepte el valor predeterminado que se configuró al instalar Commerce.

   En este ejemplo, el valor predeterminado es `9200`.

1. Para **[!UICONTROL OpenSearch Index Prefix]**, escriba un prefijo para identificar el índice de Elasticsearch.

   El valor predeterminado es `magento2`.

1. Para usar la autenticación HTTP para solicitar un nombre de usuario y una contraseña para acceder al servidor OpenSearch, establezca **[!UICONTROL Enable OpenSearch HTTP Auth]** en `Yes`.

1. Para **[!UICONTROL OpenSearch Server Timeout]**, escriba el número de segundos antes de que se agote el tiempo de espera del sistema.

   El valor predeterminado es `15`.

1. Para comprobar la configuración, haga clic en **[!UICONTROL Test Connection]**.

### Paso 3: Configurar sugerencias y recomendaciones

>[!NOTE]
>
>Las sugerencias y recomendaciones de búsqueda pueden afectar al rendimiento del servidor.

1. Para ofrecer recomendaciones, establezca **[!UICONTROL Enable Search Recommendations]** en `Yes` y haga lo siguiente:

   - Para **[!UICONTROL Search Recommendation Count]**, ingrese el número de recomendaciones que desea ofrecer.

   - Para mostrar el número de resultados encontrados para cada recomendación, establezca **[!UICONTROL Show Results Count for Each Recommendation]** en `Yes`.

1. Establezca **[!UICONTROL Enable Search Suggestions]** en `Yes` y haga lo siguiente:

   - Para **[!UICONTROL Search Suggestions Count]**, ingrese el número de sugerencias de búsqueda que desea ofrecer.

   - Para mostrar el número de resultados encontrados para cada sugerencia, establezca **[!UICONTROL Show Results for Each Suggestion]** en `Yes`.

### Paso 4: Configurar los términos mínimos de coincidencia

Para controlar el número mínimo de términos de la consulta que los resultados de la búsqueda deben coincidir para la devolución, especifique un valor para **[!UICONTROL Minimum Terms to Match]**. Especificar este valor garantiza una relevancia óptima de los resultados para los compradores. Para obtener una lista de los valores aceptados, consulte [minimum_should_match_parameter](https://opensearch.org/docs/latest/query-dsl/minimum-should-match/) en la documentación de OpenSearch.

Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
