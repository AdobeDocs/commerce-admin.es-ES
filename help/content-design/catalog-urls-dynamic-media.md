---
title: URL de Dynamic Media
description: Obtenga información acerca del uso de una URL de medios dinámicos como referencia relativa a una imagen u otro recurso multimedia.
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# URL de Dynamic Media

Una URL de medios dinámicos es una referencia relativa a una imagen u otro recurso multimedia. Si se habilita, se pueden usar direcciones URL de medios dinámicos para vincularlas directamente a recursos del servidor o a archivos almacenados en una [red de distribución de contenido](media-storage-content-delivery-network.md). El uso de direcciones URL de medios dinámicos puede afectar el rendimiento del catálogo, y el [editor](editor.md#configure-the-editor) se puede configurar para usar direcciones URL de medios estáticos o dinámicos.

Al igual que con todas las [etiquetas de marcado](../systems/markup-tags.md), la directiva está encerrada entre llaves dobles. El formato de una URL de medios dinámicos es el siguiente:

`\{\{media url="path/to/image.jpg"}}`

Las directivas de URL dinámicas se procesan a partir del contenido de HTML guardado cuando la página se procesa en la tienda. Cada vez que se representa la página, el contenido se analiza para `\{\{media url="..."}}` y cada directiva se reemplaza con la URL de medios correspondiente.

{{$include /help/_includes/directives-caution.md}}

## Configuración de URL de medios estáticos

De forma predeterminada, las imágenes insertadas en el catálogo desde el editor de WYSIWYG tienen direcciones URL relativas y dinámicas. Si prefiere utilizar una dirección URL estática, puede cambiar el valor de configuración.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo bajo _[!UICONTROL General]_, elija **[!UICONTROL Content Management]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL WYSIWYG Options]**.

   ![Opciones de WYSIWYG](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]** en una de las siguientes opciones:

   - `Yes`: utiliza direcciones URL estáticas para el contenido multimedia insertado con el editor de WYSIWYG. Las direcciones URL estáticas son absolutas y se rompen si cambia la [dirección URL base](../stores-purchase/store-urls.md) del almacén.

   - `No` - (Predeterminado) Utiliza direcciones URL dinámicas para el contenido multimedia insertado con el editor de WYSIWYG, según la directiva `\{\{media url="..."}}`. Las direcciones URL dinámicas son relativas y no se rompen si cambia la dirección URL base del almacén.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
