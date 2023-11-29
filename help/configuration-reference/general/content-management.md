---
title: '[!UICONTROL General] &gt; [!UICONTROL Content Management]'
description: Revise la configuración de en [!UICONTROL General] &gt; [!UICONTROL Content Management] de la administración de Commerce.
exl-id: 67c5e89b-0a7c-4e4f-a5ad-10376c3ef6f9
feature: Configuration, Page Content
source-git-commit: 5eef49c10680a47574afe3d3ecfa430dca7ad9ff
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Content Management]

{{config}}

## [!UICONTROL WYSIWYG Options]

![Opciones WYSIWYG](./assets/content-management-wysiwyg-options.png)<!-- zoom -->

<!-- [WYSIWYG Options](https://docs.magento.com/user-guide/cms/editor.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable WYSIWYG Editor] | Vista de tienda | Determina si el editor está habilitado para la tienda. Opciones: Habilitado por defecto/Deshabilitado por defecto/Deshabilitado por completo |
| [!UICONTROL WYSIWYG Editor] | Sitio web | Determina la versión del editor TinyMCE que se utiliza para el editor WYSIWYG. Opciones: <br/>**`TinyMCE 5`**- (Predeterminado) Utiliza la versión 5 de TinyMCE como editor WYSIWYG predeterminado.<br><br>_** Nota:**_Una actualización de la biblioteca TinyMCE 5.10 en Adobe Commerce y Magento Open Source 2.4.5 resuelve una vulnerabilidad que permitía la ejecución arbitraria de JavaScript al actualizar una imagen o vínculo mediante algunos tipos de URL. TinyMCE 3 quedó obsoleto en la versión 2.4.0 y se eliminó en la versión 2.4.3. TinyMCE 4 se eliminó en la versión 2.4.4. |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | Global | Determina si [URL estáticas](../../content-design/catalog-urls-dynamic-media.md) se utilizan para contenido multimedia al que se hace referencia desde el editor WYSIWYG. La configuración se aplica a todos los lugares donde el editor WYSIWYG está disponible, incluidos productos, categorías, páginas y bloques. Opciones: <br/>**`Yes`**: utiliza direcciones URL estáticas para el contenido multimedia insertado con el editor WYSIWYG. Las direcciones URL estáticas son absolutas y se rompen si [URL base](../../stores-purchase/store-urls.md) de los cambios de almacén.<br/>**`No`** (Predeterminado): Utiliza direcciones URL dinámicas para el contenido multimedia insertado con el editor WYSIWYG, según el  `{{media url="..."}}` Directiva. Las direcciones URL dinámicas son relativas y no se rompen si cambia la dirección URL base del almacén. |

{style="table-layout:auto"}

## [!UICONTROL CMS Page Hierarchy]

{{ee-feature}}

![Jerarquía de páginas de CMS](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--[CMS Page Hierarchy](https://docs.magento.com/user-guide/cms/page-hierarchy.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | Global | Activa el uso de la jerarquía de páginas para las páginas de contenido. Opciones: `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | Global | Permite asociar metadatos con páginas de la jerarquía. Opciones: `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | Global | Determina el estilo de menú predeterminado. Opciones: `Content` / `Left Column` / `Right Column` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Content Tools]

![Herramientas de contenido avanzadas](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!-- [Advanced Content Tools](https://docs.magento.com/user-guide/cms/page-builder-workspace.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable Page Builder] | Global | Determina si la variable [!DNL Page Builder] hay disponibles herramientas de contenido avanzadas. Opciones: <br/>**`Yes`**- El [!DNL Page Builder] Workspace aparece en la sección Contenido de páginas, bloques, productos y categorías.<br/>**`No`** - Las herramientas de edición estándar de CMS aparecen en la _[!UICONTROL Content]_sección de páginas, bloques, productos y categorías. |
| [!UICONTROL Enable Page Builder Content Preview] | Global | Determina si la variable [!DNL Page Builder] las vistas previas de contenido están habilitadas para productos y categorías. Opciones: `Yes` / `No` <br/>**_Nota:_**Se establece en `Yes` de forma predeterminada, pero desactivar la vista previa puede evitar cualquier problema de rendimiento que se derive de cargar vistas previas dentro de un formulario de producto o categoría. |
| [!UICONTROL Google Maps API Key] | Global | El [!DNL Google Maps] Clave de API de su cuenta de Google. |
| [!UICONTROL Test Key] |  | Valida el [!DNL Google Maps] Clave de API. |
| [!UICONTROL Google Maps Style] | Global | Pegue el [!DNL Google Maps] Agregue estilo al código JSON aquí para cambiar la apariencia del tipo de contenido Mapa. |
| [!UICONTROL Default Column Grid Size] | Global | Determina el número predeterminado de columnas en la [!DNL Page Builder] rejilla. |
| [!UICONTROL Maximum Column Grid Size] | Global | Determina el número máximo de columnas en la [!DNL Page Builder] rejilla. |

{style="table-layout:auto"}

>[!TIP]
>
>Page Builder facilita la creación de páginas con contenido enriquecido con diseños personalizados que mejoran la narración visual y aumentan la participación y lealtad de los clientes. Estas funciones están diseñadas para mejorar la calidad y reducir el tiempo y los gastos de producción de páginas personalizadas. Para obtener más información sobre estas funciones y cómo puede utilizarlas para crear contenido atractivo para su tienda Adobe Commerce o Magento Open Source, consulte la [_Guía del usuario de Page Builder_](../../page-builder/guide-overview.md).
