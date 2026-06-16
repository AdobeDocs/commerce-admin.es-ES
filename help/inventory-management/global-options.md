---
title: Configurar  [!DNL Inventory Management] opciones globales
description: Aprenda a configurar las  [!DNL Inventory Management] opciones de configuración predeterminadas del producto y las existencias de sus sitios web.
exl-id: 1a8c9605-ae61-4d45-b549-64911b329203
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/X4jFdmL4uXR6J5NY9z7b-swhmrVYWLTgOZVdNebJtXY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 648
ht-degree: 1%

---

# Configurar [!DNL Inventory Management] opciones globales

Configure las opciones de configuración predeterminadas del producto y las existencias para sus sitios web. Algunos de estos ajustes se pueden anular por producto mediante [Configuración de las opciones del producto](product-options.md). Para configurar la Prioridad de distancia, consulte [Configuración del algoritmo de prioridad de distancia](distance-priority-algorithm.md).

## Configurar las opciones de productos y existencias globalmente

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Inventory]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Stock Options]** y establezca las opciones:

   ![Opciones de Stock](assets/config-catalog-inventory-stock-options.png){width="600" zoomable="yes"}

   - Para ajustar la cantidad física actual cuando se realiza un pedido, establezca **[!UICONTROL Decrease Stock When Order is Placed]** en `Yes`.

   - Para devolver artículos a stock si se cancela un pedido, **[!UICONTROL Set Items' Status to be in Stock When Order in Cancelled]** a `Yes`.

   - Para seguir mostrando productos en el catálogo que ya no están disponibles, establezca **[!UICONTROL Display Out of Stock Products]** en `Yes`.

   - Si [alertas de precios](alert-setup.md) están habilitadas, los clientes pueden registrarse para recibir una notificación cuando el producto vuelva a estar disponible.

   - Para establecer el inicio para mostrar el último importe de inventario restante en la página del producto, escriba un importe para **[!UICONTROL Only X left Threshold]**.

     El mensaje empieza a aparecer cuando la cantidad en stock alcanza el umbral. Por ejemplo, si se establece en `3`, el mensaje `Only 3 left` aparece cuando la cantidad disponible es de tres. El mensaje se ajusta para reflejar la cantidad disponible, hasta que la cantidad alcance cero.

   - Para mostrar un mensaje &quot;En existencias&quot; o &quot;Sin existencias&quot; en la página del producto, establezca **[!UICONTROL Display Products Availability In Stock on Storefront]** en `Yes`.

   - Para comprobar el inventario al cargar un producto en el carro, establezca **[!UICONTROL Enable Inventory Check On Cart Load]** en `Yes`. Con esta opción deshabilitada, se omite la comprobación de inventario. Al deshabilitar esta opción, se acelera el cierre de compra, especialmente si hay muchos artículos en el carro de compras. Sin embargo, si omite la prevalidación, los clientes podrían ver errores de falta de existencias más adelante en el proceso de cierre de compra.

   - Para mantener la coherencia entre el inventario y el catálogo, establezca **[!UICONTROL Synchronize with Catalog]** en `Yes`. Con esta opción habilitada, los datos de inventario se ajustan según los cambios de catálogo (como el producto eliminado, el SKU del producto modificado y el tipo de producto modificado).

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Product Stock Options]** y establezca las opciones:

   - Para activar el [control de inventario](enable.md) para su catálogo, establezca **[!UICONTROL Manage Stock]** en `Yes`.

     ![Opciones de productos](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Establezca **[!UICONTROL Backorders]** en una de las siguientes opciones:

     | Opción | Descripción |
     | ----- | ----- |
     | `No Backorders` | [No se aceptan pedidos pendientes](backorders.md) cuando el producto está agotado. |
     | `Allow Qty Below 0` | Los pedidos no satisfechos se aceptan cuando la cantidad es inferior a cero. |
     | `Allow Qty Below 0 and Notify Customer` | Los pedidos pendientes se aceptan cuando la cantidad es inferior a cero y el sistema notifica al cliente que el pedido se puede realizar. |

   - Escriba **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

   - Escriba una cantidad para **[!UICONTROL Out-of-Stock Threshold]**:

     | Valor | Descripción |
     | ----- |-----|
     | Cantidad positiva | Con Pedidos no satisfechos desactivado, introduzca un importe positivo. |
     | Cero | Si se habilitan los pedidos no satisfechos, se pueden ingresar `0` pedidos no satisfechos infinitos. |
     | Importe negativo | Con Pedidos no satisfechos activado, se recomienda introducir un importe negativo. El importe se añade a la cantidad vendible. Por ejemplo, escriba `-50` para permitir pedidos de hasta esta cantidad. |

   - Escriba **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** para el grupo y las cantidades seleccionados.

   - Para **[!UICONTROL Notify for Quantity Below]**, introduzca el nivel de existencias que notifica a los déclencheur que el artículo está agotado.

   - Para activar los incrementos de cantidad para el producto, establezca **[!UICONTROL Enable Qty Increments]** en `Yes`. A continuación, para **[!UICONTROL Qty Increments]**, escriba el número de los artículos que deben comprarse para cumplir con el requisito.

     Por ejemplo, un artículo que se vende en incrementos de seis se puede comprar en cantidades de `6`, `12`, `18`, etc.

   - Para [!DNL Inventory Management], **[!UICONTROL Automatically Return Credit Memo Item to Stock]** está establecido en `No`. Al ejecutar una nota de abono, introduzca y seleccione para devolver el stock a los orígenes.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Admin bulk operations]** y establezca las opciones:

   ![Operaciones masivas de administración](assets/config-catalog-inventory-admin-bulk-operations.png){width="600" zoomable="yes"}

   - Establezca **[!UICONTROL Run asynchronously]** para ejecutar operaciones masivas de forma asíncrona para acciones masivas de productos

     Estas operaciones incluyen [asignación y cancelación de asignación de orígenes](bulk-assignment.md) en lotes, y [transferencia de inventario al origen](inventory-transfer.md). Recopila acciones masivas hasta el tamaño del lote asincrónico y, a continuación, ejecuta esas acciones. Esta opción está desactivada de forma predeterminada. Se recomienda revisar el rendimiento con acciones masivas antes de habilitar.

     >[!NOTE]
     >
     >Para configurar y admitir _administradores de cola asincrónicos_, debe emitir un comando mediante la línea de comandos. Este paso puede requerir la asistencia del desarrollador. Consulte [Iniciar consumidores de cola de mensajes](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) en la _Guía de configuración_.

   - Si está habilitado, establezca **[!UICONTROL Asynchronous batch size]**. El tamaño predeterminado del lote es 100. Cuando los procesos masivos alcanzan esta cantidad, el sistema los déclencheur.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
