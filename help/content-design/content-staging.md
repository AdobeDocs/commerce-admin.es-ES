---
title: Ensayo de contenido
description: El ensayo de contenido permite a su equipo empresarial crear, previsualizar y programar fácilmente una amplia gama de actualizaciones de contenido para su tienda, directamente desde el administrador.
exl-id: 929cd020-cbc7-40bf-a22c-02df35212ecf
feature: Page Content, Staging
source-git-commit: 3d04e7213d90bb4c323acce69ac31c1dbcb7ca49
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---

# Ensayo de contenido

{{ee-feature}}

El ensayo de contenido ofrece a tu equipo empresarial la capacidad de crear, previsualizar y programar fácilmente una amplia gama de actualizaciones de contenido para tu tienda directamente desde _Admin_. Por ejemplo, en lugar de pensar en términos de una página estática, considere una página como una colección de elementos diferentes que se pueden activar _en_ o desactivar _en función de una programación._ Puede utilizar el ensayo de contenido para crear una página que cambie automáticamente a lo largo del año según una programación.

El término _campaign_ hace referencia al registro de un cambio programado o a una colección de cambios que se administran desde el panel de ensayo. Los cambios pueden verse en un calendario o una cronología. Los términos _cambio programado_ y _actualización programada_ son intercambiables y hacen referencia a un solo cambio.

Cuando se programa un cambio de contenido para un período de tiempo específico, el contenido vuelve a la versión anterior cuando caduca el cambio programado. Puede crear varias versiones del mismo contenido de línea base para utilizarlas en futuras actualizaciones. También puede retroceder por la cronología para ver las versiones anteriores del contenido. Para guardar una versión de borrador, simplemente asigne una fecha en la cronología que esté tan lejos en el futuro que nunca entre en producción.

>[!NOTE]
>
>Los campos relacionados con la fecha de inicio y la fecha de finalización se han eliminado en ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce y no se pueden modificar directamente en la regla de precios del carro de compras, la regla de precios del catálogo, el producto, la categoría y la página de CMS. Debe crear una actualización programada para estas activaciones.

## Objetos y campañas de ensayo de contenido

Cuando se crea una nueva actualización programada para cualquiera de los siguientes objetos, se crea una campaña correspondiente como marcador de posición y aparece el cuadro _[!UICONTROL Scheduled Changes]_en la parte superior de la página. La campaña de marcador de posición tiene una fecha de inicio, pero no una fecha de finalización. Puede programar actualizaciones del contenido como parte de una campaña y, a continuación, previsualizar y compartir los cambios por fecha, hora o vista de tienda. Después de crear una nueva campaña para un objeto, puede asignarlo como una actualización programada para otros objetos.

- [Productos](../catalog/product-scheduled-changes.md)
- [Categorías](../catalog/category-scheduled-changes.md)
- [Reglas de precio de catálogo](../merchandising-promotions/price-rule-catalog-scheduled-changes.md)
- [Reglas de precio de carrito](../merchandising-promotions/price-rule-cart-scheduled-changes.md)
- [Páginas de CMS](pages-workspace.md#scheduled-changes)
- [Bloques de CMS](blocks.md)

## Flujo de trabajo de contenido

1. **Crear contenido de línea base**

   La línea de base es el contenido de un recurso sin campaña e incluye todo lo que hay debajo de la sección _[!UICONTROL Scheduled Changes]_en la parte superior de la página. El contenido de línea de base siempre se utiliza, a menos que haya una campaña activa con cambios programados para ese lugar en la cronología.

1. **Crear la primera campaña**

   Cree su primera campaña con las fechas de inicio y finalización según sea necesario. Para que la campaña sea abierta, deje la fecha de finalización en blanco. Cuando finaliza la primera campaña, se restaura el contenido de línea de base original.

   >[!NOTE]
   >
   >La fecha de inicio y la fecha de finalización de la campaña deben definirse usando la zona horaria del administrador **_default_**, que se convierte a partir de la zona horaria local de cada sitio web. Pongamos un ejemplo en el que tiene varios sitios web en diferentes zonas horarias, pero quiere iniciar una campaña basada en una zona horaria de EE. UU. En este caso, debe programar una actualización independiente para cada zona horaria local y establecer **[!UICONTROL Start Date]** y **[!UICONTROL End Date]** en convertidas desde cada zona horaria de sitio web local a la zona horaria de administración predeterminada.

1. **Agregar una segunda campaña**

   Cree la segunda campaña, con las fechas de inicio y finalización según sea necesario. La segunda campaña se puede asignar a un periodo de tiempo completamente diferente. Al crear varias campañas para el mismo recurso, las campañas no se pueden superponer. Puede crear tantas campañas como sea necesario.

   >[!NOTE]
   >
   >Todas las actualizaciones programadas se aplican de forma consecutiva, lo que significa que cualquier entidad solo puede tener una actualización programada a la vez. Cualquier actualización programada se aplica a todas las vistas de la tienda dentro de su lapso de tiempo. Como resultado, una entidad no puede tener una actualización programada diferente para diferentes vistas de tienda al mismo tiempo. Todos los valores de atributo de entidad dentro de todas las vistas de tienda, que no se ven afectados por la actualización programada actual, se toman de los valores predeterminados y no de la actualización programada anterior.

1. **Restaurar el contenido de línea base**

   Si todas las campañas tienen fechas de finalización, el contenido de línea de base se restaura cada vez que finalizan todas las campañas activas.

>[!NOTE]
>
>Mientras que una actualización de ensayo está activa para una entidad, al editar la entidad se está editando la actualización de ensayo activa actual. No afecta al contenido de línea de base, que se restaura cuando finaliza la actualización de ensayo.

## [!UICONTROL Content Staging] panel

El [!UICONTROL Content Staging] [panel](content-staging-dashboard.md) proporciona visibilidad sobre todos los cambios y actualizaciones del sitio planeados. Cualquier día, intervalo de fechas o período de tiempo de una campaña se puede previsualizar y compartir con otros.

![Panel de ensayo](./assets/content-staging-dashboard-grid.png){width="600" zoomable="yes"}

## Demostración de ensayo de contenido

Para obtener más información sobre el ensayo de contenido, vea este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/343784?quality=12)

## Solución de problemas de recursos

Para obtener ayuda con la resolución de problemas de ensayo de contenido, consulte los siguientes [!DNL Commerce] artículos de la Base de conocimiento de asistencia técnica:

- [Error 404 en todas las páginas debido a un problema de ensayo de contenido](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/site-down-or-unresponsive/error-404-on-all-pages-due-to-content-staging-issue.html)
- [Las actualizaciones programadas de ensayo de contenido no se muestran con la caché de Fastly obsoleta](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/scheduled-content-staging-updates-not-displayed-with-stale-fastly-cache.html)
- [¿Puedo programar actualizaciones de ensayo de contenido para los precios de un catálogo compartido?](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/faq/can-i-schedule-content-staging-updates-for-prices-in-a-shared-catalog.html)
