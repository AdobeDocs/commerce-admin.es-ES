---
title: Recursos del tema
description: Obtenga información sobre cómo administrar los recursos de temáticas, como CSS, fuentes, imágenes y archivos JavaScript.
exl-id: 326c648e-eace-45a0-b53d-bbc8702fee05
feature: Page Content, Themes
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: e50b85311f4512fb54c7cb29faf6136eaf07eae6
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# Recursos del tema

Los _archivos estáticos_ son la colección de recursos como CSS, fuentes, imágenes y JavaScript que usa un tema. La ubicación de los archivos estáticos se especifica en la configuración de [URL base](../stores-purchase/store-urls.md). Puede agregar una firma digital a la dirección URL de cada archivo estático para que los exploradores puedan detectar cuándo está disponible una versión más reciente. Se utiliza la versión más reciente del archivo si la firma difiere de lo que se almacena en la caché del explorador.

Para una instalación estándar, los recursos asociados con un tema están organizados en la carpeta `web` en la siguiente ubicación debajo de la raíz [!DNL Commerce].

`[commerce_root]/app/design/frontend/Magento/[theme_name]/web`

## Agregar una firma digital a las direcciones URL de los archivos estáticos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL Developer]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Static Files Settings]**.

   ![Configuración de archivos estáticos](./assets/developer-static-files-settings.png){width="500" zoomable="yes"}

1. Establezca **[!UICONTROL Sign Static Files]** en `Yes`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

| Tipo de archivo | Descripción |
|--- |--- |
| CSS | Controlar el estilo visual asociado a la piel. Ubicación de ejemplo en el servidor: `[commerce]/app/design/frontend/Magento/[theme]/web/css` |
| Fuentes | Proporcione las fuentes disponibles para usar en la temática. Ubicación en el servidor: `[commerce]/app/design/frontend/Magento/[theme]/web/fonts` |
| Imágenes | Proporcione los recursos gráficos utilizados por la temática, incluidos botones, texturas de fondo, etc. Ubicación de ejemplo en el servidor: `[commerce]/app/design/frontend/Magento/[theme]/web/images` |
| JS | Rutinas JavaScript específicas del tema y funciones a las que se puede llamar. Ubicación de ejemplo en el servidor: `[commerce]/app/design/frontend/Magento/[theme]/web/js` |

{style="table-layout:auto"}

## Combinar archivos CSS

Como parte del esfuerzo por optimizar el sitio y reducir el tiempo de carga de la página, puede reducir el número de archivos CSS independientes combinándolos en un único archivo condensado. Si abre un archivo CSS combinado, verá un flujo continuo de texto, con los saltos de línea eliminados. No puede editar el archivo combinado, por lo que es mejor esperar hasta que esté fuera del modo de desarrollo y ya no realice cambios frecuentes en CSS.

>[!NOTE]
>
>Los archivos CSS se pueden combinar desde el panel _Admin_ solo cuando se trabaja en [modo de desarrollador](../systems/developer-tools.md#operation-modes).

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, **[!UICONTROL Advanced]** y elija **[!UICONTROL Developer]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL CSS Settings]**.

   ![Configuración de CSS](./assets/developer-css-settings.png){width="500" zoomable="yes"}

   Para obtener descripciones detalladas de estas opciones de configuración, consulte [Configuración de CSS](../configuration-reference/advanced/developer.md#css-settings) en la _Referencia de configuración_.

1. Establezca **[!UICONTROL Merge CSS Files]** en `Yes`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Combinar archivos de JavaScript

Se pueden combinar varios archivos JavaScript en uno solo y condensado para reducir el tiempo de carga de la página. Si abre un archivo JavaScript combinado, verá un flujo continuo de texto, con los saltos de línea eliminados. Si ha finalizado el proceso de desarrollo y el código no contiene errores, considere la posibilidad de combinar los archivos.

>[!NOTE]
>
>Los archivos de JavaScript se pueden combinar desde el panel _Admin_ solo cuando se trabaja en [Modo de desarrollador](../systems/developer-tools.md#operation-modes).

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, **[!UICONTROL Advanced]** y elija **[!UICONTROL Developer]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL JavaScript Settings]**.

   ![Configuración de JavaScript](./assets/developer-javascript-settings.png){width="600" zoomable="yes"}

   Para obtener descripciones detalladas de estas opciones de configuración, consulte [Configuración de JavaScript](../configuration-reference/advanced/developer.md#javascript-settings) en la _Referencia de configuración_.

1. Establezca **[!UICONTROL Merge JavaScript Files]** en `Yes`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
