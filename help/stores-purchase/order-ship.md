---
title: Envío de un pedido
description: Obtenga información sobre cómo completar la información de envío de un pedido de procesamiento y consultar la información de envío y seguimiento.
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: abd125cc6e61850db55fb31dbcbd9dc38ac0fca5
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Envío de un pedido

Un pedido que se ha pagado pero que está a la espera de envío tiene el estado `Processing`. El registro de envío contiene un historial detallado del proceso de satisfacción de pedidos asociado al pedido. Se pueden realizar envíos parciales hasta que se complete el pedido.

1. En la barra lateral _Admin_, seleccione **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. En la lista _[!UICONTROL Orders]_, busque el pedido que desea enviar y haga clic en para abrirlo.

1. En la esquina superior derecha, haga clic en el botón **[!UICONTROL Ship]**.

1. Si desea actualizar la dirección de facturación o envío, haga clic en el vínculo **[!UICONTROL Edit]** en la esquina superior derecha de la sección.

   Realice los cambios necesarios y haga clic en **[!UICONTROL Save Order Address]**.

1. Para que el transportista genere una etiqueta de envío, marque la casilla **[!UICONTROL Create Shipping Label]** y defina las opciones:

   - Para agregar un número de seguimiento, desplácese hacia abajo hasta la sección _[!UICONTROL Shipping Information]_y haga clic en **[!UICONTROL Add Tracking Number]**.

   - Realice una de las siguientes acciones:

      - Seleccione **[!UICONTROL Carrier]** e introduzca el seguimiento **[!UICONTROL Number]**.

      - Establezca **[!UICONTROL Carrier]** en `Custom Value`, escriba un **[!UICONTROL Title]** para el operador personalizado e introduzca el seguimiento **[!UICONTROL Number]**.

      - [Ver información de seguimiento](#track-the-shipment).

1. Para realizar un envío parcial, desplácese hacia abajo hasta la sección Artículos para enviar e introduzca **[!UICONTROL Qty to Ship]** para cada artículo.

1. Para notificar el envío a los clientes por correo electrónico, haga lo siguiente:

   - Escriba los comentarios que desee incluir en el cuadro **[!UICONTROL Shipment Comments]**.

   - Para incluir los comentarios en el correo electrónico de notificación que se envía al cliente, active la casilla de verificación **[!UICONTROL Append Comments]**.

   - Para enviarse una copia del correo electrónico de envío, marque la casilla de verificación **[!UICONTROL Email Copy of Shipment]**.

     El estado de un correo electrónico de factura aparece junto al número de factura de la factura completada como enviada o no enviada.

1. Una vez finalizado, haga clic en **[!UICONTROL Submit Shipment]**.

   El estado del pedido cambia de `Processing` a `Complete`.

>[!NOTE]
>
>Si un pedido se realiza como &quot;envío en tienda&quot;, las opciones de envío no están disponibles. Haga clic en **[!UICONTROL Notify Order is Ready for Pickup]** para almacenar en déclencheur un correo electrónico para el cliente. El estado del pedido se cambia a `Complete`.

## Ver los detalles del envío

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Busque el envío en la lista y haga clic en para abrir el registro.

1. Si desea agregar un comentario al pedido, desplácese hacia abajo hasta la sección _[!UICONTROL Comments History]_e introduzca el comentario en el cuadro.

   - Para enviar el comentario al cliente por correo electrónico, marque la casilla de verificación **[!UICONTROL Notify Customer by Email]**.

   - Para publicar el comentario en la cuenta del cliente, marque la casilla de verificación **[!UICONTROL Visible on Frontend]**.

1. Haga clic en **[!UICONTROL Update]**.

## Seguimiento del envío

**Método 1:** de la ficha de información del pedido

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Busque el pedido de envío en la cuadrícula y haga clic en **[!UICONTROL View]**.

1. Desplácese hasta la sección _[!UICONTROL Shipping & Handling Information]_y haga clic en **[!UICONTROL Track Order]**.

   Cualquier información de seguimiento disponible aparece en una ventana emergente.

1. Cuando esté listo, haga clic en **[!UICONTROL Close Window]**.

**Método 2:** de la ficha de envío del pedido

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Busque el envío en la lista y haga clic en para abrir el registro.

1. Haga clic en **[!UICONTROL Track this Shipment]**.

   Cualquier información de seguimiento disponible aparece en una ventana emergente.

1. Cuando esté listo, haga clic en **[!UICONTROL Close Window]**.
