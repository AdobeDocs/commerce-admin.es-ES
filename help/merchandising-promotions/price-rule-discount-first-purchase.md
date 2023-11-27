---
title: 'Ejemplo de regla de precio del carro de compras: descuento con la primera compra'
description: Consulte un ejemplo de uso de una regla de precio de carro de compras para ofrecer un descuento a los clientes que ingresan por primera vez.
exl-id: 46add769-6fa9-40e0-9f4f-af2215f36283
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: dbe31fa6e7b83ac852e6e4988ac61627e30d9089
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# Ejemplo de regla de precio del carro de compras: descuento con la primera compra

{{ee-feature}}

Las reglas de precio del carro de compras se pueden usar para ofrecer automáticamente un descuento a los clientes en su primera compra, sin necesidad de cupones.

Para ofrecer un descuento dirigido a los clientes nuevos, puede:

- Cree un segmento de cliente definido como _compradores sin pedidos_, y luego
- Cree una regla de precios de carro de compras dirigida al nuevo segmento de clientes.

>[!NOTE]
>
>Asegúrese de que la función Segmentos del cliente esté activada. Consulte [Crear un segmento de cliente](../customers/customer-segment-create.md).

## Paso 1. Crear un segmento de cliente

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Segments]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Segment]**.

1. Defina el **[!UICONTROL General Properties]**.

   - Introduzca una **[!UICONTROL Segment Name]** para identificar el segmento de clientes (ejemplo: _Cliente por primera vez_).

   - Para **[!UICONTROL Assigned to Website]**, seleccione el sitio web donde se puede utilizar el segmento de cliente.

   - Para **[!UICONTROL Status]**, seleccione `Active`.

   - Para **[!UICONTROL Apply to]**, seleccione `Visitors and Registered Customers`.

   - Cuando termine, haga clic en **[!UICONTROL Save and Continue Edit]**.

     Hay opciones adicionales disponibles en el panel de la izquierda.

   ![Propiedades del segmento de cliente](./assets/customer-segment-first-time.png){width="600" zoomable="yes"}

1. Defina el **[!UICONTROL Conditions]**.

   Para este ejemplo, la condición se dirige a los clientes para los que _El número total de pedidos es inferior a 1_ es True.

   - En el panel de la izquierda, elija **[!UICONTROL Conditions]**.

     La condición predeterminada comienza con &quot;Si TODAS estas condiciones son VERDADERAS&quot;:

   - Clic _Añadir_ (![Icono Agregar](../assets/icon-add-green-circle.png)) y seleccione `Number of Orders`.

   - Clic **[!UICONTROL is]** y seleccione `less than`.

   - Clic **...** y escriba `1` en el campo.

   - Haga clic en la marca verde ( ![Marca de verificación verde](../assets/icon-checkmark-green-circle.png) ) para guardar la configuración de condición.

   ![Condición de segmento de cliente](./assets/customer-segment-first-time-condition.png){width="600" zoomable="yes"}

1. Haga clic **[!UICONTROL Save]**.

El segmento de cliente se crea y se muestra en la variable _[!UICONTROL Customer Segments]_rejilla.

>[!TIP]
>
>Tome nota del ID del segmento. Utilice este número de ID para crear la regla de precios del carro de compras.

## Paso 2. Crear la regla de precios del carro de compras

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rule]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add New Rule]**.

   El **[!UICONTROL Rule Information]** La sección se muestra de forma predeterminada, con secciones ampliables para **[!UICONTROL Conditions]** y **[!UICONTROL Conditions]**.

