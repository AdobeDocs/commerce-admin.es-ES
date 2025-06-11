---
title: Usar una base de datos de medios
description: Aprenda a utilizar una base de datos de medios para almacenar sus [!DNL Commerce] archivos multimedia.
exl-id: b59349fb-0cb6-4812-a126-6e0d8d37564f
feature: Page Content, Media, Configuration
level: Experienced
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Usar una base de datos de medios

>[!IMPORTANT]
>
>El método de almacenamiento de medios de la base de datos está obsoleto desde Adobe Commerce y Magento Open Source 2.4.3.

De forma predeterminada, todas las imágenes, los archivos CSS compilados y los archivos JavaScript compilados de la instancia [!DNL Commerce] se almacenan en el sistema de archivos del servidor web. Puede elegir almacenar estos archivos en una base de datos en un servidor de bases de datos. Una ventaja de este enfoque es la opción de sincronización automática y sincronización inversa entre el sistema de archivos del servidor web y la base de datos. Puede utilizar la base de datos predeterminada para almacenar medios o crear uno. Para poder usar una base de datos recién creada como almacenamiento de medios, debe agregar información sobre ella y sus credenciales de acceso al archivo `env.php`.

## Flujo de base de datos

1. **El explorador solicita los medios**: se abre una página de la tienda en el explorador del cliente y el explorador solicita los medios especificados en HTML.

1. **El sistema busca los medios en el sistema de archivos**. El sistema busca los medios en el sistema de archivos y, si se encuentran, los pasa al explorador.

1. **El sistema localiza el medio en la base de datos**. Si no se encuentra el medio en el sistema de archivos, se envía una solicitud del medio a la base de datos especificada en la configuración.

1. **El sistema localiza los medios en la base de datos**: un script PHP transfiere los archivos de la base de datos al sistema de archivos y los envía al explorador del cliente. La solicitud del explorador para los medios déclencheur el script para que se ejecute de la siguiente manera:

   - Si el servidor web [reescribe](../merchandising-promotions/url-rewrite.md) está habilitado para [!DNL Commerce] y es compatible con el servidor, el script PHP se ejecuta solamente cuando no se encuentra el medio solicitado en el sistema de archivos.
   - Si las reescrituras del servidor web están deshabilitadas para [!DNL Commerce] o no son compatibles con el servidor, el script PHP se ejecuta de todos modos, incluso si los medios necesarios están disponibles en el sistema de archivos.

## Usar una base de datos para el almacenamiento de medios

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL System]**.

1. En la esquina superior izquierda, establezca **[!UICONTROL Store View]** en `Default Config` para aplicar la configuración en el nivel global.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Storage Configuration for Media]** y haga lo siguiente:

   ![Configuración avanzada: configuración de almacenamiento para medios](./assets/database-storage-deprecated.png){width="600" zoomable="yes"}

   - Establezca **[!UICONTROL Media Storage]** en `Database`.

   - Establezca **[!UICONTROL Select Media Database]** en la base de datos que desee utilizar.

   - Para transferir los medios existentes a la base de datos recién seleccionada, haga clic en **[!UICONTROL Synchronize]**.

   - Escriba **[!UICONTROL Environment Update Time]** en segundos.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
