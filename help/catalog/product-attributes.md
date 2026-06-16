---
title: Resumen de atributos del producto
description: Obtenga información acerca de los atributos de producto y cómo se utilizan para describir características específicas de un producto.
exl-id: e15770ee-fb71-43f0-8c26-e8029935799a
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/reh5hq2WF3rmbKEKZiV8U18hfyLxXeUHHfJcUgWDcJ0
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fcid: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 547
ht-degree: 0%

---

# Resumen de atributos del producto

Los atributos son los componentes básicos del catálogo de productos y describen las características específicas de un producto. Los atributos de producto se pueden organizar en [conjuntos de atributos](attribute-sets.md), que luego se utilizan como plantillas para crear productos.

Los atributos determinan el tipo de control de entrada que se utiliza para las opciones de producto y proporcionan información adicional para las páginas de producto. También se utilizan como parámetros de búsqueda y criterios para la navegación por capas, informes de comparación de productos y promociones. Puede crear tantos atributos y conjuntos de atributos como sea necesario para describir los productos del catálogo. Además de los atributos que puede crear, los atributos del sistema, como el precio, están integrados en la plataforma principal de Commerce y no se pueden cambiar.

![Creando un nuevo atributo al editar un producto](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

Siga las prácticas recomendadas que se describen en las secciones siguientes cuando planifique y cree atributos de producto.

## Nombres de atributo

Establezca convenciones de nomenclatura de atributos coherentes, incluidos mayúsculas y minúsculas y puntuación. Por ejemplo, `Color:Green` y `Color:green` pueden ser considerados como dos valores de atributo diferentes por sistemas diferentes. Este ruido en los datos puede afectar a las reglas empresariales, los resultados de búsqueda y los filtros de datos de las aplicaciones que hacen coincidir los productos con las reglas.

## Uso de atributos

Considere cómo se deben utilizar los atributos al asignar propiedades y valores. Identifique los atributos que se utilizan como etiquetas para la presentación, como el nombre de un producto, una imagen, un precio y una descripción, y qué atributos se utilizan para la entrada de datos. Considere cómo se representan los atributos en las distintas páginas del sitio y cómo aparecen en las páginas de categorías, páginas de detalles del producto, cuadrículas de categorías y controles deslizantes de miniaturas.

## Color

Las descripciones de color específicas pueden plantear un desafío desde el punto de vista de las operaciones de la base de datos. Los nombres de color como &quot;Cielos Azure&quot; o &quot;Robin Egg Blue&quot; son muy atractivos, pero es posible que no devuelvan los mejores resultados cuando se usen como criterios de búsqueda o si la comercialización requiere que especifique `Color_Family:Blue`. Considere cómo se representan los colores en los resultados de búsqueda y en la navegación por capas, y establezca algunas directrices para sus necesidades comerciales. A continuación, sea coherente al asignar valores de atributos de color en todo el catálogo.

## Administración de variaciones

Use las [opciones de configuración](product-configurations.md) y [productos configurables](product-create-configurable.md) del producto para administrar las variaciones en las ofertas de productos. Estas funciones facilitan la categorización de productos, la creación de reglas de precios de carro de compras y reglas de categorías dinámicas, y la oferta de una selección de opciones con varios tipos de entrada de texto, selección y fecha.

## Búsqueda ponderada

A los atributos de producto habilitados para [búsqueda en el catálogo](search.md) se les puede asignar un peso para darles un valor más alto en los resultados de búsqueda. Los atributos con un peso mayor se devuelven antes que los que tienen un peso menor. Por ejemplo, considere dos atributos en el sistema, _color_ con una ponderación de búsqueda de 3 y _description_ con una ponderación de búsqueda de 1. Una búsqueda de la palabra _red_ devuelve una lista de productos con un valor de atributo de color de `red`, pero no devuelve productos con descripciones que contengan la palabra _red_. En este ejemplo, el atributo `color` tiene un peso definido mayor que el atributo `description`.

## Propiedades no utilizadas

Elimine las propiedades del producto no utilizadas para una mejor estructuración y una indexación más rápida.


>[!NOTE]
>
>Para obtener información sobre cómo optimizar la configuración de atributos de producto para obtener rendimiento, consulte [Prácticas recomendadas de administración de catálogos](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/planning/catalog-management#product-attributes) en el _Manual de implementación_.
