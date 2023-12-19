---
title: Paquete de productos
description: Aprenda a crear un paquete de productos que permita a los compradores crear un producto personalizado en su tienda.
exl-id: dfa31eb8-2330-44eb-889b-5d10ce56ef13
feature: Catalog Management, Products
source-git-commit: e38958bb57251ccc9409b849abc1aadb82ff0a54
workflow-type: tm+mt
source-wordcount: '1551'
ht-degree: 0%

---

# Paquete de productos

Un paquete es un _construya su propio_, producto personalizable. Cada elemento de un paquete se puede basar en uno de los siguientes tipos de productos:

- [Producto sencillo](product-create-simple.md)
- [Producto virtual](product-create-virtual.md)
- [Producto descargable](product-create-downloadable.md)
- [Producto virtual](product-create-virtual.md)

![Paquete de productos](./assets/product-bundle.png){width="700" zoomable="yes"}

Las opciones aparecen cuando el cliente hace clic en **[!UICONTROL Customize]** o **[!UICONTROL Add to Cart]**. Dado que los productos incluidos en el paquete varían, el SKU, el precio y el peso se pueden establecer en un valor dinámico o fijo.

>[!NOTE]
>
>El precio mínimo anunciado (MAP) no está disponible para los productos agrupados que utilizan precios dinámicos.

>[!NOTE]
>
>El producto del paquete principal siempre se muestra como un producto de mejora de ventas para todos sus productos secundarios automáticamente.

If [Compra instantánea](../stores-purchase/checkout-instant-purchase.md) está disponible, la variable _Compra instantánea_ aparece debajo de _Añadir al carro_ para cada elemento del paquete.

![Personalizar paquete](./assets/product-bundle-customize.png){width="600" zoomable="yes"}

Las siguientes instrucciones le guían a través del proceso de creación de un producto agrupado mediante una [plantilla de producto](attribute-sets.md), campos obligatorios y configuración básica. Cada campo obligatorio está marcado con un asterisco rojo (`*`). Cuando termine los conceptos básicos, puede completar el resto de la configuración del producto según sea necesario.

## Paso 1: Elija el tipo de producto

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. En la esquina superior derecha de la _[!UICONTROL Add Product]_( ![Flecha de menú](../assets/icon-menu-down-arrow-red.png){width="25"} ), seleccione **[!UICONTROL Bundle Product]**.

   ![Añadir producto del paquete](./assets/product-add-bundle.png){width="700" zoomable="yes"}

## Paso 2: Selección del conjunto de atributos

Para elegir el [conjunto de atributos](attribute-sets.md) que se utiliza como plantilla para el producto, realice una de las siguientes acciones:

- Para **[!UICONTROL Search]**, introduzca el nombre del conjunto de atributos,
- En la lista, elija el conjunto de atributos que desea utilizar.

El formulario se actualiza para reflejar el cambio.

