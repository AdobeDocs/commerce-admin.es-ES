---
title: Archivar pedidos
description: Aprenda a configurar el archivo de pedidos para mejorar el rendimiento y optimizar Commerce para su organización.
exl-id: 12025591-bfe2-4f44-9358-a38ea4493b5c
feature: Orders, Configuration
source-git-commit: 47f170f1a1dd1c236b99c2e7139bb119368abf47
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# Archivar pedidos

{{ee-feature}}

El archivado regular de los pedidos mejora el rendimiento y mantiene su espacio de trabajo libre de información innecesaria, para que pueda centrarse en los negocios actuales. Las facturas, los envíos y las notas de abono se pueden archivar automática o manualmente y consultar en cualquier momento.

>[!NOTE]
>
>El _[!UICONTROL Archive]_opción aparece en la [[!UICONTROL Sales] menú](sales-menu.md) solo cuando el archivado está [activado](../configuration-reference/sales/sales.md).

## Configuración del archivo de pedidos

El almacén se puede configurar para archivar pedidos, facturas, envíos y notas de abono después de un número determinado de días. Puede mover las solicitudes y sus documentos asociados al archivo o restaurarlos a su estado anterior. Los pedidos archivados no se eliminan y permanecen disponibles desde el administrador. Los datos archivados se pueden exportar a un archivo CSV y abrirse en una hoja de cálculo. Cuando está activada, la variable _Archivar_ Esta acción aparece en la parte superior del espacio de trabajo.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Sales]** debajo.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]** sección.

   ![Configuración de archivado de pedidos, facturas, envíos y notas de abono](../configuration-reference/sales/assets/sales-orders-invoices-shipments-credit-memos-archiving.png){width="600" zoomable="yes"}

1. Establecer **[!UICONTROL Enable Archiving]** hasta `Yes`.

   >[!NOTE]
   >
   >Si posteriormente decide desactivar el archivado, todos los pedidos archivados se restauran al estado anterior.

1. Establecer **[!UICONTROL Archive Orders Purchased]** al número de días de espera antes de archivar los pedidos completados.

   De forma predeterminada, los pedidos se archivan 30 días después de la compra.

1. En el **[!UICONTROL Order Statuses to be Archived]** , seleccione cada estado de pedido que desee utilizar para identificar los pedidos que desea archivar.

   Para seleccionar varios elementos, mantenga presionada la tecla Ctrl (Windows) o Comando (Mac) mientras hace clic en cada elemento.

1. Haga clic **[!UICONTROL Save Config]**.

1. Cuando se le solicite, actualice cualquier caché no válida.

## Ver documentos archivados

1. En el _[!UICONTROL Sales]_menú debajo de_[!UICONTROL Archive]_, elija una de las siguientes opciones:

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. Para ver los detalles, haga clic en cualquier documento archivado de la lista.

## Aplicar una acción a un documento archivado

Seleccione cada documento para que sea el destinatario de la acción y elija una de las siguientes opciones **[!UICONTROL Actions]**:

- `Cancel`
- `Hold`
- `Unhold`
- `Print`
- `Move to Orders Management`

## Archivar documentos manualmente

1. Seleccione el tipo de documento que desea archivar de la siguiente manera:

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. Seleccione la casilla de verificación de cada elemento que desee archivar.

1. En la esquina superior derecha, establezca **[!UICONTROL Actions]** hasta `Move to Archive`.

1. Clic **[!UICONTROL Submit]** para archivar los documentos seleccionados.

## Restaurar documentos archivados

1. Elija el tipo de documento que desea restaurar.

1. Seleccione documentos mediante una de las siguientes opciones:

   - Para seleccionar todos los documentos visibles, en la esquina superior izquierda, haga clic en **[!UICONTROL Select Visible]**.

   - Seleccione manualmente la casilla de verificación de cada documento que desee restaurar.

1. En la esquina superior derecha, establezca **[!UICONTROL Action]** hasta `Move to Orders Management`.

1. Clic **[!UICONTROL Submit]** para restaurar los documentos.

## Exportar documentos archivados

1. Elija el tipo de documento que desea exportar.

1. En el menú superior derecho, seleccione **[!UICONTROL Export to:]** a uno de los siguientes valores:

   - `CSV`
   - `Excel`

1. Haga clic **[!UICONTROL Export]**.

El almacén se puede configurar para archivar pedidos, facturas, envíos y notas de abono después de un número determinado de días. Puede mover las solicitudes y sus documentos asociados al archivo o restaurarlos a su estado anterior. Los pedidos archivados no se eliminan y permanecen disponibles desde el administrador. Los datos archivados se pueden exportar a un archivo CSV y abrirse en una hoja de cálculo. Cuando está activada, la variable _[!UICONTROL Archive]_aparece un comando en la parte superior del espacio de trabajo.

## Archivar pedidos manualmente

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Para seleccionar el orden en la cuadrícula, active la casilla de verificación de la primera columna.

1. Configure las variables **[!UICONTROL Actions]** control a `Move to Archive` y busque el mensaje de que el pedido se ha archivado.

   ![Mover los pedidos seleccionados al archivo ](./assets/order-move-to-archive.png){width="700" zoomable="yes"}

>[!TIP]
>
>Para especificar una lista de los estados de pedidos que se pueden archivar, consulte [Configuración del archivo de pedidos](#configure-the-order-archive).

## Ver un pedido archivado

1. Abra la vista del archivo mediante uno de los siguientes métodos:

   - En la barra de botones situada encima de _[!UICONTROL Orders]_cuadrícula, haga clic en **[!UICONTROL Go to Archive]**.

   - En el _Administrador_ barra lateral, vaya a **[!UICONTROL Sales]** > _[!UICONTROL Archive]_>**[!UICONTROL Orders]**.

   >[!NOTE]
   >
   >Al igual que la página Pedidos, el título de la página de pedidos archivada es _[!UICONTROL Orders]_. La única diferencia notable es la opción de la barra de botones para_[!UICONTROL Return to Orders Management]_. La dirección URL de la página también indica que se encuentra en el archivo de pedidos.

1. En el _Acción_ , haga clic en **[!UICONTROL View]**.

   ![Ver un pedido archivado](./assets/order-archived-view.png){width="600" zoomable="yes"}

## Restaurar un pedido archivado

>[!NOTE]
>
>Un pedido restaurado a partir de un pedido archivado se vuelve a archivar según el número de días configurados en la [!UICONTROL Archive Orders Purchased] configuración (consulte [Configuración del archivo de pedidos](#configure-the-order-archive)). El número de días se calcula en función de la variable [!UICONTROL Updated At] fecha del pedido, que se cambia cuando el pedido se mueve del archivo.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. En la barra de botones, haga clic en **[!UICONTROL Go to Archive]**.

1. Busque el registro que desea restaurar y haga clic en la casilla de verificación para seleccionarlo.

   ![Seleccione el orden de restauración](./assets/order-archived-select-to-restore.png){width="600" zoomable="yes"}

1. Configure las variables **[!UICONTROL Actions]** valor de control a `Move to Order Management`.

Busque el mensaje de que el pedido archivado se ha eliminado del archivo.

## Exportar pedido archivado

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. En el menú de acción, haga clic en **[!UICONTROL Export]** y seleccione el formato deseado.
