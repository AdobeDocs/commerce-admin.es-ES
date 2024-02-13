---
title: Tablero de administración de datos
description: Obtenga información sobre el tablero de administración de datos
feature: Products, Customers, Data Import/Export
source-git-commit: 925af4d3841f2972dfffcd52125a41c4a4b28815
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Tablero de administración de datos

El panel de administración de datos proporciona una perspectiva de los flujos de datos para los productos SaaS de Adobe Commerce. Usuarios de [!DNL Live Search], [!DNL Product Recommendations], y [!DNL Catalog Service] Puede ver los estados de sincronización de productos y resincronizar datos desde un solo panel.

El panel de administración de datos se encuentra en *Sistema* > Transferencia de datos > *Tablero de administración de datos*.

![Tablero de administración de datos](assets/data-management-dashboard.png)

## Configuración

El botón Settings de la derecha de la página abre el [[!DNL Catalog Sync]](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/data-services/catalog-sync.html) cuadro de diálogo configuración.

Normalmente, la variable [!DNL Catalog Sync] El proceso se ejecuta automáticamente una vez cada hora.

La resincronización de los datos del catálogo obliga al servicio a recuperar datos de la base de datos de Commerce, lo que garantiza que los cambios más recientes se reflejen en el servicio y en el sitio. Utilice este botón si ha realizado varios cambios en el producto y necesita que los actualice antes del proceso de sincronización automática normal.

## Estado de sincronización

El _[!UICONTROL Sync]_el panel estado informa del número de productos que se han sincronizado en las últimas tres horas. Si realiza actualizaciones poco frecuentes en el catálogo, este valor suele ser cero. Clic **[!UICONTROL Refresh]**para actualizar el recuento.

## Recuento de productos

El panel de recuento de productos refleja la cantidad total de productos de catálogo disponibles para el servicio.

El [!DNL Catalog Service] panel refleja la cantidad total de productos en el catálogo disponibles para el servicio. Generalmente, se trata de todos los productos de la base de datos de Commerce.

Los paneles de Product Recommendations y Live Search muestran el número total de [_investigable_](https://experienceleague.adobe.com/docs/commerce-admin/catalog/catalog/search/search.html) productos. Si algunos productos no están configurados para la búsqueda, esto tendría en cuenta la diferencia en los totales de productos entre [!DNL Product Recommendations] y [!DNL Live Search], y [!DNL Catalog Service].

## Productos sincronizados

La tabla Productos de catálogo sincronizados proporciona detalles sobre los productos del índice. De forma predeterminada, esta tabla está ordenada por Última actualización.

Para buscar un producto específico, utilice**[!UICONTROL Search by SKU]** campo .
Para controlar qué columnas se muestran, haga clic en **[!UICONTROL Customize Table]** a la derecha de la mesa.
