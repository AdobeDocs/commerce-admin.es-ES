---
title: Envío de tarifa de tabla
description: Aprenda a configurar una opción de envío de tarifa de tabla para su tienda.
exl-id: f73adc9a-4c6c-477d-9553-3a3f28647bdd
feature: Shipping/Delivery
source-git-commit: 0f368e87275a85e3801e6770b8985184e2071384
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 3%

---

# Envío de tarifa de tabla

El método de envío _tarifa de tabla_ hace referencia a una tabla de datos para calcular las tarifas de envío en función de una combinación de condiciones, entre las que se incluyen:

- Peso frente al destino
- Precio frente a destino
- Número de elementos frente al destino

Por ejemplo, si su almacén está en Los Ángeles, cuesta menos enviar a San Diego que a Vermont. Puede utilizar el envío de tarifa de tabla para pasar los ahorros a sus clientes.

Los datos que se utilizan para calcular las tasas de tablas se preparan en una hoja de cálculo y se importan en la tienda. Cuando el cliente solicita una oferta, los resultados aparecen en la sección de estimación de envío del carro de compras.

>[!NOTE]
>
>Solo puede haber un conjunto de datos de tasa de tabla activos a la vez.

![Opción de envío de tarifa de tabla en el resumen del pedido del carro de compras](./assets/storefront-cart-table-rate.png){width="700" zoomable="yes"}

## Paso 1: Completar la configuración predeterminada

El primer paso es completar la configuración predeterminada para las tasas de tabla. Puede completar este paso sin cambiar el ámbito de la configuración.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En la sección _[!UICONTROL Sales]_&#x200B;del panel izquierdo, elija **[!UICONTROL Delivery Methods]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Table Rates]**.

   >[!NOTE]
   >
   >Si es necesario, primero desmarque la casilla de verificación **[!UICONTROL Use system value]** para cambiar la siguiente configuración como se describe.

   ![Tarifas de tabla](../configuration-reference/sales/assets/delivery-methods-table-rates.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Enabled]** en `Yes`.

1. Escriba el(la) **[!UICONTROL Title]** que desea que aparezca para la sección de tarifas de tabla durante el cierre de compra.

   El título predeterminado es `Best Way`.

1. Escriba el(la) **[!UICONTROL Method Name]** que desea que aparezca como una etiqueta junto a la tarifa calculada en el carro de compras.

1. Establezca **[!UICONTROL Condition]** en uno de los siguientes métodos de cálculo:

   - `Weight v. Destination`
   - `Price v. Destination`
   - `Number of Items v. Destination`

1. Para pedidos que incluyen productos virtuales, establezca **[!UICONTROL Include Virtual Products in Price Calculation]** en `Yes` si desea poder incluir los productos virtuales en el cálculo.

   >[!NOTE]
   >
   >Debido a que los productos virtuales, como los servicios, no tienen peso, no pueden cambiar el resultado de un cálculo basado en la condición Peso frente a Destino. Sin embargo, los productos virtuales pueden cambiar el resultado de un cálculo basado en la condición Precio frente a Destino o Número de artículos frente a Destino.

1. Configure las opciones de gastos de manipulación según sus necesidades.

   La tarifa de manipulación es opcional y aparece como un cargo adicional que se añade al coste de envío. Si desea incluir una tarifa de manejo, haga lo siguiente:

   - Establecer **[!UICONTROL Calculate Handling Fee]**:

      - `Fixed`
      - `Percent`

   - Escriba la tarifa **[!UICONTROL Handling Fee]** según el método usado para calcular la tarifa.

     Por ejemplo, si el cargo se basa en una tarifa fija, introduzca la cantidad como decimal; por ejemplo, `4.90`. Sin embargo, si la tarifa de manipulación se basa en un porcentaje del pedido, introduzca la cantidad como porcentaje. Por ejemplo, si está cargando el seis por ciento del pedido, introduzca el valor como `.06`.

1. Si es necesario, cambie **[!UICONTROL Displayed Error Message]**.

   Este cuadro de texto está preestablecido con un mensaje predeterminado, pero puede escribir un mensaje diferente que desee que aparezca si este método de entrega deja de estar disponible.

