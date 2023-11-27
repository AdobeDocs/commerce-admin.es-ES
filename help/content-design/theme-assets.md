---
title: Recursos del tema
description: Obtenga información sobre cómo administrar los recursos de temáticas, como CSS, fuentes, imágenes y archivos JavaScript.
exl-id: 326c648e-eace-45a0-b53d-bbc8702fee05
feature: Page Content, Themes
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# Recursos del tema

El _archivos estáticos_ son la colección de recursos que un tema utiliza, como CSS, fuentes, imágenes y JavaScript. La ubicación de los archivos estáticos se especifica en la [URL básica](../stores-purchase/store-urls.md) configuración. Puede agregar una firma digital a la dirección URL de cada archivo estático para que los exploradores puedan detectar cuándo está disponible una versión más reciente. Se utiliza la versión más reciente del archivo si la firma difiere de lo que se almacena en la caché del explorador.

Para una instalación estándar, los recursos asociados a una temática se organizan en la variable `web` en la siguiente ubicación debajo de [!DNL Commerce] raíz.

`[commerce_root]/app/design/frontend/Magento/[theme_name]/web`

## Agregar una firma digital a las direcciones URL de los archivos estáticos

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL Developer]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Static Files Settings]** sección.

   ![Configuración de archivos estáticos](./assets/developer-static-files-settings.png){width="500" zoomable="yes"}

1. Establecer **[!UICONTROL Sign Static Files]** hasta `Yes`.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

| Tipo de archivo | Descripción |
|--- |--- |
| CSS | Controlar el estilo visual asociado a la piel. Ejemplo de ubicación en el servidor: `[commerce]/app/design/frontend/Magento/[theme]/web/css` |
| Fuentes | Proporcione las fuentes disponibles para usar en la temática. Ubicación en el servidor: `[commerce]/app/design/frontend/Magento/[theme]/web/fonts` |
| Imágenes | Proporcione los recursos gráficos utilizados por la temática, incluidos botones, texturas de fondo, etc. Ejemplo de ubicación en el servidor: `[commerce]/app/design/frontend/Magento/[theme]/web/images` |
| JS | Rutinas JavaScript específicas del tema y funciones a las que se puede llamar. Ejemplo de ubicación en el servidor: `[commerce]/app/design/frontend/Magento/[theme]/web/js` |

{style="table-layout:auto"}

## Combinar archivos CSS

Como parte del esfuerzo por optimizar el sitio y reducir el tiempo de carga de la página, puede reducir el número de archivos CSS independientes combinándolos en un único archivo condensado. Si abre un archivo CSS combinado, verá un flujo continuo de texto, con los saltos de línea eliminados. No puede editar el archivo combinado, por lo que es mejor esperar hasta que esté fuera del modo de desarrollo y ya no realice cambios frecuentes en CSS.

>[!NOTE]
>
>Los archivos CSS se pueden combinar desde el _Administrador_ panel solo cuando se trabaja en [modo de desarrollador](../systems/developer-tools.md#operation-modes).

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, **[!UICONTROL Advanced]** y elija **[!UICONTROL Developer]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL CSS Settings]** sección.

   ![Configuración de CSS](./assets/developer-css-settings.png){width="500" zoomable="yes"}

   Para obtener descripciones detalladas de estas opciones de configuración, consulte [Configuración de CSS](../configuration-reference/advanced/developer.md#css-settings) en el _Referencia de configuración_.

1. Establecer **[!UICONTROL Merge CSS Files]** hasta `Yes`.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Combinar archivos JavaScript

Se pueden combinar varios archivos JavaScript en un único archivo condensado para reducir el tiempo de carga de la página. Si abre un archivo JavaScript combinado, verá un flujo continuo de texto, con los saltos de línea eliminados. Si ha finalizado el proceso de desarrollo y el código no contiene errores, considere la posibilidad de combinar los archivos.

>[!NOTE]
>
>Los archivos JavaScript se pueden combinar desde el _Administrador_ panel solo cuando se trabaja en [Modo de desarrollador](../systems/developer-tools.md#operation-modes).

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, **[!UICONTROL Advanced]** y elija **[!UICONTROL Developer]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL JavaScript Settings]** sección.

   ![Configuración de JavaScript](./assets/developer-javascript-settings.png){width="600" zoomable="yes"}

   Para obtener descripciones detalladas de estas opciones de configuración, consulte [Configuración de JavaScript](../configuration-reference/advanced/developer.md#javascript-settings) en el _Referencia de configuración_.

1. Establecer **[!UICONTROL Merge JavaScript Files]** hasta `Yes`.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.
