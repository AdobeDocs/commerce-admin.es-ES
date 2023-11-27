---
title: Diseño - Fila
description: Obtenga información acerca del tipo de contenido Fila, utilizado para agregar una fila en la [!DNL Page Builder] escenario.
exl-id: 0aa8bf6f-7ae3-4718-9f76-430ed63ba05c
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '1618'
ht-degree: 0%

---

# Diseño - Fila

Utilice el _Fila_ tipo de contenido al que agregar una fila en [[!DNL Page Builder] stage](workspace.md#stage).

{{$include /help/_includes/page-builder-save-timeout.md}}

## Cuadro de herramientas Fila

El cuadro de herramientas de fila aparece cuando pasa el ratón por encima del contenedor de filas. El cuadro de herramientas incluye opciones para mover, ocultar, duplicar, editar o quitar la fila. La selección de la configuración determina el aspecto, el fondo y el diseño de la fila. Se pueden arrastrar elementos de contenido adicionales a la fila desde el [!DNL Page Builder] panel de la izquierda.

![Cuadro de herramientas Fila](./assets/pb-layout-page-add-content-row-tools.png){width="600" zoomable="yes"}

| Herramienta | Icono | Descripción |
| --------- | ---------- | ----------- |
| Mover | ![Icono Mover](./assets/pb-icon-move.png){width="25"} | Mueve la fila a otra posición en relación con otras filas del escenario. |
| (etiqueta) | [!UICONTROL Row] | Identifica el contenedor de contenido actual como una fila. Pase el ratón sobre el contenedor para ver la caja de herramientas. |
| Configuración | ![Icono de configuración](./assets/pb-icon-settings.png){width="25"} | Abre la página Editar fila, donde puede cambiar las propiedades del contenedor. |
| Hide | ![Icono Ocultar](./assets/pb-icon-hide.png){width="25"} | Oculta la fila actual. |
| Mostrar | ![Mostrar icono](./assets/pb-icon-show.png){width="25"} | Muestra la fila oculta. |
| Duplicar | ![Icono Duplicar](./assets/pb-icon-duplicate.png){width="25"} | Realiza una copia de la fila. |
| Eliminar | ![Icono Eliminar](./assets/pb-icon-remove.png){width="25"} | Elimina el contenedor de filas y su contenido de la fase. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Añadir una fila

1. En el [!DNL Page Builder] panel debajo de _[!UICONTROL Layout]_, arrastre un nuevo **[!UICONTROL Row]**al escenario, justo debajo de la primera fila.

1. Para dar formato a la fila, pase el ratón sobre el contenedor de filas para mostrar el cuadro de herramientas y seleccione _Configuración_ ( ![Icono de configuración](./assets/pb-icon-settings.png){width="20"} ) icono.

   Utilice las secciones siguientes para obtener información detallada sobre cómo completar la configuración disponible.

   ![Adición de una fila](./assets/pb-layout-row-add.png){width="600" zoomable="yes"}

## Cambiar configuración de fila

1. Pase el ratón sobre el contenedor de filas para mostrar el cuadro de herramientas y elegir _Configuración_ ( ![Icono de configuración](./assets/pb-icon-settings.png){width="20"} ) icono.

   ![Cuadro de herramientas Fila](./assets/pb-tutorial1-row-toolbox.png){width="600" zoomable="yes"}

1. Utilice las secciones siguientes para obtener información detallada sobre la actualización de la configuración disponible.

1. Cuando termine, haga clic en **[!UICONTROL Save]** para aplicar la configuración de y volver a [!DNL Page Builder] workspace.

## Aspecto

Utilice el _Aspecto_ configuración para determinar cómo se muestra el contenido en la fila.

![Configuración de aspecto](./assets/pb-row-layout.png){width="600" zoomable="yes"}

- Para determinar cómo aparece el color de fondo o la imagen de fondo en relación con el contenedor y la anchura del área de contenido, elija la alineación:

  | Opción | Descripción |
  | ------ | ----------- |
  | [!UICONTROL Contained] | El color de fondo o la imagen están limitados al ancho de página máximo definido por la temática. |
  | [!UICONTROL Full Width] | Limita el contenido al ancho de página máximo definido por la temática. El color de fondo o la imagen no están limitados y amplían el ancho completo de la fila. |
  | [!UICONTROL Full Bleed] | El contenido, la imagen de fondo o el color no están limitados y amplían el ancho completo de la fila. El sangrado completo solo se puede utilizar con [temas](../content-design/themes.md) que admiten el diseño. |

  {style="table-layout:auto"}

- Introduzca el **[!UICONTROL Minimum Height]** para la fila. Este valor puede ser un número con cualquier unidad CSS válida (como `100px`, `50%`, `50em`, `100vh`) o un cálculo (como `100vh - 237px`).

  Por ejemplo, puede establecer la altura mínima de una fila para ampliar la altura completa de la página, lo que le ofrece opciones atractivas para imágenes y vídeos de fondo de página completa.

- Elija una **[!UICONTROL Vertical Alignment]** para alinear cualquier contenedor de contenido que se añada a la fila (Superior, Centro o Inferior).

## Contexto

Existen muchas opciones para definir la visualización de fondo de una fila. Puede aplicar un color simple o una imagen de fondo, y administrar efectos más sofisticados.

### Color de fondo

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

Un tipo de fondo puede ser una imagen o un vídeo. [!DNL Page Builder] el valor predeterminado es `Image` y muestra varios ajustes de imagen. Si selecciona `Video`, [!DNL Page Builder] cambia la configuración de la imagen por la configuración del vídeo. Ambos tipos de fondo se describen de la siguiente manera.

![Tipo de fondo](./assets/pb-background-type.png){width="200"}

### Configuración del tipo de imagen

Si establece la variable _[!UICONTROL Background Type]_hasta `Image`, utilice la siguiente configuración para definir la visualización de la imagen de fondo.

![Imagen de fondo](./assets/pb-tutorial1-row-settings-background-image-selected.png){width="600" zoomable="yes"}

- **[!UICONTROL Background Image]** - Si es necesario, utilice las herramientas proporcionadas para elegir una imagen de fondo para aplicarla a la fila:

  | Opción | Descripción |
  | ------ | ----------- |
  | [!UICONTROL Upload] | Carga un archivo de imagen desde el equipo local a la galería y, a continuación, lo aplica como imagen de fondo de la fila. |
  | [!UICONTROL Select from Gallery] | Le pide que elija una imagen existente de la galería como imagen de fondo para la fila. |
  | ![Icono de cámara](./assets/pb-icon-camera.png){width="25"} | Permite arrastrar la imagen al mosaico de la cámara o navegar a la imagen en el sistema de archivos local. |

  {style="table-layout:auto"}

- **[!UICONTROL Background Mobile Image]** : Si es necesario, utilice las mismas herramientas para elegir una imagen de fondo diferente para utilizarla en la visualización en dispositivos móviles.

- **[!UICONTROL Background Size]** - Establezca esta opción para determinar cómo se escala la imagen de fondo en relación con la anchura de la fila:

  | Opción | Descripción |
  | ------ | ----------- |
  | `Cover` | La imagen de fondo cubre el ancho completo de la fila. |
  | `Contain` | La imagen de fondo está limitada a la anchura del área de contenido. |
  | `Auto` | Aplica el tamaño de la hoja de estilos actual. |

  {style="table-layout:auto"}

  ![Tamaño de fondo](./assets/pb-layout-row-settings-background-size-cover.png){width="250"}

- **[!UICONTROL Background Position]** - Establezca esta opción para determinar cómo se ancla la imagen de fondo en relación con la fila:

  | Punto de ancla | Posición |
  | ------ | ----------- |
  | `Top` | Izquierda/Centro/Derecha |
  | `Center` | Izquierda/Centro/Derecha |
  | `Bottom` | Izquierda/Centro/Derecha |

  {style="table-layout:auto"}

  El punto de ancla es como un pin de inserción que adjunta la imagen a la fila en la posición de fondo especificada.

- **[!UICONTROL Background Attachment]** - Establezca el tipo de archivo adjunto para determinar cómo se mueve la imagen de fondo en relación con la página de desplazamiento:

  | Opción | Descripción |
  | ------ | ----------- |
  | `Scroll` | La imagen de fondo adjunta se sincroniza para moverse hacia abajo a medida que la página se desplaza. Utilice Fondo paralaje para controlar la velocidad de desplazamiento. |
  | `Fixed` | (No disponible para móviles) La imagen de fondo no se mueve cuando el contenedor se desplaza por la imagen y está fijo en la posición de fondo especificada. |

  {style="table-layout:auto"}

- **[!UICONTROL Background Repeat]** - Configurado como `Yes` para repetir la imagen de fondo y rellenar el espacio disponible en la fila.

### Configuración del tipo de vídeo

Si establece la variable _Tipo de fondo_ hasta `Video`, utilice la siguiente configuración para definir la visualización de la imagen de fondo.

- **[!UICONTROL Video URL]** : introduzca una URL de vídeo válida. Las direcciones URL de vídeo válidas pueden ser vínculos a:

   - Vídeos de YouTube: `https://youtu.be/CoDhMRUUjeI`
   - Vídeos de Vimeo: `https://vimeo.com/190156113`
   - Archivos de vídeo válidos (`.mp4` se recomienda): `https://myvideos.com/spiral.mp4`

  ![URL de vídeo de fondo](./assets/pb-video-url.png){width="300"}

- **[!UICONTROL Overlay Color]** - Seleccione un color para aplicar un tinte transparente al vídeo.

- **[!UICONTROL Infinite Loop]** - Configurado como `No` para que el vídeo se reproduzca una vez y se detenga. Cuando esta opción se establece en `Yes` (valor predeterminado), el vídeo se repite en un bucle infinito.

- **[!UICONTROL Lazy Load]** - Configurado como `No` para que el vídeo se cargue con la página, incluso cuando no esté visible. Cuando esta opción se establece en `Yes` (opción predeterminada), el vídeo se carga desde el origen solo cuando está visible en la pantalla.

- **[!UICONTROL Play Only When Visible]** - Configurado como `No` para que el vídeo comience a reproducirse inmediatamente después de cargarse, independientemente de si está visible. Cuando esta opción se establece en `Yes` (opción predeterminada), el vídeo solo se reproducirá cuando esté visible.

- **[!UICONTROL Fallback Image]** - Si es necesario, especifique una imagen para mostrar en la pantalla antes de que se cargue el vídeo y si el vídeo no se carga por alguna razón.

## Fondo de paralaje

Utilice estas opciones para controlar la velocidad de una imagen de fondo o un vídeo de desplazamiento en relación con el desplazamiento de la página. El fondo se puede configurar para que se desplace más lentamente para crear una sensación de inmersión.

- Establecer **Habilitar fondo de paralaje** hasta `Yes`.
- Introduzca el **Velocidad de paralaje** como valor decimal entre `-1.0` y `2.0`.

![Configuración de fondo de paralaje](./assets/pb-settings-parallax-background.png){width="600" zoomable="yes"}

## Avanzadas

- Para controlar la posición horizontal de los contenedores de contenido que se agregan a la fila, elija una **[!UICONTROL Alignment]**:

  | Opción | Descripción |
  | ------ | ----------- |
  | `Default` | Aplica la configuración predeterminada de alineación especificada en la hoja de estilos de la temática actual. |
  | `Left` | Alinea los contenedores de contenido a lo largo del borde izquierdo del contenedor de filas, con margen para cualquier relleno que se especifique. |
  | `Center` | Alinea el contenedor de contenido en el centro del contenedor de filas, con margen para cualquier relleno que se especifique. |
  | `Right` | Alinea el contenedor de contenido a lo largo del borde derecho del contenedor de filas, con margen para cualquier relleno que se especifique. |

  {style="table-layout:auto"}

- Configure las variables **[!UICONTROL Border]** estilo que se aplica a los cuatro lados del contenedor de filas:

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

- Si establece un estilo de borde distinto de `None`, complete las opciones de visualización de bordes:

  ![Color del borde](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

  | Opción | Descripción |
  | ------ |------------ |
  | [!UICONTROL Border Color] | Especifique el color seleccionando una muestra, haciendo clic en el selector de color o introduciendo un nombre de color válido o un valor hexadecimal equivalente. |
  | [!UICONTROL Border Width] | Introduzca el número de píxeles de la anchura de la línea del borde. |
  | [!UICONTROL Border Radius] | Introduzca el número de píxeles para definir el tamaño del radio que se utiliza para redondear cada esquina del borde. |

  {style="table-layout:auto"}

  La fila del ejemplo siguiente tiene un radio de borde de 15.

  ![Fila con radio de borde de 15](./assets/pb-settings-border-radius-15.png){width="500"}

- (Opcional) Especifique los nombres de **[!UICONTROL CSS classes]** de la hoja de estilos actual para aplicarla al contenedor de filas.

  Separe los distintos nombres de clase con un espacio.

- Introduzca valores, en píxeles, para **[!UICONTROL Margins and Padding]** para especificar los márgenes externos y el relleno interno de la fila.

  Introduzca cada valor correspondiente en el diagrama del contenedor de filas.

  | Área del contenedor | Descripción |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | Cantidad de espacio en blanco que se aplica al borde exterior de todos los lados del contenedor. Opciones: `Top` / `Right` / `Bottom` / `Left` |
  | [!UICONTROL Padding] | Cantidad de espacio en blanco que se aplica al borde interior de todos los lados del contenedor. Opciones: `Top` / `Right` / `Bottom` / `Left` |

  {style="table-layout:auto"}

  ![Márgenes y relleno](./assets/pb-layout-row-settings-margin-padding-default.png){width="600" zoomable="yes"}
