---
title: '[!UICONTROL My Quote Templates]'
description: Obtenga información acerca de la experiencia del cliente con las plantillas de presupuesto, que está disponible en el panel de cuentas de tienda.
feature: B2B, Companies, Quotes
exl-id: 3d95a44e-b874-442b-af96-0dc6b589d0f7
source-git-commit: 71b9326aa5a8c3d7656b3c0f166cf25291b2abba
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# [!UICONTROL My Quote Templates]

Si las ofertas están habilitadas, la sección _[!UICONTROL My Quotes Template]_del panel de control de cuentas del cliente enumera todas las plantillas de ofertas asociadas a la cuenta del cliente. Según sus permisos, solo los compradores que realizan compras en nombre de una empresa pueden solicitar una plantilla de presupuesto y negociar los precios de presupuesto y las condiciones de los pedidos recurrentes.

![Mis plantillas de presupuesto](./assets/account-dashboard-quote-templates-list.png){width="700" zoomable="yes"}

La lista de plantillas de oferta organiza las plantillas por estado.

- **[!UICONTROL Active Quote Templates]** enumera las plantillas que se han negociado y aprobado para su uso. La información incluye el total mínimo de la oferta y los pedidos realizados si estas opciones se configuraron durante el proceso de negociación. Los compradores pueden generar una oferta vinculada a partir de la plantilla para enviar un pedido basado en las condiciones de la oferta.

- **[!UICONTROL In Review]** enumera las plantillas en el proceso de negociación que muestran el estado actual y proporcionan un vínculo para abrir la plantilla.

- **[!UICONTROL Inactive]** enumera las plantillas que han caducado, que se han cancelado o que ya no son válidas porque un comprador ha consumido el número de pedidos confirmados permitidos.

Para el comprador, la página *[!UICONTROL My Quotes Templates]* es el punto focal de todas las comunicaciones entre el comprador y el vendedor durante el proceso de negociación.

Un comprador que acepte las condiciones negociadas ofrecidas por el vendedor puede aceptar la plantilla y, a continuación, utilizarla para generar presupuestos vinculados previamente aprobados que se pueden utilizar para realizar pedidos.

- Acciones relacionadas con la gestión de la plantilla de oferta:

   - Cancelar una plantilla
   - Enviar al vendedor para que lo revise
   - Aceptar la plantilla de presupuesto
   - Cambiar la fecha de caducidad de la plantilla de oferta
   - Añadir una dirección de envío

- Acciones para actualizar detalles de plantilla de oferta durante el proceso de negociación:

   - Revisa el precio del artículo y las actualizaciones.
   - Si se han configurado umbrales de cantidad en la plantilla de oferta, ajuste los valores mínimo y máximo.
   - Rastree el proceso de negociación de las secciones [!UICONTROL Comments] y [!UICONTROL History].
   - En el caso de las plantillas que aún se están revisando, el comprador puede modificar la plantilla de oferta eliminando artículos.
   - Comunicarse y negociar con el vendedor añadiendo notas en el nivel de artículo de línea y presupuesto.

  Después de realizar los cambios, el comprador devuelve la plantilla al vendedor para que la revise.

- Acciones generales durante la negociación:

   - Enviar plantilla de presupuesto al vendedor para que la revise
   - Aceptar la plantilla de presupuesto
   - Cancelar para finalizar la negociación y cerrar la oferta

El siguiente ejemplo muestra una plantilla de oferta que el comprador ha actualizado y enviado de vuelta al vendedor para que la revise.

![Vista del comprador de la plantilla de presupuesto](./assets/account-dashboard-my-quote-template-detailed.png){width="700" zoomable="yes"}

Las plantillas con el estado `Submitted` se bloquearán hasta que el vendedor revise, actualice la plantilla y la devuelva al comprador.

## Creación de una plantilla de presupuesto

El comprador puede iniciar el proceso de negociación de la plantilla de oferta utilizando cualquiera de los siguientes métodos:

- Cree una plantilla a partir de una oferta existente haciendo clic en la acción **[!UICONTROL Create quote template]**.

- Envíe una solicitud de presupuesto desde la tienda y añada comentarios pidiendo al representante de ventas que cree una plantilla de presupuesto a partir de la solicitud de presupuesto.

## Ver una plantilla de presupuesto

1. El comprador inicia sesión en su cuenta.

1. En el panel izquierdo, elija **[!UICONTROL My Quote Templates]**.

1. Busca la plantilla de oferta en la lista y hace clic en **[!UICONTROL View]** en la columna _[!UICONTROL Action]_.

## Añadir una dirección de envío

El comprador no puede aceptar una plantilla de presupuesto hasta que tenga una dirección de envío.

1. El comprador inicia sesión en su cuenta.

1. En el panel izquierdo, elija **[!UICONTROL My Quote Templates]**.

1. Selecciona la plantilla de oferta deseada.

1. En la sección **[!UICONTROL Shipping Information]**, hace clic en **[!UICONTROL Add New Address]**.

1. Completa los detalles de la nueva dirección.

1. Clics **[!UICONTROL Save Address]**.

Cuando el comprador añade la dirección, vuelve a enviar la plantilla al vendedor para que la revise. El vendedor proporciona las opciones de envío y entrega. Estas actualizaciones pueden afectar a los precios de las ofertas negociadas. Las opciones de envío están bloqueadas en el cierre de compra.

## Generación de una oferta vinculada

Una vez que el comprador acepta una plantilla de presupuesto, puede utilizarla para generar presupuestos preaprobados y vinculados a partir de *[!UICONTROL My Quote Templates dashboard]* o de la plantilla de presupuesto mediante la acción **[!UICONTROL Generate a quote]**.

La oferta vinculada incluye una notificación que indica que está aprobada y lista para el cierre de compra. También proporciona un vínculo a la plantilla de oferta en la información del encabezado.

![Cita vinculada generada a partir de una plantilla de cotización](./assets/quote-templates-linked-quote.png){width="700" zoomable="yes"}

Si la plantilla de oferta se configuró con un umbral de pedido, el recuento se incrementa cuando se genera la oferta vinculada.

Los compradores pueden completar las siguientes acciones desde una oferta vinculada:

- Si la oferta está configurada con umbrales de cantidad, ajuste la cantidad del pedido para los artículos de línea.
- Continúe con el cierre de compra para enviar una solicitud.
- Elimine o imprima la oferta.
- Abra la plantilla de oferta utilizada para generar la oferta.

## Cancelar una plantilla de presupuesto

En la página de plantilla de oferta, haga clic en **[!UICONTROL Cancel Quote Template]**.

La plantilla de presupuesto se cancela y el estado de la oferta cambia a `Closed`. La oferta cerrada permanece en su lista de *[!UICONTROL Inactive]* comillas y permanece en la lista _[!UICONTROL Quote Templates]_de la administración.
