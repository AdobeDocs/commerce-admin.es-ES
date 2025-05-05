---
title: '[!DNL Page Builder] Tutorial, parte 3: contenido del catálogo'
description: Aprenda a agregar una lista de productos a una página  [!DNL Page Builder] .
exl-id: f2a0dc29-6d8f-4b97-a947-72659c01d0cb
feature: Page Builder, Page Content
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 0%

---

# [!DNL Page Builder], parte 3: contenido del catálogo

Este ejercicio muestra lo fácil que es agregar una lista de productos a una página, personalizar páginas de productos y crear un atributo personalizado que agregue el área de trabajo [!DNL Page Builder] a un conjunto de atributos de producto.

![Lista de productos](./assets/pb-add-content-products-list.png){width="600" zoomable="yes"}

Este ejercicio supone que ha completado [Parte 1: Página simple](1-simple-page.md) y [Parte 2: Bloques](2-blocks.md), incluidos los requisitos previos y los archivos de ejemplo descargados. Siga las tres partes de este ejercicio en orden.

## Parte 1: Añadir una lista de productos

[!DNL Page Builder] facilita la adición de una lista de productos al escenario. En este ejemplo, la lista de productos se agrega directamente a una página.

### Paso 1: Añadir una lista de productos a la fase

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Busque la _página simple_ que creó en el primer ejercicio y modificó en el segundo y seleccione **[!UICONTROL Edit]** en la columna _[!UICONTROL Action]_.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Content]** y haga clic en **[!UICONTROL Edit with Page Builder]** o dentro del área de vista previa del contenido.

1. En el panel [!DNL Page Builder] bajo _[!UICONTROL Layout]_, arrastre un(a)**[!UICONTROL Row]**&#x200B;a la parte superior del escenario.

1. En el panel [!DNL Page Builder], expanda **[!UICONTROL Add Content]** y arrastre un marcador de posición **[!UICONTROL Products]** a la nueva fila.

   ![Arrastrando un marcador de posición de productos a la fila](./assets/pb-add-content-products-drag.png){width="600" zoomable="yes"}

### Paso 2: Componga la condición

1. Pase el ratón sobre el contenedor de productos vacío para ver la caja de herramientas y elija el icono _Configuración_ ( ![icono Configuración](./assets/pb-icon-settings.png){width="20"} ).

   ![Cuadro de herramientas de productos](./assets/pb-add-content-products-toolbox.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Select Products By]**, elija `Condition`.

1. Añada una condición:

   - Haga clic en el icono _Agregar_ (![Agregar icono](../assets/icon-add-green-circle.png)).

   - En _[!UICONTROL Product Attribute]_, elija **[!UICONTROL Category]**.

     ![Eligiendo el atributo category para la condición](./assets/pb-add-content-products-settings-condition.png){width="600" zoomable="yes"}

   - Complete la parte de _[!UICONTROL Category is]..._ de la condición haciendo clic en el icono Más (...) y, a continuación, haga clic en el icono _Selector_ (![Icono del selector](../assets/icon-list-chooser.png)).

     ![Definición de la condición](./assets/pb-add-content-products-settings-condition-category-is.png){width="600" zoomable="yes"}

   - En el árbol de categorías, explora la categoría **Mujeres > Superiores** y selecciona la casilla de verificación **Tees**.

     ![Selección de la categoría en el árbol](./assets/pb-add-content-products-settings-condition-category-tree.png){width="600" zoomable="yes"}

   - Haga clic en el icono de marca de verificación (![icono de marca de verificación](../assets/icon-checkmark-green-circle.png)).

     La ID de categoría correspondiente aparece en el campo para completar la condición.

### Paso 3: Completar la configuración

1. Escriba **[!UICONTROL Number of Products to Display]**.

   De forma predeterminada, la lista muestra cinco productos.

1. Complete los ajustes restantes según sea necesario.

   Si es necesario, use las descripciones de los campos que aparecen al final de la página [Agregar contenido: productos](products.md) como referencia.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]** para guardar la configuración y volver al área de trabajo [!DNL Page Builder].

   ![Lista de productos en la fase](./assets/pb-add-content-products-list-stage.png){width="600" zoomable="yes"}

