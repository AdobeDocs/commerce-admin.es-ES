---
title: Traducción de una página de contenido
description: Aprenda a crear una versión traducida de cada página que esté disponible en la vista de tienda específica.
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# Traducción de una página de contenido

Si la tienda tiene varias vistas en diferentes [idiomas](../stores-purchase/store-localize.md), y ha establecido la configuración regional para cada vista en un idioma diferente, el resultado es un sitio parcialmente traducido. El siguiente paso es crear una versión traducida de cada página que esté disponible en la vista de tienda específica. El [!UICONTROL Store View] de la columna _[!UICONTROL Manage Pages]_La lista muestra cada vista que tiene una versión traducida de la página.

Para traducir una página de contenido, debe crear otra página que tenga la misma clave de URL que el original, pero que esté asignada a la vista de tienda específica. A continuación, actualice la página para la vista específica con el texto traducido. El siguiente ejemplo muestra cómo crear una versión traducida del _Acerca de nosotros_ para la vista de la tienda en español.

## Paso 1: copie la clave URL de la página que desea traducir

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. En la cuadrícula, busque la página que desea traducir y abra en _editar_ modo.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Search Engine Optimization]** y copie la sección **[!UICONTROL URL Key]** al portapapeles.

1. Para volver a la _[!UICONTROL Pages]_cuadrícula, haga clic en **[!UICONTROL Back]**en la barra de botones superior.

## Paso 2: Añadir una página para el contenido traducido

1. Haga clic **[!UICONTROL Add New Page]**.

1. Introduzca el traducido **[!UICONTROL Page Title]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Content]** y complete el texto traducido para la página.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Search Engine Optimization]** y haga lo siguiente:

   - Pegue el **[!UICONTROL URL Key]** que ha copiado de la página original.

   - Introduzca el texto traducido para el **[!UICONTROL Meta Title]**, **[!UICONTROL Meta Keywords]**, y **[!UICONTROL Meta Description]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Page in Websites]** sección y conjunto **[!UICONTROL Store View]** a la vista de tienda donde vaya a estar disponible la página.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Design]** y establezca la columna **[!UICONTROL Layout]** de la página.

1. Haga clic **[!UICONTROL Save]**.

1. Cuando se le solicite, actualice cualquier no válido [cachés](../systems/cache-management.md).

## Paso 3: Verificar la traducción

Para comprobar la traducción, vaya a la tienda y utilice el selector de idioma para cambiar la vista de la tienda.

Tenga en cuenta que todavía hay algunos elementos en la página que deben traducirse, incluidos los vínculos de pie de página de la empresa [bloquear](block-add.md), el [mensaje de bienvenida](../getting-started/storefront-branding.md#change-the-welcome-message), y [información del producto](../stores-purchase/store-localize.md#localize-products).
