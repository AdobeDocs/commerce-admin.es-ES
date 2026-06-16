---
title: Búsqueda de direcciones al finalizar la compra
description: Aprenda a incluir la búsqueda de direcciones en el cierre de compra de su tienda.
exl-id: 8153c456-0848-4bb4-8deb-8219323344ed
feature: Checkout
TQID: https://experienceleague.adobe.com/fMrmhB3-kGvDKNBnI1PCUhndVN0RhQprpZGB6rjfo8o
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 434
ht-degree: 0%

---

# Búsqueda de direcciones al finalizar la compra

{{ee-feature}}

Sus clientes pueden tener muchas direcciones guardadas e información en su libreta de direcciones, especialmente clientes normales, que regresan o empresas que introducen varios pedidos y ubicaciones de envío. La visualización de muchas direcciones puede ralentizar considerablemente la carga y los procesos de cierre de compra, y dar como resultado una experiencia de compra negativa. Para aumentar la capacidad de respuesta del cierre de compra, se recomienda activar y configurar la búsqueda de direcciones para el sitio.

>[!NOTE]
>
>La búsqueda de direcciones no está habilitada de forma predeterminada. Puede configurar esta función para incluir la funcionalidad en el sitio.

Cuando esta característica está habilitada y el número de direcciones guardadas del cliente cumple o supera el límite configurado, los pasos de _Envío_ y _Revisión y pagos_ muestran solo una dirección (la predeterminada). El cliente puede cambiar la dirección seleccionada haciendo clic en **Cambiar dirección** y luego buscando la dirección correcta por ciudad, estado, calle o código postal. Esta función también admite la selección de direcciones para el cierre de compra del registro de regalos.

![Cierre de compra con direcciones de envío guardadas mostradas](./assets/storefront-checkout-address-search.png){width="700" zoomable="yes"}

Si el cliente no tiene una dirección de envío predeterminada, la página _Envío_ muestra _Ninguna dirección seleccionada_. En este caso, el cliente debe hacer clic en **Cambiar dirección** para seleccionar una dirección guardada o hacer clic en **Nueva dirección** para agregar y seleccionar una dirección antes de continuar con el cierre de compra. Si el cliente no tiene una dirección de facturación predeterminada, la página _Revisión y pagos_ muestra la dirección seleccionada para el envío junto con la opción _Cambiar dirección_.

![Cierre de compra sin mensaje seleccionado de dirección](./assets/storefront-checkout-address-search-no-default.png){width="600" zoomable="yes"}

## Búsqueda de ofertas de direcciones bloqueadas

![Adobe Commerce B2B](../assets/b2b.svg) (disponible solo con Adobe Commerce B2B)

La activación de la búsqueda de direcciones también afecta al cierre de compra de pedidos creados a partir de ofertas en las que el número de direcciones guardadas del cliente cumple o supera el límite configurado. Cuando se completa la oferta y el cliente continúa con el cierre de compra, solo se muestra la dirección de envío seleccionada. La página también muestra un mensaje que indica que la dirección de envío está bloqueada y que solo se puede cambiar en la oferta.

![Dirección de envío bloqueada para un presupuesto](./assets/quote-checkout-shipping-address-locked.png){width="600" zoomable="yes"}

## Habilitar búsqueda de direcciones

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Checkout]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Checkout Options]**.

   ![Configuración - Opciones de cierre de compra](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

   Para obtener una descripción detallada de cada una de estas opciones de configuración, consulte [Opciones de desprotección](../configuration-reference/sales/checkout.md#checkout-options) en la _Guía de referencia de configuración_.

1. Establezca **[!UICONTROL Enable Address Search]** en `Yes`.

1. Para especificar el umbral para incluir la característica de búsqueda de direcciones, establezca la opción **[!UICONTROL Number of Customer Addresses Limit]**.

   Si es necesario, desactive la casilla de verificación **[!UICONTROL Use system value]** para realizar este cambio.

   Cuando el número de direcciones guardadas del cliente alcanza o supera este límite, la página muestra la dirección predeterminada (si el cliente tiene una) o _No se ha seleccionado ninguna dirección_ con la opción _Cambiar dirección_. El límite predeterminado es `10`.

1. Haga clic en **[!UICONTROL Save Config]**.
