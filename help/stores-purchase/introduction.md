---
title: Introducción a las tiendas y a la experiencia de compra
description: Conozca las funciones utilizadas para construir y gestionar sus tiendas en línea y la experiencia de compra para sus clientes.
exl-id: 7ced9cbc-49b4-48f7-aae2-fcb48fdb888f
TQID: https://experienceleague.adobe.com/wP31dNMG9kiajirB5WTj-lEhTtHqKnl4FfqPsa3tFxs
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 680
ht-degree: 0%

---

# Introducción a las tiendas y a la experiencia de compra

Adobe Commerce y Magento Open Source ofrecen un conjunto completo de funciones para crear y administrar sus tiendas en línea y la experiencia de compra para sus clientes. En la instancia de Commerce, puede administrar la jerarquía de tienda de sitios web, tiendas y vistas. También puede configurar los impuestos y las tasas de cambio necesarias para ejecutar tiendas para varias configuraciones regionales, incluidas las clases de impuestos para productos y grupos de clientes.

## Estructura del almacén

Una sola instancia de Adobe Commerce o Magento Open Source puede admitir varios sitios, tiendas o vistas de tiendas que utilicen atributos y contenido diferentes. Un escenario típico es configurar tiendas con diferentes opciones en diferentes dominios. Por ejemplo, es posible que desee un conjunto de categorías y productos en un dominio y otro conjunto de categorías y productos en un dominio diferente en otro idioma. Los comerciantes pueden configurar los sitios web, las tiendas y las vistas de las tiendas en Admin.

Cuando se define la [jerarquía](stores.md), puede aplicar las opciones de configuración según el [ámbito](../getting-started/websites-stores-views.md#scope-settings) para que cada sitio, tienda y vista de tienda proporcione el catálogo de productos y la experiencia de tienda que desee.

## Punto de compra

Adobe Commerce y Magento Open Source reducen los errores de pedidos al verificar automáticamente el SKU y la disponibilidad de todos los artículos antes de enviar un pedido. Puede configurar el [carro](cart.md) y las [opciones de cierre de compra](checkout-process.md) para proporcionar una experiencia de compra óptima, desde la transacción hasta la entrega. Los clientes que inician sesión en sus cuentas de pueden completar el cierre de compra rápidamente, porque gran parte de la información ya está en sus cuentas. La página _Cierre de compra_ guía al cliente en cada paso del proceso para completar la transacción del pedido. Si activa [compra instantánea](checkout-instant-purchase.md), los clientes pueden acelerar el proceso de cierre de compra con la información guardada en su cuenta.

>[!TIP]
>
>![Adobe Commerce B2B](../assets/b2b.svg) Con la instalación y habilitación de Adobe Commerce B2B, puede configurar _Quick Order_ para clientes asociados a una cuenta de compañía. Esta función reduce el proceso de pedido a varios clics cuando conocen el nombre o el SKU de los productos que desean solicitar. También puede configurar la compatibilidad con Ofertas negociables para las cuentas de su compañía. Para obtener más información sobre las características de B2B, consulte la [Guía del usuario de Adobe Commerce B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=es).

## Asistencia de compras

Los clientes a veces necesitan ayuda para completar una compra. A algunos clientes les gusta comprar en línea, pero prefieren pedir por teléfono. Puede ofrecer asistencia inmediata tanto a los clientes como a los clientes que se hayan registrado para obtener una cuenta en su tienda.

- [Administrar el carro de compras](shopping-assisted-cart-manage.md)
- [Crear pedidos](customer-account-create-order.md) para clientes registrados
- [Actualizar pedidos](order-update.md)

![Carro de compras](./assets/storefront-cart-price-group-discount.png){width="700" zoomable="yes"}

Consulta este vídeo para obtener más información sobre las compras asistidas por el vendedor:

>[!VIDEO](https://video.tv.adobe.com/v/343662/?quality=12&learn=on)

## Gestión de pedidos y operaciones

En Admin, los comerciantes pueden acceder a la información en cada fase del flujo de trabajo de pedidos y procesar pedidos:

- La página [Pedidos](orders.md) proporciona a los comerciantes una lista fácil de acceder de todos los pedidos actuales e incluye herramientas para editar y procesar pedidos existentes, así como para crear pedidos en nombre de clientes.

- La página [Facturas](invoices.md) enumera una factura basada en un pedido de venta temporal y proporciona un registro permanente del pedido.

- La página [Envíos](shipments.md) muestra el registro de envío de cada factura que está lista para enviarse.

- La página [Notas de crédito](credit-memos.md) permite a los comerciantes procesar y administrar una nota de crédito, que es un documento que muestra el importe que se debe al cliente. El importe puede aplicarse a una compra o reembolsarse al cliente.

- ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) La página [Devuelve](returns.md) enumera las solicitudes de mercancía devueltas (RMA) actuales y se usa para introducir nuevas solicitudes de devolución.

- La página [Transacciones](transactions.md) enumera toda la actividad de pago que se ha realizado entre su tienda y un sistema de pago, y proporciona acceso a información más detallada.

## Envío y entrega

Los estudios demuestran que las tiendas que ofrecen a los clientes la opción de elegir entre varios [métodos de envío](delivery.md) tienen tasas de conversión más altas que las tiendas que utilizan un solo método. El administrador proporciona varias herramientas que los comerciantes pueden usar para configurar varios métodos de entrega y [transportistas](carriers.md), así como para imprimir [etiquetas de envío](shipping-labels.md).
