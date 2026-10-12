---
title: Editor de WYSIWYG
description: Aprenda a utilizar el editor y a trabajar con contenido en una vista de _What You See Is What You Get_ (WYSIWYG).
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%
---
# Editor de WYSIWYG

El editor permite introducir y dar formato mientras se trabaja en una vista _What You See Is What You Get_ (WYSIWYG) del contenido. Si prefiere trabajar directamente con el código HTML subyacente, puede cambiar fácilmente los modos. El editor se puede usar para crear contenido para [páginas](pages.md), [bloques](blocks.md) y [descripciones de productos](../catalog/product-content.md). Cuando trabaje en los detalles del producto, acceda al editor haciendo clic en **[!UICONTROL Show / Hide Editor]**.

![Barra de herramientas del editor](./assets/editor-toolbar.png){width="700" zoomable="yes"}

En los temas siguientes se proporciona información detallada sobre el uso del editor:

- [Inserción de un vínculo](editor-insert-link.md)
- [Insertar una imagen](editor-insert-image.md)
- [Inserción de un widget](editor-widget.md)
- [Insertar una variable](editor-insert-variable.md)

## Configuración del editor

El editor de WYSIWYG está habilitado de forma predeterminada y se puede utilizar para editar contenido en páginas y bloques de CMS, así como en productos y categorías. Desde la configuración, puede activar o desactivar el editor y elegir usar direcciones URL estáticas en lugar de [dinámicas](../catalog/catalog-urls.md#dynamic-url) para el contenido multimedia en las descripciones de productos y categorías.

![Opciones de WYSIWYG](../configuration-reference/general/assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

>[!NOTE]
>
>TinyMCE ha sido reemplazado con Hugerte como el editor predeterminado de WYSIWYG en Magento 2.4.6 y versiones posteriores.

Para obtener una descripción detallada de todas las opciones de WYSIWYG, consulte [Administración de contenido](../configuration-reference/general/content-management.md) en la _Referencia de configuración_.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo bajo _[!UICONTROL General]_, elija **[!UICONTROL Content Management]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]**.

1. Establezca **[!UICONTROL Enable WYSIWYG Editor]** según sus preferencias.

   El editor está habilitado de forma predeterminada.

1. Establece **[!UICONTROL Static URLs for Media Content in WYSIWYG]** según tus preferencias para todo el [contenido multimedia](../catalog/catalog-urls.md#static-url) que se ingresó con el editor de WYSIWYG.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
