---
title: Notas de la versión para [!DNL Page Builder]
description: Revise las notas de la versión para obtener información acerca de todos los [!DNL Page Builder] versiones.
exl-id: 81abe2f9-ed48-49fe-bbf0-70699d7106b2
feature: Page Builder, Release Notes
source-git-commit: addc34aeb4418aa3a1a9c2fc3adca738352ef94f
workflow-type: tm+mt
source-wordcount: '2747'
ht-degree: 0%

---

# Notas de la versión para [!DNL Page Builder]

Estas notas de la versión describen las versiones de [!DNL Page Builder] e incluir:

![Nuevo](../assets/new.svg) Nuevas funciones

![Problema corregido](../assets/fix.svg) Correcciones y mejoras

![Problema conocido](../assets/bug.svg) Problemas conocidos

>[!IMPORTANT]
>
>A partir de la versión 2.4.3, [!DNL Page Builder] ahora está disponible como una extensión agrupada en Magento Open Source. Ahora es la herramienta de edición de contenido predeterminada tanto para Adobe Commerce como para Magento Open Source y puede reemplazar el editor WYSIWG con cualquier módulo de terceros.

## 1.7.2 para Commerce 2.4.5

![Nuevo](../assets/new.svg) **Nueva entidad envolvente - [!DNL Columns] contenedor introducido para diseños de columna** - Anteriormente, los usuarios solo podían agregar columnas dentro de otro tipo de contenido contenedor/envoltorio, como un [!DNL Tab] o [!DNL Row]. Ahora, la [!DNL Column] tiene su propio envoltorio y se puede añadir directamente en el escenario. Además, la variable [!DNL Columns] el contenedor tiene un elemento de configuración en el que los usuarios pueden especificar la configuración de esta entidad contenedora.<!--- PB-500-->

![Nuevo](../assets/new.svg) **Nuevas opciones de menú para duplicar, ocultar y eliminar grupos de columnas** : con estas nuevas opciones, los usuarios pueden duplicar, ocultar y eliminar [!DNL Columns] grupos, igual que con los tipos de contenido.<!--- PB-507-->

![Nuevo](../assets/new.svg) <!-- Issue 594 -->**Nueva compatibilidad con columnas multilínea agregada al grupo de columnas** : Con esta adición, los usuarios pueden manipular varias líneas de columnas dentro de una [!DNL Columns] para que los diseños de columna sean mucho más flexibles.<!--- PB-108-->

Consulte [Diseño: columna](./column.md) para obtener información sobre el uso del nuevo [!DNL Columns] grupo.

## 1.7.1 para Commerce 2.4.4

![Problema corregido](../assets/fix.svg) Page Builder ahora es compatible con PHP 8.1.<!--- AC-1300-->

![Problema corregido](../assets/fix.svg) Los comerciantes ahora pueden añadir texto alternativo (`alt_text`) a imágenes (imagen, titular, diapositiva) para mejorar la accesibilidad del contenido.<!--- PB-1193-->

![Problema corregido](../assets/fix.svg) Los usuarios administradores con permisos restringidos solo a la edición de contenido ya no ven un error al utilizar Page Builder para agregar un widget de producto a una página de CMS. Page Builder también muestra un recuento preciso de productos en la página de configuración del widget. Anteriormente, Page Builder requería permisos para el módulo Catálogo al recuperar el recuento de productos y mostraba este error: `A technical problem with the server created an error. Try again to continue what you were doing. If the problem persists, try again later`. <!--- MC-42779-->

![Problema corregido](../assets/fix.svg) Los problemas de visualización con el menú de formato de Page Builder ahora se resuelven con la actualización de la biblioteca TinyMCE 5. <!--- AC-446-->

![Problema corregido](../assets/fix.svg) Ahora puede utilizar el ratón para editar una **Texto para mostrar** en la ventana emergente Insertar vínculo. <!--- AC-982-->

![Problema corregido](../assets/fix.svg) Page Builder ahora muestra todas las opciones según lo esperado en el menú de opciones de Tamaño de fuente. Anteriormente, no se mostraban todas las opciones. <!--- AC-1056-->

![Problema corregido](../assets/fix.svg) Se ha actualizado el `phpgt/dom` Dependencia del compositor para `magento/magento2-page-builder` a las versiones más recientes. <!--- magento/magento2-page-builder/pull/779-->

