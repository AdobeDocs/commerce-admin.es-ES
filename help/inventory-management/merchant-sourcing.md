---
title: Tipos de fuentes de comerciante
description: Obtenga información acerca de los dos tipos de fuentes en función del número de ubicaciones o fuentes de su empresa.
exl-id: ec928929-5826-4504-9fd0-84256b37cb39
feature: Inventory, Products
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '470'
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
