---
title: 'Ejemplo de regla de precio del carro de compras: promoción de envío gratuito'
description: Consulte un ejemplo de uso de una regla de precio de carro de compras para ofrecer envío gratuito.
exl-id: f7652254-ff01-44ff-a207-2d7cf2017517
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 0%

---

# Ejemplo de regla de precio del carro de compras: promoción de envío gratuito

El envío gratuito se puede ofrecer como promoción, con o sin [cupón](price-rules-cart-coupon.md). También se puede aplicar un cupón de envío gratuito o un cupón a los pedidos de recogida del cliente, de modo que el pedido se pueda facturar y enviar para completar el [flujo de trabajo](../stores-purchase/order-processing.md#order-workflow-and-processing).

Algunas configuraciones de transportistas de envío le permiten ofrecer el envío gratuito en función de un pedido mínimo. Para ampliar esta capacidad básica, puede utilizar las reglas de precios del carro de compras para crear condiciones complejas basadas en varios atributos de productos, contenido del carro de compras y grupos de clientes.

## Paso 1. Habilitar envío gratuito

1. Habilita [envío gratis](../stores-purchase/shipping-free.md) en la configuración de tu tienda.

1. Complete la configuración de envío gratuito para cualquier [servicio de transportista](../stores-purchase/carriers.md) que desee usar para el envío gratuito.

## Paso 2. Crear una regla de precios de carro

En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

Siga los pasos a continuación para configurar el tipo de promoción de envío gratuito que desea ofrecer.

### Ejemplo 1: Envío gratuito para cualquier pedido

1. Complete **[!UICONTROL Rule Information]** de la siguiente manera:

   - Escriba un(a) **[!UICONTROL Rule Name]** como referencia interna.
   - Escriba un breve **[!UICONTROL Description]** para describir la regla.
   - Establezca **[!UICONTROL Active]** en `Yes`.
   - En el cuadro **[!UICONTROL Websites]**, seleccione cada sitio donde debe estar disponible el cupón de envío gratuito.
   - Seleccione el(la) **[!UICONTROL Customer Groups]** al que se aplica la regla.
   - Establezca **[!UICONTROL Coupon]** en una de las siguientes opciones:
      - Para ofrecer una promoción de envío gratuita sin cupón, acepte la configuración predeterminada (`No Coupon`).
      - Para usar un cupón con la regla de precio, seleccione `Specific Coupon`. Si es necesario, complete las instrucciones para configurar un [cupón](price-rules-cart-coupon.md).

1. Desplácese hacia abajo y expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Actions]** y haga lo siguiente:

   - Establezca **[!UICONTROL Apply]** en `Percent of product price discount`.
   - Establezca **[!UICONTROL Apply to Shipping Amount]** en `Yes`.
   - Establezca **[!UICONTROL Free Shipping]** en `For matching items only`.

   ![Regla de precio del carro de compras: acciones de envío gratis](./assets/free-shipping-actions.png){width="600" zoomable="yes"}

### Ejemplo 2: Envío gratuito para pedidos superiores a $ amount

1. Complete la configuración de **[!UICONTROL General Information]** tal como se describió en el ejemplo anterior.

1. Desplácese hacia abajo y expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Conditions]**.

1. Haga clic en _Agregar_ (![Agregar icono](../assets/icon-add-green-circle.png)) para insertar una condición y haga lo siguiente:

   - En la lista debajo de **[!UICONTROL Cart Attribute]**, elija `Subtotal`.
   - Haga clic en **[!UICONTROL is]** y elija `equals or greater than`.
   - Haga clic en **...** e introduzca un valor de umbral para el subtotal, como `100`, para completar la condición.

   ![Regla de precio del carro de compras: condición](./assets/free-shipping-condition1.png){width="600" zoomable="yes"}

1. Si es necesario, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Actions]** y haga lo siguiente:

   - Establezca **[!UICONTROL Apply]** en `Percent of product price discount`.
   - Establezca **[!UICONTROL Apply to Shipping Amount]** en `Yes`.
   - Establezca **[!UICONTROL Free Shipping]** en `For matching items only`.

## Paso 3. Completar las etiquetas

Complete [Paso 4](price-rules-cart.md) de las instrucciones de la regla de precios del carro de compras para ingresar las etiquetas que aparezcan durante el cierre de compra.

## Paso 4. Guarde y pruebe la regla

{{new-price-rule}}

1. Una vez completada la regla, haga clic en **[!UICONTROL Save Rule]**.

1. Pruebe la regla para asegurarse de que funciona correctamente.
