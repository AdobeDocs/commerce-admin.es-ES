---
title: Creación de una regla de precios de catálogo
description: Aprenda a crear una regla de precios de catálogo que aplique un descuento a productos específicos siempre que se cumpla un conjunto de condiciones.
exl-id: 53c5745b-f1c4-4ee8-b995-d2c70f639c7d
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '1662'
ht-degree: 0%

---

# Creación de una regla de precios de catálogo

Siga estas instrucciones para aplicar un descuento a productos específicos siempre que se cumpla un conjunto de condiciones. Los descuentos de la regla de precios de catálogo entran en vigor antes de que el producto se coloque en el carro de compras.

## Paso 1: Añadir una regla

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rule]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add New Rule]**.

   La sección _[!UICONTROL Rule Information]_incluye secciones expandibles para **[!UICONTROL Conditions]**y **[!UICONTROL Actions]**.

   ![Regla de precios de catálogo: información](./assets/price-rule-catalog-new-ee.png){width="700" zoomable="yes"}

1. Complete los campos **[!UICONTROL Rule Name]** y **[!UICONTROL Description]**.

   Estos campos son solo para referencia interna.

1. Establezca **[!UICONTROL Status]** de la regla de precios según sea necesario.

   De manera predeterminada, el estado es `Inactive`.

   >[!NOTE]
   >
   >Una vez creada la regla, su estado se puede actualizar cambiando el estado a `Active` o `Inactive` según sea necesario.

1. Seleccione el **[!UICONTROL Websites]** en el que la regla debe estar disponible.

1. Seleccione el(la) **[!UICONTROL Customer Groups]** al que se aplica esta regla.

   Para elegir varios grupos, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

   >[!NOTE]
   >
   >Las opciones de esta lista dependen de los grupos de clientes creados y administrados en _Clientes_ > _Grupos de clientes_.

1. ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Escriba las fechas **[!UICONTROL From]** y **[!UICONTROL To]** para determinar si la regla de precios está en vigor.

   Puede escribir las fechas o usar el **[!UICONTROL Calendar]** (![icono del calendario](../assets/icon-calendar.png)) para elegir las fechas. Si deja las fechas en blanco, la regla se activa cuando se guarda la regla de precio.

1. Escriba un número para establecer el **[!UICONTROL Priority]** de esta regla en relación con otras reglas.

   >[!NOTE]
   >
   >La configuración de _[!UICONTROL Priority]_es importante cuando el mismo producto del catálogo cumple las condiciones establecidas para más de una regla de precio. La regla con la configuración de prioridad más alta (las prioridades de mayor a menor son 0, 1, 2, 3, etc.) se activa para el producto.

## Paso 2: Definición de las condiciones

La mayoría de las condiciones disponibles se basan en valores de atributo existentes. Para aplicar la regla a todos los productos, deje las condiciones en blanco.

>[!NOTE]
>
>Si al menos un atributo de producto condicional tiene un valor vacío, la regla de precio de catálogo no se aplica al producto.

>[!NOTE]
>
>Para aplicar una condición de atributo de producto `Category` a cualquier producto [paquete](../catalog/product-create-bundle.md) o [agrupado](../catalog/product-create-grouped.md), todos los productos secundarios deben asignarse a la misma categoría para que la regla se aplique correctamente. Si no es así, puedes usar una promoción de [Regla de precio del carro de compras](price-rules-cart-create.md) en su lugar.

1. Desplácese hacia abajo y expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Conditions]**.

   La primera condición aparece de forma predeterminada y establece lo siguiente:

   `If **ALL** of these conditions are **TRUE**:`

   ![Regla de precio de catálogo: línea de condición 1](./assets/catalog-condition1.png){width="400"}

   La instrucción tiene dos vínculos en negrita en los que puede hacer clic para mostrar la selección de opciones de esa parte de la instrucción. Puede crear diferentes condiciones cambiando la combinación de estos valores.

1. Cambie la instrucción de cualquiera de las siguientes maneras:

   - Haga clic en **[!UICONTROL ALL]** y seleccione `ALL` o `ANY`.
   - Haga clic en **[!UICONTROL TRUE]** y seleccione `TRUE` o `FALSE`.
   - Deje la condición sin cambios para aplicar la regla a todos los productos.

   Puede crear diferentes condiciones cambiando la combinación de estos valores. Para este ejemplo, se utiliza la condición predeterminada.

1. Haga clic en el icono _Agregar_ (![Agregar icono](../assets/icon-add-green-circle.png)) al principio de la línea siguiente y seleccione una opción para la condición, como un atributo de producto o una combinación.

