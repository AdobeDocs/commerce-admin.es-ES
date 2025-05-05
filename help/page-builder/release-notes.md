---
title: Notas de la versión para  [!DNL Page Builder]
description: Revise las notas de la versión para obtener información acerca de todas las  [!DNL Page Builder] versiones.
exl-id: 81abe2f9-ed48-49fe-bbf0-70699d7106b2
feature: Page Builder, Release Notes
source-git-commit: addc34aeb4418aa3a1a9c2fc3adca738352ef94f
workflow-type: tm+mt
source-wordcount: '2813'
ht-degree: 0%

---

# Notas de la versión de [!DNL Page Builder]

Estas notas de la versión describen las versiones de [!DNL Page Builder] e incluyen:

![Nuevas](../assets/new.svg) nuevas características

![Se corrigió el problema](../assets/fix.svg) Correcciones y mejoras

![Problema conocido](../assets/bug.svg) Problemas conocidos

>[!IMPORTANT]
>
>A partir de la versión 2.4.3, [!DNL Page Builder] ya está disponible como una extensión agrupada en Magento Open Source. Ahora es la herramienta de edición de contenido predeterminada tanto para Adobe Commerce como para Magento Open Source y puede reemplazar el editor WYSIWG con cualquier módulo de terceros.

## 1.7.2 para Commerce 2.4.5

![Nuevo](../assets/new.svg) **Nueva entidad envolvente - [!DNL Columns] contenedor introducido para diseños de columna** - Anteriormente, los usuarios solo podían agregar columnas dentro de otro tipo de contenido contenedor/envoltorio, como un [!DNL Tab] o [!DNL Row]. Ahora, [!DNL Column] tiene su propio envoltorio y se puede agregar directamente al escenario. Además, el contenedor [!DNL Columns] tiene un elemento de configuración donde los usuarios pueden especificar la configuración de esta entidad contenedora.<!--- PB-500-->

![Nuevas](../assets/new.svg) **Nuevas opciones de menú para duplicar, ocultar y eliminar grupos de columnas**: con estas nuevas opciones, los usuarios pueden duplicar, ocultar y eliminar [!DNL Columns] grupos, tal como lo hacen con los tipos de contenido.<!--- PB-507-->

![Nuevo](../assets/new.svg) <!-- Issue 594 -->**Se ha agregado compatibilidad con columnas multilínea al grupo de columnas**. Con esta adición, los usuarios pueden manipular varias líneas de columnas dentro de un grupo de [!DNL Columns] para que los diseños de columna sean mucho más flexibles.<!--- PB-108-->

Vea [Diseño - Columna](./column.md) para obtener información acerca del uso del nuevo grupo [!DNL Columns].

## 1.7.1 para Commerce 2.4.4

![Se ha corregido un problema](../assets/fix.svg) Page Builder ahora es compatible con PHP 8.1.<!--- AC-1300-->

![Se ha corregido un problema](../assets/fix.svg) Los comerciantes ahora pueden agregar texto alternativo (`alt_text`) a las imágenes (imagen, titular, diapositiva) para mejorar la accesibilidad del contenido.<!--- PB-1193-->

![Se ha corregido un problema](../assets/fix.svg) Los usuarios administradores con permisos restringidos solo a la edición de contenido ya no ven un error al usar Page Builder para agregar un widget de producto a una página de CMS. Page Builder también muestra un recuento preciso de productos en la página de configuración del widget. Anteriormente, Page Builder requería permisos para el módulo Catálogo al recuperar el recuento de productos y mostraba este error: `A technical problem with the server created an error. Try again to continue what you were doing. If the problem persists, try again later`. <!--- MC-42779-->

![Se ha corregido un problema](../assets/fix.svg) Los problemas de visualización con el menú de formato de Page Builder ahora se resuelven con la actualización de la biblioteca TinyMCE 5. <!--- AC-446-->

![Problema corregido](../assets/fix.svg) Ahora puede usar el mouse (ratón) para editar un valor de **Texto para mostrar** en la ventana emergente Insertar vínculo. <!--- AC-982-->

![Problema corregido](../assets/fix.svg) Page Builder ahora muestra todas las opciones según lo esperado en el menú de opciones de Tamaño de fuente. Anteriormente, no se mostraban todas las opciones. <!--- AC-1056-->

