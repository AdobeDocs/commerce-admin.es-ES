---
title: Existencias y fuentes
description: Obtenga información acerca de las relaciones entre productos, fuentes y existencias.
exl-id: 01bbbd82-898b-4757-ab40-0d8b89ec59bc
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 0%

---

# Existencias y fuentes

Administre su inventario independientemente de la ubicación del almacén, el tipo de producto o servicio o el canal de ventas. Satisfaga pedidos y envíe productos desde varios almacenes, tiendas físicas, centros de distribución y envío directo para completar pedidos con un enfoque en el inventario equilibrado, los costes de envío y mucho más.

Estas descripciones incluyen productos, fuentes y existencias para una empresa de bicicletas con múltiples ubicaciones de envío y sitios web en Estados Unidos y Europa.

## Fuentes

[Fuentes](sources-manage.md) son las ubicaciones físicas en las que se administra y envía el inventario de productos para la satisfacción de pedidos o en las que hay servicios disponibles. Estas ubicaciones pueden incluir almacenes, tiendas físicas, centros de distribución y transportistas de entrega. [!DNL Commerce] utiliza las cantidades y las cantidades vendibles por stock y gestiona automáticamente los importes de inventario para los productos y pedidos gestionados. Si tiene una fuente, se le considerará en _de un solo origen_ modo. Si tiene varias fuentes, se le considerará en _de varias fuentes_ modo.

Una fuente puede tener prioridad en el ámbito de las existencias en un almacén, pero no necesariamente en todos los almacenes, ya que la fuente puede reutilizarse en diferentes existencias. El número de existencias y fuentes aumenta la complejidad para determinar el mejor almacén o tienda para satisfacer un pedido. Por ejemplo, puede tener un número limitado de productos disponibles en sus ubicaciones físicas con un amplio inventario en sus almacenes y servicios en ubicaciones clave con disponibilidad limitada.

En este ejemplo, el comerciante tiene una bicicleta de montaña disponible para el envío desde tiendas, almacenes y un transportista de entrega.

![Ejemplo de diagrama de fuentes](assets/diagram-sources.png){width="600" zoomable="yes"}

## Existencias

[Existencias](stocks-manage.md) representan un inventario virtual agregado de productos disponibles para la venta en sus canales de ventas (sitios web). Cada inventario asigna sus canales de ventas con las fuentes para los inventarios disponibles y las cantidades vendibles. Según la configuración del sitio, las existencias se pueden asignar a uno o más canales de ventas y fuentes.

Las Sales Channel representan entidades que venden su inventario, incluidos sitios web, vistas de tiendas, grupos de clientes B2B, etc. Los canales de ventas solo se pueden asociar a un Stock. Cada canal de ventas solo puede tener un único inventario asignado, y un solo inventario se puede asignar a varios sitios web. A través de stock, puede modificar la priorización de las fuentes utilizadas al enviar pedidos y por el [Algoritmo de selección de origen](selection-reservations.md).

Comience con un Stock predeterminado asignado con el Origen predeterminado y su sitio web, mejor utilizado por los comerciantes de un solo origen. A este stock solo se le puede asignar el origen predeterminado. Los comerciantes de varias fuentes crean existencias personalizadas para fuentes y sitios web personalizados según sea necesario.

![Diagrama, por ejemplo, de existencias de una tienda](assets/diagram-stock.png){width="600" zoomable="yes"}

## Cantidades de productos

Cantidad es el número de productos del inventario activo que se pueden comprar. La cantidad de productos aumenta y disminuye cuando se completan los envíos o se ajusta el inventario. Añadir productos a un carro de compras no afecta a esta cantidad. La cantidad vendible realiza un seguimiento de la disponibilidad del producto para un canal de ventas y también utiliza este valor para determinar el stock disponible para la compra. Según el número de orígenes, puede ver y administrar la cantidad de productos de una de las siguientes opciones:

- **Cantidad** - Para los comerciantes de un solo origen, la _[!UICONTROL Quantity]_columna y valor registra la cantidad de inventario disponible.
- **Cantidad por origen** - Para los comerciantes de varias fuentes, la _[!UICONTROL Quantity per Source]_columna y valores realiza un seguimiento del inventario disponible por ubicación. Si agrega varios orígenes, este valor reemplaza la cantidad y muestra todos los orígenes y las cantidades asignadas.

Las reservas hacen un seguimiento de las solicitudes de stock de todo el proceso de compra: adición de productos al carro de compras, finalización del cierre de compra y administración de los reembolsos. Para el inventario y las existencias disponibles, las reservas reservan los importes de inventario por pedido a través del proceso de cierre de compra, restados de la cantidad vendible. Las reservas se convierten en deducciones de cantidad al facturar y enviar productos.

Cantidad Vendible calcula el inventario virtual de productos (o disponibilidad), utilizando umbrales configurados, importes reservados o vendidos y cantidades por origen. Para cada población, [!DNL Commerce] accede a todos los orígenes asignados y agrega las cantidades de producto asociadas. Con este valor base, resta todos los importes de reserva y la variable _[!UICONTROL Notify for Quantity Below]_umbral.

![Cálculo de la cantidad vendible de un stock](assets/diagram-salable-quantity.png){width="600" zoomable="yes"}

## Configuraciones de inventario

Cada producto, fuente y stock incluye varias opciones para configurar para su tienda en los niveles global, fuente, stock y producto. Para obtener una lista completa de estas opciones, consulte [Configuración de Inventory management](configuration.md).

Las siguientes son opciones importantes que se deben conocer para [!DNL Inventory Management]:

- **[!UICONTROL Out-of-Stock Threshold]** - Establece una cantidad que se va a restar de la cantidad vendible. Si activa Pedidos No Satisfechos, este valor no se deduce de la Cantidad Vendible.
- **[!UICONTROL Backorders]** - Determina si los productos se pueden vender más allá de un inventario cero, lo que ahorra pedidos hasta que se reabastezcan. Cuando están activados los pedidos pendientes, configurar [!UICONTROL Out-of-Stock Threshold] se recomienda.

>[!NOTE]
>
>El valor de umbral Agotado admite importes negativos y positivos. Si habilita Pedidos no satisfechos, establezca este valor en una cantidad negativa para el número máximo de productos que se pueden poner en espera antes de que el producto se considere verdaderamente agotado.

## Demostración de Inventory management

Vea este vídeo para obtener más información sobre las fuentes y las existencias de Inventory management:

>[!VIDEO](https://video.tv.adobe.com/v/343748?quality=12)
