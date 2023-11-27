---
title: Producto virtual
description: Aprenda a crear un producto virtual que represente un elemento no tangible, como una suscripción, un servicio, una garantía o una suscripción.
exl-id: 8788ba04-e911-429e-9e48-ce589f0c9fa1
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Producto virtual

Los productos virtuales, o bienes digitales, representan elementos no tangibles como membresías, servicios, garantías o suscripciones y descargas digitales de libros, música, videos u otros productos. Los productos virtuales se pueden vender individualmente o incluir como parte de la [Producto agrupado](product-create-grouped.md), [Producto configurable](product-create-configurable.md), o [Producto agrupado](product-create-bundle.md) tipos de productos.

Aparte de la ausencia de la _[!UICONTROL Weight]_, el proceso de creación de un producto virtual y de un producto simple es el mismo. Las siguientes instrucciones muestran el proceso de creación de un producto virtual mediante una [plantilla de producto](attribute-sets.md), campos obligatorios y configuración básica. Cuando termine los conceptos básicos, puede completar el resto de la configuración del producto según sea necesario.

>[!NOTE]
>
>PayPal ha dejado de ofrecer asistencia para la venta de artículos digitales a través del proceso de pago y envío de PayPal Express. Se recomienda utilizar cualquiera de las siguientes opciones [PayPal Payments Standard](../stores-purchase/paypal-payments-standard.md) o cualquier otra pasarela de pago de PayPal para procesar cualquier pedido que incluya productos virtuales.

![Producto virtual](./assets/product-virtual-membership.png){width="700" zoomable="yes"}

## Paso 1: Elija el tipo de producto

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. En el _[!UICONTROL Add Product]_( ![Flecha de menú](../assets/icon-menu-down-arrow-red.png){width="25"} ) en la esquina superior derecha, seleccione **[!UICONTROL Virtual Product]**.

   ![Añadir producto virtual](./assets/product-add-virtual.png){width="700" zoomable="yes"}

## Paso 2: Selección del conjunto de atributos

Para elegir el [conjunto de atributos](attribute-sets.md) que se utiliza como plantilla para el producto, realice una de las siguientes acciones:

- Haga clic en en **[!UICONTROL Attribute Set]** e introduzca todo o parte del nombre del conjunto de atributos.

- En la lista mostrada, elija el conjunto de atributos que desea utilizar.

El formulario se actualiza para reflejar el cambio.

![Elegir conjunto de atributos](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Paso 3: complete la configuración necesaria

1. Introduzca el **[!UICONTROL Product Name]**.

1. Aceptar el valor predeterminado **[!UICONTROL SKU]** que se basa en el nombre del producto o introduzca otro.

1. Introduzca el producto **[!UICONTROL Price]**.

1. Como el producto aún no está listo para publicar, establezca **[!UICONTROL Enable Product]** hasta `No`.

1. Clic **[!UICONTROL Save]** y continuar.

   Cuando se guarda el producto, la variable [Vista de tienda](introduction.md#product-scope) el selector aparece en la esquina superior izquierda.

1. Elija la **[!UICONTROL Store View]** donde vaya a estar disponible el producto.

   ![Elegir vista de tienda](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Paso 4: completar la configuración básica

1. Establecer **[!UICONTROL Tax Class]** a uno de los siguientes:

   - `None`
   - `Taxable Goods`

1. Introduzca el **[!UICONTROL Quantity]** del producto que está en stock y haga lo siguiente:

   - Aceptar el valor predeterminado **[!UICONTROL Stock Status]** configuración de `In Stock`.

     Como no se envía un producto virtual, la variable **[!UICONTROL Weight]** Este campo no se utiliza.

   - Aceptar el valor predeterminado **[!UICONTROL Visibility]** configuración de `Catalog, Search`.

   >[!NOTE]
   >
   >Si activa [Inventory management](../inventory-management/introduction.md), los comerciantes de un solo origen establecen la cantidad en esta sección. Los comerciantes de varios orígenes agregan orígenes y cantidades en la sección Orígenes. Consulte lo siguiente _Asignación de Orígenes y Cantidades (Inventory management)_ sección.

1. Para asignar **[!UICONTROL Categories]** para seleccionar el producto, haga clic en **[!UICONTROL Select…]** y realice una de las acciones siguientes:

   **Elija una categoría existente**:

   - Empiece a escribir en el cuadro hasta que encuentre una coincidencia.

   - Seleccione la casilla de verificación de la categoría que se va a asignar.

   **Crear una categoría**:

   - Haga clic **[!UICONTROL New Category]**.

   - Introduzca el **[!UICONTROL Category Name]** y elija la **[!UICONTROL Parent Category]**, que determina su posición en la estructura de menú.

   - Haga clic **[!UICONTROL Create Category]**.

   Puede haber atributos individuales adicionales que describan el producto. La selección varía según el conjunto de atributos y puede completarla más adelante.

### Asignación de orígenes y cantidades ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## Paso 5: Completar la información del producto

Rellene la información de las secciones siguientes según sea necesario:

- [Contenido](product-content.md)
- [Imágenes y vídeos](product-images-and-video.md)
- [Optimización del motor de búsqueda](product-search-engine-optimization.md)
- [Productos relacionados, ampliación de ventas y ventas cruzadas](related-products-up-sells-cross-sells.md)
- [Opciones personalizables](settings-advanced-custom-options.md)
- [Productos en sitios web](settings-basic-websites.md)
- [Diseño](settings-advanced-design.md)
- [Opciones de regalo](product-gift-options.md)

>[!NOTE]
>
>El _[!UICONTROL Is this downloadable product?]_La opción está desactivada de forma predeterminada. Al habilitar esta función para un producto virtual, se crea el producto [Descargable](product-create-downloadable.md#downloadable-product).

## Paso 6: Publicar el producto

1. Si está listo para publicar el producto en el catálogo, establezca **[!UICONTROL Enable Product]** hasta `Yes`.

1. Realice una de las siguientes acciones:

   - **Método 1:** Guardar y previsualizar

      - En la esquina superior derecha, haga clic en **[!UICONTROL Save]**.

      - Para ver el producto en tu tienda, elige **[!UICONTROL Customer View]** en el _Administrador_ ( ![Flecha de menú](../assets/icon-menu-down-arrow-black.png) ) menú.

     La tienda se abre en una nueva pestaña del explorador.

     ![Vista de cliente](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Método 2:** Guardar y cerrar

     En el _[!UICONTROL Save]_(![Flecha de menú](../assets/icon-menu-down-arrow-red.png){width="25"} ), seleccione **[!UICONTROL Save & Close]**.

## Cosas que recordar

- Los productos virtuales se utilizan para productos no tangibles como servicios, suscripciones y garantías.

- Los productos virtuales son muy parecidos a los productos simples, pero sin peso.

- Las opciones de envío no aparecen durante el cierre de compra a menos que haya un producto tangible en el carro de compras.
