---
title: Programar una actualización de contenido
description: Revise este ejemplo de campaña utilizado para programar un cambio temporal de precio para un producto.
exl-id: 36b7d7f6-4590-4192-a82b-e5f645b05f62
feature: Page Content, Staging
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 07d7ca7e7f6af42fe8e06dc3c49c2df5f50d1425
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 0%

---

# Programar una actualización de contenido

{{ee-feature}}

El siguiente ejemplo muestra cómo programar un cambio de precio temporal para un producto. Incluye la programación y previsualización de cambios, así como la visualización de actualizaciones programadas en el calendario. Aunque este ejemplo incluye un solo cambio, una campaña puede incluir varios cambios en productos, reglas de precios, páginas de CMS y otras entidades programadas para realizarse al mismo tiempo. Siga un método similar para especificar las fechas de inicio y finalización para el atributo [!UICONTROL Set Product As New].

>[!NOTE]
>Debe crear una actualización programada para especificar una fecha de inicio (y finalización) para [!UICONTROL Set Product As New]. Para [!UICONTROL Special Price] y [!UICONTROL Design Change], los campos desde/hasta la fecha se eliminan de Adobe Commerce y solo están disponibles en Magento Open Source.
>
>Todas las actualizaciones programadas se aplican de forma consecutiva, lo que significa que cualquier entidad solo puede tener una actualización programada a la vez. Cualquier actualización programada se aplica a todas las vistas de la tienda dentro de su lapso de tiempo. Como resultado, una entidad no puede tener una actualización programada diferente para diferentes vistas de tienda al mismo tiempo. Todos los valores de atributo de entidad dentro de todas las vistas de tienda, que no se ven afectados por la actualización programada actual, se toman de los valores predeterminados y no de la actualización programada anterior.

## Programar una actualización de un producto

1. En la cuadrícula _[!UICONTROL Products]_, abra un producto en modo de edición.

1. En el cuadro _[!UICONTROL Scheduled Changes]_&#x200B;de la parte superior de la página, haga clic en **[!UICONTROL Schedule New Update]**.

   ![Programar nueva actualización](./assets/content-staging-product-schedule-new-update.png){width="600" zoomable="yes"}

1. Con la opción **[!UICONTROL Save as a New Update]** seleccionada, establezca los parámetros básicos para la actualización:

   - Para **[!UICONTROL Update Name]**, escriba un nombre para la nueva campaña de ensayo de contenido.

   - Escriba un breve **[!UICONTROL Description]** de la actualización y cómo se va a usar.

   - Use la herramienta Calendario (![Icono de calendario](../assets/icon-calendar.png)) para elegir las fechas de inicio **3&rbrace; y de finalización** 5&rbrace; para la campaña.**&#x200B;**

     Para crear una campaña abierta, no especifique una fecha de finalización (déjela en blanco). Para este ejemplo, la campaña está programada para comenzar a medianoche del 1 de enero de 2021 a las 12:00 AM PST.


     Para una campaña de regla de precios creada sin una fecha de finalización, no se puede añadir una fecha de finalización más tarde. En tal caso, es necesario crear una campaña y establecer la fecha de inicio en la fecha en la que desea que finalice la campaña antigua y comience la nueva. En esa fecha de inicio, la campaña antigua finaliza y la nueva comienza según se ha definido.

     ![Programando una actualización de producto](./assets/content-staging-campaign-schedule-update.png){width="600" zoomable="yes"}

     >[!NOTE]
     >
     >La fecha de inicio y finalización de la campaña deben definirse usando la zona horaria del administrador **_default_**, que se convierte a partir de la zona horaria local de cada sitio web. Por ejemplo, cuando tiene varios sitios web en diferentes zonas horarias pero quiere iniciar una campaña basada en una zona horaria de EE. UU. (predeterminada), debe programar una actualización independiente para cada zona horaria local. En este caso, establezca **[!UICONTROL Start Date]** y **[!UICONTROL End Date]** como convertidos desde cada zona horaria del sitio web local a la zona horaria de administración predeterminada.

1. Desplácese hasta _[!UICONTROL Price]_&#x200B;y haga clic en **[!UICONTROL Advanced Pricing]**.

1. Escriba un **[!UICONTROL Special Price]** para el producto durante la campaña programada y haga clic en **[!UICONTROL Done]**.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

   El cambio programado aparece en la parte superior de la página del producto, con las fechas de inicio y finalización de la campaña.

   ![Cambio programado](./assets/content-staging-product-scheduled-update-preview-rope.png){width="600" zoomable="yes"}

## Editar el cambio programado

1. En el cuadro _Cambios programados_ de la parte superior de la página, haga clic en **[!UICONTROL View/Edit]**.

1. Realice los cambios necesarios en la actualización programada.

1. Haga clic en **[!UICONTROL Save]**.

## Previsualización del cambio programado

En el cuadro _Cambios programados_ de la parte superior de la página, haga clic en **[!UICONTROL Preview]**.

La vista previa abre una nueva pestaña del explorador y muestra cómo aparece el producto durante la campaña programada.

>[!NOTE]
>
>Una vista previa de ensayo para una actualización programada siempre comienza desde la vista de tienda **default**, que emula la experiencia del cliente al navegar por la campaña de actualización de ensayo.

Para obtener más información sobre cómo usar las herramientas de contenido de vista previa para cambiar la fecha y el ámbito de la vista previa, consulte [Vista previa de una campaña](content-staging-preview.md). También puede compartir un vínculo a la vista previa de la tienda con sus compañeros.
