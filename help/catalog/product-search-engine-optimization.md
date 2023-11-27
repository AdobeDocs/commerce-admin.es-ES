---
title: Configuración del producto - [!UICONTROL Search Engine Optimization]
description: Para un producto, la variable [!UICONTROL Search Engine Optimization] La configuración de establece la clave de URL y los metadatos que los motores de búsqueda utilizan para indexar el producto.
exl-id: 78888094-759c-4e45-afcd-65858ee76159
feature: Catalog Management, Products, Search
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# Configuración del producto - [!UICONTROL Search Engine Optimization]

_Optimización del motor de búsqueda_ (SEO) es la práctica de ajustar el contenido y la presentación de un sitio para mejorar la forma en que los motores de búsqueda indexan las páginas.

El _[!UICONTROL Search Engine Optimization]_para un producto, especifique el [Clave de URL](catalog-urls.md) y [metadatos](../merchandising-promotions/meta-data.md) campos que utilizan los motores de búsqueda para indexar el producto. Aunque algunos motores de búsqueda omiten las metapalabras clave, otros motores de búsqueda las siguen utilizando. El actual [Práctica recomendada de SEO](../merchandising-promotions/seo-overview.md) es incorporar palabras clave de alto valor tanto en el meta título como en la meta descripción.

El valor predeterminado de cada campo de metadatos se puede generar automáticamente en función de los valores especificados en la configuración. Cada campo contiene un marcador de posición que se reemplaza por un valor real. Para obtener más información, consulte [Generación automática de campos de producto](../configuration-reference/catalog/catalog.md#uicontrol-product-fields-auto-generation).

## Complete los campos SEO

1. Abra el producto en modo de edición.

1. Desplazarse hacia abajo y expandir ![Selector de expansión](../assets/icon-display-expand.png) el _[!UICONTROL Search Engine Optimization]_sección.

![Optimización del motor de búsqueda](./assets/product-search-engine-optimization.png){width="600" zoomable="yes"}


1. Introduzca el **[!UICONTROL URL Key]** (opcional).

   La clave URL predeterminada se basa en el nombre del producto. Puede utilizar el valor predeterminado o cambiarlo según sea necesario. Para obtener más información, consulte [URL de catálogo](catalog-urls.md).

1. Introduzca el **[!UICONTROL Meta Title]** (opcional).

   El metatítulo es el texto que aparece en la parte superior de la ventana del explorador. Puede utilizar el valor predeterminado, que se basa en el nombre del producto, o cambiarlo según sea necesario.

1. Añada el **[!UICONTROL Meta Keywords]** (opcional).

   Algunos motores de búsqueda utilizan más las palabras clave meta que otros. Se recomienda introducir algunas palabras clave de alto valor para ayudar al producto a obtener más visibilidad.

1. Introduzca el **[!UICONTROL Meta Description]**.

   La metadescripción es el texto que aparece en los listados de resultados de búsqueda. Para obtener mejores resultados, escriba una descripción de entre 150 y 160 caracteres de longitud.

## Referencia de campo

| Campo | [Ámbito](../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |------------------|
| [!UICONTROL URL Key] | Vista de tienda | Determina la dirección en línea del producto. La clave URL se añade a la dirección URL base de la tienda y aparece en la barra de direcciones de un explorador. Commerce crea inicialmente un _compatible con el motor de búsqueda_ URL basada en el nombre del producto. La clave de URL debe tener caracteres en minúsculas, con guiones no finales entre estos caracteres en lugar de espacios. No incluya un sufijo como `.html` en la clave URL, ya que se administra en la configuración. |
| [!UICONTROL Meta Title] | Vista de tienda | El título aparece en la barra de título y en la pestaña del navegador y también se utiliza como título de la página de resultados de un motor de búsqueda (SERP). El metatítulo debe ser único para la página y tener menos de 70 caracteres de longitud. Valor generado automáticamente: `{{name}}` |
| [!UICONTROL Meta Keywords] | Vista de tienda | Palabras clave relevantes para el producto. Considere utilizar palabras clave que los clientes podrían utilizar para encontrar el producto. Valor generado automáticamente: `{{name}}` |
| [!UICONTROL Meta Description] | Vista de tienda | La metadescripción proporciona una breve descripción de la página para los listados de resultados de búsqueda. La longitud ideal es de entre 150 y 160 caracteres, con un máximo de 255 caracteres. Aunque no es visible para el cliente, algunos motores de búsqueda incluyen la metadescripción en la página de resultados de búsqueda. Valor generado automáticamente: `{{name}} {{description}}` |

{style="table-layout:auto"}
