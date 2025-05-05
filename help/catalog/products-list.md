---
title: Lista de productos
description: Obtenga información acerca de la página _[!UICONTROL Products]_ en el Administrador, donde puede crear productos y editar los existentes.
exl-id: 47e14f72-017f-456a-8904-6d32ef47e6f1
feature: Catalog Management, Products, Admin Workspace
source-git-commit: 8bb91b80f8ba957676c654e984deb5704b777612
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---

# Lista de productos

Se puede acceder a todos los productos del catálogo desde la página _[!UICONTROL Products]_&#x200B;del Administrador, donde puede crear productos y editar los existentes. Para una instalación de varios sitios, cada sitio web puede ofrecer una selección diferente de productos a la venta desde el mismo catálogo.

La lista _[!UICONTROL Products]_&#x200B;incluye todos los productos del catálogo, indica los sitios web donde están disponibles y si están actualmente habilitados para la venta. En las instalaciones de Adobe Commerce B2B con [catálogos compartidos](../b2b/catalog-shared.md) habilitados, la cuadrícula incluye una columna que indica qué productos tienen precios de descuento alternativos en un catálogo compartido.

Puede navegar por la lista página por página o buscar productos específicos. Use los [controles](../getting-started/admin-grid-controls.md) estándar para ordenar y filtrar la lista y aplicar [acciones](../getting-started/admin-actions-control.md) a los productos seleccionados.

![Cuadrícula de productos](./assets/products-grid.png){width="700" zoomable="yes"}

## Limitar visualización del producto

Para mejorar el rendimiento de los catálogos grandes, se recomienda limitar el número de productos que se muestran en la cuadrícula. Puede limitar las cuadrículas de productos mostradas para:

- Página Productos
- Añadir productos relacionados/de ampliación de venta/de venta cruzada
- Añadir productos al paquete de productos
- Añadir productos al grupo de productos
- Crear pedido (administrador)

Esta configuración para la limitación de visualización del producto está deshabilitada de forma predeterminada. Si lo habilita, puede limitar el número de productos en la cuadrícula a un valor específico. Si está habilitada y el número de productos coincidentes para la visualización de la cuadrícula es mayor que el límite de registros, se devuelve una colección limitada de registros. Cuando se alcanza el límite, el total de registros encontrados, el número de registros seleccionados y los elementos de paginación no aparecen en el encabezado de la cuadrícula.

>[!NOTE]
>
>Si no desea que la cuadrícula de productos esté limitada, utilice filtros con mayor precisión para generar una colección que tenga menos elementos que el número especificado en el campo _[!UICONTROL Records Limit]_.

