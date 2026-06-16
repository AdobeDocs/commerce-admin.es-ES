---
title: Actualizar tasas de cambio
description: Aprenda a configurar las tasas de cambio manualmente o importarlas a su tienda.
exl-id: 316a7bc8-1118-46e7-82ff-891ada04cd13
feature: Currency, Configuration, Data Import/Export
TQID: https://experienceleague.adobe.com/tEt15Mzt7MeDtf6MZfu9n6EsvJKUCNBdGhUo0-RK3zk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# Actualizar tasas de cambio

Las tasas de cambio se pueden configurar manualmente o importar en la tienda. Para asegurarse de que tu tienda tiene las tarifas más actuales, puedes configurar las tarifas de moneda para que se actualicen automáticamente según lo programado.

Antes de importar las tasas de cambio, complete la [configuración de la tasa de cambio](currency-configuration.md) para especificar las monedas que acepta y para establecer la conexión y la programación de la importación.

![Tipos de cambio](./assets/stores-currency-rate-update.png){width="600" zoomable="yes"}

## Actualizar una tasa de cambio manualmente

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. Haga clic en la tasa que desee cambiar e introduzca el nuevo valor para cada moneda admitida.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Currency Rates]**.

## Importar tipos de cambio

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. Establezca **[!UICONTROL Import Service]** en el proveedor de tarifa de moneda.

   El proveedor predeterminado es `fixer.io (legacy)`.

   >[!IMPORTANT]
   >
   >A partir de la versión 2.4.6, el servicio [[!DNL Fixer.io]](https://fixer.io/) queda obsoleto y se ha sustituido por el servicio [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api). Se recomienda encarecidamente que utilice una cuenta APILayer en lugar de una cuenta [!DNL Fixer.io] obsoleta.

1. Haga clic en **[!UICONTROL Import]**.

   Las tarifas actualizadas aparecen en la lista _[!UICONTROL Currency Rates]_. Si las tasas han cambiado desde la última actualización, la tasa antigua aparece a continuación como referencia.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Currency Rates]**.

1. Cuando se le pida que actualice la caché, haga clic en el vínculo **[!UICONTROL Cache Management]** y actualice la caché no válida.

   ![Mensaje del sistema: actualice la caché no válida](./assets/currency-cache-update.png){width="600" zoomable="yes"}

## Importar tipos de cambio según lo programado

1. Asegúrese de que [Cron](../systems/cron.md) esté habilitado para su tienda.

1. Para especificar las divisas que acepta y establecer la conexión y programación de importación, complete la [Configuración de tarifa de divisa](currency-configuration.md).

1. Para comprobar que las tarifas se importan según lo programado, consulte la lista _[!UICONTROL Currency Rates]_.

1. Espere el período de tiempo de la configuración de frecuencia establecida para la programación y compruebe las tarifas de nuevo.
