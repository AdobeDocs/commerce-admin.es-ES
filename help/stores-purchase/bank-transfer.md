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

**_Para configurar pagos de transferencia bancaria:_**

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Payment Methods]**.

1. En _Otros métodos de pago_, expanda ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Bank Transfer Payment]** sección.

   ![Pago de transferencia bancaria](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si es necesario, borre primero la **[!UICONTROL Use system value]** para cambiar esta configuración.

1. Para activar transferencias bancarias, establezca **[!UICONTROL Enabled]** hasta `Yes`.

1. Para **[!UICONTROL Title]**, introduce un título que identifique el método de pago de la transferencia bancaria durante el proceso de pago.

1. Establecer **[!UICONTROL New Order Status]** hasta `Pending` hasta que se autorice el pago.

1. Establecer **[!UICONTROL Payment from Applicable Countries]** a uno de los siguientes:

   - `All Allowed Countries` - Clientes de todos [países](../getting-started/store-details.md#country-options) especificado en la configuración de tu tienda puede utilizar este método de pago.

   - `Specific Countries` - Después de elegir esta opción, la variable _[!UICONTROL Payment from Specific Countries]_aparece una lista. Para seleccionar varios países, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

1. Introduzca el **[!UICONTROL Instructions]** que los clientes deben seguir para configurar una transferencia bancaria.

   Según el país donde se encuentre su banco y los requisitos del banco, puede incluir la siguiente información:

   - Nombre de cuenta bancaria
   - Número de cuenta bancaria
   - Código de enrutamiento bancario
   - Nombre del banco
   - Dirección bancaria

1. Establecer **[!UICONTROL Minimum Order Total]** y **[!UICONTROL Maximum Order Total]** a los importes necesarios para poder utilizar este método de pago.

   >[!NOTE]
   >
   >Una solicitud cualifica si el total se encuentra entre los valores totales mínimo o máximo, o si coincide exactamente con ellos.

1. Para **[!UICONTROL Sort Order]**, introduce un número que determina la posición de este artículo en la lista de métodos de pago que se muestra durante el pago y envío.

   Este número es relativo a las otras formas de pago. (`0` = primero, `1` = segundo, `2` = tercero, etc.)

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.
