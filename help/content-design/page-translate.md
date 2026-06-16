---
title: Traducción de una página de contenido
description: Aprenda a crear una versión traducida de cada página que esté disponible en la vista de tienda específica.
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
TQID: https://experienceleague.adobe.com/9jox-v5fCEhPsaex70yQod--qH-Xnp9dkgmuxJGTZd0
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 368
ht-degree: 0%

---

# Traducción de una página de contenido

Si su tienda tiene varias vistas en [idiomas](../stores-purchase/store-localize.md) diferentes y ha establecido la configuración regional para cada vista en un idioma diferente, el resultado es un sitio parcialmente traducido. El siguiente paso es crear una versión traducida de cada página que esté disponible en la vista de tienda específica. La columna [!UICONTROL Store View] de la lista _[!UICONTROL Manage Pages]_&#x200B;muestra cada vista que tiene una versión traducida de la página.

Para traducir una página de contenido, debe crear otra página que tenga la misma clave de URL que el original, pero que esté asignada a la vista de tienda específica. A continuación, actualice la página para la vista específica con el texto traducido. El siguiente ejemplo muestra cómo crear una versión traducida de la página _Acerca de nosotros_ para la vista de la tienda en español.

## Paso 1: copie la clave URL de la página que desea traducir

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. En la cuadrícula, busque la página que desea traducir y ábrala en modo _edit_.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Search Engine Optimization]** y copie **[!UICONTROL URL Key]** en el portapapeles.

1. Para volver a la cuadrícula _[!UICONTROL Pages]_, haga clic en **[!UICONTROL Back]**&#x200B;en la barra de botones superior.

## Paso 2: Añadir una página para el contenido traducido

1. Haga clic en **[!UICONTROL Add New Page]**.

1. Escriba el **[!UICONTROL Page Title]** traducido.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) la sección **[!UICONTROL Content]** y complete el texto traducido para la página.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Search Engine Optimization]** y haga lo siguiente:

   - Pegue el(la) **[!UICONTROL URL Key]** que copió de la página original.

   - Escriba el texto traducido para **[!UICONTROL Meta Title]**, **[!UICONTROL Meta Keywords]** y **[!UICONTROL Meta Description]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Page in Websites]** y establezca **[!UICONTROL Store View]** en la vista de tienda donde la página va a estar disponible.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Design]** y establezca la columna **[!UICONTROL Layout]** de la página.

1. Haga clic en **[!UICONTROL Save]**.

1. Cuando se le solicite, actualice las [cachés](../systems/cache-management.md) que no sean válidas.

## Paso 3: Verificar la traducción

Para comprobar la traducción, vaya a la tienda y utilice el selector de idioma para cambiar la vista de la tienda.

Observe que todavía hay algunos elementos en la página que deben traducirse, incluidos los vínculos de pie de página de la empresa [block](block-add.md), el [mensaje de bienvenida](../getting-started/storefront-branding.md#change-the-welcome-message) y [información del producto](../stores-purchase/store-localize.md#localize-products).
