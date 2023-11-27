---
title: Configuración de diseño
description: La Configuración de diseño facilita la edición de las reglas y los ajustes de configuración relacionados con el diseño al mostrar los ajustes en una sola página.
exl-id: 43fec57f-d76d-45a9-812b-ba1947cea46d
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# Configuración de diseño

La configuración de diseño facilita la edición de las reglas y los ajustes de configuración relacionados con el diseño al mostrar los ajustes en una sola página.

![Página Configuración de diseño](./assets/configuration.png){width="700" zoomable="yes"}

## Cambio de la configuración de diseño

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Busque la vista de tienda que desee configurar y haga clic en **[!UICONTROL Edit]** en el _[!UICONTROL Action]_columna.

   La página muestra la configuración de diseño actual para la vista de tienda.

1. Para cambiar la temática predeterminada, establezca **[!UICONTROL Applied Theme]** al tema que desea aplicar a la vista.

   Si no se especifica ninguna temática, se utiliza la predeterminada del sistema. Algunas extensiones de terceros modifican el tema predeterminado del sistema.

1. Si la temática solo se va a utilizar para un dispositivo específico, establezca el **[!UICONTROL User Agent Rules]**.

   ![Reglas de usuario-agente](./assets/configuration-user-agent-rules.png){width="400" zoomable="yes"}

   Para cada tipo de dispositivo en el que desee especificar una temática:

   - Haga clic **[!UICONTROL Add New User Agent Rule]**.

   - Para **[!UICONTROL Search String]**, introduzca el ID de navegador del dispositivo específico.

     Una cadena de búsqueda puede ser una expresión normal o una expresión regular compatible con Perl (PCRE) (consulte [Agente de usuario](https://en.wikipedia.org/wiki/User_agent) para obtener más información). La siguiente cadena de búsqueda identifica a Firefox:

         /^mozilla/i
     
   - Para **[!UICONTROL Theme Name]**, elija el tema que desea utilizar para el dispositivo especificado.

   >[!NOTE]
   >
   >Puede agregar tantas reglas para los dispositivos que desee designar. Las cadenas de búsqueda coinciden en el orden en que se escriben.

1. En _[!UICONTROL Other Settings]_, expanda cada sección y siga las instrucciones de los temas vinculados para editar la configuración según sea necesario.

   - [[!UICONTROL Pagination]](../catalog/navigation-product-listings.md#pagination-controls)
   - [[!UICONTROL HTML Head]](page-setup.md#html-head)
   - [[!UICONTROL Header]](page-setup.md#header)
   - [[!UICONTROL Footer]](page-setup.md#footer)
   - [[!UICONTROL Search Engine Robots]](../merchandising-promotions/seo-overview.md#search-engine-robots)
   - [[!UICONTROL Product Image Watermarks]](../catalog/product-image.md#watermarks)
   - [[!UICONTROL Transactional Emails]](../systems/email-templates.md#configure-email-templates)

   ![Otras opciones que afectan al diseño](./assets/configuration-other-settings.png){width="500" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save Configuration]**.
