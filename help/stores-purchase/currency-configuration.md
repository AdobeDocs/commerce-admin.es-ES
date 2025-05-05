---
title: Configuración de moneda
description: Obtenga información sobre cómo establecer el ámbito de la moneda base y cómo especificar las monedas que acepta y la moneda que desea utilizar para la visualización de precios.
exl-id: ba78095f-36eb-4e38-a6e8-72d85e0cf980
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---

# Configuración de moneda

Antes de configurar las tarifas de moneda individuales, primero debe establecer el ámbito de la [moneda base](../configuration-reference/general/currency-setup.md). Se establece como global de forma predeterminada, lo que aplica la configuración de moneda base a toda la [jerarquía de tiendas](../getting-started/websites-stores-views.md). Si tiene una instalación de Adobe Commerce o Magento Open Source multisitio, puede administrar varias divisas base estableciendo el ámbito en el nivel de sitio web.

También puede especificar las monedas que acepta y la moneda que desea utilizar para mostrar [precios](../catalog/catalog-price-scope.md) en su tienda. En el diagrama siguiente, el ámbito de la moneda base se establece en el nivel del sitio web, de modo que cada sitio web puede tener una moneda base diferente.

![Diagrama del ámbito de la moneda](./assets/scope-currency-config.svg){width="600" zoomable="yes"}

## Paso 1: Selección de las divisas aceptadas

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En la esquina superior izquierda, establezca **[!UICONTROL Scope]** en la vista de la tienda donde se aplica la configuración.

1. En el panel izquierdo bajo _General_, elija **[!UICONTROL Currency Setup]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Currency Options]** y establezca las siguientes opciones:

   - **[!UICONTROL Base Currency]** — Se establece en la moneda principal que usa para las transacciones en línea.

   - **[!UICONTROL Default Display Currency]** — Se establece en la moneda que se usa para mostrar los precios en la vista de tienda.

   - **[!UICONTROL Allowed Currencies]**: seleccione todas las divisas que acepta como pago en la vista de tienda. Asegúrese de seleccionar también la moneda principal.

     Para varias divisas, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción.

   ![Configuración general - opciones de moneda](../configuration-reference/general/assets/currency-setup-currency-options.png){width="600" zoomable="yes"}

   Para obtener una descripción detallada de cada una de estas opciones de configuración, consulte [Opciones de moneda](../configuration-reference/general/currency-setup.md) en la _Guía de referencia de configuración_.

1. Cuando se le pida que actualice la caché, haga clic en _Cerrar_ ( ![Cerrar cuadro](../assets/icon-close-x.png) ) en la esquina superior derecha del mensaje del sistema.

   Puede [actualizar la caché](../systems/cache-management.md) más adelante.

