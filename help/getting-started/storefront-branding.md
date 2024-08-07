---
title: Marca de tienda
description: Aprenda a cambiar los elementos que definen la identidad de marca de su tienda.
exl-id: 91630717-9da7-4d2f-a0d8-adb794a30ee1
feature: Storefront
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '1309'
ht-degree: 0%

---

# Marca de tienda

Una de las primeras cosas que debes hacer es [cambiar el logotipo](#upload-your-logo) en el encabezado y [cargar un favicon](#add-a-favicon) para el navegador. A continuación, debería [agregar su mensaje de bienvenida](#change-the-welcome-message) y [actualizar el aviso de copyright](#change-the-copyright-notice) en el pie de página. Estas tareas son algunos elementos de diseño simples que puede cuidar de inmediato. Mientras tu tienda está en desarrollo, puedes [activar el aviso de demostración de la tienda](#set-the-store-demo-notice) y luego eliminarlo cuando estés listo para iniciarla.

![Elementos de personalización de marca de tienda](./assets/storefront-home-page-branding.png){width="600" zoomable="yes"}

## Cargue su logotipo

El tamaño y la ubicación del logotipo en el encabezado están determinados por la temática de la tienda. Su logotipo puede guardarse como archivo de GIF, PNG o de JPG (JPEG) de la tienda y cargarse desde el administrador de la misma.

![Logotipo en el encabezado](./assets/storefront-header-logo.png){width="600"}

La imagen del logotipo reside en la siguiente ubicación del servidor. Cualquier archivo de imagen con el nombre `logo.svg` se utiliza como logotipo del tema predeterminado.

Ruta de acceso completa: `app/design/frontend/[vendor]/[theme]/web/images/logo.svg`

Ruta relativa - `images/logo.svg`

Si no conoce el tamaño del logotipo u otras imágenes utilizadas en la temática, abra la página en un explorador, haga clic con el botón derecho en la imagen e inspeccione el elemento.

>[!NOTE]
>
>Además del logotipo en el encabezado, su logotipo también aparece en [plantillas de correo electrónico](../systems/email-templates.md#prepare-your-email-logo) y en [facturas de PDF](../stores-purchase/sales-documents.md) y otros documentos de ventas. Los logotipos utilizados para las plantillas de correo electrónico y las facturas tienen requisitos de tamaño diferentes y deben cargarse por separado.

Formatos de archivo de logotipo admitidos:

| Formato de archivo | Descripción |
|--- |--- |
| PNG | (Portable Network Graphics) Esta nueva alternativa al formato GIF admite hasta 16 millones de colores (24 bits). El formato de compresión sin pérdidas produce una imagen de mapa de bits de alta calidad con texto nítido, pero un tamaño de archivo mayor que el de algunos formatos. El formato PNG admite capas transparentes y está diseñado para la visualización y transmisión en línea. |
| GIF | (Formato de intercambio de gráficos) Formato de mapa de bits antiguo y ampliamente admitido que está limitado a 256 colores (8 bits). El formato GIF admite animación simple y capas transparentes. |
| JPG (JPEG) | (Grupo Mixto de Expertos Fotográficos) Formato de mapa de bits comprimido que utilizan la mayoría de las cámaras digitales. La compresión con pérdida causa cierta pérdida de datos, que a veces se nota como puntos borrosos en el texto. |

{style="table-layout:auto"}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

   ![Página de configuración de diseño](./assets/design-configuration.png){width="700"}

1. Busque la vista de tienda que desea configurar y haga clic en **[!UICONTROL Edit]** en la columna _[!UICONTROL Action]_.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Header]**.

   ![Configuración del encabezado](./assets/configuration-header.png){width="600"}

1. Para cargar un nuevo logotipo, haga clic en **[!UICONTROL Upload]** y elija el archivo de su sistema.

1. Escriba **[!UICONTROL Logo Image Width]** y **[!UICONTROL Logo Image Height]** en píxeles.

1. Para **[!UICONTROL Logo Image Alt]**, escriba el texto que desea que aparezca cuando alguien pase el ratón sobre la imagen.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Configuration]**.

