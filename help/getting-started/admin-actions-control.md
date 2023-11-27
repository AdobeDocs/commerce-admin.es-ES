---
title: Control de acciones
description: Obtenga información sobre el uso del control Actions para aplicar una operación a uno o varios registros del administrador.
exl-id: 03f313a9-bc17-4151-a2c8-8906342f025d
source-git-commit: a3fb702d0b6e08c3aaaa0d6b5e07aa825026ef76
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# Control de acciones

Al trabajar con una colección de registros en la cuadrícula, puede utilizar el control Actions para aplicar una operación a uno o varios registros. El control Actions enumera cada operación que está disponible para el tipo específico de datos. Por ejemplo, puede utilizar el control Actions para actualizar los atributos de los productos seleccionados, para cambiar el estado de `Disabled` hasta `Enabled`o para eliminar registros de la base de datos.

Puede realizar tantos cambios como sea necesario y, a continuación, actualizar los registros en un solo paso. Es mucho más eficiente que cambiar la configuración individualmente para cada producto. La aplicación de ediciones a un lote de registros es una operación asincrónica, que se ejecuta en segundo plano para que pueda seguir trabajando en el administrador sin esperar a que finalice la operación. El sistema muestra un mensaje cuando se completa la tarea.

La selección de las acciones disponibles varía según la lista y podrían aparecer opciones adicionales, según la acción seleccionada. Por ejemplo, al cambiar el estado de un grupo de registros, una variable _[!UICONTROL Status]_aparece junto al control Actions con opciones adicionales.

## Paso 1: Selección de registros

La casilla de verificación de la primera columna de la lista identifica cada registro que es un objetivo para la acción. El [controles de filtro](admin-grid-controls.md) se puede utilizar para reducir la lista a los registros a los que desee destinar la acción.

1. Si es necesario, establezca los filtros en la parte superior de cada columna para mostrar solo los registros que desee incluir.

1. Seleccione la casilla de verificación de cada registro que sea un destino para la acción o utilice el selector de columnas para elegir una selección masiva.

![Seleccionar o anular la selección de todo o todo en la página](./assets/action-change-selection.png){width="500"}

## Paso 2: Aplicar una acción a los registros seleccionados

1. Configure las variables **[!UICONTROL Actions]** control a la operación que desea aplicar.

   **_Ejemplo:_** Actualizar atributos

   - En la lista, seleccione la casilla de verificación de cada registro que desea actualizar.

   - Configure las variables **[!UICONTROL Actions]** control a `Update Attributes`.

     ![Seleccione la acción Actualizar atributos](./assets/action-select.png){width="450"}

   - Haga clic **[!UICONTROL Submit]**.

     La página Actualizar atributos enumera todos los atributos disponibles, organizados por grupo, en el panel de la izquierda.

     ![Página Actualizar Atributos](./assets/action-update-attributes.png){width="700" zoomable="yes"}

   - Seleccione el **[!UICONTROL Change]** junto a cada atributo y realice los cambios necesarios.

   - Clic **[!UICONTROL Save]** para actualizar los atributos del grupo de registros seleccionados.

1. Cuando termine, haga clic en **[!UICONTROL Submit]**.

## Acciones de casilla de verificación

| Acción | Descripción |
|--- |--- |
| [!UICONTROL Select All] | Selecciona la casilla de verificación de todos los registros de la lista. |
| [!UICONTROL Unselect All] | Borra la casilla de verificación de todos los registros de la lista. |
| [!UICONTROL Select All on This Page] | Selecciona la casilla de verificación de los registros mostrados en la página actual. |
| [!UICONTROL Deselect All on This Page] | Borra la casilla de verificación de los registros mostrados en la página actual. |

{style="table-layout:auto"}
