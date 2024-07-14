---
title: Administración de imágenes y vídeos de productos
description: Obtenga información sobre la administración de recursos de imagen y vídeo para las listas de productos.
exl-id: 3cb4ab8a-8966-400f-be94-a517634d1334
feature: Catalog Management, Products, Media
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# Administración de imágenes y vídeos de productos

Para cada producto, puede cargar varias imágenes y vídeos, reorganizar su pedido y controlar cómo se utiliza cada uno. Si tiene que administrar una gran cantidad de imágenes, es posible que prefiera importarlas como un lote en lugar de cargar cada una de ellas individualmente. Para obtener más información, consulte [Importar imágenes de productos](../systems/data-import-product-images.md).

Si planea cargar imágenes grandes para verlas en la página _[!UICONTROL Product Details]_, considere la posibilidad de establecer un tamaño de píxel máximo (ancho y alto) y cambiar automáticamente el tamaño de los archivos al cargarlos. Hay una opción para habilitar el cambio de tamaño automático de archivos de imagen más grandes a medida que carga. Para obtener más información, consulte [Cambio de tamaño de la imagen del producto](product-image-config.md#product-image-resizing).

## Actualizar las imágenes del producto

1. Abra el producto en modo de edición.

1. Para trabajar con una vista de tienda específica, establezca el selector **[!UICONTROL Store View]** en la esquina superior izquierda a la vista correspondiente.

   >[!NOTE]
   >
   >Las nuevas imágenes de producto **_siempre_** están cargadas y son visibles en **_todas_** las vistas de tiendas, incluso si el ámbito `All Store Views` no se usa para la carga. <br/><br/>Para ocultar cualquier imagen de producto de una vista de tienda específica, debe cambiar a esa vista de tienda, seleccionar la casilla **[!UICONTROL Hide from Product Page]** de la imagen y hacer clic en **[!UICONTROL Save]**.

1. Desplácese hacia abajo y expanda la sección _[!UICONTROL Images and Videos]_.

### Cargar una imagen

Para obtener la mejor compatibilidad, se recomienda cargar todas las imágenes de productos con el perfil de color `sRGB`. Todos los demás perfiles de color se convierten automáticamente al perfil de color `sRGB` durante la carga de la imagen del producto, lo que podría causar incoherencia de color en la imagen cargada.

La longitud del nombre del archivo de imagen, incluida la extensión, no puede superar los 90 caracteres.

Para cargar una imagen, realice una de las siguientes acciones:

- Arrastre una imagen desde el escritorio y suéltela en el mosaico _Cámara_ ( ![Icono de cámara](../assets/icon-camera.png) ) del cuadro _[!UICONTROL Images And Videos]_.

- En el cuadro _[!UICONTROL Images And Videos]_, haga clic en el mosaico_ Cámara _( ![Icono de cámara](../assets/icon-camera.png) ), seleccione el archivo de imagen del equipo y haga clic en **[!UICONTROL Open]**.

  ![Cargar o arrastrar y soltar](./assets/product-images-and-video-jewel-tee.png){width="600" zoomable="yes"}

### Reorganizar imágenes

Para cambiar el orden de las imágenes en la galería, haga clic en el icono _[!UICONTROL Sort]_( ![Icono Ordenar](./assets/inventory-icon-sort.png) ) en la parte inferior del mosaico de la imagen y arrastre la imagen a una posición diferente en el cuadro_[!UICONTROL Images And Videos]_.

![Pedido de cambio](./assets/product-images-and-videos-drag.png){width="600" zoomable="yes"}

### Eliminar una imagen

Para quitar una imagen de la galería, haga clic en el icono **[!UICONTROL Delete]** ( ![icono de papelera](../assets/icon-delete-trashcan.png) ) en la esquina superior derecha del mosaico de la imagen y haga clic en **[!UICONTROL Save]**.

### Definir detalles de la imagen

Haga clic en la imagen que desea abrir en la vista de detalles y realice una de las acciones siguientes:

![Vista de detalles de imagen](./assets/product-image-detail-jewel-tee.png){width="600" zoomable="yes"}

Para cerrar la vista de detalles, haga clic en el icono _Cerrar_ ( ![Icono Cerrar](../assets/icon-close-x.png) ) en la esquina superior derecha.

Una vez finalizado, haga clic en **[!UICONTROL Save]**.

#### Introducir texto alternativo

Los lectores de pantalla hacen referencia al texto alternativo de imagen para mejorar la accesibilidad web y los motores de búsqueda al indexar el sitio. Algunos exploradores muestran el texto alternativo al pasar el ratón por encima. El texto alternativo puede tener varias palabras e incluir palabras clave cuidadosamente seleccionadas.

En el cuadro _[!UICONTROL Alt Text]_, escriba una breve descripción de la imagen.

#### Asignar funciones

De forma predeterminada, todas las funciones se asignan a la primera imagen cargada en el producto. Para reasignar un rol a otra imagen, haga lo siguiente:

En el cuadro _[!UICONTROL Role]_, elija la función que desea asignar a la imagen.

Cuando vuelva a la sección _Imágenes y vídeos_, los roles asignados actualmente aparecerán debajo de cada imagen.

![Roles asignados](./assets/product-images-video-swatch.png){width="600" zoomable="yes"}

#### Ocultar una imagen

Para excluir una imagen de la galería de miniaturas, seleccione la casilla **[!UICONTROL Hidden]** y haga clic en **[!UICONTROL Save]**.

![Imágenes ocultas](./assets/product-images-and-videos-hidden.png){width="600" zoomable="yes"}

## Funciones de imagen

| Función de imagen | Descripción |
|--- |--- |
| [!UICONTROL Thumbnail] | Las imágenes en miniatura aparecen en la galería de miniaturas, en el carro de compras y en algunos bloques, como Elementos relacionados. Tamaño de ejemplo: 50 x 50 píxeles |
| [!UICONTROL Small Image] | La imagen pequeña se utiliza para las imágenes de los productos que aparecen en los anuncios de las páginas de categorías y resultados de búsqueda, y para mostrar las imágenes de productos necesarias para secciones como Ampliación de ventas, Venta cruzada y la Nueva lista de productos. Tamaño de ejemplo: 470 x 470 píxeles |
| [!UICONTROL Base Image] | La imagen base es la imagen principal de la página de detalles del producto. El zoom de imagen se activa si se carga una imagen que es más grande que el contenedor de imágenes. Según el nivel de zoom que desee alcanzar, la imagen base debe ser dos o tres veces el tamaño del contenedor. Tamaños de ejemplo: 470 x 470 píxeles (sin zoom), 1100 x 1100 píxeles (con zoom) |
| [!UICONTROL Swatch] | Se puede usar una [muestra](swatches.md) para ilustrar el color, el patrón o la textura. Tamaño de ejemplo: 50 x 50 píxeles |

{style="table-layout:auto"}

## Filigranas

Si vas a expensas de crear tus propias imágenes originales del producto, no hay mucho que puedas hacer para evitar que competidores sin escrúpulos las roben con un clic del ratón. Sin embargo, puede hacer que sean un destino menos atractivo colocando una marca de agua en cada imagen para identificarlos como su propiedad. Un archivo de marca de agua puede ser un JPG (JPEG), un GIF o una imagen PNG. Los tipos de archivo GIF y PNG admiten capas transparentes, que se pueden utilizar para dar a la marca de agua un fondo transparente.

La marca de agua utilizada para la imagen _small_ del siguiente ejemplo es un logotipo negro con un fondo transparente y se guarda como archivo PNG con la siguiente configuración:

- Tamaño: 50x50
- Opacidad: 5
- Posición: Mosaico

![Marca de agua en mosaico](./assets/storefront-watermark-tiled.png){width="700" zoomable="yes"}

### Agregar marcas de agua a imágenes de productos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

   Para obtener más información acerca de las configuraciones de diseño, vea [Configuración de diseño](../content-design/configuration.md).

1. Busque la vista de tienda que desea configurar y haga clic en **[!UICONTROL Edit]** en la columna _[!UICONTROL Action]_.

1. En _[!UICONTROL Other Settings]_, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Product Image Watermarks]**.

   ![Marcas de agua de imagen de producto - Base](./assets/config-design-product-image-watermarks-base.png){width="600" zoomable="yes"}

   La configuración de las imágenes **[!UICONTROL Base]**, **[!UICONTROL Thumbnail]**, **[!UICONTROL Small]** y **[!UICONTROL Swatch Image]** es la misma.

