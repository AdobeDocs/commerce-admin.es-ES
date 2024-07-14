---
title: Cheques y giro postal
description: Aprenda a configurar el cheque y el giro postal como un método de pago sin conexión en su tienda.
exl-id: e004f0c3-f659-4b08-a41a-88bfc05acaab
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Cheques y giro postal

Adobe Commerce y Magento Open Source permiten aceptar pagos mediante cheque o giro postal. El método de pago _cheque / giro postal_ está habilitado para tu tienda de forma predeterminada. Solo puede aceptar cheques y giros postales de países específicos, y puede ajustar la configuración con límites totales de pedidos mínimos y máximos.

**_Para configurar el pago mediante cheque o giro postal:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Payment Methods]**.

1. En _[!UICONTROL Other Payment Methods]_, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Check / Money Order]**.

   ![Cheque / giro postal](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   Para obtener una descripción detallada de cada una de estas opciones de configuración, consulte [Cheque / giro postal](../configuration-reference/sales/payment-methods.md#check--money-order) en la _Guía de referencia de configuración_.

   >[!NOTE]
   >
   >Si es necesario, primero borre la casilla de verificación **[!UICONTROL Use system value]** para cambiar esta configuración.

1. Para aceptar el pago mediante cheque o giro postal, establezca **[!UICONTROL Enabled]** en `Yes`.

1. Para **[!UICONTROL Title]**, escriba un título que identifique el método de pago del cheque o giro postal durante el cierre de compra.

1. Si los pedidos suelen esperar la aprobación, acepte el valor predeterminado **[!UICONTROL New Order Status]** como `Pending"` hasta que se apruebe.

   Si lo prefiere, puede utilizar el estado `Processing` o `Suspected Fraud` para nuevos pedidos con esta forma de pago.

1. Establezca **[!UICONTROL Payment from Applicable Countries]** en una de las siguientes opciones:

   - `All Allowed Countries`: los clientes de todos los [países](../getting-started/store-details.md#country-options) especificados en la configuración de su tienda pueden usar este método de pago.
   - `Specific Countries` - Después de elegir esta opción, aparece la lista _[!UICONTROL Payment from Specific Countries]_. Para seleccionar varios países, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

1. Para **[!UICONTROL Make Check Payable To]**, escriba el nombre de la parte a la que debe pagarse el cheque.

1. Para **[!UICONTROL Send Check To]**, escriba la dirección de la calle o el apartado de correos donde se enviarán los cheques.

1. Establezca **[!UICONTROL Minimum Order Total]** y **[!UICONTROL Maximum Order Total]** en los importes de pedido necesarios para calificar para este método de pago.

   >[!NOTE]
   >
   >Una solicitud cualifica si el total se encuentra entre los valores totales mínimo o máximo, o si coincide exactamente con ellos.

1. Para **[!UICONTROL Sort Order]**, escribe un número que determine la posición de este artículo en la lista de métodos de pago que se muestra durante el cierre de compra.

   Este número es relativo a las otras formas de pago. (`0` = primero, `1` = segundo, `2` = tercero, etc.)

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
