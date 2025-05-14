---
title: Producto configurable
description: Aprenda a crear un producto configurable que proporcione a los compradores variaciones para su selección.
exl-id: 2066fd20-5227-41e9-b213-31825a58ebd9
feature: Catalog Management, Products
source-git-commit: 0cb594144a03eda985be3a86e45c93452281e9d5
workflow-type: tm+mt
source-wordcount: '2506'
ht-degree: 0%

---

# Producto configurable

Un producto configurable parece un único producto con una lista desplegable de cada variación. Cada elemento de la lista es en realidad un producto simple independiente con un SKU único, que permite rastrear el inventario para cada variación de producto. Podría lograr un efecto similar utilizando un producto simple con opciones personalizadas, pero sin la capacidad de realizar un seguimiento del inventario para cada variación.

Las siguientes instrucciones muestran el proceso de creación de un producto configurable mediante una [plantilla de producto](attribute-sets.md), los campos obligatorios y la configuración básica. Cada campo obligatorio está marcado con un asterisco rojo (`*`). Cuando termine los conceptos básicos, puede completar el resto de la configuración del producto según sea necesario.

![Producto configurable](./assets/product-configurable.png){width="700" zoomable="yes"}

## Parte 1: Creación de un producto configurable

Aunque un producto configurable utiliza más SKU y puede tardar un poco más en configurarse, puede ahorrarle tiempo al final. Si planea hacer crecer su negocio, el tipo de producto configurable es una buena opción para productos con varias opciones.

Antes de empezar, prepare un [conjunto de atributos](attribute-sets.md) que incluya un atributo que esté establecido en uno de los tipos de entrada permitidos para cada variación de producto. Por ejemplo, el conjunto de atributos puede incluir atributos desplegables de color y tamaño.

Las propiedades de cada atributo que se utiliza para una variación de producto configurable deben tener la siguiente configuración:

### Requisitos de atributos de variación del producto

| Propiedad | Configuración |
|--- |--- |
| [!UICONTROL Scope] | `Global` |
| [!UICONTROL Catalog Input Type for Store Owner] | El tipo de entrada de cualquier atributo utilizado para una variación de producto debe ser uno de los siguientes: `Dropdown`, `Visual Swatch` o `Text Swatch`. |
| [!UICONTROL Values Required] | `Yes` |
| [!UICONTROL Use for Promo Rule Conditions] | `Yes` |

{style="table-layout:auto"}

### Paso 1: Elija el tipo de producto

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. En el menú _[!UICONTROL Add Product]_( ![Flecha de menú](../assets/icon-menu-down-arrow-red.png){width="25"} ) de la esquina superior derecha, elija **[!UICONTROL Configurable Product]**.

   ![Agregar producto configurable](./assets/product-add-configurable.png){width="700" zoomable="yes"}

### Paso 2: Selección del conjunto de atributos

El [conjunto de atributos](attribute-sets.md) determina la selección de campos que se utilizan en el producto. El conjunto de atributos que se utiliza en el ejemplo siguiente tiene atributos para el color y el tamaño. El nombre del conjunto de atributos se indica en la parte superior de la página y se establece inicialmente en `Default`.

1. Para elegir el conjunto de atributos del producto, haga clic en el campo en la parte superior de la página y realice una de las siguientes acciones:

   - Para **[!UICONTROL Search]**, escriba el nombre del conjunto de atributos.
   - En la lista, elija el conjunto de atributos que desea utilizar.

   El formulario se actualiza para reflejar el cambio.

