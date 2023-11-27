---
title: Atributos de dirección del cliente
description: Obtenga información acerca de los atributos de dirección del cliente y cómo configurarlos.
exl-id: 637a0f81-4d8f-40cb-a1b6-537229b2ce5b
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '1471'
ht-degree: 0%

---

# Atributos de dirección del cliente

{{ee-feature}}

El conjunto de atributos Dirección del cliente determina las propiedades de las direcciones de las calles que se introducen en el [agenda](account-dashboard-address-book.md) desde la cuenta del cliente o durante [pago y envío](../stores-purchase/checkout-process.md).

Se pueden configurar atributos de dirección personalizados para proporcionar información adicional, como una dirección de correo electrónico opcional, una cuenta de Skype, un número de teléfono alternativo, un edificio o un condado. A continuación, el atributo personalizado se puede incorporar en la variable [plantilla de dirección](address-templates.md) que se utiliza para producir documentos de venta. El proceso para crear un atributo de dirección personalizado es casi igual que crear una [atributo del cliente](attribute-properties.md).

Los atributos de dirección del cliente se utilizan en los siguientes formularios:

- [Registro de dirección del cliente](account-create.md)
- [Dirección de cuenta del cliente](account-dashboard-address-book.md)

![Administrador - Atributos de dirección del cliente](./assets/attributes-customer-address.png){width="700" zoomable="yes"}

## Paso 1: Completar las propiedades del atributo

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Customer Address]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add New Attribute]**.

   ![Propiedades de atributos del cliente](./assets/attribute-customer-address-new.png){width="600" zoomable="yes"}

1. En el **[!UICONTROL Attribute Properties]** , haga lo siguiente:

   - Introduzca una **[!UICONTROL Default Label]** que identifica el atributo durante la entrada de datos.

   - Introduzca una **[!UICONTROL Attribute Code]** que identifica el atributo dentro del sistema.

     El código de atributo debe comenzar por una letra y puede incluir cualquier combinación de letras minúsculas (a-z) y números (0-9). El código debe tener menos de 30 caracteres de longitud y no puede incluir caracteres especiales ni espacios. El carácter de guion bajo (_) se puede utilizar para indicar un espacio.

     >[!TIP]
     >
     >**_Método abreviado:_** Para completar solo los campos obligatorios, desplácese hacia abajo hasta [!UICONTROL Storefront Properties], introduzca la variable [!UICONTROL Sort Order]y guarde.

1. Para determinar el tipo de control de entrada que se utiliza para la entrada de datos, establezca **[!UICONTROL Input Type]** a uno de los siguientes:

   - `Text Field` - Campo de texto de una sola línea.
   - `Text Area` - Un área de texto multilínea.
   - `Multiple Line` : crea varias líneas de texto para el atributo, de forma similar a una dirección de calle de varias líneas. El número de líneas de entrada de datos independientes puede estar entre 2 y 20. Utilice el `Default Value` para especificar el valor inicial del campo.
   - `Date` - Muestra un campo de fecha con un calendario emergente. Propiedades adicionales: Uso `Default Value` para especificar el valor inicial del campo. <br/>Uso `Minimal Value` para especificar la fecha más temprana que se puede introducir.  Uso `Maximum Value` para especificar la última fecha que se puede introducir.
   - `Dropdown` - Una lista desplegable que solo acepta un valor para seleccionar.
   - `Multiple Select` - Una lista desplegable que acepta que se seleccionen varios valores.
   - `Yes/No` - Un campo que solo ofrece una opción de `Yes` o `No` valores.
   - `File (attachment)` : Campo que permite cargar un archivo y asociarlo al atributo del cliente como archivo adjunto.
   - `Image File` : Campo que permite cargar una imagen en la galería y asociarla al atributo del cliente.

1. Si el cliente debe introducir un valor en el campo, establezca **[!UICONTROL Values Required]** hasta `Yes`.

1. Para asignar un valor inicial al campo, introduzca un **[!UICONTROL Default Value]**.

1. Para comprobar la precisión de los datos introducidos en el campo antes de guardar el registro, establezca **[!UICONTROL Input Validation]** al tipo de datos que se van a permitir en el campo. Los valores disponibles dependen de la variable _[!UICONTROL Input Type]_especificado.

   - `None` : el campo no tiene validación de entrada durante la entrada de datos.
   - `Alphanumeric` : acepta cualquier combinación de números (0-9) y caracteres alfabéticos (a-z, A-Z) durante la entrada de datos. Para incluir caracteres especiales, consulte [!UICONTROL Escape HTML Entities] en el paso siguiente.
   - `Alphanumeric with Space` : acepta cualquier combinación de números (0-9), caracteres alfabéticos (a-z, A-Z) y espacios durante la entrada de datos.
   - `Numeric Only` : solo acepta números (0-9) durante la entrada de datos.
   - `Alpha Only` : solo acepta caracteres alfabéticos (a-z, A-Z) durante la entrada de datos.
   - `URL` : solo acepta una dirección URL durante la entrada de datos.
   - `Email` : solo acepta una dirección de correo electrónico durante la entrada de datos.
   - `Length Only` : valida la entrada en función de la longitud de los datos introducidos en el campo.

