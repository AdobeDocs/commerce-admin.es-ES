---
title: Configuración de [!DNL Page Builder]
description: Obtenga información acerca de la configuración de  [!DNL Page Builder] funciones en Admin para Adobe Commerce y Magento Open Source.
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
TQID: https://experienceleague.adobe.com/qXSCIQN-Tpo-n2CTrXy2xzDssA6xQfuWGAVxuRgI-5o
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 403
ht-degree: 0%

---

# Configuración de [!DNL Page Builder]

Cuando se habilita en la configuración, [!DNL Page Builder] es la herramienta de creación de contenido predeterminada para páginas de CMS, bloques y bloques dinámicos. Además, el botón _[!UICONTROL Enable Advanced CMS]_&#x200B;ofrece [!DNL Page Builder] como opción para Categorías y Productos. También puede elegir el [diseño de página](../content-design/page-layout.md) predeterminado que desee usar para productos, categorías y páginas de CMS. [!DNL Page Builder] no está disponible para el contenido de la newsletter, que usa el [editor](../content-design/editor.md) de WYSIWYG.

>[!NOTE]
>
>Cuando está instalado, [!DNL Page Builder] anula la configuración predeterminada del campo de configuración [!UICONTROL Mask for Meta Description]. El valor cambió de `{{name}} {{description}}` a `{{name}}`.
><br>>Puede acceder a esta configuración cuando vaya a [!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration], expanda [!UICONTROL Catalog] y elija [!UICONTROL Catalog] debajo. El campo [!UICONTROL Mask for Meta Description] se encuentra en la sección [!UICONTROL Product Fields Auto-generation].

>[!NOTE]
>
>Un usuario administrador debe tener permisos de [!UICONTROL Content] para su [ámbito de función](../systems/permissions-user-roles.md) para ver los botones de [!UICONTROL Edit with Page Builder] y poder usar Page Builder.

Para obtener más información acerca de las opciones de configuración de las Herramientas avanzadas de administración de contenido, consulte la [_Guía de referencia de configuración_](../configuration-reference/general/content-management.md).

## Configurar [!DNL Page Builder]

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo bajo _[!UICONTROL General]_, elija **[!UICONTROL Content Management]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** y compruebe que **[!UICONTROL Enable Page Builder]** está establecido en `Yes`.

   ![Herramientas de contenido avanzadas](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. Si está listo para configurar [!DNL Google Maps], haga lo siguiente:

   - Si es necesario, sigue las instrucciones de [Obtener clave API](https://developers.google.com/maps/documentation/javascript/get-api-key) y, a continuación, copia y pega tu **[!UICONTROL Google Maps API Key]**.

   - Para cambiar **[!UICONTROL Google Maps Style]**, pegue el código JSON generado por el [[!DNL Google Maps] Asistente para diseñar API](https://mapstyle.withgoogle.com/).

   >[!NOTE]
   >
   >Vea [Medios - Mapa](map.md) para obtener más información acerca del uso de [!DNL Google Maps] en el contenido de [!DNL Page Builder].

1. Para configurar el número de directrices en la cuadrícula de la columna [!DNL Page Builder], haga lo siguiente:

   - Para **[!UICONTROL Default Column Grid Size]**, escriba el número predeterminado de columnas que desea que aparezcan en la cuadrícula.

   - Para **[!UICONTROL Maximum Column Grid Size]**, escriba el número máximo de columnas que desea que estén disponibles en la cuadrícula.

   >[!NOTE]
   >
   >Vea [Diseño - Columna](column.md) para obtener más información acerca del uso de la cuadrícula de columnas al trabajar con el contenido de [!DNL Page Builder].

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Configurar diseños predeterminados

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo bajo _[!UICONTROL General]_, elija **[!UICONTROL Web]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]** y haga lo siguiente:

   ![Diseños predeterminados](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   Para obtener más información acerca de las opciones de configuración web, consulte la [_Guía de referencia de configuración_](../configuration-reference/general/web.md#default-layouts).

   - Elija el(la) **[!UICONTROL Default Product Layout]** que desea usar para las páginas de productos.

   - Elija el(la) **[!UICONTROL Default Category Layout]** que desee usar para páginas de categoría.

   - Elija el(la) **[!UICONTROL Default Page Layout]** que desea usar para las páginas de CMS.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Deshabilitar [!DNL Page Builder]

>[!NOTE]
>
>Al deshabilitar [!DNL Page Builder], se reemplazarán las herramientas de contenido avanzado con el [editor](../content-design/editor.md) de WYSIWYG, lo que podría provocar errores de visualización en la tienda. Es posible que el contenido que creó anteriormente con [!DNL Page Builder] no se pueda editar desde el Administrador.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo bajo _[!UICONTROL General]_, elija **[!UICONTROL Content Management]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** y establezca **[!UICONTROL Enable Page Builder]** en `No`.

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL Turn Off]**.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

1. Cuando se le solicite, [actualice](../systems/cache-management.md) cualquier caché no válida.
