---
title: Creación de un catálogo compartido
description: Obtenga información sobre la creación de catálogos compartidos y la duplicación de catálogos compartidos existentes.
exl-id: 969c352c-ff88-4902-8347-334ee8b79afb
feature: B2B, Companies, Catalog Management
role: Admin
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# Creación de un catálogo compartido

Cuando se crea un [catálogo compartido](catalog-shared.md), el sistema crea automáticamente un [grupo de clientes](account-company-customer-group.md) con el mismo nombre. Por ejemplo, si crea un catálogo compartido denominado _Catálogo ABC_, el sistema también creará un grupo de clientes de _Catálogo ABC_ correspondiente. Asignar una empresa al catálogo personalizado compartido es esencialmente lo mismo que asignarla a un grupo de clientes.

Un nuevo catálogo compartido no incluye productos, precios personalizados ni asociaciones de empresas. Un catálogo público, que es el catálogo compartido predeterminado que se crea cuando los catálogos compartidos están habilitados, se asigna automáticamente a los invitados y a los clientes que no están asociados a una compañía.

![Catálogos compartidos](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

Se deben configurar los siguientes aspectos de un catálogo compartido para poder utilizarlo:

- Ámbito del catálogo
- Selección de productos
- Precios personalizados
- Asignaciones de compañías

## Alcance del precio

Si tiene una instalación multisitio, asegúrese de configurar el alcance del precio antes de crear los catálogos compartidos. El [ámbito de precio](../catalog/catalog-price-scope.md) se puede establecer en `Global` o `Website`. Sin embargo, solo se puede configurar al principio del proceso de configuración. El selector de sitio web aparece durante el paso 2 de la [configuración del catálogo compartido](catalog-shared-pricing-structure.md).

![Selector de sitio web](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **Catálogo** y elija **Catálogo** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **Precio**.

1. Establecer **ámbito de precio de catálogo** en `Website`.

   ![Ámbito de precio de catálogo](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save Config]**.

## Paso 1: Creación del catálogo compartido

Existen dos formas de crear un catálogo compartido. Puede crear un catálogo compartido de cualquier tipo o duplicar un catálogo compartido existente. Un nuevo catálogo compartido no incluye ningún producto y aún no se ha asignado a ninguna empresa.

### Método 1: añadir un nuevo catálogo compartido

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Shared Catalog]** y haga lo siguiente:

   - Escriba un(a) **[!UICONTROL Name]** para el catálogo compartido.

     El nombre que asigne se utiliza en todo el panel de administración y del cliente, si corresponde, para hacer referencia al catálogo compartido. También se convierte en el nombre del grupo de clientes correspondiente.

   - Seleccionar **[!UICONTROL Type]** : `Custom` o `Public`.

   - Elija el(la) **[!UICONTROL Customer Tax Class]** apropiado(a) que se aplique a las compras realizadas desde el catálogo compartido.

     Para obtener más información acerca de la configuración y definición de clases de impuestos, consulte [Clases de impuestos](../stores-purchase/tax-class.md).

     El siguiente ejemplo muestra un nuevo catálogo personalizado para un cliente mayorista específico.

     ![Nuevo catálogo compartido](./assets/shared-catalog-new.png){width="600" zoomable="yes"}

   - Ingresar **[!UICONTROL Description]**

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

   El nuevo catálogo aparece en la cuadrícula _[!UICONTROL Shared Catalogs]_.

### Método 2: Duplicación de un catálogo compartido existente

Un catálogo personalizado duplicado conserva el modelo de precios y la estructura del original, pero no las asociaciones de empresa. También se crea un grupo de clientes correspondiente con el mismo nombre que el catálogo duplicado. De manera predeterminada, un catálogo duplicado se llama _Duplicate of_ el catálogo original.

Si se duplica un catálogo compartido público, el tipo de catálogo duplicado cambia a `custom`.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Para el catálogo compartido en la cuadrícula que desea duplicar, vaya a la columna **[!UICONTROL Action]** y seleccione **[!UICONTROL General Settings]**.

1. En las opciones de la parte superior de la página, haga clic en **[!UICONTROL Duplicate]**.

   ![Duplicar catálogo compartido](./assets/shared-catalog-duplicate.png){width="600" zoomable="yes"}

1. Actualice los campos siguientes para el nuevo catálogo:

   - **[!UICONTROL Name]**
   - **[!UICONTROL Type]**
   - **[!UICONTROL Customer Tax Class]**
   - **[!UICONTROL Description]**

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

   El duplicado aparece en la cuadrícula _[!UICONTROL Shared Catalogs]_, con un identificador único.

## Paso 2: completar la configuración

Después de crear un nuevo catálogo compartido, debe configurarse con la selección de productos adecuada, [asignaciones de la compañía](catalog-shared-assign-companies.md) y [permisos de categoría](../catalog/category-permissions.md). Para continuar, consulta [Establecer precios y estructura](catalog-shared-pricing-structure.md).

>[!NOTE]
>
>**[Versión B2B 1.3.0](release-notes.md#b2b-v130) y posterior**: al crear un catálogo compartido, cada [permiso de categoría](../catalog/category-permissions.md) para el catálogo se establece en _[!UICONTROL Allow for the Display Product Prices]_&#x200B;y&#x200B;_[!UICONTROL Add to Cart]_ para los grupos de clientes a los que se asigna este acceso en la configuración de permisos del catálogo. Anteriormente, esta configuración se establecía automáticamente en `Deny` incluso cuando los permisos de catálogo se establecían en `Allow`.

## Demostración del catálogo compartido

Para ver una demostración de la administración de catálogos compartidos, vea este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/3410752?quality=12&learn=on&captions=spa)

## Referencia de página de catálogo compartido

### Barra de botones

| Botón | Descripción |
|--- |--- |
| [!UICONTROL Back] | Vuelve a la página Catálogos compartidos sin guardar el nuevo catálogo compartido. |
| [!UICONTROL Reset] | Borra la forma de los cambios no guardados y restaura la información detallada del catálogo original. |
| [!UICONTROL Save and Continue Edit] | Guarda todos los cambios y mantiene el formulario abierto en el modo Edición. |
| [!UICONTROL Save] | Guarda los cambios, cierra el formulario y vuelve a la página Catálogos compartidos. |

{style="table-layout:auto"}

### Detalles del catálogo

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Name] | Identifica el catálogo compartido en todo el administrador y en las cuentas de cliente donde está disponible. El nombre del catálogo debe ser descriptivo y no debe tener más de 32 caracteres de longitud. No puede tener dos catálogos compartidos con el mismo nombre. Número máximo de caracteres: 32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** - Identifica un catálogo con precios personalizados que está disponible solamente para las compañías específicas a las que está asignado.<br/>**[!UICONTROL Public]**: identifica el catálogo compartido que está disponible para todos los visitantes invitados y para los clientes que iniciaron sesión y que no están asociados a una compañía. Cuando se instala [!DNL Adobe Commerce B2B], se crea un catálogo compartido público predeterminado, pero el administrador de un almacén debe configurarlo. Solo puede existir un catálogo compartido público a la vez. |
| [!UICONTROL Customer Tax Class] | Determina la clase de impuesto que se utiliza para las compras realizadas desde el catálogo. Las opciones incluyen todas las clases de impuestos disponibles. |
| [!UICONTROL Description] | Una breve explicación de cómo se va a utilizar el catálogo. |

{style="table-layout:auto"}

### Columnas de cuadrícula

| Campo | Descripción |
|--- |--- |
| [!UICONTROL ID] | Identificador numérico único asignado a la entidad de catálogo compartido. |
| [!UICONTROL Name] | Nombre del catálogo compartido. |
| [!UICONTROL Type] | Indica el tipo de catálogo compartido. Puede ser `Public` o `Custom`. |
| [!UICONTROL Created At] | La fecha en la que se creó el catálogo compartido en el sistema. |
| [!UICONTROL Created By] | Nombre del usuario administrador que creó un catálogo compartido. |
| [!UICONTROL Action] | La lista de acciones. Opciones: `Set Pricing and Structure`, `Assign Companies`, `General Settings`, `Delete`. |

{style="table-layout:auto"}
