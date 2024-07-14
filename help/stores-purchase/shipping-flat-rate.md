---
title: Envío de tarifa única
description: Aprenda a configurar una opción de envío de tarifa plana para su tienda.
exl-id: a6874509-a79b-42ab-aa93-d70d18fc33f6
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# Envío de tarifa única

_Tarifa fija_ es un cargo fijo predefinido que se puede aplicar por artículo o por envío. La tarifa plana es una solución de envío simple, especialmente cuando se utiliza con el embalaje de tarifa plana que está disponible en algunos operadores. Cuando está habilitada, _Tarifa fija_ aparece como una opción durante el cierre de compra. Dado que no se especifica ningún operador específico, puede utilizar el operador que elija.

## Configurar el envío a tarifa plana

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Delivery Methods]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **Tarifa fija**.

   ![Tarifa fija](../configuration-reference/sales/assets/delivery-methods-flat-rate.png){width="600" zoomable="yes"}

   Para obtener una descripción detallada de cada una de estas opciones de configuración, consulte [Tarifa plana](../configuration-reference/sales/delivery-methods.md#flat-rate) en la _Guía de referencia de configuración_.

1. Establezca **[!UICONTROL Enabled]** en `Yes`.

   La tarifa plana aparece como una opción en la sección Estimar envío e impuestos del carro de compras, y también en la sección Envío durante el cierre de compra.

1. Escriba un **[!UICONTROL Title]** descriptivo para el método de tarifa plana.

1. Escriba un **Nombre de método** que aparecerá junto a la tarifa calculada en el carro de compras.

   El nombre de método predeterminado es `Fixed`. Si cobra una tarifa de manejo, podría cambiar este texto a `Plus Handling`, o a otro que sea adecuado.

1. Para describir cómo se puede utilizar el envío de tarifa plana, establezca **Type** en una de las siguientes opciones:

   - `None` - Deshabilita el tipo de pago. La opción Tarifa fija aparece en el carro de compras, pero con una tarifa de cero, que es la misma que el envío gratuito.
   - `Per Order` - Carga una sola tarifa plana por todo el pedido.
   - `Per Item` - Carga una sola tarifa plana por cada artículo. La tasa se multiplica por el número de artículos del carro de compras, independientemente de si hay varias cantidades del mismo o de artículos diferentes.

1. Escriba el **precio** que desea cobrar por el envío con tarifa plana.

1. Configure las opciones de gastos de manipulación según sus necesidades.

   La tarifa de manipulación es opcional y aparece como un cargo adicional que se añade al coste de envío. Si desea incluir una tarifa de manejo, haga lo siguiente:

   - Para **Calcular tarifa de manejo**, seleccione el método que desee usar para calcular las tarifas de manejo:

      - `Fixed`
      - `Percent`

   - Para **Cargo por manejo**, ingrese la cantidad que se va a cargar, según el método que haya elegido para calcular la cantidad.

     Por ejemplo, si el cargo se basa en una tarifa fija, introduzca la cantidad como decimal; por ejemplo, `4.90`. Sin embargo, si la tarifa de manipulación se basa en un porcentaje del coste de envío, introduzca la cantidad como porcentaje. Por ejemplo, si va a cargar el seis por ciento de los gastos de envío, escriba el valor como `6`.

1. Si es necesario, cambie el **Mensaje de error mostrado**.

   Este cuadro de texto está preestablecido con un mensaje predeterminado, pero puede escribir un mensaje diferente que desee que aparezca si la tarifa fija de envío deja de estar disponible.

1. Definir **Enviar a los países aplicables**:

   - `All Allowed Countries`: los clientes de todos los [países](../getting-started/store-details.md#country-options) especificados en la configuración de su tienda pueden usar este método de entrega.
   - `Specific Countries` - Al elegir esta opción, aparece la lista _Enviar a países específicos_. Seleccione cada país de la lista donde se pueda utilizar este método de entrega.

1. Definir **método Show si no es aplicable**:

   - `Yes`: siempre muestra el método de tarifa plana, aunque no sea aplicable.
   - `No` - Muestra el método de tarifa plana solamente cuando corresponde.

1. Para **[!UICONTROL Sort Order]**, introduzca un número para determinar la secuencia en la que aparece Envío con tarifa plana cuando se enumera con otros métodos de entrega durante el cierre de compra.

   `0` = primero, `1` = segundo, `2` = tercero, etc.

1. Haga clic en **[!UICONTROL Save Config]**.
