---
title: '[!DNL Google Content Experiments]'
description: Aprenda a usar [!DNL Google Content Experiments] para configurar una prueba A/B de productos, categorías o páginas de contenido de Commerce.
exl-id: ae03bc5a-de84-4dad-932e-e79e509feebe
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# [!DNL Google Content Experiments]

El siguiente ejemplo muestra cómo configurar una prueba A/B de productos, categorías o páginas de contenido mediante Experimentos de contenido de Google Analytics. Le recomendamos que mantenga dos pestañas del explorador abiertas mientras sigue las instrucciones, ya que debe ir y volver entre el administrador de Commerce y su cuenta de [!DNL Google Analytics].

>[!NOTE]
>
>[!DNL Google Content Experiments] se ha desaprobado y se ha programado su reemplazo por [Google Optimize](https://support.google.com/optimize/answer/7084762?hl=en).

## Paso 1. Habilitar experimentos de contenido (Commerce)

1. Inicie sesión en el administrador de la instalación de Commerce.

1. Siga las instrucciones para habilitar [Google Analytics](google-analytics.md) con experimentos de contenido en la configuración de Commerce.

   ![Configuración de ventas - API de Google - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

## Paso 2. Configuración de las variaciones (Commerce)

Cree varias variaciones del mismo producto, categoría o página.

- Cada variación debe tener una [clave URL](../catalog/catalog-urls.md) única.
- Cada variación debe tener seleccionada la misma [vista de tienda](../getting-started/websites-stores-views.md#scope-settings).

Puede crear hasta diez variaciones de cada entidad que desee probar. Para los productos, usa [Guardar y duplicar](../catalog/product-workspace.md) para ahorrar tiempo.

## Paso 3. Configuración del experimento (Google)

>[!NOTE]
>
>Debe tener los permisos adecuados para la cuenta de Google para crear un experimento.

1. Abra otra pestaña del explorador e inicie sesión en su cuenta de [Google Analytics][2].

   Si es necesario, vaya a **[!UICONTROL Account]** y **[!UICONTROL Property]**.

1. En la barra lateral de la izquierda, elija **[!UICONTROL Admin]** y utilice uno de los siguientes métodos:

   **Método 1:** Elegir una vista existente

   En el encabezado de la columna _[!UICONTROL View]_, haga clic en la flecha hacia abajo y elija la vista que desea que proporcione los datos para el experimento.

   **Método 2:** Crear una nueva vista de informes

   - En el encabezado de la columna _Ver_, haga clic en **[!UICONTROL Create View]** y haga lo siguiente:

      - Identifique la ubicación del experimento como `Website` o `Mobile app`.

      - Escriba un **[!UICONTROL Reporting View Name]** descriptivo.

      - Especifique **[!UICONTROL Reporting Time Zone]**.

   - Una vez finalizado, haga clic en **[!UICONTROL Create View]** y, a continuación, haga clic en la flecha hacia atrás para regresar a la página anterior.

1. En el panel izquierdo bajo _[!UICONTROL Reports]_, elija **[!UICONTROL Behavior]**>**[!UICONTROL Experiments]**.

1. Haga clic en **[!UICONTROL Create experiment]** y haga lo siguiente:

   - Especifique el porcentaje de tráfico que se va a redirigir.

   - Especifique **[!UICONTROL Original Page URL]** y las direcciones URL de cada **[!UICONTROL page variation]** que desee probar.

   - Complete las demás opciones.

1. Cuando se configure el experimento, haga clic en **[!UICONTROL Manually Insert the Code]** y copie el fragmento de código.

## Paso 4. Pegar fragmento de código (Commerce)

1. Vuelva al administrador de la instalación de Commerce y abra la versión original del producto, la categoría o la página en modo de edición.

1. Expanda la sección **[!UICONTROL View Optimization]** para el producto, categoría o página.

1. Pegue el fragmento de código que copió de los Google Analytics en el cuadro de texto **[!UICONTROL Experiment Code]**.

   >[!NOTE]
   >
   >No pegue el fragmento de código en ninguna de las variaciones.

   ![Optimización de vista de producto](../catalog/assets/product-view-optimization.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

## Paso 5: Revisión e inicio del experimento (Google)

1. Vuelve a tu cuenta de [Google Analytics][2].

1. Revise la configuración del experimento.

1. Si está listo para comenzar, haga clic en **[!UICONTROL Start Experiment]**.

   De lo contrario, haga clic en **[!UICONTROL Save for Later]**.


[2]: https://analytics.google.com/
