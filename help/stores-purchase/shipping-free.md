---
title: Envío gratuito
description: Aprenda a configurar una opción de envío gratuito para su tienda.
exl-id: 3ce69583-0f7f-4c23-b3e3-7d2502bc1bca
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Envío gratuito

_Envío gratuito_ es una de las promociones más efectivas que puedes ofrecer. Puede basarse en una compra mínima o configurarse como [regla de precios de carrito](../merchandising-promotions/price-rules-cart.md) que se aplica cuando se cumple un conjunto de condiciones. Si ambos se aplican al mismo orden, la configuración tiene prioridad sobre la regla de carro de compras.

>[!NOTE]
>
>Consulta la configuración de tu transportista para ver si se requiere alguna configuración adicional para el envío gratuito.

## Paso 1: Configurar el envío gratuito

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Delivery Methods]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Free Shipping]** sección.

   >[!NOTE]
   >
   >Si es necesario, anule primero la selección del **[!UICONTROL Use system value]** para cambiar la siguiente configuración como se describe.

1. Establecer **[!UICONTROL Enabled]** hasta `Yes`.

1. Para **[!UICONTROL Title]**, introduce un título que identifique el método de envío gratuito durante el pago y un **[!UICONTROL Method Name]** para describirlo.

1. Para **[!UICONTROL Minimum Order Amount]**, introduce el valor total mínimo que se ajuste al envío gratuito.

   >[!TIP]
   >
   >Para utilizar el envío gratuito con [tarifas de tabla](shipping-table-rate.md), realice la _[!UICONTROL Minimum Order Amount]_tan alto que nunca se cumple. El uso de este valor alto impide que el envío gratuito entre en vigor, a menos que se active por una regla de precio.

1. Establecer **[!UICONTROL Include Tax to Amount]**:

   - `Yes` - Incluye impuestos al calcular el importe mínimo de pedido (subtotal + impuesto - descuento).
   - `No` - No incluye impuestos al calcular el importe mínimo de pedido (subtotal - descuento).

   ![Envío gratuito](../configuration-reference/sales/assets/delivery-methods-free-shipping.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Displayed Error Message]**, escribe el mensaje que aparecerá si el envío gratuito deja de estar disponible.

1. Establecer **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - Clientes de todos [países](../getting-started/store-details.md#country-options) especificado en la configuración de tu tienda puede utilizar el envío gratuito.

   - `Specific Countries` : Después de elegir este valor, la variable _[!UICONTROL Ship to Specific Countries]_aparece una lista. Selecciona cada país de la lista donde se puede utilizar el envío gratuito.

1. Establecer **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes` - Siempre muestra el método de envío gratuito, incluso cuando no es aplicable.
   - `No` - Muestra el método de envío gratuito solo cuando corresponde.

1. Para **[!UICONTROL Sort Order]**, introduce el número que determina la posición de envío gratuito en la lista de métodos de envío durante el pago.

   `0` = primero, `1` = segundo, `2` = tercero, etc.

1. Haga clic **[!UICONTROL Save Config]**.

## Paso 2: Habilitar el envío gratuito en la configuración del operador

Asegúrese de completar cualquier configuración que sea necesaria para cada transportista que planee utilizar para el envío gratuito. Por ejemplo, si su [Configuración de UPS](ups.md) si no se completa, actualiza la siguiente configuración para habilitar y configurar el envío gratuito.

1. En el _[!UICONTROL Delivery Methods]_configuración, expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL UPS]**sección.

1. Establecer **[!UICONTROL Free Method]** hasta `UPS Ground` u otro tipo que desee designar para el envío gratuito.

1. Para requerir un pedido mínimo para el envío gratuito, establezca **[!UICONTROL Enable Free Shipping Threshold]** hasta `Enable`.

   Si decide utilizar un pedido mínimo, introduzca la cantidad necesaria para **[!UICONTROL Free Shipping Amount Threshold]**.

1. Haga clic **[!UICONTROL Save Config]**.
