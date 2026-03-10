---
title: Cierre de compra de invitado
description: Aprenda a habilitar las funciones de pago y envío de invitados en su tienda.
exl-id: ce25eba3-7503-46aa-a5cd-9b7d5662164b
feature: Checkout
source-git-commit: 347321ec5b0722f06240780136cb29816aab559f
workflow-type: tm+mt
source-wordcount: '237'
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
