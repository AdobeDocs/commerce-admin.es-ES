---
title: "Configurar  [!DNL Inventory Management]"
description: Obtenga información acerca de la configuración de  [!DNL Inventory Management] opciones que determinan la disponibilidad de la fuente, los productos de la tienda y el envío de pedidos.
exl-id: 1696999e-77b1-45c7-9b0b-dd1512427cff
feature: Inventory, Configuration
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 0%

---

# Configurar [!DNL Inventory Management]

El módulo [!DNL Inventory Management] admite valores de configuración de inventario en el nivel de producto y global, y también proporciona valores adicionales que afectan a la disponibilidad del origen, los productos de tienda y el envío de pedidos. Los ajustes de configuración se aplican a:

- Todo el catálogo: Vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**. Luego expanda **[!UICONTROL Catalog]**&#x200B;en el panel izquierdo y seleccione **[!UICONTROL Inventory]**.

- Productos específicos: Vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**. A continuación, abra el producto en modo de edición y haga clic en **[!UICONTROL Advanced Inventory]** en la sección _[!UICONTROL Sources]_.

El catálogo se puede configurar para que muestre los datos de inventario en la tienda, administre los carros de compras activos y mucho más. Mostrar la disponibilidad de cada artículo como _En stock_ o _Agotado_ y el inventario disponible cuando el stock sea bajo.

El umbral de falta de existencias indica cuándo se debe reordenar un producto, resta de la cantidad vendible de un inventario y se puede establecer para admitir pedidos pendientes habilitados o deshabilitados. Permitir pedidos pendientes para su tienda, estableciendo una cantidad máxima de pedidos para todos los productos o productos específicos.

Otra forma de utilizar el umbral de disponibilidad de existencias es administrar los productos con mucha demanda. Si deseas capturar nuevos clientes, en lugar de venderlos a compradores de gran cantidad, puedes establecer una cantidad máxima para evitar que un solo comprador saque todo el inventario.

![Ejemplo de En existencia, solo queda 1](assets/storefront-stock-options-1-left.png)

## Opciones de configuración

[!DNL Commerce] tiendas y productos admiten las siguientes configuraciones para administrar productos, inventario, notificaciones y mucho más. [!DNL Commerce] proporciona opciones de configuración adicionales para acciones masivas y el algoritmo Prioridad de distancia.

| Opción | Descripción |
|--|--|
| [!UICONTROL Manage Stock] | Permite que [!DNL Commerce] administre todo el inventario. Establece si se usa el control de inventario para este producto o para todos los productos de [!DNL Commerce]. Muestra más opciones cuando se establece en `Yes`. |
| [!UICONTROL Only X left Threshold] | Establece una cantidad que se notifica cuando se deja una cantidad específica disponible para la compra. Esta cantidad se rastrea en el nivel de stock. |
| [!UICONTROL Out-of-Stock Threshold] | Su stock de seguridad, cantidad para el déclencheur de una notificación de Agotado y para mitigar el riesgo de agotamiento de existencias. Este valor afecta a los pedidos pendientes. Opciones:<br />**[!UICONTROL No Backorders]**: no acepta pedidos pendientes cuando el producto está agotado.<br />**[!UICONTROL Allow Qty Below 0]**: acepta pedidos no satisfechos cuando la cantidad cae por debajo de cero.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: acepta pedidos no satisfechos cuando la cantidad cae por debajo de cero, pero notifica a los clientes que aún se pueden realizar pedidos.<br /><br />**[!UICONTROL Backorders disabled]**: se recomienda escribir un valor positivo superior a 0, como 5 o 25. <br/>**[!UICONTROL Backorders enabled]**: escriba un umbral negativo para la cantidad máxima de pedidos pendientes permitidos, como -5 o -25. Un valor de 0 actúa como stock infinito. Un valor positivo se ignora y se trata como 0. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Establece la cantidad mínima del producto que se puede comprar en un único pedido. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Establece la cantidad máxima del producto que se puede comprar en un único pedido. |
| [!UICONTROL Qty Uses Decimals] | Permite cantidades decimales, en lugar de números enteros, para la cantidad de un producto. Esta configuración es útil para los productos vendidos por peso, volumen o longitud. Especificado en el nivel de Source, calculado en el nivel de stock en función de las fuentes asignadas. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Determina si las partes de un producto se pueden enviar por separado. Esta opción está visible cuando **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Indica si se permiten pedidos no satisfechos. Especificado en el nivel de Source, calculado en el nivel de stock en función de las fuentes asignadas. Si se habilita para permitir pedidos no satisfechos, se recomienda establecer un valor negativo para el umbral de falta de existencias (consulte [Configuración de pedidos no satisfechos](backorders.md)). Opciones:<br />**[!UICONTROL No Backorders]**: no acepta pedidos pendientes cuando el producto está agotado.<br />**[!UICONTROL Allow Qty Below 0]**: acepta pedidos no satisfechos cuando la cantidad cae por debajo de cero.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: acepta pedidos no satisfechos cuando la cantidad cae por debajo de cero, pero notifica a los clientes que aún se pueden realizar pedidos. |
| [!UICONTROL Notify for Quantity Below] | Establece la cantidad que déclencheur una notificación Quantity below, con advertencia de stock bajo. Este importe se deduce de la cantidad vendible, no de la cantidad de inventario. |
| [!UICONTROL Enable Qty Increments] | Determina si el producto se puede vender en incrementos de cantidad. Si está activado, introduzca la cantidad de productos que deben adquirirse en un paso incremental. Los incrementos establecen cuántos artículos de producto deben comprarse como un solo producto y como un elemento secundario de productos configurables, agrupados y agrupados. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | [!DNL Inventory Management] no utiliza este valor. Al finalizar una devolución o una nota de abono, la cantidad del producto se devuelve automáticamente a la cantidad de origen afectada. Consulte [Configuración de opciones de producto](product-options.md). |

## Restauración y herencia de la configuración

Las configuraciones anulan o aplican la siguiente ruta de herencia: La sección del producto _[!UICONTROL Sources]_&#x200B;anula la configuración del almacén&#x200B;_[!UICONTROL Advanced Options]_ global _[!UICONTROL Inventory]_.

Cuando [!DNL Commerce] comprueba si se aplica la configuración personalizada, sigue este orden:

1. Comprueba la configuración personalizada en el nivel de producto en la sección _[!UICONTROL Sources]_. Hay algunos ajustes disponibles.

1. Comprueba la configuración del producto _[!UICONTROL Advanced Inventory]_.

1. Si se selecciona `Use Config Settings` para la configuración del producto, se busca un valor en la página de configuración del almacén global _Inventario_.

Por ejemplo, puede configurar pedidos pendientes de forma diferente en su tienda con una configuración similar a la siguiente:

- _En general:_ Habilita los pedidos pendientes para la tienda, establece el umbral de falta de existencias en `-50`

- _Producto:_ Deshabilitar pedidos pendientes para un producto específico, establecer el umbral de falta de existencias en `10`
