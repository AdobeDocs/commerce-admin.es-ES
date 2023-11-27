---
title: '[!UICONTROL Sales] menu'
description: El administrador de Commerce incluye el [!UICONTROL Sales] , que proporciona acceso a las herramientas para trabajar con pedidos según su ubicación en el flujo de trabajo.
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
source-git-commit: a7c6203cf738e3fb9be887d637010ca9c155937a
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# [!UICONTROL Sales] menú

El menú Ventas enumera las transacciones según su ubicación en el flujo de trabajo del pedido. Puede considerar cada una de las opciones como una etapa diferente durante la vida útil de un pedido.

![Menú Ventas](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

## Mostrar el [!UICONTROL Sales] menú

En el _Administrador_ barra lateral, haga clic en **[!UICONTROL Sales]**.

## Opciones de menú

### [!UICONTROL Quotes]

![B2B para Adobe Commerce](../assets/b2b.svg) (Disponible con B2B para Adobe Commerce)

Los compradores autorizados pueden [negociar el precio](../b2b/quotes.md) con el vendedor enviando un [solicitud](../b2b/quote-request.md) del carro de compras.

### [!UICONTROL Orders]

Cuando un [pedido](orders.md) se realiza, se crea un pedido de venta como un registro temporal de la transacción. El pago no se ha procesado y el pedido se puede cancelar.

### [!UICONTROL Invoices]

Un [factura](invoices.md) es un registro de la recepción del pago de un pedido. Se pueden crear varias facturas para un único pedido, cada una con tantos o tan pocos de los productos comprados que especifique. Según la acción de pago, el pago se puede capturar automáticamente cuando se genera la factura.

### [!UICONTROL Shipments]

A [envío](shipments.md) es un registro de los productos de un pedido enviado. Al igual que con las facturas, se pueden asociar varios envíos a un único pedido, hasta que se envíen todos los productos del pedido.

### [!UICONTROL Credit Memos]

A [nota de crédito](credit-memos.md) es un documento que muestra el importe que se debe al cliente para un reembolso completo o parcial. El importe puede aplicarse a una compra o reembolsarse al cliente.

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

A [autorización de mercancía devuelta](returns.md) (RMA) se puede conceder a los clientes que soliciten la devolución de un artículo para su sustitución o reembolso. Las RMA se pueden emitir para tipos de producto simples, agrupados, configurables y agrupados. Sin embargo, las RMA no están disponibles para productos virtuales y descargables ni para tarjetas regalo.

### [!UICONTROL Billing Agreements]

A [contrato facturación](paypal-billing-agreements.md) es similar a un pedido de compra, excepto que no se limita a una sola compra. Durante el cierre de compra, el cliente elige el Contrato de facturación como método de pago. Un acuerdo de facturación optimiza el proceso de cierre de compra porque el cliente no tiene que introducir la información de pago de cada compra.

### [!UICONTROL Transactions]

El [Transacciones](transactions.md) Esta página enumera todas las actividades de pago que han tenido lugar entre su tienda y todos los sistemas de pago, y proporciona acceso a información más detallada.

### [!UICONTROL Braintree Virtual Terminal]

En la página Terminal virtual del Braintree, un usuario administrador puede aceptar el pago del importe seleccionado. Para que la función de terminal esté disponible, un comerciante debe configurar [configuración del Braintree](braintree.md). Braintree ofrece una experiencia de pago totalmente personalizable con detección de fraude e integración con PayPal.

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

(La opción Archivar debe estar activada) [Archivado de pedidos](order-archive.md) y otros documentos de ventas mejoran regularmente el rendimiento y mantienen su espacio de trabajo libre de información innecesaria.
