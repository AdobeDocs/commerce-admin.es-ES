---
title: '[!DNL Commerce] actualizaciones'
description: Descubra cómo las actualizaciones de Adobe Commerce y Magento Open Source afectan a los catálogos y a [!DNL Inventory Management] configuraciones.
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# [!DNL Commerce] actualizaciones

Si ha utilizado inventario de origen único en una versión anterior, esta información proporciona detalles sobre nuevas funciones y cambios en las configuraciones de catálogo e inventario existentes.

[!DNL Inventory Management] para Adobe Commerce y Magento Open Source incluye funciones, mejoras y soporte para desarrolladores que mejora y actualiza la administración de todas las existencias de productos y añade nuevas funciones. Todas las funciones están disponibles de forma predeterminada, incluidos el algoritmo de selección de origen y el cierre de compra simultáneo para hacer coincidir las cantidades de los pedidos con los orígenes y la satisfacción de pedidos. Según los sitios web, las tiendas y el tipo de comerciante, puede crear existencias y orígenes adicionales, asignar cantidades de inventario y mucho más. Para obtener información completa, consulte [Inventory management](introduction.md).

Al instalar Magento Open Source 2.4.x o Adobe Commerce 2.4.x, se producen los siguientes cambios iniciales:

- [Inventory management](enable.md) habilita en el nivel de producto o tienda global. La opción Administrar stock permite o desactiva el seguimiento de las cantidades de inventario, los cálculos de las cantidades comercializables agregadas y la gestión de reservas para el seguimiento de las compras hasta la factura y el envío. Puede desactivar esta opción para utilizar un ERP y otros servicios de terceros para administrar existencias, pedidos y envíos. Para obtener más información, consulte [!DNL Inventory Management] Módulos a continuación.

- A [Origen predeterminado](sources-manage.md) y [Stock predeterminado](stocks-manage.md) agregar al sistema. No deshabilite ni elimine estos valores predeterminados. [!DNL Commerce] asigna los productos existentes y recién importados a estos valores predeterminados.

  >[!IMPORTANT]
  >
  >No se recomienda utilizar Valores por Defecto y el Origen por Defecto porque forman parte del `CatalogInventory` , que ahora está obsoleto. En su lugar, se recomienda crear y utilizar recursos y existencias personalizados.

   - Las existencias proporcionan una cantidad vendible virtual agregada con reservas para rastrear carros de compras y pedidos, lo que garantiza un cierre de compra simultáneo.

   - Todos los productos existentes en el catálogo se asignan al origen predeterminado. Hasta que se añaden nuevas fuentes, la interfaz del producto no cambia. Si solo envía productos desde una ubicación, no hay otras diferencias para las fuentes. Puede crear funciones personalizadas [orígenes](sources-add.md) y [asignar cantidades](quantities-manage.md) por ubicación de envío.

   - Puede configurar un origen como ubicación de recogida y [asignar cantidades](quantities-manage.md) para esa fuente.

   - El sitio web asigna a Stock predeterminado. Puede crear funciones personalizadas [acciones](stocks-add.md) para conectar canales de ventas (sitios web) y fuentes (ubicaciones).

- Adicional [opciones de configuración](configuration.md) añada a sus productos y tienda global. Algunas opciones de configuración existentes reciben opciones y comportamientos actualizados:

   - Notificar para la Cantidad Siguiente envía notificaciones y deducciones de la Cantidad Vendible.

   - El umbral de Agotado admite importes positivos, cero y negativos. Con los pedidos no satisfechos activados, las cantidades positivas se omiten y se consideran cero (o infinitas).

   - Los pedidos no satisfechos admiten importes cero (infinitos) y negativos. Cuando está activada, la opción Notificar para la Cantidad Siguiente no deduce de la Cantidad Vendible.

- Las nuevas reservas realizan un seguimiento de las posibles ventas, convirtiéndolas en deducciones de cantidad cuando se envía el pedido. Nunca accede directamente ni crea reservas. [!DNL Commerce] crea y administra reservas entre bastidores mediante pedidos, envíos y notas de crédito.

- [Pedidos y envíos](shipments.md) incluye nuevas funciones para recomendar envíos mediante el algoritmo de selección de origen y admite envíos parciales de varias fuentes para satisfacer un pedido.

- Nuevo [funciones de importación y exportación](inventory-import-export.md) le permite añadir orígenes de forma masiva, actualizar las cantidades de inventario y establecer el estado de las existencias (dentro/fuera de existencias) para todos los SKU del catálogo. Estas funciones permiten modificar para una, una o todas las fuentes.

- Las nuevas opciones masivas a través de la página de cuadrícula de productos admiten de forma masiva [asignar y cancelar la asignación de orígenes](bulk-assignment.md), y [transferir inventario al origen](inventory-transfer.md).

- [!DNL Inventory Management] admite catálogos B2B. Actualmente, todos los productos B2B deben asignarse al origen y las existencias predeterminados.

## [!DNL Commerce Order Management] y [!DNL Inventory Management]

[Commerce Order Management (MCOM)][1] no es compatible con el [!DNL Inventory Management]. Una vez instalados, los módulos MCOM proporcionan todas las características de administración de inventario a [!DNL Commerce], incluida la administración de fuentes únicas y múltiples, existencias, reservas y mucho más. El [!DNL Inventory Management] módulos están desactivados de forma predeterminada.

MCOM ofrece amplias funciones y servicios para la gestión de pedidos omnicanal avanzada, inventario global y múltiples fuentes, cumplimiento de tienda a almacén y servicio al cliente centralizado. Para obtener una lista completa de las funciones, consulte la [Lista de características MCOM][2].

[!DNL Inventory Management] amplía los existentes [!DNL Commerce] funciones con opciones adicionales para rastrear pedidos en proceso, inventario disponible, inventario disponible para un inventario y API para el desarrollo de extensiones.

## [!DNL Inventory Management] módulos

Es posible que desee deshabilitar [!DNL Inventory Management] módulos para:

- Agilice la actualización de los comerciantes que actualmente usan Adobe Commerce o Magento Open Source 2.0/2.1/2.2/2.3 y migre a 2.4.x.

- Utilice módulos de administración de pedidos e inventario personalizados o de terceros.

- Uso [!DNL Order Management System] para la administración de inventario. El conector actual no es compatible [!DNL Inventory Management] interfaces. Para los comerciantes de OMS que actualizan a Adobe Commerce 2.4.0, deben desactivar estos módulos.

Para obtener información detallada, consulte [Instalar y actualizar](install-update.md).

[1]: https://omsdocs.magento.com/
[2]: https://omsdocs.magento.com/en/getting-started/feature-list/
