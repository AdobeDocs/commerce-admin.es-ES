---
title: Páginas
description: Obtenga más información acerca de las páginas de contenido principales incluidas en la tienda de demostración de  [!DNL Commerce] y sobre cómo cambiar la configuración de las páginas predeterminadas.
exl-id: 4be7d3d6-ce36-42bc-9224-4804c3211f16
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '915'
ht-degree: 0%

---

# Páginas

El contenido se puede ver en términos de su vida útil, al igual que cualquier producto de una tienda. ¿Sabía que la vida útil del contenido de las redes sociales es inferior a 24 horas? La vida útil potencial del contenido que crea puede ayudarle a decidir dónde invertir sus recursos.

El contenido con una larga vida útil a veces se denomina _contenido permanente_. Algunos ejemplos de contenido permanente son los casos de éxito de los clientes, _cómo_ instrucciones y Preguntas más frecuentes (FAQ). Por el contrario, el contenido que es perecedero por naturaleza incluye eventos, noticias de la industria y comunicados de prensa.

![La página Acerca de nosotros incluida con el almacén de Luma de muestra ](./assets/storefront-about-us.png){width="700" zoomable="yes"}

## Páginas de contenido principal

El almacén de demostración de [!DNL Commerce] tiene ejemplos de páginas de contenido principal para ayudarle a empezar. Todas estas páginas se pueden modificar para adaptarlas a sus necesidades. Observe las siguientes páginas de su tienda y asegúrese de que el contenido transmite su mensaje, voz y marca.

### Inicio

