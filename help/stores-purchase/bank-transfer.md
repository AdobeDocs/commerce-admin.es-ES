---
title: Transferencias bancarias
description: Aprenda a configurar transferencias bancarias como un método de pago sin conexión en su tienda.
exl-id: 34b2163c-2edd-4741-b002-3d8fb561fc78
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# Transferencias bancarias

Adobe Commerce y Magento Open Source permiten aceptar pagos transferidos desde una cuenta bancaria de cliente y depositados en su cuenta bancaria de comerciante.

**_Para configurar los pagos de transferencia bancaria:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Payment Methods]**.

1. En _Otros métodos de pago_, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Bank Transfer Payment]**.

   ![Pago de transferencia bancaria](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si es necesario, primero borre la casilla de verificación **[!UICONTROL Use system value]** para cambiar esta configuración.

1. Para activar las transferencias bancarias, establezca **[!UICONTROL Enabled]** en `Yes`.

1. Para **[!UICONTROL Title]**, escribe un título que identifique el método de pago de transferencia bancaria durante el cierre de compra.

1. Establezca **[!UICONTROL New Order Status]** en `Pending` hasta que se autorice el pago.

1. Establezca **[!UICONTROL Payment from Applicable Countries]** en una de las siguientes opciones:

   - `All Allowed Countries`: los clientes de todos los [países](../getting-started/store-details.md#country-options) especificados en la configuración de su tienda pueden usar este método de pago.

   - `Specific Countries` - Después de elegir esta opción, aparece la lista _[!UICONTROL Payment from Specific Countries]_. Para seleccionar varios países, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

1. Escriba el **[!UICONTROL Instructions]** que sus clientes deben seguir para configurar una transferencia bancaria.

   Según el país donde se encuentre su banco y los requisitos del banco, puede incluir la siguiente información:

   - Nombre de cuenta bancaria
   - Número de cuenta bancaria
   - Código de enrutamiento bancario
   - Nombre del banco
   - Dirección bancaria

1. Establezca **[!UICONTROL Minimum Order Total]** y **[!UICONTROL Maximum Order Total]** a los montos requeridos para calificar para usar este método de pago.

   >[!NOTE]
   >
   >Una solicitud cualifica si el total se encuentra entre los valores totales mínimo o máximo, o si coincide exactamente con ellos.

1. Para **[!UICONTROL Sort Order]**, escribe un número que determine la posición de este artículo en la lista de métodos de pago que se muestra durante el cierre de compra.

   Este número es relativo a las otras formas de pago. (`0` = primero, `1` = segundo, `2` = tercero, etc.)

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
