---
title: Mapas del sitio
description: Aprenda a configurar un mapa del sitio para indexar todas las páginas e imágenes de sus sitios de Commerce.
exl-id: 48c975ae-b088-4e52-80cf-cb19c2b9b00f
feature: Merchandising, Storefront, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1207'
ht-degree: 0%

---

# Mapas del sitio

Un mapa del sitio mejora la forma en que los motores de búsqueda indizan el almacén y está diseñado para buscar páginas que los rastreadores web podrían pasar por alto. Se puede configurar un mapa del sitio para indexar todas las páginas e imágenes.

Cuando está habilitado, Commerce crea un archivo llamado `sitemap.xml` que se guarda en la instalación en la ubicación especificada. La configuración le permite establecer la frecuencia de las actualizaciones y la prioridad para cada tipo de contenido. El mapa del sitio debe actualizarse con la frecuencia con la que cambia el contenido del sitio, que puede ser diaria, semanal o mensual.

Mientras el sitio está en desarrollo, puede incluir instrucciones en la `robots.txt` para que los rastreadores web eviten indexar el sitio. A continuación, antes del lanzamiento, puede cambiar las instrucciones para permitir que el sitio se indexe.

Para obtener información técnica, consulte [Agregar mapa del sitio y robots.txt][1] en el _Guía de Commerce en la infraestructura de Cloud_.

![Cuadrícula de mapa](./assets/marketing-sitemap-grid-generated.png){width="700" zoomable="yes"}

## Paso 1. Configuración del mapa del sitio

