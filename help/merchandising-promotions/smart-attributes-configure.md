---
title: Configurar atributos inteligentes para Visual Merchandiser
description: Obtenga información sobre cómo configurar los atributos inteligentes utilizados por Visual Merchandiser.
exl-id: 7bbbca40-d991-4393-b99c-5bef2e711071
feature: Merchandising, Products, Configuration, Attributes
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
TQID: 'https://experienceleague.adobe.com/-6tbdpZ7L6nS1sIOXdk5Faxpkkt9qzqWhIjqp9MwgiM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: 76cfaac4-e563-56dd-8938-708bf8b84956
    internal-label: Attributes
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '196'
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
