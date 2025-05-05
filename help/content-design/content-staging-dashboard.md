---
title: Panel de ensayo de contenido
description: Utilice el panel de ensayo de contenido para acceder a una descripción general de todas las campañas activas y próximas.
exl-id: 67c18c1c-94c3-4d89-ae1e-868a465431e3
feature: Page Content, Staging
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 07d7ca7e7f6af42fe8e06dc3c49c2df5f50d1425
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# Panel de ensayo de contenido

{{ee-feature}}

El panel [!UICONTROL Content Staging] proporciona información general sobre todas las campañas activas y futuras. El formato del tablero se puede cambiar de una cuadrícula a una cronología. También puede utilizar filtros para buscar campañas, personalizar el diseño de la columna y guardar diferentes vistas de la cuadrícula. Para obtener más información acerca de los controles del área de trabajo, vea [Área de trabajo de administración](../getting-started/admin-workspace.md).

![Panel de ensayo en la vista de cuadrícula](./assets/content-staging-grid-view.png){width="600" zoomable="yes"}

## Ver el panel de ensayo

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**.

1. Para cambiar el formato del tablero, establezca el control **[!UICONTROL View As]** en `list`, `Grid` o `Timeline`.

   ![Vista de escala de tiempo](./assets/content-staging-dashboard-timeline.png){width="600" zoomable="yes"}

   Cuando se muestra la cronología, se puede utilizar el control deslizante de la esquina inferior derecha para ajustar la vista de una a cuatro semanas. Cada columna representa un día.

1. Si se muestra la cronología, arrastre el control deslizante a la posición `4w`, en el extremo derecho, para ver un período de tiempo más largo.

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
| [!UICONTROL Action] | Las acciones que se pueden aplicar a un registro individual incluyen:<br/>**[!UICONTROL View/Edit]**- Abre la campaña en modo de edición.<br/>**[!UICONTROL Preview]** - Muestra la campaña en modo de vista previa. |

{style="table-layout:auto"}

## Edición de una campaña

Los objetos de campaña existentes se pueden editar desde el panel de ensayo, excepto para las campañas de reglas de precios que no tienen fechas de finalización.

>[!NOTE]
>
>Si inicialmente se crea una campaña activa sin una fecha de finalización, la campaña no se puede editar más adelante para incluir una fecha de finalización. En tal caso, es necesario crear una campaña duplicada e introducir la fecha de finalización que sea necesaria.

![Detalles de campaña](./assets/content-staging-dashboard-view-edit.png){width="600" zoomable="yes"}

La campaña de este ejemplo incluye dos categorías y tres productos individuales.

Siga los pasos a continuación para editar cualquiera de los objetos de esta campaña.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**.

1. Busque la campaña en la lista mostrada o la cronología y ábrala para acceder a los detalles:

   - Para ver una lista, haga clic en **[!UICONTROL Select]** y luego en **[!UICONTROL View/Edit]** en la columna _[!UICONTROL Action]_.
   - Para una visualización de la cronología, haga clic una vez para mostrar el resumen y luego haga clic en **[!UICONTROL View/Edit]**.

1. Actualice la configuración de la sección _[!UICONTROL General]_&#x200B;según sea necesario.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) cualquier sección que contenga un elemento que se va a editar.

   ![Actualizando los productos asignados para un elemento de campaña](./assets/content-staging-campaign-edit-products.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save]**.
