---
title: United Parcel Service (UPS)
description: Aprenda a configurar UPS como transportista para su tienda.
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# United Parcel Service (UPS)

United Parcel Service (UPS) ofrece servicios de envío nacionales e internacionales por tierra y aire a más de 220 países.

{{ups-api}}

>[!NOTE]
>
>UPS puede usar [peso dimensional](carriers.md#dimensional-weight) para determinar algunas tarifas de envío. Sin embargo, Adobe Commerce solo admite el cálculo de los gastos de envío en función del peso.

## Paso 1: Abrir una cuenta de envío de UPS

Para ofrecer este método de envío a sus clientes, primero debe abrir una cuenta con UPS.

## Paso 2: Habilita UPS para tu tienda

1. En el _Barra lateral del administrador_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel de la izquierda, debajo de **[!UICONTROL Sales]**, elija **[!UICONTROL Delivery Methods]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL UPS]** sección.

1. Establecer **[!UICONTROL Enabled for Checkout]** hasta `Yes`.

1. Para una cuenta REST de UPS (predeterminada), haga lo siguiente:

   - Introduzca sus credenciales de UPS: UPS ClientID como **[!UICONTROL User ID]**, secreto de cliente de UPS como **[!UICONTROL Password]**

   - Establecer **[!UICONTROL Mode]** hasta `Live` para enviar datos al sistema de envío de UPS a través de una conexión segura. (El modo de desarrollo no envía datos a través de una conexión segura).

   - Compruebe el **[!UICONTROL Gateway URL]** que es necesario para enviar solicitudes. Utilice una URL de zona protegida para el modo de prueba y una URL de producción para las solicitudes activas.

   - Compruebe el **[!UICONTROL Tracking URL]** que es necesario para obtener información de seguimiento. Utilice una URL de zona protegida para el modo de prueba y una URL de producción para las solicitudes activas.

   - Establecer **[!UICONTROL Origin of the Shipment]** a la región de origen del envío.

   - Si tiene tarifas especiales con UPS, establezca **[!UICONTROL Enable Negotiated Rates]** hasta `Yes` e introduzca los seis dígitos **[!UICONTROL Shipper Number]** asignado a usted por UPS.

   - Establecer **[!UICONTROL Live Account]** a uno de los siguientes:

      - `Yes` - Ejecuta UPS en modo de producción y ofrece UPS como método de envío a sus clientes.
      - `No` - Ejecuta UPS en modo de prueba.

   >[!NOTE]
   >
   >El tipo estándar de United Parcel Service está programado para su desuso. Para las nuevas configuraciones, utilice el valor predeterminado `United Parcel Service REST` escriba. El tipo de REST también es necesario para generar [etiquetas de envío](shipping-labels.md).<br/>
   >Para la versión 2.4.7, **[!UICONTROL UPS Type]**  se ha eliminado porque `UPS` y `UPS XML` Los tipos de están programados para su desaprobación y `UPS REST` es el valor predeterminado. Las API de United Parcel Service (UPS) utilizadas por la integración nativa de Adobe Commerce están en desuso temporalmente porque actualmente no es compatible con el modelo de seguridad OAuth 2.0.

   >[!IMPORTANT]
   >
   >UPS está suspendiendo la compatibilidad con HTTP, que se utiliza en el valor predeterminado actual (valor del sistema). Borre la **[!UICONTROL Use system value]** y modifique la dirección URL para utilizar HTTPS. Ejemplo: `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. Para **[!UICONTROL Title]**, introduzca el nombre de esta opción de envío tal como desea que aparezca durante el cierre de compra.

   De forma predeterminada, este campo está establecido en `United Parcel Service`.

   ![Activar UPS](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## Paso 3: completar la descripción del contenedor

1. Establecer **[!UICONTROL Packages Request Type]** a uno de los siguientes:

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. Para **[!UICONTROL Container]**, especifique el tipo de paquete típico que se utiliza para el envío:

   - `Customer Packaging`
   - `UPS Letter Envelope`
   - `Customer Supplied Package`
   - `UPS Tube`
   - `PAK`
   - `UPS Express Box`
   - `UPS Worldwide 25 kilo`
   - `UPS Worldwide 10 kilo`
   - `Pallet`
   - `Small Express Box`
   - `Medium Express Box`
   - `Large Express Box`

1. Establecer **[!UICONTROL Weight Unit]** al sistema que utiliza para medir el peso del producto.

   El sistema de pesos soportado por UPS varía según el país. En caso de duda, pregunte a UPS qué sistema de peso debe utilizar. Las opciones incluyen:

   - `LBS`
   - `KGS`

1. Establecer **[!UICONTROL Destination Type]** a uno de los siguientes:

   - `Residential` - La mayoría de sus envíos son de empresa a consumidor (B2C).
   - `Commercial` - La mayoría de sus envíos son de empresa a empresa (B2B).

1. Introduzca el **[!UICONTROL Maximum Package Weight]** permitido por el transportista.

1. Establecer **[!UICONTROL Pickup Method]** a uno de los siguientes:

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. Introduzca el **[!UICONTROL Minimum Package Weight]** permitido por el transportista.

   ![Descripción del contenedor](./assets/ups2.png){width="600" zoomable="yes"}

## Paso 4: Configurar las tarifas de manipulación

La tarifa de manejo es opcional y aparece como un cargo adicional que se agrega al costo de envío de UPS. Si desea incluir una tarifa de manejo, haga lo siguiente:

1. Establecer **[!UICONTROL Calculate Handling Fee]** a uno de los siguientes métodos:

   - `Fixed`
   - `Percent`

1. Para determinar cómo se aplica la tarifa de manipulación, establezca **[!UICONTROL Handling Applied]** a uno de los siguientes:

   - `Per Order`
   - `Per Package`

1. Introduzca el importe de la **[!UICONTROL Handling Fee]** que se cobran.

   Para introducir un porcentaje, utilice el formato decimal. Por ejemplo, introduzca `0.25` por 25%.

   ![Tarifa de manipulación](./assets/ups3.png){width="600" zoomable="yes"}

## Paso 5: Especifique los métodos permitidos y los países aplicables

1. Para **[!UICONTROL Allowed Methods]**, elija cada método de envío de UPS disponible para sus clientes.

   Los métodos aparecen en UPS durante el cierre de compra. Para seleccionar varios métodos, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

1. Si desea proporcionar un [Envío gratuito](shipping-free.md) a través de UPS, establezca las opciones de envío gratuito:

   - Establecer **[!UICONTROL Free Method]** al método que desea utilizar para el envío gratuito. Si no desea ofrecer el envío gratuito a través de UPS, elija `None`.

   - Para requerir una cantidad mínima de pedido que califique un pedido para el envío gratuito con UPS, establezca **[!UICONTROL Enable Free Shipping Threshold]** hasta `Enable`. A continuación, introduzca el valor mínimo en **[!UICONTROL Free Shipping Amount Threshold]**.

1. Si es necesario, cambie el **[!UICONTROL Displayed Error Message]**.

   Este cuadro de texto está preestablecido con un mensaje predeterminado, pero puede escribir un mensaje diferente que desee que aparezca si UPS deja de estar disponible.

   ![Métodos permitidos](./assets/ups4.png){width="600" zoomable="yes"}

1. Establecer **[!UICONTROL Ship to Applicable Countries]** a uno de los siguientes:

   - `All Allowed Countries` - Clientes de todos [países](../getting-started/store-details.md#country-options) especificado en la configuración de la tienda puede utilizar este método de envío.
   - `Specific Countries` - Al elegir esta opción, la variable _Enviar a países específicos_ aparece una lista. Seleccione cada país de la lista donde se pueda utilizar este método de entrega.

1. Establecer **[!UICONTROL Show Method if Not Applicable]** a uno de los siguientes:

   - `Yes` - Enumera todos los métodos de envío de UPS disponibles durante el cierre de compra, incluidos los métodos que no se aplican al envío.
   - `No` - Muestra sólo los métodos de envío de UPS aplicables al envío.

   ![Países aplicables](./assets/ups5.png){width="600" zoomable="yes"}

1. Para crear un archivo de registro con los detalles de los envíos de UPS realizados desde su tienda, establezca **[!UICONTROL Debug]** hasta `Yes`.

1. Para **[!UICONTROL Sort Order]**, introduzca un número para determinar la secuencia en la que aparece UPS cuando se enumera con otros métodos de envío durante la comprobación.

   `0` = primero, `1` = segundo, `2` = tercero, etc.

1. Clic **[!UICONTROL Save Config]**.

## Paso 6: Configurar la dirección de origen de envío

1. Asegúrese de que su [Información de tienda](../getting-started/store-details.md#store-information) se ha completado.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y seleccione **[!UICONTROL Shipping Settings]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Origin]** en la página y configure la dirección de origen de envío.

   ![Configuración de ventas - opciones de dirección de origen de envío](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save Config]**.

>[!NOTE]
>
>El comercio no declara el precio de pedido completo a UPS al calcular los gastos de envío. Este comportamiento no se puede cambiar.
