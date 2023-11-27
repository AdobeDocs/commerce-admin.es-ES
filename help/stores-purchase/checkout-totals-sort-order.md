---
title: Orden de los totales de cierre de compra
description: Obtenga información sobre el total de cierre de compra mostrado y cómo configurar el orden de los totales de cierre de compra en el resumen del pedido.
exl-id: 2b1345e3-6ad3-472a-af3e-3f7b24577b13
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# Orden de los totales de cierre de compra

Durante la revisión del pedido, el total aparece en la parte inferior del pedido, con ajustes por descuentos, gastos de envío, crédito de tienda e impuestos. El orden de cada elemento determina la secuencia de los cálculos y se establece en la configuración mediante un número asignado a cada elemento. Por ejemplo, el subtotal es el primer elemento de la sección y se le asigna un valor de 10. El Total general aparece en último lugar y se asigna un valor de 100. A todos los demás elementos de la sección de totales se les asigna un valor entre esos valores.

![Resumen de pedidos muestra el total de cierre de compra](./assets/storefront-checkout-totals.png){width="700" zoomable="yes"}

**_Para configurar el orden de los totales de cierre de compra:_**

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Sales]** debajo.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Checkout Totals Sort Order]** sección.

   ![Opciones de totales de desprotección numeradas para determinar el criterio de ordenación](../configuration-reference/sales/assets/sales-checkout-totals-sort-order.png){width="600" zoomable="yes"}

   Para obtener una descripción detallada de cada una de estas opciones de configuración, consulte [Orden de totales de cierre](../configuration-reference/sales/sales.md#checkout-totals-sort-order) en el _Guía de referencia de configuración_.

1. Si la configuración es para una vista de tienda específica, [elija la vista de la tienda](../configuration-reference/scope-change.md#set-the-scope) donde se aplica la configuración.

   Cuando se le solicite, haga clic en **[!UICONTROL OK]** para continuar.

1. Para determinar el orden en _Totales_ , cambie el número asignado a cada elemento.

   Cuanto más bajo sea el valor, antes se colocará en la lista. En la configuración predeterminada, el subtotal (`10`) es el primer total y el general (`100`) es la última.

   Si es necesario, borre la **[!UICONTROL Use system value]** para completar estos cambios.

1. Haga clic **[!UICONTROL Save Config]**.
