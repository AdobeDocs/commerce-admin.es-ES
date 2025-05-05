---
title: '[!DNL New Relic] informe'
description: Obtenga información acerca de los informes  [!DNL New Relic] disponibles para cuentas de Adobe Commerce en la infraestructura en la nube, que incluye el software para el servicio APM de New Relic.
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
source-git-commit: 0651a2489a396ab142b60a8678d6c7590fd5f9ee
workflow-type: tm+mt
source-wordcount: '1382'
ht-degree: 0%

---

# Informes de [!DNL New Relic]

[New Relic][1] es un servicio de análisis de software que te ayuda a analizar y mejorar las interacciones entre aplicaciones. Las cuentas de Adobe Commerce en la infraestructura en la nube incluyen el software para el servicio [!DNL New Relic APM]. Para obtener más información, consulte [Servicios de New Relic][4] en la _Guía de infraestructura de Commerce en la nube_.

## Paso 1: Registrarse para obtener una cuenta de [!DNL New Relic]

1. Vaya al sitio web de [[!DNL New Relic]][1] y regístrese para obtener una cuenta.

   También puede registrarse para obtener una cuenta de prueba gratuita.

1. Siga las instrucciones del sitio. Cuando se le solicite, elija primero el producto que desea instalar.

1. Mientras esté en su cuenta, busque las siguientes credenciales necesarias para completar la configuración de comercio:

   | Opción | Descripción |
   | ------ | ----------- |
   | ID de cuenta | Desde el panel de cuentas de [!DNL New Relic], el identificador de cuenta es el número de la dirección URL después de `/accounts` |
   | ID de aplicación | En el panel de su cuenta de [!DNL New Relic], haga clic en **[!UICONTROL New Relic APM]**. En el menú, elija **[!UICONTROL Applications]**. A continuación, elija la aplicación. El ID de aplicación es el número que aparece en el URL posterior: `/applications/` |
   | Clave de API de Nuevo Relic | En el panel de su cuenta de [!DNL New Relic], haga clic en **[!UICONTROL Account Settings]**. En el menú de la izquierda, debajo de Integraciones, elija **[!UICONTROL Data Sharing]**. Puede crear, regenerar o eliminar la clave de API desde esta página. |
   | Clave API de Insights | En el panel de su cuenta de [!DNL New Relic], haga clic en **[!UICONTROL Insights]**. En el menú de la izquierda debajo de Administración, elija **[!UICONTROL API Keys]**. Las claves de API de Insights aparecen en esta página. Si es necesario, haga clic en el signo más (**+**) situado junto a Insertar claves para generar una clave. |

   {style="table-layout:auto"}

## Paso 2: Instalar el agente [!DNL New Relic] en el servidor

Para usar [!DNL New Relic APM Pro] para recopilar y transmitir datos, el agente PHP debe estar instalado en el servidor.

1. Cuando se le pida que elija un agente web, haga clic en **PHP**.

1. Para configurar el agente PHP en su servidor, siga las instrucciones.

   Si necesita ayuda, consulte [New Relic para PHP][3].

1. Asegúrese de que cron se esté ejecutando en el servidor.

   Para obtener más información, consulta [Configurar y ejecutar cron][5] en la documentación para desarrolladores.

## Paso 3: Configuración de la tienda

>[!NOTE]
>Estas opciones de configuración no se aplican a Adobe Commerce en la infraestructura de la nube.
>
>Si está en el plan Pro, New Relic ya está [preconfigurado y habilitado de manera predeterminada](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). Si se encuentra en el plan inicial, debe completar los [pasos de configuración de New Relic](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) que forman parte del proceso de instalación.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel de navegación izquierdo donde **[!UICONTROL General]** está expandido, elija **[!UICONTROL New Relic Reporting]** y haga lo siguiente:

   ![Configuración de informes de New Relic](./assets/new-relic-reporting-general.png){width="600"}

   * Establezca **[!UICONTROL Enable New Relic Integration]** en `Yes`.

   * En **[!UICONTROL Insights API URL]**, reemplace el símbolo de porcentaje (`%`) por su ID de cuenta de New Relic.

   * Escriba su **[!UICONTROL New Relic Account ID]**.

   * Escriba su **[!UICONTROL New Relic Application ID]**.

   * Escriba su **[!UICONTROL New Relic API Key]**.

   * Escriba usted **[!UICONTROL Insights API Key]**.

