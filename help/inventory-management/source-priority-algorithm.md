---
title: Configuración del algoritmo de prioridad de Source
description: Obtenga información sobre cómo configurar la prioridad de origen utilizada para el orden de orígenes asignados en su stock para hacer recomendaciones.
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '271'
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
