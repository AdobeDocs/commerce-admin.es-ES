---
title: Resumen de atributos del producto
description: Obtenga información acerca de los atributos de producto y cómo se utilizan para describir características específicas de un producto.
exl-id: e15770ee-fb71-43f0-8c26-e8029935799a
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Resumen de atributos del producto

Los atributos son los componentes básicos del catálogo de productos y describen las características específicas de un producto. Los atributos del producto se pueden organizar en [conjuntos de atributos](attribute-sets.md), que luego se utilizan como plantillas para crear productos.

Los atributos determinan el tipo de control de entrada que se utiliza para las opciones de producto y proporcionan información adicional para las páginas de producto. También se utilizan como parámetros de búsqueda y criterios para la navegación por capas, informes de comparación de productos y promociones. Puede crear tantos atributos y conjuntos de atributos como sea necesario para describir los productos del catálogo. Además de los atributos que puede crear, los atributos del sistema, como el precio, están integrados en la plataforma principal de Commerce y no se pueden cambiar.

![Creación de un nuevo atributo mientras se edita un producto](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

Siga las prácticas recomendadas que se describen en las secciones siguientes cuando planifique y cree atributos de producto.

## Nombres de atributo

Establezca convenciones de nomenclatura de atributos coherentes, incluidos mayúsculas y minúsculas y puntuación. Por ejemplo, `Color:Green` y `Color:green` diferentes sistemas pueden considerar dos valores de atributo diferentes. Este ruido en los datos puede afectar a las reglas empresariales, los resultados de búsqueda y los filtros de datos de las aplicaciones que hacen coincidir los productos con las reglas.

## Uso de atributos

Considere cómo se deben utilizar los atributos al asignar propiedades y valores. Identifique los atributos que se utilizan como etiquetas para la presentación, como el nombre de un producto, una imagen, un precio y una descripción, y qué atributos se utilizan para la entrada de datos. Considere cómo se representan los atributos en las distintas páginas del sitio y cómo aparecen en las páginas de categorías, páginas de detalles del producto, cuadrículas de categorías y controles deslizantes de miniaturas.

## Color

Las descripciones de color específicas pueden plantear un desafío desde el punto de vista de las operaciones de la base de datos. Los nombres de color como &quot;Azure Skies&quot; o &quot;Robin Egg Blue&quot; tienen un gran atractivo, pero es posible que no devuelvan los mejores resultados cuando se utilizan como criterios de búsqueda o si la comercialización requiere que especifique `Color_Family:Blue`. Considere cómo se representan los colores en los resultados de búsqueda y en la navegación por capas, y establezca algunas directrices para sus necesidades comerciales. A continuación, sea coherente al asignar valores de atributos de color en todo el catálogo.

## Administración de variaciones

Usar producto [opciones de configuración](product-configurations.md) y [productos configurables](product-create-configurable.md) para administrar las variaciones en las ofertas de productos. Estas funciones facilitan la categorización de productos, la creación de reglas de precios de carro de compras y reglas de categorías dinámicas, y la oferta de una selección de opciones con varios tipos de entrada de texto, selección y fecha.

## Búsqueda ponderada

Atributos de producto habilitados para [búsqueda en el catálogo](search.md) se le puede asignar un peso para darles un valor más alto en los resultados de búsqueda. Los atributos con un peso mayor se devuelven antes que los que tienen un peso menor. Por ejemplo, considere dos atributos en el sistema, _color_ con una ponderación de búsqueda de 3 y _description_ con una ponderación de búsqueda de 1. Una búsqueda de la palabra _rojo_ devuelve una lista de productos con un valor de atributo color de `red`, pero no devuelve productos con descripciones que contengan la palabra _rojo_. En este ejemplo, la variable `color` tiene un peso definido mayor que `description` atributo.

## Propiedades no utilizadas

Elimine las propiedades del producto no utilizadas para una mejor estructuración y una indexación más rápida.
