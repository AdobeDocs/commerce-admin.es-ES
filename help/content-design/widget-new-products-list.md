---
title: Widget de lista de nuevos productos
description: Aprenda a utilizar el nuevo widget de lista de productos para mostrar una lista de los productos añadidos más recientemente.
exl-id: bdff3655-cd14-4a19-a51f-4cabeb274d2a
feature: Page Content, Products
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Widget de lista de nuevos productos

La lista de nuevos productos es un ejemplo de contenido dinámico y consiste en datos activos que se extraen del catálogo de productos. De manera predeterminada, la lista _Nuevos productos_ incluye los ocho primeros productos agregados más recientemente. Sin embargo, también se puede configurar para incluir solo productos dentro de un intervalo de fechas especificado.

![Nueva lista de productos en la página principal de la tienda](./assets/storefront-home-page-new-products.png){width="700" zoomable="yes"}

## Paso 1: Establecer cada producto como nuevo

![Magento Open Source](../assets/open-source.svg) Este paso se aplica solo a Magento Open Source.

![Adobe Commerce](../assets/adobe-logo.svg) Para las tiendas Adobe Commerce, consulta [Programando una actualización](content-staging-scheduled-update.md) y continúa con el Paso 2 de esta página.

La configuración del intervalo de fechas _[!UICONTROL Set Product as New]_solo se puede configurar en actualizaciones programadas.

Al establecer un producto como nuevo, se agrega el producto a la lista _Nuevos productos_. Puede volver a cambiar la configuración en cualquier momento en el que ya no desee incluirla en la lista.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Busque todos los productos que desee incluir en la función y ábralos en el modo de edición.

1. Para **[!UICONTROL Set Product as New]**, cambie la opción para establecer el producto como nuevo producto o no.

   ![Estableciendo el producto como nuevo](./assets/product-set-as-new.png){width="400" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

1. Cuando se le pida que vuelva a indexar y actualice la caché de la página, haga clic en los vínculos en la parte superior de la página y siga las instrucciones.

## Paso 2: Crear el widget

La herramienta Widget genera el código que determina el contenido de la lista Nuevos productos y su ubicación en la tienda.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Widget]**.

1. En la sección _[!UICONTROL Settings]_, haga lo siguiente:

   - Establezca **[!UICONTROL Type]** en `Catalog New Products List`.

   - Elija el **[!UICONTROL Design Theme]** que usa la tienda.

1. Haga clic en **[!UICONTROL Continue]**.

   ![Nueva configuración del widget de lista de productos](./assets/widget-settings.png){width="600" zoomable="yes"}

1. En la sección _[!UICONTROL Storefront Properties]_, haga lo siguiente:

   - Para **[!UICONTROL Widget Title]**, escriba un título descriptivo para el widget. (Este título solo es visible desde _Admin_.)

   - Para **[!UICONTROL Assign to Store Views]**, seleccione las vistas de la tienda donde el widget sea visible.

     Puede seleccionar una vista de tienda específica o `All Store Views`. Para seleccionar varias vistas, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

   - (Opcional) Para **[!UICONTROL Sort Order]**, escriba un número para determinar el orden en que aparece este elemento con otros en la misma parte de la página. (`0` = primero, `1` = segundo, `3` = tercero, etc.)

   ![Actualizaciones de diseño](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

## Paso 3: Elija la ubicación

1. En la sección _[!UICONTROL Layout Updates]_, haga clic en **[!UICONTROL Add Layout Update]**.

1. Establecer **[!UICONTROL Display On]** en `Specified Page.`

1. Establezca **[!UICONTROL Page]** en `CMS Home Page`.

1. Establezca **[!UICONTROL Block Reference]** en `Main Content Area`.

1. Establezca **[!UICONTROL Template]** en una de las siguientes opciones:

   - `New Product List Template`
   - `New Products Grid Template`

     ![Actualizaciones de diseño](./assets/widget-layout-update-new-products-list.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save and Continue Edit]**.

   Por ahora, puede ignorar el mensaje para actualizar la caché.

## Paso 4: Configuración de la lista

1. En el panel izquierdo, elija **[!UICONTROL Widget Options]**.

1. Establezca **[!UICONTROL Display Products]** en una de las siguientes opciones:

   - `All Products`: enumera los productos en secuencia, empezando por el agregado más recientemente.
   - `New Products`: enumera solo los productos identificados como _nuevos_. Un producto se considera nuevo durante el intervalo de fechas especificado en _[!UICONTROL Set Product As New From/To]_. La lista está vacía si caduca el intervalo de fechas sin haber definido ningún producto nuevo.

1. Para proporcionar control de navegación para listas con varias páginas, establezca **[!UICONTROL Display Page Control]** en `Yes`.

   Para **[!UICONTROL Number of Products per Page]**, ingrese el número de productos que desea que aparezcan en cada página.

1. Establezca la opción **[!UICONTROL Number of Products to Display]** en el número de productos nuevos que desee incluir en la lista.

   La configuración predeterminada es `10`.

1. Para **[!UICONTROL Cache Lifetime (Seconds)]**, elija la frecuencia con la que desea actualizar la lista de nuevos productos.

   De forma predeterminada, la caché se establece en 86 400 segundos (24 horas).

   ![Opciones de widget](./assets/widget-options-new-product-list.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

1. Cuando se le pida que actualice la caché, haga clic en el vínculo del mensaje en la parte superior de la página y siga las instrucciones.

## Paso 5: Previsualizar su trabajo

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Busque la página en la cuadrícula en la que aparecerá la lista _Nuevos productos_ y haga clic en el vínculo **[!UICONTROL Preview]** de la columna _[!UICONTROL Action]_.