1. Utilice uno de los siguientes métodos para agregar el recurso de imagen de marca de agua:

   - Haga clic en **[!UICONTROL Upload]** y elija el archivo de imagen del sistema que desee cargar para utilizarlo como marca de agua.
   - Haga clic en **[!UICONTROL Select from Gallery]** y seleccione un recurso de imagen de la [Galería multimedia](../content-design/media-gallery.md).

1. Complete la configuración de visualización de la marca de agua:

   - Escriba **[!UICONTROL Image Opacity]** como porcentaje. Por ejemplo: `40`

   - Escriba **[!UICONTROL Image Size]** en píxeles. Por ejemplo: `200 x 200`

   - Establezca **[!UICONTROL Image Position]** para determinar dónde aparece la marca de agua.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

1. Cuando se le pida que actualice la caché, haga clic en **[!UICONTROL Cache Management]** en el mensaje del sistema y actualice la caché no válida.

   ![Actualizar caché](./assets/msg-cache-management.png){width="600" zoomable="yes"}

>[!TIP]
>
>Puede hacer clic en **[!UICONTROL Use Default Value]** ![Flecha devuelta](../assets/icon-arrow-return.png) para restaurar el valor predeterminado.

### Eliminar una marca de agua

1. En la esquina inferior izquierda de la imagen, haga clic en el icono **[!UICONTROL Delete]** ( ![icono de papelera](../assets/icon-delete-trashcan-solid.png) ).

   ![Eliminar filigrana](./assets/product-image-watermark-delete.png){width="300"}

1. Haga clic en **[!UICONTROL Save Config]**.

1. Cuando se le pida que actualice la caché, haga clic en **[!UICONTROL Cache Management]** en el mensaje del sistema y actualice la caché no válida.

   Si la imagen de marca de agua persiste en la tienda, vuelva a la administración de caché y haga clic en **[!UICONTROL Flush Magento Cache]**.
