---
title: Jerarquía de páginas
description: Descubra cómo el sistema de jerarquía de páginas le permite organizar las páginas de contenido y agregar paginación, navegación y menús.
exl-id: 2ce79b85-1420-4640-a4f7-0143a608a71a
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 0%

---

# Jerarquía de páginas

{{ee-feature}}

El sistema de jerarquía de páginas de almacenamiento le permite organizar las páginas de contenido y agregar paginación, navegación y menús. La página Política de privacidad de los datos de ejemplo es un ejemplo de una página con un menú a la izquierda. Si publica una gran cantidad de contenido regularmente, puede utilizar una jerarquía de páginas para organizar el contenido y facilitar la búsqueda de artículos de interés.

El sistema de jerarquía de páginas utiliza nodos para identificar fragmentos de contenido relacionados y organizar las páginas de contenido en relaciones principales/secundarias. Un nodo principal es como una carpeta que puede contener nodos y páginas secundarios. La posición relativa de cada nodo y página en la jerarquía se muestra como una estructura de _árbol_. Un nodo puede contener otros nodos y páginas de contenido, y una sola página de contenido puede asociarse con varios nodos y otras páginas de contenido en una relación principal/secundario o de vecino.

![Página con navegación izquierda](./assets/storefront-privacy-policy.png){width="600" zoomable="yes"}

## Configurar jerarquía de páginas

Los ajustes de configuración activan el sistema de jerarquía de páginas y los metadatos, y determinan el diseño de menú predeterminado.

![Jerarquía de páginas de CMS](./assets/content-management-cms-page-hierarchy.png){width="600" zoomable="yes"}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo bajo _[!UICONTROL General]_, elija **[!UICONTROL Content Management]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL CMS Page Hierarchy]** y realice los cambios que sean necesarios.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | Activa el uso de la jerarquía de páginas para las páginas de contenido. Opciones: `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | Cuando esta opción está habilitada, puede asociar metadatos con páginas de la jerarquía. Opciones: `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | Determina el estilo de menú predeterminado. Opciones: `Content` / `Left Column` / `Right Column` |

{style="table-layout:auto"}

## Adición de un nodo de jerarquía

En el siguiente ejemplo se muestra cómo crear un nodo con navegación sencilla a páginas de contenido relacionadas. Aunque un nodo no tiene una página de contenido asociada, tiene una clave URL a la que se puede hacer referencia en cualquier otra parte del sitio.

Por ejemplo, podría crear un nodo denominado _Comunicados de prensa_ que tenga acceso a comunicados de prensa individuales. A continuación, puede incluir el vínculo en su página _Acerca de nosotros_ al nodo. O puede crear un nodo para una colección de números anteriores de la newsletter.

Para vincular a un nodo, usa la herramienta [Widget](widgets.md) para crear un vínculo de nodo de jerarquía de CMS y coloca el widget en un bloque de contenido o una página.

![Ejemplo de menú de navegación en la página Acerca de nosotros](./assets/page-navigation-storefront.png){width="600" zoomable="yes"}

### Paso 1: Crear un nodo

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Hierarchy]**.

   ![Cuadrícula de páginas CMS](./assets/page-hierarchy-cms-pages.png){width="600" zoomable="yes"}

1. Sobre la cuadrícula, haga clic en **[!UICONTROL Add Node...]**.

1. En _[!UICONTROL Page Properties]_, escriba un **[!UICONTROL Title]**&#x200B;para el nodo y un **[!UICONTROL URL Key]**&#x200B;adecuado.

   La clave URL proporciona una dirección web única para el nodo. Debe tener todos los caracteres en minúsculas, con guiones para separar las palabras, en lugar de los espacios.

   ![Propiedades de página](./assets/page-hierarchy-add-node-page-properties.png){width="500" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save]**.

   El nodo aparece como una carpeta en el árbol a la izquierda de la página.

### Paso 2: Agregar páginas al nodo

1. En el árbol de jerarquía, haga clic en para seleccionar el nodo.

1. Haga clic en **[!UICONTROL Add Selected Pages(s) to Tree]**.

   Puede desplazarse hacia arriba para ver que cada página seleccionada aparece en el árbol debajo de la carpeta del nodo.

### Paso 3: Definición de la estructura

