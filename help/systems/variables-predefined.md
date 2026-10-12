---
title: Usar variables predefinidas
description: Obtenga información sobre las variables predefinidas y cómo añadirlas en una plantilla de correo electrónico.
exl-id: 01e909c4-c932-4262-9f33-bd2740a6355f
role: Admin, User
feature: System, Variables, Page Content, Communications
TQID: 'https://experienceleague.adobe.com/TKhaNVRFLc3VK0iDkCpqoWSnvFRJmDWAIw1uBPzlh00'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 8d0b446f-5b16-5a10-b272-01143504a11c
    internal-label: System
  - id: 17d326fa-534a-55a5-b46f-8ae1de1e2f75
    internal-label: Page Content
  - id: bb03f6c4-cab9-560e-9d02-5816e1808d17
    internal-label: Communications
subfeature_v2:
  - id: 2191e157-828a-5358-ad69-ebcaa8402915
    internal-label: Variables
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%
---
# Usar variables predefinidas

Las variables [Predefined](variables-predefined.md) facilitan la personalización de las plantillas de [correo electrónico](email-templates.md) y [newsletter](../merchandising-promotions/newsletters.md), así como de otros tipos de contenido. La lista de variables [predefinidas](variables-predefined.md) permitidas aparece al hacer clic en el botón Insertar variable. Como se muestra en la siguiente imagen, la lista de variables disponibles para una plantilla de correo electrónico específica viene determinada por los datos asociados a la plantilla. Consulte la [Referencia de variable](variables-reference.md) para obtener una lista de las plantillas de correo electrónico que se usan con frecuencia y sus variables asociadas.

![Variables predefinidas para la plantilla de correo electrónico](./assets/email-template-new-pickup-order-predefined-variables.png){width="700" zoomable="yes"}

## Añadir una variable a una plantilla de correo electrónico

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Realice una de las siguientes acciones:

   - Para añadir la variable a una plantilla existente, haga clic en la plantilla de la lista para abrirla en modo de edición.

   - Para usar la variable en una plantilla nueva, haga clic en **[!UICONTROL Add New Template]** y personalice el código de plantilla predeterminado. Ver [Plantillas de mensajes](email-template-custom.md#message-templates).

1. En _[!UICONTROL Load default template]_, elija el(la)**[!UICONTROL Template]**que desee personalizar.

1. Para aplicar una plantilla, haga clic en **[!UICONTROL Load Template]**.

   El campo _[!UICONTROL Currently used for]_muestra la ruta de configuración de la plantilla._[!UICONTROL Template Subject]_ y _[!UICONTROL Template Content]_se generan automáticamente en relación con la plantilla seleccionada.

   - **[!UICONTROL Template Subject]**: este texto se muestra en la línea de asunto de un correo electrónico.

   - **[!UICONTROL Template Content]**: este texto se muestra en todo el contenido del correo electrónico enviado.

   ![Contenido de plantilla de correo electrónico](./assets/email-template-content.png){width="600" zoomable="yes"}

1. Escriba un **[!UICONTROL Template Name]**.

1. Para obtener una lista de las [variables predefinidas](variables-predefined.md) que se pueden usar con esta plantilla de correo electrónico, haga clic en **[!UICONTROL Insert Variable]**.

   Determine qué variable desea insertar en la plantilla. A continuación, haga clic en _Cerrar_ (X) en la esquina superior derecha. (Volverá a esto más tarde).

1. Para ver una maqueta de la plantilla, haga clic en **[!UICONTROL Preview Template]** en la barra de botones.

   Cuando la vista previa se abra en una nueva pestaña, determine dónde desea colocar la variable en relación con el otro contenido. A continuación, vuelva a la pestaña original para continuar.

   ![Plantilla de vista previa](./assets/email-template-new-pickup-order-preview.png){width="600" zoomable="yes"}

1. En el cuadro **[!UICONTROL Template Content]**, coloque el punto de inserción donde desee que aparezca la variable y haga clic en **[!UICONTROL Insert Variable...]**.

1. En la lista de variables disponibles, haga clic en la que desee insertar en la plantilla.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Template]**.

## Convertir la plantilla en texto sin formato

1. Abra una plantilla en modo de edición.

1. En la parte superior de la página, haga clic en **[!UICONTROL Convert to Plain Text]**.

1. Cuando se le pida que elimine etiquetas, haga clic en **[!UICONTROL OK]**.

1. Para guardar la versión de texto sin formato, haga clic en **[!UICONTROL Save Template]**.

## Restaurar la versión de HTML

1. En la parte superior de la página, haga clic en **[!UICONTROL Return HTML Version]**.

1. Para guardar la versión de HTML de la plantilla, haga clic en **[!UICONTROL Save Template]**.
