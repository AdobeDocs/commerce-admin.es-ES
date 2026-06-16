---
title: Configuración del algoritmo de prioridad de Source
description: Obtenga información sobre cómo configurar la prioridad de origen utilizada para el orden de orígenes asignados en su stock para hacer recomendaciones.
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
TQID: https://experienceleague.adobe.com/TB4THYjkzbNvEbsjNzOewNtYS6JoRvLDiQQCovSMkbI
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 271
ht-degree: 0%

---

# Configuración del algoritmo de prioridad de Source

Las existencias personalizadas incluyen una lista asignada de fuentes para vender y enviar el inventario de productos disponible a través de su tienda. Este algoritmo utiliza el orden de las fuentes asignadas en su inventario para hacer recomendaciones.

Cuando se ejecuta, el algoritmo:

- Funciona según el orden configurado de las fuentes en el nivel de stock, empezando por la parte superior

- Recomienda una cantidad a enviar y una fuente por producto en función del pedido de la lista, la cantidad disponible y la cantidad pedida

- Continúa en la lista hasta que se completa el envío del pedido

- Omite los orígenes deshabilitados si se encuentran en la lista

Para configurarlo, organice los orígenes de arriba a abajo con prioridad para cumplir los pedidos. El Algoritmo de Selección de Source (SSA) proporciona un algoritmo Prioridad utilizando este pedido al determinar las deducciones de envío e inventario. Consulte [Priorización de orígenes para un recurso](stocks-prioritize-sources.md).

## Configuración de la prioridad de las fuentes

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**.

1. Abra una acción en modo de edición y vaya al área _[!UICONTROL Sources]_.

1. Haga clic en **[!UICONTROL Assign Sources]**.

1. En la vista _[!UICONTROL Assign Sources]_, active la casilla de verificación del origen necesario y, a continuación, haga clic en **[!UICONTROL Done]**&#x200B;para asignar un origen al inventario.

>[!NOTE]
>
>Cuando se usa el algoritmo [Prioridad de distancia](distance-priority-algorithm.md) para el envío, si las rutas y los datos no regresan para el [modo de cálculo](distance-priority-algorithm.md) seleccionado (conducir, andar en bicicleta o caminar) para un envío, el SSA usa de forma predeterminada la Prioridad Source.

![Pedido de Source después de la priorización](assets/inventory-stock-priority-after.png)

| Iconos | Descripción |
|----------------------------------------------|----------------------------------------------------------------|
| ![arrastre y suelte el icono para establecer la prioridad](assets/icon-drag-and-drop-action.png) | Utilice para arrastrar y soltar orígenes según la prioridad. |
| ![haga clic en el icono para anular la asignación de un origen](assets/icon-delete-action.png) | Anular la asignación de un origen a un inventario. |
