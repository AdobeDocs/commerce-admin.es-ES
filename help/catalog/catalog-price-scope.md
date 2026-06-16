---
title: Alcance del precio
description: Obtenga información acerca del ámbito utilizado para los precios de los productos, que se pueden configurar para aplicarse a nivel global o de sitio web.
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/4tNRviXPzBubIpyAn9vgUs8BaILjJ6BEdV4yj5ngz6Y
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 376
ht-degree: 0%

---

# Alcance del precio

El ámbito de la [moneda base](../stores-purchase/currency-configuration.md) que se usa para los precios de los productos se puede configurar para que se aplique a nivel global o de sitio web. Si se aplica al nivel global, se utiliza el mismo precio en toda la jerarquía de la tienda. Si se aplica a nivel de sitio web, el mismo producto puede estar disponible a diferentes precios desde tiendas asociadas con diferentes sitios web. De forma predeterminada, el ámbito de los precios de los productos es global.

Diferentes factores pueden afectar el precio del mismo producto en una ubicación y no en otra. Por ejemplo, puede haber costes de distribución adicionales para el producto y otras consideraciones que afectan al precio de los productos vendidos en una tienda específica. El diagrama siguiente muestra una instalación de varios sitios con la moneda base establecida en el nivel de sitio web. Las tiendas y vistas de las tiendas asociadas a cada sitio web reflejan los precios de los productos establecidos en el nivel del sitio web.

![Adobe Commerce B2B](../assets/b2b.svg) Si usa catálogos compartidos, consulte [Establecer estructura y precios de catálogo compartido](../b2b/catalog-shared-pricing-structure.md) en la _Guía Adobe Commerce B2B_.

![Diagrama del ámbito del precio](./assets/catalog-price-scope.svg){width="550"}

## Configurar el ámbito de precios

1. En el menú _Administrador_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Desplácese hacia abajo hasta la sección **[!UICONTROL Price]** y establezca **[!UICONTROL Catalog Price Scope]** en una de las siguientes opciones:

   - `Global`
   - `Website`

   La configuración de ámbito que elija aparece debajo de los campos de precio en su catálogo.

   ![Ámbito de precio de catálogo](./assets/catalog-price.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Usar ámbito para configurar precios de productos

Commerce no permite establecer un precio de producto para cada tienda. Sin embargo, puede cambiar el precio por sitio web:

1. En el menú _Administrador_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. En la ficha **[!UICONTROL Price]**, establezca el ámbito de precio en `Website` en lugar de en `Global`.

1. Configure el precio abriendo la página de edición del producto, seleccionando el ámbito en la esquina superior izquierda y, a continuación, introduciendo un nuevo precio por sitio web.

En casos excepcionales, cuando el ámbito del precio está establecido en `Global`, la base de datos de Commerce puede tener precios diferentes en el nivel de sitio web. Esto puede ocurrir como resultado de problemas de sincronización fuera de Commerce. En estos casos, el comerciante debe realizar una limpieza de precios en el nivel de tienda y ejecutar una sincronización de catálogo con los servicios de Commerce.