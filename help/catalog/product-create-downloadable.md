---
title: Producto descargable
description: Obtenga información sobre cómo crear un producto descargable que se pueda entregar como archivo digital.
exl-id: c3dd4c5f-adc1-4a8f-a9da-7f0dedd1ee34
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1622'
ht-degree: 0%

---

# Producto descargable

Un producto descargable puede ser cualquier cosa que pueda enviar como archivo, como un libro electrónico, música, vídeo, aplicación de software o actualización. Puedes ofrecer un álbum a la venta y vender cada canción individualmente. También puede utilizar un producto descargable para entregar una versión electrónica del catálogo de productos.

Como la descarga no estará disponible hasta después de la compra, puede proporcionar muestras, como un extracto de un libro, un clip de un archivo de audio o un trailer de un vídeo. Una muestra es algo que el cliente puede probar antes de comprar el producto. Los archivos que pone a disposición para su descarga se pueden cargar en su servidor o desde un servidor diferente.

![Producto descargable](./assets/storefront-product-downloadable.png){width="700" zoomable="yes"}

Los productos descargables se pueden configurar para que requieran que el cliente inicie sesión en una cuenta para recibir el vínculo o se pueden enviar por correo electrónico y compartir con otros. El estado del pedido antes de que la descarga esté disponible, los valores predeterminados y otras opciones de entrega se establecen en la configuración. A medida que planifique las adiciones a catálogos descargables, tome nota de lo siguiente:

- Los productos descargables pueden cargarse en el servidor o vincularse desde otro servidor en Internet.

- Puede determinar la cantidad de veces que un cliente puede descargar un producto.

- Los clientes que compren un producto descargable pueden tener que iniciar sesión antes de pasar por el proceso de cierre de compra.

- Se puede realizar la entrega de un producto descargable cuando el pedido está en estado `Pending` o `Invoiced`.

- Como los productos descargables no se envían, el paso _Envío_ del cierre de compra se omite cuando el carro de compras contiene únicamente el producto descargable.


## Configurar las opciones de descarga

