---
title: Configuración de envío
description: Aprenda a configurar las opciones de envío que definen el punto de origen y la política de envío de su tienda.
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# Configuración de envío

La configuración de envío establece el punto de origen de todos los envíos, la política de envío y la gestión de envíos a varias direcciones.

## Punto de origen

El punto de origen se utiliza para calcular el cargo por los envíos realizados desde su tienda o almacén, y también determina la tasa de impuestos para los productos vendidos. Al calcular [Impuestos UE](international-tax-guidelines.md#eu-tax-configuration), asegúrese de que la variable [Cálculo de Destino de Impuestos por Defecto](../configuration-reference/sales/tax.md) para cada vista de tienda corresponde al punto de origen de Configuración de envío.

![Origen](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Shipping Settings]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Origin]** y complete lo siguiente:

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address] (y la línea 2, si es necesario)

1. Haga clic **[!UICONTROL Save Config]**.

## Política de envío

Una política de envío debe explicar las reglas comerciales y las directrices de su empresa para los envíos. Por ejemplo, si tienes reglas de precios que tienen como déclencheur el envío gratuito, puedes explicar los términos en tu política de envío.

![Política de envío durante el cierre de compra](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

Para mostrar la política de envío durante el cierre de compra, complete Parámetros de la política de envío en la configuración. El texto aparece cuando los clientes hacen clic en _Consulte nuestra política de envío_ durante el cierre de compra.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Shipping Settings]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Shipping Policy Parameters]** sección.

1. Establecer **[!UICONTROL Apply Custom Shipping Policy]** hasta `Yes`.

1. Pegue o introduzca su **[!UICONTROL Shipping Policy]** en el cuadro de texto.

   >[!NOTE]
   >
   >Si utiliza un procesador de texto para componer el texto, asegúrese de guardar el documento como un archivo .txt para quitar los caracteres de control del texto. A continuación, copie y pegue el texto en el cuadro de texto Política de envío.

   ![Parámetros de política de envío](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. Haga clic **[!UICONTROL Save Config]**.

## Varias direcciones

Las opciones de envío de varias direcciones permiten a los clientes enviar un pedido a varias direcciones durante el cierre de compra y determinar el número máximo de direcciones a las que se puede enviar un pedido.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Multishipping Settings]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Options]** sección.

   ![Opciones de envío multidirección](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. Establecer **[!UICONTROL Allow Shipping to Multiple Addresses]** hasta `Yes`.

1. Introduzca el **[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]**.

1. Haga clic **[!UICONTROL Save Config]**.

>[!NOTE]
>
>![B2B para Adobe Commerce](../assets/b2b.svg) (B2B para Adobe Commerce) Para pedidos con varias direcciones de envío, la variable [Pago a cuenta](../b2b/enable-basic-features.md#configure-payment-on-account) el método de pago, incluso si está activado, no está disponible durante el proceso de pago.
