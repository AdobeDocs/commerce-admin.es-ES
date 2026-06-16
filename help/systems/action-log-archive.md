---
title: Archivo de registro de acciones
description: Obtenga información sobre cómo configurar y ver el archivo de registro de acciones de administración.
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
TQID: https://experienceleague.adobe.com/xgyeoO5XJFZPopM9bsIn2oOtrxl4fyuEY2du5ryXeTY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 160
ht-degree: 0%

---

# Archivo de registro de acciones

{{ee-feature}}

El archivo de administración [actions](action-log.md) enumera los archivos de registro CSV almacenados en el servidor. En la configuración, puede especificar cuánto tiempo se almacenan las entradas de registro y con qué frecuencia se archivan. De forma predeterminada, el nombre de archivo incluye la fecha actual en formato ISO: `yyyyMMddHH`

>[!NOTE]
>
>El archivado de registros requiere que se configure un [trabajo cron](cron.md).

## Configuración del archivo de registro

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL System]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Admin Actions Log Archiving]** y establezca estas opciones:

   - **[!UICONTROL Log Entry Lifetime, Days]**: escriba el número de días que desea conservar las entradas de registro en la base de datos antes de quitarlas.
   - **[!UICONTROL Log Archiving Frequency]** — Se establece en `Daily`, `Weekly` o `Monthly`.

   ![Configuración avanzada: archivado del registro de acciones de administración](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   Para obtener una lista detallada de las opciones de configuración, consulte [Archivado del registro de acciones de administración](../configuration-reference/advanced/system.md) en la _Referencia de configuración_.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Ver el archivo

En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**.

![Archivo de registro de acciones](./assets/action-log-archive.png){width="600" zoomable="yes"}
