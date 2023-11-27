---
title: Cambios programados para categorías
description: Aprenda a programar cambios de categoría para admitir campañas de marketing y promociones de tiendas.
exl-id: 9e25082f-4e76-4148-b76e-dca0b14971eb
feature: Catalog Management, Categories
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# Cambios programados para categorías

{{ee-feature}}

Las actualizaciones de categoría se pueden aplicar según lo programado y agrupar con otros cambios de contenido. Puede crear una campaña basada en los cambios programados en la categoría o aplicar los cambios a una campaña existente. Para obtener más información, consulte [Ensayo de contenido](../content-design/content-staging.md).

>[!NOTE]
>
>Todas las actualizaciones programadas se aplican de forma consecutiva, lo que significa que cualquier entidad solo puede tener una actualización programada a la vez. Cualquier actualización programada se aplica a todas las vistas de la tienda dentro de su lapso de tiempo. Como resultado, una entidad no puede tener varias actualizaciones programadas para diferentes vistas de tienda al mismo tiempo. Todos los valores de atributo de entidad dentro de todas las vistas de tienda, que no se ven afectados por la actualización programada actual, se toman de los valores predeterminados y no de la actualización programada anterior.

## Programar una actualización a una categoría

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. En el árbol de categorías de la izquierda, elija la categoría que desea modificar.

1. En el _Cambios programados_ en la parte superior de la página, haga clic en **[!UICONTROL Schedule New Update]**.

   ![Cambios programados](./assets/category-scheduled-changes.png){width="600" zoomable="yes"}

1. Con el **[!UICONTROL Save as a New Update]** opción seleccionada, establezca los parámetros básicos para la actualización:

   - Para **[!UICONTROL Update Name]**, introduzca un nombre para la nueva campaña de ensayo de contenido.

   - Escriba una descripción breve **[!UICONTROL Description]** de la actualización y cómo se va a utilizar.

   - Utilizar el calendario ( ![Icono de calendario](../assets/icon-calendar.png) ) para elegir la **[!UICONTROL Start Date]** y **[!UICONTROL End Date]** para la campaña.

   >[!IMPORTANT]
   >
   >Campaign **[!UICONTROL Start Date]** y **[!UICONTROL End Date]** debe definirse utilizando la variable **_predeterminado_** Zona horaria de administración, que se convierte a partir de la zona horaria local de cada sitio web. Por ejemplo, con varios sitios web en diferentes zonas horarias en los que desee iniciar una campaña en función de una zona horaria de EE. UU., debe programar una actualización independiente para cada zona horaria local. Usted establece el **[!UICONTROL Start Date]** y **[!UICONTROL End Date]** para cada, que se convierte de la zona horaria del sitio web local a la zona horaria del administrador predeterminada.

   ![Cambios programados](./assets/category-scheduled-changes-new-update.png){width="600" zoomable="yes"}

1. Realice los cambios necesarios en la actualización programada.

1. Para previsualizar los cambios, haga clic en **[!UICONTROL Preview]** en la barra de botones superior derecha.

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

## Asignar a una actualización existente

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. En el árbol de categorías de la izquierda, elija la categoría que desea modificar.

1. En el _Cambios programados_ en la parte superior de la página, haga clic en **[!UICONTROL Schedule New Update]**.

1. Seleccionar **[!UICONTROL Assign to Existing Campaign]**.

1. En la lista, busque la campaña necesaria y haga clic en **[!UICONTROL Select]**.

1. Realice los cambios necesarios en la actualización programada.

1. Cuando termine, haga clic en **[!UICONTROL Save]**.
