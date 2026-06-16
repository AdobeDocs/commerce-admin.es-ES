---
title: '[!DNL Commerce] actualizaciones'
description: Descubra cómo las actualizaciones de Adobe Commerce y Magento Open Source afectan a las configuraciones del catálogo y  [!DNL Inventory Management] .
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
TQID: https://experienceleague.adobe.com/rAnH5pJjtg4ujbQdHow-B6urN090iTTt19mv4sadVnc
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 749
ht-degree: 0%

---

# [!DNL Commerce] actualizaciones

Si ha utilizado inventario de origen único en una versión anterior, esta información proporciona detalles sobre nuevas funciones y cambios en las configuraciones de catálogo e inventario existentes.

[!DNL Inventory Management] para Adobe Commerce y Magento Open Source incluye características, mejoras y compatibilidad para desarrolladores que mejora y actualiza la administración de todas las existencias de productos y agrega nuevas características. Todas las funciones están disponibles de forma predeterminada, incluidos el algoritmo de selección de Source y el cierre de compra simultáneo para hacer coincidir las cantidades de los pedidos con los orígenes y la satisfacción de pedidos. Según los sitios web, las tiendas y el tipo de comerciante, puede crear existencias y orígenes adicionales, asignar cantidades de inventario y mucho más. Para obtener información completa, consulte [Inventory management](introduction.md).

Al instalar Magento Open Source 2.4.x o Adobe Commerce 2.4.x, se producen los siguientes cambios iniciales:

- [Inventory management](enable.md) habilita en el nivel de producto o tienda global. La opción Administrar stock permite o desactiva el seguimiento de las cantidades de inventario, los cálculos de las cantidades comercializables agregadas y la gestión de reservas para el seguimiento de las compras hasta la factura y el envío. Puede desactivar esta opción para utilizar un ERP y otros servicios de terceros para administrar existencias, pedidos y envíos. Para obtener información adicional, consulte [!DNL Inventory Management] módulos a continuación.

- [Source predeterminado](sources-manage.md) y [Stock predeterminado](stocks-manage.md) se agregan al sistema. No deshabilite ni elimine estos valores predeterminados. [!DNL Commerce] asigna los productos existentes y recién importados a estos valores predeterminados.

  >[!IMPORTANT]
  >
  >Se desaconseja encarecidamente el uso de Valores predeterminados y Source predeterminado porque forman parte del módulo `CatalogInventory`, que ahora está obsoleto. En su lugar, se recomienda crear y utilizar recursos y existencias personalizados.

   - Las existencias proporcionan una cantidad vendible virtual agregada con reservas para rastrear carros de compras y pedidos, lo que garantiza un cierre de compra simultáneo.

   - Todos los productos existentes en el catálogo se asignan al Source predeterminado. Hasta que se añaden nuevas fuentes, la interfaz del producto no cambia. Si solo envía productos desde una ubicación, no hay otras diferencias para las fuentes. Puede crear [orígenes](sources-add.md) personalizados y [asignar cantidades](quantities-manage.md) por ubicación de envío.

   - Puede configurar un origen como una ubicación de recogida y [asignar cantidades](quantities-manage.md) para ese origen.

   - El sitio web asigna a Stock predeterminado. Puede crear [existencias](stocks-add.md) personalizadas para conectar canales de ventas (sitios web) y fuentes (ubicaciones).

- [opciones de configuración](configuration.md) adicionales se agregan a sus productos y a su tienda global. Algunas opciones de configuración existentes reciben opciones y comportamientos actualizados:

   - Notificar para la Cantidad Siguiente envía notificaciones y deducciones de la Cantidad Vendible.

   - El umbral de Agotado admite importes positivos, cero y negativos. Con los pedidos no satisfechos activados, las cantidades positivas se omiten y se consideran cero (o infinitas).

   - Los pedidos no satisfechos admiten importes cero (infinitos) y negativos. Cuando está activada, la opción Notificar para la Cantidad Siguiente no deduce de la Cantidad Vendible.

- Las nuevas reservas realizan un seguimiento de las posibles ventas, convirtiéndolas en deducciones de cantidad cuando se envía el pedido. Nunca accede directamente ni crea reservas. [!DNL Commerce] crea y administra reservas entre bastidores mediante pedidos, envíos y notas de crédito.

- [Los pedidos y envíos](shipments.md) incluyen nuevas características para recomendar envíos mediante el algoritmo de selección de Source y admiten envíos parciales de varias fuentes para satisfacer un pedido.

- Las nuevas [funciones de importación y exportación](inventory-import-export.md) le permiten agregar orígenes de forma masiva, actualizar las cantidades de inventario y establecer el estado de existencias (dentro/fuera de existencias) para todas las SKU del catálogo. Estas funciones permiten modificar para una, una o todas las fuentes.

- Las nuevas opciones masivas a través de la página de cuadrícula de productos admiten [la asignación y anulación de la asignación de fuentes](bulk-assignment.md) y [la transferencia del inventario a la fuente](inventory-transfer.md).

- [!DNL Inventory Management] admite catálogos B2B. Actualmente, todos los productos B2B deben asignarse a Source predeterminado y a Stock predeterminado.

## [!DNL Commerce Order Management] y [!DNL Inventory Management]

[Commerce Order Management (MCOM)](https://commerce-docs.github.io/oms-documentation-archive/) no es compatible con [!DNL Inventory Management]. Una vez instalados, los módulos MCOM proporcionan todas las características de administración de inventario a [!DNL Commerce], incluida la administración de un solo origen y de varios orígenes, existencias, reservas y mucho más. Los módulos [!DNL Inventory Management] están deshabilitados de manera predeterminada.

MCOM ofrece amplias funciones y servicios para la gestión de pedidos omnicanal avanzada, inventario global y múltiples fuentes, cumplimiento de tienda a almacén y servicio al cliente centralizado. Para obtener una lista completa de características, consulte la [lista de características MCOM](https://commerce-docs.github.io/oms-documentation-archive/getting-started/feature-list/).

[!DNL Inventory Management] amplía las características existentes de [!DNL Commerce] con opciones adicionales para rastrear pedidos en proceso, inventario disponible, inventario disponible para un inventario y API para el desarrollo de extensiones.

## [!DNL Inventory Management] módulos

Es posible que desee deshabilitar [!DNL Inventory Management] módulos para:

- Agilice la actualización de los comerciantes que actualmente usan Adobe Commerce o Magento Open Source 2.0/2.1/2.2/2.3 y migre a 2.4.x.

- Utilice módulos de administración de pedidos e inventario personalizados o de terceros.

- Usar [!DNL Order Management System] para la administración de inventario. El conector actual no admite interfaces [!DNL Inventory Management]. Para los comerciantes de OMS que actualizan a Adobe Commerce 2.4.0, deben desactivar estos módulos.

Para obtener información detallada, consulte [Instalar y actualizar](install-update.md).
