---
title: Configuración del registro de regalos
description: Aprenda a configurar tipos de registro de regalos para los clientes de la tienda.
exl-id: d618c769-10be-4881-a799-42484d35c57b
feature: Gift, Storefront
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 0%

---

# Configuración del registro de regalos

{{ee-feature}}

Se puede crear un registro de regalos para cualquier tipo de evento, como una boda, cumpleaños, aniversario, bebé nuevo o cualquier otra ocasión especial. De forma predeterminada, Adobe Commerce incluye los siguientes eventos especiales:

- Bebé
- Cumpleaños
- Boda

Al crear un Registro, éste se convierte en una opción de la lista de tipos de Registro de regalos de la cuenta del cliente.

Puede utilizar uno de los tres registros de regalos preparados o crear su propio registro personalizado. Cada tipo de registro de regalos incluye varios atributos, que son los campos de entrada de datos que un cliente completa para crear un registro de regalos. Los atributos proporcionan información adicional sobre el evento, la hora y la ubicación, o cualquier otra información que sea necesaria. Según el tipo de entrada, algunos atributos tienen varias opciones. Por ejemplo, el tipo de registro de regalos `Wedding` tiene el atributo `Role`, con las opciones `Bride`, `Groom` y `Partner`. Para obtener más información acerca de los atributos y los tipos de entrada, vea [Atributos](../customers/attribute-properties.md).

![Tipos de registro de regalos](./assets/gift-registry-types.png){width="700" zoomable="yes"}

## Utilizar un registro de regalos preparado

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Registry]**.

   Los registros de cumpleaños, bodas y bebés están listos para que los clientes los usen desde sus cuentas.

1. Asegúrese de completar la [configuración de la plantilla de correo electrónico](../systems/email-templates.md#configure-email-templates) para que refleje su marca.

## Crear un registro de regalos personalizado

1. En la barra lateral de Administración, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Registry]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Gift Registry Type]**.

1. En **[!UICONTROL General Information]**, complete lo siguiente:

   - Escriba un único **[!UICONTROL Code]** para identificar internamente el registro de regalos.

     El código debe comenzar con una letra minúscula. El resto del código puede ser cualquier combinación de letras minúsculas (a-z), números (0-9) y guiones bajos (`_`).

   - Para **[!UICONTROL Label]**, escriba un nombre para el registro de regalos, tal como desea que aparezca en el almacén.

     Esta etiqueta es una opción de la lista de tipos de registro de regalos que están disponibles para el cliente.

   - Para **[!UICONTROL Sort Order]**, escriba un número para determinar el orden en que aparece este registro de regalos cuando se enumera con otros tipos.

   - Para activar el registro de regalos, establezca **[!UICONTROL Is Listed]** en `Yes`.

     ![Registro de regalos - información general](./assets/gift-registry-new-general-information.png){width="600" zoomable="yes"}

1. Examine cada sección del Registro de regalos para determinar el tipo de información que desea incluir.

1. En el panel izquierdo, elija **[!UICONTROL Attributes]** y haga clic en **[!UICONTROL Add Attribute]**.

   ![Registro de regalos - nuevo atributo](./assets/gift-registry-type-new-attribute.png){width="600" zoomable="yes"}

1. Para cada atributo, haga lo siguiente:

   - Asigne un(a) **[!UICONTROL Code]** único(a) para identificar el atributo internamente. El código puede tener hasta 15 caracteres de longitud y debe comenzar con una letra minúscula. El resto del código puede incluir letras minúsculas (`a`-`z`), números (`0`-`9`) y el carácter de subrayado (`_`) para separar palabras.

   - Elija **[!UICONTROL Input Type]** que se usará para la entrada de datos. Puede utilizar uno de los tipos personalizados o estáticos.

   - Si el tipo de entrada tiene varias opciones, haga clic en **[!UICONTROL Add New Option]** y complete la información de cada opción.

     Algunos tipos de entrada tienen propiedades adicionales. Por ejemplo, la Ubicación del evento tiene propiedades adicionales para que el evento pueda buscarse e incluirse en la lista pública de registros de regalos de la tienda.

      - Establezca **[!UICONTROL Attribute Group]** en la sección del registro de regalos en la que desea que aparezca el atributo.

      - Para **[!UICONTROL Label]**, escriba un nombre para identificar el campo de entrada de datos en el Registro.

      - Si el cliente debe realizar una selección o escribir un valor en el campo, establezca **[!UICONTROL Is Required]** en `Yes`.

      - Para **[!UICONTROL Sort Order]**, escriba un número para determinar la secuencia en la que aparece este registro de regalos cuando se enumera con otros registros de regalos que pueden estar disponibles en la tienda.

1. Para agregar otra opción, haga clic en **Agregar nueva opción**.

   Cada nueva opción añadida aparece en una nueva sección de la parte superior. Repita este proceso para el nuevo atributo.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

## Descripciones de campos

### [!UICONTROL General Information]

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Code] | Un nombre único para identificar internamente el tipo de registro de regalos. El primer carácter del código debe escribirse en minúsculas. El resto del código puede ser cualquier combinación de letras minúsculas (a-z), números (0-9) y el carácter de subrayado (`_`). |
| [!UICONTROL Label] | Nombre del tipo de registro de regalos que aparece en el almacén. |
| [!UICONTROL Sort Order] | Determina la secuencia en la que aparece este tipo de registro de regalos cuando se enumera con otros tipos. |
| [!UICONTROL Is Listed] | Determina si el tipo de registro de regalos está disponible para los clientes de la tienda. Opciones: `Yes` / `No`. |

