---
title: "Configurar [!DNL Inventory Management]"
description: Obtenga información acerca de la configuración de [!DNL Inventory Management] opciones que determinan la disponibilidad del origen, los productos de la tienda y el envío del pedido.
exl-id: 1696999e-77b1-45c7-9b0b-dd1512427cff
feature: Inventory, Configuration
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 0%

---

# Configurar [!DNL Inventory Management]

El [!DNL Inventory Management] Este módulo admite los ajustes de configuración de inventario en el nivel de producto y global, y también proporciona ajustes adicionales que afectan a la disponibilidad del origen, los productos de tienda y el envío de pedidos. Los ajustes de configuración se aplican a:

- Todo el catálogo: Vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**. A continuación, expanda **[!UICONTROL Catalog]**en el panel izquierdo y seleccione **[!UICONTROL Inventory]**.

- Productos específicos: Vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**. A continuación, abra el producto en modo de edición y haga clic en **[!UICONTROL Advanced Inventory]** en el _[!UICONTROL Sources]_sección.

El catálogo se puede configurar para que muestre los datos de inventario en la tienda, administre los carros de compras activos y mucho más. Mostrar la disponibilidad de cada artículo como _En stock_ o _Sin existencias_ y el inventario disponible cuando el stock es bajo.

El umbral de falta de existencias indica cuándo se debe reordenar un producto, resta de la cantidad vendible de un inventario y se puede establecer para admitir pedidos pendientes habilitados o deshabilitados. Permitir pedidos pendientes para su tienda, estableciendo una cantidad máxima de pedidos para todos los productos o productos específicos.

Otra forma de utilizar el umbral de disponibilidad de existencias es administrar los productos con mucha demanda. Si deseas capturar nuevos clientes, en lugar de venderlos a compradores de gran cantidad, puedes establecer una cantidad máxima para evitar que un solo comprador saque todo el inventario.

![Ejemplo de En existencia, solo queda 1](assets/storefront-stock-options-1-left.png)

## Opciones de configuración

[!DNL Commerce] Las tiendas y los productos admiten las siguientes configuraciones para administrar productos, inventarios, notificaciones y mucho más. [!DNL Commerce] proporciona ajustes de configuración adicionales para acciones masivas y el algoritmo Prioridad de distancia.

| Opción | Descripción |
|--|--|
| [!UICONTROL Manage Stock] | Habilita [!DNL Commerce] para administrar todo el inventario. Establece si se usa el control de inventario para este producto o para todos los productos en [!DNL Commerce]. Muestra más opciones cuando se establece en `Yes`. |
| [!UICONTROL Only X left Threshold] | Establece una cantidad que se notifica cuando se deja una cantidad específica disponible para la compra. Esta cantidad se rastrea en el nivel de stock. |
| [!UICONTROL Out-of-Stock Threshold] | Su stock de seguridad, cantidad para el déclencheur de una notificación de Agotado y para mitigar el riesgo de agotamiento de existencias. Este valor afecta a los pedidos pendientes. Opciones:<br />**[!UICONTROL No Backorders]**: No acepta pedidos pendientes cuando el producto está agotado.<br />**[!UICONTROL Allow Qty Below 0]**: Acepta pedidos no satisfechos cuando la cantidad es inferior a cero.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: acepta pedidos no satisfechos cuando la cantidad es inferior a cero, pero notifica a los clientes que aún se pueden realizar pedidos.<br /><br />**[!UICONTROL Backorders disabled]**: se recomienda introducir un valor positivo superior a 0, como 5 o 25. <br/>**[!UICONTROL Backorders enabled]**: introduzca un umbral negativo para la cantidad máxima de pedidos pendientes permitidos, como -5 o -25. Un valor de 0 actúa como stock infinito. Un valor positivo se ignora y se trata como 0. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Establece la cantidad mínima del producto que se puede comprar en un único pedido. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Establece la cantidad máxima del producto que se puede comprar en un único pedido. |
| [!UICONTROL Qty Uses Decimals] | Permite cantidades decimales, en lugar de números enteros, para la cantidad de un producto. Esta configuración es útil para los productos vendidos por peso, volumen o longitud. Especificado en el nivel de origen, calculado en el nivel de stock según los orígenes asignados. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Determina si las partes de un producto se pueden enviar por separado. Esta opción está visible cuando **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Indica si se permiten pedidos no satisfechos. Especificado en el nivel de origen, calculado en el nivel de stock según los orígenes asignados. Si está habilitado para permitir pedidos no satisfechos, establezca un valor negativo para el umbral de falta de existencias (consulte [Configuración de Pedidos No Satisfechas](backorders.md)) se recomienda. Opciones:<br />**[!UICONTROL No Backorders]**: No acepta pedidos pendientes cuando el producto está agotado.<br />**[!UICONTROL Allow Qty Below 0]**: Acepta pedidos no satisfechos cuando la cantidad es inferior a cero.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: acepta pedidos no satisfechos cuando la cantidad es inferior a cero, pero notifica a los clientes que aún se pueden realizar pedidos. |
| [!UICONTROL Notify for Quantity Below] | Establece la cantidad que déclencheur una notificación Quantity below, con advertencia de stock bajo. Este importe se deduce de la cantidad vendible, no de la cantidad de inventario. |
| [!UICONTROL Enable Qty Increments] | Determina si el producto se puede vender en incrementos de cantidad. Si está activado, introduzca la cantidad de productos que deben adquirirse en un paso incremental. Los incrementos establecen cuántos artículos de producto deben comprarse como un solo producto y como un elemento secundario de productos configurables, agrupados y agrupados. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | [!DNL Inventory Management] no utiliza este valor. Al finalizar una devolución o una nota de abono, la cantidad del producto se devuelve automáticamente a la cantidad de origen afectada. Consulte [Configuración de opciones de producto](product-options.md). |

## Restauración y herencia de la configuración

Las configuraciones anulan o se aplican en la siguiente ruta de herencia: Producto _[!UICONTROL Sources]_La sección anula el producto_[!UICONTROL Advanced Options]_ invalida global _[!UICONTROL Inventory]_configuración de la tienda.

Cuándo [!DNL Commerce] comprueba la aplicación de la configuración personalizada; sigue este orden:

1. Comprueba la configuración personalizada en el nivel de producto en _[!UICONTROL Sources]_sección. Hay algunos ajustes disponibles.

1. Comprueba el producto _[!UICONTROL Advanced Inventory]_configuración.

1. If `Use Config Settings` se selecciona para la configuración del producto, comprueba si hay un valor de la configuración global _Inventario_ página de configuración de tienda.

Por ejemplo, puede configurar pedidos pendientes de forma diferente en su tienda con una configuración similar a la siguiente:

- _Globalmente:_ Activar pedidos no satisfechos para la tienda, establecer el umbral de existencias en `-50`

- _Producto:_ Deshabilite los pedidos no satisfechos de un producto específico, establezca el umbral de stock en `10`
