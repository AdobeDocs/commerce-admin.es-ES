---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Inventory]'
description: Revise la configuración de en [!UICONTROL Catalog] &gt; [!UICONTROL Inventory] de la administración de Commerce.
exl-id: 80113a31-3585-4ee1-95af-31efc09389eb
feature: Configuration, Inventory
source-git-commit: 768c9fdc37127b408230983e39e98b11149713a7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Inventory]

{{config}}

>[!NOTE]
>
>[!DNL Inventory Management] para Adobe Commerce y Magento Open Source le ofrece las herramientas para administrar el inventario de productos. Los comerciantes con una sola tienda en varios almacenes, tiendas, ubicaciones de recogida, distribuidores directos entre otros pueden utilizar estas funciones para mantener las cantidades de ventas y gestionar los envíos para completar pedidos. Para obtener más información sobre estas funciones y cómo puede utilizarlas para administrar existencias en varias ubicaciones, consulte la [_[!DNL Inventory Management] Guía del usuario _](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html).

## [!UICONTROL Stock Options]

![Opciones de Stock](./assets/catalog-inventory-stock-options.png)<!-- zoom -->

<!-- [Stock Options](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Decrease Stock When Order is Placed] | Global | Si se establece en `Yes`, disminuye la cantidad en stock cuando se realiza el pedido. Con _Administrar stock_ activada, las reservas se introducen para los productos y las cantidades pedidos. Opciones: `Yes` / `No` |
| [!UICONTROL Set Items' Status to be in Stock When Order is Cancelled] | Vista de tienda | Si se establece en `Yes`, devuelve el artículo a stock cuando se cancela el pedido. Con _Administrar stock_ activada, la reserva se borra para los productos y cantidades cancelados. Opciones: `Yes` / `No` |
| [!UICONTROL Display Out of Stock Products] | Global | Si se establece en `Yes`, muestra los productos sin existencias. Si las alertas de productos también están habilitadas, los clientes pueden registrarse para recibir una notificación cuando el producto esté disponible. Opciones: `Yes` / `No` |
| [!UICONTROL Only X left Threshold] | Sitio web | Establece el umbral para la `Only x left` Mensaje. Por ejemplo, si se establece en 3, el mensaje aparece cuando hay tres o menos artículos en stock. El mensaje no aparece si el valor está establecido en `0`. |
| [!UICONTROL Display products availability in Stock on Storefront] | Vista de tienda | Si se establece en `Yes`, muestra un `In Stock` o `Out of Stock` en la página de producto. Opciones: `Yes` / `No` |
| [!UICONTROL Enable Inventory Check On Cart Load] | Global | Determina si se realiza una comprobación de inventario al cargar un producto en el carro de compras. Deshabilitar esta comprobación de inventario puede mejorar el rendimiento de los pasos de cierre de compra, especialmente cuando hay muchos artículos en el carro de compras. Sin embargo, si omite la prevalidación, los clientes podrían ver lo siguiente _sin existencias_ errores más adelante en el proceso de cierre de compra. Opciones: `Yes` / `No` |
| [!UICONTROL Synchronize with Catalog] | Global | Cuando se establece en `Yes`Sin embargo, los datos de inventario se ajustan según los cambios de catálogo (como eliminaciones de productos, cambios de SKU de productos y cambios de tipo de producto) y mantienen la coherencia entre el inventario y el catálogo. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Stock Options]

![Opciones de stock de productos](./assets/catalog-inventory-product-stock-options.png)<!-- zoom -->