1. En la esquina superior derecha del escenario, haga clic en el icono _Cerrar pantalla completa_ (![Icono de cerrar pantalla completa](./assets/pb-icon-reduce.png){width="20"} ).

   Al hacer clic en este icono, volverá a la sección _[!UICONTROL Content]_&#x200B;de la página con la vista previa mostrada.

1. En la esquina superior derecha, haga clic en la flecha **[!UICONTROL Save]** y elija **[!UICONTROL Save & Close]**.

## Parte 2: Personalizar la página del producto

>[!NOTE]
>
>Un usuario administrador debe tener permisos de [!UICONTROL Content] para su [ámbito de función](../systems/permissions-user-roles.md) para ver los botones de [!UICONTROL Edit with Page Builder] y poder usar Page Builder.

En esta parte del ejercicio, aprenderá lo fácil que es personalizar una página de producto colocando un vídeo debajo del conjunto de pestañas en la página de producto. El proceso para actualizar el contenido de la [página de categoría](../catalog/categories-content-settings.md) es básicamente el mismo.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Busque un producto simple que pueda utilizar para este ejemplo y ábralo en modo de edición.

1. Desplácese hacia abajo y expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Content]**.

1. Junto a _[!UICONTROL Description]_, haga clic en **[!UICONTROL Edit with Page Builder]**.

   ![Contenido de descripción del producto](./assets/pb-catalog-product-content.png){width="600" zoomable="yes"}

   Si la descripción del producto se especificó anteriormente sin [!DNL Page Builder], la descripción actual aparecerá como HTML en un contenedor de [código de HTML](html-code.md). Con la temática de Luma, la descripción del producto aparece en la pestaña Detalles.

1. En el panel [!DNL Page Builder] bajo _[!UICONTROL Layout]_, arrastre un(a)**[!UICONTROL Row]**&#x200B;al escenario y colóquelo debajo del contenedor de código de HTML.

   Busque que aparezca la guía roja cuando la fila esté en la posición correcta.

   ![Arrastrando una fila al escenario](./assets/catalog-product-content-stage-row-drag.png){width="600" zoomable="yes"}

1. En el panel [!DNL Page Builder], expanda **[!UICONTROL Media]** y arrastre un marcador de posición **[!UICONTROL Video]** a la nueva fila.

   ![Marcador de posición de vídeo en la fila](./assets/tutorial3-product-drag-video.png){width="600" zoomable="yes"}

1. Pase el ratón sobre el contenedor de vídeo vacío para ver la caja de herramientas y elija el icono _Configuración_ ( ![icono Configuración](./assets/pb-icon-settings.png){width="20"} ).

   ![Cuadro de herramientas de vídeo](./assets/pb-tutorial3-product-video-toolbox.png){width="500" zoomable="yes"}

1. Escriba **[!UICONTROL Video URL]**.

   El vídeo puede alojarse en [YouTube][1] o [Vimeo][2]. El vídeo de este ejemplo se puede encontrar en YouTube en la siguiente dirección URL:

   `https://www.youtube.com/watch?v=ZpFrNyD4100`

   ![Editando el vídeo](./assets/pb-tutorial3-product-edit-video.png){width="500" zoomable="yes"}

1. Escriba **[!UICONTROL Maximum Width]** en píxeles para la pantalla de vídeo.

   Si deja esta opción en blanco, el vídeo rellena el espacio disponible.

1. Haga clic en **[!UICONTROL Save]** para guardar la configuración y volver al área de trabajo [!DNL Page Builder].

   ![Vídeo en la fase de contenido](./assets/pb-tutorial3-product-video.png){width="600" zoomable="yes"}

1. En la esquina superior derecha del escenario, haga clic en el icono _Cerrar pantalla completa_ (![Icono de cerrar pantalla completa](./assets/pb-icon-reduce.png){width="20"} ).

   Al hacer clic en este icono, volverá a la sección _[!UICONTROL Content]_&#x200B;de la página con la vista previa mostrada.

1. En la esquina superior derecha, haga clic en la flecha **[!UICONTROL Save]** y elija **[!UICONTROL Save & Close]**.

En la tienda, el vídeo aparece debajo del conjunto de pestañas. Para ver el aspecto de la página en un dispositivo móvil, puede cambiar el tamaño de la ventana.

