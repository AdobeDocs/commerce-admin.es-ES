---
title: 'Categorías: configuración de diseño'
description: Obtenga información acerca del uso de la configuración de [!UICONTROL Design] para definir el aspecto de una categoría, todas las páginas de productos asociadas y el diseño de página.
exl-id: 6dc216ac-1c52-4196-9c93-e5cad19901b5
feature: Catalog Management, Categories, Page Content
TQID: https://experienceleague.adobe.com/cRTRPl-UTfAKXY8rmtVKlnAZooVWpTCjSkVSdNHXp28
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 379
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
| [!UICONTROL Layout] | Aplica un diseño diferente a la página de categoría. Opciones: <br/>**[!UICONTROL No layout updates]**: de forma predeterminada, las actualizaciones de diseño no están disponibles para las páginas de categoría.<br/>**[!UICONTROL Empty]**: úselo para definir su propio diseño de página. (Requiere conocimientos de XML.) <br/>**[!UICONTROL 1 column]**- Aplica un diseño de una columna a la página de categoría.<br/>**[!UICONTROL 2 columns with left bar]**: aplica un diseño de dos columnas con una barra lateral izquierda a la página de categoría. <br/>**[!UICONTROL 2 columns with right bar]**: aplica un diseño de dos columnas con una barra lateral derecha a la página de categoría.<br/>**[!UICONTROL 3 columns]**: aplica un diseño de tres columnas a la página de categoría.<br/>**[!UICONTROL Page -- Full Width]**- (Requiere [Page Builder](../page-builder/introduction.md)) Aplica el diseño de ancho completo para las páginas de CMS a la página de categoría.<br/>**[!UICONTROL Category -- Full Width]** - (Requiere Page Builder) Aplica el diseño de ancho completo para las páginas de categoría a la página de categoría. <br/>**[!UICONTROL Product -- Full Width]**: (requiere Page Builder) aplica el diseño de ancho completo para las páginas de productos a la página de categoría. |
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