<!-- [Product Stock Options](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Manage Stock] | Global | Determina si utiliza el control de inventario completo para administrar los artículos del catálogo. Opciones: <br/>**Sí** : activa el control de inventario completo para rastrear la cantidad de artículos que están actualmente en stock. <br/>**No** - No realiza el seguimiento de la cantidad de artículos que están actualmente en stock. |
| [!UICONTROL Backorders] | Global | Determina la forma en que la tienda administra los pedidos pendientes. Un pedido pendiente no cambia el estado de procesamiento del pedido. Los fondos se siguen autorizando o capturando inmediatamente cuando se realiza el pedido, independientemente de si el producto está en stock. Cuando el producto está disponible, se envía. Opciones: <br/>**No hay pedidos pendientes** - No acepta pedidos pendientes cuando el producto está agotado. <br/>**Permitir cantidad inferior a 0** - Acepta pedidos pendientes cuando la cantidad es inferior a cero. <br/>**Permitir cantidad inferior a 0 y notificar al cliente** - Acepta pedidos pendientes cuando la cantidad cae por debajo de cero, pero notifica a los clientes que aún se pueden realizar pedidos. |
| [!UICONTROL Use deferred Stock update] | Global | ![Adobe Commerce](../../assets/adobe-logo.svg) (Solo Adobe Commerce) Determina si se aplaza la actualización de existencias si se permiten pedidos no satisfechos (la variable _Pedidos en espera_ está establecida en cualquier valor que no sea `No backorders` valor predeterminado). Funciona para un solo producto o para un sitio web completo y utiliza el _Cola de trabajos_ mecanismo para permitir que los indicadores de cantidad de inventario se actualicen de forma asíncrona después de realizar los pedidos. Esta opción también funciona con [Colocación de pedido asincrónica](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/high-throughput-order-processing.html#asynchronous-order-placement) en combinación con [Inventory management](../../inventory-management/introduction.md). |
| Cantidad máxima permitida en el carro de compras | Global | Determina la cantidad máxima de un producto que se puede comprar en un único pedido. De forma predeterminada, la cantidad máxima está establecida en 10 000. |
| [!UICONTROL Out-of-Stock Threshold] | Global | Determina el nivel de existencias en el que se considera que un producto está agotado. Opciones: <br/>**Cantidad positiva** - Con _Pedidos no satisfechos_ desactivado, introduzca una cantidad positiva. Si la opción Pedidos no satisfechos está activada, se ignorará esta cantidad. <br/>**Cero** - Con _Pedidos no satisfechos_ habilitado, introducir `0` permite pedidos pendientes infinitos. <br/>**Importe negativo** - Con _Pedidos no satisfechos_ activado, se recomienda introducir una cantidad negativa. El importe se añade a la cantidad vendible. Por ejemplo, introduzca -50 para permitir pedidos de hasta esta cantidad. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Global | Determina la cantidad mínima de un artículo disponible para la compra según el grupo de clientes. De forma predeterminada, la cantidad mínima se establece en 1. Clic **[!UICONTROL Add Minimum Qty]** para introducir un valor diferente para un grupo de clientes específico. |
| [!UICONTROL Notify for Quantity Below] | Global | Determina el nivel de stock al que se envía la notificación de que el inventario ha caído por debajo del umbral. |
| [!UICONTROL Enable Qty Increments] | Global | Determina si los artículos se pueden vender en incrementos de cantidad. Opciones: `Yes` / `No` |
| [!UICONTROL Qty Increments] | Global | Establece el número de productos que componen un incremento de cantidad. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | Global | Determina si los artículos incluidos en las notas de abono se devuelven automáticamente al inventario. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Bulk Operations]

![Operaciones masivas de administrador](./assets/catalog-inventory-admin-bulk-operations.png)<!-- zoom -->

<!-- [Admin Bulk Operations](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

>[!NOTE]
>
>Para configurar y admitir **administradores de colas asincrónicos**, debe utilizar la línea de comandos. Esto puede requerir la asistencia del desarrollador. Consulte [Iniciar consumidores de cola de mensajes](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) en el _Guía de configuración_.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Run asynchronously] | Global | Determina si se ejecutan operaciones masivas de forma asíncrona para acciones de productos masivas, incluidas [a granel](../../inventory-management/bulk-assignment.md) asignar orígenes, anular la asignación de orígenes y [transferir inventario al origen](../../inventory-management/inventory-transfer.md). Recopila acciones masivas hasta el _[!UICONTROL Asynchronous batch size]_, luego ejecuta esas acciones. Esta función está desactivada de forma predeterminada. Se recomienda revisar el rendimiento con acciones masivas antes de habilitar. Opciones:<br/>**`Yes`**- Ejecuta todas las operaciones por lotes para [!DNL Inventory Management] asincrónicamente. Para habilitarlo, debe configurar un administrador de colas asincrónico.<br/>**`No`**- Predeterminado. No ejecuta operaciones masivas de forma asincrónica. |
| [!UICONTROL Asynchronous batch size] | Global | Establecer **[!UICONTROL Run asynchronously]** hasta `Yes` para introducir un valor para _[!UICONTROL Asynchronous batch size]_field. <br/>El tamaño predeterminado del lote es 100. Cuando los procesos masivos alcanzan esta cantidad, se ejecutan. |

