---
title: 'Añadir contenido: Recommendations del producto'
description: Obtenga información acerca del tipo de contenido de Product Recommendations que se utiliza para agregar una lista de recomendaciones a [!DNL Page Builder] escenario.
exl-id: ca90c10d-8d7a-42a2-bb13-2602aa9d6eef
feature: Page Builder, Page Content, Recommendations
source-git-commit: 2f86421311b218d39c1abebaf117b8af0be5ea5d
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 0%

---

# Añadir contenido: Recommendations del producto

Utilice el _Product Recommendations_ tipo de contenido para añadir un activo existente [unidad de recomendación](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/admin/create) a la [[!DNL Page Builder] stage](workspace.md#stage) para una página, bloque o bloque dinámico de CMS.

>[!NOTE]
>
>El [!DNL Page Builder] _Product Recommendations_ el tipo de contenido es compatible con Adobe Commerce 2.4.4 y versiones posteriores y está disponible en [Product Recommendations versiones de metapaquetes 3.0.x o posteriores](https://commercemarketplace.adobe.com/magento-product-recommendations.html). Para agregar [!DNL Page Builder] compatibilidad con Product Recommendations, [consulte la información de instalación](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure). **Este tipo de contenido no está disponible para el Magento Open Source.**

{{$include /help/_includes/page-builder-save-timeout.md}}

## Caja de herramientas de Recommendations

| Herramienta | Icono | Descripción |
| --- | --| --- |
| Mover | ![Icono Mover](./assets/pb-icon-move.png){width="25"} | Mueve el contenedor de recomendación de producto y su contenido a otra posición del escenario. |
| Configuración | ![Icono de configuración](./assets/pb-icon-settings.png){width="25"} | Abre la página Editar recomendación de producto, donde puede elegir la unidad de recomendación y cambiar las propiedades del contenedor. |
| Hide | ![Icono Ocultar](./assets/pb-icon-hide.png){width="25"} | Oculta el contenedor de recomendación de producto actual y su contenido. |
| Mostrar | ![Mostrar icono](./assets/pb-icon-show.png){width="25"} | Muestra el contenedor de recomendación de producto oculto y su contenido. |
| Duplicar | ![Icono Duplicar](./assets/pb-icon-duplicate.png){width="25"} | Crea una copia duplicada del contenedor de recomendación de productos y su contenido. |
| Eliminar | ![Icono Eliminar](./assets/pb-icon-remove.png){width="25"} | Elimina el contenedor de recomendación de producto y su contenido de la fase. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Agregar una unidad de recomendación existente

1. Asegúrese de que ya ha [creó una unidad de recomendación](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/admin/create) para el [!DNL Page Builder] tipo de página.

>[!NOTE]
>
>Puede crear unidades de recomendación para [!DNL Page Builder] tipo de página solo en la vista de tienda predeterminada.

1. Abra la página, el bloque o el bloque dinámico en modo de edición.

1. Expanda el _[!UICONTROL Content]_y haga clic en **[!UICONTROL Edit with Page Builder]**o dentro del área de previsualización de contenido para abrir [!DNL Page Builder] workspace.

1. En el [!DNL Page Builder] panel debajo de _[!UICONTROL Layout]_, arrastre un **[!UICONTROL Row]**marcador de posición al escenario.

1. En el [!DNL Page Builder] panel debajo de _[!UICONTROL Add Content]_, arrastre un **[!UICONTROL Product Recommendation]**marcador de posición a la fila.

   ![Adición del tipo de contenido Recomendación de producto](./assets/pb-add-prex-drag.png){width="600" zoomable="yes"}

1. Realice una de las siguientes acciones:

   - Clic **[!UICONTROL Edit Product Recommendation]**.
   - Pase el ratón sobre el contenedor vacío para mostrar la caja de herramientas y haga clic en _Configuración_ (![Icono de configuración](./assets/pb-icon-settings.png)) icono.

   ![Editar recomendación de producto](./assets/pb-prex-toolbox.png){width="600" zoomable="yes"}

1. En el _[!UICONTROL Selection]_, haga clic en **[!UICONTROL Select]**.

1. En la lista de recomendaciones de productos activas, busque la fila con la unidad de recomendación que desee agregar y haga clic en **[!UICONTROL Select]** en la última columna.

   ![Recomendación de producto seleccionada](./assets/pb-prex-select.png){width="600" zoomable="yes"}

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Selected]**.

   El nombre de la recomendación de producto seleccionada aparece en la _[!UICONTROL Selection]_de la sección_[!UICONTROL Edit Product Recommendation]_ página.

1. Realice los cambios necesarios en la [Configuración avanzada](#advanced-settings).

   ![Editar recomendación de producto](./assets/pb-prex-edit.png){width="600" zoomable="yes"}

1. Cuando termine, haga lo siguiente:

   - Si trabaja con una ventana del explorador completamente maximizada, haga clic en el _Cerrar pantalla completa_ (![Icono Cerrar pantalla completa](./assets/pb-icon-reduce.png)) icono en la esquina superior derecha del espacio de trabajo.

   - Clic **[!UICONTROL Save]** para aplicar la configuración de y volver a [!DNL Page Builder] workspace.

   Cuando vuelva al escenario, las imágenes de marcador de posición del producto aparecerán en el contenedor.

## Editar configuración de unidad de recomendación

1. Pase el ratón sobre el contenedor de unidades de recomendación para mostrar la caja de herramientas y haga clic en _Configuración_ (![Icono de configuración](./assets/pb-icon-settings.png)) icono.

   ![Recomendación Toolbox](./assets/pb-placeholder-toolbox.png){width="600" zoomable="yes"}

1. Realice los cambios necesarios en la [Configuración avanzada](#advanced-settings).

1. Cuando termine, haga clic en **[!UICONTROL Save]** para aplicar la configuración de y volver a [!DNL Page Builder] workspace.

## Duplicación de una unidad de recomendación

1. Pase el ratón sobre el contenedor de unidades de recomendación para mostrar la caja de herramientas y haga clic en _Duplicar_ (![Icono Duplicar](./assets/pb-icon-duplicate.png)) en el cuadro de herramientas.

   El duplicado aparece justo debajo del original.

1. Para mover la unidad de recomendación duplicada a una nueva posición, pase el ratón sobre el contenedor y haga clic en _Mover_ (![Icono Mover](./assets/pb-icon-move.png)) en el cuadro de herramientas.

1. Seleccione y arrastre la unidad de recomendación hasta que aparezca la guía roja en la nueva posición.

   Los bordes superior e inferior de cada contenedor aparecen como líneas discontinuas mientras se mueve la unidad de recomendación.

## Quitar una unidad de recomendación de la fase

1. Pase el ratón sobre el contenedor de unidades de recomendación y haga clic en _Eliminar_ ( ![Icono Eliminar](./assets/pb-icon-remove.png)) en el cuadro de herramientas.

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL OK]**.

## Configuración avanzada

1. Para controlar el posicionamiento de la unidad de Product Recommendations dentro del contenedor principal, seleccione la opción **[!UICONTROL Alignment]**:

   | Opción | Descripción |
   | ------ | ----------- |
   | `Default` | Aplica la configuración predeterminada de alineación especificada en la hoja de estilos de la temática actual. |
   | `Left` | Alinea la unidad a lo largo del borde izquierdo del contenedor principal, con margen para cualquier relleno que se especifique. |
   | `Center` | Alinea la unidad en el centro del contenedor principal, con margen para cualquier relleno que se especifique. |
   | `Right` | Alinea la unidad a lo largo del borde derecho del contenedor principal, con margen para cualquier relleno que se especifique. |

   {style="table-layout:auto"}

1. Configure las variables **[!UICONTROL Border]** estilo que se aplica a los cuatro lados de la unidad Product Recommendations:

   | Opción | Descripción |
   | ------ | ----------- |
   | `Default` | Aplica el estilo de borde predeterminado especificado por la hoja de estilos asociada. |
   | `None` | No proporciona ninguna indicación visible de los bordes de la unidad. |
   | `Dotted` | El borde de la unidad aparece como una línea de puntos. |
   | `Dashed` | El borde de la unidad aparece como una línea discontinua. |
   | `Solid` | El borde de la unidad aparece como una línea sólida. |
   | `Double` | El borde de la unidad aparece como una línea doble. |
   | `Groove` | El borde de la unidad aparece como una línea ranurada. |
   | `Ridge` | El borde de la unidad aparece como una línea discontinua. |
   | `Inset` | El borde de la unidad aparece como una línea de margen. |
   | `Outset` | El borde de la unidad aparece como una línea de inicio. |

   {style="table-layout:auto"}

1. Si establece un estilo de borde distinto de `None`, complete las opciones de visualización de bordes:

   | Opción | Descripción |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Especifique el color seleccionando una muestra, haciendo clic en el selector de color o introduciendo un nombre de color válido o un valor hexadecimal equivalente. |
   | [!UICONTROL Border Width] | Introduzca el número de píxeles de la anchura de la línea del borde. |
   | [!UICONTROL Border Radius] | Introduzca el número de píxeles para definir el tamaño del radio que se utiliza para redondear cada esquina del borde. |

   {style="table-layout:auto"}

1. (Opcional) Especifique los nombres de **[!UICONTROL CSS classes]** de la hoja de estilos actual para aplicarla a la unidad.

   Separe los distintos nombres de clase con un espacio.

1. Introduzca valores, en píxeles, para **[!UICONTROL Margins and Padding]** para determinar los márgenes exteriores y el relleno interior de la unidad.

   Introduzca los valores correspondientes en el diagrama.

   | Área del contenedor | Descripción |
   | ------ | ----------- |
   | [!UICONTROL Margins] | Cantidad de espacio en blanco que se aplica al borde exterior de todos los lados de la unidad. Opciones: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Cantidad de espacio en blanco que se aplica al borde interior de todos los lados de la unidad. Opciones: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}
