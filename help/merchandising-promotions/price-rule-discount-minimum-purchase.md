---
title: 'Ejemplo de regla de precio del carro de compras: descuento con precio mínimo del producto'
description: Consulte un ejemplo de uso de una regla de precio del carro de compras para ofrecer un descuento con un precio mínimo del producto.
exl-id: dc06cd12-d23b-4836-9ad2-93ca60dac927
feature: Merchandising, Price Rules, Shopping Cart
TQID: https://experienceleague.adobe.com/IRVMCZ8C4uOJ4cBYLEv0YnOsehv0T9XWSIkyjBLhFw4
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 382
ht-degree: 0%

---

# Ejemplo de regla de precio del carro de compras: descuento con precio mínimo del producto

Las reglas de precio del carro de compras se pueden usar para ofrecer un descuento porcentual basado en un precio mínimo del producto en el carro de compras. En el siguiente ejemplo, se aplica un descuento del 10 % a todos los productos de todo el carro de compras cuando se agrega al menos un producto con un precio superior a 30,00 $ de una categoría especificada. El formato del descuento es el siguiente:

X% carrito entero cuando al menos 1 producto es de la categoría Y, y su precio es de más de $ Z dólares.

## Paso 1. Crear una regla de carro de compras

Siga las [instrucciones](price-rules-cart.md) básicas para crear una regla de carro de compras.

## Paso 2. Definición de las condiciones

1. Desplácese hacia abajo y expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Conditions]**.

1. Haga clic en _Agregar_ (![Agregar icono](../assets/icon-add-green-circle.png)) y elija **[!UICONTROL Product Attribute Combination]**.

   ![Condición de regla de precio de carro de compras: combinación de atributos de producto](./assets/condition1.png){width="500" zoomable="yes"}

1. Haga clic en _Agregar_ (![Agregar icono](../assets/icon-add-green-circle.png)) al principio de la línea siguiente y en la lista bajo **[!UICONTROL Product Attribute]**, elija **[!UICONTROL Category]**.

   - Haga clic en el vínculo (**...**) _más_ para mostrar opciones adicionales.

     ![Condición de regla de precio del carro de compras: opciones de categoría](./assets/condition3.png){width="600" zoomable="yes"}

   - Haga clic en el icono _Selector_ (![Icono de lista](../assets/icon-list-chooser.png)) para ver las categorías disponibles. En el árbol de categorías, active la casilla de verificación de cada categoría que desee incluir. Haga clic en el icono de verificación para aceptar las selecciones de categoría.

     ![Condición de regla de precio del carro de compras: categoría](./assets/condition4.png){width="600" zoomable="yes"}

1. Haga clic en _Agregar_ (![Agregar icono](../assets/icon-add-green-circle.png)) al principio de la línea siguiente y haga lo siguiente:

   - En la lista debajo de **[!UICONTROL Cart Item Attribute]**, elija **[!UICONTROL Price in cart]**.

     ![Condición de regla de precio de carro de compras: atributo de artículo de carro](./assets/condition5.png){width="500"}

   - Haga clic en **is** y elija `equals or greater than`.

   - Haga clic en **...** e introduzca la cantidad que debe estar el precio en el carro de compras para cumplir la condición. Por ejemplo, escriba `30`.

     ![Condición de regla de precio del carro de compras: precio en el carro](./assets/condition6.png){width="500"}

1. Haga clic en **[!UICONTROL Save and Continue Edit]**.

## Paso 3. Definición de las acciones

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Actions]** y haga lo siguiente:

   ![Acciones de regla de precio de carro](./assets/minimum-discount-actions.png){width="600" zoomable="yes"}

   - Establezca **[!UICONTROL Apply]** en `Percent of product price discount`.

   - Escriba **[!UICONTROL Discount Amount]**. Por ejemplo, escriba `10` para obtener un descuento del 10%.

   - Para evitar que se apliquen promociones adicionales a la compra, establezca **[!UICONTROL Discard subsequent rules]** en `Yes`.

1. Haga clic en **[!UICONTROL Save and Continue Edit]** y complete la regla según sea necesario.

## Paso 4. Completar las etiquetas

Complete [Paso 4](price-rules-cart.md) de las instrucciones de la regla de precios del carro de compras para ingresar las etiquetas que aparezcan durante el cierre de compra.

## Paso 5: Guardar y probar la regla

{{new-price-rule}}

1. Una vez completada la regla, haga clic en **[!UICONTROL Save Rule]**.
1. Pruebe la regla para asegurarse de que funciona correctamente.
