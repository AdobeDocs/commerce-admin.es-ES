---
title: Reglas fiscales
description: Obtenga información sobre cómo definir las reglas fiscales mediante la clase de producto, la clase de cliente y el tipo impositivo.
exl-id: 38d65998-7769-49ce-9814-e65df9d77bba
feature: Taxes, Currency
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# Reglas fiscales

Las reglas fiscales incorporan una combinación de clase de producto, clase de cliente y tipo impositivo. A cada cliente se le asigna una clase de cliente y a cada producto se le asigna una clase de producto. Commerce analiza el carro de compras de cada cliente y calcula el impuesto correspondiente según las clases de cliente y producto y la región. La región se basa en la dirección de envío, la dirección de facturación o el origen de envío del cliente.

>[!NOTE]
>
>Cuando se deben definir numerosos tipos impositivos, se puede simplificar el proceso importándolos.

![Reglas de impuestos](./assets/tax-rules.png){width="600" zoomable="yes"}

## Paso 1: Completar la información de la regla fiscal

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add New Tax Rule]**.

1. En _Información de regla fiscal_, escriba un **[!UICONTROL Name]** para la nueva regla.

   ![Información de regla de impuestos](./assets/tax-rule-information.png){width="600" zoomable="yes"}

1. Elija el(la) **[!UICONTROL Tax Rate]** que se aplica a la regla.

   Para editar un tipo impositivo existente, haga lo siguiente:

   - Pase el ratón sobre la tasa de impuestos y haga clic en el icono _Editar_ ![Icono de lápiz](../assets/icon-edit-pencil.png).

   - Actualice el formulario según sea necesario y haga clic en **[!UICONTROL Save]**.

1. Para introducir tipos impositivos, utilice uno de los métodos siguientes:

### Método 1: Introducir tipos impositivos manualmente

1. Haga clic en **[!UICONTROL Add New Tax Rate]**.

1. Complete el formulario según sea necesario (consulte [Zonas fiscales y tasas](tax-zones-rates.md)).

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

   ![Nueva tasa de impuestos](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

### Método 2: Importar tipos impositivos

1. Desplácese hacia abajo hasta la sección situada en la parte inferior de la página.

1. Para importar tipos impositivos, haga lo siguiente:

   - Haga clic en **[!UICONTROL Choose File]** y vaya al archivo CSV con las tasas de impuestos que se van a importar.

   - Haga clic en **[!UICONTROL Import Tax Rates]**.

1. Para exportar tasas de impuestos, haga clic en **[!UICONTROL Export Tax Rates]** (consulte [Importar/Exportar tasas de impuestos](../systems/data-transfer-tax-rates.md)).

![Tasas de impuestos de importación/exportación](./assets/tax-rule-new-import-export.png){width="600" zoomable="yes"}

## Paso 2: Completar la configuración adicional

1. Para abrir la sección, haga clic en **[!UICONTROL Additional Settings]**.

   ![Configuración adicional para la regla de impuestos](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. Elija el(la) **[!UICONTROL Customer Tax Class]** al que se aplica la regla.

   - Para editar una clase de impuestos de cliente, haga clic en el icono _Editar_ ![Icono de lápiz](../assets/icon-edit-pencil.png), actualice el formulario según sea necesario y haga clic en **[!UICONTROL Save]**.

   - Para crear una clase de impuestos, haga clic en **[!UICONTROL Add New Tax Class]**, complete el formulario según sea necesario y haga clic en **[!UICONTROL Save]**.

1. Elija el(la) **[!UICONTROL Product Tax Class]** al que se aplica la regla.

   - Para editar una clase de impuestos de productos, haga clic en el icono _Editar_ ![Icono de lápiz](../assets/icon-edit-pencil.png), actualice el formulario según sea necesario y haga clic en **[!UICONTROL Save]**.

   - Para crear una clase de impuestos, haga clic en **[!UICONTROL Add New Tax Class]**, complete el formulario según sea necesario y haga clic en **[!UICONTROL Save]**.

1. Cuando se aplique más de un impuesto, escriba un número para indicar la prioridad de este impuesto para **[!UICONTROL Priority]**.

   Si se aplican dos reglas fiscales con la misma prioridad, se añaden los impuestos. Si se aplican dos impuestos con diferentes configuraciones de prioridad, los impuestos se componen.

1. Si desea que los impuestos se basen en el subtotal del pedido, active la casilla de verificación **[!UICONTROL Calculate off Subtotal Only]**.

1. Para **[!UICONTROL Sort Order]**, escriba un número para indicar el orden de esta regla fiscal cuando se enumera con otros.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Rule]**.

## Demostración de reglas fiscales y de divisa

Obtenga información acerca de la administración de reglas monetarias y fiscales con este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/343657/?quality=12&learn=on)
