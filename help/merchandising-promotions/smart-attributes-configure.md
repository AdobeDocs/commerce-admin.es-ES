---
title: Configurar atributos inteligentes para Visual Merchandiser
description: Obtenga información sobre cómo configurar los atributos inteligentes utilizados por Visual Merchandiser.
exl-id: 7bbbca40-d991-4393-b99c-5bef2e711071
feature: Merchandising, Products, Configuration, Attributes
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---

# Configurar atributos inteligentes para Visual Merchandiser

{{ee-feature}}

La configuración de Visual Merchandiser determina los atributos que se pueden utilizar en la ventana de comercialización y el umbral de existencias mínimo. La configuración también identifica el atributo utilizado para el color y el orden de los valores de color.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Visual Merchandiser]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL General Options]**.

   ![Configuración del catálogo - comerciante visual](../configuration-reference/catalog/assets/catalog-visual-merchandiser-general-options.png){width="600" zoomable="yes"}

1. En la lista **[!UICONTROL Attributes for Category Rules]**, seleccione cada atributo que desee que esté disponible para la comercialización visual.

   Para seleccionar varios atributos, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada elemento.

1. Escriba **[!UICONTROL Minimum Stock Threshold]** para que un producto aparezca en la ventana de Visual Merchandiser.

1. Escriba **[!UICONTROL Color Attribute Code]**.

   El valor predeterminado es `color`. Si el catálogo utiliza un atributo diferente, introduzca el nombre del atributo en minúsculas.

1. Para **[!UICONTROL Color Order]**, introduzca cada valor de color en una línea independiente y en secuencia para determinar la prioridad de cada color.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