![Vídeo mostrado en la página del producto](./assets/pb-tutorial3-product-video-storefront.png){width="600" zoomable="yes"}

**¡Felicitaciones!** Ha completado la segunda parte del tutorial Contenido del catálogo. Conserve el trabajo que ha creado para poder consultarlo más adelante.

## Parte 3: Añadir atributos personalizados

Use el atributo personalizado [!DNL Page Builder] para agregar un área de trabajo [!DNL Page Builder] que funcione completamente a una página de producto, que puede usar para crear contenido atractivo. En esta parte del ejercicio, aprenderá a crear un atributo personalizado con el tipo de entrada [!DNL Page Builder] y a aplicarlo a las páginas de producto del catálogo. Para obtener más información acerca de estos atributos, vea [Atributos del producto](../catalog/product-attributes.md).

### Paso 1: Crear un producto

Para evitar cambios en la tienda activa, cree un producto con las propiedades descritas.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Product]**.

1. Cree el producto con las siguientes propiedades:

   - &#x200B;

     [!UICONTROL Conjunto de atributos]: Default
   - [!UICONTROL Product Name]: Mi producto
   - &#x200B;

     [!UICONTROL SKU]: Tutorial
   - &#x200B;

     [!UICONTROL Price]: 75.00
   - &#x200B;

     [!UICONTROL Quantity]: 100
   - [!UICONTROL Stock Status]: en stock
   - &#x200B;

     [!UICONTROL Weight]: 1
   - [!UICONTROL Categories]: Mujeres > Tops > Camisetas

1. En la esquina superior derecha, haga clic en la flecha **[!UICONTROL Save]** y elija **[!UICONTROL Save & Close]**.

### Paso 2: Crear atributos personalizados

En este paso, creará dos nuevos atributos personalizados para mostrar cómo se pueden utilizar los tipos de entrada [!DNL Page Builder] y Editor de texto.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add New Attribute]**.

1. Escriba **[!UICONTROL Default Label]** para el atributo.

   Para este ejemplo, use `My Page Builder Attribute` para la etiqueta.

1. Establezca **[!UICONTROL Catalog Input Type for Store Owner]** en `Page Builder`.

   Al crear un atributo personalizado, puede especificar el editor más adecuado para la aplicación como `Page Builder` o el WYSIWYG estándar `Text Editor`.

   ![[!DNL Page Builder] tipo de entrada](./assets/pb-attribute-page-builder.png){width="600" zoomable="yes"}

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Advanced Attribute Properties]** y realice la siguiente configuración:

   - [!UICONTROL Attribute Code]: escriba un código de atributo en minúsculas, con guiones en lugar de espacios. Para este ejemplo, use `my_page_builder_attribute`.
   - [!UICONTROL Scope]: acepte el valor predeterminado `Store View`.
   - [!UICONTROL Default Value]: escriba un valor predeterminado para el atributo.
   - &#x200B;

     [!UICONTROL Unique Value]: `No`
   - &#x200B;

     [!UICONTROL Add to Column Options]: `No`
   - &#x200B;

     [!UICONTROL Use in Filter Options]: `Yes`

1. En el panel _[!UICONTROL Attribute Information]_&#x200B;de la izquierda, elija **[!UICONTROL Storefront Properties]**&#x200B;y realice la siguiente configuración:

   - &#x200B;

     [!UICONTROL Use for Promo Rule Conditions]: `Yes`
   - &#x200B;

     [!UICONTROL Visible on Catalog Pages on Storefront]: `Yes`
   - &#x200B;

     [!UICONTROL Used in Product Listing]: `Yes`

1. Una vez finalizado, haga clic en **[!UICONTROL Save Attribute]**.

1. Repita los pasos anteriores para crear un segundo atributo con las mismas propiedades básicas, pero con el tipo de entrada Editor de texto de la siguiente manera:

   - [!UICONTROL Default Label]: Atributo de mi editor de texto
   - [!UICONTROL Catalog Input Type for Store Owner]: Editor de texto
   - &#x200B;

     [!UICONTROL Código de atributo]: `my_text_editor_attribute`

### Paso 3: Actualizar el conjunto de atributos del producto

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

   Para este ejemplo, agrega temporalmente los nuevos atributos al conjunto de atributos `default`. Al final de este ejercicio, elimine los atributos del conjunto de atributos, por lo que no afectará a su catálogo.

   >[!NOTE]
   >
   >Si no desea cambiar la tienda activa, puede continuar sin actualizar el conjunto de atributos.

