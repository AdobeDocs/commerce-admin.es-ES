---
title: DHL
description: Aprenda a configurar DHL como transportista para su tienda.
exl-id: 765e5f90-3e93-43cf-a5bc-6132e00b506c
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# DHL

DHL ofrece servicios internacionales integrados y soluciones personalizadas y centradas en el cliente para gestionar y transportar cartas, bienes e información.

## Paso 1: Habilitar DHL

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Delivery Methods]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL DHL]**.

   >[!NOTE]
   >
   >Si es necesario, primero desmarque la casilla de verificación **[!UICONTROL Use system value]** para cambiar la siguiente configuración como se describe.

1. Establezca **[!UICONTROL Enabled for Checkout]** en `Yes`.

1. Normalmente, puede aceptar el valor predeterminado **[!UICONTROL Gateway URL]**.

   Si DHL le ha proporcionado una URL alternativa, introduzca ese valor en este campo.

1. Utilice las credenciales proporcionadas por DHL para completar los siguientes campos:

   - **[!UICONTROL Access ID]**
   - **[!UICONTROL Password]**
   - **[!UICONTROL Account Number]**

![Configuración de cuenta DHL](../configuration-reference/sales/assets/delivery-methods-dhl-account-settings.png){width="600" zoomable="yes"}

## Paso 2; Especifique la descripción del paquete y la tarifa de manipulación

1. En la lista **[!UICONTROL Content Type]**, seleccione la opción que mejor describa el tipo de paquete que envía:

   - `Documents`
   - `Non documents`

1. Configure las opciones de gastos de manipulación según sus necesidades.

   La tarifa de manipulación es opcional y aparece como un cargo adicional que se añade al coste de envío de DHL. Si desea incluir una tarifa de manejo, haga lo siguiente:

   - Para **[!UICONTROL Calculate Handling Fee]**, seleccione el método que desee usar para calcular las tarifas de manipulación:

      - `Fixed`
      - `Percentage`

   - Para **[!UICONTROL Handling Applied]**, seleccione cómo desea que se apliquen las tarifas de manipulación:

      - `Per Order`
      - `Per Package`

   - Para **[!UICONTROL Handling Fee]**, escriba la cantidad que se va a cargar, según el método que haya elegido para calcular la cantidad.

     Por ejemplo, si el cargo se basa en una tarifa fija, introduzca la cantidad como decimal; por ejemplo, `4.90`. Sin embargo, si la tarifa de manipulación se basa en un porcentaje del pedido, introduzca la cantidad como porcentaje. Por ejemplo, si está cargando el seis por ciento del pedido, introduzca el valor como `.06`.

   - Para permitir que se desglose el peso total del pedido para garantizar un cálculo preciso de los gastos de envío, establezca **[!UICONTROL Divide Order Weight]** en `Yes`.

   - Establezca **[!UICONTROL Weight Unit]** del paquete en una de las siguientes opciones:

      - `Pounds`
      - `Kilograms`

   - Establezca **[!UICONTROL Size]** de un paquete típico en uno de los siguientes:

      - `Regular`
      - `Specific`

     Si elige `Specific`, escriba **[!UICONTROL Height]**, **[!UICONTROL Depth]** y **[!UICONTROL Width]** del paquete en centímetros.

   ![Configuración del paquete DHL](../configuration-reference/sales/assets/delivery-methods-dhl-package-settings.png){width="600" zoomable="yes"}

## Paso 3: Especificar métodos de entrega permitidos

1. Para **[!UICONTROL Allowed Methods]**, elija cada método que desee que esté disponible para los clientes.

   Para seleccionar varios métodos, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

   Para mostrar la lista correcta de métodos de entrega, primero debe especificar [País de origen](../configuration-reference/sales/shipping-settings.md).

1. Para **[!UICONTROL Ready Time]**, introduzca el número de horas después de enviar un pedido que un paquete está listo para enviarse.

1. Edite **[!UICONTROL Displayed Error Message]** según sea necesario.

   Este mensaje aparece cuando un método seleccionado no está disponible.

1. Si desea proporcionar una opción de [envío gratuito](shipping-free.md) a través de DHL, establezca las opciones de envío gratuito.

   - Para **[!UICONTROL Free Method]**, elige el método que prefieras usar para el envío gratuito.

   - Establecer **[!UICONTROL Free Shipping Amount Threshold]**:

     `Enable` - Si ofrece envío gratuito con pedido mínimo, ingrese el **[!UICONTROL Minimum Order Amount for Free Shipping]**.

     `Disable` - No aplica envío DHL gratuito a ningún pedido.

     Esta configuración es similar a la del método estándar de _envío gratuito_, pero aparece en la sección de DHL para que los clientes sepan qué método se usa para su pedido.

   - Para **[!UICONTROL Free Shipping Amount Threshold]**, ingrese la cantidad mínima de un pedido para calificar para el envío gratuito.

     ![Métodos permitidos de DHL](../configuration-reference/sales/assets/delivery-methods-dhl-allowed-methods.png){width="600" zoomable="yes"}

## Paso 4: Especifique los países aplicables

1. Establezca **[!UICONTROL Ship to Applicable Countries]** en una de las siguientes opciones:

   - `All Allowed Countries`
   - `Specific Countries`

   Si realiza envíos a países específicos, seleccione cada país de la lista **[!UICONTROL Ship to Specific Countries]**.

1. Establecer **[!UICONTROL Show Method if Not Applicable]**:

   `Yes`: muestra DHL como método de envío durante el cierre de compra, aunque no sea aplicable al pedido.

   `No`: muestra DHL como método de envío durante el cierre de compra, solo si corresponde.

1. Para crear un archivo de registro con los detalles de los envíos DHL realizados desde su tienda, establezca **[!UICONTROL Debug]** en `Yes`.

1. Para **[!UICONTROL Sort Order]**, escriba un número para determinar la secuencia en la que DHL aparece cuando aparece junto con otros métodos de envío durante la desprotección.

   `0` = primero, `1` = segundo, `2` = tercero, etc.

1. Haga clic en **[!UICONTROL Save Config]**.

   ![Países Aplicables DHL](../configuration-reference/sales/assets/delivery-methods-dhl-applicable-countries.png){width="600" zoomable="yes"}
