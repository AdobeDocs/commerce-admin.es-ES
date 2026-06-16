---
title: '[!UICONTROL Sales] > [!UICONTROL Google API]'
description: Revise la configuración en la página [!UICONTROL Sales] > [!UICONTROL Google API] del administrador de Commerce.
exl-id: 5031ad3d-1c9a-4bc6-9bfa-683414dca979
feature: Configuration, Marketing Tools
TQID: https://experienceleague.adobe.com/KscchSWeGd3TwpcCQaGxuVXa6-7wZJinSpyA0NvTSAc
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 927
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Google API]

{{config}}

## [!UICONTROL Google Analytics]

![Google Analytics](./assets/google-api-analytics-ee.png)<!-- zoom -->

<!-- [Google Analytics](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/google-tools/google-analytics) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Vista de tienda | Habilita [!DNL Google Analytics] para su tienda. Opciones: `Yes` / `No` |
| [!UICONTROL Account Type] | Vista de tienda | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) Determina las opciones de configuración según el tipo de cuenta de Google Analytics. Opciones: Universal Analytics (predeterminado) / Google Tag Manager |
| [!UICONTROL Account Number] | Vista de tienda | El número de cuenta o código de seguimiento que se asignó al crear su cuenta de [!DNL Google Analytics]. |
| [!UICONTROL Anonymize IP] | Vista de tienda | Determina si se quita la información de identificación de las direcciones IP que aparecen en [!DNL Google Analytics] resultados. |

{style="table-layout:auto"}

## [!UICONTROL Google Analytics - Google Tag Manager]

{{ee-feature}}

![Google Analytics - tipo de cuenta de Google Tag Manager](./assets/google-api-analytics-tag-manager.png)<!-- zoom -->

Cuando **[!UICONTROL Account Type]** se establece en `Google Tag Manager`, hay campos adicionales mostrados.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container ID] | Vista de tienda | Identificador exclusivo del contenedor [!DNL Google Tag Manager]. Este valor generalmente comienza con `GTM-`. Este identificador se encuentra en su cuenta de [!DNL Google Tag Manager]. Si [!DNL Google Tag Manager] ya está instalado y configurado para su tienda, el ID de contenedor aparecerá automáticamente en este campo. |
| [!UICONTROL List property for the catalog page] | Vista de tienda | Identifica la propiedad [!DNL Google Tag Manager] asociada con la página del catálogo. Valor predeterminado: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Vista de tienda | Identifica la propiedad [!DNL Google Tag Manager] asociada con el bloque de venta cruzada. Valor predeterminado: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Vista de tienda | Identifica la propiedad [!DNL Google Tag Manager] asociada con el bloque de ampliación de venta. Valor predeterminado: `Up-sell` |
| [!UICONTROL List property for the related products block] | Vista de tienda | Identifica la propiedad [!DNL Google Tag Manager] asociada con el bloque de productos relacionado. Valor predeterminado: `Related Products` |
| [!UICONTROL List property for the search results page] | Vista de tienda | Identifica la propiedad [!DNL Google Tag Manager] asociada con la página de resultados de búsqueda. Valor predeterminado: `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Vista de tienda | Identifica la propiedad [!DNL Google Tag Manager] asociada con las etiquetas para las promociones internas. Valor predeterminado: `Label` |

{style="table-layout:auto"}

## [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-google-adwords.png)<!-- zoom -->

<!-- [Google AdWords](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/google-tools/google-adwords) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Vista de tienda | Habilita Google AdWords para la tienda. Opciones: `Yes` / `No` |
| [!UICONTROL Conversion ID] | Vista de tienda | El ID de su cuenta de Google AdWords. |
| [!UICONTROL Conversion Language] | Vista de tienda | El idioma que se usa para las conversiones de AdWords. Opciones: `All available languages` |
| [!UICONTROL Conversion Format] | Vista de tienda | Determina el formato de la notificación [!DNL Google Site Stats] que aparece en la página de conversión. La notificación establece un vínculo a una página que informa a los visitantes sobre las cookies que se utilizan para realizar un seguimiento de sus visitas. Este valor numérico se asigna a la variable `google_conversion_format` en el script de AdWords. Para obtener más información, consulta [Acerca del seguimiento de conversión](https://support.google.com/google-ads/answer/1722022?hl=en) en el sitio web de Google. Opciones: <br/>**`1`**- Muestra una notificación de una línea.<br/>**`2`** - (Predeterminado) Muestra una notificación de dos líneas. <br/>**`3`**- No muestra ninguna notificación al cliente. |
| [!UICONTROL Conversion Color] | Vista de tienda | Determina el color de la etiqueta de conversión. Use un [selector de color](https://www.w3schools.com/colors/colors_picker.asp) para elegir el valor hexadecimal. Este valor hexadecimal se asigna a la variable `google_conversion_color` en el script de AdWords. Por ejemplo: ffffff `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Vista de tienda | Etiqueta de texto que aparece con la notificación [!DNL Google Site Stats]. Esta cadena de texto se ha asignado a la variable `~` en el script de AdWords. Por ejemplo: &quot;¡Gracias por comprar!&quot; |
| [!UICONTROL Conversion Value Type] | Vista de tienda | Especifica el tipo de valor que se utiliza para determinar cuándo se produce una conversión. Opciones: <br/>**`Dynamic`**- Determina que se ha producido una conversión basada en el importe de pedido dinámico.<br/>**`Constant`**: determina que se ha producido una conversión en función del valor introducido. |
| [!UICONTROL Conversion Value] | Vista de tienda | Especifica el valor utilizado para un tipo de valor de conversión _[!UICONTROL Constant]_. |
| [!UICONTROL Send Order Currency] | Vista de tienda | Permite valores de conversión de moneda específicos de la transacción en AdWords (para sitios web con diferentes monedas base). |

