---
title: Optimización de imagen de Media Gallery
description: Aprenda a utilizar la optimización de imágenes para sus  [!DNL Commerce] recursos multimedia.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# Optimización de imagen de Media Gallery

La nueva [Galería multimedia](media-gallery.md) proporciona una característica de _optimización de imágenes_, que mejora el rendimiento y reduce el tamaño de los archivos multimedia en la tienda. Esta optimización está habilitada de forma predeterminada y se puede modificar en los ajustes de configuración de la tienda.

## Configurar optimización de imágenes

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL System]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** y haga lo siguiente:

   - Establezca **[!UICONTROL Enable Image Optimization]** en `Yes`.
   - Escriba los valores **[!UICONTROL Maximum Width]** y **[!UICONTROL Maximum Height]** (en píxeles) según sus necesidades.

## Comportamiento

Cuando la funcionalidad de optimización de imágenes de la Galería multimedia está habilitada, se inserta automáticamente una copia optimizada de una imagen en el contenido de [Galería multimedia](media-gallery.md) en lugar del archivo original.

Cuando se cambian los valores _Anchura máxima_ y _Altura máxima_ en la configuración, se actualizan todas las imágenes optimizadas existentes que se insertaron anteriormente.

La optimización de imágenes de la Galería multimedia requiere que los consumidores de cola de `media.gallery.renditions.update` se estén ejecutando para regenerar imágenes optimizadas cuando se cambie la configuración. Consulte [Administrar colas de mensajes](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) en la _Guía de configuración_ para obtener más información.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}
