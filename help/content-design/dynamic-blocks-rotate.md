---
title: Añadir un bloque dinámico giratorio
description: Presenta una presentación con diapositivas de contenido interactivo en la tienda agregando varios bloques dinámicos a un rotador.
exl-id: 3d338014-cf26-4171-b48b-d37b3d7b0e81
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 0%

---

# Añadir un bloque dinámico giratorio

{{ee-feature}}

Para presentar una presentación con diapositivas de contenido interactivo, puede agregar varios [bloques dinámicos](dynamic-blocks.md) a un rotador. La herramienta [widget](widgets.md) se usa para colocar el rotador en un lugar específico en una sola página o en varias páginas de la tienda.

![Rotador de bloques dinámico](./assets/widget-dynamic-block-rotator.png){width="700" zoomable="yes"}

## Paso 1: Crear bloques dinámicos individuales

Para [crear los bloques dinámicos](dynamic-blocks.md) que desea colocar en el rotador, siga estas instrucciones:

## Paso 2: Agregar un widget de rotador de bloque dinámico

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Widget]**.

1. En _Configuración_, establezca **[!UICONTROL Type]** en `Dynamic Blocks Rotator`.

1. Elija el(la) **[!UICONTROL Design Theme]** actual(a) de la tienda.

   Esta configuración identifica el paquete actual o [tema](themes.md) que determina el diseño de página de la tienda.

1. Haga clic en **[!UICONTROL Continue]**.

   ![Configuración del rotador de bloques dinámicos](./assets/widget-dynamic-block-rotator-settings.png){width="600" zoomable="yes"}

## Paso 3: Completar las opciones

1. En _Propiedades de tienda_, establezca las opciones:

   - Escriba **[!UICONTROL Title]** para el rotador.

   - En la lista **[!UICONTROL Assign to Store Views]**, seleccione las [vistas de la tienda](../getting-started/websites-stores-views.md) donde el rotador esté disponible.

   - (Opcional) Escriba un número **[!UICONTROL Sort Order]** para determinar la posición del rotador en el contenedor de destino. Es relativa a otros widgets que podrían asignarse al mismo contenedor.

   ![Propiedades de tienda de rotadores](./assets/widget-dynamic-block-rotator-storefront-properties.png){width="600" zoomable="yes"}

1. En _Opciones de diseño_, haga clic en **[!UICONTROL Add Layout Update]** y haga lo siguiente:

   - Establezca **[!UICONTROL Display on]** en la página, o tipo de página, en la que aparecerá el rotador.

      - `Categories` - Muestra el rotador en [anclaje](../catalog/navigation-layered.md) o en páginas de categoría que no sean de anclaje. Opciones: Categorías de anclaje / Categorías no de anclaje
      - `Products` - Muestra el rotador en un tipo específico de página de producto o en todas las páginas de producto. Opciones: Todos los tipos de producto / [Producto sencillo](../catalog/product-create-simple.md) / [Producto virtual](../catalog/product-create-virtual.md) / [Producto en paquete](../catalog/product-create-bundle.md) / [Producto descargable](../catalog/product-create-downloadable.md) / [Tarjeta regalo](../catalog/product-gift-card-create.md) / [Producto configurable](../catalog/product-create-configurable.md) / [Producto agrupado](../catalog/product-create-grouped.md)
      - `Generic Pages`: muestra el rotador en todas las páginas, en una página específica o solo en páginas con un diseño determinado. Opciones: `All Pages` / `Specified Page` / `Page Layouts`

     En el ejemplo, el rotador debe colocarse en un `Specified Page`.

   - Seleccione el **[!UICONTROL Page]** específico en el que aparecerá el rotador.

   - Establezca **[!UICONTROL Container]** en la parte del [diseño de página](page-layout.md#standard-page-layouts) en la que aparecerá el rotador.

     Si se asignan otros widgets al mismo contenedor, aparecerán en secuencia según el criterio de ordenación.

   - Acepte `Dynamic Block Template` como predeterminado **[!UICONTROL Template]**.

     Esta configuración determina la plantilla que se utiliza para dar formato al rotador, en función de si el rotador se va a colocar solo o dentro de texto existente.

     ![Actualizaciones del diseño del rotador](./assets/widget-dynamic-block-rotator-layout-updates.png){width="600" zoomable="yes"}

   - Haga clic en **[!UICONTROL Save and Continue Edit]**.

1. En el panel izquierdo, elija **[!UICONTROL Widget Options]**.

1. Para **[!UICONTROL Dynamic Blocks to Display]**, acepte `Specified Dynamic Blocks`.

   Este ajuste determina el tipo de bloques dinámicos que se incluyen en el rotador.

   - `Specified Dynamic Blocks`: solo incluye bloques dinámicos específicos.
   - `Cart Price Rule Related`: incluye solo bloques dinámicos asociados con una regla de precio del carro de compras.
   - `Catalog Price Rule Related`: incluye solo bloques dinámicos asociados a la regla de precio del catálogo.

1. Para **[!UICONTROL Restrict the Dynamic Block Types]** que se puedan usar con el widget, seleccione `Content Area`.

   Esta configuración limita el banner a una parte específica del diseño de página.

   - `Content Area` - Coloca el bloque dinámico en el área de contenido principal de la página.
   - `Footer` - Coloca el bloque dinámico en el pie de página.
   - `Header` - Coloca el bloque dinámico en el encabezado de la página.
   - `Left Column` - Coloca el bloque dinámico en la columna izquierda del diseño de página, si está disponible.
   - `Right Column` - Coloca el bloque dinámico en la columna derecha del diseño de página, si está disponible.

1. Establezca **[!UICONTROL Rotation Mode]** en una de las siguientes opciones:

   - `Display all instead of rotating`: muestra una pila de bloques dinámicos, donde todos son visibles.
   - `One at a time, Random` - Muestra los bloques dinámicos especificados en un orden aleatorio. Cuando se actualiza la página, aparece un bloque dinámico diferente (y aleatorio).
   - `One at the time, Series` - Muestra los bloques dinámicos especificados en la secuencia en que se agregaron. Cuando se actualiza la página, aparece el siguiente bloque dinámico de la secuencia.
   - `One at the time, Shuffle` - Muestra un bloque dinámico a la vez en orden aleatorio. Esta opción es similar a la opción `One at a time, Random`, excepto que el mismo bloque dinámico no se repite.

     ![Opciones del widget de rotor](./assets/widget-dynamic-block-rotator-widget-options.png){width="600" zoomable="yes"}

1. En la cuadrícula **[!UICONTROL Specify Dynamic Blocks]**, active la casilla de verificación de cada bloque dinámico que desee incluir en el rotador.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.
