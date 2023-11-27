---
title: Creación y administración de widgets
description: Aprenda a crear y administrar los widgets que actualizan automáticamente el contenido de su tienda.
exl-id: 680f2f41-ec51-4ac6-9e92-2817591af3e6
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 1%

---

# Creación y administración de widgets

Los widgets son componentes reutilizables. Puede crear fácilmente widgets y modificar los existentes para actualizar automáticamente el contenido en toda la tienda. También puede eliminar widgets que ya no estén en uso.

![Widgets](./assets/widgets.png){width="700" zoomable="yes"}

## Crear un widget

El proceso de creación de un widget es casi el mismo para cada uno [tipo de widget](widgets.md#widget-types). Puede seguir la primera parte de las instrucciones y, a continuación, completar la última parte para el tipo específico de widget que desee.

### Paso 1: Elija el tipo

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Haga clic **[!UICONTROL Add Widget]**.

1. En el _[!UICONTROL Settings]_sección:

   - Establecer **[!UICONTROL Type]** al tipo de widget que desea crear.

   - Compruebe que la variable **[!UICONTROL Design Theme]** se establece en la temática actual.

     ![Configuración del widget](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Haga clic **[!UICONTROL Continue]**.

### Paso 2: Especificar las propiedades y el diseño de la tienda

1. En el _[!UICONTROL Storefront Properties]_sección:

   - Para **[!UICONTROL Widget Title]**, introduzca un título descriptivo para el widget.

     Este título solo es visible desde Admin.

   - Para **[!UICONTROL Assign to Store Views]**, seleccione las vistas de tienda en las que desea que el widget sea visible.

     Puede seleccionar una vista de tienda específica, o `All Store Views`. Para seleccionar varias vistas, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

   - (Opcional) Para **[!UICONTROL Sort Order]**, introduzca un número para determinar el orden en que aparece este elemento con otros en la misma parte de la página. (`0` = primero, `1` = segundo, `3` = tercero, etc.)

     ![Propiedades de tienda](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

1. En el _[!UICONTROL Layout Updates]_, haga clic en **[!UICONTROL Add Layout Update]**.

1. Establecer **[!UICONTROL Display On]** al tipo de página donde va a aparecer.

1. En el **[!UICONTROL Container]** , elija el área del diseño de página donde se va a colocar.

   ![Actualizaciones de diseño](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

1. Si el widget es un vínculo, establezca **[!UICONTROL Template]** a uno de los siguientes:

   - `Block Template` - Formatea el contenido para que se pueda colocar como unidad independiente en la página.
   - `Inline Template` - Formatea el contenido para que se pueda colocar dentro de otro contenido. Por ejemplo, un vínculo que va dentro de un párrafo de texto.

### Paso 3: Completar las opciones del widget

Las opciones de cada tipo de widget varían ligeramente, pero el proceso es básicamente el mismo. En el ejemplo siguiente se muestra la lista de productos de una categoría específica, con controles de paginación.

1. En el panel izquierdo, elija **[!UICONTROL Widget Options]**.

1. Haga clic **[!UICONTROL Select Block]**.

1. Introduzca una **[!UICONTROL Title]** para aparecer encima de la lista, como `Featured Products`.

1. Para los controles de paginación, establezca **[!UICONTROL Display Page Control]** hasta `Yes`  y haga lo siguiente:

   - Introduzca el **[!UICONTROL Number of Products per Page]**.

   - Introduzca el total **[!UICONTROL Number of Products to Display]**.

   - Establecer **[!UICONTROL Condition]** a la categoría de productos que se va a mostrar.

     El proceso es el mismo que establecer una condición para una [regla de precios](../merchandising-promotions/price-rules-catalog.md).

### Paso 4: guardar y comprobar el resultado

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

1. Cuando se le solicite, siga las instrucciones de la parte superior del espacio de trabajo para actualizar la caché según sea necesario.

1. Vuelva a la tienda para comprobar que el widget funciona correctamente.

   Para moverlo a una ubicación diferente, puede volver a abrir el widget y probar con una página o referencia de bloque diferente.

## Demostración de creación de widget

Para obtener más información sobre la creación de widgets, vea este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/343786?quality=12)

## Edición de un widget

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Localice el widget mediante los filtros situados encima de la cuadrícula y, a continuación, haga clic en el nombre del widget.

1. Realice los cambios necesarios.

   Revise los pasos para crear un widget para obtener información sobre las opciones del widget.

1. Haga clic en **[!UICONTROL Save]**.

## Eliminar un widget

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Busque los widgets mediante los filtros situados encima de la cuadrícula y, a continuación, active la casilla de los widgets que desea eliminar.

1. En la esquina superior izquierda de la lista, establezca **[!UICONTROL Actions]** hasta `Delete`.

1. Cuando termine, haga clic en **[!UICONTROL Submit]**.

1. Para confirmar la acción, haga clic en **[!UICONTROL OK]**.
