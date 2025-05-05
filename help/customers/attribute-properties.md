---
title: Propiedades de atributos del cliente
description: Obtenga información sobre cómo configurar las propiedades de atributos del cliente.
exl-id: d464f846-6a1f-43bd-876a-6834605ef794
feature: Customers, Configuration
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '1796'
ht-degree: 0%

---

# Propiedades de atributos del cliente

{{ee-feature}}

Los atributos del cliente proporcionan la información necesaria para respaldar los procesos de pedido, cumplimiento y gestión de clientes. Como su empresa es única, es posible que necesite campos además de los elementos predeterminados que proporciona el sistema. Puede agregar atributos personalizados a las secciones Información de cuenta, Libreta de direcciones e Información de facturación de la cuenta del cliente. Los atributos de la dirección [del cliente](address-attributes.md) también se pueden usar en la sección _Información de facturación_ durante el cierre de compra o cuando los huéspedes se registran para obtener una cuenta.

![Atributos del cliente](./assets/attributes-customer.png){width="700" zoomable="yes"}

## Paso 1: Completar las propiedades del atributo

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Customer]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add New Attribute]**.

   ![Propiedades de atributo del cliente](./assets/attribute-customer-new.png){width="600" zoomable="yes"}

1. En la sección **[!UICONTROL Attribute Properties]**, haga lo siguiente:

   - Escriba un(a) **[!UICONTROL Default Label]** que identifique el atributo durante la entrada de datos.

   - Escriba un **[!UICONTROL Attribute Code]** que identifique el atributo en el sistema.

   El código de atributo debe comenzar por una letra y puede incluir cualquier combinación de letras minúsculas (a-z) y números (0-9). El código debe tener menos de 30 caracteres de longitud y no puede incluir caracteres especiales ni espacios. El carácter de guion bajo (`_`) se puede usar para indicar un espacio.

   >[!TIP]
   >
   >**Acceso directo:** Para completar solo los campos requeridos, desplácese hacia abajo hasta _[!UICONTROL Storefront Properties]_, escriba&#x200B;_[!UICONTROL Sort Order]_ y guarde.

