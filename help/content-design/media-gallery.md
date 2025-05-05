---
title: El(la) [!DNL Media Gallery]
description: Utilice la Galería multimedia para organizar y administrar los archivos multimedia en el servidor.
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# El [!DNL Media Gallery]

Con Adobe Commerce o Magento Open Source 2.4, los comerciantes pueden usar el nuevo _Enhanced_ [!DNL Media Gallery] para organizar y administrar sus archivos multimedia en el servidor. Este nuevo [!DNL Media Gallery] contiene las mismas funcionalidades que el almacenamiento de medios existente, pero incluye una interfaz de usuario mejorada y una integración más estrecha con [Adobe Stock][adobe-stock].

![Imágenes mostradas en la cuadrícula de la Galería multimedia](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Las imágenes de producto agregadas a la sección de productos [_[!UICONTROL Images and Videos]_](../catalog/product-image.md#upload-an-image) no son administradas por [!DNL Media Gallery]. Solo las imágenes utilizadas en los campos de la sección de productos&#x200B;_[!UICONTROL Content]_ se muestran y filtran en el nuevo [!DNL Media Gallery].

## Habilitar el nuevo [!DNL Media Gallery]

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL System]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]**.

   ![Configuración avanzada - [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Enable Old Media Gallery]** en `No`.

1. Haga clic en **[!UICONTROL Save Config]**.

1. Cuando se le solicite, haga clic en el vínculo **[!UICONTROL Cache Management]** en el mensaje del sistema y actualice la caché no válida.

   El menú [[!UICONTROL Content]](/help/content-design/content-menu.md) ahora muestra la nueva opción _[!UICONTROL Media Gallery]_.

>[!NOTE]
>
>La funcionalidad completa para el nuevo [!DNL Media Gallery] requiere que `media.gallery.synchronization` y `media.content.synchronization` consumidores de cola se inicien para la sincronización inicial. Consulte [Administrar colas de mensajes](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html?lang=es) en la _Guía de configuración_ para obtener más información.

## Acceder al nuevo(a) [!DNL Media Gallery]

Se puede acceder al nuevo [!DNL Media Gallery] desde el menú Contenido o cuando [agrega o edita una página](/help/content-design/page-add.md). También puede obtener acceso a ella al [crear o editar una categoría](/help/catalog/category-create.md) o al [insertar imágenes mediante el Editor de contenido](/help/content-design/editor-insert-image.md).

Para tener acceso al nuevo(a) [!UICONTROL Media Gallery] a través del menú [!UICONTROL Content]:

- En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

Para acceder a la nueva Galería de medios al agregar o editar una página:

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Haga clic en **[!UICONTROL Add a New Page]**.

   Si desea editar una página existente, puede usar la columna _[!UICONTROL Action]_&#x200B;para hacer clic en **[!UICONTROL Select]**&#x200B;y elegir **[!UICONTROL Edit]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Content]** y haga lo siguiente:

   - Si tiene [Page Builder habilitado](../page-builder/setup.md), expanda el panel **[!UICONTROL Media]** y arrastre un marcador de posición **[!UICONTROL Image]** al contenedor de destino. Luego haga clic en **[!UICONTROL Select from Gallery]**.

     ![Arrastrar imagen al escenario](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - Si tiene habilitado [WYSIWYG editor](/help/content-design/editor.md), haga clic en **[!UICONTROL Show/Hide Editor]** y luego en **[!UICONTROL Insert Image]**.

## Demostración de [!DNL Media Gallery]

Para obtener más información acerca de [!DNL Media Gallery], vea este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/3411043?quality=12&learn=on&captions=spa)

[adobe-stock]: https://stock.adobe.com