1. En la lista debajo de **[!UICONTROL Product Attribute]**, elija el atributo que desea usar como base de la condición.

   Para este ejemplo, la condición es `Attribute Set`.

   ![Regla de precio de catálogo: línea de condición 2](./assets/catalog-condition2.png){width="400"}

   >[!NOTE]
   >
   >Para que un atributo aparezca en la lista, debe configurarse para su uso en condiciones de regla promocional. Para obtener más información, consulte [Atributos de producto](../catalog/product-attributes.md).

   >[!NOTE]
   >
   >Cuando se usa la condición `is not one of` con un atributo de producto _SKU_ y un producto configurable, se deben seleccionar tanto los SKU del producto principal como los secundarios. Para evitar enumerar todos los SKU secundarios en la regla, puede utilizar la condición `does not contain` con partes de SKU comunes de un producto configurable y sus productos secundarios.

   La condición seleccionada aparece en la instrucción, seguida de dos vínculos en negrita más. Las opciones difieren según el atributo de condición que seleccione. La declaración ahora dice:

   `If **ALL** of these conditions are **TRUE**: <br/>Attribute Set **is** …`

1. Haga clic en **[!UICONTROL is]** y elija el operador de comparación que describe la condición que se debe cumplir.

   Estas opciones pueden incluir una opción para diferentes comparaciones. En este ejemplo, las opciones son `is` y `is not`.

1. Seleccione o introduzca valores para la condición.

   Según la condición, puede seleccionar productos de una cuadrícula o lista, introducir un valor numérico, etc.

   ![Regla de precio de catálogo: línea de condición 2](./assets/catalog-condition3.png){width="400"}

   El elemento seleccionado aparece en la instrucción para completar la condición.

   `If **ALL** of these conditions are **TRUE**: <br/> Attribute Set **is Default**`

1. Para agregar otra línea de condición a la instrucción, haga clic en el icono _Agregar_ (![Agregar icono](../assets/icon-add-green-circle.png)) y elija una de las siguientes opciones:

   - `Conditions Combination`
   - `Product Attribute`

   Repita el proceso hasta que se hayan completado todas las condiciones deseadas.

   Si en cualquier momento desea eliminar parte de la condición, haga clic en el icono **[!UICONTROL Delete]** (![Eliminar icono](../assets/icon-delete-red-circle.png) al final de la línea.

## Paso 3: Definir las acciones

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png)la sección **[!UICONTROL Actions]** y haga lo siguiente:

   ![Regla de precios de catálogo: acciones](./assets/price-rule-catalog-actions.png){width="600" zoomable="yes"}

1. En **[!UICONTROL Pricing Structure Rules]**, establezca **[!UICONTROL Apply]** en una de las siguientes opciones:

   - `Apply as percentage of original` - Artículo de descuentos al restar un porcentaje del precio normal. Por ejemplo: introduzca 10 en Importe de descuento para un precio final marcado como inferior en un 10% al precio normal.
   - `Apply as fixed amount` - artículo de descuentos al restar un importe fijo del precio normal. Por ejemplo: Introduzca 10 en Importe de Descuento para un precio final que sea 10 euros inferior al precio normal.
   - `Adjust final price to this percentage` - Ajusta el precio final en un porcentaje del precio normal. Por ejemplo: introduzca 25 en Importe de descuento para un precio final marcado como inferior en un 75% al precio normal.
   - `Adjust final price to discount value` - Establece el precio final en una cantidad fija con descuento. Por ejemplo: introduzca 20 en Importe de descuento para un precio final de 20,00 $.

   >[!NOTE]
   >
   >_Precio regular_ se refiere al precio base del producto sin ningún tipo de descuento avanzado (especial/nivel/grupo) o descuentos promocionales. _Precio final_ se refiere al precio con descuento que aparece en el carro de compras. <br/>El precio del producto **_final_** se calcula como el precio **_mínimo_** relevante, utilizando la siguiente fórmula: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

   >[!NOTE]
   >
   >**_Precio fijo_** Las opciones personalizables del producto están _no_ afectadas por las reglas de Precio de grupo, Precio de nivel, Precio especial o Precio de catálogo.

1. Escriba **[!UICONTROL Discount Amount]**.

1. Para detener el procesamiento de otras reglas después de aplicar esta regla, establezca **[!UICONTROL Discard Subsequent Rules]** en `Yes`.

   >[!NOTE]
   >
   >Configurar esto en `Yes` es una medida de seguridad para evitar que el sistema aplique varios descuentos (reglas) al mismo producto.

## Paso 4: Agregar bloques dinámicos relacionados

{{ee-feature}}

[Los bloques dinámicos](../content-design/dynamic-blocks.md) asociados con una regla de precio de catálogo aparecen en la tienda siempre que se cumplan las condiciones. Este es un paso opcional.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png)la sección **[!UICONTROL Related Dynamic Blocks]**.

1. Use los [filtros de búsqueda](../getting-started/admin-workspace.md) para localizar los bloques dinámicos que desea asociar con la regla.

1. Seleccione la casilla de verificación de la primera columna para asociar el bloque dinámico a la regla.

   ![Regla de precios de catálogo: bloques dinámicos relacionados](./assets/price-rule-catalog-related-dynamic-blocks.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save and Continue Edit]**.

## Paso 5: Programar la regla

{{ee-feature}}

>[!NOTE]
>
>Si la regla se establece en activa, debe agregarse como una actualización programada. Para obtener más información, consulte [Cambios programados](price-rule-catalog-scheduled-changes.md).

