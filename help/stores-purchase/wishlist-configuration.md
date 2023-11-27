---
title: Configuración de listas de deseos
description: Aprenda a configurar la funcionalidad de la lista de deseos para sus clientes de la tienda.
exl-id: 479455f1-282f-4277-b132-45c5867fb21c
feature: Customers, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# Configuración de listas de deseos

La configuración de la lista de deseos habilita las listas de deseos y determina la plantilla de correo electrónico y el remitente de los mensajes de correo electrónico que se utilizan cuando se comparte una lista de deseos.

## Habilitar la funcionalidad de lista de deseos

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Wish List]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL General Options]** y haga lo siguiente:

   ![Configuración de clientes: configuración general de la lista de deseos](../configuration-reference/customers/assets/wishlist-general-options.png){width="600" zoomable="yes"}

   - Alternar **[!UICONTROL Enabled]** hasta `Yes`, que activa el módulo de lista de artículos deseados para la tienda.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Alternar **[!UICONTROL Enable Multiple Wish Lists]** hasta `Yes`, que permite a los clientes crear y mantener varias listas de deseos.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Para limitar el número de listas de deseos que los clientes pueden tener asociadas a su cuenta, introduzca un valor para **[!UICONTROL Number of Multiple Wish Lists]**.

   - Alternar **[!UICONTROL Show in Sidebar]** hasta `Yes`, que muestra las listas de deseos en la barra lateral.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Share Options]** y haga lo siguiente:

   ![Configuración de clientes: opciones de uso compartido de listas de deseos](../configuration-reference/customers/assets/wishlist-share-options.png){width="600" zoomable="yes"}

   - Configure las variables **[!UICONTROL Email Sender]** al contacto de tienda que debe aparecer como remitente del mensaje. Opciones: Contacto general, Representante de ventas, Atención al cliente, Correo electrónico personalizado.

   - Configure las variables **[!UICONTROL Email Template]** para utilizar cuando un cliente comparte una lista de deseos.

   - Para limitar el número total de correos electrónicos que puede enviar un cliente, escriba un **[!UICONTROL Max Emails Allowed to be Sent]** valor. El valor predeterminado es 10 y el máximo permitido es 10 000.

   - Para limitar el tamaño del mensaje, introduzca un valor para **[!UICONTROL Email Text Length Limit]**. El valor predeterminado es 255.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL My Wish List Link]** sección y conjunto **[!UICONTROL Display Wish List Summary]** a uno de los siguientes:

   - `Display number of items in wish list`
   - `Display item quantities`

   ![Configuración de clientes: visualización de la lista de deseos](../configuration-reference/customers/assets/wishlist-my-wishlist-link.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Añadir búsqueda en la lista de deseos

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

Cualquier lista de deseos pública se puede encontrar usando la Búsqueda de la lista de deseos [widget](../content-design/widgets.md). El widget permite que un cliente busque por el nombre o la dirección de correo electrónico del propietario de la lista de deseos. Los clientes de tienda pueden encontrar listas de deseos que pertenecen a otros clientes, verlas y solicitar productos de ellos o agregar los productos a sus propias listas de deseos. Si otro cliente compra un artículo de una lista pública de artículos deseados, no se elimina de la lista original de artículos deseados. El _Búsqueda en lista de deseos_ widget se puede añadir a cualquier página de su tienda para facilitar a los clientes a encontrar las listas de deseos de amigos y familiares.

![Ejemplo de tienda: búsqueda en la lista de deseos](./assets/storefront-wishlist-search.png){width="700" zoomable="yes"}

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Widget]**.

1. En el _[!UICONTROL Settings]_pestaña, haga lo siguiente:

   - Establecer **[!UICONTROL Type]** hasta `Wish List Search`.

   - Establecer **[!UICONTROL Design Theme]** al tema de la tienda donde se agrega la lista de deseos.

   - Haga clic **[!UICONTROL Continue]**.

1. Complete la _[!UICONTROL Storefront Properties]_:

   - Introduzca el **[!UICONTROL Widget Title]**.

   - Establecer **[!UICONTROL Assign to Store Views]** a la vista o sitio web donde se utilizará el widget.

   - Para **[!UICONTROL Sort Order]**, introduzca un número para determinar la ubicación del widget dentro de su contenedor.

     `0` = primero (predeterminado), `1` = segundo, `2` = tercero, etc.

1. En el _[!UICONTROL Layout Updates]_, haga clic en **[!UICONTROL Add Layout Update]**y establecer **[!UICONTROL Display on]**a uno de los siguientes:

   - _[!UICONTROL Categories]_

      - `Anchor Categories`
      - `Non-Anchor Categories`

   - _[!UICONTROL Products]_

      - `All Product Type`
      - `Simple Product`
      - `Virtual Product`
      - `Bundle Product`
      - `Configurable Product`
      - `Downloadable Product`
      - `Gift Card`
      - `Grouped Product`

   - _[!UICONTROL Generic Page]_

      - `All Pages`
      - `Specified Page`
      - `Page Layouts`

1. En el **[!UICONTROL Container]** , elija el área del diseño de página donde se va a colocar.

   ![Widget de búsqueda de lista de deseos - diseño](./assets/widget-wishlist-search-storefront.png){width="700" zoomable="yes"}

1. En el panel izquierdo, elija **[!UICONTROL Widget Options]**.

1. Establecer **[!UICONTROL Quick Search Form Types]** a uno de los siguientes:

   - `All Forms` - Los clientes pueden buscar por todos los parámetros disponibles.
   - `Owner Name` - Los clientes pueden buscar listas de deseos por nombre de propietario.
   - `Owner Email` - Los clientes pueden buscar listas de deseos por dirección de correo electrónico del propietario.

   >[!NOTE]
   >
   >Las direcciones de envío no se incluyen en las listas de deseos.

1. Configure las propiedades de los widgets restantes según sea necesario, siguiendo el estándar [instrucciones](../content-design/widget-create.md).

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

1. Cuando se le solicite, actualice todas las cachés no válidas.
