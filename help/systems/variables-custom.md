---
title: Añadir variables personalizadas
description: Obtenga información sobre cómo crear variables personalizadas e insertarlas en páginas, bloques y contenido de productos.
exl-id: 8233518a-abcf-4889-b75b-4aa503c7cebb
role: Admin, User
feature: System, Variables, Page Content, Communications
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 1%

---

# Añadir variables personalizadas

Para satisfacer las necesidades específicas de su empresa, puede crear variables personalizadas e insertarlas en [páginas](../content-design/pages.md), [bloques](../content-design/blocks.md) y [plantillas de correo electrónico](email-templates.md). La lista de variables permitidas que aparece al hacer clic en el botón _Insertar variable_ incluye [variables predefinidas](variables-predefined.md) y personalizadas. La lista de variables disponibles para una plantilla de correo electrónico específica viene determinada por los datos asociados a la plantilla. Consulte la [Referencia de variable](variables-reference.md) para obtener una lista de las plantillas de correo electrónico que se usan con frecuencia y sus variables asociadas.

![Variables personalizadas](./assets/variables-custom.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Solo se pueden utilizar variables predefinidas o personalizadas permitidas en las plantillas de correo electrónico y newsletter.

## Paso 1: Crear una variable personalizada

1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Custom Variables]**.

1. Haga clic en **[!UICONTROL Add New Variable]**.

1. Escriba un identificador para **[!UICONTROL Variable Code]**, usando todos los caracteres en minúsculas sin espacios.

   Si es necesario, puede utilizar un carácter de guion bajo o un guión para representar un espacio. Por ejemplo: `my_custom_variable`

1. Escriba un **[!UICONTROL Variable Name]**, que se usa como referencia interna. Por ejemplo: `My Custom Variable`

1. Para introducir el valor asociado a la variable, realice una de las siguientes acciones:

   - Para **[!UICONTROL Variable HTML Value]**, introduzca el valor de la variable con formato de etiquetas de HTML simples. Por ejemplo:

     `<b>This formatted content appears in place of the variable.</b>`

   - Para **[!UICONTROL Variable Plain Value]**, escriba el valor de la variable como texto sin formato. Por ejemplo:

     `This unformatted content appears in place of the variable.`

   >[!TIP]
   >
   >Si necesita más espacio, arrastre la esquina inferior derecha del cuadro de texto.

   ![Nueva variable personalizada](./assets/variable-custom-add.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

## Paso 2: Insertar la variable personalizada en el contenido

Use [!DNL Page Builder] para insertar una variable personalizada.

1. Abra la página, bloque, categoría o producto donde desee agregar la variable al contenido.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Content]**.

1. Haga clic en **[!UICONTROL Edit with Page Builder]**.

1. En el panel izquierdo, haga clic en **[!UICONTROL Elements]** y realice una de las siguientes acciones:

   - Haga clic en un área de texto existente en la que desee insertar la variable.

   - Arrastre un nuevo objeto **[!UICONTROL Text]** al escenario.

1. En el extremo derecho de la barra de herramientas del editor, haga clic en ( ![Insertar variable](./assets/editor-btn-insert-variable.png) ) para insertar una variable.

   ![[!DNL Page Builder] escenario y panel](./assets/variable-custom-pagebuilder-stage.png){width="600" zoomable="yes"}

1. En la lista, seleccione la variable personalizada que desee insertar y haga clic en **[!UICONTROL Insert Variable]**.

   ![Nueva variable personalizada](./assets/variable-custom-insert-select.png){width="600" zoomable="yes"}

   El identificador de variable aparece como un marcador de posición en el editor.

   ![[!DNL Page Builder] fase - marcador de posición de variable](./assets/pagebuilder-variable-inserted.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.
