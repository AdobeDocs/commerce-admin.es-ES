---
title: Envío gratuito
description: Aprenda a configurar una opción de envío gratuito para su tienda.
exl-id: 3ce69583-0f7f-4c23-b3e3-7d2502bc1bca
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Envío gratuito

_Envío gratuito_ es una de las promociones más efectivas que puedes ofrecer. Se puede basar en una compra mínima o configurarse como una [regla de precio del carro de compras](../merchandising-promotions/price-rules-cart.md) que se aplica cuando se cumple un conjunto de condiciones. Si ambos se aplican al mismo orden, la configuración tiene prioridad sobre la regla de carro de compras.

>[!NOTE]
>
>Consulta la configuración de tu transportista para ver si se requiere alguna configuración adicional para el envío gratuito.

## Paso 1: Configurar el envío gratuito

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Delivery Methods]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Free Shipping]**.

   >[!NOTE]
   >
   >Si es necesario, anule primero la selección de la casilla de verificación **[!UICONTROL Use system value]** para cambiar la siguiente configuración como se describe a continuación.

1. Establezca **[!UICONTROL Enabled]** en `Yes`.

1. Para **[!UICONTROL Title]**, escriba un título que identifique el método de envío gratuito durante el cierre de compra y un **[!UICONTROL Method Name]** para describirlo.

1. Para **[!UICONTROL Minimum Order Amount]**, ingrese el valor total mínimo que califica para el envío gratuito.

   >[!TIP]
   >
   >Para usar el envío gratuito con [tarifas de tabla](shipping-table-rate.md), haga que _[!UICONTROL Minimum Order Amount]_&#x200B;sea tan alto que nunca se cumpla. El uso de este valor alto impide que el envío gratuito entre en vigor, a menos que se active por una regla de precio.

1. Establecer **[!UICONTROL Include Tax to Amount]**:

   - `Yes` - Incluye impuestos al calcular el importe mínimo de pedido (subtotal + impuestos - descuento).
   - `No` - No incluye impuestos al calcular el importe mínimo de pedido (Subtotal - Descuento).

   ![Envío gratuito](../configuration-reference/sales/assets/delivery-methods-free-shipping.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Displayed Error Message]**, ingrese el mensaje que aparecerá si el envío gratuito deja de estar disponible.

1. Establecer **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - Los clientes de todos los [países](../getting-started/store-details.md#country-options) especificados en la configuración de tu tienda pueden usar el envío gratis.

   - `Specific Countries` - Después de elegir este valor, aparece la lista _[!UICONTROL Ship to Specific Countries]_. Selecciona cada país de la lista donde se puede utilizar el envío gratuito.

1. Establecer **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes`: siempre muestra el método de envío gratuito, aunque no sea aplicable.
   - `No`: muestra el método de envío gratuito solo cuando corresponde.

1. Para **[!UICONTROL Sort Order]**, escriba el número que determina la posición del envío gratuito en la lista de métodos de envío durante el cierre de compra.

   `0` = primero, `1` = segundo, `2` = tercero, etc.

1. Haga clic en **[!UICONTROL Save Config]**.

## Paso 2: Habilitar el envío gratuito en la configuración del operador

Asegúrese de completar cualquier configuración que sea necesaria para cada transportista que planee utilizar para el envío gratuito. Por ejemplo, si la [configuración de UPS](ups.md) se ha completado, actualice la siguiente configuración para habilitar y configurar el envío gratuito.

1. En la configuración de _[!UICONTROL Delivery Methods]_, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL UPS]**.

1. Establezca **[!UICONTROL Free Method]** en `UPS Ground` o en otro tipo que desee designar para el envío gratuito.

1. Para requerir un pedido mínimo para el envío gratuito, establezca **[!UICONTROL Enable Free Shipping Threshold]** en `Enable`.

   Si decide utilizar un pedido mínimo, escriba la cantidad necesaria para **[!UICONTROL Free Shipping Amount Threshold]**.

1. Haga clic en **[!UICONTROL Save Config]**.
