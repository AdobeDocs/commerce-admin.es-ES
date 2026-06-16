---
title: Envío de un pedido
description: Obtenga información sobre cómo completar la información de envío de un pedido de procesamiento y consultar la información de envío y seguimiento.
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
TQID: https://experienceleague.adobe.com/w1MPvqsRVfsRwEcRB5uClGM3vnwAda3sOtkZzuLBKAA
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 453
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
