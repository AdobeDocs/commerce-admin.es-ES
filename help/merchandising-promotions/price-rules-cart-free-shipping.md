---
title: 'Ejemplo de regla de precio del carro de compras: promoción de envío gratuito'
description: Consulte un ejemplo de uso de una regla de precio de carro de compras para ofrecer envío gratuito.
exl-id: f7652254-ff01-44ff-a207-2d7cf2017517
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
TQID: https://experienceleague.adobe.com/FR-q4Qj-ZDDzmfEKSvSj-BlwsM7ro-BqAE1yCppTaXE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 407
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