![Elegir plantilla](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Paso 3: complete la configuración necesaria

1. Introduzca el producto **[!UICONTROL Product Name]**.

1. Acepte el valor predeterminado **[!UICONTROL SKU]** que se basa en el nombre del producto o introduzca un valor diferente.

   Para determinar el tipo de SKU asignado a cada elemento del paquete, haga lo siguiente:

   - A **[!UICONTROL Dynamic SKU]** se puede asignar automáticamente a cada elemento del paquete añadiendo un sufijo al SKU predeterminado. De forma predeterminada, se establece en `Yes`.

   - Si prefiere asignar un SKU único para cada elemento del paquete, establezca **[!UICONTROL Dynamic SKU]** hasta `No`.

   ![SKU dinámico y precio](./assets/product-bundle-manual-sku.png){width="600" zoomable="yes"}

1. Para determinar el precio del paquete, realice una de las siguientes acciones:

   - Para que el precio refleje las opciones elegidas por el cliente, establezca **[!UICONTROL Dynamic Price]** hasta `Yes` y salir **[!UICONTROL Price]** en blanco.

   - Para cargar un precio fijo por el paquete, establezca **[!UICONTROL Dynamic Price]** hasta `No` e introduzca la variable **[!UICONTROL Price]** que desea cobrar por el paquete.

   >[!NOTE]
   >
   >[!UICONTROL Special Price] y [!UICONTROL Customer Group Price] (Precio de nivel) siempre se establecen como porcentaje de descuento para todos los tipos de productos de paquete.

1. Como el producto aún no está listo para publicar, establezca **[!UICONTROL Enable Product]** hasta `No`.

1. Clic **[!UICONTROL Save]** y continuar.

   Cuando se guarda el producto, la variable [Vista de tienda](introduction.md#product-scope) el selector aparece en la esquina superior izquierda.

1. Elija la **[!UICONTROL Store View]** donde vaya a estar disponible el producto.

   ![Elegir vista de tienda](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Paso 4: completar la configuración básica

1. Si el paquete tiene Precios fijos, establezca **[!UICONTROL Tax Class]** a uno de los siguientes:

   - `None`
   - `Taxable Goods`

   Si el paquete tiene Asignación de Precios Dinámica, el impuesto se determina para **_cada_** artículo agrupado. Si el paquete tiene Precios fijos, el impuesto se determina para la variable **_entero_** paquete de producto.

1. Tome nota de lo siguiente:

   - El **[!UICONTROL Quantity]** no está disponible porque el valor se determina para cada elemento del paquete.

   - De forma predeterminada, la variable **[!UICONTROL Stock Status]** se establece en `In Stock`.

1. Para determinar el peso del paquete, realice una de las siguientes acciones:

   - Para que el peso refleje las opciones elegidas por el cliente, establezca **[!UICONTROL Dynamic Weight]** set `Yes` y salir **[!UICONTROL Weight]** en blanco.

   - Para asignar un peso fijo al paquete, establezca **[!UICONTROL Dynamic Weight]** hasta `No` e introduzca la variable **[!UICONTROL Weight]** del paquete.

   ![Peso dinámico](./assets/product-bundle-dynamic-weight.png){width="600" zoomable="yes"}

1. Para incluir el producto en la lista de [nuevos productos](../content-design/widget-new-products-list.md), seleccione la **[!UICONTROL Set Product as New]** casilla de verificación

1. Aceptar el valor predeterminado **[!UICONTROL Visibility]** configuración de `Catalog, Search`.

1. Para asignar _[!UICONTROL Categories]_para seleccionar el producto, haga clic en **[!UICONTROL Select…]**y realice una de las acciones siguientes:

   **Elija una categoría existente:**

   - Empiece a escribir en el cuadro hasta que encuentre una coincidencia.

   - Seleccione la casilla de verificación de cada categoría que se va a asignar.

   ![Seleccione una o más categorías para el producto del paquete](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **Crear una categoría:**

   - Clic **[!UICONTROL New Category]**.

   - Introduzca el **[!UICONTROL Category Name]** y elija la **[!UICONTROL Parent Category]**, que determina su posición en la estructura de menú.

   - Clic **[!UICONTROL Create Category]**.

1. Elija la **[!UICONTROL Country of Manufacture]**.

   Puede haber atributos adicionales que describan el producto. La selección varía según el conjunto de atributos y puede completarlos más adelante.

## Paso 5: Añadir los elementos del paquete

El _[!UICONTROL Bundle Items]_se utiliza para añadir elementos a un tipo de producto Paquete y editar la selección actual de elementos.

![Elementos de paquete definidos para un producto](./assets/product-bundle-items-ball.png){width="600" zoomable="yes"}

1. Desplácese hacia abajo hasta el _Elementos de paquete_ sección y conjunto **[!UICONTROL Ship Bundle Items]** a uno de los siguientes:

   - `Separately`
   - `Together`

   Si selecciona `Together`, todos los elementos del paquete deben asignarse al mismo [origen](../inventory-management/sources-manage.md).

1. Clic **[!UICONTROL Add Option]** y haga lo siguiente:

   - Introduzca una **[!UICONTROL Option Title]** para utilizarse como etiqueta de campo.

   - Establecer **[!UICONTROL Input Type]** a uno de los siguientes:

      - `Drop-down`
      - `Radio buttons`
      - `Checkbox`
      - `Multiple Select`

   - Para que el campo sea una entrada obligatoria, seleccione la **[!UICONTROL Required]** casilla de verificación

   - Clic **[!UICONTROL Add Products to Option]** y active la casilla de verificación de cada producto que desee incluir en esta opción.

     Si hay muchos productos, utilice los filtros de lista y los controles de paginación para encontrar los productos que necesita.

   - Clic **[!UICONTROL Add Selected Products]**.

     ![Añadir productos seleccionados](./assets/product-bundle-add-products-to-option.png){width="600" zoomable="yes"}

   - Después de que los elementos aparezcan en la _Opciones_ , elija un elemento para que sea el **[!UICONTROL Default]** selección.

   - En el _Cantidad predeterminada_ , introduzca la cantidad de cada artículo que se añadirá al paquete cuando un cliente elija el artículo.

   - Para permitir que los clientes cambien la cantidad de un artículo agrupado, seleccione **[!UICONTROL User Defined]**.


     >[!NOTE]
     >
     >La cantidad puede ser un valor preestablecido o definido por el usuario. Sin embargo, no asigne los _[!UICONTROL User Defined]_propiedad para marcar la casilla de verificación o seleccionar varios tipos de entrada.

     De forma predeterminada, el cliente no puede cambiar la cantidad predeterminada que se incluye en un artículo agrupado. Sin embargo, el cliente puede introducir la cantidad del artículo que se va a incluir en el paquete.

     Por ejemplo, si la cantidad predeterminada de la bola de estado de Sprite está definida en `2` y los pedidos de los clientes `4` de esa opción de paquete, el número total de bolas compradas es `8`.

     ![Detalles del elemento](./assets/product-bundle-item-detail.png){width="600" zoomable="yes"}

1. Repita estos pasos para cada elemento que desee agregar al paquete.

1. Para cambiar el orden de los elementos en una sección del paquete, haga clic en _Mover_ ( ![Icono Mover](../assets/icon-move.png) ) icono al principio de la fila y arrastre el elemento a su posición.

   ![Cambiar el orden de los elementos del paquete](./assets/product-bundle-items-move.png){width="600" zoomable="yes"}

   El orden de los elementos también se puede cambiar en los datos de un paquete de productos exportado y, a continuación, volver a importarse en el catálogo. Para obtener más información, consulte [Importación de productos agrupados](../systems/data-transfer-bundle-products.md).

   Para obtener una mejor vista del espacio de trabajo, contraiga primero cada sección y, a continuación, arrástrela a su posición.

1. Para eliminar cualquier elemento del paquete, haga clic en **[!UICONTROL Delete]** ( ![Icono de papelera](../assets/icon-delete-trashcan.png) ) icono.

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

## Paso 6: Completar la información del producto

Desplácese hacia abajo y complete la información de las siguientes secciones según sea necesario:

- [Contenido](product-content.md)
- [Imágenes y vídeos](product-images-and-video.md)
- [Optimización del motor de búsqueda](product-search-engine-optimization.md)
- [Productos relacionados, ampliación de ventas y ventas cruzadas](related-products-up-sells-cross-sells.md)
- [Opciones personalizables](settings-advanced-custom-options.md)
- [Productos en sitios web](settings-basic-websites.md)
- [Diseño](settings-advanced-design.md)
- [Opciones de regalo](product-gift-options.md)

## Paso 7: Publicar el producto

1. Si está listo para publicar el producto en el catálogo, establezca **[!UICONTROL Enable Product]** hasta `Yes` ( ![Alternar sí](../assets/toggle-yes.png) ).

1. Realice una de las siguientes acciones:

   **Método 1:** Guardar y previsualizar

   - En la esquina superior derecha, haga clic en **[!UICONTROL Save]**.

   - Para ver el producto en tu tienda, elige **[!UICONTROL Customer View]** en el _Administrador_ ( ![Flecha de menú](../assets/icon-menu-down-arrow-black.png) ) menú.

     La tienda se abre en una nueva pestaña del explorador.

   ![Vista de cliente](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **Método 2:** Guardar y cerrar

   En el _[!UICONTROL Save]_( ![Flecha de menú](../assets/icon-menu-down-arrow-red.png){width="25"} ), seleccione **[!UICONTROL Save & Close]**.

## Controles de entrada

| Control | Descripción | Ejemplo |
|--- |--- |--- |
| [!UICONTROL Drop-down] | Muestra una lista desplegable de opciones con el nombre del producto y el precio. Solo se puede seleccionar un elemento. | ![Desplegable](./assets/product-bundle-input-type-drop-down.png){width="200"} |
| [!UICONTROL Radio Buttons] | Muestra un botón de opción para cada opción, seguido del nombre y el precio del producto. Solo se puede seleccionar un elemento. | ![Botones de opción](./assets/product-bundle-input-type-radio-buttons.png){width="200"} |
| [!UICONTROL Checkbox] | Muestra una casilla de verificación para cada opción, seguida del nombre y el precio del producto. Se pueden seleccionar varios elementos. | ![Casilla](./assets/product-bundle-input-type-checkbox.png){width="200"} |
| [!UICONTROL Multiple Select] | Muestra una lista de opciones con el nombre del producto y el precio. Para seleccionar varios elementos, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada elemento. | ![Selección múltiple](./assets/product-bundle-input-type-multiple-select.png){width="200"} |

{style="table-layout:auto"}

## Descripciones de campos

| Campo | Descripción |
|--- |--- |
| [!UICONTROL SKU] | Determina si a cada elemento se le asigna un SKU variable o dinámico, o si se utiliza un SKU fijo para el paquete. Opciones: `Fixed` / `Dynamic` |
| [!UICONTROL Weight] | Especifica si el peso se calcula en función de los elementos seleccionados o si es un peso fijo para todo el paquete. Opciones: `Fixed` / `Dynamic` |
| [!UICONTROL Price View] | Determina si el precio del producto se muestra como un intervalo, desde el menos caro al más caro (Intervalo de precios) o con el menos caro mostrado (Tan bajo como). Opciones: `Price Range` / `As Low As` |
| Enviar artículos agrupados | Especifica si los productos individuales se pueden enviar por separado. |

{style="table-layout:auto"}

## Estado de stock del producto agrupado

El estado de stock del paquete es **_se cambia automáticamente a Agotado_** cuando se produce cualquiera de estos escenarios:

- Todas las opciones son opcionales y todos los productos asociados son _Sin existencias_.

- Algunas opciones son obligatorias y los productos asociados a cualquier opción requerida son _Sin existencias_.

El estado de stock del paquete es **_no se cambia automáticamente a Agotado_** cuando se produce cualquiera de estos escenarios:

- Todas las opciones son opcionales y al menos un producto asociado es _En stock_.

- Se requieren algunas opciones y al menos un producto asociado en cada opción requerida es _En stock_.

## Cosas que recordar

![Casilla](../assets/checkbox.png) Los clientes pueden _construyan los suyos_ paquete de producto.

![Casilla](../assets/checkbox.png) Los artículos agrupados pueden ser productos simples o virtuales sin opciones personalizadas.

![Casilla](../assets/checkbox.png) La Vista de precios se puede establecer en `Price Range` o `As Low As`.

![Casilla](../assets/checkbox.png) El SKU y el peso pueden ser `Fixed` o `Dynamic`.

![Casilla](../assets/checkbox.png) La cantidad puede ser un valor preestablecido o definido por el usuario. Sin embargo, no asigne los _[!UICONTROL User Defined]_propiedad para marcar la casilla de verificación o seleccionar varios tipos de entrada.

![Casilla](../assets/checkbox.png) Los artículos agrupados se pueden enviar juntos o por separado.

![Casilla](../assets/checkbox.png) El producto del paquete principal siempre se muestra como un producto de mejora de ventas para todos sus productos secundarios automáticamente.

![Casilla](../assets/checkbox.png) [!UICONTROL Special Price] y [!UICONTROL Customer Group Price] (Precio de nivel) siempre se establecen como porcentaje de descuento para todos los tipos de productos de paquete.
