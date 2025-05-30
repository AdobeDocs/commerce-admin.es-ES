---
title: "Configurar  [!DNL Inventory Management] pedidos no satisfechos"
description: Aprenda a configurar los pedidos pendientes para admitir la venta de productos sin existencias.
exl-id: 2fe778df-781e-4cda-8b85-47cf973c9e94
feature: Inventory, Orders
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 0%

---

# Configurar [!DNL Inventory Management] pedidos pendientes

Los pedidos pendientes permiten que su tienda siga vendiendo productos después de que la cantidad alcance cero o esté efectivamente sin existencias. Cuando un pedido del cliente es un pedido pendiente, los fondos se autorizan y se capturan inmediatamente, el estado de procesamiento del pedido no cambia y el envío permanece en espera hasta que esté disponible el stock.

Según la tienda y las ventas, es posible que desee habilitar o deshabilitar los pedidos pendientes en los siguientes niveles:

- **[!UICONTROL Global]**: todos los productos del catálogo en el nivel de sitio

- **[!UICONTROL Product]**: productos específicos que anulan la configuración del sitio, el origen y las existencias

## Comprender la configuración de pedidos pendientes

Se recomienda encarecidamente que configure umbrales y configuraciones específicos para admitir mejor los pedidos pendientes.

### Umbral de Agotado el stock

Use un valor negativo para este umbral para establecer la cantidad máxima de productos que se pueden poner en reserva antes de que el producto se considere verdaderamente agotado. Esta cantidad se suma a la cantidad vendible. El valor establecido en el nivel de producto anula cualquier valor establecido en el nivel global.

La fórmula para la cantidad vendible es `(Quantity - (Out-of-Stock Threshold))`.

El siguiente es un ejemplo:

- Cantidad: 25
- Notificar para la cantidad inferior: 10
- Solo X umbral izquierdo: 5
- Umbral de Agotado: -50

La cantidad vendible de este producto es `75 (25 - (-50))`.

![Ejemplo de cantidad vendible antes de pedidos pendientes habilitados](assets/inventory-backorders-before.png){width="600" zoomable="yes"}

![Ejemplo de cantidad vendible después de habilitar los pedidos pendientes](assets/inventory-backorders-after.png){width="600" zoomable="yes"}

Cuando los clientes compran los 25 productos disponibles, los nuevos pedidos se introducen como pedidos no satisfechos. A medida que la cantidad vendible del producto se reduce a 5 (se han vendido 70 artículos), la página _Producto_ muestra un mensaje `Only 5 left` en la tienda. Cuando la cantidad vendible alcanza `0`, el producto se muestra como `Out of Stock` en la tienda.

>[!NOTE]
>
>Cuando un cliente hace un pedido con _[!UICONTROL backorder qty]_, [!DNL Inventory Management] resta automáticamente la cantidad de la cantidad vendible. Si un pedido no se envía y se cancela, la cantidad vuelve a la cantidad virtual vendible agregada. La cantidad de pedido **_cancelado no se ha asignado a ninguno de los orígenes_**, pero se devuelve al número total de productos disponibles para la venta (columna&#x200B;_[!UICONTROL Salable Quantity]_ en la cuadrícula de productos).

<!--### Notify for Quantity Below JIRA MDVA-8099 MDVA-33783

The _Notify for Quantity Below_ configuration option is configurable at the global, source, and product levels. When it is enabled, the system sends an email notification when the product quantity reaches a level at or below the configured value. For this example, a notification is triggered when the product has a quantity of 10 or less. When backorders are enabled, _Notify for Quantity Below_ is determined by the Salable Quantity (`Salable Quantity = Quantity - (Out-of-Stock Threshold)`). -->

### Estado de stock

Los productos deben estar en estado `In Stock` al habilitar los pedidos no satisfechos. Puede establecer este valor desde la página _Product_. Para comerciantes de varios orígenes, debe haber al menos un origen marcado como `In Stock`. Acceda y establezca el estado a través de la página _Producto_ y la cuadrícula _Fuentes_ asignadas.

## Configurar pedidos pendientes globalmente

Estos pasos permiten pedidos pendientes de todos los productos en el nivel de sitio.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Establezca **[!UICONTROL Store View]** en `Default Config`.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Inventory]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Product Stock Options]**.

