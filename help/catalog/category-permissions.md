---
title: Permisos de categoría
description: Aprenda a utilizar categorías para controlar la visualización de los precios de los productos, determinar qué grupos de clientes pueden agregar productos al carro de compras y especificar la página de aterrizaje.
exl-id: d80a0545-918e-4c08-9f37-4aa3cd7771f4
feature: Catalog Management, Categories, Customers, Configuration
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# Permisos de categoría

{{ee-feature}}

El acceso a las categorías puede limitarse a grupos de clientes específicos o restringirse por completo. Puede controlar la visualización de los precios de los productos, determinar qué grupos de clientes pueden agregar productos al carro de compras y especificar la página de aterrizaje.

>[!NOTE]
>
>Los permisos de categorías tienen un ámbito global y, cuando se habilita, restringe el acceso a cada categoría según sus permisos individuales. De forma predeterminada, Permisos de categorías no está habilitado.

Por ejemplo, si vende solo a clientes mayoristas, puede permitir que cualquiera explore el catálogo, pero mostrar precios y permitir compras solo para compradores en _Venta al por mayor_ grupo de clientes. En el ejemplo siguiente, solo los usuarios que han iniciado sesión tienen acceso a la categoría &quot;Colecciones&quot;. Para los invitados, la opción &quot;Colecciones&quot; no aparece en el menú principal.

![Los usuarios que iniciaron sesión ven la categoría &quot;Colecciones&quot;](./assets/storefront-category-permissions-logged-in.png){width="600" zoomable="yes"}

Cuando se habilita, se crea un nuevo _[!UICONTROL Category Permissions]_aparece en la página Categoría, que le permite aplicar el acceso necesario para cada categoría. Puede agregar varias reglas de permisos a cada categoría para diferentes sitios web y grupos de clientes.

## Paso 1: Configurar los permisos de categoría

>[!IMPORTANT]
>
>Todos los existentes [configuración de permisos de grupo](../configuration-reference/catalog/catalog.md#category-permissions) son ignoradas por **_todo_** categorías en el catálogo cuando la variable **_[!UICONTROL Shared Catalog]_** La función está activada. [!UICONTROL Shared Catalog] controla completamente todos los permisos de categoría del catálogo cuando está activado.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Category Permissions]** sección.

   ![Permisos de categoría](../configuration-reference/catalog/assets/catalog-category-permissions.png){width="600" zoomable="yes"}

   Para ver una lista detallada de estas opciones, consulte [Permisos de categoría](../configuration-reference/catalog/catalog.md#category-permissions) en el _Referencia de configuración_.

1. Establecer **[!UICONTROL Enable]** hasta `Yes`.

1. Complete las demás opciones según lo que desee permitir o restringir en la tienda (consulte las secciones siguientes).

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

1. Cuando se le pida que actualice la caché, haga clic en **[!UICONTROL Cache Management]** en el mensaje del sistema y siga las instrucciones para actualizar la caché.

### [!UICONTROL Allow Browsing Category]

Esta opción se aplica a todas las categorías de la [sitio web](../getting-started/websites-stores-views.md).

Para permitir miembros de un **_grupo de clientes específico_** para examinar los productos de la categoría, haga lo siguiente:

1. Establecer **[!UICONTROL Allow Browsing Category]** hasta `Specified Customer Groups`.

1. En el **[!UICONTROL Customer Groups]** , seleccione cada grupo que pueda examinar los productos de la categoría.

   Para seleccionar varios grupos, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) mientras hace clic en cada grupo.

   ![Permitir navegación por grupo de clientes mayoristas](./assets/category-permissions-allow-browsing-customer-groups.png){width="600" zoomable="yes"}

Hasta **_restringir el acceso y redirigir a una página de aterrizaje_**, haga lo siguiente:

1. Establecer **[!UICONTROL Allow Browsing Category]** hasta `No, Redirect to Landing Page`.

1. Elija la **[!UICONTROL Landing Page]** donde se redirigen los visitantes.

   ![Redirigir a página de inicio](./assets/category-permissions-browse-category-landing-page.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Aunque la variable _[!UICONTROL Allow Browsing Category]_La configuración se aplica a todas las categorías del sitio web y se puede configurar una página de aterrizaje diferente para cada vista de tienda.

### [!UICONTROL Display Product Prices]

Esta opción se aplica a todas las categorías de la [sitio web](../getting-started/websites-stores-views.md).

Para permitir sólo miembros de **_grupos de clientes específicos_** para ver el precio de los productos en la categoría, haga lo siguiente:

1. Establecer **[!UICONTROL Display Product Prices]** hasta `Yes, for Specified Customer Groups`.

1. En el **[!UICONTROL Customer Groups]** , seleccione cada grupo que pueda ver el precio de los productos de la categoría.

   Para seleccionar varios grupos, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) mientras hace clic en cada grupo.)

   ![Solo el grupo de clientes mayoristas puede ver los precios](./assets/category-permissions-price-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Allow Adding to Cart]

Esta opción se aplica a todas las categorías de la [sitio web](../getting-started/websites-stores-views.md).

Para permitir sólo miembros de **_grupos de clientes específicos_** para colocar productos de categoría en el carro de compras, haga lo siguiente:

1. Establecer **[!UICONTROL Allow Adding to Cart]** hasta `Yes, for Specified Customer Groups`.

1. En el **[!UICONTROL Customer Groups]** , seleccione cada grupo que tenga permiso para agregar productos de la categoría al carro de compras.

   Para seleccionar varios grupos, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) mientras hace clic en cada grupo.

   ![Solo el grupo de clientes mayoristas puede poner el producto en el carro de compras](./assets/category-permissions-cart-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Disallow Catalog Search]

Establezca esta opción para evitar que los miembros de un grupo de clientes específico utilicen la búsqueda en el catálogo. Se aplica a todas las categorías de la [sitio web](../getting-started/websites-stores-views.md).

- Para permitir **_solo clientes que han iniciado sesión_** para utilizar la búsqueda en el catálogo, seleccione `NOT LOGGED IN`.

- Para permitir **_solo grupos de clientes específicos_** para utilizar la búsqueda en el catálogo, seleccione cada grupo que desee excluir mediante la búsqueda por categorías.

  Para seleccionar varios grupos, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) mientras hace clic en cada grupo.

  ![No se permite la búsqueda en el catálogo para el grupo de clientes generales](./assets/category-permissions-disallow-category-search.png){width="600" zoomable="yes"}

## Paso 2: Aplicar permisos de categoría

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. En el árbol de categorías, seleccione la categoría de destino.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Category Permissions]** en la página y haga lo siguiente:

   - Para crear una regla de permisos, haga clic en **[!UICONTROL New Permission]**.

     ![Sección de permisos de categoría](./assets/category-permissions-section-admin.png){width="600" zoomable="yes"}

   - Elija el aplicable **[!UICONTROL Website]** y **[!UICONTROL Customer Group]**.

   - Establezca los permisos individuales según sea necesario.

   >[!NOTE]
   >
   >Cuándo `Browsing Category` = `Deny` se define para cualquier categoría principal, no se muestra en la [Ruta de ruta](navigation-breadcrumb-trail.md) en la página categoría secundaria.

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

>[!NOTE]
>
>Si existe **_Permitir_** Los permisos se establecen para `Root Category`, estos permisos se aplican automáticamente a todas las subcategorías y a todos los productos de `Catalog`. Si algún producto está asignado a varias categorías y tiene alguno **_Permitir_** para al menos una categoría, tiene automáticamente el mismo **_Permitir_** permisos para todas las categorías asignadas.
