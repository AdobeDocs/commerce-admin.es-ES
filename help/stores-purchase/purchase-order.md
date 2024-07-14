---
title: Pedidos de compra
description: Aprenda a configurar pedidos de compra como un método de pago sin conexión en su tienda.
exl-id: 493c1b59-2155-449f-a08a-eb1aa2af9b3e
feature: Purchase Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Pedidos de compra

Un _pedido de compra_ (PC) permite a los clientes comerciales pagar las compras autorizadas haciendo referencia al número de PC. La orden de compra está autorizada y emitida por adelantado por la compañía que realiza la compra. Durante el cierre de compra, el cliente elige el pedido de compra como forma de pago. Una vez recibida la factura, la empresa procesa el pago en su sistema de cuentas a pagar y paga la compra.

Antes de aceptar el pago por orden de compra, establezca siempre la solvencia del cliente comercial.

**_Para configurar el pago por pedido de compra:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Payment Methods]**.

1. En _[!UICONTROL Other Payment Methods]_, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Purchase Order]**.

   ![Pedido de compra](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   Para obtener una descripción detallada de cada una de estas opciones de configuración, consulte [Pedido de compra](../configuration-reference/sales/payment-methods.md#purchase-order) en la _Guía de referencia de configuración_.

   >[!NOTE]
   >
   >Si es necesario, primero borre la casilla de verificación **[!UICONTROL Use system value]** para cambiar esta configuración.

1. Para activar este método de pago, establezca **[!UICONTROL Enabled]** en `Yes`.

1. Para **[!UICONTROL Title]**, escribe un título que identifique este método de pago durante el cierre de compra.

1. Establezca **[!UICONTROL New Order Status]** en `Pending` hasta que se autorice el pago.

1. Establezca **[!UICONTROL Payment from Applicable Countries]** en una de las siguientes opciones:

   - `All Allowed Countries`: los clientes de todos los [países](../getting-started/store-details.md#country-options) especificados en la configuración de su tienda pueden usar este método de pago.
   - `Specific Countries` - Después de elegir esta opción, aparece la lista _[!UICONTROL Payment from Specific Countries]_. Para seleccionar varios países, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

1. Establezca **[!UICONTROL Minimum Order Total]** y **[!UICONTROL Maximum Order Total]** a los montos requeridos para calificar para este método de pago.

   >[!NOTE]
   >
   >Una solicitud cualifica si el total se encuentra entre los valores totales mínimo o máximo, o si coincide exactamente con ellos.

1. Para **[!UICONTROL Sort Order]**, escribe un número que determine la posición de este artículo en la lista de métodos de pago que se muestra durante el cierre de compra.

   Este número es relativo a las otras formas de pago. (`0` = primero, `1` = segundo, `2` = tercero, etc.)

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
