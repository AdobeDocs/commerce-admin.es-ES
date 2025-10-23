---
title: Monitorización del estado de fuente de datos
description: Supervise la sincronización de exportación de datos e identifique cualquier problema o retraso con el procesamiento de fuentes para  [!DNL Catalog Service], [!DNL Live Search] y [!DNL Product Recommendations].
feature: Products, Customers, Data Import/Export
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 433d3fd4dc10a81b685262c1e3c06a0da5778841
workflow-type: tm+mt
source-wordcount: '1455'
ht-degree: 0%

---


# Monitorización del estado de fuente de datos

Los administradores de Adobe Commerce pueden monitorizar el estado de sincronización de los datos exportados de Adobe Commerce a los servicios conectados de Commerce mediante la página Estado de sincronización de fuentes de datos en el Administrador de Commerce.

![Página de detalles de estado de sincronización de fuente de datos con informes de estado de elemento de fuente](assets/data-feed-sync-status.png)

Esta página proporciona información en tiempo real sobre el estado y el rendimiento de las fuentes de exportación de datos que transfieren datos de productos y categorías de Commerce a servicios externos como [!DNL Product Recommendations], [!DNL Live Search] y [!DNL Catalog Service].

La página de estado de sincronización solo muestra el estado de exportación. Un estado correcto indica que los datos se exportan correctamente a la base de datos SaaS para su publicación. Use [Panel de administración de datos](data-dashboard.md) para rastrear los datos transferidos de la base de datos de Commerce a los servicios conectados.

La monitorización del estado de la fuente ayuda a garantizar la coherencia de los datos y permite la rápida resolución de cualquier problema que surja durante el proceso de exportación. Los administradores pueden:

* **Ver el estado de sincronización** para todas las fuentes de datos
* **Identificar y solucionar errores** en el procesamiento de fuentes
* **Acceder a la información detallada de estado** para elementos de fuente individuales

El estado se rastrea para las siguientes fuentes:

* Fuente de productos
* Fuente de atributos del producto
* Fuente de categorías
* Fuente de invalidaciones de productos
* Fuente de precios de productos
* Fuente de variantes del producto

>[!TIP]
>
>Para obtener más información sobre el proceso de sincronización de datos, consulte [Sincronizar datos con la exportación de datos SaaS](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/data-synchronization)en la *Guía de exportación de datos SaaS**.

## Instalación de la extensión

La página Estado de fuente de datos está disponible para todos los comerciantes de Commerce con licencias activas para los siguientes servicios de Commerce:

