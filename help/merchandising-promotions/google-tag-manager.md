---
title: '[!DNL Google Tag Manager]'
description: Aprenda a usar [!DNL Google Tag Manager] para administrar las muchas etiquetas (fragmentos de código) que están relacionadas con los eventos de campañas de marketing en los sitios de Adobe Commerce.
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: 22a619db0b0673dc520b9bdc5d6cd0c8ffecdf08
workflow-type: tm+mt
source-wordcount: '1459'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] es una potente herramienta que le ayuda a administrar e implementar de manera eficiente varias etiquetas (fragmentos de código) asociadas con los eventos de campañas de marketing. [!DNL Google Tag Manager] le permite agregar etiquetas de seguimiento a su sitio para medir la audiencia o personalizar, redirigir o llevar a cabo iniciativas de marketing de motores de búsqueda.

[!DNL Google Tag Manager] transfiere directamente datos y eventos a [!DNL Google Analytics], el comercio electrónico mejorado y otras soluciones de análisis de terceros para obtener una imagen clara del rendimiento de su sitio, productos y promociones.

Debe tener una cuenta de [!DNL Google Analytics] y [!DNL Tag Manager] para continuar con este proceso. Las siguientes instrucciones le guían a través del proceso de configuración de las cuentas de Google, la configuración de la tienda de Commerce y la creación de una etiqueta.

