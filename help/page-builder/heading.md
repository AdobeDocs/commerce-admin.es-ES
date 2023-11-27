---
title: 'Elementos: encabezado'
description: Obtenga información acerca del tipo de contenido Encabezado, utilizado para agregar un contenedor de texto con un nivel de encabezado de H1 a H6 a [!DNL Page Builder] escenario.
exl-id: dc51e7f6-a235-49dc-a978-1419a63fa33e
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# Elementos: encabezado

Los niveles de encabezado establecen una jerarquía que organiza el contenido y ayuda a los motores de búsqueda a indexar cada página. Utilice el _Encabezado_ tipo de contenido en [[!DNL Page Builder] stage](workspace.md#stage) para agregar un contenedor de texto con un nivel de encabezado de H1 a H6 al escenario. El formato de los encabezados depende de la hoja de estilos asociada al tema actual.

El [Encabezado de contenido](workspace.md) en el campo _[!UICONTROL Content]_se puede utilizar para añadir un encabezado H1 a la parte superior de la página. Sin embargo, el campo es un heredado del anterior [!DNL Commerce] y se proporciona para admitir contenido antiguo. Este campo no aprovecha las [!DNL Page Builder]Funciones avanzadas de. Se recomienda dejar en blanco el campo Encabezado de contenido y utilizar la variable [!DNL Page Builder] Tipo de contenido de encabezado para agregar encabezados de cualquier nivel a la página.

El siguiente ejemplo muestra cómo aparecen el encabezado de contenido y el tipo de contenido de encabezado cuando se les aplica formato mediante la temática de Luma.

![Niveles de encabezado y encabezado de contenido en la tienda](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

Puede arrastrar un encabezado desde _Elementos_ de la sección [!DNL Page Builder] panel a una fila, columna o conjunto de pestañas del escenario. El nivel de encabezado y la alineación se pueden controlar desde la barra de herramientas del editor en el escenario o utilizando _Configuración_ ( ![Icono de configuración](./assets/pb-icon-settings.png){width="20"} ) control.

{{$include /help/_includes/page-builder-save-timeout.md}}

## Editor de encabezado

![Editor de encabezados con barra de herramientas](./assets/pb-elements-heading-toolbar.png){width="500" zoomable="yes"}

## Cuadro de herramientas Contenedor de encabezado

Al igual que con todos los contenedores de contenido, la caja de herramientas aparece al pasar el ratón por encima del contenedor.

![Cuadro de herramientas Contenedor de encabezado](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

| Herramienta | Icono | Descripción |
| --------- | ----------------- | ---------------------- |
| Mover | ![Icono Mover](./assets/pb-icon-move.png){width="25"} | Mueve el contenedor de encabezado a otro lugar válido de la página. |
| (etiqueta) | Encabezado | Identifica el contenedor actual como un encabezado. |
| Configuración | ![Icono de configuración](./assets/pb-icon-settings.png){width="25"} | Abre la página Editar encabezado, donde puede cambiar las propiedades del contenedor. |
| Hide | ![Icono Ocultar](./assets/pb-icon-hide.png){width="25"} | Oculta el contenedor del encabezado. |
| Mostrar | ![Mostrar icono](./assets/pb-icon-show.png){width="25"} | Muestra el contenedor de encabezados oculto. |
| Duplicar | ![Icono Duplicar](./assets/pb-icon-duplicate.png){width="25"} | Realiza una copia del contenedor de encabezado. |
| Eliminar | ![Icono Eliminar](./assets/pb-icon-remove.png){width="25"} | Elimina el contenedor de encabezado y su contenido del escenario. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Añadir un encabezado

1. En el [!DNL Page Builder] panel, expandir **[!UICONTROL Elements]** y arrastre un **[!UICONTROL Heading]** marcador de posición a una fila, columna o ficha establecida en el escenario.

   ![Arrastrar un encabezado al escenario](./assets/pb-elements-heading-drag.png){width="600" zoomable="yes"}

1. En el editor, escriba el texto del encabezado sobre la etiqueta `Edit Heading Text` marcador.

   De forma predeterminada, al texto del encabezado se le asigna un tipo de encabezado de nivel dos (H2).

   ![Marcador de posición en el editor de encabezados](./assets/pb-elements-header-editor-placeholder.png){width="500" zoomable="yes"}

1. En la barra de herramientas, elija el tipo de encabezado adecuado entre H1 y H6.

1. Cambie la alineación si es necesario.

## Editar configuración de encabezado

1. Pase el ratón sobre el contenedor de encabezados para mostrar el cuadro de herramientas y elegir _Configuración_ ( ![Icono de configuración](./assets/pb-icon-settings.png){width="20"} ) icono.

   ![Encabezado, caja de herramientas](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

1. Actualice el contenido del encabezado (**[!UICONTROL Heading Type]** y **[!UICONTROL Heading Text]**) si es necesario.

   También puede actualizar este contenido en el editor de encabezados.

1. Actualice el _[!UICONTROL Advanced]_ajustes según sea necesario.

   - Para controlar el posicionamiento del encabezado dentro del contenedor principal, elija una **[!UICONTROL Alignment]**:

     | Opción | Descripción |
     | ------ | ----------- |
     | `Default` | Aplica la configuración predeterminada de alineación especificada en la hoja de estilos de la temática actual. |
     | `Left` | Alinea la lista a lo largo del borde izquierdo del contenedor principal, con margen para cualquier relleno que se especifique. |
     | `Center` | Alinea la lista en el centro del contenedor principal, con margen para cualquier relleno que se especifique. |
     | `Right` | Alinea el bloque a lo largo del borde derecho del contenedor principal, con margen para cualquier relleno que se especifique. |

     {style="table-layout:auto"}

   - Configure las variables **[!UICONTROL Border]** estilo aplicado a los cuatro lados del contenedor de encabezado:

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

     | Opción | Descripción |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Especifique el color seleccionando una muestra, haciendo clic en el selector de color o introduciendo un nombre de color válido o un valor hexadecimal equivalente. |
     | [!UICONTROL Border Width] | Introduzca el número de píxeles de la anchura de la línea del borde. |
     | [!UICONTROL Border Radius] | Introduzca el número de píxeles para definir el tamaño del radio que se utiliza para redondear cada esquina del borde. |

     {style="table-layout:auto"}

   - (Opcional) Especifique los nombres de **[!UICONTROL CSS classes]** de la hoja de estilos actual para aplicarla al contenedor.

     Separe los distintos nombres de clase con un espacio.

   - Introduzca valores, en píxeles, para **[!UICONTROL Margins and Padding]** para determinar los márgenes externos y el relleno interno del contenedor de encabezado.

     Introduzca los valores correspondientes en el diagrama.

     | Área del contenedor | Descripción |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | Cantidad de espacio en blanco que se aplica al borde exterior de todos los lados del contenedor. Opciones: `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | Cantidad de espacio en blanco que se aplica al borde interior de todos los lados del contenedor. Opciones: `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. Cuando termine, haga clic en **[!UICONTROL Save]** para aplicar la configuración de y volver a [!DNL Page Builder] workspace.

## Duplicación de un encabezado

Para un encabezado con formato y con una configuración específica, es más eficaz duplicarlo, en lugar de empezar de nuevo con un nuevo marcador de posición.

1. Pase el ratón sobre el contenedor de encabezados para mostrar el cuadro de herramientas y elegir _Duplicar_ ( ![Icono Duplicar](./assets/pb-icon-duplicate.png){width="20"} ) icono.

   El duplicado aparece justo debajo del original.

   ![Duplicación de un contenedor de encabezado](./assets/pb-elements-heading-duplicate.png){width="500" zoomable="yes"}

1. Pase el ratón sobre el nuevo contenedor de encabezados para mostrar el cuadro de herramientas y elegir _Mover_ ( ![Icono Mover](./assets/pb-icon-move.png){width="20"} ) icono.

   ![Mover un encabezado](./assets/pb-elements-heading-move.png){width="500" zoomable="yes"}

1. Seleccione y arrastre el encabezado hasta que la guía roja marque la nueva posición.

   Los bordes superior e inferior de cada contenedor aparecen como líneas discontinuas mientras se mueve el encabezado.

   ![Mover el encabezado duplicado a su posición](./assets/pb-elements-heading-move-guideline.png){width="500" zoomable="yes"}

1. Si desea cambiar el nivel de encabezado, haga clic en el texto del encabezado y elija el nuevo nivel en la barra de herramientas del editor.

   ![Elección de un nuevo nivel de encabezado](./assets/pb-elements-heading-change-heading-level.png){width="500" zoomable="yes"}