1. Para **[!UICONTROL New Relic Application Name]**, escriba un nombre para identificar la configuración de referencia interna.

1. (Opcional) Para **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]**, seleccione `Yes` para enviar los datos recopilados de la tienda y el administrador como aplicaciones independientes a New Relic.

   Esta opción requiere un nombre escrito para **[!UICONTROL New Relic Application Name]**.

   >[!NOTE]
   >
   >Al habilitar esta característica, se reduce el número de alertas de [!DNL New Relic] falsos positivos y se permite la supervisión y las alertas configuradas estrictamente para el rendimiento de front-end. New Relic recibe archivos de datos de aplicaciones independientes con nombres de Nombre de aplicación anexados a `Adminhtml` y front-end. Por ejemplo: `MyStore_Adminhtml`

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Paso 4: Habilitar Cron para la creación de informes de [!DNL New Relic]

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Cron]**.

   ![Configuración de New Relic Cron](./assets/new-relic-reporting-cron.png){width="600"}

1. Establezca **[!UICONTROL Enable Cron]** en `Yes`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## [!DNL New Relic] consultas

Los datos de [!DNL New Relic Insights] se basan en instrucciones escritas en [!DNL New Relic Query Language] (NRQL) y en cualquier parámetro personalizado que pueda incluir. Los datos se pueden devolver desde consultas ad hoc o mediante consultas guardadas en el panel. Para obtener más información, consulte la [Referencia de NRQL][6] en la documentación de [!DNL New Relic].

### Eventos de administración

#### Usuarios administradores activos

Devuelve el número de usuarios administradores activos.

    SELECT uniqueCount(AdminId)
    FROM Transacción
    WHERE appName=&#39;&lt;your_app_name>&#39; DESDE hace 15 minutos

#### Usuarios administradores activos actualmente

Devuelve los nombres de los usuarios administradores activos.

    SELECCIONAR valores exclusivos(AdminName)
    DE la transacción
    WHERE appName=&#39;&lt;your_app_name>&#39; DESDE hace 15 minutos

#### Actividad reciente del administrador

Devuelve el número de acciones de administración recientes.

    SELECT count(AdminId)
    FROM Transacción
    WHERE appName =&#39;&lt;your_app_name>&#39; FACET AdminName DESDE hace 1 día

#### Última actividad de administración

Devuelve información detallada sobre las acciones recientes de la administración, incluido el nombre de usuario, la duración y el nombre aplicación del administrador.

    SELECT AdminName, duration, name
    FROM Transacción
    DONDE appName=&#39;&lt;your_app_name>&#39; Y AdminName NO ES NULO
    y AdminName !&lt;/your_app_name>= &#39;N/A&#39; LÍMITE 50

### Eventos Cron

#### Recuento Categoría

Devuelve el número de sucesos de aplicación por categoría durante el período de tiempo especificado.

    SELECT average(CatalogCategoryCount)
    FROM Cron
    WHERE CatalogCategoryCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minutes

#### Recuento del catálogo actual

Devuelve el número promedio de eventos de aplicación en el catálogo por categoría durante el período de tiempo especificado.

    SELECT average(CatalogCategoryCount)
    FROM cron
    WHERE CatalogCategoryCount NO ES NULO
    y CatalogCategoryCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SINCE 2 minutes ago LIMIT 1
&lt;/your_app_name>

#### Productos activos

Devuelve el número de eventos de aplicación por producto durante el período de tiempo especificado.

    SELECT average(CatalogProductActiveCount)
    FROM Cron
    WHERE CatalogProductActiveCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minutes

#### Recuento de productos activos

Devuelve el promedio de eventos de aplicación activos por producto durante el período de tiempo especificado.

    SELECT average(CatalogProductActiveCount)
    FROM Cron
    WHERE CatalogProductActiveCount IS NOT NULL
    AND CatalogProductActiveCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SINCE 2 minutes ago LIMIT 1

#### Productos configurables

Devuelve el número promedio de eventos de aplicación para productos configurables durante el período de tiempo especificado.

    SELECCIONE average(CatalogProductConfigurableCount)
    FROM Cron
    WHERE CatalogProductConfigurableCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minutes

#### Recuento de productos configurables

Devuelve el número promedio de eventos de aplicación por producto configurable durante el período de tiempo especificado.

    SELECT average(CatalogProductConfigurableCount)
    FROM Cron
    WHERE CatalogProductConfigurableCount IS NOT NULL
    AND CatalogProductConfigurableCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; FROM 2 minutes ago LIMIT 1

