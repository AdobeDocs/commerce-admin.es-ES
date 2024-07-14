---
title: Devuelve el atributo
description: Obtenga información sobre los atributos de devoluciones y cómo crear los atributos necesarios para procesar las devoluciones en su tienda.
exl-id: 639c1e94-1211-4a4e-8599-e54ed99b2355
feature: Attributes, Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Devuelve el atributo

{{ee-feature}}

Los atributos de devolución se utilizan para almacenar información necesaria durante el proceso de devolución del producto. Los atributos predeterminados incluyen la condición del producto devuelto, el motivo de la devolución y un campo que indica cómo se resolvió la devolución. El proceso para crear un atributo de devoluciones es similar a crear un [atributo del cliente](../customers/attribute-properties.md).

![Administrador - Devuelve atributos](./assets/attribute-returns.png){width="700" zoomable="yes"}

## Crear un atributo de devolución

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Returns]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add New Attribute]**.

   ![Nuevo resultado - propiedades del atributo](./assets/attribute-returns-new-properties.png){width="600" zoomable="yes"}

### Definición de las propiedades

1. Para identificar el atributo durante la entrada de datos, establezca **[!UICONTROL Default Label]**.

1. Para **[!UICONTROL Attribute Code]**, escriba un código que identifique el atributo en el sistema.

1. Para determinar el tipo de control de entrada que se usa para la entrada de datos, establezca **[!UICONTROL Input Type]** en uno de los siguientes:

   - `Text Field`
   - `Text Area`
   - `Dropdown`
   - `Yes/No`
   - `File`
   - `Image File`

1. Para que el campo sea un elemento obligatorio, establezca **[!UICONTROL Values Required]** en `Yes`.

1. Para asignar un valor inicial al campo, escriba un **[!UICONTROL Default Value]**.

1. Para validar la precisión de los datos introducidos en el campo antes de guardar el registro, establezca **[!UICONTROL Input Validation]** en uno de los siguientes valores:

   - `None`
   - `Alphanumeric`
   - `Alphanumeric with Space`
   - `Numeric Only`
   - `Alpha Only`
   - `URL`
   - `Email`

1. Para los tipos de entrada `Text Field` y `Text Area`, escriba **[!UICONTROL Minimum Text Length]** y **[!UICONTROL Maximum Text Length]**.

1. Para aplicar un filtro de preprocesamiento, establezca **[!UICONTROL Input/Output Filter]** en uno de los siguientes:

   - `None`
   - `Strip HTML Tags`
   - `Escape  HTML Entities`

1. Para que el atributo sea visible para los clientes, establezca **[!UICONTROL Show on Storefront]** en `Yes` en la sección _[!UICONTROL Storefront Properties]_.

1. (Opcional) Para **[!UICONTROL Sort Order]**, escriba un número para determinar dónde aparece este atributo en relación con los demás en la misma parte de la página. (`0` = primero, `1` = segundo, `2` = tercero, etc.)

### Administrar etiquetas/opciones

1. En el panel izquierdo, elija **[!UICONTROL Manage Labels/Options]**.

1. En la sección **[!UICONTROL Manage Titles (Size, Color, etc.)]**, escriba la etiqueta para cada vista de tienda.

   ![Administrar etiquetas](./assets/return-attributes.png){width="600" zoomable="yes"}

1. Si el **[!UICONTROL Input Type]** del atributo es `Dropdown`, administre las opciones en la sección **[!UICONTROL Manage Options (Values of Your Attribute)]**.

   - Para agregar una opción, haga clic en **[!UICONTROL Add Option]** e introduzca la etiqueta para el administrador y para cada vista de tienda.
   - Para hacer que una opción sea la opción predeterminada seleccionada, elija **[!UICONTROL Is Default]**.
   - Para quitar una opción, haga clic en **[!UICONTROL Delete]**.

1. Para guardar los cambios, haga clic en **[!UICONTROL Save Attribute]**.
