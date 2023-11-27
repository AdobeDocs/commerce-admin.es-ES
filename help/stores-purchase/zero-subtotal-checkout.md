---
title: Cierre de compra de subtotal cero
description: Aprenda a configurar un subtotal cero como método de pago sin conexión en su tienda.
exl-id: c14ce289-8292-41d9-a448-f493c784f35c
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Cierre de compra de subtotal cero

_Cierre de compra de subtotal cero_ se puede utilizar para pedidos con un subtotal de cero que se gravan después de aplicar un descuento. Por ejemplo, el cierre de compra de subtotales cero se puede utilizar en las siguientes situaciones:

- Un descuento cubre el precio total de la compra, sin cargo adicional por envío.

- El cliente añade una [descargable](../catalog/product-create-downloadable.md) o [virtual](../catalog/product-create-virtual.md) producto al carro de compras y el precio es igual a cero.

- El precio de un [simple](../catalog/product-create-simple.md) el producto es cero y la [envío gratuito](shipping-free.md) método está disponible.

- A [código de cupón](../merchandising-promotions/price-rules-cart-coupon.md) cubre el precio total de los productos y el envío.

Para ahorrar tiempo, se puede establecer que el subtotal de pedidos cero se factura automáticamente.

**_Para configurar la desprotección de subtotales cero:_**

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Payment Methods]**.

1. En _[!UICONTROL Other Payment Methods]_, expanda ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Zero Subtotal Checkout]**sección.

   ![Cierre de compra con subtotal cero](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si es necesario, borre primero la **[!UICONTROL Use system value]** para cambiar esta configuración.

1. Para activar el cierre de compra de subtotales cero, establezca **[!UICONTROL Enabled]** hasta `Yes`.

1. Para **[!UICONTROL Title]**, introduzca un título que identifique el método de subtotal cero durante el cierre de compra.

1. Si las solicitudes suelen esperar la aprobación, acepte el valor predeterminado **[!UICONTROL New Order Status]** as `Pending"` hasta que se apruebe la solicitud.

   Si lo prefiere, puede utilizar el `Processing` o `Suspected Fraud` estado de los nuevos pedidos con esta forma de pago.

1. Establecer **[!UICONTROL Automatically Invoice All Items]** hasta `Yes` si desea facturar automáticamente todos los artículos con saldo cero.

   Esta opción solo está disponible si la variable **[!UICONTROL New Order Status]** se establece en `Processing`.

   >[!NOTE]
   >
   >If _[!UICONTROL New Order Status]_se establece en `Processing` y_[!UICONTROL Automatically Invoice All Items]_ se establece en `No`, también debe asignar **[!UICONTROL Order Status]** = `Processing` para el **[!UICONTROL Order State]** = `Pending` y **[!UICONTROL Default Status]** = `No` asignación en el [Estado del pedido](order-status.md#custom-order-status) página.

1. Establecer **[!UICONTROL Payment from Applicable Countries]** a uno de los siguientes:

   - `All Allowed Countries` - Clientes de todos [países](../getting-started/store-details.md#country-options) especificado en la configuración de tu tienda puede utilizar este método de pago.
   - `Specific Countries` - Después de elegir esta opción, la variable _[!UICONTROL Payment from Specific Countries]_aparece una lista. Para seleccionar varios países, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

1. Para **[!UICONTROL Sort Order]**, introduce un número que determina la posición de este artículo en la lista de métodos de pago que se muestra durante el pago y envío.

   Este número es relativo a las otras formas de pago. (`0` = primero, `1` = segundo, `2` = tercero, etc.)

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.