## Añadir un icono de favoritos

_Favicon_ es la abreviatura de _icono favorito_ y hace referencia al icono pequeño de la ficha de cada página del explorador. Según el explorador, el icono de favoritos también aparece en la barra de direcciones, justo antes de la dirección URL.

Un icono de favoritos suele tener un tamaño de 16 x 16 píxeles o de 32 x 32 píxeles. [!DNL Commerce] acepta los tipos de archivo ICO, PNG, APNG, GIF JPG y JPEG, aunque no todos los exploradores admiten estos formatos. El formato de archivo más utilizado para un favicon es ICO. Puede utilizar otros tipos de archivo de imagen, pero es posible que el formato no sea compatible con todos los exploradores. Hay muchas herramientas gratuitas disponibles en línea que puede utilizar para generar una imagen ICO o convertir una imagen a ese formato.

![Favicon en la ficha del explorador](./assets/storefront-favicon.png){width="600"}

[!DNL Commerce] admite los siguientes formatos de archivo como icono de favoritos:

| Formato de archivo | Descripción |
|--- |--- |
| ICO | Este formato de archivo de imagen está diseñado para imágenes de iconos de ordenador de pequeño tamaño. Utilizado principalmente en el sistema operativo Microsoft® Windows, el formato ICO puede contener imágenes de hasta 256 x 256 píxeles y 16 millones de colores (24 bits) con 8 bits de transparencia. |
| PNG | (Portable Network Graphics) Esta nueva alternativa al formato GIF admite hasta 16 millones de colores (24 bits). El formato de compresión sin pérdidas produce una imagen de mapa de bits de alta calidad con texto nítido, pero un tamaño de archivo mayor que el de algunos formatos. El formato PNG admite capas transparentes y está diseñado para la visualización y transmisión en línea. |
| APNG | (Gráficos de red portátiles animados) Formato de archivo similar a PNG que admite animación simple. |
| GIF | (Formato de intercambio de gráficos) Formato de mapa de bits antiguo y ampliamente admitido que está limitado a 256 colores (8 bits). El formato GIF admite animación simple y capas transparentes. |
| JPG (JPEG) | (Grupo Mixto de Expertos Fotográficos) Formato de mapa de bits comprimido que utilizan la mayoría de las cámaras digitales. La compresión con pérdida causa cierta pérdida de datos, que a veces se nota como puntos borrosos en el texto. |

{style="table-layout:auto"}

### Paso 1: Crear un icono de favoritos

1. Con el editor de imágenes que elija, cree una imagen gráfica de su logotipo de 16 x 16 o 32 x 32.

1. (Opcional) Utilice una de las herramientas en línea disponibles para convertir el archivo al formato .ico y guardarlo en el equipo.

### Paso 2: Sube el icono de favoritos a tu tienda

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. En la cuadrícula, busque la vista de almacén que desea configurar y haga clic en **[!UICONTROL Edit]** en la columna _[!UICONTROL Action]_.

1. En _[!UICONTROL Other Settings]_, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL HTML Head]**.

   ![Configuración del encabezado del HTML](./assets/configuration-html-head.png){width="600"}

1. Si desea quitar el favicon actual, haga clic en el icono _Eliminar_ (![icono de la papelera](../assets/icon-delete-trashcan.png)) en la esquina inferior izquierda de la imagen.

1. Haga clic en **[!UICONTROL Upload]** y abra el archivo de favicon que ha preparado.

   ![Favicon cargado](./assets/favicon-upload.png){width="400"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Configuration]**.

### Paso 3: Actualizar la caché

1. Cuando se le pida que actualice la caché, haga clic en el vínculo **[!UICONTROL Cache Management]** en el mensaje en la parte superior del área de trabajo.

