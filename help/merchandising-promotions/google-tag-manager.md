---
title: '[!DNL Google Tag Manager]'
description: Aprenda a utilizar [!DNL Google Tag Manager] para administrar las diversas etiquetas (fragmentos de código) relacionadas con los eventos de campañas de marketing en los sitios de Adobe Commerce.
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '1161'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] le ayuda a administrar las numerosas etiquetas (fragmentos de código) relacionadas con los eventos de campañas de marketing. [!DNL Google Tag Manager] permite agregar etiquetas de seguimiento al sitio para medir la audiencia o personalizar, redirigir o llevar a cabo iniciativas de marketing de motores de búsqueda.

[!DNL Google Tag Manager] transfiere directamente datos y eventos a [!DNL Google Analytics], comercio electrónico mejorado y otras soluciones de análisis de terceros para producir una imagen clara del rendimiento de su sitio, productos y promociones.

Usted debe tener un [!DNL Google Analytics] y [!DNL Tag Manager] cuenta para continuar este proceso. Las siguientes instrucciones le guían a través del proceso de configuración de sus cuentas de Google, la configuración de su tienda de Commerce y la creación de una etiqueta de.

>[!NOTE]
>
>Si su empresa está sujeta a normas de privacidad como las siguientes [Reglamento general de protección de datos](../getting-started/compliance-gdpr.md) y/o el [California Consumer Privacy Act](../getting-started/compliance-ccpa.md), consulte [Configuración de privacidad de Google](google-tools.md#google-privacy-settings).

## Paso 1. Configure su [!DNL Google Analytics] account

Consulte [Configurar la búsqueda del sitio](https://support.google.com/analytics/answer/1012264) en la Ayuda de Google para conocer los conceptos básicos que necesita para empezar. Consulte también las guías de Google para [Google Analytics](https://support.google.com/analytics/answer/9304153) y [Google Tag Manager](https://support.google.com/tagmanager/answer/6102821).

1. Inicie sesión en su [!DNL Google Analytics] cuenta.

1. Para habilitar **[!UICONTROL Internal Site Search Tracking]**, haga lo siguiente:

   - Vaya a **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

   - Establecer **[!UICONTROL Site Search Tracking]** hasta `On`.

   - Establecer **[!UICONTROL Query]** parámetro a `q`.

   - Una vez finalizado, **[!UICONTROL Save]** la configuración.

1. Para habilitar las funciones de visualización, haga lo siguiente:

   - Elegir **[!UICONTROL Property Settings]**.

   - En _[!UICONTROL Advertising Features]_, configurado **[!UICONTROL Enable Demographics and Interest Reports]**hasta `On`.

   - **[!UICONTROL Save]** la configuración.

1. Para habilitar el seguimiento del comercio electrónico, haga lo siguiente:

   - Vaya a **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**.

   - Establecer **[!UICONTROL Enable Ecommerce]** hasta `On`.

   - Establecer **[!UICONTROL Enable Enhanced Ecommerce Reporting]** hasta `On`.

   - **[!UICONTROL Save]** la configuración.

1. Vuelva a cargar la página y compruebe que se conserva toda la configuración `On`.

   >[!NOTE]
   >
   >Si no todos los ajustes son `On`, repita los pasos anteriores, guarde y vuelva a cargar la página. Repita este proceso hasta que todos los ajustes estén configurados en `On`.

## Paso 2. Configure su [!DNL Google Tag Manager] account

Las siguientes instrucciones muestran cómo configurar un nuevo contenedor con la configuración básica. Una muestra [Compositor](https://developer.adobe.com/commerce/php/development/composer/) El archivo de configuración (.json) de se utiliza para simplificar el proceso de importación para generar una etiqueta en un nuevo contenedor. Para este ejemplo, se recomienda crear un contenedor, en lugar de modificar un contenedor existente.

>[!NOTE]
>
>Google Para obtener más información, consulte la [Exportación e importación de contenedores](https://support.google.com/tagmanager/answer/6106997). Estas instrucciones proporcionan una guía para importar un JSON de muestra en un contenedor nuevo.

1. Descargar el archivo vinculado [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt), abra el archivo en un editor y guárdelo como `GTM_M2_Config.json`.

   El archivo json se carga directamente en [!DNL Google Tag Manager].

1. Vaya a **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**.

1. Clic **[!UICONTROL Choose container file]** y seleccione el archivo json.

1. En **[!UICONTROL Choose workspace]**, haga clic en **[!UICONTROL New]**.

1. Introduzca un título y una descripción y haga clic en **[!UICONTROL Save]**.

1. Para importar el archivo, seleccione una de las siguientes acciones:

   - El **[!UICONTROL Overwrite]** debe seleccionarse para un contenedor nuevo.

   - El **[!UICONTROL Merge]** La opción debe estar seleccionada si está utilizando un contenedor existente.

1. Clic **[!UICONTROL Preview]** para revisar las etiquetas, los déclencheur y las variables.

1. Para editar la variable **[!UICONTROL Google Analytics ID]** a la que se hace referencia en las variables, haga lo siguiente:

   - Vaya a **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**.

   - Elegir **[!UICONTROL Google Analytics]** y actualice el marcador de posición (`UA-xxxxxx-x`) con los suyos **[!UICONTROL GA ID]**.

1. Siga las instrucciones de Google para agregar etiquetas, déclencheur y variables al nuevo contenedor.

   Si tiene configuraciones en otro contenedor que desee utilizar, se pueden mover al nuevo contenedor.

1. Clic **[!UICONTROL Confirm]** cuando se complete.

1. Siga las instrucciones de Google para publicar el nuevo contenedor.

## Paso 3. Configurar la tienda

{{gtag-api-note}}

1. Inicie sesión en el administrador de su tienda de Commerce.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Google API]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Google Analytics]** y configure lo siguiente:

   ![Configuración de ventas - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - Establecer **[!UICONTROL Enable]** hasta `Yes`.

   - Establecer **[!UICONTROL Account type]** hasta `Google Tag Manager`.

   - En el **[!UICONTROL Container ID]** , introduzca su ID de GTM (`GTM-xxxxxx`).

   - Si también usa Google Analytics para experimentos de contenido, establezca **Habilitar experimentos de contenido** hasta `Yes`.

   - Utilice los valores predeterminados para los campos restantes.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

1. Pruebe su [!DNL Google Tag Manager] y compruebe que todo funciona correctamente.

>[!NOTE]
>
>Cada contenedor está asociado con un sitio web y solo necesita un contenedor por cuenta. Si tiene una instancia de Commerce de varios sitios, necesita contenedores independientes.

## Paso 4. Añada el código GTM en su tienda de Adobe Commerce

1. Para copiar el código GTM, vaya a **[!UICONTROL Admin]** > **[!UICONTROL Install Google Tag Manager]**.

   Hay dos fragmentos de código GTM que se añaden al sitio de Commerce: el primero para `<head>` y el segundo para la etiqueta `<body>` etiqueta.

1. En el Administrador de comercio, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**y abra la vista de la tienda en modo de edición.

1. En _[!UICONTROL Other Settings]_, expanda **[!UICONTROL HTML Head]**y pegue el código que ha copiado de GTM para `<head>` etiqueta en el **[!UICONTROL Scripts and Style Sheets]**field.

   ![Inserción de código en el encabezado del HTML](./assets/head-tag.png){width="600" zoomable="yes"}

1. Expandir **[!UICONTROL Footer]** y pegue el código GTM de `<body>` en el **[!UICONTROL Miscellaneous HTML]** field.

   ![Inserción de código en el pie de página](./assets/footer-tag-section.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save Configuration]**.

## Descripciones de campos

| Campo | Ámbito | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable] | Vista de tienda | Determina si se puede utilizar el comercio electrónico mejorado de Google Analytics para analizar la actividad en la tienda. Opciones: `Yes` / `No` |
| [!UICONTROL Account type] | Vista de tienda | Determina el código de seguimiento de Google que se utiliza para supervisar la actividad y el tráfico de la tienda. Opciones: `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | Vista de tienda | Determina si se elimina la información de identificación de las direcciones IP que aparecen en los resultados de Google Analytics. |
| [!UICONTROL Enable Content Experiments] | Vista de tienda | Activa los experimentos de contenido de Google, que pueden utilizarse para probar hasta diez versiones diferentes de la misma página. Opciones: `Yes` / `No` |
| [!UICONTROL Container Id] | Vista de tienda | If [!DNL Google Tag Manager] ya está instalado y configurado para su tienda, el ID de contenedor aparece automáticamente en este campo. |
| [!UICONTROL List property for the catalog page] | Vista de tienda | Identifica la propiedad del Administrador de etiquetas asociada a la página del catálogo. Valor predeterminado: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Vista de tienda | Identifica la propiedad del Administrador de etiquetas asociada al bloque de venta cruzada. Valor predeterminado: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Vista de tienda | Identifica la propiedad del Administrador de etiquetas asociada al bloque de ampliación de venta. Valor predeterminado: `Up-sell` |
| [!UICONTROL List property for the related products block] | Vista de tienda | Identifica la propiedad del Administrador de etiquetas asociada al bloque de productos relacionado. Valor predeterminado: `Related Products` |
| [!UICONTROL List property for the search results page] | Vista de tienda | Identifica la propiedad del Administrador de etiquetas asociada a la página de resultados de la búsqueda. Valor predeterminado: `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | Vista de tienda | Identifica la propiedad del Administrador de etiquetas asociada a las etiquetas de las promociones internas. Valor predeterminado: `Label` |

{style="table-layout:auto"}

## Creación de una etiqueta para el seguimiento de conversiones

Si tiene una cuenta de Google AdWords, puede crear una etiqueta de que realice un seguimiento de las conversiones. El siguiente ejemplo muestra cómo utilizar ambos [!DNL Google Tag Manager] y [!DNL Google Analytics] para crear una etiqueta que se active durante la conversión de la tienda _Correcto_ página.

### Paso 1. Creación de una etiqueta

1. Inicie sesión en su [!DNL Google Tag Manager] y haga clic en el vínculo del contenedor que ha creado para su tienda.

1. En el **[!UICONTROL New Tag]** , haga clic en **[!UICONTROL Add a new tag]**.

1. Obtenga la siguiente información de su cuenta de AdWords:

   - ID de conversión
   - Etiqueta de conversión

   Si necesita ayuda, visite el sitio web de Google [sitio de asistencia](https://support.google.com/tagmanager/answer/6105160).

1. Desde el [!DNL Google Tag Manager] panel, haga clic en **[!UICONTROL Google AdWords]** y haga lo siguiente:

   - Haga clic en el marcador de posición de título e introduzca un nombre para la etiqueta nueva.

   - En **[!UICONTROL Choose Product]**, seleccione **[!UICONTROL Google AdWords]**.

   - En _[!UICONTROL Choose a Tag Type]_, seleccione **[!UICONTROL AdWords Conversion Tracking]**y haga clic en **[!UICONTROL Continue]**.

1. Introduzca el **[!UICONTROL Conversion ID]** y **[!UICONTROL Conversion Label]** en su cuenta de AdWords y haga clic en **[!UICONTROL Continue]**.

### Paso 2. Crear una regla

Continuando desde el [!DNL Google Tag Manager] , el siguiente paso es crear una regla que active la etiqueta en la página de conversión.

1. En **[!UICONTROL Fire On]**, haga clic en **[!UICONTROL Some Pages]**.

1. En el _[!UICONTROL Choose Pages]_, complete la siguiente configuración:

   - **[!UICONTROL Name]** : introduzca un nombre para la descripción de la página.

   - **[!UICONTROL Variable]** `url`

   - **Operación** - `matches RegEx`

     Para obtener más información, consulte [Operadores de selector de Regex y CSS](https://support.google.com/tagmanager/answer/7679109) en la Ayuda de Google Tag Manager.

   - **[!UICONTROL Value]** - `checkout/success.*`

1. Seleccione la casilla verde y haga clic en **[!UICONTROL Save]**.

   El déclencheur que ha configurado aparece como un botón azul en la sección Activar.

1. Cuando termine, haga clic en **[!UICONTROL Save Tag]**.

### Paso 3. Previsualización y publicación

El siguiente paso del proceso es obtener una vista previa de la etiqueta. Cada vez que se obtiene una vista previa de la etiqueta, se guarda una instantánea de la versión. Cuando esté satisfecho con los resultados, vaya a la versión que desee utilizar y haga clic en **[!UICONTROL Publish]**.
