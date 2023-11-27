---
title: Editor WYSIWYG
description: Aprenda a utilizar el editor y a trabajar con contenido en una vista _Lo que ve es lo que obtiene_ (WYSIWYG).
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# Editor WYSIWYG

El editor permite introducir y dar formato mientras se trabaja en una _Lo Que Ves Es Lo Que Obtienes_ (WYSIWYG) vista del contenido. Si prefiere trabajar directamente con el código de HTML subyacente, puede cambiar fácilmente los modos. El editor se puede utilizar para crear contenido para [páginas](pages.md), [bloques](blocks.md), y [descripciones de productos](../catalog/product-content.md). Cuando trabaje en los detalles del producto, acceda al editor haciendo clic en **[!UICONTROL Show / Hide Editor]**.

>[!NOTE]
>
>TinyMCE 5 es el editor WYSIWYG predeterminado. Una actualización de la biblioteca TinyMCE 5.10 en Adobe Commerce y Magento Open Source 2.4.5 resuelve una vulnerabilidad que permitía la ejecución arbitraria de JavaScript al actualizar una imagen o vínculo mediante algunos tipos de URL. TinyMCE 3 quedó obsoleto en la versión 2.4.0 y se eliminó en la versión 2.4.3. TinyMCE 4 se eliminó en la versión 2.4.4.

![Barra de herramientas Editor](./assets/editor-toolbar.png){width="700" zoomable="yes"}

En los temas siguientes se proporciona información detallada sobre el uso del editor:

- [Inserción de un vínculo](editor-insert-link.md)
- [Insertar una imagen](editor-insert-image.md)
- [Inserción de un widget](editor-widget.md)
- [Insertar una variable](editor-insert-variable.md)

## Configuración del editor

El editor WYSIWYG está habilitado de forma predeterminada y se puede utilizar para editar contenido en páginas y bloques de CMS, y en productos y categorías. En la configuración, puede activar o desactivar el editor y seleccionar utilizar la función estática en lugar de la de [dinámico](../catalog/catalog-urls.md#dynamic-url), direcciones URL para el contenido multimedia en las descripciones de productos y categorías.

![Opciones WYSIWYG](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

Para ver una descripción detallada de todas las opciones de WYSIWYG, consulte [Gestión de contenido](../configuration-reference/general/content-management.md) en el _Referencia de configuración_.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, debajo de _[!UICONTROL General]_, elija **[!UICONTROL Content Management]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]**.

1. Establecer **[!UICONTROL Enable WYSIWYG Editor]** según sus preferencias.

   El editor está habilitado de forma predeterminada.

1. Establecer **[!UICONTROL Static URLs for Media Content in WYSIWYG]** a su preferencia para todos [contenido multimedia](../catalog/catalog-urls.md#static-url) que se introduce con el editor WYSIWYG.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.
