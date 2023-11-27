---
title: 'Ejemplo de regla de precio del carro de compras: promoción de envío gratuito'
description: Consulte un ejemplo de uso de una regla de precio de carro de compras para ofrecer envío gratuito.
exl-id: f7652254-ff01-44ff-a207-2d7cf2017517
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Ejemplo de regla de precio del carro de compras: promoción de envío gratuito

El envío gratuito se puede ofrecer como una promoción, ya sea con o sin una [cupón](price-rules-cart-coupon.md). También se puede aplicar un cupón de envío gratuito o un cupón a los pedidos de recogida del cliente, de modo que el pedido se pueda facturar y enviar para completar la [workflow](../stores-purchase/order-processing.md#order-workflow-and-processing).

Algunas configuraciones de transportistas de envío le permiten ofrecer el envío gratuito en función de un pedido mínimo. Para ampliar esta capacidad básica, puede utilizar las reglas de precios del carro de compras para crear condiciones complejas basadas en varios atributos de productos, contenido del carro de compras y grupos de clientes.

## Paso 1. Habilitar envío gratuito

1. Activar [envío gratuito](../stores-purchase/shipping-free.md) en la configuración de la tienda.

1. Completa la configuración de envío gratuito para cualquier [servicio de transportista](../stores-purchase/carriers.md) que desee utilizar para el envío gratuito.

## Paso 2. Crear una regla de precios de carro

En el _Administrador_ barra lateral, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

Siga los pasos a continuación para configurar el tipo de promoción de envío gratuito que desea ofrecer.

### Ejemplo 1: Envío gratuito para cualquier pedido

1. Complete la **[!UICONTROL Rule Information]** como sigue:

   - Introduzca una **[!UICONTROL Rule Name]** para consulta interna.
   - Escriba una descripción breve **[!UICONTROL Description]** para describir la regla.
   - Establecer **[!UICONTROL Active]** hasta `Yes`.
   - En el **[!UICONTROL Websites]** , seleccione cada sitio en el que vaya a estar disponible el cupón de envío gratuito.
   - Seleccione el **[!UICONTROL Customer Groups]** al que se aplica la regla.
   - Establecer **[!UICONTROL Coupon]** a uno de los siguientes:
      - Para ofrecer una promoción de envío gratis sin cupón, acepta el valor predeterminado (`No Coupon`).
      - Para utilizar un cupón con la regla de precio, seleccione `Specific Coupon`. Si es necesario, complete las instrucciones para configurar una [cupón](price-rules-cart-coupon.md).

1. Desplazarse hacia abajo y expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Actions]** y haga lo siguiente:

   - Establecer **[!UICONTROL Apply]** hasta `Percent of product price discount`.
   - Establecer **[!UICONTROL Apply to Shipping Amount]** hasta `Yes`.
   - Establecer **[!UICONTROL Free Shipping]** hasta `For matching items only`.

   ![Regla de precio del carro de compras: acciones de envío gratis](./assets/free-shipping-actions.png){width="600" zoomable="yes"}

### Ejemplo 2: Envío gratuito para pedidos superiores a $ amount

1. Complete la **[!UICONTROL General Information]** configuración tal como se describe en el ejemplo anterior.

1. Desplazarse hacia abajo y expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Conditions]** sección.

1. Clic _Añadir_ (![Icono Agregar](../assets/icon-add-green-circle.png)) para insertar una condición y haga lo siguiente:

   - En la lista debajo de **[!UICONTROL Cart Attribute]**, elija `Subtotal`.
   - Clic **[!UICONTROL is]** y elija `equals or greater than`.
   - Clic **...** e introduzca un valor de umbral para el subtotal, como `100`, para completar la condición.

   ![Regla de precio del carro de compras: condición](./assets/free-shipping-condition1.png){width="600" zoomable="yes"}

1. Si es necesario, expanda ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Actions]** y haga lo siguiente:

   - Establecer **[!UICONTROL Apply]** hasta `Percent of product price discount`.
   - Establecer **[!UICONTROL Apply to Shipping Amount]** hasta `Yes`.
   - Establecer **[!UICONTROL Free Shipping]** hasta `For matching items only`.

## Paso 3. Completar las etiquetas

Completar [Paso 4](price-rules-cart.md) de las instrucciones de regla de precio del carro de compras para introducir cualquier etiqueta que aparezca durante el cierre de compra.

## Paso 4. Guarde y pruebe la regla

{{new-price-rule}}

1. Una vez completada la regla, haga clic en **[!UICONTROL Save Rule]**.

1. Pruebe la regla para asegurarse de que funciona correctamente.
