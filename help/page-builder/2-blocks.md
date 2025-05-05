---
title: '[!DNL Page Builder] Tutorial parte 2: bloques'
description: Descubra la diferencia entre bloques simples y bloques dinámicos al usar  [!DNL Page Builder].
exl-id: 864a3078-8cb3-4add-bdb7-14189aba535e
feature: Page Builder, Page Content
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '2054'
ht-degree: 0%

---

# [!DNL Page Builder] Tutorial, parte 2: bloques

El siguiente ejercicio ilustra la diferencia entre [bloques simples](../content-design/blocks.md) y [bloques dinámicos](dynamic-block.md), y cómo usar [!DNL Page Builder] para crear cada tipo de bloque.

>[!NOTE]
>
>[!DNL Page Builder] tiene un nuevo tipo de contenido denominado _Banner_, el cual aparece en el primer ejercicio de tutorial y no está relacionado con la funcionalidad de banner anterior. Lo que antes era la opción Banner en el [menú Contenido](../content-design/content-menu.md), ahora es _Bloque dinámico_.

![Bloque dinámico en la tienda](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

Este ejercicio supone que ha completado [Parte 1: Página simple](1-simple-page.md), incluidos los requisitos previos y [archivos de ejemplo descargados](./assets/simple-page-assets.zip). Siga las partes de este ejercicio de introducción en orden.

>[!NOTE]
>
>Estos ejercicios de introducción se actualizan para reflejar los cambios recientes realizados en el espacio de trabajo [!DNL Page Builder] en la versión 2.4.1.

## Parte 1: Crear un bloque simple

En este ejercicio de tutorial, creará un bloque simple con contenido de [!DNL Google Maps]. Los bloques simples a veces se denominan _bloques CMS_ o _bloques estáticos_, porque el contenido no cambia. Un bloque simple es ideal para contenido que quizá desee reutilizar.

### Paso 1: Crear un bloque

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add New Block]**.

1. Para **[!UICONTROL Block Title]**, escriba `Google Map`.

1. Para **[!UICONTROL Identifier]**, escriba `google-map`.

1. Elija el **[!UICONTROL Store View]** en el que el bloque va a estar disponible.

   ![Información de bloqueo](./assets/pb-tutorial2-block-new-google-map.png){width="600" zoomable="yes"}

1. En la esquina superior derecha, haga clic en **[!UICONTROL Save]**.

### Paso 2: Agregar un(a) [!DNL Google Map]

1. Desplácese hacia abajo hasta la vista previa de contenido [!DNL Page Builder] (actualmente vacía) y haga clic en **[!UICONTROL Edit with Page Builder]**.