1. Complete las propiedades de entrada de datos:

   - Para determinar el tipo de control de entrada que se usa para la entrada de datos, establezca **[!UICONTROL Input Type]** en uno de los siguientes:

     | Tipo | Descripción |
     |----|-----------|
     | `Text Field` | Campo de texto de una sola línea. |
     | `Text Area` | Campo de entrada de varias líneas para introducir párrafos de texto, como una descripción del producto. Puede utilizar el editor de WYSIWYG para dar formato al texto con etiquetas de HTML o introducir las etiquetas directamente en el texto. |
     | `Multiple Line` | Crea varias líneas de texto para el atributo, de forma similar a una dirección de calle de varias líneas. El número de líneas de entrada de datos independientes puede ser de dos a 20. Use `Default Value` para especificar el valor inicial del campo. |
     | `Date` | Muestra un valor de fecha en el formato de fecha y zona horaria preferidos. Los valores de fecha se pueden seleccionar de una lista o un calendario ( ![Icono de calendario](../assets/icon-calendar.png)). <br/><br/>**_Nota:_**&#x200B;Según la configuración del sistema, los usuarios de_Admin _pueden introducir fechas directamente en un campo o seleccionar una fecha del calendario o lista. Para obtener información acerca de cómo especificar valores de fecha y hora, vea [Opciones de fecha y hora](../catalog/attributes-input-types.md#date-and-time-options). |
     | `Yes/No` | Muestra una lista desplegable con opciones predefinidas de `Yes` y `No`. |
     | `Dropdown` | Muestra una lista desplegable de valores que solo acepta una selección. El tipo de entrada desplegable es un componente clave de [productos configurables](../catalog/product-create-configurable.md). |
     | `Multiple Select` | Lista desplegable que acepta que se seleccionen varios valores. |
     | `File (attachment)` | Campo que permite cargar un archivo y asociarlo al atributo del cliente como archivo adjunto. |
     | `Image File` | Campo que permite cargar una imagen en la galería y asociarla al atributo del cliente. |

   - Si el cliente debe escribir un valor en el campo, establezca **[!UICONTROL Values Required]** en `Yes`.

   - Para asignar un valor inicial al campo, escriba un **[!UICONTROL Default Value]**.

   - Para comprobar la precisión de los datos especificados en el campo antes de guardar el registro, establezca **[!UICONTROL Input Validation]** en el tipo de datos que se permitirá en el campo. Los valores disponibles dependen del [!UICONTROL Input Type] especificado.

     | Valor | Descripción |
     |-----|-----------|
     | `None` | El campo no tiene validación de entrada durante la entrada de datos. |
     | `Alphanumeric` | Acepta cualquier combinación de números (0-9) y caracteres alfabéticos (a-z, A-Z) durante la entrada de datos. Para incluir caracteres especiales, consulte _Entidades HTML de escape_. |
     | `Alphanumeric with Space` | Acepta cualquier combinación de números (0-9), caracteres alfabéticos (a-z, A-Z) y espacios durante la entrada de datos. |
     | `Numeric Only` | Solo acepta números (0-9) durante la entrada de datos. |
     | `Alpha Only` | Solo acepta caracteres alfabéticos (a-z, A-Z) durante la entrada de datos. |
     | `URL` | Solo acepta una dirección URL durante la entrada de datos. |
     | `Email` | Solo acepta direcciones de correo electrónico durante la entrada de datos. |
     | `Length Only` | Valida la entrada en función de la longitud de los datos introducidos en el campo. |

   - Para limitar el tamaño de los tipos de entrada Campo de texto y Área de texto, escriba **[!UICONTROL Minimum Text Length]** y **[!UICONTROL Maximum Text Length]**.

   - Para aplicar un filtro de preprocesamiento a los valores especificados en un campo de texto, área de texto o tipo de entrada de varias líneas, establezca **[!UICONTROL Input/Output Filter]** en uno de los siguientes:

     | Valor | Descripción |
     |-----|-----------|
     | `None` | No aplica ningún filtro al texto introducido en el campo. |
     | `Strip HTML Tags` | Quita las HTML del texto. Este filtro puede ayudar a limpiar los datos que se pegan en un campo de otra fuente que incluye etiquetas de HTML. |
     | `Escape  HTML Entities` | Convierte los caracteres especiales encontrados en el texto en una secuencia de escape de HTML válida, como `&;`. Las secuencias de escape se encierran entre un signo &amp; y un punto y coma, y se utilizan con frecuencia para las comillas tipográficas, los derechos de autor y los símbolos de marca comercial. Las secuencias de escape también se utilizan para identificar caracteres como los símbolos menor que (`<`) y mayor que (`>`), y el carácter ampersand que también se utilizan en el código. Este filtro puede ayudar a limpiar los caracteres especiales que a veces se pegan en los campos de base de datos desde procesadores de texto. |

1. Complete las propiedades de la cuadrícula del cliente y del segmento:

   - Para poder incluir la columna en la cuadrícula Clientes, establezca **[!UICONTROL Add to Column Options]** en `Yes`.

   - Para filtrar la cuadrícula Clientes por este atributo, establezca **[!UICONTROL Use in Filter Options]** en `Yes`.

   - Para filtrar la cuadrícula Clientes por atributo de texto con diferentes condiciones de coincidencia de filtro, establezca **[!UICONTROL Grid Filter Condition Type]** en `Partial Match`, `Prefix Match` o `Full Match`. No afecta el campo _Buscar por palabra clave_ de la cuadrícula.

   - Para buscar en la cuadrícula Customers por este atributo, establezca **[!UICONTROL Use in Search Options]** en `Yes`.

   - Para que este atributo esté disponible para [segmentos del cliente](customer-segments.md), establezca **[!UICONTROL Use in Customer Segment]** en `Yes`.

## Paso 2: Completar las propiedades de la tienda

1. Vaya a la sección **[!UICONTROL Storefront Properties]**.

   ![Atributos del cliente - propiedades de la tienda](./assets/attribute-customer-storefront-properties.png){width="600" zoomable="yes"}

1. Para que el atributo sea visible para los clientes, establezca **[!UICONTROL Show on Storefront]** en `Yes`.

1. Escriba un número en el campo **[!UICONTROL Sort Order]**, que determina el orden de aparición cuando se enumera con otros atributos.

1. Establezca **[!UICONTROL Forms to Use]** en cada formulario que vaya a incluir el atributo. Para elegir varias opciones, mantenga presionada la tecla Ctrl y haga clic en cada formulario.

   - [&quot;Registro de cliente&quot;](customer-sign-in.md)
   - [&quot;Edición de cuenta de cliente&quot;](account-create.md)
   - [&quot;Cierre de compra de administrador&quot;](../stores-purchase/checkout-process.md)