**_Para configurar la limitación de visualización del producto:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL Admin]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Admin Grids]** y haga lo siguiente:

   - Establezca **[!UICONTROL Limit Number of Products in Grid]** en `Yes`.

   - (Opcional) Escriba un valor en el campo **[!UICONTROL Records Limit]** para limitar el número de productos en la cuadrícula a un valor específico. El valor mínimo predeterminado es `20000`.

   ![Configuración de cuadrículas de administración](../configuration-reference/advanced/assets/admin-admin-grids.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Controles de página

| Control | Descripción |
|--- |--- |
| [!UICONTROL Add Product] | Inicia el proceso para crear un nuevo producto simple. Para elegir un tipo de producto específico, haga clic en la flecha hacia abajo. Opciones: [[!UICONTROL Simple Product]](product-create-simple.md) / [[!UICONTROL Configurable Product]](product-create-configurable.md) / [[!UICONTROL Grouped Product]](product-create-grouped.md) / [[!UICONTROL Virtual Product]](product-create-virtual.md) / [[!UICONTROL Bundle Product]](product-create-bundle.md) / [[!UICONTROL Downloadable Product]](product-create-downloadable.md) / [[!UICONTROL Gift Card]](product-gift-card-create.md) |
| [!UICONTROL Actions] | Muestra todas las acciones que se pueden aplicar a los productos seleccionados de la lista. Para aplicar una acción a un producto o grupo de productos, seleccione la casilla de verificación en la primera columna de cada producto. Opciones: `Delete` / `Change Status` / `Update Attributes` / `Assign Inventory Source` / `Unassign Inventory Source` / `Transfer Inventory To Source` |
| [!UICONTROL Filters] | Inicia una búsqueda en el catálogo basada en los filtros actuales. |
| [!UICONTROL Default View] | Indica el diseño actual de la columna de cuadrícula. Si hay vistas de columnas de cuadrícula guardadas, puede elegir otra. |
| [!UICONTROL Columns] | Muestra todas las acciones que se pueden aplicar a los productos seleccionados de la lista. Para aplicar una acción a un producto o grupo de productos, seleccione la casilla de verificación en la primera columna de cada producto. |
| [!UICONTROL Search by keyword] | El cuadro de búsqueda, en la esquina superior izquierda, se utiliza para encontrar productos por palabra clave. |
| [!UICONTROL Edit] | Abre el producto en modo de edición. Puede lograr lo mismo haciendo clic en cualquier lugar de la fila. |

{style="table-layout:auto"}

## Columnas predeterminadas

| Columna | Descripción |
|--- |--- |
| (Casilla de verificación) | Selecciona varios registros para que estén sujetos a una acción. La casilla de verificación de la primera columna de cada registro seleccionado está marcada. Opciones: <br/>**[!UICONTROL Select All]**- Selecciona todos los registros encontrados que coinciden con la configuración de filtro actual.<br/>**[!UICONTROL Select All on This Page]** - Selecciona solamente los registros encontrados en la página actual que coinciden con la configuración del filtro. |
| [!UICONTROL ID] | Un número secuencial y único que se asigna cuando se guarda un nuevo producto por primera vez. |
| [!UICONTROL Thumbnail] | Muestra una miniatura de la imagen principal del producto. |
| [!UICONTROL Name] | El nombre del producto. |
| [!UICONTROL Type] | El tipo de producto. |
| [!UICONTROL Attribute Set] | El nombre del conjunto de atributos que se utiliza como plantilla para el producto. |
| [!UICONTROL SKU] | La única unidad de stock asignada al producto. |
| [!UICONTROL Price] | El precio unitario del producto. |
| [!UICONTROL Quantity] | La cantidad que está en stock. |
| [!UICONTROL Salable Quantity] | La suma de todas las unidades disponibles de este producto. |
| [!UICONTROL Visibility] | Indica dónde está visible el producto en el catálogo. Opciones: `Not Visible Individually` / `Catalog` / `Search` / `Catalog, Search` |
| [!UICONTROL Status] | Indica el estado del producto. Opciones: `Enabled` y `Disabled` |
| [!UICONTROL Websites] | Indica los sitios web donde el producto está disponible. |
| [!UICONTROL Action] | Abre el producto en modo de edición. |
| [!UICONTROL Shared Catalog] | ![Adobe Commerce B2B](../assets/b2b.svg) (disponible solo con [Adobe Commerce B2B](./b2b/../introduction.md)) Indica los catálogos compartidos que contienen precios personalizados para el producto. |

{style="table-layout:auto"}

## Otras columnas

| Columna | Descripción |
|--- |--- |
| [!UICONTROL Short Description] | Breve descripción del producto. |
| [!UICONTROL Special Price From Date] | La primera fecha de la promoción de precio especial. |
| [!UICONTROL Special Price To Date] | La última fecha de la promoción de precio especial. |
| [!UICONTROL Cost] | El coste real del artículo. |
| [!UICONTROL Manufacturer] | El fabricante del producto. |
| [!UICONTROL Meta Keywords] | Meta palabras clave para el producto. |
| [!UICONTROL Color] | El color del producto. |
| [!UICONTROL Set Product as New from Date] | La primera fecha del producto definido como una nueva promoción. |
| [!UICONTROL Set Product as New to Date] | La última fecha del producto definido como una nueva promoción. |
| [!UICONTROL Active From / To] | La fecha de inicio y finalización del producto. |
| [!UICONTROL Layout] | El diseño del producto. |
| [!UICONTROL Minimum Advertised Price] | El precio mínimo anunciado del producto. |
| [!UICONTROL Allow Gift Message] | El mensaje de regalo a los clientes que compran una tarjeta regalo. |
| [!UICONTROL Special Price] | Precio especial para el producto. |
| [!UICONTROL Weight] | El peso del producto. |
| [!UICONTROL Meta Title] | Meta título del producto. |
| [!UICONTROL Meta Description] | La descripción de metadatos del producto. |
| [!UICONTROL Country of Manufacture] | El país de fabricación. |
| [!UICONTROL New Theme] | Se ha aplicado una temática personalizada al producto. |
| [!UICONTROL URL Key] | La clave URL del producto. |
| [!UICONTROL Tax Class] | La clase de impuestos del producto. |
| [!UICONTROL Allow Gift Message] | Muestra la disponibilidad de la opción de mensaje de regalo para el producto. |

{style="table-layout:auto"}
