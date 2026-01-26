---
title: Añadir bloques de contenido
description: Cree bloques personalizados de contenido que pueda reutilizar en cualquier página o dentro de otro bloque.
exl-id: 2f104d77-a1d1-4f10-82ce-014955fe560b
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Añadir bloques de contenido

Se pueden crear bloques personalizados de contenido y luego agregarlos a cualquier página, grupo de páginas o incluso a otro bloque. Por ejemplo, puede colocar un control deslizante de imagen en un bloque y, a continuación, colocar el bloque en la página principal. El área de trabajo Bloques usa los mismos [controles básicos](pages-workspace.md) que el área de trabajo _Páginas_ para ayudarle a encontrar bloques disponibles y realizar tareas de mantenimiento rutinarias. Cuando finalice el bloque, puedes usar la herramienta [Widget](widget-static-block.md) para colocarla en páginas específicas de tu tienda.

![La página Bloques muestra una cuadrícula de bloques existentes](./assets/blocks-workspace.png){width="700" zoomable="yes"}

## Crear un bloque

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. En la esquina superior derecha, haga clic en **Agregar nuevo bloque**.

   ![La página Nuevo bloque muestra opciones y un espacio de contenido](./assets/block-detail.png){width="500" zoomable="yes"}

1. Si desea cambiar el estado habilitado de forma predeterminada del nuevo bloque, establezca **Habilitar bloque** en `No`.

1. Asigne un **Título de bloque** para referencia interna.

1. Asigne un **Identificador** único para el bloque.

   Utilice todos los caracteres en minúsculas con guiones bajos en lugar de espacios.

1. Seleccione cada **[!UICONTROL Store View]** en que desee que el bloque esté disponible.

1. Añada el contenido del bloque con el conjunto de herramientas de contenido mostrado:

   - Si [Page Builder](../page-builder/introduction.md) está habilitado, seleccione **[!UICONTROL Edit with Page Builder]** para usar las herramientas de Page Builder en el contenido [espacio de trabajo](../page-builder/workspace.md).

     ![Espacio de trabajo de Page Builder](./assets/pb-workspace-block.png){width="500" zoomable="yes"}

     >[!NOTE]
     >
     >Para obtener información sobre cómo agregar bloques con Page Builder, consulte [Tutorial 2: Bloques](../page-builder/2-blocks.md).

   - Use el [editor](editor.md) para dar formato al texto, crear vínculos y agregar tablas, imágenes, vídeo y audio.

     Si prefiere trabajar con código HTML, haga clic en **Mostrar / Ocultar editor**.

     ![Editor de bloques (oculto)](./assets/block-editor-hidden.png){width="500" zoomable="yes"}

1. Una vez finalizado, haga clic en la flecha **[!UICONTROL Save]** y elija **[!UICONTROL Save & Close]**.

   El nuevo bloque aparece en la parte inferior de la lista de la cuadrícula Bloques.

1. Usa la herramienta [Widget](widget-static-block.md) para colocar el bloque completado en una página específica de tu tienda.

## Eliminación de un bloque

Existen dos formas de eliminar un bloque personalizado. Puede quitarlo de la cuadrícula _Bloques_ o de la página Editar bloque.

### Método 1: Quitar un bloque de la cuadrícula Bloques

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. Localice los bloques mediante filtros encima de la cuadrícula y marque la casilla de verificación de uno o varios bloques para eliminarlos.
1. En la esquina superior izquierda de la lista, establezca **[!UICONTROL Actions]** en `Delete`.
1. Para confirmar la acción, haga clic en **[!UICONTROL OK]**.

### Método 2: Eliminar un bloque de la página de edición

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. Busque el bloque que desea eliminar.
1. En la columna _Acciones_ del bloque, haga clic en **[!UICONTROL Select]** y elija **[!UICONTROL Edit]**.
1. En la barra de menús, haga clic en **[!UICONTROL Delete Block]**.
1. Para confirmar la acción, haga clic en **[!UICONTROL OK]**.

## Menú Guardar

| Comando | Descripción |
|----------|----------- |
| [!UICONTROL Save] | Guarda el bloque actual y sigue trabajando. |
| [!UICONTROL Save & Duplicate] | Guarde y cierre el bloque actual y abra una nueva copia duplicada. |
| [!UICONTROL Save & Close] | Guarde y cierre el bloque actual y vuelva a la cuadrícula Bloques. |

{style="table-layout:auto"}

## Añadir un lightbox o un control deslizante

- Es fácil agregar un [control deslizante](../page-builder/slider.md) a tu tienda con [[!DNL Page Builder]](../page-builder/introduction.md). El control deslizante puede configurarse para que se reproduzca automáticamente o controlarse manualmente con los botones de navegación.

  ![Regulador de Page Builder](./assets/pb-tutorial3-slider-tee-shirt-promo.png){width="600" zoomable="yes"}

  También hay una amplia variedad de lightboxes de imágenes basados en jQuery disponibles en [[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions.html?q=lightbox), y algunos son gratuitos.

- También puede descargar una extensión desde [!DNL Commerce Marketplace]. Para obtener ayuda adicional, consulte la documentación proporcionada por el desarrollador de la extensión.