![Problema corregido](../assets/fix.svg) Page Builder ya no cambia el tamaño de los cuadros de diálogo Insertar vínculo e Insertar imagen al mostrar el control deslizante en una columna pequeña. <!--- AC-973-->

![Problema corregido](../assets/fix.svg) El menú Propiedades de tabla de Page Builder ahora se muestra según lo esperado. <!--- AC-407-->

![Problema corregido](../assets/fix.svg) Los puntos de deslizamiento ya no se muestran en el modal Insertar vínculo o imagen cuando el ratón no pasa el ratón por encima del deslizador. <!--- AC-406-->

![Problema corregido](../assets/fix.svg) Se ha optimizado el tamaño de fuente utilizado para mostrar las opciones del menú Tabla. <!--- AC-396-->

![Problema corregido](../assets/fix.svg) Se han corregido anomalías al colocar los cuadros de diálogo Insertar/Editar imagen e Insertar/Editar vínculo. <!--- AC-397-->

![Problema corregido](../assets/fix.svg) Page Builder ya no genera un error cuando hace clic en **Editor de texto** para un titular. <!--- AC-398-->

![Problema corregido](../assets/fix.svg) Page Builder ya no convierte todos los bloques dinámicos en un idioma durante la actualización. <!--- MC-42265-->

## 1.6.0 para Adobe Commerce 2.4.2

![Nuevo](../assets/new.svg) <!-- Issue 558 -->**Nuevo [!DNL Page Builder] estilo** - [!DNL Page Builder] se han realizado mejoras masivas en la forma en que diseña el contenido. Los cambios ahora facilitan la creación de selectores de CSS simples para anular los estilos de tipo de contenido existentes. Estos cambios permiten crear lo siguiente [!DNL Page Builder] temas con una respuesta enriquecida para todos los tipos de contenido.

![Nuevo](../assets/new.svg) <!-- Issue 429 -->**Contenedor de fila ahora opcional** - Ahora puede crear contenido en [!DNL Page Builder] sin requerir un contenedor de fila. Además de Fila, ahora se pueden arrastrar y soltar los siguientes tipos de contenido directamente en el escenario: HTML, Bloque, Bloque dinámico, Columnas y Pestañas.

![Nuevo](../assets/new.svg) <!-- Issue 636 -->**Nuevo conmutador de ventanilla adaptable** - Ahora puede previsualizar su [!DNL Page Builder] contenido en diferentes anchos de dispositivo (puntos de interrupción) utilizando los nuevos botones del conmutador de ventanilla de administración encima del escenario. El conmutador de ventanilla móvil simula el modo en que se diseña el contenido cuando se muestra en la tienda mediante diferentes dispositivos.

![Nuevo](../assets/new.svg) <!-- Issue 637 -->**Nuevos campos de formulario específicos de punto de interrupción** : los valores de campo de tipo de contenido ahora se pueden configurar en puntos de interrupción de ventanilla específicos. Los indicadores de icono junto a los campos muestran la ventanilla móvil a la que se aplica el valor del campo de tipo de contenido.

![Nuevo](../assets/new.svg) <!-- Issue 559 -->**Se eliminaron las entradas de campo de formulario predefinidas** : La configuración avanzada de formularios para márgenes, rellenos y propiedades relacionadas con bordes (borde, ancho de borde y radio de borde) ahora se establece como `default`, de modo que los valores se puedan definir mediante el CSS de un módulo.

![Nuevo](../assets/new.svg) <!-- Issue 635, 557,  -->**Espaciado de escenario agregado** : las filas y columnas ahora proporcionan asignaciones de espacio adicionales alrededor de los tipos de contenido contenidos en el escenario, pero no en la tienda. El espaciado de escenario adicional facilita el acceso a los menús de opciones del ratón tanto para el contenedor como para los tipos de contenido contenidos.

![Problema corregido](../assets/fix.svg) <!-- MC-37348 -->**Se ha corregido el desplazamiento automático a las críticas** - El desplazamiento automático a las críticas de producto en la tienda ya está corregido.

![Problema corregido](../assets/fix.svg) <!-- MC-36227 -->**Contenido recortado fijo** - Las descripciones largas de categorías y productos ya no se recortan.

