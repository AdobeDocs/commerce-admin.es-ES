---
title: El [!DNL Media Gallery]
description: Utilice la Galería multimedia para organizar y administrar los archivos multimedia en el servidor.
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# El [!DNL Media Gallery]

Con Adobe Commerce o Magento Open Source 2.4, los comerciantes pueden utilizar el nuevo _mejorado_ [!DNL Media Gallery] para organizar y administrar sus archivos multimedia en el servidor. Esta nueva [!DNL Media Gallery] contiene las mismas funcionalidades que el almacenamiento de medios existente, pero incluye una interfaz de usuario mejorada y una integración más estrecha con [Adobe Stock][adobe-stock].

![Imágenes mostradas en la cuadrícula de la Galería multimedia](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Imágenes de productos añadidas a [_[!UICONTROL Images and Videos]_sección de productos](../catalog/product-image.md#upload-an-image) no son administrados por [!DNL Media Gallery]. Solo las imágenes utilizadas en_[!UICONTROL Content]_ los campos de sección del producto se muestran y filtran en la nueva [!DNL Media Gallery].

## Habilitar el nuevo [!DNL Media Gallery]

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL System]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]**.

   ![Configuración avanzada: [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. Establecer **[!UICONTROL Enable Old Media Gallery]** hasta `No`.

1. Haga clic **[!UICONTROL Save Config]**.

1. Cuando se le solicite, haga clic en **[!UICONTROL Cache Management]** vínculo en el mensaje del sistema y actualice la caché no válida.

   El [[!UICONTROL Content] menú](/help/content-design/content-menu.md) ahora muestra el nuevo _[!UICONTROL Media Gallery]_opción.

>[!NOTE]
>
>Funcionalidad completa para el nuevo [!DNL Media Gallery] requiere `media.gallery.synchronization` y `media.content.synchronization` consumidores de cola que se van a iniciar para la sincronización inicial. Consulte [Administrar colas de mensajes](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) en el _Guía de configuración_ para obtener más información.

## Acceda a la nueva [!DNL Media Gallery]

El nuevo [!DNL Media Gallery] es accesible desde el menú Contenido o cuando [agregar o editar una página](/help/content-design/page-add.md). También puede acceder a ella cuando [crear o editar una categoría](/help/catalog/category-create.md), o cuando [inserción de imágenes con el editor de contenido](/help/content-design/editor-insert-image.md).

Para acceder al nuevo [!UICONTROL Media Gallery] a través de [!UICONTROL Content] menú:

- En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

Para acceder a la nueva Galería de medios al agregar o editar una página:

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Haga clic **[!UICONTROL Add a New Page]**.

   Si desea editar una página existente, puede utilizar la variable _[!UICONTROL Action]_columna para hacer clic **[!UICONTROL Select]**y elija **[!UICONTROL Edit]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Content]** y haga lo siguiente:

   - Si tiene [Page Builder habilitado](../page-builder/setup.md), expanda el **[!UICONTROL Media]** panel y arrastre un **[!UICONTROL Image]** marcador de posición al contenedor de destinatario. Luego haga clic en **[!UICONTROL Select from Gallery]**.

     ![Arrastrar imagen al escenario](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - Si tiene el [Editor WYSIWYG habilitado](/help/content-design/editor.md), haga clic en **[!UICONTROL Show/Hide Editor]** y luego haga clic en **[!UICONTROL Insert Image]**.

## [!DNL Media Gallery] demostración

Para obtener más información sobre [!DNL Media Gallery], vea este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/343785?quality=12)

[adobe-stock]: https://stock.adobe.com

