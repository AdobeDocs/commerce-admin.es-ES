---
title: Bandeja de entrada de mensaje del administrador
description: Obtenga información acerca de la bandeja de entrada de mensajes del administrador, que proporciona mensajes importantes y útiles desde el Adobe y desde el [!DNL Commerce] sistema.
exl-id: c53bb0e4-9f18-4d40-8cc4-8c3b485f8d68
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Bandeja de entrada de mensaje del administrador

Su tienda recibe mensajes del Adobe con regularidad. Los mensajes se clasifican por importancia y pueden hacer referencia a actualizaciones del sistema, parches, nuevas versiones, mantenimiento programado o eventos próximos. El icono de campana del encabezado indica la cantidad de mensajes no leídos en la bandeja de entrada.

![Administrador - mensajes entrantes](./assets/admin-inbox-summary.png){width="700" zoomable="yes"}

El _[!UICONTROL Notifications]_La página enumera todos los mensajes clasificados por fecha. El_[!UICONTROL Action]_ Los comandos se pueden utilizar para marcar mensajes individuales como leídos, ver información más detallada o quitar el mensaje de la bandeja de entrada.

La configuración determina la frecuencia con la que se actualiza la bandeja de entrada y cómo se envían los mensajes. Si el administrador de la tienda tiene una URL segura, las notificaciones deben enviarse a través de HTTPS.

## Ver nuevos mensajes entrantes

1. Haga clic en **[!UICONTROL Notification]** en el encabezado y lea el resumen.

1. Realice una de las siguientes acciones:

   - Si es necesario, haga clic en el mensaje para mostrar el texto completo.
   - Para eliminar el mensaje, haga clic en el icono Eliminar a la derecha del mensaje.
   - Para mostrar la lista completa de Notificaciones, haga clic en **[!UICONTROL See All]**.

## Abordar un mensaje esencial

Para un mensaje de importancia crítica, realice una de las siguientes acciones:

- Haga clic **[!UICONTROL Read Details]**.
- Para cerrar el cuadro de alerta y mantener el mensaje activo, haga clic en **[!UICONTROL Close]**.

## Administración de las notificaciones

1. Realice una de las siguientes acciones para abrir la página Notificaciones:

   - Haga clic en **[!UICONTROL Notification]** en el encabezado. Si se muestran uno o más mensajes nuevos, haga clic en **[!UICONTROL See All]**.

   - En el _Administrador_ barra lateral, vaya a **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Notifications]**.

1. En el **[!UICONTROL Action]** , realice una de las siguientes acciones:

   - Para obtener más información, haga clic en **[!UICONTROL Read Details]** para abrir la página vinculada en una nueva ventana.

   - Para mantener el mensaje en la bandeja de entrada, haga clic en **[!UICONTROL Mark As Read]**.

     ![Administrador - Marcar las notificaciones seleccionadas como leídas](./assets/admin-notifications-mark-as-read.png){width="700" zoomable="yes"}

   - Para eliminar el mensaje, haga clic en **[!UICONTROL Remove]**.

1. Para aplicar una acción a varios mensajes, realice una de las siguientes acciones:

   - Seleccione la casilla de verificación de la primera columna para cada mensaje que desea administrar.
   - Para seleccionar varios mensajes, establezca **[!UICONTROL Mass Actions]** controle según sea necesario.

1. Configure las variables **[!UICONTROL Actions]** a una de las siguientes opciones:

   - `Mark as Read`
   - `Remove`

1. Clic **[!UICONTROL Submit]** para completar el proceso.

## Configuración de notificaciones

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel de navegación izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL System]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png)el **[!UICONTROL Notifications]** sección.

   ![Configuración de notificaciones](./assets/system-notifications.png){width="600"}

1. Si el administrador de la tienda ejecuta [URL segura](../stores-purchase/store-urls.md), configurado **[!UICONTROL Use HTTPS to Get Feed]** hasta `Yes`.

1. Establecer **[!UICONTROL Update Frequency]** para determinar con qué frecuencia se actualiza la bandeja de entrada.

   El intervalo puede ser de una a 24 horas.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

Para obtener más información sobre [!UICONTROL System] opciones de configuración, consulte las [_Guía de referencia de configuración_](../configuration-reference/advanced/system.md).
