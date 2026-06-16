---
title: Configuración de presupuestos
description: Obtenga información acerca de la configuración de ofertas, que controla la cantidad de pedido mínima necesaria para las solicitudes de ofertas, la duración de las ofertas y los archivos adjuntos.
exl-id: 865f6624-df9b-4f78-abfa-1f9a3d82bc0d
feature: B2B, Companies, Configuration, Quotes
role: Admin
TQID: https://experienceleague.adobe.com/RenH7-cnfF8qVEqFQc7IPMVsIp0alug5OgvYlr5piTM
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 0%

---

# Configuración de presupuestos

Si las comillas están habilitadas en las [características B2B](enable-basic-features.md) generales, puede configurar la compatibilidad con las comillas en el Administrador. La configuración de oferta determina la cantidad mínima de pedido necesaria para las solicitudes de oferta, la duración de la oferta y los formatos de archivo admitidos para los archivos adjuntos.

>[!NOTE]
>
>Las opciones de configuración de oferta y la capacidad de usar las funciones de negociación de oferta se controlan mediante los [recursos de rol](../systems/permissions-user-roles.md#role-resources). Estos recursos de rol deben seleccionarse para el rol de usuario Administrador que se asigna a la cuenta de usuario Administrador. Para conceder acceso a las funciones de presupuesto en Admin, vaya a **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**, seleccione el rol y vaya a [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] en el árbol_ Recursos de rol _.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Quotes]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL General]** y haga lo siguiente:

   ![Configuración de presupuestos de ventas - general](./assets/quotes-general.png){width="700" zoomable="yes"}

   Consulte [Comillas](../configuration-reference/sales/quotes.md) en _Referencia de configuración_ para obtener una lista completa de las opciones de la característica Comillas y sus funciones.

   - Escriba **[!UICONTROL Minimum Amount]** en el carro de compras que debe satisfacerse antes de que se pueda enviar una solicitud de presupuesto.

   - Para **[!UICONTROL Minimum Amount Message]**, escriba el mensaje que desea que aparezca cuando el total del carro de compras no alcance la cantidad mínima requerida.

   - Para **[!UICONTROL Default Expiration Period]**, escriba el número de **[!UICONTROL days]**, **[!UICONTROL weeks]** o **[!UICONTROL months]** para que una oferta siga siendo válida.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Attached files]** y haga lo siguiente:

   - Para **[!UICONTROL File formats for upload]**, escriba el sufijo de cada tipo de archivo compatible con los archivos adjuntos a un presupuesto.

     Escriba cada sufijo de archivo en minúsculas y separado por una coma.

     De manera predeterminada, se admiten los siguientes formatos: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png` y `jpeg`

   - Para **[!UICONTROL Maximum file size]**, escriba el tamaño máximo de un archivo adjunto en megabytes.

     El valor que introduzca puede ser anulado por la configuración del servidor.

     ![Configuración de presupuestos de ventas - archivos adjuntos](./assets/quotes-attached-files.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
