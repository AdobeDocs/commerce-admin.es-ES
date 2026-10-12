---
title: Expandir y reestructurar el inventario
description: Amplíe el inventario de un solo origen a varios orígenes o vuelva a reestructurarlo en un único origen a medida que cambie su negocio.
exl-id: 880474e3-6533-4b2f-adf7-4312787ff736
feature: Inventory, Configuration
TQID: 'https://experienceleague.adobe.com/w4TV-BQrg0RzlHn4DVSdHFPD2M5CF11wA7I5OyA7jsY'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
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
source-wordcount: '221'
ht-degree: 0%
---
# Expandir y reestructurar el inventario

A medida que su empresa crece y cambia, [!DNL Inventory Management] satisface sus necesidades. Puede expandirse a un comerciante de varias fuentes o reducir a un comerciante de una sola fuente con facilidad.

## Expandir a varios orígenes

Los comerciantes de una sola fuente pueden agregar nuevas tiendas, almacenes, cargadores de entrega y más. La expansión solo requiere algunas adiciones y actualizaciones de existencias para ampliarse a múltiples fuentes:

1. Agregar [orígenes personalizados](sources-add.md) para cada nueva ubicación.

   Solo se utiliza el Source predeterminado para productos agrupados.

1. Agregue [existencias personalizadas](stocks-add.md) según sea necesario para sus nuevas fuentes.

   Por ejemplo, es posible que desee crear existencias por sitio web, país, configuración regional u otro método. Puede asignar fuentes a sus existencias personalizadas. Solo se utiliza el Stock predeterminado para los productos agrupados.

1. Actualice [asignaciones y cantidades de origen](quantities-manage.md) para sus productos.

   También puede usar la [herramienta de acciones masivas](bulk-assignment.md) y la característica [Importar-exportar](inventory-import-export.md) para agregar rápidamente fuentes y datos de productos.

## Reestructurar a un solo origen

Para los comerciantes de varios orígenes que deseen reducir las ventas en línea a una ubicación para el envío, modifique los orígenes, las existencias y las cantidades para actualizar:

1. Deshabilitar [orígenes personalizados](sources-disable.md).

1. Transfiera el inventario de productos a su Source predeterminado.

   Se recomienda el uso de acciones masivas. Consulte [Transferencia de inventario a Source](inventory-transfer.md).

1. Asignar todos los sitios web a [Stock predeterminado](stocks-manage.md).
