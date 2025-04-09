---
title: Casos de uso y flujos de trabajo de plantillas de oferta
description: Cree una plantilla de oferta a partir de una oferta existente para agilizar la negociación de ofertas para pedidos recurrentes.
feature: B2B, Quotes
exl-id: 7d1e7a3d-6c50-416a-b490-0a083e1c06b4
source-git-commit: 6fe8a356ab517fc5dd169c4a6f7ef52937f705c4
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 0%

---

# Caso de uso y flujos de trabajo de plantillas de oferta

La función Plantilla de oferta permite a compradores y vendedores optimizar el proceso de oferta mediante la creación de plantillas de oferta reutilizables y personalizables.

- **Ofertas personalizables**: los compradores pueden generar ofertas vinculadas a partir de una plantilla aprobada previamente, lo que permite la personalización dentro de parámetros especificados, como cantidades y selecciones de artículos de línea.
- **Umbrales de pedido**: los vendedores pueden establecer compromisos de pedido mínimos y máximos para garantizar que los compradores cumplan los volúmenes de compra acordados. Una vez que el comprador acepta la plantilla de oferta, el recuento de umbral de pedido aumenta cada vez que se genera una oferta vinculada. Si la oferta vinculada se cierra sin convertirse en un pedido, el pedido se resta del recuento de umbral. Cuando se alcanza el umbral de pedido máximo, caduca la plantilla de oferta.
- **Fechas de caducidad**: las plantillas pueden tener períodos de validez (*[!UICONTROL Valid Until]*), lo que garantiza que los términos solo se apliquen en un lapso de tiempo especificado. En el momento de la caducidad, la plantilla se cierra y todas las comillas vinculadas se cierran.
- **Descuentos y Asignación de Precios**- Los vendedores pueden utilizar las mismas capacidades de descuento de artículos de línea, ofertas y precios de envío disponibles con las ofertas para establecer descuentos para pedidos recurrentes, lo que simplifica el proceso de negociación.
- **Tracking and Reporting**—The system tracks the number of linked quotes generated from the template and successfully completed orders to provide insights into the fulfillment of agreed upon order quotas.
- **Reference Document Links**—Both buyers and sellers can add, edit, and manage external document links (such as DocuSign, Adobe Sign, or other online services) to the quote template. This enables easy access to related contracts and agreements during the quote template process.

## Use Case

A company buyer can use a quote template to order a specific set of products over a period of time. The buyer configures the following quote template options to make the quoting process more efficient, consistent, and aligned with strategic purchasing agreements.

- El pedido umbral especificar el número mínimo y máximo de pedidos elegibles para el precio negociado. Se puede utilizar para aplicar y rastrear las cuotas de pedidos especificadas en los acuerdos de contrato.

- Umbrales de cantidad (cantidades mínimas/máximas) La plantilla especifica un umbral de cantidad para establecer la cantidad mínima y máxima que se puede comprar para cada pedido, lo que garantiza que el vendedor pueda gestionar los niveles de stock de forma eficaz y, al mismo tiempo, proporciona al comprador la flexibilidad para ajustar las cantidades según sea necesario.

- Vínculos de documento de referencia para mantener conexiones con contratos y acuerdos externos, lo que facilita el acceso a la documentación relacionada durante el proceso de oferta.

## Flujo de trabajo de plantilla de oferta

Quote templates can be initiated by the buyer or the seller.

**Step 1: Quote template creation (New)**

- **El comprador crea la plantilla de presupuesto**

  Al revisar una oferta existente, el comprador decide que la empresa debe enviar varios pedidos durante el año siguiente y quiere solicitar descuentos adicionales basados en la repetición de la operación. Crean una plantilla de oferta utilizando la acción *[!UICONTROL Create quote template]* en la oferta. El comprador puede añadir enlaces de documentos de referencia a contratos o acuerdos externos utilizando el control *[!UICONTROL Add]* en la sección de documentos de referencia. A continuación, inicia la negociación enviando la plantilla de oferta al vendedor para que la revise.

  Los compradores también pueden solicitar una plantilla de presupuesto añadiendo productos que deseen comprar con regularidad al carro de compras. A continuación, solicite un presupuesto y mencione en los comentarios la frecuencia con la que desean repetir la compra.

