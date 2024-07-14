---
title: Estado del pedido
description: Obtenga información sobre los estados de pedidos predefinidos y cómo definir estados de pedidos personalizados para adaptarlos a sus necesidades operativas.
exl-id: d1153558-a721-4643-a70c-7fc20072983c
feature: Orders
source-git-commit: c2d5e9b41a76ba58d1343a8b3ee5122104d5bfe0
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# Estado del pedido

Todos los pedidos tienen un estado de pedido asociado a una fase del procesamiento de pedidos [workflow](order-processing.md).\
La diferencia entre los estados de pedidos y los estados de pedidos es que **[!UICONTROL order states]** se usan mediante programación. No lo son
visible para los clientes o los usuarios administradores. Determinan el flujo de una solicitud y qué operaciones son posibles para una
orden en un estado determinado.\
**[!UICONTROL Order statuses]** se utilizan para comunicar el estado de un pedido a clientes y usuarios administradores.
Puede crear estados de pedidos adicionales para adaptarlos a sus necesidades operativas. Los estados de pedidos son fáciles de mostrar
progreso fuera de Adobe Commerce, por ejemplo, progreso de picking y entrega de pedidos. No afectan al pedido
flujo de trabajo de procesamiento\
Cada estado de pedido está asociado a un estado de pedido. Su tienda tiene un conjunto de estados de pedidos predefinidos y
configuración del estado del pedido.

![Estados y estados de pedidos](./assets/order-states-and-statuses.png){width="700" zoomable="yes"}

El estado de cada pedido se muestra en la columna _Estado_ de la cuadrícula _Pedidos_.

![Estado del pedido](./assets/stores-order-status-column.png){width="700" zoomable="yes"}

>[!TIP]
>
>Un pedido reembolsado parcialmente permanece en estado `Processing` hasta que se envíen **_todos_** los artículos pedidos (incluidos los artículos reembolsados). El estado del pedido no cambia a `Complete` hasta que se han enviado todos los artículos del pedido.

## Flujo de trabajo de estado de pedidos

![Flujo de trabajo de estado del pedido](./assets/order-state-workflow.png)

## Estado predefinido

| Estado del pedido | Código de estado |                                                                                                                                                                                                                                                                                        |
|--------------------------|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Recibido | `received` | Este estado es el estado inicial de los pedidos que se realizan cuando se activa la colocación asincrónica de pedidos. |
| Sospecha de fraude | `fraud` | A veces, los pedidos pagados a través de PayPal u otra puerta de pago se marcan como _Sospecha de fraude_. Este estado significa que el pedido no tiene una factura emitida y que el correo electrónico de confirmación tampoco se envía. |
| Procesamiento | `processing` | Cuando el estado de los nuevos pedidos se establece en &#39;Procesando&#39;, la opción _Facturar automáticamente todos los artículos_ está disponible en la configuración. Las facturas no se crean automáticamente para los pedidos realizados mediante tarjeta de regalo, crédito de tienda, puntos de recompensa u otros métodos de pago sin conexión. |
| Pendiente de pago | `pending_payment` | Este estado se utiliza si se crea el pedido y se utiliza PayPal o una forma de pago similar. Significa que el cliente fue dirigido al sitio web de la pasarela de pago, pero aún no se ha recibido información de devolución. Este estado cambia cuando el cliente paga. |
| Revisión de pago | `payment_review` | Este estado aparece cuando se activa la revisión de pagos de PayPal. |
| Pendiente | `pending` | Este estado indica que no se han enviado facturas ni envíos. |
| En espera | `holded` | Este estado solo se puede asignar manualmente. Puedes poner cualquier orden en espera. |
| Completar | `complete` | Este estado significa que el pedido se crea, se paga y se envía al cliente. |
| Cerrado | `closed` | Este estado indica que a un pedido se le asignó una nota de abono y que el cliente ha recibido un reembolso. |
| Cancelado | `canceled` | Este estado se asigna manualmente en el Administrador o, en el caso de algunas puertas de enlace de pago, cuando el cliente no paga en el plazo especificado. |
| Rechazado | `rejected` | Este estado significa que se rechazó una solicitud durante el procesamiento asincrónico de pedidos. Esto sucede cuando se produce un error durante la colocación asincrónica de un pedido. |
| Reversión cancelada de PayPal | `paypay_canceled_reversal` | Este estado significa que PayPal ha cancelado la reversión. |
| PayPal pendiente | `pending_paypal` | Este estado significa que el pedido se recibió en PayPal, pero el pago aún no se ha procesado. |
| PayPal revertido | `paypal_reversed` | Este estado significa que PayPal ha revertido la transacción. |

{style="table-layout:auto"}

## Estado de pedido personalizado

Además de la configuración preestablecida de estado de pedidos, puede crear su propia configuración de estado de pedidos personalizada, asignarla a estados de pedidos y establecer estados de pedidos predeterminados para los estados de pedidos. El estado del pedido indica la posición del pedido dentro del flujo de trabajo de procesamiento del pedido y el estado del pedido asigna una etiqueta traducible significativa a la posición del pedido. Por ejemplo, es posible que necesite un estado de pedido personalizado como `packaging"`, `backordered` o un estado que sea específico de sus necesidades. Puede crear un nombre descriptivo para el estado personalizado y asignarlo al estado de pedido asociado en el flujo de trabajo.

>[!NOTE]
>
>En el flujo de trabajo de pedidos solo se utilizan los valores de estado de pedidos personalizados predeterminados. Los valores de estado personalizados que no están configurados como predeterminados solo se pueden utilizar en la sección de comentarios del pedido.

