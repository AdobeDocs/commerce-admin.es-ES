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

_Tarifa plana_ es un cargo fijo predefinido que se puede aplicar por artículo o por envío. La tarifa plana es una solución de envío simple, especialmente cuando se utiliza con el embalaje de tarifa plana que está disponible en algunos operadores. Cuando está activada, _Tarifa plana_ aparece como una opción durante el cierre de compra. Dado que no se especifica ningún operador específico, puede utilizar el operador que elija.

## Configurar el envío a tarifa plana

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Delivery Methods]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **Tarifa plana** sección.

   ![Tarifa plana](../configuration-reference/sales/assets/delivery-methods-flat-rate.png){width="600" zoomable="yes"}

   Para obtener una descripción detallada de cada una de estas opciones de configuración, consulte [Tarifa plana](../configuration-reference/sales/delivery-methods.md#flat-rate) en el _Guía de referencia de configuración_.

1. Establecer **[!UICONTROL Enabled]** hasta `Yes`.

   La tarifa plana aparece como una opción en la sección Estimar envío e impuestos del carro de compras, y también en la sección Envío durante el cierre de compra.

1. Introduzca un elemento descriptivo **[!UICONTROL Title]** para el método Tasa única.

1. Introduzca una **Nombre del método** aparece junto a la tarifa calculada en el carro de compras.

   El nombre de método predeterminado es `Fixed`. Si cobra una tarifa de manejo, podría cambiar este texto a `Plus Handling`, o cualquier otra cosa que sea adecuada.

1. Para describir cómo se puede utilizar el envío a tarifa única, establezca **Tipo** a uno de los siguientes:

   - `None` - Desactiva el tipo de pago. La opción Tarifa fija aparece en el carro de compras, pero con una tarifa de cero, que es la misma que el envío gratuito.
   - `Per Order` - Se cobra una única tarifa plana por todo el pedido.
   - `Per Item` - Se cobra una única tarifa plana por cada artículo. La tasa se multiplica por el número de artículos del carro de compras, independientemente de si hay varias cantidades del mismo o de artículos diferentes.

1. Introduzca el **Precio** que desea cobrar por el envío de tarifa plana.

1. Configure las opciones de gastos de manipulación según sus necesidades.

   La tarifa de manipulación es opcional y aparece como un cargo adicional que se añade al coste de envío. Si desea incluir una tarifa de manejo, haga lo siguiente:

   - Para **Calcular tarifa de manejo**, seleccione el método que desee utilizar para calcular las tarifas de manipulación:

      - `Fixed`
      - `Percent`

   - Para **Tarifa de manipulación**, introduzca el importe que se va a cargar, según el método que haya elegido para calcular el importe.

     Por ejemplo, si el cargo se basa en una tarifa fija, introduzca la cantidad como decimal, por ejemplo `4.90`. Sin embargo, si la tarifa de manipulación se basa en un porcentaje del coste de envío, introduzca la cantidad como porcentaje. Por ejemplo, si va a cargar el seis por ciento de los gastos de envío, introduzca el valor como `6`.

1. Si es necesario, cambie el **Mensaje de error mostrado**.

   Este cuadro de texto está preestablecido con un mensaje predeterminado, pero puede escribir un mensaje diferente que desee que aparezca si la tarifa fija de envío deja de estar disponible.

1. Establecer **Enviar a los países aplicables**:

   - `All Allowed Countries` - Clientes de todos [países](../getting-started/store-details.md#country-options) especificado en la configuración de la tienda puede utilizar este método de envío.
   - `Specific Countries` - Al elegir esta opción, la variable _Enviar a países específicos_ aparece una lista. Seleccione cada país de la lista donde se pueda utilizar este método de entrega.

1. Establecer **Mostrar método si no es aplicable**:

   - `Yes` - Muestra siempre el método de Tarifa Plana, aunque no sea aplicable.
   - `No` - Muestra el método de tarifa plana solo cuando corresponde.

1. Para **[!UICONTROL Sort Order]**, introduzca un número para determinar la secuencia en la que aparece la tarifa plana de envío cuando se enumera con otros métodos de envío durante el cierre de compra.

   `0` = primero, `1` = segundo, `2` = tercero, etc.

1. Haga clic **[!UICONTROL Save Config]**.
