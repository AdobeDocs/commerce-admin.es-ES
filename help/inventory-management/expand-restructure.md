---
title: Expandir y reestructurar el inventario
description: Aprenda a expandirse a un comerciante de varias fuentes o a reducir a un comerciante de una sola fuente.
exl-id: 880474e3-6533-4b2f-adf7-4312787ff736
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# Expandir y reestructurar el inventario

A medida que su negocio crece y cambia, [!DNL Inventory Management] satisface sus necesidades. Puede expandirse a un comerciante de varias fuentes o reducir a un comerciante de una sola fuente con facilidad.

## Expandir a varios orígenes

Los comerciantes de una sola fuente pueden agregar nuevas tiendas, almacenes, cargadores de entrega y más. La expansión solo requiere algunas adiciones y actualizaciones de existencias para ampliarse a múltiples fuentes:

1. Añadir [fuentes personalizadas](sources-add.md) para cada nueva ubicación.

   Solo se utiliza la Fuente predeterminada para los productos del paquete.

1. Añadir [existencias aduana](stocks-add.md) según sea necesario para las nuevas fuentes.

   Por ejemplo, es posible que desee crear existencias por sitio web, país, configuración regional u otro método. Puede asignar fuentes a sus existencias personalizadas. Solo se utiliza el Stock predeterminado para los productos agrupados.

1. Actualizar [asignaciones y cantidades de origen](quantities-manage.md) para sus productos.

   También puede utilizar la variable [Herramienta Acciones masivas](bulk-assignment.md) y [Importar-Exportar](inventory-import-export.md) para añadir rápidamente fuentes y datos de productos.

## Reestructurar a un solo origen

Para los comerciantes de varios orígenes que deseen reducir las ventas en línea a una ubicación para el envío, modifique los orígenes, las existencias y las cantidades para actualizar:

1. Deshabilitar [fuentes personalizadas](sources-disable.md).

1. Transfiera el inventario de productos a su origen predeterminado.

   Se recomienda el uso de acciones masivas. Consulte [Transferencia de Inventario a Origen](inventory-transfer.md).

1. Asigne todos los sitios web al [Stock predeterminado](stocks-manage.md).
