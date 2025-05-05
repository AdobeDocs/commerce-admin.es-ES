---
title: Alertas de productos
description: Obtenga información sobre las alertas de productos y cómo utilizarlas para notificar a los clientes sobre el estado de las existencias y los cambios de precio de los productos.
exl-id: c9f736c5-7bba-4e3e-804d-5b0fe52c8f9b
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Alertas de productos

Los clientes pueden suscribirse a dos tipos de alertas por correo electrónico: alertas de cambio de precio y alertas en stock. Para cada tipo de alerta, puede determinar si los clientes pueden suscribirse, seleccionar la plantilla de correo electrónico que se utiliza e identificar el remitente del correo electrónico.

![Regístrese para recibir una alerta sobre un producto](assets/product-alert-setting.png){width="600" zoomable="yes"}

## Alertas de cambio de precio

Cuando las alertas de cambio de precio están habilitadas, aparece un vínculo _Notificarme cuando el precio caiga_ en todas las páginas de productos. Los clientes pueden hacer clic en el vínculo para suscribirse a las alertas relacionadas con el producto. Se le pide a los huéspedes que abran una cuenta en su tienda. Cada vez que el precio cambia o el producto pasa a ser especial, todos los que se hayan suscrito a la alerta reciben una alerta por correo electrónico.

## Alertas en stock

La alerta en existencia crea un vínculo llamado _Notificarme cuando este producto esté en existencias_ para cada producto que esté agotado. Los clientes pueden hacer clic en el vínculo para suscribirse a la alerta. Cuando el producto vuelva a estar disponible, los clientes recibirán una notificación por correo electrónico avisando de que el producto está disponible. Los productos con alertas tienen una ficha _Alertas de productos_ en el panel Información del producto que enumera los clientes que se han suscrito a una alerta.

![Lista de suscripciones a alertas de productos y precios](assets/inventory-product-alerts.png){width="600" zoomable="yes"}

## Configurar alertas de productos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Haga clic para expandir la sección _[!UICONTROL Product Alerts]_&#x200B;y haga lo siguiente:

   ![Alertas de producto](assets/config-catalog-product-alerts.png){width="600" zoomable="yes"}

   - Para ofrecer alertas de cambio de precio a sus clientes, establezca **[!UICONTROL Allow Alert When Product Price Changes]** en `Yes`.

   - Establezca **[!UICONTROL Price Alert Email Template]** en la plantilla que desee usar para las notificaciones de alertas de precios.

   - Para ofrecer alertas cuando los productos sin existencias vuelvan a estar disponibles, establezca **[!UICONTROL Allow Alert When Product Comes Back in Stock]** en `Yes`.

     >[!NOTE]
     >
     >El mensaje _Notificarme cuando este producto esté disponible_ solo aparece cuando **[!UICONTROL Display Out of Stock Products]** está establecido en `Yes` (en la configuración de [!UICONTROL Catalog] > [!UICONTROL Inventory]).

   - Establezca **[!UICONTROL Stock Alert Email Template]** en la plantilla que desee usar para las alertas de existencias de productos.

   - Establece **[!UICONTROL Alert Email Sender]** en el [contacto de tienda](../getting-started/store-details.md#store-email-addresses){target="_blank"} que desea que aparezca como remitente de la alerta por correo electrónico. Obtenga más información acerca de [almacenar direcciones de correo electrónico](../configuration-reference/general/store-email-addresses.md){target="_blank"} en la guía del usuario principal.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Configurar alertas de productos y plantillas de correo electrónico

A continuación, configure, añada o modifique la plantilla de correo electrónico para la alerta de precio. Es posible que desee editar las configuraciones de alerta de precios después de crear plantillas adicionales.

Para obtener información más detallada sobre el uso de los mensajes de correo electrónico, consulte [Plantillas de mensajes](../systems/email-template-custom.md#message-templates) en la _Guía de sistemas de administración_.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Haga clic en **[!UICONTROL Add New Template]**.

1. En _Cargar plantilla predeterminada_, elija la **[!UICONTROL Template]** que desee personalizar.

   Puede elegir la plantilla de alerta incluida con la temática. O puede seleccionar las `Price Alert` o `Stock Alert` plantillas en _[!UICONTROL Magento_PriceAlert]_.

1. Haga clic en **[!UICONTROL Load Template]**.

1. Escriba un **[!UICONTROL Template Name]**.

   Puede seleccionar este nombre en la configuración de _Alertas de precio_.

1. Lea el contenido existente y realice los cambios necesarios en lo siguiente:

   | Campo | Descripción |
   | ----- | ----- |
   | [!UICONTROL Template Subject] | Este texto se muestra en la línea de asunto de un correo electrónico. |
   | [!UICONTROL Template Content] | Este texto se muestra en el contenido completo del correo electrónico enviado. |

1. Para agregar información generada a partir de los datos de [!DNL Commerce], use la opción **[!UICONTROL Insert Variable]** para usar una lista de variables disponibles.

1. Haga clic en **[!UICONTROL Save Template]**.

## Configuración de ejecución de alerta de producto

Esta configuración le permite seleccionar la frecuencia con la que [!DNL Commerce] comprueba si hay cambios que requieran que se envíen alertas. También puede seleccionar el destinatario, el remitente y la plantilla para los correos electrónicos que se envían si falla la entrega de alertas.

![Configuración de ejecución de alerta de producto](assets/config-catalog-product-alerts-run-settings.png){width="600" zoomable="yes"}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Product Alerts Run Settings]**.

1. Para determinar la frecuencia con la que se envían las alertas de productos, establezca **[!UICONTROL Frequency]** en una de las siguientes opciones:

   - `Daily`
   - `Weekly`
   - `Monthly`

1. Para determinar la hora del día en que se enviarán las alertas de productos, establezca **[!UICONTROL Start Time]** a la hora, los minutos y los segundos.

   >[!NOTE]
   >
   >El consumidor &quot;product_alert&quot; envía las alertas de producto.

1. Para **[!UICONTROL Error Email Recipient]**, escriba el correo electrónico de la persona con la que se va a contactar si se produce un error.

1. Para **[!UICONTROL Error Email Sender]**, seleccione la identidad del almacén que aparece como remitente de la notificación de error.

1. Establezca **[!UICONTROL Error Email Template]** en la plantilla de correo electrónico transaccional que se utilizará para la notificación de error.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
