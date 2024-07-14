---
title: Segmentos de cliente en reglas de precios
description: Obtenga información acerca de la asociación de segmentos de clientes con una regla de precios de carro de compras para poder definir promociones segmentadas para su tienda.
exl-id: eaa04e7a-c0f9-4f09-8e65-75965ccbdc69
feature: Customers, Configuration, Price Rules
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---

# Segmentos de cliente en reglas de precios

{{ee-feature}}

Un segmento de cliente se puede usar para promociones segmentadas asociándolo con una [regla de precio del carro de compras](../merchandising-promotions/price-rules-cart.md).

![Regla de precio del carro de compras - segmento de clientes segmentados](assets/price-rule-cart-condition-segments.png){width="700" zoomable="yes"}

_**Para asociar un segmento con una regla de precios del carro de compras:**_

1. En la barra lateral de _Administración_, vaya a **[!UICONTROL Marketing]** > _Promociones_ > **[!UICONTROL Cart Price Rules]**.

1. Abra una regla nueva o existente:

   * Para usar una regla nueva, haga clic en **[!UICONTROL Add New Rule]** en la esquina superior derecha.
   * Para utilizar una regla existente, haga clic en la regla de la lista para abrirla en modo de edición.

1. Desplácese hacia abajo y expanda la sección **[!UICONTROL Conditions]**.

1. Añada la condición.

   * Haga clic en el icono _Agregar_ (![Icono de lista](../assets/icon-add-green-circle.png)), que muestra la lista de condiciones. A continuación, elija **[!UICONTROL Customer Segment]**.

   ![Regla de precio del carro de compras: agregar condición de segmento de cliente](assets/condition-customer-segment.png){width="600" zoomable="yes"}

   De forma predeterminada, la condición está configurada para encontrar una condición que coincida. Si es necesario, haga clic en el vínculo **[!UICONTROL matches]** y cambie el operador a uno de los siguientes:

   * `does not match`
   * `is one of`
   * `is not one of`

   ![Operador de condición](assets/price-rule-condition-customer-segment-operator.png){width="600" zoomable="yes"}

1. Para dirigirse a un segmento específico, haga clic en el vínculo Más **...** para mostrar opciones adicionales. A continuación, haga clic en el icono _Selector_ (![Icono de lista](../assets/icon-list-chooser.png)) para mostrar la lista de segmentos del cliente.

1. En la lista, seleccione la casilla de verificación de cada segmento al que desee destinar la condición.

   ![Regla de precio del carro de compras: lista de selector de condiciones](assets/condition-segment-chooser-list.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Select]** para colocar los segmentos de cliente seleccionados en la condición.

1. Complete el resto de la regla de precios según sea necesario.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.
