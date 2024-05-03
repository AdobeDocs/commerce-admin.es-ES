---
title: Actualizaciones programadas de productos
description: Aprenda a programar cambios en las listas de productos para que sean compatibles con campañas y programas promocionales.
exl-id: ce1aebe6-9032-438d-b950-4b13116b8ed3
feature: Catalog Management, Products
source-git-commit: 3d04e7213d90bb4c323acce69ac31c1dbcb7ca49
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# Programar actualizaciones de productos

{{ee-feature}}

Las actualizaciones de productos se pueden aplicar según lo programado y agrupar con otros cambios de contenido. Puede utilizar [ensayo de contenido](../content-design/content-staging.md) para crear una campaña basada en cambios programados en el producto o aplicar los cambios a una campaña existente.

>[!NOTE]
>
>El [!UICONTROL Set Product as New From] y [!UICONTROL To] campos y [!UICONTROL Schedule Design Update] se han eliminado en ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce y no se pueden modificar directamente en el producto. Debe crear una actualización programada para estas activaciones.

>[!NOTE]
>
>Todas las actualizaciones programadas se aplican de forma consecutiva, lo que significa que cualquier entidad solo puede tener una actualización programada a la vez. Cualquier actualización programada se aplica a todas las vistas de la tienda dentro de su lapso de tiempo. Como resultado, una entidad no puede tener diferentes actualizaciones programadas para diferentes vistas de tienda al mismo tiempo. Todos los valores de atributo de entidad dentro de todas las vistas de tienda, que no se ven afectados por la actualización programada actual, se toman de los valores predeterminados y no de la actualización programada anterior.

>[!NOTE]
>
>Una previsualización de ensayo para una actualización programada siempre comienza desde el **predeterminado** la vista de tienda, que emula la experiencia del cliente al navegar por la campaña de actualización de ensayo.

## Creación de una actualización programada

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Seleccione un producto existente y haga clic en **[!UICONTROL Edit]**.

1. Clic **[!UICONTROL Schedule New Update]**.

1. Seleccionar **[!UICONTROL Save as a New Update]**.

1. Para **[!UICONTROL Update Name]**, introduzca un nombre para la nueva campaña de ensayo de contenido.

1. Escriba una descripción breve **[!UICONTROL Description]** de la actualización y cómo se va a utilizar.

1. Utilizar el calendario (![icono de calendario](../assets/icon-calendar.png)) para elegir la **[!UICONTROL Start Date]** y **[!UICONTROL End Date]** para la campaña.

   >[!NOTE]
   >
   >Campaign **[!UICONTROL Start Date]** y **[!UICONTROL End Date]** debe definirse utilizando la variable **_predeterminado_** Zona horaria del administrador, que se convierte a partir de la zona horaria local para cada sitio web. Por ejemplo, con varios sitios web en diferentes zonas horarias en los que desee iniciar una campaña en función de una zona horaria de EE. UU., debe programar una actualización independiente para cada zona horaria local. Establecer **[!UICONTROL Start Date]** y **[!UICONTROL End Date]** para cada, y se convierte de la zona horaria del sitio web local a la zona horaria de administración predeterminada.

   ![Programar como nueva actualización](./assets/product-schedule-as-new.png){width="600" zoomable="yes"}

1. Desplácese hacia abajo hasta _[!UICONTROL Price]_y haga clic en **[!UICONTROL Advanced Pricing]**.

1. Introduzca una **[!UICONTROL Special Price]** para el producto durante la campaña programada y haga clic en **[!UICONTROL Done]**.

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

## Asignar a una actualización existente

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Seleccione un producto existente y haga clic en **[!UICONTROL Edit]**.

1. Clic **[!UICONTROL Schedule New Update]**.

1. Seleccionar **[!UICONTROL Assign to Existing Campaign]**.

1. En la lista, seleccione la campaña que desea modificar.

   ![Asignación a una campaña existente](./assets/scheduled-changes-assign-to-existing-campaign.png){width="600" zoomable="yes"}

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

## Ver el cambio programado

El cambio programado aparece en la parte superior de la página del producto, con las fechas de inicio y finalización de la campaña.

![Cambio programado](./assets/view-product-scheduled-changes.png){width="600" zoomable="yes"}

## Editar el cambio programado

1. En el _[!UICONTROL Scheduled Changes]_en la parte superior de la página, haga clic en **[!UICONTROL View/Edit]**.

1. Realice los cambios necesarios en la actualización programada.

1. Clic **[!UICONTROL Save]**.

## Eliminar el cambio programado

1. En el _[!UICONTROL Scheduled Changes]_en la parte superior de la página, haga clic en **[!UICONTROL View/Edit]**.

1. En la barra superior, haga clic en **[!UICONTROL Remove from Update]**.

   ![Quitar cambio programado](./assets/remove-product-scheduled-changes.png){width="600" zoomable="yes"}

1. En el cuadro de diálogo, seleccione **[!UICONTROL Delete the Update]** y haga clic en **[!UICONTROL Done]**.

   >[!NOTE]
   >
   >El producto se elimina de la actualización y se pierden todos los cambios programados.

## Programar una actualización de diseño

{{ce-feature}}

El _[!UICONTROL Schedule Design Update]_le permite realizar cambios temporales en el aspecto de la página del producto. Puede programar cambios de diseño para una temporada, promoción o simplemente para hacer las cosas nuevas. Los cambios de diseño se pueden programar con antelación para que entren en vigor, o_ gotear _, en la programación definida.

![Actualización de diseño programada](./assets/product-design-update-scheduled-ce.png){width="600" zoomable="yes"}


| Campo | Descripción |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | Determina el intervalo de fechas en que se aplica un diseño personalizado al producto. |
| [!UICONTROL New Theme] | Aplica una temática personalizada al producto. |
| [!UICONTROL New Layout] | Aplica un diseño diferente a la página del producto. Opciones: <br/>**[!UICONTROL No layout updates]**: De forma predeterminada, las actualizaciones de diseño no están disponibles para la página del producto.<br/>**[!UICONTROL Empty]** : le permite definir su propio diseño, como una página de 4 columnas. (Requiere conocimientos de XML). <br/>**[!UICONTROL 1 column]**: aplica un diseño de una columna a la página del producto.<br/>**[!UICONTROL 2 columns with left bar]** : aplica un diseño de dos columnas con una barra lateral izquierda a la página del producto. <br/>**[!UICONTROL 2 columns with right bar]**: aplica un diseño de dos columnas con una barra lateral derecha a la página del producto.<br/>**[!UICONTROL 3 columns]** : aplica un diseño de tres columnas a la página del producto. |

{style="table-layout:auto"}
