---
title: Monitorización del estado de sincronización de fuentes de datos en Commerce
description: Seguimiento de exportaciones. Diagnosticar problemas de sincronización para  [!DNL Catalog Service], [!DNL Live Search], [!DNL Product Recommendations] y [!DNL Adobe Commerce Optimizer Connector].
feature: Products, Customers, Data Import/Export
role: Admin
level: Beginner
exl-id: 4e1b9da0-450c-4488-8693-1938a948e792
TQID: https://experienceleague.adobe.com/Y8vYxKS-8iX-bCLSJpAiJOItWlJk348bSMWfk1Cgpbg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 424b379815ffbf818c2490d0195bf0bf7dd51ab7
workflow-type: tm+mt
source-wordcount: 1664
ht-degree: 0%

---


# Monitorización del estado de sincronización de fuentes de datos

La página [!UICONTROL Data Feed Sync Status] permite a los administradores de Commerce supervisar el estado de la exportación de las fuentes de datos de productos y categorías en el área de administración.

## Audiencia y disponibilidad {#audience}

La página Estado de sincronización de fuentes de datos está disponible sin coste adicional para los comerciantes de Commerce con una licencia activa para uno de los siguientes servicios:

- [[!DNL Product Recommendations v6.0.0]](https://experienceleague.adobe.com/es/docs/commerce/product-recommendations/guide-overview)
- [[!DNL Live Search v4.1.0]](https://experienceleague.adobe.com/es/docs/commerce/live-search/overview)
- [[!DNL Catalog Service v1.17]](https://experienceleague.adobe.com/es/docs/commerce/catalog-service/guide-overview)
- [[!DNL Adobe Commerce Optimizer Connector]](https://experienceleague.adobe.com/es/docs/commerce/aco-optimizer-connector/overview)

La página Estado de sincronización de fuentes de datos está disponible automáticamente en las configuraciones de servicio de Commerce admitidas. En implementaciones locales y de infraestructura en la nube de Adobe Commerce, si falta la página después de habilitar un servicio o conector apto, siga las instrucciones de instalación manual a continuación. No utilice el procedimiento de instalación del Compositor para experiencias SaaS gestionadas por el producto.

## Acceso a la página de estado de sincronización {#access-data-feed-sync-status-page}

En el área de Administración, vaya a **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Feed Sync Status]**.

![Página de estado de sincronización de fuente de datos que resume la actividad de exportación de fuente de datos](assets/data-feed-sync-status.png){width="600" zoomable="yes"}

>[!NOTE]
>
> Esta página informa solamente del estado de exportación. Un estado de éxito significa que los datos se exportaron correctamente; no confirma que estén disponibles en los servicios conectados. Consulte [Confirmar datos en servicios conectados](#confirm-data-in-connected-services) para obtener más información.

## Fuentes de exportación disponibles

La lista de fuentes de exportación disponibles que puede administrar desde la página Estado de sincronización de datos depende de los servicios de Commerce conectados.

- **Para [!DNL Adobe Commerce on Cloud, On Premises, and Commerce as a Cloud Service] con servicios de Commerce configurados:** Consulte [Fuentes admitidas](https://experienceleague.adobe.com/es/docs/commerce/saas-data-export/reference/feed-table-reference#supported-feeds) en la _Guía de exportación de datos SaaS_.

- **Para implementaciones locales o en la nube de Adobe Commerce configuradas con[!DNL Adobe Commerce Optimizer Connector]:** Consulte [Fuentes admitidas](https://experienceleague.adobe.com/es/docs/commerce/aco-optimizer-connector/reference/connector-reference#supported-feeds) en la _Guía del conector de Adobe Commerce Optimizer_.


## Resumen del estado de sincronización de fuente de datos {#data-feed-sync-status-summary}

La cuadrícula de resumen muestra cada fuente y sus recuentos de exportación.

| Campo | Descripción |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Nombre de fuente** | Indexador de fuentes para una entidad o parte de una entidad (producto, precio del producto). |
| **Registros de Source** | Número de registros de Commerce que requieren sincronización. Puede superar el recuento de cuadrícula de administración porque los elementos de fuente tienen ámbito (por ejemplo, código de vista de tienda). |
| **Registros enviados correctamente** | Número de elementos de fuente enviados correctamente desde Commerce al extremo de servicio configurado. Esto no confirma la ingesta descendente ni la disponibilidad del catálogo. Si se producen errores de sincronización, este número puede ser menor que el número de registros de origen. |
| **Registros con errores** | Número de registros que no se pudieron enviar a los servicios de Commerce conectados. |
| **Acción** | Seleccione **[!UICONTROL Details]** para ver la actividad de sincronización de una fuente. |

## Detalles del estado de sincronización de fuente de datos {#data-feed-sync-status-details}

En la página de resumen, seleccione un nombre de fuente o seleccione **[!UICONTROL Details]** para ver el estado de exportación de cada elemento de fuente:

![Página de detalles de estado de sincronización de fuente de datos con informes de estado de elemento de fuente](assets/data-feed-sync-status-details.png){width="600" zoomable="yes"}

| Campo | Descripción |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ID de elemento de fuente** | Identificador generado automáticamente que se utiliza con fines del sistema |
| **Id. de entidad** | El identificador único de la entidad de origen (ID de producto, ID de categoría, etc.) |
| **Identificadores de fuente** | Identificadores únicos para el elemento de fuente. Por ejemplo, SKU y código de vista de tienda de la fuente de productos. Los valores varían según la fuente. |
| **Estado de exportación** | El [estado de sincronización](#export-status-types) del elemento de fuente, con indicadores con códigos de color |
| **Fecha de última sincronización** | Fecha y hora del intento de exportación o envío más reciente desde Commerce. Esta marca de tiempo no confirma la disponibilidad descendente. |
| **¿Se ha eliminado la entidad?** | Indica si la entidad se ha eliminado en Adobe Commerce. Los elementos eliminados solo se muestran si falla la sincronización. |
| **ID de solicitud** | ID único de la solicitud de sincronización. Proporciónelo al equipo de asistencia cuando solucione problemas con las actualizaciones de entidad. |
| **Error** | Información detallada sobre errores de sincronización |

Puede administrar la vista mediante los siguientes controles:

- [!UICONTROL Mass Action] para programar la resincronización de los elementos de fuente seleccionados
- [!UICONTROL Filters] y [!UICONTROL Columns]
- [!UICONTROL Default View] para crear y guardar una vista filtrada y cambiar entre vistas

### Indicadores de estado de alimentación {#feed-health-indicators}

| **Indicador** | **Descripción** |
| ------------- | --------------- |
| Estado del indexador | <ul><li>**Listo**: el indizador está actualizado. No se requiere reindexación.</li><li>**Se requiere reindexación**: Se han cambiado los datos de Source. Ejecute un reíndice para capturar los cambios recientes.</li><li>**Procesando**: la indización está en curso.</li></ul> |
| Registro de cambios pendientes | <ul><li>**Todo sincronizado**: no hay cambios pendientes para procesar.</li><li>**Elementos pendientes**: número de cambios pendientes que esperan ser procesados. Un registro de pendientes de más de 1000 elementos puede indicar problemas de rendimiento.</li></ul> |
| Modo de indizador | <ul><li>**Modo de horario** (recomendado): el indizador se ejecuta según lo programado, lo que reduce el riesgo de pérdida de datos.</li><li>**Actualización al guardar** (tiempo real): se muestra como advertencia en la página. No se espera el modo en tiempo real y aumenta el riesgo de pérdida de datos bajo carga.</li></ul> |

>[!TIP]
>
> Para obtener más información acerca del procesamiento de índices, vea el tema [Administración de índices](index-management.md).

### Exportar tipos de estado {#export-status-types}

| **Estado** | **Descripción** | **Acción necesaria** |
| ----------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------------ |
| **Enviado al servicio** | El elemento de fuente se envió correctamente desde Commerce para su procesamiento posterior. | Ninguno |
| **Error, se volverá a intentar** | No se pudo enviar, pero el sistema intentará reenviar. | Monitor para resolución |
| **Error, requiere atención** | Error debido a un error de datos o de la aplicación. | Investigue y resuelva el problema en la columna [!UICONTROL Error] |
| **Esperando envío** | Cambios detectados en el registro de cambios pero aún no procesados. | Estado de procesamiento normal |

## Monitorización del estado de fuente de datos

Cuando se actualizan entidades relacionadas con productos y categorías en la base de datos de Commerce, los datos se transfieren a los servicios de Commerce según la configuración de la fuente. Puede supervisar la actividad de exportación y su estado actual desde la página de resumen [!UICONTROL Data Feed Sync Status].

>[!IMPORTANT]
>
> El tiempo que se tarda en completar la sincronización de datos varía en función del tamaño del catálogo, el volumen de datos actualizados y el rendimiento del servicio externo.

Cuando el recuento enviado correctamente coincide con el recuento de origen de una fuente y no queda ningún elemento en espera de envío o de error, Commerce ha completado la exportación de esa fuente. Use el tablero apropiado para [confirmar la disponibilidad descendente](#confirm-data-in-connected-services).

>[!NOTE]
>
> Adobe también proporciona herramientas de interfaz de línea de comandos y registros del sistema que los desarrolladores e integradores de sistemas pueden utilizar para administrar y realizar un seguimiento de las operaciones de sincronización. Para obtener más información, consulte la [Guía de exportación de datos SaaS](https://experienceleague.adobe.com/es/docs/commerce/saas-data-export/overview).

### Administración de exportaciones fallidas {#manage-failed-exports}

Para revisar las exportaciones con errores y programar una resincronización:

1. En la página de resumen, busque la fuente con registros fallidos.
1. Seleccione **[!UICONTROL Details]**.
1. Revise los mensajes de error en la columna [!UICONTROL Error].
1. Seleccione los registros que desea volver a sincronizar mediante las casillas de verificación.
1. En el menú [!UICONTROL Mass Action], seleccione **[!UICONTROL Schedule Resync]**, seleccione **[!UICONTROL Submit]** y confirme la operación.
1. Monitorice los cambios de estado en la página de detalles.

El sistema reintenta automáticamente ciertos errores.

#### Cuándo se debe volver a sincronizar manualmente {#resync-feed-items}

Sincronizar manualmente en estos casos:

- Persisten los errores de autenticación o permiso (códigos de estado 401 o 403)
- Ha corregido problemas de formato de datos que causaban errores de carga útil
- Se ha cambiado la configuración del servicio externo o los extremos
- Se han implementado personalizaciones que afectan a la exportación de datos

### Confirmar datos en servicios conectados {#confirm-data-in-connected-services}

Para comprobar la sincronización de un extremo a otro después de completar la exportación, utilice uno de los métodos siguientes. Para conocer los límites del estado de exportación en esta página, consulte la [nota anterior](#export-status-scope).

- **[!DNL Adobe Commerce as a Cloud Service]con servicios de Commerce:** Compruebe el [tablero de administración de datos](data-dashboard.md) aplicable para confirmar la disponibilidad del flujo descendente.
- **Adobe Commerce en la nube o local con el conector de Adobe Commerce Optimizer**: compruebe primero el estado de exportación del administrador de Commerce y, a continuación, compruebe la [página de sincronización de datos](https://experienceleague.adobe.com/es/docs/commerce/optimizer/setup/data-sync) en [!DNL Commerce Optimizer Studio]
- **[!DNL Adobe Commerce Optimizer] (independiente):** Los datos no se exportan desde el servidor de Commerce. Use la [página de sincronización de datos](https://experienceleague.adobe.com/es/docs/commerce/optimizer/setup/data-sync) en [!DNL Commerce Optimizer Studio] para confirmar la disponibilidad de los datos.

>[!TIP]
>
> Para obtener más información sobre el proceso de sincronización de datos, consulte [Sincronizar datos con la exportación de datos SaaS](https://experienceleague.adobe.com/es/docs/commerce/saas-data-export/data-synchronization/data-sync-manage#view-and-manage-the-synchronization-process) en la *Guía de exportación de datos SaaS*.

## Prácticas recomendadas {#best-practices}

- Revise la página Resumen diariamente para ver las fuentes con tasas de error altas.
- Examine semanalmente los detalles de las fuentes esenciales, como los productos y los precios.
- Rastree las tendencias de éxito de las exportaciones mensualmente para identificar problemas recurrentes.

## Solución de problemas comunes {#troubleshoot-common-issues}

| Problema | Síntomas | Qué hacer |
| ---------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Altas tasas de fallo | Muchos registros muestran *Error, requiere atención* estado | <ul><li>Comprobar el estado y la configuración del servicio externo</li><li>Revisar mensajes de error para patrones en la columna [!UICONTROL Error]</li><li>Después de resolver el problema subyacente, consulte [Administrar y resincronizar exportaciones con errores](#manage-failed-exports)</li><li>Póngase en contacto con soporte técnico externo si es necesario</li></ul> |
| Rendimiento de exportación lento | Alto registro de cambios pendientes o actualizaciones de estado lentas | <ul><li>Comprobar [indicadores de estado de fuente](#feed-health-indicators) para el indizador y el estado del registro de pendientes</li><li>Volver a ejecutar la indexación si se muestra **Reindexación necesaria**</li><li>Monitorización de tiempos de respuesta de servicio externo</li><li>Programar exportaciones durante las horas de menor actividad cuando sea posible</li><li>Revisar los recursos y el rendimiento del sistema</li></ul> |
| Errores de autenticación | Códigos de estado 401 o 403 en la columna [!UICONTROL Error] | <ul><li>Verificar credenciales y tokens de API</li><li>Compruebe los permisos de la cuenta de servicio externo</li><li>Renovar tokens caducados o ponerse en contacto con su proveedor de servicios</li><li>Una vez restauradas las credenciales, [vuelva a sincronizar los registros afectados](#manage-failed-exports)</li></ul> |
| Falta la página Estado de sincronización de fuente de datos | **[!UICONTROL Data Feed Sync Status]** no aparece en la lista bajo **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** después de habilitar un servicio conectado | <ul><li>Para Commerce as a Cloud Service, confirma que hay un servicio apto habilitado (consulta [Audiencia y disponibilidad](#audience))</li><li>Solo para Commerce en la nube o local, [Instale la extensión manualmente](#install-the-extension)</li></ul> |

Adobe Commerce on Cloud Infrastructure o local: confirme que un servicio apto para el conector de Adobe Commerce Optimizer está activado; si la página sigue sin aparecer, siga las instrucciones de instalación manual.
ACCS o Adobe Commerce Optimizer: no instale el módulo manualmente; utilice la experiencia de sincronización administrada por el producto o póngase en contacto con el equipo de asistencia técnica de servicio correspondiente.

## Instalación de la extensión {#install-the-extension}

Se requiere la instalación manual para las implementaciones locales o de Adobe Commerce en la nube solo si la página [!UICONTROL Data Feed Sync Status] no está en el área de administración después de habilitar un servicio apto. Ver [Audiencia y disponibilidad](#audience).

### Requisitos previos

- Adobe Commerce 2.4.4+. Para ver los requisitos detallados, consulte [Requisitos del sistema](https://experienceleague.adobe.com/es/docs/commerce-operations/installation-guide/system-requirements).
- [Extensión de exportación de datos de Adobe Commerce](https://experienceleague.adobe.com/es/docs/commerce/saas-data-export/reference/manage-extension), versión 103.4.15 o posterior
- Claves de autenticación con permiso para descargar el paquete requerido del repositorio de Adobe Commerce. Para crear claves de autenticación y obtener el acceso necesario al paquete, consulta [Obtener tus claves de autenticación](https://experienceleague.adobe.com/es/docs/commerce-operations/installation-guide/prerequisites/authentication-keys). Para instalaciones en la nube, consulte la [Guía de Commerce en infraestructura en la nube](https://experienceleague.adobe.com/es/docs/commerce-on-cloud/user-guide/develop/authentication-keys).
- Acceso a la línea de comandos del servidor de aplicaciones de Adobe Commerce.

### Pasos de instalación

Agregar el módulo `magento/module-data-exporter-status` mediante Composer:

```shell
composer require magento/module-data-exporter-status
```

Para ver los pasos detallados de la instalación, consulte las siguientes guías:

- [Instalar la extensión para Adobe Commerce en la infraestructura de la nube](https://experienceleague.adobe.com/es/docs/commerce-on-cloud/user-guide/configure-store/extensions)
- [Instalación de la extensión en Adobe Commerce local](https://experienceleague.adobe.com/es/docs/commerce-operations/installation-guide/tutorials/extensions)

>[!MORELIKETHIS]
>
> - [Panel de administración de datos](data-dashboard.md)
> - [Guía De Exportación De Datos SaaS](https://experienceleague.adobe.com/es/docs/commerce/saas-data-export/overview)
