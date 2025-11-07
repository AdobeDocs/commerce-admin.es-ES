---
title: Pedidos
description: Obtenga información sobre el espacio de trabajo Pedidos y las funciones de búsqueda utilizadas para localizar pedidos en el administrador.
exl-id: 6ec8b8c7-97c4-446e-9420-e36e72e90237
feature: Orders, Admin Workspace
source-git-commit: c60f0af09fb1af08deea49216aff340eea59f1b4
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---

# Pedidos

La cuadrícula _Pedidos_ enumera todos los pedidos actuales y rastrea su progreso y [estado de los pedidos](order-status.md) a través del [flujo de trabajo](order-processing.md). Una manera fácil de entender el proceso básico es que un pedido se convierte en una [factura](invoices.md) y una factura se convierte en un [envío](shipments.md). La cuadrícula representa la primera etapa del proceso y es donde puede [actualizar](order-update.md) pedidos existentes y crear pedidos.

Normalmente, los pedidos se crean cuando los clientes completan el proceso de cierre de compra desde la tienda. Sin embargo, si un cliente necesita ayuda, también puede acceder a su [carro de compras](shopping-assisted-cart-manage.md) o [crear un pedido](customer-account-create-order.md) desde la cuadrícula _Pedidos_ o directamente desde su cuenta de cliente.

## Área de trabajo Pedidos

El área de trabajo Pedidos enumera todos los pedidos actuales y le permite editar los pedidos existentes y [crear](customer-account-create-order.md). Cada fila de la cuadrícula representa un pedido del cliente y cada columna representa un atributo o campo de datos. Use los [controles](../getting-started/admin-grid-controls.md) estándar para ordenar y filtrar la lista, buscar pedidos y aplicar [acciones](../getting-started/admin-actions-control.md) a los pedidos seleccionados. Utilice las pestañas situadas encima de los controles de paginación para filtrar la lista, cambiar la vista predeterminada, cambiar y reorganizar las columnas y exportar datos.

![Cuadrícula de pedidos](./assets/orders-grid.png){width="700" zoomable="yes"}

### Diseño de cuadrícula

La selección de columnas y su orden en la cuadrícula se pueden cambiar según sus preferencias. El nuevo diseño se puede guardar como una cuadrícula _vista_. De forma predeterminada, solo se incluyen en la cuadrícula nueve de las 20 columnas disponibles.

![Ordenar columnas de cuadrícula](./assets/order-grid-columns.png){width="600" zoomable="yes"}

#### Cambiar la selección de columna

En la esquina superior derecha, haga clic en el control _Columns_ ( ![Column settings](../assets/icon-columns.png) ) y haga lo siguiente:

- Seleccione la casilla de verificación de cualquier columna que desee agregar a la cuadrícula.
- Desactive la casilla de verificación de cualquier columna que desee quitar de la cuadrícula.

#### Restablecer la selección de columna

1. Haga clic en el control _Columnas_ ( ![Configuración de columna](../assets/icon-columns.png) ).

