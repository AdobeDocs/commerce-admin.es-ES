---
title: Pedidos de compra
description: Aprenda a configurar pedidos de compra como un método de pago sin conexión en su tienda.
exl-id: 493c1b59-2155-449f-a08a-eb1aa2af9b3e
feature: Purchase Orders
TQID: https://experienceleague.adobe.com/Oc2vdP-OTXwo-6cjKWFj5zPf-QJVvU8aK6OUMPko4eY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 296
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