![Se ha corregido un problema](../assets/fix.svg) que actualizaba la dependencia del Compositor `phpgt/dom` para la extensión `magento/magento2-page-builder` a las últimas versiones. <!--- magento/magento2-page-builder/pull/779-->

![Problema corregido](../assets/fix.svg) Page Builder ya no cambia el tamaño de los cuadros de diálogo Insertar vínculo e Insertar imagen al mostrar el control deslizante en una columna pequeña. <!--- AC-973-->

![Se ha corregido un problema](../assets/fix.svg). El menú Propiedades de la tabla de Page Builder ahora se muestra según lo esperado. <!--- AC-407-->

![Se ha corregido un problema](../assets/fix.svg): ya no se muestran los puntos del control deslizante en el modal Insertar vínculo o imagen cuando el ratón no pasa el ratón por encima del control deslizante. <!--- AC-406-->

![Se ha corregido un problema](../assets/fix.svg) Se ha optimizado el tamaño de fuente utilizado para mostrar las opciones del menú Tabla. <!--- AC-396-->

![Se ha corregido un problema](../assets/fix.svg) que corregía anomalías al colocar los cuadros de diálogo Insertar/Editar imagen e Insertar/Editar vínculo. <!--- AC-397-->

![Se ha corregido un problema](../assets/fix.svg) Page Builder ya no genera un error cuando hace clic en **Editor de texto** para un titular. <!--- AC-398-->

![Se ha corregido un problema](../assets/fix.svg) Page Builder ya no convierte todos los bloques dinámicos a un idioma durante la actualización. <!--- MC-42265-->

## 1.6.0 para Adobe Commerce 2.4.2

![Nuevo](../assets/new.svg) <!-- Issue 558 -->**Nuevo estilo [!DNL Page Builder]** - [!DNL Page Builder] realizó mejoras sustanciales en la forma en que aplica estilo al contenido. Los cambios ahora facilitan la creación de selectores de CSS simples para anular los estilos de tipo de contenido existentes. Estos cambios permiten crear [!DNL Page Builder] temas con respuesta enriquecida para todos los tipos de contenido.

![Nuevo](../assets/new.svg) <!-- Issue 429 -->**contenedor de fila ahora opcional**: ahora puede crear contenido en [!DNL Page Builder] sin requerir un contenedor de fila. Además de Fila, ahora se pueden arrastrar y soltar los siguientes tipos de contenido directamente en el escenario: HTML, Bloque, Bloque dinámico, Columnas y Pestañas.

![Nuevo](../assets/new.svg) <!-- Issue 636 -->**Nuevo conmutador de ventanilla adaptable**: ahora puede obtener una vista previa del contenido de [!DNL Page Builder] en diferentes anchos de dispositivo (puntos de interrupción) mediante los nuevos botones del conmutador de ventanilla de administración situados encima del escenario. El conmutador de ventanilla móvil simula el modo en que se diseña el contenido cuando se muestra en la tienda mediante diferentes dispositivos.

![Nuevos](../assets/new.svg) <!-- Issue 637 -->**nuevos campos de formulario específicos de punto de interrupción**: los valores de los campos de tipo de contenido ahora se pueden establecer en puntos de interrupción específicos de la ventanilla móvil. Los indicadores de icono junto a los campos muestran la ventanilla móvil a la que se aplica el valor del campo de tipo de contenido.

![Nuevo](../assets/new.svg) <!-- Issue 559 -->**Se eliminaron las entradas predefinidas de los campos de formulario**. La configuración avanzada de los márgenes, los rellenos y las propiedades relacionadas con los bordes (borde, ancho de borde y radio de borde) ahora se establece como `default`, de modo que los valores se pueden definir mediante CSS de un módulo.

![Nuevo](../assets/new.svg) <!-- Issue 635, 557,  -->**Espaciado de escenario agregado**: ahora las filas y columnas proporcionan espacios adicionales para los tipos de contenido contenidos en el escenario, pero no en la tienda. El espaciado de escenario adicional facilita el acceso a los menús de opciones del ratón tanto para el contenedor como para los tipos de contenido contenidos.

![Se ha corregido un problema](../assets/fix.svg) <!-- MC-37348 -->**Se ha corregido el desplazamiento automático a las críticas**. El desplazamiento automático a las críticas de producto en la tienda ya está solucionado.

![Se ha corregido un problema](../assets/fix.svg) <!-- MC-36227 -->**Se ha corregido el contenido recortado**. Ya no se recortan las descripciones largas de categorías y productos.

