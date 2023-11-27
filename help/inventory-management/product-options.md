---
title: "Configurar [!DNL Inventory Management] opciones de producto"
description: Obtenga información sobre cómo configurar el [!DNL Inventory Management] opciones de configuración del producto.
exl-id: b5cff7d2-5197-4362-9503-b07c80793ac7
feature: Inventory, Products
source-git-commit: ccd93a54b6fa23a7a54fb423f8232c72cd8fe027
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---

# Configurar [!DNL Inventory Management] opciones de producto

Estas configuraciones se aplican únicamente al producto editado, anulando todas las configuraciones en el nivel de sitio web global. Modifique esta configuración al editar un producto, a través del _[!UICONTROL Sources]_y_[!UICONTROL Advanced Inventory]_ página.

- Configurar opciones de producto por origen
- Configurar opciones de producto para inventario avanzado

## Opciones de producto por origen

Configure las cantidades y la configuración adicional por [fuente añadida](sources-add.md) para el producto.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Abra un producto en modo de edición.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Sources]** y configure las opciones del producto para cada origen:

   - Introduzca una **[!UICONTROL Qty]** (cantidad) cantidad.

   - Configure las variables **[!UICONTROL Source Item Status]** as `In Stock` o `Out of Stock`.

   - Para modificar la notificación de la cantidad inferior por origen, borre o seleccione **[!UICONTROL Notify Quantity Use Default]** casilla de verificación

     Si está conciliado, introduzca la cantidad de nivel de stock que déclencheur el aviso de falta de existencias del artículo. La cantidad introducida se resta de la cantidad vendible del artículo en el nivel de stock.

     `Select to use Default` - [!DNL Commerce] comprueba las opciones de inventario avanzado del producto para ver los ajustes de configuración.
     `Clear to Modify` - Introduzca un valor para Notificar Cantidad, sustituyendo los ajustes de configuración de inventario avanzado y tienda.

   ![Sección de orígenes de un producto](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Done]**, entonces **[!UICONTROL Save]**.

### Descripciones de campos

| Campo | Ámbito | Descripción |
|--|--|--|
| [!UICONTROL Source Code] | Global | El código único de un [origen](sources-manage.md). |
| [!UICONTROL Name] | Global | El nombre único de un origen. |
| [!UICONTROL Status] | Global | El producto está activado o desactivado en el catálogo. |
| [!UICONTROL Source Item Status] | Global | Determina la disponibilidad actual del producto. Opciones:<br />`In Stock` - Hace que el producto esté disponible para la compra.<br />`Out of Stock` - A menos que se activen los pedidos no satisfechos, impide que el producto esté disponible para la compra y elimina el listado del catálogo. |
| [!UICONTROL Qty] | Global | Cantidades de stock disponibles para cada origen o ubicación. |
| [!UICONTROL Notify Quantity] | Global | Una cantidad para _[!UICONTROL Notify for Quantity Below]_para esta fuente específica si_[!UICONTROL Notify Quantity Use Default]_ no está seleccionado. |
| [!UICONTROL Notify Quantity Use Default] | Global | Indica que se debe utilizar la configuración predeterminada para _[!UICONTROL Notify for Quantity Below]_en el producto_[!UICONTROL Advanced Inventory]_ o la configuración global en la configuración de la tienda. |

## Opciones de producto avanzadas

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Abra un producto en modo de edición.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Sources]** y haga clic en **[!UICONTROL Advanced Inventory]**.

