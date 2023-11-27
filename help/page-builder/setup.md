---
title: '[!DNL Page Builder] setup'
description: Más información [!DNL Page Builder] Configuración de funciones de en Admin para Adobe Commerce y Magento Open Source.
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# [!DNL Page Builder] configurar

Cuando está habilitado en la configuración de, [!DNL Page Builder] es la herramienta de creación de contenido predeterminada para páginas CMS, bloques y bloques dinámicos. Además, la variable _[!UICONTROL Enable Advanced CMS]_ofertas de botones [!DNL Page Builder] como opción para Categorías y Productos. También puede elegir la opción predeterminada [diseño de página](../content-design/page-layout.md) que desee utilizar para páginas de productos, categorías y CMS. [!DNL Page Builder] no está disponible para el contenido de la newsletter, que utiliza el WYSIWYG [editor](../content-design/editor.md).

>[!NOTE]
>
>Una vez instalado, [!DNL Page Builder] anula la configuración predeterminada de [!UICONTROL Mask for Meta Description] campo de configuración. El valor cambia de `{{name}} {{description}}` hasta `{{name}}`.
><br>
>Puede acceder a esta configuración cuando vaya a [!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration], expanda [!UICONTROL Catalog]y elija [!UICONTROL Catalog] debajo. El [!UICONTROL Mask for Meta Description] está en el campo [!UICONTROL Product Fields Auto-generation] sección.

>[!NOTE]
>
>Un usuario administrador debe tener [!UICONTROL Content] permisos para su [ámbito de función](../systems/permissions-user-roles.md) para ver [!UICONTROL Edit with Page Builder] y poder usar Page Builder.

Para obtener más información sobre las opciones de configuración de las Herramientas avanzadas de administración de contenido, consulte la [_Guía de referencia de configuración_](../configuration-reference/general/content-management.md).

## Configurar [!DNL Page Builder]

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, debajo de _[!UICONTROL General]_, elija **[!UICONTROL Content Management]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** y compruebe que **[!UICONTROL Enable Page Builder]** se establece en `Yes`.

   ![Herramientas de contenido avanzadas](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. Si está listo para la configuración [!DNL Google Maps], haga lo siguiente:

   - Si es necesario, siga las [Obtener clave API][1] Instrucciones de, y después copie y pegue su **[!UICONTROL Google Maps API Key]**.

   - Para cambiar el **[!UICONTROL Google Maps Style]**, pegue el código JSON generado por el [[!DNL Google Maps] Asistente de estilo de API][2].

   >[!NOTE]
   >
   >Consulte [Medios: mapa](map.md) para obtener más información sobre el uso de [!DNL Google Maps] en su [!DNL Page Builder] contenido.

1. Para configurar el número de directrices en [!DNL Page Builder] , haga lo siguiente:

   - Para **[!UICONTROL Default Column Grid Size]**, introduzca el número predeterminado de columnas que desea que aparezcan en la cuadrícula.

   - Para **[!UICONTROL Maximum Column Grid Size]**, introduzca el número máximo de columnas que desea que estén disponibles en la cuadrícula.

   >[!NOTE]
   >
   >Consulte [Diseño: columna](column.md) para obtener más información sobre el uso de la cuadrícula de columnas al trabajar con su [!DNL Page Builder] contenido.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Configurar diseños predeterminados

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, debajo de _[!UICONTROL General]_, elija **[!UICONTROL Web]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]** y haga lo siguiente:

   ![Diseños predeterminados](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   Para obtener más información sobre las opciones de configuración web, consulte la [_Guía de referencia de configuración_](../configuration-reference/general/web.md#default-layouts).

   - Elija la **[!UICONTROL Default Product Layout]** que desee utilizar para las páginas de producto.

   - Elija la **[!UICONTROL Default Category Layout]** que desee utilizar para páginas de categoría.

   - Elija la **[!UICONTROL Default Page Layout]** que desee utilizar para páginas de CMS.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Deshabilitar [!DNL Page Builder]

>[!NOTE]
>
>Desactivando [!DNL Page Builder] reemplaza las herramientas de contenido avanzadas con el WYSIWYG [editor](../content-design/editor.md)y podrían provocar errores de visualización en la tienda. Contenido que ha creado anteriormente con [!DNL Page Builder] puede que no se pueda editar desde el administrador.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, debajo de _[!UICONTROL General]_, elija **[!UICONTROL Content Management]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** y establecer **[!UICONTROL Enable Page Builder]** hasta `No`.

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL Turn Off]**.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

1. Cuando se le solicite, [actualizar](../systems/cache-management.md) cualquier caché no válida.

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
[2]: https://mapstyle.withgoogle.com/
