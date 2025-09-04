---
title: 'Medios: imagen'
description: Obtenga información acerca del tipo de contenido Imagen, que se usa para agregar una imagen JPG, GIF o PNG al escenario  [!DNL Page Builder] .
exl-id: 1b8d906e-7570-4c1f-87a0-992400faf55c
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '1550'
ht-degree: 0%

---

# Medios: imagen

Utilice el tipo de contenido _Image_ para agregar una imagen JPG, GIF o PNG al [[!DNL Page Builder] escenario](workspace.md#stage). Además de la imagen de escritorio predeterminada, puede especificar una imagen secundaria para dispositivos móviles. También puede añadir un pie de ilustración debajo de la imagen y vincular la imagen a cualquier dirección URL, producto, categoría o página.

>[!TIP]
>
>Puede usar la [integración de Adobe Stock](../content-design/adobe-stock.md) para buscar y guardar un recurso apropiado entre los millones proporcionados por [Adobe Stock](https://stock.adobe.com). Consulte [Uso de imágenes de Adobe Stock](../content-design/adobe-stock-manage.md) para obtener más información sobre cómo buscar, refinar y guardar recursos de Adobe Stock en la galería.

{{$include /help/_includes/page-builder-save-timeout.md}}

## Cuadro de herramientas Imagen

El cuadro de herramientas de imagen aparece cuando pasa el ratón por encima del contenedor de imágenes.

![Cuadro de herramientas de imagen](./assets/pb-media-image-giftcard-column-toolbox.png){width="500" zoomable="yes"}

| Herramienta | Icono | Descripción |
|--- |--- |--- |
| Mover | ![Icono de mover](./assets/pb-icon-move.png){width="25"} | Mueve la imagen a otra posición en el escenario. |
| (etiqueta) | Imagen | Identifica el contenedor de contenido actual como una imagen. Pase el ratón sobre el contenedor de imágenes para ver el cuadro de herramientas. |
| Configuración | ![Icono de configuración](./assets/pb-icon-settings.png){width="25"} | Abre la página _Editar imagen_, donde puede cambiar las propiedades de la imagen y del contenedor. |
| Hide | ![Ocultar icono](./assets/pb-icon-hide.png){width="25"} | Oculta la imagen actual. |
| Mostrar | ![Mostrar icono](./assets/pb-icon-show.png){width="25"} | Muestra la imagen oculta. |
| Duplicar | ![Icono duplicado](./assets/pb-icon-duplicate.png){width="25"} | Realiza una copia de la imagen. |
| Eliminar | ![Quitar icono](./assets/pb-icon-remove.png){width="25"} | Elimina la imagen del escenario. |
| Cargar nueva imagen |  | Carga una imagen desde el sistema de archivos local a la galería. |
| Seleccionar de la galería |  | Elige una imagen existente de la galería. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Añadir una imagen

1. En el panel [!DNL Page Builder], expanda **[!UICONTROL Media]** y arrastre un marcador de posición **[!UICONTROL Image]** al contenedor de destino.

   Puede agregar una imagen a una fila, columna o pestaña. En el ejemplo siguiente, la imagen se arrastra a una columna vacía.

   ![Arrastrando un tipo de contenido de imagen al escenario](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

1. Utilice uno de los siguientes métodos para agregar el recurso de imagen:

   ![Cargar imagen o seleccionar de las herramientas de la Galería en el escenario](./assets/pb-media-image-upload-select.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >El tamaño máximo de archivo es 4 MB. Los tipos de archivo admitidos son JPG, GIF y PNG.

   - _&#x200B;**Cargar una nueva imagen**&#x200B;_: use este método para cargar un nuevo archivo de imagen desde el sistema.

      - Haga clic en **[!UICONTROL Upload Image]**.

      - Busque y elija la imagen para agregarla a la galería y al contenedor de destino.

     Como alternativa, también puede arrastrar un archivo de imagen desde el sistema y soltarlo en el icono _Cámara_ ( ![Icono de cámara](./assets/pb-icon-camera.png){width="20"} ).

   - _&#x200B;**Seleccionar un recurso existente**&#x200B;_: utilice este método para seleccionar un recurso de imagen existente del almacenamiento o galería de medios.

      - Haga clic en **[!UICONTROL Select from Gallery]**.

      - Utilice el árbol para desplazarse a la imagen.

      - Haga clic en la miniatura y luego en **[!UICONTROL Add Selected]**.

        ![Agregando una imagen seleccionada](./assets/pb-media-image-gallery-add-selected.png){width="600" zoomable="yes"}

   - _&#x200B;**Busque y seleccione una imagen de Adobe Stock**&#x200B;_: Utilice este método para encontrar una imagen de Adobe Stock.

     >[!NOTE]
     >
     >Este método requiere una [integración de Adobe Stock](../content-design/adobe-stock.md) configurada para su administrador.

      - Haga clic en **[!UICONTROL Search Adobe Stock]** y busque una imagen.

      - Guarde la vista previa o la imagen con licencia en la galería.

        Consulte [Uso de imágenes de Adobe Stock](../content-design/adobe-stock-manage.md) para obtener más información sobre cómo trabajar con recursos de Adobe Stock.

      - Seleccione la miniatura del recurso en la galería y haga clic en **[!UICONTROL Add Selected]**.

   La imagen aparece en el contenedor de destino en la ubicación del marcador de posición. A diferencia de una imagen de fondo, puede mover la imagen a una posición diferente dentro del contenedor actual o a un contenedor diferente.

   >[!NOTE]
   >
   >Los tipos de contenido [Banner](banner.md) y [Slider](slider.md) también incluyen las opciones _Cargar imagen_ y _Seleccionar de la galería_ para agregar imágenes.

   ![Imagen en una columna](./assets/pb-media-image-column1-giftcard.png){width="500" zoomable="yes"}

## Cambiar configuración de imagen

1. Pase el ratón sobre el contenedor de imágenes para ver el cuadro de herramientas y elija el icono _Configuración_ (![icono Configuración](./assets/pb-icon-settings.png){width="20"} ).
El nombre, las dimensiones y el tamaño del archivo aparecen debajo de la imagen actual.

   ![Imagen actual](./assets/pb-media-image-settings-image.png){width="600" zoomable="yes"}

1. Para cambiar el(la) **[!UICONTROL Image]** actual(a), realice una de las siguientes acciones:

   - _&#x200B;**Cargar una nueva imagen**&#x200B;_: use este método para cargar un nuevo archivo de imagen desde el sistema.

      - Haga clic en **[!UICONTROL Upload Image]**.

      - Busque y elija la imagen para agregarla a la galería y al contenedor de destino.

   - _&#x200B;**Seleccionar un recurso existente**&#x200B;_: utilice este método para seleccionar un recurso de imagen existente del almacenamiento o galería de medios.

      - Haga clic en **[!UICONTROL Select from Gallery]**.

      - Utilice el árbol para desplazarse a la imagen.

      - Haga clic en la miniatura y luego en **[!UICONTROL Add Selected]**.

        ![Agregando una imagen seleccionada](./assets/pb-media-image-gallery-add-selected.png){width="600" zoomable="yes"}

   - **Busque y seleccione una imagen de Adobe Stock**: Utilice este método para encontrar una imagen de Adobe Stock.

     >[!NOTE]
     >
     >Este método requiere una [integración de Adobe Stock](../content-design/adobe-stock.md) configurada para su administrador.

      - Haga clic en **[!UICONTROL Search Adobe Stock]** y busque una imagen.

      - Guarde la vista previa o la imagen con licencia en la galería.

        Consulte [Uso de imágenes de Adobe Stock](../content-design/adobe-stock-manage.md) para obtener más información sobre cómo trabajar con recursos de Adobe Stock.

      - Seleccione la miniatura del recurso en la galería y haga clic en **[!UICONTROL Add Selected]**.

1. Para agregar un(a) **[!UICONTROL Mobile Image]**, utilice los mismos métodos descritos en el paso anterior para seleccionar una imagen que se utilizará para su visualización en dispositivos móviles.

   ![Imagen móvil](./assets/pb-media-image-settings-mobile-image.png){width="600" zoomable="yes"}

1. Si es necesario, especifique un **[!UICONTROL Link]** para la imagen.

   El vínculo es la página de destino que aparece cuando el cliente hace clic en la imagen. Puede utilizar uno de los tres tipos de vínculos:

   - **[!UICONTROL URL]**: vínculos a una dirección URL relativa o completa.

   - **[!UICONTROL Product]**: identifica la página de destino según el nombre o el SKU del producto. Busque el producto por nombre en función de un nombre parcial o completo. Elija el producto de la lista de resultados de búsqueda.

     ![Elegir un producto para vincular](./assets/pb-media-image-settings-image-link-product-results.png){width="600" zoomable="yes"}

   - **[!UICONTROL Category]** - Identifica la página de destino como una categoría o subcategoría específica en el árbol de categorías. Busque la categoría en función de un nombre parcial o completo. Elija la categoría de la sección expandida del árbol mostrado.

     ![Elegir una categoría para vincular](./assets/pb-media-image-settings-image-link-category-tree.png){width="600" zoomable="yes"}

   - **[!UICONTROL Page]** - Identifica la página de destino como una página de contenido específica. Busque la página en función de un nombre parcial o completo. Elija la página en la lista de resultados de la búsqueda.

     ![Elegir una página para vincular](./assets/pb-media-image-settings-image-link-page-results.png){width="600" zoomable="yes"}

   Si desea evitar que el visitante salga de su tienda, active la casilla de verificación **[!UICONTROL Open in new tab]**. Cuando se desactiva la casilla de verificación, el destino vinculado se abre en la misma pestaña del explorador, lo que podría sacar al visitante de la tienda.

1. Para agregar un **[!UICONTROL Image Caption]**, escriba el texto que desea que aparezca debajo de la imagen.

   El formato del pie de ilustración viene determinado por la hoja de estilo asociada a la temática actual.

   El pie de ilustración suele aparecer debajo de la imagen y proporciona información sobre la imagen para visitantes y motores de búsqueda. Si el sitio está disponible en varios idiomas, puede utilizar la misma imagen, pero traducir el pie de ilustración. En HTML, la etiqueta `<figcaption>` es un subconjunto de la etiqueta `<figure>`. `<figcaption>This is the image caption</figcaption>`

1. Actualice cualquiera de las otras opciones según sea necesario:

   - [Optimización del motor de búsqueda](#search-engine-optimization)
   - [Avanzadas](#advanced)

1. Una vez finalizado, haga clic en **[!UICONTROL Save]** para aplicar la configuración y volver al área de trabajo [!DNL Page Builder].

## Mover una imagen

1. Pase el ratón sobre el contenedor de imágenes para ver la caja de herramientas y elija el icono _Mover_ (![Icono Mover](./assets/pb-icon-move.png){width="20"}).

   ![Moviendo una imagen](./assets/pb-media-image-column1-move-giftcard.png){width="500" zoomable="yes"}

1. Seleccione y arrastre la imagen a la nueva posición, justo debajo de la guía roja.

   ![Utilizando la guía roja para colocar la imagen](./assets/pb-media-image-column2-move-giftcard-red-guideline.png){width="500" zoomable="yes"}

## Eliminar una imagen

1. Pase el ratón sobre el contenedor de imágenes para mostrar la caja de herramientas y elija el icono _Quitar_ ( ![Quitar icono](./assets/pb-icon-remove.png){width="20"} ).

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL OK]**.

## Optimización del motor de búsqueda

El texto de esta configuración es visible para los motores de búsqueda y mejora la forma en que se indexa la página.

- Para **[!UICONTROL Alternative Text]**, escriba una descripción de texto de _alt_ para que se muestren las herramientas de accesibilidad digital.

  El uso de texto alternativo es una práctica recomendada de accesibilidad y es obligatorio por ley en algunas configuraciones regionales. En HTML, el atributo `alt` es un subconjunto de la etiqueta `image`: `<image title="tooltip" alt="description" src="image.jpg">`.

- Para **[!UICONTROL Title Attribute]**, escriba el texto que se mostrará como información sobre herramientas al pasar el ratón por encima.

  Como práctica recomendada, elija un título descriptivo y con muchas palabras clave para mejorar la forma en que los motores de búsqueda indexan la imagen. En HTML, el atributo `title` es un subconjunto de la etiqueta `image`: `<image title="tooltip" alt="description" src="image.jpg">`.

## [!UICONTROL Advanced]

- Para controlar la posición horizontal de las imágenes agregadas al contenedor, elija un **[!UICONTROL Alignment]**.

  | Opción | Descripción |
  | ------ | ----------- |
  | `Default` | Aplica la configuración predeterminada de alineación especificada en la hoja de estilos de la temática actual. |
  | `Left` | Alinea el contenido de la imagen a lo largo del borde izquierdo del contenedor de imágenes, con margen para cualquier relleno que se especifique. |
  | `Center` | Alinea el contenido de la imagen en el centro del contenedor de imágenes, con margen para cualquier relleno que se especifique. |
  | `Right` | Alinea el contenido de la imagen a lo largo del borde derecho del contenedor de imágenes, con margen para cualquier relleno que se especifique. |

  {style="table-layout:auto"}

- Establezca el estilo **[!UICONTROL Border]** aplicado a los cuatro lados del contenedor de imágenes:

  | Opción | Descripción |
  | ------ | ----------- |
  | `Default` | Aplica el estilo de borde predeterminado especificado por la hoja de estilos asociada. |
  | `None` | No proporciona ninguna indicación visible de los bordes del contenedor. |
  | `Dotted` | El borde del contenedor aparece como una línea de puntos. |
  | `Dashed` | El borde del contenedor aparece como una línea discontinua. |
  | `Solid` | El borde del contenedor aparece como una línea sólida. |
  | `Double` | El borde del contenedor aparece como una línea doble. |
  | `Groove` | El borde del contenedor aparece como una línea ranurada. |
  | `Ridge` | El borde del contenedor aparece como una línea discontinua. |
  | `Inset` | El borde del contenedor aparece como una línea de margen. |
  | `Outset` | El borde del contenedor aparece como una línea de inicio. |

  {style="table-layout:auto"}

- Si establece un estilo de borde distinto de `None`, complete las opciones de visualización de borde:

  ![Color del borde](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

  | Opción | Descripción |
  | ------ |------------ |
  | [!UICONTROL Border Color] | Especifique el color seleccionando una muestra, haciendo clic en el selector de color o introduciendo un nombre de color válido o un valor hexadecimal equivalente. |
  | [!UICONTROL Border Width] | Introduzca el número de píxeles de la anchura de la línea del borde. |
  | [!UICONTROL Border Radius] | Introduzca el número de píxeles para definir el tamaño del radio que se utiliza para redondear cada esquina del borde. |

  {style="table-layout:auto"}

- (Opcional) Especifique los nombres de **[!UICONTROL CSS classes]** de la hoja de estilos actual para aplicarlos al contenedor de imágenes.

  Separe los distintos nombres de clase con un espacio.

- Escriba valores, en píxeles, para que **[!UICONTROL Margins and Padding]** especifique los márgenes externos y el relleno interno del contenedor de imágenes.

  Introduzca cada valor correspondiente en el diagrama del contenedor de imágenes.

  | Área del contenedor | Descripción |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | Cantidad de espacio en blanco que se aplica al borde exterior de todos los lados del contenedor. |
  | [!UICONTROL Padding] | Cantidad de espacio en blanco que se aplica al borde interior de todos los lados del contenedor. |

  {style="table-layout:auto"}

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
