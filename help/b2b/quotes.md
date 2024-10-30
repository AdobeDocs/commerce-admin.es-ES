---
title: Comillas negociables
description: Obtenga información sobre los flujos de trabajo de presupuestos y cómo puede proporcionar este servicio a las cuentas de su empresa.
exl-id: c278818b-fa5a-4e7a-8ca2-c4b757da4f05
feature: B2B, Quotes
source-git-commit: 7f4993ff8b16beda2a371737fb5a8ecb5f9c9396
workflow-type: tm+mt
source-wordcount: '1269'
ht-degree: 0%

---

# Comillas negociables

Los compradores y vendedores utilizan las ofertas para gestionar el proceso de negociación de artículos de adición de pedidos, actualización de cantidades, solicitud y aplicación de descuentos, etc., hasta que llegan a un acuerdo. El proceso de negociación de la oferta puede iniciarlo un comprador autorizado de la empresa o un representante de ventas de la empresa.

![Vista de lista de comillas en el administrador](./assets/quotes-admin-list-view-intro.png){width="700" zoomable="yes"}

Una vez creada la oferta, el proceso de negociación comienza cuando el comprador o el vendedor envía la oferta para su revisión. La cuadrícula _Ofertas_ que enumera todas las ofertas recibidas y mantiene un historial de la comunicación entre el comprador y el vendedor. Use los [controles de área de trabajo](../getting-started/admin-workspace.md) estándar para filtrar la lista, cambiar el diseño de la columna, guardar vistas y exportar datos.

- En la tienda, los compradores envían la cotización como una [solicitud para negociar](quote-price-negotiation.md) el precio del carro de compras. Al crear la solicitud de presupuesto, un comprador puede guardarla como borrador o enviarla directamente al vendedor.

- En el Administrador, los representantes de ventas pueden crear presupuestos en nombre del comprador de la empresa. Al crear la oferta, un vendedor puede guardarla como borrador o enviarla directamente al comprador para iniciar el proceso de negociación.

Durante el proceso de negociación, la oferta sólo puede ser actualizada por la persona que revisa y propone las condiciones para una negociación posterior.

## Requisitos previos

Las ofertas negociables solo están disponibles si Adobe Commerce tiene las siguientes opciones de configuración:

- [Se instala la extensión Adobe Commerce B2B](install.md)
- [Funciones B2B configuradas](enable-basic-features.md)
   - Habilitar cuentas de empresa
   - Activar presupuesto B2B

## Flujo de trabajo de oferta

El comprador o el vendedor pueden iniciar las cotizaciones.

Este diagrama muestra los estados de las ofertas de un comprador y un vendedor (administrador) en los diferentes pasos que se siguen cuando se inicia una oferta.

![Flujo de trabajo de estado de ofertas](./assets/quote-status-workflow.svg){width="700" zoomable="yes"}

**Paso 1: Creación de presupuesto (Nuevo)**

- **El comprador solicita un presupuesto** - El comprador [solicita un presupuesto](quote-request.md) del carro de compras. La solicitud aparece en la lista _Mis presupuestos_ del panel de cuentas del comprador y se envía una notificación por correo electrónico al representante de ventas asignado a la cuenta de la compañía. En el Administrador, la solicitud aparece en la cuadrícula _Quotes_, con el estado `New`. El comprador puede modificar una solicitud de presupuesto hasta que el vendedor la abra.

  ![Comillas](./assets/quote-request-from-shopping-cart.png){width="700" zoomable="yes"}

- **Representante de ventas** — Un representante de ventas puede [crear una cotización](sales-rep-initiates-quote.md) del administrador en nombre de un comprador específico de la compañía. El representante de ventas debe actualizar la oferta para añadir productos y otra información como descuentos y notas al comprador. La representación de ventas puede guardar la oferta como `draft` o enviarla al comprador para que inicie la negociación. En estado de borrador, la oferta solo es visible para el vendedor. Una vez enviado el presupuesto, el estado es `Submitted`. El vendedor no puede modificarla hasta que el comprador la devuelva.

  ![El vendedor está iniciando una cotización de comprador desde la cuadrícula de cotizaciones del administrador](./assets/quote-draft-from-admin.png){width="700" zoomable="yes"}

**Paso 2: Revisión y negociación de presupuesto (Revisar)**

La revisión o negociación de una oferta puede incluir el cambio de cantidades, la eliminación de artículos, la adición de comentarios de artículos de línea, la aplicación de descuentos de artículos de línea o ofertas (vendedor) y la adición de una dirección de envío (comprador).

- **El vendedor ve la solicitud y envía una respuesta**: en el administrador, el vendedor ve la solicitud de presupuesto. En la tienda, el estado de la oferta cambia a `Pending` y el comprador no puede realizar ningún cambio. El [vendedor responde](quote-price-negotiation.md) ofreciendo descuentos en los precios y ajustando las cantidades y los artículos según sea necesario, introduce un comentario y devuelve el presupuesto al comprador. Se notifica al comprador y al vendedor por correo electrónico que el vendedor ha respondido.

- **El comprador ve el presupuesto del vendedor y envía una respuesta**. El comprador hace clic en el vínculo de la notificación por correo electrónico para abrir el presupuesto o abre el presupuesto desde la página _Mis presupuestos_ del panel de la cuenta. El comprador puede dejar notas al vendedor en el nivel de artículo de línea u oferta, cambiar cantidades y eliminar artículos.

