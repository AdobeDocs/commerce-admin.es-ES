---
title: 'Ejemplo de regla de precio del carro de compras: comprar esto y obtener aquello'
description: Consulte un ejemplo de uso de una regla de precio del carro de compras para ofrecer una promoción "compre esto y obtenga lo otro".
exl-id: 49e4f9d1-bc60-4861-baca-a23fe148d1c4
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# Ejemplo de regla de precio del carro de compras: comprar esto y obtener aquello

Este ejemplo muestra cómo configurar una [regla de precio del carro de compras](price-rules-cart.md) para una _Compra esto y recibe esa promoción gratis_. El formato del descuento es el siguiente:

_Compre X cantidad de producto, obtenga Y cantidad gratis_

## Paso 1. Crear una regla de precios de carro

Complete [Paso 1](price-rules-cart.md) de las instrucciones de regla de precios del carro de compras para completar la información de regla.

## Paso 2. Definición de las condiciones

Complete [Paso 2](price-rules-cart.md) de las instrucciones del carro de compras para definir las condiciones de la regla de precios. Esta es la primera de las dos condiciones que se pueden agregar a la regla y determina cuándo se activa. Se puede basar en una combinación de lo siguiente:

- Atributos del producto
- Productos
- Atributos del carro
- ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Segmentos de cliente

Si se deja en blanco, la regla se activará para cada carro de compras.

![Regla de precio del carro de compras: condición](./assets/buy-x-get-y-condition-default.png){width="600" zoomable="yes"}

## Paso 3. Definición de las acciones

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Actions]** y haga lo siguiente:

   - Establezca **[!UICONTROL Apply]** en `Buy X get Y free (_[!UICONTROL _[!UICONTROL Discount Amount]_]_ is Y)`.

   - Establezca **[!UICONTROL Discount Amount]** en `1`. Esta es la cantidad que el cliente recibe gratis.

   - Para limitar el número de descuentos que se pueden aplicar cuando se cumple la condición, escriba el número en el campo **[!UICONTROL Maximum Qty Discount is Applied To]**. Esto se calcula usando esta [fórmula](#maximum-quantity-discount).

   - Para **[!UICONTROL Discount Qty Step (Buy X)]**, escriba la cantidad que el cliente debe comprar para calificar para el descuento. En este ejemplo, el cliente debe comprar tres.

   - Si desea evitar que se apliquen otros descuentos a la compra, establezca **[!UICONTROL Discard subsequent rules]** en `Yes`.

   ![Regla de precio del carro de compras: comprar 3 obtener 1 gratis](./assets/buy-3-get-1-actions.png){width="600" zoomable="yes"}

1. Para aplicar la regla solo a artículos específicos del carro de compras, complete la condición para describir los artículos del carro de compras o los atributos de producto necesarios para la promoción.

   El siguiente ejemplo utiliza el SKU para aplicar la regla a todas las variaciones asociadas de un producto configurable.

   ![Regla de precio del carro de compras: condición para los artículos del carro de compras](./assets/buy-3-get-1-actions-condition.png){width="600" zoomable="yes"}

1. Para incluir **[!UICONTROL Free Shipping]**, elija `For matching items only`.

1. Haga clic en **[!UICONTROL Save and Continue Edit]** y complete el resto de la regla según sea necesario.

## Paso 4. Complete la etiqueta

Complete [Paso 4](price-rules-cart.md) de las instrucciones de regla de precios del carro de compras para ingresar la etiqueta que aparece durante el cierre de compra.

## Paso 5: Guardar y probar la regla

{{new-price-rule}}

1. Una vez completada la regla, haga clic en **[!UICONTROL Save Rule]**.

1. Pruebe la regla para asegurarse de que funciona correctamente.

## Variaciones

Comprar X Obtener Y Gratis se procesa como una sola acción, con una dependencia de _total de filas_. Todos los artículos deben pertenecer al mismo SKU para poder optar a la promoción. Por ejemplo:

Comprar X cantidad de producto de la categoría A, obtener Y cantidad del mismo producto de forma gratuita.

Para limitar el producto libre a las categorías A, B y C, establezca la acción de la siguiente manera:

Si TODAS estas condiciones son TRUE:
La categoría es una de A, B, C

Para limitar los elementos libres de cualquier categoría (A, B o C) y recibir Y de SKU (D123, E123 o F123), establezca la acción de la siguiente manera:

Si TODAS estas condiciones son TRUE:
El SKU es uno de los D123, E123, F123

## Descuento de cantidad máxima

Utilice la siguiente fórmula para determinar el valor correcto del descuento de cantidad máxima:

Fórmula = `(X+Y) * (M/Y)`
Donde
`X` = número de artículos comprados
`Y` = número de elementos libres
`M` = Número máximo de elementos libres permitidos

Por ejemplo:

Compre cinco y obtenga dos gratis con un máximo de cuatro artículos gratis permitidos.

    Donde
    X = 5
    Y = 2
    M = 4
    Descuento De Cantidad Máxima = (5+2)*(4/2)=(7)*(2)=14

Compre cinco y obtenga tres gratis con un máximo de nueve artículos gratis permitidos.

    Donde
    X = 5
    Y = 3
    M = 9
    Descuento De Cantidad Máxima = (5+3)*(9/3)=24

Compre 20 y obtenga dos gratis con un máximo de 20 artículos gratis permitidos.

    Donde
    X = 20
    Y = 2
    M = 20
    Descuento De Cantidad Máxima = (20+2)*(20/2)=(22)*(10)=220
