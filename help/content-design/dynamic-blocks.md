---
title: Bloques dinámicos
description: Utilice bloques dinámicos para crear contenido enriquecido e interactivo que se base en la lógica de las reglas de precios y los segmentos de clientes.
exl-id: 0c842ad9-2e46-48aa-9a12-2f74a54c352e
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# Bloques dinámicos

{{ee-feature}}

Cree contenido enriquecido e interactivo basado en la lógica de [reglas de precios](../merchandising-promotions/introduction.md#price-rules) y [segmentos de clientes](../customers/customer-segments.md). Los [bloques dinámicos](../page-builder/dynamic-block.md) existentes se pueden agregar directamente al [!DNL Page Builder] [escenario](../page-builder/workspace.md). Para ver un ejemplo detallado paso a paso sobre el uso de bloques dinámicos, vea [Tutorial 2: Bloques](../page-builder/2-blocks.md).

>[!NOTE]
>
>La opción _[!UICONTROL Banner]_&#x200B;del menú [[!UICONTROL Content]](content-menu.md) estaba obsoleta en 2.3.1 y se ha eliminado en 2.4.0. Su funcionalidad se ha sustituido por Bloques dinámicos.

![[!DNL Page Builder] - bloque dinámico con regla de precios y segmento de cliente](../page-builder/assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

## Paso 1: Crear un bloque dinámico

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

   ![Lista de bloques dinámicos](../page-builder/assets/pb-tutorial2-block-dynamic-add.png){width="600" zoomable="yes"}

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Dynamic Block]**.

   ![Nuevo bloque dinámico](../page-builder/assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. Si corresponde, establezca **[!UICONTROL Store View]** en una vista de almacén específica en la que aparecerá el bloque dinámico.

1. Para activar el bloque dinámico, establezca **[!UICONTROL Enable Dynamic Block]** en `Yes`.

1. Para referencia interna, escriba un **[!UICONTROL Dynamic Block Name]** descriptivo.

1. Establezca **[!UICONTROL Dynamic Block Type]** en el área de la página donde desea que aparezca el bloque dinámico y haga clic en **[!UICONTROL Done]**.

   ![Estableciendo el tipo de bloque dinámico](../page-builder/assets/pb-dynamic-block-type.png){width="500" zoomable="yes"}

1. En la lista **[!UICONTROL Customer Segment]**, seleccione la casilla de verificación de cada segmento que desee ver en el bloque dinámico y haga clic en **[!UICONTROL Done]** para guardar la configuración.

   ![Elegir un segmento de cliente](../page-builder/assets/pb-dynamic-block-customer-segment.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >- Si no se crea ningún segmento, el bloque dinámico es visible para todos.
   >- Si el cliente no pertenece a ningún segmento y el bloque dinámico se crea para todos los segmentos, se muestra el contenido del bloque dinámico.
   >- Si se eliminan todos los segmentos de clientes asignados a un bloque dinámico, su contenido será visible para todos.

### Uso de audiencias de Real-Time CDP en bloques dinámicos

Si [instaló](../customers/audience-activation.md#install-the-extension) y [configuró](../customers/audience-activation.md#configure-the-extension) la extensión [!DNL Audience Activation], verá una sección llamada **[!UICONTROL Audiences]**.

![Elegir una audiencia de Real-Time CDP](./assets/dynamic-block-rtcdp.png){width="600" zoomable="yes"}

En la lista **[!UICONTROL Real-Time CDP Audience]**, seleccione la casilla de verificación de cada audiencia que desee ver en el bloque dinámico y haga clic en **[!UICONTROL Done]** para guardar la configuración.

## Paso 2: Completar el contenido

Use [!DNL Page Builder] [espacio de trabajo](../page-builder/workspace.md) para completar el contenido.

![[!DNL Page Builder] - espacio de trabajo de bloque dinámico](../page-builder/assets/pb-dynamic-block-workspace.png){width="600" zoomable="yes"}

## Paso 3: Elegir una promoción relacionada

1. Desplazarse hacia abajo y expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Related Promotions]**.

1. Haga clic en el tipo de promoción que desee asociar al bloque dinámico:

   - **[!UICONTROL Add Cart Price Rules]** (consulte [Reglas de precio del carro de compras](../merchandising-promotions/price-rules-cart.md))

   - **[!UICONTROL Add Catalog Price Rules]** (consulte [Reglas de precio de catálogo](../merchandising-promotions/price-rules-catalog.md))

   >[!NOTE]
   >
   >Las reglas de precios de catálogo no son compatibles con las audiencias de Real-Time CDP.

1. En la lista de reglas disponibles, seleccione la casilla de verificación de cada regla que desee usar y haga clic en **[!UICONTROL Add Selected]**.

1. Cuando finalice el bloque dinámico, haga clic en **[!UICONTROL Save]**.

## Paso 4: Añadir el bloque dinámico a una página

1. Abra la página donde desee que aparezca el bloque dinámico.

1. Utilice el tipo de contenido [[!UICONTROL Add Dynamic Block]](../page-builder/dynamic-block.md) para agregar el bloque dinámico al escenario.

## Descripciones de campos y herramientas

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Store View] | Especifica las vistas de almacén en las que el bloque dinámico va a estar disponible. |
| [!UICONTROL Enable Dynamic Block] | Activa o desactiva el bloque dinámico. Opciones: Sí / No |
| [!UICONTROL Dynamic Block Name] | Un nombre descriptivo que identifica el bloque dinámico en el Admin. |
| [!UICONTROL Dynamic Block Type] | Identifica el lugar del [diseño de página estándar](layout-updates.md) en el que se encuentra el bloque dinámico. Opciones: <br/>**[!UICONTROL Content Area]**- Coloca el bloque dinámico en el [área de contenido](layout-updates.md) principal de la página.<br/>**[!UICONTROL Footer]** - Coloca el bloque dinámico en la página [pie de página](page-setup.md#footer). <br/>**[!UICONTROL Header]**- Coloca el bloque dinámico en la página [encabezado](page-setup.md#header).<br/>**[!UICONTROL Left Column]** - Coloca el bloque dinámico en la [barra lateral izquierda](page-layout.md#standard-page-layouts) de un diseño de dos o tres columnas. <br/>**[!UICONTROL Right Column]**- Coloca el bloque dinámico en la [barra lateral derecha](page-layout.md#standard-page-layouts) de un diseño de dos o tres columnas. |
| Segmento de cliente | Asocia un segmento de cliente con el bloque dinámico para determinar qué clientes pueden verlo. |
| Audiencia de Real-Time CDP | Asocia una [audiencia de Real-Time CDP](../customers/audience-activation.md) al bloque dinámico para determinar qué clientes pueden verlo. |

{style="table-layout:auto"}

### Contenido

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Layout] | Agregue filas, columnas o pestañas al escenario. |
| [!UICONTROL Elements] | Agregue texto, encabezados, botones, divisores y código HTML a cualquier contenedor de diseño del escenario. |
| [!UICONTROL Media] | Agregue imágenes, vídeos, titulares, controles deslizantes y mapas de Google a cualquier contenedor de diseño existente en el escenario. |
| [!UICONTROL Add Content] | Añada bloques existentes, bloques dinámicos y productos al escenario. |

{style="table-layout:auto"}

### Promociones relacionadas

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Related Cart Price Rule] | **[!UICONTROL Add Cart Price Rules]** - Asociar una [regla de precio del carro de compras](../merchandising-promotions/price-rules-cart.md) existente con el bloque dinámico como promoción. |
| [!UICONTROL Related Catalog Price Rule] | **[!UICONTROL Add Catalog Price Rules]** - Asociar una regla de precio de catálogo [existente](../merchandising-promotions/price-rules-catalog.md) con el bloque dinámico como promoción. |

{style="table-layout:auto"}
