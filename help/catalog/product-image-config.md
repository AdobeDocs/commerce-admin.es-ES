---
title: Configuración de imagen de producto
description: Obtenga información sobre cómo establecer un tamaño de píxel máximo (anchura y altura) y cambiar automáticamente el tamaño de los archivos de imagen del producto durante la carga.
exl-id: d8fce5f8-eddf-4335-9a72-24036db077db
feature: Catalog Management, Products, Media
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 0%

---

# Configuración de imagen de producto

Si tiene pensado cargar imágenes grandes para verlas en el _[!UICONTROL Product Details]_, quizá le interese definir un tamaño de píxel máximo (ancho y alto) y cambiar automáticamente el tamaño de los archivos al cargar. Para admitir este tipo de carga de imagen de producto, existe la opción de habilitar el cambio de tamaño automático de archivos de imagen más grandes a medida que carga. Para el producto que desea añadir al catálogo pero que aún no tiene un recurso de imagen para mostrar, puede configurar una imagen de marcador de posición.

## Cambio de tamaño de imagen de producto

Al cargar imágenes de productos, puede añadir imágenes de mayor tamaño y con distintos tamaños para proporcionar ampliaciones detalladas y de alta calidad de la _[!UICONTROL Product Details]_página. Para garantizar que todas las imágenes tengan un tamaño y un aspecto similares, existe la opción de cambiar el tamaño de las imágenes para garantizar que todas las imágenes coincidan con un tamaño de píxel específico. Esta opción cambia automáticamente el tamaño de todas las imágenes del producto utilizando los ajustes de configuración, lo que puede ayudar con el rendimiento del zoom, la carga más rápida de imágenes y mantener un aspecto uniforme de las imágenes del producto.

>[!NOTE]
>
>Para conseguir la mejor compatibilidad, se recomienda cargar todas las imágenes de productos con `sRGB` perfil de color. Todos los demás perfiles de color se convierten automáticamente en `sRGB` perfil de color durante la carga de la imagen del producto, lo que podría provocar incoherencia de color en la imagen cargada.

Al establecer una anchura y altura de píxel máximas, se cambia el tamaño de la imagen según las dimensiones físicas en píxeles. Commerce cambia el tamaño de la imagen según la cantidad más alta de anchura o altura, manteniendo al mismo tiempo las proporciones. Al reducir la cantidad de calidad de las imágenes JPG, se reduce el tamaño del archivo.

Por ejemplo, un JPG de 3000 x 2100 píxeles al 100% podría ser un archivo de imagen de 5 mb o más. Cambiar el tamaño de esta imagen reduciría la anchura a 1920 píxeles, manteniendo las proporciones y la calidad al 80% para proporcionar un tamaño de archivo mucho más pequeño con alta calidad.

### Habilitar cambio de tamaño de imagen

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL System]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el _Configuración de carga de imágenes_ sección.

   Para cambiar la configuración predeterminada, anule la selección del **[!UICONTROL Use system value]** casilla de verificación si es necesario.

   ![Configuración de carga de imagen](../configuration-reference/advanced/assets/system-image-upload-configuration.png){width="600" zoomable="yes"}

   Para obtener una lista detallada de estas opciones de configuración, consulte [_Configuración de carga de imagen_](../configuration-reference/advanced/system.md#image-upload-configuration) en el _Referencia de configuración_.

1. Para habilitar, asegúrese de lo siguiente **[!UICONTROL Enable Frontend Resize]** se establece en `Yes`.

1. Introduzca una **[!UICONTROL Quality]** configuración entre `1` y `100`%.

   Se recomienda un ajuste entre 80 y 90 % para un tamaño de archivo reducido y alta calidad.

1. Configure las variables **[!UICONTROL Maximum Width]** en píxeles para la imagen.

   Cuando se cambia el tamaño de la imagen, no se supera esta anchura y se conservan las proporciones.

1. Configure las variables **[!UICONTROL Maximum Height]** en píxeles para la imagen.

   Cuando se cambia el tamaño de la imagen, no se supera esta altura y se conservan las proporciones.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

### Descripciones de campos

| Campo | [Ámbito](../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Quality] | Global | Determina la calidad del JPG para la imagen cuyo tamaño se ha cambiado. Una calidad menor reduce el tamaño del archivo. Se recomienda el 80-90% para ayudar a reducir el tamaño del archivo con alta calidad. Predeterminado: 80 |
| [!UICONTROL Enable Frontend Resize] | Global | Permite a Commerce cambiar el tamaño de las imágenes grandes y sobredimensionadas que puede cargar para _[!UICONTROL Product Details]_página. Commerce cambia el tamaño de los archivos de imagen mediante JavaScript al cargar el archivo. Cuando se cambia el tamaño de la imagen, se conservan las proporciones exactas, para cumplir y no superar el tamaño más grande para la anchura máxima o la altura máxima. Predeterminado: `Yes` |
| [!UICONTROL Maximum Width] | Global | Determina la anchura máxima en píxeles de la imagen. Cuando se cambia el tamaño de la imagen, no se supera esta anchura. Predeterminado: `1920` |
| [!UICONTROL Maximum Height] | Global | Determina la altura máxima en píxeles de la imagen. Cuando se cambia el tamaño de la imagen, no se supera esta altura. Predeterminado: `1200` |

{style="table-layout:auto"}

## Marcadores de imagen

Adobe Commerce y Magento Open Source utilizan imágenes temporales como marcadores de posición hasta que las imágenes de producto permanentes estén disponibles. Se puede cargar un marcador de posición diferente para cada función. La imagen inicial del marcador de posición es un logotipo de ejemplo, que puede reemplazar por la imagen de su elección.

![Marcador de imagen](./assets/storefront-image-placeholder.png){width="600" zoomable="yes"}

**_Para cargar imágenes de marcador de posición:_**

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Expandir ![Icono de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Product Image Placeholders]** sección.

   ![Marcadores de imagen del producto](../configuration-reference/catalog/assets/catalog-product-image-placeholders.png){width="600" zoomable="yes"}

   Para obtener una lista detallada de estas opciones de configuración, consulte [_Marcadores de imagen del producto_](../configuration-reference/catalog/catalog.md#product-image-placeholders) en el _Referencia de configuración_.

1. Para cada función de imagen, haga clic en **[!UICONTROL Choose File]**, busque la imagen en el equipo y cargue el archivo.

   Puede utilizar la misma imagen para las tres funciones o cargar una imagen de marcador de posición diferente para cada función.

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

Para obtener información sobre las funciones de imagen y los tamaños recomendados, consulte [Cargar una imagen](product-image.md#upload-an-image).