![Se ha corregido un problema](../assets/fix.svg) <!-- MC-35402 -->**Se ha corregido el contenido de categoría a sangrado completo y de ancho completo**. Ahora, el contenido de categoría se puede mostrar en un diseño de ancho completo o de sangrado completo.

![Problema corregido](../assets/fix.svg) <!-- MC-37989 -->**Mejoras de seguridad**

## 1.5.1 para Adobe Commerce 2.4.1-p1

![Se ha corregido un problema](../assets/fix.svg) <!-- PB-1140, MC-38812 -->**Visualización de error** - Se ha corregido un problema en el cual [!DNL Page Builder] mostraba un error al agregar subcategorías de catálogo en el administrador.

## 1.5.0 para Adobe Commerce 2.4.1

![Nuevo](../assets/new.svg) <!-- Issue 510, 511, 512, 513 -->**Edición inmersiva a pantalla completa** - Editar contenido de [!DNL Page Builder] ahora solo es a pantalla completa para todas las áreas controladas por [!DNL Page Builder]. Este cambio incluye páginas de CMS, páginas de productos y categorías, bloques y bloques dinámicos. La edición a pantalla completa centra la atención en el contenido y proporciona una vista que se adapta mejor a la experiencia del usuario en la tienda.

![Nuevas](../assets/new.svg) <!-- Issue 544 -->**[!DNL Page Builder] vistas previas de contenido &#x200B;**- De forma predeterminada, [!DNL Page Builder] ahora proporciona vistas previas de contenido no solo para páginas CMS, Bloques y Bloques dinámicos, sino también para páginas de Productos y Categorías. Puede configurar esta característica para que esté activada o desactivada en las páginas de Productos y Categorías mediante la nueva configuración de Vista previa de contenido de [!DNL Page Builder], a la que se tiene acceso en la configuración de tienda en Administración de contenido > Herramientas de contenido avanzadas.

![Nuevo](../assets/new.svg) <!-- Issue 543 -->**Se ha mejorado el acceso a las descripciones cortas del producto**. De forma predeterminada, ahora se muestra una descripción breve del producto antes de la descripción más larga. Este cambio hace que coincida con el orden en el que aparecen en la tienda, lo que evita la necesidad de desplazarse por el contenido de la descripción más larga para obtener acceso a la descripción breve.

![Nuevo](../assets/new.svg) <!-- Issue 419 -->**Impidió vínculos anidados en titulares y diapositivas**: al agregar vínculos al contenido y a los elementos externos de titulares y diapositivas, se crearon vínculos anidados que no se mostraban o no se comportaban correctamente en la tienda. Para resolver el problema, ya no se pueden agregar vínculos a *tanto* el área Texto del mensaje como el atributo Vínculo para titulares y diapositivas.

![Se ha corregido un problema](../assets/fix.svg) <!-- Issue 421 --> Se ha corregido un problema por el cual al establecer el radio de borde vacío en un elemento de ficha se producían errores y se rompía el contenido del elemento de ficha.

![Se ha corregido un problema](../assets/fix.svg) <!-- Issue 422 -->. Se ha corregido un problema que causaba que, al agregar ciertas combinaciones de condiciones al filtro de condición de productos, se generaran errores que no permitían guardar el formulario de productos.

![Se corrigió un problema](../assets/fix.svg) <!-- Issue 425 -->Se corrigió un problema en el cual el tipo de contenido del control deslizante no se comportaba correctamente cuando se deshabilitaba la configuración de Bucle infinito.

![Problema corregido](../assets/fix.svg) <!-- Issue 426 -->Se ha corregido el precio mínimo anunciado para que ahora funcione en [!DNL Page Builder].

![Se ha corregido un problema](../assets/fix.svg) <!-- Issue 436 -->Se ha corregido un problema en Safari e IE 11 que impedía arrastrar y soltar una imagen en el área de carga en titulares y diapositivas.

![Se ha corregido un problema](../assets/fix.svg) <!-- Issue 525 -->Se ha corregido un problema por el cual el tipo de contenido del control deslizante no respondía en Firefox.

![Se ha corregido un problema](../assets/fix.svg) <!-- Issue 567 -->Se ha corregido el problema por el cual la configuración del widget creaba selectores incorrectos en el DOM para las diferentes apariencias.

