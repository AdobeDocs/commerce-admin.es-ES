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

Los atributos de devolución se utilizan para almacenar información necesaria durante el proceso de devolución del producto. Los atributos predeterminados incluyen la condición del producto devuelto, el motivo de la devolución y un campo que indica cómo se resolvió la devolución. El proceso para crear un atributo de devolución es similar a crear un [atributo del cliente](../customers/attribute-properties.md).

![Administrador - Devuelve atributos](./assets/attribute-returns.png){width="700" zoomable="yes"}

## Crear un atributo de devolución

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Returns]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add New Attribute]**.

   ![Nuevo retorno: propiedades de atributo](./assets/attribute-returns-new-properties.png){width="600" zoomable="yes"}

### Definición de las propiedades

1. Para identificar el atributo durante la entrada de datos, establezca **[!UICONTROL Default Label]**.

1. Para **[!UICONTROL Attribute Code]**, introduzca un código que identifique el atributo dentro del sistema.

1. Para determinar el tipo de control de entrada que se utiliza para la entrada de datos, establezca **[!UICONTROL Input Type]** a uno de los siguientes:

   - `Text Field`
   - `Text Area`
   - `Dropdown`
   - `Yes/No`
   - `File`
   - `Image File`

1. Para que el campo sea un elemento obligatorio, establezca **[!UICONTROL Values Required]** hasta `Yes`.

1. Para asignar un valor inicial al campo, introduzca un **[!UICONTROL Default Value]**.

1. Para validar la precisión de los datos introducidos en el campo antes de guardar el registro, establezca **[!UICONTROL Input Validation]** a uno de los siguientes:

   - `None`
   - `Alphanumeric`
   - `Alphanumeric with Space`
   - `Numeric Only`
   - `Alpha Only`
   - `URL`
   - `Email`

1. Para el `Text Field` y `Text Area` tipos de entrada, introduzca la variable **[!UICONTROL Minimum Text Length]** y **[!UICONTROL Maximum Text Length]**.

1. Para aplicar un filtro de preprocesamiento, defina **[!UICONTROL Input/Output Filter]** a uno de los siguientes:

   - `None`
   - `Strip HTML Tags`
   - `Escape  HTML Entities`

1. Para que el atributo sea visible para los clientes, establezca **[!UICONTROL Show on Storefront]** hasta `Yes` en el _[!UICONTROL Storefront Properties]_sección.

1. (Opcional) Para **[!UICONTROL Sort Order]**, introduzca un número para determinar dónde aparece este atributo en relación con los demás en la misma parte de la página. (`0` = primero, `1` = segundo, `2` = tercero, etc.)

### Administrar etiquetas/opciones

1. En el panel izquierdo, elija **[!UICONTROL Manage Labels/Options]**.

1. En el **[!UICONTROL Manage Titles (Size, Color, etc.)]** , introduzca la etiqueta para cada vista de tienda.

   ![Administrar etiquetas](./assets/return-attributes.png){width="600" zoomable="yes"}

1. Si la variable **[!UICONTROL Input Type]** para el atributo es `Dropdown`, administre las opciones de **[!UICONTROL Manage Options (Values of Your Attribute)]** sección.

   - Para añadir una opción, haga clic en **[!UICONTROL Add Option]** e introduzca la etiqueta para el administrador y para cada vista de tienda.
   - Para que una opción sea la opción seleccionada por defecto, elija **[!UICONTROL Is Default]**.
   - Para quitar una opción, haga clic en **[!UICONTROL Delete]**.

1. Para guardar los cambios, haga clic en **[!UICONTROL Save Attribute]**.
