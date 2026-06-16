---
title: Casos de uso y flujos de trabajo de plantillas de oferta
description: Cree una plantilla de oferta a partir de una oferta existente para agilizar la negociación de ofertas para pedidos recurrentes.
feature: B2B, Quotes
exl-id: 7d1e7a3d-6c50-416a-b490-0a083e1c06b4
TQID: https://experienceleague.adobe.com/-eAzkqLT6fhPLp-JeQH3-oap4AuIZ8MXcQx5EPb78uU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e1e0219c-f879-479f-8427-888ed2a6e9c2id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1285
ht-degree: 0%

---

# Caso de uso y flujos de trabajo de plantillas de oferta

La función Plantilla de oferta permite a compradores y vendedores optimizar el proceso de oferta mediante la creación de plantillas de oferta reutilizables y personalizables.

- **Ofertas personalizables**: los compradores pueden generar ofertas vinculadas a partir de una plantilla aprobada previamente, lo que permite la personalización dentro de parámetros especificados, como cantidades y selecciones de artículos de línea.
- **Umbrales de pedido**: los vendedores pueden establecer compromisos de pedido mínimos y máximos para garantizar que los compradores cumplan los volúmenes de compra acordados. Una vez que el comprador acepta la plantilla de oferta, el recuento de umbral de pedido aumenta cada vez que se genera una oferta vinculada. Si la oferta vinculada se cierra sin convertirse en un pedido, el pedido se resta del recuento de umbral. Cuando se alcanza el umbral de pedido máximo, caduca la plantilla de oferta.
- **Fechas de caducidad**: las plantillas pueden tener períodos de validez (*[!UICONTROL Valid Until]*), lo que garantiza que los términos solo se apliquen en un lapso de tiempo especificado. En el momento de la caducidad, la plantilla se cierra y todas las comillas vinculadas se cierran.
- **Descuentos y Asignación de Precios**- Los vendedores pueden utilizar las mismas capacidades de descuento de artículos de línea, ofertas y precios de envío disponibles con las ofertas para establecer descuentos para pedidos recurrentes, lo que simplifica el proceso de negociación.
- **Seguimiento e informes**: el sistema realiza un seguimiento del número de ofertas vinculadas generadas a partir de la plantilla y de los pedidos completados correctamente para proporcionar información sobre el cumplimiento de las cuotas de pedidos acordadas.
- **Vínculos de documentos de referencia**: tanto los compradores como los vendedores pueden agregar, editar y administrar vínculos de documentos externos (como DocuSign, Adobe Sign u otros servicios en línea) a la plantilla de presupuesto. Esto permite acceder fácilmente a los contratos y acuerdos relacionados durante el proceso de plantilla de oferta.

## Caso de uso

Un comprador de una empresa puede utilizar una plantilla de presupuesto para solicitar un conjunto específico de productos durante un periodo de tiempo. El comprador configura las siguientes opciones de plantilla de oferta para que el proceso de oferta sea más eficiente, coherente y acorde con los acuerdos estratégicos de compra.

- Umbral de pedido para especificar el número mínimo y máximo de pedidos aptos para la asignación de precios negociada. Se puede utilizar para aplicar y rastrear las cuotas de pedidos especificadas en los acuerdos de contrato.

- Umbrales de cantidad (cantidades mínimas/máximas) La plantilla especifica un umbral de cantidad para establecer la cantidad mínima y máxima que se puede comprar para cada pedido, lo que garantiza que el vendedor pueda gestionar los niveles de stock de forma eficaz y, al mismo tiempo, proporciona al comprador la flexibilidad para ajustar las cantidades según sea necesario.

- Vínculos de documento de referencia para mantener conexiones con contratos y acuerdos externos, lo que facilita el acceso a la documentación relacionada durante el proceso de oferta.

## Flujo de trabajo de plantilla de oferta

El comprador o el vendedor pueden iniciar las plantillas de presupuesto.

**Paso 1: Creación de la plantilla de presupuesto (Nuevo)**

- **El comprador crea la plantilla de presupuesto**

  Al revisar una oferta existente, el comprador decide que la empresa debe enviar varios pedidos durante el año siguiente y quiere solicitar descuentos adicionales basados en la repetición de la operación. Crean una plantilla de oferta utilizando la acción *[!UICONTROL Create quote template]* en la oferta. El comprador puede añadir enlaces de documentos de referencia a contratos o acuerdos externos utilizando el control *[!UICONTROL Add]* en la sección de documentos de referencia. A continuación, inicia la negociación enviando la plantilla de oferta al vendedor para que la revise.

  Los compradores también pueden solicitar una plantilla de presupuesto añadiendo productos que deseen comprar con regularidad al carro de compras. A continuación, solicite un presupuesto y mencione en los comentarios la frecuencia con la que desean repetir la compra.

