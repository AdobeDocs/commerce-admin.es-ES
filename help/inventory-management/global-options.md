---
title: "Configurar [!DNL Inventory Management] opciones globales"
description: Obtenga información sobre cómo configurar los valores predeterminados [!DNL Inventory Management] opciones de configuración para el producto y stock para sus sitios web.
exl-id: 1a8c9605-ae61-4d45-b549-64911b329203
feature: Inventory, Configuration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 1%

---

# Configurar [!DNL Inventory Management] opciones globales

Configure las opciones de configuración predeterminadas del producto y las existencias para sus sitios web. Algunos de estos ajustes se pueden sobrescribir por producto mediante [Configuración de opciones de producto](product-options.md). Para configurar la Prioridad de distancia, consulte [Configuración del algoritmo de prioridad de distancia](distance-priority-algorithm.md).

## Configurar las opciones de productos y existencias globalmente

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Inventory]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Stock Options]** y defina las opciones:

   ![Opciones de Stock](assets/config-catalog-inventory-stock-options.png){width="600" zoomable="yes"}

   - Para ajustar la cantidad física actual cuando se realiza un pedido, establezca **[!UICONTROL Decrease Stock When Order is Placed]** hasta `Yes`.

   - Para devolver artículos a stock si se cancela un pedido, **[!UICONTROL Set Items' Status to be in Stock When Order in Cancelled]** hasta `Yes`.

   - Para seguir mostrando productos en el catálogo que ya no están en stock, establezca **[!UICONTROL Display Out of Stock Products]** hasta `Yes`.

   - If [alertas de precios](alert-setup.md) Una vez activados, los clientes pueden registrarse para recibir una notificación cuando el producto vuelva a estar disponible.

   - Para definir el inicio para mostrar el último importe de inventario restante en la página de productos, introduzca un importe para **[!UICONTROL Only X left Threshold]**.

     El mensaje empieza a aparecer cuando la cantidad en stock alcanza el umbral. Por ejemplo, si se establece en `3`, el mensaje `Only 3 left` aparece cuando la cantidad en existencia alcanza tres. El mensaje se ajusta para reflejar la cantidad disponible, hasta que la cantidad alcance cero.

   - Para mostrar el mensaje &quot;En stock&quot; o &quot;Sin existencias&quot; en la página del producto, configure **[!UICONTROL Display Products Availability In Stock on Storefront]** hasta `Yes`.

   - Para comprobar el inventario al cargar un producto en el carro, establezca **[!UICONTROL Enable Inventory Check On Cart Load]** hasta `Yes`. Con esta opción deshabilitada, se omite la comprobación de inventario. Al deshabilitar esta opción, se acelera el cierre de compra, especialmente si hay muchos artículos en el carro de compras. Sin embargo, si omite la prevalidación, los clientes podrían ver errores de falta de existencias más adelante en el proceso de cierre de compra.

   - Para mantener la coherencia entre el inventario y el catálogo, establezca **[!UICONTROL Synchronize with Catalog]** hasta `Yes`. Con esta opción habilitada, los datos de inventario se ajustan según los cambios de catálogo (como el producto eliminado, el SKU del producto modificado y el tipo de producto modificado).

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Product Stock Options]** y defina las opciones:

   - Para activar [control de inventario](enable.md) para su catálogo, establezca **[!UICONTROL Manage Stock]** hasta `Yes`.

     ![Opciones de stock de productos](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Establecer **[!UICONTROL Backorders]** a uno de los siguientes:

     | Opción | Descripción |
     | ----- | ----- |
     | `No Backorders` | [Pedidos no satisfechos](backorders.md) no se aceptan cuando el producto está agotado. |
     | `Allow Qty Below 0` | Los pedidos no satisfechos se aceptan cuando la cantidad es inferior a cero. |
     | `Allow Qty Below 0 and Notify Customer` | Los pedidos pendientes se aceptan cuando la cantidad es inferior a cero y el sistema notifica al cliente que el pedido se puede realizar. |

   - Introduzca el **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

   - Introduzca una cantidad para **[!UICONTROL Out-of-Stock Threshold]**:

     | Valor | Descripción |
     | ----- |-----|
     | Cantidad positiva | Con Pedidos no satisfechos desactivado, introduzca un importe positivo. |
     | Cero | Con Pedidos No Satisfechos activado, introducir `0` permite pedidos pendientes infinitos. |
     | Importe negativo | Con Pedidos no satisfechos activado, se recomienda introducir un importe negativo. El importe se añade a la cantidad vendible. Por ejemplo, introduzca `-50` para permitir pedidos de hasta este importe. |

   - Introduzca el **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** para el grupo y los importes seleccionados.

   - Para **[!UICONTROL Notify for Quantity Below]**, introduzca el nivel de stock que déclencheur la notificación de que el artículo está agotado.

   - Para activar los incrementos de cantidad para el producto, defina **[!UICONTROL Enable Qty Increments]** hasta `Yes`. A continuación, para **[!UICONTROL Qty Increments]**, introduzca el número de artículos que deben adquirirse para cumplir el requisito.

     Por ejemplo, un artículo que se vende en incrementos de seis se puede comprar en cantidades de `6`, `12`, `18`, etc.

   - Para [!DNL Inventory Management], **[!UICONTROL Automatically Return Credit Memo Item to Stock]** se establece en `No`. Al ejecutar una nota de abono, introduzca y seleccione para devolver el stock a los orígenes.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Admin bulk operations]** y defina las opciones:

   ![Operaciones masivas de administrador](assets/config-catalog-inventory-admin-bulk-operations.png){width="600" zoomable="yes"}

   - Establecer **[!UICONTROL Run asynchronously]** para ejecutar operaciones por lotes de forma asíncrona para acciones de productos masivas

     Estas operaciones incluyen lotes [asignar y cancelar la asignación de orígenes](bulk-assignment.md), y [transferir inventario al origen](inventory-transfer.md). Recopila acciones masivas hasta el tamaño del lote asincrónico y, a continuación, ejecuta esas acciones. Esta opción está desactivada de forma predeterminada. Se recomienda revisar el rendimiento con acciones masivas antes de habilitar.

     >[!NOTE]
     >
     >Para configurar y admitir _administradores de colas asincrónicos_, debe emitir un comando utilizando la línea de comandos. Este paso puede requerir la asistencia del desarrollador. Consulte [Iniciar consumidores de cola de mensajes](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) en el _Guía de configuración_.

   - Si está activado, configure el **[!UICONTROL Asynchronous batch size]**. El tamaño predeterminado del lote es 100. Cuando los procesos masivos alcanzan esta cantidad, el sistema los déclencheur.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.