![Problema corregido](../assets/fix.svg) <!-- MC-35402 -->**Se ha corregido el contenido de categoría de ancho completo y sangrado completo** : el contenido de la categoría ahora se puede mostrar en un diseño de ancho completo o de sangrado completo.

![Problema corregido](../assets/fix.svg) <!-- MC-37989 -->**Mejoras de seguridad**

## 1.5.1 para Adobe Commerce 2.4.1-p1

![Problema corregido](../assets/fix.svg) <!-- PB-1140, MC-38812 -->**Visualización de error** - Se ha corregido un problema en el que [!DNL Page Builder] Se ha mostrado un error al añadir subcategorías de catálogo en el Administrador.

## 1.5.0 para Adobe Commerce 2.4.1

![Nuevo](../assets/new.svg) <!-- Issue 510, 511, 512, 513 -->**Edición envolvente en pantalla completa** - Edición [!DNL Page Builder] ahora, el contenido solo está en pantalla completa en todas las áreas controladas por [!DNL Page Builder]. Este cambio incluye páginas de CMS, páginas de productos y categorías, bloques y bloques dinámicos. La edición a pantalla completa centra la atención en el contenido y proporciona una vista que se adapta mejor a la experiencia del usuario en la tienda.

![Nuevo](../assets/new.svg) <!-- Issue 544 -->**[!DNL Page Builder] previsualizaciones de contenido **- De forma predeterminada, [!DNL Page Builder] ahora proporciona previsualizaciones de contenido no solo para páginas de CMS, bloques y bloques dinámicos, sino también para páginas de productos y categorías. Puede configurar esta función para que esté activada o desactivada en las páginas de Productos y Categorías mediante el nuevo [!DNL Page Builder] Configuración de vista previa de contenido, a la que se accede en la configuración de tienda en Administración de contenido > Herramientas de contenido avanzadas.

![Nuevo](../assets/new.svg) <!-- Issue 543 -->**Acceso mejorado a descripciones cortas de los productos** - De forma predeterminada, ahora se muestra una descripción breve del producto antes de la descripción más larga. Este cambio hace que coincida con el orden en el que aparecen en la tienda, lo que evita la necesidad de desplazarse por el contenido de la descripción más larga para obtener acceso a la descripción breve.

![Nuevo](../assets/new.svg) <!-- Issue 419 -->**Se han impedido los vínculos anidados en titulares y diapositivas** - Al agregar vínculos tanto al contenido como a los elementos externos de los titulares y las diapositivas, se crearon vínculos anidados que no se mostraban o comportaban correctamente en la tienda. Para resolver el problema, ya no se pueden añadir vínculos a *ambos* el área Texto del mensaje y el atributo Vínculo para titulares y diapositivas.

![Problema corregido](../assets/fix.svg) <!-- Issue 421 --> Se ha corregido un problema por el cual al establecer el radio de borde vacío en un elemento de pestaña se producían errores y se rompía el contenido del elemento de pestaña.

![Problema corregido](../assets/fix.svg) <!-- Issue 422 --> Se ha corregido un problema que causaba que, al agregar ciertas combinaciones de condiciones al filtro de condición de productos, se generaran errores que impedían guardar el formulario de productos.

![Problema corregido](../assets/fix.svg) <!-- Issue 425 -->Se ha corregido un problema en el cual el tipo de contenido Regulador no se comportaba correctamente cuando la configuración Bucle infinito estaba deshabilitada.

![Problema corregido](../assets/fix.svg) <!-- Issue 426 -->Se ha corregido el precio mínimo anunciado para que ahora funcione en [!DNL Page Builder].

![Problema corregido](../assets/fix.svg) <!-- Issue 436 -->Se ha corregido un problema en Safari e IE 11 que impedía arrastrar y soltar una imagen en el área de carga en titulares y diapositivas.

![Problema corregido](../assets/fix.svg) <!-- Issue 525 -->Se ha corregido un problema por el cual el tipo de contenido del control deslizante no respondía en Firefox.

![Problema corregido](../assets/fix.svg) <!-- Issue 567 -->Se ha corregido el problema por el cual la configuración del widget creaba selectores incorrectos en el DOM para las diferentes apariencias.

