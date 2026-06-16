---
title: '[!UICONTROL Sales] > [!UICONTROL Payment Methods]'
description: Revise la configuración en la página [!UICONTROL Sales] > [!UICONTROL Payment Methods] del administrador de Commerce.
exl-id: 6545b980-c8ef-460a-a884-d5315f5ad513
feature: Configuration, Payments
TQID: https://experienceleague.adobe.com/Z6f-lyypn4xUeVxiR0SQ81PswzU69X3sVCqEa8bTDnc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1746
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods]

>[!TIP]
>
>Payment Services para Adobe Commerce y Magento Open Source proporciona una solución de autoservicio llave en mano que incluye pruebas de zona protegida y una configuración sencilla para proporcionar un procesamiento de pagos sólido y seguro. Para obtener más información sobre este potente conjunto de herramientas y cómo puede proporcionarte el control y el insight que necesitas para crear la mejor experiencia para tus compradores, consulta la [_Guía del usuario de servicios de pago_](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html?lang=es).

{{config}}

## [!UICONTROL Merchant Location]

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."}

![Ubicación del comerciante](./assets/payment-methods-merchant-location.png)<!-- zoom -->

<!-- [Merchant Location](https://experienceleague.adobe.com/es/docs/commerce-admin/start/setup/store-details#merchant-location) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Merchant Country] | Sitio web | Identifica el país en el que el comerciante está registrado para realizar negocios. |

{style="table-layout:auto"}

## Soluciones recomendadas

Las siguientes soluciones de pago se recomiendan como una manera fácil para los comerciantes que están empezando a aceptar pagos en línea por cuenta PayPal o tarjeta de crédito. A medida que tu negocio crezca, puedes combinarlo con soluciones de pago adicionales de PayPal.

- [Servicios de pago](payment-services.md)
- [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."} [Pago y envío de PayPal Express](paypal-express-checkout.md)
- [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."} [Braintree](braintree.md)

>[!NOTE]
>
>Algunas integraciones de pago y extensiones agrupadas se han eliminado en las versiones 2.4.x y se han trasladado a Commerce Marketplace. Puede encontrar las extensiones de integración de pagos oficiales más recientes en [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"}.
><br/>>**Amazon Pay** y **Klarna**: las versiones 2.4.0 a 2.4.3 de Adobe Commerce y Magento Open Source incluían estas extensiones desarrolladas por el proveedor. A partir de la versión 2.4.4, estas extensiones ya no se incluyen en la versión principal y deben instalarse y actualizarse desde Commerce Marketplace. Marketplace también proporciona acceso a la documentación actual proporcionada por el desarrollador de extensiones.
><br/>>Si tiene habilitada y configurada alguna de estas extensiones agrupadas, debe actualizar el archivo `composer.json` como parte del proceso de actualización de la versión 2.4.4 y administrar las actualizaciones de extensión en adelante. Consulte [Módulos de actualización](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html?lang=es) en la _Guía de actualización_ para obtener más información.<br/>
><br/>>**Worldpay**, **Eway**, **CyberSource** y **Authorize.Net**: Para obtener más información sobre cómo realizar una transición segura desde estas integraciones de pago, consulta [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"}.

## Otros métodos de PayPal

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."}

PayPal ofrece varias soluciones de pago que satisfacen las necesidades de las empresas de todos los tamaños, y que se dedican a los negocios en todo el mundo. PayPal te permite aceptar pagos de todas las principales tarjetas de débito y crédito. PayPal ofrece comodidad adicional sin esfuerzo adicional, porque incluso los clientes que no tienen una cuenta PayPal pueden pagar sus compras con PayPal.

### Métodos todo en uno de PayPal

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."}

- [Pago mediante PayPal avanzado](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal Payments Standard](paypal-payments-standard.md)

### Puertas de pago PayPal

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."}

- [PayPal Payflow Pro](paypal-payflow-pro.md) (incluye Pago y envío exprés)
- [Vínculo de flujo de pago de PayPal](paypal-payflow-link.md) (incluye Pago y envío exprés)

## Métodos de pago básicos

Los siguientes métodos de pago están incorporados en Commerce y no utilizan un proveedor de pagos de terceros para procesar la transacción. Muchos de los métodos de pago básicos se gestionan sin conexión, en lugar de en línea.

### [!UICONTROL Check / Money Order]

![Cheque / giro postal](./assets/payment-methods-check-money-order.png)<!-- zoom -->

<!-- [Check / Money Order](https://experienceleague.adobe.com/es/docs/commerce-admin/stores-sales/payments/offline/check-money-order) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enabled] | Sitio web | Determina si los clientes pueden pagar mediante cheque o giro postal. Opciones: `Yes` / `No` |
| [!UICONTROL Title] | Vista de tienda | El nombre de esta forma de pago que aparece a los clientes durante el cierre de compra. |
| [!UICONTROL New Order Status] | Sitio web | Determina el [estado de pedido](../../stores-purchase/order-status.md) inicial asignado a pedidos pagados por un cheque o giro postal. Valor predeterminado: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Sitio web | Determina los países desde los que se acepta el pago mediante cheque o giro postal. Opciones: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Sitio web | Identifica los países específicos desde los que acepta el pago mediante cheque o giro postal. |
| [!UICONTROL Make Check Payable to] | Vista de tienda | El nombre de la entidad a la que deben hacerse pagaderos los cheques y las órdenes de pago. |
| [!UICONTROL Send Check to] | Vista de tienda | La dirección postal a la que deben enviarse los cheques y giros postales. |
| [!UICONTROL Minimum Order Total] | Sitio web | La cantidad de pedido más pequeña que se puede pagar por cheque o giro postal. |
| [!UICONTROL Maximum Order Total] | Sitio web | La mayor cantidad de pedido que se puede pagar por cheque o giro postal. <br/><br/>**_Nota:_** Un pedido califica si el total está entre el total de pedido mínimo o máximo, o si coincide con él. |
| [!UICONTROL Sort Order] | Sitio web | Un número que determina el orden en que aparece el pago mediante cheque o giro postal cuando se enumera con otros métodos de pago durante el pago. Escriba `0` para colocarlo al principio de la lista. |

{style="table-layout:auto"}

### [!UICONTROL Bank Transfer Payment]

![Pago de transferencia bancaria](./assets/payment-methods-bank-transfer-payment.png)<!-- zoom -->

<!-- [Bank Transfer Payment](https://experienceleague.adobe.com/es/docs/commerce-admin/stores-sales/payments/offline/bank-transfer) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enabled] | Sitio web | Determina si los clientes pueden pagar transfiriendo el pago directamente desde su banco a su cuenta de comerciante. Opciones: `Yes` / `No` |
| [!UICONTROL Title] | Vista de tienda | El nombre de esta forma de pago que aparece a los clientes durante el cierre de compra. |
| [!UICONTROL New Order Status] | Sitio web | Determina el estado de pedido inicial asignado a pedidos pagados por transferencia bancaria. Valor predeterminado: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Sitio web | Determina los países desde los que se acepta el pago mediante transferencia bancaria. Opciones: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Sitio web | Identifica los países específicos desde los que se acepta el pago mediante transferencia bancaria. |
| [!UICONTROL Minimum Order Total] | Sitio web | El importe de pedido más pequeño que se puede pagar por transferencia bancaria. |
| [!UICONTROL Maximum Order Total] | Sitio web | La mayor cantidad de pedido que se puede pagar por transferencia bancaria. <br/><br/>**_Nota:_** Un pedido califica si el total está entre el total de pedido mínimo o máximo, o si coincide con él. |
| [!UICONTROL Sort Order] | Sitio web | Un número que determina el orden en que aparece el pago por transferencia bancaria cuando se enumera con otros métodos de pago durante el cierre de compra. Escriba `0` para colocarlo al principio de la lista. |

{style="table-layout:auto"}

### [!UICONTROL Payment on Account]

{{b2b-feature}}

![Pago en la cuenta](./assets/payment-methods-payment-on-account.png)<!-- zoom -->

<!-- [Payment on Account](https://experienceleague.adobe.com/es/docs/commerce-admin/b2b/enable-basic-features#configure-payment-on-account) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enabled] | Sitio web | Determina si las empresas pueden utilizar el crédito de la empresa para realizar compras. Opciones: `Yes` / `No` |
| [!UICONTROL Title] | Vista de tienda | El nombre de esta forma de pago que aparece a los clientes durante el cierre de compra. |
| [!UICONTROL New Order Status] | Sitio web | Determina el estado de los nuevos pedidos cargados a una cuenta de empresa. Opciones: `Pending (default)` / `Processing` / `Suspected Fraud` |
| [!UICONTROL Payment from Applicable Countries] | Sitio web | Determina los países en los que se permite a las compañías cargar compras en sus cuentas. Opciones: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Sitio web | Identifica los países específicos en los que las empresas pueden cargar compras a sus cuentas. |
| [!UICONTROL Minimum Order Total] | Sitio web | Especifica el importe de pedido más pequeño que se puede cargar a una cuenta de empresa. |
| [!UICONTROL Maximum Order Total] | Sitio web | El mayor importe de pedido que se puede cargar a una cuenta de empresa. <br/><br/>**_Nota:_** Un pedido califica si el total está entre el total de pedido mínimo o máximo, o si coincide con él. |
| [!UICONTROL Sort Order] | Sitio web | Un número que determina el orden en que aparece el pago a cuenta cuando se enumera con otros métodos de pago durante el cierre de compra. Escriba `0` para colocarlo al principio de la lista. |

{style="table-layout:auto"}

>[!NOTE]
>
>Pago a cuenta no es compatible con pedidos con [varias direcciones de envío](../../stores-purchase/shipping-settings.md#multiple-addresses) y no aparece entre las opciones de pago.

### [!UICONTROL Cash On Delivery Payment]

![Pago contra reembolso](./assets/payment-methods-cash-on-delivery-payment.png)<!-- zoom -->

<!-- [Cash On Delivery Payment](../../stores-purchase/cash-on-delivery.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enabled] | Sitio web | Determina si los clientes pueden pagar transfiriendo el pago directamente desde su banco a su cuenta de comerciante. Opciones: `Yes` / `No` |
| [!UICONTROL Title] | Vista de tienda | El nombre de esta forma de pago que aparece a los clientes durante el cierre de compra. |
| [!UICONTROL New Order Status] | Sitio web | Determina el estado de pedido inicial asignado a pedidos pagados por transferencia bancaria. Valor predeterminado: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Sitio web | Determina los países desde los que se acepta el pago mediante transferencia bancaria. Opciones: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Sitio web | Identifica los países específicos desde los que se acepta el pago mediante transferencia bancaria. |
| [!UICONTROL Minimum Order Total] | Sitio web | Especifica el importe de pedido más pequeño que se puede pagar mediante transferencia bancaria. |
| [!UICONTROL Maximum Order Total] | Sitio web | La mayor cantidad de pedido que se puede pagar por transferencia bancaria. <br/><br/>**_Nota:_** Un pedido califica si el total está entre el total de pedido mínimo o máximo, o si coincide con él. |
| [!UICONTROL Sort Order] | Sitio web | Un número que determina el orden en que aparece el pago por transferencia bancaria cuando se enumera con otros métodos de pago durante el cierre de compra. Escriba `0` para colocarlo al principio de la lista. |

{style="table-layout:auto"}

### [!UICONTROL Zero Subtotal Checkout]

![Cierre de compra con subtotal cero](./assets/payment-methods-zero-subtotal-checkout.png)<!-- zoom -->

<!-- [Zero Subtotal Checkout](../../stores-purchase/zero-subtotal-checkout.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Title] | Vista de tienda | El nombre que se usa para este método de pago durante el cierre de compra. Valor predeterminado: no se requiere información de pago |
| [!UICONTROL Enabled] | Sitio web | Determina si el administrador de la tienda puede gestionar pedidos que tienen un subtotal de cero, como uno que se ha gravado, pero un descuento ha reducido el importe a cero. Opciones: `Yes` / `No` |
| [!UICONTROL New Order Status] | Sitio web | Determina el estado de pedido inicial asignado a pedidos procesados como Cierre de Subtotal Cero. Valor predeterminado: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Sitio web | Determina los países desde los que se puede aplicar el cierre de compra de subtotal cero. Opciones: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Sitio web | Identifica los países específicos a los que se puede aplicar el cierre de compra con subtotal cero. |
| [!UICONTROL Sort Order] | Sitio web | Un número que determina el orden en el que aparece el título, como &quot;No se requiere información de pago&quot;, al ponerse en venta con otros métodos de pago durante el cierre de compra. Escriba `0` para colocarlo al principio de la lista. |

{style="table-layout:auto"}

## [!UICONTROL Payment actions]

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."}

Las acciones de pago están configuradas _por método de pago_. La acción de pago determina cuándo se capturan los fondos y cuándo se crean facturas para los pedidos de venta.

Consulte la sección Configuración básica de cada método de pago individual para obtener una lista completa de las opciones de configuración individuales.

| Acción de pago | Descripción |
|--- |---|
| [!UICONTROL Authorization] | Aprueba la compra, pero retiene los fondos. El importe no se retira hasta que el comerciante lo capture. |
| [!UICONTROL Authorize] | Autoriza la cuenta del comprador para el total del pedido, pero no registra el pago. Capture el pago creando una factura. Los pedidos autorizados se pueden anular o cancelar. |
| [!UICONTROL Authorize and Capture] | Autoriza la cuenta del comprador para el total del pedido y captura el pago. Se crea automáticamente una factura. Puede reembolsar los fondos capturados a través de la nota de crédito. No puede cancelar un pedido una vez registrado el pago. |
| [!UICONTROL Charge on shipment] | Amazon recibe una solicitud de captura y carga al cliente cuando se crea una factura en Commerce. |
| [!UICONTROL Charge on order] | Amazon crea la factura y carga al cliente cuando se realiza el pedido. |
| [!UICONTROL Not Capture] | Cuando se envía la factura, el sistema no registra el pago. Se da por hecho que el pago se registra más adelante a través de Commerce. Hay un botón Capturar en la factura completada. Antes de capturar, puede cancelar la factura. Después de la captura, puede crear una nota de abono y anular la factura. |
| [!UICONTROL Order] | Representa un acuerdo con PayPal que permite al comerciante capturar una o más cantidades hasta el total del pedido desde la cuenta de comprador del cliente, en un período de tiempo definido (hasta 29 días). |
| [!UICONTROL Sale] | El importe de la compra se autoriza y se retira inmediatamente de la cuenta del cliente. |

{style="table-layout:auto"}

>[!NOTE]
>
>No seleccione la opción _[!UICONTROL Not Capture]_&#x200B;a menos que esté seguro de que va a capturar el pago mediante Commerce más adelante. No puede crear una nota de abono hasta que el pago se haya capturado con el botón Capturar.

## [!UICONTROL Purchase Order]

![Pedido de compra](./assets/payment-methods-purchase-order.png)<!-- zoom -->

<!-- [Purchase Order](../../stores-purchase/purchase-order.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enabled] | Sitio web | Determina si los clientes pueden pagar por pedido de compra. Opciones: `Yes` / `No` |
| [!UICONTROL Title] | Vista de tienda | El nombre de esta forma de pago que aparece a los clientes durante el cierre de compra. |
| [!UICONTROL New Order Status] | Sitio web | Determina el [estado de pedido](../../stores-purchase/order-status.md) inicial asignado a pedidos pagados por PC. Valor predeterminado: Pendiente |
| [!UICONTROL Payment from Applicable Countries] | Sitio web | Determina los países desde los que se acepta el pago por OC. Opciones: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Sitio web | Identifica los países específicos desde los que acepta el pago por OC. |
| [!UICONTROL Minimum Order Total] | Sitio web | El importe de pedido más pequeño que se puede pagar por pedido. |
| [!UICONTROL Maximum Order Total] | Sitio web | El importe de pedido más grande que puede pagar la OC. <br/><br/>**_Nota:_** Un pedido califica si el total está entre el total de pedido mínimo o máximo, o si coincide con él. |
| [!UICONTROL Sort Order] | Sitio web | Número que determina el orden en el que aparece el pago por pedido cuando se enumera con otros métodos de pago durante el cierre de compra. Escriba `0` para colocarlo al principio de la lista. |

{style="table-layout:auto"}
