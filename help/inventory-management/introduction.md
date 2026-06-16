---
title: Introducción a Inventory management
description: 'Aprenda a utilizar las características de  [!DNL Inventory Management] para administrar las existencias en varias ubicaciones y que su tienda refleje con precisión el inventario físico. [!DNL Commerce] '
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
TQID: https://experienceleague.adobe.com/7v-G-DZEki7y-4HSmq-rJxsmu6vih26jRYYCRRUF-XY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 364
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