![Problema corregido](../assets/fix.svg) <!-- Issue 609 -->Se ha corregido el problema por el que la barra de herramientas Encabezado ocultaba el menú de opciones del tipo de contenido, lo que impedía el acceso al formulario y a otras opciones.

![Problema corregido](../assets/fix.svg) <!-- Issue 612, 613 -->Se han corregido problemas en los que los reguladores y varias filas que utilizan fondos de paralaje no se representaban correctamente después de alternar el modo de pantalla completa varias veces.

![Problema corregido](../assets/fix.svg) <!--MC-35220-->Se ha corregido un problema que impedía copiar el contenido de un tipo de contenido de Encabezado en un tipo de contenido de texto [!DNL Page Builder] de guardar.

![Problema corregido](../assets/fix.svg) <!-- MC-34620 -->Se ha corregido el tipo de contenido Texto para que gestione y guarde correctamente caracteres que no sean de tipo Latín-1.

![Problema corregido](../assets/fix.svg) <!-- MC-34679 -->Fijo [!DNL Page Builder] Estilos CSS que provocaban que Safari 13.1 representara incorrectamente el menú del sitio del tema de Luma para puertos de vista pequeños y pantallas móviles.

![Problema corregido](../assets/fix.svg) <!-- MC-34848 -->Se ha corregido el tipo de contenido HTML para que muestre correctamente los widgets incrustados como &quot;Ordenar por SKU&quot; en la tienda.

## 1.4.1 para Adobe Commerce 2.4.0-p1

![Nuevo](../assets/new.svg) <!-- PB-590 --> Actualizado a TinyMCE 4. Se ha eliminado TinyMCE 3 para mejorar la seguridad.

## 1.4.0 para Adobe Commerce 2.4.0

![Nuevo](../assets/new.svg) <!-- PB-494 -->Se ha agregado compatibilidad con PHP 7.4.

![Problema corregido](../assets/fix.svg) <!-- MC-31247 -->Se ha corregido un problema en el cual el tipo de contenido Productos no mostraba productos configurables cuando la condición se establecía en precio.

![Problema corregido](../assets/fix.svg) <!-- PB-179 -->Se ha corregido la configuración de alineación Productos para colocar únicamente el contenedor de producto en sí, no el contenido del contenedor de producto, como el nombre del producto, el precio, los botones, las imágenes y otros elementos.

![Problema corregido](../assets/fix.svg) <!-- MC-33556 -->Mejoras de rendimiento.

![Problema corregido](../assets/fix.svg) Mejoras de seguridad.

## 1.3.3-p1 para Adobe Commerce 2.3.6-p1

![Problema corregido](../assets/fix.svg) Mejoras de seguridad.

## 1.3.3 para Adobe Commerce 2.3.6

![Problema corregido](../assets/fix.svg) <!-- MC-32766 -->Se ha corregido el tipo de contenido Texto para guardar correctamente las directivas de variables agregadas a los atributos html.

![Problema corregido](../assets/fix.svg) <!-- MC-34590 -->Se ha corregido el tipo de contenido Texto para que gestione y guarde correctamente caracteres que no sean de tipo Latín-1.

![Problema corregido](../assets/fix.svg) <!-- MC-34677 -->Fijo [!DNL Page Builder] Estilos CSS que provocaban que Safari 13.1 representara incorrectamente el menú del sitio del tema de Luma para puertos de vista pequeños y pantallas móviles.

![Problema corregido](../assets/fix.svg) <!-- MC-34846 -->Se ha corregido el tipo de contenido HTML para que muestre correctamente widgets incrustados como _Ordenar por SKU_ en la tienda.

![Problema corregido](../assets/fix.svg) Se ha corregido un error que, en ocasiones, impedía a los usuarios guardar formularios de tipo de contenido. El error (&quot;[!DNL Page Builder] se procesaba durante 5 segundos sin liberar bloqueos&quot;) provocaba que el icono del cargador girara indefinidamente después de intentar guardar un formulario.

## 1.3.2 para Adobe Commerce 2.3.5-p2

![Nuevo](../assets/new.svg) Mejoras de seguridad.

## 1.3.1 para Adobe Commerce 2.3.5-p1

Esta versión de [!DNL Page Builder] es solo una actualización de número de versión para Adobe Commerce 2.3.5-p1. Todas las funciones descritas para la versión 1.3.0 se aplican a esta versión también.

