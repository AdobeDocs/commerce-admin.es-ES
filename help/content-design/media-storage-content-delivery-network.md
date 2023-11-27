---
title: Uso de una red de entrega de contenido
description: Aprenda a utilizar una red de distribución de contenido (CDN) para almacenar archivos multimedia.
exl-id: cb612b79-f3e3-4f1b-8cf9-d47886486686
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Uso de una red de entrega de contenido

Se puede utilizar una red de entrega de contenido (CDN) para almacenar archivos multimedia. Adobe Commerce en la infraestructura en la nube incluye Fastly CDN (consulte [Rápido](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/fastly.html) en el _Guía de Commerce en la infraestructura de Cloud_). Se ha instalado una instancia de Commerce. _local_ no incluye una integración con ninguna CDN específica, puede utilizar la CDN de su elección.

Después de configurar la CDN, debe completar la configuración desde el Administrador. Los cambios se pueden realizar a nivel global o de sitio web. Cuando se utiliza una CDN para el almacenamiento de medios, todas las rutas a medios en páginas de la tienda de Commerce se cambian a las rutas de CDN especificadas en la configuración.

## Flujo de trabajo de CDN

1. **El explorador solicita medios** : Se abre una página de la tienda en el explorador del cliente y el explorador solicita el medio especificado en el HTML.
1. **Solicitud enviada a CDN; imágenes encontradas y servidas** : la solicitud se envía primero a la CDN. Si la CDN tiene las imágenes almacenadas, envía los archivos multimedia al explorador del cliente.
1. **Medios no encontrados, solicitud enviada a [!DNL Commerce] servidor web** : Si la CDN no tiene los archivos multimedia, la solicitud se envía a [!DNL Commerce] servidor web. Si los archivos multimedia se encuentran en el sistema de archivos, el servidor web los envía al explorador del cliente.

>[!IMPORTANT]
>
>Por motivos de seguridad, cuando se utiliza una CDN como almacenamiento de medios, es posible que JavaScript no funcione correctamente si la CDN está ubicada fuera del subdominio.

## Configuración de una red de entrega de contenido

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, debajo de _[!UICONTROL General]_, elija **[!UICONTROL Web]**.

1. En la esquina superior izquierda, establezca **[!UICONTROL Store View]** según sea necesario.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Base URLs]** y haga lo siguiente:

   ![Configuración general: URL de base web](./assets/web-base-urls.png){width="600" zoomable="yes"}

   - Actualice el **[!UICONTROL Base URL for Static View Files]** con la dirección URL de la ubicación de la CDN donde se almacenan los archivos de vista estática.

   - Actualice el **[!UICONTROL Base URL for User Media Files]** con la URL de los archivos JavaScript en la CDN.

     Ambos campos se pueden dejar en blanco o pueden comenzar con el marcador de posición: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Base URLs (Secure)]** y haga lo siguiente:

   ![Configuración general: direcciones URL de base web (seguras)](./assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - Actualice el **[!UICONTROL Secure Base URL for Static View Files]** con la dirección URL de la ubicación de la CDN donde se almacenan los archivos de vista estática.

   - Actualice el **[!UICONTROL Secure Base URL for User Media Files]** con la URL de los archivos JavaScript en la CDN.

     Ambos campos se pueden dejar en blanco o pueden comenzar con el marcador de posición: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.
