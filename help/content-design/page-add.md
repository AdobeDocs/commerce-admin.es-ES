---
title: Adición y eliminación de páginas
description: Aprenda a agregar y quitar páginas de contenido utilizadas en su  [!DNL Commerce] tienda.
exl-id: a7a503ea-3631-4be2-81e4-aed2ae9419dc
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '1122'
ht-degree: 0%

---

# Adición y eliminación de páginas

El proceso de añadir una página de contenido a la tienda es esencialmente el mismo para cualquier tipo de página que desee crear. Puede incluir texto, imágenes, bloques de contenido, variables y widgets. La mayoría de las páginas de contenido están diseñadas para su lectura por los motores de búsqueda primero y por las personas en segundo lugar. Tenga en cuenta las necesidades de cada una de estas dos audiencias diferentes al elegir el título de página, la dirección URL y al maquetar los metadatos, y el contenido. Una vez completada la página, se puede agregar a la navegación de tu tienda, vincular a otras páginas, vincular desde el pie de página de tu tienda o usar como una nueva [página de inicio](page-home-new.md).

![Cuadrícula de páginas](./assets/pages-grid.png){width="700" zoomable="yes"}

## Agregar una página

Las siguientes instrucciones le guían a través de cada paso para crear una página básica. Algunas funciones avanzadas se omiten, pero se tratan en otros temas.

### Paso 1: Crear la página

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Haga clic en **[!UICONTROL Add New Page]**.

   ![Nueva página](./assets/pages-new-page.png){width="600" zoomable="yes"}

1. Si no desea publicar la página inmediatamente, establezca **[!UICONTROL Enable Page]** en `No`.

1. Escriba **[!UICONTROL Page Title]**.

   El título de la página aparece en la [ruta de exploración](../catalog/navigation-breadcrumb-trail.md).

### Paso 2: Completar el contenido

Según la [configuración avanzada de herramientas de contenido](../configuration-reference/general/content-management.md), agregue el contenido de la página.

#### Uso de las herramientas de contenido de Page Builder

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

   ![Contenido con Page Builder](../page-builder/assets/pb-page-content.png){width="600" zoomable="yes"}

1. En el cuadro **[!UICONTROL Content Heading]**, escriba el encabezado que desea que aparezca en la parte superior de la página.

   Si se habilita, el escenario y el panel [Page Builder](../page-builder/introduction.md) aparecerán debajo del encabezado de contenido. Para obtener más información, consulte [Workspace](../page-builder/workspace.md). Si _Page Builder_ no está habilitado, el editor se abrirá en modo WYSIWYG con la barra de herramientas en la parte superior.

1. Complete el contenido y dé formato al texto según sea necesario.

#### Uso de la barra de herramientas del editor

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

   ![Contenido](./assets/page-content-editor.png){width="600" zoomable="yes"}

1. En el cuadro **[!UICONTROL Content Heading]**, escriba el encabezado que desea que aparezca en la parte superior de la página.

1. Complete el contenido y dé formato al texto según sea necesario.

   Puede agregar [imágenes](media-storage.md), [variables](../systems/variables-predefined.md) y [widgets](widgets.md) según sea necesario. Para obtener más información, vea [Usar el editor](editor.md).

### Paso 3: Completar la información de SEO

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]**.

   ![Optimización del motor de búsqueda](./assets/page-search-engine-optimization.png){width="600" zoomable="yes"}

1. Acepte el valor predeterminado o escriba otro **[!UICONTROL URL Key]** que esté formado por todos los caracteres en minúsculas, con guiones en lugar de espacios.

   La clave URL predeterminada se creó al guardar la página y se basa en el encabezado de contenido.

1. Escriba un **[!UICONTROL Meta Title]** para la página.

   El metatítulo debe contener menos de 70 caracteres y aparece en la barra de título y en la pestaña del explorador.

1. Escriba su elección de **[!UICONTROL Meta Keywords]** de alto valor que los motores de búsqueda puedan usar para indexar la página.

   Separe las palabras con comas. Algunos motores de búsqueda omiten las metapalabras clave, pero otros las utilizan.

1. Para **[!UICONTROL Meta Description]**, escriba una breve descripción de la página para los listados de resultados de búsqueda.

   Lo ideal es que la descripción tenga entre 150 y 160 caracteres de longitud, con un límite máximo de 255.

1. Haga clic en **[!UICONTROL Save]**.

### Paso 4: Especificar el ámbito de la página

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Page in Websites]**.

   ![Páginas en sitios web](./assets/page-in-websites.png){width="600" zoomable="yes"}

1. En la lista **[!UICONTROL Store View]**, seleccione cada vista donde la página vaya a estar disponible.

   Si la instalación tiene varios sitios web, seleccione cada sitio web y la vista de tienda donde la página vaya a estar disponible.

### Paso 5: Identificar la página principal (si corresponde)

{{ee-feature}}

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Hierarchy]**.

   ![Jerarquía](./assets/page-hierarchy.png){width="600" zoomable="yes"}

1. Si esta página es un elemento secundario de otra página, active la casilla de verificación del **[!UICONTROL Parent page]**.

### Paso 6: introducir cambios de diseño (opcional)

1. Para cambiar el diseño de la página, expanda ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Design]**.

   ![Diseño](./assets/page-design.png){width="600" zoomable="yes"}