## 1.3.0 para Adobe Commerce 2.3.5

![Nuevo](../assets/new.svg) **Plantillas** - [!DNL Page Builder] ahora tiene plantillas que se pueden crear a partir del contenido existente y aplicar a nuevas áreas de contenido. [!DNL Page Builder] las plantillas guardan el contenido y los diseños de páginas, bloques, bloques dinámicos, atributos de productos y descripciones de categorías existentes. Por ejemplo, puede guardar un archivo existente [!DNL Page Builder] Página de CMS como plantilla y, a continuación, aplique esa plantilla (con todo su contenido y diseños) para crear rápidamente páginas de CMS para su sitio. Esta nueva función está documentada aquí: [Plantillas](templates.md).

![Nuevo](../assets/new.svg) **Fondos de vídeo para filas, titulares y deslizadores** - [!DNL Page Builder] Ahora, las filas, los titulares y los deslizadores pueden utilizar vídeos para sus fondos. Estas nuevas funciones se documentan aquí: [Filas](row.md), [Titulares](banner.md), [Reguladores](slider.md).

![Nuevo](../assets/new.svg) **Adiciones y mejoras de compatibilidad con vídeo** - [!DNL Page Builder] ahora admite una mayor variedad de formatos de vídeo. Además de los vídeos de YouTube y Vimeo, el tipo de contenido de vídeo y los fondos de vídeo ahora admiten vínculos de URL de vídeo a formatos de vídeo como `.mp4` y otros formatos compatibles con el explorador. El tipo de contenido de vídeo también agrega una función de reproducción automática. Estas nuevas funciones se documentan aquí: [Tipo de contenido de vídeo](video.md).

![Nuevo](../assets/new.svg) **Filas, titulares y deslizadores de altura completa** - [!DNL Page Builder] Ahora, las filas, los titulares y los deslizadores pueden establecer su altura a la altura completa de la página mediante un número con cualquier unidad CSS (px, %, vh, em) o un cálculo entre unidades (100 vh - 237 px). Estas nuevas funciones se documentan aquí: [Filas](row.md), [Titulares](banner.md), [Reguladores](slider.md).

![Nuevo](../assets/new.svg) **Biblioteca de actualización de tipo de contenido** : Los desarrolladores ahora pueden crear versiones de [!DNL Page Builder] tipos de contenido sin introducir problemas incompatibles con versiones anteriores. Antes de esta versión, los cambios significativos en las configuraciones de tipo de contenido crearían problemas de visualización y pérdida de datos con versiones guardadas anteriormente [!DNL Page Builder] tipos de contenido. La nueva biblioteca de actualización elimina estos problemas. La biblioteca está diseñada para actualizar versiones anteriores de tipos de contenido guardados en la base de datos, de modo que coincidan con los cambios de configuración de las nuevas versiones. [!DNL Page Builder] ejecuta la biblioteca de actualización en tipos de contenido nativos según sea necesario para una nueva versión. Este cambio garantiza que la variable [!DNL Page Builder] los tipos de contenido siempre se actualizan para que coincidan con los cambios realizados en los tipos de contenido en una versión más reciente.