![Configuración del estado del pedido](./assets/order-status.png){width="700" zoomable="yes"}

### Creación de un estado de pedido personalizado

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Order Status]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Create New Status]**.

   ![Crear nuevo estado de pedido](./assets/order-status-new.png){width="600" zoomable="yes"}

1. Actualice la sección _[!UICONTROL Order Status Information]_:

   - Escriba un(a) **[!UICONTROL Status Code]** como referencia interna. El primer carácter debe ser una letra (a-z) y el resto puede ser cualquier combinación de letras y números (0-9). Utilice el carácter de guion bajo en lugar de un espacio.

   - Para **[!UICONTROL Status Label]**, escriba una etiqueta que identifique la configuración de estado tanto en el administrador como en la tienda.

1. En la sección _[!UICONTROL Store View Specific Labels]_, escriba las etiquetas que sean necesarias para las distintas vistas de la tienda.

1. Haga clic en **[!UICONTROL Save Status]**.

### Asignación de un estado de pedido a un estado

1. En la página _Estado del pedido_, haga clic en **[!UICONTROL Assign Status to State]**.

   ![Asignar estado](./assets/store-status-assign-status.png){width="600" zoomable="yes"}

1. Actualice la sección **[!UICONTROL Assignment Information]**, haga lo siguiente:

   - Elija el(la) **[!UICONTROL Order Status]** que desea asignar. Se muestran por etiqueta de estado.

   - Establezca **[!UICONTROL Order State]** en el lugar del flujo de trabajo al que pertenece el estado del pedido.

     >[!NOTE]
     >
     >La lista **_[!UICONTROL Order State]_** incluye los estados de pedidos asignados predeterminados. Por ejemplo, se muestra el estado de pedido predeterminado `Pending` en lugar del valor de estado de pedido `New`.

   - Para hacer que este estado sea el predeterminado para el estado del pedido, active la casilla de verificación **[!UICONTROL Use Order Status as Default]**.

     >[!NOTE]
     >
     >En el flujo de trabajo de pedidos solo se utilizan los estados de pedidos predeterminados. Los estados no predeterminados solo se pueden establecer en la sección **[!UICONTROL Order Comments]** del Administrador.

   - Para que este estado sea visible desde la tienda, seleccione la casilla de verificación **[!UICONTROL Visible On Storefront]**.

   ![Asignar estado al estado](./assets/order-status-assign-state.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save Status Assignment]**.

### Editar un estado de pedido existente

1. En la cuadrícula _[!UICONTROL Order Status]_, abra el registro de estado en modo de edición.

1. Actualice la configuración de estado según sea necesario.

1. Haga clic en **[!UICONTROL Save Status]**.

### Eliminación de un estado de pedido de un estado asignado

>[!NOTE]
>
>No se puede quitar la asignación de un estado a una configuración de estado si el estado está en uso.

1. En la cuadrícula _[!UICONTROL Order Status]_, busque el registro de estado del pedido que se va a anular.

1. En la columna _[!UICONTROL Action]_del extremo derecho de la fila, haga clic en el vínculo **[!UICONTROL Unassign]**.

   Aparece un mensaje en la parte superior del espacio de trabajo que indica que se ha anulado la asignación del estado del pedido. Aunque la etiqueta de estado del pedido sigue apareciendo en la lista, ya no está asignada a ningún estado. No se puede eliminar la configuración de estado del pedido.

>[!NOTE]
>
>Si el estado de pedido predeterminado es sin asignar del estado de pedido, _**otro**_ estado de pedido es _**establecido automáticamente**_ como predeterminado para este estado de pedido.

## Notificación

Los clientes pueden hacer un seguimiento del estado de sus pedidos por [fuente RSS](../merchandising-promotions/social-rss.md) si la fuente RSS de pedidos está habilitada en la configuración. Cuando se habilita, aparece un vínculo a la fuente RSS en cada pedido.

### Activar notificación de estado del pedido

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL RSS Feeds]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Order]**.

1. Establezca **[!UICONTROL Customer Order Status Notification]** en `Enable`.

   ![Notificación de estado de pedido de cliente](../configuration-reference/catalog/assets/rss-feeds-order.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

### Configurar nuevas notificaciones de correo electrónico de pedidos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Sales Emails]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Order]**.

   ![Configuración - Opciones de pedido](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL New Order Confirmation Email Sender]** en una de las siguientes opciones:

   - `General Contact`
   - `Sales Representative`
   - `Customer Support`
   - `Custom Email 1`
   - `Custom Email 2`

1. Elija las plantillas que desea utilizar para cada tipo de cliente:

   - **[!UICONTROL New Order Confirmation Template]**: elija una plantilla para usarla con los clientes que tengan una cuenta de tienda registrada.
   - **[!UICONTROL New Order Confirmation Template for Guest]**: elija una plantilla para usarla con los clientes invitados que no tengan una cuenta de tienda registrada.

1. Para notificar el nuevo pedido a otra persona (como un administrador de empresa), escriba la dirección de correo electrónico **[!UICONTROL Send Order Email Copy To]**.

   Puede añadir varias direcciones de correo electrónico si se necesita más de un destinatario.

1. Establezca **[!UICONTROL Send Order Email Copy Method]** en una de las siguientes opciones:

   - `Bcc`: solo se envía un correo electrónico sobre el nuevo pedido al cliente y al destinatario adicional, pero el cliente no ve que el correo electrónico que recibió también se envió al destinatario adicional.
   - `Separate Email`: se envían dos correos electrónicos independientes: uno al destinatario y otro al cliente.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
