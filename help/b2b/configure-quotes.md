---
title: Configuración de presupuestos
description: Obtenga información acerca de la configuración de ofertas, que controla la cantidad de pedido mínima necesaria para las solicitudes de ofertas, la duración de las ofertas y los archivos adjuntos.
exl-id: 865f6624-df9b-4f78-abfa-1f9a3d82bc0d
feature: B2B, Companies, Configuration, Quotes
role: Admin
source-git-commit: d4c3ea4b49e30ae3af249516d32fb28437d218b8
workflow-type: tm+mt
source-wordcount: '296'
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
