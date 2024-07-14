---
title: Actualizar tasas de cambio
description: Aprenda a configurar las tasas de cambio manualmente o importarlas a su tienda.
exl-id: 316a7bc8-1118-46e7-82ff-891ada04cd13
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '271'
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
