---
title: Priorización de orígenes de inventario para un inventario
description: Establezca el orden de prioridad de origen en un stock en Admin para controlar las recomendaciones del algoritmo de selección de Source durante el envío.
exl-id: 16db3ee3-ce99-40dd-b1a3-fcb145b1298f
feature: Inventory, Configuration
TQID: 'https://experienceleague.adobe.com/oPgeuN3-Il-yf3zpG2r4PNAmNbf-4gmz5-GFngM3-Ng'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 8dc0e58b-adf0-51bb-8db5-bb36e3e656fb
    internal-label: Inventory
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%
---
# Priorización de orígenes para una existencia

Después de agregar [orígenes](sources-manage.md) a [existencias](stocks-manage.md), organice esos orígenes de arriba a abajo con prioridad para cumplir los pedidos. El Algoritmo de Selección de Source (SSA) proporciona un algoritmo Prioridad utilizando este pedido al determinar las deducciones de envío e inventario.

La prioridad de las fuentes sobre las existencias no influye en las fuentes asignadas al editar los inventarios de productos.

En este ejemplo, las acciones del Reino Unido tienen fuentes asignadas de forma desordenada para una tienda y dos almacenes en Londres y un almacén en Berlín.

![Pedido de Source antes de la priorización](assets/inventory-priority-before.png){width="350" zoomable="yes"}

El comerciante prefiere tener los envíos priorizados desde el almacén más grande de Berlín, luego el almacén de Londres, la ubicación de desbordamiento de Londres, y finalmente la tienda en Londres. Para cambiar el orden, las entradas se arrastran y se sueltan en el orden deseado.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stocks]**.

1. Abra las existencias en el modo _Editar_.

1. Expanda la ficha _[!UICONTROL Sources]_, si es necesario.

1. Use ![Icono de orden](assets/icon-sort.png) para arrastrar y soltar los orígenes en una prioridad de arriba (primero) a abajo (último).

   Este pedido es importante cuando se envían pedidos. SSA recomienda envíos basados en el orden de las fuentes

1. Haga clic en **[!UICONTROL Save & Continue]** para guardar los cambios.

![Pedido de Source después de la priorización](assets/inventory-stock-priority-after.png){width="350" zoomable="yes"}
