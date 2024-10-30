---
title: Casos de uso y flujos de trabajo de plantillas de oferta
description: Cree una plantilla de oferta a partir de una oferta existente para agilizar la negociación de ofertas para pedidos recurrentes.
feature: B2B, Quotes
source-git-commit: 3000d9abab467a86e37c7eca6e7db16b39c763ab
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---


# Caso de uso y flujos de trabajo de plantillas de oferta

La función Plantilla de oferta permite a compradores y vendedores optimizar el proceso de oferta mediante la creación de plantillas de oferta reutilizables y personalizables.

- **Ofertas personalizables**: los compradores pueden generar ofertas vinculadas a partir de una plantilla aprobada previamente, lo que permite la personalización dentro de parámetros especificados, como cantidades y selecciones de artículos de línea.
- **Umbrales de pedido**: los vendedores pueden establecer compromisos de pedido mínimos y máximos para garantizar que los compradores cumplan los volúmenes de compra acordados.
- **Fechas de caducidad**: las plantillas pueden tener períodos de validez, lo que garantiza que los términos solo sean aplicables en un lapso de tiempo especificado.
- **Descuentos y Asignación de Precios**- Los vendedores pueden utilizar las mismas capacidades de descuento de artículos de línea, ofertas y precios de envío disponibles con las ofertas para establecer descuentos para pedidos recurrentes, lo que simplifica el proceso de negociación.
- **Seguimiento e informes**: el sistema realiza un seguimiento del número de ofertas vinculadas generadas a partir de la plantilla y de los pedidos completados correctamente para proporcionar información sobre el cumplimiento de las cuotas de pedidos acordadas.

## Caso de uso

Un comprador de una empresa puede utilizar una plantilla de presupuesto para solicitar un conjunto específico de productos durante un periodo de tiempo. El comprador configura las siguientes opciones de plantilla de oferta para que el proceso de oferta sea más eficiente, coherente y acorde con los acuerdos estratégicos de compra.

- Umbral de pedido para especificar el número mínimo y máximo de pedidos aptos para la asignación de precios negociada. Se puede utilizar para aplicar y rastrear las cuotas de pedidos especificadas en los acuerdos de contrato.

- Umbrales de cantidad (cantidades mínimas/máximas) La plantilla especifica un umbral de cantidad para establecer la cantidad mínima y máxima que se puede comprar para cada pedido, lo que garantiza que el vendedor pueda gestionar los niveles de stock de forma eficaz y, al mismo tiempo, proporciona al comprador la flexibilidad para ajustar las cantidades según sea necesario.

## Flujo de trabajo de plantilla de oferta

El comprador o el vendedor pueden iniciar las plantillas de presupuesto.

**Paso 1: Creación de la plantilla de presupuesto (Nuevo)**

- **El comprador crea la plantilla de presupuesto**

  Al revisar una plantilla de oferta existente, el comprador decide que la empresa debe enviar varios pedidos durante el año siguiente y quiere solicitar descuentos adicionales basados en la repetición de la operación. Crean una plantilla de oferta utilizando la acción *[!UICONTROL Create quote template]* en la oferta. A continuación, inicia la negociación enviando la nueva plantilla al vendedor para que la revise.

  Los compradores también pueden crear una plantilla de presupuesto directamente desde la página *[!UICONTROL My Quote Templates]** de la tienda.

- **Representante de ventas**: un representante de ventas puede crear una plantilla de presupuesto del administrador en nombre de un comprador específico de la compañía. El representante de ventas puede crear la plantilla de oferta en el administrador a partir de una oferta existente o de la cuadrícula [!UICONTROL Quote Templates] y guardarla como `draft` o enviarla al comprador para que inicie la negociación. En estado de borrador, la oferta solo es visible para el vendedor. Una vez enviado el presupuesto, el estado es `Submitted`. El vendedor no puede modificarla hasta que el comprador la devuelva.

  ![El vendedor está iniciando una cotización de comprador desde la cuadrícula de cotizaciones del administrador](./assets/quote-template-create-from-grid.png){width="700" zoomable="yes"}

**Paso 2: Revisión y negociación de presupuesto (Revisar)**

