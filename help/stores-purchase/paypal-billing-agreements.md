---
title: Acuerdos de facturación de PayPal
description: Aprende cómo puedes respaldar los acuerdos de facturación de PayPal y un método de pago dentro de tu tienda.
exl-id: b0800b41-816a-4c48-a54d-41ddc1d586ce
feature: Payments
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 0%

---

# Acuerdos de facturación de PayPal

Para simplificar el proceso de pago y envío, los clientes pueden firmar un acuerdo de facturación con PayPal como proveedor de servicios de pago. Durante el proceso de pago, el cliente elige el acuerdo de facturación como forma de pago. El sistema de pago verifica el acuerdo de facturación por su número único y carga la cuenta del cliente. Cuando se establece un acuerdo de facturación, ya no es necesario que el cliente introduzca la información de pago de cada compra. Los clientes pueden administrar sus contratos de facturación desde el panel de su cuenta de cliente, donde el estado de cada uno de ellos se muestra como _Activo_ o _Cancelado_. Cuando se cancela un acuerdo de facturación, no se puede reactivar.

## Flujo de trabajo del acuerdo de facturación

1. **El cliente se suscribe a un contrato de facturación**. Una vez establecido un acuerdo de facturación, los acuerdos de facturación adicionales solo se pueden agregar desde la cuenta del cliente. No hay límite en el número de acuerdos de facturación que puede crear un cliente. Los clientes pueden utilizar cualquiera de los siguientes métodos para suscribirse a contratos de facturación:

   - **Registrarse en la cuenta de cliente**: los clientes pueden suscribirse a un acuerdo de facturación desde sus cuentas de cliente.
   - **Registrarse al finalizar la compra** - Los clientes que paguen una compra con Pago y envío de PayPal Express pueden marcar una casilla de verificación para crear un acuerdo de facturación. Aunque el acuerdo de facturación no se utiliza para el pedido actual, estará disponible como opción de método de pago la próxima vez que el cliente realice un pedido.
   - **Registrarse por el administrador de la tienda**: a petición del cliente, el administrador de la tienda puede crear un pedido de ventas utilizando el acuerdo de facturación del cliente.

1. **PayPal verifica y registra el acuerdo**. Cuando el cliente realiza el pedido con pago por acuerdo de facturación, el ID de referencia del acuerdo de facturación y los detalles del pago del pedido de venta se transfieren a PayPal y se registran en la cuenta del cliente, junto con la información de referencia. Si el pago está autorizado, se crea un pedido en Commerce. El ID de referencia del acuerdo de facturación se envía al cliente y a la tienda.

## Administrar acuerdos de facturación

La página _[!UICONTROL Billing Agreements]_&#x200B;enumera todos los contratos de facturación entre su tienda y sus clientes. Los comerciantes pueden filtrar los registros según la información del acuerdo de facturación o del cliente, incluidos el ID de referencia del acuerdo de facturación, el estado y la fecha de creación. Cada registro incluye información general sobre el acuerdo de facturación y todos los pedidos de venta que lo han utilizado como método de pago. Puede consultar, cancelar o suprimir acuerdos de facturación de clientes. Solamente el administrador de la tienda puede eliminar un acuerdo de facturación cancelado.

### Ver un acuerdo de facturación

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Billing Agreements]**.

1. Busque el acuerdo de facturación en la lista y haga clic en para abrirlo.

Cada página de acuerdo de facturación consta de dos fichas: _[!UICONTROL General Information]_&#x200B;y&#x200B;_[!UICONTROL Related Orders]_.

#### Información general

Esta pestaña incluye la información general sobre el acuerdo de facturación:

- [!UICONTROL Reference ID]: identificador numérico único asignado al contrato de facturación actual.
- [!UICONTROL Customer]: cuenta del cliente asignada al contrato de facturación actual.
- [!UICONTROL Status]: estado del acuerdo de pago.
- [!UICONTROL Created At]: fecha de creación.
- [!UICONTROL Updated At]: fecha de actualización.