{style="table-layout:auto"}

## [!UICONTROL Inventory Indexer Settings]

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Stock/Source reindex strategy] | Global | Determina la estrategia utilizada para la reindexación de stock/origen. Opciones: `Synchronous` / `Asynchronous` (se debe configurar un administrador de colas asincrónico para el modo asincrónico) |

{style="table-layout:auto"}

>[!NOTE]
>
> Debido a las dependencias de las actualizaciones de inventario para las actividades relacionadas con pedidos, el indexador de inventario también se activa al guardar el producto, independientemente del `Synchronous` o `Asynchronous` configuración.


## [!UICONTROL Distance Provider for Distance Based SSA]

![Proveedores de Distancia para SSA Basado en Distancia](./assets/catalog-inventory-distance-provider.png)<!-- zoom -->

<!-- [Distance Providers for Distance Based SSA](https://docs.magento.com/user-guide/catalog/inventory-configure-distance-priority.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Provider] | Global | Determina el proveedor que se utilizará para el algoritmo de selección de origen de prioridad de distancia. Esta función está habilitada de forma predeterminada. Opciones: <br/>**`Google MAP`**: utiliza los servicios de Google para calcular la distancia y el tiempo entre la dirección de destino de envío y las ubicaciones de origen (dirección y coordenadas GPS). Esta opción requiere una clave de API de Google y puede conllevar gastos a través de Google.<br/>**`Offline Calculation`** - Calcula la distancia utilizando una base de datos integrada para determinar el origen más cercano a la dirección de destino de envío. Para utilizar esta opción, es posible que necesite asistencia para desarrolladores para descargar inicialmente el contenido de ubicación de la base de datos de todos los países a los que realiza envíos mediante una línea de comandos. |

{style="table-layout:auto"}

## [!UICONTROL Google Distance Provider]

![Proveedor de distancia de Google](./assets/catalog-inventory-distance-provider-settings.png)<!-- zoom -->

<!-- [Google Distance Provider](https://docs.magento.com/user-guide/catalog/inventory-configure-distance-priority.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Google API key] | Global | Introduzca la clave de API de Google para el proveedor de Google MAP. La clave es del [!DNL Google Maps Platform] y debería tener [!DNL Geocoding API] y [!DNL Distance Matrix API] activado. Para obtener más información, consulte [Configuración del algoritmo de prioridad de distancia](../../inventory-management/distance-priority-algorithm.md#configure-the-distance-priority-algorithm) en el _Guía de Inventory management_. |
| [!UICONTROL Computation mode] | Global | Determina las direcciones y rutas para calcular la distancia desde la dirección de envío y todos los orígenes asignados al stock. De forma predeterminada, los cálculos utilizan el modo de conducción. Opciones: <br/>**`Driving`**- Ajuste predeterminado, solicita indicaciones de conducción estándar usando la red de carreteras.<br/>**`Walking`** - Solicita indicaciones para caminar usando caminos peatonales y aceras (cuando estén disponibles). <br/>**`Bicycling`**- Solicita direcciones de ciclismo usando rutas de bicicleta y calles preferidas (actualmente solo disponible en los EE.UU. y algunas ciudades canadienses). |
| [!UICONTROL Value] | Global | Indica lo que se debe calcular y devolver para la distancia y el tiempo de las ubicaciones de origen a la dirección de destino de envío. El algoritmo de prioridad de distancia recomienda el origen con la distancia o el tiempo más corto a la dirección de destino de envío, lo que ofrece envíos más rápidos y posiblemente más baratos. Opciones: <br/>**`Distance`**- Devuelve la distancia entre puntos en métricas (kilómetros y metros) o imperiales (millas y pies).<br/>**`Time to Destination`** - Devuelve el tiempo necesario para viajar desde las ubicaciones de origen a la dirección de envío en horas y minutos. |

{style="table-layout:auto"}