La página de demostración [Home](../getting-started/storefront.md#home-page) incluye un banner, un carrusel de imágenes, varios bloques estáticos con vínculos y una lista de productos nuevos.

### Política de privacidad

La página de la tienda [Política de privacidad](../getting-started/privacy-policy.md) debe actualizarse con su propia información. Como práctica recomendada, la política de privacidad debe explicar a sus clientes el tipo de información que recopila su compañía y cómo se utiliza.

### 404 No encontrado

La página 404 Página no encontrada recibe un nombre por el código de respuesta que se devuelve cuando no se puede encontrar una página. Las redirecciones de URL reducen el número de veces que aparece esta página. Sin embargo, en aquellos momentos en que sea necesario, también puede aprovechar la oportunidad para ofrecer algunos vínculos a productos que el cliente pueda encontrar interesantes.

### Acceso denegado

{{b2b-feature}}

La página [Acceso denegado](../b2b/account-company-roles-permissions.md) aparece cuando los permisos asignados a un usuario de la compañía impiden el acceso a la página.

### Habilitar cookies

La página [Habilitar cookies](../getting-started/compliance-cookie-law.md) aparece cuando los visitantes del sitio no tienen las cookies habilitadas en los exploradores. La página proporciona instrucciones paso a paso e ilustradas para habilitar las cookies en los exploradores más populares.

### Servicio no disponible

La página [Servicio 503 no disponible](../configuration-reference/general/general.md) recibe un nombre por el código de respuesta que se devuelve cuando el servidor no está disponible.

### Acerca de nosotros

La página Acerca de nosotros está vinculada desde el pie de página de la tienda. Puede incluir imágenes, vídeos, vínculos a comunicados de prensa y anuncios. La página de muestra tiene una imagen a la derecha y una decorativa para indicar el final de la página.

### Servicio al cliente

La página Servicio de atención al cliente es otro nodo de la jerarquía de páginas. Los dos encabezados de la página tienen contenido que solo se vuelve visible cuando el cliente hace clic en el encabezado.

![Página de servicio al cliente en la tienda](./assets/storefront-customer-service.png){width="700" zoomable="yes"}

## Configurar páginas predeterminadas

La configuración de _Páginas predeterminadas_ determina la página de aterrizaje asociada con la [URL base](../stores-purchase/store-urls.md) y la página de inicio correspondiente. También determina qué página aparece cuando se produce un error de _Página no encontrada_ y si aparece un [seguimiento de ruta de exploración](../catalog/navigation-breadcrumb-trail.md) en la parte superior de cada página.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo bajo _[!UICONTROL General]_, elija **[!UICONTROL Web]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Default Pages]**.

   ![Páginas predeterminadas](./assets/web-default-pages.png){width="500" zoomable="yes"}

   | Campo | [Ámbito](../getting-started/websites-stores-views.md#scope-settings) | Descripción |
   |--- |--- |--- |
   | [!UICONTROL Default Web URL] | Vista de tienda | Indica la página de aterrizaje asociada a la dirección URL base. De manera predeterminada, este campo se establece en `cms` para indicar una página del sistema de administración de contenido [!DNL Commerce]. También puede utilizar un tipo diferente de página de aterrizaje, como un blog. Por ejemplo, si un blog está instalado en el servidor en `magento/blog`, puede escribir el nombre de carpeta `blog` como una ruta relativa a la selección de páginas. |
   | [!UICONTROL CMS Home Page] | Vista de tienda | Para elegir la página de inicio de la tienda, simplemente seleccione la página de CMS en la lista. De forma predeterminada, la página principal de CMS muestra toda la selección de páginas de CMS disponibles para su tienda. |
   | [!UICONTROL Default No-route URL] | Vista de tienda | Contiene la dirección URL de la página predeterminada que desea que aparezca cuando se produzca un error `404 Page not Found`. El valor predeterminado es `cms/noroute/index`. |
   | [!UICONTROL CMS No Route Page] | Vista de tienda | Identifica una página CMS específica que desea que aparezca cuando se produzca un error 404 Página no encontrada. La página predeterminada es `404 Not Found`. |
   | [!UICONTROL CMS No Cookies Page] | Vista de tienda | Identifica una página de CMS específica que aparece cuando las cookies no están habilitadas para el explorador. La página explica por qué se utilizan las cookies y cómo habilitarlas para cada explorador. La página predeterminada es `Enable Cookies`. |
   | [!UICONTROL Show Breadcrumbs for CMS Pages] | Vista de tienda | Determina si aparece una ruta de exploración en todas las páginas de CMS del catálogo. Opciones: `Yes` / `No` |

   {style="table-layout:auto"}

1. Para **[!UICONTROL Default Web URL]**, escriba la ruta relativa a la carpeta en la instalación de [!DNL Commerce] que contiene la página de aterrizaje.

   La configuración predeterminada `cms` indica una página del sistema de administración de contenido [!DNL Commerce].

   >[!NOTE]
   >
   >Para una vista de almacén específica, desactive la casilla de verificación **[!UICONTROL Use Default]** junto a _[!UICONTROL Default Web URL]_y cualquier otra configuración predeterminada que desee cambiar.

1. Configure **[!UICONTROL CMS Home Page]** a la página de CMS para usarla como página de inicio. Otras páginas creadas pueden utilizarse como página de inicio, como:

   - Bienvenido a la tienda en línea exclusiva
   - Puntos de recompensas
   - Acerca de nosotros
   - Servicio al cliente
   - Habilitar cookies
   - Política de privacidad
   - Empresa: acceso denegado

1. Para **[!UICONTROL Default No-route URL]**, escriba la ruta relativa a la carpeta de la instalación de [!DNL Commerce] a la que se redirige la página cuando se produce un error de _404 Página no encontrada_.

   El valor predeterminado es `cms/index/noRoute`.

1. Establezca **[!UICONTROL CMS No Route Page]** en la página de CMS que aparece cuando se produce un error de _404 Página no encontrada_.

1. Configure **[!UICONTROL CMS No Cookies Page]** a la página de CMS que aparece cuando las cookies están deshabilitadas en el explorador. La página explica por qué se utilizan las cookies y cómo habilitarlas para cada explorador. La página predeterminada es `Enable Cookies`.

1. Si desea que aparezca una ruta de exploración en la parte superior de todas las páginas de CMS, establezca **[!UICONTROL Show Breadcrumbs for CMS Pages]** en `Yes`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
