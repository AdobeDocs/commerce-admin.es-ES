---
title: Insertar un widget en el editor
description: Añada varios elementos de contenido a una página mediante la herramienta widget en el editor WYSIWYG.
exl-id: bbc5e059-06d8-4dda-89a7-6c9826b73fd3
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# Insertar un widget en el editor

El [widget](widget-create.md) se puede utilizar para añadir varios elementos de contenido a la página, incluidos vínculos a cualquier página de contenido o nodo, producto o categoría de Commerce. Los vínculos se pueden colocar en la página en formato de bloque o incorporar directamente al contenido. Puede utilizar la herramienta Widget para crear vínculos a los siguientes tipos de contenido:

- [Páginas de contenido](pages.md)
- [Categorías de catálogo](../catalog/categories.md)
- [Productos de catálogo](../catalog/product-create.md)

De forma predeterminada, los vínculos heredan su estilo de la hoja de estilos de la temática.

{{$include /help/_includes/directives-caution.md}}

1. Abra una página, un bloque o un bloque dinámico en modo de edición.

1. Vaya a la _[!UICONTROL Content]_y haga clic en cualquier elemento que admita el editor.

1. Sitúe el cursor donde desee que aparezca el widget y haga clic en _Insertar widget_ icono.

   ![Barra de herramientas del editor: Insertar widget](./assets/editor-toolbar-widget-button.png){width="700" zoomable="yes"}

   Si no ha habilitado Page Builder y prefiere trabajar con el código, haga clic en **[!UICONTROL Show / Hide Editor]**. Sitúe el punto de inserción en el texto en el que desea que aparezca el widget. A continuación, haga clic en **[!UICONTROL Insert Widget]**.

1. Elija la **[!UICONTROL Widget Type]**.

   Para obtener más información sobre estas opciones, consulte [Tipos de widget](widgets.md#widget-types). Los pasos siguientes utilizan un ejemplo para insertar un vínculo a un producto.

1. Para utilizar el nombre del producto, deje **[!UICONTROL Anchor Custom Text]** campo vacío.

1. Introduzca una **[!UICONTROL Anchor Custom Title]** para una mejor práctica de SEO.

   Este título no es visible en la página.

1. Establecer **[!UICONTROL Template]** a uno de los siguientes:

   - Para incorporar el vínculo al texto, seleccione `Product Link Inline Template`.

   - Para colocar el vínculo en una línea independiente, seleccione `Product Link Block Template`.

1. Clic **[!UICONTROL Select Product]** y haga lo siguiente:

   - En el árbol, vaya a la categoría que desee.

   - En la lista, seleccione el producto vinculado.

1. Clic **[!UICONTROL Insert Widget]** para colocar el vínculo en la página.

   Si está trabajando con código de HTML, [etiqueta de marcado](../systems/markup-tags.md) para el vínculo aparece en la parte superior de la página, entre llaves dobles. Si es necesario, utilice _Cortar y pegar_ para colocar la etiqueta de marcado en el código donde desea que aparezca el vínculo.

1. Cuando haya completado las ediciones de contenido, haga clic en **[!UICONTROL Save]**.