1. Establecer **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries`: los clientes de todos los [países](../getting-started/store-details.md#country-options) especificados en la configuración de su tienda pueden usar este método de entrega.
   - `Specific Countries` - Cuando elige esta opción, aparece la lista _[!UICONTROL Ship to Specific Countries]_. Seleccione cada país de la lista donde se pueda utilizar este método de entrega.

1. Establezca **[!UICONTROL Show Method if Not Applicable]** en `Yes` si desea mostrar las tarifas de tabla todo el tiempo

1. Para **[!UICONTROL Sort Order]**, introduzca un número para determinar la secuencia en la que aparece la Tabla Tasa de envío cuando se enumera con otros métodos de envío durante el cierre de compra.

   `0` = primero, `1` = segundo, `2` = tercero, etc.

1. Haga clic en **[!UICONTROL Save Config]**.

## Paso 2: Preparar los datos de tasa de tabla

1. En la esquina superior izquierda, establezca **[!UICONTROL Store View]** en `Main Website` o en cualquier otro sitio web donde se aplique la configuración.

   >[!NOTE]
   >
   >Si es necesario, anule primero la selección de la casilla de verificación **[!UICONTROL Use system value]** para cambiar la siguiente configuración como se describe a continuación.

1. Cambie **[!UICONTROL Condition]** según sea necesario.

1. Haga clic en **[!UICONTROL Export CSV]**.

   ![Exportar CSV](./assets/shipping-table-rates-export.png){width="700" zoomable="yes"}

1. Guarde el archivo `tablerates.csv` en el sistema.

1. Abra el archivo en una aplicación de hoja de cálculo.

1. Complete la tabla con los valores adecuados para la condición de cálculo de envío.

   - Utilice un asterisco (*) como comodín que represente todos los valores posibles de cualquier categoría.
   - La columna _[!UICONTROL Country]_&#x200B;debe contener [un código de tres caracteres válido][1] para cada fila.
   - Ordene los datos por _[!UICONTROL Region/State]_&#x200B;de modo que las ubicaciones específicas estén en la parte superior de la lista y las ubicaciones de los comodines en la parte inferior. Al utilizar este método, se procesan primero las reglas con los valores absolutos y, después, los valores comodín.
   - No se admiten intervalos de código postal. Use un asterisco (*) para permitir todos los códigos de la región o el estado, o especifique un solo código para una ubicación específica en la columna _[!UICONTROL Zip/Postal Code]_.
   - Los valores de la columna _[!UICONTROL Weight (and above)]_&#x200B;pueden tener un máximo de cuatro decimales (como `2.5075`). Si utiliza más decimales en los datos, la importación fallará.

   ![Peso vs. Destino (Australia)](./assets/table-rates-weight-destination-csv.png){width="500"}

1. Guarde el archivo `tablerates.csv`.

## Paso 3: Importación de los datos de tasa de tabla

1. Vuelva a la sección **[!UICONTROL Table Rates]** de la configuración de la tienda.

1. En la esquina superior izquierda, establezca **[!UICONTROL Store View]** en el sitio web donde se utiliza este método.

1. Para **[!UICONTROL Import]**, haga clic en **[!UICONTROL Choose File]** y seleccione el archivo `tablerates.csv` completado para importar las tarifas.

   ![Importar tarifas de tabla](./assets/shipping-table-rates-import.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save Config]**.

## Paso 4: Verificar las tarifas

Para asegurarse de que los datos de tarifa de tabla son correctos, siga el proceso de pago con varias direcciones diferentes para asegurarse de que las tarifas de envío y manipulación se calculan correctamente.

### Ejemplo 1: Precio y destino

En este ejemplo se utiliza la condición Precio contra Destino para crear un conjunto de tres tarifas de envío diferentes basadas en la cantidad del subtotal del pedido para los Estados Unidos continentales, Alaska y Hawai. El asterisco (*) es un comodín que representa todos los valores.

| PAÍS | REGIÓN/ESTADO | CÓDIGO POSTAL | SUBTOTAL DE PEDIDOS (y superior) | PRECIO DE ENVÍO |
|--- |--- |--- |--- |--- |
| EE. UU. | HOLA | * | 100 | 10 |
| EE. UU. | HOLA | * | 50 | 15 |
| EE. UU. | HOLA | * | 0 | 20 |
| EE. UU. | AK | * | 100 | 10 |
| EE. UU. | AK | * | 50 | 15 |
| EE. UU. | AK | * | 0 | 20 |
| EE. UU. | * | * | 100 | 5 |
| EE. UU. | * | * | 50 | 10 |
| EE. UU. | * | * | 0 | 15 |

{style="table-layout:auto"}

### Ejemplo 2: Peso y destino

En este ejemplo se utiliza la condición Weight v. Destination para crear tarifas de envío diferentes en función del peso del pedido.

| PAÍS | REGIÓN/ESTADO | CÓDIGO POSTAL | PESO (y superior) | PRECIO DE ENVÍO |
|--- |--- |--- |--- |--- |
| AUS | NT | * | 9 | 39,95 |
| AUS | NT | * | 0 | 19,95 |
| AUS | VIC | * | 9 | 19,95 |
| AUS | VIC | * | 0 | 5,95 |
| AUS | WA | * | 9 | 39,95 |
| AUS | WA | * | 0 | 19,95 |
| AUS | * | * | 9 | 29,95 |
| AUS | * | * | 0 | 9,95 |

{style="table-layout:auto"}

### Ejemplo 3: Restringir el envío gratuito a Estados Unidos continental

1. Cree un archivo de `tablerates.csv` que incluya todos los destinos de estado a los que desea proporcionar el envío gratuito.

1. Complete la configuración de tasa de tabla con las siguientes opciones:

   | Configuración | Valor |
   |----------|-------|
   | [!UICONTROL Condition] | `Price v. Destination` |
   | [!UICONTROL Method Name] | `Free Shipping` |
   | [!UICONTROL Ship to Applicable Countries] | `Specific Countries` |
   | [!UICONTROL Ship to Specific Countries] | `Select only United States` |
   | [!UICONTROL Show method if not applicable] | `No` |

   {style="table-layout:auto"}

1. En la esquina superior izquierda, establezca **[!UICONTROL Store View]** en `Main Website` o en cualquier otro sitio web donde se aplique la configuración.

1. Para **[!UICONTROL Import]**, haga clic en **[!UICONTROL Choose File]** y seleccione el archivo `tablerates.csv` completado para importar las tarifas.


[1]: https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3