![Se ha corregido un problema](../assets/fix.svg) <!-- Issue 609 -->Se ha corregido el problema por el que la barra de herramientas Encabezado ocultaba el menú de opciones del tipo de contenido, lo que impedía el acceso al formulario y a otras opciones.

![Se ha corregido un problema](../assets/fix.svg) <!-- Issue 612, 613 -->Se han corregido problemas por los que los controles deslizantes y las filas múltiples que usan fondos de paralaje no se representaban correctamente después de alternar el modo de pantalla completa varias veces.

![Se ha corregido un problema](../assets/fix.svg) <!--MC-35220-->Se ha corregido un problema que impedía que [!DNL Page Builder] guardara al intentar copiar el contenido de un tipo de contenido de Encabezado en un tipo de contenido de Texto.

![Se ha corregido un problema](../assets/fix.svg) <!-- MC-34620 -->Se ha corregido el tipo de contenido Texto para que gestione y guarde correctamente caracteres que no sean Latin-1.

![Se ha corregido un problema](../assets/fix.svg) <!-- MC-34679 -->Se han corregido [!DNL Page Builder] estilos CSS que provocaban que Safari 13.1 representara incorrectamente el menú de sitio del tema de Luma para los puertos de vista pequeños y las pantallas móviles.

![Se ha corregido un problema](../assets/fix.svg) <!-- MC-34848 -->Se ha corregido el tipo de contenido del HTML para que muestre correctamente los widgets incrustados como &quot;Ordenar por SKU&quot; en la tienda.

## 1.4.1 para Adobe Commerce 2.4.0-p1

![Nuevo](../assets/new.svg) <!-- PB-590 --> actualizado a TinyMCE 4. Se ha eliminado TinyMCE 3 para mejorar la seguridad.

## 1.4.0 para Adobe Commerce 2.4.0

![Nuevo](../assets/new.svg) <!-- PB-494 -->Se agregó compatibilidad con PHP 7.4.

![Se ha corregido un problema](../assets/fix.svg) <!-- MC-31247 -->Se ha corregido un problema por el que el tipo de contenido Productos no mostraba productos configurables cuando la condición se establecía en precio.

![Se ha corregido un problema](../assets/fix.svg) <!-- PB-179 -->Se ha corregido la configuración de alineación de productos para colocar únicamente el contenedor de productos, no el contenido del contenedor de productos, como el nombre del producto, el precio, los botones, las imágenes y otros elementos.

![Se corrigió el problema](../assets/fix.svg) <!-- MC-33556 -->Mejoras de rendimiento.

![Se corrigió un problema](../assets/fix.svg) en las mejoras de seguridad.

## 1.3.3-p1 para Adobe Commerce 2.3.6-p1

![Se corrigió un problema](../assets/fix.svg) en las mejoras de seguridad.

## 1.3.3 para Adobe Commerce 2.3.6

![Se ha corregido un problema](../assets/fix.svg) <!-- MC-32766 -->Se ha corregido el tipo de contenido Texto para guardar correctamente las directivas de variables agregadas a los atributos html.

![Se ha corregido un problema](../assets/fix.svg) <!-- MC-34590 -->Se ha corregido el tipo de contenido Texto para que gestione y guarde correctamente caracteres que no sean Latin-1.

![Se ha corregido un problema](../assets/fix.svg) <!-- MC-34677 -->Se han corregido [!DNL Page Builder] estilos CSS que provocaban que Safari 13.1 representara incorrectamente el menú de sitio del tema de Luma para los puertos de vista pequeños y las pantallas móviles.

![Se ha corregido un problema](../assets/fix.svg) <!-- MC-34846 -->Se ha corregido el tipo de contenido HTML para que muestre correctamente widgets incrustados como _Ordenar por SKU_ en la tienda.

![Se ha corregido un problema](../assets/fix.svg). Se ha corregido un error que a veces impedía a los usuarios guardar formularios de tipo de contenido. El error (&quot;[!DNL Page Builder] se estaba representando durante 5 segundos sin liberar bloqueos&quot;) provocó que el icono del cargador girara indefinidamente después de intentar guardar un formulario.

## 1.3.2 para Adobe Commerce 2.3.5-p2

![Nuevas](../assets/new.svg) mejoras de seguridad.

## 1.3.1 para Adobe Commerce 2.3.5-p1

