---
title: Ventas privadas y eventos
description: Aprenda a utilizar ventas privadas y otros eventos de catálogo para aumentar las ventas a su base de clientes existente y generar rumores y nuevos posibles clientes.
exl-id: 0b890463-b1e5-4327-8d8a-372afd53312a
feature: Reporting, Promotions/Events
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---

# Ventas privadas y eventos

{{ee-feature}}

Las ventas privadas y otros eventos de catálogo son una buena manera de usar su base de clientes existente para generar rumores y nuevos clientes potenciales, o para descargar el inventario excedente. Puede crear ventas por tiempo limitado, limitar las ventas a miembros específicos o crear una página de venta privada independiente. También puede definir invitaciones y detalles del evento. Aumente la lealtad de su marca y genere sensación al ofrecer a sus mejores clientes el tratamiento VIP. Ofrezca acceso exclusivo a las ventas privadas o a las ventas de los miembros únicamente para aumentar la lealtad de la marca. También puede utilizar estas ventas para liquidar el exceso de mercancía. Los grupos de clientes son útiles para configurar estos tipos de miembros únicamente y las ventas de VIP.

![Ejemplo de tienda: evento en la página principal](./assets/storefront-event-home-page.png){width="700" zoomable="yes"}

## Componentes de administración de eventos

- **Categorías** - Cada evento está asociado con una [categoría](../catalog/category-create.md) de su catálogo.

- **Eventos**: las ventas de eventos se basan en una fecha de inicio y de finalización. Puede usar un [ticker de cuenta atrás](#event-ticker) para mostrar el tiempo restante.

- **Carrusel de eventos de catálogo**: cuando el widget [Evento de catálogo](../content-design/widget-event-carousel.md) está habilitado en la configuración, se puede colocar en páginas de tienda como un listado de eventos abiertos y próximos, ordenados por fecha de finalización. Si dos o más eventos tienen la misma fecha de finalización, los eventos se ordenan según el orden especificado en la configuración.

- **[!UICONTROL Websites]**: los permisos de categoría se basan principalmente en [grupos de clientes](../customers/customer-groups.md).

- **Permisos de categoría** - [Permisos de categoría](../catalog/category-permissions.md) le proporciona control total sobre las actividades específicas que pueden tener lugar en una categoría determinada.

- **Restricciones de acceso**: impide que el público [acceda](event-configure.md#restrict-access) al sitio al redirigir a una página de aterrizaje, una página de inicio de sesión o una página de registro.

- **Invitaciones**: los mensajes de correo electrónico se envían con un vínculo para crear una cuenta en la tienda. Puede restringir la capacidad de crear una cuenta solamente a aquellos que reciban una [invitación](invitations.md).

- **Informes de ventas privados** - Los [Informes de ventas privados](../getting-started/private-sales-reports.md) proporcionan información sobre invitaciones enviadas, clientes invitados y conversiones.

## Marcador de evento

El bloque ticker muestra un ticker de cuenta atrás para los eventos abiertos, con las fechas de inicio y finalización de los próximos eventos. Si un evento se ha cerrado, el valor muestra las fechas de inicio y finalización.

![Ejemplo de tienda - carrusel de eventos](./assets/storefront-event-ticker-carousel.png){width="700" zoomable="yes"}

Si el marcador de página de categoría está habilitado para un evento, el bloque de marcador aparece en la parte superior de la lista de categorías. Si el marcador de página de producto está activado, el bloque de marcador también aparece en la parte superior de la página de producto de cualquier producto asociado a la categoría.

El marcador de eventos se puede habilitar al [crear eventos](event-create.md).

![Ejemplo de tienda - barra lateral del evento](./assets/storefront-event-sidebar.png){width="700" zoomable="yes"}
