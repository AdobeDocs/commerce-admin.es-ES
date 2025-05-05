---
title: Permisos de categoría
description: Aprenda a utilizar categorías para controlar la visualización de los precios de los productos, determinar qué grupos de clientes pueden agregar productos al carro de compras y especificar la página de aterrizaje.
exl-id: d80a0545-918e-4c08-9f37-4aa3cd7771f4
feature: Catalog Management, Categories, Customers, Configuration
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 0%

---

# Permisos de categoría

{{ee-feature}}

El acceso a las categorías puede limitarse a grupos de clientes específicos o restringirse por completo. Puede controlar la visualización de los precios de los productos, determinar qué grupos de clientes pueden agregar productos al carro de compras y especificar la página de aterrizaje.

>[!NOTE]
>
>Los permisos de categorías tienen un ámbito global y, cuando se habilita, restringe el acceso a cada categoría según sus permisos individuales. De forma predeterminada, Permisos de categorías no está habilitado.

Por ejemplo, si vende solamente a clientes mayoristas, puede permitir que cualquiera examine el catálogo, pero mostrando precios y permitiendo compras solamente para compradores del grupo de clientes _Mayorista_. En el ejemplo siguiente, solo los usuarios que han iniciado sesión tienen acceso a la categoría &quot;Colecciones&quot;. Para los invitados, la opción &quot;Colecciones&quot; no aparece en el menú principal.

![Los usuarios que iniciaron sesión ven la categoría &quot;Colecciones&quot;](./assets/storefront-category-permissions-logged-in.png){width="600" zoomable="yes"}

Cuando está habilitada, aparece una nueva sección _[!UICONTROL Category Permissions]_&#x200B;en la página Categoría que le permite aplicar el acceso necesario para cada categoría. Puede agregar varias reglas de permisos a cada categoría para diferentes sitios web y grupos de clientes.

## Paso 1: Configurar los permisos de categoría

>[!IMPORTANT]
>
>**_todas_** las categorías del catálogo omiten la configuración de permisos de grupo[&#128279;](../configuration-reference/catalog/catalog.md#category-permissions) de existente cuando la característica **_[!UICONTROL Shared Catalog]_** está habilitada. [!UICONTROL Shared Catalog] controla completamente todos los permisos de categoría en el catálogo cuando está habilitado.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Category Permissions]**.

   ![Permisos de categoría](../configuration-reference/catalog/assets/catalog-category-permissions.png){width="600" zoomable="yes"}

   Para obtener una lista detallada de estas opciones, consulte [Permisos de categoría](../configuration-reference/catalog/catalog.md#category-permissions) en la _Referencia de configuración_.

1. Establezca **[!UICONTROL Enable]** en `Yes`.

1. Complete las demás opciones según lo que desee permitir o restringir en la tienda (consulte las secciones siguientes).

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

1. Cuando se le pida que actualice la caché, haga clic en el vínculo **[!UICONTROL Cache Management]** en el mensaje del sistema y siga las instrucciones para actualizar la caché.

### [!UICONTROL Allow Browsing Category]

Esta opción se aplica a todas las categorías del [sitio web](../getting-started/websites-stores-views.md).

Para permitir que los miembros de un **_grupo de clientes específico_** examinen los productos de la categoría, haga lo siguiente:

1. Establezca **[!UICONTROL Allow Browsing Category]** en `Specified Customer Groups`.

1. En el cuadro **[!UICONTROL Customer Groups]**, seleccione cada grupo que tenga permiso para examinar los productos de la categoría.

   Para seleccionar varios grupos, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) mientras hace clic en cada grupo.

   ![Permitir navegación por grupo de clientes mayoristas](./assets/category-permissions-allow-browsing-customer-groups.png){width="600" zoomable="yes"}

Para **_restringir el acceso y redirigir a una página de aterrizaje_**, haga lo siguiente:

1. Establezca **[!UICONTROL Allow Browsing Category]** en `No, Redirect to Landing Page`.

1. Elija **[!UICONTROL Landing Page]** a donde se redirigirá a los visitantes.

   ![Redirigir a la página principal](./assets/category-permissions-browse-category-landing-page.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Aunque la configuración _[!UICONTROL Allow Browsing Category]_&#x200B;se aplica a todas las categorías del sitio web, puede configurar una página de aterrizaje diferente para cada vista de tienda.

### [!UICONTROL Display Product Prices]

Esta opción se aplica a todas las categorías del [sitio web](../getting-started/websites-stores-views.md).

Para permitir que solamente los miembros de **_grupos de clientes específicos_** vean el precio de los productos en la categoría, haga lo siguiente:

1. Establezca **[!UICONTROL Display Product Prices]** en `Yes, for Specified Customer Groups`.

1. En el cuadro **[!UICONTROL Customer Groups]**, seleccione cada grupo que tenga permiso para ver el precio de los productos de la categoría.

   Para seleccionar varios grupos, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) mientras hace clic en cada grupo.)

   ![Solo el grupo de clientes mayoristas puede ver los precios](./assets/category-permissions-price-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Allow Adding to Cart]

