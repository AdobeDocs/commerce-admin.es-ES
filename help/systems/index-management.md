---
title: Administración de índices
description: Déclencheur Obtenga información acerca de la administración de índices, incluidas las acciones que afectan a la reindexación y las prácticas recomendadas.
exl-id: cbb249a2-b957-44fe-bf81-df795a8fd5d1
feature: System, Configuration
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 422fce6c2676f7c760c1a97b67fbd0f45d65e19c
workflow-type: tm+mt
source-wordcount: '1296'
ht-degree: 0%

---

# Administración de índices

Adobe Commerce y Magento Open Source se reindexan automáticamente cada vez que cambian uno o más elementos. Las acciones que tienen como déclencheur la reindexación incluyen cambios de precio, la creación de reglas de precio de catálogo o de carro de compras, la adición de nuevas categorías, etc. Para optimizar el rendimiento, Commerce acumula datos en tablas especiales utilizando indexadores. A medida que los datos cambian, las tablas indizadas deben actualizarse o reindexarse. Commerce vuelve a indexar como un proceso en segundo plano y se puede acceder a su tienda durante los procesos.

La reindexación de datos acelera el procesamiento y reduce el tiempo de espera del cliente. Por ejemplo, si cambia el precio de un artículo de 4,99 a 3,99 dólares, Commerce vuelve a indexar los datos para mostrar el cambio de precio en la tienda. Sin la indexación, Commerce tendría que calcular el precio de cada producto sobre la marcha; administrar las reglas de precios del carro de compras, los precios de paquetes, los descuentos, los precios de nivel, etc. Cargar el precio de un producto puede llevar más tiempo del que el cliente está dispuesto a esperar.

Los indexadores se pueden configurar para que se actualicen al guardarlos o según lo programado. Todos los índices pueden utilizar cualquiera de las opciones, excepto Customer Grid, que solo admite al guardar. Al indexar al guardar, Commerce inicia una reindexación al guardar las acciones. La página Administración de índices completa la actualización y vacía la caché. El mensaje de reindexación aparece en un minuto o dos. Al reindexar en una programación, se ejecuta una reindexación según una programación como trabajo cron. Aparecerá un mensaje del sistema si no hay un [trabajo cron](cron.md) disponible para actualizar los indizadores que no sean válidos. Se puede acceder a su tienda durante los procesos de reindexación.

