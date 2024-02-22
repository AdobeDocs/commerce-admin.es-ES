---
title: Tablero de administración de datos
description: Obtenga información sobre cómo acceder a perspectivas sobre flujos de datos para el servicio de catálogo, Live Search, Product Recommendations.
feature: Products, Customers, Data Import/Export
source-git-commit: eed80afd8755d416d979c362f8c21fe97ce2d2ba
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---


# Tablero de administración de datos

El panel de administración de datos proporciona una perspectiva de los flujos de datos para los productos SaaS de Adobe Commerce. Usuarios de [!DNL Live Search], [!DNL Product Recommendations], y [!DNL Catalog Service] Puede ver los estados de sincronización de productos y resincronizar datos desde un solo panel.

El panel de administración de datos se encuentra en *Sistema* > Transferencia de datos > *Tablero de administración de datos*.

![Tablero de administración de datos](assets/data-management-dashboard.png)

## Configuración

El **[!UICONTROL Settings]** en la parte derecha de la página se abre el cuadro de diálogo, donde puede volver a sincronizar los datos del catálogo.

La resincronización de los datos del catálogo obliga al servicio a recuperar los datos de la base de datos de Commerce. Esta acción se utiliza generalmente durante la primera incorporación cuando la sincronización del catálogo no se ha ejecutado durante un par de horas.

## Estado de sincronización

El _[!UICONTROL Sync]_el panel estado informa del número de productos que se han sincronizado en las últimas tres horas. Si realiza actualizaciones poco frecuentes en el catálogo, este valor suele ser cero. Clic **[!UICONTROL Refresh]**para actualizar el recuento.

## Recuento de productos

El panel de recuento de productos refleja la cantidad total de productos de catálogo disponibles para el servicio.

El [!DNL Product Recommendations] y [!DNL Live Search] los paneles muestran el número total de _mostrable_ productos. [!DNL Catalog Service] no filtra productos por mostrables, por lo que si tiene ambas [!DNL Catalog Service] y [!DNL Live Search] o [!DNL Product Recommendations] instalados, es posible que los dos paneles muestren dos valores diferentes para el recuento de productos.

## Productos sincronizados

La tabla Productos sincronizados proporciona detalles sobre los productos del índice. De forma predeterminada, esta tabla está ordenada por Última actualización.

Para buscar un producto específico, utilice el **[!UICONTROL Search by SKU]** field .
Para controlar qué columnas se muestran, haga clic en **[!UICONTROL Customize Table]** a la derecha de la mesa.