1. Si es necesario, arrastre las páginas a su posición para reflejar el orden en que aparecerán en el menú.

   ![Arrastrando páginas a la posición](./assets/page-hierarchy-drag-to-position.png){width="500" zoomable="yes"}

1. Haga clic en el nodo en la parte superior de la jerarquía.

   La sección _[!UICONTROL Page Properties]_&#x200B;ahora muestra información sobre el nodo.

1. En **[!UICONTROL Render Metadata in HTML Head]**, haga lo siguiente:

   ![Procesar configuración de metadatos](./assets/page-hierarchy-render-metadata.png){width="400" zoomable="yes"}

   - Para identificar el nodo como la parte superior de la jerarquía, establezca **[!UICONTROL First]** en `Yes`.

   - Para mostrar un control de paginación, establezca **[!UICONTROL Next/Previous]** en `Yes`.

   - Para organizar las páginas de la jerarquía como un libro, establezca **[!UICONTROL Enable Chapter/Section]** en `Yes`.

     Si no desea incluir el nodo como parte del libro, deje el valor predeterminado `No`.

   - Para asignar el nodo a una parte específica del libro, establezca **[!UICONTROL Chapter/Section]** en una de las siguientes opciones:

      - `No`: no define el nodo como capítulo/sección.
      - `Chapter` - Asigna el nodo actual como un capítulo.
      - `Section` - Asigna el nodo actual como una sección.
      - `Both` - Asigna el nodo actual como capítulo y sección.

### Paso 4: Añadir controles de paginación

1. En _Opciones de paginación para páginas anidadas_, establezca **[!UICONTROL Enable Pagination]** en `Yes`.

1. Para **[!UICONTROL Frame]**, escriba el número de vínculos de página que desea incluir en el control de paginación.

   Si hay más páginas en la jerarquía que se pueden incluir en el control de paginación.

1. En **[!UICONTROL Frame Skip]**, escriba el número de páginas que desea saltar para el siguiente conjunto de vínculos de paginación.

### Paso 5: Selección del diseño del menú

Si desea que el nodo aparezca en el menú, haga lo siguiente:

1. En _Opciones del menú de navegación de páginas_, establezca **[!UICONTROL Show in navigation menu]** en `Yes`.

   Esta configuración determina si se genera un menú de navegación para la jerarquía de páginas.

   ![Opciones del menú de navegación de la página](./assets/page-hierarchy-page-navigation-menu-options.png){width="300" zoomable="yes"}

1. Para especificar la ubicación del menú en relación con el contenido, establezca **[!UICONTROL Menu Layout]**:

   - `Content`: el diseño de menú está en el contenido.
   - `Use Default`: utiliza el estilo de menú especificado en la [configuración](../configuration-reference/general/content-management.md).
   - `Left Column`: el menú aparece a la izquierda del contenido.
   - `Right Column`: el menú aparece a la derecha del contenido.

1. Para especificar cuántos detalles se incluyen en el menú, establezca **[!UICONTROL Menu Detalization]** en uno de los siguientes:

   - `Only Children` - Solo incluye subpáginas en el menú.
   - `Neighbours and Children`: incluye subpáginas y otras páginas que se encuentran en el mismo nivel de la jerarquía.

1. Para determinar la profundidad del menú, escriba **[!UICONTROL Maximal Depth]** para el número máximo de niveles que desea incluir.

1. Para dar formato al menú, elija un **[!UICONTROL List Type]**:

   - `Unordered`: las opciones de menú no están numeradas y se les puede dar formato con o sin viñetas. Opciones para el tipo de lista sin ordenar: Predeterminado/Círculo/Disco/Cuadrado
   - `Ordered`: las opciones de menú están numeradas y se les puede dar formato de números numéricos, alfabéticos o romanos en mayúsculas o minúsculas.

1. Establezca **[!UICONTROL List Style]** en una de las siguientes opciones:

   - `Circle`
   - `Disc`
   - `Square`

1. Si también desea que el nodo esté visible en el menú de navegación, desplácese hasta _Opciones del menú de navegación principal_ y establezca **[!UICONTROL Show in Navigation menu]** en `Yes`.

   ![Opciones del menú de navegación principal](./assets/page-hierarchy-main-navigation-menu-options.png){width="250" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save]**.
