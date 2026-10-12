---
title: Tipos de fuentes de comerciante
description: Compare los modos de comerciante de un solo origen y de varios orígenes para elegir cómo asignar orígenes, existencias y cantidades en [!DNL Inventory Management].
exl-id: ec928929-5826-4504-9fd0-84256b37cb39
feature: Inventory, Products
TQID: 'https://experienceleague.adobe.com/-ABDMLnAibksuQGkdEM683g8JwcUSt2DQERC0WJnQiM'
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
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
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
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%
---
# Tipos de fuentes de comerciante

[!DNL Commerce] admite [!DNL Inventory Management] para empresas de todos los tamaños, incluida una sola tienda con un sitio web a una red internacional de sitios web, tiendas, almacenes y distribuidores directos. Todos los comerciantes que utilizan Adobe Commerce o Magento Open Source se dividen en dos tipos en función del número de ubicaciones o fuentes de su empresa.

- Los comerciantes de origen único envían productos desde una ubicación. Se le considera un comerciante/modo de un solo origen hasta que empiece a añadir fuentes y existencias personalizadas a su instalación.

- Los comerciantes de múltiples fuentes envían productos desde más de una ubicación, como tiendas físicas, almacenes, expedidores de entrega y centros de distribución. Después de agregar fuentes personalizadas por ubicación, se convierte automáticamente en un comerciante de varias fuentes.

## Comerciantes de un solo origen

Los comerciantes de un solo origen tienen una sola ubicación que administra el inventario disponible y satisface los pedidos. Normalmente, tiene varios sitios web (o canales de ventas) que venden productos del mismo catálogo, inventario y ubicación.

Por ejemplo, tiene un sitio web o una implementación de varios sitios con sitios para Estados Unidos, Alemania, Francia y Brasil que extraen productos de un gran almacén. Este único origen administra todas las cantidades de inventario, los envíos y las devoluciones, independientemente del canal de ventas que reciba el pedido.

Para empezar:

- Configura [la configuración global y de producto](configuration.md) para el inventario de tu tienda según sea necesario.

- Actualice [Source predeterminado](sources-manage.md) con información para su ubicación de inventario única. No es necesario crear fuentes adicionales.

- Actualizar [Stock predeterminado](stocks-manage.md). Asegúrese de que todos los sitios web estén seleccionados como canales de ventas. A medida que agrega nuevos sitios web, [!DNL Commerce] los agrega automáticamente al Stock predeterminado. No es necesario crear stock adicionales.

>[!NOTE]
>
>A medida que su empresa se expanda, agregue fuentes y existencias adicionales y actualice su configuración de [!DNL Inventory Management] para convertirla en un comerciante de múltiples fuentes. Consulte [Expandir y reestructurar inventario](expand-restructure.md) para todos los detalles.

## Comerciantes de varias fuentes

Los comerciantes de varias fuentes tienen un sitio web o una implementación de varios sitios y administran el inventario disponible y el cumplimiento de pedidos a través de varias ubicaciones.

Por ejemplo, tiene una implementación de varios sitios con sitios web para Estados Unidos, Alemania, Francia y Brasil. Su negocio incluye múltiples almacenes y tiendas en estos países y servicios de envío directo que administran todas las existencias de inventario y cumplen con los pedidos. Estas ubicaciones y sitios web se convierten en orígenes y existencias en [!DNL Commerce]. Puede crear un inventario para América y otro para Europa, y asignar sitios web y fuentes basados en configuraciones regionales y ubicaciones. Los clientes que compran cada sitio web solo tienen acceso a los inventarios vendibles de las fuentes asignadas.

Para empezar:

- Configure las opciones globales del inventario de su tienda según sea necesario.

- Agregue [fuentes personalizadas](sources-add.md) para sus ubicaciones de inventario: almacenes, tiendas, centros de distribución y distribuidores directos entre terceros.

- Agregue [existencias personalizadas](stocks-add.md) a cada región para asignar sus sitios web con múltiples orígenes. Reordene las fuentes en cada stock en la prioridad de ubicación, lo que resulta útil al cumplir sus pedidos.

- Asignar orígenes a productos, agregando cantidades por ubicación.

- Complete cualquier configuración adicional por producto para umbrales de cantidad, pedidos pendientes, etc.
