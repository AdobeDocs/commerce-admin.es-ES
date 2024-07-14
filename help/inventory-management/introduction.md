---
title: Introducción a Inventory management
description: Aprenda a utilizar las características de  [!DNL Inventory Management] para administrar las existencias en varias ubicaciones y que su tienda refleje con precisión el inventario físico. [!DNL Commerce]
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# Introducción a Inventory management

[!DNL Inventory Management] para [!DNL Commerce] le proporciona las herramientas para administrar el inventario de productos. Los comerciantes con una sola tienda en varios almacenes, tiendas, ubicaciones de recogida, distribuidores directos entre otros pueden utilizar estas funciones para mantener las cantidades de ventas y gestionar los envíos para completar pedidos. Puede realizar un seguimiento de las cantidades de inventario, proporcionar cantidades precisas de existencias vendibles a los clientes para todos los sitios web y enviar según las recomendaciones basadas en la distancia o la prioridad. También puede configurar las configuraciones de producto preferidas globalmente (para todas las tiendas y productos), por origen y por producto. Estas funciones aumentan con su empresa, lo que le permite trabajar desde un único almacén o desde una compleja red de envío con algunos ajustes adicionales.

[!DNL Inventory Management] características incluyen:

- Diferentes configuraciones para comerciantes cuyo inventario se origina desde un único origen y desde varios orígenes
- Existencias para el seguimiento de las cantidades agregadas disponibles a través de los orígenes asignados
- Protección de cierre de compra simultáneo
- Algoritmos de coincidencia de envíos

>[!NOTE]
>
>Estas características se desarrollaron como parte del proyecto [Inventory management](https://github.com/magento/inventory) (anteriormente MSI) a través del programa de ingeniería de la comunidad.<br/>
>
>El módulo [!DNL Inventory Management] se instala con Magento Open Source y Adobe Commerce, con todas las características habilitadas de forma predeterminada. Para obtener información acerca de los cambios incluidos en las versiones de módulos, consulte las [Notas de la versión](release-notes.md).

## Terminología básica

Es importante que entienda los siguientes términos cuando trabaje con [!DNL Inventory Management]:

[!UICONTROL **Fuentes**] representan ubicaciones físicas que almacenan y envían productos disponibles. Estas ubicaciones pueden incluir almacenes, tiendas físicas, centros de distribución y transportistas de entrega. (Cualquier ubicación puede designarse como fuente para los productos virtuales).

[!UICONTROL **Existencias**] asignan un canal de ventas (actualmente limitado a sitios web) a ubicaciones de origen e inventario disponible. Un inventario puede asignarse a varios canales de ventas, pero un canal de ventas solo puede asignarse a un inventario.

[!UICONTROL **Cantidad vendible agregada**] es el inventario virtual total que se puede vender a través de un canal de ventas. La cantidad se calcula entre todos los orígenes asignados a un stock.

[!UICONTROL **Reservas**] realiza un seguimiento de las deducciones de la cantidad vendible a medida que los clientes agregan productos al carro de compras y completan el cierre de compra. Cuando se envía un pedido, la reserva borra y deduce los importes enviados de cantidades de inventario de origen específicas.