>[!NOTE]
> Los comerciantes de Adobe Commerce que usan Live Search, Servicio de catálogo o Product Recommendations tienen la opción de usar un [indexador de precios basado en SaaS](https://experienceleague.adobe.com//en/docs/commerce/price-indexer/price-indexing).

Cuando es necesario reindexar, aparece una notificación en la parte superior de la página. El índice y el mensaje se borran según el modo de reindexación y las posibles acciones que realice. Para obtener información más detallada sobre la indexación , consulte [Cómo implementa la aplicación la indexación](https://developer.adobe.com/commerce/php/development/components/indexing/#how-the-application-implements-indexing) en la _Guía para desarrolladores de PHP_.

![Administración de índices: acciones](./assets/index-management.png){width="700" zoomable="yes"}

- La administración de índices tiene una presentación ligeramente diferente para los catálogos de productos planos.
- Para evitar problemas cuando varios usuarios administradores actualicen objetos que déclencheur la reindexación automática, se recomienda configurar todos los indexadores para que se ejecuten según lo programado como [trabajos cron](cron.md). De lo contrario, cada vez que se guarde un objeto, cualquier objeto con interdependencias podría provocar un interbloqueo. Los síntomas de un bloqueo incluyen un alto uso de CPU y errores de MySQL. Como práctica recomendada, se recomienda utilizar la indexación programada.
- ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) De forma predeterminada, las acciones de administración, como la reindexación, las registra el sistema y se pueden ver en el [Informe de registros de acciones](action-log-report.md). El registro de acciones se puede configurar en [Registro de acciones de administración](action-log.md), en la configuración de administración avanzada de la tienda.

## Prácticas recomendadas para la reindexación

La reindexación y el almacenamiento en caché tienen diferentes propósitos en Commerce. Los índices hacen un seguimiento de la información de la base de datos para obtener un mayor rendimiento de búsqueda, una recuperación de datos más rápida para tiendas y mucho más. [Cachés](cache-management.md) guarda los datos cargados, las imágenes, los formatos y similares para aumentar el rendimiento al cargar y acceder a la tienda.

- Normalmente, le interesa reindexar al actualizar datos en Commerce.
- Si tiene una tienda grande o varias, puede que desee establecer indexadores como categoría y productos en trabajos cron programados debido a la posibilidad de reindexar bucles. Es posible que desee establecer el reindexado en una programación durante las horas de menor actividad.
- Al reindexar, no es necesario que realice también un vaciado de caché.
- Para instalaciones de Commerce nuevas, debe vaciar la caché y reindexar.
- El vaciado de la caché y la reindexación no vaciarán la caché del explorador web del equipo. Borra la memoria caché del explorador después de completar las actualizaciones de la tienda.

## Cambio del modo de índice

>[!IMPORTANT]
>
>En tiendas que usan [Adobe Commerce B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html) y han establecido Elasticsearch como indizador de texto completo (`catalogsearch_fulltext`): el índice de texto completo debe volver a ejecutarse después de cualquier cambio de permisos en masa o cuando el indizador &#39;permisos&#39; esté en modo &#39;Programado&#39;.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Index Management]**.

1. Seleccione la casilla de verificación de cada indizador que desee cambiar.

1. Establezca **[!UICONTROL Actions]** en una de las siguientes opciones:

   - `Update on Save`
   - `Update by Schedule`
   - `Invalidate index`

   >[!IMPORTANT]
   >
   >La cuadrícula de clientes solo se puede reindexar con `Update on Save`. Este índice **_no_** admite `Update by Schedule`.

1. Haga clic en **[!UICONTROL Submit]** para aplicar el cambio a cada indizador seleccionado.

   **Columnas de administración de índices**

   | Columna | Descripción |
   | ------ |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | [!UICONTROL Indexer] | Nombre del indizador. |
   | [!UICONTROL Description] | Descripción del indizador. |
   | [!UICONTROL Mode] | Indica el modo de actualización actual para cada indizador. Opciones: <br/>**[!UICONTROL Update on Save]**: el índice se establece para actualizarse cada vez que se guarda un cambio de entidad. Estas entidades incluyen productos, categorías y clientes. Cuando finaliza la acción de guardar, se inicia una serie de pasos para capturar los cambios y actualizar el índice. La página Administración de índices actualiza y vacía el mensaje de reindexación en un minuto o dos.<br/>**[!UICONTROL Update on Schedule]** - El índice está configurado para actualizarse según lo programado según un [trabajo cron](cron.md). El trabajo cron incluye el intervalo de programación para la reindexación y la escritura de actualizaciones en el índice cuando se ejecuta. |
   | [!UICONTROL Schedule Status] | Muestra las actualizaciones de estado de programación. |
   | [!UICONTROL Status] | Muestra uno de los elementos siguientes: <br/>**[!UICONTROL Ready]**— El índice está actualizado.<br/>**[!UICONTROL Suspended]**: la reindexación está en pausa. <br/>**[!UICONTROL Processing]**- Se está ejecutando la reindexación.<br/>**[!UICONTROL Reindex Required]**: se realizó un cambio que requiere reindexación, pero los indexadores no se pueden actualizar automáticamente. Comprueba si [cron](cron.md) está disponible y configurado correctamente. |
   | [!UICONTROL Updated] | Indica la fecha y la hora de la última actualización de un índice. |

   {style="table-layout:auto"}

## Reindexe utilizando la línea de comandos

Commerce proporciona opciones de reindexación adicionales mediante la línea de comandos. Para obtener información detallada y opciones de comando completas, consulte [Reindex](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html#reindex){:target="blank"} en la _Guía de configuración_.

## Eventos de déclencheur de índice

## Reindexación de déclencheur

| Tipo de índice | Evento de reindexación |
| ---------- | ---------------- |
| [!UICONTROL Product Prices] | Agregar grupo de clientes<br/>Cambiar configuración |
| [!UICONTROL Flat catalog product data] | Agregar almacén<br/>Agregar grupo de almacén<br/>Agregar, editar o eliminar atributo (para buscar y filtrar) |
| [!UICONTROL Flat catalog category data] | Agregar almacén<br/>Agregar grupo de almacén<br/>Agregar, editar o eliminar atributo (para buscar y filtrar) |
| [!UICONTROL Catalog category/product index] | Agregar, editar o eliminar productos (únicos, masivos e importados)<br/>Cambiar las relaciones entre productos y categorías<br/>Agregar, editar o eliminar categorías<br/>Agregar o eliminar tiendas<br/>Eliminar grupos de tiendas<br/>Eliminar sitios web |
| [!UICONTROL Catalog search index] | Agregar, editar o eliminar productos (únicos, masivos e importados)<br/>Agregar o eliminar tiendas<br/>Eliminar grupos de tiendas<br/>Eliminar sitios web |
| [!UICONTROL Stock status index] | Cambiar la configuración de inventario. |
| [!UICONTROL Category permissions index] | Agregar almacén<br/>Agregar grupo de almacén<br/>Agregar, eliminar o actualizar atributo (para buscar y filtrar) |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Ya no se recomienda el uso de un catálogo plano como práctica recomendada. Se sabe que el uso continuo de esta función causa una degradación del rendimiento y otros problemas de indexación. Consulte [Usar producto de catálogo plano](../catalog/catalog-flat.md) para obtener más información.

## Acciones y controles de índice

| Acción | Resultado | Controles |
| ------ | ------ | -------- |
| Creando una tienda, un nuevo grupo de clientes o cualquier acción enumerada en `Actions that Cause a Full Reindex` | Reindexación completa | La reindexación completa se realiza según la programación determinada por el trabajo cron de Adobe Commerce o Magento Open Source. |
| Carga masiva de elementos (importación o exportación de Commerce, consulta SQL directa y cualquier otro método que agregue, cambie o elimine datos directamente) | Reindexación parcial (solo se reindexan los elementos modificados) | Con la frecuencia determinada por su trabajo cron de Commerce. |
| Cambio del ámbito (por ejemplo, de global a sitio web) | Reindexación parcial (solo se reindexan los elementos modificados) | Con la frecuencia determinada por su trabajo cron de Commerce. |

{style="table-layout:auto"}

## Eventos que tienen como déclencheur la reindexación completa

| Indexador | Evento |
| ------- | ----- |
| [!UICONTROL Catalog Category Flat Indexer] | Crear una tienda web<br/>Crear una vista de tienda web<br/>Crear o eliminar un atributo que sea cualquiera de los siguientes:<br/>- Buscable o visible en la búsqueda avanzada<br/>- Filtrable<br/>- Filtrable en la búsqueda<br/>- Utilizado para ordenar<br/>Cambiar un atributo existente para que sea cualquiera de los anteriores.<br/>Habilitar opciones de tienda de categoría plana |
| [!UICONTROL Catalog Product Flat Indexer] | Crear una tienda web<br>Crear una vista de tienda web<br/>Crear o eliminar un atributo que sea cualquiera de los siguientes:<br/>- Buscable o visible en la búsqueda avanzada<br>- Filtrable<br>- Filtrable en la búsqueda<br/>- Utilizado para ordenar <br/>Cambiar un atributo existente para que sea cualquiera de los anteriores.<br/>Habilitar opciones de tienda de categoría plana |
| [!UICONTROL Stock status indexer] | Cuando cambien las siguientes _opciones de inventario de catálogo_ en la configuración del sistema:<br/>`Stock Options` - Mostrar productos sin existencias<br/>`Product Stock Options` - Administrar existencias |
| [!UICONTROL Price Indexer] | Agregar un grupo de clientes.<br/>Cuando cambia cualquiera de las siguientes opciones de inventario de catálogo en la configuración del sistema:<br/>`Stock Options` - Mostrar productos sin existencias<br/>`Product Stock Options` - Administrar existencias<br/>`Price` - Ámbito del precio de catálogo |
| [!UICONTROL Category or Product Indexer] | Crear o eliminar una vista de tienda<br/>Eliminar una tienda<br/>Eliminar un sitio web |

{style="table-layout:auto"}
