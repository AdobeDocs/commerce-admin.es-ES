---
title: Estructura del sitio y la tienda
description: Obtenga información acerca del sitio web, la tienda y la jerarquía de vistas de la tienda.
exl-id: d745cbd0-151b-4f82-bb6c-fb6b9565a014
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# Estructura del sitio y la tienda

Cuando se instala Adobe Commerce o Magento Open Source, se crea una jerarquía que incluye un sitio web principal, una tienda y una vista de la tienda. Puede crear sitios web, tiendas y vistas de tiendas adicionales, según sea necesario. Por ejemplo: además del sitio web principal, es posible que tenga sitios web adicionales con un dominio diferente. En cada sitio web, puede tener varias tiendas y, en cada tienda, vistas de tiendas independientes. Muchas instalaciones tienen un sitio web y una tienda, pero con varias vistas de la tienda para admitir diferentes idiomas.

Antes de empezar, planifique la jerarquía del catálogo de tiendas con antelación, ya que se hace referencia a ella en toda la configuración. Cada almacén puede tener una [categoría raíz](../catalog/category-root.md) independiente, lo que permite tener un conjunto completamente diferente de opciones de menú principal para cada almacén.

![Diagrama de ámbito](./assets/scope-multisite.svg){width="550"}

## Agregar tiendas

Una sola instalación de Adobe Commerce o Magento Open Source puede tener varias tiendas que compartan un administrador. Las tiendas que están en el mismo sitio web tienen la misma dirección IP y el mismo dominio, utilizan el mismo certificado de seguridad y comparten un solo proceso de cierre de compra.

Lo importante es comprender que las tiendas utilizan el mismo código y comparten un administrador. Cada tienda puede tener un catálogo independiente o las tiendas pueden compartir un catálogo. Cada tienda puede tener una [categoría raíz](../catalog/category-root.md) independiente, lo que permite tener un menú principal diferente para cada tienda. Las tiendas también pueden tener diferentes marcas, presentaciones y contenidos. Tómese un tiempo para planificar la jerarquía de la tienda teniendo en cuenta el crecimiento futuro antes de comenzar, ya que se utiliza en toda la configuración.

![Ámbito - varias tiendas](./assets/scope-multistore.svg){width="550"}

Estos son algunos ejemplos de cómo se pueden configurar las direcciones URL para varias tiendas:

| URL | Descripción |
| --- | ----------- |
| `yourdomain.com/store1`<br>`yourdomain.com/store2` | Cada almacén tiene una ruta diferente, pero comparte un dominio. |
| `store1.yourdomain.com`<br>`store2.yourdomain.com` | Cada almacén tiene un subdominio diferente del dominio principal. |

Las instalaciones de varias tiendas de Adobe Commerce deben configurarse desde el administrador y también desde la línea de comandos del servidor. La [Guía de configuración](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html?lang=es) de Adobe Commerce proporciona instrucciones detalladas para configurar el entorno del servidor.

### Paso 1: Selección del dominio de almacenamiento

El primer paso es elegir cómo desea colocar la tienda. ¿Deben las tiendas compartir un dominio, tener cada uno un subdominio o tener dominios claramente diferentes? Para cada almacén, realice una de las siguientes acciones:

- Para colocar el almacén un nivel por debajo del dominio principal, no tiene que hacer nada.
- Configure un subdominio del dominio principal.
- Configure un dominio principal diferente.

### Paso 2: Crear el almacén

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Haga clic en **[!UICONTROL Create Store]** y defina las opciones de la nueva tienda:

   - **[!UICONTROL Web Site]**: elija un sitio web que va a ser el principal de la nueva tienda. Si la instalación tiene un solo sitio web, acepte el valor predeterminado (`Main Website`).

   - **[!UICONTROL Name]**: escriba un nombre para el nuevo almacén. El nombre solo es para referencia interna.

   - **[!UICONTROL Code]**: escriba un código en minúsculas para identificar el almacén. Por ejemplo: `mainstore`.

   - **[!UICONTROL Root Category]** — Se establece en la [categoría raíz](../catalog/category-root.md) que define la estructura de categorías para el menú principal de la nueva tienda. Si ya ha creado una categoría raíz específica para el almacén, selecciónela. De lo contrario, seleccione `Default Category`. Puede volver más tarde y actualizar la configuración.

   ![Crear tienda - opciones de tienda](./assets/stores-all-store-information.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save Store]**.

### Paso 3: Crear una vista de tienda predeterminada

1. Haga clic en **[!UICONTROL Create Store View]** y defina las opciones de vista de tienda:

   - **[!UICONTROL Store]** — Se establece en el nuevo almacén que creó.

   - **[!UICONTROL Name]**: escriba un nombre para la vista. Por ejemplo, `English`.

   - **[!UICONTROL Code]**: escriba un código para la vista en caracteres en minúsculas.

   - **[!UICONTROL Status]** — Se estableció en `Enabled`.

   - **[!UICONTROL Sort Order]**: escriba un número para determinar la posición de la tienda cuando aparezca en otras tiendas.

