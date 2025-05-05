---
title: Reglas de categoría para la comercialización
description: Aprenda a crear reglas para cambiar dinámicamente las selecciones de productos según un conjunto de condiciones.
exl-id: 765b863a-bb83-418b-9fca-ef0a148b09eb
feature: Categories, Merchandising
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 0%

---

# Reglas de categoría para la comercialización

{{ee-feature}}

Las reglas de categoría cambian dinámicamente la selección del producto según un conjunto de condiciones. Cada categoría solo puede tener una regla de categoría, aunque la única regla puede tener varias condiciones. Por ejemplo, puede crear una regla de categoría para una marca específica. Los productos de la misma marca se añaden automáticamente a la lista, incluso si no están asignados a la misma categoría. Puede agregar a la expresión tantas condiciones como sea necesario para describir los productos que desea incluir.

>[!TIP]
>
>Durante la configuración de la regla de categoría, los productos son _clasificados_, _coincidentes_, _asignados_ y _sin asignar_ según esa regla **_solo_** cuando se guarde esta categoría. Por ejemplo, si agrega un producto al catálogo y desea asignarlo de acuerdo con la regla, **debe volver a guardar cada categoría** que se haya establecido para que coincida con los productos por regla. Además, si algún estado de stock de producto se cambia a `In Stock` o `Out of Stock` y los productos de la categoría deben _ordenarse_ según la regla **[!UICONTROL Automatic Sorting]**, debe hacer clic en **[!UICONTROL Save Category]**.

Cada condición consta de un atributo, valor y operador lógico. En las reglas de categoría solo se pueden usar atributos con la propiedad _[[!UICONTROL Use in Product Listing]](../catalog/attribute-product-create.md)_establecida en `Yes`. Debe establecer esta propiedad para el atributo si desea utilizar un atributo que no esté incluido en las listas de productos. Aunque no se admiten los atributos Fecha, puede utilizar los atributos Fecha de creación o Fecha de modificación para definir una fecha o un rango de fechas. Por ejemplo, para incluir solo los productos creados durante la semana pasada, establezca &quot;Fecha de creación&quot; en un valor de `<7`.

>[!NOTE]
>
>Asegúrese de configurar cada atributo que se use en la regla como un atributo [_smart_](smart-attributes-configure.md).

![Regla de producto de categoría](../catalog/assets/category-product-rule-with-stock.png){width="600" zoomable="yes"}

Las reglas de productos de categorías pueden acelerar el proceso de asignación de productos específicos a categorías, en función de las condiciones que determinan qué productos aparecen en la categoría. Los atributos &quot;inteligentes&quot; que se pueden usar con las reglas de productos de categoría se especifican en la configuración de [Visual Merchandiser](visual-merchandiser.md).

>[!NOTE]
>
>Tenga cuidado al aplicar una regla de producto de categoría, ya que los productos que no cumplen la condición se eliminan de la categoría. Por ejemplo, si crea una regla que incluya solo las camisetas sin mangas moradas, todas las demás camisetas sin mangas se eliminarán de la categoría.

## Paso 1: Configurar los atributos _smart_

1. Para cada atributo que se va a usar en la regla, asegúrese de que la propiedad de tienda [[!UICONTROL Use in Product Listing]](../catalog/product-attributes.md) está establecida en `Yes`.

   >[!NOTE]
   >
   >Asegúrese de que el atributo que seleccione NO sea una selección múltiple _[!UICONTROL Input Type]_.

1. Complete la [configuración](smart-attributes-configure.md) para identificar cada atributo _smart_ que se va a usar con Visual Merchandiser.

## Paso 2: Crear la regla de categoría

1. En el árbol de categorías, abra la categoría que desea editar.

1. En la sección **[!UICONTROL Products in Category]**, establezca **[!UICONTROL Match products by rule]** en `Yes`.

   Aparecerán las opciones de ordenación y condición automáticas.

1. Haga clic en **[!UICONTROL Add Condition]**.

1. Elija **[!UICONTROL Attribute]** que es la base de la condición.

1. Establezca **[!UICONTROL Operator]** en una de las siguientes opciones:

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. Escriba el(la) **[!UICONTROL Value]** con el que desea establecer una coincidencia.

   ![Agregar condición a regla de categoría](../catalog/assets/category-rule-create.png){width="500"}

1. Repita este proceso para cada atributo necesario para describir las condiciones que se deben cumplir.

   Por ejemplo, para hacer coincidir productos creados entre hace siete y 30 días, haga lo siguiente:

   - Establezca **[!UICONTROL Date Created]** en `Less than 30`.

   - Establezca **[!UICONTROL Logic]** en `AND`.

     >[!NOTE]
     >
     >Al elegir `AND`, la regla se aplica a los productos en los que se cumplen todas las condiciones. Al elegir `OR`, se aplica a los productos en los que se cumple al menos una condición.

   - Establezca **[!UICONTROL Date Modified]** en `Greater than 7`.