## Paso 3: Completar la etiqueta y guardar

1. En el panel izquierdo, elija **[!UICONTROL Manage Labels/Options]**.

1. En **[!UICONTROL Manage Titles]**, escriba una etiqueta para identificar el atributo de cada [vista de tienda](../getting-started/websites-stores-views.md).

1. Una vez finalizado, haga clic en **[!UICONTROL Save Attribute]**.

   ![Atributos del cliente: etiquetas/opciones](./assets/attribute-customer-manage-label-options.png){width="600" zoomable="yes"}

## Descripciones de campos

### [!UICONTROL Attribute Properties]

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Default Label] | La etiqueta predeterminada que identifica el atributo en la administración y en la tienda. |
| [!UICONTROL Attribute Code] | Código único que identifica el atributo dentro del sistema. El código puede tener hasta 60 caracteres de longitud y no puede incluir espacios ni caracteres especiales. Se puede utilizar el símbolo de guion bajo en lugar de un espacio. |
| [!UICONTROL Input Type] | Determina el control de entrada utilizado para la entrada de datos. Opciones: <br/>**`Text Field`**- Campo de texto de una sola línea.<br/>**`Text Area`**: área de texto multilínea. <br/>**`Multiple Line`**: crea varias líneas de texto para el atributo, de forma similar a una dirección de calle de varias líneas. El número de líneas de entrada de datos independientes puede estar entre 2 y 20.<br/>**`Date`** - Muestra un campo de fecha con un calendario emergente.<br/>**`Dropdown`**: lista desplegable que solo acepta un valor para seleccionar.<br/>**`Multiple Select`**: lista desplegable que acepta que se seleccionen varios valores. <br/>**`Yes/No`**- Campo que ofrece solamente una opción de `Yes` o `No` valores.<br/>**`File (attachment)`**: campo que permite cargar un archivo y asociarlo al atributo del cliente como archivo adjunto. <br/>**`Image File`**: campo que permite cargar una imagen en la galería y asociarla al atributo del cliente. |
| [!UICONTROL Values Required] | Determina si se debe introducir un valor en el campo. Opciones: `Yes` / `No` |
| [!UICONTROL Default Value] | Especifica el valor inicial del atributo. |
| [!UICONTROL Input Validation] | La selección de opciones viene determinada por el tipo de entrada. Opciones: <br/>**`None`**- El campo no tiene validación de entrada durante la entrada de datos.<br/>**`Alphanumeric`** - Acepta cualquier combinación de números (0-9) y caracteres alfabéticos (a-z, A-Z) durante la entrada de datos. <br/>**`Alphanumeric with Space`**: permite que los espacios de la dirección de la calle cumplan los requisitos de longitud máxima del operador. Durante el cierre de compra, el cliente puede introducir cualquier combinación de números (0-9), caracteres alfabéticos (a-z, A-Z) y espacios en la dirección de la calle del destinatario y del remitente. Los espacios adicionales se recortan cuando se guarda la dirección.<br/>**`Numeric Only`** - Acepta solamente números (0-9) durante la entrada de datos. <br/>**`Alpha Only`**- Acepta solamente caracteres alfabéticos (a-z, A-Z) durante la entrada de datos.<br/>**`URL`** - Acepta solamente una dirección URL durante la entrada de datos. <br/>**`Email`**- Acepta solamente una dirección de correo electrónico durante la entrada de datos.<br/>**`Length Only`** - Valida la entrada en función de la longitud de los datos introducidos en el campo. |
| [!UICONTROL Input/Output Filter] | Aplica un filtro de preprocesamiento a los valores introducidos en un campo de texto, área de texto o tipo de entrada de varias líneas antes de guardar el registro. Opciones: <br/>**`None`**: no aplica ningún filtro al texto introducido en el campo.<br/>**`Strip HTML Tags`**: quita las etiquetas de HTML del texto. Este filtro puede ayudar a limpiar los datos que se pegan en un campo de otra fuente que incluye etiquetas de HTML. <br/>**`Escape HTML Entities`**: convierte los caracteres especiales encontrados en el texto en una secuencia de escape de HTML válida, como `amp;`. Las secuencias de escape se encierran entre un signo &amp; y un punto y coma, y se utilizan frecuentemente para comillas tipográficas, símbolos de copyright y símbolos de marca comercial. Las secuencias de escape también se utilizan para identificar caracteres como los símbolos menor que (`<`) y mayor que (`>`), y el carácter ampersand que también se utilizan en el código. Este filtro puede ayudar a limpiar los caracteres especiales que a veces se pegan en los campos de base de datos desde procesadores de texto. |
| [!UICONTROL Add to Column Options] | Especifica si el atributo se incluye como una columna en la cuadrícula [Clientes](customers-all.md). Opciones: `Yes` / `No` |
| [!UICONTROL Use in Filter Options] | Especifica si el atributo se puede utilizar como filtro para operaciones de búsqueda desde la cuadrícula. Opciones: `Yes` / `No` |
| [!UICONTROL Grid Filter Condition Type] | Especifica las condiciones de coincidencia de filtros para los atributos de las operaciones de búsqueda de la cuadrícula. No afecta el campo _Buscar por palabra clave_ de la cuadrícula. Opciones: `Partial Match` / `Prefix Match` / `Full Match` |
| [!UICONTROL Use in Search Options] | Especifica si el valor del atributo se puede utilizar como palabra clave en las operaciones de búsqueda. Opciones: `Yes` / `No` |
| [!UICONTROL Use in Customer Segment] | Determina si el atributo se incluye en [condiciones del segmento del cliente](customer-segments.md). Opciones: `Yes` / `No` |