Esta opción se aplica a todas las categorías del [sitio web](../getting-started/websites-stores-views.md).

Para permitir que solamente los miembros de **_grupos de clientes específicos_** pongan productos de categoría en el carro de compras, haga lo siguiente:

1. Establezca **[!UICONTROL Allow Adding to Cart]** en `Yes, for Specified Customer Groups`.

1. En el cuadro **[!UICONTROL Customer Groups]**, seleccione cada grupo que tenga permiso para agregar productos de la categoría al carro de compras.

   Para seleccionar varios grupos, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) mientras hace clic en cada grupo.

   ![Solo el grupo de clientes mayoristas puede poner el producto en el carro](./assets/category-permissions-cart-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Disallow Catalog Search]

Establezca esta opción para evitar que los miembros de un grupo de clientes específico utilicen la búsqueda en el catálogo. Se aplica a todas las categorías del [sitio web](../getting-started/websites-stores-views.md).

- Para permitir que **_solo los clientes que iniciaron sesión_** utilicen la búsqueda en el catálogo, seleccione `NOT LOGGED IN`.

- Para permitir que **_solo grupos de clientes específicos_** usen la búsqueda en el catálogo, seleccione cada grupo que desee excluir mediante la búsqueda en categorías.

  Para seleccionar varios grupos, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) mientras hace clic en cada grupo.

  ![No se permite la búsqueda en el catálogo para el grupo de clientes generales](./assets/category-permissions-disallow-category-search.png){width="600" zoomable="yes"}

## Paso 2: Aplicar permisos de categoría

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. En el árbol de categorías, seleccione la categoría de destino.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Category Permissions]** en la página y haga lo siguiente:

   - Para crear una regla de permisos, haga clic en **[!UICONTROL New Permission]**.

     ![Sección de permisos de categoría](./assets/category-permissions-section-admin.png){width="600" zoomable="yes"}

   - Elija el(la) **[!UICONTROL Website]** y **[!UICONTROL Customer Group]** aplicables.

   - Establezca los permisos individuales según sea necesario.

   >[!NOTE]
   >
   >Cuando el permiso `Browsing Category` = `Deny` está establecido para cualquier categoría principal, no se muestra en la ruta de exploración [Ruta de exploración](navigation-breadcrumb-trail.md) en la página de la categoría secundaria.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

>[!NOTE]
>
>Si se establecen permisos de **_Permitir_** para `Root Category`, estos permisos se aplicarán automáticamente a todas las subcategorías y a todos los productos dentro de `Catalog`. Si algún producto está asignado a varias categorías y tiene permisos de **_Permitir_** para al menos una categoría, tiene automáticamente los mismos permisos de **_Permitir_** para todas las categorías asignadas.
