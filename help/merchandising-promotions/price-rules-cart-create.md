---
title: Crear una regla de precios de carro
description: Aprenda a crear una regla de precios de carro de compras basada en el carro de compras o en los atributos del producto.
exl-id: 7260e7c3-3b1e-43e5-9c09-c40538e37378
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: bf52884cb0eccd4d9c7326a95f8600a3ed950918
workflow-type: tm+mt
source-wordcount: '2885'
ht-degree: 0%

---

# Crear una regla de precios de carro

Complete los siguientes pasos para agregar una regla, describir las condiciones y definir las acciones. Complete también las etiquetas y pruebe la regla. Las condiciones de regla de precio pueden basarse en el carro o en [atributos del producto](../catalog/product-attributes.md) o [Audiencias de Real-Time CDP](#use-real-time-cdp-audiences-to-set-a-condition), pero no en [opciones personalizables](../catalog/settings-advanced-custom-options.md).

## Paso 1: Añadir una regla

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

1. Clic **[!UICONTROL Add New Rule]** y haga lo siguiente:

   - En _[!UICONTROL Rule Information]_, complete la **[!UICONTROL Rule Name]**y **[!UICONTROL Description]**.

   - Si no desea que la regla entre en vigor inmediatamente, establezca **[!UICONTROL Active]** hasta `No`.

   ![Regla de precio del carro de compras: información de regla](./assets/price-rule-cart-new.png){width="600" zoomable="yes"}

1. Para establecer el [ámbito](../getting-started/websites-stores-views.md#scope-settings) de la regla, haga lo siguiente:

   - Seleccione el **[!UICONTROL Websites]** donde la promoción va a estar disponible.

   - Seleccione el **[!UICONTROL Customer Groups]** al que se aplica la promoción.

     Si desea que la promoción esté disponible solo para clientes registrados, **_no_** elija el `NOT LOGGED IN` opción.

1. Configure la regla para que se aplique con o sin [cupón](price-rules-cart-coupon.md) como sigue:

   - Para que se aplique la regla de carro de compras sin utilizar un código de cupón, establezca **[!UICONTROL Coupon]** hasta `No Coupon` y vaya directamente al paso 5.

   - Para asociar un cupón a una regla de precio, establezca **[!UICONTROL Coupon]** hasta `Specific Coupon` y haga lo siguiente:

      - Escriba un texto libre **[!UICONTROL Coupon Code]** que el cliente debe introducir para recibir el descuento.

      - Para establecer un límite en el número de veces que se puede utilizar el cupón, complete las siguientes opciones:

     | Opción | Descripción |
     |------|-----------|
     | `Uses per Coupon` | Determina cuántas veces se puede utilizar el código de cupón. Si no hay límite, deje el campo en blanco. |
     | `Uses per Customer` | Determina cuántas veces el mismo cliente registrado que pertenece a cualquiera de los grupos de clientes seleccionados puede usar la regla de precio del carro de compras. La configuración no se aplica a compradores invitados que sean miembros del grupo de clientes NOT LOGGED IN, ni a clientes que compren sin iniciar sesión en sus cuentas. Si no hay límite, deje el campo en blanco. |

     {style="table-layout:auto"}

     Para obtener más información, consulte [Códigos de cupón](price-rules-cart-coupon.md).

     ![Regla de precio del carro de compras: configuración de cupones](./assets/price-rule-cart-coupon-settings-ee.png){width="600" zoomable="yes"}

   - ![Magento Open Source](../assets/open-source.svg) (Solo Magento Open Source) Utilice el _Calendario_ (![Icono de calendario](../assets/icon-calendar.png)) para elegir el **[!UICONTROL From]** y **[!UICONTROL To]** intervalo de fechas de la promoción.

1. Introduzca un número para definir la variable **[!UICONTROL Priority]** de esta regla de precios en relación con la configuración de acción de otras reglas de precios que estén activas al mismo tiempo.

   >[!NOTE]
   >
   >La configuración Prioridad es importante cuando dos reglas de carro de compras/códigos de cupones son válidos para el mismo producto al mismo tiempo. La regla con la configuración de prioridad más alta (`1` siendo la más alta) controla la acción del carro de compras. Consulte _Descartar reglas de precios posteriores_ en el _Definición de las acciones_ paso.

   >[!NOTE]
   >
   >Las reglas de precios del carro de compras que tienen la misma prioridad no resultan en un descuento combinado. Cada regla se aplica a los productos coincidentes por separado, uno a uno.

1. Para aplicar la regla a los recursos publicados [Fuentes RSS](social-rss.md#rss-feeds), configurado **Público en fuente RSS** hasta `Yes`.

1. Haga clic **[!UICONTROL Save and Continue Edit]**.

   - ![Magento Open Source](../assets/open-source.svg) (Solo Magento Open Source) Una vez guardada la regla, el nombre de la regla de precio del carro de compras aparece en la parte superior de la página.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Una vez guardada la regla, el nombre de la regla de precios del carro de compras y el [Cambios programados](price-rule-cart-scheduled-changes.md) aparece en la parte superior de la página.

     ![Regla de precio del carro de compras: cambios programados](./assets/price-rule-cart-scheduled-changes.png){width="600" zoomable="yes"}

## Paso 2: Describir las condiciones

En este paso se describen las condiciones que deben cumplirse para que una solicitud cumpla los requisitos para la promoción. La regla entra en acción cada vez que se cumple el conjunto de condiciones.

Si utiliza audiencias de Real-Time CDP, vaya a [esta sección](#use-real-time-cdp-audiences-to-set-a-condition).

>[!NOTE]
>
>La regla de precio del carro de compras se aplica a **_cada_** producto en el carro de compras siempre que el conjunto de condiciones del _[!UICONTROL Conditions]_se cumple la pestaña. Añadir condiciones en la_[!UICONTROL Actions]_ para limitar el número de productos afectados por la regla de precio del carro de compras.

>[!NOTE]
>
>Si al menos un atributo de producto condicional tiene un valor vacío, la regla de precio del carro de compras no se aplica al producto.

1. En el panel izquierdo, seleccione **[!UICONTROL Conditions]**.

   ![Regla de precio del carro de compras: condiciones](./assets/conditions.png){width="600" zoomable="yes"}

   La primera condición aparece de forma predeterminada y establece lo siguiente:

   `If **ALL** of these conditions are **TRUE**:`

   La instrucción tiene dos vínculos en negrita en los que puede hacer clic para mostrar la selección de opciones de esa parte de la instrucción. Puede crear diferentes condiciones cambiando la combinación de estos valores. Realice una de las siguientes acciones:

   - Clic **[!UICONTROL ALL]** y seleccione `ALL` o `ANY`.
   - Clic **[!UICONTROL TRUE]** y seleccione `TRUE` o `FALSE`.
   - Deje la condición sin cambios para aplicar la regla a todos los productos.

1. Clic _Añadir_ (![Icono Agregar](../assets/icon-add-green-circle.png)) al principio de la línea siguiente y seleccione una opción para la condición, como atributo de carro de compras, subselección de productos o combinación.

   Para este ejemplo, complete la siguiente parte de la condición de la siguiente manera:

   - Cuando se le solicite **[!UICONTROL Choose the condition to add]**, elija `Products Subselection`.

     ![Condición de regla de precio del carro de compras: subselección de productos](./assets/price-rule-cart-condition-products-subselection.png){width="600" zoomable="yes"}

   - En la instrucción condition, haga clic en **[!UICONTROL total quantity]** y seleccione `total quantity` o `total amount`.

   >[!IMPORTANT]
   >
   >[!UICONTROL Total amount] es un total de fila, por lo que los impuestos no se incluyen en la `total amount` para el [!UICONTROL Products Subselection] condición de regla de precio de carro. Utilice el [!UICONTROL Subtotal (Incl. Tax)] condición para incluir impuestos.

   - En la instrucción condition, haga clic en **[!UICONTROL is]** y seleccione `greater than`.

1. Cuando aparezca la siguiente parte de la condición, haga clic en los elementos de la instrucción para que pueda ver dónde se encuentra cada vínculo con valores de variables.

1. Haga clic en el vínculo &quot;más&quot; (...) e introduzca `100`.

   Esta condición requiere que la cantidad total del carro de compras sea `101` o superior.

   ![Condición de regla de precio del carro de compras: valor de cantidad total](./assets/condition-products-subselection3.png){width="600" zoomable="yes"}

1. Clic **Añadir** (![Icono Agregar](../assets/icon-add-green-circle.png)) al principio de la línea siguiente y, a continuación, agregue una condición basada en **Categoría**.

   ![Condición de regla de precio del carro de compras: categoría de atributo de producto](./assets/condition-products-subselection4.png){width="600" zoomable="yes"}

1. En la siguiente parte de la condición, haga clic en _más_ (**...**) para mostrar el campo de entrada y, a continuación, abrir _Selector_ (![Icono de lista](../assets/icon-list-chooser.png)) para mostrar el árbol de categorías.

1. Seleccione la casilla de la categoría que desee utilizar como condición para la regla de precio y haga clic en ![Icono Agregar](../assets/icon-checkmark-green-circle.png) para aceptar las selecciones de categoría.

   La condición se puede basar en cualquier categoría que sea secundaria de la del almacén [categoría raíz](../catalog/category-root.md).

   ![Condición de regla de precio del carro de compras: categoría de producto](./assets/subselection-category.png){width="600" zoomable="yes"}

1. Para añadir más condiciones, haga clic en _Añadir_ (![Icono Agregar](../assets/icon-add-green-circle.png)) y defina otra condición.

   Puede repetir el proceso tantas veces como sea necesario para describir las condiciones que deben cumplirse para la regla de precio. Estos son algunos ejemplos:

   **Ejemplo 1:** Regla de precio regional

   Para crear una regla de precios regional, utilice uno de los siguientes atributos de carro de compras:

   - `Shipping Postcode`
   - `Shipping Region`
   - `Shipping State/Province`
   - `Shipping Country`

   **Ejemplo 2:** Totales del carro de compras

   Para basar la condición en los totales del carro de compras, utilice uno de los siguientes atributos:

   - `Subtotal`
   - `Total Items Quantity`
   - `Total Weight`

>[!NOTE]
>
>En el caso de varias promociones paralelas, la variable _Subtotal_ La condición se aplica a _basar_ subtotal del carro de compras **_antes_** cualquier descuento.

>[!IMPORTANT]
>
>**Solo para pedidos de compra**: Cuando se establece una regla de precio de carro de compras basada en uno o más métodos de pago específicos, el descuento se aplica al total cuando se crea un pedido de compra. Una vez creado el pedido de compra, el descuento permanece aplicado al total si el método de pago se cambia por uno que no esté cubierto por la regla de precio del carro de compras.

### Añadir un atributo de producto a las reglas de precios del carro de compras

1. Ir a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**y abra el atributo product.

1. En el panel izquierdo, seleccione **[!UICONTROL Storefront Properties]**.

1. Establecer **[!UICONTROL Use for Promo Rule Conditions]** hasta `Yes`.

1. Haga clic **[!UICONTROL Save Attribute]**.

1. Ir a **[!UICONTROL Marketing]** > **[!UICONTROL Cart Price Rules]** y abra la regla de precio del carro de compras requerida.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Condition]** y seleccione **[!UICONTROL Product attribute combination]**.

1. Establezca esta condición en uno de los siguientes valores:

   - Clic **[!UICONTROL FOUND]** y seleccione `FOUND` o `NOT FOUND`.

   - Clic **[!UICONTROL ALL]** y seleccione `ALL` o `ANY`.

1. Haga clic en _Añadir_ (![Icono Agregar](../assets/icon-add-green-circle.png)) y seleccione el icono **[!UICONTROL Product Attribute]** que configure para las condiciones de regla promocional.

1. Haga clic **[!UICONTROL Save]**.

>[!NOTE]
>
>Al usar el `is not one of` condición con un _SKU_ atributo de producto y producto configurable, se deben seleccionar tanto la SKU del producto principal como la secundaria. Para evitar enumerar todos los SKU secundarios en la regla, puede utilizar el `does not contain` con las partes SKU comunes de un producto configurable y sus productos secundarios.

### Usar audiencias de Real-Time CDP para establecer una condición

Puede establecer una condición para una regla de precios de carro de compras basada en una Real-Time CDP [audiencia](../customers/audience-activation.md).

1. Expandir **[!UICONTROL Conditions]**, haga clic en el icono &quot;+&quot; y seleccione **[!UICONTROL Real-Time CDP Audience]** de la lista.

   ![Seleccionar condición de audiencia de Real-Time CDP](./assets/rtcdp-conditions.png){width="300"}

1. Seleccione el _Más_ (**...**), haga clic en **[!UICONTROL Open Chooser]** y vea todas las audiencias de Real-Time CDP disponibles.

   ![Ver audiencias de Real-Time CDP](./assets/rtcdp-conditions-chooser.png){width="600" zoomable="yes"}

1. Seleccione la audiencia de Real-Time CDP que desee utilizar para la regla de precio del carro de compras.

   | Opción | Descripción |
   |------|-----------|
   | `ID` | Un identificador interno de la audiencia que se usa en el administrador |
   | `Real-Time CDP Audience ID` | Identificador único de la audiencia cuando se creó en Experience Platform |
   | `Name` | Nombre de la audiencia como, por ejemplo, `Orders over $50` |
   | `Description` | Descripción de la audiencia, como `People who placed an order over $50 in the last month.`. |
   | `Source` | Indica la procedencia de la audiencia, como `Experience Platform`. |
   | `Website` | Indica qué sitio web ha vinculado al conjunto de datos que contiene las audiencias. Este vínculo se crea al conectar la instancia de Commerce al Experience Platform a través de [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html) extensión. |

   {style="table-layout:auto"}

En el siguiente paso, defina la acción que se producirá cuando se cumpla la condición.

## Paso 3: Definir las acciones

Las acciones de regla de precios del carro de compras describen cómo se actualizan los precios cuando se cumplen las condiciones.

1. Desplácese hacia abajo hasta **[!UICONTROL Actions]**, y expanda ![Selector de expansión](../assets/icon-display-expand.png) la sección.

   ![Regla de precio del carro de compras: acciones ](./assets/price-rule-cart-actions.png){width="600" zoomable="yes"}

1. Establecer **[!UICONTROL Apply]** a una de las siguientes opciones de descuento:

   | Opción | Descripción |
   |------|-----------|
   | `Percent of product price discount` | Artículo de descuentos al restar un porcentaje del precio original. El descuento se aplica a cada artículo que cumpla los requisitos del carro de compras. Por ejemplo: Intro `10` in [!UICONTROL Discount Amount] por un precio actualizado un 10% inferior al precio original. |
   | `Fixed amount discount` | Descuenta un artículo restando una cantidad fija del precio original de cada artículo que cumple los requisitos del carro de compras. Por ejemplo: Intro `10` in [!UICONTROL Discount Amount] por un precio actualizado que es $10 menos que el precio original. |
   | Descuento de cantidad fija para todo el carro | Descuenta todo el carro de compras restando una cantidad fija del total del carro de compras. Por ejemplo: introduzca 10 en [!UICONTROL Discount Amount] para restar 10 $ del total del carro de compras. De forma predeterminada, el descuento se aplica solo al subtotal del carro de compras. Para aplicar el descuento al subtotal y al envío por separado, use _[!UICONTROL Apply to Shipping Amount]_opción. |
   | `Buy X get Y free` | Define una cantidad que el cliente debe comprar para recibir una cantidad de forma gratuita. (La [!UICONTROL Discount Amount] es Y.) |

   {style="table-layout:auto"}

   - Introduzca el **[!UICONTROL Discount Amount]** como un número, sin símbolos. Por ejemplo, dependiendo de la opción de descuento seleccionada, el número 10 puede indicar un porcentaje, una cantidad fija o una cantidad de artículos.

   - Para un _Comprar X obtener Y Gratis_ descuento, introduzca la cantidad en el **[!UICONTROL Discount Qty Step (Buy X)]** campo que el cliente debe comprar para recibir el descuento.

   - En el **[!UICONTROL Maximum Qty Discount is Applied To]** , introduzca la cantidad máxima del mismo producto que puede optar al descuento en la misma compra.

   - Establecer **[!UICONTROL Apply to Shipping Amount]** (![Alternar opción](../assets/toggle-yes.png)) como se indica a continuación:

     | Opción | Descripción |
     |------|-----------|
     | `Yes` | Aplica el importe de descuento por separado al subtotal y a los importes de envío. |
     | `No` | Aplica el importe del descuento sólo al subtotal. |

     {style="table-layout:auto"}

   - Para detener el procesamiento de otras reglas después de aplicar esta regla, establezca **[!UICONTROL Discard Subsequent Rules]** (![Alternar opción](../assets/toggle-yes.png)) a `Yes`. Esta configuración evita que se apliquen varios descuentos al mismo producto.

     | Opción | Descripción |
     |------|-----------|
     | `Yes` | Evita que se apliquen otras reglas de precios que puedan aplicarse a un producto. Cuando se aplican varias reglas de asignación de precios al mismo producto, solo la regla con la prioridad definida más alta (en una regla [!UICONTROL Priority] campo) se aplica al producto que cumple los requisitos. Esto evita que se apilen varias reglas de precios y proporciona descuentos adicionales no deseados. |
     | `No` | Permite que se apliquen varias reglas de precios al mismo producto. Esto podría provocar el apilamiento y el suministro de múltiples descuentos aplicados al precio del anuncio. |

     {style="table-layout:auto"}

     >[!IMPORTANT]
     >
     >Para descartar reglas subsiguientes, una regla de asignación de precios debe utilizar las prioridades definidas que se establecen en el campo Prioridad de cada regla y varias reglas no deben tener la misma prioridad definida Consulte **[!UICONTROL Priority]** en el _Añadir nueva regla_ paso.

1. Para definir la variable **_exacto_** productos del carro de compras afectados por la regla de precio del carro de compras, agregue **_adicional_** condiciones necesarias para la acción.

   Para determinar si el envío gratuito se aplica a los pedidos que cumplen las condiciones, establezca **[!UICONTROL Free Shipping]** a uno de los siguientes:

   | Opción | Descripción |
   |------|-----------|
   | `No` | El envío gratuito no está disponible. |
   | `For matching items only` | El envío gratuito solo está disponible para artículos que cumplan las condiciones de la regla. |
   | `For shipment with matching items` | El envío gratuito está disponible para cualquier envío que incluya artículos coincidentes. El [Envío gratuito](../stores-purchase/shipping-free.md) el método de envío debe estar habilitado para poder utilizar esta opción. |

   {style="table-layout:auto"}

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Para **[!UICONTROL Add Rewards Points]**, introduzca el número fijo de puntos que gana el cliente **_una vez_** por pedido siempre que se aplique la regla de precio del carro de compras.

   Si los puntos de recompensa no están activados, deje este campo en blanco.

1. Cuando termine, haga clic en **[!UICONTROL Save and Continue Edit]**.

## Paso 4: Completar las etiquetas

La etiqueta aparece en la sección de totales del pedido para identificar el descuento. El texto de la etiqueta se incluye entre paréntesis, después de la palabra `Discount`. Puede escribir una etiqueta predeterminada para todas las vistas de tiendas o escribir una etiqueta diferente para cada vista.

![Carrito de tienda - etiquetas de descuento](./assets/order-totals-section-discount-special.png){width="600"}

1. Desplácese hacia abajo hasta **[!UICONTROL Labels]**, y expanda ![Selector de expansión](../assets/icon-display-expand.png)la sección.

1. Escriba el texto que desee utilizar como **[!UICONTROL Default Rule Label for All Store Views]**.

   ![Regla de precio del carro de compras: etiqueta predeterminada](./assets/label-default.png){width="600" zoomable="yes"}

1. Si la tienda tiene varias vistas o varios sitios web con varias vistas, escriba el texto de etiqueta adecuado para cada uno.

   Por ejemplo, si cada vista de tienda está en un idioma diferente, introduzca la traducción de la etiqueta para cada vista.

   ![Almacenar etiquetas específicas](./assets/label-store-specific.png){width="600" zoomable="yes"}

## Paso 5: Agregar bloques dinámicos relacionados (opcional)

{{ee-feature}}

[Bloques dinámicos](../content-design/dynamic-blocks.md) Las que estén asociadas con la regla aparecerán en la tienda siempre que se cumplan las condiciones.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Related Dynamic Blocks]** sección.

1. Utilice el [filtros de búsqueda](../getting-started/admin-workspace.md) para localizar los bloques que desea asociar con la regla.

1. Seleccione la casilla de verificación de la primera columna para asociar el bloque con la regla.

   Para obtener más información, consulte [Bloques dinámicos en reglas de precios](../content-design/dynamic-blocks-price-rules.md).

## Paso 6: Guardar y probar la regla

1. Cuando termine, haga clic en **[!UICONTROL Save Rule]**.

1. Pruebe la regla para asegurarse de que funciona correctamente.

   Las reglas de precios se procesan automáticamente con otras reglas del sistema cada noche. Cuando cree una regla de precios, deje tiempo suficiente para que entre en el sistema. Pruebe también la regla para asegurarse de que funciona correctamente. A medida que se añaden nuevas reglas, Commerce vuelve a calcular los precios y las prioridades en consecuencia.

## Demostración de regla de precio del carro

Vea este vídeo para obtener más información sobre la creación de reglas de precios de carro de compras:

>[!VIDEO](https://video.tv.adobe.com/v/343835?quality=12)

## Descripciones de campos

### [!UICONTROL Rule Information]

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Rule Name] | (Obligatorio) El nombre de la regla es para referencia interna. |
| [!UICONTROL Description] | Una descripción de la regla debe incluir su propósito y explicar cómo se utiliza. |
| [!UICONTROL Active] | (Obligatorio) Determina si la regla está activa en el almacén. Opciones: `Yes` / `No` |
| [!UICONTROL Websites] | (Obligatorio) Identifica los sitios web en los que se puede utilizar la regla. |
| [!UICONTROL Customer Groups] | (Obligatorio) Identifica los grupos de clientes a los que se aplica la regla. |
| [!UICONTROL Coupon] | (Obligatorio) Indica si hay un cupón asociado a la regla. Opciones: <br/>**[!UICONTROL No Coupon]**: No hay ningún cupón asociado a la regla.<br/>**[!UICONTROL Specific Coupon]** : Se asocia un cupón específico con la regla. <br/>**[!UICONTROL Coupon Code]**: Cuando se le solicite, introduzca el código de cupón que debe introducir el cliente para aprovechar la promoción.<br/>**[!UICONTROL Use Auto Generation]** : Seleccione la casilla de verificación para generar automáticamente varios códigos de cupón que se puedan utilizar con la promoción. <br/>**[!UICONTROL Auto]**- Muestra el _[!UICONTROL Manage Coupon Codes]_para definir el formato de los códigos de cupón que se van a generar. |
| [!UICONTROL Uses per Coupon] | Determina cuántas veces se puede utilizar el código de cupón. Si no hay límite, deje el campo en blanco. |
| [!UICONTROL Uses per Customer] | Determina cuántas veces el mismo cliente registrado que pertenece a un grupo de clientes seleccionado puede utilizar la regla de precio del carro de compras. No se aplica a los compradores invitados que sean miembros del grupo de clientes NOT LOGGED IN, ni a los clientes que compren sin iniciar sesión en sus cuentas. Si no hay límite, déjelo en blanco. |
| [!UICONTROL Priority] | Un número que indica la prioridad de esta regla en relación con otras. La prioridad más alta es un número `1`. |
| [!UICONTROL Public in RSS Feed] | Determina si la promoción está incluida en la fuente RSS pública de la tienda. Opciones:  `Yes` / `No` |
| [!UICONTROL From] | ![Magento Open Source](../assets/open-source.svg) (Solo Magento Open Source) La primera fecha en que se puede utilizar el cupón. |
| [!UICONTROL To] | ![Magento Open Source](../assets/open-source.svg) (Solo Magento Open Source) Última fecha en la que se puede utilizar el cupón. |

{style="table-layout:auto"}

### [!UICONTROL Conditions]

Especifica las condiciones que deben cumplirse antes de que la regla de precios del carro de compras entre en acción. Si se deja en blanco, la regla se aplica a todos los productos del carro de compras. Las condiciones se pueden basar en cualquier combinación de atributos del carro de compras y del producto. Sin embargo, [opciones personalizables](../catalog/settings-advanced-custom-options.md) no se puede hacer referencia a en las condiciones de regla de precios de carrito.

### [!UICONTROL Actions]

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Apply] | Determina el tipo de cálculo que se aplica a la compra. Opciones: <br/>**[!UICONTROL Percent of product price discount]**- Artículo de descuentos al restar un porcentaje del precio original. Por ejemplo: Intro `10` in _[!UICONTROL Discount Amount]_por un precio actualizado un 10% inferior al precio original.<br/>**[!UICONTROL Fixed amount discount]**- Descuentos de artículos al restar una cantidad fija del precio original de cada artículo que cumple los requisitos del carro de compras. Por ejemplo: Intro `10` in_[!UICONTROL Discount Amount]_ por un precio actualizado que es $10 menos que el precio original. <br/>**[!UICONTROL Fixed amount discount for whole cart]**: Descuenta todo el carro de compras restando una cantidad fija del subtotal del carro de compras. Por ejemplo: Intro `10` in _[!UICONTROL Discount Amount]_para restar 10 $ del subtotal del carrito de compra. De forma predeterminada, el descuento se aplica solo al subtotal del carro de compras. Para aplicar el descuento al subtotal y al envío por separado, consulte_Aplicar al importe de envío _.<br/>**[!UICONTROL Buy X Get Y Free (discount amount is Y)]**- Define una cantidad que el cliente debe comprar para recibir una cantidad de forma gratuita. (La_[!UICONTROL Discount Amount]_ es Y.) |
| [!UICONTROL Discount Amount] | (Obligatorio) El importe del descuento ofrecido. |
| [!UICONTROL Maximum Qty Discount is Applied To] | Establece el número máximo de productos a los que se puede aplicar el descuento en la misma compra. |
| [!UICONTROL Discount Qty Step (Buy X)] | Establece el número de productos representados por `X` en un `Buy X Get Y Free` promoción. |
| [!UICONTROL Apply to Shipping Amount] | Determina si el descuento se aplica por separado a los importes de subtotal y envío. De lo contrario, sólo se aplica al subtotal. Opciones: `Yes` / `No` |
| [!UICONTROL Discard Subsequent Rules] | Determina si se pueden aplicar reglas de prioridad inferior (1 es la prioridad más alta) al producto cuando esta regla de precios del carro de compras coincide. Active esta opción para evitar que se apliquen varios descuentos al mismo producto. Opciones: `Yes` / `No` |
| [!UICONTROL Free Shipping] | Determina si se incluye el envío gratuito en la promoción y, si es así, para qué artículos. Opciones: <br/>**[!UICONTROL No]**- El envío gratuito no está disponible para la regla actual.<br/>**[!UICONTROL For matching items only]** - El envío gratuito solo está disponible para artículos específicos del carro de compras que coincidan con la regla. <br/>**[!UICONTROL For shipment with matching items]**- Envío gratuito disponible para todos los artículos del carro de compras. El [Envío gratuito](../stores-purchase/shipping-free.md) el método de envío debe estar habilitado para poder utilizar esta opción. |
| [!UICONTROL Add Reward Points] | ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Especifica el número de [puntos de recompensa](rewards-loyalty.md) que obtiene el cliente siempre que se aplica la regla de precio. |

{style="table-layout:auto"}

### [!UICONTROL Labels]

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Default Rule Label for All Store Views] | Una etiqueta predeterminada que identifica el descuento y se puede utilizar para todas las vistas de la tienda. |
| [!UICONTROL Store View Specific Labels] | Si procede, especifica una etiqueta diferente para identificar el descuento en cada vista de tienda. |

{style="table-layout:auto"}

### [!UICONTROL Related Dynamic Blocks]

{{ee-feature}}

Identifica cualquier [bloques dinámicos](../content-design/dynamic-blocks.md) que están asociados a la regla.
