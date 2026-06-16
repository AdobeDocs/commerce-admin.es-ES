---
title: '[!DNL Google Analytics]'
description: Aprenda a usar [!DNL Google Analytics] para recopilar métricas útiles para sus sitios de Commerce.
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
feature: Marketing Tools, Integration
TQID: https://experienceleague.adobe.com/3YXwPB-1yDciblELQDGHXfnv1hwPJAW4Us0iG6vCf0k
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 766
ht-degree: 0%

---

# [!DNL Google Analytics]

[!DNL Google Analytics] le permite definir dimensiones y métricas personalizadas adicionales para el seguimiento, con compatibilidad para interacciones de aplicaciones móviles y sin conexión, y acceso a actualizaciones en curso. [!DNL Google Analytics] 4 es la solución de medición de próxima generación de Google y está reemplazando a [!DNL Universal Analytics]. El 1 de julio de 2023, las propiedades estándar de Universal Analytics dejarán de procesar nuevas visitas.

>[!NOTE]
>
>Si su empresa está sujeta a regulaciones de privacidad tales como el [Reglamento General de Protección de Datos](../getting-started/compliance-gdpr.md) y/o la [Ley de Privacidad del Consumidor de California](../getting-started/compliance-ccpa.md), consulte la [Configuración de Privacidad de Google](google-tools.md#google-privacy-settings).

>[!IMPORTANT]
>
>Si habilita el [Modo de restricción de cookies](../getting-started/compliance-cookie-law.md), [!DNL Google Analytics] no recopila datos sobre los visitantes a menos que hayan aceptado cookies.

## [!DNL Google Analytics] 4

{{gtag-api-note}}

### Paso 1: Configurar [!UICONTROL Google Analytics] 4

Si todavía no ha configurado [!DNL Google Analytics] 4 para su sitio, siga uno de estos métodos:

- [Configure la recopilación de datos de Analytics por primera vez](https://support.google.com/analytics/answer/9304153)
- [Agregar Google Analytics 4 a un sitio con  [!DNL Universal Analytics]](https://support.google.com/analytics/answer/9744165)

### Paso 2: Completar la configuración de Commerce

1. Inicie sesión en el administrador de su tienda de Commerce.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Google API]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Google GTag]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la subsección **[!UICONTROL Google Analytics4]** y haga lo siguiente:

   - Establezca **[!UICONTROL Enable]** en `Yes`.

   - Deje **[!UICONTROL Account type]** como `Google Analytics4`.

   - Escriba su **[!UICONTROL Measurement ID]**. Para obtener más información, consulte [Ayuda de Google Analytics](https://support.google.com/analytics/answer/9539598).

   - Si desea realizar pruebas A/B y otras pruebas de rendimiento en el contenido, establezca **Experimentos de contenido** en `Yes`.

   ![Configuración de ventas - API de Google para Google Analytics 4](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Google Universal Analytics

>[!IMPORTANT]
>
>El 1 de julio de 2023, las propiedades estándar de Universal Analytics dejarán de procesar datos. Si todavía confía en [!DNL Universal Analytics], se recomienda que [se prepare para usar Google Analytics 4](https://support.google.com/analytics/answer/10759417) a partir de ahora.

### Paso 1: Configuración de Google Universal Analytics

Visite el sitio web de Google y regístrese para obtener una cuenta de [Google Universal Analytics](https://support.google.com/analytics/answer/2817075?hl=en).

### Paso 2: Completar la configuración de Commerce

1. Inicie sesión en el administrador de su tienda de Commerce.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Google API]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Google Analytics]** y haga lo siguiente:

   - Establezca **[!UICONTROL Enable]** en `Yes`.

   - Escriba su [!DNL Google Analytics] **[!UICONTROL Account Number]**.

   - Si desea realizar pruebas A/B y otras pruebas de rendimiento en el contenido, establezca **[!UICONTROL Content Experiments]** en `Yes`.

   ![Configuración de ventas - API de Google - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Comercio electrónico mejorado

El comercio electrónico mejorado es un complemento para [!DNL Google Universal Analytics] que le permite conocer el comportamiento de compra y compra de sus clientes con insight. Puede utilizar el comercio electrónico mejorado para generar informes sobre actividades clave de los clientes, como cuándo los clientes agregan artículos al carro de compras, comienzan el proceso de cierre de compra o completan una compra. También puede identificar y analizar los patrones de los compradores que abandonan su carro de compras sin realizar una compra.

Las siguientes instrucciones muestran cómo configurar [!DNL Google Tag Manager] con [!DNL Universal Analytics] para producir informes y datos de comercio electrónico mejorados.

### Paso 1. Registrarse para cuentas de Google

1. Regístrese para obtener una cuenta de [Google Tag Manager](google-tag-manager.md) y complete la configuración de Commerce.

1. Regístrese para obtener una nueva cuenta de [Google Universal Analytics](https://support.google.com/analytics/answer/2817075?hl=en).

### Paso 2. Configurar comercio electrónico mejorado

1. Inicie sesión en su cuenta de Google Universal Analytics.

1. Cree una propiedad para el análisis de comercio electrónico mejorado con la siguiente configuración:

   - Estado: ACTIVADO
   - Productos relacionados: ON
   - Habilitar los informes mejorados de comercio electrónico: ACTIVADO
   - Etiquetado de cierre de compra: (no obligatorio)

1. Una vez finalizado, haga clic en **[!UICONTROL Submit]**.

### Paso 3. Creación de etiquetas y déclencheur

1. Inicie sesión en su cuenta de [!DNL Google Tag Manager] y cree las siguientes déclencheur:

   | Nombre | Tipo de evento | Filtrar |
   |--- |--- |--- |
   | `addToCart` | Evento personalizado |  |
   | `checkout` | Evento personalizado |  |
   | `checkout only` | Vista de página | La dirección URL de la página coincide con RegEx /checkout/.* |
   | `checkoutOption` | Evento personalizado |  |
   | `gtm.dom` | Evento personalizado |  |
   | `productClick` | Evento personalizado |  |
   | `promotionClick` | Evento personalizado |  |
   | `removeFromCart` | Evento personalizado |  |

   >[!NOTE]
   >
   >El evento [!UICONTROL Checkout] solo se activa para los métodos de pago básicos integrados de Commerce (como `Check / Money Order` y `Cash On Delivery Payment`). Este evento no se ejecuta para `PayPal checkout` y otros métodos de pago externos, que utilizan la redirección al cierre de compra desde recursos externos.

1. Cree las siguientes etiquetas de Universal Analytics con la misma configuración básica.

   - Etiquetas de Universal Analytics

     | Nombre | Tipo | Déclencheur de disparo |
     |--- |--- |--- |
     | `Add to cart tracking` | Universal Analytics | addToCart |
     | `Checkout option tracking` | Universal Analytics | checkoutOption |
     | `Checkout tracking` | Universal Analytics | pago y envío |
     | `Pageview tracking` | Universal Analytics | gtm.dom |
     | `Product click tracking` | Universal Analytics | productClick |
     | `Promo click tracking` | Universal Analytics | promotionClick |
     | `Remove from cart tracking` | Universal Analytics | removeFromCart |

   - Configuración básica de etiquetas

     | Configuración | Valor |
     |--- |--- |
     | [!UICONTROL Product] | Google Analytics |
     | [!UICONTROL Tag Type] | Universal Analytics |
     | [!UICONTROL Tracking ID] | UA-XXX (el ID de seguimiento de su cuenta de Universal Analytics). |
     | [!UICONTROL Enable Enhanced Ecommerce Features] | Verdadero |
     | [!UICONTROL Use data layer] | Verdadero |
     | [!UICONTROL Use Debug version] | Verdadero |

1. Complete las configuraciones de seguimiento individuales.

   - Introduzca la siguiente configuración de seguimiento **[!UICONTROL Add to Cart]**:

     | Configuración | Valor |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | Comercio electrónico |
     | [!UICONTROL Action] | Añadir al carro |
     | [!UICONTROL Trigger] | addToCart |

   - Introduzca la siguiente configuración de seguimiento **[!UICONTROL Checkout option]**:

     | Configuración | Valor |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | Comercio electrónico |
     | [!UICONTROL Action] | Opción de extracción |
     | [!UICONTROL Trigger] | checkoutOption |

   - Introduzca la siguiente configuración de seguimiento **[!UICONTROL PageView]**:

     | Configuración | Valor |
     |--- |--- |
     | [!UICONTROL Track Type] | PageView |
     | [!UICONTROL Trigger] | gtm.dom |

   - Complete la siguiente configuración de seguimiento **[!UICONTROL Product Click]**:

     | Configuración | Valor |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | Comercio electrónico |
     | [!UICONTROL Action] | Clic del producto |
     | [!UICONTROL Trigger] | productClick |

   - Complete la siguiente configuración de seguimiento **[!UICONTROL Promotion Click]**:

     | Configuración | Valor |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | Comercio electrónico |
     | [!UICONTROL Action] | Clic de promoción |
     | [!UICONTROL Trigger] | promotionClick |

   - Complete la siguiente configuración de seguimiento **[!UICONTROL Remove from Cart]**:

     | Configuración | Valor |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | Comercio electrónico |
     | [!UICONTROL Action] | Eliminar del carro |
     | [!UICONTROL Trigger] | removeFromCart |

1. Cuando termine, haga clic en **[!UICONTROL Preview]** y compruebe que las etiquetas funcionan correctamente.

1. Después de comprobar la configuración, haga clic en **[!UICONTROL Publish]**.