1. Si desea agregar otro atributo al conjunto de atributos, haga clic en **[!UICONTROL Add Attribute]** y siga las instrucciones de [Agregar un atributo](product-attributes-add.md).

   ![Elegir plantilla](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

### Paso 3: complete la configuración necesaria

1. Escriba el producto **[!UICONTROL Product Name]**.

1. Acepte el valor predeterminado **[!UICONTROL SKU]** basado en el nombre del producto o escriba otro.

1. Escriba el producto **[!UICONTROL Price]**.

1. Dado que el producto aún no está listo para publicarse, establezca **[!UICONTROL Enable Product]** en `No`.

1. haga clic en **[!UICONTROL Save]** y continúe.

   Cuando se guarda el producto, aparece el selector [Vista de tienda](introduction.md#product-scope) en la esquina superior izquierda.

1. Elija el **[!UICONTROL Store View]** en el que el producto estará disponible.

   ![Elija la vista de la tienda](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Paso 4: completar la configuración básica

1. Establezca **[!UICONTROL Tax Class]** en una de las siguientes opciones:

   - `None`
   - `Taxable Goods`

1. El **[!UICONTROL Quantity]** está determinado por las variaciones de productos, por lo que puede dejarlo en blanco.

1. Deje **[!UICONTROL Stock Status]** como está configurado.

   El estado de stock de un producto configurable viene determinado por cada configuración asociada. Como el producto se guardó sin escribir una cantidad, **[!UICONTROL Stock Status]** se establece en `Out of Stock`.

   >[!NOTE]
   >
   >El **estado de stock** del producto configurable es una configuración controlada de **_forma semimanual_**. Está parcialmente controlado por el estado de existencias de sus productos secundarios. Forma parte de un cálculo del estado de las existencias de **_varios criterios_**, que se describe en la sección [Configurar el estado de las existencias](#configure-the-stock-status).

1. Escriba el producto **[!UICONTROL Weight]**.

>[!NOTE]
>
>Un producto configurable siempre debe tener un peso. Si selecciona **[!UICONTROL This item has no weight]** en la lista desplegable, se cambiará automáticamente a **[!UICONTROL This item has weight]** después de guardar el producto.

1. Acepte la configuración predeterminada **[!UICONTROL Visibility]** de `Catalog, Search`.

1. Para incluir el producto en la lista de [nuevos productos](../content-design/widget-new-products-list.md), seleccione la casilla de verificación **[!UICONTROL Set Product as New]**.

1. Para asignar categorías al producto, haga clic en el cuadro **[!UICONTROL Select…]** y realice una de las acciones siguientes:

   **Elija una categoría existente**:

   - Empiece a escribir en el cuadro hasta que encuentre una coincidencia.

   - Seleccione la casilla de verificación de la categoría que se va a asignar.

   ![Seleccione una o más categorías para el producto del paquete](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **Crear una categoría**:

   - Haga clic en **[!UICONTROL New Category]**.

   - Escriba **[!UICONTROL Category Name]** y elija **[!UICONTROL Parent Category]**, que determina su posición en la estructura de menú.

   s- Haga clic en **[!UICONTROL Create Category]**.

1. Elija **[!UICONTROL Country of Manufacture]**.

   Puede haber atributos adicionales que se usan para describir el producto. La selección varía según el conjunto de atributos y puede completarla más adelante.

### Paso 5: Guardar y continuar

Ahora es un buen momento para guardar su trabajo. En la esquina superior derecha, haga clic en **[!UICONTROL Save]**. En la siguiente serie de pasos, debe configurar las configuraciones para cada variación del producto.

## Parte 2: Añadir configuraciones

En el siguiente ejemplo se muestra cómo agregar configuraciones para tres colores y tres tamaños. En total, se crean nueve productos simples con SKU únicos para cubrir cada combinación posible de variaciones. De forma predeterminada, el nombre y el SKU del producto de cada variación se basan en el valor del atributo y en el nombre o el SKU del producto principal.

La barra de progreso de la parte superior de la página muestra dónde se encuentra en el proceso y le guía a través de cada paso.

### Paso 1: Elija los atributos

1. Continuando desde arriba, desplácese hacia abajo hasta la sección _[!UICONTROL Configurations]_y haga clic en **[!UICONTROL Create Configurations]**.

   ![Configuraciones](./assets/product-configurable-create-configurations.png){width="600" zoomable="yes"}

1. Seleccione la casilla de verificación de cada atributo que desee incluir como configuración.

   Para este ejemplo, `color` y `size` están seleccionados.

   ![Seleccionar atributos](./assets/product-create-configurable-step1.png){width="600" zoomable="yes"}

   La lista incluye todos los atributos del conjunto de atributos que se pueden utilizar en un producto configurable.

1. Si desea agregar un atributo, haga clic en **[!UICONTROL Create New Attribute]** y haga lo siguiente:

   - Complete las propiedades del atributo.

   - Haga clic en **[!UICONTROL Save Attribute]**.

   - Seleccione la casilla de verificación del atributo.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Next]**.

### Paso 2: Introduzca los valores de atributo

1. Para cada atributo, seleccione la casilla de los valores que se aplican al producto.

   ![Valores de atributo](./assets/product-create-configurable-step2.png){width="600" zoomable="yes"}

1. Para reorganizar los atributos, coja el icono _Reordenar_ ( ![icono de orden](../assets/icon-sort-order.png) ) y mueva la sección a una nueva posición.

   El orden determina la posición de las listas desplegables en la página del producto.

1. En la barra de progreso, haga clic en **[!UICONTROL Next]**.

### Paso 3: Configurar las imágenes, el precio y la cantidad

Este paso determina las imágenes, los precios y la cantidad de cada configuración. Las opciones disponibles son las mismas para cada una y solo puede elegir una. Puede aplicar la misma configuración a todos los SKU, aplicar una configuración única a cada SKU u omitir la configuración por ahora.

Elija las opciones de configuración aplicables.

Utilice uno de los siguientes métodos para configurar **[!UICONTROL images]**:

**Método 1:** Aplicar un solo conjunto de imágenes a todos los SKU

1. Seleccione **[!UICONTROL Apply single set of images to all SKUs]**.

1. Busque todas las imágenes que desee incluir en la galería de productos o arrástrelas al cuadro.

![Usar las mismas imágenes para todos los SKU](./assets/product-configurations-images-apply-single-set.png){width="600" zoomable="yes"}

**Método 2:** Aplicar imágenes únicas para cada SKU

Como la imagen del producto principal ya se ha cargado, puede utilizar esta opción para cargar una imagen de cada color. Puede añadir una imagen diferente que aparezca en el carro de compras cuando alguien compre el artículo en un color específico.

1. Seleccione **[!UICONTROL Apply unique images by attribute to each SKU]**.

1. Seleccione el(la) **[!UICONTROL Attribute]** que ilustran las imágenes, como `color`.

1. Para cada valor de atributo, vaya a las imágenes que desee utilizar para esa configuración o arrástrelas al cuadro.

   Si arrastra la imagen a un cuadro de valor, también aparecerá en las secciones de los demás valores. Si desea eliminar una imagen, haga clic en el icono _Papelera_ (![Icono de papelera](../assets/icon-delete-trashcan-solid.png)).

   ![Imágenes únicas por SKU](./assets/product-configurable-create-configurations-add-images-unique.png){width="600" zoomable="yes"}

Utilice uno de los siguientes métodos para configurar **[!UICONTROL prices]**:

>[!NOTE]
>
>Un producto configurable no tiene su propio precio en el catálogo. El precio de producto configurable se deriva de sus [!UICONTROL In Stock] productos secundarios.

**Método 1:** Aplicar el mismo precio a todos los SKU

1. Si el precio es el mismo para todas las variaciones, seleccione **[!UICONTROL Apply single price to all SKUs]**.

1. Escriba **[!UICONTROL Price]**.

   ![Mismo precio por SKU](./assets/product-configurable-create-configurations-price-all-skus.png){width="600" zoomable="yes"}

**Método 2:** Aplicar un precio diferente para cada SKU

1. Si el precio difiere para cada una o para algunas variaciones del producto, seleccione **[!UICONTROL Apply unique prices by attribute to each SKU]**.

1. Seleccione el **[!UICONTROL Attribute]** que es la base de la diferencia de precio.

1. Escriba **[!UICONTROL Price]** para cada valor de atributo.

   En este ejemplo, el tamaño XL cuesta más.

   ![Precio único por SKU](./assets/product-configurable-create-configurations-price-unique.png){width="600" zoomable="yes"}

Utilice uno de los siguientes métodos para configurar **[!UICONTROL Quantity]**:

**Método 1:** Aplicar la misma cantidad a todos los SKU

Si la cantidad es la misma para todas las SKU, seleccione **[!UICONTROL Apply single quantity to each SKU]** y especifique la cantidad.

_Comerciantes de origen único_ - Escriba **[!UICONTROL Quantity]**.

_Comerciantes de varios Source que usan [Inventory management](../inventory-management/introduction.md)_: asigne orígenes y agregue cantidades para todas las variantes de productos generadas:

1. Seleccione la opción **[!UICONTROL Apply single quantity to each SKU]**.

1. Para agregar un origen, haga clic en **[!UICONTROL Assign Sources]**.

1. Busque o examine un origen que desee agregar. Seleccione la casilla de verificación situada junto a los orígenes que desee agregar para el producto.

1. Introduzca un importe de inventario disponible por origen.

   ![Cantidad única para todos los SKU, asignar origen](./assets/inventory-configure-product-quantity.png){width="600" zoomable="yes"}

**Método 2:** Aplicar cantidad diferente por atributo

_Comerciantes de origen único_ - Escriba **[!UICONTROL Quantity]**.

_Comerciantes de varios Source que usan [Inventory management](../inventory-management/introduction.md)_: asigne orígenes y agregue cantidades para todas las variantes de productos generadas:

1. Si la cantidad es diferente para cada SKU, seleccione **[!UICONTROL Apply unique quantity by attribute to each SKU]**.

1. Escriba **[!UICONTROL Quantity]** para cada uno.

   ![Cantidades diferentes por atributo](./assets/product-configurations-quantity-different.png){width="600" zoomable="yes"}

Una vez completada la configuración de las imágenes, el precio y la cantidad, haga clic en **[!UICONTROL Next]** en la esquina superior derecha.

### Paso 4: Generar las configuraciones de producto

Espere un momento a que aparezca la lista de productos y realice una de las siguientes acciones:

- Si está satisfecho con las configuraciones, haga clic en **[!UICONTROL Generate Products]**.

- Para hacer correcciones, haga clic en **[!UICONTROL Back]**.

![Revisar el resumen antes de generar variaciones de productos](./assets/product-create-configurable-summary.png){width="600" zoomable="yes"}

Las variaciones de productos actuales aparecen al final de la sección _Configuración_.

![Configuraciones actuales](./assets/product-create-configurable-generated.png){width="600" zoomable="yes"}

### Paso 5: Añadir imágenes de producto

1. Desplácese hacia abajo y expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección _[!UICONTROL Images and Videos]_.

1. Haga clic en el mosaico _Cámara_ y busque la imagen principal que desee usar para el producto configurable.

Para obtener más información, vea [Imágenes y vídeo](product-images-and-video.md).

### Paso 6: Completar la información del producto

Desplácese hacia abajo y complete la información de las siguientes secciones según sea necesario:

- [Contenido](product-content.md)

- [Productos relacionados, ampliación de ventas y ventas cruzadas](related-products-up-sells-cross-sells.md)

- [Optimización del motor de búsqueda](product-search-engine-optimization.md)

- [Opciones personalizables](settings-advanced-custom-options.md)

- [Productos en sitios web](settings-basic-websites.md)

- [Diseño](settings-advanced-design.md)

- [Opciones de regalo](product-gift-options.md)

### Paso 7: Publicar el producto

1. Si está listo para publicar el producto en el catálogo, establezca **[!UICONTROL Enable Product]** en `Yes` y realice una de las siguientes acciones:

   - **Método 1:** Guardar y previsualizar

      - En la esquina superior derecha, haga clic en **[!UICONTROL Save]**.

      - Para ver el producto en tu tienda, elige **[!UICONTROL Customer View]** en el menú _Administrador_ ( ![Flecha de menú](../assets/icon-menu-down-arrow-black.png) ).

     La tienda se abre en una nueva pestaña del explorador.

     ![Vista del cliente](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Método 2:** Guardar y cerrar

     En el menú _[!UICONTROL Save]_( ![flecha de menú](../assets/icon-menu-down-arrow-red.png){width="25"} ), elija **[!UICONTROL Save & Close]**.

### Paso 8: Configurar las miniaturas del carro de compras

Si tiene una imagen diferente para cada variación, puede establecer la configuración para utilizar la imagen correcta para la miniatura del carro de compras.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Checkout]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección _[!UICONTROL Shopping Cart]_.

1. Establezca **[!UICONTROL Configurable Product Image]** en `Product Thumbnail Itself`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

   ![Carro de compras: imagen de producto configurable](./assets/config-checkout-configurable-product.png){width="600" zoomable="yes"}

## Configuración del estado de Stock

El estado de stock del producto configurable es diferente del estado de stock del producto simple, donde es una representación directa de la disponibilidad del producto. Para un producto configurable, el estado de las existencias es parte de un cálculo del estado de las existencias de **_varios criterios_**.

### Información general

Los principios principales de las relaciones de estado de stock son los siguientes:

- Cuando cambia el **[!UICONTROL Stock Status]** del producto configurable como `Out of Stock` y hace clic en **[!UICONTROL Save]**, **_no está controlado_** por los estados de existencias de sus productos secundarios. Siempre se muestra como `Out of Stock` en el Administrador y en la Tienda.

- Cuando establece el **[!UICONTROL Stock Status]** del producto configurable como `In Stock` y hace clic en **[!UICONTROL Save]**, **_solo está parcialmente controlado_** por los estados de existencias de sus productos secundarios, que se reflejan en el Administrador y en la Tienda.

### Descripción detallada

El _estado de existencias_ del producto configurable está parcialmente controlado por el estado de existencias de sus productos secundarios y según los siguientes cálculos de estado de existencias de **_varios criterios_**:

#### Solo con origen/stock predeterminado:

- Si el estado de las existencias del producto configurable es **_manualmente_** establecido en `Out of Stock` por un usuario administrador, una importación de archivos o una llamada de API, permanecerá como `Out of Stock` tanto en **_Admin_** como en **_Storefront_** hasta que un usuario administrador, una importación de archivos o una llamada de API lo cambien a **_manualmente_**. `In stock` No puede estar controlada por el estado de existencias de sus productos secundarios.

- Si el estado de existencias del producto configurable es **_manualmente_** establecido en `In Stock` por un usuario administrador, una importación de archivos o una llamada de API, su estado de existencias es **_automáticamente_** controlado por el estado de existencias de sus productos secundarios en **_Admin_** y **_Storefront_**.

>[!NOTE]
>
>Las existencias y las fuentes personalizadas forman parte de la extensión [Inventory management](../inventory-management/sources-stocks.md) y se recomienda usar esta herramienta exclusivamente para administrar existencias y fuentes. Las funciones de origen y existencias predeterminadas forman parte del módulo `CatalogInventory`, que ahora está obsoleto.

#### Con al menos un origen/stock personalizado:

- Si el valor configurable del estado de las existencias del producto es **_manualmente_** establecido en `Out of Stock` por un usuario administrador, una importación de archivos o una llamada de API, permanecerá como `Out of Stock` tanto en **_Admin_** como en **_Storefront_** hasta que un usuario administrador, una importación de archivos o una llamada de API lo cambien **_manualmente_** a `In Stock`. **_no puede_** estar controlado por el estado de stock de sus productos secundarios.

- Si el valor configurable del estado de las existencias del producto es **_manualmente_** establecido en `In Stock` por un usuario administrador, una importación de archivos o una llamada de API, su estado de existencias es **_automáticamente_** controlado por el estado de las existencias de sus productos secundarios solo en **_Storefront_**.

- Si el valor configurable del estado de las existencias del producto es **_manualmente_** establecido en `In Stock` por un usuario administrador, una importación de archivos o una llamada de API, permanecerá como `In Stock` en **_Admin_** hasta que un usuario administrador, una importación de archivos o una llamada de API lo cambien **_manualmente_** a `Out of Stock`. **_no puede_** estar controlado por el estado de stock de sus productos secundarios.

## Cosas que recordar

- Un producto configurable permite al comprador elegir entre tipos de entrada de muestras desplegables, de selección múltiple, de muestra visual y de muestra de texto. Cada opción es un producto independiente y sencillo.

- [Estado de stock](../inventory-management/sources-stocks.md) para un producto configurable es una configuración controlada de forma semimanual. Es diferente al estado de stock del producto simple, donde es una representación directa de la disponibilidad del producto. Para un producto configurable, el estado de las existencias forma parte de un cálculo del estado de las existencias con varios criterios.

- Los productos secundarios configurables pueden ser productos simples o virtuales **sin opciones personalizadas**. Para hacer virtuales los productos secundarios personalizados, debe seleccionar `Тhis item has no weight` para la configuración **[!UICONTROL Weight]** de cada uno de ellos.

- Todos los productos secundarios se asignan y quitan la asignación del producto configurable **_globalmente_** para todos los sitios web, tiendas y vistas de tiendas al mismo tiempo.

- Un producto configurable no tiene su propio precio en el catálogo. El precio de producto configurable se deriva de sus [!UICONTROL In Stock] productos secundarios.

- Los atributos que se utilizan para las variaciones de productos deben tener un ámbito global y se debe exigir al cliente que elija un valor. Los atributos de variación del producto deben incluirse en el conjunto de atributos que se utiliza como plantilla para el producto configurable.

- El conjunto de atributos que se utiliza como plantilla para un producto configurable debe incluir los atributos que contienen los valores necesarios para cada variación de producto.

- La imagen en miniatura del carro de compras se puede configurar para que muestre la imagen del registro de producto configurable o de la variación de producto.

- [Los atributos de muestra](swatches.md#create-swatches-for-products) se pueden configurar para que no muestren las imágenes de producto simples correspondientes cuando se seleccione la muestra; para ello, establezca el valor de la opción **[!UICONTROL Update Product Preview Image]** en `No` en la página de edición de atributos del Administrador.

- El tema controla cómo se comporta la Galería de imágenes cuando un usuario cambia entre configuraciones de producto. El comportamiento predeterminado para el tema _En blanco_ es anular las imágenes de producto configurables principales con la variación de producto seleccionada. Para la temática de Luma, el comportamiento predeterminado es anteponer las imágenes de variación de producto seleccionadas a las imágenes de producto configurables principales.
