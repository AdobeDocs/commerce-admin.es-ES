---
title: Widget de pedidos y devoluciones
description: Aprenda a utilizar el widget pedidos y devoluciones para ofrecer a los clientes la capacidad de comprobar el estado de sus pedidos, imprimir facturas y rastrear envíos.
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# Widget de pedidos y devoluciones

El _Pedidos y devoluciones_ El widget permite a los clientes comprobar el estado de sus pedidos, imprimir facturas y realizar un seguimiento de los envíos. Cuando el widget se añade a la tienda, solo es visible para los invitados y para los clientes que no han iniciado sesión en sus cuentas. Los huéspedes pueden encontrar pedidos proporcionando el ID de pedido, el apellido de facturación y la dirección de correo electrónico o el código postal.

![Widget Pedidos y devoluciones en la barra lateral de la tienda](./assets/storefront-widget-orders-returns-sidebar.png){width="600" zoomable="yes"}

## El widget pedidos y devoluciones de la tienda

1. El cliente puede utilizar el **[!UICONTROL Find Order By]** opción para elegir uno de los siguientes parámetros para utilizar en la búsqueda del pedido:

   - Correo electrónico
   - Código postal

1. El cliente introduce el **[!UICONTROL Order ID]** y **[!UICONTROL Billing Last Name]**.

1. Introduce la facturación **[!UICONTROL Email Address]** o **[!UICONTROL ZIP Code]** que está asociado con el pedido.

1. Clics **[!UICONTROL Search]** para recuperar el pedido.

   ![Información de pedido mostrada en la tienda](./assets/storefront-widget-orders-returns-view.png){width="700" zoomable="yes"}

## Configurar el widget Pedidos y devoluciones

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Widget]**.

1. En el _[!UICONTROL Settings]_, haga lo siguiente:

   - Establecer **[!UICONTROL Type]** hasta `Orders and Returns`.

   - Elija la **[!UICONTROL Design Theme]** que utiliza la tienda.

1. Haga clic **[!UICONTROL Continue]**.

1. En el _[!UICONTROL Storefront Properties]_, haga lo siguiente:

   - Para **[!UICONTROL Widget Title]**, introduzca un título descriptivo para el widget.

     Este título solo es visible desde Admin.

   - Para **[!UICONTROL Assign to Store Views]**, seleccione las vistas de la tienda donde el widget sea visible.

     Puede seleccionar una vista de tienda específica, o `All Store Views`. Para seleccionar varias vistas, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

   - (Opcional) Para **[!UICONTROL Sort Order]**, introduzca un número para determinar el orden en que aparece este elemento con otros en la misma parte de la página. (`0` = primero, `1` = segundo, `3` = tercero, etc.)

1. En el _[!UICONTROL Layout Updates]_, haga clic en **[!UICONTROL Add Layout Update]**y haga lo siguiente:

   - Establecer **[!UICONTROL Display On]** al tipo de página donde desea que aparezca el widget.

   - Para determinar dónde se muestra el widget en la página, complete el resto de la información de actualización del diseño.

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

1. Cuando se le pida que actualice la caché, haga clic en el vínculo del mensaje en la parte superior de la página y siga las instrucciones.