{style="table-layout:auto"}

## [!UICONTROL Google GTag]

{{gtag-api-note}}

### [!UICONTROL Google Analytics4]

![Google Analytics4](./assets/google-api-gtag-google-analytics4.png)<!-- zoom -->

<!-- [Google Analytics4](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/google-tools/google-analytics) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Vista de tienda | Habilita Google Analytics 4 para tu tienda. Opciones: `Yes` / `No` |
| [!UICONTROL Account Type] | Vista de tienda | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) Determina las opciones de configuración según el tipo de cuenta de Google Analytics. Opciones: `Google Analytics4` (predeterminado) / `Google Tag Manager` |
| [!UICONTROL Measurement ID] | Vista de tienda | El número de cuenta, o código de seguimiento, que se asignó al crear su cuenta de Google Analytics. |
| [!UICONTROL Anonymize IP] | Vista de tienda | Determina si se elimina la información de identificación de las direcciones IP que aparecen en los resultados de Google Analytics. |

{style="table-layout:auto"}

### [!UICONTROL Google Analytics4 - Google Tag Manager]

{{ee-feature}}

![Google Analytics4 - Tipo de cuenta de Google Tag Manager](./assets/google-api-gtag-google-analytics4-gtm.png)<!-- zoom -->

Cuando **[!UICONTROL Account Type]** se establece en `Google Tag Manager`, hay campos adicionales mostrados.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container Id] | Vista de tienda | Identificador exclusivo del contenedor [!DNL Google Tag Manager]. Este valor generalmente comienza con `GTM-`. Este ID se encuentra en su cuenta de Google Tab Manager. Si [!DNL Google Tag Manager] ya está instalado y configurado para su tienda, el ID de contenedor aparecerá automáticamente en este campo. |
| [!UICONTROL List property for the catalog page] | Vista de tienda | Identifica la propiedad [!DNL Google Tag Manager] asociada con la página del catálogo. Valor predeterminado: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Vista de tienda | Identifica la propiedad [!DNL Google Tag Manager] asociada con el bloque de venta cruzada. Valor predeterminado: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Vista de tienda | Identifica la propiedad [!DNL Google Tag Manager] asociada con el bloque de ampliación de venta. Valor predeterminado: `Up-sell` |
| [!UICONTROL List property for the related products block] | Vista de tienda | Identifica la propiedad [!DNL Google Tag Manager] asociada con el bloque de productos relacionado. Valor predeterminado: `Related Products` |
| [!UICONTROL List property for the search results page] | Vista de tienda | Identifica la propiedad [!DNL Google Tag Manager] asociada con la página de resultados de búsqueda. Valor predeterminado: `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Vista de tienda | Identifica la propiedad [!DNL Google Tag Manager] asociada con las etiquetas para las promociones internas. Valor predeterminado: `Label` |

{style="table-layout:auto"}

### [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-gtag-google-adwords.png)<!-- zoom -->

<!-- -- Google AdWords](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/google-tools/google-adwords) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Vista de tienda | Habilita Google AdWords para la tienda. Opciones: `Yes` / `No` |
| [!UICONTROL Conversion ID] | Vista de tienda | El ID de su cuenta de Google AdWords. |
| [!UICONTROL Conversion Language] | Vista de tienda | El idioma que se usa para las conversiones de AdWords. Opciones: todos los idiomas disponibles |
| [!UICONTROL Conversion Format] | Vista de tienda | Determina el formato de la notificación de estadísticas del sitio de Google que aparece en la página de conversión. La notificación establece un vínculo a una página que informa a los visitantes sobre las cookies que se utilizan para realizar un seguimiento de sus visitas. Este valor numérico se asigna a la variable `google_conversion_format` en el script de AdWords. Para obtener más información, consulta [Acerca del seguimiento de conversión](https://support.google.com/google-ads/answer/1722022?hl=en) en el sitio web de Google. Opciones: <br/>**`1`**- Muestra una notificación de una línea.<br/>**`2`** - (Predeterminado) Muestra una notificación de dos líneas. <br/>**`3`**- No muestra ninguna notificación al cliente. |
| [!UICONTROL Conversion Color] | Vista de tienda | Determina el color de la etiqueta de conversión. Use un [selector de color](https://www.w3schools.com/colors/colors_picker.asp) para elegir el valor hexadecimal. Este valor hexadecimal se asigna a la variable `google_conversion_color` en el script de AdWords. Por ejemplo: ffffff `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Vista de tienda | Etiqueta de texto que aparece con la notificación de Google Sites Stats. Esta cadena de texto se ha asignado a la variable `~` en el script de AdWords. Por ejemplo: &quot;¡Gracias por comprar!&quot; |
| [!UICONTROL Conversion Value Type] | Vista de tienda | Especifica el tipo de valor que se utiliza para determinar cuándo se produce una conversión. Opciones: <br/>**`Dynamic`**- Determina que se ha producido una conversión basada en el importe de pedido dinámico.<br/>**`Constant`**: determina que se ha producido una conversión en función del valor introducido. |
| [!UICONTROL Conversion Value] | Vista de tienda | Especifica el valor utilizado para un tipo de valor de conversión _[!UICONTROL Constant]_. |
| [!UICONTROL Send Order Currency] | Vista de tienda | Permite valores de conversión de moneda específicos de la transacción en AdWords (para sitios web con diferentes monedas base). |

{style="table-layout:auto"}
