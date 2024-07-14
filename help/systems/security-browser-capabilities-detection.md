---
title: Detección de funcionalidades del explorador
description: Obtenga información sobre cómo configurar la detección de funcionalidades del explorador y mostrar un aviso si es necesario cambiar la configuración del explorador del cliente.
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Detección de funcionalidades del explorador

Al igual que la mayoría de los sitios web y aplicaciones de Internet, Adobe Commerce y Magento Open Source requieren que el explorador del visitante permita las cookies y JavaScript para realizar operaciones completas. Sin embargo, ocasionalmente el explorador del usuario está configurado con la configuración de privacidad más alta que evita tanto las cookies como JavaScript. La tienda se puede configurar para probar las capacidades del explorador de cada visitante y mostrar un aviso si es necesario cambiar la configuración.

- Si la configuración de privacidad del explorador no permite las cookies, puede configurar el sistema para que las redirija automáticamente a la página [Habilitar cookies](../content-design/pages.md#enable-cookies), que explica cómo realizar la configuración recomendada con la mayoría de los exploradores.
- Si la configuración de privacidad del explorador no permite JavaScript, puede configurar el sistema para que muestre el siguiente mensaje encima del encabezado de cada página.

Para obtener información técnica, consulte [Exploradores compatibles](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html#supported-browsers) en la _Guía de instalación_.

## Configuración de la detección de funcionalidades del explorador

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel de la izquierda debajo de _[!UICONTROL General]_, elija **[!UICONTROL Web]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Browser Capabilities Detection]** y haga lo siguiente:

   - Para mostrar instrucciones que explican cómo configurar el explorador para permitir cookies, establezca **[!UICONTROL Redirect to CMS-page if Cookies are Disabled]** en `Yes`.

   - Para mostrar un banner encima del encabezado cuando JavaScript esté deshabilitado en el explorador del usuario, establezca **[!UICONTROL Show Notice if JavaScript is Disabled]** en `Yes`.

   - Para mostrar un banner encima del encabezado cuando Almacenamiento local está deshabilitado en el explorador del usuario, establezca **[!UICONTROL Show Notice if Local Storage is Disabled]** en `Yes`.

   ![Configuración general: detección de capacidades del explorador web](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