1. Para aplicar un filtro de preprocesamiento a los valores introducidos en un campo de texto, área de texto o tipo de entrada de varias líneas, defina **[!UICONTROL Input/Output Filter]** a uno de los siguientes:

   - `None` - No aplica ningún filtro al texto introducido en el campo.
   - `Strip HTML Tags` - Elimina las etiquetas de HTML del texto. Este filtro puede ayudar a limpiar los datos que se pegan en un campo de otra fuente que incluye etiquetas de HTML.
   - `Escape  HTML Entities`  : convierte los caracteres especiales encontrados en el texto en una secuencia de escape de HTML válida, como `&;`. Las secuencias de escape se encierran entre un signo &amp; y un punto y coma, y se utilizan con frecuencia para las comillas tipográficas, los derechos de autor y los símbolos de marca comercial. Las secuencias de escape también se utilizan para identificar caracteres como el menor que (`<`) y mayor que (`>`), y el carácter ampersand que también se utiliza en el código. Este filtro puede ayudar a limpiar los caracteres especiales que a veces se pegan en los campos de base de datos desde procesadores de texto.

1. Complete las propiedades de la cuadrícula del cliente y del segmento:

   - Para poder incluir la columna en la cuadrícula Clientes, establezca **[!UICONTROL Add to Column Options]** hasta `Yes`.

   - Para filtrar la cuadrícula Clientes por este atributo, establezca **[!UICONTROL Use in Filter Options]** hasta `Yes`.

   - Para filtrar la cuadrícula Clientes por atributo de texto con diferentes condiciones de coincidencia de filtros, establezca **[!UICONTROL Grid Filter Condition Type]** hasta `Partial Match`, `Prefix Match`, o `Full Match`. No afecta al _Buscar por palabra clave_ para la cuadrícula.

   - Para buscar en la cuadrícula Clientes por este atributo, establezca **[!UICONTROL Use in Search Options]** hasta `Yes`.

   - Para que este atributo esté disponible para [segmentos del cliente](customer-segments.md), configurado **[!UICONTROL Use in Customer Segment]** hasta `Yes`.

## Paso 2: Completar las propiedades de la tienda

1. Desplácese hacia abajo hasta el **[!UICONTROL Storefront Properties]** sección.

   ![Atributos de dirección del cliente: propiedades de Storefront](./assets/attribute-customer-address-storefront-properties.png){width="600" zoomable="yes"}

1. Para que el atributo sea visible para los clientes, establezca **[!UICONTROL Show on Storefront]** hasta `Yes`.

1. Introduzca un número en la **[!UICONTROL Sort Order]** , que determina su orden de aparición cuando se enumera con otros atributos.

1. Establecer **[!UICONTROL Forms to Use]** a cada formulario que vaya a incluir el atributo.

   Para elegir ambas opciones, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) mientras hace clic en cada formulario.

   - [Registro de dirección del cliente](account-create.md)
   - [Dirección de cuenta del cliente](account-dashboard-address-book.md)

## Paso 3: Completar la etiqueta y guardar

1. En el panel de la izquierda, elija **[!UICONTROL Manage Labels/Options]**.

1. En **[!UICONTROL Manage Titles]**, introduzca una etiqueta para identificar el atributo de cada [vista de tienda](../getting-started/websites-stores-views.md).

1. Cuando termine, haga clic en **[!UICONTROL Save Attribute]**.

   ![Atributos de dirección del cliente: etiquetas/opciones](./assets/attribute-customer-address-new-manage-label-options.png){width="600" zoomable="yes"}

## Descripciones de campos

