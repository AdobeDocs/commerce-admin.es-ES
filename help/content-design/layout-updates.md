---
title: Actualizaciones de diseño
description: Aprenda a utilizar actualizaciones de diseño para personalizar el diseño de una página.
exl-id: e2d8261f-cae1-4bd4-a047-f861dd7ca14e
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '1007'
ht-degree: 0%

---

# Actualizaciones de diseño

Antes de empezar a trabajar con actualizaciones de diseño personalizadas, es importante comprender cómo se construyen las páginas de la tienda y la diferencia entre los términos *layout* y *actualización del diseño*. Diseño hace referencia a la composición visual y estructural de la página. La actualización de diseño hace referencia a un conjunto específico de instrucciones XML que pueden anular o personalizar el modo en que se construye la página.

El diseño XML de su [!DNL Commerce] store es una estructura jerárquica de contenedores y bloques. Algunos elementos aparecen en cada página y otros solo en páginas específicas. Para obtener más información sobre el diseño, los contenedores y los bloques, consulte la [Información general de diseños](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) en el _Guía para desarrolladores de Frontend_.

El [Widget](widgets.md) herramienta es una forma sencilla de agregar una existente [bloque de contenido](blocks.md) al diseño predeterminado de una página. Para obtener actualizaciones más avanzadas, debe guardar el código de actualización de diseño XML en el servidor y, a continuación, hacer referencia al archivo como una actualización de diseño personalizada desde el administrador. Para obtener una descripción general del proceso, consulte [Usar actualizaciones de diseño](layout-updates.md#place-a-block-using-layout-updates).

En el diagrama siguiente, los nombres que hacen referencia a los contenedores son negros y los tipos de bloque, o rutas de clase de bloque, son azules.

![Diagrama de diseño de bloque estándar](./assets/page-layout-default.png){width="500" zoomable="yes"}

| Tipo de bloque | Descripción |
|--- |--- |
| `page/html` | El nombre de este bloque es `root` y es uno de los pocos bloques raíz en el diseño. También puede crear su propio bloque y ponerle un nombre `root`, que es el nombre estándar para bloques de este tipo. Solo puede haber un bloque de este tipo por página. |
| `page/html_head` | El nombre del bloque es `head` y es un elemento secundario del bloque raíz. Solo puede haber un bloque de este tipo por página y no se debe eliminar. |
| `page/html_notices` | El nombre del bloque es `global_notices` y es un elemento secundario del bloque raíz. Si este bloque se elimina del diseño, los avisos globales no aparecerán en la página. Solo puede haber un bloque de este tipo por página. |
| `page/html_header` | El nombre del bloque es `header` y es un elemento secundario del bloque raíz. Este bloque corresponde al encabezado visual en la parte superior de la página y contiene varios bloques estándar. Solo puede haber un bloque de este tipo por página y no se debe eliminar. |
| `page/html_wrapper` | Aunque se incluye en el diseño predeterminado, este bloque está obsoleto y se incluye solo para garantizar la compatibilidad con versiones anteriores. No utilice bloques de este tipo. |
| `page/html_breadcrumbs` | El nombre de este bloque es `breadcrumbs` y es un elemento secundario del bloque de encabezado. Este bloque muestra las rutas de exploración de la página actual. Solo puede haber un bloque de este tipo por página. |
| `page/html_footer` | El nombre del bloque es `footer` y es un elemento secundario del bloque raíz. El bloque de pie de página corresponde al pie de página visual en la parte inferior de la página y contiene varios bloques estándar. Solo puede haber un bloque de este tipo por página y no se debe eliminar. |
| `page/template_links` | Hay dos bloques de este tipo en el diseño estándar. El `top.links` block es un elemento secundario del bloque header y corresponde al menú de navegación superior. El `footer_links` block es un elemento secundario del bloque footer y corresponde al menú de navegación inferior. <br/><br/>**_Nota:_**Es posible manipular los vínculos de la plantilla, como se muestra en los ejemplos. |
| `page/switch` | Hay dos bloques de este tipo en un diseño estándar. El `store_language` block es un elemento secundario del bloque de encabezado y corresponde al conmutador de idioma superior. El `store_switcher` block es un elemento secundario del bloque footer y corresponde al conmutador de almacén inferior. |
| core/messages | Hay dos bloques de este tipo en un diseño estándar. El `global_messages` block muestra mensajes globales. El `messages` se utiliza para mostrar todos los demás mensajes. Si elimina estos bloques, el cliente no verá ningún mensaje. |
| `core/text_list` | Este tipo de bloque se utiliza ampliamente en [!DNL Commerce] como marcador de posición para procesar bloques secundarios. |
| `core/profiler` | Solo hay una instancia de este tipo de bloque por página. Se utiliza para el informe interno [!DNL Commerce] generador de perfiles y no debe utilizarse para ningún otro fin. |

{style="table-layout:auto"}

## Colocar un bloque mediante actualizaciones de diseño

[Actualizaciones de diseño](layout-updates.md) permiten personalizar el diseño de una página. Las actualizaciones de diseño ofrecen más flexibilidad que una [widget](widgets.md), pero requieren acceso al servidor y un conocimiento básico de XML.

Los siguientes pasos muestran cómo utilizar una actualización de diseño para colocar un bloque en una página. Para ver ejemplos específicos y ayuda con la sintaxis, consulte [Tareas comunes de personalización de diseños](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) en el _Guía para desarrolladores de Frontend_.

### Paso 1: Crear el bloque

1. Cree el [bloquear](block-add.md) que desee colocar.

1. Tome nota de la `block_id`, porque se utiliza en las instrucciones de actualización de diseño.

### Paso 2: Componga la actualización de diseño en XML

1. Componga las instrucciones de diseño en XML para [Hacer referencia a un bloque CMS](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-manage/).

1. Guarde el [instrucciones de diseño](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-instructions/) en el servidor de la carpeta de diseño donde se guardan los archivos XML para la temática.

   Por ejemplo:

   `<theme_dir>/<Namespace>_<Module>/layout`

   El controlador de diseño es el nombre de archivo que comienza por `cms_page_view_selectable_`, seguido de la clave URL de la página de CMS, la opción de actualización de diseño y la variable `xml` sufijo de archivo. En el ejemplo siguiente, `customer-service` es la clave URL de la página y `ChatTool` es la opción que selecciona para aplicar la actualización de diseño a la página.

   `cms_page_view_selectable_`&lt;`customer-service`>`_`&lt;`ChatTool`>`.xml`

   | Elemento | Descripción |
   |--- |--- |
   | Identificador de página de CMS | La clave URL de la página con cualquier barra diagonal (`/`) reemplazado por un guion bajo (`_`). |
   | Nombre de actualización de diseño | La opción que aparece para _Actualización de diseño personalizado_. |

   {style="table-layout:auto"}

### Paso 3: Hacer referencia a la actualización de diseño desde la página

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Busque la página donde desee colocar el bloque y ábralo en modo de edición.

1. Desplazarse hacia abajo y expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Design]** sección.

1. Para mostrar todas las actualizaciones de diseño disponibles asociadas con la página, haga clic en **[!UICONTROL Custom Layout Update]** menú.

   ![Lista de actualización de diseño personalizado](./assets/page-design-custom-layout-update.png){width="400" zoomable="yes"}

1. Seleccione la actualización de diseño que desee aplicar a la página.

### Paso 4: Guardar y actualizar la caché

1. Cuando termine, haga clic en **[!UICONTROL Save & Close]**.

1. En el mensaje situado en la parte superior del espacio de trabajo, haga clic en **[!UICONTROL Cache Management]** y actualice todos los elementos de caché no válidos.