Esta versión de [!DNL Page Builder] es solo una actualización de número de versión para Adobe Commerce 2.3.5-p1. Todas las funciones descritas para la versión 1.3.0 se aplican a esta versión también.

## 1.3.0 para Adobe Commerce 2.3.5

![Nuevas](../assets/new.svg) **plantillas** - [!DNL Page Builder] ahora tienen plantillas que se pueden crear a partir del contenido existente y aplicar a nuevas áreas de contenido. Las plantillas de [!DNL Page Builder] guardan el contenido y los diseños de páginas, bloques, bloques dinámicos, atributos de productos y descripciones de categorías existentes. Por ejemplo, puede guardar una página CMS [!DNL Page Builder] existente como plantilla y luego aplicar esa plantilla (con todo su contenido y diseños) para crear rápidamente páginas CMS para su sitio. Esta nueva característica está documentada aquí: [Plantillas](templates.md).

![Nuevos](../assets/new.svg) **Fondos de vídeo para filas, titulares y controles deslizantes** - [!DNL Page Builder] filas, titulares y controles deslizantes ahora pueden usar vídeos para sus fondos. Estas nuevas características están documentadas aquí: [Filas](row.md), [Banners](banner.md), [Correderas](slider.md).

![Nuevo](../assets/new.svg) **El vídeo admite adiciones y mejoras** - [!DNL Page Builder] ahora admite una variedad más amplia de formatos de vídeo. Además de los vídeos de YouTube y Vimeo, el tipo de contenido de vídeo y los fondos de vídeo ahora admiten vínculos de URL de vídeo a formatos de vídeo como `.mp4` y otros formatos compatibles con el explorador. El tipo de contenido de vídeo también agrega una función de reproducción automática. Estas nuevas características están documentadas aquí: [Tipo de contenido de vídeo](video.md).

![Nuevas](../assets/new.svg) **filas, titulares y controles deslizantes de altura completa** - [!DNL Page Builder] filas, titulares y controles deslizantes ahora pueden establecer su altura a la altura completa de la página usando un número con cualquier unidad CSS (px, %, vh, em) o un cálculo entre unidades (100vh - 237px). Estas nuevas características están documentadas aquí: [Filas](row.md), [Banners](banner.md), [Correderas](slider.md).

![Nueva](../assets/new.svg) **biblioteca de actualización de tipo de contenido**: los desarrolladores ahora pueden crear versiones de [!DNL Page Builder] tipos de contenido sin introducir problemas incompatibles con versiones anteriores. Antes de esta versión, los cambios significativos en las configuraciones de tipo de contenido crearían problemas de visualización y pérdida de datos con [!DNL Page Builder] tipos de contenido guardados anteriormente. La nueva biblioteca de actualización elimina estos problemas. La biblioteca está diseñada para actualizar versiones anteriores de tipos de contenido guardados en la base de datos, de modo que coincidan con los cambios de configuración de las nuevas versiones. [!DNL Page Builder] ejecuta la biblioteca de actualización en tipos de contenido nativo según sea necesario para una nueva versión. Este cambio garantiza que los tipos de contenido integrados de [!DNL Page Builder] siempre se actualicen para que coincidan con los cambios realizados en los tipos de contenido en una versión más reciente.

