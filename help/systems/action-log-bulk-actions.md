---
title: Acciones masivas
description: Obtenga información sobre cómo configurar y ver el registro de acciones masivas.
exl-id: 3907d9ef-3592-4dbb-805f-97b79bafd8ab
feature: Logs, Configuration
TQID: https://experienceleague.adobe.com/hmZYwUcG-rgx--kG5RNE3xe38LWn7OM0rq2q7RC3xeQ
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 3%

---

# Acciones masivas

{{ee-feature}}

El registro de acciones masivas registra los detalles de las operaciones masivas asincrónicas que se ejecutan en segundo plano, como la importación/exportación o la asignación de [precios personalizados](../b2b/catalog-shared-manage.md#update-custom-pricing) a varios productos en un [catálogo compartido](../b2b/catalog-shared.md).

![Registro de acciones en lotes](./assets/bulk-actions-log.png){width="600" zoomable="yes"}

## Configuración de acciones masivas

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL System]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Bulk Actions]** y establezca la opción para guardar el registro:

   **[!UICONTROL Days Saved in Log]**: escriba el número de días durante los cuales se guardarán las acciones masivas en un registro.

   ![Configuración avanzada: acciones masivas](../configuration-reference/advanced/assets/system-bulk-actions.png){width="600" zoomable="yes"}

   Para obtener una lista detallada de las opciones de configuración, consulte [_Acciones masivas_](../configuration-reference/advanced/system.md) en la _Referencia de configuración_.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Ver acciones masivas

1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Bulk Actions]**.

1. Busque la acción que desee en el registro.

1. En la columna _[!UICONTROL Action]_, haga clic en **[!UICONTROL Details]**.
