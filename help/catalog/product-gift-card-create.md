---
title: Producto de tarjeta regalo
description: Aprenda a crear un producto de tarjeta regalo que produzca un código único que un cliente destinatario pueda canjear durante el cierre de compra.
exl-id: bc4b60fe-10b3-4d17-85ce-35c2720c90a2
feature: Catalog Management, Products, Gift
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 0%

---

# Producto de tarjeta regalo

{{ee-feature}}

Cada tarjeta regalo tiene un código único, que solo un cliente puede canjear durante el pago. A [grupo de códigos](../stores-purchase/product-gift-card-accounts.md#step-3-establish-the-gift-card-code-pool) debe establecerse antes de poder vender tarjetas de regalo. Consulte [Flujo de trabajo de tarjeta regalo](../stores-purchase/product-gift-card-workflow.md) para obtener información sobre cómo se canjean las tarjetas regalo en el carro de compras.

![Página de productos de tarjeta regalo](./assets/storefront-giftcard-product-page.png){width="700" zoomable="yes"}

Hay tres tipos de productos de tarjeta de regalo:

- **Virtual** - Se envía una tarjeta regalo virtual a la dirección de correo electrónico del destinatario, que es necesaria durante la compra de la tarjeta regalo. No es necesaria una dirección de envío.

- **Físico** - Se envía una tarjeta de regalo física a la dirección del destinatario, que es necesaria durante la compra de la tarjeta de regalo.

- **Combinado** - Se envía una tarjeta regalo combinada y se envía por correo electrónico al destinatario. El correo electrónico y la dirección de envío del destinatario son obligatorios durante la compra de la tarjeta regalo.

## Crear un producto de tarjeta regalo

Las siguientes instrucciones muestran el proceso de creación de una tarjeta regalo mediante una [plantilla de producto](attribute-sets.md), campos obligatorios y configuración básica. Cada campo obligatorio está marcado con un asterisco rojo (`*`). Cuando termine los conceptos básicos, puede completar el resto de la configuración del producto según sea necesario.

### Paso 1: Elija el tipo de producto

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. En la esquina superior derecha de la _[!UICONTROL Add Product]_( ![Flecha de menú](../assets/icon-menu-down-arrow-red.png){width="25"}  ), seleccione **[!UICONTROL Gift Card]**.

   ![Añadir tarjeta regalo](./assets/product-add-gift-card.png){width="700" zoomable="yes"}

### Paso 2: Selección del conjunto de atributos

Puede usar el valor predeterminado `Gift Card` establezca un atributo o elija otro. Para elegir el conjunto de atributos que se utiliza como plantilla para el producto, realice una de las siguientes acciones:

- Haga clic en en **[!UICONTROL Attribute Set]** e introduzca todo o parte del nombre del conjunto de atributos.

- En la lista mostrada, elija el conjunto de atributos que desea utilizar.

![Elegir conjunto de atributos](./assets/product-create-choose-attribute-set-gift-card.png){width="600" zoomable="yes"}

### Paso 3: complete la configuración necesaria

1. Introduzca una **[!UICONTROL Product Name]** para la tarjeta regalo.

   También puede indicar el tipo de tarjeta regalo en el nombre. Por ejemplo, _Tarjeta de regalo virtual de Luma_.

1. Introduzca una **[!UICONTROL SKU]** para el producto.

   De forma predeterminada, el Nombre del producto se utiliza como SKU predeterminado.

1. Establecer **[!UICONTROL Card Type]** a uno de los siguientes:

   - `Virtual` - Las tarjetas de regalo virtuales se entregan por correo electrónico al destinatario.
   - `Physical` - Las tarjetas de regalo físicas pueden ser producidas en masa por adelantado y en relieve con códigos únicos.
   - `Combined` - Una tarjeta de regalo combinada tiene las características de una tarjeta de regalo virtual y física.

   ![Tipo de tarjeta regalo](./assets/product-create-gift-card-type.png){width="600" zoomable="yes"}

1. Para ofrecer al cliente una opción de importes fijos, haga clic en **[!UICONTROL Add Amount]** e introduzca el primer valor fijo de la tarjeta como decimal.

   Para introducir la selección de importes fijos, repita este paso para cada uno.

1. Para ofrecer a los clientes la posibilidad de establecer el valor de la tarjeta regalo, haga lo siguiente:

   - Establecer **[!UICONTROL Open Amount]** hasta `Yes`.

   - Para definir el rango de valores mínimos y máximos aceptables, introduzca la variable **[!UICONTROL Open Amount From]** y **[!UICONTROL To]** valores.

   Puede crear tarjetas regalo con precios fijos, precios de cantidad abierta o ambos.

   ![Importes de tarjeta regalo](./assets/product-create-gift-card-amounts.png){width="600" zoomable="yes"}

### Paso 4: completar la configuración básica

1. Para una tarjeta regalo física o combinada, ingrese el **[!UICONTROL Quantity]** en stock.

1. Si la tarjeta regalo que se va a enviar, introduzca la **[!UICONTROL Weight]** del paquete.

1. En el **[!UICONTROL Categories]** , elija `Gift Card`.

Puede haber atributos individuales adicionales que describan el producto. La selección varía según el conjunto de atributos y puede completarlos más adelante.

### Paso 5: Completar la información de la tarjeta regalo

El _[!UICONTROL Gift Card Information]_de la configuración del producto se puede utilizar para anular la [configuración de tarjeta regalo](../configuration-reference/sales/gift-cards.md) configuración que determina cómo se administra la tarjeta.

1. Desplácese hacia abajo hasta el _[!UICONTROL Gift Card Information]_sección.

   La configuración predeterminada de esta sección viene determinada por la configuración del sistema.

   ![Información de tarjeta regalo](./assets/product-gift-card-information.png){width="600" zoomable="yes"}

1. Cambie los campos adicionales según cómo desee que funcione la tarjeta regalo:

   - **[!UICONTROL Treat Balance as Store Credit]** - Determina si el titular de la tarjeta regalo puede canjear el saldo como crédito de la tienda.

   - **[!UICONTROL Lifetime (days)]** - Determina el número de días después de la compra hasta que caduque la tarjeta regalo. Si no desea establecer un límite para la duración de la tarjeta, deje este campo en blanco.

   - **[!UICONTROL Allow Message]** - Determina si el comprador de la tarjeta regalo puede introducir un mensaje para el destinatario. Se puede incluir un mensaje de regalo para tarjetas de regalo virtuales (por correo electrónico) y físicas (enviadas).

   - **[!UICONTROL Email Template]** : Determina la plantilla de correo electrónico que se utiliza para la notificación enviada al destinatario de una tarjeta de regalo.

### Paso 6: Completar la información del producto

Rellene la información de las secciones siguientes según sea necesario:

- [Contenido](product-content.md)
- [Imágenes y vídeos](product-images-and-video.md)
- [Productos relacionados, ampliación de ventas y ventas cruzadas](related-products-up-sells-cross-sells.md)
- [Optimización del motor de búsqueda](product-search-engine-optimization.md)
- [Opciones personalizables](settings-advanced-custom-options.md)
- [Productos en sitios web](settings-basic-websites.md)
- [Diseño](settings-advanced-design.md)
- [Opciones de regalo](product-gift-options.md)

### Paso 7: Publicar el producto

1. Si está listo para publicar el producto en el catálogo, configure el **Activar producto** cambiar a `Yes`.

1. Realice una de las siguientes acciones:

   **Método 1:** Guardar y previsualizar

   - En la esquina superior derecha, haga clic en **[!UICONTROL Save]**.

   - Para ver el producto en tu tienda, elige **[!UICONTROL Customer View]** en el _Administrador_ ( ![Flecha de menú](../assets/icon-menu-down-arrow-black.png) ) menú,

   ![Vista de cliente](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **Método 2:** Guardar y cerrar

   En el _[!UICONTROL Save]_( ![Flecha de menú](../assets/icon-menu-down-arrow-red.png){width="25"} ), seleccione **[!UICONTROL Save & Close]**.

## Cosas que recordar

- A _grupo de códigos_ Antes de poder ofrecer una tarjeta regalo para la venta, es necesario generar una lista de números únicos.

- Las tarjetas regalo se pueden configurar en `Redeemable` o `Non-Redeemable`.

- Los impuestos son **_no aplicado_** a las tarjetas regalo durante la compra de la tarjeta regalo. Los impuestos se aplican a los productos solo cuando se utiliza una tarjeta de regalo comprada para comprar productos.

- La duración de una tarjeta regalo puede ser ilimitada o fijarse en un número determinado de días.

- El valor de una tarjeta regalo se puede establecer en una cantidad fija o en una cantidad abierta con un valor mínimo y máximo.

- Se puede crear una cuenta de tarjeta regalo para el cliente cuando se realiza el pedido o en el momento de la factura.
