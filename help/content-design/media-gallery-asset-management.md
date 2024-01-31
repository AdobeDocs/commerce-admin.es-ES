---
title: Administración de recursos de Media Gallery
description: Obtenga información sobre cómo administrar los archivos multimedia cargados y los recursos que adquiere a través de una integración con Adobe Stock.
exl-id: 4fc489ae-b1e5-4aa4-832d-cd88c58d103a
feature: Page Content, Media
source-git-commit: a93e96353f4be0e771064cdcfbdf794772386a28
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# Administración de recursos de Media Gallery

El nuevo [Galería de medios](media-gallery.md) proporciona herramientas para administrar los archivos multimedia cargados y los recursos que adquiere a través de una [Integración de Adobe Stock](adobe-stock.md). Si ha guardado un Adobe Stock [previsualización de imagen](adobe-stock-save-preview.md), también puede [licencia](adobe-stock-license-image.md) Seleccione la imagen en la nueva Galería multimedia.

## Cargar un recurso

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Clic **[!UICONTROL Upload Image]**.

1. Seleccione el archivo que desea cargar.

   El recurso seleccionado se carga automáticamente en la carpeta seleccionada (o en la raíz de almacenamiento si no hay ninguna carpeta seleccionada).

## Ver detalles del recurso

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Haga clic en los tres puntos situados debajo del recurso (![Icono Detalles](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}) y haga clic en **[!UICONTROL View Details]**.

   ![Acciones de recurso](./assets/media-gallery-asset-actions.png){width="600" zoomable="yes"}

   Los detalles del recurso se muestran en un panel de diapositivas. Incluyen la información sobre dónde se está utilizando el recurso:

   - **[!UICONTROL Categories]**
   - **[!UICONTROL Products]**
   - **[!UICONTROL Pages]**
   - **[!UICONTROL Blocks]**

   ![Detalles del recurso](./assets/media-gallery-asset-details.png){width="600" zoomable="yes"}

   Para ver los detalles, haga clic en **[!UICONTROL Used In]** vínculos . La cuadrícula del siguiente ejemplo muestra todas las categorías en las que se utiliza un recurso específico.

   ![Cuadrícula de categorías](./assets/media-gallery-asset-categories.png){width="600" zoomable="yes"}

   También es posible eliminar el recurso del _Ver detalles_ sección.

## Editar un recurso

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Haga clic en los tres puntos situados debajo del recurso (![Icono de menú de recursos](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}) y haga clic en **[!UICONTROL Edit]**.

   ![Editar recurso](./assets/media-gallery-edit-asset.png){width="600" zoomable="yes"}

1. Si es necesario, cambie uno de los siguientes valores de metadatos:

   - **[!UICONTROL Title]**
   - **[!UICONTROL Description]**
   - **[!UICONTROL Tags/Keywords]**

   Estos datos se guardan en la base de datos y en los propios metadatos del archivo. XMP Actualmente, se admiten los formatos e IPTC.

   Puede descargar la imagen con los metadatos actualizados.

## Usar un recurso

Los recursos se pueden utilizar ampliamente en todo el administrador, como [agregar o editar una página](page-add.md), [crear o editar una categoría](../catalog/category-create.md), o [insertar imágenes desde el editor de contenido](editor-insert-image.md).

1. Acceda a la nueva Galería de medios desde un área que le permita utilizar recursos multimedia.

1. Seleccione el recurso y haga clic en **[!UICONTROL Add Selected]**.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}

## Eliminar recursos

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Clic **[!UICONTROL Delete Images...]** y active la casilla de verificación de cada recurso que desee eliminar.

1. En el diálogo de confirmación, haga clic en **[!UICONTROL Delete Image]**.

   ![Confirmación de eliminación](./assets/media-gallery-bulk-delete-confirm.png){width="500" zoomable="yes"}

## Búsqueda de recursos

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Utilice el **[!UICONTROL Search by keywords]** entrada para realizar búsquedas de imágenes por palabras clave/etiquetas.

   La búsqueda del ejemplo siguiente busca recursos que contienen una etiqueta específica (`mountain`).

   ![Búsqueda de recursos](./assets/media-gallery-asset-search.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Para obtener información sobre cómo actualizar las etiquetas de imagen, consulte la _[Editar un recurso](#edit-an-asset)_ sección.

## Filtrar recursos

>[!NOTE]
>
>El _Utilizado en_ La funcionalidad requiere que [!UICONTROL Media Gallery Image Optimization] está habilitado en la [opciones de configuración](media-gallery-image-optimization.md).

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Haga clic en **[!UICONTROL Filters]** pestaña.

   ![Filtros](./assets/media-gallery-filters.png){width="600" zoomable="yes"}

1. Defina las opciones de filtrado.

   Puede filtrar los recursos según el uso de las entidades:

   - **[!UICONTROL Used in Categories]**
   - **[!UICONTROL Used in Products]**
   - **[!UICONTROL Used in Pages]**
   - **[!UICONTROL Used in Blocks]**

   También puede filtrar los recursos por **[!UICONTROL Store View]**, **[!UICONTROL License Status]**, y **[!UICONTROL Content Status]**. Definir un intervalo de fechas para **[!UICONTROL Uploaded Date]** y/o **[!UICONTROL Modification Date]** para filtrar recursos según las fechas del archivo.

1. Clic **[!UICONTROL Apply Filters]** para ver los resultados.

   El filtrado del ejemplo siguiente busca los recursos que se utilizan en una categoría específica (`cars`) y están activadas.

   ![Filtrar los recursos habilitados por categoría](./assets/media-gallery-filter-by-category.png){width="600" zoomable="yes"}

## Buscar duplicados de imagen

1. Haga clic en **[!UICONTROL Filters]** y seleccione la pestaña **[!UICONTROL Show duplicates]** casilla de verificación

1. Para ver los resultados, haga clic en **[!UICONTROL Apply Filters]**.
