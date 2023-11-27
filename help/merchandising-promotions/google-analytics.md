---
title: '[!DNL Google Analytics]'
description: Descubra cómo puede utilizar [!DNL Google Analytics] para recopilar métricas útiles para sus sitios de Commerce.
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# [!DNL Google Analytics]

[!DNL Google Analytics] permite definir dimensiones y métricas personalizadas adicionales para el seguimiento, con compatibilidad para interacciones de aplicaciones móviles y sin conexión, y acceso a actualizaciones en curso. [!DNL Google Analytics] 4 es la solución de medición de nueva generación de Google y está reemplazando a [!DNL Universal Analytics]. El 1 de julio de 2023, las propiedades estándar de Universal Analytics dejarán de procesar nuevas visitas.

>[!NOTE]
>
>Si su empresa está sujeta a normas de privacidad como las siguientes [Reglamento general de protección de datos](../getting-started/compliance-gdpr.md) y/o el [California Consumer Privacy Act](../getting-started/compliance-ccpa.md), consulte [Configuración de privacidad de Google](google-tools.md#google-privacy-settings).

>[!IMPORTANT]
>
>Si activa la variable [Modo de restricción de cookies](../getting-started/compliance-cookie-law.md), [!DNL Google Analytics] no recopila datos sobre los visitantes a menos que hayan aceptado cookies.

## [!DNL Google Analytics] 4

{{gtag-api-note}}

### Paso 1: Configuración [!UICONTROL Google Analytics] 4

Si todavía no tiene un [!DNL Google Analytics] 4 para configurar su sitio, siga uno de estos métodos:

- [Configure la recopilación de datos de Analytics por primera vez](https://support.google.com/analytics/answer/9304153)
- [Añadir Google Analytics 4 a un sitio con [!DNL Universal Analytics]](https://support.google.com/analytics/answer/9744165)

### Paso 2: Completar la configuración de Commerce

1. Inicie sesión en el administrador de su tienda de Commerce.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Google API]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Google GTag]** sección.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Google Analytics4]** y haga lo siguiente:

   - Establecer **[!UICONTROL Enable]** hasta `Yes`.

   - Deje el **[!UICONTROL Account type]** as `Google Analytics4`.

   - Introduzca su **[!UICONTROL Measurement ID]**. Para obtener más información, consulte [Ayuda para Google Analytics](https://support.google.com/analytics/answer/9539598).

   - Si desea realizar pruebas A/B y otras pruebas de rendimiento en el contenido, establezca **Experimentos de contenido** hasta `Yes`.

   ![Configuración de ventas - API de Google para Google Analytics 4](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Google Universal Analytics

>[!IMPORTANT]
>
>El 1 de julio de 2023, las propiedades estándar de Universal Analytics dejarán de procesar datos. Si sigue confiando en [!DNL Universal Analytics], se recomienda que [preparar para usar Google Analytics 4](https://support.google.com/analytics/answer/10759417) en adelante.

### Paso 1: Configuración de Google Universal Analytics

Visite el sitio web de Google y regístrese para obtener una [Google Universal Analytics][1] cuenta.

### Paso 2: Completar la configuración de Commerce

1. Inicie sesión en el administrador de su tienda de Commerce.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Google API]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Google Analytics]** y haga lo siguiente:

   - Establecer **[!UICONTROL Enable]** hasta `Yes`.

   - Introduzca su [!DNL Google Analytics] **[!UICONTROL Account Number]**.

   - Si desea realizar pruebas A/B y otras pruebas de rendimiento en el contenido, establezca **[!UICONTROL Content Experiments]** hasta `Yes`.

   ![Configuración de ventas - API de Google - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Comercio electrónico mejorado

Enhanced Ecommerce es un complemento para [!DNL Google Universal Analytics] esto le ofrece una perspectiva del comportamiento de compra de sus clientes. Puede utilizar el comercio electrónico mejorado para generar informes sobre actividades clave de los clientes, como cuándo los clientes agregan artículos al carro de compras, comienzan el proceso de cierre de compra o completan una compra. También puede identificar y analizar los patrones de los compradores que abandonan su carro de compras sin realizar una compra.

Las siguientes instrucciones muestran cómo configurar [!DNL Google Tag Manager] con [!DNL Universal Analytics] para producir informes y datos de comercio electrónico mejorados.

### Paso 1. Registrarse para cuentas de Google

1. Regístrese para obtener una [Google Tag Manager](google-tag-manager.md) y complete la configuración de Commerce.

1. Regístrese para obtener una nueva [Google Universal Analytics][1] cuenta.

### Paso 2. Configurar comercio electrónico mejorado

1. Inicie sesión en su cuenta de Google Universal Analytics.

1. Cree una propiedad para el análisis de comercio electrónico mejorado con la siguiente configuración:

   - Estado: ACTIVADO
   - Productos relacionados: ON
   - Habilitar los informes mejorados de comercio electrónico: ACTIVADO
   - Etiquetado de cierre de compra: (no obligatorio)

1. Cuando termine, haga clic en **[!UICONTROL Submit]**.

### Paso 3. Creación de etiquetas y déclencheur

1. Inicie sesión en su [!DNL Google Tag Manager] y cree las siguientes déclencheur:

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
   >El [!UICONTROL Checkout] se activa solo para los métodos de pago básicos integrados de Commerce (como `Check / Money Order` y `Cash On Delivery Payment`). Este evento no se ejecuta para `PayPal checkout` y otros métodos de pago externos, que utilizan la redirección al cierre de compra desde recursos externos.

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

   - Introduzca lo siguiente **[!UICONTROL Add to Cart]** configuración de seguimiento:

     | Configuración | Valor |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | Comercio electrónico |
     | [!UICONTROL Action] | Añadir al carro |
     | [!UICONTROL Trigger] | addToCart |

   - Introduzca lo siguiente **[!UICONTROL Checkout option]** configuración de seguimiento:

     | Configuración | Valor |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | Comercio electrónico |
     | [!UICONTROL Action] | Opción de extracción |
     | [!UICONTROL Trigger] | checkoutOption |

   - Introduzca lo siguiente **[!UICONTROL PageView]** configuración de seguimiento:

     | Configuración | Valor |
     |--- |--- |
     | [!UICONTROL Track Type] | PageView |
     | [!UICONTROL Trigger] | gtm.dom |

   - Complete lo siguiente **[!UICONTROL Product Click]** configuración de seguimiento:

     | Configuración | Valor |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | Comercio electrónico |
     | [!UICONTROL Action] | Clic del producto |
     | [!UICONTROL Trigger] | productClick |

   - Complete lo siguiente **[!UICONTROL Promotion Click]** configuración de seguimiento:

     | Configuración | Valor |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | Comercio electrónico |
     | [!UICONTROL Action] | Clic de promoción |
     | [!UICONTROL Trigger] | promotionClick |

   - Complete lo siguiente **[!UICONTROL Remove from Cart]** configuración de seguimiento:

     | Configuración | Valor |
     |--- |--- |
     | [!UICONTROL Track Type] | Evento |
     | [!UICONTROL Category] | Comercio electrónico |
     | [!UICONTROL Action] | Eliminar del carro |
     | [!UICONTROL Trigger] | removeFromCart |

1. Cuando termine, haga clic en **[!UICONTROL Preview]** y compruebe que las etiquetas funcionan correctamente.

1. Después de comprobar la configuración, haga clic en **[!UICONTROL Publish]**.


[1]: https://support.google.com/analytics/answer/2817075?hl=en
