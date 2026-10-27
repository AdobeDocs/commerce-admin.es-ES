---
title: Orden de los totales de cierre de compra
description: Obtenga información sobre el total de cierre de compra mostrado y cómo configurar el orden de los totales de cierre de compra en el resumen del pedido.
exl-id: 2b1345e3-6ad3-472a-af3e-3f7b24577b13
feature: Checkout, Configuration
TQID: 'https://experienceleague.adobe.com/cXt3dbS5Jd8baKFk8K8HP1Cypk1oMS85iCq-WZ8cIgg'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 8cd50456-5eb0-5364-922a-f14161feb828
    internal-label: Checkout
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9d3fe9829bb5a7f2a75ad3c89edd38010f816a0c
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%
---
# Orden de los totales de cierre de compra

Durante la revisión del pedido, el total aparece en la parte inferior del pedido, con ajustes por descuentos, gastos de envío, crédito de tienda e impuestos. El orden de cada elemento determina la secuencia de los cálculos y se establece en la configuración mediante un número asignado a cada elemento. Por ejemplo, el subtotal es el primer elemento de la sección y se le asigna un valor de 10. El Total general aparece en último lugar y se asigna un valor de 100. A todos los demás elementos de la sección de totales se les asigna un valor entre esos valores.

![Resumen de pedidos muestra el total de cierres de compra](./assets/storefront-checkout-totals.png){width="700" zoomable="yes"}

**_Para configurar el criterio de ordenación de totales de desprotección:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > **[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda la sección **[!UICONTROL Sales]** y elija **[!UICONTROL Sales]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Checkout Totals Sort Order]**.

   ![Se han numerado las opciones de totales de desprotección para determinar el criterio de ordenación](../configuration-reference/sales/assets/sales-checkout-totals-sort-order.png){width="600" zoomable="yes"}

   Para obtener una descripción detallada de cada una de estas opciones de configuración, consulte [Orden de clasificación de totales de desprotección](../configuration-reference/sales/sales.md#checkout-totals-sort-order) en la _Guía de referencia de configuración_.

1. Si la configuración es para una vista de tienda específica, [elija la vista de tienda](../configuration-reference/scope-change.md#set-the-scope) donde se aplica la configuración.

   Cuando se le solicite, haga clic en **[!UICONTROL OK]** para continuar.

1. Para determinar el orden en la sección _Totales_, cambie el número asignado a cada elemento.

   Cuanto más bajo sea el valor, antes se colocará en la lista. En la configuración predeterminada, el subtotal (`10`) es el primero y el total general (`100`) es el último.

   Si es necesario, desactive la casilla de verificación **[!UICONTROL Use system value]** para completar estos cambios.

1. Haga clic en **[!UICONTROL Save Config]**.
