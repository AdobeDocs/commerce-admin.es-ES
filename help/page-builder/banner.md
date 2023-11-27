---
title: 'Medios: titular'
description: Obtenga información acerca del tipo de contenido de titular utilizado para agregar un componente interactivo ilustrado en la [!DNL Page Builder] escenario.
exl-id: 287d866c-8a63-4531-8c1b-40d560a07947
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '2300'
ht-degree: 0%

---

# Medios: titular

Utilice el _Titular_ tipo de contenido para añadir un componente interactivo e ilustrado que involucre a los usuarios con una llamada a la acción y un botón en el [[!DNL Page Builder] stage](workspace.md#stage).

>[!NOTE]
>
>¿Qué era antes el _Titular_ en el menú Contenido, ahora es [Bloque dinámico](../content-design/dynamic-blocks.md).

![Titular de la página principal de una tienda](./assets/pb-banner-homepage.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Cuadro de herramientas Banner

El cuadro de herramientas del titular aparece cuando pasa el ratón por encima del contenedor del titular.

![Cuadro de herramientas Banner](./assets/pb-tutorial1-banner-toolbox.png){width="600" zoomable="yes"}

| Herramienta | Icono | Descripción |
|--- |--- |--- |
| Mover | ![Icono Mover](./assets/pb-icon-move.png){width="25"} | Mueve el titular a otra posición en el escenario. |
| (etiqueta) | Titular | Identifica el contenedor de contenido actual como un banner. Pase el ratón sobre el contenedor para ver la caja de herramientas. |
| Configuración | ![Icono de configuración](./assets/pb-icon-settings.png){width="25"} | Abre la página Editar titular, donde puede cambiar las propiedades del titular y del contenedor. |
| Hide | ![Icono Ocultar](./assets/pb-icon-hide.png){width="25"} | Oculta el titular actual. |
| Mostrar | ![Mostrar icono](./assets/pb-icon-show.png){width="25"} | Muestra el banner oculto. |
| Duplicar | ![Icono Duplicar](./assets/pb-icon-duplicate.png){width="25"} | Realiza una copia del titular. |
| Eliminar | ![Icono Eliminar](./assets/pb-icon-remove.png){width="25"} | Elimina el titular del escenario. |
| [!UICONTROL Upload New Image] |  | Carga una imagen del sistema de archivos local en la galería para el fondo del titular. |
| [!UICONTROL Select from Gallery] |  | Utiliza una imagen existente de la galería para el fondo del titular. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Añadir un titular

1. En el [!DNL Page Builder] panel, expandir **[!UICONTROL Media]** y arrastre un **[!UICONTROL Banner]** marcador de posición al escenario.

   ![Arrastrar un tipo de contenido de banner al escenario](./assets/pb-tutorial1-banner-drag-to-stage.png){width="600" zoomable="yes"}

   El _[!UICONTROL Upload Image]_y_[!UICONTROL Select from Gallery]_ se incluyen botones para que pueda realizar cambios rápidos en el contenido del titular directamente desde el escenario. También puede cambiar el contenido en la _[!UICONTROL Edit Banner]_página.

1. Haga clic en el marcador de posición del titular para mostrar el [editor de texto](../content-design/editor.md) e introduzca el contenido del titular.

   También puede incluir contenido de titular más complejo mediante el [Contenido](#content) configuración.

## Cambiar configuración del banner

1. Pase el ratón sobre el contenedor del titular para mostrar el cuadro de herramientas y elegir _Configuración_ (![Icono de configuración](./assets/pb-icon-settings.png)) icono.

1. Utilice las secciones siguientes para obtener información detallada sobre la actualización de la configuración disponible:

   - [[!UICONTROL Appearance]](#appearance)
   - [[!UICONTROL Content]](#content)
   - [[!UICONTROL Background]](#background)
   - [[!UICONTROL Advanced]](#advanced)

1. Cuando termine, haga clic en **[!UICONTROL Save]** en la esquina superior derecha para cerrar el _[!UICONTROL Edit Banner]_página.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Save]** para aplicar la configuración de y volver a [!DNL Page Builder] workspace.

## [!UICONTROL Appearance]

Los titulares son fáciles de configurar y mantener, ya que se basan en una de las cuatro plantillas predefinidas.

- Elija uno de los siguientes tipos de colocación de banner:

  | Ubicación | Descripción |
  | --------- | ----------- |
  | [!UICONTROL Poster] | Centra el contenido y el botón en el titular. Si se utiliza, la superposición amplía la anchura completa del titular. |
  | [!UICONTROL Collage Left] | Coloca el contenido y el botón en un área definida en el lado izquierdo del banner. Si se utiliza la superposición, solo se cubre el área definida. |
  | [!UICONTROL Collage Center] | Coloca el contenido y el botón en un área definida centrada en el titular. Si se utiliza la superposición, solo se cubre el área definida. |
  | [!UICONTROL Collage Right] | Coloca el contenido y el botón en un área definida en el lado derecho del banner. Si se utiliza la superposición, solo se cubre el área definida. |

  {style="table-layout:auto"}

  ![Apariencia - collage derecho](./assets/pb-tutorial1-row-banner-settings-appearance-collage-right.png){width="600" zoomable="yes"}

- (Opcional) Introduzca el **[!UICONTROL Minimum Height]** para la fila.

  La altura mínima puede ser un número con cualquier unidad CSS válida (como `100px`, `50%`, `50em`, `100vh`) o un cálculo (como `100vh - 237px`).

  Por ejemplo, puede establecer la altura mínima de un banner para ampliar la altura completa de la página, lo que le ofrece opciones atractivas para imágenes y vídeos de fondo de página completa.

## [!UICONTROL Background]

Existen muchas opciones para definir la visualización de fondo de un titular. Puede aplicar un color simple o una imagen de fondo, y administrar efectos más sofisticados.

### [!UICONTROL Background Color]

Especifique el color de fondo eligiendo una muestra, haciendo clic en el selector de color o introduciendo un nombre de color válido o un valor hexadecimal equivalente. Esta configuración determina el color de fondo de la fila. También puede ajustar la opacidad del color.

![Sin color (predeterminado)](./assets/pb-settings-background-color-no-color.png){width="200"}

Puede establecer el valor de una de las tres maneras siguientes:

- Un nombre de color predefinido, como `White`
- El valor hexadecimal del color, como `#ffffff`
- El valor de rgba para el color, con un porcentaje de opacidad, como `rgba(255, 255, 255, 0.75)`

Si desea elegir un color, haga clic en la muestra a la izquierda del _Sin color_ cuadro.

![Selección de una muestra de color](./assets/pb-settings-background-color-picker-swatch.png){width="600" zoomable="yes"}

Si hace clic en el cuadro de color para abrir de nuevo el selector de color, el cuadro situado debajo del control deslizante mostrará los valores actuales de rojo, verde, azul y alfa (rgba). El último número indica el porcentaje de opacidad actual como decimal. Puede utilizar el control deslizante para ajustar la opacidad o introducir el valor decimal deseado.

![Configuración de opacidad](./assets/pb-settings-background-color.png){width="600" zoomable="yes"}

>[!NOTE]
>
>[!DNL Page Builder] también admite una capa de transparencia, o _canal alfa_, en imágenes de fondo que pueden utilizarse para crear fondos con distintos grados de opacidad.

### [!UICONTROL Background Type]

Un tipo de fondo puede ser una imagen o un vídeo. [!DNL Page Builder] el valor predeterminado es `Image` y muestra varios ajustes de imagen. Si selecciona `Video`, [!DNL Page Builder] cambia la configuración de la imagen por la configuración del vídeo. Ambas configuraciones de tipo de fondo se describen en las secciones siguientes.

![Tipo de fondo](./assets/pb-background-type.png){width="200"}

### Configuración del tipo de imagen

Si establece la variable _Tipo de fondo_ hasta `Image`, utilice la siguiente configuración para definir la visualización de la imagen de fondo.

![Titular con imagen de fondo](./assets/pb-tutorial1-banner-background.png){width="600" zoomable="yes"}

- **[!UICONTROL Background Image]** - Si es necesario, utilice las herramientas proporcionadas para elegir una imagen de fondo para aplicarla al titular:

  | Herramienta | Descripción |
  | ---- | ----------- |
  | [!UICONTROL Upload] | Carga un archivo de imagen desde el equipo local a la galería y, a continuación, lo aplica como imagen de fondo para el titular. |
  | [!UICONTROL Select from Gallery] | Le pide que elija una imagen existente de la galería como imagen de fondo para el titular. |
  | ![Icono de cámara](./assets/pb-icon-camera.png){width="25"} | Permite arrastrar la imagen al mosaico de la cámara o navegar a la imagen en el sistema de archivos local. |

  {style="table-layout:auto"}

- **[!UICONTROL Background Mobile Image]** : Si es necesario, utilice las mismas herramientas para elegir una imagen de fondo diferente para utilizarla en la visualización en dispositivos móviles.

- **[!UICONTROL Background Size]** - Establezca esta opción para determinar cómo se escala la imagen de fondo en relación con la anchura del titular:

  | Opción | Descripción |
  | ------ | ----------- |
  | `Cover` | La imagen de fondo cubre la anchura completa del titular. |
  | `Contain` | La imagen de fondo está limitada a la anchura del área de contenido. |
  | `Auto` | Aplica el tamaño de la hoja de estilos actual. |

  {style="table-layout:auto"}

  ![Tamaño de fondo](./assets/pb-layout-row-settings-background-size-cover.png){width="200"}

- **[!UICONTROL Background Position]** - Establezca esta opción para determinar cómo se ancla la imagen de fondo en relación con el titular:

  | Anclaje | Posiciones |
  | ------ | ----------- |
  | `Top` | Izquierda/Centro/Derecha |
  | `Center` | Izquierda/Centro/Derecha |
  | `Bottom` | Izquierda/Centro/Derecha |

  {style="table-layout:auto"}

  El punto de ancla es como un pin de inserción que adjunta la imagen al titular en la posición de fondo especificada.

- **[!UICONTROL Background Attachment]** - Establezca el tipo de archivo adjunto para determinar cómo se mueve la imagen de fondo en relación con la página de desplazamiento:

  | Opción | Descripción |
  | ------ | ----------- |
  | `Scroll` | La imagen de fondo adjunta se sincroniza para moverse hacia abajo a medida que la página se desplaza. |
  | `Fixed` | (No disponible para móviles) La imagen de fondo no se mueve cuando el contenedor se desplaza por la imagen y está fijo en la posición de fondo especificada. |

  {style="table-layout:auto"}

- **[!UICONTROL Background Repeat]** - Si desea repetir la imagen de fondo para rellenar el espacio, cambie este ajuste `Yes`.

### Configuración del tipo de vídeo

Si establece la variable _[!UICONTROL Background Type]_hasta `Video`, utilice la siguiente configuración para definir la visualización de la imagen de fondo.

- **[!UICONTROL Video URL]** : introduzca una URL de vídeo válida. Las direcciones URL de vídeo válidas pueden ser vínculos a:

   - Vídeos de YouTube: `https://youtu.be/CoDhMRUUjeI`
   - Vídeos de Vimeo: `https://vimeo.com/190156113`
   - Archivos de vídeo válidos (`.mp4` se recomienda): `https://myvideos.com/spiral.mp4`

  ![URL de vídeo de fondo](./assets/pb-video-url.png){width="200"}

- **[!UICONTROL Overlay Color]** - Seleccione un color para aplicar un tinte transparente al vídeo.

- **[!UICONTROL Infinite Loop]** - Configurado como `No` para que el vídeo se reproduzca una vez y se detenga. Cuando se establece en `Yes` (valor predeterminado), el vídeo se repite en un bucle infinito.

- **[!UICONTROL Lazy Load]** - Configurado como `No` para que el vídeo se cargue con la página, incluso cuando no esté visible. Cuando se establece en `Yes` (opción predeterminada), el vídeo se carga desde el origen solo cuando está visible en la pantalla.

- **[!UICONTROL Play Only When Visible]** - Configurado como `No` para que el vídeo comience a reproducirse inmediatamente después de cargarse, independientemente de si está visible. Cuando se establece en `Yes` (opción predeterminada), el vídeo solo se reproducirá cuando esté visible.

- **[!UICONTROL Fallback Image]** - Si es necesario, especifique una imagen para mostrar en la pantalla antes de que se cargue el vídeo y si el vídeo no se carga por alguna razón.

## [!UICONTROL Content]

Puede modificar el contenido del titular directamente en el escenario o al cambiar la configuración. La configuración proporciona funciones de contenido más complejas, como vínculos y botones de banner y superposiciones. La posición del contenido refleja el [Aspecto](#appearance) configuración de ubicación.

### Contenido sencillo en el escenario

1. Haga clic en el texto del marcador de posición e introduzca el texto que desee que aparezca en el titular.

   La barra de herramientas del editor aparece encima del cuadro de texto.

   ![Editar contenido en el escenario](./assets/pb-tutorial1-banner-stage-text.png){width="600" zoomable="yes"}

1. Utilice la barra de herramientas del editor para introducir y dar formato al texto, así como para insertar elementos como vínculos, imágenes y widgets.

   ![Escenario con texto con formato](./assets/pb-tutorial1-banner-stage-text-format-line2.png){width="600" zoomable="yes"}

### Contenido complejo en la configuración

1. Pase el ratón sobre el contenedor del titular para mostrar el cuadro de herramientas y elegir _Configuración_ ( ![Icono de configuración](./assets/pb-icon-settings.png){width="25"} ) icono.

1. Desplácese hacia abajo hasta el _[!UICONTROL Content]_y utilice la sección **[!UICONTROL Message Text]**editor para introducir y dar formato al texto del banner.

   También puede insertar elementos, como vínculos de texto, imágenes y widgets.

   ![Editor de texto de mensaje](./assets/pb-tutorial1-banner-settings-content-message-text.png){width="600" zoomable="yes"}

1. Si es necesario, especifique un **[!UICONTROL Link]** para el titular.

   El vínculo es la página de destino que aparece cuando el cliente hace clic en el área o el botón del titular. Puede utilizar uno de los tres tipos de vínculos:

   - **[!UICONTROL URL]** : Vínculos a una dirección URL relativa o completa.
   - **[!UICONTROL Product]** : identifica la página de destino según el nombre del producto o el SKU. Busque el producto por nombre en función de un nombre parcial o completo. Elija el producto de la lista de resultados de búsqueda.
   - **[!UICONTROL Category]** : identifica la página de destino como una categoría o subcategoría específica en el árbol de categorías. Busque la categoría en función de un nombre parcial o completo. Elija la categoría de la sección expandida del árbol mostrado.
   - **[!UICONTROL Page]** : identifica la página de destino como una página de contenido específica. Busque la página en función de un nombre parcial o completo. Elija la página en la lista de resultados de la búsqueda.

   >[!NOTE]
   >
   >A partir de la versión 2.4.1, [!DNL Page Builder] ya no admite la vinculación del titular y los vínculos dentro del texto anidado debido a problemas con la visualización en la tienda. Si utiliza un vínculo en la _[!UICONTROL Message Text]_, no se puede configurar el_[!UICONTROL Link]_ opción. Si prefiere utilizar un solo vínculo para todo el titular, puede quitar todos los vínculos del texto.<br/>
   >
   >![Configuración de vínculo bloqueada](./assets/pb-nested-link-blocked.png){width="200"}


1. Si es necesario, agregue un botón para pedir a los clientes que sigan el vínculo.

   La configuración del aspecto del banner coloca un solo vínculo o botón debajo del texto. Complete las propiedades del vínculo o del botón que desee agregar.

   ![Apariencia con texto y botón (o vínculo)](./assets/pb-tutorial1-row-banner-settings-appearance-collage-right.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >También puede utilizar varios botones o vínculos añadiendo una [bloquear](block.md) al titular. Para evitar conflictos, mantenga todos los vínculos o botones en el bloque independiente y no agregue un vínculo o botón directamente al titular.

   - Establecer **[!UICONTROL Show Button]** a uno de los siguientes:

     | Opción | Descripción |
     | ------ | ----------- |
     | `Always` | Siempre aparece un botón en el titular. |
     | `On Hover` | Un botón aparece en el titular solo al pasar el ratón por encima. |
     | `Never Show` | Nunca aparece un botón en el titular. |

     {style="table-layout:auto"}

   - Introduzca el **[!UICONTROL Button Text]** para que aparezca en el botón.

   - Establecer **[!UICONTROL Button Type]** a uno de los siguientes:

     | Opción | Descripción |
     | ------ | ----------- |
     | `Primary` | Aplica el estilo del botón principal de la hoja de estilos actual. |
     | `Secondary` | Aplica el estilo del botón secundario de la hoja de estilos actual, si corresponde. |
     | `Link` | Crea un hipervínculo en lugar de un botón. |

     {style="table-layout:auto"}

     El estilo de botón del tema actual determina el formato del botón. Normalmente, un botón principal tiene un color de fondo más prominente que un botón secundario.

1. Establecer **[!UICONTROL Show Overlay]** a uno de los siguientes:

   | Opción | Descripción |
   | ------ | ----------- |
   | `Always` | La superposición siempre es visible. |
   | `On Hover` | La superposición solo aparece al pasar el ratón por encima. |
   | `Never Show` | La superposición no es visible. |

   {style="table-layout:auto"}

   Puede utilizar una superposición para aplicar un color de fondo al área de contenido activo definida por el [!UICONTROL Appearance] configuración. La imagen de fondo del titular permanece visible durante todo el ancho del titular.

   Si elige mostrar una superposición, configure el **[!UICONTROL Overlay Color]**:

   - Haga clic en **Sin color** muestra y elija una muestra.
   - En el **Sin color** , introduzca un nombre de color válido o un valor hexadecimal.

   ![Color de superposición](./assets/pb-tutorial1-banner-settings-overlay-color.png){width="600" zoomable="yes"}

1. En la esquina superior derecha, haga clic en **[!UICONTROL Save]** para aplicar la configuración de y volver a [!DNL Page Builder] workspace.

   ![Titular con mensaje de texto y botón](./assets/pb-tutorial1-banner-stage-background-color.png){width="600" zoomable="yes"}


## [!UICONTROL Search Engine Optimization] {#seo}

El texto de esta configuración es visible para los motores de búsqueda y mejora la forma en que se indexa la página.

- Para **[!UICONTROL Alternative Text]**, introduzca un _alt_ descripción de texto de las herramientas de accesibilidad digital para mostrar.

  El uso de texto alternativo es una práctica recomendada de accesibilidad y es obligatorio por ley en algunas configuraciones regionales. En HTML, la variable `alt` es un subconjunto del atributo `image` etiqueta: `<image title="tooltip" alt="description" src="image.jpg">`.

- Para **[!UICONTROL Title Attribute]**, introduzca el texto que se mostrará como información sobre herramientas al pasar el ratón por encima.

  Como práctica recomendada, elija un título descriptivo y con muchas palabras clave para mejorar la forma en que los motores de búsqueda indexan la imagen. En HTML, la variable `title` es un subconjunto del atributo `image` etiqueta: `<image title="tooltip" alt="description" src="image.jpg">`.

## [!UICONTROL Advanced]

1. Para controlar la colocación horizontal de los contenedores de contenido que se añaden al titular, elija un **[!UICONTROL Alignment]**:

   | Opción | Descripción |
   | ------ | ----------- |
   | `Default` | Aplica la configuración predeterminada de alineación especificada en la hoja de estilos de la temática actual. |
   | `Left` | Alinea los contenedores de contenido a lo largo del borde izquierdo del contenedor de banner, con margen para cualquier relleno que se especifique. |
   | `Center` | Alinea el contenedor de contenido en el centro del contenedor de banner, con margen para cualquier relleno que se especifique. |
   | `Right` | Alinea el contenedor de contenido a lo largo del borde derecho del contenedor de banner, con margen para cualquier relleno que se especifique. |

   {style="table-layout:auto"}

1. Configure las variables **[!UICONTROL Border]** estilo aplicado a los cuatro lados del contenedor de banner:

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

1. Si establece un estilo de borde distinto de `None`, complete las opciones de visualización de bordes:

   - **[!UICONTROL Border Color]** - Especifique el color seleccionando una muestra, haciendo clic en el selector de color o introduciendo un nombre de color válido o un valor hexadecimal equivalente.

     ![Color del borde](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

   - **[!UICONTROL Border Width]** : introduzca el número de píxeles para la anchura de la línea del borde.

   - **[!UICONTROL Border Radius]** : introduzca el número de píxeles para definir el tamaño del radio que se utiliza para redondear cada esquina del borde.

1. (Opcional) Especifique los nombres de **[!UICONTROL CSS classes]** de la hoja de estilo actual para aplicarla al contenedor de banner.

   Separe los distintos nombres de clase con un espacio.

1. Introduzca valores, en píxeles, para **[!UICONTROL Margins and Padding]** para especificar los márgenes exteriores y el relleno interno del titular.

   Introduzca cada valor correspondiente en el diagrama del contenedor de banner.

   | Opción | Descripción |
   | ------ | ----------- |
   | [!UICONTROL Margins] | Cantidad de espacio en blanco que se aplica al borde exterior de todos los lados del contenedor. |
   | [!UICONTROL Padding] | Cantidad de espacio en blanco que se aplica al borde interior de todos los lados del contenedor. |

   {style="table-layout:auto"}
