---
title: Menú [!UICONTROL Sales]
description: El administrador de Commerce incluye el menú [!UICONTROL Sales], que proporciona acceso a las herramientas para trabajar con pedidos según su ubicación en el flujo de trabajo.
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
TQID: https://experienceleague.adobe.com/mliJ1Q1-DEkR5rAoIRLQ9qBxQopBytjicPiqzWTg7ac
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-wordcount: 579
ht-degree: 0%

---

# Menú [!UICONTROL Sales]

El menú Ventas enumera las transacciones según su ubicación en el flujo de trabajo del pedido. Puede considerar cada una de las opciones como una etapa diferente durante la vida útil de un pedido.

>[!BEGINTABS]

>[!TAB Adobe Commerce]

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."}

![Menú de ventas](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

>[!TAB Adobe Commerce as a Cloud Service]

[!BADGE Solo SaaS]{type=Positive url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Solo se aplica a los proyectos de Adobe Commerce as a Cloud Service y Adobe Commerce Optimizer (infraestructura de SaaS administrada por Adobe)."}

![Menú de ventas](./assets/admin-menu-sales-accs.png){width="450" zoomable="yes"}

>[!ENDTABS]

## Mostrar el menú [!UICONTROL Sales]

En la barra lateral _Admin_, haga clic en **[!UICONTROL Sales]**.

## Opciones de menú

### [!UICONTROL Quotes]

![Adobe Commerce B2B](../assets/b2b.svg) (disponible con Adobe Commerce B2B)

Los compradores autorizados pueden [negociar el precio](../b2b/quotes.md) con el vendedor enviando una [solicitud](../b2b/quote-request.md) desde el carro de compras.

### [!UICONTROL Quote Templates]

![Adobe Commerce B2B](../assets/b2b.svg) (disponible con Adobe Commerce B2B)

Permite a compradores y vendedores optimizar el proceso de oferta creando [plantillas de oferta](../b2b/quote-templates-overview.md) reutilizables y personalizables.

### [!UICONTROL Orders]

Cuando se realiza un [pedido](orders.md), se crea un pedido de ventas como un registro temporal de la transacción. El pago no se ha procesado y el pedido se puede cancelar.

### [!UICONTROL Invoices]

Una [factura](invoices.md) es un registro del recibo de pago de un pedido. Se pueden crear varias facturas para un único pedido, cada una con tantos o tan pocos de los productos comprados que especifique. Según la acción de pago, el pago se puede capturar automáticamente cuando se genera la factura.

### [!UICONTROL Shipments]

Un [envío](shipments.md) es un registro de los productos de un pedido que se han enviado. Al igual que con las facturas, se pueden asociar varios envíos a un único pedido, hasta que se envíen todos los productos del pedido.

### [!UICONTROL Credit Memos]

Un [abono](credit-memos.md) es un documento que muestra el importe que se debe al cliente por un reembolso total o parcial. El importe puede aplicarse a una compra o reembolsarse al cliente.

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

Se puede otorgar una [autorización de devolución de mercancía](returns.md) (RMA) a los clientes que soliciten la devolución de un artículo para su reemplazo o reembolso. Las RMA se pueden emitir para tipos de producto simples, agrupados, configurables y agrupados. Sin embargo, las RMA no están disponibles para productos virtuales y descargables ni para tarjetas regalo.

### [!UICONTROL Billing Agreements]

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."}

Un [acuerdo de facturación](paypal-billing-agreements.md) es similar a un pedido de compra, excepto que no se limita a una sola compra. Durante el cierre de compra, el cliente elige el Contrato de facturación como método de pago. Un acuerdo de facturación optimiza el proceso de cierre de compra porque el cliente no tiene que introducir la información de pago de cada compra.

### [!UICONTROL Transactions]

La página [Transacciones](transactions.md) enumera toda la actividad de pago que se ha realizado entre su tienda y todos los sistemas de pago, y proporciona acceso a información más detallada.

### [!UICONTROL Braintree Virtual Terminal]

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."}

En la página Terminal virtual de Braintree, un usuario administrador puede aceptar el pago del importe seleccionado. Para que la característica de terminal esté disponible, el comerciante debe establecer la [configuración básica de Braintree](braintree.md). Braintree ofrece una experiencia de pago y envío totalmente personalizable con detección de fraude e integración con PayPal.

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

(La opción de archivar debe estar habilitada) [El archivado de pedidos](order-archive.md) y otros documentos de ventas mejora regularmente el rendimiento y mantiene el espacio de trabajo libre de información innecesaria.
