---
title: Configuración del producto - [!UICONTROL Customizable Options]
description: Para un producto, la configuración de [!UICONTROL Customizable Options] le permite ofrecer una selección de opciones con tipos de entrada de texto, selección y fecha.
exl-id: 7d23c5c5-2b2a-4f2a-b843-9c27b851be5f
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 0%

---

# Configuración del producto - [!UICONTROL Customizable Options]

Añadir opciones personalizables a un producto es una manera sencilla de ofrecer una selección de opciones con tipos de entrada de texto, selección y fecha. Las opciones personalizables son una buena solución si las necesidades del inventario son simples. Sin embargo, como se basan en variaciones de un solo SKU, no se pueden utilizar para administrar acciones o como base de las condiciones de las reglas de precios. Si tiene varios productos con las mismas opciones, puede configurar un producto e importar las opciones a los demás productos.

Cuando un cliente compra un producto con una opción personalizable, aparece una descripción de cada opción seleccionada debajo de la descripción del producto y cualquier marca asociada (o markdown) se aplica automáticamente al precio del artículo.

![Detalles del producto con opción personalizable](./assets/storefront-customizable-option-product-detail.png){width="700" zoomable="yes"}

Si la compra activa una regla de precio del carro de compras, el cálculo inicial se aplica primero al precio del producto y, en segundo lugar, al precio del artículo de línea con cualquier ajuste para las opciones personalizables aplicables. En el siguiente ejemplo, el cliente compra una bolsa de lona por 74,00 $, además de una opción personalizable para un monograma. Se aplica un margen de 14,80 $ al precio base del producto y el precio ajustado se muestra como 88,80 $. En este caso, la compra de la bolsa de lona déclencheur una regla de precio del carro de compras basada en el SKU del producto y aplica un descuento a la compra, además del envío gratuito. Aunque la regla de precio del carro de compras no se activa mediante la opción personalizable, aplica el descuento al contenido del carro de compras, lo que incluye el marcado de la opción personalizable.

![Carro con opción personalizable y regla de precio](./assets/storefront-customizable-option-cart-price-rule.png){width="700" zoomable="yes"}

>[!NOTE]
>
>No se aplica un descuento de regla de precio de catálogo a las opciones personalizables de precio fijo.

## Crear opciones personalizables

1. Abra el producto en modo de edición.

1. Desplácese hacia abajo y expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección _[!UICONTROL Customizable Options]_.

1. Haga clic en **[!UICONTROL Add Option]**.

   ![Opciones personalizables](./assets/product-customizable-options.png){width="600" zoomable="yes"}

1. Complete la nueva configuración de opciones:

   - Para **[!UICONTROL Option Title]**, escriba un nombre para la opción.

   - Establezca **[!UICONTROL Option Type]** para el tipo de entrada de datos.

   - Si la opción no es necesaria para adquirir el producto, anule la selección de la casilla de verificación **[!UICONTROL Required]**.

1. Rellene los campos según el tipo de entrada de datos:

   - Para **[!UICONTROL Title]**, escriba un nombre para esta opción.

   - (Opcional) Para **[!UICONTROL Price]**, introduzca cualquier margen de beneficio o margen de beneficio del precio de producto base que se aplique a esta opción.

   - Establezca **[!UICONTROL Price Type]** en una de las siguientes opciones:

      - `Fixed`: el precio de la variación difiere del precio del producto base en una cantidad monetaria fija, como 1 $.
      - `Percentage`: el precio de la variación difiere del precio del producto base en un porcentaje, como 10 %.

   - (Opcional) Escriba un **[!UICONTROL SKU]** para la opción. El SKU de opción es un sufijo que se añade al SKU del producto.

   - Si _[!UICONTROL Option Type]_&#x200B;es `File`, establezca los parámetros del archivo. Para **[!UICONTROL Compatible File Extensions]**, escriba las extensiones válidas como valores separados por comas (como `png, jpg, gif`). Para **[!UICONTROL Maximum Image Size]**, escriba el tamaño máximo de la imagen en píxeles. Si es una entrada de texto, escriba el valor máximo de **[!UICONTROL Maximum Characters]**.

   ![Agregar valores para la opción de personalización](./assets/product-customizable-options-add-values.png){width="600" zoomable="yes"}

1. (Opcional) Si desea agregar otra opción personalizable, haga clic en **[!UICONTROL Add Option]**.

   - Complete la configuración como antes.

   - Para cambiar el orden de las opciones, haga clic en el icono _[!UICONTROL Order]_![Icono de orden](../assets/icon-sort-order.png) y arrastre la opción a una nueva posición en la lista.

   Repita este paso para cada opción que desee añadir.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

## Importar opciones personalizables

1. En la sección _Opciones personalizables_, haga clic en **[!UICONTROL Import Options]**.


1. Todos los productos con opciones personalizables aparecen en la cuadrícula.

1. En la lista, seleccione la casilla del producto con las opciones que desea importar.

1. Haga clic en **[!UICONTROL Import]**.

1. Una vez finalizado, puede seguir agregando más opciones personalizadas o hacer clic en **[!UICONTROL Save and Close]**.

## Tipos de entrada

| Tipo | Descripción |
|---------------------|---------------|
| [!UICONTROL Text] | Línea de entrada o cuadro de texto en el que el cliente puede introducir la información necesaria. Opciones: <br />**[!UICONTROL Field]**: campo de entrada de una sola línea para texto.<br />**[!UICONTROL Area]** - Campo de entrada de varias líneas. Este tipo no admite formatos avanzados como HTML. Utilice caracteres máximos para limitar la longitud del texto que se puede introducir y garantizar la representación correcta del texto introducido en el administrador. |
| [!UICONTROL File] | Permite al cliente cargar un archivo. |
| [!UICONTROL Select] | Permite al cliente seleccionar una o varias opciones, según el tipo de entrada utilizado. Opciones: <br />**[!UICONTROL Drop-down]**: una lista desplegable de opciones que sólo permite una selección.<br />**[!UICONTROL Radio Buttons]**: conjunto de opciones que permite una sola selección.<br />**[!UICONTROL Checkbox]**: una casilla de verificación es una variación de una opción sí/no. Si el producto tiene más de una casilla de verificación, se pueden realizar varias selecciones.<br />**[!UICONTROL Multiple Select]**: cuadro de lista desplegable de opciones que acepta varias selecciones. Para elegir varias opciones, mantenga presionada la tecla Ctrl (PC) o Comando (Mac) y haga clic en cada opción. |
| [!UICONTROL Date] | Permite al cliente introducir una fecha u hora o elegir el valor de un calendario. Opciones: <br />**[!UICONTROL Date]**: campo de entrada para un valor de fecha. La fecha se puede escribir directamente en el campo o seleccionarse de una lista o calendario. El método y formato de entrada están determinados por la configuración [opciones de fecha y hora](attributes-input-types.md#date-and-time-options).<br />**[!UICONTROL Date & Time]**: campo de entrada para un valor de fecha y hora.<br />**[!UICONTROL Time]**: campo de entrada para un valor de tiempo. |

{style="table-layout:auto"}
