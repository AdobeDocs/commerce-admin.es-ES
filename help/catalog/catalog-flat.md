---
title: Catálogos planos
description: Obtenga información sobre la creación de un catálogo plano, en el que cada fila contiene todos los datos necesarios sobre un producto o una categoría.
exl-id: f67bd2e0-3902-41eb-b26f-c772a7692cef
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# Catálogos planos

>[!IMPORTANT]
>
>Ya no se recomienda el uso de un catálogo plano como práctica recomendada. Se sabe que el uso continuo de esta función causa una degradación del rendimiento y otros problemas de indexación. Encontrará una descripción detallada y una solución en [Centro de ayuda](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/slow-performance-slow-and-long-running-crons.html).<br/><br/>Las versiones afectadas incluyen: <br/>- Adobe Commerce en infraestructura en la nube, 2.3.x y superior<br/>- Adobe Commerce (On-Premise), 2.3.x y superior<br/>- Magento Open Source, 2.3.x y superior <br/><br/>En cualquier versión de la versión, algunas extensiones solo funcionan con tablas planas, lo que crea un riesgo si deshabilita las tablas planas. Si sabe que tiene algunas extensiones que utilizan indexadores de catálogo plano, debe tener en cuenta este riesgo al establecer esos valores en `No`.

Commerce generalmente almacena los datos de catálogo en varias tablas, según el modelo de entidad-atributo-valor (EAV). Dado que los atributos de producto se almacenan en muchas tablas, las consultas SQL a veces son largas y complejas.

Por el contrario, un catálogo plano crea tablas sobre la marcha, donde cada fila contiene todos los datos necesarios sobre un producto o una categoría. Un catálogo plano se actualiza automáticamente, ya sea cada minuto o según su trabajo cron. La indexación de catálogos planos también puede acelerar el procesamiento de las reglas de precios de catálogo y de carro de compras. Un catálogo con hasta 500 000 SKU se puede indexar rápidamente como un catálogo plano.

>[!NOTE]
>
>Antes de habilitar un catálogo plano para una tienda en directo, asegúrese de probar la configuración en un entorno de desarrollo.

## Paso 1: Habilitar el catálogo plano

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Expanda la sección _Tienda_ y haga lo siguiente:

   - Establezca **[!UICONTROL Use Flat Catalog Category]** en `Yes`. (Si es necesario, anule la selección de la casilla de verificación **[!UICONTROL Use system value]**).

   - Establezca **[!UICONTROL Use Flat Catalog Product]** en `Yes`.

   ![Configuración de catálogo plano](./assets/use-flat-catalog.png){width="700" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

1. Cuando se le pida que actualice la caché, haga clic en **[!UICONTROL Cache Management]** en el mensaje del sistema y siga las instrucciones para actualizar la caché.

## Paso 2: Verificar los resultados

Puede utilizar dos métodos para comprobar los resultados.

### Método 1: Verificar los resultados de un solo producto

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Abra un producto en modo de edición.

1. Para **[!UICONTROL Name]**, agregue el texto `_TEST` al final del nombre del producto.

1. Haga clic en **[!UICONTROL Save]**.

1. En una nueva pestaña del explorador, vaya a la página principal de la tienda y haga lo siguiente:

   - Busque el producto que ha editado.

   - Utilice la navegación para buscar el producto en la categoría asignada.

     Si es necesario, actualice la página para ver los resultados. El cambio aparecerá en un minuto o según la programación de [Cron](../systems/cron.md).

   ![Tienda con catálogo plano](./assets/storefront-flat-catalog-enabled.png){width="700" zoomable="yes"}

### Método 2: Comprobar los resultados de una categoría

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. En la esquina superior izquierda, compruebe que **[!UICONTROL Store View]** está establecido en `All Store Views`.

   Si se le solicita, haga clic en **[!UICONTROL OK]** para confirmar.

1. En el árbol de categorías, seleccione una categoría existente, haga clic en **[!UICONTROL Add Subcategory]** y siga este procedimiento:

   - Para **[!UICONTROL Category Name]**, escriba `Test Category`.

   - Una vez finalizado, haga clic en **[!UICONTROL Save]**.

     ![Subcategoría de prueba](./assets/catalog-flat-test-category.png){width="600" zoomable="yes"}

   - Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Products in Category]** y haga clic en **[!UICONTROL Reset Filter]** para mostrar todos los productos.

   - Seleccione la casilla de verificación de varios productos para añadirlos a la nueva categoría.

   - haga clic en **[!UICONTROL Save]**.

   ![Productos de categoría de prueba](./assets/catalog-flat-test-category-products.png){width="600" zoomable="yes"}

1. En una nueva pestaña del explorador, vaya a la página principal de la tienda y utilice la navegación de la tienda para ir a la categoría que ha creado.

   Si es necesario, actualice la página para ver los resultados. El cambio aparece dentro del minuto o según su programación de cron.

## Paso 3: Eliminar los datos de prueba

Haga lo siguiente para eliminar los datos de prueba y restaurar el nombre del producto y la configuración del catálogo originales.

### Quitar la categoría de prueba

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. En el árbol de categorías, seleccione la subcategoría de prueba que ha creado.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Delete]**.

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL OK]**.

   La eliminación de esta categoría no elimina los productos asignados a ella.

### Restaurar el nombre original del producto

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Abra el producto de prueba en modo de edición.

1. Quitar el texto de `_TEST` que agregó a **[!UICONTROL Product Name]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Save]**.

### Restaurar la configuración original del catálogo

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Expanda la sección _Tienda_ y haga lo siguiente:

   - Establezca **[!UICONTROL Use Flat Catalog Category]** en `No`.

   - Establezca **[!UICONTROL Use Flat Catalog Product]** en `No`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

1. Cuando se le solicite, actualice la caché.