- **Representante de ventas**: un representante de ventas puede crear una plantilla de presupuesto del administrador en nombre de un comprador específico de la compañía. El representante de ventas puede crear la plantilla de oferta en el administrador a partir de una oferta existente o de la cuadrícula [!UICONTROL Quote Templates] y guardarla como `draft` o enviarla al comprador para que inicie la negociación. En estado de borrador, la oferta solo es visible para el vendedor. Una vez enviado el presupuesto, el estado es `Submitted`. El vendedor no puede modificarla hasta que el comprador la devuelva.

  ![El vendedor está iniciando una cotización de comprador desde la cuadrícula de cotizaciones del administrador](./assets/quote-template-create-from-grid.png){width="700" zoomable="yes"}

  Cuando el vendedor crea la plantilla de oferta, la fecha de caducidad (campo [!UICONTROL Valid until]) es de 180 días de forma predeterminada. Si el comprador ha creado la plantilla, la fecha de caducidad está en blanco.  El comprador debe establecer la fecha de caducidad antes de devolver la plantilla al comprador para que la revise.

  When the seller creates the quote template, the expiration date (*[!UICONTROL Valid until]* date field) defaults to 180 days. If the buyer created the template, the expiration date is blank.  The buyer must set the expiration date before sending the template back to the buyer for review.

**Step 2: Quote review and negotiation (Review)**

Revisar o negociar un plantilla de cotización puede incluir cambiar cantidades, eliminar artículos, agregar elemento de línea comentarios, aplicar descuentos de elemento de línea o cotización (vendedor), agregar una dirección de envío (comprador) y administrar enlaces de documento de referencia.

- **El vendedor ve solicitud y envía la respuesta** : en el administrador, el vendedor ve el plantilla de cotización desde la *[!UICONTROL Quote Templates]* cuadrícula * o lo abre desde la vincular en el correo electrónico notificación. En el escaparate, el estado de la cita cambia a `Pending`, y el comprador no puede realizar ningún cambio. Siguiendo el mismo proceso para la [negociación de presupuesto](quote-price-negotiation.md), el vendedor responde ofreciendo descuentos en los precios y ajustando las cantidades y los artículos según sea necesario, introduce un comentario y devuelve la plantilla de presupuesto al comprador. El vendedor también puede añadir, editar o eliminar vínculos a documentos de referencia durante este proceso. Se notifica al comprador y al vendedor por correo electrónico que el vendedor ha respondido.

- **Buyer views quote template from seller and sends response** - The buyer clicks the link in the email notification to open the quote template, or opens it from the _My Quote Templates_ page of the account dashboard. The buyer can leave notes to the seller at the line item or quote level, change quantities, remove items, and manage reference document links.

The buyer and seller continue the negotiation process until an agreement is reached, or the seller declines the quote template. If the buyer makes changes to the quote template—adding or removing products, changing product quantities, or modifying reference document links—it must be returned to the seller for review.

- **Buyer adds a shipping address** - The buyer must add a shipping address to the quote template if it doesn&#39;t have one. Una vez que el comprador añade la dirección, el vendedor puede proporcionar las opciones de envío y entrega. Los métodos de envío mostrados dependen de la configuración de la Tienda.

Si el comprador añade una dirección de envío, el acuerdo de negociación debe revisarse y el vendedor puede continuar con el proceso de negociación hasta que se alcance un acuerdo o hasta que el vendedor rechace la plantilla de oferta.

**Paso 3: el comprador acepta la plantilla de presupuesto**

El comprador acepta las condiciones negociadas en la plantilla. Una vez aceptada la plantilla de oferta, el comprador puede usarla para [generar ofertas vinculadas y preaprobadas](account-dashboard-my-quote-templates.md#generate-a-linked-quote) que se pueden usar para enviar pedidos sin necesidad de más negociación.

Las opciones de envío están bloqueadas en el cierre de compra.

Quote templates remain active until it expires, is canceled or closed, or it is no longer valid buyer has reached the maximum order threshold.

### View a quote template

1. In the **[!UICONTROL Actions]** column for a record, click **[!UICONTROL View]**.

1. To respond to the customer request, follow the instructions and begin the same [price negotiation](quote-price-negotiation.md) process used to negotiation quotes.

### View quote template activity

Vea la cronología de negociación, la comunicación y otra actividad de plantilla de oferta de [!UICONTROL Comments] y [!UICONTROL History Log]; la información incluye cambios de estado, actualizaciones de la información de cliente y envío, actualizaciones de artículos y precios y otra información importante.

1. Abra una plantilla de presupuesto.

1. Ver comentarios e historial de negociación de presupuesto desplazándose hasta **[!UICONTROL Negotiation]** y seleccionando **[!UICONTROL Comments]** y **[!UICONTROL History Log]**.

   ![View History](./assets/quote-view-history.png){width="400" zoomable="yes"}

1. History is also tracked at the line item level.

   ![View Line Item History](./assets/quote-view-line-item-history.png){width="400" zoomable="yes"}

### Rechazar una plantilla de presupuesto

Solo se pueden rechazar las plantillas de presupuesto con un estado `In Review`.

1. En la cuadrícula *[!UICONTROL Quote Templates]*, abra la plantilla de oferta que desee rechazar.

1. En la plantilla de presupuesto, haga clic en **[!UICONTROL Decline]**.

1. Cuando se le solicite, introduzca el motivo por el que se rechazó la oferta y haga clic en **[!UICONTROL Confirm]**.
