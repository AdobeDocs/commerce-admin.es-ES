---
title: Envíos
description: Obtenga información sobre cómo crear registros de envío para facturas y cancelar envíos.
exl-id: 6df83549-ba38-43f7-aab1-dbf3f6b89d74
feature: Shipping/Delivery, Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 0%

---

# Envíos

La cuadrícula _[!UICONTROL Shipments]_muestra el registro de envío de todas las facturas que se han preparado para el envío. Se puede generar un registro de envío cuando se [factura](invoices.md) o posterior un pedido.

Adobe Commerce y el Magento Open Source admiten el envío de pedidos parcial y completo, con opciones adicionales disponibles en [Inventory management](../inventory-management/introduction.md) y extensiones de terceros.

![Cuadrícula de envíos](./assets/shipments.png){width="600" zoomable="yes"}

## Descripciones de columna

| Columna o control | Descripción |
|--- |--- |
| [!UICONTROL Select] | Seleccione la casilla de verificación para que cada comilla esté sujeta a una acción o utilice el control de selección en el encabezado de la columna. Opciones: `Select All` / `Deselect All` |
| [!UICONTROL Shipment] | Un número secuencial único que se asigna cuando se guarda un nuevo envío por primera vez |
| [!UICONTROL Ship Date] | Fecha de envío |
| [!UICONTROL Order] | Número único del pedido |
| [!UICONTROL Order Date] | La fecha y la hora en que se realizó el pedido |
| [!UICONTROL Ship-to Name] | El nombre de la persona a la que se envía el pedido |
| [!UICONTROL Total Quantity] | Cantidad total de artículos para enviar |
| [!UICONTROL Action] | Ver abre el envío en modo de edición |

{style="table-layout:auto"}

Columnas adicionales:

| Columna | Descripción |
|--- |--- |
| [!UICONTROL Order Status] | Indica el estado del pedido |
| [!UICONTROL Purchased From] | Indica el sitio web, la tienda y la vista de la tienda donde se realizó el pedido |
| [!UICONTROL Customer Name] | El nombre del cliente o comprador que realizó el pedido |
| [!UICONTROL Email] | La dirección de correo electrónico de un cliente registrado |
| [!UICONTROL Customer Group] | El nombre del grupo de clientes o del catálogo compartido al que está asignado el cliente |
| [!UICONTROL Billing Address] | El nombre del cliente o comprador que realizó el pedido |
| [!UICONTROL Shipping Address] | El nombre de la persona a la que se envía el pedido |
| [!UICONTROL Payment Method] | El método de pago que se utilizará para el pedido |
| [!UICONTROL Shipping Information] | El método que se utilizará para enviar el pedido |

{style="table-layout:auto"}

## Creación de un envío

Las siguientes instrucciones le guían a través del proceso para crear un envío en Adobe Commerce o Magento Open Source. Si tienes Inventory management habilitado, puedes revisar [Crear envíos de varios Source](../inventory-management/shipments-create.md) y seleccionar un origen (o ubicación) y una cantidad para enviar por artículo de línea.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Busque el orden en la cuadrícula y ábralo.

1. Si el pedido está pagado, facturado y listo para enviarse, haga clic en **[!UICONTROL Ship]**.

   Las secciones de la parte superior del envío contienen el nombre, la dirección y la información de pago del pedido de venta.

1. Complete cada sección del formulario de envío siguiendo las instrucciones de las secciones siguientes.

### [!UICONTROL Items to Ship]

Para cada elemento de línea del pedido, modifique **[!UICONTROL Qty to Ship]** según sea necesario.

### [!UICONTROL Shipping Information]

**Método 1:** que usa la página de pedidos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. En la columna **[!UICONTROL Action]** del orden seleccionado, haga clic en **[!UICONTROL View]**.

1. Haga clic en **[!UICONTROL Ship]**.

1. Desplácese hasta el bloque _[!UICONTROL Payment & Shipping Method]_y haga clic en **[!UICONTROL Add Tracking Number]**.

1. Establecer **[!UICONTROL Carrier]**:

   - `Custom Value`
   - `DHL`
   - `Federal Express`
   - `United Parcel Service`
   - `United States Postal Service`

1. Para realizar el seguimiento del envío, escriba **[!UICONTROL Title]** y **[!UICONTROL Number]**

**Método 2:** usando la página de envío

Este método solo se permite si el envío del pedido ya se ha creado desde la página de pedidos.
Puede modificar la información de envío y seguimiento según sea necesario mediante la página Envío Directo:

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Busque y abra el envío en modo de edición.

1. Desplácese hacia abajo hasta el bloque _[!UICONTROL Payment & Shipping Method]_.

1. Seleccione **[!UICONTROL Carrier]**.

1. Escriba un **[!UICONTROL Title]** para el paquete.

1. Escriba el seguimiento **[!UICONTROL Number]**.

1. Haga clic en **[!UICONTROL Add]**.

1. Para enviar un correo electrónico con información de seguimiento al cliente, haga clic en **[!UICONTROL Send Tracking Information]** y confirme la acción.

   Para rastrear la ubicación de cualquier envío, abra el envío requerido en modo de edición y haga clic en **[!UICONTROL Track this shipment]**.

   ![Información de envío y seguimiento](./assets/tracking-information.png){width="600" zoomable="yes"}

