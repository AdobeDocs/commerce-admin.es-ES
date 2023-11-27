---
title: 'Categorías: configuración de contenido'
description: Obtenga información acerca del uso de [!UICONTROL Content] configuración para definir cualquier contenido adicional que aparezca en la página de categoría.
exl-id: 988083e1-0993-4e08-b5e6-8b0855e56467
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# Categorías: configuración de contenido

El _[!UICONTROL Content]_la configuración determina si aparece contenido adicional en la página categoría. Además de la lista de productos de categoría, la página puede incluir una imagen, una descripción y un bloque de CMS. Puede usar el complemento [[!DNL Page Builder]](../page-builder/introduction.md) herramientas de contenido para definir la descripción de la categoría.

## Añada la descripción de la categoría en [!DNL Page Builder]

1. Abra la categoría en modo de edición.

1. Desplazarse hacia abajo y expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Content]** sección.

   ![Contenido de categoría](./assets/category-content.png){width="600" zoomable="yes"}

1. En la parte superior derecha de la **[!UICONTROL Description]** , haga clic en **[!UICONTROL Edit with Page Builder]**.

1. Utilice el [[!DNL Page Builder]](../page-builder/introduction.md) herramientas de contenido para [editar cualquier texto existente](../page-builder/text.md) y agregue otro contenido (si es necesario).

## [!DNL Page Builder] previsualización

Cuando expanda el _Contenido_ para una categoría existente en la que hay contenido creado con [!DNL Page Builder], muestra una previsualización del **[!UICONTROL Description]** contenido tal como aparecería en la página de categoría. Al hacer clic en el área de contenido, se abre [!DNL Page Builder] espacio de trabajo, donde puede realizar las actualizaciones que sean necesarias.

![Previsualización de descripción](../page-builder/assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

Esta vista previa del contenido está habilitada para los formularios de productos y categorías de forma predeterminada. Si el rendimiento se ve afectado debido a la carga de la vista previa, puede deshabilitar la vista previa en el [Configuración de administración de contenido](../configuration-reference/general/content-management.md#advanced-content-tools) configuración.

## Añada la descripción de la categoría en el editor

Introduzca solo caracteres ASCII sin formato en el cuadro de texto. Si pega texto desde un procesador de texto, guárdelo primero como un archivo .TXT sin formato para eliminar los caracteres de control invisibles.

Para obtener más información, consulte [Editor WYSIWYG](../content-design/editor.md).

1. Abra la categoría en modo de edición.

1. Desplazarse hacia abajo y expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Content]** sección.

   ![Contenido de categoría](./assets/category-content-ce.png){width="500" zoomable="yes"}

1. Introduzca la categoría **[!UICONTROL Description]** y utilice el [barra del editor](../content-design/editor.md) para formatear según sea necesario.

   Puede arrastrar la esquina inferior derecha para cambiar el alto del cuadro de texto.

## Añadir un bloque de CMS a la página de categoría

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. En el árbol de categorías, seleccione la categoría que desee editar.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Content]** sección.

1. Para **[!UICONTROL Add the CMS block]**, seleccione el bloque que desee añadir.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Display Settings]** sección.

1. Configure las variables **[!UICONTROL Display Mode]** a uno de los siguientes:

   - `Static block only`
   - `Static block and products`

1. Cuando termine, haga clic en **[!UICONTROL Save]** y revise la visualización del bloque en la tienda (requiere actualizar la caché).

## Referencia de configuración de contenido

| Configuración | [Ámbito](../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Category Image] | Vista de tienda | Especifica una imagen para la parte superior de la página de categoría. Métodos: <br/><br/>**[!UICONTROL Upload]**: carga un archivo de imagen desde el equipo local a la galería y lo utiliza como imagen de categoría.<br/><br/>**[!UICONTROL Select from Gallery]** - Le pide que elija una imagen existente de la galería. <br/><br/>![Icono de cámara de Page Builder](../assets/icon-camera.png) : arrastre un archivo de imagen al mosaico de la cámara o busque la imagen y selecciónela en el sistema de archivos local. |
| [!UICONTROL Description] | Vista de tienda | Especifica una descripción que aparece en la página de categoría. <br/><br/>**[!UICONTROL Edit with Page Builder]**- Abre el [[!DNL Page Builder] workspace](../page-builder/workspace.md), donde puede editar la descripción.<br/><br/>**[!UICONTROL Show / Hide Editor]** : Alterna la visualización entre los modos de editor WYSIWYG y HTML. |
| [!UICONTROL Add CMS Block] | Vista de tienda | Agrega un existente [Bloque CMS](../content-design/blocks.md) a la página categoría. |

{style="table-layout:auto"}
