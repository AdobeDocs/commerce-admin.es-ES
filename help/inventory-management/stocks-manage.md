---
title: Administrar existencias de inventario
description: Descubra cómo se utilizan las existencias para representar un inventario virtual agregado de productos para las fuentes de sus canales de ventas.
exl-id: 076b1325-2de4-46d3-9976-d900bd2cef47
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Administrar stock

Stock representa un inventario virtual agregado de productos para las fuentes de sus canales de ventas (sitios web). Según la configuración del sitio, las existencias se pueden asignar a uno o más canales de ventas. Cada canal de ventas solo puede tener un único inventario asignado, y un solo inventario se puede asignar a varios canales de ventas. A través de las existencias, puede modificar la priorización de las fuentes utilizadas como pedidos que llegan a través de un canal de ventas.

Comience con un Stock predeterminado que no se puede eliminar ni deshabilitar. Solo puede añadir canales de ventas adicionales a las existencias. El único origen asignado es Origen predeterminado. Este stock lo utilizan comerciantes de un solo origen, integraciones de terceros y productos importados.

Sales Channel representa las entidades que venden su inventario. De forma predeterminada, [!DNL Commerce] proporciona los sitios web de la tienda como canales de ventas. Los canales de ventas se pueden ampliar para admitir canales adicionales, como grupos de clientes B2B y vistas de tiendas. Cada canal de ventas solo puede asociarse a un Stock.

- **Compatibilidad con Sales Channel** - Los canales de ventas incluyen actualmente sitios web listos para usar. Puede ampliar los canales de ventas para incluir opciones personalizadas como grupos de clientes B2B y vistas de tiendas. Cada canal de ventas solo puede tener un único inventario asignado. Se puede asignar un único inventario a varios canales de ventas.
- **Asignación a orígenes** - Cada stock puede tener uno o más orígenes habilitados o deshabilitados asignados, calculando el inventario agregado virtual por producto.
- **Cumplimiento de orden de prioridad** : El algoritmo de prioridad predeterminado para el algoritmo de selección de fuentes utiliza la lista de fuentes de stock de arriba a abajo al cumplir pedidos.

El siguiente diagrama ayuda a definir el funcionamiento de un Stock en relación con las Fuentes y Sales Channel de un comerciante de tienda de bicicletas.

![Diagrama, por ejemplo, de existencias de una tienda](assets/diagram-stock.png){width="600" zoomable="yes"}

## Ejemplo de existencias para una bicicleta de montaña y una tienda

Todas las tiendas comienzan con un Stock predeterminado. Debe permanecer `Enabled` por los motivos siguientes:

- Se utiliza al importar nuevos productos, asignando automáticamente productos al origen y stock predeterminados para el acceso inmediato a [!DNL Inventory Management].
- No puede añadir fuentes adicionales a este stock, aparte de la fuente predeterminada.
- Los comerciantes de un solo origen, los productos agrupados y los productos agrupados la necesitan y la utilizan.

Para los comerciantes de varias fuentes, cree y configure las existencias para que se ajusten mejor a sus tiendas y a la satisfacción de pedidos. Al asignar nuevas existencias a un canal de ventas, se anula la asignación de cualquier stock preexistente en ese canal de ventas.

Para una instalación de varias tiendas, el Stock predeterminado se asigna inicialmente al [Sitio web principal](../stores-purchase/stores.md#add-websites){target="_blank"} y el almacén predeterminado. Se muestran las existencias y cantidades correctas para los productos activados y desactivados en la **[!UICONTROL Products]** vista de cuadrícula.

![Administrar stock](assets/inventory-stock.png){width="600" zoomable="yes"}

## Barra de botones

| Botón | Descripción |
|--|--|
| [!UICONTROL Add New Stock] | Abre el _[!UICONTROL New Stock]_formulario que se utiliza para introducir un nuevo inventario de stock para asignar el inventario al canal de ventas. |

## Administración de descripciones de columnas de Stock

| Columna | Descripción |
|--|--|
| [!UICONTROL ID] | ID numérico único generado para la entrada de stock. |
| [!UICONTROL Name] | Nombre único que identifica el inventario de stock. |
| [!UICONTROL Sales Channels] | Define el ámbito de las existencias al asignar las existencias a sitios web específicos como _canales de ventas_. |
| [!UICONTROL Assigned sources] | Orígenes asignados al stock que suministran todas las cantidades de productos. |
| [!UICONTROL Action] | **[!UICONTROL Edit]** : abre el registro de existencias de inventario en modo de edición. |
