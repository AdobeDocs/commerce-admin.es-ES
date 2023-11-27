---
title: Introducción a las tiendas y a la experiencia de compra
description: Conozca las funciones utilizadas para construir y gestionar sus tiendas en línea y la experiencia de compra para sus clientes.
exl-id: 7ced9cbc-49b4-48f7-aae2-fcb48fdb888f
source-git-commit: a56509eeedbb30a1e9cacfd521ea4c18e0241d94
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# Introducción a las tiendas y a la experiencia de compra

Adobe Commerce y Magento Open Source ofrecen un conjunto completo de funciones para crear y administrar sus tiendas en línea y la experiencia de compra para sus clientes. En la instancia de Commerce, puede administrar la jerarquía de tiendas de sitios web, tiendas y vistas. También puede configurar los impuestos y las tasas de cambio necesarias para ejecutar tiendas para varias configuraciones regionales, incluidas las clases de impuestos para productos y grupos de clientes.

## Estructura del almacén

Una sola instancia de Adobe Commerce o Magento Open Source puede admitir varios sitios, tiendas o vistas de tiendas que utilicen atributos y contenido diferentes. Un escenario típico es configurar tiendas con diferentes opciones en diferentes dominios. Por ejemplo, es posible que desee un conjunto de categorías y productos en un dominio y otro conjunto de categorías y productos en un dominio diferente en otro idioma. Los comerciantes pueden configurar los sitios web, las tiendas y las vistas de las tiendas en Admin.

Si la variable [jerarquía](stores.md) está definida, puede aplicar los ajustes de configuración según lo siguiente [ámbito](../getting-started/websites-stores-views.md#scope-settings) para que cada vista de sitio, tienda y tienda proporcione el catálogo de productos y la experiencia de tienda que desee.

## Punto de compra

Adobe Commerce y el Magento Open Source reducen los errores de pedidos al verificar automáticamente el SKU y la disponibilidad de todos los artículos antes de enviar un pedido. Puede configurar las variables [carrito](cart.md) y [opciones de pago y envío](checkout-process.md) para proporcionar una experiencia de compra óptima, desde la transacción hasta la entrega. Los clientes que inician sesión en sus cuentas de pueden completar el cierre de compra rápidamente, porque gran parte de la información ya está en sus cuentas. El _Finalizar compra_ Esta página lleva al cliente a través de cada paso del proceso para completar la transacción del pedido. Si activa [Compra instantánea](checkout-instant-purchase.md)Sin embargo, los clientes pueden acelerar el proceso de cierre de compra con información guardada en su cuenta.

>[!TIP]
>
>![B2B para Adobe Commerce](../assets/b2b.svg) Con la instalación y activación de B2B para Adobe Commerce, puede configurar _Pedido rápido_ para clientes asociados a una cuenta de compañía. Esta función reduce el proceso de pedido a varios clics cuando conocen el nombre o el SKU de los productos que desean solicitar. También puede configurar la compatibilidad con Ofertas negociables para las cuentas de su compañía. Para obtener más información sobre las funciones de B2B, consulte la [Guía del usuario de B2B para Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

## Asistencia de compras

Los clientes a veces necesitan ayuda para completar una compra. A algunos clientes les gusta comprar en línea, pero prefieren pedir por teléfono. Puede ofrecer asistencia inmediata tanto a los clientes como a los clientes que se hayan registrado para obtener una cuenta en su tienda.

- [Administrar el carro de compras](shopping-assisted-cart-manage.md)
- [Creación de pedidos](customer-account-create-order.md) para clientes registrados
- [Actualizar pedidos](order-update.md)

![Carro de compras](./assets/storefront-cart-price-group-discount.png){width="700" zoomable="yes"}

Consulta este vídeo para obtener más información sobre las compras asistidas por el vendedor:

>[!VIDEO](https://video.tv.adobe.com/v/343662/?quality=12)

## Gestión de pedidos y operaciones

En Admin, los comerciantes pueden acceder a la información en cada fase del flujo de trabajo de pedidos y procesar pedidos:

- El [Pedidos](orders.md) Esta página proporciona a los comerciantes una lista fácil de acceder de todos los pedidos actuales e incluye herramientas para editar y procesar pedidos existentes y crear pedidos en nombre de clientes.

- El [Facturas](invoices.md) listas de páginas Una factura se basa en un pedido de venta temporal y proporciona un registro permanente del pedido.

- El [Envíos](shipments.md) Esta página muestra el registro de envío de cada factura que está lista para enviarse.

- El [Notas de abono](credit-memos.md) Esta página permite a los comerciantes procesar y administrar una nota de abono, que es un documento que muestra el importe que se debe al cliente. El importe puede aplicarse a una compra o reembolsarse al cliente.

- ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) La variable [Devuelve](returns.md) Esta página enumera las solicitudes de mercancía devueltas (RMA) actuales y se utiliza para introducir nuevas solicitudes de devolución.

- El [Transacciones](transactions.md) Esta página enumera todas las actividades de pago que han tenido lugar entre su tienda y un sistema de pago, y proporciona acceso a información más detallada.

## Envío y entrega

Los estudios demuestran que las tiendas ofrecen a los clientes una variedad de [métodos de envío](delivery.md) tienen tasas de conversión más altas que las tiendas que utilizan un solo método. El administrador proporciona varias herramientas que los comerciantes pueden utilizar para configurar varios métodos de entrega y [transportistas](carriers.md)y para imprimir [etiquetas de envío](shipping-labels.md).
