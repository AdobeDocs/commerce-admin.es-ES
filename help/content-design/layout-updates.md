---
title: Actualizaciones de diseño
description: Aprenda a utilizar actualizaciones de diseño para personalizar el diseño de una página.
exl-id: e2d8261f-cae1-4bd4-a047-f861dd7ca14e
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 0%

---

# Actualizaciones de diseño

Antes de empezar a trabajar con actualizaciones de diseño personalizadas, es importante que entiendas cómo se construyen las páginas de tu tienda y la diferencia entre los términos *layout* y *layout update*. Diseño hace referencia a la composición visual y estructural de la página. La actualización de diseño hace referencia a un conjunto específico de instrucciones XML que pueden anular o personalizar el modo en que se construye la página.

El diseño XML del almacén [!DNL Commerce] es una estructura jerárquica de contenedores y bloques. Algunos elementos aparecen en cada página y otros solo en páginas específicas. Para obtener más información sobre diseño, contenedores y bloques, consulte la [descripción general de los diseños](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) en la _Guía para desarrolladores de Frontend_.

La herramienta [Widget](widgets.md) es una forma sencilla de agregar un [bloque de contenido](blocks.md) existente al diseño predeterminado de una página. Para obtener actualizaciones más avanzadas, debe guardar el código de actualización de diseño XML en el servidor y, a continuación, hacer referencia al archivo como una actualización de diseño personalizada desde el administrador. Para obtener una descripción general del proceso, consulte [Usar actualizaciones de diseño](layout-updates.md#place-a-block-using-layout-updates).

En el diagrama siguiente, los nombres que hacen referencia a los contenedores son negros y los tipos de bloque, o rutas de clase de bloque, son azules.

![Diagrama de diseño de bloque estándar](./assets/page-layout-default.png){width="500" zoomable="yes"}

| Tipo de bloque | Descripción |
|--- |--- |
| `page/html` | El nombre de este bloque es `root` y es uno de los pocos bloques raíz del diseño. También puede crear su propio bloque y asignarle el nombre `root`, que es el nombre estándar para bloques de este tipo. Solo puede haber un bloque de este tipo por página. |
| `page/html_head` | El nombre de bloque es `head` y es un elemento secundario del bloque raíz. Solo puede haber un bloque de este tipo por página y no se debe eliminar. |
| `page/html_notices` | El nombre de bloque es `global_notices` y es un elemento secundario del bloque raíz. Si este bloque se elimina del diseño, los avisos globales no aparecerán en la página. Solo puede haber un bloque de este tipo por página. |
| `page/html_header` | El nombre de bloque es `header` y es un elemento secundario del bloque raíz. Este bloque corresponde al encabezado visual en la parte superior de la página y contiene varios bloques estándar. Solo puede haber un bloque de este tipo por página y no se debe eliminar. |
| `page/html_wrapper` | Aunque se incluye en el diseño predeterminado, este bloque está obsoleto y se incluye solo para garantizar la compatibilidad con versiones anteriores. No utilice bloques de este tipo. |
| `page/html_breadcrumbs` | El nombre de este bloque es `breadcrumbs` y es un elemento secundario del bloque de encabezado. Este bloque muestra las rutas de exploración de la página actual. Solo puede haber un bloque de este tipo por página. |
| `page/html_footer` | El nombre de bloque es `footer` y es un elemento secundario del bloque raíz. El bloque de pie de página corresponde al pie de página visual en la parte inferior de la página y contiene varios bloques estándar. Solo puede haber un bloque de este tipo por página y no se debe eliminar. |
| `page/template_links` | Hay dos bloques de este tipo en el diseño estándar. El bloque `top.links` es un elemento secundario del bloque de encabezado y corresponde al menú de navegación superior. El bloque `footer_links` es un elemento secundario del bloque de pie de página y corresponde al menú de navegación inferior. <br/><br/>**_Nota:_**&#x200B;Es posible manipular los vínculos de la plantilla, como se muestra en los ejemplos. |
| `page/switch` | Hay dos bloques de este tipo en un diseño estándar. El bloque `store_language` es un elemento secundario del bloque de encabezado y corresponde al conmutador de idioma superior. El bloque `store_switcher` es un elemento secundario del bloque de pie de página y corresponde al conmutador de almacén inferior. |
| core/messages | Hay dos bloques de este tipo en un diseño estándar. El bloque `global_messages` muestra mensajes globales. El bloque `messages` se usa para mostrar todos los demás mensajes. Si elimina estos bloques, el cliente no verá ningún mensaje. |
| `core/text_list` | Este tipo de bloque se utiliza ampliamente en [!DNL Commerce] como marcador de posición para representar bloques secundarios. |
| `core/profiler` | Solo hay una instancia de este tipo de bloque por página. Se utiliza para el generador de perfiles [!DNL Commerce] interno y no debe usarse para ningún otro fin. |

{style="table-layout:auto"}

## Colocar un bloque mediante actualizaciones de diseño

[Actualizaciones de diseño](layout-updates.md) permiten personalizar el diseño de una página. Las actualizaciones de diseño ofrecen más flexibilidad que un [widget](widgets.md), pero requieren acceso al servidor y conocimientos básicos de XML.

Los siguientes pasos muestran cómo utilizar una actualización de diseño para colocar un bloque en una página. Para obtener ejemplos específicos y ayuda con la sintaxis, consulte [Tareas comunes de personalización de diseños](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) en la _Guía para desarrolladores de Frontend_.

### Paso 1: Crear el bloque

1. Cree el [bloque](block-add.md) que quiera colocar.

1. Tome nota de `block_id`, ya que se utiliza en las instrucciones de actualización de diseño.

### Paso 2: Componga la actualización de diseño en XML

1. Componga las instrucciones de diseño en XML para [hacer referencia a un bloque de CMS](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-manage/).

1. Guarde las [instrucciones de diseño](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-instructions/) en el servidor de la carpeta de diseño donde se guardan los archivos XML para la temática.

   Por ejemplo:

   `<theme_dir>/<Namespace>_<Module>/layout`

   El identificador de diseño es el nombre de archivo que comienza por `cms_page_view_selectable_`, seguido de la clave URL de la página de CMS, la opción de actualización de diseño y el sufijo de archivo `xml`. En el ejemplo siguiente, `customer-service` es la clave URL de la página y `ChatTool` es la opción que selecciona para aplicar la actualización de diseño a la página.

   `cms_page_view_selectable_`&lt;`customer-service`>`_`&lt;`ChatTool`>`.xml`

   | Elemento | Descripción |
   |--- |--- |
   | Identificador de página de CMS | La clave URL de la página con cualquier barra diagonal (`/`) reemplazada por un guion bajo (`_`). |
   | Nombre de actualización de diseño | La opción que aparece para _Actualización de diseño personalizado_. |

   {style="table-layout:auto"}

### Paso 3: Hacer referencia a la actualización de diseño desde la página

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Busque la página donde desee colocar el bloque y ábralo en modo de edición.

1. Desplácese hacia abajo y expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Design]**.

1. Para mostrar todas las actualizaciones de diseño disponibles asociadas con la página, haga clic en el menú **[!UICONTROL Custom Layout Update]**.

   ![Lista de actualización de diseño personalizado](./assets/page-design-custom-layout-update.png){width="400" zoomable="yes"}

1. Seleccione la actualización de diseño que desee aplicar a la página.

### Paso 4: Guardar y actualizar la caché

1. Una vez finalizado, haga clic en **[!UICONTROL Save & Close]**.

1. En el mensaje que aparece en la parte superior del área de trabajo, haga clic en **[!UICONTROL Cache Management]** y actualice todos los elementos de caché no válidos.
