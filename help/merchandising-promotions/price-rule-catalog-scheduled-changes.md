---
title: Cambios programados para reglas de precios de catálogo
description: Aprenda a aplicar reglas de precios de catálogo según lo programado como parte de una campaña y agrupadas con otros cambios de contenido.
exl-id: ec4b915f-0a27-438d-b1b0-f1bcd297af6d
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 11f8fcba70491f9dcb6c20d14b406fba4b14cab4
workflow-type: tm+mt
source-wordcount: '832'
ht-degree: 0%

---

# Cambios programados para reglas de precios de catálogo

{{ee-feature}}

La casilla Cambios programados aparece en la parte superior de la página cuando se guarda o actualiza una nueva regla de precios. Las reglas de precios de catálogo se pueden aplicar según lo programado como parte de una campaña y agruparse con otros cambios de contenido. Puede crear una campaña basada en cambios programados de una regla de precios o aplicar los cambios a una campaña existente.

>[!NOTE]
>
>Los campos [!UICONTROL From] y [!UICONTROL To] se han eliminado en ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce y no se pueden modificar directamente en la regla de precios del catálogo. Debe crear una actualización programada para estas activaciones.

>[!NOTE]
>
>Todas las actualizaciones programadas se aplican de forma consecutiva. Esto significa que cualquier entidad solo puede tener una actualización programada en un momento dado. Cualquier actualización programada se aplica a todas las vistas de la tienda dentro de su lapso de tiempo. Como resultado, una entidad no puede tener diferentes actualizaciones programadas para diferentes vistas de tienda al mismo tiempo. Todos los valores de atributo de entidad dentro de todas las vistas de tienda, que no se ven afectados por la actualización programada actual, se toman de los valores predeterminados y no de la actualización programada anterior.

Si se ejecutan varias reglas de precios en la misma campaña, la configuración Prioridad de la regla de precios determina qué regla tiene prioridad. Para obtener más información, consulte [Ensayo de contenido](../content-design/content-staging.md).

>[!IMPORTANT]
>
>Si inicialmente se crea una campaña activa sin una fecha de finalización, la campaña no se puede editar más adelante para incluir una fecha de finalización. En tal caso, es necesario crear una campaña duplicada e introducir la fecha de finalización que sea necesaria.

![Regla de precios de catálogo - cambios programados](./assets/price-rule-catalog-scheduled.png){width="600" zoomable="yes"}

## Programar una actualización a una regla de precios de catálogo

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**Regla de precio de catálogo**.

1. Abra la regla en modo de edición.

1. En el cuadro **[!UICONTROL Scheduled Changes]** de la parte superior de la página, haga clic en **[!UICONTROL Schedule New Update]**.

1. Con la opción **[!UICONTROL Save as a New Update]** seleccionada, haga lo siguiente:

   - Para **[!UICONTROL Update Name]**, escriba un nombre para la actualización de la regla.

   - Escriba un breve **[!UICONTROL Description]** de la actualización, incluyendo cómo o por qué se aplica.

   - Use el _Calendario_ (![Icono del calendario](../assets/icon-calendar.png)) para elegir **[!DNL Start Date]** y **[!UICONTROL End Date]** para que el cambio programado entre en vigencia. Para crear un cambio abierto, deje en blanco la fecha de finalización.

   ![Reglas de precios de catálogo: nuevos cambios programados](./assets/price-rule-catalog-schedule-update.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >La fecha y la hora de inicio y finalización están determinadas por la fecha y la zona horaria predeterminadas del panel de administración, no por la zona horaria de un sitio web en particular. Tenga en cuenta la zona horaria del sitio web para determinar correctamente las horas de inicio y finalización. Cree reglas independientes para sitios web en diferentes zonas horarias que necesiten iniciarse o detenerse en horas locales específicas.

1. Desplácese hacia abajo hasta la sección **[!UICONTROL Rule Information]** y cambie la regla según sea necesario.

   Puede programar cambios para cualquier parámetro de regla, incluidos los sitios web (ámbito)/grupos de clientes para la regla, las condiciones de la regla y las acciones aplicadas por la regla. Para obtener más información, consulte [Creación de una regla de precio de catálogo](price-rules-catalog-create.md).

   >[!NOTE]
   >
   >Si cambia a cualquiera de los parámetros de información de regla, asegúrese de que _[!UICONTROL Status]_está configurado correctamente. Si desea que el cambio genere una regla aplicada activamente, el estado debe ser `Active`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

   El cambio programado aparece en la parte superior de la página, con las fechas de inicio y finalización de la campaña.

## Editar un cambio de regla programado

1. En el cuadro **[!UICONTROL Scheduled Changes]** de la parte superior de la página, haga clic en **[!UICONTROL View/Edit]**.

1. Realice los cambios necesarios en la actualización programada.

   >[!NOTE]
   >
   >Si una campaña está vinculada a más de una regla de precios de catálogo, la campaña solo se puede editar desde el [Panel de ensayo de contenido](../content-design/content-staging-dashboard.md).

1. Haga clic en **[!UICONTROL Save]**.

## Previsualizar el cambio de regla programado

1. En el cuadro **[!UICONTROL Scheduled Changes]** de la parte superior de la página, haga clic en **[!UICONTROL Preview]**.

   La vista previa abre una nueva pestaña del explorador que carga la tienda con el cambio programado aplicado. Vaya a un producto afectado por el cambio.

   ![Previsualizar cambio programado](./assets/price-rule-catalog-scheduled-update-preview.png){width="600" zoomable="yes"}

1. En la esquina superior izquierda de la ventana Vista previa, haga clic en **[!UICONTROL Calendar]**.

   El detalle del calendario muestra otras campañas programadas para el mismo día. Cada registro de la lista es una actualización de regla independiente.

   ![Lista de actualizaciones programadas para una fecha específica](./assets/price-rule-catalog-scheduled-preview-calendar.png){width="600" zoomable="yes"}

1. Para obtener una vista previa de un día u hora diferente, haga clic en el ![icono del calendario](../assets/icon-calendar.png) de **[!UICONTROL Date & Time]** y haga lo siguiente:

   - Elija una fecha u hora diferente.

   - Haga clic en **[!UICONTROL Preview]**.

1. Para volver al calendario, haga clic en **[!UICONTROL Calendar]** en el encabezado de la página Vista previa.

   Desde aquí, puede hacer lo siguiente:

   **Compartir un vínculo a la vista previa**

   Para compartir un vínculo a la vista previa de la tienda con sus compañeros, haga clic en **[!UICONTROL Share]**. Copie el vínculo al portapapeles y péguelo en el cuerpo de un mensaje de correo electrónico.

   >[!NOTE]
   >
   >Se requiere una cuenta de usuario administrador para ver una vista previa compartida. Si la función [tiene acceso](../systems/permissions-user-roles.md) para crear una cuenta de usuario administrador, debe crear la cuenta para un nuevo usuario antes de compartir.

   **Cambiar el ámbito de la vista previa**

   Para ver los cambios programados para diferentes vistas de la tienda, haga clic en **[!UICONTROL Scope]** en el encabezado de la página Vista previa. Elija el sitio web, la tienda o la vista de la tienda que desea previsualizar.

1. Si es necesario, vuelva al calendario y haga clic en **[!UICONTROL View/Edit]** en la columna _[!UICONTROL Action]_para abrir otra actualización programada.
