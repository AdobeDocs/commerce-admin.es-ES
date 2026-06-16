---
title: Configuración de devoluciones
description: Obtenga información sobre cómo habilitar las devoluciones para su tienda y configurar los métodos de envío admitidos.
exl-id: a1b508fc-7e42-4d37-bf7e-dea17a40d39b
feature: Returns, Configuration
TQID: https://experienceleague.adobe.com/TgVsqEceM-mTY91OCl7XRL0Uwk8VJAHatv0kHiOM00g
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 353
ht-degree: 0%

---

# Configuración de devoluciones

{{ee-feature}}

Cuando está activada, los clientes pueden enviar las solicitudes de RMA desde la tienda. Sólo se puede generar una autorización de devolución de material si hay un artículo en el pedido disponible para su devolución. Las solicitudes para devolver elementos individuales se administran mediante el atributo _Habilitar RMA_ en cada registro de producto. De manera predeterminada, los valores de configuración se aplican al producto (_[!UICONTROL Use Config Settings]_está seleccionado). Si_[!UICONTROL Enable RMA]_ está establecido en `No`, el producto no aparece en la lista de elementos que se pueden devolver. Si cambia la configuración de _Habilitar RMA_, se aplica tanto a los pedidos nuevos como a los existentes.

## Habilitar RMA para su tienda

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Sales]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL RMA Settings]**.

   ![Configuración de RMA](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Enable RMA on Storefront]** en `Yes`.

   Esta configuración determina si los clientes pueden crear y ver solicitudes de RMA desde la tienda. Las autorizaciones de devolución de material se pueden aplicar tanto a pedidos nuevos como existentes.

1. Establezca **[!UICONTROL Enable RMA on Product Level]** en `Yes`.

   Esta configuración determina el comportamiento del atributo _Habilitar RMA_ para productos individuales de la tienda:

   - Cuando [!UICONTROL Enable RMA on Product Level] se establece en `Yes`, los clientes de la tienda pueden devolver todos los productos individuales. Incluye valores de atributo de producto _[!UICONTROL Enable RMA]_= `Yes` y_[!UICONTROL Enable RMA]_ = `No`.
   - Cuando [!UICONTROL Enable RMA on Product Level] se establece en `No`, los clientes de la tienda solo pueden devolver los productos con un valor de atributo de producto _[!UICONTROL Enable RMA]_= `Yes`.

1. Establezca **[!UICONTROL Use Store Address]** en uno de los siguientes valores:

   - `Yes` - Enviar los productos devueltos a la dirección de la tienda.
   - `No`: escriba una dirección alternativa para las devoluciones de productos.

   ![Configuración de RMA con dirección alternativa](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save Config]**.

## Configuración de métodos de envío para devoluciones

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Delivery Methods]**.

1. Expanda la sección del transportista que desee utilizar para el servicio de devolución, como **[!UICONTROL UPS]**.

   ![Habilitar el servicio RMA para el operador](./assets/rma-delivery-method.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Enabled for RMA]** en `Yes`.

1. Haga clic en **[!UICONTROL Save Config]**.

## Cambiar las RMA permitidas en el nivel de producto

Si activa las RMA para su tienda y el catálogo contiene algunos productos que no deberían poder devolverse, puede modificar la configuración en el nivel de producto.

1. Abra el producto en modo de edición.

1. Desplácese hacia abajo y expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Autosettings]**.

1. Desactive la casilla de verificación **[!UICONTROL Use Config Setting]**, si es necesario.

1. Cambie la configuración de **[!UICONTROL Enable RMA]** a `No`.

   ![Deshabilitar RMA para un producto](./assets/product-advanced-autosettings-enable-rma.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save]**.
