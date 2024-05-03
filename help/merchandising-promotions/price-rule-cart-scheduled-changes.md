---
title: Cambios programados para reglas de precios del carro de compras
description: Aprenda a aplicar reglas de precios del carro de compras según lo programado como parte de una campaña y agrupadas con otros cambios de contenido.
exl-id: 4c9caa04-1e11-440d-b3db-7cc5fc83a08f
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 3d04e7213d90bb4c323acce69ac31c1dbcb7ca49
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---

# Cambios programados para reglas de precios del carro de compras

{{ee-feature}}

Las reglas de precios del carro de compras se pueden aplicar según lo programado como parte de una campaña y agruparse con otros cambios de contenido. Puede crear una campaña basada en cambios programados de una regla de precios o aplicar los cambios a una campaña existente.

>[!NOTE]
>
>El [!UICONTROL From] y [!UICONTROL To] Se han eliminado campos en ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce y no se pueden modificar directamente en la regla de precios del carro de compras. Debe crear una actualización programada para estas activaciones.

![Reglas de precios del carro de compras: cambios programados](./assets/content-staging-price-rules-cart-scheduled-changes.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Todas las actualizaciones programadas se aplican de forma consecutiva. Esto significa que cualquier entidad solo puede tener una actualización programada en un momento dado. Cualquier actualización programada se aplica a todas las vistas de la tienda dentro de su lapso de tiempo. Como resultado, una entidad no puede tener diferentes actualizaciones programadas para diferentes vistas de tienda al mismo tiempo. Todos los valores de atributo de entidad dentro de todas las vistas de tienda, que no se ven afectados por la actualización programada actual, se toman de los valores predeterminados y no de la actualización programada anterior.

Si se ejecutan varias reglas de precios en la misma campaña, la variable _[!UICONTROL Priority]_la configuración de la regla de precio determina qué regla tiene prioridad. Para obtener más información, consulte [Ensayo de contenido](../content-design/content-staging.md).

Tenga en cuenta las siguientes advertencias:

- Si una campaña que incluye una regla de precio se crea inicialmente sin una fecha de finalización, la campaña no se puede editar posteriormente para incluir una fecha de finalización. Se recomienda añadir una fecha de finalización al crear la campaña o crear una versión duplicada de la campaña existente y añadir la fecha de finalización al duplicado según sea necesario.
- Cuando utilice una actualización programada para habilitar una regla de precio del carro de compras con una fecha de finalización, asegúrese de establecer la regla como deshabilitada inicialmente. Las reglas que ya están activas no respetan la fecha de finalización.
- Los cupones no están conectados a las reglas de precios del carro de compras. Una actualización programada no proporciona acceso al _[!UICONTROL Coupon]_,_[!UICONTROL Coupon Code]_, _[!UICONTROL Uses per Coupon]_, y_[!UICONTROL Uses per Customer]_ campos en la _[!UICONTROL Rule Information]_pestaña. Además, todos los ajustes de la_[!UICONTROL Manage Coupon Codes]_ no están disponibles.

>[!IMPORTANT]
>
>Campaign **[!UICONTROL Start Date]** y **[!UICONTROL End Date]** debe definirse utilizando la variable **_predeterminado_** Zona horaria del administrador, que se convierte a partir de la zona horaria local de cada sitio web. Imagine un ejemplo en el que tiene varios sitios web en diferentes zonas horarias, pero quiere iniciar una campaña en función de una zona horaria de EE. UU. En este caso, debe programar una actualización independiente para cada zona horaria local y establecer **[!UICONTROL Start Date]** y **[!UICONTROL End Date]** se convierte de cada zona horaria del sitio web local a la zona horaria de administración predeterminada.
