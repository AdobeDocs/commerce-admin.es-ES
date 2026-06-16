---
title: Integración de Adobe Stock
description: Integra Adobe Stock con tu instancia  [!DNL Commerce] para acceder a innumerables recursos multimedia para usarlos en tu tienda.
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
TQID: https://experienceleague.adobe.com/VwiTbOAj5V8s7OWtkq5hfoP4LcvNLPR9QaKStaCdArs
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c32adafa-ed01-4b31-997e-2413013911b0
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
source-wordcount: 427
ht-degree: 0%

---

# Integración de Adobe Stock

Para obtener acceso a innumerables recursos multimedia para usar en tu tienda, integra [Adobe Stock](https://stock.adobe.com) con [!UICONTROL Commerce].

![Resultados de búsqueda de Adobe Stock](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

El servicio Adobe Stock proporciona a las empresas acceso a millones de fotos, vectores, ilustraciones, vídeos, plantillas y recursos 3D de alta calidad, depurados y libres de derechos para todos sus proyectos creativos. Los usuarios de [!DNL Commerce] pueden buscar, previsualizar y obtener licencias de recursos de Adobe Stock rápidamente. Los usuarios también pueden guardarlos en [almacenamiento de medios](./media-storage.md), sin salir del área de trabajo de administración.

## Requisitos previos

Esta integración requiere:

- Una cuenta de [Adobe Developer](https://developer.adobe.com/console/home)
- Adobe Commerce o Magento Open Source, 2.3.4 o posterior

Para obtener licencias de imágenes de Adobe Stock se requiere:

- Una [cuenta de Adobe](https://helpx.adobe.com/es/manage-account/using/access-adobe-id-account.html)
- Un plan [Adobe Stock](https://stock.adobe.com) de pago asociado con la cuenta

## Integrar [!DNL Commerce] y Adobe Stock

La configuración de la integración de Adobe Stock para Adobe Commerce es un proceso de dos pasos:

1. [Crear una integración adobe.developer](#create-an-adobe-developer-integration) para generar una clave de API
1. [Configuración de la integración de Adobe Stock en el administrador de Commerce](#configure-the-adobe-stock-integration)

### Creación de una integración de Adobe Developer

1. Vaya a [Adobe Developer Console](https://developer.adobe.com/console/home).

1. En _[!UICONTROL Quick Start]_, haga clic en **[!UICONTROL Create new project]**.

1. En el bloque _[!UICONTROL Project overview]_, haga clic en **[!UICONTROL Add API]**.

1. Seleccione **[!UICONTROL Adobe Stock]** de la lista de integraciones y haga clic en **[!UICONTROL Next]**.

1. Seleccione OAuth 2.0 **[!UICONTROL Web App]**.

1. Especifique **[!UICONTROL redirect URI]**.

   El URI de redirección predeterminado tiene el formato `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`, como `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`, donde:

   - `${HOST}` es su [!DNL Commerce] nombre de dominio completo (por ejemplo, `https://store.myshop.com`).
   - `${ADMIN_URI}` es su URI de administrador [!DNL Commerce] (como `admin_hgkq1l`), que se puede recuperar ejecutando `magento info:adminuri`.

1. Especifique **[!UICONTROL Redirect URI pattern]**, que es el mismo que el URI de redireccionamiento, con dos diferencias:

   - Cualquier punto (`.`) debe ser de escape con dos barras invertidas (`\\`).
   - Agregar `.*` al final del patrón.

   Utilizando el ejemplo del URI de redireccionamiento predeterminado anterior, el patrón sería `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`

1. Haga clic en **[!UICONTROL Next]**.

1. Revise los ámbitos disponibles y haga clic en **[!UICONTROL Save configured API]**.

1. En la página siguiente, copie su **[!UICONTROL Client ID]** (clave de API) y **[!UICONTROL Client secret]**.

   Esta información se utiliza en los pasos de la siguiente sección.

### Configuración de la integración de Adobe Stock

Para establecer la configuración del sistema en su administrador de [!DNL Commerce], use la _clave de API_ y el _secreto de cliente_ generados en la [sección anterior](#create-an-adobeio-integration).

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL System]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** y haga lo siguiente:

   - Establezca **[!UICONTROL Enabled Adobe Stock]** en `Yes`.

   - Escriba su **[!UICONTROL API Key (Client ID)]**.

   - Escriba su **[!UICONTROL Client Secret]**.

   - Haga clic en **[!UICONTROL Test Connection]** para validar las claves.

   ![Configuración avanzada: integración de Adobe Stock](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   Asigne unos segundos a la validación. Si sus credenciales son válidas, debería ver una _conexión correcta verde._ Mensaje.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
