---
title: Integración de Adobe Stock
description: Integración de Adobe Stock con [!DNL Commerce] para acceder a innumerables recursos de medios para usarlos en su tienda.
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Integración de Adobe Stock

Para obtener acceso a un sinfín de recursos multimedia para su uso en su tienda, integre [Adobe Stock][adobe-stock] con [!UICONTROL Commerce].

![Resultados de búsqueda de Adobe Stock](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

El servicio Adobe Stock proporciona a las empresas acceso a millones de fotos, vectores, ilustraciones, vídeos, plantillas y recursos 3D de alta calidad, depurados y libres de derechos para todos sus proyectos creativos. [!DNL Commerce] los usuarios pueden buscar, previsualizar y otorgar licencias rápidamente a los recursos de Adobe Stock. Los usuarios también pueden guardarlos en el [almacenamiento de medios][media-storage], todo sin salir del espacio de trabajo de administración.

## Requisitos previos

Esta integración requiere:

- Un [Adobe Developer][dev-console] account
- Adobe Commerce o Magento Open Source, 2.3.4 o posterior

Para obtener licencias de imágenes de Adobe Stock se requiere:

- Un [cuenta Adobe][adobe-signin]
- A de pago [Adobe Stock][adobe-stock] plan asociado a la cuenta

## Integrar [!DNL Commerce] y ADOBE STOCK

La configuración de la integración de Adobe Stock para Adobe Commerce es un proceso de dos pasos:

1. [Creación de una integración de adobe.developer](#create-an-adobe-developer-integration) para generar una clave de API
1. [Configuración de la integración de Adobe Stock en el administrador de Commerce](#configure-the-adobe-stock-integration)

### Creación de una integración de Adobe Developer

1. Vaya a [Consola de Adobe Developer][dev-console].

1. En _[!UICONTROL Quick Start]_, haga clic en **[!UICONTROL Create new project]**.

1. En el _[!UICONTROL Project overview]_, haga clic en **[!UICONTROL Add API]**.

1. Seleccionar **[!UICONTROL Adobe Stock]** en la lista integraciones y haga clic en **[!UICONTROL Next]**.

1. Seleccione OAuth 2.0 **[!UICONTROL Web App]**.

1. Especifique el **[!UICONTROL redirect URI]**.

   El URI de redirección predeterminado está en el formulario `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`, como `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`, donde:

   - `${HOST}` es su [!DNL Commerce] nombre de dominio completo (por ejemplo, `https://store.myshop.com`).
   - `${ADMIN_URI}` es su [!DNL Commerce] URI de administrador (como `admin_hgkq1l`), que se puede recuperar ejecutando `magento info:adminuri`.

1. Especifique el **[!UICONTROL Redirect URI pattern]**, que es el mismo que el URI de redireccionamiento con dos diferencias:

   - Cualquier punto (`.`) debe tener dos barras invertidas (`\\`).
   - Añadir `.*` hasta el final del patrón.

   En el ejemplo del URI de redireccionamiento predeterminado anterior, sería `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`.

1. Haga clic **[!UICONTROL Next]**.

1. Revise los ámbitos disponibles y haga clic en **[!UICONTROL Save configured API]**.

1. En la página siguiente, copie su **[!UICONTROL Client ID]** (clave de API) y **[!UICONTROL Client secret]**.

   Esta información se utiliza en los pasos de la siguiente sección.

### Configuración de la integración de Adobe Stock

Para establecer la configuración del sistema en su [!DNL Commerce] Administrador, utilice el _Clave de API_ y _Secreto de cliente_ generadas en el [sección anterior][create-integration].

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL System]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** y haga lo siguiente:

   - Establecer **[!UICONTROL Enabled Adobe Stock]** hasta `Yes`.

   - Introduzca su **[!UICONTROL API Key (Client ID)]**.

   - Introduzca su **[!UICONTROL Client Secret]**.

   - Clic **[!UICONTROL Test Connection]** para validar las claves.

   ![Configuración avanzada: integración con Adobe Stock](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   Asigne unos segundos a la validación. Si las credenciales son válidas, debería ver un verde _Conexión correcta._ Mensaje.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
[media-storage]: media-storage.md
[dev-console]: https://developer.adobe.com/console/home
[create-integration]: #create-an-adobeio-integration
