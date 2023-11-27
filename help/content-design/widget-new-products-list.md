---
title: Widget de lista de nuevos productos
description: Aprenda a utilizar el nuevo widget de lista de productos para mostrar una lista de los productos añadidos más recientemente.
exl-id: bdff3655-cd14-4a19-a51f-4cabeb274d2a
feature: Page Content, Products
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Widget de lista de nuevos productos

La lista de nuevos productos es un ejemplo de contenido dinámico y consiste en datos activos que se extraen del catálogo de productos. De forma predeterminada, la variable _Nuevos productos_ Esta lista incluye los ocho primeros productos añadidos más recientemente. Sin embargo, también se puede configurar para incluir solo productos dentro de un intervalo de fechas especificado.

![Lista de nuevos productos en la página principal de la tienda](./assets/storefront-home-page-new-products.png){width="700" zoomable="yes"}

## Paso 1: Establecer cada producto como nuevo

![Magento Open Source](../assets/open-source.svg) Este paso solo se aplica al Magento Open Source.

![Adobe Commerce](../assets/adobe-logo.svg) Para tiendas Adobe Commerce, consulte [Programando una actualización](content-staging-scheduled-update.md) y, a continuación, continúe con el paso 2 de esta página.

_[!UICONTROL Set Product as New]_la configuración del intervalo de fechas solo se puede configurar en actualizaciones programadas.

Al establecer un producto como nuevo, se agrega el producto al _Nuevos productos_ lista. Puede volver a cambiar la configuración en cualquier momento en el que ya no desee incluirla en la lista.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Busque todos los productos que desee incluir en la función y ábralos en el modo de edición.

1. Para **[!UICONTROL Set Product as New]**, active la opción para configurar el producto como nuevo producto o no.

   ![Configuración del producto como nuevo](./assets/product-set-as-new.png){width="400" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

1. Cuando se le pida que vuelva a indexar y actualice la caché de la página, haga clic en los vínculos en la parte superior de la página y siga las instrucciones.

## Paso 2: Crear el widget

La herramienta Widget genera el código que determina el contenido de la lista Nuevos productos y su ubicación en la tienda.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Widget]**.

1. En el _[!UICONTROL Settings]_, haga lo siguiente:

   - Establecer **[!UICONTROL Type]** hasta `Catalog New Products List`.

   - Elija la **[!UICONTROL Design Theme]** que utiliza la tienda.

1. Haga clic **[!UICONTROL Continue]**.

   ![Nueva configuración del widget de lista de productos](./assets/widget-settings.png){width="600" zoomable="yes"}

1. En el _[!UICONTROL Storefront Properties]_, haga lo siguiente:

   - Para **[!UICONTROL Widget Title]**, introduzca un título descriptivo para el widget. (Este título solo es visible desde el _Administrador_.)

   - Para **[!UICONTROL Assign to Store Views]**, seleccione las vistas de la tienda donde el widget sea visible.

     Puede seleccionar una vista de tienda específica, o `All Store Views`. Para seleccionar varias vistas, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

   - (Opcional) Para **[!UICONTROL Sort Order]**, introduzca un número para determinar el orden en que aparece este elemento con otros en la misma parte de la página. (`0` = primero, `1` = segundo, `3` = tercero, etc.)

   ![Actualizaciones de diseño](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

## Paso 3: Elija la ubicación

1. En el _[!UICONTROL Layout Updates]_, haga clic en **[!UICONTROL Add Layout Update]**.

1. Establecer **[!UICONTROL Display On]** hasta `Specified Page.`

1. Establecer **[!UICONTROL Page]** hasta `CMS Home Page`.

1. Establecer **[!UICONTROL Block Reference]** hasta `Main Content Area`.

1. Establecer **[!UICONTROL Template]** a uno de los siguientes:

   - `New Product List Template`
   - `New Products Grid Template`

     ![Actualizaciones de diseño](./assets/widget-layout-update-new-products-list.png){width="600" zoomable="yes"}

1. Haga clic **[!UICONTROL Save and Continue Edit]**.

   Por ahora, puede ignorar el mensaje para actualizar la caché.

## Paso 4: Configuración de la lista

1. En el panel izquierdo, elija **[!UICONTROL Widget Options]**.

1. Establecer **[!UICONTROL Display Products]** a uno de los siguientes:

   - `All Products` - Enumera los productos en secuencia, empezando por el agregado más recientemente.
   - `New Products` - Enumera solo los productos identificados como _nuevo_. Un producto se considera nuevo durante el intervalo de fechas especificado en _[!UICONTROL Set Product As New From/To]_. La lista está vacía si caduca el intervalo de fechas sin haber definido ningún producto nuevo.

1. Para proporcionar control de navegación a listas con varias páginas, establezca **[!UICONTROL Display Page Control]** hasta `Yes`.

   Para **[!UICONTROL Number of Products per Page]**, introduzca el número de productos que desea que aparezcan en cada página.

1. Configure las variables **[!UICONTROL Number of Products to Display]** al número de productos nuevos que desea incluir en la lista.

   La configuración predeterminada es `10`.

1. Para **[!UICONTROL Cache Lifetime (Seconds)]**, elija con qué frecuencia desea actualizar la lista de nuevos productos.

   De forma predeterminada, la caché se establece en 86 400 segundos (24 horas).

   ![Opciones del widget](./assets/widget-options-new-product-list.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

1. Cuando se le pida que actualice la caché, haga clic en el vínculo del mensaje en la parte superior de la página y siga las instrucciones.

## Paso 5: Previsualizar su trabajo

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Busque la página en la cuadrícula en la que la variable _Nuevos productos_ y haga clic en el icono **[!UICONTROL Preview]** vínculo en el _[!UICONTROL Action]_columna.
