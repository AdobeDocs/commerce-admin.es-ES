---
title: Acciones masivas
description: Obtenga información sobre cómo configurar y ver el registro de acciones masivas.
exl-id: 3907d9ef-3592-4dbb-805f-97b79bafd8ab
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# Acciones masivas

{{ee-feature}}

El registro de acciones masivas registra los detalles de las operaciones masivas asincrónicas que se ejecutan en segundo plano, como la importación/exportación o la asignación de [precios personalizados](../b2b/catalog-shared-manage.md#update-custom-pricing) a varios productos en un [catálogo compartido](../b2b/catalog-shared.md).

![Registro de acciones en lotes](./assets/bulk-actions-log.png){width="600" zoomable="yes"}

## Configuración de acciones masivas

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL System]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Bulk Actions]** y establezca la opción para guardar el registro:

   **[!UICONTROL Days Saved in Log]**: escriba el número de días durante los cuales se guardarán las acciones masivas en un registro.

   ![Configuración avanzada: acciones masivas](../configuration-reference/advanced/assets/system-bulk-actions.png){width="600" zoomable="yes"}

   Para obtener una lista detallada de las opciones de configuración, consulte [_Acciones masivas_](../configuration-reference/advanced/system.md) en la _Referencia de configuración_.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Ver acciones masivas

1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Bulk Actions]**.

1. Busque la acción que desee en el registro.

1. En la columna _[!UICONTROL Action]_, haga clic en **[!UICONTROL Details]**.