>[!NOTE]
>
>Si su empresa está sujeta a regulaciones de privacidad tales como el [Reglamento General de Protección de Datos](../getting-started/compliance-gdpr.md) y/o la [Ley de Privacidad del Consumidor de California](../getting-started/compliance-ccpa.md), consulte la [Configuración de Privacidad de Google](google-tools.md#google-privacy-settings).

## Paso 1. Configurar su cuenta de [!DNL Google Analytics]

Consulte [Configurar la búsqueda en el sitio](https://support.google.com/analytics/answer/1012264) en la Ayuda de Google para conocer los conceptos básicos que necesita para empezar. Consulte también las guías de Google para [Google Analytics](https://support.google.com/analytics/answer/9304153) y [Google Tag Manager](https://support.google.com/tagmanager/answer/6102821).

1. Inicie sesión en su cuenta de [!DNL Google Analytics].

1. Para habilitar **[!UICONTROL Internal Site Search Tracking]**, haga lo siguiente:

   - Vaya a **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

   - Establezca **[!UICONTROL Site Search Tracking]** en `On`.

   - Establezca el parámetro **[!UICONTROL Query]** en `q`.

   - Una vez completada, **[!UICONTROL Save]** la configuración.

1. Para habilitar las funciones de visualización, haga lo siguiente:

   - Elija **[!UICONTROL Property Settings]**.

   - En _[!UICONTROL Advertising Features]_, establezca **[!UICONTROL Enable Demographics and Interest Reports]**en `On`.

   - **[!UICONTROL Save]** la configuración.

1. Para habilitar el seguimiento del comercio electrónico, haga lo siguiente:

   - Vaya a **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**.

   - Establezca **[!UICONTROL Enable Ecommerce]** en `On`.

   - Establezca **[!UICONTROL Enable Enhanced Ecommerce Reporting]** en `On`.

   - **[!UICONTROL Save]** la configuración.

1. Vuelva a cargar la página y compruebe que todas las opciones de configuración se mantengan en `On`.

   >[!NOTE]
   >
   >Si no todas las configuraciones son `On`, repita los pasos anteriores, guarde y vuelva a cargar la página. Repita este proceso hasta que toda la configuración esté establecida en `On`.

## Paso 2. Configurar su cuenta de [!DNL Google Tag Manager]

Las siguientes instrucciones muestran cómo configurar un nuevo contenedor con la configuración básica. Se usa un archivo de configuración (.json) de [Composer](https://developer.adobe.com/commerce/php/development/composer/) de muestra para simplificar el proceso de importación con el fin de generar una etiqueta en un contenedor nuevo. Para este ejemplo, se recomienda crear un contenedor, en lugar de modificar un contenedor existente.

>[!NOTE]
>
>Para obtener más información, consulte [Exportación e importación de contenedores](https://support.google.com/tagmanager/answer/6106997) de Google. Estas instrucciones proporcionan una guía para importar un JSON de muestra en un contenedor nuevo.

1. Descargue el archivo vinculado [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt), ábralo en un editor y guárdelo como `GTM_M2_Config.json`.

   El archivo json se subió directamente a [!DNL Google Tag Manager].

1. Vaya a **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**.

1. Haga clic en **[!UICONTROL Choose container file]** y seleccione el archivo json.

1. En **[!UICONTROL Choose workspace]**, haga clic en **[!UICONTROL New]**.

1. Escriba un título y una descripción y luego haga clic en **[!UICONTROL Save]**.

1. Para importar el archivo, seleccione una de las siguientes acciones:

   - La opción **[!UICONTROL Overwrite]** debe estar seleccionada para un nuevo contenedor.

   - La opción **[!UICONTROL Merge]** debe estar seleccionada si está usando un contenedor existente.

1. Haga clic en **[!UICONTROL Preview]** para revisar las etiquetas, los déclencheur y las variables.

1. Para editar **[!UICONTROL Google Analytics ID]** al que se hace referencia en las variables, haga lo siguiente:

   - Vaya a **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**.

   - Elija **[!UICONTROL Google Analytics]** y actualice el marcador de posición (`UA-xxxxxx-x`) con su propio **[!UICONTROL GA ID]**.

1. Siga las instrucciones de Google para agregar etiquetas, déclencheur y variables al nuevo contenedor.

   Si tiene configuraciones en otro contenedor que desee utilizar, se pueden mover al nuevo contenedor.

1. Haga clic en **[!UICONTROL Confirm]** cuando haya terminado.

1. Siga las instrucciones de Google para publicar el nuevo contenedor.

## Paso 3. Configurar la tienda

{{gtag-api-note}}

1. Inicie sesión en el administrador de su tienda de Commerce.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Google API]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Google Analytics]** y configure lo siguiente:

   ![Configuración de ventas - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - Establezca **[!UICONTROL Enable]** en `Yes`.

   - Establezca **[!UICONTROL Account type]** en `Google Tag Manager`.

   - En el campo **[!UICONTROL Container ID]**, introduzca su ID de GTM (`GTM-xxxxxx`).

   - Si también usa Google Analytics para experimentos de contenido, establezca **Habilitar experimentos de contenido** en `Yes`.

   - Utilice los valores predeterminados para los campos restantes.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

1. Pruebe la configuración de [!DNL Google Tag Manager] y compruebe que todo funciona correctamente.

>[!NOTE]
>
>Cada contenedor está asociado con un sitio web y solo necesita un contenedor por cuenta. Si tiene una instancia de Commerce de varios sitios, necesita contenedores independientes.

## Descripciones de campos

| Campo | Ámbito | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable] | Vista de tienda | Determina si se puede utilizar Google Analytics Enhanced Ecommerce para analizar la actividad de la tienda. Opciones: `Yes` / `No` |
| [!UICONTROL Account type] | Vista de tienda | Determina el código de seguimiento de Google que se utiliza para supervisar la actividad y el tráfico de la tienda. Opciones: `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | Vista de tienda | Determina si se elimina la información de identificación de las direcciones IP que aparecen en los resultados de Google Analytics. |
| [!UICONTROL Enable Content Experiments] | Vista de tienda | Activa los experimentos de contenido de Google, que pueden utilizarse para probar hasta diez versiones diferentes de la misma página. Opciones: `Yes` / `No` |
| [!UICONTROL Container Id] | Vista de tienda | Si [!DNL Google Tag Manager] ya está instalado y configurado para su tienda, el ID de contenedor aparecerá automáticamente en este campo. |
| [!UICONTROL List property for the catalog page] | Vista de tienda | Identifica la propiedad del Administrador de etiquetas asociada a la página del catálogo. Valor predeterminado: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Vista de tienda | Identifica la propiedad del Administrador de etiquetas asociada al bloque de venta cruzada. Valor predeterminado: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Vista de tienda | Identifica la propiedad del Administrador de etiquetas asociada al bloque de ampliación de venta. Valor predeterminado: `Up-sell` |
| [!UICONTROL List property for the related products block] | Vista de tienda | Identifica la propiedad del Administrador de etiquetas asociada al bloque de productos relacionado. Valor predeterminado: `Related Products` |
| [!UICONTROL List property for the search results page] | Vista de tienda | Identifica la propiedad del Administrador de etiquetas asociada a la página de resultados de la búsqueda. Valor predeterminado: `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | Vista de tienda | Identifica la propiedad del Administrador de etiquetas asociada a las etiquetas de las promociones internas. Valor predeterminado: `Label` |

{style="table-layout:auto"}

## Creación de una etiqueta para el seguimiento de conversiones

Si tiene una cuenta de Google AdWords, puede crear una etiqueta de que realice un seguimiento de las conversiones. El siguiente ejemplo muestra cómo usar [!DNL Google Tag Manager] y [!DNL Google Analytics] para crear una etiqueta que se active en la página de conversión _Success_ de su tienda.

### Paso 1. Creación de una etiqueta

1. Inicie sesión en su cuenta de [!DNL Google Tag Manager] y haga clic en el vínculo del contenedor que creó para su tienda.

1. En el cuadro **[!UICONTROL New Tag]**, haga clic en **[!UICONTROL Add a new tag]**.

1. Obtenga la siguiente información de su cuenta de AdWords:

   - ID de conversión
   - Etiqueta de conversión

   Si necesita ayuda, visite el [sitio de soporte técnico](https://support.google.com/tagmanager/answer/6105160) de Google.

1. En el tablero [!DNL Google Tag Manager], haga clic en **[!UICONTROL Google AdWords]** y haga lo siguiente:

   - Haga clic en el marcador de posición de título e introduzca un nombre para la etiqueta nueva.

   - En **[!UICONTROL Choose Product]**, seleccione **[!UICONTROL Google AdWords]**.

   - En _[!UICONTROL Choose a Tag Type]_, seleccione **[!UICONTROL AdWords Conversion Tracking]**y haga clic en **[!UICONTROL Continue]**.

1. Escriba **[!UICONTROL Conversion ID]** y **[!UICONTROL Conversion Label]** desde su cuenta de AdWords y haga clic en **[!UICONTROL Continue]**.

### Paso 2. Crear una regla

Continuando desde el panel [!DNL Google Tag Manager], el siguiente paso es crear una regla que active la etiqueta en la página de conversión.

1. En **[!UICONTROL Fire On]**, haga clic en **[!UICONTROL Some Pages]**.

1. En la sección _[!UICONTROL Choose Pages]_, complete la siguiente configuración:

   - **[!UICONTROL Name]** - Escriba un nombre para la descripción de la página.

   - **[!UICONTROL Variable]** `url`

   - **Operación** - `matches RegEx`

     Para obtener más información, consulte [Operadores de selector de Regex y CSS](https://support.google.com/tagmanager/answer/7679109) en la Ayuda de Google Tag Manager.

   - **[!UICONTROL Value]** - `checkout/success.*`

1. Seleccione la casilla verde y haga clic en **[!UICONTROL Save]**.

   El déclencheur que ha configurado aparece como un botón azul en la sección Activar.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Tag]**.

### Paso 3. Previsualización y publicación

El siguiente paso del proceso es obtener una vista previa de la etiqueta. Cada vez que se obtiene una vista previa de la etiqueta, se guarda una instantánea de la versión. Cuando esté satisfecho con los resultados, vaya a la versión que desee usar y haga clic en **[!UICONTROL Publish]**.

## Etiqueta personalizada de HTML con JavaScript

En esta sección se explica cómo agregar un nonce de CSP a HTML Tag JavaScript personalizado para su ejecución en la página de cierre de compra, lo que garantiza el cumplimiento de los requisitos de la Política de seguridad de contenido (CSP). Esta adición mejora la seguridad del sitio al evitar la ejecución de scripts no autorizados. Para obtener información más detallada, consulte la documentación de [Política de seguridad de contenido](https://developer.adobe.com/commerce/php/development/security/content-security-policies).

>[!NOTE]
>
>La importación de la variable global `cspNonce` en Google Tag Manager solo es compatible con la versión 2.4.8 y posteriores de Adobe Commerce.

>[!WARNING]
>
>Añadir secuencias de comandos desconocidas a la tienda puede poner en peligro los datos. Los scripts autorizados en la página de pago pueden robar información confidencial del cliente, incluidos los detalles de pago. Es esencial tomar precauciones para proteger la cuenta de Google Tag Manager. Agregue solo scripts de confianza, revise y audite regularmente sus etiquetas e implemente medidas de seguridad sólidas como autenticación de doble factor (2FA) y controles de acceso.

### Paso 1. Crear una variable nonce de CSP

Puede crear una variable nonce CSP que se puede utilizar en el Administrador de etiquetas de Google importando la configuración de la variable o configurándola manualmente.

#### Importar la configuración de la variable

La variable de seguridad CSP está incluida en el contenedor de ejemplo [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt). Puede crear la variable importando este código en el espacio de trabajo.

#### Crear la variable manualmente

Si no puede importar la configuración de la variable, complete los siguientes pasos para crearla.

1. En su área de trabajo, vaya a la sección **Variables** de la barra lateral.
1. Haga clic en el botón **Nuevo** en la parte inferior de la página en la sección **Variables definidas por el usuario**.
1. Asigne un nombre a la variable `gtmNonce`.
1. Haga clic en el icono de lápiz para editar la variable.
1. Seleccione **Variable JavaScript** de la sección **Variable de página**.
1. En el campo **Nombre de variable global**, escriba `window.cspNonce`.
1. Guarde la variable.

Para obtener más información acerca de [Variables de Google Tag Manager](https://support.google.com/tagmanager/answer/7683056?hl=en), consulte [Tipos de variables definidas por el usuario para la web](https://support.google.com/tagmanager/answer/7683362?hl=en) en la documentación de Google. Esta documentación ofrece instrucciones detalladas sobre la creación y administración de variables personalizadas para adaptar la administración de etiquetas a necesidades específicas de marketing y análisis.

### Paso 2. Crear una etiqueta personalizada de HTML

1. En su área de trabajo, vaya a la sección **Etiquetas** de la barra lateral.
1. Haga clic en el botón **Nuevo**.
1. En la sección **Configuración de etiqueta**, seleccione **Etiqueta personalizada de HTML**.
1. Escriba el JavaScript necesario en el área de texto y agregue un atributo nonce a la etiqueta `<script>` de apertura que apunte a la variable que creó en el paso anterior. Por ejemplo:

   ```html
   <script nonce="{{gtmNonce}}">
       // Your JavaScript code here
   </script>
   ```

1. Seleccione **Documento de asistencia.write**.
1. En la sección **Activación**, seleccione el déclencheur que desee. Por ejemplo, **Inicialización del consentimiento - Todas las páginas**.

Para obtener más información sobre [Etiquetas](https://support.google.com/tagmanager/answer/3281060) en el Administrador de etiquetas de Google, consulte [Etiquetas personalizadas](https://support.google.com/tagmanager/answer/6107167) en la documentación de Google.
