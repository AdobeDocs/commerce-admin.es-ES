---
title: Experiencia de tienda de puntos de recompensa
description: Descubra cómo los clientes pueden acceder a un historial de su saldo de puntos de recompensa en su cuenta de tienda.
exl-id: 6aa2d406-95c1-408c-a971-5c2a4132a0c8
feature: Rewards, Promotions/Events, Customers, Storefront
TQID: 'https://experienceleague.adobe.com/R2LBruTKbg4EhfNJ4tO795Y4LPS094UtRpZIuVNFe6c'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
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
source-wordcount: '149'
ht-degree: 0%
---
# Experiencia de tienda de puntos de recompensa

{{ee-feature}}

La sección [Puntos de recompensa](rewards-loyalty.md) de la cuenta del cliente muestra que el saldo actual de puntos de recompensa obtenidos por el cliente y un historial de su saldo de puntos de recompensa.

![Puntos de recompensa](./assets/account-dashboard-reward-points.png){width="700" zoomable="yes"}

## Canjee los puntos de recompensa durante el pago

Si se configura la [tasa de cambio de recompensa](reward-exchange-rates.md) con dirección de `Points to Currency`, los clientes pueden usar puntos de recompensa durante el cierre de compra.

1. Después de agregar todos los productos necesarios al carro de compras, el cliente accede al cierre de compra.

1. Ingresa toda la información de envío requerida y navega al paso _Revisar y pagar_.

1. En la sección _[!UICONTROL Reward points]_, comprueba la cantidad de puntos disponibles y su valor de moneda.

1. Clics **[!UICONTROL Use reward points]**.

![Puntos de recompensa al pagar](./assets/reward-points-on-checkout.png){width="700" zoomable="yes"}

El descuento por puntos disponible se aplica al subtotal.

>[!NOTE]
>
>Si el saldo disponible es mayor que el total general del pedido, no se requiere otro método de pago.