### Botones

| Botón | Descripción |
|--- |--- |
| **[!UICONTROL Back]** | Cierra el formulario Nuevo envío y vuelve al pedido |
| **[!UICONTROL Submit Shipment]** | Añade el envío del pedido. |
| **[!UICONTROL Reset]** | Restaura todos los campos a los valores originales. |

{style="table-layout:auto"}

### Comentarios de envío

1. Escriba **Comentarios** para el envío, si es necesario.

1. Cuando el envío esté listo, haga clic en **Enviar envío**.

## Configuración de comentarios para envíos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En _[!UICONTROL Sales]_, seleccione **[!UICONTROL Sales Email]**.

1. Expanda la sección **Comentarios sobre el envío** y modifique la configuración según sea necesario:

   ![Configuración de comentarios de envío](../configuration-reference/sales/assets/sales-emails-shipment-comments.png){width="600" zoomable="yes"}

   - La opción **[!UICONTROL Enabled]** está establecida en `Yes` de forma predeterminada, lo que significa que el correo electrónico se envía a un cliente cuando se escribe un comentario de envío.

   - Para **[!UICONTROL Shipment Comment Email Sender]**, seleccione la persona desde la que se enviará el correo electrónico de comentarios sobre el envío. El valor predeterminado ofrece cinco direcciones de correo electrónico.

   - Para **[!UICONTROL Shipment Comment Email Template]**, seleccione la plantilla según sus necesidades o seleccione la opción predeterminada.

   - Para **[!UICONTROL Shipment Comment Email Template for Guests]**, elija la plantilla usada para los clientes que no tienen una cuenta en su tienda.

   - Para **[!UICONTROL Shipment Comment Email Copy To]**, escriba las direcciones de correo electrónico para enviar una copia del correo electrónico de comentarios de envío. Separe varias direcciones de correo electrónico con una coma.

   - Para **[!UICONTROL Shipment Comment Email Copy Method]**, seleccione `bcc` (copia oculta) o `separate email copy` método según sus preferencias.

1. Haga clic en **[!UICONTROL Save Config]**.

## Cancelar un envío

Antes de enviar un envío a un transportista, se puede cancelar abriendo el pedido y navegando hasta el envío, siempre que el transportista admita las cancelaciones. Algunos operadores restringen o limitan las cancelaciones después de una reserva. Por ejemplo, UPS permite cancelaciones, pero requiere que espere 24 horas después de que se reserve el envío. Si se cancela un envío, la cancelación no se puede revertir. El único recurso es recrear el orden.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Busque el orden en la cuadrícula.

1. En la columna _Acción_, elija **[!UICONTROL View]**.

1. En el panel izquierdo, elija **[!UICONTROL Shipments]**.

   Si el envío se puede cancelar, _[!UICONTROL Cancel Shipment]_aparece como una opción en la barra de botones superior.

1. Haga clic en **[!UICONTROL Cancel Shipment]**.

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL OK]**.

El estado del envío cambia a `Canceled`. Si el transportista no admite cancelaciones, aparece un mensaje de error que explica por qué no se pudo cancelar el envío.

## Descripciones de campos de envío

### [!UICONTROL Shipping Information]

| Campo | Descripción |
|-----|-----------|
| [!UICONTROL Carrier] | El nombre del operador seleccionado |
| [!UICONTROL Title] | Un nombre descriptivo asignado al paquete por el transportista. |
| [!UICONTROL Number] | El número de seguimiento vinculado asignado al paquete. |
| [!UICONTROL Action] | ![Icono de la papelera](../assets/icon-delete-trashcan-solid.png): elimina la información del paquete del registro de envío. |
| [!UICONTROL Add] | Añada otro paquete al envío. |

{style="table-layout:auto"}

### [!UICONTROL Route Information]

| Campo | Descripción |
|-----|-----------|
| [!UICONTROL Origin Location] | Muestra una lista de ubicaciones disponibles. |
| [!UICONTROL International] | Si está activado, identifica el envío como envío internacional. |

{style="table-layout:auto"}

### [!UICONTROL Items Ordered]

| Campo | Descripción |
|-----|-----------|
| [!UICONTROL Description] | La descripción del artículo. |
| [!UICONTROL SKU] | La unidad de mantenimiento de stock del artículo. |
| [!UICONTROL Weight] | El peso del elemento. |
| [!UICONTROL Qty Ordered] | La cantidad del artículo que se ha pedido. |
| [!UICONTROL Qty Shipped] | La cantidad de artículos que se han enviado. |
| [!UICONTROL Qty Packed] | El número de elementos incluidos en este paquete. |

{style="table-layout:auto"}

### [!UICONTROL Shipment Comments]

| Campo | Descripción |
|-----|-----------|
| [!UICONTROL Comments] | Los comentarios sobre el envío son para uso interno. |

{style="table-layout:auto"}

### [!UICONTROL Documentation]

| Campo | Descripción |
|-----|-----------|
| [!UICONTROL Package Label] | **PNG** - Descargue la etiqueta del paquete de envío. Tamaño: A6 (105 x 148 mm; 4,1 x 5,6 pulgadas) |

{style="table-layout:auto"}