1. Busque el atributo _[!UICONTROL Default]_&#x200B;establecido en la lista y haga doble clic en él para abrirlo en modo de edición.

1. En la lista _Atributos sin asignar_, busque los nuevos atributos que creó y arrastre cada uno a la columna _[!UICONTROL Groups]_, en **[!UICONTROL Content]**.

   La ubicación del atributo en la columna [!UICONTROL Groups] determina dónde aparece en la página.

   ![Nuevos atributos agregados al grupo de contenido](./assets/pb-product-attribute-set.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save]** para volver a la lista Conjuntos de atributos.

1. Cuando se le solicite, haga clic en el vínculo **[!UICONTROL Cache Management]** en la parte superior de la página y actualice cualquier caché no válida.

### Paso 4: Actualizar el producto

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. En la cuadrícula Productos, busque _Mi producto_ y ábralo en modo de edición.

1. Desplácese hacia abajo y expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Content]**.

   En la parte superior de la sección, hay dos atributos estándar para el contenido del producto:

   - _Descripción breve_, que usa el [editor](../content-design/editor.md) WYSIWYG estándar.
   - _Descripción_, que muestra la vista previa de [!DNL Page Builder].

   ![Contenido del producto](./assets/pb-product-content-edit-with-page-builder.png){width="600" zoomable="yes"}

   A medida que se desplaza hasta la mitad inferior de la sección, aparecen los dos atributos que ha creado y asignado:

   - _Mi atributo [!DNL Page Builder]_, que muestra la vista previa [!DNL Page Builder].
   - _Atributo de mi editor de texto_, que usa el editor WYSIWYG estándar.

   ![Edición de contenido de producto](./assets/pb-product-content-my-attributes.png){width="600" zoomable="yes"}

1. En el editor de **Atributos de mi editor de texto**, escriba `Text Editor Attribute placeholder text`.

   - En la esquina superior derecha, haga clic en la flecha **[!UICONTROL Save]** y elija **[!UICONTROL Save & Close]**.

1. Para **Mi atributo de Page Builder**, haga clic en **[!UICONTROL Edit with Page Builder]** y agregue el texto de descripción:

   - En el panel [!DNL Page Builder], expanda **[!UICONTROL Elements]** y arrastre un(a) **[!UICONTROL Text object]** al escenario.

   - Escriba `Page Builder attribute placeholder text`.

   - En la esquina superior derecha del escenario, haga clic en el icono _Cerrar pantalla completa_ (![Icono de cerrar pantalla completa](./assets/pb-icon-reduce.png){width="20"} ).

     ![Atributos personalizados con texto de marcador de posición](./assets/pb-product-content-attributes.png){width="600" zoomable="yes"}

1. Desplácese hasta **[!UICONTROL Description]**, haga clic en **[!UICONTROL Edit with Page Builder]** y agregue el texto que desee utilizando el mismo método que en el paso anterior.

1. En la esquina superior derecha de la página de producto, haga clic en la flecha **[!UICONTROL Save]** y elija **[!UICONTROL Save & Close]**.

1. Si se le solicita, haga clic en el vínculo **[!UICONTROL Cache Management]** en el mensaje en la parte superior de la página y actualice cualquier caché no válida.

### Paso 5: Ver el resultado

1. Navegue hasta la página de producto de muestra en la tienda.

   En este ejemplo, el producto se puede encontrar en la barra de navegación superior debajo de Mujeres > Tops > Camisetas.

1. Desplácese hacia abajo hasta la información de _Mi atributo de Page Builder_.

   La posición de los atributos en la página del producto está determinada por la temática. En la temática de Luma, los nuevos atributos se encuentran justo después de la descripción del producto.

   ![[!DNL Page Builder] y atributos del Editor de texto en la tienda](./assets/pb-storefront-product-attribute.png){width="600" zoomable="yes"}

Ha completado el ejercicio [!DNL Page Builder] contenido de catálogo. Conserve el trabajo que ha creado para poder consultarlo más adelante.

[1]: https://www.youtube.com/
[2]: https://vimeo.com/
