---
title: Monitorización del estado de sincronización de vista de catálogo
description: Monitorice el estado de la proyección del catálogo compartido B2B y concilie las vistas de catálogo, las políticas, los libros de precios y las claves de acceso del conector de Adobe Commerce Optimizer.
feature: Products, Customers, Data Import/Export
role: Admin
level: Intermediate
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: b974b164-8a4e-43b8-a9e2-8e67ec131677
    internal-label: Commerce on Prem
  - id: cdf0c6dd-1717-4e20-9530-a24eee57088b
    internal-label: Commerce on Cloud
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
    internal-label: Reporting
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '1332'
ht-degree: 0%
---

# Monitorización del estado de sincronización de vista de catálogo

Utilice la página Estado de Sincronización de Vista de Catálogo para supervisar la sincronización y solucionar problemas de las vistas de catálogo que se han proyectado en Adobe Commerce Optimizer. Para cada catálogo compartido personalizado, [!DNL Adobe Commerce Optimizer Connector for B2B] crea una vista de catálogo para cada vista de tienda dentro del ámbito del sitio web del catálogo compartido. Cada vista del catálogo se configura con una directiva de selección, su libro de precios vinculado y la clave pública utilizada para validar los tokens de acceso restringido. Adobe Commerce conserva los metadatos de la vista de catálogo correspondientes, incluida la clave privada y el ID de libro de precios predeterminado.

>[!NOTE]
>
>Para realizar un seguimiento del estado de sincronización de las fuentes de datos del catálogo, utilice la página [[!UICONTROL Data Feed Sync Status]](data-feed-sync-status.md).

## Audiencia y disponibilidad {#audience}

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Solo se aplica a Adobe Commerce en infraestructura en la nube y a proyectos locales."}

La página [!UICONTROL Catalog View Sync Status] está disponible para Adobe Commerce en la infraestructura en la nube y para los comerciantes locales que utilizan catálogos compartidos B2B con la integración [!DNL Adobe Commerce Optimizer Connector for B2B]. La página se instala y activa automáticamente cuando se instala la extensión del conector.

## Acceso a la página Estado de sincronización de vista de catálogo {#access-catalog-view-sync-status-page}

En el área de Administración, vaya a **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Catalog View Sync Status]**.

![La página Estado de sincronización de vista de catálogo enumera las vistas de catálogo con su estado de sincronización](assets/catalog-view-sync-status.png){width="600" zoomable="yes"}

La página tiene tres pestañas:

