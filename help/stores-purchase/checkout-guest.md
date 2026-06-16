---
title: Cierre de compra de invitado
description: Aprenda a habilitar las funciones de pago y envío de invitados en su tienda.
exl-id: ce25eba3-7503-46aa-a5cd-9b7d5662164b
feature: Checkout
TQID: https://experienceleague.adobe.com/jxrHQ1knuqHBmM1DsVa9NqdV-XNFdQDWjvwW4kHEyYM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 247
ht-degree: 0%

---

# Cierre de compra de invitado

Tu tienda se puede configurar para que exija a los compradores que abran una cuenta antes de realizar una compra. La configuración predeterminada permite a los huéspedes realizar compras, con la opción de registrarse para obtener una cuenta después de completar el proceso de pago y envío.

![La tienda Luma muestra Desproteger como invitado](./assets/storefront-checkout-as-guest.png){width="600" zoomable="yes"}

**_Para deshabilitar la desprotección de invitados:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Checkout]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Checkout Options]**.

   ![Opciones de cierre de compra expandidas en la página de configuración](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

Para obtener una descripción detallada de cada una de estas opciones de configuración, consulte [Opciones de desprotección](../configuration-reference/sales/checkout.md#checkout-options) en la _Guía de referencia de configuración_.

1. Si la configuración es para una vista de tienda específica, [elija la vista de tienda](../configuration-reference/scope-change.md#set-the-scope) donde se aplica la configuración.

   Cuando se le solicite, haga clic en **[!UICONTROL OK]** para continuar.

1. Establezca **[!UICONTROL Allow Guest Checkout]** en `No`.

   Si es necesario, desactive la casilla de verificación **[!UICONTROL Use system value]** para habilitar los cambios en esta configuración.

1. Haga clic en **[!UICONTROL Save Config]**.

## Permitir el acceso de pedidos de invitados para correos electrónicos registrados

[!BADGE Solo SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Solo se aplica a proyectos de Adobe Commerce as a Cloud Service (infraestructura de SaaS administrada por Adobe)."}

Una configuración opcional en el nivel de tienda, que está desactivada de forma predeterminada, permite a los compradores invitados rastrear sus pedidos realizados con una dirección de correo electrónico que coincida con una cuenta de cliente registrada.

Cuando se habilita, los pedidos de pago y envío de invitados realizados con un correo electrónico registrado siguen siendo accesibles, y también aparecen en el historial de pedidos del cliente.

Para habilitar esta característica, vaya a **Tiendas** > Configuración > **Configuración** > Ventas > **Ventas** > **Cierre de compra para invitados** y establezca la opción **Permitir el acceso a pedidos de invitados para correos electrónicos registrados** en `Yes`.