1. Para **[!UICONTROL Backorders]**, anule la selección de la casilla de verificación **[!UICONTROL Use system value]** y seleccione una opción:

   | Opción | Descripción |
   | -- | -- |
   | `No Backorders` | Para no aceptar pedidos pendientes cuando el producto esté agotado. |
   | `Allow Qty Below 0` | Para aceptar pedidos pendientes cuando la cantidad es inferior a cero. |
   | `Allow Qty Below 0 and Notify Customer` | Para aceptar pedidos pendientes cuando la cantidad es inferior a cero y notificar al cliente que se puede realizar el pedido. |

1. Para **[!UICONTROL Out-of-Stock Threshold]**, anule la selección de la casilla de verificación **[!UICONTROL Use system value]** e introduzca una cantidad diferente.

   | Valor | Descripción |
   | -- | -- |
   | Cantidad positiva | Con Pedidos no satisfechos desactivado, introduzca un valor positivo. |
   | Cero | Si se habilitan los pedidos no satisfechos, se pueden ingresar `0` pedidos no satisfechos infinitos. |
   | Importe negativo | Con los pedidos no satisfechos activados, se recomienda introducir un valor negativo. El importe se añade a la cantidad vendible. Por ejemplo, escriba `-50` para permitir pedidos de hasta esta cantidad. |

1. Haga clic en **[!UICONTROL Save Config]**.

## Configurar pedidos no satisfechos de un producto

Las configuraciones de nivel de producto anulan las configuraciones globales. Es posible que desee configurar los pedidos pendientes en el nivel de producto para anular la configuración en el nivel de origen o almacén global. Por ejemplo, es posible que su tienda admita pedidos no satisfechos a nivel global. Con la configuración del producto, puede deshabilitar los pedidos no satisfechos o cambiar el umbral de Agotado sin que ello afecte a otros productos y orígenes.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Abra un producto en modo **[!UICONTROL Edit]** y desplácese hacia abajo por la página hasta el área _[!UICONTROL Sources]_.

   En los productos configurados sin [!DNL Inventory Management], la ficha no aparece. El botón `Advanced Inventory` se muestra debajo del campo _[!UICONTROL Quantity]_.

1. Haga clic en **[!UICONTROL Advanced Inventory]**.

   Esta acción muestra una página de configuraciones específicas del producto. Cualquier configuración enumerada como `global` muestra la configuración global actual del almacén.

1. Para **[!UICONTROL Backorders]**, anule la selección de la casilla de verificación **[!UICONTROL Use Config Setting]** y seleccione una opción:

   | Opción | Descripción |
   | -- | -- |
   | `No Backorders` | Para no aceptar pedidos pendientes cuando el producto esté agotado. |
   | `Allow Qty Below 0` | Para aceptar pedidos pendientes cuando la cantidad es inferior a cero. |
   | `Allow Qty Below 0 and Notify Customer` | Para aceptar pedidos pendientes cuando la cantidad es inferior a cero y para notificar al cliente que aún se puede realizar el pedido. |

1. Para **[!UICONTROL Out-of-Stock Threshold]**, anule la selección de la casilla de verificación **[!UICONTROL Use Config Setting]** e introduzca una cantidad:

   | Valor | Descripción |
   | -- | -- |
   | Cantidad positiva | Con Pedidos no satisfechos desactivado, introduzca un valor positivo. |
   | Cero | Si se habilitan los pedidos no satisfechos, se pueden ingresar `0` pedidos no satisfechos infinitos. |
   | Importe negativo | Con los pedidos no satisfechos activados, se recomienda introducir un valor negativo. El importe se añade a la cantidad vendible. Por ejemplo, escriba `-50` para permitir pedidos de hasta esa cantidad. |

   ![Inventario avanzado configurado para pedidos pendientes](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Done]** y luego en **[!UICONTROL Save]**.