La revisión o negociación de una plantilla de oferta puede incluir el cambio de cantidades, la eliminación de artículos, la adición de comentarios de artículos de línea, la aplicación de descuentos de artículos de línea o ofertas (vendedor) y la adición de una dirección de envío (comprador).

- **El vendedor ve la solicitud y envía una respuesta**: en el administrador, el vendedor ve la plantilla de presupuesto desde la cuadrícula *[!UICONTROL Quote Templates]** o la abre desde el vínculo de la notificación por correo electrónico. En la tienda, el estado de la oferta cambia a `Pending` y el comprador no puede realizar ningún cambio. Siguiendo el mismo proceso para la [negociación de presupuesto](quote-price-negotiation.md), el vendedor responde ofreciendo descuentos en los precios y ajustando las cantidades y los artículos según sea necesario, introduce un comentario y devuelve el presupuesto al comprador. Se notifica al comprador y al vendedor por correo electrónico que el vendedor ha respondido.

- **El comprador ve la plantilla de presupuesto del vendedor y envía una respuesta**. El comprador hace clic en el vínculo de la notificación por correo electrónico para abrir la plantilla de presupuesto o abre el presupuesto desde la página _Mis plantillas de presupuesto_ del panel de cuentas. El comprador puede dejar notas al vendedor en el nivel de artículo de línea u oferta, cambiar cantidades y eliminar artículos.

El comprador y el vendedor continúan el proceso de negociación hasta que se llegue a un acuerdo o el vendedor rechace la plantilla de oferta. Si el comprador realiza cambios en la oferta (añadir o eliminar productos o cambiar cantidades de productos), la oferta debe devolverse al vendedor para que la revise.

- **El comprador agrega una dirección de envío**. Si no la tiene, el comprador debe agregar una dirección de envío a la plantilla de presupuesto. Una vez que el comprador añade la dirección, el vendedor puede proporcionar las opciones de envío y entrega. Los métodos de envío mostrados dependen de la configuración de la Tienda.

Si el comprador añade una dirección de envío, el acuerdo de negociación debe revisarse y el vendedor puede continuar con el proceso de negociación hasta que se alcance un acuerdo o hasta que el vendedor rechace la plantilla de oferta.

**Paso 3: el comprador acepta la plantilla de presupuesto**

El comprador acepta las condiciones negociadas en la plantilla. Una vez aceptada la plantilla de oferta, el comprador puede utilizarla para generar ofertas preaprobadas y vinculadas que se pueden utilizar para enviar pedidos sin necesidad de más negociación.

Las opciones de envío están bloqueadas en el cierre de compra.

### Ver una plantilla de presupuesto

1. En la columna **[!UICONTROL Actions]** de un registro, haga clic en **[!UICONTROL View]**.

1. Para responder a la solicitud del cliente, siga las instrucciones y comience el mismo proceso de [negociación de precios](quote-price-negotiation.md) que se usa para negociar las ofertas.

### Ver actividad de plantilla de presupuesto

Vea la cronología de negociación, la comunicación y otra actividad de oferta de [!UICONTROL Comments] y [!UICONTROL History Log]; la información incluye cambios de estado, actualizaciones de la información de cliente y envío, actualizaciones de artículos y precios y otra información importante.

1. Abra una plantilla de presupuesto.

1. Ver comentarios e historial de negociación de presupuesto desplazándose hasta **[!UICONTROL Negotiation]** y seleccionando **[!UICONTROL Comments]** y **[!UICONTROL History Log]**.

   ![Ver historial](./assets/quote-view-history.png){width="400"}

1. El historial también se rastrea en el nivel de elemento de línea.

   ![Ver historial de elementos de línea](./assets/quote-view-line-item-history.png){width="400"}


### Rechazar una plantilla de presupuesto

Solo se pueden rechazar las plantillas de presupuesto con un estado `In Review`.

1. En la cuadrícula *[!UICONTROL Quote Templates]*, abra la plantilla de oferta que desee rechazar.

1. En la plantilla de presupuesto, haga clic en **[!UICONTROL Decline]**.

1. Cuando se le solicite, introduzca el motivo por el que se rechazó la oferta y haga clic en **[!UICONTROL Confirm]**.
