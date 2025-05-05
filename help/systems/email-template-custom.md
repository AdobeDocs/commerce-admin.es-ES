---
title: Personalizar plantillas de correo electrónico
description: Aprenda a personalizar las plantillas de correo electrónico para cada sitio web, tienda o vista de tienda.
exl-id: d328b84d-fab7-4956-9071-2d8848f7c21e
feature: Communications, Configuration
source-git-commit: c0d6523f820558c8cd6cfa6b745568784b9e784c
workflow-type: tm+mt
source-wordcount: '1303'
ht-degree: 0%

---

# Personalizar plantillas de correo electrónico

Commerce incluye una plantilla de correo electrónico predeterminada para la sección del cuerpo de cada mensaje que envía el sistema. La plantilla para el contenido del cuerpo se combina con las plantillas de encabezado y pie de página para crear el mensaje completo. El contenido tiene formato de HTML y CSS, y se puede editar y personalizar fácilmente agregando [variables](variables-predefined.md). Las plantillas de correo electrónico se pueden personalizar para cada sitio web, tienda o vista de tienda. Si usa plantillas personalizadas, asegúrese de actualizar la [configuración del sistema](email-templates.md#configure-email-templates) para asegurarse de que se usa la plantilla correcta. Para obtener información sobre cómo usar afirmaciones condicionales al personalizar la plantilla de correo electrónico, consulte la [documentación para desarrolladores](https://developer.adobe.com/commerce/frontend-core/guide/templates/email/#theme-based-customizations-1).

![Ejemplo: vista previa del correo electrónico de bienvenida](./assets/email-template-preview.png){width="500" zoomable="yes"}

Las plantillas predeterminadas incluyen su logotipo y la información de la tienda, y se pueden utilizar sin más personalización. Sin embargo, como práctica recomendada, debe ver cada plantilla y realizar los cambios necesarios antes de enviarla a los clientes.

- [Plantilla de encabezado](email-template-custom.md#header-template)
- [Plantilla de pie](email-template-custom.md#footer-template)
- [Plantillas de mensajes](email-template-custom.md#message-templates)

![Plantillas de correo electrónico](./assets/email-templates.png){width="700" zoomable="yes"}

## Información de plantilla

| Campo | Descripción |
| ----- | ----------- |
| [!UICONTROL Template Name] | Nombre de la plantilla personalizada. |
| [!UICONTROL Insert Variable] | Inserta una variable en la plantilla en la ubicación del cursor. |
| [!UICONTROL Template Subject] | El asunto de la plantilla aparece en la columna Asunto y se puede utilizar para ordenar y filtrar las plantillas de la lista. |
| [!UICONTROL Template Content] | El contenido de la plantilla en HTML. |
| [!UICONTROL Template Styles] | Cualquier declaración de estilo CSS necesaria para dar formato a la plantilla se puede escribir en el cuadro _[!UICONTROL Template Styles]_. |

{style="table-layout:auto"}

## Plantilla de encabezado

Después de completar la [configuración](email-templates.md#configure-email-templates), la plantilla de encabezado de correo electrónico incluye tu logotipo que está vinculado a tu tienda. Si tiene conocimientos básicos de HTML, puede usar fácilmente [variables predefinidas](variables-predefined.md) para agregar información de contacto de tienda al encabezado.

### Paso 1. Cargar la plantilla predeterminada

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Haga clic en **[!UICONTROL Add New Template]**.

1. En la sección **[!UICONTROL Load default template]**, haga clic en el selector **[!UICONTROL Template]** y elija `Magento_Email` > `Header`.

   ![Encabezado de plantilla de correo electrónico: cargar plantilla predeterminada](./assets/email-template-select-default-header.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Load Template]**.

   El código del HTML y las variables de la plantilla aparecen en el formulario.

### Paso 2. Personalización de la plantilla

1. Escriba **[!UICONTROL Template Name]** para el encabezado personalizado.

1. Escriba un(a) **[!UICONTROL Template Subject]** para organizar las plantillas.

   En la cuadrícula, la lista de plantillas se puede ordenar y filtrar por la columna _[!UICONTROL Subject]_.

   ![Información del encabezado de la plantilla de correo electrónico](./assets/email-template-information.png){width="600" zoomable="yes"}

1. En el cuadro **[!UICONTROL Template Content]**, modifique el HTML según sea necesario.

   >[!NOTE]
   >
   >Cuando trabaje con el código de plantilla, asegúrese de no sobrescribir nada que esté entre llaves dobles.

1. Para insertar una [variable](variables-reference.md), coloque el cursor en el código donde desee colocar la variable y haga clic en **[!UICONTROL Insert Variable]**.

1. Elija la variable que desea insertar.

   ![Plantilla de encabezado - Insertar variable](./assets/email-template-insert-variable.png){width="600" zoomable="yes"}

   Cuando se selecciona una variable, se inserta en el código una [etiqueta de marcado](markup-tags.md) para la variable.

   Aunque las variables Almacenar dirección de correo electrónico son las que se incluyen con mayor frecuencia en el encabezado, puede escribir el código de cualquier sistema o [variable personalizada](variables-custom.md) directamente en la plantilla.

1. Si necesita realizar alguna declaración CSS, escriba los estilos en el cuadro **[!UICONTROL Template Styles]**.

1. Cuando esté listo para revisar su trabajo, haga clic en **[!UICONTROL Preview Template]**.

   Realice los cambios necesarios en la plantilla.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Template]**.

   El encabezado personalizado ahora aparece en la lista de plantillas de correo electrónico disponibles.

### Paso 3. Actualizar la configuración

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. En la cuadrícula, busque la vista de almacén que desea configurar y haga clic en **[!UICONTROL Edit]** en la columna _[!UICONTROL Action]_.

1. Desplácese hacia abajo y expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Transactional Emails]**.

1. Elija el **[!UICONTROL Header Template]** que se usa como predeterminado para las notificaciones por correo electrónico.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

![Configuración del diseño de correo electrónico transaccional - Plantilla de encabezado](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

## Plantilla de pie

El pie de la plantilla de correo electrónico contiene la línea de cierre y firma del mensaje de correo electrónico. Puede cambiar el cierre para que se ajuste a su estilo y agregar información adicional, como el nombre de la empresa y la dirección debajo de su nombre.

### Paso 1. Cargar la plantilla predeterminada

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Haga clic en **[!UICONTROL Add New Template]**.

1. En la sección **[!UICONTROL Load default template]**, haga clic en el selector **[!UICONTROL Template]** y elija `Magento_Email` > `Footer`.

1. Haga clic en **[!UICONTROL Load Template]**.

   El código del HTML y las variables de la plantilla aparecen en el formulario.

### Paso 2. Personalización y previsualización de la plantilla

1. Escriba **[!UICONTROL Template Name]** para el pie de página personalizado.

1. Escriba un(a) **[!UICONTROL Template Subject]** para organizar las plantillas.

   En la cuadrícula, las plantillas se pueden ordenar y filtrar por la columna _[!UICONTROL Subject]_.

   ![Pie de página de plantilla de correo electrónico - información](./assets/email-template-footer-information.png){width="600" zoomable="yes"}

1. En el cuadro **[!UICONTROL Template Content]**, modifique el HTML según sea necesario.

   >[!NOTE]
   >
   >Cuando trabaje con el código de plantilla, asegúrese de no sobrescribir nada que esté entre llaves dobles.

1. Para insertar una [variable](variables-reference.md), coloque el cursor en el código donde desee colocar la variable y haga clic en **[!UICONTROL Insert Variable]**.

1. Elija la variable que desea insertar.

   Cuando se selecciona una variable, se inserta en el código una [etiqueta de marcado](markup-tags.md) para la variable.

   Aunque las variables de Contacto de tienda son las que se incluyen con más frecuencia en el pie de página, puede escribir el código de cualquier sistema o [variable personalizada](variables-custom.md) directamente en la plantilla.

1. Si necesita realizar alguna declaración CSS, escriba los estilos en el cuadro **[!UICONTROL Template Styles]**.

### Paso 3. Actualizar la configuración

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. En la cuadrícula, busque la vista de almacén que desea configurar y haga clic en **[!UICONTROL Edit]** en la columna _[!UICONTROL Action]_.

1. Desplácese hacia abajo y expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Transactional Emails]**.

1. Elija el **[!UICONTROL Footer Template]** que se usa como pie de página predeterminado en las notificaciones por correo electrónico.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

![Configuración del diseño de correo electrónico transaccional - Plantilla de pie de página](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

## Plantillas de mensajes

El proceso de personalizar el cuerpo de cada mensaje es el mismo que para personalizar el encabezado o el pie de página. La única diferencia es la plantilla de mensaje para cada actividad o evento que almacena en déclencheur una notificación. Puede usar las plantillas tal cual, o personalizarlas para que coincidan con su voz y marca. Además del texto de la plantilla, hay una amplia selección de variables [predefinidas](variables-predefined.md) y [personalizadas](variables-custom.md) permitidas que puede crear e incorporar a la plantilla.

### Paso 1. Cargar la plantilla predeterminada

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Haga clic en **[!UICONTROL Add New Template]**.

   ![Plantillas de correo electrónico: cargar plantilla predeterminada](./assets/email-templates-message-load-default.png){width="600" zoomable="yes"}

1. Haga lo siguiente:

   - En **[!UICONTROL Load default template]**, elija el(la) **[!UICONTROL Template]** que desee personalizar.

   - Haga clic en **[!UICONTROL Load Template]**.

### Paso 2. Personalización de la plantilla

1. Para **[!UICONTROL Template Name]**, escriba un nombre para la plantilla personalizada.

1. Si es necesario, cambie **[!UICONTROL Template Subject]**.

   Esta es la primera línea del mensaje, que es el saludo de forma predeterminada. Puede dejarlo tal cual, o puede introducir algo más descriptivo.

1. Tome nota de la ruta de acceso **[!UICONTROL Currently Used For]** a la plantilla, que es la ruta utilizada para actualizar la configuración.

   ![Plantillas de correo electrónico: información de plantilla](./assets/email-template-message-information.png){width="600" zoomable="yes"}

1. En el cuadro **[!UICONTROL Template Content]**, modifique el HTML según sea necesario.

   El contenido consiste en una combinación de etiquetas de HTML, directivas CSS, variables y texto.

   >[!NOTE]
   >
   >Cuando trabaje con el código de plantilla, asegúrese de no escribir accidentalmente el código entre llaves dobles.

1. Para insertar una variable, coloque el cursor en el código donde desee que aparezca la variable.

   La selección de variables varía según la plantilla e incluye las variables [predefinidas](variables-predefined.md) y [personalizadas](variables-custom.md) permitidas, si están disponibles.

1. Haga clic en **[!UICONTROL Insert Variable]** y elija la variable que desea insertar.

   Un comando para insertar la variable se coloca entre llaves y se agrega al código en la ubicación del cursor. Por ejemplo:

   `customVar code=my_custom_variable`

1. Para hacer declaraciones CSS, escriba los estilos en **[!UICONTROL Template Styles]**.

   ![Plantillas de correo electrónico - agregar estilos personalizados](./assets/email-template-add-custom-styles-min.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Los estilos personalizados se aplican al correo electrónico solamente si `{{template config_path="design/email/header_template"}}` está presente en _[!UICONTROL Template Styles]_. Para utilizar CSS personalizado sin una plantilla de encabezado predeterminada, debe proporcionarlos aquí dentro de la etiqueta de HTML `<style>`.

### Paso 3. Actualizar la configuración

La ruta de exploración _[!UICONTROL Currently Used For]_&#x200B;muestra dónde se utiliza la plantilla. En este ejemplo, la configuración de la plantilla se encuentra en la página&#x200B;_[!UICONTROL Customer Configuration]_, en la sección _[!UICONTROL Create New Account Options]_&#x200B;y en el campo&#x200B;_[!UICONTROL Default Welcome Email]_.

- Página - [!UICONTROL Customer Configuration]
- Sección - [!UICONTROL Create New Account Options]
- Campo - [!UICONTROL Default Welcome Email]

1. En la ruta de exploración **[!UICONTROL Currently Used For]**, haga clic en el vínculo para abrir la página de configuración de la plantilla.

   ![Plantilla de correo electrónico actual](./assets/email-template-new-currently-used-for.png){width="600" zoomable="yes"}

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) la sección y busque el campo de la plantilla de correo electrónico que ha personalizado.

1. Desactive la casilla de verificación **[!UICONTROL Use system value]** y haga clic en el nombre de la plantilla personalizada.

   ![Configuración de clientes - plantilla de correo electrónico de bienvenida predeterminada](./assets/email-template-message-configuration-default-template.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

1. En el mensaje que aparece en la parte superior del área de trabajo, haga clic en **[!UICONTROL Cache Management]** y borre cualquier caché no válida.

### Paso 4. Previsualizar y guardar la plantilla

1. Cuando esté listo para revisar su trabajo, haga clic en **[!UICONTROL Preview Template]**.

1. Actualice la plantilla según sea necesario.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Template]**.

   La plantilla personalizada ahora está disponible en la lista de plantillas de correo electrónico.
