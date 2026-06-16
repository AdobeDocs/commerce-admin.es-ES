---
title: Añadir variables personalizadas
description: Obtenga información sobre cómo crear variables personalizadas e insertarlas en páginas, bloques y contenido de productos.
exl-id: 8233518a-abcf-4889-b75b-4aa503c7cebb
role: Admin, User
feature: System, Variables, Page Content, Communications
TQID: https://experienceleague.adobe.com/zhgemfdr2g5sanaFuiF9l20figj9ZD-3codE97WWWg8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 344
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

   - Para **[!UICONTROL Variable HTML Value]**, introduzca el valor de la variable con formato de etiquetas HTML simples. Por ejemplo:

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
