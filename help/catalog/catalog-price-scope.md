---
title: Alcance del precio
description: Obtenga información acerca del ámbito utilizado para los precios de los productos, que se pueden configurar para aplicarse a nivel global o de sitio web.
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 0%

---

# Alcance del precio

El ámbito de la [divisa base](../stores-purchase/currency-configuration.md) que se utiliza para que los precios del producto se puedan configurar para aplicarse en el nivel global o de sitio web. Si se aplica al nivel global, se utiliza el mismo precio en toda la jerarquía de la tienda. Si se aplica a nivel de sitio web, el mismo producto puede estar disponible a diferentes precios desde tiendas asociadas con diferentes sitios web. De forma predeterminada, el ámbito de los precios de los productos es global.

Diferentes factores pueden afectar el precio del mismo producto en una ubicación y no en otra. Por ejemplo, puede haber costes de distribución adicionales para el producto y otras consideraciones que afectan al precio de los productos vendidos en una tienda específica. El diagrama siguiente muestra una instalación de varios sitios con la moneda base establecida en el nivel de sitio web. Las tiendas y vistas de las tiendas asociadas a cada sitio web reflejan los precios de los productos establecidos en el nivel del sitio web.

![B2B para Adobe Commerce](../assets/b2b.svg) Si utiliza catálogos compartidos, consulte también [Establecer estructura y precios de catálogo compartido](../b2b/catalog-shared-pricing-structure.md) en el _Guía de B2B para Adobe Commerce_.

![Diagrama del ámbito del precio](./assets/catalog-price-scope.svg){width="550"}

## Configurar el ámbito de precios

1. En el _Administrador_ , vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Desplácese hacia abajo hasta el **[!UICONTROL Price]** sección y conjunto **[!UICONTROL Catalog Price Scope]** a uno de los siguientes:

   - `Global`
   - `Website`

   La configuración de ámbito que elija aparece debajo de los campos de precio en su catálogo.

   ![Precios de catálogo](./assets/catalog-price.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Usar ámbito para configurar precios de productos

Commerce no permite establecer un precio de producto para cada tienda. Sin embargo, puede cambiar el precio por sitio web:

1. En el _Administrador_ , vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. En el **[!UICONTROL Price]** pestaña, establecer el alcance del precio en `Website` en lugar de global.

1. Configure el precio abriendo la página de edición del producto, seleccionando el ámbito en la esquina superior izquierda y, a continuación, introduciendo un nuevo precio por sitio web.
