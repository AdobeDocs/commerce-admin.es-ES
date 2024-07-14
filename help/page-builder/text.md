---
title: Elementos - Texto
description: Obtenga información acerca del tipo de contenido Texto, utilizado para agregar un contenedor de texto en el escenario  [!DNL Page Builder] .
exl-id: 3f14af35-9c04-4f4b-b3dd-d3406d56a9c0
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 0%

---

# Elementos - Texto

Utilice el tipo de contenido _Text_ para agregar un contenedor de texto con un editor WYSIWYG (&quot;Lo que ves es lo que obtienes&quot;) en [[!DNL Page Builder] stage](workspace.md#stage). Además, puede agregar vínculos, imágenes, [variables](../systems/variables-predefined.md) y widgets al texto desde la barra de herramientas del editor.

![Texto con formato en un titular](./assets/pb-storefont-banner-with-button.png){width="700"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Herramientas del editor de texto

Puede acceder al editor de texto directamente desde el escenario o desde una página de configuración. Los cambios realizados directamente en la fase se guardan automáticamente. Para obtener más información, vea [Usar el editor](../content-design/editor.md).

![Herramienta de edición de texto: TinyMCE](./assets/pb-elements-text-editor-tools.png){width="600"}

## Cuadro de herramientas Contenedor de texto

![Cuadro de herramientas de contenedor de texto](./assets/pb-elements-text-toolbox.png){width="600"}

| Herramienta | Icono | Descripción |
| --------- | --------------------- | -------------- |
| Mover | ![Icono de mover](./assets/pb-icon-move.png){width="25"} | Mueve el contenedor de texto a otro lugar válido de la página. |
| (etiqueta) | TEXTO | Identifica el contenedor actual como un elemento de texto. |
| Configuración | ![Icono de configuración](./assets/pb-icon-settings.png){width="25"} | Abre las propiedades del contenedor de texto en modo de edición. |
| Hide | ![Ocultar icono](./assets/pb-icon-hide.png){width="25"} | Oculta el contenedor de texto. |
| Mostrar | ![Mostrar icono](./assets/pb-icon-show.png){width="25"} | Muestra el contenedor de texto oculto. |
| Duplicar | ![Icono duplicado](./assets/pb-icon-duplicate.png){width="25"} | Realiza una copia del contenedor de texto. |
| Eliminar | ![Quitar icono](./assets/pb-icon-remove.png){width="25"} | Elimina el contenedor de texto y su contenido del escenario. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Añadir texto

1. En el panel [!DNL Page Builder], expanda **[!UICONTROL Elements]** y arrastre un marcador de posición **[!UICONTROL Text]** a una fila, columna o conjunto de pestañas en el escenario.

   ![Arrastrando un marcador de posición de texto al escenario](./assets/pb-elements-text-drag.png){width="600" zoomable="yes"}

1. Utilice el editor para introducir y dar formato al texto, según sea necesario.

   Para obtener más información, vea [Usar el editor](../content-design/editor.md).

   ![Editor de texto con contenido](./assets/pb-elements-text-editor.png){width="600"}

## Crear un vínculo

El botón Insertar vínculo del editor facilita la adición de un hipervínculo a una imagen de la galería. Sin embargo, también se puede utilizar para crear un vínculo en línea en texto, si tiene la URL por adelantado. A diferencia del botón Widget, el botón Insertar/Editar vínculo no está integrado con páginas, productos o categorías de la tienda.

Para crear un vínculo para un número de teléfono o correo electrónico, consulte [Agregar variables personalizadas](../systems/variables-custom.md).

1. En la tienda, vaya a la página que va a ser el destino de destino del vínculo y copie la información del vínculo.

   Puede utilizar la dirección URL completa o una dirección URL relativa que omita la referencia al dominio de almacén.

   Dirección URL completa: `https://mystore.com/women/tops-women/tees-women.html`

   URL relativa - `../women/tops-women/tees-women.html`

1. Seleccione el texto en el espacio del editor y haga clic en _Insertar/editar vínculo_ ( ![Botón Insertar/editar vínculo](./assets/pb-icon-add-link.png){width="20"} ) en la barra de herramientas del editor.

   ![Agregando un vínculo a texto con formato](./assets/pb-tutorial2-column-text-editor-link-insert.png){width="500" zoomable="yes"}

1. Para **[!UICONTROL URL]**, escriba el vínculo relativo que ha preparado.

1. Establezca **[!UICONTROL Target]** en `None`.

   Esta configuración abre la página en la misma ventana del explorador, en lugar de abrir una nueva pestaña.

1. Para **[!UICONTROL Title]**, escriba `Shop Tees`.

   Algunos exploradores utilizan el atributo de vínculo `Title` como información de objeto.

1. Para guardar el vínculo y volver al área de trabajo [!DNL Page Builder], haga clic en **[!UICONTROL OK]**.

   ![Detalle del vínculo](./assets/pb-tutorial2-column-text-editor-link-insert-detail.png){width="500" zoomable="yes"}

## Insertar una imagen

1. Coloque el cursor en el texto donde desee insertar la imagen.

1. Haga clic en _Insertar/editar imagen_ ( ![Botón Insertar/editar imagen](./assets/icon-pb-add-image.png){width="20"} ) en la barra de herramientas del editor.

1. Para **[!UICONTROL Source]**, haga clic en el icono de búsqueda para usar el almacenamiento de medios para buscar y seleccionar una imagen.

1. Para **[!UICONTROL Image Description]**, escriba el texto descriptivo de la imagen.

   Este texto rellena el atributo de vínculo `alt` para la imagen y lo utilizan algunos exploradores para fines de accesibilidad.

1. Escriba la anchura y altura **[!UICONTROL Dimensions]**, en píxeles, para representar la imagen en la página.

   Mantenga la casilla de verificación **[!UICONTROL Constrain proportions]** seleccionada para mantener automáticamente la relación de aspecto de la imagen.

1. Para insertar la imagen y, a continuación, volver al espacio de trabajo [!DNL Page Builder], haga clic en **[!UICONTROL OK]**.

## Cambiar la configuración de texto

1. Pase el ratón sobre el contenedor de texto para mostrar la caja de herramientas y elija el icono _Configuración_ ( ![icono Configuración](./assets/pb-icon-settings.png){width="20"} ).

   >[!NOTE]
   >
   >Dado que el contenedor de texto está perfectamente anidado dentro de otro contenedor, asegúrese de que dispone del cuadro de herramientas correcto.

1. Actualice el contenido según sea necesario.

1. Actualice la configuración de _[!UICONTROL Advanced]_según sea necesario.

   - Para controlar la colocación del texto dentro del contenedor principal, elija un **[!UICONTROL Alignment]**:

     | Opción | Descripción |
     | ------ |------------ |
     | `Default` | Aplica la configuración predeterminada de alineación especificada en la hoja de estilos de la temática actual. |
     | `Left` | Alinea la lista a lo largo del borde izquierdo del contenedor principal, con margen para cualquier relleno que se especifique. |
     | `Center` | Alinea la lista en el centro del contenedor principal, con margen para cualquier relleno que se especifique. |
     | `Right` | Alinea el bloque a lo largo del borde derecho del contenedor principal, con margen para cualquier relleno que se especifique. |

     {style="table-layout:auto"}

   - Establezca el estilo **[!UICONTROL Border]** que se aplica a los cuatro lados del contenedor de texto:

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

   - Si establece un estilo de borde distinto de `None`, complete las opciones de visualización de borde:

     | Opción | Descripción |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Especifique el color seleccionando una muestra, haciendo clic en el selector de color o introduciendo un nombre de color válido o un valor hexadecimal equivalente. |
     | [!UICONTROL Border Width] | Introduzca el número de píxeles de la anchura de la línea del borde. |
     | [!UICONTROL Border Radius] | Introduzca el número de píxeles para definir el tamaño del radio que se utiliza para redondear cada esquina del borde. |

     {style="table-layout:auto"}

   - (Opcional) Especifique los nombres de **[!UICONTROL CSS classes]** de la hoja de estilos actual para aplicarlos al contenedor.

     Separe los distintos nombres de clase con un espacio.

   - Escriba valores, en píxeles, para que **[!UICONTROL Margins and Padding]** determine los márgenes externos y el margen interno del contenedor de texto.

     Introduzca los valores correspondientes en el diagrama.

     | Área del contenedor | Descripción |
     | -------------- |------------ |
     | [!UICONTROL Margins] | Cantidad de espacio en blanco que se aplica al borde exterior de todos los lados del contenedor. Opciones: `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | Cantidad de espacio en blanco que se aplica al borde interior de todos los lados del contenedor. Opciones: `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save]** para aplicar la configuración y volver al área de trabajo [!DNL Page Builder].
