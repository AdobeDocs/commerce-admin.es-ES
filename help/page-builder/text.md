---
title: Elementos - Texto
description: Obtenga información acerca del tipo de contenido Texto, utilizado para agregar un contenedor de texto en la [!DNL Page Builder] escenario.
exl-id: 3f14af35-9c04-4f4b-b3dd-d3406d56a9c0
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 0%

---

# Elementos - Texto

Utilice el _Texto_ Tipo de contenido para agregar un contenedor de texto con un editor WYSIWYG (&quot;Lo que ve es lo que obtiene&quot;) en la [[!DNL Page Builder] stage](workspace.md#stage). Además, puede agregar vínculos, imágenes, [variables](../systems/variables-predefined.md)y añaden widgets al texto desde la barra de herramientas del editor.

![Texto con formato en un titular](./assets/pb-storefont-banner-with-button.png){width="700"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Herramientas del editor de texto

Puede acceder al editor de texto directamente desde el escenario o desde una página de configuración. Los cambios realizados directamente en la fase se guardan automáticamente. Para obtener más información, consulte [Uso del editor](../content-design/editor.md).

![Herramienta de edición de texto: TinyMCE](./assets/pb-elements-text-editor-tools.png){width="600"}

## Cuadro de herramientas Contenedor de texto

![Cuadro de herramientas Contenedor de texto](./assets/pb-elements-text-toolbox.png){width="600"}

| Herramienta | Icono | Descripción |
| --------- | --------------------- | -------------- |
| Mover | ![Icono Mover](./assets/pb-icon-move.png){width="25"} | Mueve el contenedor de texto a otro lugar válido de la página. |
| (etiqueta) | TEXTO | Identifica el contenedor actual como un elemento de texto. |
| Configuración | ![Icono de configuración](./assets/pb-icon-settings.png){width="25"} | Abre las propiedades del contenedor de texto en modo de edición. |
| Hide | ![Icono Ocultar](./assets/pb-icon-hide.png){width="25"} | Oculta el contenedor de texto. |
| Mostrar | ![Mostrar icono](./assets/pb-icon-show.png){width="25"} | Muestra el contenedor de texto oculto. |
| Duplicar | ![Icono Duplicar](./assets/pb-icon-duplicate.png){width="25"} | Realiza una copia del contenedor de texto. |
| Eliminar | ![Icono Eliminar](./assets/pb-icon-remove.png){width="25"} | Elimina el contenedor de texto y su contenido del escenario. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Añadir texto

1. En el [!DNL Page Builder] panel, expandir **[!UICONTROL Elements]** y arrastre un **[!UICONTROL Text]** marcador de posición a una fila, columna o ficha establecida en el escenario.

   ![Arrastrar un marcador de posición de texto al escenario](./assets/pb-elements-text-drag.png){width="600" zoomable="yes"}

1. Utilice el editor para introducir y dar formato al texto, según sea necesario.

   Para obtener más información, consulte [Uso del editor](../content-design/editor.md).

   ![Editor de texto con contenido](./assets/pb-elements-text-editor.png){width="600"}

## Creación de un vínculo

El botón Insertar vínculo del editor facilita la adición de un hipervínculo a una imagen de la galería. Sin embargo, también se puede utilizar para crear un vínculo en línea en texto, si tiene la URL por adelantado. A diferencia del botón Widget, el botón Insertar/Editar vínculo no está integrado con páginas, productos o categorías de la tienda.

Para crear un vínculo para un número de teléfono o un correo electrónico, consulte [Adición de variables personalizadas](../systems/variables-custom.md).

1. En la tienda, vaya a la página que va a ser el destino de destino del vínculo y copie la información del vínculo.

   Puede utilizar la dirección URL completa o una dirección URL relativa que omita la referencia al dominio de almacén.

   URL completa - `https://mystore.com/women/tops-women/tees-women.html`

   URL relativa - `../women/tops-women/tees-women.html`

1. Seleccione el texto en el espacio del editor y haga clic en _Insertar/editar vínculo_ ( ![Botón Insertar/editar vínculo](./assets/pb-icon-add-link.png){width="20"} ) en la barra de herramientas del editor.

   ![Adición de un vínculo a texto con formato](./assets/pb-tutorial2-column-text-editor-link-insert.png){width="500" zoomable="yes"}

1. Para **[!UICONTROL URL]**, introduzca el vínculo relativo que ha preparado.

1. Establecer **[!UICONTROL Target]** hasta `None`.

   Esta configuración abre la página en la misma ventana del explorador, en lugar de abrir una nueva pestaña.

1. Para **[!UICONTROL Title]**, introduzca `Shop Tees`.

   El `Title` algunos exploradores utilizan el atributo de vínculo como información de objeto.

1. Para guardar el vínculo y volver a [!DNL Page Builder] workspace, haga clic en **[!UICONTROL OK]**.

   ![Detalles del vínculo](./assets/pb-tutorial2-column-text-editor-link-insert-detail.png){width="500" zoomable="yes"}

## Insertar una imagen

1. Coloque el cursor en el texto donde desee insertar la imagen.

1. Clic _Insertar/editar imagen_ ( ![Botón Insertar/editar imagen](./assets/icon-pb-add-image.png){width="20"} ) en la barra de herramientas del editor.

1. Para **[!UICONTROL Source]**, haga clic en el icono de búsqueda para utilizar el almacenamiento de medios para localizar y seleccionar una imagen.

1. Para **[!UICONTROL Image Description]**, introduzca un texto descriptivo para la imagen.

   Este texto rellena el `alt` atributo de vínculo para la imagen y lo utilizan algunos exploradores para la accesibilidad.

1. Introduzca la anchura y la altura **[!UICONTROL Dimensions]**, en píxeles, para representar la imagen en la página.

   Guarde el **[!UICONTROL Constrain proportions]** casilla de verificación seleccionada para mantener automáticamente la proporción de aspecto de la imagen.

1. Para insertar la imagen y volver al [!DNL Page Builder] workspace, haga clic en **[!UICONTROL OK]**.

## Cambiar la configuración de texto

1. Pase el ratón sobre el contenedor de texto para mostrar el cuadro de herramientas y elegir la _Configuración_ ( ![Icono de configuración](./assets/pb-icon-settings.png){width="20"} ) icono.

   >[!NOTE]
   >
   >Dado que el contenedor de texto está perfectamente anidado dentro de otro contenedor, asegúrese de que dispone del cuadro de herramientas correcto.

1. Actualice el contenido según sea necesario.

1. Actualice el _[!UICONTROL Advanced]_ajustes según sea necesario.

   - Para controlar la posición del texto dentro del contenedor principal, elija una **[!UICONTROL Alignment]**:

     | Opción | Descripción |
     | ------ |------------ |
     | `Default` | Aplica la configuración predeterminada de alineación especificada en la hoja de estilos de la temática actual. |
     | `Left` | Alinea la lista a lo largo del borde izquierdo del contenedor principal, con margen para cualquier relleno que se especifique. |
     | `Center` | Alinea la lista en el centro del contenedor principal, con margen para cualquier relleno que se especifique. |
     | `Right` | Alinea el bloque a lo largo del borde derecho del contenedor principal, con margen para cualquier relleno que se especifique. |

     {style="table-layout:auto"}

   - Configure las variables **[!UICONTROL Border]** estilo que se aplica a los cuatro lados del contenedor de texto:

     | Opción | Descripción |
     | ------ |------------ |
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

     | Opción | Descripción |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Especifique el color seleccionando una muestra, haciendo clic en el selector de color o introduciendo un nombre de color válido o un valor hexadecimal equivalente. |
     | [!UICONTROL Border Width] | Introduzca el número de píxeles de la anchura de la línea del borde. |
     | [!UICONTROL Border Radius] | Introduzca el número de píxeles para definir el tamaño del radio que se utiliza para redondear cada esquina del borde. |

     {style="table-layout:auto"}

   - (Opcional) Especifique los nombres de **[!UICONTROL CSS classes]** de la hoja de estilos actual para aplicarla al contenedor.

     Separe los distintos nombres de clase con un espacio.

   - Introduzca valores, en píxeles, para **[!UICONTROL Margins and Padding]** para determinar los márgenes exteriores y el relleno interno del contenedor de texto.

     Introduzca los valores correspondientes en el diagrama.

     | Área del contenedor | Descripción |
     | -------------- |------------ |
     | [!UICONTROL Margins] | Cantidad de espacio en blanco que se aplica al borde exterior de todos los lados del contenedor. Opciones: `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | Cantidad de espacio en blanco que se aplica al borde interior de todos los lados del contenedor. Opciones: `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. Cuando termine, haga clic en **[!UICONTROL Save]** para aplicar la configuración de y volver a [!DNL Page Builder] workspace.
