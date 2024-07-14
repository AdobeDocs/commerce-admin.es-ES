---
title: Pedidos de compra para empresas
description: Obtenga información sobre los flujos de trabajo de pedidos de compra que permiten a las empresas rastrear y controlar el gasto.
exl-id: 4f93ab4c-6bdf-495e-9183-3a18898b377f
feature: B2B, Purchase Orders
source-git-commit: 4b34645377102e890779059e57c61cf23f71f34c
workflow-type: tm+mt
source-wordcount: '924'
ht-degree: 0%

---

# Pedidos de compra para empresas

Las órdenes de compra (PO) son una forma común para que las compañías rastreen y controlen el gasto. [El pedido de compra](../stores-purchase/purchase-order.md) es uno de los métodos de pago sin conexión estándar admitidos en Adobe Commerce y Magento Open Source. Cuando se instala B2B de Adobe Commerce y se activa [_Habilitar pedidos de compra_](account-company-manage.md#advanced-settings) para una cuenta de compañía, todos los pedidos se crean automáticamente como pedidos de compra. Los usuarios de la compañía con los [permisos](account-company-roles-permissions.md) necesarios pueden crear, editar y eliminar PC que creen y PC creados por usuarios subordinados.

## Flujo de pedido de compra

Según su función y el orden, los usuarios de la empresa podrían estar sujetos a varias reglas de aprobación. Y dependiendo de si se utilizan métodos de pago en línea o sin conexión, el flujo es ligeramente diferente. Los administradores de la empresa pueden crear pedidos automáticamente, omitiendo las reglas de aprobación. Como almacenar los detalles de pago en línea durante el proceso de aprobación supone un riesgo para la seguridad, estos detalles se añaden después de la aprobación y, a continuación, la orden de compra se convierte en un pedido real.

![Flujo de pedido de compra](./assets/purchase-order-flow.png){width="600" zoomable="yes"}

>[!NOTE]
>
>No se puede realizar un pedido si uno o más productos del pedido de compra están desactivados o agotados.

El flujo de trabajo del pedido de compra de una empresa puede variar en varios aspectos:

- Si no se establecen reglas de aprobación, los pedidos de compra se pueden realizar y el pedido se completa directamente.

  >[!NOTE]
  >
  >De manera predeterminada, siempre se muestra un mensaje `Purchase order has been submitted for approval` a los usuarios de la compañía, incluso cuando no se hayan establecido reglas de aprobación. Cuando no se requiere ningún proceso de aprobación, los usuarios de la empresa reciben automáticamente un correo electrónico que les informa de que la solicitud se ha creado y aprobado.

- Si el administrador de la empresa define las reglas de aprobación, los usuarios pasan por el proceso de aprobación.
- Los detalles de pago sin conexión se introducen al crear el pedido de compra.
- Los detalles de pago en línea se introducen después de aprobar el pedido de compra.

>[!NOTE]
>
>Los pedidos de compra crean una _instantánea_ de los precios de los artículos, los descuentos y los precios de envío en el momento en que se creó el pedido. Si el precio de un artículo cambia después de crear el pedido, se utiliza el precio original.

### Ejemplo de flujo de trabajo básico

Las empresas utilizan órdenes de compra para controlar qué pueden comprar los empleados en nombre de la empresa y, a menudo, configuran reglas de aprobación para aplicar las directrices de la empresa. Según las reglas de aprobación, es posible que varias personas tengan que aprobar la solicitud.

1. El usuario crea un pedido de compra de bienes por un valor de 25 000 $.
1. Su jefe debe aprobarlo.
1. Debido a que la orden es de más de $10,000, el vicepresidente también debe aprobar.
1. Según la forma de pago, después de las aprobaciones, el pedido de compra se convierte en un pedido automáticamente o el usuario vuelve para introducir los detalles de pago.

### Reglas de aprobación

Las reglas de aprobación se utilizan para controlar el gasto en función de las directrices de la empresa. Estos son algunos ejemplos de reglas de aprobación:

- Cualquier pedido de más de $100 necesita la aprobación de su gerente.
- Cualquier pedido superior a $1000 necesita la aprobación de su gerente y del administrador de la empresa.
- Cualquier pedido con más de 30 SKU únicas necesita la aprobación del administrador de la empresa.

Con estas reglas implementadas para una compañía, un usuario de la compañía puede completar el pedido inmediatamente cuando este sea inferior a 100 dólares. Para conocer la definición de la regla de aprobación, consulte [Reglas de aprobación](account-dashboard-approval-rules.md)

### Tipos de usuarios de tiendas

El flujo de trabajo del pedido de compra también puede variar en función de quién realice la compra.

- Un empleado regular puede estar sujeto a todas las reglas de aprobación
- Un gerente podría tener más poder adquisitivo y tendría diferentes reglas de aprobación
- Los administradores de la empresa pueden omitir todas las reglas de aprobación y hacer que sus pedidos de compra se completen automáticamente.

Todos estos factores pueden influir en el proceso de pago y envío exacto.

## [!UICONTROL My Purchase Orders]

Cuando los pedidos de compra están habilitados para una empresa, el elemento **[!UICONTROL My Purchase Orders]** se muestra en el panel izquierdo para los clientes que iniciaron sesión en una cuenta de usuario de la empresa. Existen tres pestañas que proporcionan diferentes listas y funciones de pedidos:

- **[!UICONTROL My Purchase Orders]**: pedidos creados por el cliente.
- **[!UICONTROL Company Purchase Orders]**: pedidos realizados por usuarios subordinados dentro de la compañía (dependen de la estructura y las funciones de la compañía).
- **[!UICONTROL Requires My Approval]**: (visible para aprobadores designados) PC que están esperando la aprobación del cliente. El contador muestra cuántas solicitudes están a la espera de aprobación.

![Mis pedidos de compra](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

Para obtener más información acerca de las funciones de pedidos de compra compatibles disponibles para los usuarios de la compañía en la tienda, vea [Mis pedidos de compra](account-dashboard-my-purchase-orders.md).

## Métodos de pago sin conexión o en línea

Los flujos de trabajo pueden variar según la forma de pago. Para obtener más información acerca de los métodos de pago de Adobe Commerce, consulte [Métodos de pago](../stores-purchase/payments.md) en la _Guía de ventas y compras_.

>[!IMPORTANT]
>
>Los pedidos de compra deben usar una experiencia de cierre de compra _en contexto_. No se admiten desprotecciones de _Fuera de contexto_ porque omiten el flujo de desprotección normal. Por lo general, _en contexto_ significa que el cliente permanece en su sitio de comercio para completar el proceso. _Fuera de contexto_ es cuando el cliente es llevado a otro sitio para completar la compra.

### Pagos en línea

Por motivos de seguridad, las tiendas en línea no suelen querer recopilar los datos de la tarjeta de crédito de la tienda mientras esperan a que se complete el proceso de aprobación. Por lo tanto, si se selecciona una opción de pago en línea, el creador de la orden de compra vuelve a la tienda después de la aprobación, introduce los detalles del pago y completa la orden. Algunos ejemplos de pagos en línea son:

- Tarjetas de crédito/débito
- PayPal
- Braintree

>[!IMPORTANT]
>
>No se admite el uso de tarjetas de regalo, puntos de crédito de tienda o puntos de recompensa con métodos de pago en línea para pedidos de compra. Habilitar estas funciones con pagos en línea puede causar un comportamiento inesperado. Se recomienda desactivar las tarjetas de regalo, el crédito de la tienda y los puntos de recompensa cuando los pagos en línea estén habilitados para pedidos de compra.

### Pagos sin conexión

Como los métodos de pago fuera de línea, como una orden de pago, se gestionan fuera del sitio web, son más seguros. Los pedidos de compra con pagos sin conexión se pueden procesar automáticamente, después de cualquier proceso de aprobación.

Algunos ejemplos de pagos sin conexión son:

- Cheque/giro postal
- Pago a cuenta
- Pago contra reembolso
- Transferencias bancarias
- Crédito de tienda
