---
title: Puntos de recompensa en las reglas de precios
description: Descubra cómo se pueden conceder puntos de recompensa a los clientes según la regla de precio del carro de compras.
exl-id: 6e23b56d-64e4-435d-9f4c-ee3f400b0250
feature: Rewards, Promotions/Events, Customers
TQID: 'https://experienceleague.adobe.com/amQYBXl5evC-BUqmb5SyGR97iOAMIPv5UxqCFfOkGmQ'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 4069cee6-4dc8-5a83-81de-232af6a7c9e9
    internal-label: Rewards
  - id: 19d9b313-1a3c-5bed-9da7-4364f71c3a28
    internal-label: Promotions/Events
  - id: 22bad240-8308-569b-a9d5-578f1ff890ca
    internal-label: Customers
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%
---
# Puntos de recompensa en las reglas de precios

{{ee-feature}}

Los puntos de recompensa se pueden otorgar a los clientes según la [regla de precio del carro de compras](price-rules-cart.md). La concesión de puntos puede ser la única acción de la regla de precio, o puede utilizarse con un descuento.

>[!NOTE]
>
>Se requiere la configuración de [Tasas de cambio de recompensa](reward-exchange-rates.md) para que los clientes y los usuarios administradores puedan canjear los puntos de recompensa durante el cierre de compra.

## Añadir puntos de recompensa a una regla de precio

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

1. Haga clic en **[!UICONTROL Add New Rule]** para crear una regla de precios de carro de compras o haga clic en una regla de precios de carro de compras existente para abrirla.

1. Desplácese hacia abajo, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Actions]**, establezca las condiciones e introduzca el número de puntos en el campo **[!UICONTROL Add Reward Points]**.

   ![Regla de precios del carro de compras: puntos de recompensa](./assets/reward-points-price-rule-actions.png){width="600" zoomable="yes"}

1. Siga las instrucciones estándar para completar la [regla de precio del carro de compras](price-rules-cart-create.md).

   Cuando se activa la regla de precio, aparece un mensaje en el carro de compras para que los clientes sepan cuántos puntos pueden obtener al realizar el pedido. Esto solo se aplica a los usuarios registrados y puede variar cuando un usuario ha iniciado sesión.
