---
title: Compra y canje con tarjeta regalo
description: Obtenga información acerca del ciclo de vida de compra a canje de tarjetas de regalo cuando incluya tarjetas de regalo en el catálogo de la tienda.
exl-id: ecaa39aa-f504-4bfd-874b-12b44093c2a9
feature: Products, Gift
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 0%

---

# Compra y canje con tarjeta regalo

{{ee-feature}}

Las tarjetas de regalo se canjean en el carro de compras de forma similar a la forma en que se aplica un cupón a un pedido. Durante el proceso de pago y envío, el comprador introduce el código de la tarjeta regalo para aplicar un importe de la tarjeta regalo a la compra. Los titulares de tarjetas de regalo que tengan cuentas de cliente pueden comprobar el estado y el saldo restante desde su panel de cuentas. Las tarjetas de regalo individuales y múltiples se pueden usar para pagar la totalidad o parte de un pedido.

El código de tarjeta regalo aplicado se puede ver abriendo el pedido en el _Administrador_, lo que le permite recuperar el código para colocarlo en una tarjeta de regalo física, si es necesario. Si se cancela o reembolsa un pedido con tarjeta regalo, debe cancelar manualmente la cuenta con tarjeta regalo asociada. Puede eliminar la cuenta por completo o desactivarla.

![Detalles de la tarjeta de regalo en el carro](./assets/storefront-gift-card-order-customer-account.png){width="700" zoomable="yes"}

Por ejemplo, un cliente que compra en la tienda de Luma de demostración puede comprar una tarjeta de regalo virtual o física.

**Tarjeta regalo virtual** : Se envía por correo electrónico una tarjeta regalo virtual de Luma con un mensaje opcional al destinatario. Se puede canjear en cualquiera de los sitios web de la familia Luma y nunca caduca.

**Tarjeta de regalo física** - Una tarjeta regalo de Luma se empaqueta en un correo de arte personalizado y se envía sin cargo al destinatario. Se puede producir por adelantado, etiquetar con códigos únicos y canjear en la tienda, por teléfono o en cualquiera de los sitios web de la familia de Luma. Nunca caduca.

**Tarjeta regalo combinada** - Una tarjeta de regalo combinada tiene las características de una tarjeta de regalo virtual y física. Se envía una tarjeta regalo combinada de Luma y se envía por correo electrónico al destinatario. El correo electrónico y la dirección de envío son obligatorios durante la compra de la tarjeta regalo. Nunca caduca.

## Ciclo de tarjeta regalo

1. **El cliente determina el valor de la tarjeta regalo**.

   El cliente determina el valor de la tarjeta regalo de la página del producto. Según la configuración, hay un campo de precio fijo, una lista de opciones de precio o ambos. Todos los importes aparecen en la divisa utilizada en el almacén.

1. **El cliente completa la información de la tarjeta regalo**.

   Para una tarjeta regalo física, el cliente introduce la **Nombre del remitente** y **Nombre del destinatario**. En el caso de las tarjetas regalo virtuales o combinadas, el cliente también introduce el **Correo electrónico del remitente** y **Correo electrónico del destinatario**. Si el cliente ha iniciado sesión, el nombre del remitente (y el correo electrónico del remitente, si corresponde) se introducen automáticamente desde su cuenta. Según la configuración, el cliente también puede introducir un mensaje al destinatario.

1. **El cliente finaliza el cierre de compra**.

   La tarjeta regalo aparece como un elemento de línea en el carro de compras con detalles que muestran el nombre del remitente, el destinatario y el mensaje, si corresponde. La cantidad asociada con la tarjeta regalo se convierte a la moneda base de la tienda cuando se agrega al carro de compras.

1. **El cliente recibe la confirmación del pedido**.

   El comprador de tarjetas regalo puede hacer clic en el vínculo de la confirmación para rastrear el pedido desde su panel de cuentas.

