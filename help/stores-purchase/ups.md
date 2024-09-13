---
title: United Parcel Service (UPS)
description: Aprenda a configurar UPS como transportista para su tienda.
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: 59daaca469ca1bf21c420ce8520efea6c54166fa
workflow-type: tm+mt
source-wordcount: '938'
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

1. En la _barra lateral de administración_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel de la izquierda, debajo de **[!UICONTROL Sales]**, elija **[!UICONTROL Delivery Methods]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL UPS]**.

1. Establezca **[!UICONTROL Enabled for Checkout]** en `Yes`.

1. Para una cuenta REST de UPS (predeterminada), haga lo siguiente:

   - Escriba sus credenciales de UPS: el identificador de cliente de UPS es **[!UICONTROL User ID]**, el secreto de cliente de UPS es **[!UICONTROL Password]**

   - Establezca **[!UICONTROL Mode]** en `Live` para enviar datos al sistema de envío de UPS a través de una conexión segura. (El modo de desarrollo no envía datos a través de una conexión segura).

   - Compruebe **[!UICONTROL Gateway URL]** que es necesario para enviar solicitudes. Use una dirección URL de zona protegida (`https://wwwcie.ups.com/`) para el modo de prueba y una dirección URL de producción para solicitudes activas (`https://onlinetools.ups.com`). Asegúrese de utilizar los puntos de conexión respectivos para cada solicitud con el host determinado.

   - Compruebe **[!UICONTROL Tracking URL]** que es necesario para obtener información de seguimiento. Use una dirección URL de zona protegida (`https://wwwcie.ups.com/`) para el modo de prueba y una dirección URL de producción para solicitudes activas (`https://onlinetools.ups.com`). Asegúrese de utilizar los puntos de conexión respectivos para cada solicitud con el host determinado.

   - Establezca **[!UICONTROL Origin of the Shipment]** en la región donde se origina el envío.

   - Si tiene tarifas especiales con UPS, establezca **[!UICONTROL Enable Negotiated Rates]** en `Yes` e ingrese el **[!UICONTROL Shipper Number]** de seis dígitos que UPS le asignó.

   - Establezca **[!UICONTROL Live Account]** en una de las siguientes opciones:

      - `Yes`: ejecuta UPS en modo de producción y ofrece UPS como método de envío a sus clientes. Asegúrese de utilizar los puntos de conexión correctos en URL de puerta de enlace y URL de seguimiento.
      - `No` - Ejecuta UPS en modo de prueba. Asegúrese de utilizar los puntos de conexión correctos en URL de puerta de enlace y URL de seguimiento.

   >[!NOTE]
   >
   >El tipo estándar de United Parcel Service está programado para su desuso. Para las nuevas configuraciones, use el tipo predeterminado `United Parcel Service REST`. El tipo REST también es necesario para generar [etiquetas de envío](shipping-labels.md).<br/>
   >Para la versión 2.4.7, **[!UICONTROL UPS Type]** se ha eliminado porque los tipos `UPS` y `UPS XML` están programados para su desuso y `UPS REST` es el predeterminado. Las API de United Parcel Service (UPS) utilizadas por la integración nativa de Adobe Commerce están en desuso temporalmente porque actualmente no es compatible con el modelo de seguridad OAuth 2.0.

   >[!IMPORTANT]
   >
   >UPS está suspendiendo la compatibilidad con HTTP, que se utiliza en el valor predeterminado actual (valor del sistema). Desactive la casilla de verificación **[!UICONTROL Use system value]** y modifique la dirección URL para utilizar HTTPS. Ejemplo: `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. Para **[!UICONTROL Title]**, escriba el nombre de esta opción de envío tal como desea que aparezca durante el cierre de compra.

   De manera predeterminada, este campo está establecido en `United Parcel Service`.

   ![Habilitar UPS](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## Paso 3: completar la descripción del contenedor

1. Establezca **[!UICONTROL Packages Request Type]** en una de las siguientes opciones:

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. Para **[!UICONTROL Container]**, especifique el tipo de paquete típico que se usa para el envío:

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

1. Establezca **[!UICONTROL Weight Unit]** en el sistema que use para medir el peso del producto.

   El sistema de pesos soportado por UPS varía según el país. En caso de duda, pregunte a UPS qué sistema de peso debe utilizar. Las opciones incluyen:

   - `LBS`
   - `KGS`

1. Establezca **[!UICONTROL Destination Type]** en una de las siguientes opciones:

   - `Residential`: la mayoría de los envíos son de empresa a consumidor (B2C).
   - `Commercial`: la mayoría de sus envíos son de empresa a empresa (B2B).

1. Escriba el **[!UICONTROL Maximum Package Weight]** permitido por el operador.

1. Establezca **[!UICONTROL Pickup Method]** en una de las siguientes opciones:

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. Escriba el **[!UICONTROL Minimum Package Weight]** permitido por el operador.

   ![Descripción del contenedor](./assets/ups2.png){width="600" zoomable="yes"}

## Paso 4: Configurar las tarifas de manipulación

La tarifa de manejo es opcional y aparece como un cargo adicional que se agrega al costo de envío de UPS. Si desea incluir una tarifa de manejo, haga lo siguiente:

1. Establezca **[!UICONTROL Calculate Handling Fee]** en uno de los siguientes métodos:

   - `Fixed`
   - `Percent`

1. Para determinar cómo se aplica la tarifa de administración, establezca **[!UICONTROL Handling Applied]** en una de las siguientes opciones:

   - `Per Order`
   - `Per Package`

1. Escriba el importe de **[!UICONTROL Handling Fee]** que se va a cargar.

   Para introducir un porcentaje, utilice el formato decimal. Por ejemplo, escriba `0.25` para 25%.

   ![Cargo por manejo](./assets/ups3.png){width="600" zoomable="yes"}

## Paso 5: Especifique los métodos permitidos y los países aplicables

1. Para **[!UICONTROL Allowed Methods]**, elija cada método de envío de UPS que estará disponible para sus clientes.

   Los métodos aparecen en UPS durante el cierre de compra. Para seleccionar varios métodos, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

1. Si desea proporcionar una opción de [envío gratuito](shipping-free.md) a través de UPS, establezca las opciones de envío gratuito:

   - Establezca **[!UICONTROL Free Method]** en el método que desee utilizar para el envío gratuito. Si no desea ofrecer el envío gratuito a través de UPS, elija `None`.

   - Para requerir una cantidad de pedido mínima que permita un envío gratuito con UPS, establezca **[!UICONTROL Enable Free Shipping Threshold]** en `Enable`. A continuación, escriba el valor mínimo en **[!UICONTROL Free Shipping Amount Threshold]**.

1. Si es necesario, cambie **[!UICONTROL Displayed Error Message]**.

   Este cuadro de texto está preestablecido con un mensaje predeterminado, pero puede escribir un mensaje diferente que desee que aparezca si UPS deja de estar disponible.

   ![Métodos permitidos](./assets/ups4.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Ship to Applicable Countries]** en una de las siguientes opciones:

   - `All Allowed Countries`: los clientes de todos los [países](../getting-started/store-details.md#country-options) especificados en la configuración de su tienda pueden usar este método de entrega.
   - `Specific Countries` - Al elegir esta opción, aparece la lista _Enviar a países específicos_. Seleccione cada país de la lista donde se pueda utilizar este método de entrega.

1. Establezca **[!UICONTROL Show Method if Not Applicable]** en una de las siguientes opciones:

   - `Yes`: enumera todos los métodos de envío de UPS disponibles durante el cierre de compra, incluidos los métodos que no se aplican al envío.
   - `No`: enumera únicamente los métodos de envío de UPS aplicables al envío.

   ![Países Aplicables](./assets/ups5.png){width="600" zoomable="yes"}

1. Para crear un archivo de registro con los detalles de los envíos de UPS realizados desde su tienda, establezca **[!UICONTROL Debug]** en `Yes`.

1. Para **[!UICONTROL Sort Order]**, escriba un número para determinar la secuencia en la que aparece UPS cuando se enumera con otros métodos de envío durante la desprotección.

   `0` = primero, `1` = segundo, `2` = tercero, etc.

1. Haga clic en **[!UICONTROL Save Config]**.

## Paso 6: Configurar la dirección de origen de envío

1. Asegúrate de que tu [Información de la tienda](../getting-started/store-details.md#store-information) esté completa.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y seleccione **[!UICONTROL Shipping Settings]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Origin]** en la página y configure la dirección de origen de envío.

   ![Configuración de ventas - opciones de dirección de origen de envío](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Commerce no declara el precio de pedido completo a UPS al calcular los gastos de envío. Este comportamiento no se puede cambiar.
