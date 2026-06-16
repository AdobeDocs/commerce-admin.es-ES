---
title: '[!UICONTROL Sales Channels] > [!UICONTROL Global Settings]'
description: Revise la configuración en la página [!UICONTROL Sales Channels] > [!UICONTROL Global Settings] del administrador de Commerce.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
TQID: https://experienceleague.adobe.com/jnjAspEdJbx3unjmoqgH12JEiLz4ThbgFGeFOArOonU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 225
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

Esta configuración está disponible cuando [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html) está instalado.

![Configuración de Sales Channel](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| Campo | [Ámbito](../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|-----|---------|------|
| [!UICONTROL Clear Log History] | Global | Opciones:<br/><br/>**`Once Daily`**: seleccione esta opción para borrar el historial de actividades de la tienda una vez al día.<br/><br/>**`Once Weekly`**: seleccione esta opción para borrar el historial de actividades de la tienda una vez a la semana.<br/><br/>**`Once Monthly`**: (Predeterminado) Seleccione esta opción para borrar el historial de actividades de la tienda una vez al mes. |
| [!UICONTROL Background Tasks (CRON) Source] | Global | Seleccione `Magento CRON` para especificar que [!DNL Amazon Sales Channel] usa la configuración de Commerce Cron para determinar los intervalos de comunicación y sincronización de datos con Amazon Seller Central. |
| [!UICONTROL Enable Debug Logging] | Global | Seleccione `Enabled` para recopilar datos de sincronización adicionales cuando sea necesario solucionar problemas.<br/><br/>Esta opción está deshabilitada de manera predeterminada y sólo debe habilitarse cuando sea necesario para solucionar problemas, ya que el registro continuo afecta negativamente al rendimiento. Si está habilitado para la resolución de problemas, debe deshabilitarse cuando se complete. |
| [!UICONTROL Read-Only Mode] | Global | Seleccione `Enabled` para bloquear todas las solicitudes de API salientes que cambian de estado. Los cambios potenciales se guardan, pero no se envían, hasta que se desactiva el modo de solo lectura. Para volver a iniciar las transferencias de datos, seleccione `Disabled`.<br/><br/>Cuando se migra una base de datos a una copia nueva de la instancia (detectada cuando cambia la dirección URL de un almacén en la configuración), el modo de sólo lectura se habilita automáticamente.<br/><br/>Está diseñado para utilizarse en copias de la instancia de producción, como _Ensayo_ o _Control de calidad_, y no debe usarse en la instancia de producción.<br/><br/>**_Nota _**: la caché de configuración debe borrarse para que [!UICONTROL Read-Only Mode] se habilite. |

{style="table-layout:auto"}