1. **El destinatario recibe la tarjeta regalo**.

   En el caso de las tarjetas regalo virtuales o combinadas, el destinatario recibe un correo electrónico con el código de la tarjeta regalo, el nombre del remitente y el mensaje, si corresponde. Si se compran varias tarjetas regalo en un único pedido y el tipo es virtual o combinado, todos los códigos de tarjetas regalo correspondientes se envían al destinatario en un único correo electrónico. Las tarjetas de regalo físicas se pueden enviar directamente al destinatario o al cliente, que luego puede entregar personalmente la tarjeta de regalo al destinatario.

1. **El destinatario aplica una tarjeta regalo a la compra**.

   El destinatario compra un artículo en su tienda y aplica el código de la tarjeta regalo durante el cierre de compra. Cada vez que se aplica una tarjeta regalo durante el cierre de compra, la cantidad aparece en el bloque de totales del pedido y se resta del total general. El saldo completo de cada tarjeta de regalo se resta del total del carro de compras. Si se utilizan varias tarjetas regalo para una compra, se aplican en orden ascendente, empezando por la tarjeta con el saldo restante más pequeño, hasta que se apliquen todas las tarjetas o el total general sea cero. Cuando el total general llega a cero, la última cuenta de tarjeta de regalo aplicada al carro de compras recibe una deducción parcial. Las tarjetas que no se hayan aplicado al carro de compras no reciben una deducción por saldo. Las cantidades se deducen de las cuentas de tarjetas de regalo solo después de realizar el pedido.

## Experiencia en tienda

Cómo funcionan las tarjetas de regalo en la tienda:

- El código de la tarjeta regalo se puede aplicar en el carrito o en el pago para cubrir la cantidad total del pedido.

- En el catálogo, se presenta una tarjeta regalo como un tipo de producto independiente.

- El código de la tarjeta regalo se activa después de que se factura el pedido. Si el pedido no se paga, el cliente receptor no puede utilizar la tarjeta regalo.

- Las cuentas para códigos de regalo se crean para realizar un seguimiento del saldo de un cupón específico. Un administrador de tienda puede ajustar manualmente el saldo.

El cliente receptor puede utilizar el _[!UICONTROL Gift Card]_de su tablero de cuentas para comprobar el saldo de sus cuentas [cuenta de tarjeta regalo](product-gift-card-accounts.md) y canjear tarjetas regalo por [crédito de tienda](../customers/store-credit-using.md).

![Tarjeta regalo](./assets/account-dashboard-gift-card.png){width="700" zoomable="yes"}

### Comprobar el estado y el saldo de la tarjeta regalo

1. Desde la tienda, el cliente inicia sesión y abre la página de su cuenta de cliente.

1. El cliente abre el **[!UICONTROL Gift Card]** e introduce el código de la tarjeta regalo.

1. El cliente hace clic en **[!UICONTROL Check status and balance]**.

![Saldo de tarjeta regalo](./assets/gift-balance.png){width="700" zoomable="yes"}

Se muestra el saldo de la tarjeta regalo.

### Activación de tarjeta regalo

1. En el _[!UICONTROL Gift Card]_página, el cliente introduce el código de la tarjeta regalo.

1. El cliente hace clic en **[!UICONTROL Redeem Gift Card]**.

![Mensaje sobre la activación correcta de la tarjeta regalo](./assets/gift-redeemed-balance.png){width="700" zoomable="yes"}

El importe de la tarjeta regalo se activa y se añade al saldo de crédito total de la tienda.

![Saldo de crédito de tienda](./assets/store-credit.png){width="700" zoomable="yes"}

Todas las operaciones para el saldo de la tarjeta regalo están disponibles en la _[!UICONTROL Store Credit]_página.

### Aplicar una tarjeta regalo durante el cierre de compra

Si la tarjeta regalo no se puede canjear, un cliente puede aplicar el código de la tarjeta regalo durante el pago.

1. Durante el _Revisión y pagos_ paso, el cliente hace clic en **[!UICONTROL Apply Gift Card]**.

1. Introduce el código de la tarjeta regalo y luego hace clic en **[!UICONTROL Apply]**.

   El descuento debe reflejarse en la variable _[!UICONTROL Order Summary]_.

1. Clics **[!UICONTROL Place Order]** para finalizar el pedido.
