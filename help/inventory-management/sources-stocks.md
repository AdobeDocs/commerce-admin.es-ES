---
title: Existencias y fuentes
description: Obtenga información acerca de las relaciones entre productos, fuentes y existencias.
exl-id: 01bbbd82-898b-4757-ab40-0d8b89ec59bc
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Existencias y fuentes

Administre su inventario independientemente de la ubicación del almacén, el tipo de producto o servicio o el canal de ventas. Satisfaga pedidos y envíe productos desde varios almacenes, tiendas físicas, centros de distribución y envío directo para completar pedidos con un enfoque en el inventario equilibrado, los costes de envío y mucho más.

Estas descripciones incluyen productos, fuentes y existencias para una empresa de bicicletas con múltiples ubicaciones de envío y sitios web en Estados Unidos y Europa.

## Fuentes

[Fuentes](sources-manage.md) son las ubicaciones físicas donde se administra y envía el inventario de productos para la satisfacción de pedidos o donde hay servicios disponibles. Estas ubicaciones pueden incluir almacenes, tiendas físicas, centros de distribución y transportistas de entrega. [!DNL Commerce] utiliza las cantidades y las cantidades vendibles por stock y administra automáticamente los importes de inventario de los productos y pedidos administrados. Si tiene un origen, se le considerará en modo _origen único_. Si tiene varias fuentes, se le considerará en modo _multifuente_.

Una fuente puede tener prioridad en el ámbito de las existencias en un almacén, pero no necesariamente en todos los almacenes, ya que la fuente puede reutilizarse en diferentes existencias. El número de existencias y fuentes aumenta la complejidad para determinar el mejor almacén o tienda para satisfacer un pedido. Por ejemplo, puede tener un número limitado de productos disponibles en sus ubicaciones físicas con un amplio inventario en sus almacenes y servicios en ubicaciones clave con disponibilidad limitada.

En este ejemplo, el comerciante tiene una bicicleta de montaña disponible para el envío desde tiendas, almacenes y un transportista de entrega.

![Ejemplo de diagrama de orígenes](assets/diagram-sources.png){width="600" zoomable="yes"}

## Existencias

[Existencias](stocks-manage.md) representa un inventario virtual agregado de productos disponibles para la venta en sus canales de ventas (sitios web). Cada inventario asigna sus canales de ventas con las fuentes para los inventarios disponibles y las cantidades vendibles. Según la configuración del sitio, las existencias se pueden asignar a uno o más canales de ventas y fuentes.

Las Sales Channel representan entidades que venden su inventario, incluidos sitios web, vistas de tiendas, grupos de clientes B2B, etc. Los canales de ventas solo se pueden asociar a un Stock. Cada canal de ventas solo puede tener un único inventario asignado, y un solo inventario se puede asignar a varios sitios web. A través de las existencias, puede modificar la priorización de los orígenes utilizados al enviar pedidos y mediante el [Algoritmo de selección de Source](selection-reservations.md).

Comience con una Stock predeterminada asignada con el Source predeterminado y su sitio web, mejor utilizado por los comerciantes de un solo origen. Solo se puede asignar la Source predeterminada a estas existencias. Los comerciantes de varias fuentes crean existencias personalizadas para fuentes y sitios web personalizados según sea necesario.

![Diagrama, por ejemplo, existencias para una tienda](assets/diagram-stock.png){width="600" zoomable="yes"}

## Cantidades de productos

Cantidad es el número de productos del inventario activo que se pueden comprar. La cantidad de productos aumenta y disminuye cuando se completan los envíos o se ajusta el inventario. Añadir productos a un carro de compras no afecta a esta cantidad. La cantidad vendible realiza un seguimiento de la disponibilidad del producto para un canal de ventas y también utiliza este valor para determinar el stock disponible para la compra. Según el número de orígenes, puede ver y administrar la cantidad de productos de una de las siguientes opciones:

- **Cantidad**: para comerciantes de un solo origen, la columna _[!UICONTROL Quantity]_&#x200B;y el valor rastrean la cantidad de inventario disponible.
- **Cantidad por Source**: para comerciantes de varios orígenes, la columna _[!UICONTROL Quantity per Source]_&#x200B;y los valores rastrean el inventario disponible disponible por ubicación. Si agrega varios orígenes, este valor reemplaza la cantidad y muestra todos los orígenes y las cantidades asignadas.

Las reservas hacen un seguimiento de las solicitudes de stock de todo el proceso de compra: adición de productos al carro de compras, finalización del cierre de compra y administración de los reembolsos. Para el inventario y las existencias disponibles, las reservas reservan los importes de inventario por pedido a través del proceso de cierre de compra, restados de la cantidad vendible. Las reservas se convierten en deducciones de cantidad al facturar y enviar productos.

Cantidad Vendible calcula el inventario virtual de productos (o disponibilidad), utilizando umbrales configurados, importes reservados o vendidos y cantidades por origen. Para cada inventario, [!DNL Commerce] accede a todos los orígenes asignados y agrega las cantidades de producto asociadas. Con este valor base, se restan todos los importes de reserva y el umbral _[!UICONTROL Notify for Quantity Below]_.

![Cálculo de la cantidad vendible de un inventario](assets/diagram-salable-quantity.png){width="600" zoomable="yes"}

## Configuraciones de inventario

Cada producto, fuente y stock incluye varias opciones para configurar para su tienda en los niveles global, fuente, stock y producto. Para obtener una lista completa de estas opciones, consulte [Configuración de Inventory management](configuration.md).

Las siguientes son opciones importantes que se deben entender para [!DNL Inventory Management]:

- **[!UICONTROL Out-of-Stock Threshold]** - Establece una cantidad que se restará de la cantidad vendible. Si activa Pedidos No Satisfechos, este valor no se deduce de la Cantidad Vendible.
- **[!UICONTROL Backorders]**: determina si los productos se pueden vender más allá de un inventario cero y guarda los pedidos hasta que se reabastezcan. Cuando los pedidos pendientes están habilitados, se recomienda configurar [!UICONTROL Out-of-Stock Threshold].

>[!NOTE]
>
>El valor de umbral Agotado admite importes negativos y positivos. Si habilita Pedidos no satisfechos, establezca este valor en una cantidad negativa para el número máximo de productos que se pueden poner en espera antes de que el producto se considere verdaderamente agotado.

## Demostración de Inventory management

Vea este vídeo para obtener más información sobre las fuentes y las existencias de Inventory management:

>[!VIDEO](https://video.tv.adobe.com/v/343748?quality=12&learn=on)
