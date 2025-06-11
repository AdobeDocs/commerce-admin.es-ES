---
title: Insertar una imagen en el editor
description: El editor de WYSIWYG permite insertar de forma sencilla una imagen desde el almacenamiento de medios, vincular a una imagen que reside en otro servidor o utilizar recursos de Adobe Stock.
exl-id: 591830c9-6dba-4738-a6e7-cf5f93b3c319
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Insertar una imagen en el editor

Desde el editor, puede insertar una imagen utilizando tres tipos de origen:

- Agregue una imagen que se haya cargado al [almacenamiento de medios](media-storage.md)
- Vínculo a una imagen que reside en otro servidor
- Uso de la integración de Adobe Stock para buscar y utilizar recursos de Adobe Stock

![Almacenamiento de medios](./assets/media-storage.png){width="650" zoomable="yes"}

1. Abra una página, un bloque o un bloque dinámico en modo de edición.

1. Vaya a la sección _[!UICONTROL Content]_&#x200B;y haga clic en cualquier elemento que admita el editor.

1. Coloque el cursor donde desee que aparezca la imagen.

1. En la barra de herramientas del editor, haga clic en el icono _Insertar imagen_.

   ![Icono Insertar imagen](./assets/editor-toolbar-image-button.png){width="700" zoomable="yes"}

   Esta acción abre el diálogo _[!UICONTROL Insert/edit image]_.

1. Para **Source**, haga clic en el icono _Buscar_ y use el método que coincida con la ubicación del recurso de imagen que desea usar:

   ![Seleccionar el icono de búsqueda](./assets/editor-dialog-insert-image.png){width="250" zoomable="yes"}

   - **Cargar una nueva imagen**: use este método para cargar un nuevo archivo de imagen.

      - Seleccione la carpeta del árbol en la que desea añadir el nuevo archivo de imagen.

      - Haga clic en **[!UICONTROL Choose Files]**.

      - Busque y elija el archivo de imagen.

      - Haga clic en la miniatura del nuevo archivo y haga clic en **[!UICONTROL Add Selected]**.

   - **Seleccionar un recurso existente**: utilice este método para seleccionar un recurso de imagen existente del almacenamiento o galería de medios.

      - Utilice el árbol para desplazarse a la imagen.

      - Haga clic en la miniatura y luego en **[!UICONTROL Add Selected]**.

   - **Busque y seleccione una imagen de Adobe Stock**: Utilice este método para encontrar una imagen de Adobe Stock.

     >[!NOTE]
     >
     >Este método requiere una [integración de Adobe Stock](adobe-stock.md) configurada para su administrador.

      - Haga clic en **[!UICONTROL Search Adobe Stock]** y busque una imagen.

      - Guarde la vista previa o la imagen con licencia en la galería.

        Consulte [Uso de imágenes de Adobe Stock](adobe-stock-manage.md) para obtener más información sobre cómo trabajar con recursos de [Adobe Stock](https://stock.adobe.com).

      - Seleccione la miniatura del recurso en la galería y haga clic en **[!UICONTROL Add Selected]**.

1. Para **[!UICONTROL Image Description]**, escriba una breve descripción de la imagen.

1. Escriba la anchura y altura **[!UICONTROL Dimensions]**, en píxeles, para representar la imagen en la página.

   Mantenga la casilla de verificación **[!UICONTROL Constrain proportions]** seleccionada para mantener automáticamente la relación de aspecto de la imagen.

1. Haga clic en **[!UICONTROL Insert]** para completar el proceso.