- **[!UICONTROL Catalog Views]**: vistas de catálogo creadas por el conector, con estado de sincronización para cada una. Ver [Resumen del estado de sincronización de vista de catálogo](#catalog-view-sync-status-summary).
- **[!UICONTROL Orphaned in ACO]**: entidades que existen en [!DNL Adobe Commerce Optimizer] sin el origen correspondiente [!DNL Adobe Commerce]. Ver [Huérfano en la ficha ACO](#orphaned-in-aco-tab).
- **[!UICONTROL Deleted]**: registro de proyecciones de vista de catálogo eliminado porque se eliminó su catálogo compartido. Consulte [Ficha eliminada](#deleted-tab).

## Resumen del estado de sincronización de vista de catálogo {#catalog-view-sync-status-summary}

Las tarjetas de resumen de la parte superior de la página muestran el número de vistas de catálogo en cada estado de mantenimiento, además de un recuento de claves de acceso restringido que caducan en un plazo de 30 días:

| Tarjeta | Descripción |
| --- | --- |
| **Correcto** | Vistas de catálogo sin deriva detectada. |
| **Degradado** | Vistas de catálogo con deriva reparable. |
| **Error** | Vistas de catálogo que nunca se crearon o que se eliminaron directamente en [!DNL Adobe Commerce Optimizer]. |
| **Claves ≤ 30D** | Claves de acceso restringido que caducan en un plazo de 30 días. |

La cuadrícula muestra una fila por vista de catálogo:

| Campo | Descripción |
| --- | --- |
| **Vista de catálogo** | El identificador de la vista de catálogo proyectada en [!DNL Adobe Commerce Optimizer]. |
| **Source** | El catálogo compartido desde el que se proyectó la vista de catálogo. Seleccione el vínculo para abrir el catálogo compartido en Admin. |
| **Vista de tienda** | La vista de tienda que representa la vista de catálogo. |
| **Compañías** | Número de empresas vinculadas actualmente a esta vista de catálogo. |
| **Estado** | Estado de sincronización general de la vista de catálogo. Ver [Valores de estado de sincronización](#sync-status-values). |
| **Directiva** | Si la directiva de selección asignada a esta vista de catálogo coincide con la configuración de [!DNL Adobe Commerce]. |
| **Libro de precios** | Si el libro de precios asignado a esta vista de catálogo coincide con la configuración de [!DNL Adobe Commerce]. |
| **Clave de acceso** | Si una clave de acceso restringido está vinculada a esta vista de catálogo. |
| **La Clave Caduca** | La fecha de caducidad de la clave de acceso restringido de la vista de catálogo y el número de días restantes. |
| **Desviación** | El tipo de deriva detectada, si la hay. |
| **Última reconciliación** | La última vez que el proceso de reconciliación comprobó esta vista de catálogo. |
| **Acción** | **[!UICONTROL View details]** abre la página de detalles Estado de sincronización de vista de catálogo para ver el estado actual, el desplazamiento, las claves de acceso y los eventos recientes. **[!UICONTROL Open in ACO admin]** abre la página de detalles de vista de catálogo en [!DNL Adobe Commerce Optimizer] Studio. **[!UICONTROL Copy ID]** copia el identificador de vista de catálogo como referencia. Ver [Conciliar y reparar el desfase](#reconcile-and-repair-drift). |

## Sincronizar valores de estado {#sync-status-values}

| Estado | Significado |
| --- | --- |
| **Correcto** | No se detectan desviaciones. La vista de catálogo, la directiva, el libro de precios y las claves coinciden con la configuración de [!DNL Adobe Commerce]. |
| **Degradado** | Se detectó la deriva y es reparable; por ejemplo, se cambió una directiva o un libro de precios directamente en [!DNL Adobe Commerce Optimizer]. |
| **Error** | La vista de catálogo nunca se creó o se eliminó directamente en [!DNL Adobe Commerce Optimizer]. |
| **Pendiente** | La vista de catálogo aún no se ha reconciliado o está esperando a su primera proyección. |
| **Retirándose** | El catálogo compartido se eliminó en [!DNL Adobe Commerce] y la vista del catálogo se encuentra dentro de su período de gracia de eliminación. |
| **Eliminado** | La proyección de la vista de catálogo se eliminó después de su período de gracia. Se guarda como un registro en la ficha [!UICONTROL Deleted] durante 90 días. |
| **Huérfano** | La vista o clave del catálogo existe en [!DNL Adobe Commerce Optimizer], pero no tiene el origen [!DNL Adobe Commerce] correspondiente. Ver [Huérfano en la ficha ACO](#orphaned-in-aco-tab). |

### Configuración del período de gracia de eliminación {#configure-the-deletion-grace-period}

El período de gracia de eliminación especifica el período de retención de datos para las vistas de catálogo y los datos asociados después de eliminar el catálogo compartido asociado. El valor predeterminado es de 7 días.
Una vez que caduca la ventana, se eliminan todos los datos.

#### Cambiar la configuración de retención de datos

1. Abra el administrador [!DNL Adobe Commerce].

1. En el menú **[!UICONTROL Stores]**, seleccione **[!UICONTROL Configuration]** > **[!UICONTROL Services]** > **[!UICONTROL ACO Catalog View Sync]** > **[!UICONTROL Deletion]** > **[!UICONTROL Deletion Grace Period (days)]**.

1. Actualice el valor **[!UICONTROL Deletion Grace Period (days)]** según sea necesario.

   Para quitar una proyección de ACO de vista de catálogo inmediatamente después de eliminar un catálogo compartido, establezca este valor en `0`.

1. Seleccione **[!UICONTROL Save Config]**.

Para obtener más información, consulte [Servicios > Sincronización de vista de catálogo de ACO](../configuration-reference/services/aco-catalog-view-sync.md) para todos los ajustes de sincronización y reconciliador de deriva disponibles.

## Reconciliación y reparación de diferencias de configuración {#reconcile-and-repair-drift}

[!DNL Adobe Commerce] es el origen autorizado para la proyección del catálogo compartido B2B. La reconciliación compara la configuración de [!DNL Adobe Commerce] con [!DNL Adobe Commerce Optimizer] y notifica o repara cualquier diferencia.

>[!IMPORTANT]
>
>Los cambios realizados directamente en [!DNL Adobe Commerce Optimizer] en una vista de catálogo, una directiva, un libro de precios o una clave administrados por el conector no son la fuente primaria de verdad. La reconciliación informa de estas diferencias como diferencias de configuración y, cuando se repara, las revierte para que coincidan con [!DNL Adobe Commerce]. Realice cambios de configuración en [!DNL Adobe Commerce], no en [!DNL Adobe Commerce Optimizer]. La reparación no elimina las directivas que haya añadido manualmente junto con la que administra el conector.

Utilice los botones de nivel de página para reconciliar:

- **[!UICONTROL Reconcile]**: comprueba las diferencias de configuración y actualiza el estado de sincronización sin realizar ningún cambio en [!DNL Adobe Commerce Optimizer].

- **[!UICONTROL Reconcile & Repair]**: comprueba las diferencias de configuración y restaura automáticamente la configuración esperada para detectar cualquier diferencia reparable.

  Si se selecciona **[!UICONTROL Reconcile & Repair]**, se enviará una solicitud de reconciliación asincrónica y se devolverá antes de que se ejecute la reparación. Un mensaje de confirmación indica que el estado se actualizará en breve, pero la página no se vuelve a cargar automáticamente. Espere a que finalice el procesamiento y, a continuación, actualice la cuadrícula para comprobar el resultado.

Utilice el menú **[!UICONTROL Action]** de una fila para lo siguiente:

- **[!UICONTROL View details]**: abra la página de detalles Estado de sincronización de vista de catálogo para ver el estado actual, el desplazamiento, las claves de acceso y los eventos recientes.
- **[!UICONTROL Open in ACO admin]**: abre la página de detalles de vista de catálogo en [!DNL Adobe Commerce Optimizer] Studio.
- **[!UICONTROL Copy ID]**: copie el ID de vista de catálogo como referencia.

## Huérfano en la ficha ACO {#orphaned-in-aco-tab}

La ficha **[!UICONTROL Orphaned in ACO]** enumera las vistas de catálogo y las claves de acceso restringido que existen en [!DNL Adobe Commerce Optimizer] pero que no tienen un origen [!DNL Adobe Commerce] correspondiente; por ejemplo, las entidades creadas manualmente en [!DNL Adobe Commerce Optimizer] Studio en lugar de hacerlo el conector. Estas entidades no pueden aparecer en la cuadrícula principal porque no hay ningún registro de [!DNL Adobe Commerce] con el que coincidan.

![Entidades huérfanas en la ficha ACO que enumeran sin origen Adobe Commerce](assets/catalog-view-sync-orphan.png){width="600" zoomable="yes"}

| Campo | Descripción |
| --- | --- |
| **Tipo** | La categoría de la entidad huérfana: [!UICONTROL Catalog View] o [!UICONTROL Access Key]. |
| **ID DE ACO** | El identificador de la entidad en [!DNL Adobe Commerce Optimizer]. |
| **Detalle** | Contexto adicional sobre la entidad, como su directiva. |
| **Visto por primera vez** | Cuando la reconciliación detectó esta entidad por primera vez. |
| **Acción** | Seleccione **[!UICONTROL Copy ID]** para copiar el identificador de entidad. Utilice el identificador copiado para localizar y quitar la entidad de [!DNL Adobe Commerce Optimizer] vistas del catálogo de Studio. |

>[!NOTE]
>
>Esta pestaña es solo de informe. La reconciliación nunca elimina las entidades huérfanas. Elimínelos directamente en [!DNL Adobe Commerce Optimizer] Studio si ya no los necesita.

## Pestaña Eliminada {#deleted-tab}

La ficha **[!UICONTROL Deleted]** enumera las proyecciones de vista de catálogo que se eliminaron porque su catálogo compartido se eliminó en [!DNL Adobe Commerce]. Dado que el catálogo compartido y su vista de catálogo ya no existen, estas filas no se vinculan a ninguna parte. Solo se guardan como un registro de lo que se ha eliminado.

![Se eliminó una pestaña que enumera las proyecciones de vista de catálogo eliminadas después de que se eliminara su catálogo compartido](assets/catalog-view-sync-deleted.png){width="600" zoomable="yes"}

| Campo | Descripción |
| --- | --- |
| **Vista de catálogo** | El identificador de la vista de catálogo eliminada. |
| **Source** | El catálogo compartido que se ha eliminado. |
| **Vista de tienda** | La vista de tienda que representa la vista de catálogo. |
| **Eliminado A Las** | Cuando se eliminó la proyección. |

Las filas de esta pestaña se borran automáticamente al cabo de 90 días.

## Limitaciones conocidas

- No hay ningún indicador visual en [!DNL Adobe Commerce Optimizer] Studio que distinga las vistas de catálogo administradas por conectores de las creadas manualmente. Utilice esta página, no la interfaz de usuario de [!DNL Adobe Commerce Optimizer] Studio, para determinar lo que administra el conector.
- La columna **[!UICONTROL ACO ID]** de la ficha **[!UICONTROL Orphaned in ACO]** identifica una vista de catálogo, una directiva o una clave de acceso, no un identificador único. El nombre de las columnas está sujeto a cambios.

>[!MORELIKETHIS]
>
> - [Administrar configuración de vista de catálogo](/help/b2b/catalog-views-manage.md): revise las vistas de catálogo desde el catálogo compartido o la cuenta de la compañía
> - [Estado de sincronización de fuente de datos](data-feed-sync-status.md)
> - [Servicios > Sincronización de vista de catálogo de ACO](../configuration-reference/services/aco-catalog-view-sync.md): configure los períodos de gracia de eliminación y creación y el reconciliador de deriva
> - [Administración de claves de acceso restringido](restricted-access-keys.md): administre las claves cuya caducidad muestra esta página
> - [Supervisar la sincronización de la vista del catálogo para los catálogos compartidos B2B](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/manage-sync/catalog-view-sync/catalog-view-sync-status) en la *Guía del conector de Adobe Commerce Optimizer*
> - [Vistas del catálogo privado](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/private-catalog-view)
> - [Claves de acceso restringido](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/restricted-access-keys)
