---
title: Insertar un widget en el editor
description: Añada varios elementos de contenido a una página mediante la herramienta widget del editor de WYSIWYG.
exl-id: bbc5e059-06d8-4dda-89a7-6c9826b73fd3
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# Insertar un widget en el editor

La herramienta [widget](widget-create.md) se puede usar para agregar varios elementos de contenido a la página, incluidos vínculos a cualquier página de contenido, nodo, producto o categoría de Commerce. Los vínculos se pueden colocar en la página en formato de bloque o incorporar directamente al contenido. Puede utilizar la herramienta Widget para crear vínculos a los siguientes tipos de contenido:

- [Páginas de contenido](pages.md)
- [Categorías de catálogo](../catalog/categories.md)
- [Productos de catálogo](../catalog/product-create.md)

De forma predeterminada, los vínculos heredan su estilo de la hoja de estilos de la temática.

{{$include /help/_includes/directives-caution.md}}

1. Abra una página, un bloque o un bloque dinámico en modo de edición.

1. Vaya a la sección _[!UICONTROL Content]_&#x200B;y haga clic en cualquier elemento que admita el editor.

1. Coloque el cursor donde desee que aparezca el widget y haga clic en el icono _Insertar widget_.

   ![Barra de herramientas del editor - Insertar widget](./assets/editor-toolbar-widget-button.png){width="700" zoomable="yes"}

   Si no ha habilitado Page Builder y prefiere trabajar con el código, haga clic en **[!UICONTROL Show / Hide Editor]**. Sitúe el punto de inserción en el texto en el que desea que aparezca el widget. A continuación, haga clic en **[!UICONTROL Insert Widget]**.

1. Elija **[!UICONTROL Widget Type]**.

   Para obtener más información acerca de estas opciones, vea [Tipos de widget](widgets.md#widget-types). Los pasos siguientes utilizan un ejemplo para insertar un vínculo a un producto.

1. Para usar el nombre del producto, deje vacío el campo **[!UICONTROL Anchor Custom Text]**.

1. Escriba un **[!UICONTROL Anchor Custom Title]** como práctica recomendada de SEO.

   Este título no es visible en la página.

1. Establezca **[!UICONTROL Template]** en una de las siguientes opciones:

   - Para incorporar el vínculo al texto, seleccione `Product Link Inline Template`.

   - Para colocar el vínculo en una línea independiente, seleccione `Product Link Block Template`.

1. Haga clic en **[!UICONTROL Select Product]** y haga lo siguiente:

   - En el árbol, vaya a la categoría que desee.

   - En la lista, seleccione el producto vinculado.

1. Haga clic en **[!UICONTROL Insert Widget]** para colocar el vínculo en la página.

   Si está trabajando con código HTML, aparecerá una [etiqueta de marcado](../systems/markup-tags.md) para el vínculo en la parte superior de la página, entre llaves dobles. Si es necesario, use _Cortar y pegar_ para colocar la etiqueta de marcado en el código donde desea que aparezca el vínculo.

1. Una vez completadas las ediciones del contenido, haga clic en **[!UICONTROL Save]**.