1. En la lista, seleccione la casilla de verificación **[!UICONTROL Page Cache]** que está marcada como `Invalidated`.

1. Establezca **[!UICONTROL Actions]** en `Refresh` y haga clic en **[!UICONTROL Submit]**.

1. Para ver el nuevo icono de favoritos, vuelve a tu tienda y actualiza el navegador.

## Cambio del mensaje de bienvenida

El mensaje de bienvenida del encabezado se amplía para incluir el nombre del cliente que ha iniciado sesión. Antes de iniciar la tienda, asegúrese de cambiar el texto predeterminado _Bienvenido_ para cada vista de tienda.

![Mensaje de bienvenida](./assets/storefront-welcome-message.png){width="600"}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. En la cuadrícula, busque la vista de almacén que desea configurar y haga clic en **[!UICONTROL Edit]** en la columna _[!UICONTROL Action]_.

1. En _[!UICONTROL Other Settings]_, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Header]**.

1. Para **[!UICONTROL Welcome Text]**, escriba el texto del mensaje de bienvenida que desea que aparezca en el encabezado de su tienda.

   ![Configuración del encabezado](./assets/configuration-header.png){width="600"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Configuration]**.

1. Cuando se le pida que actualice la caché de páginas, haga clic en el vínculo **[!UICONTROL Cache Management]** en la parte superior del área de trabajo y siga las instrucciones para actualizar la caché.

## Cambiar el aviso de copyright

La tienda muestra un aviso de copyright al pie de cada página. Como práctica recomendada, el aviso de copyright debe incluir el año actual e identificar a su empresa como el propietario legal del contenido del sitio.

![Ejemplo de aviso de copyright](./assets/storefront-footer-copyright.png){width="600"}

El código de carácter `&copy;` se utiliza para insertar el símbolo de copyright, como se muestra en los ejemplos siguientes:

- Ejemplo de formato largo

  `Copyright &copy; 2013-present Luma, Inc. All rights reserved.`

- Ejemplo de formato corto

  `&copy; 2021 Luma, Inc. All rights reserved.`

**_Para actualizar el aviso de copyright:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. En la cuadrícula, busque la vista de almacén que desea configurar y haga clic en **[!UICONTROL Edit]** en la columna _[!UICONTROL Action]_.

1. En _Otra configuración_, expanda ![Selector de expansión](../assets/icon-display-expand.png)la sección **[!UICONTROL Footer]**.

   ![Configuración del diseño del pie de página](./assets/configuration-footer.png){width="600"}

1. Para **[!UICONTROL Copyright]**, escriba el aviso de copyright que desea que aparezca en el pie de página de cada página.

   Utilice el código de carácter `&copy;` para insertar un símbolo de copyright.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Configuration]**.

## Configurar el aviso de demostración de tienda

Si la tienda está en línea, pero aún está en construcción, puede mostrar un aviso de demostración en la parte superior de la página para que la gente sepa que la tienda aún no está abierta para los negocios. Cuando esté listo para _publicar_, simplemente quite el mensaje. Es similar a voltear el letrero que cuelga en la ventana de _Cerrado_ a _Abierto_. El formato del aviso de demostración está determinado por el tema de su tienda.

![Aviso de demostración de tienda](./assets/storefront-demo-notice.png){width="600"}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. En la cuadrícula, busque la vista de almacén que desea configurar y haga clic en **[!UICONTROL Edit]** en la columna _[!UICONTROL Action]_.

1. En _[!UICONTROL Other Settings]_, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL HTML Head]**.

   ![Cabeza de HTML](./assets/configuration-html-head.png){width="600"}

1. Desplácese hacia abajo hasta la parte inferior y establezca **[!UICONTROL Display Demo Store Notice]** según sus preferencias.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Configuration]**.

1. Si se le pide que actualice la caché, haga clic en **[!UICONTROL Cache Management]** en el mensaje del sistema y siga las instrucciones para actualizar la caché.
