---
title: '[!UICONTROL General] &gt; [!UICONTROL Content Management]'
description: Revise la configuración en la página [!UICONTROL General] &gt; [!UICONTROL Content Management] del administrador de Commerce.
exl-id: 67c5e89b-0a7c-4e4f-a5ad-10376c3ef6f9
feature: Configuration, Page Content
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Content Management]

{{config}}

## [!UICONTROL WYSIWYG Options]

![Opciones de WYSIWYG](./assets/content-management-wysiwyg-options.png)<!-- zoom -->

<!-- [WYSIWYG Options](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/wysiwyg/editor) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable WYSIWYG Editor] | Vista de tienda | Determina si el editor está habilitado para la tienda. Opciones: Habilitado por defecto/Deshabilitado por defecto/Deshabilitado por completo |
| [!UICONTROL WYSIWYG Editor] | Sitio web | Determina la versión del editor TinyMCE que se utiliza para el editor de WYSIWYG. Opciones: <br/>**`TinyMCE 5`**- (Predeterminado) Utiliza TinyMCE versión 5 como editor de WYSIWYG predeterminado.<br><br>_ **&#x200B; Nota:**&#x200B;_Una actualización de la biblioteca TinyMCE 5.10 en Adobe Commerce y el Magento Open Source 2.4.5 resuelve una vulnerabilidad que permitía la ejecución arbitraria de JavaScript al actualizar una imagen o un vínculo mediante algunos tipos de direcciones URL. TinyMCE 3 quedó obsoleto en la versión 2.4.0 y se eliminó en la versión 2.4.3. TinyMCE 4 se eliminó en la versión 2.4.4. |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | Global | Determina si se utilizan [direcciones URL estáticas](../../content-design/catalog-urls-dynamic-media.md) para el contenido multimedia al que se hace referencia desde el editor de WYSIWYG. La configuración se aplica a todos los lugares donde el editor de WYSIWYG está disponible, incluidos productos, categorías, páginas y bloques. Opciones: <br/>**`Yes`**: utiliza direcciones URL estáticas para el contenido multimedia insertado con el editor de WYSIWYG. Las direcciones URL estáticas son absolutas y se rompen si cambia la [dirección URL base](../../stores-purchase/store-urls.md) del almacén.<br/>**`No`** (predeterminado): utiliza direcciones URL dinámicas para el contenido multimedia insertado con el editor de WYSIWYG, según la directiva `{{media url="..."}}`. Las direcciones URL dinámicas son relativas y no se rompen si cambia la dirección URL base del almacén. |

{style="table-layout:auto"}

## [!UICONTROL CMS Page Hierarchy]

{{ee-feature}}

![Jerarquía de páginas de CMS](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--[CMS Page Hierarchy](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/pages/page-hierarchy) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | Global | Activa el uso de la jerarquía de páginas para las páginas de contenido. Opciones: `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | Global | Permite asociar metadatos con páginas de la jerarquía. Opciones: `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | Global | Determina el estilo de menú predeterminado. Opciones: `Content` / `Left Column` / `Right Column` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Content Tools]

![Herramientas de contenido avanzadas](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!-- [Advanced Content Tools](https://experienceleague.adobe.com/en/docs/commerce-admin/page-builder/walkthrough/3-catalog-content) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable Page Builder] | Global | Determina si están disponibles las herramientas de contenido avanzado [!DNL Page Builder]. Opciones: <br/>**`Yes`**- El área de trabajo [!DNL Page Builder] aparece en la sección Contenido de páginas, bloques, productos y categorías.<br/>**`No`**: las herramientas de edición estándar de CMS aparecen en la sección _[!UICONTROL Content]_&#x200B;de páginas, bloques, productos y categorías. |
| [!UICONTROL Enable Page Builder Content Preview] | Global | Determina si las [!DNL Page Builder] vistas previas de contenido están habilitadas para productos y categorías. Opciones: `Yes` / `No` <br/>**_Nota:_**&#x200B;Esto está establecido en `Yes` de forma predeterminada, pero desactivar la vista previa puede evitar cualquier problema de rendimiento que resulte de cargar vistas previas dentro de un formulario de producto o categoría. |
| [!UICONTROL Google Maps API Key] | Global | La clave de API [!DNL Google Maps] de su cuenta de Google. |
| [!UICONTROL Test Key] |  | Valida la clave de API [!DNL Google Maps]. |
| [!UICONTROL Google Maps Style] | Global | Pegue aquí el código JSON de estilo [!DNL Google Maps] para cambiar la apariencia del tipo de contenido Map. |
| [!UICONTROL Default Column Grid Size] | Global | Determina el número predeterminado de columnas en la cuadrícula [!DNL Page Builder]. |
| [!UICONTROL Maximum Column Grid Size] | Global | Determina el número máximo de columnas en la cuadrícula [!DNL Page Builder]. |

{style="table-layout:auto"}

>[!TIP]
>
>Page Builder facilita la creación de páginas con contenido enriquecido con diseños personalizados que mejoran la narración visual y aumentan la participación y lealtad de los clientes. Estas funciones están diseñadas para mejorar la calidad y reducir el tiempo y los gastos de producción de páginas personalizadas. Para obtener más información sobre estas funciones y cómo utilizarlas para crear contenido atractivo para tu tienda Adobe Commerce o Magento Open Source, consulta la [_Guía del usuario de Page Builder_](../../page-builder/guide-overview.md).