{style="table-layout:auto"}

### [!UICONTROL Attributes]

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Code] | Un nombre único para identificar el atributo internamente. El código puede incluir cualquier combinación de letras minúsculas (a-z), números (0-9) y el carácter de subrayado (`_`). |
| [!UICONTROL Input Type] | Determina el tipo de datos y el control de entrada asociado al atributo, según el tipo. |
| [!UICONTROL Attribute Group] | Seleccione el grupo en el que el atributo aparece en el registro de regalos. |
| [!UICONTROL Label] | Nombre que identifica el atributo en el panel de cuentas del cliente. |
| [!UICONTROL Is Required] | Indica si el atributo es una entrada obligatoria. No se puede guardar el registro de regalos hasta que se hayan completado todos los atributos necesarios. Opciones: `Yes` / `No`. |
| [!UICONTROL Sort Order] | Determina la secuencia en la que aparece el atributo cuando se enumera con otros atributos. |

{style="table-layout:auto"}

#### [!UICONTROL Input Type Options]

Seleccione el tipo de datos y el control de entrada asociado al atributo.

**_[!UICONTROL Custom Types]_**

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Text] | Muestra el atributo como un campo de texto. |
| [!UICONTROL Select] | Muestra el atributo como una lista desplegable. Haga clic en **[!UICONTROL Add New Option]** para agregar más condiciones a la lista desplegable: <br/>**[!UICONTROL Code]**- Un nombre único para identificar el atributo internamente.<br/>**[!UICONTROL Label]**: nombre que identifica el atributo en el panel de cuentas del cliente.<br/>**[!UICONTROL Is Default]**: configure este modificador para seleccionar la condición predeterminada.<br/>**[!UICONTROL Delete Option]** - Haga clic para eliminar la opción. |
| [!UICONTROL Date] | Muestra el atributo como un campo de fecha. Opciones: `Short (3/23/2014)` / `Medium (Mar 23, 1914)` / `Long (March 23, 1914)` / `Full (Sunday, March 23, 2014)` |
| [!UICONTROL Country] | Muestra el atributo como una lista desplegable de países. Establezca **[!UICONTROL Show Region]** en: `Yes` / `No`. |

{style="table-layout:auto"}

**_[!UICONTROL Static Types]_**

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Event Date] | Determina cómo se utiliza el atributo de fecha en el almacén. Opciones: <br/>**[!UICONTROL Searchable]**- Determina si el atributo está disponible para la búsqueda avanzada. Opciones: `Yes` / `No`.<br/>**[!UICONTROL Is Listed]**: determina si el evento se incluye en la lista de eventos disponibles en el almacén. Opciones: `Yes` / `No`. <br/>**[!UICONTROL Date Format]**: determina el formato de la fecha del evento. Opciones: `Short (3/23/2014)` / `Medium (Mar 23, 1914)` / `Long (March 23, 1914)` / `Full (Sunday, March 23, 2014)` |
| [!UICONTROL Event Country] | Muestra el atributo como una lista de países. Opciones: <br/>**[!UICONTROL Searchable]**- Determina si el atributo está disponible para la búsqueda avanzada. Opciones: `Yes` / `No`.<br/>**[!UICONTROL Is Listed]**: determina si el evento se incluye en la lista de eventos disponibles en el almacén. Opciones: `Yes` / `No`. <br/>**[!UICONTROL Show Region]**: determina la región del evento. |
| [!UICONTROL Event Location] | La ubicación del evento relacionado con el registro de regalos. <br/>Establecer **[!UICONTROL Is Searcheable]** en: `Yes` / `No` <br/>Establecer **[!UICONTROL Is Listed]** en: `Yes` / `No` |
| [!UICONTROL Role] | La función que identifica al destinatario del regalo. Por ejemplo, `Bride`, `Groom` o `Partner`.<br/>**[!UICONTROL Is Searcheable]**- Establecido en `Yes`/ `No`<br/>** Está en la lista **- Establecido en `Yes` / `No`<br/>**[!UICONTROL Add New Option]** - Haga clic para agregar más condiciones al menú desplegable:<br/>**Código** - Un nombre único para identificar el atributo internamente.<br/>**[!UICONTROL Label]**: nombre que identifica el atributo en el panel de cuentas del cliente.<br/>**[!UICONTROL Is Default]**: configure este modificador para seleccionar la condición predeterminada.<br/>**[!UICONTROL Delete Option]**- Haga clic para eliminar la opción. |

{style="table-layout:auto"}

#### [!UICONTROL Attribute Group Options]

Seleccione el grupo en el que el atributo aparece en el registro de regalos.

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Event Information] | Agrupa todos los atributos del Registro de regalos que agregan información sobre el evento del Registro de regalos, su hora, lugar, etc. |
| [!UICONTROL Gift Registry Properties] | Combina todos los atributos que agregan información directamente sobre el registro de regalos. |
| [!UICONTROL Privacy Settings] | Enumera los atributos que agregan información sobre la privacidad de eventos del registro de regalos. |
| [!UICONTROL Recipients Information] | Agrupa los atributos que proporcionan información sobre la persona que crea un registro de regalos. |
| [!UICONTROL Shipping Address] | Combina los atributos que agregan información acerca de la dirección de envío del evento de registro de regalos. |

{style="table-layout:auto"}
