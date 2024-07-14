---
title: Crear y eliminar atributos de producto
description: Obtenga información sobre cómo crear y eliminar atributos de producto, que se utilizan para describir características específicas de los productos en su catálogo.
exl-id: fd0e5d5b-a917-4e55-8ec2-7ebb040d3d06
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 0%

---

# Crear y eliminar atributos de producto

Puede crear atributos mientras trabaja en un producto o desde la página _[!UICONTROL Product Attributes]_. Los pasos siguientes muestran cómo crear atributos a partir del menú_[!UICONTROL Stores]_.

## Paso 1: Describir las propiedades básicas de los atributos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Haga clic en **[!UICONTROL Add New Attribute]**.

   ![Propiedades de nuevo atributo](./assets/attribute-properties.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Default Label]**, escriba una etiqueta que identifique el atributo.

1. Para determinar el tipo de control de entrada que se usa para la entrada de datos, establezca **[!UICONTROL Catalog Input Type for Store Owner]** en uno de los siguientes:

   | Propiedad | Descripción |
   |--- |--- |
   | `Text Field` | Campo de entrada de una sola línea para texto. |
   | `Text Area` | Campo de entrada de varias líneas para introducir párrafos de texto, como una descripción del producto. Puede utilizar el Editor WYSIWYG para dar formato al texto con etiquetas de HTML o introducirlas directamente en el texto. |
   | `Text Editor` | Un editor de texto que funcione completamente en la ubicación del atributo. |
   | Fecha | Muestra un valor de fecha en el [formato preferido](attributes-input-types.md#date-and-time-options) y en la [zona horaria](../getting-started/store-details.md#locale-options). Los valores de fecha se pueden seleccionar de una lista o un calendario ( ![Icono de calendario](../assets/icon-calendar.png)). <br/><br/>**_Nota:_**Según la configuración del sistema, los usuarios de_Admin _pueden introducir fechas directamente en un campo o seleccionar una fecha del calendario o lista. Para obtener información acerca de cómo especificar valores de fecha y hora, vea [Opciones de fecha y hora](attributes-input-types.md#date-and-time-options). |
   | `Yes/No` | Muestra una lista desplegable con opciones predefinidas de `Yes` y `No`. |
   | `Dropdown` | Muestra una lista desplegable de valores que solo acepta una selección. El tipo de entrada desplegable es un componente clave de [productos configurables](product-create-configurable.md). |
   | `Multiple Select` | Muestra una lista desplegable de valores que acepta varias selecciones. |
   | `Price` | Este tipo de entrada se utiliza para crear campos de precio que se agregan a los atributos predefinidos: Precio, Precio especial, Precio de nivel y Coste. La moneda utilizada viene determinada por la configuración del sistema. |
   | `Media Image` | Asocia una imagen adicional a un producto, como un logotipo de producto, instrucciones de cuidado o ingredientes de una etiqueta de alimentos. Cuando se agrega un atributo de imagen multimedia al conjunto de atributos de un producto, se convierte en un tipo de imagen adicional, junto con Base, Pequeño y Miniatura. El atributo de imagen multimedia se puede excluir del [explorador multimedia de tienda](catalog-images-video.md#storefront-media-browser). |
   | `Fixed Product Tax` | Le permite definir [tarifas de FTP](../stores-purchase/fixed-product-tax.md) según los requisitos de su configuración regional. |
   | `Visual Swatch` | Muestra una muestra que muestra el color, la textura o el motivo de un producto configurable. Una [muestra visual](swatches.md) se puede rellenar con un valor de color hexadecimal o mostrar una imagen cargada que represente el color, el material, la textura o el motivo de la opción. |
   | `Text Swatch` | Representación basada en texto de una opción de producto configurable que se utiliza frecuentemente para el tamaño. [Las muestras de texto](swatches.md#text-based-swatches) también pueden incluir valores de color hexadecimales. |
   | `Page Builder` | Un área de trabajo [Page Builder](../page-builder/introduction.md) que funciona por completo en la ubicación del atributo y que facilita la adición de contenido atractivo a la página del producto. |

   {style="table-layout:auto"}

1. Si desea requerir una selección de opciones antes de que el cliente pueda adquirir el producto, establezca **[!UICONTROL Values Required]** en `Yes`.

1. Para los tipos de entrada [!UICONTROL Dropdown] y [!UICONTROL Multiple Select], haga lo siguiente:

   - En _[!UICONTROL Manage Options]_, haga clic en **[!UICONTROL Add Option]**.

   - Introduzca el primer valor que desee que aparezca en la lista.

     Puede introducir un valor para el administrador y una traducción del valor para cada vista de tienda. Si solo tiene una vista de tienda, puede introducir solo el valor Admin y también se utiliza para la tienda.

   - Haga clic en **[!UICONTROL Add Option]** y repita el paso anterior para cada opción que desee incluir en la lista.

   - Seleccione **[!UICONTROL Is Default]** para usar la opción como valor predeterminado.

   ![Atributo del producto - administrar opciones](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

## Paso 2: Describa las propiedades avanzadas (si es necesario)

1. Escriba un **[!UICONTROL Attribute Code]** único en caracteres en minúsculas y sin espacios.

   ![Atributo del producto - propiedades avanzadas](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

   Las opciones disponibles dependen de la configuración _[!UICONTROL Catalog Input Type for Store Owner]_.

1. Establezca **[!UICONTROL Scope]** para indicar en qué parte de su [jerarquía de almacén](../getting-started/websites-stores-views.md) se puede usar el atributo.

1. Si desea evitar entradas de valor duplicadas, establezca **[!UICONTROL Unique Value]** en `Yes`.

1. Para los tipos de entrada que son valores especificados, ejecute una prueba de validez de los datos introducidos en un campo de texto estableciendo **[!UICONTROL Input Validation for Store Owner]** en el tipo de datos que debe contener el campo.

   Este campo no está disponible para tipos de entrada con valores seleccionados. La prueba puede validar cualquiera de las siguientes opciones:

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![Validación de entrada](./assets/product-attribute-input-validation.png){width="400"}

1. Para agregar este atributo a la [lista de productos](products-list.md), establezca las siguientes opciones en `Yes`.

   - **Agregar a opciones de columna** - Incluye el atributo como una columna en la lista _[!UICONTROL Products]_.
   - **Usar en opciones de filtro** - Agrega un control de filtro al encabezado de columna en la lista _[!UICONTROL Products]_.

## Paso 3: introducir la etiqueta de campo

1. En la navegación del lado izquierdo, elija **[!UICONTROL Manage Labels]**.

1. Escriba un(a) **[!UICONTROL Title]** para utilizarlo como etiqueta en el campo.

   Si la tienda está disponible en diferentes idiomas, puede introducir un título traducido para cada vista.

   ![Atributo del producto - administrar títulos](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## Paso 4: Describir las propiedades de la tienda

1. En la navegación del lado izquierdo, elija **[!UICONTROL Storefront Properties]**.

   ![Atributos de producto - propiedades de tienda](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

   Las opciones disponibles dependen de la configuración _[!UICONTROL Catalog Input Type for Store Owner]_.

1. Si el atributo va a estar disponible para la búsqueda, establezca **[!UICONTROL Use in Search]** en `Yes`.

   - Establezca el valor **[!UICONTROL Search Weight]** para controlar dónde aparece el elemento en los resultados de búsqueda: 1 (menor peso) a 10 (mayor peso).

   - Establezca **[!UICONTROL Visible in Advanced Search]** según sea necesario. Obtenga más información en [Búsqueda avanzada](search.md#advanced-search).

1. Para incluir el atributo en la comparación de productos, establezca **[!UICONTROL Comparable on Storefront]** en `Yes`.

1. Para los campos desplegable, de selección múltiple y de precio, haga lo siguiente:

   - Para usar el atributo como filtro en la navegación por capas, establezca **[!UICONTROL Use in Layered Navigation]** en `Yes`.

   - Para usar el atributo en la navegación por capas en las páginas de resultados de búsqueda, establezca **[!UICONTROL Use in Search Results Layered Navigation]** en `Yes`.

   - Para **[!UICONTROL Position]**, escriba un número para indicar la posición relativa del atributo en el bloque de navegación por capas.

1. Para usar el atributo en las reglas de precios, establezca **[!UICONTROL Use for Promo Rule Conditions]** en `Yes`.

1. Para permitir que se aplique formato al texto con el HTML, establezca **[!UICONTROL Allow HTML Tags on Frontend]** en `Yes`.

   Esta configuración hace que el editor WYSIWYG esté disponible para el campo.

1. Para incluir el atributo en la página de productos, establezca **[!UICONTROL Visible on Catalog Pages on Storefront]** en `Yes`.

1. Complete la siguiente configuración si su temática lo admite:

   - Para incluir el atributo en los listados de productos, establezca **[!UICONTROL Used in Product Listing]** en `Yes`.

   - Para usar el atributo como parámetro de ordenación para las listas de productos, establezca **[!UICONTROL Used for Sorting in Product Listing]** en `Yes`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Attribute]**.

## Paso 5: Asignar el atributo creado al conjunto de atributos

Para que un atributo sea visible en la página de creación del producto, agréguelo a un conjunto de atributos específico.

1. Después de completar los pasos anteriores, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Seleccione el conjunto de atributos que necesite en la lista y ábralo en modo de edición.

1. Arrastre el atributo creado de la lista **[!UICONTROL Unassigned Attributes]** a la carpeta correspondiente de la columna **Grupos**.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

## Atributos para productos configurables

Cualquier atributo que se use como lista desplegable de opciones para un [producto configurable](product-create-configurable.md) debe tener las siguientes propiedades:

| Propiedad | Valor |
|----------|------ |
| Tipo de entrada de catálogo del propietario de la tienda | Desplegable |
| Ámbito | Global |

{style="table-layout:auto"}

## Eliminación de un atributo

Cuando se elimina un atributo, se elimina de cualquier producto relacionado y conjunto de atributos. Los atributos del sistema forman parte de la funcionalidad principal de su tienda y no se pueden eliminar.

Antes de eliminar un atributo, asegúrese de que ningún producto del catálogo lo esté utilizando en ese momento. Una manera fácil de determinar si un atributo está en uso es usar la herramienta [Exportar](../systems/data-export.md) para comprobar la lista de Atributos de entidad del producto. Si el atributo no se incluye en la lista, ningún producto del catálogo lo utiliza.

**_Para eliminar un atributo:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Busque el atributo en la lista y ábralo en modo de edición.

1. Haga clic en **[!UICONTROL Delete Attribute]**.

   ![Eliminar atributo](./assets/attribute-delete.png){width="600" zoomable="yes"}

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL OK]**.