>[!IMPORTANT]
>
>Si ha creado entidades de base de datos adicionales para almacenar [!DNL Page Builder] contenido, usted _debe_ añada esas entidades a su `etc/di.xml`. Si no lo hace, la variable [!DNL Page Builder] el contenido almacenado en su entidad no se actualiza, lo que provoca posibles pérdidas de datos y problemas de visualización. Por ejemplo, si ha creado una entidad de blog que almacena [!DNL Page Builder] contenido, debe añadir la entidad de blog a su `etc/di.xml` archivo como un `UpgradableEntitiesPool` escriba para que la biblioteca de actualización pueda actualizar el [!DNL Page Builder] tipos de contenido utilizados en su blog. Para obtener más información e instrucciones sobre el uso de la biblioteca de actualización, consulte [Actualizar tipos de contenido](https://developer.adobe.com/commerce/frontend-core/page-builder/upgrade-content-types/) en el _Guía para desarrolladores de Page Builder_.

![Nuevo](../assets/new.svg) **Documentación para añadir nuevas apariencias** : Información para desarrolladores publicada ahora acerca de [adición de apariencias](https://developer.adobe.com/commerce/frontend-core/page-builder/content-types/extend/add-appearances/) para tipos de contenido existentes o personalizados.

![Problema corregido](../assets/fix.svg) **Varias correcciones**

- <!-- PB-50 -->Se ha corregido un problema por el cual el menú TinyMCE del contenido de la diapositiva aparecía debajo de otros tipos de contenido si el contenedor principal de la diapositiva estaba duplicado.
- <!-- PB-166 -->Actualizado [!DNL Page Builder] para implementar un método de destrucción para evitar pérdidas de memoria en algunos casos.
- <!-- PB-170 -->Se ha mejorado el rendimiento de TinyMCE cuando se utilizan varias instancias en la fase de administración.
- <!-- PB-252 -->Se ha corregido un problema en el cual el tipo de contenido del bloque dinámico no se procesa en la fase de administración si la fila superior está marcada como oculta.
- <!-- PB-273 -->Se han refinado los eventos al pasar el ratón por encima del escenario del administrador al eliminar un retraso de 200 ms de varios controles de interfaz de usuario. Este cambio facilita el trabajo con elementos de contenido anidados en el escenario.
- <!-- PB-294 -->Se ha corregido un problema en el cual el símbolo de moneda se escapaba incorrectamente en el widget de lista de productos dentro del bloque/bloque dinámico en el escenario de Administración.
- <!-- PB-296 -->Se ha corregido un problema en el cual el total del producto de la variable [!DNL Page Builder] El panel de edición no funcionaba para productos MSI estándar personalizados.
- <!-- PB-317 -->Se ha corregido un problema en el cual [!DNL Page Builder] el contenido con imágenes de fondo en Microsoft Edge no procesa esas imágenes en la tienda.
- <!-- PB-390 -->Se ha corregido un problema en el que anidaba [!DNL Page Builder] El contenido no se guarda si los usuarios hacen clic en el botón Guardar antes de que la página se procese completamente.
- <!-- PB-418 -->Se ha corregido un error de excepción producido en trabajos cron debido a [!DNL Page Builder] análisis.

## 1.2.2 para Adobe Commerce 2.3.4-p2

![Nuevo](../assets/new.svg) Mejoras de seguridad.

## 1.2.1 para Adobe Commerce 2.3.4-p1

![Nuevo](../assets/new.svg) Mejoras de seguridad.

## 1.2.0 para Adobe Commerce 2.3.4

![Nuevo](../assets/new.svg)  **[!DNL Page Builder]integración con PWA Studio** - Añadido [!DNL Page Builder] representación de contenido en la aplicación Venia en PWA Studio. [!DNL Page Builder] Ahora, el contenido se puede ver dentro de la aplicación Venia de PWA Studio. Consulte la [!DNL Page Builder] documentación dentro de [PWA Studio] para obtener toda la información acerca de esta nueva función.

![Nuevo](../assets/new.svg) **Carrusel de productos agregado** - <!-- PB-77, PB-173, PB-175 -->El tipo de contenido Productos ahora proporciona una opción para mostrar los productos en formato de carrusel/control deslizante, incluidas varias opciones para personalizar el carrusel según sus necesidades.

![Nuevo](../assets/new.svg) **Clasificación de SKU del producto añadida** - <!-- PB-69 -->El tipo de contenido Productos ahora proporciona una opción para ordenar los productos por SKU en el orden en que se agregan a una lista dentro del Administrador.

![Nuevo](../assets/new.svg) **Clasificación de categoría de producto añadida** - <!-- PB-181 -->. El tipo de contenido Productos ahora proporciona una opción para ordenar los productos por categoría _position_, mostrándolos en el mismo orden en que aparecen en su catálogo comercial.

![Nuevo](../assets/new.svg) **Totales de selección de productos añadidos** - <!-- PB-107 -->. El editor de administración de tipo de contenido Productos ahora muestra el número total de productos que coinciden con las opciones de selección de productos.

![Problema corregido](../assets/fix.svg) **Varias correcciones**

- <!-- PB-237 -->Mejoras de seguridad.
- <!-- PB-41 -->AJAX Se han corregido las búsquedas dentro de los componentes seleccionados de la IU para realizar solo una solicitud de por término de búsqueda.
- <!-- PB-76, PB-84-->Se han actualizado las vistas previas de productos en el Administrador para que coincidan con la tienda, incluidas las opciones de clasificación por estrellas, color y tamaño del producto cuando corresponda.
- <!-- PB-169 -->Se ha corregido un problema en el cual [!DNL Page Builder] no se pudo guardar cuando la minificación y el agrupamiento de JavaScript están habilitados en Commerce.
- <!-- PB-241 -->Se han corregido las previsualizaciones de administración de productos, bloques y bloques dinámicos para que se representen correctamente en las instalaciones de Commerce que definen distintas URL para el administrador y el front-end.
- <!-- PB-238 -->Se han corregido las previsualizaciones de administración de productos, bloques y bloques dinámicos para que se representen correctamente en las instalaciones de Commerce con B2B instalado con _Solo inicio de sesión_ opción activada. Antes de esta corrección, la variable [!DNL Page Builder] La vista previa de haría que la página se redirigiera al inicio de sesión de la cuenta del cliente.
- <!-- PB-239 -->Se ha corregido un error de sesión que se podía producir al obtener una vista previa de una página grande en la [!DNL Page Builder] Administrador.
- <!-- PB-248 -->Actualizado [!DNL Page Builder] MENOS estilos para evitar la duplicación de estilos de tienda.

## 1.1.1 para Adobe Commerce 2.3.3-p1

![Nuevo](../assets/new.svg) Mejoras de seguridad.

## 1.1.0 para Adobe Commerce 2.3.3

![Nuevo](../assets/new.svg) <!-- MC-15250 -->Se ha añadido la ordenación explícita de productos al tipo de contenido Productos.

![Nuevo](../assets/new.svg) <!-- MC-17823 -->Se han añadido botones para insertar imágenes, widgets y variables en el tipo de contenido HTML.

![Problema corregido](../assets/fix.svg) Mejorado [!DNL Page Builder] seguridad.

![Problema corregido](../assets/fix.svg) <!-- MC-1805 -->Actualizado [!DNL Page Builder] para admitir PHP versión 7.3.

![Problema corregido](../assets/fix.svg) <!-- MC-4137 -->Se ha actualizado TinyMCE a la versión 4.9.5. Esta actualización, junto con las mejoras adicionales, solucionó varios problemas con el editor en línea TinyMCE:

- Las variables, las imágenes y los vínculos de imagen se agregan donde se coloca el cursor.
- Las tablas y las celdas de la tabla se pueden alinear al centro.
- Copiar/pegar ahora pega el contenido en la posición del cursor.
- Los vínculos se pueden aplicar al texto seleccionado.
- Las viñetas están correctamente alineadas.
- Los cambios dentro del editor en línea se pueden guardar sin hacer clic primero fuera del editor.

![Problema corregido](../assets/fix.svg) <!-- MC-3880 -->Se ha corregido un problema en el cual la altura mínima y la alineación vertical eran incoherentes entre las secciones del panel de edición para cada tipo de contenido.

![Problema corregido](../assets/fix.svg) <!-- MC-14994 -->Se ha corregido un problema en el cual la barra de herramientas del tipo de contenido Encabezado se colocaba incorrectamente la primera vez que se colocaba en el escenario.

![Problema corregido](../assets/fix.svg) <!-- MC-15742 -->Se corrigieron los márgenes codificados en los tipos de contenido de deslizador y vídeo.

![Problema corregido](../assets/fix.svg) <!-- MC-16241 -->Se ha corregido un problema por el cual el símbolo de asterisco requerido se mostraba dos veces en los campos del formulario.

## 1.0.3 para Adobe Commerce 2.3.2-p2

![Nuevo](../assets/new.svg) Mejoras de seguridad.

## 1.0.2 para Adobe Commerce 2.3.2-p1

![Nuevo](../assets/new.svg) Mejoras de seguridad.

## 1.0.1 para Adobe Commerce 2.3.2

![Nuevo](../assets/new.svg) Garantiza la compatibilidad con Adobe Commerce 2.3.2.

## 1.0.0 para Adobe Commerce 2.3.1

![Nuevo](../assets/new.svg) Versión de disponibilidad general


[PWA Studio]: https://developer.adobe.com/commerce/pwa-studio/