>[!IMPORTANT]
>
>Si ha creado entidades de base de datos adicionales para almacenar contenido de [!DNL Page Builder], _debe_ agregar esas entidades a su `etc/di.xml`. Si no lo hace, el contenido de [!DNL Page Builder] almacenado en su entidad no se actualiza, lo que provoca posibles problemas de pérdida de datos y visualización. Por ejemplo, si ha creado una entidad de blog que almacena contenido de [!DNL Page Builder], debe agregar la entidad de blog al archivo `etc/di.xml` como un tipo de `UpgradableEntitiesPool` para que la biblioteca de actualización pueda actualizar los tipos de contenido de [!DNL Page Builder] utilizados en su blog. Para obtener más información e instrucciones sobre cómo usar la biblioteca de actualización, consulte [Actualizar tipos de contenido](https://developer.adobe.com/commerce/frontend-core/page-builder/upgrade-content-types/) en la _Guía para desarrolladores de Page Builder_.

![Nueva](../assets/new.svg) **Documentación para agregar nuevas apariencias** - Información para desarrolladores publicada ahora acerca de [agregar apariencias](https://developer.adobe.com/commerce/frontend-core/page-builder/content-types/extend/add-appearances/) para tipos de contenido existentes o personalizados.

![Problema corregido](../assets/fix.svg) **Varias correcciones**

- &#x200B;<!-- PB-50 -->Se ha corregido un problema por el cual el menú TinyMCE del contenido de la diapositiva aparecía debajo de otros tipos de contenido si el contenedor principal de la diapositiva estaba duplicado.
- &#x200B;<!-- PB-166 -->Se ha actualizado [!DNL Page Builder] para implementar un método de destrucción con el fin de evitar pérdidas de memoria en algunos casos.
- &#x200B;<!-- PB-170 -->Se ha mejorado el rendimiento de TinyMCE cuando se utilizan varias instancias en la fase de administración.
- &#x200B;<!-- PB-252 -->Se ha corregido un problema en el cual el tipo de contenido del bloque dinámico no se procesa en la fase de administración si la fila superior está marcada como oculta.
- &#x200B;<!-- PB-273 -->Se han refinado los eventos al pasar el ratón por encima del escenario del administrador al eliminar un retraso de 200 ms de varios controles de interfaz de usuario. Este cambio facilita el trabajo con elementos de contenido anidados en el escenario.
- &#x200B;<!-- PB-294 -->Se ha corregido un problema en el cual el símbolo de moneda se escapaba incorrectamente en el widget de lista de productos dentro del bloque/bloque dinámico en el escenario de Administración.
- &#x200B;<!-- PB-296 -->Se corrigió un problema en el cual el total del producto en el panel de edición de [!DNL Page Builder] no funcionaba para los productos de MSI Stock personalizados.
- &#x200B;<!-- PB-317 -->Se corrigió un problema en el cual guardar contenido de [!DNL Page Builder] con imágenes de fondo en Microsoft Edge no procesa esas imágenes en la tienda.
- &#x200B;<!-- PB-390 -->Se ha corregido un problema en el cual el contenido de [!DNL Page Builder] anidado no se podía guardar si los usuarios hacían clic en el botón Guardar antes de que la página se procesara por completo.
- &#x200B;<!-- PB-418 -->Se corrigió un error de excepción producido en trabajos cron debido a análisis de [!DNL Page Builder].

## 1.2.2 para Adobe Commerce 2.3.4-p2

![Nuevas](../assets/new.svg) mejoras de seguridad.

## 1.2.1 para Adobe Commerce 2.3.4-p1

![Nuevas](../assets/new.svg) mejoras de seguridad.

## 1.2.0 para Adobe Commerce 2.3.4

Integración de ![New](../assets/new.svg) **[!DNL Page Builder]con PWA Studio** - Se agregó la representación de contenido de [!DNL Page Builder] a la aplicación Venia en PWA Studio. Ahora, el contenido [!DNL Page Builder] se puede ver dentro de la aplicación Venia de PWA Studio. Consulte la documentación de [!DNL Page Builder] en [PWA Studio] para obtener toda la información sobre esta nueva característica.

![Nuevo](../assets/new.svg) **Carrusel de productos agregado** - <!-- PB-77, PB-173, PB-175 -->El tipo de contenido de productos ahora proporciona una opción para mostrar sus productos en formato de carrusel/control deslizante, que incluye varias opciones para personalizar el carrusel según sus necesidades.

![Nuevo](../assets/new.svg) **Clasificación agregada de SKU del producto** - <!-- PB-69 -->El tipo de contenido de productos ahora proporciona una opción para ordenar los productos por SKU en el orden en que los agrega a una lista dentro del administrador.

![Nuevo](../assets/new.svg) **Se agregó la clasificación de categorías de productos** - <!-- PB-181 -->. El tipo de contenido Productos ahora proporciona una opción para ordenar los productos por categoría _posición_, mostrándolos en el mismo orden en que aparecen en el catálogo Commerce.

![Nuevo](../assets/new.svg) **Totales de selección de productos agregados** - <!-- PB-107 -->. El editor de administración de tipo de contenido Productos ahora muestra el número total de productos que coinciden con las opciones de selección de productos.

![Problema corregido](../assets/fix.svg) **Varias correcciones**

- &#x200B;<!-- PB-237 -->Mejoras de seguridad.
- &#x200B;<!-- PB-41 -->AJAX Se han corregido las búsquedas dentro de los componentes seleccionados de la IU para realizar solo una solicitud de por término de búsqueda.
- &#x200B;<!-- PB-76, PB-84-->Se han actualizado las vistas previas de productos en el Administrador para que coincidan con la tienda, incluidas las opciones de clasificación por estrellas, color y tamaño del producto cuando corresponda.
- &#x200B;<!-- PB-169 -->Se ha corregido un problema en el cual [!DNL Page Builder] no se podía guardar cuando la minificación y el agrupamiento de JavaScript estaban habilitados en Commerce.
- &#x200B;<!-- PB-241 -->Se han corregido las vistas previas de administración de productos, bloques y bloques dinámicos para que se representen correctamente en instalaciones de Commerce que definen distintas direcciones URL para el administrador y el front-end.
- &#x200B;<!-- PB-238 -->Se han corregido las previsualizaciones de administración de productos, bloques y bloques dinámicos para que se representen correctamente en instalaciones de Commerce con B2B instalado con la opción _Iniciar sesión solo_ habilitada. Antes de esta corrección, la vista previa de [!DNL Page Builder] haría que la página se redirigiera al inicio de sesión de la cuenta del cliente.
- &#x200B;<!-- PB-239 -->Se corrigió un error de sesión que se puede producir al obtener una vista previa de una página grande en el administrador de [!DNL Page Builder].
- &#x200B;<!-- PB-248 -->Se han actualizado [!DNL Page Builder] estilos LESS para evitar la duplicación de estilos de tienda.

## 1.1.1 para Adobe Commerce 2.3.3-p1

![Nuevas](../assets/new.svg) mejoras de seguridad.

## 1.1.0 para Adobe Commerce 2.3.3

![Nuevo](../assets/new.svg) <!-- MC-15250 -->Se agregó la ordenación explícita de productos al tipo de contenido Productos.

![Nuevo](../assets/new.svg) <!-- MC-17823 -->Se han agregado botones para insertar imágenes, widgets y variables en el tipo de contenido del HTML.

![Se ha corregido un problema](../assets/fix.svg) que mejoraba la seguridad de [!DNL Page Builder].

![Se ha corregido un problema](../assets/fix.svg) <!-- MC-1805 -->Se ha actualizado [!DNL Page Builder] para que sea compatible con la versión 7.3 de PHP.

![Se ha corregido un problema](../assets/fix.svg) <!-- MC-4137 -->Se ha actualizado TinyMCE a la versión 4.9.5. Esta actualización, junto con las mejoras adicionales, solucionó varios problemas con el editor en línea TinyMCE:

- Las variables, las imágenes y los vínculos de imagen se agregan donde se coloca el cursor.
- Las tablas y las celdas de la tabla se pueden alinear al centro.
- Copiar/pegar ahora pega el contenido en la posición del cursor.
- Los vínculos se pueden aplicar al texto seleccionado.
- Las viñetas están correctamente alineadas.
- Los cambios dentro del editor en línea se pueden guardar sin hacer clic primero fuera del editor.

![Se corrigió un problema](../assets/fix.svg) <!-- MC-3880 -->Se corrigió un problema en el cual la altura mínima y la alineación vertical eran incoherentes entre las secciones del panel de edición para cada tipo de contenido.

![Se ha corregido un problema](../assets/fix.svg) <!-- MC-14994 -->Se ha corregido un problema por el cual la barra de herramientas del tipo de contenido Encabezado se colocaba de manera incorrecta la primera vez que se colocaba en el escenario.

![Se corrigió un problema](../assets/fix.svg) <!-- MC-15742 -->Se corrigieron los márgenes predefinidos en los tipos de contenido de deslizador y vídeo.

![Se corrigió un problema](../assets/fix.svg) <!-- MC-16241 -->Se corrigió un problema en el cual el símbolo de asterisco requerido se mostraba dos veces en los campos del formulario.

## 1.0.3 para Adobe Commerce 2.3.2-p2

![Nuevas](../assets/new.svg) mejoras de seguridad.

## 1.0.2 para Adobe Commerce 2.3.2-p1

![Nuevas](../assets/new.svg) mejoras de seguridad.

## 1.0.1 para Adobe Commerce 2.3.2

![Nuevo](../assets/new.svg) Garantiza la compatibilidad con Adobe Commerce 2.3.2.

## 1.0.0 para Adobe Commerce 2.3.1

![Nuevo](../assets/new.svg) lanzamiento de disponibilidad general


[PWA Studio]: https://developer.adobe.com/commerce/pwa-studio/
