---
title: Habilitar  [!DNL Inventory Management]
description: Habilite o deshabilite [!DNL Inventory Management] y administre las existencias en el nivel de tienda o producto para controlar la cantidad vendible y el seguimiento de la satisfacción de pedidos.
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/evCX34nY-m7WQnZt3xw7ng6-It7Xlf5DTanjKbP1fCk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 464a5510b4215a8402f0180077ec313629de74af
workflow-type: tm+mt
source-wordcount: 309
ht-degree: 0%

---

# Habilitar [!DNL Inventory Management]

Para administrar el inventario de productos, habilite [!DNL Inventory Management] en el nivel de producto o almacén global. Cuando la opción _Administrar existencias_ está habilitada, [!DNL Inventory Management] realiza un seguimiento automático de las cantidades de productos disponibles para el sitio a través de las existencias y los orígenes configurados. Todas las funciones y opciones de comienzan a rastrear y generar informes cuando se habilitan, sin necesidad de configuración adicional.

Cuando [!DNL Inventory Management] está habilitado, el inventario se actualiza con su actividad de ventas:

- Las cantidades vendibles se actualizan por stock cuando los clientes agregan productos a los carros de compras, completan el cierre de compra y cuando envía o reembolsa pedidos.
- Las existencias nuevas o transferidas en un origen están disponibles para las ventas en línea después de actualizar las cantidades.
- Los pedidos pendientes respetan los umbrales configurados sin necesidad de una configuración adicional.
- Puede crear envíos parciales o completos desde uno o varios orígenes utilizando recomendaciones de algoritmo o la selección manual de origen.

>[!NOTE]
>
>De manera predeterminada, [!DNL Inventory Management] está habilitado al instalar o actualizar [!DNL Commerce]. Según sus necesidades comerciales, es posible que desee habilitar o deshabilitar el(la) [!DNL Inventory Management] rastreado(a) dentro de [!DNL Commerce].

Cómo funciona esta configuración en inventarios de un solo origen y de varios orígenes:

- Para usar [!DNL Inventory Management], habilite _[!UICONTROL Manage Stock]_.

- La configuración de [!UICONTROL Manage Stock] en el nivel de producto anula la configuración del almacén.

- Para usar Order Management o servicios de terceros (como ERP), deshabilite [!UICONTROL Manage Stock].

- Si la configuración de nivel de producto utiliza el valor predeterminado del sistema, se anula la configuración de tienda.

Con [!DNL Inventory Management] habilitado, consulte lo siguiente para configurar todas las opciones:

- [Configuración de opciones globales](global-options.md): opciones que afectan a todo el catálogo y que se consideran la configuración predeterminada del sistema.

- [Configuración de opciones de producto](product-options.md) - Configuración de un producto específico que anula las opciones globales.

## Habilitar o deshabilitar [!DNL Inventory Management]

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Inventory]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) _Opciones de productos_ y configure:

   ![Opciones de productos](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Para administrar el inventario y usar todas las características de [!DNL Commerce], establezca **[!UICONTROL Manage Stock]** en `Yes` (predeterminado).

   - Para deshabilitar [!DNL Inventory Management], anule la selección de la casilla de verificación **[!UICONTROL Use system value]** y establezca **[!UICONTROL Manage Stock]** en `No`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Administrar existencias de una tienda

Consulte [Configurar opciones globales](global-options.md).

## Administración de existencias de un producto

Consulte [Configuración de opciones de producto](product-options.md).
