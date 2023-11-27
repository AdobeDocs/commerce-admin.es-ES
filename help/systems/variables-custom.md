---
title: Añadir variables personalizadas
description: Obtenga información sobre cómo crear variables personalizadas e insertarlas en páginas, bloques y contenido de productos.
exl-id: 8233518a-abcf-4889-b75b-4aa503c7cebb
role: Admin, User
feature: System, Variables, Page Content, Communications
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 2%

---

# Añadir variables personalizadas

Para satisfacer las necesidades específicas de su empresa, puede crear variables personalizadas e insertarlas en [páginas](../content-design/pages.md), [bloques](../content-design/blocks.md), y [plantillas de correo electrónico](email-templates.md). La lista de variables permitidas que aparece al hacer clic en el icono _Insertar variable_ incluye ambos botones [predefinido](variables-predefined.md) y variables personalizadas. La lista de variables disponibles para una plantilla de correo electrónico específica viene determinada por los datos asociados a la plantilla. Consulte la [Referencia de variables](variables-reference.md) para obtener una lista de las plantillas de correo electrónico utilizadas frecuentemente y sus variables asociadas.

![Variables personalizadas](./assets/variables-custom.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Solo se pueden utilizar variables predefinidas o personalizadas permitidas en las plantillas de correo electrónico y newsletter.

## Paso 1: Crear una variable personalizada

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Custom Variables]**.

1. Haga clic **[!UICONTROL Add New Variable]**.

1. Introduzca un identificador para **[!UICONTROL Variable Code]**, usando todos los caracteres en minúsculas sin espacios.

   Si es necesario, puede utilizar un carácter de guion bajo o un guión para representar un espacio. Por ejemplo: `my_custom_variable`

1. Introduzca una **[!UICONTROL Variable Name]**, que se utiliza como referencia interna. Por ejemplo: `My Custom Variable`

1. Para introducir el valor asociado a la variable, realice una de las siguientes acciones:

   - Para **[!UICONTROL Variable HTML Value]**, introduzca el valor de la variable con formato de etiquetas de HTML simples. Por ejemplo:

     `<b>This formatted content appears in place of the variable.</b>`

   - Para **[!UICONTROL Variable Plain Value]**, introduzca el valor de la variable como texto sin formato. Por ejemplo:

     `This unformatted content appears in place of the variable.`

   >[!TIP]
   >
   >Si necesita más espacio, arrastre la esquina inferior derecha del cuadro de texto.

   ![Nueva variable personalizada](./assets/variable-custom-add.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

## Paso 2: Insertar la variable personalizada en el contenido

Uso [!DNL Page Builder] para insertar una variable personalizada.

1. Abra la página, bloque, categoría o producto donde desee agregar la variable al contenido.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Content]** sección.

1. Haga clic **[!UICONTROL Edit with Page Builder]**.

1. En el panel izquierdo, haga clic en **[!UICONTROL Elements]** y realice una de las siguientes acciones:

   - Haga clic en un área de texto existente en la que desee insertar la variable.

   - Arrastrar un nuevo **[!UICONTROL Text]** objeto al escenario.

1. En el extremo derecho de la barra de herramientas del editor, haga clic en ( ![Insertar variable](./assets/editor-btn-insert-variable.png) ) para insertar una variable.

   ![[!DNL Page Builder] escenario y panel](./assets/variable-custom-pagebuilder-stage.png){width="600" zoomable="yes"}

1. En la lista, seleccione la variable personalizada que desee insertar y haga clic en **[!UICONTROL Insert Variable]**.

   ![Nueva variable personalizada](./assets/variable-custom-insert-select.png){width="600" zoomable="yes"}

   El identificador de variable aparece como un marcador de posición en el editor.

   ![[!DNL Page Builder] stage - variable placeholder](./assets/pagebuilder-variable-inserted.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save]**.
