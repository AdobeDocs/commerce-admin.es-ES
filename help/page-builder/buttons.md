---
title: 'Elementos: botones'
description: Obtenga información acerca del tipo de contenido Botones, que se usa para agregar un botón individual o un conjunto de botones en el escenario  [!DNL Page Builder] .
exl-id: 9f1681c5-04b0-4259-aaf6-5d8081bd8cdb
feature: Page Builder, Page Content
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1586'
ht-degree: 0%

---

# Elementos: botones

Utilice el tipo de contenido _Botones_ para agregar un botón individual o un conjunto de botones en el [[!DNL Page Builder] escenario](workspace.md#stage). Puede organizar los botones horizontal o verticalmente y agregarlos directamente a las filas, columnas, pestañas y titulares del escenario.

![Titular con un botón en la tienda](./assets/pb-storefont-banner-with-button.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Cajas de herramientas

Cuando trabaja con el tipo de contenido Botones, agrega y edita botones individuales y el contenedor de botones que contiene uno o más botones. Cada una tiene su propia caja de herramientas que se utiliza para diseñar botones en el escenario [!DNL Page Builder].

### Cuadro de herramientas de botón individual

![Cuadro de herramientas de botón](./assets/pb-elements-button-settings.png){width="500" zoomable="yes"}

| Herramienta | Icono | Descripción |
| --------- | -------- | -------------- |
| Configuración | ![Icono de configuración](./assets/pb-icon-settings.png){width="25"} | Abre la página Botón de edición, donde puede cambiar las propiedades del botón. |
| Duplicar | ![Icono duplicado](./assets/pb-icon-duplicate.png){width="25"} | Realiza una copia del botón. |
| Eliminar | ![Quitar icono](./assets/pb-icon-remove.png){width="25"} | Elimina el botón del escenario. |

{style="table-layout:auto"}

### Cuadro de herramientas Contenedor de botones

![Cuadro de herramientas de contenedor de botones](./assets/pb-elements-buttons-toolbox-settings.png){width="500" zoomable="yes"}

| Herramienta | Icono | Descripción |
| --------- | ----------------- | ----------- |
| Mover | ![Icono de mover](./assets/pb-icon-move.png){width="25"} | Mueve el contenedor de botón a otro lugar válido de la página. |
| Añadir | ![Agregar icono](./assets/pb-icon-add-button.png){width="25"} | Agrega un botón al contenedor. |
| (etiqueta) | Botón | Identifica el contenedor actual como un elemento de botón. |
| Configuración | ![Icono de configuración](./assets/pb-icon-settings.png){width="25"} | Abre la página Editar botones, donde puede cambiar las propiedades del contenedor. |
| Hide | ![Ocultar icono](./assets/pb-icon-hide.png){width="25"} | Oculta el contenedor de botón. |
| Mostrar | ![Mostrar icono](./assets/pb-icon-show.png){width="25"} | Muestra el contenedor de botones oculto. |
| Duplicar | ![Icono duplicado](./assets/pb-icon-duplicate.png){width="25"} | Realiza una copia del contenedor de botones. |
| Eliminar | ![Quitar icono](./assets/pb-icon-remove.png){width="25"} | Elimina el contenedor de botón y su contenido del escenario. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Añadir un botón individual

1. En el panel [!DNL Page Builder], expanda **[!UICONTROL Elements]** y arrastre un marcador de posición **[!UICONTROL Buttons]** a una fila, columna o conjunto de pestañas en el escenario.

   ![Arrastrando un botón al escenario](./assets/pb-elements-button-drag.png){width="500" zoomable="yes"}

1. Pase el ratón sobre el botón para mostrar la caja de herramientas y elija el icono _Configuración_ (![icono Configuración](./assets/pb-icon-settings.png)).

1. Escriba **[!UICONTROL Button Text]** para que se muestre en el botón.

   ![Configuración básica del botón](./assets/pb-elements-button-settings-button-text.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Button Type]** en una de las siguientes opciones:

   | Tipo | Descripción |
   | ------ | ----------- |
   | `Primary` | Aplica el estilo del botón principal de la hoja de estilos actual. |
   | `Secondary` | Aplica el estilo del botón secundario de la hoja de estilos actual, si corresponde. |
   | `Link` | Crea un hipervínculo en lugar de un botón. |

   {style="table-layout:auto"}

   ![Ejemplo de botón primario y secundario](./assets/pb-elements-button-settings-button-primary-secondary.png){width="500" zoomable="yes"}

1. Establezca **[!UICONTROL Button Link]** mediante uno de los siguientes tipos:

   - **[!UICONTROL URL]** - Escriba la dirección URL de destino para el vínculo.

     La dirección URL puede ser un vínculo relativo a un producto o a una página de la tienda, o bien una dirección URL completa.

     Ejemplo de dirección URL relativa: `../luma-analog-watch.html`

     Ejemplo de dirección URL completa: `http://mystore.com/luma-analog-watch.html`

     Si el vínculo va a un sitio web diferente, puede mantener la página actual abierta en la tienda abriendo el vínculo en una nueva pestaña del explorador.

     Para evitar que el visitante salga de su tienda, marque la casilla de verificación **[!UICONTROL Open in new tab]**.

   - **[!UICONTROL Product]**: escriba un nombre de producto (parcial o completo) o un SKU y, a continuación, elija el nombre de producto en la lista.

     >[!NOTE]
     >
     >Los productos se muestran en la lista según la configuración _Mostrar productos sin existencias_. Para los comerciantes de Multi Source que usan [Inventory management](../inventory-management/introduction.md), la lista de productos está limitada únicamente por la fuente asignada al sitio web predeterminado.

     ![Elegir un producto para el vínculo del botón](./assets/pb-elements-button-settings-button-link-product-search.png){width="600" zoomable="yes"}

   - **[!UICONTROL Category]**: escriba un nombre de categoría (parcial o completo) o haga clic en el campo en blanco para mostrar el árbol de categorías. A continuación, elija el nombre de la categoría en el árbol.

     ![Elegir una categoría para el vínculo del botón](./assets/pb-elements-button-settings-button-link-category-search.png){width="600" zoomable="yes"}

   - **[!UICONTROL Page]**: escriba el nombre de una página de CMS (parcial o completa) o haga clic en el campo en blanco para mostrar la lista completa. A continuación, elija el nombre de la página en la lista de resultados de la búsqueda.

     ![Elija la página de CMS para el vínculo de botón](./assets/pb-elements-button-settings-button-link-page-search.png){width="600" zoomable="yes"}

1. Complete [la configuración avanzada](#change-advanced-settings) según sea necesario.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]** en la esquina superior derecha para aplicar la configuración y volver al área de trabajo [!DNL Page Builder].

## Añadir un conjunto de botones

En las secciones siguientes se describe una serie de pasos para comenzar con un botón individual y crear un conjunto de tres botones dentro de un contenedor de botones. Si aún no tiene un botón individual, siga las instrucciones anteriores para agregar un botón individual al escenario.

### Paso 1: Crear el segundo botón

1. Pase el ratón sobre el contenedor del botón para mostrar la caja de herramientas y elija el icono _Agregar_ ( ![Agregar icono](./assets/pb-icon-add-button.png){width="20"} ).

   ![Agregando otro botón](./assets/pb-elements-buttons-toolbox-add.png){width="500" zoomable="yes"}

1. Escriba el texto que desea que aparezca en el segundo botón.

1. Haga clic en el nuevo botón para mostrar su cuadro de herramientas y elija el icono _Configuración_ ( ![icono Configuración](./assets/pb-icon-settings.png){width="20"} ).

   ![Editando el botón](./assets/pb-elements-button-set-edit-button2-toolbox.png){width="500" zoomable="yes"}

1. Establezca **[!UICONTROL Button Type]** en `Secondary`.

1. Configure **[!UICONTROL Button Link]** según sea necesario.

   En el ejemplo siguiente, el vínculo es una dirección URL relativa que va a la página [Contáctenos](../getting-started/store-details.md#contact-us-form).

   ![Configuración del botón Contáctenos](./assets/pb-elements-button-set-edit-button2-toolbox-settings.png){width="600" zoomable="yes"}

1. Complete [la configuración avanzada](#change-advanced-settings) según sea necesario.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]** para aplicar la configuración y volver al área de trabajo [!DNL Page Builder].

### Paso 2: crear el tercer botón

1. Vuelva a hacer clic en el segundo botón del escenario y elija el icono _Duplicar_ ( ![Icono de duplicado](./assets/pb-icon-duplicate.png){width="20"} ).

   ![Duplicando un botón](./assets/pb-elements-button-set-contact-us-toolbox-duplicate.png){width="500" zoomable="yes"}

1. Escriba el texto que desea que aparezca en el tercer botón.

1. Haga clic en el tercer botón para mostrar el cuadro de herramientas y elija el icono _Configuración_ ( ![icono Configuración](./assets/pb-icon-settings.png){width="20"} ).

   ![Cuadro de herramientas para el tercer botón](./assets/pb-elements-button-set-find-us-toolbox-settings.png){width="500" zoomable="yes"}

1. Actualice **[!UICONTROL Button Link]** según sea necesario.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Save]** para aplicar la configuración y volver al área de trabajo [!DNL Page Builder].

### Paso 3: Actualizar el contenedor del botón

1. Pase el ratón sobre el contenedor del botón para mostrar la caja de herramientas y elija el icono _Configuración_ ( ![icono Configuración](./assets/pb-icon-settings.png){width="20"} ).

   ![Cuadro de herramientas de contenedor de botones](./assets/pb-elements-buttons-toolbox-settings.png){width="500" zoomable="yes"}

1. En _[!UICONTROL Appearance]_, elija **[!UICONTROL Stacked]**.

1. Establezca **[!UICONTROL All Buttons are same size]** en `Yes`.

   ![Botones apilados del mismo tamaño](./assets/pb-elements-buttons-settings-appearance-stacked.png){width="300"}

1. Actualice los valores restantes según sea necesario, utilizando las descripciones de [Cambiar la configuración de un contenedor de botones](#change-settings-for-a-button-container).

1. Una vez finalizado, haga clic en **[!UICONTROL Save]** para aplicar la configuración y volver al área de trabajo [!DNL Page Builder].

   El conjunto completo de botones apilados aparece en el escenario, con un botón principal y dos botones secundarios.

   ![Botones apilados en el escenario](./assets/pb-elements-buttons-stacked.png){width="500" zoomable="yes"}

## Mover un botón

1. Haga clic en el botón que desee mover.

1. Seleccione y arrastre el icono Mover (![icono Mover](./assets/pb-icon-move.png){width="20"} ), que aparece justo antes del texto del botón, a una nueva posición para el botón dentro del contenedor de botones.

   ![Mover un botón](./assets/pb-elements-button-set-move-button.png){width="500" zoomable="yes"}

## Cambiar la configuración de un botón

1. Haga clic en el botón del escenario para mostrar la caja de herramientas y elija el icono _Configuración_ ( ![icono Configuración](./assets/pb-icon-settings.png){width="20"} ).

   ![Cuadros de herramientas de botones](./assets/pb-elements-button-toolboxes.png){width="500" zoomable="yes"}

1. Actualice la configuración estándar según sea necesario.

   - **[!UICONTROL Button Text]**: escriba el texto que se mostrará en el botón (también se puede actualizar directamente desde el escenario).

   - **[!UICONTROL Button Type]**: determina el formato del botón.

     | Tipo | Descripción |
     | ------ | ----------- |
     | `Primary` | Aplica el estilo del botón principal de la hoja de estilos actual. |
     | `Secondary` | Aplica el estilo del botón secundario de la hoja de estilos actual, si corresponde. |
     | `Link` | Crea un hipervínculo en lugar de un botón. |

     {style="table-layout:auto"}

   - **[!UICONTROL Button Link]**: determina la página de destino que se proporciona cuando se hace clic en el botón.

     | Opción | Descripción |
     | ------ | ----------- |
     | `URL` | Utiliza una dirección URL relativa o completa para identificar la página de destino. |
     | `Product` | Identifica la página de destino según el nombre del producto o el SKU. El nombre del producto se puede buscar en función de un nombre parcial o completo. A continuación, se elige el producto de la lista de resultados de búsqueda. |
     | `Category` | Identifica la página de destino como una categoría o subcategoría específica en el árbol de categorías. |
     | `Page` | Identifica la página de destino como una página de CMS específica. |

     {style="table-layout:auto"}

1. Complete [la configuración avanzada](#change-advanced-settings) según sea necesario.

1. Para guardar la configuración y volver al área de trabajo [!DNL Page Builder], haga clic en **[!UICONTROL Save]** en la esquina superior derecha.

## Cambiar la configuración de un contenedor de botones

1. Pase el ratón sobre el contenedor del botón para mostrar la caja de herramientas y elija el icono _Configuración_ ( ![icono Configuración](./assets/pb-icon-settings.png){width="20"} ).

1. Actualice la configuración de **[!UICONTROL Appearance]** según sea necesario.

   - Utilice las opciones de disposición para mostrar los botones horizontal o verticalmente en el contenedor:

     | Opción | Descripción |
     | ------ | ----------- |
     | `Inline` | Organiza los botones horizontalmente. |
     | `Stacked` | Organiza los botones verticalmente. |

     {style="table-layout:auto"}

   - Establezca la opción **[!UICONTROL All buttons are same size]** según sus preferencias.

     Cuando se establece en `Yes`, todos los botones del contenedor tienen un tamaño uniforme, según la longitud del texto de botón más largo.

1. Complete [Configuración avanzada](#change-advanced-settings) según sea necesario.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]** para aplicar la configuración y volver al área de trabajo [!DNL Page Builder].

## Cambiar configuración avanzada

Puede modificar la configuración de _[!UICONTROL Advanced]_&#x200B;para botones individuales y para el contenedor de botones.

1. Para controlar la posición dentro del contenedor principal, elija **[!UICONTROL Alignment]**:

   | Opción | Descripción |
   | ------ | ----------- |
   | `Default` | Aplica la configuración predeterminada de alineación especificada en la hoja de estilos de la temática actual. |
   | `Left` | Alinea el contenido a lo largo del borde izquierdo del contenedor principal, con margen para cualquier relleno que se especifique. |
   | `Center` | Alinea el contenido en el centro del contenedor principal, con margen para cualquier relleno que se especifique. |
   | `Right` | Alinea el contenido a lo largo del borde derecho del contenedor principal, con margen para cualquier relleno que se especifique. |

   {style="table-layout:auto"}

1. Establezca el estilo **[!UICONTROL Border]** aplicado a los cuatro lados del contenedor de botones o botones:

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

1. Si establece un estilo de borde distinto de `None`, complete las opciones de visualización de borde:

   | Opción | Descripción |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Especifique el color seleccionando una muestra, haciendo clic en el selector de color o introduciendo un nombre de color válido o un valor hexadecimal equivalente. |
   | [!UICONTROL Border Width] | Introduzca el número de píxeles de la anchura de la línea del borde. |
   | [!UICONTROL Border Radius] | Introduzca el número de píxeles para definir el tamaño del radio que se utiliza para redondear cada esquina del borde. |

   {style="table-layout:auto"}

1. (Opcional) Especifique los nombres de **[!UICONTROL CSS classes]** de la hoja de estilos actual para aplicarlos al contenedor de botones o botones.

   Separe los distintos nombres de clase con un espacio.

1. Escriba valores, en píxeles, para que **[!UICONTROL Margins and Padding]** determine los márgenes externos y el margen interno del contenedor de botones o botones.

   Introduzca los valores correspondientes en el diagrama.

   | Área del contenedor | Descripción |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | Cantidad de espacio en blanco que se aplica al borde exterior de todos los lados del contenedor. Opciones: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Cantidad de espacio en blanco que se aplica al borde interior de todos los lados del contenedor. Opciones: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}


<!-- Last updated from includes: 2023-09-11 14:30:19 -->
