---
title: Introducción a  [!DNL Inventory Management]
description: Aprenda a usar [!DNL Inventory Management] for [!DNL Commerce] para administrar el inventario entre orígenes y existencias, calcular las cantidades vendibles, hacer un seguimiento de las reservas y admitir el cumplimiento de pedidos. Use el Administrador para configurar y generar informes, y la interfaz de línea de comandos para cambios de configuración y fondo.
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
source-git-commit: 125a49f740639bce0ced8063074ca43d627c0eac
workflow-type: tm+mt
source-wordcount: 371
ht-degree: 0%

---

# Introducción a [!DNL Inventory Management]

[!DNL Inventory Management] para [!DNL Commerce] ayuda a los comerciantes a administrar el inventario en uno o más sitios web y en ubicaciones de productos físicas o virtuales. Proporciona herramientas en la interfaz de línea de comandos y administración para configurar el inventario, realizar un seguimiento de las cantidades disponibles y agregadas, proteger el inventario durante el cierre de compra y admitir el cumplimiento de pedidos. Puede utilizar [!DNL Inventory Management] para una única fuente o una red de varios orígenes que incluya almacenes, tiendas, ubicaciones de recogida, distribuidores directos entre terceros y otras ubicaciones de entrega.

## Formas de usar [!DNL Inventory Management]

- **Administrador:** Establezca opciones de inventario y genere informes de inventario.
- **Interfaz de línea de comandos:** Ejecute comandos de instalación y aplique los cambios de inventario en segundo plano.
- **Ámbito de configuración:** Configure las opciones de inventario de forma global, por origen o por producto.

## Características principales

[!DNL Inventory Management] características incluyen:

- Diferentes configuraciones para comerciantes cuyo inventario se origina desde un único origen o desde varios orígenes
- Existencias para el seguimiento de cantidades vendibles agregadas entre orígenes asignados
- Protección de cierre de compra simultáneo
- Algoritmos de coincidencia de envíos que admiten recomendaciones de cumplimiento basadas en la distancia o la prioridad

>[!NOTE]
>
>Estas características se desarrollaron como parte del proyecto [Inventory management](https://github.com/magento/inventory) (anteriormente MSI) a través del programa de ingeniería de la comunidad.<br/>
>
>El módulo [!DNL Inventory Management] se instala con Magento Open Source y Adobe Commerce, con todas las características habilitadas de forma predeterminada. Para obtener información acerca de los cambios incluidos en las versiones de módulos, consulte las [Notas de la versión](release-notes.md).

## Terminología básica

Es importante que entienda los siguientes términos cuando trabaje con [!DNL Inventory Management]:

[!UICONTROL Sources] representan ubicaciones físicas que almacenan y envían productos disponibles. Consulte [Existencias y orígenes](sources-stocks.md) para ver ejemplos y diagramas. (Cualquier ubicación puede designarse como fuente para los productos virtuales).

[!UICONTROL Stocks] asigna un canal de ventas (actualmente limitado a sitios web) a ubicaciones de origen e inventario disponible. Un inventario puede asignarse a varios canales de ventas, pero un canal de ventas solo puede asignarse a un inventario.

[!UICONTROL Aggregate Salable Quantity] es el inventario virtual total que se puede vender a través de un canal de ventas. La cantidad se calcula entre todos los orígenes asignados a un stock.

[!UICONTROL Reservations] realiza el seguimiento de las deducciones de la cantidad vendible a medida que los clientes agregan productos a los carros de compras y completan el cierre de compra. Cuando se envía un pedido, la reserva borra y deduce los importes enviados de cantidades de inventario de origen específicas.