Las opciones de configuración descargables determinan los valores predeterminados y las opciones de entrega de los productos descargables y especifican si los invitados pueden comprar descargas.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección _[!UICONTROL Downloadable Product Options]_.

   ![Opciones de producto descargables](../configuration-reference/catalog/assets/catalog-downloadable-product-options.png){width="700" zoomable="yes"}

   Para obtener una lista detallada de estas opciones de configuración, consulte [_Opciones de producto descargables_](../configuration-reference/catalog/catalog.md#downloadable-product-options) en la _Referencia de configuración_.

1. Para determinar el estado del proceso de pedido cuando la descarga esté disponible, establezca **[!UICONTROL Order Item Status to Enable Downloads]** en una de las siguientes opciones:

   - `Pending`
   - `Invoiced`

1. Para establecer un límite predeterminado en el número de descargas que puede realizar un solo cliente, escriba el número de **[!UICONTROL Default Maximum Number of Downloads]**.

1. Establezca **[!UICONTROL Shareable]** en una de las siguientes opciones:

   - `Yes`: permite a los clientes enviar por correo electrónico el vínculo de descarga a otras personas.
   - `No`: impide que los clientes compartan el vínculo de descarga con otros usuarios al exigir que inicien sesión en sus cuentas para acceder a los vínculos de descarga.

1. Para **[!UICONTROL Default Sample Title]**, escriba el encabezado que desea que aparezca encima de la selección de muestras.

   ![Título de muestra](./assets/product-downloadable-config-sample-title.png){width="400"}

1. Para **[!UICONTROL Default Link Title]**, escriba el texto predeterminado que desee usar para los vínculos de descarga.

1. Si desea que el vínculo de descarga se abra en una nueva ventana del explorador, establezca **[!UICONTROL Opens Links in New Window]** en `Yes`.

   Esta configuración se utiliza para mantener abierta la ventana del explorador de la tienda.

1. Para determinar cómo se entrega el contenido descargable, establezca **[!UICONTROL Use Content Disposition]** en una de las siguientes opciones:

   - `Attachment`: envía el vínculo de descarga por correo electrónico como datos adjuntos.
   - `Inline`: envía el vínculo de descarga como un vínculo en una página web.

1. Si desea exigir que los compradores se registren para obtener una cuenta de cliente e inicien sesión antes de comprar una descarga, establezca **[!UICONTROL Disable Guest Checkout if Cart Contains Downloadable Items]** en `Yes`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Crear un producto descargable

Las siguientes instrucciones muestran el proceso de creación de un producto descargable mediante una [plantilla de producto](attribute-sets.md), los campos obligatorios y la configuración básica. Cada campo obligatorio está marcado con un asterisco rojo (`*`). Cuando termine los conceptos básicos, puede completar el resto de la configuración del producto según sea necesario.

>[!NOTE]
>
>Los nombres de archivo descargables pueden incluir letras y números. Se puede utilizar un guión o un guión bajo para representar un espacio entre palabras. Cualquier carácter no válido del nombre de archivo se reemplaza por un guion bajo.

### Paso 1: Elija el tipo de producto

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. En el menú _[!UICONTROL Add Product]_( ![Flecha de menú](../assets/icon-menu-down-arrow-red.png){width="25"} ) de la esquina superior derecha, elija `Downloadable Product`.

   ![Agregar producto descargable](./assets/product-add-downloadable.png){width="700" zoomable="yes"}

### Paso 2: Selección del conjunto de atributos

Los datos de ejemplo incluyen un [conjunto de atributos](attribute-sets.md) denominado _descargable_ que tiene campos especiales para productos descargables. Puede utilizar una plantilla existente o crear otra antes de guardar el producto.

Para elegir el conjunto de atributos que se utiliza como plantilla para el producto, realice una de las siguientes acciones:

- Para **[!UICONTROL Search]**, escriba el nombre del conjunto de atributos.

- En la lista, elija el conjunto de atributos `Downloadable`.

El formulario se actualiza para reflejar el cambio.

![Elegir conjunto de atributos](./assets/product-create-choose-attribute-set-downloadable.png){width="600" zoomable="yes"}

### Paso 3: complete la configuración necesaria

1. Escriba **[!UICONTROL Product Name]**.

1. Acepte el valor predeterminado **[!UICONTROL SKU]** basado en el nombre del producto o escriba otro.

1. Escriba el producto **[!UICONTROL Price]**.

1. Dado que el producto aún no está listo para publicarse, establezca **[!UICONTROL Enable Product]** en `No`.

1. haga clic en **[!UICONTROL Save]** y continúe.

   Cuando se guarda el producto, aparece el selector [Vista de tienda](introduction.md#product-scope) en la esquina superior izquierda.

1. Elija el **[!UICONTROL Store View]** en el que el producto estará disponible.

   ![Elegir vista de tienda](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Paso 4: completar la configuración básica

1. Establezca **[!UICONTROL Tax Class]** en una de las siguientes opciones:

   - `None`
   - `Taxable Goods`

1. Escriba el **[!UICONTROL Quantity]** del producto que está en stock.

   Tome nota de lo siguiente:

   - De manera predeterminada, **[!UICONTROL Stock Status]** está establecido en `Out of Stock`.

   - Como los productos descargables no se envían, el campo **[!UICONTROL Weight]** no se utiliza. Si habilita esta característica, se convierte en un [producto simple](product-create-simple.md) y el _¿Es este producto descargable?No se puede usar la ficha_.

   >[!NOTE]
   >
   >Si habilitas [Inventory management](../inventory-management/introduction.md), los comerciantes de Source único establecerán la cantidad en esta sección. Varios comerciantes de Source agregan orígenes y cantidades en la sección Orígenes. Consulte la siguiente sección _Asignar orígenes y cantidades (Inventory management)_.

1. Acepte la configuración predeterminada **[!UICONTROL Visibility]** de `Catalog, Search`.

1. Para incluir el producto en la [lista de nuevos productos](../content-design/widget-new-products-list.md), seleccione la casilla de verificación **[!UICONTROL Set Product as New]**.

1. Para asignar _[!UICONTROL Categories]_al producto, haga clic en el cuadro **[!UICONTROL Select…]**y realice una de las acciones siguientes:

   **Elija una categoría existente**:

   - Empiece a escribir en el cuadro hasta que encuentre una coincidencia.

   - Seleccione la casilla de verificación de cada categoría que se va a asignar.

   **Crear una categoría**:

   - Haga clic en **[!UICONTROL New Category]**.

   - Escriba **[!UICONTROL Category Name]** y elija **[!UICONTROL Parent Category]**, que determina su posición en la [estructura de menú](category-root.md).

   - Haga clic en **[!UICONTROL Create Category]**.

1. Establezca **[!UICONTROL Format]** en una de las siguientes opciones:

   - `Download`
   - `DVD`

   Si es necesario, puede editar [attribute](attribute-product-create.md) para agregar más valores.

   Puede haber atributos adicionales que describan el producto. La selección varía según el conjunto de atributos y puede completarla más adelante.

#### Asignar orígenes y cantidades ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

### Paso 5: Completar la información descargable

Desplácese hacia abajo, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección _[!UICONTROL Downloadable Information]_y seleccione la casilla de verificación **[!UICONTROL Is this downloadable product?]**.

Cuando está habilitada, la sección _[!UICONTROL Downloadable Information]_tiene dos partes. La primera parte describe cada vínculo de descarga y la segunda parte describe cada archivo de muestra. El valor predeterminado de muchas de estas opciones se puede establecer en la [configuración](#configure-the-download-options).

![Información descargable](./assets/product-downloadable-information.png){width="600" zoomable="yes"}

#### Completar los vínculos

1. En la sección _[!UICONTROL Links]_, escriba el **[!UICONTROL Title]**que desee usar como encabezado para los vínculos de descarga.

1. Si corresponde, active la casilla de verificación **[!UICONTROL Links can be purchased separately]**.

1. Haga clic en **[!UICONTROL Add Link]** y haga lo siguiente:

   - Escriba **[!UICONTROL Title]** y **[!UICONTROL Price]** de la descarga.

   - Para los archivos **[!UICONTROL File]** y **[!UICONTROL Sample]**, elija uno de los siguientes métodos de distribución para las descargas:

      - `Upload File`: elija este método para cargar el archivo de distribución en el servidor. Busque el archivo y selecciónelo para cargarlo.
      - `URL`: elija este método para acceder al archivo de distribución desde una dirección URL. Introduzca la dirección URL completa del archivo de descarga.

   >[!NOTE]
   >
   >No puede utilizar vínculos a recursos externos como productos descargables. Los dominios de vínculo válidos están predefinidos mediante programación en el archivo `env.php` (consulte [env.php reference](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/files/config-reference-envphp.html) en la _Guía de configuración_).

   - Establezca **[!UICONTROL Shareable]** en una de las siguientes opciones:

      - `No`: requiere que los clientes inicien sesión en sus cuentas para acceder al vínculo de descarga.

      - `Yes`: envía el vínculo por correo electrónico, que los clientes pueden compartir con otros.

      - `Use Config`: utiliza el método especificado en la configuración de [Opciones de producto descargables](../configuration-reference/catalog/catalog.md).

   - Realice una de las siguientes acciones:

      - Para limitar las descargas por cliente, escriba el número máximo de **[!UICONTROL Max. Downloads]**.
      - Para permitir descargas ilimitadas, marque la casilla de verificación **[!UICONTROL Unlimited]**.

   ![Detalle del vínculo](./assets/product-downloadable-link-detail.png){width="600" zoomable="yes"}

1. Para agregar otro vínculo, haga clic en **[!UICONTROL Add Link]** y repita estos pasos.

#### Completar las muestras

1. En la sección _[!UICONTROL Samples]_, escriba el **[!UICONTROL Title]**que desee usar como encabezado para las muestras.

1. Para completar la información de cada muestra, haga clic en **[!UICONTROL Add Link]**.

   ![Muestras](./assets/product-downloadable-samples.png){width="600" zoomable="yes"}

1. Complete los detalles del vínculo de la siguiente manera:

   - Escriba **[!UICONTROL Title]** de la muestra individual.

   - Elija uno de los siguientes métodos de distribución:

      - `Upload File`: elija este método para cargar el archivo de distribución en el servidor. Busque el archivo y selecciónelo para cargarlo.
      - `URL`: elija este método para acceder al archivo de distribución desde una dirección URL. Introduzca la dirección URL completa del archivo de descarga.

   - Para agregar otra muestra, haga clic en **[!UICONTROL Add Link]** y repita estos pasos.

   - Para cambiar el orden de las muestras, coja el icono _Cambiar orden_ ( ![Controlador de posición](../assets/icon-sort-order.png) ) y arrastre la muestra a una nueva posición.

### Paso 6: Completar la información del producto

Desplácese hacia abajo y complete la información de las siguientes secciones según sea necesario:

- [Contenido](product-content.md)
- [Imágenes y vídeos](product-images-and-video.md)
- [Optimización del motor de búsqueda](product-search-engine-optimization.md)
- [Productos relacionados, ampliación de ventas y ventas cruzadas](related-products-up-sells-cross-sells.md)
- [Opciones personalizables](settings-advanced-custom-options.md)
- [Productos en sitios web](settings-basic-websites.md)
- [Diseño](settings-advanced-design.md)
- [Opciones de regalo](product-gift-options.md)

### Paso 7: Publish del producto

Si está listo para publicar el producto en el catálogo, establezca **[!UICONTROL Enable Product]** en `Yes` y realice una de las siguientes acciones:

**Método 1:** Guardar y previsualizar

- En la esquina superior derecha, haga clic en **[!UICONTROL Save]**.

- Para ver el producto en tu tienda, elige **[!UICONTROL Customer View]** en el menú _Administrador_ ( ![Flecha de menú](../assets/icon-menu-down-arrow-black.png) ).

  La tienda se abre en una nueva pestaña del explorador.

  ![Vista del cliente](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

**Método 2:** Guardar y cerrar

En el menú _[!UICONTROL Save]_( ![flecha de menú](../assets/icon-menu-down-arrow-red.png){width="25"} ), elija **[!UICONTROL Save & Close]**.

## Experiencia en tienda

En el panel de cuenta del cliente, la página _[!UICONTROL My Downloadable Products]_vincula a cada pedido de productos descargables. Las descargas están disponibles en la cuenta del cliente cuando se completa el pedido.

![Mis productos descargables](./assets/customer-account-my-downloadable-products.png){width="700" zoomable="yes"}

En la tabla siguiente se describen los valores de _Mis productos descargables_:

| Columna | Descripción |
|--- |--- |
| [!UICONTROL Order#] | El [pedido](../stores-purchase/orders.md) en el que se compró el producto descargable. Proporciona un vínculo a los detalles del pedido. |
| [!UICONTROL Date] | Fecha de creación del pedido. |
| [!UICONTROL Title] | El nombre del producto descargable comprado con el pedido. Proporciona un vínculo al producto descargable. |
| [!UICONTROL Status] | Estado de procesamiento del pedido. |
| [!UICONTROL Remaining Downloads] | Número de descargas disponibles del producto descargado. |

_**Para descargar un archivo de producto desde el panel de cuentas**_

1. En su panel de cuentas, el cliente elige **[!UICONTROL My Downloadable Products]**.

1. Busca el orden en la lista y hace clic en el vínculo situado después del título.

1. En la esquina inferior derecha de la ventana de descarga, hace clic en el icono _descargar_.

1. Localiza el archivo en su ubicación de descargas y lo guarda en la ubicación deseada.
