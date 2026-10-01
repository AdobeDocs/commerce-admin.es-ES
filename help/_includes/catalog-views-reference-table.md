---
title: Tabla de referencia de vistas de catálogo
description: Tabla de referencia reutilizada para la cuadrícula Vistas del catálogo
source-git-commit: bc4baccc4b40fb7ecdc7f489bfaf3c797881db88
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%
---
# Tabla de referencia de vistas de catálogo

La cuadrícula muestra una fila para cada vista de catálogo creada cuando un catálogo compartido se sincroniza con [!DNL Adobe Commerce Optimizer]. La cuadrícula es de solo lectura, excepto en la acción de asignación de claves. Las vistas de catálogo se crean y eliminan automáticamente a medida que el conector sincroniza los catálogos compartidos configurados en Adobe Commerce. Si se quita un catálogo, hay un [período de gracia](/help/systems/catalog-view-sync-status.md#configure-the-deletion-grace-period) antes de que se eliminen la vista de catálogo y los datos correspondientes.

Para asignar o anular la asignación de claves de acceso restringido, consulte [Asignar claves a una vista de catálogo](/help/systems/restricted-access-keys.md#assign-keys-to-a-catalog-view).

| Campo | Descripción |
| --- | --- |
| [!UICONTROL ACO Catalog View ID] | El identificador de la vista de catálogo correspondiente en [!DNL Adobe Commerce Optimizer]. Consulte [Resumen del estado de sincronización de la vista de catálogo](/help/systems/catalog-view-sync-status.md#catalog-view-sync-status-summary) para comprobar su estado de sincronización. |
| [!UICONTROL Store View] | La vista de tienda que representa la vista de catálogo. Ver [vistas de tiendas](/help/stores-purchase/store-views.md). |
| [!UICONTROL Access Keys] | Los títulos de las claves de acceso restringido asignadas actualmente a la vista de catálogo. Consulte [Administración de claves de acceso restringido](/help/systems/restricted-access-keys.md). |
| [!UICONTROL Actions] | Seleccione **[!UICONTROL Edit Restricted Access Keys]** para asignar o anular la asignación de claves a la vista de catálogo. Ver [Asignar claves a una vista de catálogo](/help/systems/restricted-access-keys.md#assign-keys-to-a-catalog-view). |

{style="table-layout:auto"}
