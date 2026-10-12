---
title: Cierre de compra de una página
description: Obtenga información acerca del proceso de cierre de compra de una página, que puede proporcionar un proceso de cierre de compra optimizado para su tienda.
exl-id: c91347b6-bb6f-44e7-b470-f237bf430d5f
feature: Checkout
TQID: 'https://experienceleague.adobe.com/rY0sw7iSq7-4Y5EPQ1cL8bJ7cuqdDfDqvjEQvH-jsvM'
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
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%
---
# Cierre de compra de una página

El propósito del pago y envío de una página es recopilar la información que se necesita y completar la venta lo más rápido posible sin requerir clics adicionales para el comprador. Cuando se habilita la desprotección de una página, todo el proceso de desprotección se realiza en una sola página. Cada sección de la información de cierre de compra se expande según sea necesario.

El cierre de compra de una página está habilitado de forma predeterminada. Si va a implementar una integración personalizada o una extensión de cierre de compra, puede que sea necesario deshabilitar el cierre de compra de una página.

**_Para deshabilitar la desprotección de una página:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Checkout]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Checkout Options]**.

   ![Configuración - opciones de cierre de compra](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

   Para obtener una descripción detallada de cada una de estas opciones de configuración, consulte [Opciones de desprotección](../configuration-reference/sales/checkout.md#checkout-options) en la _Guía de referencia de configuración_.

1. Si la configuración es para una vista de tienda específica, [elija la vista de tienda](../configuration-reference/scope-change.md#set-the-scope) donde se aplica la configuración.

   Cuando se le solicite, haga clic en **[!UICONTROL OK]** para continuar.

1. Establezca **[!UICONTROL Enable Onepage Checkout]** en `No`.

   Si es necesario, desactive la casilla de verificación **[!UICONTROL Use system value]** para cambiar esta configuración.

1. Haga clic en **[!UICONTROL Save Config]**.