1. Para habilitar [control de inventario](enable.md) para su catálogo, establezca **[!UICONTROL Manage Stock]** hasta `Yes`.

   >[!NOTE]
   >
   >[!UICONTROL Manage Stock] la configuración de los productos secundarios anula la configuración de un producto.

   ![Inventario avanzado de un producto](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. Introduzca una cantidad para **[!UICONTROL Out-of-Stock Threshold]**:

   | Valor | Descripción |
   | ----- | ----- |
   | Cantidad positiva | Con _[!UICONTROL Backorders]_desactivado, introduzca un valor positivo. |
   | Cero | Con _[!UICONTROL Backorders]_habilitado, introducir `0` permite pedidos pendientes infinitos. |
   | Importe negativo | Con _[!UICONTROL Backorders]_Si está activada, se recomienda introducir un valor negativo. El importe se añade a la cantidad vendible. Por ejemplo, introduzca `-50` para permitir pedidos de hasta este importe. |

1. Introduzca el **[!UICONTROL Minimum Qty Allowed in Shopping Cart]**.

1. Introduzca el **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

1. Establecer **[!UICONTROL Qty uses Decimals]** hasta `Yes` si los clientes pueden utilizar un valor decimal en lugar de un número entero al introducir la cantidad solicitada.

1. Establecer **[!UICONTROL Allow Multiple Boxes for Shipping]** hasta `Yes` si el producto se puede vender por separado, en muchas cajas. Esta opción está visible cuando **[!UICONTROL Qty Uses Decimals]** se establece en `Yes` solo.

1. Establecer **[!UICONTROL Backorders]** a uno de los siguientes:

   | Opción | Descripción |
   | ----- | ----- |
   | `No Backorders` | Para no aceptar pedidos pendientes cuando el producto esté agotado. |
   | `Allow Qty Below 0` | Para aceptar pedidos pendientes cuando la cantidad es inferior a cero. |
   | `Allow Qty Below 0 and Notify Customer` | Para aceptar pedidos pendientes cuando la cantidad es inferior a cero y notificar al cliente que el pedido se puede realizar. |

   Para obtener más información, consulte [Configuración de Pedidos No Satisfechas](backorders.md).

1. Para activar los incrementos de cantidad para el producto, defina **[!UICONTROL Enable Qty Increments]** hasta `Yes` e introduzca el número de los artículos que deben adquirirse para cumplir el requisito en la **[!UICONTROL Qty Increments]** field.

   Por ejemplo, un artículo que se vende en incrementos de seis se puede comprar en cantidades de 6, 12, 18, etc.

1. Cuando termine, haga clic en **[!UICONTROL Done]** y luego **[!UICONTROL Save]**.

### Descripciones de campos

| Campo | Ámbito | Descripción |
|--|--|--|
| [!UICONTROL Manage Stock] | Global | Determina si se utiliza el control de inventario para administrar este producto en el catálogo. Establezca esta opción para habilitar o deshabilitar todo [!DNL Inventory Management] funciones. Al finalizar una devolución o una nota de abono, la cantidad del producto se devuelve automáticamente a la cantidad de origen afectada. Es posible que desee deshabilitar si utiliza un sistema ERP de terceros. |
| [!UICONTROL Out-of-Stock Threshold] | Global | Determina el nivel de existencias en el que se considera que un producto está agotado. Opciones:<br />Valor positivo: con los pedidos pendientes deshabilitados, introduzca una cantidad positiva.<br />Cero (0): con los pedidos no satisfechos activados, introducir cero permite pedidos no satisfechos infinitos.<br />Valor negativo: Con los pedidos pendientes activados, se recomienda introducir una cantidad negativa. El importe se añade a la cantidad vendible. Por ejemplo, introduzca `-50` para permitir pedidos de hasta este importe. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Global | Determina el número mínimo de productos que se pueden comprar en un único pedido. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Global | Determina el número máximo de productos que se pueden comprar en un único pedido. |
| [!UICONTROL Qty Uses Decimals] | Global | Determina si los clientes pueden utilizar un valor decimal en lugar de un número entero al introducir la cantidad pedida. Opciones:<br />`Yes` : permite introducir valores como decimales, en lugar de números enteros. Los decimales son adecuados para los productos vendidos por peso, volumen o longitud.<br />`No` - Requiere que los valores de cantidad se especifiquen como números enteros. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Global | Determina si las partes del producto se pueden enviar por separado. Esta opción está visible cuando **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Global | Determina cómo se administran los pedidos pendientes. Los pedidos no satisfechos no cambian el estado de procesamiento del pedido. Los fondos se siguen autorizando o capturando inmediatamente cuando se realiza el pedido, independientemente de si el producto está en stock. Los productos se envían cuando están disponibles. Cuando está activada, se recomienda introducir una cantidad negativa para el umbral de Agotado. Opciones:<br/>`No Backorders` - No acepta pedidos pendientes cuando el producto está agotado.<br />`Allow Qty Below 0` - Acepta pedidos pendientes cuando la cantidad es inferior a cero.<br />`Allow Qty Below 0 and Notify Customer` - Acepta pedidos pendientes cuando la cantidad cae por debajo de cero, pero notifica a los clientes que aún se pueden realizar pedidos. |
| [!UICONTROL Enable Qty Increments] | Global | Determina si el producto se puede vender en incrementos de cantidad. |

>[!NOTE]
>
>La configuración de producto simple anula las configuraciones de producto configurables para un producto específico.
