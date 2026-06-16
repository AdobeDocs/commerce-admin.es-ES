---
title: Configuración de listas de deseos
description: Aprenda a configurar la funcionalidad de la lista de deseos para sus clientes de la tienda.
exl-id: 479455f1-282f-4277-b132-45c5867fb21c
feature: Customers, Configuration
TQID: https://experienceleague.adobe.com/pSVYKFjf0Iz-zJ7fw1HxraizUwLYj7l1ykIWtnbI30w
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 537
ht-degree: 0%

---

# Configuración de listas de deseos

La configuración de la lista de deseos habilita las listas de deseos y determina la plantilla de correo electrónico y el remitente de los mensajes de correo electrónico que se utilizan cuando se comparte una lista de deseos.

## Habilitar la funcionalidad de lista de deseos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Wish List]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL General Options]** y haga lo siguiente:

   ![Configuración de clientes: configuración general de la lista de deseos](../configuration-reference/customers/assets/wishlist-general-options.png){width="600" zoomable="yes"}

   - Cambie **[!UICONTROL Enabled]** a `Yes`, lo que activa el módulo de lista de artículos deseados para la tienda.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce): cambia **[!UICONTROL Enable Multiple Wish Lists]** a `Yes`, lo que permite a los clientes crear y mantener varias listas de deseos.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Para limitar el número de listas de deseos que los clientes pueden tener asociados a su cuenta, escriba un valor para **[!UICONTROL Number of Multiple Wish Lists]**.

   - Cambie **[!UICONTROL Show in Sidebar]** por `Yes`, para que se muestren las listas de deseos en la barra lateral.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Share Options]** y haga lo siguiente:

   ![Configuración de clientes - opciones de uso compartido de la lista de deseos](../configuration-reference/customers/assets/wishlist-share-options.png){width="600" zoomable="yes"}

   - Establezca **[!UICONTROL Email Sender]** en el contacto de tienda que debe aparecer como remitente del mensaje. Opciones: Contacto general, Representante de ventas, Atención al cliente, Correo electrónico personalizado.

   - Configure **[!UICONTROL Email Template]** para que se use cuando un cliente comparta una lista de deseos.

   - Para limitar el número total de correos electrónicos que puede enviar un cliente, escriba un valor de **[!UICONTROL Max Emails Allowed to be Sent]**. El valor predeterminado es 10 y el máximo permitido es 10 000.

   - Para limitar el tamaño del mensaje, escriba un valor para **[!UICONTROL Email Text Length Limit]**. El valor predeterminado es 255.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL My Wish List Link]** y establezca **[!UICONTROL Display Wish List Summary]** en uno de los siguientes:

   - `Display number of items in wish list`
   - `Display item quantities`

   ![Configuración de clientes - visualización de la lista de deseos](../configuration-reference/customers/assets/wishlist-my-wishlist-link.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Añadir búsqueda en la lista de deseos

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

Cualquier lista de deseos pública se puede encontrar usando el widget de búsqueda de listas de deseos [Wish List](../content-design/widgets.md). El widget permite que un cliente busque por el nombre o la dirección de correo electrónico del propietario de la lista de deseos. Los clientes de tienda pueden encontrar listas de deseos que pertenecen a otros clientes, verlas y solicitar productos de ellos o agregar los productos a sus propias listas de deseos. Si otro cliente compra un artículo de una lista pública de artículos deseados, no se elimina de la lista original de artículos deseados. El widget _Búsqueda en la lista de deseos_ se puede agregar a cualquier página de la tienda para facilitar a los clientes la búsqueda de las listas de deseos de amigos y familiares.

![Ejemplo de tienda - búsqueda en la lista de deseos](./assets/storefront-wishlist-search.png){width="700" zoomable="yes"}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Widget]**.

1. En la ficha _[!UICONTROL Settings]_, haga lo siguiente:

   - Establezca **[!UICONTROL Type]** en `Wish List Search`.

   - Establezca **[!UICONTROL Design Theme]** en el tema de la tienda donde se agrega la lista de artículos deseados.

   - Haga clic en **[!UICONTROL Continue]**.

1. Completar _[!UICONTROL Storefront Properties]_:

   - Escriba **[!UICONTROL Widget Title]**.

   - Establezca **[!UICONTROL Assign to Store Views]** en la vista o sitio web donde se utilizará el widget.

   - Para **[!UICONTROL Sort Order]**, escriba un número para determinar la ubicación del widget dentro de su contenedor.

     `0` = primero (predeterminado), `1` = segundo, `2` = tercero, etc.

1. En la sección _[!UICONTROL Layout Updates]_, haga clic en **[!UICONTROL Add Layout Update]**&#x200B;y establezca **[!UICONTROL Display on]**&#x200B;en uno de los siguientes:

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

1. En la lista **[!UICONTROL Container]**, elija el área del diseño de página donde se colocará.

   ![Widget de búsqueda de lista de deseos - diseño](./assets/widget-wishlist-search-storefront.png){width="700" zoomable="yes"}

1. En el panel izquierdo, elija **[!UICONTROL Widget Options]**.

1. Establezca **[!UICONTROL Quick Search Form Types]** en una de las siguientes opciones:

   - `All Forms`: los clientes pueden buscar según todos los parámetros disponibles.
   - `Owner Name`: los clientes pueden buscar listas de deseos por nombre de propietario.
   - `Owner Email`: los clientes pueden buscar listas de deseos por dirección de correo electrónico del propietario.

   >[!NOTE]
   >
   >Las direcciones de envío no se incluyen en las listas de deseos.

1. Configure las propiedades de los widgets restantes según sea necesario, siguiendo las [instrucciones](../content-design/widget-create.md) estándar.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

1. Cuando se le solicite, actualice todas las cachés no válidas.
