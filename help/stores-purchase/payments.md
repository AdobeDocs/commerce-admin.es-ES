---
title: Resumen de pagos
description: Conozca los métodos y servicios de pago compatibles de forma nativa con Adobe Commerce y Magento Open Source.
exl-id: 474bf6df-96e2-4db3-ad3c-1804b5de33b0
feature: Payments
source-git-commit: 15118877bb8cc533b2323819db34da0513899e25
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Resumen de pagos

Adobe Commerce y Magento Open Source admiten una amplia variedad de métodos y servicios de pago. Esto incluye varios métodos de pago sin conexión, incluyendo el pago por cheque o giro postal y el pago contra reembolso (COD). También hay integraciones nativas para numerosas soluciones de pago en línea y puertas de enlace, incluida Braintree como extensión desarrollada por el proveedor.

>[!TIP]
>
>Payment Services para Adobe Commerce y Magento Open Source proporciona una solución de autoservicio llave en mano que incluye pruebas de zona protegida y una configuración sencilla para proporcionar un procesamiento de pagos sólido y seguro. Para obtener más información sobre este potente conjunto de herramientas y cómo puede proporcionarte el control y el insight que necesitas para crear la mejor experiencia para tus compradores, consulta la [Guía del usuario de servicios de pago](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html?lang=es). Esta es la solución de pagos predeterminada en [Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/es/docs/commerce/cloud-service/overview).

>[!NOTE]
>
>Revise las [directrices de cumplimiento de PCI](../getting-started/compliance-pci.md) que describen los requisitos establecidos por la industria de tarjetas de pago (PCI) para las empresas que aceptan pagos con tarjeta de crédito a través de Internet.

## Cambios en 2.4

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."}

Algunas integraciones de pago y extensiones agrupadas se han eliminado en las versiones 2.4.x y se han trasladado a Commerce Marketplace. Puedes encontrar las extensiones de integración de pagos oficiales más recientes en [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"}.

- **Amazon Pay** y **Klarna**: las versiones 2.4.0 a 2.4.3 de Adobe Commerce y Magento Open Source incluían estas extensiones desarrolladas por el proveedor. A partir de la versión 2.4.4, estas extensiones ya no se incluyen en la versión principal y deben instalarse y actualizarse desde Commerce Marketplace. Marketplace también proporciona acceso a la documentación actual proporcionada por el desarrollador de extensiones.

  Si tiene alguna de estas extensiones agrupadas habilitada y configurada, debe actualizar el archivo composer.json como parte del proceso de actualización 2.4.4 y administrar las actualizaciones de extensión a partir de ahora. Consulte [Módulos de actualización](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html?lang=es) en la _Guía de actualización_ para obtener más información.

- **Worldpay**, **Eway**, **CyberSource** y **Authorize.Net**: Para obtener más información sobre cómo realizar una transición segura a partir de estas integraciones de pago, consulta [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"}.

## Métodos de pago sin conexión

Adobe Commerce y Magento Open Source incluyen varios métodos de pago sin conexión integrados, que no requieren los servicios de una empresa de procesamiento de pagos de terceros:

- [Cierre de compra con subtotal cero](zero-subtotal-checkout.md)
- [Pago contra reembolso](cash-on-delivery.md)
- [Pago de transferencia bancaria](bank-transfer.md)
- [Cheque / giro postal](check-money-order.md)
- [Pedido de compra](purchase-order.md)
- [Pago en la cuenta](../b2b/enable-basic-features.md#configure-payment-on-account) ![Adobe Commerce B2B](../assets/b2b.svg) (disponible con Adobe Commerce B2B)

## Métodos de pago en línea

Adobe Commerce y Magento Open Source admiten numerosas soluciones de pago que ofrecen servicios comerciales en todas partes del mundo. A diferencia de las soluciones de pago que transfieren el control a otro sitio para completar la transacción, una pasarela de pago le permite aceptar pagos con tarjeta de crédito directamente desde su tienda sin que el cliente salga de su sitio.

### Soluciones recomendadas

- [Servicios de pago](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html?lang=es)
- [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."} [Pago y envío de PayPal Express](paypal-express-checkout.md)
- [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."} [Braintree](braintree.md)

### Otras soluciones de pago de PayPal

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."}

Consulta [Soluciones de pago PayPal](paypal.md) para obtener más información sobre las opciones de métodos de pago PayPal.

#### Soluciones todo en uno de PayPal

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."}

- [Pagos mediante PayPal avanzados](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal Payments Standard](paypal-payments-standard.md)

#### Puertas de pago PayPal

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."}

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [Vínculo de flujo de pago PayPal](paypal-payflow-link.md)

## Protección contra el fraude

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."}

Los servicios y filtros de protección contra el fraude examinan las solicitudes enviadas antes de que se procese la transacción para detectar las solicitudes fraudulentas y protegerle de los gastos de devolución de cargos. Adobe Commerce y Magento Open Source admiten las siguientes soluciones de protección contra el fraude:

- [Filtro de gestión de fraude de PayPal](paypal.md#paypal-fraud-management-filters)

- [Soluciones de protección contra el fraude en Marketplace][1]

>[!NOTE]
>
>Para admitir actualizaciones de la conformidad con la seguridad, la protección contra fraudes significativa se elimina de Commerce a partir de la versión 2.4.0. Si ha estado utilizando la integración Signifyd en una versión 2.3.x o anterior, se recomienda realizar la transición a la [extensión Signifyd Fraud &amp; Chargeback Protection](https://marketplace.magento.com/signifyd-module-connect.html){:target="_blank"}. Asegúrese de mantener las actualizaciones de la extensión según las directrices del proveedor.

## Solución de problemas de recursos

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."}

Para obtener ayuda para solucionar problemas de pago, consulte la [Base de conocimiento de soporte técnico](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html?lang=es).

[1]: https://marketplace.magento.com/catalogsearch/result?q=fraud%20protection
