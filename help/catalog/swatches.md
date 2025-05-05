---
title: Muestras de producto
description: Obtenga información sobre cómo definir muestras para los listados de productos configurables.
exl-id: 6163cec4-5d84-4e2c-ba5c-3c22ac4e3f28
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1164'
ht-degree: 0%

---

# Muestras de producto

Los clientes tienen grandes expectativas de elegir un color y es crucial que las descripciones de los productos representen con precisión cada color, patrón o textura disponible. Por ejemplo, los pantalones del siguiente ejemplo no están disponibles en rojo, verde y azul. En cambio, solo están disponibles en tonos específicos de rojo, verde y azul, que probablemente sean únicos para este producto.

![Muestras en una página de producto](./assets/storefront-color-swatches.png){width="700" zoomable="yes"}

Para [productos configurables](product-create-configurable.md), el color se puede indicar mediante una muestra visual, una muestra de texto o un control de entrada. Las muestras se pueden usar en la página de productos, en las listas de productos y en [navegación por capas](navigation-layered.md). En la página del producto, las muestras se sincronizan para mostrar la imagen del producto correspondiente cuando se selecciona la muestra. Cuando el cliente selecciona la muestra, el valor correspondiente aparece en el campo de entrada y la muestra se esquematiza como la selección actual.

>[!NOTE]
>
>Los atributos de muestra se pueden configurar para que no muestren las imágenes de producto simples correspondientes cuando se seleccione la muestra estableciendo el valor de opción _[!UICONTROL Update Product Preview Image]_&#x200B;en `No` en la página [!UICONTROL Attribute Edit] en el Administrador.

## Muestras basadas en texto

Si una imagen no está disponible para una muestra, el valor del atributo aparece como texto. Una muestra basada en texto es como un botón con una etiqueta de texto y se comporta de la misma manera que una muestra con una imagen. Cuando se utilizan muestras basadas en texto para mostrar los tamaños disponibles, cualquier tamaño que no esté disponible se tachará.

![La selección de muestras basadas en texto muestra un tamaño sin existencias](./assets/storefront-swatch-size-out-of-stock.png){width="700" zoomable="yes"}

## Muestras en la navegación por capas

Las muestras también se pueden usar en la navegación por capas, si la propiedad _[!UICONTROL Use in Layered Navigation]_&#x200B;del atributo de color está establecida en `Yes`. El siguiente ejemplo muestra muestras de imagen basadas en texto y en color en la navegación por capas.

![Muestras mostradas en la navegación por capas](./assets/storefront-swatches-layered-navigation.png){width="700" zoomable="yes"}

## Creación de muestras para los productos

