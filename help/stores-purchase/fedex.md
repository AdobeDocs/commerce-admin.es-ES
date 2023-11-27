---
title: FedEx
description: Aprenda a configurar FedEx como transportista para su tienda.
exl-id: 75bb3ed1-3ae9-418a-be90-888046b28a7b
feature: Shipping/Delivery
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---

# FedEx

FedEx es una de las compañías de servicios de transporte marítimo más grandes del mundo, que proporciona servicios de transporte aéreo, de carga y terrestre con varios niveles de prioridades.

![Opciones de envío de FedEx al pagar](./assets/storefront-checkout-shipping-fedex.png){width="700" zoomable="yes"}

>[!NOTE]
>
>FedEx puede utilizar [peso dimensional](carriers.md#dimensional-weight) para determinar algunas tarifas de envío. Sin embargo, Adobe Commerce y Magento Open Source solo admiten el cálculo de los costes de envío en función del peso.

## Paso 1: Regístrese para la producción de servicios web de FedEx

A [Cuenta de comerciante de FedEx][1] Se requiere un registro para el acceso de producción a los servicios web de FedEx. Después de crear una cuenta de FedEx, lea la página de información de la cuenta de producción y haga clic en _Obtener clave de producción_ en la parte inferior de la página para registrarse y obtener una clave.

>[!NOTE]
>
>Asegúrese de copiar o escribir la clave de autenticación. Es necesario configurar FedEx en la configuración de envío de Commerce.

## Paso 2: Habilitar FedEx para su tienda

{{beta2-updates}}

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Delivery Methods]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL FedEx]** sección.

1. Establecer **[!UICONTROL Enabled for Checkout]** hasta `Yes`.

1. Para **[!UICONTROL Title]**, introduzca un título que identifique el método de envío de FedEx durante el cierre de compra.

1. Introduzca la siguiente información de su cuenta de FedEx:

   - **[!UICONTROL Account ID]**
   - **[!UICONTROL Meter Number]**
   - **[!UICONTROL Key]**
   - **[!UICONTROL Password]**

