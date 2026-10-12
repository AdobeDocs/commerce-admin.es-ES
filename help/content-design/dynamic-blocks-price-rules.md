---
title: Bloques dinámicos en reglas de precios
description: Asocie un bloque dinámico a una regla de precios promocionales.
exl-id: e1564df2-1c06-4d11-a32d-6f5c0be974e3
feature: Page Content, Price Rules
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
TQID: 'https://experienceleague.adobe.com/Fzw3GXEp2PNXIuvOpN62tBiLhTeMJGsDMfQpRwV1dSg'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 17d326fa-534a-55a5-b46f-8ae1de1e2f75
    internal-label: Page Content
  - id: a507b1ed-4937-53da-97ae-57d36bd5b9e0
    internal-label: Price Rules
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
source-wordcount: '317'
ht-degree: 0%
---
# Bloques dinámicos en reglas de precios

{{ee-feature}}

Cualquier [bloque dinámico](dynamic-blocks.md) que cree se puede asociar con una promoción. Para realizar la asociación, primero debe crear el bloque dinámico y la [regla de precio de catálogo](../merchandising-promotions/price-rules-catalog.md) o [regla de precio de carro de compras](../merchandising-promotions/price-rules-cart.md). La asociación se puede realizar mientras se trabaja en una regla de precios o cuando se trabaja en un bloque dinámico.

>[!IMPORTANT]
>
>Después de crear esta asociación, el bloque dinámico se muestra **solamente** cuando se activa la regla. Si la promoción está dirigida al segmento A, el bloque se muestra al segmento A. Si la promoción no está activa, el bloque no se muestra.

## Asociación de un bloque dinámico a una regla de precio

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_y elija una de las siguientes opciones:

   - **[!UICONTROL Catalog Price Rules]**
   - **[!UICONTROL Cart Price Rules]**

1. En la cuadrícula, busque la regla que desee asociar al bloque dinámico y ábrala en modo de edición.

1. Desplazarse hacia abajo y expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Related Dynamic Blocks]**.

1. En la primera columna, establezca el filtro en `Any` y haga clic en **[!UICONTROL Reset Filter]**.

   La cuadrícula ahora enumera todos los bloques dinámicos disponibles.

1. Seleccione la casilla de verificación de cada bloque dinámico que desee asociar a la regla.

   ![Agregando bloques dinámicos seleccionados](./assets/price-rule-cart-related-dynamic-blocks-any.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

## Asociación de una regla de precio a un bloque dinámico

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. Busque el bloque dinámico en la cuadrícula y ábralo en modo de edición.

1. Desplazarse hacia abajo y expandir **[!UICONTROL Related Promotions]**.

   Cualquier regla de precios asociada actualmente aparece en la cuadrícula.

1. Agregar una regla asociada nueva o quitar una asociación actual.

   - Para asociar una promoción del carro de compras, haga clic en **[!UICONTROL Add Cart Price Rules]**.

   - Para asociar una promoción relacionada con un producto, haga clic en **[!UICONTROL Add Catalog Price Rules]**.

1. En la cuadrícula, seleccione la casilla de verificación de cada regla que desee asociar al bloque dinámico.

1. Haga clic en **[!UICONTROL Add Selected]**.

   ![Agregando reglas de precio seleccionadas a un bloque dinámico](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.
