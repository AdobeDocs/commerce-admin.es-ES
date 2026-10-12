---
title: 'Categorías: configuración de visualización'
description: Obtenga información acerca del uso de la configuración [!UICONTROL Display] para definir qué elementos de contenido aparecen en una página de categoría y el orden en que aparecen los productos.
exl-id: bb3a1b00-ba56-4113-8208-860963612333
feature: Catalog Management, Categories, Page Content
TQID: 'https://experienceleague.adobe.com/t5UfvWvJ7R-kZb5kyMwpzwI2gfs3x3g1amlfWzQcAsw'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: 17d326fa-534a-55a5-b46f-8ae1de1e2f75
    internal-label: Page Content
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
    internal-label: Categories
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%
---
# Categorías: configuración de visualización

La configuración de visualización determina qué elementos de contenido aparecen en una página de categoría y el orden en que aparecen los productos. Puede habilitar bloques de CMS, establecer el estado de anclaje de la categoría y administrar las opciones de ordenación desde la pestaña _[!UICONTROL Display Settings]_. Para ver ejemplos de cómo se reflejan las categorías en la tienda, consulte [Navegación por el catálogo](navigation.md).

![Configuración de visualización para categorías](./assets/category-display-settings.png){width="600" zoomable="yes"}

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Display Mode] | Determina los elementos de contenido mostrados en la página de categoría. Opciones: `Products Only` / `Static Block Only` / `Static Block and Products` |
| [!UICONTROL Anchor] | Cuando se establece en `Yes`, muestra los productos de las subcategorías de la categoría aunque no se hayan agregado explícitamente a ella y habilita la visualización de la sección _[!UICONTROL filter by attribute]_&#x200B;en la navegación por capas. Opciones: `Yes` / `No` |
| [!UICONTROL Available Product Listing Sort By] | (Obligatorio) Los valores predeterminados son `Position`, `Name` y `Price`. Para personalizar la opción de ordenación, anule la selección de la casilla de verificación **[!UICONTROL Use All Available Attributes]** y seleccione los atributos que desee utilizar. Puede definir y agregar atributos según sea necesario. Esta configuración no se aplica al [!DNL Live Search] [widget de página de lista de productos](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Default Product Listing Sort By] | (Obligatorio) Para definir la opción predeterminada _[!UICONTROL Sort By]_, anule la selección de la casilla de verificación **[!UICONTROL Use Config Settings]**&#x200B;y seleccione un atributo. Esta configuración no se aplica al [!DNL Live Search] [widget de página de lista de productos](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Layered Navigation Price Step] | De forma predeterminada, Commerce muestra el rango de precios en incrementos de 10, 100 y 1000, según los productos de la lista. Para cambiar el rango del paso Precio, anule la selección de la casilla **[!UICONTROL Use Config Settings]**. |

{style="table-layout:auto"}
