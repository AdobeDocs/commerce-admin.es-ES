---
title: Optimización de imagen de Media Gallery
description: Aprenda a utilizar la optimización de imágenes para su [!DNL Commerce] recursos de medios.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
source-git-commit: a93e96353f4be0e771064cdcfbdf794772386a28
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Optimización de imagen de Media Gallery

El nuevo [Galería de medios](media-gallery.md) proporciona un _optimización de imágenes_ función, que mejora el rendimiento y disminuye el tamaño de los archivos multimedia en la tienda. Esta optimización está habilitada de forma predeterminada y se puede modificar en los ajustes de configuración de la tienda.

## Configurar optimización de imágenes

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL System]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** y haga lo siguiente:

   - Establecer **[!UICONTROL Enable Image Optimization]** hasta `Yes`.
   - Introduzca el **[!UICONTROL Maximum Width]** y **[!UICONTROL Maximum Height]** valores (en píxeles) según sus necesidades.

## Comportamiento

Cuando la funcionalidad de optimización de imágenes de la Galería multimedia está habilitada, se inserta automáticamente una copia optimizada de una imagen en el contenido del [Galería de medios](media-gallery.md) en lugar del archivo original.

Si la variable _Anchura máxima_ y _Altura máxima_ Si los valores de se cambian en la configuración, se actualizan todas las imágenes optimizadas existentes que se insertaron anteriormente.

La optimización de imágenes de la Galería multimedia requiere que la variable `media.gallery.renditions.update` los consumidores de cola se están ejecutando para regenerar imágenes optimizadas cuando se cambia la configuración. Consulte [Administrar colas de mensajes](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) en el _Guía de configuración_ para obtener más información.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}
