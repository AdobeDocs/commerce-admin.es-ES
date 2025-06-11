---
title: Creación y administración de widgets
description: Aprenda a crear y administrar los widgets que actualizan automáticamente el contenido de su tienda.
exl-id: 680f2f41-ec51-4ac6-9e92-2817591af3e6
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# Creación y administración de widgets

Los widgets son componentes reutilizables. Puede crear fácilmente widgets y modificar los existentes para actualizar automáticamente el contenido en toda la tienda. También puede eliminar widgets que ya no estén en uso.

![Widgets](./assets/widgets.png){width="700" zoomable="yes"}

## Crear un widget

El proceso de creación de un widget es casi el mismo para cada [tipo de widget](widgets.md#widget-types). Puede seguir la primera parte de las instrucciones y, a continuación, completar la última parte para el tipo específico de widget que desee.

### Paso 1: Elija el tipo

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Haga clic en **[!UICONTROL Add Widget]**.

1. En la sección _[!UICONTROL Settings]_:

   - Establezca **[!UICONTROL Type]** en el tipo de widget que desea crear.

   - Compruebe que **[!UICONTROL Design Theme]** esté establecido en el tema actual.

     ![Configuración del widget](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Continue]**.

### Paso 2: Especificar las propiedades y el diseño de la tienda

1. En la sección _[!UICONTROL Storefront Properties]_:

   - Para **[!UICONTROL Widget Title]**, escriba un título descriptivo para el widget.

     Este título solo es visible desde Admin.

   - Para **[!UICONTROL Assign to Store Views]**, seleccione las vistas de la tienda donde desee que el widget sea visible.

     Puede seleccionar una vista de tienda específica o `All Store Views`. Para seleccionar varias vistas, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

   - (Opcional) Para **[!UICONTROL Sort Order]**, escriba un número para determinar el orden en que aparece este elemento con otros en la misma parte de la página. (`0` = primero, `1` = segundo, `3` = tercero, etc.)

     ![Propiedades de tienda](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

1. En la sección _[!UICONTROL Layout Updates]_, haga clic en **[!UICONTROL Add Layout Update]**.

1. Establezca **[!UICONTROL Display On]** en el tipo de página donde debe aparecer.

1. En la lista **[!UICONTROL Container]**, elija el área del diseño de página donde se colocará.

   ![Actualizaciones de diseño](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

1. Si el widget es un vínculo, establezca **[!UICONTROL Template]** en una de las siguientes opciones:

   - `Block Template`: da formato al contenido para que se pueda colocar como unidad independiente en la página.
   - `Inline Template`: da formato al contenido para que se pueda colocar dentro de otro contenido. Por ejemplo, un vínculo que va dentro de un párrafo de texto.

### Paso 3: Completar las opciones del widget

Las opciones de cada tipo de widget varían ligeramente, pero el proceso es básicamente el mismo. En el ejemplo siguiente se muestra la lista de productos de una categoría específica, con controles de paginación.

1. En el panel izquierdo, elija **[!UICONTROL Widget Options]**.

1. Haga clic en **[!UICONTROL Select Block]**.

1. Escriba un(a) **[!UICONTROL Title]** para que aparezca sobre la lista, como `Featured Products`.

1. Para los controles de paginación, establezca **[!UICONTROL Display Page Control]** en `Yes` y haga lo siguiente:

   - Escriba **[!UICONTROL Number of Products per Page]**.

   - Escriba el total **[!UICONTROL Number of Products to Display]**.

   - Establezca **[!UICONTROL Condition]** en la categoría de productos que se mostrarán.

     El proceso es el mismo que establecer una condición para una [regla de precio](../merchandising-promotions/price-rules-catalog.md).

### Paso 4: guardar y comprobar el resultado

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

1. Cuando se le solicite, siga las instrucciones de la parte superior del espacio de trabajo para actualizar la caché según sea necesario.

1. Vuelva a la tienda para comprobar que el widget funciona correctamente.

   Para moverlo a una ubicación diferente, puede volver a abrir el widget y probar con una página o referencia de bloque diferente.

## Demostración de creación de widget

Para obtener más información sobre la creación de widgets, vea este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/343786?quality=12&learn=on)

## Edición de un widget

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Localice el widget mediante los filtros situados encima de la cuadrícula y, a continuación, haga clic en el nombre del widget.

1. Realice los cambios necesarios.

   Revise los pasos para crear un widget para obtener información sobre las opciones del widget.

1. Haga clic en **[!UICONTROL Save]**.

## Eliminar un widget

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Busque los widgets mediante los filtros situados encima de la cuadrícula y, a continuación, active la casilla de los widgets que desea eliminar.

1. En la esquina superior izquierda de la lista, establezca **[!UICONTROL Actions]** en `Delete`.

1. Una vez finalizado, haga clic en **[!UICONTROL Submit]**.

1. Para confirmar la acción, haga clic en **[!UICONTROL OK]**.
