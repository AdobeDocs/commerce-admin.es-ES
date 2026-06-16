---
title: Segmentos de cliente
description: Los segmentos de cliente le permiten mostrar dinámicamente contenido y promociones a clientes específicos.
exl-id: b254a6ac-cb0b-46c1-9ef7-ffc97360a98e
TQID: https://experienceleague.adobe.com/K10qvsYlYebR6fJG8-QNI5qrqwjE-Sn-kSxzfiuoXdo
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 492
ht-degree: 0%

---

# Segmentos de clientes

Los segmentos de clientes le permiten mostrar dinámicamente contenido y promociones a clientes específicos, en función de varias propiedades. Algunos ejemplos son la dirección del cliente, el historial de pedidos y el contenido del carro de compras. Puede optimizar las iniciativas de marketing en función de segmentos segmentados con reglas de precios del carro de compras. También puede generar informes y exportar la lista de clientes objetivo. Debido a que la información del segmento del cliente se actualiza constantemente, los clientes pueden asociarse y desasociarse de un segmento a medida que compran en su tienda.

Para comprender mejor la diferencia entre [grupos de clientes](../customers/customer-groups.md) y los segmentos de clientes, tenga en cuenta dónde se utilizan:

|  | Segmento de cliente | Grupo de clientes |
|--- |--- |--- |
| Regla de precio de catálogo |  | ✔️ |
| Regla de precio del carro | ✔️ | ✔️ |
| Precio de nivel |  | ✔️ |
| Regla de producto relacionada | ✔️ |  |
| Bloque dinámico | ✔️ |  |
| Tasas de cambio de recompensa |  | ✔️ |
| Permisos de categoría |  | ✔️ |
| Invitaciones |  | ✔️ |

{style="table-layout:auto"}

## Atributos de segmento de clientes

Los atributos del segmento de clientes se definen de manera similar a las reglas de precios del catálogo y del carro de compras. Para que se use un atributo en una condición de segmento de cliente, la _[!UICONTROL Use in Customer Segment]_[propiedad](attribute-properties.md#) debe establecerse en `Yes`. Las condiciones de los segmentos de cliente pueden incorporar los siguientes tipos de atributos:

| Atributo | Descripción |
|---|---|
| `Customer Address Fields` | Puede definir cualquiera de los campos de dirección, como ciudad o país. Cualquier dirección de la libreta de direcciones de un cliente puede cumplir estas condiciones. O bien, puede especificar que sólo se puedan utilizar las direcciones de facturación o envío predeterminadas para hacer coincidir un cliente. Los atributos de dirección del cliente solo están disponibles para los clientes que han iniciado sesión en sus cuentas. |
| `Customer Information Fields` | Se puede definir información diversa sobre el cliente, incluido el grupo de clientes, el nombre, el correo electrónico, el estado de suscripción al boletín informativo y el saldo de crédito de tienda. La información del cliente solo está disponible para los clientes que iniciaron sesión en sus cuentas. |
| `Cart Fields` | Las propiedades del carro de compras se pueden basar en la cantidad (artículos de línea o cantidad total) o en el valor (como el total general, los impuestos y la tarjeta regalo) del contenido del carro de compras. |
| `Products` | Puede hacer referencia a productos que están actualmente en el carro de compras o en la lista de deseos, o que se han visto o solicitado anteriormente. También puede establecer un intervalo de fechas en el que se produjo. Los productos se definen mediante atributos de producto. |
| `Order Fields` | Las características de los pedidos anteriores se pueden definir en función de la dirección de facturación/envío del pedido, el importe total (o medio) o la cantidad de los pedidos, o el número total de pedidos. También puede establecer un intervalo de fechas para cuándo se produjo y el estado de los pedidos que cumplen estas condiciones. Disponible solo para clientes que han iniciado sesión. Las condiciones establecidas para los compradores que no han iniciado sesión dejan de funcionar cuando inician sesión. |

{style="table-layout:auto"}

Consulte [Crear y eliminar segmentos de clientes](../customers/customer-segment-create.md) para obtener más información sobre cómo definir segmentos de clientes.

## eBooks

- **Segmentación de clientes**: obtenga el [libro electrónico](https://business.adobe.com/resources/identifying-your-most-profitable-customers-introduction-customer-segmentation.html) para aprender a aumentar las ganancias y la satisfacción general del cliente.
- **Tácticas de segmentación**: obtenga el [libro electrónico](https://business.adobe.com/resources/3-segmentation-tactics-ignite-conversion.html) para mejorar el direccionamiento de sus mensajes y promociones y crear conversaciones significativas con sus clientes.
