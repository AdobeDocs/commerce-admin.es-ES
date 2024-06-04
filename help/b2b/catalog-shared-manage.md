---
title: Administrar los catálogos compartidos
description: Obtenga información acerca de la información y las herramientas disponibles en la página Catálogos compartidos.
exl-id: a01ac292-240d-42e7-b4c9-2982f293c521
feature: B2B, Companies, Catalog Management
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 0%

---

# Administrar los catálogos compartidos

El _[!UICONTROL Shared Catalogs]_proporciona acceso a las herramientas necesarias para administrar los catálogos compartidos. La página es similar al espacio de trabajo de administración estándar, con filtros y controles de acción. La cuadrícula enumera todos los catálogos compartidos, incluido el catálogo compartido público predeterminado y los catálogos personalizados que haya configurado.

## Actualizar la selección del producto

La selección de productos en cualquier catálogo compartido se puede actualizar fácilmente desde el _[!UICONTROL Action]_de la cuadrícula de catálogos compartidos. Los cambios que realice serán visibles para los miembros de cualquier cuenta de compañía asociada. El proceso es esencialmente el mismo que elegir productos para una nueva [estructura del catálogo](catalog-shared-pricing-structure.md), excepto que el ámbito de la configuración no se puede cambiar.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Para el catálogo compartido en la cuadrícula, vaya a **[!UICONTROL Action]** y seleccione **[!UICONTROL Set Pricing and Structure]**.

   ![Cuadrícula de catálogo compartido y menú de acciones](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. Siga las instrucciones de [Paso 2: Elegir productos](catalog-shared-pricing-structure.md#step-2-choose-the-products).

   Puede omitir el primer elemento, ya que el ámbito de un catálogo compartido no se puede cambiar después de guardarlo por primera vez.

Si está trabajando con un producto específico, la variable _[!UICONTROL Products In Shared Catalog]_enumera cada catálogo compartido donde está disponible el producto. Para obtener más información, consulte [Añadir productos a un catálogo compartido](catalog-shared-product-add.md).

![Producto en catálogos compartidos](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

## Actualizar precios personalizados

Los precios personalizados de los productos en cualquier catálogo compartido se pueden actualizar fácilmente desde la columna Acción de la cuadrícula Catálogos compartidos. Los cambios que realice serán visibles para los miembros de la compañía o grupo de clientes asociados en la tienda. El proceso es esencialmente el mismo que configurar los precios personalizados para una nueva [catálogo compartido](catalog-shared-pricing-structure.md), excepto que el ámbito de la configuración no se puede cambiar.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Para el catálogo compartido de la cuadrícula que desea actualizar, vaya a **[!UICONTROL Action]** y seleccione **[!UICONTROL Set Pricing and Structure]**.

1. En el _[!UICONTROL Catalog Structure]_página, haga clic en **[!UICONTROL Configure]**y realice una de las siguientes acciones:

   - En el indicador de progreso de la parte superior de la página, haga clic en **[!UICONTROL Pricing]**.
   - En la esquina superior derecha, haga clic en **[!UICONTROL Next]**.

1. Siga las instrucciones de [Paso 3: Establecer precios personalizados](catalog-shared-pricing-structure.md#step-3-set-custom-prices).

## Actualizar permisos de categoría

[Permisos de categoría](../catalog/category-permissions.md) se establecen automáticamente como `Allow` para productos que se agregan del árbol de categorías a un catálogo compartido. Posteriormente, puede ajustar los permisos o crear reglas adicionales, según sea necesario.

>[!NOTE]
>
>**[Versión 1.3.0 de B2B](release-notes.md#b2b-v130) y más tarde** — Al crear un catálogo compartido, cada [permiso de categoría](../catalog/category-permissions.md) para el catálogo se establece en `Allow` para el _[!UICONTROL Display Product Prices]_y_[!UICONTROL Add to Cart]_ para grupos de clientes a los que se asigna este acceso en la configuración de permisos de catálogo. Anteriormente, esta configuración se establecía automáticamente en `Deny` incluso cuando los permisos de catálogo estaban configurados en `Allow`.

>[!IMPORTANT]
>
>Todos los existentes [configuración de permisos de grupo](../configuration-reference/catalog/catalog.md#category-permissions) son ignoradas por **_todo_** categorías en el catálogo cuando la variable **_[!UICONTROL Shared Catalog]_** La función está activada. [!UICONTROL Shared Catalog] controla completamente todos los permisos de categoría del catálogo cuando está activado.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. En el árbol de categorías, seleccione la categoría de los productos que desea actualizar.

   Para incluir todos los productos, seleccione la categoría de nivel superior en el árbol.

1. Desplazarse hacia abajo y expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Category Permissions]** sección.

1. Clic **[!UICONTROL New Permission]** y haga lo siguiente:

   ![Nuevo permiso](./assets/category-permissions-new.png){width="600" zoomable="yes"}

   - Elija la **[!UICONTROL Customer Group]** que corresponde al catálogo compartido y cambie la configuración de permisos según sea necesario.

     ![Regla de permisos de categoría](./assets/shared-catalog-category-permissions.png){width="600" zoomable="yes"}

   - Para crear una regla de permisos para otro grupo de clientes, haga clic en **[!UICONTROL New Permissions]** y repita el proceso.

   - Para eliminar una regla de permiso, haga clic en _Eliminar_ ![Papelera](../assets/icon-delete-trashcan-solid.png) icono.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

## Actualización de los detalles del catálogo

La información detallada de cualquier catálogo compartido se puede actualizar fácilmente desde la columna Acción de la cuadrícula Catálogos compartidos. Los cambios que realice se reflejarán en las cuentas de compañía asociadas.

![Configuración general](./assets/shared-catalog-grid-general-settings.png){width="700" zoomable="yes"}

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Para el catálogo compartido que desea actualizar, vaya a **[!UICONTROL Action]** y seleccione **[!UICONTROL General Settings]**.

   ![Detalles del catálogo](./assets/shared-catalog-update-details.png){width="600" zoomable="yes"}

1. Actualice la información detallada del catálogo según sea necesario.

   - Al cambiar el nombre de un catálogo compartido, también se cambia el nombre del grupo de clientes correspondiente.
   - Cambio del tipo de catálogo de `Custom` hasta `Public` convierte el catálogo público existente en un catálogo personalizado. Todas las compañías asociadas con el catálogo público original se reasignan al reemplazo. Un catálogo público no se puede convertir en un catálogo personalizado.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

## Referencia de página de catálogo compartido

### Barra de botones

| Botón | Descripción |
|--- |--- |
| [!UICONTROL Back] | Vuelve a la página Catálogos compartidos sin guardar el nuevo catálogo compartido. |
| [!UICONTROL Delete] | Elimina el catálogo y reasigna las empresas asociadas y sus miembros al catálogo compartido público. |
| [!UICONTROL Reset] | Borra la forma de los cambios no guardados y restaura la información detallada del catálogo original. |
| [!UICONTROL Duplicate] | Crea un [copia duplicada del catálogo](catalog-shared-create.md). Para un catálogo personalizado, el modelo de precios y la estructura del original, pero sin las asociaciones de empresa. Si se duplica un catálogo compartido público, el tipo de catálogo duplicado cambia a `custom`. También se crea un grupo de clientes correspondiente con el mismo nombre que el catálogo duplicado. De forma predeterminada, se denomina catálogo duplicado _Duplicado de_ el catálogo original. |
| [!UICONTROL Save and Continue Edit] | Guarda todos los cambios y mantiene el formulario abierto en el modo Edición. |
| [!UICONTROL Save] | Guarda los cambios, cierra el formulario y vuelve a la página Catálogos compartidos. |

{style="table-layout:auto"}

### Detalles del catálogo

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Name] | Identifica el catálogo compartido en todo el administrador y en las cuentas de cliente donde está disponible. El nombre del catálogo debe ser descriptivo y no debe tener más de 32 caracteres de longitud. No puede tener dos catálogos compartidos con el mismo nombre. Número máximo de caracteres: 32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** : identifica un catálogo con precios personalizados que solo está disponible para las empresas específicas a las que está asignado.<br/>**[!UICONTROL Public]**: identifica el catálogo compartido que está disponible para todos los visitantes invitados y para los clientes que iniciaron sesión y que no están asociados a una compañía. Cuando se instala Adobe Commerce B2B, se crea un catálogo compartido público &quot;predeterminado&quot;, pero el administrador debe configurarlo. Solo puede existir un catálogo compartido público a la vez. |
| [!UICONTROL Customer Tax Class] | Determina la clase de impuesto que se utiliza para las compras realizadas desde el catálogo. Las opciones incluyen todas las clases de impuestos disponibles. |
| [!UICONTROL Description] | Una breve explicación de cómo se va a utilizar el catálogo. |

{style="table-layout:auto"}
