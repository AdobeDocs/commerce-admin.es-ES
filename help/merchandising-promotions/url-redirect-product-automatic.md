---
title: Redirecciones automáticas
description: Obtenga información sobre cómo configurar las redirecciones automáticas que se generan cada vez que la clave URL de un producto o categoría cambia en la tienda Commerce.
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
source-git-commit: d088d5833b9c61e7b1c90a0839fdf38527929ce5
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# Redirecciones automáticas

Su tienda se puede configurar para que genere automáticamente una redirección permanente cada vez que cambie la clave URL de un producto o categoría. En la sección Optimización del motor de búsqueda, la casilla de verificación debajo de la clave URL indica si las redirecciones permanentes están habilitadas. Si la tienda ya está configurada para redirección automáticamente las URL del catálogo, una redirección es una simple actualización de la clave URL. El proceso para crear una redirección automática es el mismo para los productos y las categorías.

>[!NOTE]
>
>Cuando se habilitan las redirecciones automáticas y se guarda una categoría, todas las reescrituras de productos y categorías se generan en tiempo real y se almacenan en tablas de bases de datos de forma predeterminada. Esto podría provocar problemas de rendimiento significativos para las categorías con muchos productos asignados. La solución consiste en cambiar este valor predeterminado y omitir la generación de reescrituras de URL de categoría/productos para los productos al guardar la categoría. En este caso, las reescrituras de productos se generan solo para la URL del producto canónico.

## Configurar redirecciones automáticas

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Expanda ![Expansión selector](../assets/icon-display-expand.png) la **[!UICONTROL Search Engine Optimization]** sección.

   ![Configuración del catálogo: optimización del motor de búsqueda](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Se establece **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]** en `Yes`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.


>[!NOTE]
>
> Las reescrituras de URL se pueden generar para la vista de tienda o el ámbito del sitio web. Configure el URL ámbito de reescritura desde el administrador en **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]****[!UICONTROL Catalog]**>**[!UICONTROL Catalog]**>**[!UICONTROL Search Engine Optimization]**. Seleccione el ámbito en el_[!UICONTROL Product URL Rewrite Scope]_ campo.

## redirección automáticamente las URL del producto

1. En la barra lateral _Administración_ , ve a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Busque el producto en la lista y haga clic para abrir el registro.

1. Expanda ![Expansión selector ](../assets/icon-display-expand.png) la **[!UICONTROL Search Engine Optimization]** sección.

   ![Optimización del motor de búsqueda de productos: redirección permanente](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL URL Key]**, haga lo siguiente:

   - Asegúrese de que la casilla de verificación **[!UICONTROL Create Permanent Redirect for old URL]** esté seleccionada. Si no, siga las instrucciones para [habilitar las redirecciones automáticas](url-rewrite.md#configure-url-rewrites).

   - Actualice según **[!UICONTROL URL Key]** sea necesario, utilizando todos los caracteres en minúsculas y guiones no finales entre estos caracteres en lugar de espacios.

1. Cuando haya terminado, haga clic en **[!UICONTROL Save]**.

1. Cuando se le pida que actualice la caché, siga los vínculos del mensaje situado en la parte superior del espacio de trabajo.

   La redirección permanente ya está en vigor para el producto y cualquier dirección URL de categoría asociada.

## Redirigir automáticamente las direcciones URL de categoría

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Busque la categoría en el árbol y haga clic en para abrir el registro.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Search Engine Optimization]**.

1. Para **[!UICONTROL URL Key]**, haga lo siguiente:

   - Asegúrese de que la casilla de **[!UICONTROL Create Permanent Redirect for old URL]** verificación esté seleccionada. Si no es así, seguir las instrucciones para [habilitar los redireccionamientos automáticos](url-rewrite.md#configure-url-rewrites).

   - Actualice según **[!UICONTROL URL Key]** sea necesario, utilizando todos los caracteres en minúsculas y guiones no finales entre estos caracteres en lugar de espacios.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

1. Cuando se le pida que actualice la caché, siga los vínculos del mensaje situado en la parte superior del espacio de trabajo.

   La redirección permanente ya está en vigor para la categoría y todas las direcciones URL de productos asociadas.

## Omitir la generación de productos URL reescrituras para guardarlas categoría {#skip-rewrite}

>[!WARNING]
>
>Si se desactiva la generación automática de categoría/productos URL reescrituras, se eliminan permanentemente todas las reescrituras existentes de categoría/tipo de producto URL, que no se pueden restaurar. Esto podría causar conflictos de tipo categoría o de producto sin resolver URL que requieren una actualización manual de la clave de URL para resolverse.

1. En la barra lateral _Administración_ , ve a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Search Engine Optimization]**.

1. Establezca **[!UICONTROL Generate "category/product" URL Rewrites]** en `No`.

1. En el cuadro de diálogo de confirmación, haga clic en **[!UICONTROL OK]** para confirmar el cambio y la eliminación de las reescrituras de URL existentes.

   ![Desactivación de reescrituras de categoría URL de producto y confirme](./assets/seo-rewrite-off.png){width="350"}

1. Cuando haya terminado, haga clic en **[!UICONTROL Save Config]**.
