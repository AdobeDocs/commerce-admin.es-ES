---
title: Etiquetas de marcado
description: Obtenga información sobre las etiquetas de marcado que contienen fragmentos de código para hacer referencia a un objeto de su tienda.
exl-id: 0d6f5a9b-983d-473e-b641-0dceba40974f
feature: Page Content, Communications, Variables
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# Etiquetas de marcado

Una etiqueta de marcado es una directiva que contiene un fragmento de código con una referencia relativa a un objeto del almacén, como una variable, una dirección URL, una imagen o un bloque. Las etiquetas de marcado se pueden usar en cualquier parte donde el editor esté disponible e incorporado a las plantillas HTML de [correo electrónico](email-templates.md) y [boletín](../merchandising-promotions/newsletter-template.md), así como a otros tipos de [contenido](../content-design/introduction.md#content).

Las etiquetas de marcado se encierran entre llaves dobles y se pueden generar mediante la herramienta Widget o escribir directamente en el contenido de HTML. Por ejemplo, en lugar de programar la ruta completa a una página, puede utilizar una etiqueta de marcado para representar la dirección URL de la tienda. Las etiquetas de marcado que aparecen en los siguientes ejemplos incluyen:

{{$include /help/_includes/directives-caution.md}}

## Variable personalizada

La etiqueta Variable markup se puede usar para insertar una [variable personalizada](variables-custom.md) en una plantilla de correo electrónico, bloques, boletines informativos y páginas de contenido.

\{\{CustomVar code= &quot;my_custom_variable&quot;}}

## URL de tienda

La etiqueta Store URL markup representa la dirección URL base del sitio web y se utiliza como sustituto de la primera parte de una dirección URL completa, incluido el nombre de dominio. Hay dos versiones de esta etiqueta de marcado: una que va directamente a su tienda y otra con una barra diagonal (`/`) al final que se usa cuando se agrega una ruta de acceso.

\{\{store url=&#39;vestimenta/zapatos/mujer&#39;}}

## URL de medios

La etiqueta de marcado de URL de medios dinámicos representa la ubicación y el nombre de archivo de una imagen almacenada en una red de entrega de contenido (CDN). La etiqueta se puede utilizar para colocar una imagen en una página, bloque, banner o plantilla de correo electrónico.

\{\{media url=&#39;shoe-sale.jpg&#39;}}

## ID de bloque

La etiqueta de marcado ID de bloque es una de las más fáciles de usar y se puede usar para colocar un bloque directamente en una página de CMS o incluso anidado dentro de otro bloque. Puede utilizar esta técnica para modificar un bloque para diferentes promociones o idiomas. La etiqueta de marcado ID de bloque hace referencia a un bloque por su identificador.

\{\{block id=&#39;block-id&#39;}}

## Etiqueta de plantilla

Una etiqueta de plantilla hace referencia a un archivo de plantilla PHTML y se puede utilizar para mostrar el bloque en una página CMS o un bloque estático. El código del siguiente ejemplo se puede agregar a una página o bloque para mostrar el formulario Contáctenos.

\{\{block class=&quot;Magento\Contact\Block\ContactForm&quot; name=&quot;contactForm&quot; template=&quot;Magento_Contact::form.phtml&quot;}}

El código del siguiente ejemplo se puede añadir a una página o bloque para mostrar una lista de productos en una categoría específica, por ID de categoría.

\{\{block type=&quot;catalog/product_list&quot; category_id=&quot;22&quot; template=&quot;catalog/product/list.phtml&quot;}}

## Código de widget

La herramienta Widget se puede utilizar para mostrar listas de productos o para insertar vínculos complejos, como uno que va a una página de producto específica, en función del ID del producto. El código que se genera incluye la referencia de bloque, la ubicación del módulo de código y la plantilla PHTML correspondiente. Una vez generado el código, puede copiarlo y pegarlo de un lugar a otro.

El código del siguiente ejemplo se puede añadir a una página o bloque para mostrar la lista de nuevos productos.

\{\{widget type=&quot;catalog/product_widget_new&quot; display_type=&quot;new_products&quot; products_count=&quot;10&quot; template=&quot;catalog/product/widget/new/content/new_grid.phtml&quot;}}

El código del siguiente ejemplo se puede añadir a una página o bloque para mostrar un vínculo a un producto específico, por ID de producto.

\{\{widget type=&quot;catalog/product_widget_link&quot; anchor_text=&quot;Mi vínculo de producto&quot; title=&quot;Mi vínculo de producto&quot; template=&quot;catalog/product/widgetlink/link_block.phtml&quot; id_path=&quot;product/31&quot;}}

## Uso de etiquetas de marcado en vínculos

Puede utilizar etiquetas de marcado con etiquetas de anclaje de HTML y vincular directamente a cualquier página de la tienda. El vínculo se puede incorporar a páginas de contenido, bloques o plantillas de correo electrónico y newsletter. También puede utilizar esta técnica para vincular una imagen a una página específica.

### Paso 1. Identificación de la dirección URL de destino

Si es posible, vaya a la página a la que desee vincular y copie la dirección URL completa de la barra de direcciones del explorador. La parte de la dirección URL que necesita viene después de `.com/`. De lo contrario, copie la clave URL de la página de CMS que desee utilizar como destino del vínculo.

#### Dirección URL completa de la página de categoría

`https://mystore.com/apparel/shoes/womens`
`https://mystore.com/apparel/shoes/womens.html`

#### Dirección URL completa de la página del producto

`https://mystore.com/apparel/shoes/womens/nine-west-pump`
`https://mystore.com/apparel/shoes/womens/nine-west-pump.html`

#### Dirección URL completa de la página de CMS

`https://mystore.com/about-us`

### Paso 2. Agregar el marcado a la dirección URL

La etiqueta Store URL representa la dirección URL base del sitio web y se utiliza como sustituto de la parte de la dirección HTTP de la dirección URL del almacén, incluidos el nombre de dominio y `.com`. Existen dos versiones de la etiqueta que puede utilizar según los resultados que desee lograr.

`store direct_url`: vincula directamente a una página.

`store url` - Coloca una barra diagonal al final para que se puedan anexar referencias adicionales como ruta de acceso.

En los ejemplos siguientes, la clave de URL está entre comillas simples y toda la etiqueta de marcado está entre llaves dobles. Cuando se utiliza con una etiqueta de anclaje, la etiqueta de marcado se coloca dentro de las comillas dobles del anclaje. Para evitar confusiones, puede utilizar comillas simples y dobles para cada conjunto anidado de comillas.

Si comienza con una dirección URL completa, elimine la parte de la dirección HTTP (`http://` o `https://`) de la dirección URL, hasta la dirección `.com/` inclusive. En su lugar, introduzca la etiqueta Store URL markup mediante la comilla simple de apertura.

#### Etiqueta de marcado de URL de tienda

`https://mystore.com/apparel/shoes/womens`

`{{store url='apparel/shoes/womens'}}`

De lo contrario, introduzca la primera parte de la etiqueta Store URL markup y pegue la clave URL o la ruta que copió anteriormente.

### Almacenar etiqueta de marcado de URL con clave de URL

`{{store url=`

Para completar la etiqueta de marcado, escriba las comillas dobles de cierre y las llaves dobles.

`{{store url='apparel/shoes/womens'}}`

### Paso 3. Completar la etiqueta de anclaje

Envuelva la etiqueta de marcado completada dentro de una etiqueta de anclaje con la etiqueta de marcado en lugar de la dirección URL de destino. A continuación, añada el texto del vínculo y la etiqueta de anclaje de cierre.

#### Marcado en la etiqueta de anclaje

\&lt;a href=&quot;\{\{la etiqueta de marcado se incluye aquí}}&quot;>Texto del vínculo\&lt;/a>

Pegue la etiqueta de anclaje completada en el código de cualquier página de CMS, bloque, banner o plantilla de correo electrónico donde desee que aparezca el vínculo.

### Vínculo completo con marcado

\&lt;a href=&quot;\&lbrace;\{store url=&#39;vestir/zapatos&#39;}&quot;>Venta de zapatos\&lt;/a>

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