1. Haga clic en **[!UICONTROL Save Store View]**.

   Si abre la tienda en modo de edición, verá que ahora tiene una vista predeterminada.

   ![Nuevo almacén con vista predeterminada](./assets/new-store-default-view.png){width="600" zoomable="yes"}

### Paso 4: Configuración de la dirección URL de la tienda

1. En la barra lateral _Admin_, haga clic en **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En _[!UICONTROL General]_, en el panel izquierdo de la izquierda, elija **[!UICONTROL Web]**.

1. En la esquina superior izquierda, establezca **[!UICONTROL Store View]** en la vista que creó para la nueva tienda.

1. Cuando se le pida que confirme el cambio de [ámbito](../getting-started/websites-stores-views.md#scope-settings), haga clic en **[!UICONTROL OK]**.

   ![Elija la vista de la tienda](./assets/create-store-config-view.png){width="600" zoomable="yes"}

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Base URLs]** e introduzca la dirección URL base de la tienda.

   Si es necesario, desactive la casilla de verificación **[!UICONTROL Use system value]** para cambiar la configuración.

   ![Configuración general - URL de base web](./assets/config-general-web-base-urls-clear-checkbox.png){width="600" zoomable="yes"}

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Secure Base URLs]** y repita el paso anterior si desea configurar la [URL segura](store-urls.md) de la tienda.

1. Haga clic en **[!UICONTROL Save Config]**.

### Paso 5: Configuración del servidor

Para configurar el servidor de modo que admita varios sitios web, consulte [Varios sitios web o tiendas](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html?lang=es) en la _Guía de configuración_.

Para obtener ayuda sobre la configuración del servidor web, consulte los siguientes recursos:

- [Configurar varios sitios web con NGNX](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-nginx.html?lang=es)
- [Configurar varios sitios web con Apache](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-apache.html?lang=es)

Para Adobe Commerce sobre la infraestructura en la nube, consulte [Configuración de varios sitios web o tiendas](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/multiple-sites.html?lang=es).

## Agregar sitios web

Se pueden configurar varios sitios web desde una sola instalación de Adobe Commerce o Magento Open Source con el mismo dominio o dominios diferentes. De forma predeterminada, las tiendas que están en el mismo sitio web tienen la misma dirección IP y el mismo dominio, utilizan el mismo certificado de seguridad y comparten un único proceso de cierre de compra. Si desea que cada almacén tenga un proceso de cierre de compra dedicado en su propio dominio, cada almacén debe tener una dirección IP distinta y un certificado de seguridad independiente.

Las instalaciones de varios sitios de Adobe Commerce o Magento Open Source deben configurarse desde Admin y desde la línea de comandos del servidor. La [Guía de configuración](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html?lang=es) de Commerce proporciona instrucciones detalladas para configurar el entorno del servidor.

![Ámbito - sitios web](./assets/scope-multisite.svg){width="550"}

### Paso 1: Crear un sitio web

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Create Website]**.

1. Establecer las opciones de **[!UICONTROL Web Site Information]**:

   ![Crear sitio web - opciones](./assets/create-website-info.png){width="600" zoomable="yes"}

   - **[!UICONTROL Name]**: escriba el dominio del nuevo sitio web. Por ejemplo, `domain.com`.

   - **[!UICONTROL Code]**: escriba un código que se use en el servidor para que apunte al dominio.

     El código debe comenzar por una letra minúscula (a-z) y puede incluir cualquier combinación de letras (a-z), números (0-9) y el símbolo de subrayado (_).

   - **[!UICONTROL Sort Order]** — _(Opcional)_ Escriba un número para determinar la secuencia en la que este sitio se enumera con otros sitios. Para que este sitio aparezca al principio de la lista, escriba un cero (`0`).

1. Haga clic en **[!UICONTROL Save Web Site]**.

1. Configure cada [tienda](#add-stores) y [vista de tienda](store-views.md) que se necesiten para el nuevo sitio web.

   A continuación, puede abrir el sitio web en modo de edición para establecer la tienda predeterminada.

### Paso 2: Configuración de la dirección URL de la tienda

Para configurar las [direcciones URL del almacén](store-urls.md), siga las instrucciones.

### Paso 3: Configuración del servidor

Para configurar el servidor de modo que admita varios sitios web, consulte [Varios sitios web o tiendas](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html?lang=es) en la _Guía de configuración_.

Para obtener ayuda sobre la configuración del servidor web, consulte los siguientes tutoriales:

- [Configurar varios sitios web con NGNX](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-nginx.html?lang=es)
- [Configurar varios sitios web con Apache](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-apache.html?lang=es)

Para Adobe Commerce sobre la infraestructura en la nube, consulte [Configuración de varios sitios web o tiendas](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/multiple-sites.html?lang=es).
