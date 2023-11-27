---
title: Archivo de registro de acciones
description: Obtenga información sobre cómo configurar y ver el archivo de registro de acciones de administración.
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Archivo de registro de acciones

{{ee-feature}}

El administrador [acciones](action-log.md) archive enumera los archivos de registro CSV almacenados en el servidor. En la configuración, puede especificar cuánto tiempo se almacenan las entradas de registro y con qué frecuencia se archivan. De forma predeterminada, el nombre del archivo incluye la fecha actual en formato ISO:  `yyyyMMddHH`

>[!NOTE]
>
>El archivado de registros requiere un [trabajo cron](cron.md) para configurar.

## Configuración del archivo de registro

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL System]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Admin Actions Log Archiving]** y establezca estas opciones:

   - **[!UICONTROL Log Entry Lifetime, Days]** — Introduzca el número de días que desea conservar las entradas de registro en la base de datos antes de eliminarlas.
   - **[!UICONTROL Log Archiving Frequency]** — Definir como `Daily`, `Weekly`, o `Monthly`.

   ![Configuración avanzada: archivado de registros de acciones de administración](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   Para obtener una lista detallada de los ajustes de configuración, consulte [Archivado de registros de acciones de administración](../configuration-reference/advanced/system.md) en el _Referencia de configuración_.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Ver el archivo

En el _Administrador_ barra lateral, vaya a **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**.

![Archivo de registro de acciones](./assets/action-log-archive.png){width="600" zoomable="yes"}