1. Para restablecer las columnas de la cuadrícula, haga clic en **[!UICONTROL Reset]**.

   El diseño de la cuadrícula cambia para mostrar solamente [columnas predeterminadas](#column-descriptions).

#### Mover una columna

1. Haga clic en y mantenga presionado el encabezado de la columna.

1. Arrastre la columna a la nueva posición y suéltela.

#### Guardar una vista de cuadrícula

1. Haga clic en el control **[!UICONTROL View]** ( ![Icono de ojo](../assets/icon-view-eye.png) ).

1. Haga clic en **[!UICONTROL Save Current View]**.

1. Escriba **[!UICONTROL name]** para la vista.

1. Para guardar todos los cambios, haga clic en la flecha ( ![Icono de flecha](../assets/icon-arrow-save.png) ).

   El nombre de la vista aparece ahora como la vista actual.

#### Cambio de la vista

Haga clic en el control **[!UICONTROL View]** ( ![Icono de ojo](../assets/icon-view-eye.png) ). A continuación, realice una de las siguientes acciones:

- Para utilizar una vista diferente, haga clic en el nombre de la vista.

- Para cambiar el nombre de una vista, haga clic en el icono _Editar_ ( ![Icono de lápiz](../assets/icon-edit-pencil.png) ) y actualice el nombre.

### Controles de Workspace

| Control | Descripción |
|--- |--- |
| [!UICONTROL Create New Order] | Crea un pedido. Consulte [Creación de un pedido](customer-account-create-order.md) para obtener más información. |
| [!UICONTROL Go to Archive] | Muestra la lista de pedidos archivados. |
| [!UICONTROL Search] | Inicia una búsqueda de pedidos basada en los filtros actuales. |
| [!UICONTROL Filters] | Define un conjunto de parámetros de búsqueda utilizados para filtrar los registros que aparecen en la cuadrícula. |
| [!UICONTROL Default View] | Determina el diseño de columna predeterminado de la cuadrícula. |
| [!UICONTROL Columns] | Determina la selección de columnas y su orden en la cuadrícula. El diseño de la columna se puede cambiar y guardar como _vista_. De forma predeterminada, solo algunas de las columnas se incluyen en la cuadrícula. |
| [!UICONTROL Export] | Exporta los registros seleccionados como un archivo CSV o XML de Excel. |

{style="table-layout:auto"}

### Acciones

Para aplicar una acción a pedidos específicos, seleccione la casilla de verificación en la primera columna de cada pedido. Para seleccionar o anular la selección de todos los pedidos, utilice el control situado en la parte superior de la columna.

![Acciones de pedido](./assets/orders-action.png){width="600" zoomable="yes"}

| Control | Descripción |
|--- |--- |
| [!UICONTROL Actions] | Muestra todas las acciones que se pueden aplicar a los pedidos seleccionados. Para aplicar una acción a un pedido o grupo de pedidos, active la casilla de verificación de la primera columna de cada pedido. <br/>Acciones de pedido: `Cancel` / `Hold` / `Unhold` / `Print Invoices` / `Print Packing Slips` / `Print Credit Memos` / `Print All` / `Print Shipping Labels` / `Move to Archive` ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) |
| [!UICONTROL Mass Actions] | Se puede utilizar para seleccionar varios registros como objetivo de la acción. Seleccione la casilla de verificación en la primera columna de cada registro sujeto a la acción. Opciones: `Select All` / `Unselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL Submit] | Aplica la acción actual a los registros de pedidos seleccionados. |
| [!UICONTROL Edit] | Abre el orden en el modo de edición. |

{style="table-layout:auto"}

### Descripciones de columna

| Columna | Descripción |
|--- |--- |
| [!UICONTROL Select] | Seleccione las casillas de verificación para que las comillas estén sujetas a una acción o utilice el control de selección en el encabezado de la columna. Opciones: Seleccionar todo/Anular la selección de todo |
| [!UICONTROL ID] | Un número secuencial único que se asigna cuando se guarda un nuevo pedido por primera vez. |
| [!UICONTROL Purchase Point] | Identifica la vista de la tienda en la que se realizó el pedido. |
| [!UICONTROL Purchase Date] | La fecha y la hora en que se realizó el pedido. Siempre se muestra según la zona horaria predeterminada. |
| [!UICONTROL Bill-to Name] | El nombre de la persona responsable de pagar el pedido. |
| [!UICONTROL Ship-to Name] | El nombre de la persona a la que se va a enviar el pedido. |
| [!UICONTROL Grand Total (Base)] | El total general del pedido. |
| [!UICONTROL Grand Total (Purchased)] | El total general de productos comprados en el pedido. |
| [!UICONTROL Status] | El estado actual del pedido. |
| [!UICONTROL Action] | _[!UICONTROL View]_abre el pedido en modo de edición. |
| [!UICONTROL Allocated sources] | Las fuentes asignadas a ese orden específico. |

{style="table-layout:auto"}

Columnas adicionales disponibles:

| Columna | Descripción |
|--- |--- |
| [!UICONTROL Billing Address] | La dirección de facturación del cliente que realizó el pedido. |
| [!UICONTROL Shipping Address] | La dirección a la que se enviará el pedido. |
| [!UICONTROL Shipping Information] | El método que se va a utilizar para enviar el pedido. |
| [!UICONTROL Customer Email] | La dirección de correo electrónico de la persona que realizó el pedido. |
| [!UICONTROL Customer Group] | Grupo de clientes al que está asignada la persona que realizó el pedido. |
| [!UICONTROL Subtotal] | El subtotal del pedido, sin envío ni manipulación, y los impuestos. |
| [!UICONTROL Shipping and Handling] | El importe cobrado por el envío y la manipulación. |
| [!UICONTROL Customer Name] | El nombre y los apellidos del cliente que realizó el pedido. |
| [!UICONTROL Payment Method] | El método de pago que se utilizará para el pedido. |
| [!UICONTROL Total Refunded] | Cualquier importe del pedido que deba reembolsarse al cliente. |
| [!UICONTROL Refunded to Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Cualquier cantidad del pedido que se deba reembolsar al crédito de tienda del cliente. |
| [!UICONTROL Company Name] | ![Adobe Commerce B2B](../assets/b2b.svg) (disponible con Adobe Commerce B2B) El nombre de la [empresa](../b2b/account-companies.md) que realizó el pedido. |

{style="table-layout:auto"}

## Búsqueda de pedidos

El cuadro Buscar de la parte superior izquierda de la cuadrícula Pedidos se puede utilizar para buscar pedidos específicos por palabra clave o filtrando los registros de pedidos de la cuadrícula.

![Resultados de búsqueda](./assets/order-search.png){width="600" zoomable="yes"}

### Buscar una coincidencia

1. Introduzca un término de búsqueda en el cuadro de búsqueda de la página.

1. Para mostrar los resultados, haga clic en _Buscar_ ( ![Icono de lupa](../assets/icon-magnify-search.png) ).

### Filtrado de la búsqueda

1. Para mostrar la selección de filtros de búsqueda, haga clic en la ficha _Filtros_ ( ![icono de Funnel](../assets/icon-filter-search.png) ).

   ![Filtros de pedidos](./assets/order-search-filter.png){width="600" zoomable="yes"}

1. Complete tantos filtros como desee para describir los pedidos que desea encontrar.

1. Haga clic en **[!UICONTROL Apply Filters]** para mostrar los resultados.

### Filtros de búsqueda

| Filtrar | Descripción |
|--- |--- |
| [!UICONTROL Purchase Date] | Filtra la búsqueda en función de la fecha de compra. Para buscar pedidos dentro de un intervalo de fechas, escriba las fechas **[!UICONTROL from]** y **[!UICONTROL to]**. |
| [!UICONTROL ID] | Filtra la búsqueda en función del ID de pedido. |
| [!UICONTROL Grand Total (Base)] | Filtra la búsqueda según el total general de cada pedido, que incluye los créditos aplicados al pedido. |
| [!UICONTROL Grand Total (Purchased)] | Filtra la búsqueda en función del total general de artículos comprados en cada pedido. |
| [!UICONTROL Bill-to Name] | Filtra la búsqueda según el nombre de la persona responsable de pagar el pedido. |
| [!UICONTROL Ship-to Name] | Filtra la búsqueda según el nombre de la persona a la que se envía cada pedido |
| [!UICONTROL Purchase Point] | Filtra la búsqueda por sitio web, tienda o vista de tienda donde se realizó el pedido. |
| [!UICONTROL Status] | Filtra la búsqueda en función del estado del pedido. Opciones: `Canceled` / `Closed` / `Complete` / `Suspected Fraud` / `On Hold` / `Payment Review` / `PayPal Canceled Reversal` /` PayPal Reversed` /` Pending` / `Pending Payment` / `Pending PayPal` / `Processing` |
| [!UICONTROL Braintree Transaction Source] | Filtra la búsqueda en función del origen de transacción. |

{style="table-layout:auto"}

### Herramientas de búsqueda

| Herramienta | Descripción |
|--- |--- |
| [!UICONTROL Apply Filters] | Aplica todos los filtros a los resultados de búsqueda. |
| [!UICONTROL Cancel] | Cancela la búsqueda actual. |
| [!UICONTROL Clear All] | Borra todos los filtros de búsqueda. |

{style="table-layout:auto"}