1. En el cuadro _Cambios programados_, haga clic en **[!UICONTROL Schedule New Update]** en la parte superior del cuadro).

   Si la regla tiene una actualización programada existente, puede hacer clic en **[!UICONTROL View/Edit]** a la derecha del cambio de la lista.

   Puede editar la actualización existente o asignar la regla de precio de catálogo a otra campaña. La opción **Editar actualización existente** está seleccionada de manera predeterminada.

1. Para programar la regla, escriba **[!UICONTROL Start Date]** y **[!UICONTROL End Date]** para que la regla de precios esté activa.

   Puede introducir las fechas o elegir las fechas del _Calendario_ (![Icono del calendario](../assets/icon-calendar.png)).

   ![Regla de precios de catálogo - actualizar programación](./assets/price-rule-catalog-schedule-update.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save]**.

1. En la sección _Información de regla_, establezca **[!UICONTROL Status]** en `active`.

## Paso 6: Guardar y probar la regla

1. Cuando haya terminado, guarde la regla.

   - ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Haga clic en **[!UICONTROL Save and Apply]**.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Haga clic en **[!UICONTROL Save]**.

     La página Información de la regla muestra una cronología actualizada en Cambios programados de la regla.

     ![Reglas de precios de catálogo: cambios programados](./assets/price-rule-scheduled-changes-updated.png){width="600" zoomable="yes"}

1. Actualizar las propiedades de una regla:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Haga clic en **[!UICONTROL Edit]** para mostrar la página _[!UICONTROL Rule Information]_.

   - ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Haga clic en la regla de la lista para mostrar la página _[!UICONTROL Rule Information]_.

1. Pruebe la regla para asegurarse de que funciona correctamente.

   Las reglas de precios se procesan automáticamente con otras reglas del sistema cada noche. Cuando cree una regla de precios, deje tiempo suficiente para que entre en el sistema antes de probar la regla y asegurarse de que funciona correctamente. A medida que se añaden nuevas reglas, Commerce vuelve a calcular los precios y las prioridades en consecuencia.

## Demostración de regla de precio de catálogo

Vea este vídeo para obtener más información sobre la creación de reglas de precios de catálogo:

>[!VIDEO](https://video.tv.adobe.com/v/343834?quality=12&learn=on)

## Descripciones de campos

### [!UICONTROL Rule Information]

| Campo | Descripción |
|-----|-----------|
| [!UICONTROL Rule name] | (Obligatorio) El nombre de la regla es para referencia interna. |
| [!UICONTROL Description] | Una descripción de la regla debe incluir su propósito y explicar cómo se utiliza. |
| [!UICONTROL Websites] | (Obligatorio) Identifica los sitios web en los que se puede utilizar la regla. |
| [!UICONTROL Customer Groups] | (Obligatorio) Identifica los grupos de clientes a los que se aplica la regla. |
| [!UICONTROL Priority] | Un número que indica la prioridad de esta regla en relación con otras. Las prioridades de mayor a menor son `0,1,2,3...` |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Determina si la regla está activa en el almacén. Opciones: `Yes` / `No` |
| [!UICONTROL From] | ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Especifica el primer día en que la regla de precio está en vigor. Si se deja en blanco, la regla de precio entra en vigor cuando se guarda. |
| [!UICONTROL To] | ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Especifica el último día en que la regla de precio está en vigor. Si se deja en blanco, la regla de precio continúa indefinidamente. |

{style="table-layout:auto"}

### [!UICONTROL Conditions]

Especifica las condiciones que deben cumplirse antes de que la regla de precios de catálogo entre en vigor. Si se deja en blanco, la regla se aplica a todos los productos.

### [!UICONTROL Actions]

| Campo | Descripción |
|-----|-----------|
| [!UICONTROL Apply] | Determina el tipo de cálculo que se aplica a la compra. Opciones: <br/>**[!UICONTROL Apply as percentage of original]**- artículo de descuentos al restar un porcentaje del precio normal.<br/>**[!UICONTROL Apply as fixed amount]** - artículo de descuentos al restar un importe fijo del precio normal. <br/>**[!UICONTROL Adjust final price to this percentage]**- Ajusta el precio final en un porcentaje del precio normal.<br/>**[!UICONTROL Adjust final price to discount value]** - Establece el precio final en una cantidad fija con descuento. <br/><br/>**_Nota:_**El precio regular se refiere al precio base del producto sin ningún precio avanzado (especial/nivel/grupo) o descuentos promocionales. El precio final hace referencia al precio con descuento que aparece en el carro de compras. <br/>El precio del producto**_final _**se calcula como el precio**_mínimo _**relevante, utilizando la siguiente fórmula: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)` |
| [!UICONTROL Discount Amount] | (Obligatorio) El importe del descuento ofrecido. |
| [!UICONTROL Discard Subsequent Rules] | Determina si se pueden aplicar reglas adicionales a esta compra. Para evitar que se apliquen varios descuentos a la misma compra, seleccione `Yes`. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Related Dynamic Blocks]

{{ee-feature}}

Identifica cualquier [bloque dinámico](../content-design/dynamic-blocks.md) que esté asociado con la regla.
