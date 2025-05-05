---
title: '[!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings]'
description: Revise la configuración en la página [!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings] del administrador de Commerce.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

Esta configuración está disponible cuando [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html?lang=es) está instalado.

![Configuración de Sales Channel](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| Campo | [Ámbito](../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|-----|---------|------|
| [!UICONTROL Clear Log History] | Global | Opciones:<br/><br/>**`Once Daily`**: seleccione esta opción para borrar el historial de actividades de la tienda una vez al día.<br/><br/>**`Once Weekly`**: selecciona esta opción para borrar el historial de actividades de tu tienda una vez por semana.<br/><br/>**`Once Monthly`**: (Predeterminado) Seleccione esta opción para borrar el historial de actividades de su tienda una vez al mes. |
| [!UICONTROL Background Tasks (CRON) Source] | Global | Seleccione `Magento CRON` para especificar que [!DNL Amazon Sales Channel] usa la configuración de Commerce Cron para determinar los intervalos de comunicación y sincronización de datos con Amazon Seller Central. |
| [!UICONTROL Enable Debug Logging] | Global | Seleccione `Enabled` para recopilar datos de sincronización adicionales cuando sea necesario solucionar problemas.<br/><br/>Esta opción está deshabilitada de manera predeterminada y sólo debe habilitarse cuando sea necesario para solucionar problemas, ya que el registro continuo afecta negativamente al rendimiento. Si está habilitado para la resolución de problemas, debe deshabilitarse cuando se complete. |
| [!UICONTROL Read-Only Mode] | Global | Seleccione `Enabled` para bloquear todas las solicitudes de API salientes que cambian de estado. Los cambios potenciales se guardan, pero no se envían, hasta que se desactiva el modo de solo lectura. Para volver a iniciar las transferencias de datos, seleccione `Disabled`.<br/><br/>Cuando se migra una base de datos a una copia nueva de la instancia (se detecta cuando la dirección URL de un almacén cambia en la configuración), el modo de solo lectura se habilita automáticamente.<br/><br/>Está diseñado para utilizarse en copias de la instancia de producción, como _Ensayo_ o _Control de calidad_, y no debería usarse en la instancia de producción.<br/><br/>**_Nota _**: la caché de configuración debe borrarse para que [!UICONTROL Read-Only Mode] se habilite. |

{style="table-layout:auto"}
