---
title: Panel de ensayo de contenido
description: Utilice el panel de ensayo de contenido para acceder a una descripción general de todas las campañas activas y próximas.
exl-id: 67c18c1c-94c3-4d89-ae1e-868a465431e3
feature: Page Content, Staging
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Panel de ensayo de contenido

{{ee-feature}}

El [!UICONTROL Content Staging] El panel proporciona una descripción general de todas las campañas activas y futuras. El formato del tablero se puede cambiar de una cuadrícula a una cronología. También puede utilizar filtros para buscar campañas, personalizar el diseño de la columna y guardar diferentes vistas de la cuadrícula. Para obtener más información sobre los controles del espacio de trabajo, vea [Admin Workspace](../getting-started/admin-workspace.md).

![Panel de ensayo en vista de cuadrícula](./assets/content-staging-grid-view.png){width="600" zoomable="yes"}

## Ver el panel de ensayo

1. En el _Administrador_ barra lateral, vaya a  **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**.

1. Para cambiar el formato del tablero, defina la variable **[!UICONTROL View As]** control a `list`, `Grid`, o `Timeline`.

   ![Vista Cronología](./assets/content-staging-dashboard-timeline.png){width="600" zoomable="yes"}

   Cuando se muestra la cronología, se puede utilizar el control deslizante de la esquina inferior derecha para ajustar la vista de una a cuatro semanas. Cada columna representa un día.

1. Si se muestra la cronología, arrastre el control deslizante hasta la `4w` situado en el extremo derecho para ver un intervalo de tiempo más largo.

   ![Vista de cuatro semanas](./assets/content-staging-timeline-4-week-view.png){width="600" zoomable="yes"}

1. Para mostrar información general sobre la campaña, haga clic en cualquier elemento de la página.

   - Para abrir la campaña, haga clic en **[!UICONTROL View/Edit]**.

   - Para ver el aspecto de la campaña para los clientes de la tienda ese día, haga clic en **[!UICONTROL Preview]**.

   ![Información de campaña](./assets/content-staging-campaign-info.png){width="600" zoomable="yes"}

## Descripciones de columnas del panel de ensayo

| Columna | Descripción |
|--- |--- |
| [!UICONTROL Status] | Estado de la campaña. `Active` o `Upcoming`. |
| [!UICONTROL Update Name] | Nombre de la campaña. |
| [!UICONTROL Includes] | Define cuántos objetos se incluyen en la campaña. |
| [!UICONTROL Start Time] | La fecha en la que comienza la campaña. |
| [!UICONTROL End Time] | La fecha en la que finaliza la campaña. |
| [!UICONTROL Description] | Descripción adicional de cada campaña. |
| [!UICONTROL Action] | Las acciones que se pueden aplicar a un registro individual incluyen:<br/>**[!UICONTROL View/Edit]**: abre la campaña en modo de edición.<br/>**[!UICONTROL Preview]** - Muestra la campaña en modo de vista previa. |

{style="table-layout:auto"}

## Edición de una campaña

Los objetos de campaña existentes se pueden editar desde el panel de ensayo, excepto para las campañas de reglas de precios que no tienen fechas de finalización.

>[!NOTE]
>
>Si una campaña que incluye una regla de precio se crea inicialmente sin una fecha de finalización, la campaña no se puede editar más adelante para incluir una fecha de finalización. En tal caso, es necesario crear una campaña duplicada e introducir la fecha de finalización que sea necesaria.

![Detalles de campaña](./assets/content-staging-dashboard-view-edit.png){width="600" zoomable="yes"}

La campaña de este ejemplo incluye dos categorías y tres productos individuales.

Siga los pasos a continuación para editar cualquiera de los objetos de esta campaña.

1. En el _Administrador_ barra lateral, vaya a  **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**.

1. Busque la campaña en la lista mostrada o la cronología y ábrala para acceder a los detalles:

   - Para ver una lista, haga clic en **[!UICONTROL Select]** y luego **[!UICONTROL View/Edit]** en el _[!UICONTROL Action]_columna.
   - Para mostrar una cronología, haga clic una vez para mostrar el resumen y, a continuación, haga clic en **[!UICONTROL View/Edit]**.

1. Actualice cualquiera de los ajustes de la _[!UICONTROL General]_según sea necesario.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) cualquier sección que contenga un elemento que se va a editar.

   ![Actualización de los productos asignados para un elemento de campaña](./assets/content-staging-campaign-edit-products.png){width="600" zoomable="yes"}

1. Haga clic **[!UICONTROL Save]**.