1. Defina el ámbito de la moneda base:

   - En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

   - Desplácese hacia abajo y expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Price]**. (Esta sección solo aparece si el ámbito está establecido como **[!UICONTROL Store View:]** _Configuración predeterminada_.)

   - Establezca **[!UICONTROL Catalog Price Scope]** en `Global` o `Website`.

   ![Configuración del catálogo - opciones de precio](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

## Paso 2: Configuración de la conexión de importación

1. Desplácese al principio de la página.

1. En el panel izquierdo, expanda **[!UICONTROL General]** y elija **[!UICONTROL Currency Setup]**.

1. Configure la conexión del servicio de divisas:

   Hay tres opciones de servicio: _[!UICONTROL Fixer.io (legacy)]_,_[!UICONTROL Fixer Api (APILayer)]_ y _[!UICONTROL Currency Converter API]_

   >[!IMPORTANT]
   >
   >A partir de la versión 2.4.6, el servicio [[!DNL Fixer.io]](https://fixer.io/) queda obsoleto y se ha sustituido por el servicio [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api). Se recomienda encarecidamente que utilice una cuenta APILayer en lugar de una cuenta [!DNL Fixer.io] obsoleta.

   - _Para conectarse al servicio [fixer.io](https://fixer.io/):_

      - Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Fixer.io]**.

      - Escriba su fixer.io **[!UICONTROL API key]**.

      - Para **[!UICONTROL Connection Timeout in Seconds]**, ingrese el número de segundos de inactividad que se permitirán antes de que se agote el tiempo de espera de la conexión.

     ![Configuración general - configuración de moneda - Opciones de Fixer.io](../configuration-reference/general/assets/currency-setup-fixer.png){width="600" zoomable="yes"}

   - _Para conectarse al [[!DNL Fixer Api (APILayer)] servicio](https://apilayer.com/):_

      - Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Fixer Api (APILayer)]**.

      - Escriba su [!DNL APILayer] **[!UICONTROL API key]**.

      - Para **[!UICONTROL Connection Timeout in Seconds]**, ingrese el número de segundos de inactividad que se permitirán antes de que se agote el tiempo de espera de la conexión.

     ![Configuración general - configuración de moneda - Opciones de API de fijador (APILayer)](../configuration-reference/general/assets/currency-setup-fixer-api.png){width="600" zoomable="yes"}

   - _Para conectarse al [[!DNL Currency Convertor API] servicio](https://free.currencyconverterapi.com/):_

      - Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Currency Convertor API]**.

      - Introduzca su conversor de moneda **[!UICONTROL API key]**.

      - Para **[!UICONTROL Connection Timeout in Seconds]**, ingrese el número de segundos de inactividad que se permitirán antes de que se agote el tiempo de espera de la conexión.

     ![Configuración general - configuración de moneda - Opciones de API del convertidor de moneda](../configuration-reference/general/assets/currency-setup-converter.png){width="600" zoomable="yes"}

## Paso 3: Configurar las opciones de importación programadas

1. Continuando con la configuración de moneda, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Scheduled Import Settings]**.

   ![Configuración general - configuración de importación programada de moneda](../configuration-reference/general/assets/currency-setup-scheduled-import-settings.png){width="600" zoomable="yes"}

1. Para actualizar automáticamente las tasas de cambio, establezca **[!UICONTROL Enabled]** en `Yes`.

1. Defina las opciones de actualización:

   - **[!UICONTROL Service]** — Se establece en el proveedor de tarifa. El valor predeterminado es `Fixer.io (legacy)`.

   - **[!UICONTROL Start Time]** — Se establece en la hora, el minuto y el segundo en que las tarifas se actualizan de acuerdo con la programación.

   - **[!UICONTROL Frequency]**: para determinar la frecuencia con la que se actualizan las tarifas, establezca una de las siguientes opciones:

      - `Daily`
      - `Weekly`
      - `Monthly`

   - **[!UICONTROL Error Email Recipient]**: escriba la dirección de correo electrónico de la persona que va a recibir la notificación por correo electrónico si se produce un error durante el proceso de importación.

     Para introducir varias direcciones de correo electrónico, sepárelas con una coma.

   - **[!UICONTROL Error Email Sender]** — Se establece en [contacto de tienda](../getting-started/store-details.md#store-email-addresses) que aparece como remitente de la notificación de error.

   - **[!UICONTROL Error Email Template]** — Se establece en la plantilla de correo electrónico utilizada para la notificación de error.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

1. Cuando se le pida que actualice la caché, haga clic en el vínculo **[!UICONTROL Cache Management]** y actualice la caché no válida.

   ![Mensaje del sistema: actualice la caché no válida](./assets/msg-cache-management.png){width="600" zoomable="yes"}

## Paso 4: Actualizar las tasas de cambio

Los tipos de cambio deben actualizarse con los valores actuales antes de que entren en vigor. [Actualice las tarifas](currency-update.md) manualmente o para importar las tarifas automáticamente.

## Paso 5: Personalizar los símbolos de moneda (opcional)

La gestión de símbolos de moneda le permite personalizar el símbolo asociado a cada moneda que se acepta como pago en su tienda.

![Símbolos de moneda](./assets/stores-currency-symbols.png){width="600" zoomable="yes"}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Symbols]**.

   Cada moneda habilitada para su tienda aparece en la lista _[!UICONTROL Currency]_.

1. Cambie la configuración de la lista según sea necesario:

   - Escriba un símbolo personalizado para cada moneda que desee usar o active la casilla de verificación **[!UICONTROL Use Standard]** para cada moneda.

   - Para anular el símbolo predeterminado, desactive la casilla de verificación _[!UICONTROL Use Standard]_&#x200B;e introduzca el símbolo que desee utilizar.

   >[!NOTE]
   >
   >No es posible cambiar la alineación del símbolo de moneda de izquierda a derecha.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Currency Symbols]**.

1. Cuando se le pida que actualice la caché, haga clic en el vínculo **[!UICONTROL Cache Management]** y actualice cualquier caché no válida.
