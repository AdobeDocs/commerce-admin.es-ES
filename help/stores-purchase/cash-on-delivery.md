---
title: Pago contra reembolso (COD)
description: Aprenda a configurar el pago contra reembolso como método de pago sin conexión en su tienda.
exl-id: dcf94734-a66e-4d32-b389-b47c979ceaa9
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Pago contra reembolso (COD)

Adobe Commerce y Magento Open Source permiten aceptar _pago contra reembolso_ (COD) pagos por compras. Solo puede aceptar pagos contra reembolso de países específicos, y puede ajustar la configuración con límites totales de pedidos mínimos y máximos.

El transportista recibe el pago del cliente en el momento de la entrega, que luego se transfiere a usted. Puedes hacer un ajuste por cualquier cargo cobrado por el servicio de transporte en tus gastos de envío y manipulación.

**_Para configurar los pagos de efectivo en la entrega:_**

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Payment Methods]**.

1. En _Otros métodos de pago_, expanda ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Cash On Delivery Payment]** sección.

   ![Pago contra reembolso](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   Para obtener una descripción detallada de cada una de estas opciones de configuración, consulte [Pago contra reembolso](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment) en el _Guía de referencia de configuración_.

   >[!NOTE]
   >
   >Si es necesario, borre primero la **[!UICONTROL Use system value]** para cambiar esta configuración.

1. Para activar el pago contra reembolso, configure **[!UICONTROL Enabled]** hasta `Yes`.

1. Para **[!UICONTROL Title]**, introduzca un título que identifique el método de pago contra reembolso durante el pago.

1. Establecer **[!UICONTROL New Order Status]** hasta `Pending` hasta que se confirme la recepción del pago.

   Si lo prefiere, puede utilizar el `Processing` o `Suspected Fraud` estado de los nuevos pedidos con esta forma de pago.

1. Establecer **[!UICONTROL Payment from Applicable Countries]** a uno de los siguientes:

   - `All Allowed Countries` - Clientes de todos [países](../getting-started/store-details.md#country-options) especificado en la configuración de tu tienda puede utilizar este método de pago.
   - `Specific Countries` - Después de elegir esta opción, la variable _[!UICONTROL Payment from Specific Countries]_aparece una lista. Para seleccionar varios países, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

1. Introduzca el **[!UICONTROL Instructions]** para aceptar la entrega de un pedido de COD.

1. Establecer **[!UICONTROL Minimum Order Total]** y **[!UICONTROL Maximum Order Total]** a los importes de pedido necesarios para poder optar al pago contra reembolso.

   >[!NOTE]
   >
   >Un pedido indica si el total está entre el total de pedido mínimo o máximo, o si coincide con él.

1. Para **[!UICONTROL Sort Order]**, introduce un número que determina la posición de este artículo en la lista de métodos de pago que se muestra durante el pago y envío.

   Este número es relativo a las otras formas de pago. (`0` = primero, `1` = segundo, `2` = tercero, etc.)

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.