### [!UICONTROL Storefront Properties]

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Show on Storefront] | Determina si el atributo aparece como un campo en la información del cliente de la tienda. Opciones: `Yes` / `No` |
| [!UICONTROL Sort Order] | Especifica el orden de este atributo en relación con otros atributos del cliente. El criterio de ordenación determina la secuencia en la que los campos reciben el foco durante la entrada de datos al utilizar la navegación mediante el teclado. |
| [!UICONTROL Forms to Use in] | Determina las páginas con formularios de entrada de datos donde aparece el atributo. Opciones: <br/>[`Customer Registration`](account-dashboard-account-information.md) <br/>[`Customer Account Edit`](account-create.md) <br/>[`Admin Checkout`](../stores-purchase/checkout-process.md) |

## Atributos de cliente predeterminados

| Código de atributo | Descripción |
| --------------- | ------------------ |
| `created_at` | La fecha de creación de la cuenta del cliente. |
| `updated_at` | La fecha en la que se actualizó la cuenta del cliente por última vez. |
| `website_id` | El ID de sitio web del sitio donde se creó la cuenta de cliente. |
| `store_id` | El ID de tienda del sitio donde se creó la cuenta de cliente. |
| `created_in` | La vista de la tienda en la que se creó la cuenta. |
| `group_id` | El ID del grupo de clientes donde se asigna el cliente. |
| `disable_auto_group_change` | Determina si los grupos de clientes se pueden asignar dinámicamente durante la [validación del identificador de IVA](../stores-purchase/vat.md#configure-vat-id-validation). |
| `prefix` | Cualquier prefijo que se utilice con el nombre del cliente (como Sr., Sra. o Dr.). |
| `firstname` | El nombre del cliente. |
| `middlename` | El segundo nombre o la inicial del segundo nombre del cliente. |
| `lastname` | El apellido del cliente. |
| `suffix` | Cualquier sufijo que se utilice con el nombre del cliente. (como Jr., Sr. o Esquire) |
| `email` | La dirección de correo electrónico del cliente. |
| `dob` | La fecha de nacimiento del cliente.  <br><br>**_Importante:_**&#x200B;De acuerdo con las prácticas recomendadas actuales de seguridad y privacidad, tenga en cuenta cualquier posible riesgo legal y de seguridad asociado con el almacenamiento de la fecha de nacimiento completa de los clientes (mes, día, año) con otros identificadores personales. Se recomienda limitar el almacenamiento de las fechas de nacimiento completas de los clientes y sugerir el uso del año de nacimiento del cliente como alternativa. |
| `taxvat` | El ID del impuesto sobre el valor añadido (IVA) asignado al cliente. La etiqueta predeterminada de este atributo es `VAT Number`. El campo Número de IVA siempre está presente en todas las direcciones de clientes de envío y facturación cuando se visualiza desde el administrador, pero no es un campo obligatorio. |
| `gender` | El sexo del cliente. |

## Demostración de atributos del cliente

Vea este vídeo para ver una demostración de la creación de atributos del cliente:

>[!VIDEO](https://video.tv.adobe.com/v/343661?quality=12&learn=on)
