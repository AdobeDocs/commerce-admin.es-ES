---
title: Promociones de regalo gratis
description: Aprenda a configurar una promoción de regalo gratis con reglas de precio de carro de compras para ofrecer un regalo gratis cuando se cumpla un conjunto de condiciones.
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
TQID: https://experienceleague.adobe.com/FR-q4Qj-ZDDzmfEKSvSj-BlwsM7ro-BqAE1yCppTaXE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 3cddc90c619a27b1404e0be7bb4b2c9a3b77e443
workflow-type: tm+mt
source-wordcount: 349
ht-degree: 0%

---


# Promoción de regalos gratis

La promoción *Regalo gratis* te permite establecer una [regla de precio del carro de compras](price-rules-cart.md) que agrega un artículo gratis al carro de compras en condiciones específicas.

>[!NOTE]
>
>Esta función no se admite en tiendas Luma. Es accesible a través de [GraphQL](https://developer.adobe.com/commerce/webapi/graphql/schema/cart/mutations/select-free-gift/) y está disponible en las tiendas de Edge Delivery Services (EDS).

## Crear una promoción de regalo gratuita

En esta sección se describe cómo crear una promoción de regalo gratuita utilizando el siguiente formato:

**Compra un producto X y obtén un producto Y gratis**

1. [Crea una regla de precio para el carro de compras](price-rules-cart.md#step-1-add-a-rule) con una promoción de regalo gratis.

1. [Describa las condiciones](price-rules-cart.md#step-2-describe-the-conditions) de las instrucciones del carro de compras para definir las condiciones de la regla de precios. Esta es la primera de varias condiciones que se pueden agregar a la regla y determina cuándo se activa. Se puede basar en una combinación de lo siguiente:

   - Atributos del producto
   - Productos
   - Atributos del carro
   - Segmentos de cliente de Adobe Commerce

   Si se deja en blanco, la regla se activará para cada carro de compras.

   ![Regla de precio del carro de compras: condiciones](./assets/conditions.png){width="600" zoomable="yes"}

1. Defina las acciones para la regla de precios del carro de compras:

   1. Expanda  (../assets/icon-display-expand.png) la sección **[!UICONTROL Actions]** e introduzca la siguiente información:

   - Establezca **[!UICONTROL Apply]** en `Free Gift`.
   - En **[!UICONTROL Gift SKU(s)]**, seleccione uno o más SKU que el cliente pueda elegir como regalo gratuito.
   - Establezca **[!UICONTROL Free Gift Discount Type]** en **[!UICONTROL Price Based]** o **[!UICONTROL Discount Based]**.
   - En **[!UICONTROL Gift Qty]**, escriba la cantidad del regalo gratuito que recibe el cliente. Por ejemplo, escriba `2` si desea que el cliente reciba dos artículos gratuitos.
   - Para evitar que se apliquen otros descuentos, establezca **[!UICONTROL Discard subsequent rules]** en `Yes`.

   1. Haga clic en **[!UICONTROL Save and Continue Edit]** y complete el resto de la regla según sea necesario.

1. [Complete la etiqueta](price-rules-cart.md) de las instrucciones de la regla de precios del carro de compras para introducir la etiqueta que aparece durante el cierre de compra.

![Regla de precio del carro de compras - Etiqueta de regalo gratis](./assets/free-gift-promotion-label.png){width="600" zoomable="yes"}

{{new-price-rule}}

1. Una vez completada la regla, haga clic en **[!UICONTROL Save Rule]**.

## Variaciones

Puede personalizar las reglas de precios del carro de compras de muchas maneras diferentes. La función de regalo gratuito se puede configurar con dos tipos de descuento diferentes:

- **Basado en el precio** : Se agrega un artículo de línea de regalo al precio de `0`.
- **Basado en descuento** : Se aplica un descuento completo al artículo de línea de regalo.
