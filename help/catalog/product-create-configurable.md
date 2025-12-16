---
title: Producto configurable
description: Aprenda a crear un producto configurable que proporcione a los compradores variaciones para su selección.
exl-id: 2066fd20-5227-41e9-b213-31825a58ebd9
feature: Catalog Management, Products
source-git-commit: 6fcbcd3b7cace10f0841a46b3cd27343862b3f3b
workflow-type: tm+mt
source-wordcount: '1981'
ht-degree: 0%

---

# Producto configurable

Un producto configurable se muestra como un único producto con opciones desplegables para variaciones (como color o tamaño). Cada variación es un producto simple independiente con su propio SKU, lo que permite el seguimiento de inventario individual, a diferencia de los productos simples con opciones personalizadas.

**Ideal para:** productos con varias opciones (color, tamaño, material, etc.) en las que necesita realizar un seguimiento del inventario para cada variación. La configuración inicial tarda más tiempo, pero ofrece una mejor escalabilidad.

![Producto configurable](./assets/product-configurable.png){width="700" zoomable="yes"}

## Antes de empezar

### Lista de comprobación de requisitos previos

Antes de crear un producto configurable, asegúrese de lo siguiente:

1. **Conjunto de atributos**: un conjunto de atributos que incluye atributos de variación (como color y tamaño)
1. **Atributos de variación creados** - Atributos configurados con la siguiente configuración
1. **Imágenes del producto** - (Opcional pero recomendada) Imágenes para el producto principal y cada variación

### Requisitos de atributos

Cada atributo utilizado para las variaciones de productos debe tener esta configuración:

| Propiedad | Configuración requerida |
|--- |--- |
| [!UICONTROL Scope] | `Global` |
| [!UICONTROL Catalog Input Type for Store Owner] | `Dropdown`, `Visual Swatch` o `Text Swatch` |
| [!UICONTROL Values Required] | `Yes` |

{style="table-layout:auto"}

Para obtener instrucciones sobre cómo crear atributos, consulte [Atributos de producto](product-attributes.md).

## Fase 1: crear la base del producto

### Paso 1: Elija el tipo de producto

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. En el menú _[!UICONTROL Add Product]_( ![Flecha de menú](../assets/icon-menu-down-arrow-red.png){width="25"} ) de la esquina superior derecha, elija **[!UICONTROL Configurable Product]**.

   ![Agregar producto configurable](./assets/product-add-configurable.png){width="700" zoomable="yes"}

### Paso 2: Selección del conjunto de atributos

El [conjunto de atributos](attribute-sets.md) determina qué campos aparecen en el formulario del producto y qué atributos están disponibles para las variaciones.

1. Haga clic en el campo del conjunto de atributos en la parte superior de la página y realice una de las siguientes acciones:

   - Para **[!UICONTROL Search]**, escriba el nombre del conjunto de atributos.
   - En la lista, elija el conjunto de atributos que desea utilizar.

   El formulario se actualiza para reflejar el conjunto de atributos seleccionado.