![Vista del contrato de facturación](./assets/billing-agreement-view.png){width="600" zoomable="yes"}

#### Pedidos relacionados

Esta pestaña muestra la lista de los pedidos realizados con el acuerdo de facturación actual.

![Vista del contrato de facturación](./assets/billing-agreement-related-orders.png){width="600" zoomable="yes"}

### Cancelar un acuerdo de facturación

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Billing Agreements]**.

1. Busque el acuerdo de facturación en la lista y haga clic en para abrirlo.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Cancel]**.

1. Para confirmar la acción, haga clic en **[!UICONTROL OK]**.

### Eliminar un acuerdo de facturación

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Billing Agreements]**.

1. Busque el acuerdo de facturación en la lista y haga clic en para abrirlo.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Delete]**.

1. Para confirmar la acción, haga clic en **[!UICONTROL OK]**.

### Descripciones de columna

| Columna | Descripción |
|--- |--- |
| [!UICONTROL ID] | Identificador numérico único asignado a cada acuerdo de facturación |
| [!UICONTROL Email] | Correo electrónico de contacto de un cliente |
| [!UICONTROL First Name] | El nombre de pila de un cliente |
| [!UICONTROL Last Name] | El apellido de un cliente |
| [!UICONTROL Reference ID] | Identificador de referencia numérico y único asignado a cada contrato de facturación |
| [!UICONTROL Status] | Estado del acuerdo de pago. Opciones: `Active` o `Canceled` |
| [!UICONTROL Created] | Fecha de creación |
| [!UICONTROL Updated] | Fecha de actualización |

{style="table-layout:auto"}

## Experiencia en tienda

Los clientes que suscriban un acuerdo de facturación con un proveedor de pago pueden realizar compras ahora y pagarlas más tarde, según el acuerdo. El

![Lista de acuerdos de facturación en el panel del cliente](./assets/billing-agreements-dashboard.png){width="700" zoomable="yes"}

| Columna | Descripción |
|--- |--- |
| [!UICONTROL Reference ID] | Identificador de referencia numérico y único asignado a cada contrato de facturación |
| [!UICONTROL Status] | Estado del acuerdo de pago. Opciones: `Active` o `Canceled` |
| [!UICONTROL Created At] | Fecha de creación |
| [!UICONTROL Updated At] | Fecha de actualización |
| [!UICONTROL Payment Method] | Proveedor de pago de un acuerdo de facturación |
| [!UICONTROL View] | Botón utilizado para ver los acuerdos de facturación |

{style="table-layout:auto"}

### Crear un acuerdo de facturación

1. En su panel de cuentas, el cliente selecciona **[!UICONTROL Billing Agreements]**.

1. En **[!UICONTROL New Billing Agreement]**, selecciona un proveedor de pago.

1. Haga clic en **[!UICONTROL Create]**.

Esta acción redirige al cliente al sitio web del sistema de pago.

![Nuevo acuerdo de facturación en el panel de cuentas del cliente](./assets/create-billing-agreement-dashboard.png){width="700" zoomable="yes"}

### Ver un acuerdo de facturación

1. En su panel de cuentas, el cliente selecciona **[!UICONTROL Billing Agreements]**.

1. Selecciona el contrato de facturación y hace clic en **[!UICONTROL View]**.

![Ver acuerdo de facturación en el panel del cliente](./assets/view-billing-agreement.png){width="700" zoomable="yes"}

### Cancelar un acuerdo de facturación

1. En su panel de cuentas, el cliente selecciona **[!UICONTROL Billing Agreements]**.

1. Selecciona el contrato de facturación y hace clic en **[!UICONTROL View]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Cancel]** y luego en **[!UICONTROL OK]** para confirmar.

>[!NOTE]
>
>Si un usuario administrador (comerciante) cancela el acuerdo de facturación, no se puede cancelar en la tienda. Se muestra el estado _Cancelado_ para este contrato.
