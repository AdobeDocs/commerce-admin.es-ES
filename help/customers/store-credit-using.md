---
title: Aplicar crédito de tienda
description: Los administradores de tienda pueden aplicar crédito de tienda a una compra.
exl-id: 97b6b206-71db-435c-8736-a781437bb0b4
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Aplicar crédito de tienda

{{ee-feature}}

Los administradores de tienda pueden ver el saldo y el historial de crédito desde la cuenta del cliente y también aplicar el crédito de tienda a una compra.

![Historial y saldo de crédito del cliente](assets/store-credit-balance-history.png){width="600" zoomable="yes"}

## Ver el saldo de crédito

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Busque al cliente en la cuadrícula.

1. En la columna _Acción_, haga clic en **[!UICONTROL Edit]**.

1. Desplácese _[!UICONTROL Customer View]_&#x200B;página y vea **[!UICONTROL Store Credit Balance]**&#x200B;en la parte inferior.

![Saldo de crédito de tienda](assets/store-credit-balance.png){width="600" zoomable="yes"}

## Actualizar saldo de crédito del almacén

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > _Operaciones_ > **[!UICONTROL All Customers]**.

1. Busque al cliente en la cuadrícula.

1. En la columna _Acción_, haga clic en **[!UICONTROL Edit]**.

1. En el panel izquierdo, elija **[!UICONTROL Store Credit]**.

1. Elija el sitio web (tienda) que desea asociar con el saldo.

1. Para **[!UICONTROL Update Balance]**, escriba el nuevo valor.

1. Para notificar al cliente la actualización del saldo, active la casilla de verificación **[!UICONTROL Notify Customer by Email]** y elija la vista de tienda de **[!UICONTROL Send Email Notification From the Following Store View]**.

1. Escriba **[!UICONTROL Comment]** acerca del cambio.

1. Cuando se hayan completado las actualizaciones, haga clic en **[!UICONTROL Save and Continue Edit]** o **[!UICONTROL Save Customer]**.

El saldo actualizado se debe mostrar en **[!UICONTROL Balance History]**.

## Aplicar un saldo acreedor a un pedido como administrador de tienda

Como administrador de tienda, puede hacer varias cosas en nombre de un cliente, incluido el envío de pedidos. Cuando [crea un pedido](../stores-purchase/customer-account-create-order.md), puede aplicar un saldo de crédito de tienda que se debe al cliente. El saldo disponible se muestra en la sección _Información de pago y envío_. Seleccione la casilla de verificación **[!UICONTROL Use Store Credit]** para aplicar el saldo o una parte del saldo si el total del pedido es menor.

![Aplicar el saldo de crédito de tienda al pedido](assets/store-credit-apply.png){width="500" zoomable="yes"}

## Aplicar crédito de tienda durante el cierre

Si hay un saldo de crédito para el sitio, el cliente puede aplicar crédito de tienda al saldo del pedido antes de colocar el pedido en la tienda.

1. El cliente consulta la cantidad de crédito de tienda disponible.

   Durante el paso _Revisar y pagar_, la cantidad disponible aparece en _[!UICONTROL Store Credit]_.

1. Para aplicar la cantidad al pedido, haga clic en **[!UICONTROL Use Store Credit]**.

   >[!INFO]
   >
   >El total del pedido se vuelve a calcular y la cantidad de crédito del almacén que se aplica aparece en _[!UICONTROL Order Summary]_.

   ![Saldo de crédito de almacenamiento aplicado al pedido](assets/store-credit-checkout.png){width="700" zoomable="yes"}

1. Cuando esté listo, haga clic en **[!UICONTROL Place Order]**.