1. Para cambiar el diseño de columna de la página, establezca **[!UICONTROL Layout]** en una de las siguientes opciones:

   - `Empty`
   - `1 column`
   - `2 columns with left bar`
   - `2 columns with right bar`
   - `3 columns`
   - `Page -- Full Width` (Requiere [Page Builder](../page-builder/introduction.md))
   - `Category -- Full Width` (Requiere Page Builder)
   - `Product -- Full Width` (Requiere Page Builder)

1. Para aplicar un **[!UICONTROL Custom Layout Update]**, elija el nombre del archivo en la lista.

   Para obtener más información, consulte [Actualizaciones de diseño](layout-updates.md).

1. Para cambiar el tema de la página, establezca **[!UICONTROL New Theme]** en uno de los siguientes:

   - `Magento Black`
   - `Magento Luma`

1. ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Para programar un cambio de diseño, expanda ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Custom Design Update]** y haga lo siguiente:

   ![Actualización de diseño personalizado](./assets/page-custom-design-update.png){width="600" zoomable="yes"}

   - Use el calendario (![Icono del calendario](../assets/icon-calendar.png)) para elegir las fechas de **[!UICONTROL From]** y **[!UICONTROL To]** para que el cambio surta efecto.

   - Para aplicar un tema diferente a la página, seleccione el nombre de **[!UICONTROL New Theme]**.

   - Para cambiar el diseño de columna de la página, elija el(la) **[!UICONTROL Layout]** que desee aplicar.

### Paso 7: Previsualizar la página

1. Haga clic en la flecha **[!UICONTROL Save]** y elija **[!UICONTROL Save & Close]** para regresar a la cuadrícula Páginas.

1. Busque la página en la cuadrícula y seleccione **[!UICONTROL View]** en la columna _[!UICONTROL Action]_.

1. Para volver a la cuadrícula, haga clic en **[!UICONTROL Back]** en la esquina superior izquierda de la ventana del explorador.

### Paso 8: Publicar la página

1. Seleccione **[!UICONTROL Edit]** en la columna _[!UICONTROL Action]_de la cuadrícula.

1. Establezca **[!UICONTROL Enable Page]** en `Yes`.

1. Haga clic en la flecha **[!UICONTROL Save]** y elija **[!UICONTROL Save & Close]**.

## Duplicación de una página

Cualquier página de contenido puede utilizarse como plantilla y guardarse como duplicado. Puede utilizar esta técnica que ahorra tiempo para crear un diseño coherente para las páginas de contenido de todo el sitio. La página duplicada conserva el Título de página del original, pero se deben actualizar los campos Clave de URL y Estado.

![Guardar y duplicar](./assets/page-duplicate-save-menu.png){width="600" zoomable="yes"}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. En la cuadrícula, busque la página que desea duplicar y haga clic en **[!UICONTROL Edit]** en la columna _[!UICONTROL Action]_.

1. Haga clic en la flecha **[!UICONTROL Save]** y elija **[!UICONTROL Save & Duplicate]**.

1. Cuando vea los mensajes de que la página se ha guardado y duplicado, haga clic en **[!UICONTROL Back]** en la barra de botones superior para volver a la cuadrícula.

1. Busque la página duplicada en la cuadrícula y tome nota de lo siguiente:

   - El Título de página es el mismo que el original.
   - Se asigna una clave URL única, pero temporal.
   - El estado de la página es `Disabled`.

1. Abra la página duplicada en el modo _Editar_ y haga lo siguiente:

   - Si desea publicar la página inmediatamente, establezca **[!UICONTROL Enable Page]** en `Yes`.

   - Actualice **[!UICONTROL Page Title]** según sea necesario.

   - Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Search Engine Optimization]** e introduzca el **[!UICONTROL URL Key]** único que desea usar para la página duplicada.

     ![Clave de URL temporal](./assets/page-search-engine-optimization-url-key-duplicate.png){width="600" zoomable="yes"}

   - Actualice el contenido restante de la página, según sea necesario.

1. Haga clic en la flecha **[!UICONTROL Save]** y elija **[!UICONTROL Save & Close]**.

   La página duplicada de la cuadrícula refleja los cambios.

## Menú Guardar

| Comando | Descripción |
|--- |--- |
| [!UICONTROL Save] | Guarde la página actual y continúe trabajando. |
| [!UICONTROL Save & New] | Guarde y cierre la página actual y empiece una nueva página. |
| [!UICONTROL Save & Duplicate] | Guarde y cierre la página actual y abra una nueva copia duplicada. |
| [!UICONTROL Save & Close] | Guarde y cierre la página actual y vuelva a la cuadrícula Páginas. |

{style="table-layout:auto"}

## Eliminación de una página

Existen dos formas de eliminar una página creada. Puede quitarlo de la cuadrícula _[!UICONTROL Pages]_o de la página_[!UICONTROL Edit]_.

### Método 1: Quitar una página de la cuadrícula Páginas

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Busque las páginas que utilizan filtros encima de la cuadrícula y marque la casilla de verificación de una o varias páginas que desee eliminar.

1. En la esquina superior izquierda de la lista, establezca **[!UICONTROL Actions]** en `Delete`.

1. Para confirmar la acción, haga clic en **[!UICONTROL OK]**.

### Método 2: Eliminar una página de la página de edición

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Busque la página que desea eliminar.

1. En la columna _[!UICONTROL Actions]_de la entidad de página, haga clic en **[!UICONTROL Select]**y elija **[!UICONTROL Edit]**.

1. En la barra de botones, haga clic en **[!UICONTROL Delete Page]**.

1. Para confirmar la acción, haga clic en **[!UICONTROL OK]**.
