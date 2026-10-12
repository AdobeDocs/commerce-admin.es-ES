---
title: Boletines y suscripciones
description: Obtenga información acerca de los boletines informativos y cómo habilitar esta función como herramienta promocional de bajo coste.
exl-id: ad4488c2-1b8b-4326-8486-743c75c5b9a6
feature: Customers, Communications
TQID: 'https://experienceleague.adobe.com/riYrvqQTvcEa2p9EQXv-oy3juefmg4pch20aOHDOoEQ'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 22bad240-8308-569b-a9d5-578f1ff890ca
    internal-label: Customers
  - id: bb03f6c4-cab9-560e-9d02-5816e1808d17
    internal-label: Communications
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%
---
# Boletines y suscripciones

La publicación periódica de un boletín se considera una de las herramientas de marketing más potentes y asequibles disponibles. Commerce permite publicar y distribuir boletines informativos a los clientes suscritos, además de herramientas para producir el boletín, crear y administrar la lista de suscriptores, desarrollar contenido y dirigir el tráfico a la tienda. También puede usar [jerarquía de páginas](../content-design/page-hierarchy.md) para crear un archivo de problemas pasados.

>[!NOTE]
>
>Puede añadir funcionalidades integrando su instancia de Commerce con un proveedor de servicios de newsletter de terceros y añadiendo extensiones. Para obtener más información, consulta [Commerce Marketplace](../getting-started/commerce-marketplace.md).

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
