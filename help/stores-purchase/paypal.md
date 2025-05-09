---
title: Soluciones de pago PayPal
description: Obtenga información sobre las integraciones de la solución de pago PayPal disponibles para su tienda.
exl-id: d447b98e-d30c-4759-9ae0-94ccbeed9ba4
feature: Payments
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '1247'
ht-degree: 0%

---

# Soluciones de pago PayPal

PayPal es líder mundial en pagos en línea y una forma rápida y segura de que sus clientes paguen en línea. La selección de soluciones de PayPal disponibles varía según la ubicación del comerciante. PayPal Express Checkout y PayPal Payments Standard se pueden utilizar en cualquier parte del mundo. Para obtener más información, consulta [Soluciones de PayPal por país](#paypal-solutions-by-country).

>[!IMPORTANT]
>
>**Requisitos de PSD2:** <br/>
>A partir del 14 de septiembre de 2019, los bancos europeos podrán rechazar los pagos que no cumplan los requisitos de [PSD2](../getting-started/compliance-payment-services-directive.md). Para la mayoría de las soluciones de PayPal, no es necesario realizar ninguna acción para cumplir con PSD2 porque estos requisitos los gestiona PayPal.

## Cuenta comercial de PayPal

Para ofrecer PayPal como forma de pago en tu tienda, debes tener una [cuenta comercial][1] de PayPal y/o una [cuenta PayPal Payflow][2]. Los requisitos de la cuenta se especifican en la descripción de cada solución de PayPal. Tu cuenta de PayPal también se usa para administrar los [filtros de fraude](#paypal-fraud-management-filters) que se apliquen a las compras realizadas en tu tienda.

Los clientes que utilizan Pago y envío exprés de PayPal o Pago exprés de Payflow Pro deben tener una cuenta de comprador de PayPal. PayPal Payments Standard (Estándar de pagos en sitios web en algunos países) se puede usar directamente o a través de una cuenta de comprador cuando el comerciante habilite _Cuenta PayPal opcional_. De forma predeterminada, este parámetro está habilitado para que los clientes puedan especificar la información de su tarjeta de crédito o crear una cuenta de comprador con PayPal. Si se desactiva, los clientes deben crear primero una cuenta de comprador de PayPal antes de realizar una compra.

Los pagos de sitio web Pro, los pagos de sitio web Pro Payflow Edition, Payflow Pro Gateway y Payflow Link requieren que los clientes introduzcan la información de la tarjeta de crédito durante el pago.

## Crédito de PayPal y PayAfter

PayPal PayAfter ofrece a tus clientes un acceso rápido a la financiación, para que puedan comprar ahora y pagar con el tiempo, sin coste adicional para ti. No se te cobrará cuando los clientes elijan las opciones de crédito de PayPal y pagues solo la tarifa normal de transacción de PayPal. Para obtener más información, visita el [sitio web de PayPal][3].

Dale un impulso a tus ventas cuando anuncies financiamiento. PayPal ayuda a convertir los navegadores en compradores con financiación mediante PayPal Paylater. Sus clientes pueden pagar con el tiempo, mientras que usted recibe el pago por adelantado, sin costo adicional para usted. Utiliza los anuncios de banner gratuitos de PayPal para anunciar la financiación de PayPal como una opción de pago cuando tus clientes cierren la compra con PayPal. Se ha demostrado que el programa PayPal Advertising genera compras adicionales y aumenta el tamaño promedio de las compras en un 15 % o más.

Puedes añadir fácilmente anuncios de banner gratuitos y listos para usar a las páginas de tu sitio y el botón _Crédito PayPal_ al carro de compras durante el cierre de compra para recordar a tus clientes que la financiación está disponible.

>[!NOTE]
>
>A partir de la versión 2.4.3, PayPal PayAfter es compatible con las implementaciones que incluyen PayPal. Esta función permite a los compradores pagar un pedido en cuotas quincenales en lugar de pagar el importe completo en el momento de la compra. La experiencia de crédito de PayPal está en desuso.

Para los comerciantes estadounidenses, el crédito de PayPal está habilitado de manera predeterminada para la opción de pago [Pago y envío exprés de PayPal](paypal-express-checkout.md). Para deshabilitarlo para esta forma de pago, consulta la sección _Características_ de la [configuración del Pago y envío de PayPal Express](paypal-express-checkout.md#features).

El crédito de PayPal está desactivado de forma predeterminada para las otras soluciones de pago de PayPal, pero se puede activar en la configuración del método de pago para las soluciones de soporte:

- [Pagos avanzados](paypal-payments-advanced.md)
- [Payments Pro](paypal-payments-pro.md)
- [Estándar de pagos](paypal-payments-standard.md)
- [Payflow Pro](paypal-payflow-pro.md)
- [Vínculo de flujo de pago](paypal-payflow-link.md)

>[!IMPORTANT]
>
>Antes de configurar el crédito de PayPal o PayPal Paylater para tu tienda, asegúrate de que esté activado en tu cuenta comercial de PayPal.

## Soluciones PayPal integradas

Con PayPal y Adobe Commerce, puedes aceptar pagos de todas las principales tarjetas de débito y crédito. PayPal ofrece comodidad adicional sin esfuerzo adicional, ya que incluso los clientes que no tienen una cuenta PayPal pueden pagar sus compras con PayPal.

>[!NOTE]
>
>No puedes tener más de un método PayPal habilitado en tu tienda a la vez, excepto Pago y envío con PayPal Express. PayPal Express Checkout se puede utilizar con otros métodos de pago de PayPal, excepto con PayPal Payments Standard. Si cambia las soluciones de pago, se desactiva el método anterior.

### Pago y envío con PayPal Express

[Pago y envío con PayPal Express](paypal-express-checkout.md)

### PayPal Soluciones de pago todo en uno

En Estados Unidos, PayPal ofrece las siguientes soluciones compatibles con PCI para satisfacer las necesidades de su empresa en expansión.

- [Pagos mediante PayPal avanzados](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal Payments Standard](paypal-payments-standard.md)

![Soluciones de pago todo en uno PayPal](./assets/paypal-all-in-one.png){width="600" zoomable="yes"}

### Puertas de pago PayPal

Una pasarela de pago es un servicio comercial proporcionado por un proveedor de servicios de aplicaciones de comercio electrónico que autoriza el procesamiento de tarjetas de crédito o pagos directos. Funcionan como intermediarios entre clientes y bancos.

Las puertas de enlace de pago están disponibles en entornos en línea y sin conexión. Los pagos se pueden aceptar por teléfono, en línea o a través de una aplicación móvil. La transacción se envía al sistema de procesamiento del proveedor de servicios y, a continuación, se envía al banco del cliente para su verificación y confirmación. Si se verifica, el comerciante recibe el pago sin tener contacto directo con la cuenta bancaria del cliente.

Existen dos tipos de puertas de enlace de pago: directas y alojadas.

- Las puertas de enlace de pago directo permiten a los usuarios introducir los datos de su tarjeta en el sitio web de la tienda.
- Las puertas de enlace de pago alojadas redirigen a los usuarios a una página de pago alojada fuera del sitio web de la tienda.

La pasarela de pago proporciona seguridad y protección a todas las partes involucradas en una transacción.

PayPal ofrece una opción de dos soluciones de pasarela de pago para tu negocio. Puedes dejar que PayPal aloje tu pago en su sitio de pago seguro, o puedes tomar el control de toda la experiencia de pago con una solución personalizable.

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [Vínculo de flujo de pago PayPal](paypal-payflow-link.md)

![Configurar puertas de enlace de pago de PayPal](./assets/paypal-payment-gateway.png){width="600" zoomable="yes"}

## Filtros de administración de fraude de PayPal

Los filtros de gestión de fraude de PayPal facilitan la detección y la respuesta a transacciones fraudulentas y pueden configurarse para marcar, retener para su revisión o denegar pagos más peligrosos. Las acciones relacionadas con los valores de Commerce [estado del pedido](order-status.md) cambiaron según la configuración del filtro de fraude:

| Acción | Resultado |
| --- | --- |
| [!UICONTROL Review] | El pedido sospechoso recibe el estado _Revisión de pago_ cuando se realiza el pedido. Puedes revisar el pedido y aprobarlo, o cancelar el pago en el Administrador o en PayPal. Al hacer clic en **[!UICONTROL Accept Payment]** o **[!UICONTROL Deny Payment]**, no se crean nuevas transacciones para el pedido. <br/><br/>Si cambias el estado de la transacción en el sitio PayPal, debes hacer clic en **[!UICONTROL Get Payment Update]** en la página de pedidos del administrador para aplicar los cambios. Si hace clic en **[!UICONTROL Accept Payment]** o **[!UICONTROL Deny Payment]**, se aplicarán los cambios realizados en el sitio PayPal. |
| [!UICONTROL Deny] | El cliente no puede realizar el pedido sospechoso porque PayPal rechaza la transacción correspondiente. <br/><br/>Para rechazar el pago del administrador, haga clic en **[!UICONTROL Deny Payment]** en la esquina superior derecha de la página. El estado del pedido cambia a `Canceled`, la transacción se revierte y los fondos se liberan en la cuenta del cliente. La información correspondiente se agrega en la sección _[!UICONTROL Comments History]_de la vista de pedidos. |
| [!UICONTROL Flag] | El pedido sospechoso obtiene el estado `Processing` cuando se realiza. La transacción correspondiente se marca con un indicador en la lista de transacciones de cuentas de comerciante. |

{style="table-layout:auto"}

## Soluciones PayPal por país

| País | Solución de pago PayPal |
|--- |--- |
| Australia | [!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Pro Hosted Solution]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Canadá | [!DNL PayPal Website Payments Standard]<br/>[!DNL PayPal Website Payments Pro]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) (incluye cierre de compra exprés)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Francia | [!DNL PayPal Integral Evolution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Alemania | [[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| RAE de Hong Kong | [!DNL PayPal Website Payments Pro Hosted Solution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Italia | [!DNL PayPal ProPay]<br/>[[!DNL Pal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Japón | [!DNL PayPal Website Payments Plus]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Nueva Zelanda | [[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| España | [!DNL PayPal Pasarela Integral]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Reino Unido | [!DNL PayPal Payments Pro Hosted Solution] (incluye cierre de compra exprés)<br/>[[!DNL PayPal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Estados Unidos | [[!DNL PayPal Payments Advanced]](paypal-payments-advanced.md) (incluye Pago y envío exprés)<br/>[[!DNL PayPal Payments Pro]](paypal-payments-pro.md) (incluye Pago y envío exprés)<br/>[[!DNL PayPal Payments Standard+]](paypal-payments-standard.md)<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md) (incluye Pago y envío exprés)<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) (incluye Pago y envío exprés)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |

{style="table-layout:auto"}

### Otros países

PayPal Express Checkout y PayPal Website Payments Standard están disponibles en los siguientes países:

- Argentina
- Austria
- Bélgica
- Brasil
- Bulgaria
- Chile
- Costa Rica
- Chipre
- República Checa
- Dinamarca
- República Dominicana
- Ecuador
- Estonia
- Finlandia
- Guayana Francesa
- Gibraltar
- Grecia
- Guadalupe
- Hungría
- Islandia
- India
- Indonesia
- Irlanda
- Israel
- Jamaica
- Letonia
- Liechtenstein
- Lituania
- Luxemburgo
- Malasia
- Malta
- Martinica
- México
- Países Bajos
- Noruega
- Filipinas
- Polonia
- Portugal
- Reunión
- Rumanía
- San Marino
- Singapur
- Eslovaquia
- Eslovenia
- Sudáfrica
- Corea del Sur
- Suecia
- Suiza
- Taiwán
- Tailandia
- Turquía
- Emiratos Árabes Unidos
- Uruguay
- Venezuela
- Vietnam


[1]: https://manager.paypal.com/
[2]: https://developer.paypal.com/docs/payflow/payflow-gateway/
[3]: https://www.paypal.com/us/business/buy-now-pay-later