#### Recuento de productos (todos)

Devuelve el número total de eventos de aplicación para todos los productos.

    SELECCIONAR average(CatalogProductCount)
    FROM Cron
    WHERE CatalogProductCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minutes

#### Recuento actual de productos (todos)

Devuelve el número promedio de eventos de aplicación para todos los productos durante el período de tiempo especificado.

    SELECCIONAR average(CatalogProductCount)
    FROM Cron
    WHERE CatalogProductCount IS NOT NULL
    AND CatalogProductCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SINCE 2 minutes ago LIMIT 1

#### Recuento de clientes

Devuelve el número promedio de eventos de aplicación por cliente.

    SELECT average(CustomerCount)
    FROM Cron
    WHERE CustomerCount IS NOT NULL
    AND CustomerCount > 0&lt;
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minutes

#### Recuento de clientes actuales

Devuelve el número promedio de clientes durante el período de tiempo especificado.

    SELECT average(CustomerCount)
    FROM Cron
    WHERE CustomerCount IS NOT NULL
    AND CustomerCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SINCE 2 minutes ago LIMIT 1

#### Estado del módulo

Devuelve el número promedio de veces que los módulos de aplicación están habilitados, deshabilitados o instalados durante el período de tiempo especificado.

    SELECT average(ModulesDisabled), average(ModulesEnabled), average
    (ModulesInstalled)
    FROM Cron&lt;
    WHERE appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minutes

#### Estado actual del módulo

Devuelve el número promedio de veces que los módulos se habilitaron, deshabilitaron o instalaron durante el período de tiempo especificado.

    SELECT average(ModulesDisabled), average(ModulesEnabled), average
    (ModulesInstalled)
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name>&#39; SINCE 2 minutes ago LIMIT 1

#### Recuentos de sitios web y tiendas

Devuelve el número promedio de eventos de aplicación por sitio web y almacén durante el período de tiempo especificado.

    SELECT average(StoreViewCount), average(WebsiteCount)
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name&gt;&#39; TIMESERIES 2 minutos

#### Recuentos actuales de sitios web y tiendas

Devuelve el número promedio de eventos de la aplicación actual durante el período de tiempo especificado.

    SELECCIONAR promedio(StoreViewCount), promedio(WebsiteCount)
    DE Cron
    DONDE appName = &#39;&lt;your_app_name>&#39; DESDE HACE 2 minutos LÍMITE 1

#### Cron: todos los datos del evento

Devuelve todos los datos de evento de la aplicación.

    SELECCIONAR *
    DE Cron
    DONDE appName = &#39;&lt;your_app_name>&#39;

### Clientes

#### Recuento de clientes activos

Devuelve el número de clientes activos durante el período de tiempo especificado.

    SELECT uniqueCount(CustomerId)
    FROM Transacción
    WHERE appName = &#39;&lt;your_app_name>&#39; DESDE hace 15 minutos

#### Clientes activos

Devuelve los nombres de los clientes activos durante el período de tiempo especificado.

    SELECT uniques(CustomerName)
    FROM Transacción
    WHERE appName=&#39;&lt;your_app_name>&#39; DESDE hace 15 minutos

#### Clientes principales

Devuelve los clientes principales durante el período de tiempo especificado.

    SELECT count(CustomerId)
    FROM Transaction
    WHERE appName = &#39;&lt;your_app_name>&#39; FACET CustomerName DESDE hace 1 día

#### Actividad reciente del administrador

Devuelve un número definido de registros de actividad reciente, que incluyen el nombre del cliente y la duración de la visita.

    SELECT CustomerName, duration, name
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39;
    And CustomerName IS NOT NULL
    AND CustomerName !&lt;/your_app_name>= &#39;N/A&#39; LÍMITE 50

### Órdenes

#### Número de pedidos asentados

Devuelve el número de pedidos realizados durante el período de tiempo especificado.

    SELECT count(Order)
    FROM Transacción DESDE hace 1 día

#### Valor de pedido total

Devuelve el número total de elementos de línea pedidos durante el período de tiempo especificado.

    SELECT sum(orderValue)
    FROM Transacción DESDE hace 1 día

#### Total de elementos de línea pedidos

Devuelve el número total de elementos de línea pedidos durante el período de tiempo especificado.

    SELECT sum(lineItemCount)
    FROM Transacción DESDE hace 1 día


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
