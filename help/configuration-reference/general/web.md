---
title: '[!UICONTROL General] &gt; [!UICONTROL Web]'
description: Revise la configuración de en [!UICONTROL General] &gt; [!UICONTROL Web] de la administración de Commerce.
exl-id: 1809b03a-a55c-41b4-947b-f66f4bd290a1
feature: Site Management, Configuration
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1795'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Web]

{{config}}

## [!UICONTROL URL Options]

![Web > Opciones generales](./assets/web-url-options.png)<!-- zoom -->

<!-- [URL Options configuration settings](https://docs.magento.com/user-guide/stores/store-urls.html) -->

| Campo | Ámbito | Descripción |
|  ---  |  ---  |  ---  |
| [!UICONTROL Add Store Code to URLs] | Global | Si las reescrituras de servidor web están habilitadas, inserta el código de almacén de la vista actual en la dirección URL. Opciones: `Yes` / `No`. <br />Cuando este campo se establece en `Yes`Además, debe incluir códigos de tienda en las direcciones URL del explorador para asegurarse de que las reescrituras de URL se asignen correctamente y de que todas las páginas se abran correctamente. Esto evita _404 Página no encontrada_ errores. |
| [!UICONTROL Auto-redirect to Base URL] | Vista de tienda | (En configuraciones de tienda única) Si hay un vínculo roto en el sitio, redirige el tráfico a la dirección URL base, en lugar de a una página con el mensaje &quot;404 Page Not Found&quot;. Opciones:` No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br />**_Importante:_**No utilice el redireccionamiento automático para URL base en configuraciones de varias tiendas. |
| [!UICONTROL Catalog media URL format] | Global | Define el [Formato de URL](../../catalog/catalog-urls.md) asignado a productos y categorías. Opciones: hash único por variante de imagen (modo heredado) define el nombre de archivo convertido como un valor hash único. La optimización de imágenes basada en parámetros de consulta define [optimización de imágenes](../../content-design/media-gallery-image-optimization.md) procesar según los parámetros de consulta. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Optimization]

![Web > Optimización del motor de búsqueda](./assets/web-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization configuration settings](https://docs.magento.com/user-guide/marketing/url-rewrite.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Use Web Server Rewrites] | Vista de tienda | Los sistemas basados en PHP suelen incluir un archivo llamado `index.php` en la carpeta raíz. De forma predeterminada, el nombre del archivo aparece en la dirección URL justo después del nombre de la carpeta raíz. Cuando está activada, el sistema omite `index.php` desde la dirección URL. Esta práctica recomendada de uso hace que cada dirección URL sea más concisa y no afecta al rendimiento ni a la clasificación del sitio. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Base URLs]

![Web > URL base](./assets/web-base-urls.png)<!-- zoom -->

<!-- [Base URLS configuration settings](https://docs.magento.com/user-guide/stores/store-urls.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Base URL] | Vista de tienda | Dirección completa de la carpeta raíz de Commerce que no se ejecuta en un canal cifrado (SSL). La dirección URL debe finalizar con una barra diagonal. |
| [!UICONTROL Base Link URL] | Vista de tienda | Etiqueta de marcado que se utiliza como marcador de posición para la dirección URL base. |
| [!UICONTROL Base URL for Static View Files] | Vista de tienda | Una ruta que señala a la ubicación de los archivos estáticos utilizados por la temática, como css, fuentes, imágenes y JavaScript. Se utiliza un marcador de posición para representar la dirección URL base. Si la instalación de Commerce tiene varios sitios con la misma estructura de carpetas, puede tener una carpeta diferente para cada sitio. Establezca el ámbito de configuración en el sitio correcto antes de escribir la dirección URL base para los archivos de vista estática. También puede especificar una carpeta fuera de la instalación de Commerce. |
| [!UICONTROL Base URL for User Media Files] | Vista de tienda | Una ruta que señala a la ubicación de las imágenes del catálogo y otros archivos multimedia. Se utiliza un marcador de posición para representar la dirección URL base. Si la instalación de Commerce tiene varios sitios con la misma estructura de carpetas, puede tener una carpeta de medios diferente para cada uno. Esto le permite realizar copias de seguridad y revertir cada carpeta multimedia por separado. También puede especificar una carpeta de medios fuera de la instalación de Commerce. |

{style="table-layout:auto"}

## [!UICONTROL Base URLs (Secure)]

![Web > Direcciones URL base (seguras)](./assets/web-base-urls-secure.png)<!-- zoom -->

<!-- [Base URLs (Secure) configuration settings](https://docs.magento.com/user-guide/stores/store-urls.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Secure Base URL] | Vista de tienda | La dirección completa de la carpeta raíz de Commerce que se entrega con el protocolo cifrado seguro (SSL/TLS). La dirección URL debe finalizar con una barra diagonal. |
| [!UICONTROL Secure Base Link URL] | Vista de tienda | Una etiqueta de marcado que se utiliza como marcador de posición para la dirección URL base que se ejecuta en un canal seguro. |
| [!UICONTROL Secure Base URL for Static View Files] | Vista de tienda | Una etiqueta de marcado que señala a la ubicación de archivos estáticos como CSS, fuentes, imágenes y JavaScript que utiliza la temática. Los archivos pueden estar en un canal no seguro o seguro. Si la instalación de Commerce tiene varios sitios con la misma estructura de carpetas, puede tener una carpeta diferente para cada sitio. Establezca el ámbito de configuración en el sitio correcto antes de escribir la dirección URL base para los archivos de vista estática. También puede especificar una carpeta fuera de la instalación de Commerce. |
| [!UICONTROL Secure Base URL for User Media Files] | Vista de tienda | Una ruta que señala a la ubicación de las imágenes del catálogo y otros archivos multimedia. Los archivos pueden estar en un canal no seguro o seguro. Se utiliza un marcador de posición para representar la dirección URL base. Si la instalación de Commerce tiene varios sitios con la misma estructura de carpetas, puede tener una carpeta de medios diferente para cada uno. Esto le permite realizar copias de seguridad y revertir cada carpeta multimedia por separado. También puede especificar una carpeta de medios fuera de la instalación de Commerce. |
| [!UICONTROL Use Secure URLs on Storefront] | Vista de tienda | Si el dominio tiene un certificado de seguridad, puede elegir ejecutar la tienda, con o sin cifrado SSL. Opciones:<br />**`Yes`**: las direcciones URL de tienda comienzan por `https` para indicar que la página se entrega con un protocolo cifrado y seguro.<br />**`No`** : las direcciones URL de tienda comienzan por `http` para indicar que la página se entrega sin protocolo seguro. |
| [!UICONTROL Use Secure URLs in Admin] | Global | Si su dominio tiene un certificado de seguridad, puede elegir ejecutar el administrador del almacén, con o sin cifrado SSL. Opciones: <br />**`Yes`**: Las direcciones URL de administrador comienzan con `https` para indicar que la página se entrega con un protocolo cifrado y seguro.<br />**`No`** : Las direcciones URL de administrador comienzan con `http` para indicar que la página se entrega sin protocolo seguro.<br /> Cuando las direcciones URL seguras están habilitadas tanto para el almacén como para el administrador, aparecen dos campos adicionales para habilitar y configurar `HSTS`. |
| [!UICONTROL Enable HTTP Strict Transport Security (HSTS)] | Vista de tienda | Cuando está activada, [`HSTS`][1] proporciona una medida de seguridad contra los ataques de &quot;hombre en medio&quot; e impide que los usuarios anulen el mensaje &quot;certificado no válido&quot;. Opciones: `Yes` / `No` |
| [!UICONTROL Upgrade Insecure Requests] | Vista de tienda | Cuando está habilitada, convierte a no seguro (`HTTP`) solicitudes recibidas desde el explorador al seguro (`HTTPS`) protocolo. Opciones: `Yes` / `No` |
| [!UICONTROL Offloader Header] | Global | Especifica el `offloader_header` en la configuración del servidor para identificar el protocolo entre el cliente y el equilibrador de carga. La mayoría de las instalaciones de Commerce utilizan el valor predeterminado, `X-Forwarded-Proto` (XFP) para identificar el protocolo como `HTTP` o `HTTPS`. |

{style="table-layout:auto"}

## [!UICONTROL Default Pages]

![Web > Páginas predeterminadas](./assets/web-default-pages.png)<!-- zoom -->

<!-- [Default Pages configuration settings](https://docs.magento.com/user-guide/cms/pages-default.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Default Web URL] | Vista de tienda | Indica la página de aterrizaje asociada a la dirección URL base. Esto se establece de forma predeterminada en &quot;cms&quot; para indicar una página del sistema de administración de contenido de Commerce (CMS). También puede utilizar un tipo diferente de página de aterrizaje, como un blog. Por ejemplo, si un blog está instalado en el servidor en `magento/blog`, puede introducir el nombre de la carpeta &quot;blog&quot; como una ruta relativa a la selección de páginas. |
| [!UICONTROL CMS Home Page] | Vista de tienda | Para elegir la página de inicio de la tienda, simplemente seleccione la página de CMS en la lista. De forma predeterminada, la página principal de CMS muestra toda la selección de páginas de CMS disponibles para su tienda. |
| [!UICONTROL Default No-route URL] | Vista de tienda | Contiene la dirección URL de la página predeterminada que desea que aparezca cuando `404 Page not Found` se produce un error. El valor predeterminado es `cms/noroute/index`. |
| [!UICONTROL CMS No Route Page] | Vista de tienda | Identifica una página CMS específica que desea que aparezca cuando se produzca un error 404 Página no encontrada. La página predeterminada es 404 Not Found. |
| [!UICONTROL CMS No Cookies Page] | Vista de tienda | Identifica una página de CMS específica que aparece cuando las cookies no están habilitadas para el explorador. La página explica por qué se utilizan las cookies y cómo habilitarlas para cada explorador. La página predeterminada es Habilitar cookies. |
| [!UICONTROL Show Breadcrumbs for CMS Pages] | Vista de tienda | Determina si aparece una ruta de exploración en todas las páginas de CMS del catálogo. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Default Layouts]

![Diseños predeterminados](./assets/web-default-layouts.png)<!-- zoom -->

<!--[Default Layouts](https://docs.magento.com/user-guide/design/page-layout.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Default Product Layout] | Global | Determina el [layout](../../content-design/page-layout.md) que se utiliza de forma predeterminada para las páginas de producto de. Opciones: <br/>**`No layout updates`**: De forma predeterminada, las actualizaciones de diseño no están disponibles para las páginas de productos.<br/>**`Empty`** : De forma predeterminada, utiliza un diseño en blanco para las páginas de productos. <br/>**`1 column`**: De forma predeterminada, utiliza un diseño de columna única para las páginas de producto.<br/>**`2 columns with left bar`** : De forma predeterminada, utiliza un diseño de dos columnas con la barra lateral a la izquierda para las páginas de productos. <br/>**`2 columns with right bar`**: De forma predeterminada, utiliza un diseño de dos columnas con la barra lateral a la derecha para las páginas de productos.<br/>**`3 columns`** : De forma predeterminada, utiliza un diseño de tres columnas con barras laterales a la izquierda y a la derecha para las páginas de productos.<br/>**`Page -- Full Width`**- (Requiere [!DNL Page Builder]) De forma predeterminada, utiliza el diseño Página — Anchura completa para las páginas de producto.<br/>**`Category - Full Width`** - (Requiere [!DNL Page Builder]) De forma predeterminada, utiliza el diseño Categoría - Anchura completa para las páginas de productos. <br/>**`Product - Full Width`**- (Requiere [!DNL Page Builder]) De forma predeterminada, utiliza el diseño Producto - Anchura completa para las páginas de producto. |
| [!UICONTROL Default Category Layout] | Global | Determina el [layout](../../content-design/page-layout.md) que se utiliza de forma predeterminada para las páginas de categoría. Opciones: <br/>**`No layout updates`**- De forma predeterminada, las actualizaciones de diseño no están disponibles para las páginas de categoría.<br/>**`Empty`** - De forma predeterminada, utiliza un diseño en blanco para las páginas de categoría. <br/>**`1 column`**- De forma predeterminada, utiliza un diseño de columna única para las páginas de categoría.<br/>**`2 columns with left bar`** - De forma predeterminada, utiliza un diseño de dos columnas con la barra lateral a la izquierda para las páginas de categoría. <br/>**`2 columns with right bar`**: De forma predeterminada, utiliza un diseño de dos columnas con la barra lateral a la derecha para las páginas de categoría.<br/>**`3 columns`** - De forma predeterminada, utiliza un diseño de tres columnas con barras laterales a la izquierda y a la derecha para las páginas de categoría.<br/>**`Page - Full Width`**- (Requiere [!DNL Page Builder]) De forma predeterminada, utiliza el diseño Página - Anchura completa para las páginas de categoría.<br/>**`Category - Full Width`** - (Requiere [!DNL Page Builder]) De forma predeterminada, utiliza el diseño Categoría - Anchura completa para las páginas de categoría. <br/>**`Product - Full Width`**- (Requiere [!DNL Page Builder]) De forma predeterminada, utiliza el diseño Producto - Anchura completa para las páginas de categoría. |
| Diseño de página predeterminado | Global | Determina el [layout](../../content-design/page-layout.md) que se utiliza de forma predeterminada para las páginas de CMS. Opciones: <br/>**`No layout updates`**: De forma predeterminada, las actualizaciones de diseño no están disponibles para páginas de CMS.<br/>**`Empty`** : De forma predeterminada, utiliza un diseño en blanco para las páginas de CMS. <br/>**`1 column`**: De forma predeterminada, utiliza un diseño de columna única para las páginas de CMS.<br/>**`2 columns with left bar`** : De forma predeterminada, utiliza un diseño de dos columnas con la barra lateral a la izquierda para páginas CMS.<br/>**`2 columns with right bar`**: De forma predeterminada, utiliza un diseño de dos columnas con la barra lateral a la derecha para páginas de CMS.<br/>**`3 columns`** : De forma predeterminada, utiliza un diseño de tres columnas con barras laterales a la izquierda y a la derecha para páginas de CMS.<br/>**`Page - Full Width`**- (Requiere [!UICONTROL Page Builder]) De forma predeterminada, utiliza el diseño Página - Anchura completa para páginas CMS.<br/>**`Category - Full Width`** - (Requiere [!UICONTROL Page Builder]) De forma predeterminada, utiliza el diseño Categoría: Anchura completa para las páginas de CMS. <br/>**`Product - Full Width`**- (Requiere [!DNL Page Builder]) De forma predeterminada, utiliza el diseño Producto - Anchura completa para páginas CMS. |

{style="table-layout:auto"}

## [!UICONTROL Default Cookie Settings]

![Web > Configuración de cookies predeterminada](./assets/web-default-cookie-settings.png)<!-- zoom -->

<!-- [Default Cookie configuration settings](https://docs.magento.com/user-guide/stores/compliance-cookie-law.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Cookie Lifetime] | Vista de tienda | Determina cuánto tiempo puede existir una cookie antes de que se elimine automáticamente. El valor predeterminado es 3600 segundos (1 hora) |
| [!UICONTROL Cookie Path] | Vista de tienda | Especifica las carpetas del servidor donde se pueden utilizar las cookies comerciales. Para que las cookies de Commerce estén disponibles en cualquier lugar de la instalación, establezca la Ruta de la cookie en una sola barra diagonal: `/`. Este valor solo puede contener la ruta de la cookie, y **_no puede_** contener cualquier otro parámetro de cookie. |
| [!UICONTROL Cookie Domain] | Vista de tienda | Determina si las cookies de Commerce están disponibles para los subdominios. Por ejemplo, para admitir `mysubdomain`.domain.com, introduzca el nombre de su dominio con un punto al principio, como `.domain.com`. Este valor solo puede contener el dominio de la cookie, y **_no puede_** contener cualquier otro parámetro de cookie. |
| [!UICONTROL Use HTTP Only] | Vista de tienda | Determina si las cookies comerciales solo se pueden utilizar en un canal no seguro (http) o en un canal cifrado (https). Opciones: `Yes` / `No` |
| [!UICONTROL Cookie Restriction Mode] | Sitio web | Determina si el modo de restricción de cookies está habilitado. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Session Validation Settings]

![Web > Validación de sesión](./assets/web-session-validation-settings.png)<!-- zoom -->

<!-- [Session Validation configuration settings](https://docs.magento.com/user-guide/stores/security-session-validation.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Validate REMOTE_ADDR] | Global | Comprueba que la dirección IP de una solicitud coincida `$_SESSION` datos. La sesión finaliza si se detecta una dirección IP diferente. Opciones: `Yes` / `No` |
| [!UICONTROL Validate HTTP_VIA] | Global | Comprueba los datos proxy entrantes y comprueba que la dirección proxy de una solicitud coincide `$_SESSION` datos. La sesión finaliza si se detecta una dirección proxy diferente. Opciones: `Yes` / `No` |
| [!UICONTROL Validate HTTP_x_FORWARDED_FOR] | Global | Comprueba los datos del proxy saliente y comprueba que la dirección de reenvío de una solicitud coincide  `$_SESSION` datos. La sesión finaliza si se detecta una dirección de reenvío diferente. Opciones: `Yes` / `No` |
| [!UICONTROL Validate HTTP_USER_AGENT] | Global | `USER_AGENT` hace referencia al explorador o dispositivo que se utiliza para acceder al sitio web. Comprueba que el nombre y la versión del explorador, y del sistema operativo, coinciden `$_SESSION` datos. La sesión finaliza si se detecta un agente de usuario diferente de una solicitud a otra en la misma sesión. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Browser Capabilities Detection]

![Web > Detección de capacidades del explorador](./assets/web-browser-capabilities-detection.png)<!-- zoom -->

<!-- [Browser Capabilities Detection configuration settings](https://docs.magento.com/user-guide/stores/security-browser-capabilities-detection.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Redirect to CMS-page if Cookies are Disabled] | Vista de tienda | Si el explorador desactiva las cookies, se redirige automáticamente a la página Sin cookies de CMS. Opciones: `Yes` / `No` |
| [!UICONTROL Show Notice if JavaScript is Disabled] | Vista de tienda | Si el explorador desactiva JavaScript, se muestra un aviso que solicita al usuario que habilite Opciones de JavaScript: `Yes` / `No` (deshabilita) |
| [!UICONTROL Show Notice if Local Storage is Disabled] | Vista de tienda | Muestra un mensaje si la caché local está deshabilitada. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

[1]: https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html
