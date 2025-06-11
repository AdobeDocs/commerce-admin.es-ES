---
title: Widget de pedidos y devoluciones
description: Aprenda a utilizar el widget pedidos y devoluciones para ofrecer a los clientes la capacidad de comprobar el estado de sus pedidos, imprimir facturas y rastrear envíos.
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---

# Widget de pedidos y devoluciones

El widget _Pedidos y devoluciones_ permite a los invitados comprobar el estado de sus pedidos, imprimir facturas y realizar un seguimiento de los envíos. Cuando el widget se añade a la tienda, solo es visible para los invitados y para los clientes que no han iniciado sesión en sus cuentas. Los huéspedes pueden encontrar pedidos proporcionando el ID de pedido, el apellido de facturación y la dirección de correo electrónico o el código postal.

![Widget de pedidos y devoluciones en la barra lateral de la tienda](./assets/storefront-widget-orders-returns-sidebar.png){width="600" zoomable="yes"}

## El widget pedidos y devoluciones de la tienda

1. El cliente puede usar la opción **[!UICONTROL Find Order By]** para elegir uno de los siguientes parámetros para usar en la búsqueda del pedido:

   - Correo electrónico
   - Código postal

1. El cliente escribe **[!UICONTROL Order ID]** y **[!UICONTROL Billing Last Name]**.

1. Introduce la facturación **[!UICONTROL Email Address]** o **[!UICONTROL ZIP Code]** asociada con el pedido.

1. Hace clic en **[!UICONTROL Search]** para recuperar el pedido.

   ![Información de pedido mostrada en la tienda](./assets/storefront-widget-orders-returns-view.png){width="700" zoomable="yes"}

## Configurar el widget Pedidos y devoluciones

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Widget]**.

1. En la sección _[!UICONTROL Settings]_, haga lo siguiente:

   - Establezca **[!UICONTROL Type]** en `Orders and Returns`.

   - Elija el **[!UICONTROL Design Theme]** que usa la tienda.

1. Haga clic en **[!UICONTROL Continue]**.

1. En la sección _[!UICONTROL Storefront Properties]_, haga lo siguiente:

   - Para **[!UICONTROL Widget Title]**, escriba un título descriptivo para el widget.

     Este título solo es visible desde Admin.

   - Para **[!UICONTROL Assign to Store Views]**, seleccione las vistas de la tienda donde el widget sea visible.

     Puede seleccionar una vista de tienda específica o `All Store Views`. Para seleccionar varias vistas, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

   - (Opcional) Para **[!UICONTROL Sort Order]**, escriba un número para determinar el orden en que aparece este elemento con otros en la misma parte de la página. (`0` = primero, `1` = segundo, `3` = tercero, etc.)

1. En la sección _[!UICONTROL Layout Updates]_, haga clic en **[!UICONTROL Add Layout Update]**&#x200B;y haga lo siguiente:

   - Establezca **[!UICONTROL Display On]** en el tipo de página donde desea que aparezca el widget.

   - Para determinar dónde se muestra el widget en la página, complete el resto de la información de actualización del diseño.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

1. Cuando se le pida que actualice la caché, haga clic en el vínculo del mensaje en la parte superior de la página y siga las instrucciones.