1. Defina el **[!UICONTROL Rule Information]**.

   - Complete la **[!UICONTROL Rule Name]** y **[!UICONTROL Description]** campos. Estos campos son solo para referencia interna.

   - Para **[!UICONTROL Websites]**, seleccione el sitio web donde la regla debe estar disponible.

   - Para **[!UICONTROL Customer Groups]**, seleccione el grupo de clientes al que se aplica esta regla.

     Para seleccionar varios grupos, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

     >[!NOTE]
     >
     >Las opciones de esta lista dependen de los grupos de clientes creados y administrados en **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

   - Para **[!UICONTROL Coupon]**, seleccione `No Coupon`.

   - Para **[!UICONTROL Uses per Customer]**, introduzca `1`.

   - Para **[!UICONTROL Priority]**, introduzca un número para establecer la prioridad de esta regla en relación con otras reglas.

     >[!NOTE]
     >
     >La configuración Prioridad es importante cuando el mismo producto de catálogo cumple las condiciones establecidas para más de una regla de precio. La regla con la configuración de prioridad más alta se activa para el cliente. La prioridad más alta es 1. Para este ejemplo, introduzca `1` significa que esta regla se aplica antes que cualquier otra regla de precio. Este valor lo utiliza la variable **[!UICONTROL Discard Subsequent Rules]** configuración en la **[!UICONTROL Action]** sección.

   - Cuando termine, haga clic en **[!UICONTROL Save and Continue Edit]**.

     Hay opciones adicionales disponibles en el panel de la izquierda.

   ![Información de regla de precio de carro](./assets/rule-information-first-time.png){width="600" zoomable="yes"}

1. Defina el **[!UICONTROL Conditions]**.

   - Desplazarse hacia abajo y expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Conditions]** sección.

     La regla predeterminada comienza con &quot;Si TODAS estas condiciones son VERDADERAS:&quot;.

   - Clic _Añadir_ (![Icono Agregar](../assets/icon-add-green-circle.png)) y seleccione `Customer Segment`.

     El valor predeterminado del campo cualificador es `matches`.

   - Clic **...** e introduzca el ID del segmento de cliente al que desea dirigirse.

     Para este ejemplo, el ID del segmento nuevo creado en el paso 1 es `2`.

     >[!NOTE]
     >
     >Si no conoce el ID del segmento, haga clic en el icono del selector ( ![Icono de lista](../assets/icon-list-chooser.png) ) para mostrar la lista Segmento de cliente. Puede introducir manualmente el ID en el campo o seleccionar la casilla de verificación del segmento deseado para rellenar automáticamente el campo.

   - Haga clic en la marca verde ( ![Marca de verificación verde](../assets/icon-checkmark-green-circle.png) ) para guardar la configuración de condición.

   - Cuando termine, haga clic en **[!UICONTROL Save and Continue Edit]**.

     Esta línea de la regla se aplica a todos los clientes que coinciden con el ID de segmento de cliente 2.

   ![Condición de segmento de cliente](./assets/customer-segment-matches.png){width="400"}

1. Desplazarse hacia abajo y expandir ![Selector de expansión](../assets/icon-display-expand.png)el **[!UICONTROL Conditions]** y definir las acciones de la regla.

   En esta sección, defina el tipo de descuento y el valor/importe del descuento que desea aplicar a los clientes que ingresan por primera vez. En este ejemplo se define un descuento del 10% para todos los clientes que cumplan la condición definida. Para obtener información sobre otras opciones disponibles, consulte [Creación de una Regla de Precio de Carro](price-rules-cart-create.md).

   - Para **[!UICONTROL Apply]**, seleccione Porcentaje de descuento en el precio del producto.

   - Para **[!UICONTROL Discount Amount]**, introduzca `10`.

   - Para aplicar esta regla de precio solo a importes de productos, establezca **[!UICONTROL Apply to Shipping Amount]** hasta `No`.

   - Para evitar que el sistema aplique varias reglas de precios al mismo producto, establezca **[!UICONTROL Discard Subsequent Rules]** hasta `Yes`.

   - Cuando termine, haga clic en **[!UICONTROL Save]**.

   ![Acciones de regla de precios de carrito](./assets/actions-first-time.png){width="600" zoomable="yes"}

La nueva regla suele estar disponible en una hora. Pruebe la regla para asegurarse de que funciona como la definió.

## Paso 3: Guardar y probar la regla

{{new-price-rule}}

1. Una vez completada la regla, haga clic en **[!UICONTROL Save Rule]**.

1. Pruebe la regla para asegurarse de que funciona correctamente.
