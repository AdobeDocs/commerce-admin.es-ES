---
title: '[!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings]'
description: Revise la configuración de en [!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings] de la administración de Commerce.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

Esta configuración está disponible cuando [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html) está instalado.

![Configuración de Sales Channel](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| Campo | [Ámbito](../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|-----|---------|------|
| [!UICONTROL Clear Log History] | Global | Opciones:<br/><br/>**`Once Daily`**: selecciona esta opción para borrar el historial de actividades de tu tienda una vez al día.<br/><br/>**`Once Weekly`**: selecciona esta opción para borrar el historial de actividades de tu tienda una vez por semana.<br/><br/>**`Once Monthly`**: (Predeterminado) Seleccione esta opción para borrar el historial de actividades de su tienda una vez al mes. |
| [!UICONTROL Background Tasks (CRON) Source] | Global | Seleccionar `Magento CRON` para especificar que la variable [!DNL Amazon Sales Channel] utiliza la configuración de Commerce Cron para determinar los intervalos de comunicación y sincronización de datos con Amazon Seller Central. |
| [!UICONTROL Enable Debug Logging] | Global | Seleccionar `Enabled` para recopilar datos de sincronización adicionales cuando sea necesario solucionar problemas.<br/><br/>Esta opción está deshabilitada de forma predeterminada y solo debe habilitarse cuando sea necesario para solucionar problemas, ya que el registro continuo afecta negativamente al rendimiento. Si está habilitado para la resolución de problemas, debe deshabilitarse cuando se complete.<br/><br/>**_Nota _**: el registro de Sales Channel de Amazon se escribe en `/var/log/channel_amazon.log` y se pueden ver en [modo de desarrollador](../systems/developer-tools.md#operation-modes). |
| [!UICONTROL Read-Only Mode] | Global | Seleccionar `Enabled` para bloquear todas las solicitudes de API salientes de cambio de estado. Los cambios potenciales se guardan, pero no se envían, hasta que se desactiva el modo de solo lectura. Para volver a iniciar las transferencias de datos, seleccione `Disabled`.<br/><br/>Cuando se migra una base de datos a una copia nueva de la instancia (se detecta cuando la dirección URL de un almacén cambia en la configuración), se activa automáticamente el modo de solo lectura.<br/><br/>Está diseñado para su uso en copias de la instancia de producción, como _Ensayo_ o _QA_, y no deben utilizarse en la instancia de producción.<br/><br/>**_Nota _**: la caché de configuración debe borrarse para [!UICONTROL Read-Only Mode] para habilitar. |

{style="table-layout:auto"}
