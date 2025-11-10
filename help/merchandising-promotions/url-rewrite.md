---
title: Reescrituras de URL
description: Obtenga información acerca de las reescrituras de URL y el uso de la herramienta de reescritura de URL de Commerce para cambiar las URL asociadas a una página de producto, categoría o CMS.
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 2f2db4926ff92adfa27692eeca872c1765fd31d6
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# Reescrituras de URL

>[!TIP]
>
>Para Adobe Commerce as a Cloud Service, consulte las [directrices SEO](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/?lang=es) en la documentación de Commerce Storefront

La herramienta de reescritura de URL permite cambiar cualquier URL asociada a un producto, categoría o página de CMS. Al crear una reescritura de URL, Commerce crea automáticamente una redirección permanente (301) para que cualquier vínculo que apunte a la dirección URL antigua se redirija a la nueva.

>[!NOTE]
>
>Para actualizar las reescrituras de URL de varios o todos los productos simultáneamente, consulte [Reescrituras de URL múltiples](url-rewrite-product.md#multiple-url-rewrites).

>[!BEGINSHADEBOX &quot;Explicación de reescrituras y redirecciones&quot;]

Los términos _rewrite_ y _redirect_ se utilizan a menudo de forma intercambiable, pero son operaciones diferentes:

* **Reescritura de URL**: un proceso del lado del servidor que asigna internamente una dirección URL a otra sin cambiar lo que aparece en la barra de direcciones del explorador. Cuando un visitante solicita una dirección URL, el servidor la procesa como una dirección URL diferente en segundo plano, pero el explorador sigue mostrando la dirección URL original.

* **Redireccionamiento de URL**: envía una respuesta HTTP al explorador indicándole que se desplace a una dirección URL diferente. La barra de direcciones del explorador se actualiza para mostrar la nueva dirección URL. Las redirecciones pueden ser temporales (302) o permanentes (301).

>[!ENDSHADEBOX]

## Cómo funciona la herramienta Reescrituras

En Adobe Commerce, la herramienta de reescritura de URL crea redirecciones permanentes (301) de forma predeterminada para conservar el valor SEO al cambiar la clave URL de un producto, categoría o página. Este comportamiento garantiza que los vínculos existentes sigan funcionando y que se mantengan las clasificaciones de los motores de búsqueda.

De manera predeterminada, las [redirecciones automáticas de URL](url-redirect-product-automatic.md) están habilitadas para su tienda y la casilla de verificación **Crear redireccionamiento permanente para la URL antigua** está seleccionada en el campo Clave de URL de cada producto.

{{url-rewrite-skip}}

![Optimización del motor de búsqueda: crear redirección de URL permanente](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

{{url-rewrite-params}}

## La URL reescribe la demostración

Vea el siguiente vídeo para obtener más información sobre la administración de reescrituras de URL:

>[!VIDEO](https://video.tv.adobe.com/v/343751?quality=12&learn=on)

## Crear reescrituras de URL

Utilice la herramienta de reescritura de URL para crear redirecciones de productos y categorías, así como redirecciones personalizadas para cualquier página de la tienda. Cuando se aplica la configuración de reescritura de URL, los vínculos existentes que apuntan a la URL anterior se redirigen sin problemas a la nueva dirección.

Puede crear reescrituras de URL en:

* Añada palabras clave de alto valor para mejorar la forma en que los motores de búsqueda indexan el producto.

* Añada direcciones URL adicionales para un cambio temporal o estacional o permanente.

* Añada una ruta válida para una página, incluidas las páginas de contenido de CMS. Por ejemplo, puede crear una URL para crear una URL más fácil de usar o usar en un sistema que siempre haga referencia a productos y categorías por su ID interno.

Las reescrituras de URL que cree pueden redireccionarse a categorías existentes o a páginas personalizadas sin cambiar la estructura del sitio, lo que facilita la creación de direcciones URL memorables para las campañas de marketing.

![La URL reescribe la cuadrícula](./assets/url-rewrites.png){width="700" zoomable="yes"}

Commerce ofrece estos tipos de reescritura de URL:

* [Reescrituras de productos](url-rewrite-product.md)
* [Reescrituras de categoría](url-rewrite-category.md)
* [Reescrituras de páginas de CMS](url-rewrite-cms-page.md)
* [Reescrituras personalizadas](url-rewrite-custom.md)

### Casos de uso y ejemplos

Las reescrituras de URL se utilizan comúnmente en estos casos:

#### Cambiar una URL interna del sistema por una URL compatible con SEO

Commerce utiliza direcciones URL basadas en ID internamente, pero puede crear direcciones URL compatibles con SEO para los clientes:

**URL del sistema (interna):**

    http://www.example.com/catalog/category/id/6

**URL orientada al cliente:**

    http://www.example.com/peripherals/keyboard.html

#### Cambio de marca de producto u optimización de URL

Cuando cambie el nombre de un producto o desee mejorar su dirección URL para SEO, cree una redirección para conservar los vínculos existentes:

**URL original:**

    http://www.example.com/peripherals/keyboard.html

**Nueva URL optimizada:**

    http://www.example.com/ergonomic-keyboard.html

La herramienta de reescritura crea automáticamente una redirección 301 desde la antigua URL a la nueva, por lo que los clientes y motores de búsqueda se dirigen sin problemas a la página correcta.

#### Páginas de aterrizaje promocionales

Cree direcciones URL personalizadas temporales o permanentes para las campañas de marketing:

**URL promocionales:**

    http://www.example.com/all-on-sale.html
    http://www.example.com/save-now/spring-sale

## Configuración adicional de administración de URL

En las secciones siguientes se describe cómo configurar las reescrituras de servidor web y las URL canónicas para Commerce.

### Configurar reescrituras de servidor web

>[!NOTE]
>
>En esta sección se describe la reescritura de URL en el servidor web, que es diferente de la capacidad de la herramienta de reescritura de URL. Las reescrituras de servidor web administran el formato técnico de URL (como quitar `index.php`), mientras que la herramienta de reescritura de URL administra las redirecciones para los cambios de contenido.

La activación de las reescrituras del servidor web forma parte de la configuración inicial de Commerce y se suele configurar durante la instalación. Cuando está habilitado, el servidor web (Apache o Nginx) elimina automáticamente el nombre de archivo `index.php` de las direcciones URL, lo que crea direcciones más limpias y compatibles con la optimización de los motores de búsqueda.
El siguiente ejemplo muestra cómo aparecen las direcciones URL con y sin las reescrituras del servidor web habilitadas:

**URL sin reescritura de servidor web**

    http://www.yourdomain.com/magento/index.php/storeview/url-identifier

**URL con reescritura de servidor web**

    http://www.yourdomain.com/magento/storeview/url-identifier

#### Habilitar o deshabilitar las reescrituras de servidores web:

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo donde **[!UICONTROL General]** está expandido, elija **[!UICONTROL Web]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Search Engine Optimization]**.

   ![Configuración general: optimización del motor de búsqueda web](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Use Web Server Rewrites]** según sus preferencias.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

### Especificar URL canónicas

Para fines de la SEO, cada una de las páginas web debe tener una sola dirección URL distinta.

Si tiene una sola página accesible mediante varias direcciones URL o páginas diferentes con contenido similar, Google las verá como versiones duplicadas de la misma página. Google elige una dirección URL como versión canónica y rastrea esa y todas las demás direcciones URL se consideran direcciones URL duplicadas y se rastrean con menos frecuencia.

Si no le indica explícitamente a Google qué dirección URL es canónica, hace la elección por usted o puede considerarlas de igual peso. Esto podría provocar un comportamiento no deseado y conlleva el riesgo de un presupuesto de rastreo ineficaz y de vínculos de retorno distribuidos bajos.

Según la configuración del sitio web, puede haber varias versiones del sitio en el índice, por ejemplo:

    https://www.example.com
    https://www.example.com/
    http://www.example.com
    https://example.com
    https://www.example.com/index.html

Para especificar una página canónica, consulte [Documentación de Google Search Central](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).
