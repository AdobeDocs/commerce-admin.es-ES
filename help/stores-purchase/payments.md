---
title: Resumen de pagos
description: Obtenga información acerca de los métodos y servicios de pago compatibles de forma nativa con Adobe Commerce y Magento Open Source.
exl-id: 474bf6df-96e2-4db3-ad3c-1804b5de33b0
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 0%

---

# Resumen de pagos

Adobe Commerce y Magento Open Source admiten varios métodos y servicios de pago que puede ofrecer para facilitar el pago y la comodidad del cliente. Esta lista incluye varios métodos de pago sin conexión, incluido el pago mediante cheque o giro postal y el pago contra reembolso (COD). También hay integraciones nativas para numerosas soluciones de pago en línea y puertas de enlace, incluyendo Braintree como una extensión desarrollada por el proveedor.

>[!TIP]
>
>Payment Services for Adobe Commerce and Magento Open Source ofrece una solución de autoservicio llave en mano que incluye pruebas de zona protegida y una configuración sencilla para proporcionar un procesamiento de pagos sólido y seguro. Para obtener más información sobre este potente conjunto de herramientas y cómo puede proporcionarte la perspectiva y el control necesarios para crear la mejor experiencia para tus compradores, consulta la [Guía del usuario de Payment Services](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

>[!NOTE]
>
>Revise la [Directrices de conformidad con PCI](../getting-started/compliance-pci.md) que describen los requisitos establecidos por la industria de tarjetas de pago (PCI) para las empresas que aceptan pagos con tarjeta de crédito a través de Internet.

## Cambios en 2.4

Algunas integraciones de pago y extensiones agrupadas se han eliminado en las versiones 2.4.x y se han trasladado al Commerce Marketplace. Puede encontrar las extensiones de integración de pagos oficiales más recientes en [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target=&quot;_blank&quot;}.

- **Amazon Pay** y **Klarna**: Adobe Commerce y las versiones 2.4.0 a 2.4.3 de Magento Open Source incluían estas extensiones desarrolladas por el proveedor. A partir de la versión 2.4.4, estas extensiones ya no se incluyen en la versión principal y deben instalarse y actualizarse desde el Commerce Marketplace. Marketplace también proporciona acceso a la documentación actual proporcionada por el desarrollador de extensiones.

  Si tiene alguna de estas extensiones agrupadas habilitada y configurada, debe actualizar el archivo composer.json como parte del proceso de actualización 2.4.4 y administrar las actualizaciones de extensión a partir de ahora. Consulte [Actualización de módulos](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) en el _Guía de actualización_ para obtener más información.

- **Worldpay**, **Eway**, **CyberSource**, y **Authorize.Net**: Para obtener más información sobre cómo realizar una transición segura desde estas integraciones de pago, consulte la [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target=&quot;_blank&quot;}.

## Métodos de pago sin conexión

Adobe Commerce y Magento Open Source incluyen varios métodos de pago sin conexión integrados, que no requieren los servicios de una empresa de procesamiento de pagos de terceros:

- [Cierre de compra con subtotal cero](zero-subtotal-checkout.md)
- [Pago contra reembolso](cash-on-delivery.md)
- [Pago de transferencia bancaria](bank-transfer.md)
- [Cheque / giro postal](check-money-order.md)
- [Pedido de compra](purchase-order.md)
- [Pago a cuenta](../b2b/enable-basic-features.md#configure-payment-on-account) ![B2B para Adobe Commerce](../assets/b2b.svg) (Disponible con B2B para Adobe Commerce)

## Métodos de pago en línea

Adobe Commerce y Magento Open Source admiten numerosas soluciones de pago que ofrecen servicios comerciales en todas partes del mundo. A diferencia de las soluciones de pago que transfieren el control a otro sitio para completar la transacción, una pasarela de pago le permite aceptar pagos con tarjeta de crédito directamente desde su tienda sin que el cliente salga de su sitio.

### Soluciones recomendadas

- [Servicios de pago](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html)
- [Pago y envío con PayPal Express](paypal-express-checkout.md)
- [Braintree](braintree.md)

### Otras soluciones de pago de PayPal

Consulte [Soluciones de pago PayPal](paypal.md) para obtener más información sobre las opciones de formas de pago de PayPal.

#### Soluciones todo en uno de PayPal

- [Pagos mediante PayPal avanzados](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal Payments Standard](paypal-payments-standard.md)

#### Puertas de pago PayPal

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [Vínculo de flujo de pago PayPal](paypal-payflow-link.md)

## Protección contra el fraude

Los servicios y filtros de protección contra el fraude examinan las solicitudes enviadas antes de que se procese la transacción para detectar las solicitudes fraudulentas y protegerle de los gastos de devolución de cargos. Adobe Commerce y Magento Open Source admiten las siguientes soluciones de protección contra el fraude:

- [Filtro de gestión de fraude de PayPal](paypal.md#paypal-fraud-management-filters)

- [Soluciones de protección contra el fraude en Marketplace][1]

>[!NOTE]
>
>Para admitir actualizaciones para el cumplimiento de la seguridad, la protección contra fraude Signifyd se elimina de Commerce a partir de la versión 2.4.0. Si ha estado utilizando la integración Signifyd en una versión 2.3.x o anterior, se recomienda realizar la transición a la versión [Extensión de protección contra fraudes y contracargos significativa](https://marketplace.magento.com/signifyd-module-connect.html){:target=&quot;_blank&quot;}. Asegúrese de mantener las actualizaciones de la extensión según las directrices del proveedor.

## Solución de problemas de recursos

Si necesita ayuda para solucionar problemas de pago, consulte la [Base de conocimiento de asistencia](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html?lang=en).

[1]: https://marketplace.magento.com/catalogsearch/result?q=fraud%20protection