### [!UICONTROL Attribute Properties]

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Default Label] | La etiqueta predeterminada que identifica el atributo en la administración y en la tienda. |
| [!UICONTROL Attribute Code] | Código único que identifica el atributo dentro del sistema. El código puede tener hasta 21 caracteres de longitud y no puede incluir espacios ni caracteres especiales. Se puede utilizar el símbolo de guion bajo en lugar de un espacio. |
| [!UICONTROL Input Type] | Determina el [control de entrada](../catalog/attributes-input-types.md) que se utiliza para la entrada de datos. Opciones: <br/>**`Text Field`**- Campo de texto de una sola línea.<br/>**`Text Area`** - Un área de texto multilínea. <br/>**`Multiple Line`**: crea varias líneas de texto para el atributo, de forma similar a una dirección de calle de varias líneas. El número de líneas de entrada de datos independientes puede estar entre 2 y 20.<br/>**`Date`** - Muestra un campo de fecha con un calendario emergente.<br/>**`Dropdown`**- Una lista desplegable que solo acepta un valor para seleccionar.<br/>**`Multiple Select`** - Una lista desplegable que acepta que se seleccionen varios valores. <br/>**`Yes/No`**- Un campo que solo ofrece una opción de `Yes` o `No` valores.<br/>**`File (attachment)`** : Campo que permite cargar un archivo y asociarlo al atributo del cliente como archivo adjunto. <br/>**`Image File`**: Campo que permite cargar una imagen en la galería y asociarla al atributo del cliente. |
| [!UICONTROL Values Required] | Determina si se debe introducir un valor en el campo. Opciones: `Yes` / `No` |
| [!UICONTROL Default Value] | Especifica el valor inicial del atributo. |
| [!UICONTROL Input Validation] | La selección de opciones viene determinada por el tipo de entrada. Opciones: <br/>**`None`**: el campo no tiene validación de entrada durante la entrada de datos.<br/>**`Alphanumeric`** : acepta cualquier combinación de números (0-9) y caracteres alfabéticos (a-z, A-Z) durante la entrada de datos. <br/>**`Alphanumeric with Space`**- Permite que los espacios en la dirección de la calle cumplan con los requisitos de longitud máxima del transportista. Durante el cierre de compra, el cliente puede introducir cualquier combinación de números (0-9), caracteres alfabéticos (a-z, A-Z) y espacios en la dirección de la calle del destinatario y del remitente. Los espacios adicionales se recortan cuando se guarda la dirección.<br/>**`Numeric Only`** : solo acepta números (0-9) durante la entrada de datos. <br/>**`Alpha Only`**: solo acepta caracteres alfabéticos (a-z, A-Z) durante la entrada de datos.<br/>** URL **: solo acepta una dirección URL durante la entrada de datos.<br/>**`Email`** : solo acepta una dirección de correo electrónico durante la entrada de datos. <br/>**`Length Only`**: valida la entrada en función de la longitud de los datos introducidos en el campo. |
| [!UICONTROL Input/Output Filter] | Aplica un filtro de preprocesamiento a los valores introducidos en un campo de texto, área de texto o tipo de entrada de varias líneas antes de guardar el registro. Opciones: <br/>**`None`**- No aplica ningún filtro al texto introducido en el campo.<br/>**`Strip HTML Tags`** - Elimina las etiquetas de HTML del texto. Este filtro puede ayudar a limpiar los datos que se pegan en un campo de otra fuente que incluye etiquetas de HTML. <br/>**`Escape HTML Entities`**: convierte los caracteres especiales encontrados en el texto en una secuencia de escape de HTML válida, como `amp;`. Las secuencias de escape se encierran entre un signo &amp; y un punto y coma, y se utilizan frecuentemente para comillas tipográficas, símbolos de copyright y símbolos de marca comercial. Las secuencias de escape también se utilizan para identificar caracteres como el menor que (`<`) y mayor que (`>`), y el carácter ampersand que también se utiliza en el código. Este filtro puede ayudar a limpiar los caracteres especiales que a veces se pegan en los campos de base de datos desde procesadores de texto. |
| [!UICONTROL Add to Column Options] | Especifica si el atributo se incluye como una columna en la variable [Clientes](./customers-all.md) rejilla. Opciones: `Yes` / `No` |
| Uso en opciones de filtro | Especifica si el atributo se puede utilizar como filtro para operaciones de búsqueda desde la cuadrícula. Opciones: `Yes` / `No` |
| [!UICONTROL Grid Filter Condition Type] | Especifica las condiciones de coincidencia de filtros para los atributos en operaciones de búsqueda desde la cuadrícula. No afecta al _[!UICONTROL Search by keyword]_para la cuadrícula. Opciones: `Partial Match` / `Prefix Match` / `Full Match` |
| [!UICONTROL Use in Search Options] | Especifica si el valor del atributo se puede utilizar como palabra clave en las operaciones de búsqueda. Opciones: `Yes` / `No` |
| [!UICONTROL Use in Customer Segment] | Determina si el atributo se incluye en [segmento de cliente](./customer-segments.md) condiciones. Opciones: `Yes` / `No` |

### [!UICONTROL Storefront Properties]

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Show on Storefront] | Determina si el atributo aparece como un campo en la información del cliente de la tienda. Opciones: `Yes` / `No` |
| [!UICONTROL Sort Order] | Especifica el orden de este atributo en relación con otros atributos del cliente. El criterio de ordenación determina la secuencia en la que los campos reciben el foco durante la entrada de datos al utilizar la navegación mediante el teclado. |
| [!UICONTROL Forms to Use in] | Determina las páginas con formularios de entrada de datos donde aparece el atributo. Opciones: <br/>[`Customer Address Registration`](account-create.md) <br/>[`Customer Account Address`](account-dashboard-address-book.md) |