- **Representante de ventas**: un representante de ventas puede crear una plantilla de presupuesto del administrador en nombre de un comprador específico de la compañía. El representante de ventas puede crear la plantilla de oferta en el administrador a partir de una oferta existente o de la cuadrícula [!UICONTROL Quote Templates] y guardarla como `draft` o enviarla al comprador para que inicie la negociación. En estado de borrador, la oferta solo es visible para el vendedor. Una vez enviado el presupuesto, el estado es `Submitted`. El vendedor no puede modificarla hasta que el comprador la devuelva.

  ![El vendedor está iniciando una cotización de comprador desde la cuadrícula de cotizaciones del administrador](./assets/quote-template-create-from-grid.png){width="700" zoomable="yes"}

  Cuando el vendedor crea la plantilla de oferta, la fecha de caducidad (campo [!UICONTROL Valid until]) es de 180 días de forma predeterminada. Si el comprador ha creado la plantilla, la fecha de caducidad está en blanco.  El comprador debe establecer la fecha de caducidad antes de devolver la plantilla al comprador para que la revise.

  Cuando el vendedor crea la plantilla de oferta, la fecha de caducidad (campo *[!UICONTROL Valid until]*) es de 180 días de forma predeterminada. Si el comprador ha creado la plantilla, la fecha de caducidad está en blanco.  El comprador debe establecer la fecha de caducidad antes de devolver la plantilla al comprador para que la revise.

**Paso 2: Revisión y negociación de presupuesto (Revisar)**

La revisión o negociación de una plantilla de oferta puede incluir el cambio de cantidades, la eliminación de artículos, la adición de comentarios de artículos de línea, la aplicación de descuentos de artículos de línea o ofertas (vendedor), la adición de una dirección de envío (comprador) y la administración de vínculos de documentos de referencia.

- **El vendedor ve la solicitud y envía una respuesta**: en el administrador, el vendedor ve la plantilla de presupuesto desde la cuadrícula *[!UICONTROL Quote Templates]** o la abre desde el vínculo de la notificación por correo electrónico. En la tienda, el estado de la oferta cambia a `Pending` y el comprador no puede realizar ningún cambio. Siguiendo el mismo proceso para la [negociación de presupuesto](quote-price-negotiation.md), el vendedor responde ofreciendo descuentos en los precios y ajustando las cantidades y los artículos según sea necesario, introduce un comentario y devuelve la plantilla de presupuesto al comprador. El vendedor también puede añadir, editar o eliminar vínculos a documentos de referencia durante este proceso. Se notifica al comprador y al vendedor por correo electrónico que el vendedor ha respondido.

- **El comprador ve la plantilla de presupuesto del vendedor y envía una respuesta**. El comprador hace clic en el vínculo de la notificación por correo electrónico para abrir la plantilla de presupuesto o la abre desde la página _Mis plantillas de presupuesto_ del panel de cuentas. El comprador puede dejar notas al vendedor en el nivel de artículo de línea u oferta, cambiar cantidades, eliminar artículos y gestionar enlaces de documentos de referencia.

El comprador y el vendedor continúan el proceso de negociación hasta que se llegue a un acuerdo o el vendedor rechace la plantilla de oferta. Si el comprador realiza cambios en la plantilla de oferta (adición o eliminación de productos, cambio de cantidades de productos o modificación de enlaces de documentos de referencia), debe devolvérselos al vendedor para que los revise.

- **El comprador agrega una dirección de envío**. Si no la tiene, el comprador debe agregar una dirección de envío a la plantilla de presupuesto. Una vez que el comprador añade la dirección, el vendedor puede proporcionar las opciones de envío y entrega. Los métodos de envío mostrados dependen de la configuración de la Tienda.

Si el comprador añade una dirección de envío, el acuerdo de negociación debe revisarse y el vendedor puede continuar con el proceso de negociación hasta que se alcance un acuerdo o hasta que el vendedor rechace la plantilla de oferta.

**Paso 3: el comprador acepta la plantilla de presupuesto**

El comprador acepta las condiciones negociadas en la plantilla. Una vez aceptada la plantilla de oferta, el comprador puede usarla para [generar ofertas vinculadas y preaprobadas](account-dashboard-my-quote-templates.md#generate-a-linked-quote) que se pueden usar para enviar pedidos sin necesidad de más negociación.

Las opciones de envío están bloqueadas en el cierre de compra.

Las plantillas de oferta permanecen activas hasta que caducan, se cancelan o cierran, o bien el comprador ya no es válido y ha alcanzado el umbral máximo de pedidos.

### Ver una plantilla de presupuesto

1. En la columna **[!UICONTROL Actions]** de un registro, haga clic en **[!UICONTROL View]**.

1. Para responder a la solicitud del cliente, siga las instrucciones y comience el mismo proceso de [negociación de precios](quote-price-negotiation.md) que se usa para negociar las ofertas.

### Ver actividad de plantilla de presupuesto

Vea la cronología de negociación, la comunicación y otra actividad de plantilla de oferta de [!UICONTROL Comments] y [!UICONTROL History Log]; la información incluye cambios de estado, actualizaciones de la información de cliente y envío, actualizaciones de artículos y precios y otra información importante.

1. Abra una plantilla de presupuesto.

1. Ver comentarios e historial de negociación de presupuesto desplazándose hasta **[!UICONTROL Negotiation]** y seleccionando **[!UICONTROL Comments]** y **[!UICONTROL History Log]**.

   ![Ver historial](./assets/quote-view-history.png){width="400" zoomable="yes"}

1. El historial también se rastrea en el nivel de elemento de línea.

   ![Ver historial de elementos de línea](./assets/quote-view-line-item-history.png){width="400" zoomable="yes"}

### Rechazar una plantilla de presupuesto

Solo se pueden rechazar las plantillas de presupuesto con un estado `In Review`.

1. En la cuadrícula *[!UICONTROL Quote Templates]*, abra la plantilla de oferta que desee rechazar.

1. En la plantilla de presupuesto, haga clic en **[!UICONTROL Decline]**.

1. Cuando se le solicite, introduzca el motivo por el que se rechazó la oferta y haga clic en **[!UICONTROL Confirm]**.
