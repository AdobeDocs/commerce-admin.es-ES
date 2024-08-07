---
title: Controles de cuadrícula de administración
description: Aprenda a trabajar en las páginas de administración que administran los datos para mostrar una colección de registros en una cuadrícula.
exl-id: a4a9531d-eb2f-41d6-bb36-dc6d8811ee95
source-git-commit: a3fb702d0b6e08c3aaaa0d6b5e07aa825026ef76
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# Controles de cuadrícula de administración

Las páginas de administración que administran datos muestran una colección de registros en una cuadrícula. Los controles de la parte superior de cada columna se pueden utilizar para ordenar los datos. El orden de clasificación actual se indica mediante una flecha ascendente o descendente en el encabezado de la columna. Puede especificar qué columnas aparecen en la cuadrícula y arrastrarlas a diferentes posiciones. También puede guardar diferentes disposiciones de columna como vistas que se pueden utilizar más adelante. La columna **[!UICONTROL Action]** enumera las operaciones que se pueden aplicar a un registro individual. Además, la fecha de la vista actual de la mayoría de las cuadrículas se puede exportar a un archivo [CSV](../systems/data-csv.md) o XML.

![Página de pedidos - visualización de cuadrícula](./assets/admin-workspace-grid.png){width="700" zoomable="yes"}

## Ordenar la lista

1. Haga clic en cualquier encabezado de columna.

   La flecha indica el orden actual en orden ascendente o descendente.

1. Utilice los controles de paginación para ver páginas adicionales de la colección.

   ![Pantalla de cuadrícula: controles de página](./assets/pagination-controls.png){width="300"}

## Paginación de la lista

1. Establezca el control **[!UICONTROL Pagination]** en el número de registros que desee ver por página.

1. Haga clic en **[!UICONTROL Next]** y **[!UICONTROL Previous]** para recorrer la página de la lista o escriba un elemento específico **[!UICONTROL Page Number]**.

## Filtrado de la lista

1. Haga clic en **[!UICONTROL Filters]**.

1. Complete tantos filtros como sea necesario para describir el registro que desea buscar.

1. Haga clic en **[!UICONTROL Apply Filters]**.

   ![Lista de pedidos - controles de filtro](./assets/admin-workspace-filters.png){width="700" zoomable="yes"}

## Exportación de datos

1. Seleccione los registros que desea exportar.

   >[!NOTE]
   >
   >Los datos del producto no se pueden exportar desde la cuadrícula. Para obtener más información, consulte [Exportar](../systems/data-export.md).

1. En el menú _Exportar_ (![Selector de menú](../assets/icon-export.png)) de la esquina superior derecha, elija uno de los siguientes formatos de archivo:

   - `CSV`
   - `Excel XML`

   ![Lista de pedidos - opciones de exportación](./assets/customers-grid-export.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Export]**.

1. Busque el archivo descargado de datos exportados en la ubicación utilizada por el explorador para las descargas.

## Diseño de cuadrícula

La selección de columnas y su orden en la cuadrícula se pueden cambiar según sus preferencias y guardar como una _vista_. Puede controlar qué atributos se muestran en la cuadrícula en la configuración de atributos individuales. Si se muestran muchos atributos en la cuadrícula de productos, el tiempo de carga de los administradores y el rendimiento pueden verse afectados.

![Ordenar columnas de cuadrícula](./assets/admin-grid-columns.png){width="700" zoomable="yes"}

### Cambiar la selección de columnas

1. En la esquina superior derecha, haga clic en el control _Columns_ (![Columns control](../assets/icon-columns.png)).

1. Cambie las selecciones de columna:

   - Seleccione la casilla de verificación de cualquier columna que desee agregar a la cuadrícula.
   - Desactive la casilla de verificación de cualquier columna que desee quitar de la cuadrícula.
   - Para devolver la vista de cuadrícula predeterminada, haga clic en **[!UICONTROL Reset]**.

Asegúrese de desplazarse hacia abajo para ver todas las columnas disponibles.

### Mover una columna

1. Haga clic en el encabezado de la columna y mantenga presionado.

1. Arrastre la columna a la nueva posición y suéltela.

### Guardar una vista de cuadrícula

1. Haga clic en el control _Ver_ (![Ver control](../assets/icon-view-eye.png)).

1. Haga clic en **[!UICONTROL Save Current View]**.

1. Escriba **[!UICONTROL name]** para la vista.

1. Para guardar todos los cambios, haga clic en la _flecha_ (![Guardar todos los cambios](../assets/icon-arrow-save.png)).

   El nombre de la vista aparece ahora como la vista actual.

### Cambio de la vista de cuadrícula

1. Haga clic en el control _Ver_ (![Ver icono](../assets/icon-view-eye.png)).

1. Realice una de las siguientes acciones:

   - Para utilizar una vista diferente, haga clic en el nombre de la vista.
   - Para cambiar el nombre de una vista, haga clic en el icono _Editar_ (![Editar icono](../assets/icon-edit-pencil.png)) y actualice el nombre.
   - Para eliminar una vista, haz clic en el icono _Editar_ (![Editar icono](../assets/icon-edit-pencil.png)) y luego en el icono _Eliminar_ (![Eliminar icono](../assets/icon-delete-trashcan-solid.png)).
