---
title: Temas
description: Más información [!DNL Commerce] temas, que incluyen archivos de diseño, archivos de plantilla, archivos de traducción y máscaras que definen el aspecto de su tienda.
exl-id: d2ccff51-5019-4f80-8eaa-3fe50d5cd6cc
feature: Page Content, Themes
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# Temas

Un tema es una colección de archivos que determina la presentación visual del almacén. La primera vez que instale [!DNL Commerce], los elementos de diseño de la tienda se basan en la variable _Predeterminado_ tema. Además de la temática predeterminada inicial que viene con su [!DNL Commerce] instalación, hay una amplia variedad de temas disponibles que puede utilizar _como está_ o modifique según sus necesidades.

Una temática adaptable ajusta el diseño de página para adaptarse al puerto de vista del dispositivo. La muestra _Luma_ La temática tiene un diseño flexible y adaptable que se puede ver desde el escritorio, la tableta o el dispositivo móvil.

[!DNL Commerce] las temáticas incluyen archivos de diseño, archivos de plantilla, archivos de traducción y máscaras. Una máscara es una colección de archivos CSS, imágenes y JavaScript compatibles que, juntos, crean la presentación visual y las interacciones que los clientes experimentan cuando visitan la tienda. Un desarrollador o profesional del diseño que entienda el diseño de temas de Commerce y tenga acceso a su servidor puede modificar y personalizar temas y máscaras. Para obtener más información, consulte la [_Guía para desarrolladores de Frontend_](https://developer.adobe.com/commerce/frontend-core/guide/themes/).

![Tema de Luma](./assets/design-responsive.png){width="600" zoomable="yes"}

## La temática predeterminada

El `Magento Blank` la temática adaptable procesa la visualización de la tienda para diferentes dispositivos e incorpora prácticas recomendadas para equipos de escritorio, mesas y dispositivos móviles. Algunas temáticas están diseñadas para utilizarse únicamente con dispositivos específicos. Cuándo [!DNL Commerce] detecta un ID de explorador específico, o un agente de usuario, y utiliza el tema configurado para el explorador específico. La cadena de búsqueda también puede incluir expresiones regulares compatibles con Perl (PCRE).

![Temas](./assets/themes.png){width="700" zoomable="yes"}

### Filtrar la cuadrícula de temas

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Haga clic **[!UICONTROL Filters]**.

1. Introduzca un rango de ID, un nombre de tema (o título), una ruta de carpeta o un tema principal.

1. Clic **[!UICONTROL Apply Filters]** para actualizar la lista de temáticas.

## Ver la configuración del tema actual

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. En la lista de temáticas instaladas, busque la temática que desee examinar y haga clic en la fila para mostrar la configuración.

1. Para ver una página de muestra, haga clic en **[!UICONTROL Theme Preview Image]**.

![Previsualizar tema](./assets/theme-settings.png){width="600" zoomable="yes"}

## Aplicar una temática predeterminada

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Busque la vista de tienda que desee configurar y haga clic en **[!UICONTROL Edit]** en el _[!UICONTROL Action]_columna.

1. En _[!UICONTROL Default Theme]_, configurado **[!UICONTROL Applied Theme]**al que desee utilizar para la vista actual.

   ![Tema aplicado](./assets/theme-default-apply.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save Configuration]**.

## Agregar una regla de agente de usuario

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. En _[!UICONTROL Design Rule]_, haga clic en **[!UICONTROL Add New User Agent Rule]**.

   ![Regla de diseño](./assets/theme-design-rule.png){width="600" zoomable="yes"}

1. Para **[!UICONTROL Search String]**, introduzca el ID de navegador del dispositivo específico.

   Las cadenas de búsqueda coinciden en el orden en que se escriben. Por ejemplo, para Firefox escriba:

   `/^mozilla/i`

1. Para introducir dispositivos adicionales, repita el proceso.

1. Cuando termine, haga clic en **[!UICONTROL Save Configuration]**.
