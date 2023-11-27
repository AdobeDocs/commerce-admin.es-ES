---
title: "Habilitar [!DNL Inventory Management]"
description: Obtenga información sobre cómo habilitar [!DNL Inventory Management] a nivel de tienda global o producto.
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Activar [!DNL Inventory Management]

Para administrar el inventario de productos, habilite [!DNL Inventory Management] a nivel de tienda global o producto. Si la variable _Administrar stock_ está activada, [!DNL Inventory Management] realiza un seguimiento automático de las cantidades de productos disponibles para el sitio a través de las existencias y los orígenes configurados. Todas las funciones y opciones de comienzan a rastrear y generar informes cuando se habilitan, sin necesidad de configuración adicional.

Su empresa se ejecuta y se actualiza el inventario a la velocidad de las ventas. A medida que los clientes compran, recibe información exacta y actualizada sobre las existencias disponibles por canal de ventas y fuente. Las Cantidades Vendibles Disponibles se actualizan por stock cuando los clientes añaden productos al carro de compras y finalizan las compras, y cuando gestiona los pedidos, crea envíos y emite reembolsos. Llegadas de stock nuevo o transferido a sus fuentes, inmediatamente disponible para ventas en línea. Los pedidos pendientes se completan hasta umbrales especificados sin pedidos infinitos ni configuraciones adicionales. Además, puede introducir y completar envíos parciales o completos a través de uno o más orígenes con recomendaciones, lo que le proporciona un control completo sobre la satisfacción de pedidos y el inventario disponible.

>[!NOTE]
>
>De forma predeterminada, [!DNL Inventory Management] está habilitado al instalar o actualizar [!DNL Commerce]. Según sus necesidades comerciales, es posible que desee habilitar o deshabilitar el seguimiento [!DNL Inventory Management] dentro [!DNL Commerce].

Cómo funciona esta configuración en inventarios de un solo origen y de varios orígenes:

- Para usar [!DNL Inventory Management], habilitar _[!UICONTROL Manage Stock]_.

- [!UICONTROL Manage Stock] las opciones de configuración de nivel de producto anulan la configuración de la tienda.

- Para utilizar Order Management o servicios de terceros (como ERP), desactive [!UICONTROL Manage Stock].

- Si la configuración de nivel de producto utiliza el valor predeterminado del sistema, se anula la configuración de tienda.

Con [!DNL Inventory Management] si está activada, consulte lo siguiente para configurar todas las opciones:

- [Configuración de opciones globales](global-options.md) - Ajustes que afectan a todo el catálogo, considerados los ajustes por defecto del sistema.

- [Configuración de opciones de producto](product-options.md) : Configuración de un producto específico que anula las opciones globales.

## Habilitar o deshabilitar [!DNL Inventory Management]

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Inventory]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) _Opciones de stock de productos_ y configure:

   ![Opciones de stock de productos](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Para administrar el inventario y utilizar todo [!DNL Commerce] características, conjunto **[!UICONTROL Manage Stock]** hasta `Yes` (valor predeterminado).

   - Para deshabilitar [!DNL Inventory Management], anule la selección del **[!UICONTROL Use system value]** casilla de verificación y definir **[!UICONTROL Manage Stock]** hasta `No`.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Administrar existencias de una tienda

Consulte [Configurar opciones globales](global-options.md).

## Administración de existencias de un producto

Consulte [Configuración de opciones de producto](product-options.md).
