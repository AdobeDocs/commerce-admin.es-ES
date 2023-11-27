---
title: '[!DNL Google Content Experiments]'
description: Aprenda a utilizar [!DNL Google Content Experiments] para configurar una prueba A/B de productos, categorías o páginas de contenido de Commerce.
exl-id: ae03bc5a-de84-4dad-932e-e79e509feebe
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# [!DNL Google Content Experiments]

El siguiente ejemplo muestra cómo configurar una prueba A/B de productos, categorías o páginas de contenido mediante Experimentos de contenido de Google Analytics. Le recomendamos que mantenga dos pestañas del explorador abiertas mientras sigue las instrucciones, ya que debe realizar devoluciones entre el administrador de comercio y su [!DNL Google Analytics] cuenta.

>[!NOTE]
>
>[!DNL Google Content Experiments] ha quedado obsoleto y se ha programado su sustitución por [Optimización de Google](https://support.google.com/optimize/answer/7084762?hl=en).

## Paso 1. Habilitar experimentos de contenido (Commerce)

1. Inicie sesión en el administrador de la instalación de Commerce.

1. Siga las instrucciones para habilitar [Google Analytics](google-analytics.md) con Experimentos de contenido en la configuración de Commerce.

   ![Configuración de ventas - API de Google - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

## Paso 2. Configuración de las variaciones (Commerce)

Cree varias variaciones del mismo producto, categoría o página.

- Cada variación debe tener un único [Clave de URL](../catalog/catalog-urls.md).
- Cada variación debe tener el mismo [vista de tienda](../getting-started/websites-stores-views.md#scope-settings) seleccionados.

Puede crear hasta diez variaciones de cada entidad que desee probar. Para los productos, utilice [Guardar y duplicar](../catalog/product-workspace.md) para ahorrar tiempo.

## Paso 3. Configuración del experimento (Google)

>[!NOTE]
>
>Debe tener los permisos adecuados para la cuenta de Google para crear un experimento.

1. Abra otra pestaña del explorador e inicie sesión en su [Google Analytics][2] cuenta.

   Si es necesario, vaya a **[!UICONTROL Account]** y **[!UICONTROL Property]**.

1. En la barra lateral de la izquierda, elija **[!UICONTROL Admin]** y utilice uno de los siguientes métodos:

   **Método 1:** Elegir una vista existente

   En el encabezado de _[!UICONTROL View]_, haga clic en la flecha hacia abajo y seleccione la vista que desea que proporcione los datos para el experimento.

   **Método 2:** Crear una nueva vista Informes

   - En el encabezado de _Ver_ , haga clic en **[!UICONTROL Create View]** y haga lo siguiente:

      - Identifique la ubicación del experimento como `Website` o `Mobile app`.

      - Introduzca un elemento descriptivo **[!UICONTROL Reporting View Name]**.

      - Especifique el **[!UICONTROL Reporting Time Zone]**.

   - Cuando termine, haga clic en **[!UICONTROL Create View]** y, a continuación, haga clic en la flecha hacia atrás para volver a la página anterior.

1. En el panel izquierdo, debajo de _[!UICONTROL Reports]_, elija **[!UICONTROL Behavior]**>**[!UICONTROL Experiments]**.

1. Clic **[!UICONTROL Create experiment]** y haga lo siguiente:

   - Especifique el porcentaje de tráfico que se va a redirigir.

   - Especifique el **[!UICONTROL Original Page URL]** y las direcciones URL de cada **[!UICONTROL page variation]** que desee probar.

   - Complete las demás opciones.

1. Cuando se configure el experimento, haga clic en **[!UICONTROL Manually Insert the Code]** y copie el fragmento de código.

## Paso 4. Pegar fragmento de código (Commerce)

1. Vuelva al administrador de la instalación de Commerce y abra la versión original del producto, la categoría o la página en modo de edición.

1. Expanda el **[!UICONTROL View Optimization]** para el producto, categoría o página.

1. Pegue el fragmento de código que ha copiado de los Google Analytics en **[!UICONTROL Experiment Code]** cuadro de texto.

   >[!NOTE]
   >
   >No pegue el fragmento de código en ninguna de las variaciones.

   ![Optimización de vista de producto](../catalog/assets/product-view-optimization.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

## Paso 5: Revisión e inicio del experimento (Google)

1. Vuelva a su [Google Analytics][2] cuenta.

1. Revise la configuración del experimento.

1. Si está listo para empezar, haga clic en **[!UICONTROL Start Experiment]**.

   De lo contrario, haga clic en **[!UICONTROL Save for Later]**.


[2]: https://analytics.google.com/
