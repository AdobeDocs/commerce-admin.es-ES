---
title: 'Ejemplo de regla de precio del carro de compras: descuento con compra mínima'
description: Consulte un ejemplo de uso de una regla de precio de carro de compras para ofrecer un descuento con una compra mínima.
exl-id: dc06cd12-d23b-4836-9ad2-93ca60dac927
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Ejemplo de regla de precio del carro de compras: descuento con compra mínima

Las reglas de precio del carro de compras se pueden usar para ofrecer un descuento porcentual basado en una compra mínima. En el ejemplo siguiente, se aplica un descuento del 25% a todas las compras superiores a 200,00 $ en una categoría específica. El formato del descuento es el siguiente:

X% de descuento en todos los Y (categoría) sobre $Z dólares

## Paso 1. Crear una regla de carro de compras

Siga los pasos básicos [instrucciones](price-rules-cart.md) para crear una regla de carro de compras.

## Paso 2. Definición de las condiciones

1. Desplazarse hacia abajo y expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Conditions]** sección.

1. Clic _Añadir_ (![Icono Agregar](../assets/icon-add-green-circle.png)) y elija **[!UICONTROL Product Attribute Combination]**.

   ![Condición de regla de precio del carro de compras: combinación de atributos del producto](./assets/condition1.png){width="500" zoomable="yes"}

1. Clic _Añadir_ (![Icono Agregar](../assets/icon-add-green-circle.png)) al principio de la línea siguiente y en la lista debajo de **[!UICONTROL Product Attribute]**, elija **[!UICONTROL Category]**.

   - Haga clic en el botón (**...**) _más_ para mostrar opciones adicionales.

     ![Condición de regla de precio del carro de compras: opciones de categoría](./assets/condition3.png){width="600" zoomable="yes"}

   - Haga clic en _Selector_ (![Icono de lista](../assets/icon-list-chooser.png)) para ver las categorías disponibles. En el árbol de categorías, active la casilla de verificación de cada categoría que desee incluir. Haga clic en el icono de verificación para aceptar las selecciones de categoría.

     ![Condición de regla de precio del carro de compras: categoría](./assets/condition4.png){width="600" zoomable="yes"}

1. Clic _Añadir_ (![Icono Agregar](../assets/icon-add-green-circle.png)) al principio de la línea siguiente y haga lo siguiente:

   - En la lista debajo de **[!UICONTROL Cart Item Attribute]**, elija **[!UICONTROL Price in cart]**.

     ![Condición de regla de precio del carro de compras: atributo de artículo del carro](./assets/condition5.png){width="500"}

   - Clic **es** y elija `equals or greater than`.

   - Clic **...** e introduzca el importe que debe tener el precio en el carro de compras para cumplir la condición. Por ejemplo, introduzca `30`.

     ![Condición de regla de precio del carro de compras: precio en el carro](./assets/condition6.png){width="500"}

1. Haga clic **[!UICONTROL Save and Continue Edit]**.

## Paso 3. Definición de las acciones

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Actions]** y haga lo siguiente:

   ![Acciones de regla de precios de carrito](./assets/minimum-discount-actions.png){width="600" zoomable="yes"}

   - Establecer **[!UICONTROL Apply]** hasta `Percent of product price discount`.

   - Introduzca el **[!UICONTROL Discount Amount]**. Por ejemplo, introduzca `10` por un 10% de descuento.

   - Para evitar que se apliquen promociones adicionales a la compra, establezca **[!UICONTROL Discard subsequent rules]** hasta `Yes`.

1. Clic **[!UICONTROL Save and Continue Edit]** y complete la regla según sea necesario.

## Paso 4. Completar las etiquetas

Completar [Paso 4](price-rules-cart.md) de las instrucciones de regla de precio del carro de compras para introducir cualquier etiqueta que aparezca durante el cierre de compra.

## Paso 5: Guardar y probar la regla

{{new-price-rule}}

1. Una vez completada la regla, haga clic en **[!UICONTROL Save Rule]**.

1. Pruebe la regla para asegurarse de que funciona correctamente.
