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

Adobe Commerce y Magento Open Source permiten aceptar pagos mediante cheque o giro postal. El _Cheque / giro postal_ la forma de pago está activada de forma predeterminada en tu tienda. Solo puede aceptar cheques y giros postales de países específicos, y puede ajustar la configuración con límites totales de pedidos mínimos y máximos.

**_Para configurar el pago mediante cheque o giro postal:_**

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Payment Methods]**.

1. En _[!UICONTROL Other Payment Methods]_, expanda ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Check / Money Order]**sección.

   ![Cheque / giro postal](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   Para obtener una descripción detallada de cada una de estas opciones de configuración, consulte [Cheque / giro postal](../configuration-reference/sales/payment-methods.md#check--money-order) en el _Guía de referencia de configuración_.

   >[!NOTE]
   >
   >Si es necesario, borre primero la **[!UICONTROL Use system value]** para cambiar esta configuración.

1. Para aceptar el pago mediante cheque o giro postal, establezca **[!UICONTROL Enabled]** hasta `Yes`.

1. Para **[!UICONTROL Title]**, introduzca un título que identifique el método de pago del cheque/giro postal durante el pago.

1. Si las solicitudes suelen esperar la aprobación, acepte el valor predeterminado **[!UICONTROL New Order Status]** as `Pending"` hasta que se apruebe.

   Si lo prefiere, puede utilizar el `Processing` o `Suspected Fraud` estado de los nuevos pedidos con esta forma de pago.

1. Establecer **[!UICONTROL Payment from Applicable Countries]** a uno de los siguientes:

   - `All Allowed Countries` - Clientes de todos [países](../getting-started/store-details.md#country-options) especificado en la configuración de tu tienda puede utilizar este método de pago.
   - `Specific Countries` - Después de elegir esta opción, la variable _[!UICONTROL Payment from Specific Countries]_aparece una lista. Para seleccionar varios países, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

1. Para **[!UICONTROL Make Check Payable To]**, introduzca el nombre de la parte a la que debe pagarse el cheque.

1. Para **[!UICONTROL Send Check To]**, introduzca la dirección de la calle o el apartado de correos donde se envían los cheques.

1. Establecer **[!UICONTROL Minimum Order Total]** y **[!UICONTROL Maximum Order Total]** a los importes de pedido necesarios para cumplir los requisitos de este método de pago.

   >[!NOTE]
   >
   >Una solicitud cualifica si el total se encuentra entre los valores totales mínimo o máximo, o si coincide exactamente con ellos.

1. Para **[!UICONTROL Sort Order]**, introduce un número que determina la posición de este artículo en la lista de métodos de pago que se muestra durante el pago y envío.

   Este número es relativo a las otras formas de pago. (`0` = primero, `1` = segundo, `2` = tercero, etc.)

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.
