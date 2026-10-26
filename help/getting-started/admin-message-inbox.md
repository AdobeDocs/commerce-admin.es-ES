---
title: Bandeja de entrada de mensaje del administrador
description: Obtenga información acerca de la Bandeja de entrada de mensajes de administrador, que proporciona mensajes importantes y útiles de Adobe y del sistema [!DNL Commerce].
exl-id: c53bb0e4-9f18-4d40-8cc4-8c3b485f8d68
TQID: https://experienceleague.adobe.com/3RgVAR8efVGsjazQsH8-3Ohfw1h8SDuqLyCDzMYAAng
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: eec5be4541c143c34dd75cda1903990ac4b74f8c
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%
---
# Bandeja de entrada de mensaje del administrador

>[!NOTE]
>
>Para ver las notificaciones, solicitudes y anuncios de productos de Adobe Commerce as a Cloud Service en la navegación superior de Adobe Unified Experience, consulte [Ver notificaciones](admin-unified-experience.md#view-notifications). En este tema se describe la bandeja de entrada del mensaje del administrador de Commerce, no el panel de notificaciones de la interfaz de Adobe Unified Experience Platform.

Su tienda recibe mensajes de Adobe con regularidad. Los mensajes se clasifican por importancia y pueden hacer referencia a actualizaciones del sistema, parches, nuevas versiones, mantenimiento programado o eventos próximos. El icono de campana del encabezado indica la cantidad de mensajes no leídos en la bandeja de entrada.

![Administrador - mensajes entrantes](./assets/admin-inbox-summary.png){width="700" zoomable="yes"}

La página _[!UICONTROL Notifications]_enumera todos los mensajes clasificados por fecha. Los comandos_[!UICONTROL Action]_ se pueden usar para marcar mensajes individuales como leídos, ver información más detallada o quitar el mensaje de la bandeja de entrada.

La configuración determina la frecuencia con la que se actualiza la bandeja de entrada y cómo se envían los mensajes. Si el administrador de la tienda tiene una URL segura, las notificaciones deben enviarse a través de HTTPS.

## Ver nuevos mensajes entrantes

1. Haga clic en el icono **[!UICONTROL Notification]** en el encabezado y lea el resumen.

1. Realice una de las siguientes acciones:

   - Si es necesario, haga clic en el mensaje para mostrar el texto completo.
   - Para eliminar el mensaje, haga clic en el icono Eliminar a la derecha del mensaje.
   - Para mostrar la lista de notificaciones completa, haga clic en **[!UICONTROL See All]**.

## Abordar un mensaje esencial

Para un mensaje de importancia crítica, realice una de las siguientes acciones:

- Haga clic en **[!UICONTROL Read Details]**.
- Para cerrar el cuadro de alerta y mantener el mensaje activo, haga clic en **[!UICONTROL Close]**.

## Administración de las notificaciones

1. Realice una de las siguientes acciones para abrir la página Notificaciones:

   - Haga clic en el icono **[!UICONTROL Notification]** del encabezado. Si se muestran uno o más mensajes nuevos, haga clic en **[!UICONTROL See All]**.

   - En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Notifications]**.

1. En la columna **[!UICONTROL Action]**, realice una de las acciones siguientes:

   - Para obtener más información, haga clic en **[!UICONTROL Read Details]** para abrir la página vinculada en una nueva ventana.

   - Para mantener el mensaje en la bandeja de entrada, haga clic en **[!UICONTROL Mark As Read]**.

     ![Administrador - Marcar las notificaciones seleccionadas como leídas](./assets/admin-notifications-mark-as-read.png){width="700" zoomable="yes"}

   - Para eliminar el mensaje, haga clic en **[!UICONTROL Remove]**.

1. Para aplicar una acción a varios mensajes, realice una de las siguientes acciones:

   - Seleccione la casilla de verificación de la primera columna para cada mensaje que desea administrar.
   - Para seleccionar varios mensajes, establezca el control **[!UICONTROL Mass Actions]** según sea necesario.

1. Establezca el control **[!UICONTROL Actions]** en uno de los siguientes:

   - `Mark as Read`
   - `Remove`

1. Haga clic en **[!UICONTROL Submit]** para completar el proceso.

## Configuración de notificaciones

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel de navegación izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL System]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png)la sección **[!UICONTROL Notifications]**.

   ![Configuración de notificaciones](./assets/system-notifications.png){width="600"}

1. Si el administrador de su tienda usa [una URL segura](../stores-purchase/store-urls.md), establezca **[!UICONTROL Use HTTPS to Get Feed]** en `Yes`.

1. Establezca **[!UICONTROL Update Frequency]** para determinar la frecuencia con la que se actualiza la bandeja de entrada.

   El intervalo puede ser de una a 24 horas.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

Para obtener más información acerca de las opciones de configuración de [!UICONTROL System], consulte la [_Guía de referencia de configuración_](../configuration-reference/advanced/system.md).
