---
title: Creación y actualización de eventos
description: Obtenga información sobre cómo crear un evento asociado a una categoría desde el catálogo.
exl-id: 6c9f6a33-6785-4c3a-add6-dc2a6b16ed88
feature: Marketing Tools, Promotions/Events
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 0%

---

# Creación y actualización de eventos

{{ee-feature}}

Cada evento se asocia a una categoría del catálogo y solo se puede asociar un evento a una categoría determinada a la vez. Para mostrar una lista de los próximos eventos en tu tienda, también debes configurar un widget de [Carrusel de eventos de catálogo](../content-design/widget-event-carousel.md).

![Lista de eventos](./assets/category-events.png){width="700" zoomable="yes"}

## Creación de un evento

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Catalog Event]**.

1. En el árbol de categorías, elija la categoría que desea asociar al evento.

   Dado que cada categoría solo puede tener un evento a la vez, las categorías que ya tengan un evento se desactivan.

   ![Nuevo evento - árbol de categorías](./assets/catalog-events-category-tree.png){width="500" zoomable="yes"}

1. Definir **[!UICONTROL Catalog Event Information]**:

   ![Información del evento del catálogo](./assets/catalog-event-information.png){width="700" zoomable="yes"}

   - Para el **[!UICONTROL Start Date]** del evento, usa el calendario (![icono de calendario](../assets/icon-calendar.png)) para elegir la fecha. Use los controles deslizantes **[!UICONTROL Hour]** y **[!UICONTROL Minute]** para establecer la hora en que comienza el evento.

   - Para el **[!UICONTROL End Date]** del evento, usa el calendario (![icono de calendario](../assets/icon-calendar.png)) para elegir la fecha. Use los controles deslizantes **[!UICONTROL Hour]** y **[!UICONTROL Minute]** para establecer la hora a la que finaliza el evento.

   - Para cargar un **[!UICONTROL Image]** para el widget de evento, haga clic en **[!UICONTROL Choose File]** y seleccione el archivo de imagen en el directorio.

   - En el campo **[!UICONTROL Sort Order]**, escriba un número para indicar la secuencia en la que aparece este evento cuando se enumera con otros eventos.

   - Seleccione la casilla de verificación de cada tipo de página en la que desee mostrar el ticker de cuenta atrás.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

## Eventos de actualización

Los eventos se pueden editar desde la página Eventos o desde la categoría asociada al evento. Cuando una categoría tiene un evento asociado, aparece un botón Editar evento en la esquina superior derecha.

### Método 1: Editar un evento desde la página Eventos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. Busque el evento en la lista y ábralo en modo de edición.

1. Realice los cambios necesarios en el evento.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

### Método 2: Edición de un evento desde una categoría

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. En el árbol de categorías de la izquierda, seleccione la categoría asociada al evento.

1. En la esquina superior derecha, haz clic en **[!UICONTROL Edit Even]t**.

1. Realice los cambios necesarios en el evento.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

## Eliminación de un evento

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. Busque el evento en la lista y ábralo en modo de edición.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Delete]**.

1. Para confirmar la acción, haga clic en **[!UICONTROL OK]**.

## Descripciones de campos

| Campo | [Ámbito](../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Category] | Global | Al crear un evento, este campo se vincula de nuevo al árbol de categorías. Al editar un evento, se vincula a la página de categoría relacionada con el evento. |
| [!UICONTROL Start Date] | Global | La fecha y hora de inicio del evento en formato `MMDDYYYY HH;MM`. Haga clic en el icono de calendario para seleccionar la fecha. |
| [!DNL End Date] | Global | La fecha y hora de finalización del evento en formato `MMDDYYYY HH;MM`. Haga clic en el icono de calendario para seleccionar la fecha. |
| [!UICONTROL Image] | Vista de tienda | Carga una imagen que aparece en el widget de carrusel de [eventos de catálogo](../content-design/widget-event-carousel.md). |
| [!UICONTROL Sort Order] | Global | Determina la secuencia en la que aparece este evento cuando se enumera con otros eventos. |
| [!UICONTROL Display Countdown Ticker On] | Global | Muestra el ticker de cuenta atrás en el encabezado de cada página especificada. Opciones: `Category Page` / `Product Page` |
| [!UICONTROL Status] | Global | Indica el estado del evento en función del intervalo de fechas de inicio y finalización. Status es un valor de solo lectura. Valores: `Open` / `Closed` / `Upcoming` |

{style="table-layout:auto"}

## Barra de botones

| Botón | Descripción |
|--- |--- |
| **[!UICONTROL Back]** | Vuelve a la página Eventos sin guardar el nuevo evento o los cambios en un evento existente. |
| **[!UICONTROL Delete]** | Elimina el evento. |
| **[!UICONTROL Reset]** | Borra la forma de los cambios no guardados y restaura la información del evento original. |
| **[!UICONTROL Save and Continue Edit]** | Guarda todos los cambios y mantiene el formulario abierto en el modo Edición. |
| **[!UICONTROL Save]** | Guarda los cambios, cierra el formulario y vuelve a la página Eventos. |

{style="table-layout:auto"}
