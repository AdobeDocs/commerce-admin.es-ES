---
title: Google AdWords
description: Aprenda a configurar su tienda de Commerce para el seguimiento de conversión de Google AdWords a fin de medir los clics en anuncios que generan una venta u otra acción valiosa.
exl-id: 3dd3beba-edcf-4f9e-a527-7ed3609ef1ae
feature: Marketing Tools, Integration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Google AdWords

[Google AdWords](https://www.google.com/adwords/) es un servicio que puedes usar para colocar anuncios en los resultados de búsqueda de Google y en las páginas de compañías en la red de pantallas de Google. El panel de AdWords incluye herramientas para administrar sus campañas, rastrear las respuestas y medir los resultados.

El seguimiento de conversión muestra el número de clics en publicidad que conducen a una venta u otra acción valiosa. La página _Correcto_ que aparece para su cliente después de enviar un pedido se usa para realizar un seguimiento de las conversiones, ya que solo aparece después de una venta. Después de completar la configuración de Google AdWords para su tienda, no es necesario copiar el script de seguimiento de conversión en la página Éxito, porque Commerce ya tiene la información necesaria. Para obtener más información, consulte la [Ayuda de Google AdWords](https://support.google.com/adwords/answer/6095821).

![Resultados de búsqueda del anuncio de Adobe en Google](./assets/google-adwords-adobe-ad.png){width="500"}

## Paso 1. Creación de una campaña de Google AdWords

1. Visita [Google AdWords](https://ads.google.com/) y regístrate para obtener una cuenta.

1. Siga las instrucciones para crear una campaña.

1. Para configurar el seguimiento de conversión de la campaña, haga lo siguiente:

   - En la ficha **[!UICONTROL Tools]** del panel de AdWords, elija **[!UICONTROL Conversions]** y haga clic en **[!UICONTROL Conversion]**.

   - Cuando se le pida el origen de conversión, elija **[!UICONTROL Website]**.

   - Escriba un nombre para la acción de conversión que desea rastrear y haga clic en **[!UICONTROL Done]**.

   - Haga clic en **[!UICONTROL Value]** y, si corresponde, asigne un valor a la conversión. Por ejemplo:

      - Si gana $5 en cada venta, elija `Each time it happens` y asigne un valor de `$5`.
      - Si el valor de cada venta varía, deje el valor en blanco.

     Para completar, haga clic en **[!UICONTROL Done]**.

   - Haga clic en **[!UICONTROL Conversion windows]** y complete la configuración para determinar cuánto tiempo se rastrearán las conversiones, la categoría de informes y el modelo de atribución.

1. Una vez finalizado, haga clic en **[!UICONTROL Save and Continue]**.

## Paso 2. Obtenga su etiqueta de conversión

1. En **[!UICONTROL Install your tag]**, elija contar las conversiones en **[!UICONTROL Page load]**.

1. Como opción, puede agregar la notificación **[!UICONTROL Google Site Stats]** a la página de conversión.

   La notificación aparece en la esquina inferior con un vínculo a los estándares de seguridad de Google y al uso de cookies.

1. Para elegir cómo desea administrar la etiqueta de AdWords, siga uno de estos procedimientos:

   - Si planea agregar el script a su tienda, elija **[!UICONTROL Save instructions and tag]**.
   - Si planea que otra persona agregue el script a su tienda, elija **[!UICONTROL Email instructions and tag]**.

1. Una vez finalizado, haga clic en **[!UICONTROL Done]**.

## Paso 3. Configurar la tienda

{{gtag-api-note}}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Si configura Google AdWords para una vista de tienda específica, haga lo siguiente:

   - En la esquina superior izquierda, elija el(la) **[!UICONTROL Store View]** que desea configurar.

   - Cuando se le pida que confirme el cambio de ámbito, haga clic en **[!UICONTROL OK]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Google API]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Google AdWords]** y haga lo siguiente:

   - Establezca **[!UICONTROL Enable]** en `Yes`.

   - Escriba **[!UICONTROL Conversion ID]** desde el script de Google AdWords.

   ![Configuración de ventas - API de Google Ads](../configuration-reference/sales/assets/google-api-google-adwords.png){width="600" zoomable="yes"}

1. Para dar formato a la notificación de estado de Google Sites, haga lo siguiente:

   - Establezca **[!UICONTROL Conversion Language]** en el idioma identificado en el script de Google AdWords.

   - Escriba **[!UICONTROL Conversion Format]** para usar en la notificación de inicio de sitios de Google en la página de conversión.

      - `1`: muestra una notificación de una línea con un vínculo para obtener más información sobre el seguimiento de Google.
      - `2`: muestra una notificación de dos líneas con un vínculo para obtener más información sobre el seguimiento de Google.
      - `3` - No muestra ninguna notificación al cliente.

   - Escriba el [código hexadecimal](https://www.w3schools.com/colors/colors_picker.asp){:target="_blank"} de **[!UICONTROL Conversion Color]** que desea usar para la etiqueta de notificación de estadísticas del sitio de Google.

   - Escriba el texto cifrado de **[!UICONTROL Conversion Label]** que aparece en la notificación de inicio de Google Sites.

     Por ejemplo: `MlEYCOKBnGoQz6CZoAM`

     **Código de etiqueta de Google AdWords de muestra**

     ```html
     <!-- Google Code for Back to School Sale Conversion Page -->
     <script type="text/javascript">
     /* <![CDATA[ */
     var google_conversion_id = 999999999;
     var google_conversion_language = "en";
     var google_conversion_format = "3";
     var google_conversion_color = "ffffff";
     var google_conversion_label = "MlEYCOKBnGoQz6CZoAM";
     var google_remarketing_only = false;
     /* ]]> */
     </script>
     
     <script type="text/javascript" src="//www.googleadservices.com/pagead/conversion.js">
     </script>
     <noscript>
     <div style="display:inline;">
     <img height="1" width="1" style="border-style:none;" alt="" src="//www.googleadservices.com/pagead/conversion/872829007/?label=MlEYCOKBnGoQz6CZoAM&amp;guid=ON&amp;script=0"/>
     
     </noscript>
     ```

1. Establezca **[!UICONTROL Conversion Value Type]** en una de las siguientes opciones:

   - `Dynamic`: determina que se ha producido una conversión en función del valor de importe de pedido dinámico.
   - `Constant` - Determina que se ha producido una conversión basada en un valor específico ingresado.

   Para un tipo de valor de conversión _Constant_, escriba un **[!UICONTROL Value]** específico para que _[!UICONTROL Order Amount]_se califique como conversión.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Paso 4. Compruebe la configuración

En unas pocas horas, el estado de seguimiento en su panel de Google AdWords cambiará de `Unverified` a `No recent conversions` o `Recording conversions`. Cuando alguien hace clic en su anuncio y realiza una compra, la conversión aparece en la página Acciones de conversión del tablero y el informe de campaña.
