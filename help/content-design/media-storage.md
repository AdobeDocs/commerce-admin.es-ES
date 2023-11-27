---
title: Almacenamiento de medios
description: Descubra cómo el almacenamiento de medios le ayuda a organizar y obtener acceso a los archivos de medios de Commerce que se almacenan en el servidor.
exl-id: 5cf1bb20-d747-4a12-8558-e167c229efe8
feature: Page Content, Media
source-git-commit: 7dae6b6d387c796c5ff472293c6590fabaa83e85
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Almacenamiento de medios

El almacenamiento de medios le ayuda a organizar y obtener acceso a los archivos multimedia almacenados en el servidor. La ruta a la ubicación de los archivos viene determinada por la variable [URL base](../stores-purchase/store-urls.md) configuración. Se puede acceder a los archivos del almacenamiento de medios desde el editor mientras se trabaja en páginas y bloques estáticos. Normalmente, el almacenamiento de medios reside en el sistema de archivos en el mismo servidor que el [!DNL Commerce] archivos de programa.

Como alternativa, los archivos multimedia se pueden administrar en una [database](media-storage-database.md), o en un servidor independiente o [red de distribución de contenido](media-storage-content-delivery-network.md). La ventaja de utilizar un almacenamiento alternativo es que minimiza el esfuerzo necesario para sincronizar los medios. El rendimiento de la sincronización se ve especialmente afectado cuando se implementan varias instancias del sistema en diferentes servidores que necesitan acceso a las mismas imágenes, archivos CSS y otros archivos multimedia.

El editor se puede configurar para que utilice estático o [URL de medios dinámicos](../catalog/catalog-urls.md#configure-catalog-media-url-format) para el contenido del catálogo en categorías o descripciones de productos.

![[!DNL Commerce] Almacenamiento de medios](./assets/media-storage.png){width="650" zoomable="yes"}

## Agregar archivos al almacenamiento de medios

Los dos primeros pasos son los mismos que si inserta una imagen.

1. En el [editor](editor.md) , haga clic en _Insertar imagen_ icono.

   ![Icono Insertar imagen](./assets/editor-toolbar-image-button.png){width="700" zoomable="yes"}

   Esta acción abre el _[!UICONTROL Insert/edit image]_diálogo.

1. Después _[!UICONTROL Source]_, haga clic en_ Buscar _icono (![Icono de búsqueda](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

1. En el árbol de directorios de la izquierda, realice una de las siguientes acciones:

   - Vaya a la carpeta en la que desea guardar la imagen cargada.

   - Vaya al lugar en el que desea crear una carpeta y haga clic en **Crear carpeta**.

     Para añadir una carpeta, introduzca el nombre de la carpeta y haga clic en **[!UICONTROL OK]**.

1. Para agregar uno o más archivos a Media Storage, puede cargarlos desde el sistema o utilizar el [Integración de Adobe Stock](adobe-stock.md):

   Para cargar archivos desde el sistema, haga clic en **[!UICONTROL Choose Files]** y haga lo siguiente:

   - En el directorio del equipo local, vaya a la ubicación de las imágenes.

   - Seleccione cada imagen que desee cargar.

   - Haga clic **[!UICONTROL Open]**.

   Para usar recursos de Adobe Stock con [integración](adobe-stock.md):

   - Haga clic **[!UICONTROL Search Adobe Stock]**.

   - Añada una vista previa o una imagen con licencia de Adobe Stock (consulte [Uso de imágenes de Adobe Stock](adobe-stock-manage.md)).

Las imágenes se cargan en la carpeta de Media Storage actual del servidor.

![[!DNL Commerce] Almacenamiento de medios](./assets/media-storage.png){width="650" zoomable="yes"}

## Inserción de una imagen desde el almacenamiento de medios

Abra la página o el bloque que desea editar. A continuación, utilice uno de los siguientes métodos para insertar una imagen desde el almacenamiento de medios:

### Método 1: modo WYSIWYG

1. En el [editor](editor.md) , haga clic en _Insertar imagen_ icono.

1. Después _[!UICONTROL Source]_, haga clic en_ Buscar _icono (![Icono de búsqueda](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

   ![Selección del icono de búsqueda](./assets/editor-dialog-insert-image.png){width="250" zoomable="yes"}

1. En el árbol de directorio de la izquierda, navegue hasta la carpeta donde se almacena la imagen.

1. Seleccione el mosaico de la imagen y haga clic en **[!UICONTROL Add Selected]**.

### Método 2: modo HTML

1. Coloque el cursor en el código donde `<img>` se va a insertar la etiqueta.

1. Haga clic **[!UICONTROL Insert Image]**.

   ![Insertar imagen (modo HTML)](./assets/editor-html-mode-insert-image.png){width="600" zoomable="yes"}