1. Si necesita agregar otro atributo al conjunto de atributos, haga clic en **[!UICONTROL Add Attribute]** y siga las instrucciones de [Agregar un atributo](product-attributes-add.md).

   ![Elegir plantilla](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

### Paso 3: Introducir información básica

1. Escriba el producto **[!UICONTROL Product Name]**.

1. Acepte el valor predeterminado **[!UICONTROL SKU]** basado en el nombre del producto o escriba un valor diferente.

1. Escriba el producto **[!UICONTROL Price]**.

   >[!NOTE]
   >
   >Este precio se anula con los precios de los productos secundarios. El precio real que se muestra a los clientes proviene de [!UICONTROL In Stock] productos secundarios.

1. Dado que el producto aún no está listo para publicarse, establezca **[!UICONTROL Enable Product]** en `No`.

1. Haga clic en **[!UICONTROL Save]** y continúe.

   Cuando se guarda el producto, aparece el selector [Vista de tienda](introduction.md#product-scope) en la esquina superior izquierda.

1. Elija el **[!UICONTROL Store View]** en el que el producto estará disponible.

   ![Elija la vista de la tienda](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Paso 4: completar la configuración básica

1. Establezca **[!UICONTROL Tax Class]** en una de las siguientes opciones:

   - `None`
   - `Taxable Goods`

1. Deje **[!UICONTROL Quantity]** en blanco. La cantidad está determinada por las variaciones del producto.

1. Deje **[!UICONTROL Stock Status]** como se estableció.

   El estado de stock de un producto configurable viene determinado por sus variaciones asociadas. Como el producto se guardó sin cantidad, **[!UICONTROL Stock Status]** se establece en `Out of Stock`.

   >[!NOTE]
   >
   >El **estado de stock** de un producto configurable es un ajuste controlado **_semimanualmente_**, parcialmente basado en el estado de stock de sus productos secundarios. Forma parte del cálculo del estado de las existencias de **_varios criterios_**. Consulte [Configurar el estado de las existencias](#configure-stock-status) para obtener más información.

1. Escriba el producto **[!UICONTROL Weight]**.

   >[!NOTE]
   >
   >Un producto configurable siempre debe tener un peso. Si selecciona **[!UICONTROL This item has no weight]** en el menú desplegable, cambiará automáticamente a **[!UICONTROL This item has weight]** cuando guarde el producto.

1. Acepte la configuración predeterminada **[!UICONTROL Visibility]** de `Catalog, Search`.

1. Para incluir el producto en la lista de [nuevos productos](../content-design/widget-new-products-list.md), seleccione la casilla de verificación **[!UICONTROL Set Product as New]**.

1. Para asignar categorías al producto, haga clic en el cuadro **[!UICONTROL Select…]** y realice una de las siguientes acciones:

   **Elija una categoría existente:**

   - Empiece a escribir en el cuadro para encontrar una coincidencia.

   - Seleccione la casilla de verificación de cada categoría que desee asignar.

   ![Seleccione una o más categorías para el producto del paquete](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **Crear una nueva categoría:**

   - Haga clic en **[!UICONTROL New Category]**.

   - Escriba **[!UICONTROL Category Name]** y elija **[!UICONTROL Parent Category]** para determinar su posición en la estructura de menú.

   - Haga clic en **[!UICONTROL Create Category]**.

1. Elija **[!UICONTROL Country of Manufacture]**.

   Pueden aparecer atributos adicionales en función del conjunto de atributos. Puede completarlas más adelante.

### Paso 5: Guardar y continuar

Este es un buen momento para guardar su trabajo. Haga clic en **[!UICONTROL Save]** en la esquina superior derecha. En la siguiente fase, se configuran las opciones de configuración para cada variación.

## Fase 2: Agregar variaciones de productos

Los siguientes pasos muestran cómo agregar configuraciones para varias variaciones. La barra de progreso de la parte superior de la página muestra la posición actual en el proceso.

**Ejemplo:** Para una camisa con 3 colores y 3 tallas, crearás 9 productos simples con SKU únicas (una para cada combinación). De forma predeterminada, el nombre de producto y el SKU de cada variación se basan en el valor de atributo y el nombre de producto o SKU principal.

### Paso 6: Elegir atributos de variación

1. Desplácese hasta la sección _[!UICONTROL Configurations]_&#x200B;y haga clic en **[!UICONTROL Create Configurations]**.

   ![Configuraciones](./assets/product-configurable-create-configurations.png){width="600" zoomable="yes"}

1. Seleccione la casilla de verificación de cada atributo para incluirlo como una variación.

   Para este ejemplo, `color` y `size` están seleccionados.

   ![Seleccionar atributos](./assets/product-create-configurable-step1.png){width="600" zoomable="yes"}

   La lista incluye todos los atributos del conjunto de atributos que se pueden utilizar en un producto configurable.

1. Si necesita agregar un atributo, haga clic en **[!UICONTROL Create New Attribute]** y haga lo siguiente:

   - Complete las propiedades del atributo.

   - Haga clic en **[!UICONTROL Save Attribute]**.

   - Seleccione la casilla de verificación del atributo.

1. Haga clic en **[!UICONTROL Next]** en la esquina superior derecha.

### Paso 7: Seleccionar valores de atributo

1. Para cada atributo, seleccione la casilla de los valores que se aplican al producto.

   ![Valores de atributo](./assets/product-create-configurable-step2.png){width="600" zoomable="yes"}

1. Para reorganizar los atributos, coja el icono _Reordenar_ ( ![icono de orden](../assets/icon-sort-order.png) ) y mueva la sección a una nueva posición.

   El orden determina la posición de las listas desplegables en la página del producto.

1. En la barra de progreso, haga clic en **[!UICONTROL Next]**.

### Paso 8: Configurar imágenes, precios e inventario

Este paso determina las imágenes, los precios y la cantidad de cada configuración. Las opciones disponibles son las mismas para cada una. Puede aplicar la misma configuración a todos los SKU, aplicar configuraciones únicas a cada SKU u omitir la configuración por ahora.

#### Configuración de imágenes

Elija la opción de configuración que se aplica:

**Opción 1: aplicar un solo conjunto de imágenes a todos los SKU**

1. Seleccione **[!UICONTROL Apply single set of images to all SKUs]**.

1. Examine cada imagen para incluirla en la galería de productos o arrastre imágenes al cuadro.

![Usar las mismas imágenes para todos los SKU](./assets/product-configurations-images-apply-single-set.png){width="600" zoomable="yes"}

**Opción 2: aplicar imágenes únicas para cada SKU**

Dado que la imagen del producto principal ya se ha cargado, utilice esta opción para cargar imágenes para cada variación. Puede agregar diferentes imágenes que aparecerán en el carro de compras cuando alguien compre una variación específica.

1. Seleccione **[!UICONTROL Apply unique images by attribute to each SKU]**.

1. Seleccione el(la) **[!UICONTROL Attribute]** que ilustran las imágenes, como `color`.

1. Para cada valor de atributo, examine las imágenes que desea utilizar para esa configuración o arrástrelas al cuadro.

   Si arrastra una imagen a un cuadro de valor, también aparecerá en las secciones de otros valores. Para eliminar una imagen, haz clic en el icono _Papelera_ (![Icono de papelera](../assets/icon-delete-trashcan-solid.png)).

   ![Imágenes únicas por SKU](./assets/product-configurable-create-configurations-add-images-unique.png){width="600" zoomable="yes"}

#### Configurar precios

>[!NOTE]
>
>Un producto configurable no tiene su propio precio en el catálogo. El precio de producto configurable se deriva de sus [!UICONTROL In Stock] productos secundarios.

Elija la opción de configuración que se aplica:

**Opción 1: aplicar el mismo precio a todos los SKU**

1. Si el precio es el mismo para todas las variaciones, seleccione **[!UICONTROL Apply single price to all SKUs]**.

1. Escriba **[!UICONTROL Price]**.

   ![Mismo precio por SKU](./assets/product-configurable-create-configurations-price-all-skus.png){width="600" zoomable="yes"}

**Opción 2: aplicar un precio diferente para cada SKU**

1. Si el precio difiere para cada una o algunas variaciones, seleccione **[!UICONTROL Apply unique prices by attribute to each SKU]**.

1. Seleccione el **[!UICONTROL Attribute]** que es la base de la diferencia de precio.

1. Escriba **[!UICONTROL Price]** para cada valor de atributo.

   En este ejemplo, el tamaño XL cuesta más.

   ![Precio único por SKU](./assets/product-configurable-create-configurations-price-unique.png){width="600" zoomable="yes"}

#### Configurar inventario

Elija la opción de configuración que se aplica:

**Opción 1: aplicar la misma cantidad a todos los SKU**

Si la cantidad es la misma para todas las SKU, seleccione **[!UICONTROL Apply single quantity to each SKU]** y especifique la cantidad.

_Comerciantes de Source únicos :_

Escriba **[!UICONTROL Quantity]**.

_Varios comerciantes de Source con [Inventory management &#x200B;](../inventory-management/introduction.md):_

Asigne orígenes y añada cantidades para todas las variantes de producto generadas:

1. Seleccione la opción **[!UICONTROL Apply single quantity to each SKU]**.

1. Para agregar un origen, haga clic en **[!UICONTROL Assign Sources]**.

1. Busque o examine un origen para agregar. Seleccione la casilla de verificación situada junto a los orígenes del producto.

1. Introduzca un importe de inventario disponible por origen.

   ![Cantidad única para todos los SKU, asignar origen](./assets/inventory-configure-product-quantity.png){width="600" zoomable="yes"}

**Opción 2: Aplicar cantidad diferente por atributo**

_Comerciantes de Source únicos :_

Escriba **[!UICONTROL Quantity]** para cada valor de atributo.

_Varios comerciantes de Source con [Inventory management &#x200B;](../inventory-management/introduction.md):_

Asigne orígenes y añada cantidades para todas las variantes de producto generadas:

1. Seleccione **[!UICONTROL Apply unique quantity by attribute to each SKU]**.

1. Escriba **[!UICONTROL Quantity]** para cada variación.

   ![Cantidades diferentes por atributo](./assets/product-configurations-quantity-different.png){width="600" zoomable="yes"}

Una vez completada la configuración de imágenes, precio y cantidad, haga clic en **[!UICONTROL Next]** en la esquina superior derecha.

### Paso 9: Generar configuraciones de producto

Espere un momento a que aparezca la lista de productos y realice una de las siguientes acciones:

- Si está satisfecho con las configuraciones, haga clic en **[!UICONTROL Generate Products]**.

- Para hacer correcciones, haga clic en **[!UICONTROL Back]**.

![Revisar el resumen antes de generar variaciones de productos](./assets/product-create-configurable-summary.png){width="600" zoomable="yes"}

Las variaciones de productos actuales aparecen al final de la sección _Configuración_.

![Configuraciones actuales](./assets/product-create-configurable-generated.png){width="600" zoomable="yes"}

### Paso 10: Añadir imágenes de producto

1. Desplácese hacia abajo y expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección _[!UICONTROL Images and Videos]_.

1. Haga clic en el mosaico _Cámara_ y busque la imagen principal que se utilizará para el producto configurable.

Para obtener más información, vea [Imágenes y vídeo](product-images-and-video.md).

### Paso 11: completar la información del producto

Desplácese hacia abajo y complete la información de las siguientes secciones según sea necesario:

- [Contenido](product-content.md)

- [Productos relacionados, ampliación de ventas y ventas cruzadas](related-products-up-sells-cross-sells.md)

- [Optimización del motor de búsqueda](product-search-engine-optimization.md)

- [Opciones personalizables](settings-advanced-custom-options.md)

- [Productos en sitios web](settings-basic-websites.md)

- [Diseño](settings-advanced-design.md)

- [Opciones de regalo](product-gift-options.md)

## Fase 3: Publicar el producto

### Paso 12: Publicar el producto

1. Si está listo para publicar el producto en el catálogo, establezca **[!UICONTROL Enable Product]** en `Yes`.

1. Realice una de las siguientes acciones:

   **Método 1: guardar y previsualizar**

   - En la esquina superior derecha, haga clic en **[!UICONTROL Save]**.

   - Para ver el producto en tu tienda, elige **[!UICONTROL Customer View]** en el menú _Administrador_ ( ![Flecha de menú](../assets/icon-menu-down-arrow-black.png) ).

   La tienda se abre en una nueva pestaña del explorador.

   ![Vista del cliente](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **Método 2: guardar y cerrar**

   En el menú _[!UICONTROL Save]_( ![flecha de menú](../assets/icon-menu-down-arrow-red.png){width="25"} ), elija **[!UICONTROL Save & Close]**.

## Configuración del estado de stock

El estado de stock de productos configurables difiere del estado de stock de productos simple. Para un producto configurable, el estado de las existencias es parte de un cálculo de **_varios criterios_**.

### Funcionamiento del estado de las existencias

Los principios clave del comportamiento del estado de las existencias:

| El Estado Se Establece En | Resultado | ¿Está Controlado Por Productos Secundarios? |
|---|---|---|
| `Out of Stock` (manual) | Siempre muestra `Out of Stock` en el administrador y en la tienda | No, permanece hasta que se cambia manualmente a `In Stock` |
| `In Stock` (manual) | El estado es dinámico, según los productos secundarios | Parcial: consulte los detalles a continuación |

{style="table-layout:auto"}

### Cuando se establece en &quot;En stock&quot;

Cuando establece manualmente el estado de existencias del producto configurable en `In Stock`, se comporta de forma diferente según la configuración del inventario:

**Solo con origen/existencias predeterminado:**

- **Administrador y tienda:** El estado de las existencias refleja automáticamente la disponibilidad del producto secundario

**Con al menos un origen/stock personalizado:**

- **Tienda:** El estado de las existencias refleja automáticamente la disponibilidad del producto secundario
- **Administrador:** permanece como `In Stock` hasta que se cambia manualmente (no controlado por productos secundarios)

>[!NOTE]
>
>Las existencias y los orígenes personalizados forman parte de la extensión [Inventory management](../inventory-management/sources-stocks.md). Se recomienda encarecidamente utilizar esta herramienta exclusivamente para administrar stock y origen. Las funciones de origen y existencias predeterminadas forman parte del módulo `CatalogInventory`, que ahora está obsoleto.

### Cambios manuales de estado de stock

Si establece manualmente el estado de las existencias en `Out of Stock` (mediante la acción del usuario administrador, la importación de archivos o la llamada a la API), permanecerá `Out of Stock` tanto en el administrador como en la tienda hasta que vuelva a cambiarlo manualmente a `In Stock`. No se ve afectado por el estado de stock de productos secundarios.

## Configuración del sistema (opcional)

### Mostrar imágenes de variación en miniaturas del carro de compras

Si tiene diferentes imágenes para cada variación, puede configurar el sistema para que muestre la imagen correcta para la miniatura del carro de compras.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Checkout]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección _[!UICONTROL Shopping Cart]_.

1. Establezca **[!UICONTROL Configurable Product Image]** en `Product Thumbnail Itself`.

1. Haga clic en **[!UICONTROL Save Config]**.

   ![Carro de compras: imagen de producto configurable](./assets/config-checkout-configurable-product.png){width="600" zoomable="yes"}

## Consideraciones clave

- **Tipos de variación:** Los compradores pueden seleccionar opciones entre los tipos de entrada de lista desplegable, selección múltiple, muestra visual y muestra de texto. Cada opción es un producto independiente y sencillo.

- **Seguimiento del inventario:** A diferencia de los productos simples con opciones personalizadas, los productos configurables realizan un seguimiento del inventario para cada variación de forma independiente.

- **Tipos de productos secundarios:** Los productos secundarios pueden ser productos simples o virtuales **sin opciones personalizadas**. Para hacer que los productos secundarios sean virtuales, seleccione `Тhis item has no weight` para la configuración **[!UICONTROL Weight]** de cada elemento secundario.

- **Asignación global:** Los productos secundarios se asignan y se quitan de la asignación del producto configurable **globalmente** en todos los sitios web, tiendas y vistas de tiendas simultáneamente.

- **Precios:** Un producto configurable no tiene su propio precio en el catálogo. El precio mostrado proviene de sus [!UICONTROL In Stock] productos secundarios.

- **Atributos:** Los atributos de variación deben tener un ámbito global y se debe requerir a los clientes que elijan un valor. Los atributos deben incluirse en el conjunto de atributos utilizado para el producto configurable.

- **Miniaturas del carro de compras:** La miniatura del carro de compras puede mostrar la imagen del registro de producto configurable o de la variación de producto. Consulte [Configuración del sistema](#system-configuration-optional) más arriba.

- **Comportamiento de muestra:** [Los atributos de muestra](swatches.md#create-swatches-for-products) se pueden configurar para que no muestren las imágenes de producto simples correspondientes cuando se seleccione la muestra estableciendo **[!UICONTROL Update Product Preview Image]** en `No` en la página de edición de atributos.

- **Comportamiento de la galería de imágenes:** El tema controla cómo se comporta la Galería de imágenes cuando los usuarios cambian entre configuraciones de producto. El comportamiento predeterminado para el tema _En blanco_ anula las imágenes de producto configurables principales con la variación seleccionada. Para el tema de Luma, el comportamiento predeterminado es anteponer las imágenes de variación seleccionadas a las imágenes de producto configurables principales.