* [[!DNL Product Recommendations v6.0.0+]](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview)
* [[!DNL Live Search v4.1.0+]](https://experienceleague.adobe.com/en/docs/commerce/live-search/guide-overview)
* [[!DNL Catalog Service v1.17+]](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/guide-overview) con una licencia activa.

**Requisitos**

* PHP 8.1, 8.2, 8.3 u 8.4
* Adobe Commerce 2.4.4+
* [Extensión de exportación de datos de Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/manage-extension), versión 103.4.15 o posterior
* Acceso a [repo.magento.com](https://repo.magento.com)

  Para generar claves y obtener los derechos necesarios, consulta [Obtener tus claves de autenticación](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys). Para instalaciones en la nube, consulte la [Guía de Commerce en infraestructura en la nube](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/authentication-keys).

* Acceso a la línea de comandos del servidor de aplicaciones de Adobe Commerce.

### Pasos de instalación

Agregar el módulo `adobe-commerce/module-data-exporter-status` mediante Composer:

```shell
composer require magento/module-data-exporter-status
```

Para ver los pasos detallados de la instalación, consulte las siguientes guías:

* [Instalar extensión en Adobe Commerce en la infraestructura de la nube](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure-store/extensions)

* [Instalar extensión de Adobe Commerce local](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/tutorials/extensions)

## Acceso a la página Estado de fuente de datos

Desde Commerce Admin, acceda a la página Estado de fuente de datos desde Commerce Admin en **[!DNL System]** > Transferencia de datos > **[!DNL Data Feed SyncStatus]**.

![Página de estado de sincronización de fuente de datos que resume la actividad de exportación de fuente de datos](assets/data-feed-sync-status.png)

La monitorización del estado de las fuentes de datos proporciona dos interfaces:

* La [página de resumen del estado de sincronización de fuentes de datos](#data-feed-sync-status-summary) que enumera las fuentes disponibles y el estado actual
* [Estado de sincronización de fuente de datos - página de detalles](#data-feed-sync-status-details) que muestra información detallada sobre una fuente seleccionada.

## Resumen del estado de sincronización de fuente de datos

La página de resumen Estado de sincronización de fuentes proporciona información sobre la actividad de exportación de fuentes de datos, incluida la siguiente información:

| Campo | Descripción |
|-------|-------------|
| **Nombre de fuente** | El nombre del indexador de fuente responsable de sincronizar una entidad específica o su parte, por ejemplo, el precio del producto. |
| **Registros de Source** | Número de registros disponibles para exportar desde la base de datos de Commerce. Este número puede ser mayor que el número de registros mostrados en el administrador de Commerce, ya que cada elemento de fuente pertenece a un ámbito específico, como el código de vista de tienda. |
| **Registros enviados correctamente** | Número de registros transmitidos correctamente al SaaS de Commerce para un procesamiento posterior. Si se produjeron errores durante la transmisión, el número de registros transmitidos correctamente a los servicios externos. |
| **Registros con errores** | Número de registros que no se exportaron y que requieren atención. |
| **Acción** | Seleccione **[!UICONTROL Details]** para ver la actividad de sincronización de una fuente. |

## Detalles del estado de sincronización de fuente de datos

En la página de resumen de estado de fuente de datos, haga clic en el nombre de una fuente o use la acción [!DNL View Details] para acceder a información detallada sobre registros individuales dentro de una fuente.

![[!UICONTROL Data Feed Sync Status - Details] página con informe de estado de elemento de fuente](assets/data-feed-sync-status-details.png)

La vista de detalles proporciona la siguiente información para cada elemento de fuente:

| Campo | Descripción |
|-------|-------------|
| **ID de elemento de fuente** | Identificador interno del registro de fuente |
| **Id. de entidad** | El ID de entidad de origen (ID de producto, ID de categoría, etc.) |
| **Estado de exportación** | El [estado de sincronización](#export-status-types) del elemento de fuente. Estado actual del intento de exportación con indicadores con códigos de color |
| **Fecha de última sincronización** | Marca de tiempo de la última vez que se envió el registro a Commerce Services |
| **¿Se ha eliminado la entidad?** | Indica si la entidad o su artículo (precio de producto o producto, por ejemplo) se ha eliminado en Adobe Commerce. Los elementos sólo se muestran si se ha producido un error durante la sincronización. |
| **ID de solicitud** | Identificador único de la solicitud de sincronización. Proporcione este ID al equipo de asistencia cuando solucione problemas relacionados con actualizaciones de entidades específicas. |
| **Error** | Información detallada del error si el elemento de fuente no se pudo sincronizar. |

Puede administrar la vista mediante los siguientes controles:

* [!DNL Mass Action] para programar la resincronización de los elementos de fuente seleccionados
* [!DNL Filters]
* [!DNL Default View] para crear y guardar una vista filtrada y cambiar entre vistas
* [!DNL Columns] para mostrar y ocultar columnas en la tabla.

### Indicadores de estado de alimentación

En la parte superior de cada página de detalles de fuente, los indicadores de estado críticos proporcionan el estado del sistema para cada fuente:

#### Estado del indexador

* **Válido**: los datos están sincronizados; no se requiere reindexación.
* **No válido**: los datos originales se cambiaron; el índice debe actualizarse.
* **Procesamiento**: indización en curso.

>[!TIP]
>
>Para obtener más información acerca del procesamiento de índices, vea el tema [Administración de índices](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/tools/index-management).

#### Registro de cambios pendientes

* **Todo sincronizado**: no hay cambios pendientes para procesar
* **Elementos pendientes**: número de cambios pendientes que esperan ser procesados

### Exportar tipos de estado

El sistema proporciona indicadores de estado para ayudarle a identificar los problemas rápidamente:

#### Categorías de estado

| **Estado** | **Descripción** | **Acción necesaria** |
|--------|-----------|-------------|
| **Enviado al servicio** | El elemento de fuente se exportó correctamente al servicio Commerce. | Ninguno |
| **Error, se volverá a intentar** | Error temporal. El sistema lo volverá a intentar automáticamente. | Monitor para resolución |
| **Error, requiere atención** | Error debido a un error de datos o de la aplicación. | Investigue y resuelva el problema en la columna [!DNL Error] |
| **Esperando envío** | En cola para la exportación, pero aún no procesado. | Estado de procesamiento normal |

## Monitorización del estado de fuente de datos

Cuando se actualizan entidades relacionadas con productos y categorías en la base de datos de Commerce, los datos se transfieren a los servicios de Commerce según la configuración de la fuente. Puede monitorizar este proceso en tiempo real desde la página de resumen del estado de sincronización de fuentes de datos.

>[!IMPORTANT]
>
>El tiempo que se tarda en completar la sincronización de datos varía en función del tamaño del catálogo, el volumen de datos actualizados y el rendimiento del servicio externo.

Cuando el número de registros enviados correctamente coincide con el número de registros de origen, indica que la sincronización ha finalizado y que todos los datos se han transmitido correctamente.

>[!NOTE]
>
>Adobe también proporciona herramientas de interfaz de línea de comandos y registros del sistema que los desarrolladores e integradores de sistemas pueden utilizar para administrar y realizar un seguimiento de las operaciones de sincronización. Para obtener más información, consulte la [Guía de exportación de datos SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview).

### Administración de exportaciones fallidas

Para ver los detalles de las exportaciones fallidas y tomar medidas correctivas:

1. En la página Estado de sincronización de fuentes, busque la fuente con registros con errores.
1. Haga clic en **[!DNL Details]**.

1. Revise los mensajes de error por motivos de error específicos.

1. Utilice acciones masivas para programar operaciones de resincronización de elementos fallidos.

### Resincronizar datos con errores

Puede volver a sincronizar manualmente las fuentes de datos problemáticas o con errores mediante el menú [!DNL Actions] de la página [!DNL Data Feed Sync Status - Details].

Aunque el sistema reintenta automáticamente ciertos tipos de errores, puede ser necesaria una intervención manual en los siguientes casos:

* Observará errores de autenticación o permisos (códigos de estado 401 y 403).
* Después de resolver los problemas de formato de datos que causaban errores de carga útil.
* Las siguientes actualizaciones corresponden a configuraciones de servicio externo o extremos.
* Está implementando personalizaciones que afectan a los procesos de exportación de datos.

Al monitorizar proactivamente el estado de las fuentes y corregir los errores con rapidez, puede mantener la coherencia y fiabilidad de los datos en todo el ecosistema de Commerce.

#### Resincronizar manualmente los elementos de fuente

Si necesita volver a sincronizar elementos de fuente específicos:

1. **Seleccionar registros**: utilice casillas de verificación para seleccionar los registros con errores que requieran atención.
2. **Elegir acción**: seleccione **[!DNL Schedule Resync]** en la lista desplegable de acciones masivas.
3. **Confirmar**: Haga clic en **[!DNL Submit]** y confirme la operación de resincronización.
4. **Supervisar resultados**: Compruebe el mensaje de éxito y los cambios de estado del monitor.

## Prácticas recomendadas

### Monitorización regular

1. **Comprobaciones diarias**: revise diariamente la página de información general para ver si hay fuentes que muestren tasas de error elevadas
1. **Inmersión profunda semanal**: Examine el estado detallado de las fuentes críticas (productos, precios)
1. **Análisis mensual**: haga un seguimiento de las tendencias en las tasas de éxito de exportación y el rendimiento

### Flujo de trabajo de resolución

1. **Identificar problemas**: busque errores y recuentos altos de errores
1. **Comprobar el estado del indizador**: Asegúrese de que los indizadores son válidos y de que el registro de pendientes es manejable
1. **Revisar detalles del error**: haga clic en los registros con errores para ver mensajes de error específicos
1. **Programar resincronización**: use acciones masivas para reintentar exportaciones con errores
1. **Resolución del monitor**: compruebe que los elementos resincronizados muestran el estado correcto

### Solucionar problemas comunes

#### Altas tasas de fallo

**Síntomas**: hay un gran número de registros que muestran el estado &quot;Fallido, requiere atención&quot;

**Causas potenciales**:

* Cambios en la configuración del servicio externo
* Incompatibilidades de formato de datos
* Problemas de autenticación o permisos

**Pasos para la resolución**:

1. Comprobar el estado y la configuración del servicio externo
1. Revisar mensajes de error para patrones
1. Verificar credenciales de autenticación
1. Póngase en contacto con soporte técnico externo si es necesario

#### Rendimiento de exportación lento

**Síntomas**: Registro de cambios alto, actualizaciones de estado lentas

**Causas potenciales**:

* Problemas de rendimiento del indizador
* Volumen de datos alto
* Limitación de velocidad de servicio externo

**Pasos de resolución**:

1. Comprobar el estado del indexador y volver a ejecutar si no es válido
2. Monitorización de tiempos de respuesta de servicio externo
3. Considere programar exportaciones durante las horas de menor actividad
4. Revisar los recursos y el rendimiento del sistema

#### Errores de autenticación

**Síntomas**: 401 o 403 códigos de estado

**Pasos de resolución**:

1. Verificar credenciales y tokens de API
1. Compruebe los permisos de la cuenta de servicio externo
1. Renovar tokens de autenticación caducados
1. Póngase en contacto con su proveedor de servicios para problemas de acceso

>[!MORELIKETHIS]
>
>* [Panel de administración de datos](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/data-transfer/data-dashboard)
>* [Guía De Exportación De Datos SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview)
