---
title: Clases de impuestos
description: Obtenga información sobre cómo configurar las clases de impuestos que se utilizan para las reglas de impuestos.
exl-id: dd867eba-3f1e-45a8-9332-9e668a2092e1
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# Clases de impuestos

Las clases de impuestos se pueden asignar a clientes, productos y envíos. Commerce analiza el carro de compras de cada cliente y calcula el impuesto apropiado según la clase del cliente, la clase de los productos del carro y la región. La región está determinada por la dirección de envío, la dirección de facturación o el origen de envío del cliente. Se pueden crear nuevas clases de impuestos cuando [regla fiscal](tax-rules.md) está definida.

- **Cliente** — Puede crear tantas clases de impuestos de cliente como necesite y asignarlas a [grupos de clientes](../customers/customer-groups.md). Por ejemplo, en algunas jurisdicciones, las transacciones al por mayor no están gravadas, pero sí las transacciones al por menor. Puede asociar miembros del grupo de clientes mayoristas a la clase de impuestos mayoristas.

- **Product** — Las clases de productos se utilizan en los cálculos para determinar el tipo impositivo correcto que se aplica en el carro de compras. Al crear un producto, se asigna a una clase de impuestos específica. Por ejemplo, los alimentos podrían no estar sujetos a impuestos, o estar sujetos a una tasa diferente.

- **Envío** — Si la tienda cobra un impuesto adicional por el envío, debe designar una clase de impuesto de producto específica para el envío. A continuación, en la configuración, especifíquela como la clase de impuesto que se utiliza para el envío.

## Configurar clases de impuestos

La clase de impuesto utilizada para el envío y las clases de impuesto predeterminadas para [productos y clientes](#add-a-product-tax-class) se establecen en la _[!UICONTROL Sales]_configuración.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Tax]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Tax Classes]** sección.

   ![Configuración - clases de impuestos](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. Elija la clase de impuesto para cada una de las siguientes opciones:

   - **[!UICONTROL Set Tax Class for Shipping]**
   - **[!UICONTROL Tax Class for Gift Options]**
   - **[!UICONTROL Default Tax Class for Product]**
   - **[!UICONTROL Default Tax Class for Customer]**

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Agregar clases de impuestos

Las clases de impuestos para clientes y productos se pueden añadir fácilmente y luego asignar a clientes y productos individuales, y se pueden utilizar en reglas de impuestos.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Haga clic **[!UICONTROL Add New Tax Rule]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Additional Settings]** sección.

   ![Agregar nueva clase de impuestos](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. En _Clase de impuestos del cliente_, haga clic en **[!UICONTROL Add New Tax Class]**.

1. Introduzca el **[!UICONTROL Name]** de la nueva clase de impuestos en el cuadro de texto.

   ![Agregar nueva clase de impuestos](./assets/tax-class-customer-add-new.png){width="600" zoomable="yes"}

1. Para añadir la nueva clase a la lista de clases de impuestos de clientes disponibles, haga clic en la marca de verificación.

   ![Nuevas clases de impuestos](./assets/tax-classes-updated.png){width="600" zoomable="yes"}

## Agregar una clase de impuestos de producto

1. En _Clase de impuestos del producto_, haga clic en **[!UICONTROL Add New Tax Class]**.

1. Introduzca el **[!UICONTROL Name]** de la nueva clase de impuestos en el cuadro de texto.

1. Para agregar la nueva clase a la lista de clases de impuestos de productos disponibles, haga clic en la marca de verificación.

1. Cuando termine, haga clic en **[!UICONTROL Back]** en la barra de botones para volver a la _Reglas Fiscales_ rejilla.

## Destino de impuestos predeterminado

La configuración predeterminada de destino de impuestos determina el país, el estado y el código postal que se usan como base para los cálculos de impuestos.

**_Para configurar el destino de impuestos por defecto para los cálculos:_**

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Tax]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Default Tax Destination Calculation]** sección.

   ![Cálculo de Destino de Impuestos por Defecto](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. Establecer **[!UICONTROL Default Country]** al país en el que se basan los cálculos de impuestos.

1. Establecer **[!UICONTROL Default State]** al estado o provincia que se utiliza como base de los cálculos fiscales.

1. Establecer **[!UICONTROL Default Post Code]** al código postal que se utiliza como base para los cálculos de impuestos locales.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.
