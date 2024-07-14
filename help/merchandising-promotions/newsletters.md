---
title: Boletines y suscripciones
description: Obtenga información acerca de los boletines informativos y cómo habilitar esta función como herramienta promocional de bajo coste.
exl-id: ad4488c2-1b8b-4326-8486-743c75c5b9a6
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Boletines y suscripciones

La publicación periódica de un boletín se considera una de las herramientas de marketing más potentes y asequibles disponibles. Commerce permite publicar y distribuir boletines informativos a los clientes suscritos, además de herramientas para producir el boletín, crear y administrar la lista de suscriptores, desarrollar contenido y dirigir el tráfico a la tienda. También puede usar [jerarquía de páginas](../content-design/page-hierarchy.md) para crear un archivo de problemas pasados.

>[!NOTE]
>
>Puede añadir funcionalidades integrando su instancia de Commerce con un proveedor de servicios de newsletter de terceros y añadiendo extensiones. Para obtener más información, consulte [Commerce Marketplace](../getting-started/commerce-marketplace.md).

El primer paso para crear boletines es establecer la configuración de la newsletter para el sitio. Puede solicitar a los clientes que hagan clic en un vínculo de confirmación enviado por correo electrónico para confirmar la suscripción. Este método de inclusión doble requiere que los clientes confirmen dos veces que desean recibir la newsletter y reduce la posibilidad de que se considere correo no deseado.

## Habilitar boletines informativos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Newsletter]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL General Options]**.

1. Para habilitar los boletines para el ámbito de vista de tienda, establezca **[!UICONTROL Enabled]** en `Yes`.

Después de habilitar la función de boletín, aparece la sección _[!UICONTROL Subscription Options]_.

## Configuración de las opciones de suscripción

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Newsletter]**.

1. Si es necesario, [cambie el ámbito de configuración](../getting-started/websites-stores-views.md#scope-settings) para aplicar los cambios de configuración de la newsletter a una vista específica de un sitio o tienda.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Subscription Options]** y haga lo siguiente:

   ![Configuración de clientes - suscripciones a boletines](../configuration-reference/customers/assets/newsletter-subscription-options.png){width="600" zoomable="yes"}

   - Confirme la plantilla de correo electrónico y el remitente de cada uno de los siguientes mensajes de correo electrónico que se envían a los suscriptores:

      - [!UICONTROL Success email]
      - [!UICONTROL Confirmation email]
      - [!UICONTROL Unsubscribe email]

   - Para utilizar el proceso de inclusión doble para confirmar suscripciones, establezca **[!UICONTROL Need to Confirm]** en `Yes`.

   - Para permitir que las personas que no tengan una cuenta en su tienda se suscriban al boletín, establezca **[!UICONTROL Allow Guest Subscription]** en `Yes`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