Complete la [Configuración de mapa del sitio XML](#site-map-configuration) para determinar qué se incluye y con qué frecuencia se actualiza el mapa del sitio.

## Paso 2. Generación del mapa del sitio

1. En el _Administrador_ , vaya a **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**.

1. Haga clic **[!UICONTROL Add Site Map]**.

   ![Cuadrícula del mapa del sitio](./assets/marketing-sitemap.png){width="700" zoomable="yes"}

1. Introducir el mapa del sitio **[!UICONTROL Filename]**. Por ejemplo: `sitemap.xml`

1. Introduzca el **[!UICONTROL Path]** para determinar dónde residirá el archivo del mapa del sitio en el servidor. Asegúrese de que la ruta de acceso sea de escritura.

   - `/sitemap/` : coloca el archivo del mapa del sitio en un directorio llamado _mapa del sitio_.

   - `/` : coloca el archivo del mapa del sitio en la ruta base o raíz de la instalación de Commerce.

   ![Nuevo mapa del sitio](./assets/marketing-sitemap-new.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save & Generate]**.

   El mapa del sitio puede tardar unos minutos en aparecer en la cuadrícula.

## Paso 3. Configure y habilite robots.txt (opcional)

Complete la [robots de motor de búsqueda](seo-overview.md#search-engine-robots) con instrucciones que dirigen a los motores de búsqueda a rastrear las partes del sitio que desea indexar.

## Paso 4. Envíe el mapa del sitio a los motores de búsqueda

Puede enviar el mapa del sitio a distintos motores de búsqueda proporcionándoles el vínculo al `sitemap.xml` en su instalación de Commerce. Para copiar el vínculo, haga lo siguiente:

1. En el _Mapa del sitio_ , haga clic con el botón derecho en la dirección URL de la lista **[!UICONTROL Link for Google]** columna.

1. En el menú, elija **[!UICONTROL Copy Link Address]**.

Para obtener más información, consulte las instrucciones del motor de búsqueda específico. Aquí tiene vínculos a instrucciones para dos motores de búsqueda principales:

- [Google][2]
- [Microsoft® Bing][3]

## Paso 5: Restauración de las instrucciones anteriores del robot (opcional)

Ahora puede restaurar las restricciones originales (predeterminadas).

## Administración de mapas del sitio y robots.txt para varios sitios web

Si tiene varios sitios web, puede simplificar el proceso de creación y envío de mapas del sitio. Simplemente [crear](#site-map-configuration) uno o más mapas del sitio que incluyen direcciones URL de todas las tiendas comprobadas y guardan los mapas del sitio en una sola ubicación. Todos los sitios deben verificarse en [Consola de búsqueda de Google](https://support.google.com/webmasters/answer/7451001).

Para crear mapas del sitio para una instancia de varias tiendas, haga lo siguiente:

1. Cree una carpeta llamada `sitemaps` en la raíz del sitio web, cree subcarpetas para cada dominio:

       /sitemaps/domain_1/
       /sitemaps/domain_2/
   
1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**.

1. Cree o edite los listados de mapa del sitio para cada tienda y establezca el **[!UICONTROL Path]** al que creó para la tienda:

   `/sitemaps/domain_1/`
   `/sitemaps/domain_2/`

1. Si es necesario, actualice el archivo robots.txt.

   Para asegurarse de que las arañas del motor de búsqueda se dirigen correctamente a los nuevos mapas del sitio, puede actualizar o crear el archivo robots.txt. Añada las siguientes líneas en la parte superior.

       Mapa del sitio web
       Mapa del sitio: https://www.domain_1.com/sitemaps/domain_1/sitemap.xml
       Mapa del sitio: https://www.domain_2.com/sitemaps/domain_2/sitemap.xml
   
>[!NOTE]
>
>Si su sitio utiliza el [Apache](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/web-server/apache.html) motor del servidor web, debe actualizar el [`.htaccess`](https://httpd.apache.org/docs/current/howto/htaccess.html) en la raíz del sitio web para dirigir cualquier otra solicitud de mapa del sitio al lugar adecuado.

## Descripciones de columna

| Columna | Descripción |
|------|-----------|
| [!UICONTROL ID] | Número de registro secuencial del mapa del sitio actual. |
| [!UICONTROL Filename] | Nombre de archivo del mapa del sitio. |
| [!UICONTROL Path] | Ubicación en la que reside el mapa del sitio en el servidor. Por ejemplo: <br/>`/sitemap/` : coloca el archivo del mapa del sitio en un directorio llamado _mapa del sitio_, un nivel por debajo de la raíz de la instalación de Commerce. <br/>`/` : coloca el archivo del mapa del sitio en la ruta base o raíz de la instalación de Commerce. |
| [!UICONTROL Link for Google] | Dirección URL del mapa del sitio que se va a enviar a Google y otros motores de búsqueda. |
| [!UICONTROL Last Generated] | Indica la fecha y la hora de la última generación del mapa del sitio. |
| [!UICONTROL Store View] | La vista de tienda donde se aplica el mapa del sitio. |
| [!UICONTROL Generate] | Vuelve a generar el mapa del sitio. |

{style="table-layout:auto"}

## Configuración del mapa del sitio

El mapa del sitio debe actualizarse con la frecuencia con la que cambia el contenido del sitio, que puede ser diaria, semanal o mensual. La configuración permite establecer la frecuencia y la prioridad para cada tipo de contenido.

### Paso 1. Establecer la frecuencia y la prioridad de las actualizaciones de contenido

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL XML Sitemap]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Categories Options]** y haga lo siguiente:

   >[!NOTE]
   >
   >Si es necesario, borre la **[!UICONTROL Use system value]** para cambiar esta configuración.

   - Establecer **[!UICONTROL Frequency]** a uno de los siguientes:

      - `Always`
      - `Hourly`
      - `Daily`
      - `Weekly`
      - `Monthly`
      - `Yearly`
      - `Never`

   - Para **[!UICONTROL Priority]**, introduzca un valor entre `0.0` y `1.0`. Cero tiene la prioridad más baja.

   ![Mapa del sitio XML: opciones de categorías](../configuration-reference/catalog/assets/xml-sitemap-categories-options.png){width="600" zoomable="yes"}

   Para ver una lista detallada de estas opciones, consulte [Opciones de categorías](../configuration-reference/catalog/xml-sitemap.md#categories-options) en el _Referencia de configuración_.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Products Options]** y complete la sección **[!UICONTROL Frequency]** y **[!UICONTROL Priority]** ajustes según sea necesario.

   Para ver una lista detallada de estas opciones, consulte [Opciones de productos](../configuration-reference/catalog/xml-sitemap.md#products-options) en el _Referencia de configuración_.

1. Para determinar la extensión de las imágenes en el mapa del sitio, establezca **[!UICONTROL Add Images into Sitemap]** a uno de los siguientes:

   - `None`
   - `Base Only`
   - `All`

   ![Configuración del catálogo: productos XML de mapa del sitio](../configuration-reference/catalog/assets/xml-sitemap-products-options.png){width="600" zoomable="yes"}

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL CMS Pages Options]** y complete la sección **[!UICONTROL Frequency]** y **[!UICONTROL Priority]** ajustes según sea necesario.

   ![Configuración del catálogo: páginas CMS de mapa del sitio XML](../configuration-reference/catalog/assets/xml-sitemap-cms-pages-options.png){width="600" zoomable="yes"}

   Para ver una lista detallada de estas opciones, consulte [Opciones de páginas de CMS](../configuration-reference/catalog/xml-sitemap.md#cms-pages-options) en el _Referencia de configuración_.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Store Url Options]** y complete la sección **[!UICONTROL Frequency]** y **[!UICONTROL Priority]** ajustes según sea necesario.

   ![Configuración del catálogo: URL del almacén de mapas del sitio XML](./assets/xml-sitemap.png){width="600" zoomable="yes"}

   Para ver una lista detallada de estas opciones, consulte [Opciones De Url De Tienda](../configuration-reference/catalog/xml-sitemap.md#store-url-options) en el _Referencia de configuración_.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

### Paso 2. Completar la configuración de generación

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Generation Settings]** sección.

   Si es necesario, borre la **Usar valor del sistema** para cambiar esta configuración.

   ![Configuración del catálogo: configuración de generación de mapas del sitio XML](../configuration-reference/catalog/assets/xml-sitemap-generation-settings.png){width="600" zoomable="yes"}

   Para ver una lista detallada de estas opciones, consulte [Configuración de generación](../configuration-reference/catalog/xml-sitemap.md#generation-settings) en el _Referencia de configuración_.

1. Para generar un mapa del sitio, establezca **[!UICONTROL Enabled]** hasta `Yes` y haga lo siguiente:

   - Establecer **[!UICONTROL Start Time]** a la hora, los minutos y el segundo en que desea que se actualice el mapa del sitio.

   - Establecer **[!UICONTROL Frequency]** a uno de los siguientes:

      - `Daily`
      - `Weekly`
      - `Monthly`

   - Para **[!UICONTROL Error Email Recipient]**, introduzca la dirección de correo electrónico de la persona que va a recibir la notificación si se produce un error durante una actualización del mapa del sitio.

   - Establecer **[!UICONTROL Error Email Sender]** al contacto de la tienda que aparece como remitente de la notificación de error.

   - Establecer **[!UICONTROL Error Email Template]** a la plantilla utilizada para la notificación de error.

### Paso 3. Establecer los límites de archivos del mapa del sitio

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Sitemap File Limits]** sección.

   ![Configuración del catálogo: límites de archivos de mapa del sitio XML](../configuration-reference/catalog/assets/xml-sitemap-sitemap-file-limits.png){width="600" zoomable="yes"}

   Para ver una lista detallada de estas opciones, consulte [Límites de archivos de mapa](../configuration-reference/catalog/xml-sitemap.md#sitemap-file-limits) en el _Referencia de configuración_.

1. Para **[!UICONTROL Maximum No of URLs per File]**, introduzca el número máximo de direcciones URL que se pueden incluir en el mapa del sitio.

   De forma predeterminada, el límite es 50 000.

1. Para **[!UICONTROL Maximum File Size]**, introduzca el tamaño máximo en bytes asignado para el mapa del sitio.

   El tamaño predeterminado es 10.485.760 bytes.

### Paso 4. Establecer la configuración de envío del motor de búsqueda

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Search Engine Submission Settings]** sección.

   ![Configuración del catálogo: configuración de envío del motor de búsqueda de mapa del sitio XML](../configuration-reference/catalog/assets/xml-sitemap-search-engine-submission-settings.png){width="600" zoomable="yes"}

1. Si se usa un `robots.txt` para proporcionar instrucciones a los motores de búsqueda que rastrean el sitio, establezca **[!UICONTROL Enable Submission to Robots.txt]** hasta `Yes`.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/robots-sitemap.html
[2]: https://support.google.com/webmasters/answer/183669?hl=en
[3]: https://www.bing.com/webmasters/help/Sitemaps-3b5cf6ed
