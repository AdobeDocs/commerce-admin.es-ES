---
title: Configuración de visualización de precios
description: Obtenga información sobre la visualización de impuestos en el catálogo, el carro de compras, los pedidos, las facturas y los abonos que admiten la experiencia de compra del cliente.
exl-id: 6f97c474-ef6e-4ca6-899d-812c58b993ca
feature: Checkout, Invoices, Taxes
TQID: https://experienceleague.adobe.com/XIcN-vl8owiToGhM3Et2euyNWgnJdsgSl6urwJcRdLE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 519
ht-degree: 0%

---

# Configuración de visualización de precios

La configuración de visualización de precios determina si los precios de producto y envío incluyen o excluyen impuestos, o muestran dos versiones del precio: una con y otra sin impuestos.

Si el precio del producto incluye impuestos, el impuesto sólo aparece si hay una regla fiscal que coincida con el origen del impuesto o si una dirección de cliente coincide con la regla fiscal. Los eventos que pueden almacenar en déclencheur una coincidencia incluyen cuándo un cliente crea una cuenta, inicia sesión o genera una estimación de impuestos y envíos a partir del carro de compras.

>[!IMPORTANT]
>
>Mostrar precios que incluyen y excluyen impuestos puede ser confuso para el cliente. Para evitar activar un mensaje de advertencia, consulte las [directrices](international-tax-guidelines.md) de su país y [configuración recomendada](taxes.md#warning-messages) para evitar mensajes de advertencia.

![Configuración de visualización de precios](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

Para obtener una descripción detallada de cada una de estas opciones de configuración, consulte [Opciones de visualización de precios](../configuration-reference/sales/tax.md#price-display-settings) en la _Guía de referencia de configuración_.

## Configuración de la visualización de precios

Cuando finaliza la configuración del cálculo de impuestos, tasas y clases, los impuestos se calculan según esa configuración. Sin embargo, la visualización de impuestos en el catálogo, el carro de compras, los pedidos, las facturas y los abonos también debe configurarse para admitir la experiencia del cliente en la tienda.

Se recomienda mostrar los precios con los impuestos asociados (ya sean impuestos incluidos o ambos) para que los clientes sepan cómo se aplican estos cálculos antes de realizar un pedido.

### Paso 1: Configurar los precios de catálogo y la configuración de visualización

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Tax]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Price Display Settings]**.

1. Para **[!UICONTROL Display Product Prices in Catalog]**, elija una de las siguientes opciones:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

   >[!NOTE]
   >
   >Si establece esta opción en `Including Tax`, el impuesto sólo aparece si hay una regla fiscal que coincida con el origen del impuesto o si hay una dirección de cliente que coincida con la regla fiscal. Los eventos que pueden almacenar en déclencheur una coincidencia incluyen la creación de cuentas de cliente, el inicio de sesión o el uso de la herramienta de estimación de impuestos y envíos en el carro de compras.

1. Para **[!UICONTROL Display Shipping Prices]**, elija una de las siguientes opciones:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

Si elige mostrar ambos precios (con y sin impuestos), la tienda tiene un aspecto similar al siguiente:

![Ejemplo de visualización de precios que incluye impuestos en la tienda](./assets/catalog-prices-tax.png){width="700" zoomable="yes"}

### Paso 2: Configurar las opciones de visualización del carro de compras

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Shopping Cart Display Settings]**.

   ![Configuración de visualización del carro de compras](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Display Prices]**, elija una de las siguientes opciones:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Para **[!UICONTROL Display Subtotal]**, elija una de las siguientes opciones:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Para **[!UICONTROL Display Shipping Amount]**, elija una de las siguientes opciones:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Para **[!UICONTROL Display Gift Wrapping Prices]**, elija una de las siguientes opciones:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Para **[!UICONTROL Display Printed Card Prices]**, elija una de las siguientes opciones:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Para cada una de estas opciones restantes, cambie a `Yes` o `No` según sus preferencias:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

### Paso 3: Configuración del orden, la factura y la nota de abono

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]**.

   ![Configuración de visualización de pedidos, facturas y notas de abono](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Display Prices]**, elija una de las siguientes opciones:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Para **[!UICONTROL Display Subtotal]**, elija una de las siguientes opciones:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Para **[!UICONTROL Display Shipping Amount]**, elija una de las siguientes opciones:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Para **[!UICONTROL Display Gift Wrapping Prices]**, elija una de las siguientes opciones:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Para **[!UICONTROL Display Printed Card Prices]**, elija una de las siguientes opciones:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Para cada una de estas opciones restantes, cambie a `Yes` o `No` según sus preferencias:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
