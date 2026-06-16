---
title: Optimización de imagen de Media Gallery
description: Aprenda a utilizar la optimización de imágenes para sus  [!DNL Commerce] recursos multimedia.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
TQID: https://experienceleague.adobe.com/BTjXX6X70q2Mwm0xPNx-t429R5m93VprCHBDcYgQNpY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 211
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

<!-- Last updated from includes: 2024-01-30 15:43:39 -->