1. En el panel [!DNL Page Builder], expanda **[!UICONTROL Media]** y arrastre un marcador de posición **[!UICONTROL Map]** al escenario.

   ![Arrastrando un mapa al escenario](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   Aparecerá un mapa a la ubicación de su tienda si [!DNL Google Maps] está configurado para ella.

   ![Google Map configurado para tu tienda](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   Aparecerá un mapa de marcador de posición si [!DNL Google Maps] aún no se ha configurado para su tienda.

   ![[!DNL Google Maps] marcador de posición](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

1. En la esquina superior derecha del escenario, haga clic en el icono _Cerrar pantalla completa_ (![Icono de cerrar pantalla completa](./assets/pb-icon-reduce.png)).

   Al hacer clic en este icono, volverá a la sección _[!UICONTROL Content]_&#x200B;del bloque con la vista previa mostrada.

1. En la esquina superior derecha, haga clic en la flecha **[!UICONTROL Save]** y elija **[!UICONTROL Save & Close]**.

### Paso 3: Configurar [!DNL Google Maps]

Si [!DNL Google Maps] ya está configurado para su tienda, puede omitir este paso y continuar con el siguiente.

1. Vaya a la [consola de Google Cloud Platform](https://console.cloud.google.com/google/maps-apis/overview).

1. Haga clic en el menú desplegable del proyecto y seleccione o cree el proyecto para el que desea agregar una clave de API.

1. Para configurar las credenciales de la API, siga las [instrucciones][1] de la documentación de [!DNL Google Maps].

1. Copie la clave API en el portapapeles.

1. Vuelva al administrador de [!DNL Commerce] y vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo bajo _[!UICONTROL General]_, elija **[!UICONTROL Content Management]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

   ![Herramientas de contenido avanzadas](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   Para obtener más información acerca de las opciones de configuración de [!UICONTROL Content Management Advanced Tools], consulte la [_Guía de referencia de configuración_](../configuration-reference/general/content-management.md).

1. Para **[!UICONTROL Google Maps API Key]**, pegue la clave que ha copiado.

1. Haga clic en **[!UICONTROL Test Key]**.

   Si hay algún problema con su clave, vuelva al sitio de [!DNL Google Maps] Platform para resolver el problema. A continuación, inténtelo de nuevo.

1. Una vez verificada su clave, haga clic en **[!UICONTROL Save Config]**.

### Paso 4: Añadir el bloque a una página

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. En la cuadrícula, busque el _[!UICONTROL Simple Page]_&#x200B;que creó en el primer tutorial y seleccione **[!UICONTROL Edit]**&#x200B;en la columna&#x200B;_[!UICONTROL Action]_.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Content]** y haga clic en **[!UICONTROL Edit with Page Builder]** o dentro del área de vista previa del contenido.

1. En el panel [!DNL Page Builder] bajo _[!UICONTROL Layout]_, arrastre un marcador de posición **[!UICONTROL Row]**&#x200B;a la parte superior del escenario.

   ![Agregando la fila a la parte superior del escenario](./assets/pb-tutorial2-elements-row-drag-top.png){width="600" zoomable="yes"}

1. En el panel [!DNL Page Builder], expanda **[!UICONTROL Add Content]** y arrastre un marcador de posición **[!UICONTROL Block]** a la nueva fila.

1. Pase el ratón sobre el contenedor de bloques vacío para ver la caja de herramientas y elija el icono _Configuración_ (![icono Configuración](./assets/pb-icon-settings.png){width="20"} ).

   ![Bloquear caja de herramientas](./assets/pb-add-content-block-toolbox.png){width="600" zoomable="yes"}

1. En la página Editar bloque, haga clic en **[!UICONTROL Select Block]**.

   ![Seleccionar bloque](./assets/pb-add-content-block-settings-block-select.png){width="600" zoomable="yes"}

1. En el cuadro de búsqueda, escriba `map` y presione la tecla Intro/Retorno para encontrar el bloque que creó.

   ![Buscar bloque en la lista](./assets/pb-add-content-block-settings-block-find.png){width="600" zoomable="yes"}

1. En la cuadrícula, haga clic en **[!UICONTROL Select]** para elegir el bloque [!DNL Google Maps].

1. En la esquina superior derecha, haga clic en **[!UICONTROL Save]** para guardar la configuración y volver al área de trabajo [!DNL Page Builder].

1. En la esquina superior derecha del escenario, haga clic en el icono _Cerrar pantalla completa_ (![Icono de cerrar pantalla completa](./assets/pb-icon-reduce.png)).

   Al hacer clic en este icono, volverá a la sección _[!UICONTROL Content]_&#x200B;de la página con la vista previa mostrada.

1. En la esquina superior derecha, haga clic en la flecha **[!UICONTROL Save]** y elija **[!UICONTROL Save & Close]**.

**¡Felicitaciones!** Ha completado la primera parte del ejercicio Bloquear. Asegúrese de mantener su trabajo como referencia.

## Parte 2: Crear un bloque dinámico

Un bloque dinámico incluye una lógica que determina dónde, cuándo y a quién aparece. En este ejercicio de tutorial, se crea un bloque dinámico para una promoción que se activa cuando se cumplen las condiciones de la regla de precios y que solo aparece en un segmento de cliente específico. El resultado de este ejemplo es similar al titular que se creó en el primer ejercicio, pero con lógica que controla cuándo aparece en la tienda.

![Ejemplo de promoción de camiseta de Luma](./assets/pb-tutorial2-dynamic-block-row-page.png){width="600" zoomable="yes"}

### Paso 1: Crear un nuevo bloque dinámico

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

   ![Lista de bloques dinámicos](./assets/pb-tutorial2-block-dynamic-add.png){width="700" zoomable="yes"}

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Dynamic Block]**.

   ![Nueva página de Dynamic Block](./assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. Complete la configuración básica del nuevo bloque dinámico:

   - Establezca **[!UICONTROL Enable Dynamic Block]** en `Yes`.

   - Para **[!UICONTROL Dynamic Block Name]**, escriba `Tee Shirt Promo`.

   - Establezca **[!UICONTROL Dynamic Block Type]** en `Content Area` y haga clic en **[!UICONTROL Done]**.

     El tipo de bloque dinámico determina en qué parte del [diseño de página](../content-design/page-layout.md) se coloca el bloque. Al configurar un bloque dinámico para tu tienda, ten en cuenta tanto el diseño de la página como el [tema](../content-design/themes.md), para que puedas aprovechar bien el espacio disponible. Algunas tiendas tienen un área de contenido activo limitada a una anchura fija, mientras que otras amplían la anchura completa de la pantalla.

     ![Configuración del tipo de bloque dinámico](./assets/pb-dynamic-block-type.png){width="600" zoomable="yes"}

   - Para **[!UICONTROL Customer Segment]**, seleccione la casilla de verificación de cada segmento que desee aplicar al bloque dinámico y haga clic en **Listo** para guardar la lista de segmentos.

     En el ejemplo siguiente, hay dos [segmentos de clientes](../customers/customer-segments.md) que identifican a los clientes registrados por sexo. Este bloque dinámico solo aparece para las clientas mujeres registradas que han iniciado sesión en sus cuentas mientras compran en su tienda.

     ![Selección de los segmentos del cliente](./assets/pb-dynamic-block-customer-segment.png){width="600" zoomable="yes"}

### Paso 2: Completar la configuración

Desplácese hacia abajo hasta la sección _[!UICONTROL Content]_, que muestra una vista previa del contenido [!DNL Page Builder] vacío, y haga clic en **[!UICONTROL Edit with Page Builder]**. A continuación, complete las siguientes tareas:

**Tarea 1:** Agregar una imagen de fondo

1. Pase el ratón sobre el contenedor de filas para ver la caja de herramientas y elija el icono _Configuración_ (![Icono de configuración](./assets/pb-icon-settings.png){width="20"} ).

1. En _[!UICONTROL Appearance]_, elija **[!UICONTROL Full Bleed]**.

1. Para **[!UICONTROL Minimum Height]**, escriba `400px`.

1. Desplácese a la sección _[!UICONTROL Background]_&#x200B;y establezca **[!UICONTROL Background Image]**. Para ello, haga clic en **[!UICONTROL Select from Gallery]**&#x200B;y elija la imagen `wide-banner-background.png` cargada en el primer tutorial.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Save]** para aplicar la configuración y volver al área de trabajo [!DNL Page Builder].

   ![Fila con la imagen](./assets/pb-tutorial2-row-image.png){width="600" zoomable="yes"}

**Tarea 2:** Agregar columnas

En el panel [!DNL Page Builder] bajo _[!UICONTROL Layout]_, arrastre un marcador de posición **[!UICONTROL Column]**&#x200B;a la fila.

![Arrastrando el tipo de columna a la fila](./assets/pb-tutorial2-column-drag.png){width="600" zoomable="yes"}

La fila ahora se divide en dos columnas de igual ancho.

**Tarea 3:** Agregar texto

1. En el panel [!DNL Page Builder], expanda **[!UICONTROL Elements]** y arrastre un marcador de posición **Texto** a la segunda columna.

   ![Arrastrando un cuadro de texto a la segunda columna](./assets/pb-tutorial2-column-text-drag.png){width="600" zoomable="yes"}

1. Introduzca las tres líneas de texto siguientes en el editor:

   `Even more ways to mix and match.`

   `Buy 3 Luma tees and get a 4th free.`

   `Shop Tees >`

   ![Escribiendo texto para la columna](./assets/pb-tutorial2-column-text-editor.png){width="600" zoomable="yes"}

1. Seleccione las tres líneas de texto y use la barra de herramientas para establecer el **Alto de línea** en `40px`.

   ![Estableciendo la altura de línea](./assets/pb-tutorial2-column-text-editor-line-height.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Font Size]** para cada línea de la siguiente manera:

   | Línea | Tamaño de fuente |
   |-----| ---------- |
   | Línea 1: | `28px` |
   | Línea 2: | `24px` |
   | Línea 3: | `18px` |

   Dado que este bloque podría colocarse en cualquier lugar de la página, utilice el estilo de párrafo predeterminado en lugar de los niveles de encabezado. Además, no se preocupe de que el texto aún no se ajuste correctamente en la columna.  

   ![Texto con formato](./assets/pb-tutorial2-column-text-editor-text-formatted.png){width="600" zoomable="yes"}

**Tarea 4:** Agregar un vínculo

En el primer ejercicio, aprendió a usar el tipo de contenido [Button](buttons.md) para crear un vínculo. Este ejemplo muestra cómo insertar un vínculo desde la barra de herramientas del editor.

1. En otra pestaña del explorador, abra la tienda y navegue hasta la página que va a ser el destino de destino del vínculo.

   Puede utilizar la dirección URL completa o una dirección URL relativa que omita la referencia al dominio de almacén.

   URL completa
: `https://mystore.com/women/tops-women/tees-women.html`

   URL relativa
: `../women/tops-women/tees-women.html`

1. Vuelva a la ficha y al editor de texto de [!DNL Page Builder] Workspace, seleccione el texto de `Shop Tees >` en la tercera línea y elija **Negrita** (![Botón Negrita](./assets/editor-btn-bold.png)) en la barra de herramientas del editor.

1. Con el texto `Shop Tees >` todavía seleccionado en la tercera línea, elija **Insertar/editar vínculo** (![Botón Insertar/editar vínculo](./assets/pb-icon-add-link.png)) en la barra de herramientas del editor.

   ![Insertando un vínculo](./assets/pb-tutorial2-column-text-editor-link-insert.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL URL]**, escriba el vínculo relativo que ha preparado.

1. Establezca **[!UICONTROL Target]** en `None`.

   Esta configuración abre la página en la misma ventana del explorador, en lugar de abrir una nueva pestaña.

1. Para **[!UICONTROL Title]**, escriba `Shop Tees`.

   Algunos exploradores utilizan el atributo de vínculo Título como información sobre herramientas.

1. Para guardar el vínculo y volver al área de trabajo [!DNL Page Builder], haga clic en **[!UICONTROL OK]**.

   ![Detalles del vínculo](./assets/pb-tutorial2-column-text-editor-link-insert-detail.png){width="600" zoomable="yes"}

1. En la esquina superior derecha del escenario, haga clic en el icono _Cerrar pantalla completa_ (![Icono de cerrar pantalla completa](./assets/pb-icon-reduce.png)).

   Al hacer clic en este icono, volverá a la sección _[!UICONTROL Content]_&#x200B;del bloque dinámico con la vista previa mostrada.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Save]**.

### Paso 3: Añadir una regla de precio

1. Abra de nuevo el bloque dinámico _Tee Shirt Promo_ en el modo de edición.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Related Promotions]** y haga clic en **[!UICONTROL Add Cart Price Rules]**.

   ![Promociones relacionadas](./assets/pb-dynamic-blocks-related-promotions.png){width="600" zoomable="yes"}

1. En la página _Agregar reglas de precio del carro de compras relacionadas_, selecciona la casilla de verificación de _Comprar 3 camisetas y recibe la cuarta regla de precio gratuita_ y haz clic en **[!UICONTROL Add Selected]**.

   ![Agregando una regla de precio del carro de compras relacionada](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

   La regla de precio aparece en la sección _Promociones relacionadas_, en _Regla de precio del carro de compras relacionada_. Puede asociar varias reglas de precios con un bloque dinámico. Sin embargo, este ejemplo sencillo utiliza solo uno.

   ![Regla de precio del carro de compras seleccionada](./assets/pb-dynamic-block-related-cart-price-rule-list.png){width="600" zoomable="yes"}

1. En la esquina superior derecha, haga clic en **[!UICONTROL Save]**.

### Paso 4: Añadir el bloque dinámico a una página

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**

1. Busque la _página simple_ que creó en el [primer ejercicio de tutorial](1-simple-page.md) y ábrala en modo de edición.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Content]** y haga clic en **[!UICONTROL Edit with Page Builder]**.

1. Pase el ratón sobre la fila superior con la misma imagen que el bloque dinámico para mostrar el cuadro de herramientas y el icono _Quitar_ (![Quitar icono](./assets/pb-icon-remove.png){width="20"} ).

   Para confirmar la eliminación de la fila de la página, haga clic en **[!UICONTROL OK]**

1. En el panel [!DNL Page Builder] bajo _[!UICONTROL Layout]_, arrastre un nuevo marcador de posición **[!UICONTROL Row]**&#x200B;a la parte superior del escenario.

1. En el panel [!DNL Page Builder], expanda **[!UICONTROL Add Content]** y arrastre un marcador de posición **[!UICONTROL Dynamic Block]** a la nueva fila.

   ![Arrastrando un bloque dinámico a la fila](./assets/pb-dynamic-block-drag.png){width="600" zoomable="yes"}

1. Pase el ratón sobre el contenedor de bloques dinámicos para mostrar la caja de herramientas y elija el icono _Configuración_ ( ![icono Configuración](./assets/pb-icon-settings.png){width="20"} ).

   ![Cuadro de herramientas de bloques dinámicos](./assets/pb-dynamic-block-settings.png){width="600" zoomable="yes"}

1. En la página _[!UICONTROL Edit Dynamic Block]_, haga clic en **[!UICONTROL Select Dynamic Block]**.

   ![Seleccionar bloque dinámico](./assets/pb-dynamic-block-select.png){width="600" zoomable="yes"}

1. Busque el bloque dinámico _[!DNL Tee Shirt Promo]_&#x200B;que creó y haga clic en **[!UICONTROL Select]**.

   A continuación, aparece un resumen de la información del bloque dinámico.

   ![Información de bloque dinámico](./assets/pb-tutorial2-dynamic-block-edit.png){width="600" zoomable="yes"}

1. Aceptar el valor predeterminado **[!UICONTROL Template]**, `Dynamic Block Block Template`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]** para guardar la configuración y volver al área de trabajo [!DNL Page Builder].

   ![Bloque dinámico en la vista previa de la página](./assets/pb-tutorial2-dynamic-block-on-page.png){width="600" zoomable="yes"}

1. En la esquina superior derecha del escenario, haga clic en el icono _Cerrar pantalla completa_ (![Icono de cerrar pantalla completa](./assets/pb-icon-reduce.png)).

   Al hacer clic en este icono, volverá a la sección _[!UICONTROL Content]_&#x200B;de la página con la vista previa mostrada.

1. En la esquina superior derecha, haga clic en la flecha **[!UICONTROL Save]** y elija **[!UICONTROL Save & Close]**.

Ha completado la segunda parte del ejercicio Bloquear. Asegúrese de mantener su trabajo como referencia.

## Parte 3: Actualización del bloque dinámico

En esta parte final del ejercicio, puede editar un bloque dinámico mientras la página está activa en su tienda. A continuación, inicie sesión en la tienda como miembro del segmento de clientes para que aparezca el bloque.

![Bloque dinámico de muestra en la tienda](./assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

### Paso 1: Editar el bloque dinámico

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. Busque el bloque dinámico _[!DNL Tee Shirt Promo]_&#x200B;en la cuadrícula y ábralo en modo de edición.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Content]** y haga clic en **[!UICONTROL Edit with Page Builder]**.

1. Cambie el ancho de la columna:

   - Pase el ratón sobre el borde entre las dos columnas.

   - Mantenga pulsado el botón del ratón y arrastre el borde dos divisiones hacia la izquierda.

     ![Divisiones de cuadrícula](./assets/pb-tutorial2-dynamic-block-edit-column-width.png){width="600" zoomable="yes"}

     La primera columna tiene ahora cuatro de las 12 (4/12) divisiones de cuadrícula de ancho, y la segunda columna tiene ocho de las 12 (8/12) divisiones de ancho.

     ![Dos columnas desiguales](./assets/pb-tutorial2-dynamic-block-edit-column-width-changed.png){width="600" zoomable="yes"}

1. Cambiar el color del texto:

   - Seleccione las dos primeras líneas del texto.

   - En la barra de herramientas del editor, elija **[!UICONTROL Text Color]** y haga clic en la muestra **[!UICONTROL White]**.

   ![Color del texto](./assets/pb-tutorial2-dynamic-block-edit-text-color.png){width="600" zoomable="yes"}

1. En la esquina superior derecha del escenario, haga clic en el icono _Cerrar pantalla completa_ (![Icono de cerrar pantalla completa](./assets/pb-icon-reduce.png)).

   Al hacer clic en este icono, volverá a la sección _[!UICONTROL Content]_&#x200B;del bloque dinámico con la vista previa mostrada.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Save]**.

### Paso 2: Ver el bloque dinámico

Dado que este bloque dinámico solo es visible para los miembros de un segmento de cliente específico, debe iniciar sesión como cliente que sea miembro del segmento de cliente para ver la promoción. En este ejemplo, el bloque solo aparece para clientes mujeres.

1. Abra una ventana del explorador en la tienda.

1. Para ver la página de ejemplo, modifique la dirección URL en la barra de direcciones de la siguiente manera:

   mystore.com/sample-page

   Si el almacén está configurado para incluir el sufijo html, inclúyalo de la siguiente manera:

   mystore.com/sample-page.html

1. Iniciar sesión como cliente femenina:

   - En la esquina superior derecha de la página principal, haga clic en **[!UICONTROL Sign In]**.

   - Si los datos de Luma de ejemplo están instalados en el sistema, utilice las siguientes credenciales:

     **[!UICONTROL Email]** - `roni_cost@example.com`

     **[!UICONTROL Password]** - `roni_cost3@example.com`

   - Haga clic en **[!UICONTROL Sign In]**.

   - Vuelva a la página de muestra para ver el bloque dinámico que creó con la promoción de camiseta.

   ![Bloque dinámico mostrado para un segmento de cliente](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

Ha completado el ejercicio Bloquear. Asegúrese de mantener su trabajo como referencia.

Cuando esté listo, continúe con [Parte 3: Contenido del catálogo](3-catalog-content.md)

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
