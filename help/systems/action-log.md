---
title: Registros de acciones
description: Obtenga información acerca de los registros de acciones y cómo configurar las acciones registradas para que pueda realizar un seguimiento de todos los cambios realizados en la tienda.
exl-id: a482adfe-a63f-428b-b078-7542a1e2ecee
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Registros de acciones

{{ee-feature}}

La función Registros de acciones registra (registra) todos los cambios realizados por un usuario administrador que trabaja en su tienda. Esto le permite realizar un seguimiento de todos los cambios realizados en la tienda. Realizar un seguimiento de estos cambios, junto con la configuración [Permisos de administración](permissions.md) para un usuario, puede ayudar a proteger su tienda de cambios no deseados.

Para la mayoría de las acciones de administración, la información registrada incluye la acción, el nombre del usuario, el éxito o el error de la acción y el ID del objeto afectado por la acción. La dirección IP y la fecha también se registran.

De forma predeterminada, todas las acciones de administración están habilitadas y registradas. Para configurar el registro de acciones de administración, revise las opciones y active o desactive la casilla de verificación de cada tipo de acción. Adobe Commerce registra solo los tipos comprobados.

Ver el [Informe de registros de acciones](action-log-report.md) para revisar las acciones y los detalles de administración registrados.

![Configuración avanzada: registro de acciones de administración](../configuration-reference/advanced/assets/admin-actions-logging.png){width="600" zoomable="yes"}

Para obtener una lista detallada de los ajustes de configuración, consulte [Archivado de registros de acciones de administración](../configuration-reference/advanced/system.md) en el _Referencia de configuración_.

## Configurar acciones de administración para el registro

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL Admin]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Admin Actions Logging]** y haga lo siguiente para cada acción:

   - Para activar el registro de administrador para la acción, marque la casilla de verificación.
   - Para desactivar el registro de administración para la acción, desactive la casilla de verificación.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Archivar registro de acciones de administración

Los registros de acciones de administración se pueden archivar durante cualquier número de días. Los archivos también se pueden eliminar después de una duración especificada.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL System]**.

1. Expandir **[!UICONTROL Admin Action Log Archiving]** y defina las opciones:

   - **[!UICONTROL Logs Entry Lifetime, Days]** - Defina el número de días para conservar el registro archivado.
   - **[!UICONTROL Log Archiving Frequency]** - Establecer la frecuencia para la creación de archivos.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.
