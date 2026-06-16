---
title: Categorías ocultas
description: Aprenda a utilizar categorías ocultas con fines internos o para vincular a una categoría que no esté incluida en el menú de navegación.
exl-id: 43aa74b3-b4cd-488d-aa58-fa2c468fe3a2
feature: Catalog Management, Categories
TQID: https://experienceleague.adobe.com/vXJFiYxeTBcRQxdc4XGrPEPKuBAcqr-mnuUlh1WIskM
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fc
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 186
ht-degree: 0%

---

# Categorías ocultas

Hay muchas maneras de usar categorías ocultas. Es posible que desee crear niveles de categoría adicionales para sus propios propósitos internos, pero mostrar únicamente las categorías de nivel superior a sus clientes. O bien, puede que desee vincular una categoría que no esté incluida en el menú de navegación.

## Crear categorías ocultas

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. En el árbol de categorías, seleccione la categoría que desee ocultar y haga lo siguiente:

   - Establezca **[!UICONTROL Is Active]** en `Yes`.
   - Establezca **[!UICONTROL Include in Menu]** en `No`.

1. En la sección **[!UICONTROL Display Settings]**, establezca **[!UICONTROL Anchor]** en `No`.

   ![Categoría oculta](./assets/hidden-categories.png){width="600" zoomable="yes"}

   La categoría oculta está activa, pero no aparece en el menú superior ni en la navegación por capas.

1. Complete la siguiente configuración para cada subcategoría oculta con el fin de crear subcategorías:

   >[!NOTE]
   >
   >Aunque la categoría está oculta, puede crear subcategorías debajo de ella y activarlas.

   - Establezca **[!UICONTROL Enable Category]** en `Yes`.
   - En la sección **[!UICONTROL Display Settings]**, establezca **[!UICONTROL Anchor]** en `Yes`.

   Como categorías activas, ahora puedes enlazarlas desde otros lugares de tu tienda, pero no aparecen en el menú.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.