1. Para aplicar un criterio de ordenación automáticamente a la lista de productos generada dinámicamente, establezca **[!UICONTROL Automatic Sorting]**.

   ![Ordenación automática](./assets/automatic-sorting-field.png){width="600" zoomable="yes"}

   Las opciones de orden se definen globalmente y se aplican según las condiciones actuales. No puede establecer un criterio de ordenación diferente para el sitio web, tienda o nivel de vista de tienda.

   | Ordenar, opción | Descripción |
   |-----------| -----------|
   | [!UICONTROL Stock quantity] | Ordenar según existencias, desde arriba o abajo: `Move low stock to top` o `Move out of stock to bottom` |
   | [!UICONTROL Special price] | Ordenar según el precio, de arriba a abajo: `Special price to top` o `Special price to bottom` |
   | [!UICONTROL New Products] | Lista de productos más recientes: `Newest products first` |
   | [!UICONTROL Color] | Ordenar alfabéticamente por color: `Sort by color` |
   | [!UICONTROL Product Names] | Ordenar por nombre en orden ascendente o descendente: `Name A - Z` o `Name Z -A` |
   | [!UICONTROL SKU] | Ordenar por SKU en orden ascendente o descendente: `SKU: Ascending` o `SKU: Descending` |
   | [!UICONTROL Price] | Ordenar por precio en orden ascendente o descendente: `Price: High to low` o `Price: Low to high` |

   {style="table-layout:auto"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Category]**.

>[!NOTE]
>
>Al configurar una regla de categoría, los productos coinciden con la regla y se asignan a ella cuando se guarda la categoría. Si agrega un producto al catálogo y desea incluirlo en la regla, debe volver a guardar cada categoría que esté configurada para que coincida con los productos por regla. Esto garantiza que se incluya el nuevo producto.

### Opciones de menú

- **[!UICONTROL Match products by rule]**: determina si una regla de categoría genera dinámicamente la lista de productos de la categoría. Opciones: `Yes` / `No`

- **[!UICONTROL Automatic Sorting]**: aplica automáticamente un orden de clasificación a la lista de productos de categoría. Opciones: `None`, `Move low stock to top`, `Move low stock to bottom`, `Special price to top`, `Special price to bottom`, `Newest products first`, `Sort by color`, `Name: A - Z`, `Name: Z - A`, `SKU: Ascending`, `SKU: Descending`, `Price: High to Low` y `Price: Low to High`

  >[!NOTE]
  >
  >Si tiene un producto configurable con productos secundarios, las existencias del producto principal se calculan en función del total combinado de existencias de productos secundarios. Piénsese en un ejemplo en el que tiene un producto _Proteus Fitness Shirt_ configurable con productos secundarios de color naranja, rojo y amarillo con diferentes cantidades de stock de cada uno. Las existencias del producto principal se calculan sobre la base del total combinado de existencias de productos secundarios de color naranja, rojo y amarillo. Con la opción `Move low stock to top`, calcula las existencias de los productos principales combinando todas las existencias de productos secundarios comercializables y las ordena en consecuencia.

- **[!UICONTROL Add Condition]** - Agrega otra condición a la regla.

- **[!UICONTROL Attribute]**: determina el atributo que se usa como base de la condición. Opciones:

  | Opción | Descripción |
  | ------ | ----------- |
  | `Clone Category ID(s)` | Clona de forma dinámica productos, sin su orden ni clasificación, de varias categorías en función del ID de categoría. |
  | `Color` | Incluye productos basados en el color. |
  | `Date Created (days ago)` | Incluye productos en función del número de días desde que se añadieron al catálogo. |
  | `Date Modified (days ago)` | Incluye productos en función del número de días desde la última modificación de los productos. |
  | `Name` | Incluye productos basados en el nombre del producto. |
  | `Price` | Incluye productos en función del precio. Este atributo no se aplica a los productos configurables porque no tienen su propio precio. |
  | `Quantity` | Incluye productos basados en la cantidad en stock. |
  | `SKU` | Incluye productos basados en SKU. |

  {style="table-layout:auto"}

  >[!NOTE]
  >
  >La cantidad de un producto configurable con opciones secundarias se calcula combinando todas las cantidades de productos secundarios comercializables. Piénsese en un ejemplo en el que tiene un producto configurable _Basic Fitness Tank_ con opciones de color morado, rojo y amarillo y diferentes cantidades de cada uno. En este caso, la cantidad del producto principal (tanque de fitness básico) es la cantidad vendible combinada de los productos secundarios de color morado, rojo y amarillo.

- **[!UICONTROL Operator]**: especifica el operador que se aplica al valor del atributo para cumplir la condición. A menos que se especifique un operador, `Equal` se usa como valor predeterminado. Opciones: `Equal`, `Not equal`, `Greater than`, `Greater than or equal to`, `Less than`, `Less than or equal to` y `Contains`

- **[!UICONTROL Value]**: especifica el valor que debe tener el atributo para cumplir la condición.

- **[!UICONTROL Logic]**: la columna Lógica se usa para definir varias condiciones y solo aparece cuando se agrega otra condición. Los operadores siguen las reglas de prioridad para MySQL [operadores booleanos](https://dev.mysql.com/doc/refman/8.0/en/operator-precedence.html). Opciones: `AND` / `OR`
