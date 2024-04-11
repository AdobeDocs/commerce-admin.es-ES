---
title: Tablero de administración de datos
description: Obtenga información sobre cómo acceder a perspectivas sobre flujos de datos para [!DNL Catalog Service], [!DNL Live Search], y [!DNL Product Recommendation]s.
feature: Products, Customers, Data Import/Export
exl-id: 63c261c1-1a52-46f7-93f8-81055edf1f7b
source-git-commit: 13f47c8dccb98a721924df716ae0793db6889f3a
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# Tablero de administración de datos

El panel de administración de datos ofrece una descripción general del estado de sincronización de los datos de producto transferidos desde la base de datos de Commerce a los servicios SaaS de Commerce. Los usuarios pueden monitorizar convenientemente los estados de sincronización de productos e iniciar la resincronización de datos desde un panel unificado. Esta función proporciona información valiosa sobre la disponibilidad de los datos de productos para su tienda, lo que garantiza que se puedan mostrar rápidamente a los compradores.

## Público

El tablero de administración de datos está disponible sin coste adicional para todos los comerciantes de Commerce que utilicen [[!DNL Product Recommendations]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview), [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/guide-overview), o [[!DNL Catalog Service]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/guide-overview) con una licencia activa.

El panel de administración de datos se encuentra en *Sistema* > Transferencia de datos > *Tablero de administración de datos*.

![Tablero de administración de datos](assets/data-management-dashboard.png)

El tablero contiene los campos siguientes:

| Campo | Descripción |
|--- |--- |
| Ámbito | Sitio web específico para los datos sincronizados. |
| [!DNL Product Recommendations] | Muestra el estado de sincronización, el número de productos sincronizados y una tabla de [mostrable](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) productos sincronizados para [!DNL Product Recommendations]. |
| [!DNL Live Search] | Muestra el estado de sincronización, el número de productos sincronizados y una tabla de [mostrable](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) productos sincronizados para [!DNL Live Search]. |
| [!DNL Catalog Service] | Muestra el estado de sincronización, el número de productos sincronizados y una tabla de productos sincronizados para [!DNL Catalog Service]. |
| Configuración | Abre un cuadro de diálogo en el que puede [resincronizar manualmente los datos del catálogo](#resync-catalog-data). |
| Estado de sincronización | Muestra el número de productos que se han transferido de la base de datos de Commerce a cualquiera de los servicios SaaS en las últimas tres horas. Si realiza actualizaciones poco frecuentes en el catálogo, este valor suele ser cero. Si la sincronización está en curso, haga clic en **[!UICONTROL Refresh]** para obtener un recuento actualizado. |
| Recuento de productos | Refleja el número total de productos de catálogo disponibles para el servicio. El [!DNL Product Recommendations] y [!DNL Live Search] los paneles muestran el número total de _mostrable_ productos. [!DNL Catalog Service] no filtra productos por mostrables, por lo que si tiene ambas [!DNL Catalog Service] y [!DNL Live Search] o [!DNL Product Recommendations] instalados, es posible que los dos paneles muestren dos valores diferentes para el recuento de productos. |
| Productos sincronizados | Proporciona detalles sobre los productos del índice principal de Commerce. De forma predeterminada, esta tabla está ordenada por Última actualización. Para buscar un producto específico, utilice el **[!UICONTROL Search by SKU]** field. Para controlar qué columnas se muestran, haga clic en **[!UICONTROL Customize Table]** a la derecha de la mesa. |

## Uso del panel de administración de datos

Al actualizar productos en la base de datos de Commerce, los datos de los productos se transfieren a los servicios SaaS según la configuración del sistema. Cuando se inicia el proceso de sincronización, **Recuento de productos** indica el número de productos enviados a los servicios SaaS.

>[!IMPORTANT]
>
>El tiempo que se tarda en completar la sincronización varía en función del tamaño del catálogo y el volumen de datos actualizados.

Cuando el número de productos procesados coincide con el número de productos actualizados, indica que la sincronización ha finalizado.

### Lista de productos sincronizados

Para ver los detalles de un producto sincronizado, haga clic en el producto en la tabla.

![Detalles del producto sincronizado](assets/sync-product-detail.png)

### Resincronizar datos de catálogo

Para garantizar que los servicios SaaS de Commerce estén siempre actualizados con la información de producto más reciente, debe [implementación de una programación](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-indexers#reindex) para sincronizar datos de catálogo.

Mientras que puede [iniciar manualmente](#manually-resync-catalog) Al realizar una resincronización de datos de catálogo de la base de datos de Commerce a los servicios SaaS, no se recomienda, ya que puede aumentar la carga en los recursos de hardware. Sin embargo, la resincronización manual del catálogo puede ser necesaria en los siguientes casos:

- Siempre que se realicen cambios significativos en el catálogo de productos, como añadir nuevos productos, actualizar detalles del producto o modificar categorías

- Si notas discrepancias o problemas de rendimiento en la visualización de datos de productos en tus tiendas

- Después de cualquier actualización o cambio en las integraciones entre la base de datos de Commerce y los servicios SaaS

- Al implementar personalizaciones o configuraciones que afectan a la administración de datos del producto o a los procesos de sincronización

Al seguir estas directrices y resincronizar proactivamente los datos del catálogo según sea necesario, puede mantener la coherencia, precisión y fiabilidad de los datos en todo el ecosistema de Adobe Commerce.

#### Resincronizar el catálogo manualmente

Si necesita volver a sincronizar los datos del catálogo, haga clic en **[!UICONTROL Settings]** en el lado derecho de la página para mostrar un cuadro de diálogo donde puede iniciar una resincronización. La resincronización de los datos del catálogo obliga al servicio a recuperar datos de la base de datos de Commerce a los servicios SaaS.

![Sincronizar productos manualmente](assets/resync-data.png)
