---
title: Envío de un pedido
description: Obtenga información sobre cómo completar la información de envío de un pedido de procesamiento y consultar la información de envío y seguimiento.
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# Envío de un pedido

Un pedido que se ha pagado, pero que está a la espera de envío, tiene el `Processing` estado. El registro de envío contiene un historial detallado del proceso de satisfacción de pedidos asociado al pedido. Se pueden realizar envíos parciales hasta que se complete el pedido.

1. En el _Administrador_ barra lateral, seleccione **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. En el _[!UICONTROL Orders]_, busque el pedido que desea enviar y haga clic en para abrirlo.

1. En la esquina superior derecha, haga clic **[!UICONTROL Ship]** botón.

1. Si desea actualizar la dirección de facturación o envío, haga clic en el botón **[!UICONTROL Edit]** en la esquina superior derecha de la sección.

   Realice los cambios necesarios y haga clic en **[!UICONTROL Save Order Address]**.

1. Para que el transportista genere una etiqueta de envío, seleccione **[!UICONTROL Create Shipping Label]** y establezca las opciones:

   - Para añadir un número de seguimiento, desplácese hacia abajo hasta la _[!UICONTROL Shipping Information]_y haga clic en **[!UICONTROL Add Tracking Number]**.

   - Realice una de las siguientes acciones:

      - Seleccione el **[!UICONTROL Carrier]** e introduzca el seguimiento **[!UICONTROL Number]**.

      - Establecer **[!UICONTROL Carrier]** hasta `Custom Value`, introduzca un **[!UICONTROL Title]** para el operador de telefonía personalizado e introduzca el seguimiento **[!UICONTROL Number]**.

      - [Ver información de seguimiento](#track-the-shipment).

1. Para realizar un envío parcial, desplácese hacia abajo hasta la sección Artículos a Enviar e introduzca la **[!UICONTROL Qty to Ship]** para cada elemento.

1. Para notificar el envío a los clientes por correo electrónico, haga lo siguiente:

   - Escriba los comentarios que desee incluir en la **[!UICONTROL Shipment Comments]** cuadro.

   - Para incluir los comentarios en el correo electrónico de notificación enviado al cliente, seleccione **[!UICONTROL Append Comments]** casilla de verificación

   - Para enviarse una copia del correo electrónico de envío, seleccione la **[!UICONTROL Email Copy of Shipment]** casilla de verificación

     El estado de un correo electrónico de factura aparece junto al número de factura de la factura completada como enviada o no enviada.

1. Cuando termine, haga clic en **[!UICONTROL Submit Shipment]**.

   El estado de la solicitud cambia de `Processing` hasta `Complete`.

>[!NOTE]
>
>Si un pedido se realiza como &quot;envío en tienda&quot;, las opciones de envío no están disponibles. Clic **[!UICONTROL Notify Order is Ready for Pickup]** para almacenar en déclencheur un correo electrónico para el cliente. El estado del pedido se cambia a `Complete`.

## Ver los detalles del envío

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Busque el envío en la lista y haga clic en para abrir el registro.

1. Si desea agregar un comentario al pedido, desplácese hacia abajo hasta el _[!UICONTROL Comments History]_y escriba el comentario en el cuadro.

   - Para enviar el comentario al cliente por correo electrónico, seleccione la **[!UICONTROL Notify Customer by Email]** casilla de verificación

   - Para publicar el comentario en la cuenta del cliente, seleccione la **[!UICONTROL Visible on Frontend]** casilla de verificación

1. Haga clic **[!UICONTROL Submit Comment]**.

## Seguimiento del envío

**Método 1:** Desde la pestaña de información del pedido

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Busque el pedido de envío en la cuadrícula y haga clic en **[!UICONTROL View]**.

1. Desplácese hacia abajo hasta el _[!UICONTROL Shipping & Handling Information]_y haga clic en **[!UICONTROL Track Order]**.

   Cualquier información de seguimiento disponible aparece en una ventana emergente.

1. Cuando esté listo, haga clic en **[!UICONTROL Close Window]**.

**Método 2:** Desde la pestaña Envío de Pedidos

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Busque el envío en la lista y haga clic en para abrir el registro.

1. Haga clic **[!UICONTROL Track this Shipment]**.

   Cualquier información de seguimiento disponible aparece en una ventana emergente.

1. Cuando esté listo, haga clic en **[!UICONTROL Close Window]**.