Las muestras pueden definirse como un componente del atributo `color` o configurarse localmente para un producto específico y cargarse como [imágenes de producto](product-image.md#upload-an-image).

En los ejemplos anteriores, los pantalones &quot;Sylvia Capri&quot; están disponibles en valores específicos de `red`, `green` y `blue`. Dado que las muestras se tomaron de la imagen del producto, cada una es una verdadera representación del color. El atributo `color` se usa para administrar la información de todos los colores y muestras del producto.

### Paso 1: Creación de las muestras

Utilice cualquiera de los siguientes métodos para crear muestras para sus productos.

#### Método 1: añadir una muestra de color

1. Para capturar el color verdadero de un producto, abra la imagen en un editor de fotos y use la herramienta de cuentagotas para identificar el color exacto y tomar nota del valor hexadecimal equivalente.

   ![Valores de color hexadecimales](./assets/swatch-hex-values.png){width="400"}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. En la cuadrícula, abra el atributo _color_ en el modo de edición.

1. Compruebe que **[!UICONTROL Catalog Input Type for Store Owner]** está establecido en `Visual Swatch`.

1. Si prefiere no mostrar las imágenes de productos simples correspondientes cuando la muestra se selecciona en la página de visualización del producto, establezca **[!UICONTROL Update Product Preview Image]** en `No`.

1. En _[!UICONTROL Manage Swatch (Values of Your Attribute)]_, haga clic en **[!UICONTROL Add Swatch]**&#x200B;y haga lo siguiente:

   ![Administrar valores de muestra](./assets/attribute-color-manage-swatch-values.png){width="600" zoomable="yes"}

   - En la columna _Muestra_, haga clic en la nueva muestra y seleccione **[!UICONTROL Choose a color]** en el menú.

     ![Elegir un color de muestra](./assets/attribute-color-swatch-menu.png){width="500" zoomable="yes"}

   - En el selector de color, coloque el cursor en el campo **#**, elimine el valor actual e introduzca el valor hexadecimal de seis caracteres del nuevo color.

     ![Escriba el valor hexadecimal](./assets/attribute-swatch-color-picker-hex-value.png){width="500" zoomable="yes"}

   - Para guardar la muestra, haga clic en el icono _Rueda de color_ ( ![Icono de color](../assets/icon-color-wheel.png) ) en la esquina inferior derecha del selector de color.

   - En la columna _Admin_, escriba una etiqueta para describir el color al administrador de la tienda.

     Si procede, también puede introducir la traducción del color para cada idioma admitido. En el siguiente ejemplo, el SKU se incluye como referencia en la etiqueta _Admin_ porque los colores solo se utilizan para un producto específico. Puede incluir un espacio o un guion bajo en la etiqueta, pero no un guión.

   - En la columna _Predeterminado_, seleccione la muestra que será la opción predeterminada.

   - Para cambiar el orden de las muestras de color, haga clic en el icono _[!UICONTROL Order]_![Icono de orden](../assets/icon-sort-order.png) y arrastre el elemento a una nueva posición en la lista.

     ![Etiquetas de muestras](./assets/attribute-swatch-labels.png){width="400"}

1. Cuando termine, haga clic en **[!UICONTROL Save Attribute]** y actualice la caché cuando se le solicite.

1. Abra cada producto en modo de edición y actualice el atributo **Color** con la muestra correcta.

   Para actualizar varios productos al mismo tiempo, siga los pasos a continuación.

#### Método 2: cargar una imagen de muestra

1. Para capturar una imagen para una muestra, abra la imagen del producto en un editor de fotos y guarde un área cuadrada de la imagen que represente el color, el patrón o la textura.

   Si es necesario, puede repetir esta acción para cada variación del producto.

   El tamaño y las dimensiones de la muestra vienen determinados por la temática. Por lo general, guardar una imagen como un cuadrado ayuda a conservar la relación de aspecto de un motivo.

   ![Imágenes de muestra](./assets/swatch-samples.png){width="400"}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. En la cuadrícula, abra el atributo **[!UICONTROL color]** en modo de edición.

1. Compruebe que **[!UICONTROL Catalog Input Type for Store Owner]** está establecido en `Visual Swatch`.

1. Si prefiere no mostrar las imágenes de productos simples correspondientes cuando la muestra se selecciona en la página de visualización del producto, establezca **[!UICONTROL Update Product Preview Image]** en `No`.

1. En _[!UICONTROL Manage Swatch]_(valores de su atributo), haga clic en **[!UICONTROL Add Swatch]**&#x200B;y haga lo siguiente:

   - En la columna _[!UICONTROL Swatch]_, haga clic en la nueva muestra para mostrar el menú y elija **[!UICONTROL Upload a file]**.

   - Vaya al archivo de muestra que ha preparado y elija el archivo que desea cargar.

   - Repita estos pasos para cada imagen de muestra.

   - Introduzca las etiquetas para el administrador y la tienda.

     En este ejemplo, el SKU se incluye en la etiqueta Admin como referencia, ya que estos colores solo se utilizan para un producto específico. Puede incluir un espacio o un guion bajo en la etiqueta, pero no puede incluir un guion.

     ![Introducir etiquetas](./assets/swatch-upload.png){width="500" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save Attribute]** y actualice la caché cuando se le solicite.

1. Abra cada producto en modo de edición y actualice el atributo **[!UICONTROL Color]** con la muestra correcta.

   Para actualizar varios productos al mismo tiempo, siga los pasos a continuación.

### Paso 2: Actualizar los productos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Use **[!UICONTROL Filter]** para mostrar la lista por nombre o SKU e incluir solo los productos aplicables.

1. En la cuadrícula, seleccione la casilla de verificación de cada producto al que se aplique la muestra.

1. Establezca **[!UICONTROL Actions]** en `Update Attributes`.

   En este ejemplo, se seleccionan todas las configuraciones azules de los pantalones.

   ![Actualizar atributos de muestra de producto](./assets/swatch-apply-update-attributes.png){width="600" zoomable="yes"}

1. Desplácese hacia abajo hasta el atributo **[!UICONTROL Color]** y seleccione la casilla de verificación **[!UICONTROL Change]**.

   ![Cambiar casilla](./assets/swatch-update-attributes-choose-color.png){width="400"}

1. Elija la muestra que se aplica a los productos seleccionados y haga clic en **[!UICONTROL Save]**.

1. Cuando se le solicite, actualice la caché.

   ![Muestra en la tienda](./assets/swatch-blue-schmear.png){width="200"}

## Añadir muestras a un producto sencillo

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Abra un producto en modo de edición y compruebe su estado (debe estar activado).

1. Haga clic en el botón **[!UICONTROL Create Configurations]** (en la ficha `Configurations`).

1. En la ventana emergente, elija el atributo Color y **[!UICONTROL Next]**.

1. Seleccione muestras de color del atributo que desee incluir en este producto.

1. En la barra de progreso, haga clic en **[!UICONTROL Next]**.

1. [Configurar las imágenes, el precio y la cantidad](product-create-configurable.md#step-3-configure-the-images-price-and-quantity).

   En este paso, establezca las imágenes, los precios y la cantidad de cada configuración. Las opciones disponibles son las mismas para cada una y solo puede elegir una. Puede aplicar la misma configuración a todos los SKU, aplicar una configuración única a cada SKU u omitir la configuración por ahora.

1. Una vez completada la configuración de las imágenes, el precio y la cantidad, haga clic en **[!UICONTROL Next]** en la esquina superior derecha.

   Las variaciones de productos actuales aparecen en la parte inferior de la sección Configuración. Si está satisfecho con las configuraciones, haga clic en **[!UICONTROL Generate Products]**.