El comprador y el vendedor pueden continuar con el proceso de negociación hasta que se llegue a un acuerdo o hasta que el vendedor rechace la oferta. Si el comprador realiza cambios en la oferta (añadir o eliminar productos o cambiar cantidades de productos), la oferta debe devolverse al vendedor para que la revise.

- **El comprador agrega una dirección de envío**. El comprador puede agregar una dirección de envío a la oferta. Una vez que el comprador añade la dirección, el vendedor puede proporcionar las opciones de envío y entrega. Los métodos de envío mostrados dependen de la configuración de la Tienda.

Si el comprador añade una dirección de envío, el acuerdo de negociación debe revisarse y el vendedor puede continuar con el proceso de negociación hasta que se alcance un acuerdo o hasta que el vendedor rechace la oferta.

**Paso 3: el comprador acepta el presupuesto (cierre de compra)**

El comprador acepta el precio propuesto y procede al pago. No se pueden añadir descuentos adicionales al presupuesto negociado.

Las opciones de envío están bloqueadas en el cierre de compra.

## Estado de oferta

El estado de la oferta proporciona información sobre el estado actual de la oferta en el flujo de trabajo de oferta. El estado de una oferta solo cambia cuando un comprador o vendedor realiza una acción sobre la oferta. Por ejemplo, el estado cambia a pedido si un comprador selecciona [!UICONTROL Proceed to Checkout] en una oferta activa.

- *[!UICONTROL New]**: el comprador envió una solicitud de presupuesto, pero el vendedor no la ha visto. El comprador puede actualizar la solicitud hasta que la abra el vendedor.

- **[!UICONTROL Draft]** - El vendedor crea un presupuesto provisional para un comprador. El comprador no puede ver la oferta hasta que el vendedor añade los detalles de la oferta (artículos, cantidad, descuento, etc.) y envía la oferta al comprador.

- **[!UICONTROL Open]**: el vendedor ha abierto la solicitud y está revisándola y preparando una respuesta

- **[!UICONTROL Submitted]** - El vendedor envió una respuesta al comprador. El registro de oferta no se puede editar durante el proceso de negociación.

- **[!UICONTROL Client Reviewed]**: el comprador ha visto la respuesta del vendedor y está preparando una respuesta.

- **[!UICONTROL Updated]**: el comprador envió una respuesta, pero el vendedor no la ha visto.

- **[!UICONTROL Ordered]** - El comprador envió el pedido basándose en la oferta negociada.

- **[!UICONTROL Closed]** - El comprador ha cancelado la solicitud de presupuesto.

- **[!UICONTROL Declined]** - El vendedor rechazó la solicitud de presupuesto. Los precios personalizados se eliminan del presupuesto y el registro está bloqueado para futuras ediciones.

- **[!UICONTROL Expired]** - El comprador no respondió a la respuesta del vendedor en el período de tiempo designado y la oferta ya no es válida.

## Recursos de rol B2B para presupuestos de tienda

Las opciones de configuración para las comillas se controlan mediante los [recursos de rol](../systems/permissions-user-roles.md#role-resources). Estos recursos de rol deben establecerse para el rol de usuario Administrador que se asigna al administrador del almacén.

Para conceder acceso a las funciones de presupuesto en Admin, vaya a **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**, seleccione el rol y vaya a [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] en el árbol_ Recursos de rol _.

![Comillas, roles y permisos](./assets/roles-permissions-quotes.png){width="700" zoomable="yes"}

## Aplicar una acción

En el Administrador, los administradores y vendedores de B2B pueden administrar presupuestos desde la cuadrícula de presupuestos mediante el menú [!UICONTROL Actions].

![Comillas](./assets/quotes-grid.png){width="700" zoomable="yes"}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Sales]** > **[!UICONTROL Quotes]**.

1. En la primera columna de la cuadrícula, active la casilla de verificación de cada registro al que desee aplicar la acción.

1. En **[!UICONTROL Actions]**, seleccione la acción que desea aplicar.

### Ver un presupuesto

1. En la columna **[!UICONTROL Actions]** de un registro, haga clic en **[!UICONTROL View]**.

1. Para responder a la solicitud del cliente, siga las instrucciones y comience el proceso de [negociación de precios](quote-price-negotiation.md).

### Ver actividad de presupuesto

Vea la cronología de negociación, la comunicación y otra actividad de oferta de [!UICONTROL Comments] y [!UICONTROL History Log]; la información incluye cambios de estado, actualizaciones de la información de cliente y envío, actualizaciones de artículos y precios y otra información importante.

1. Abra una cotización.

1. Ver comentarios e historial de negociación de presupuesto desplazándose hasta **[!UICONTROL Negotiation]** y seleccionando **[!UICONTROL Comments]** y **[!UICONTROL History Log]**.

   ![Ver historial](./assets/quote-view-history.png){width="400"}

1. El historial también se rastrea en el nivel de elemento de línea.

   ![Ver historial de elementos de línea](./assets/quote-view-line-item-history.png){width="400"}


### Rechazar una solicitud de presupuesto

Solo se pueden rechazar las solicitudes de presupuesto con un estado `Open`.

1. Seleccione cada solicitud de presupuesto abierta que desee rechazar.

1. Establezca el control _[!UICONTROL Actions]_en `Declined`.

1. Cuando se le solicite, introduzca el motivo por el que se rechazó la oferta y haga clic en **[!UICONTROL Confirm]**.

   ![Rechazar presupuesto?](./assets/quote-decline-confirm.png){width="400"}
