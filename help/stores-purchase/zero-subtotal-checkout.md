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

Se puede usar _Pago y envío sin subtotal_ para pedidos con un subtotal de cero que se gravan después de aplicar un descuento. Por ejemplo, el cierre de compra de subtotales cero se puede utilizar en las siguientes situaciones:

- Un descuento cubre el precio total de la compra, sin cargo adicional por envío.

- El cliente agrega un producto [descargable](../catalog/product-create-downloadable.md) o [virtual](../catalog/product-create-virtual.md) al carro de compras, y el precio es igual a cero.

- El precio de un producto [simple](../catalog/product-create-simple.md) es cero y el método de [envío gratis](shipping-free.md) está disponible.

- Un [código de cupón](../merchandising-promotions/price-rules-cart-coupon.md) cubre el precio total de los productos y del envío.

Para ahorrar tiempo, se puede establecer que el subtotal de pedidos cero se factura automáticamente.

**_Para configurar el cierre de compra de subtotales cero:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Payment Methods]**.

1. En _[!UICONTROL Other Payment Methods]_, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Zero Subtotal Checkout]**.

   ![Cierre de compra con subtotal cero](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si es necesario, primero borre la casilla de verificación **[!UICONTROL Use system value]** para cambiar esta configuración.

1. Para activar el cierre de compra de subtotales cero, establezca **[!UICONTROL Enabled]** en `Yes`.

1. Para **[!UICONTROL Title]**, escriba un título que identifique el método de subtotal cero durante el cierre de compra.

1. Si los pedidos suelen esperar la aprobación, acepte el valor predeterminado **[!UICONTROL New Order Status]** como `Pending"` hasta que se apruebe el pedido.

   Si lo prefiere, puede utilizar el estado `Processing` o `Suspected Fraud` para nuevos pedidos con esta forma de pago.

1. Establezca **[!UICONTROL Automatically Invoice All Items]** en `Yes` si desea facturar automáticamente todos los artículos que tienen un saldo cero.

   Esta opción solo está disponible si la opción **[!UICONTROL New Order Status]** está establecida en `Processing`.

   >[!NOTE]
   >
   >Si _[!UICONTROL New Order Status]_se establece en `Processing` y_[!UICONTROL Automatically Invoice All Items]_ se establece en `No`, también debe asignar **[!UICONTROL Order Status]** = `Processing` para la asignación **[!UICONTROL Order State]** = `Pending` y **[!UICONTROL Default Status]** = `No` en la página [Estado del pedido](order-status.md#custom-order-status).

1. Establezca **[!UICONTROL Payment from Applicable Countries]** en una de las siguientes opciones:

   - `All Allowed Countries`: los clientes de todos los [países](../getting-started/store-details.md#country-options) especificados en la configuración de su tienda pueden usar este método de pago.
   - `Specific Countries` - Después de elegir esta opción, aparece la lista _[!UICONTROL Payment from Specific Countries]_. Para seleccionar varios países, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

1. Para **[!UICONTROL Sort Order]**, escribe un número que determine la posición de este artículo en la lista de métodos de pago que se muestra durante el cierre de compra.

   Este número es relativo a las otras formas de pago. (`0` = primero, `1` = segundo, `2` = tercero, etc.)

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