1. Si ha configurado una zona protegida de FedEx y desea trabajar en el entorno de prueba, establezca **[!UICONTROL Sandbox Mode]** hasta `Yes`.

   >[!NOTE]
   >
   >Recuerde establecer el modo de espacio aislado en `No` cuando esté listo para ofrecer FedEx como método de envío a sus clientes.

   ![Configuración de cuenta de FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

## Paso 3: Descripción del paquete y gastos de manipulación

1. Seleccione el **[!UICONTROL Packages Request Type]** a la opción que mejor describe sus preferencias al dividir un pedido en varios envíos:

   - `Divide to equal weight (one request)`
   - `Use origin weight (few requests)`

1. Seleccione el tipo de **[!UICONTROL Packaging]** normalmente se utiliza para enviar productos desde su tienda.

1. Establecer **[!UICONTROL Dropoff]** al método de recogida utilizado para la entrega.

   - `Regular Pickup` - Si tiene un gran volumen de envíos, puede ser rentable hacer arreglos con FedEx para recoger regularmente.

   - `Request Courier` - Debe llamar y solicitar a un mensajero de FedEx que recoja los envíos.

   - `Drop Box` - Debe entregar los envíos en la caja de entrega de FedEx cercana.

   - `Business Service Center` - Debe entregar los envíos en su centro de servicio comercial local de FedEx.

   - `Station` - Debe entregar los envíos en su estación local de FedEx.

1. Establecer **[!UICONTROL Weight Unit]** a la unidad de medida que se utiliza en su configuración regional.

   - `Pounds`
   - `Kilograms`

1. Introduzca el **[!UICONTROL Maximum Package Weight]** permitido para envíos de FedEx.

   El peso máximo predeterminado de FedEx es de 150 libras. Consulte a su transportista para obtener más información. Se recomienda el valor predeterminado, a menos que haya realizado acuerdos especiales con FedEx. Consulte [Peso dimensional](carriers.md#dimensional-weight) para obtener más información.

   ![Configuración del paquete de FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

1. Configure las opciones de gastos de manipulación según sus necesidades.

   La tarifa de manipulación es opcional y no es visible durante el cierre de compra. Si desea incluir una tarifa de manejo, haga lo siguiente:

   - Establecer **[!UICONTROL Calculate Handling Fee]**:

      - `Fixed Fee`
      - `Percentage`

   - Para **[!UICONTROL Handling Applied]**, elija uno de los siguientes métodos para administrar las tarifas de manipulación:

      - `Per Order`
      - `Per Package`

   - Introduzca el **[!UICONTROL Handling Fee]** como a `fixed` importe o `percentage`, según el método de cálculo.

1. Establecer **[!UICONTROL Residential Delivery]** a una de las siguientes, en función de si vende de empresa a consumidor (B2C) o de empresa a empresa (B2B).

   - `Yes` - Para entregas residenciales B2C.
   - `No` - Para entregas residenciales B2B.

   ![Configuración de tarifas de manejo de FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

## Paso 4: Métodos permitidos y países aplicables

1. Establecer **[!UICONTROL Allowed Methods]** a cada método de envío que desee ofrecer.

   Al elegir los métodos, considere su cuenta de FedEx, la frecuencia y el tamaño de sus envíos y si permite envíos internacionales. Puede ofrecer tantos métodos como desee, o tan pocos como desee, como:

   - Primera prioridad de Europa
   - Opciones de día de entrega: 1 día de carga, 2 días de carga, 2 días, 2 días a la mañana, 3 días de carga
   - Opciones nacionales: Express Saver, Ground, First, Overnight, Home Delivery, Standard Overnight
   - Opciones internacionales-Economía internacional, Economía internacional, Flete, Internacional primero, Internacional terrestre, Internacional, Prioridad internacional
   - Opciones de prioridad: flete, prioridad a la vista
   - Smart Post-If que ofrece el método Smart Post (introduzca la variable **ID de concentrador**)
   - Opciones de flete-Flete, Flete nacional

1. Si desea proporcionar un [Envío gratuito](shipping-free.md) a través de FedEx, establezca las opciones de envío gratuitas.

   - Establecer **[!UICONTROL Free Method]** al método que desea utilizar para el envío gratuito. Si no desea ofrecer envío gratuito a través de FedEx, elija `None`.

   - Para requerir una cantidad mínima de pedido que califique un pedido para el envío gratuito con FedEx, establezca **[!UICONTROL Enable Free Shipping Threshold]** hasta `Enable`. A continuación, introduzca el valor mínimo en **[!UICONTROL Free Shipping Amount Threshold]**.

   Esta configuración es similar a la del método de envío gratuito estándar, pero aparece en la sección FedEx durante el cierre de compra, por lo que los clientes saben qué método se utiliza para su pedido.

1. Si es necesario, cambie el **[!UICONTROL Displayed Error Message]**.

   Este cuadro de texto está preestablecido con un mensaje predeterminado, pero puede escribir un mensaje diferente que desee que aparezca si FedEx deja de estar disponible.

   ![Métodos de envío permitidos por FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

1. Establecer **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - Clientes de todos [países](../getting-started/store-details.md#country-options) especificado en la configuración de la tienda puede utilizar este método de envío.

   - `Specific Countries` - Al elegir esta opción, la variable _Enviar a países específicos_ aparece una lista. Seleccione cada país de la lista donde se pueda utilizar este método de entrega.

1. Si desea mantener un registro de todas las comunicaciones entre su tienda y el sistema de FedEx, establezca **[!UICONTROL Debug]** hasta `Yes`.

1. Establecer **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes` - Muestra todos los métodos de envío de FedEx a los clientes, independientemente de su disponibilidad.
   - `No` - Muestra únicamente los métodos de envío de FedEx que se aplican al pedido.

1. Para **[!UICONTROL Sort Order]**, introduzca un número para determinar la secuencia en la que aparece FedEx cuando aparece junto con otros métodos de envío durante el cierre de compra.

   `0` = primero, `1` = segundo, `2` = tercero, etc.

1. Haga clic **[!UICONTROL Save Config]**.

   ![Países aplicables de FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Commerce siempre declara el precio completo del pedido a FedEx cuando calcula los gastos de envío. Este comportamiento no se puede cambiar.

[1]: https://www.fedex.com/login/web/jsp/contactInfo1.jsp
