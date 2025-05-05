---
title: 'Categorías: configuración de diseño'
description: Obtenga información acerca del uso de la configuración de [!UICONTROL Design] para definir el aspecto de una categoría, todas las páginas de productos asociadas y el diseño de página.
exl-id: 6dc216ac-1c52-4196-9c93-e5cad19901b5
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Categorías: configuración de diseño

La sección _[!UICONTROL Design]_&#x200B;le proporciona control sobre el aspecto de una categoría, todas las páginas de productos asociadas y el diseño de página. Puede personalizar una página de categoría y sus productos asociados para una promoción o diferenciar la categoría. Por ejemplo, puede desarrollar un diseño distintivo para una marca o línea especial de productos, o aplicar una actualización durante un período de tiempo específico.

![Configuración de diseño para una categoría](./assets/category-design.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Cuando el mismo producto se asigna a varias categorías con diferentes configuraciones de diseño para cada categoría, se recomienda establecer **Usar ruta de acceso de las categorías para las direcciones URL del producto** = `Yes` en las [opciones de configuración de optimización del motor de búsqueda](../configuration-reference/catalog/catalog.md#search-engine-optimization). Para obtener acceso a esta configuración, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**, expanda **[!UICONTROL Catalog]**&#x200B;y elija **Catálogo**&#x200B;en el panel izquierdo y, a continuación, expanda la sección **Optimización del motor de búsqueda**&#x200B;de la página.

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Use Parent Category Settings] | Permite que la categoría actual herede la configuración de diseño de la categoría principal. Si se utiliza, el resto de campos de la sección Diseño dejan de estar disponibles. Opciones: `Yes` / ` No` |
| [!UICONTROL Theme] | Aplica una temática personalizada a la categoría. |
| [!UICONTROL Layout] | Aplica un diseño diferente a la página de categoría. Opciones: <br/>**[!UICONTROL No layout updates]**: de forma predeterminada, las actualizaciones de diseño no están disponibles para las páginas de categoría.<br/>**[!UICONTROL Empty]**: utilice para definir su propio diseño de página. (Requiere conocimientos de XML). <br/>**[!UICONTROL 1 column]**: aplica un diseño de una columna a la página de categoría.<br/>**[!UICONTROL 2 columns with left bar]**: aplica un diseño de dos columnas con una barra lateral izquierda a la página de categoría. <br/>**[!UICONTROL 2 columns with right bar]**: aplica un diseño de dos columnas con una barra lateral derecha a la página de categoría.<br/>**[!UICONTROL 3 columns]**: aplica un diseño de tres columnas a la página de categoría.<br/>**[!UICONTROL Page -- Full Width]**- (Requiere [Page Builder](../page-builder/introduction.md)) Aplica el diseño de ancho completo de las páginas de CMS a la página de categoría.<br/>**[!UICONTROL Category -- Full Width]** - (Requiere Page Builder) Aplica el diseño de ancho completo para las páginas de categoría a la página de categoría. <br/>**[!UICONTROL Product -- Full Width]**- (Requiere Page Builder) Aplica el diseño de ancho completo para las páginas de productos a la página de categoría. |
| [!UICONTROL Custom Layout Update] | Enumera los archivos de actualización de diseño personalizado disponibles en el servidor. Elija la actualización de diseño personalizado que desee aplicar a la categoría. |
| [!UICONTROL Apply Design to Products] | Cuando se selecciona esta opción, se aplica la configuración personalizada a todos los productos de la categoría. |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Design Update]

{{ce-feature}}

La sección _[!UICONTROL Scheduled Design Update]_&#x200B;determina el intervalo de fechas en que se aplica un diseño personalizado a las páginas de categorías.

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | Determina el intervalo de fechas en que se aplicará un diseño personalizado a la categoría. |

![Actualización de diseño programada](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}
