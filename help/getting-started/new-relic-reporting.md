---
title: 'sistema de informes[!DNL New Relic] '
description: Obtenga información sobre los sistema de informes disponibles para las [!DNL New Relic] cuentas de Adobe Systems Commerce on infraestructura en la nube, que incluye el software para el servicio APM de Nuevo Relic.
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
source-git-commit: e9a7645aed0e3b48bf565b04cdb6a31ce5d39ca0
workflow-type: tm+mt
source-wordcount: '1361'
ht-degree: 0%

---

# [!DNL New Relic] informe

[New Relic][1] es un servicio de análisis de software que le ayuda a analizar y mejorar las interacciones entre aplicaciones. Las cuentas de Adobe Commerce en la infraestructura en la nube incluyen el software para [!DNL New Relic APM] servicio. Para obtener más información, consulte [Servicios de New Relic][4] en el _Guía de Commerce en la infraestructura de Cloud_.

## Paso 1: Regístrese para obtener una [!DNL New Relic] account

1. Vaya al [[!DNL New Relic]][1] sitio web y regístrese para obtener un cuenta.

   También puede inscribirse para una cuenta de prueba gratuito.

1. Siga las instrucciones del sitio. Cuando se le solicite, elija primero el producto que desea instalar.

1. Mientras esté en su cuenta, busque las siguientes credenciales necesarias para completar la configuración de comercio:

   | Opción | Descripción |
   | ------ | ----------- |
   | ID de cuenta | De su [!DNL New Relic] en el tablero de cuentas, el ID de cuenta es el número de la URL después de: `/accounts` |
   | ID de aplicación | De su [!DNL New Relic] panel de cuentas, haga clic en **[!UICONTROL New Relic APM]**. En el menú, elija **[!UICONTROL Applications]**. A continuación, elija la aplicación. El ID de aplicación es el número de la dirección URL después de: `/applications/` |
   | Clave de API de New Relic | De su [!DNL New Relic] panel de cuentas, haga clic en **[!UICONTROL Account Settings]**. En el menú de la izquierda, debajo de Integraciones, elija **[!UICONTROL Data Sharing]**. Puede crear, regenerar o eliminar la clave de API desde esta página. |
   | Clave API de Insights | De su [!DNL New Relic] panel de cuentas, haga clic en **[!UICONTROL Insights]**. En el menú de la izquierda, debajo de Administración, elija **[!UICONTROL API Keys]**. Las claves de API de Insights aparecen en esta página. Si es necesario, haga clic en el signo más (**+**) junto a Insertar claves para generar una clave. |

   {style="table-layout:auto"}

## Paso 2: Instalar el [!DNL New Relic] agente en su servidor

Para usar [!DNL New Relic APM Pro] para recopilar y transmitir datos, el agente PHP debe estar instalado en su servidor.

1. Cuando se le pida que elija un agente web, haga clic en **PHP**.

1. Para configurar el agente PHP en su servidor, siga las instrucciones.

   Si necesita ayuda, consulte [New Relic para PHP][3].

1. Asegúrese de que cron se esté ejecutando en el servidor.

   Para obtener más información, consulte [Configurar y ejecutar cron][5] en la documentación para desarrolladores.

## Paso 3: Configuración de la tienda

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel de navegación izquierdo donde **[!UICONTROL General]** está expandido, elija **[!UICONTROL New Relic Reporting]** y haga lo siguiente:

   ![Configuración de informes de New Relic](./assets/new-relic-reporting-general.png){width="600"}

   * Establecer **[!UICONTROL Enable New Relic Integration]** hasta `Yes`.

   * En el **[!UICONTROL Insights API URL]**, reemplace el porcentaje (`%`) con su ID de cuenta de New Relic.

   * Introduzca su **[!UICONTROL New Relic Account ID]**.

   * Introduzca su **[!UICONTROL New Relic Application ID]**.

   * Introduzca su **[!UICONTROL New Relic API Key]**.

   * Ingrese usted **[!UICONTROL Insights API Key]**.

1. Para **[!UICONTROL New Relic Application Name]**, introduzca un nombre para identificar la configuración de para referencia interna.

1. (Opcional) Para **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]**, seleccione `Yes` para enviar los datos recopilados para la tienda y el administrador como aplicaciones independientes a New Relic.

   Esta opción requiere que se escriba un nombre para el **[!UICONTROL New Relic Application Name]** archivo .

   >[!NOTE]
   >
   >Al habilitar esta función, se reduce el número de falsos positivos [!DNL New Relic] alertas y permite la monitorización configurada y las alertas estrictamente para el rendimiento de front-end. New Relic recibe archivos de datos de aplicación independientes con nombres de Nombre de aplicación anexados a `Adminhtml` y front-end. Por ejemplo: `MyStore_Adminhtml`

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Paso 4: Habilitar Cron para [!DNL New Relic] informe

1. Expanda ![Expansión selector](../assets/icon-display-expand.png) la **[!UICONTROL Cron]** sección.

   ![Configuración de New Relic Cron](./assets/new-relic-reporting-cron.png){width="600"}

1. Establecer **[!UICONTROL Enable Cron]** hasta `Yes`.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## [!DNL New Relic] consultas

[!DNL New Relic Insights] Los datos de se basan en declaraciones escritas en [!DNL New Relic Query Language] (NRQL) y cualquier parámetro personalizado que pueda incluir. Los datos se pueden devolver desde consultas ad hoc o mediante consultas guardadas en el panel. Para obtener más información, consulte la [Referencia de NRQL][6] en el [!DNL New Relic] documentación.

### Eventos de administración

#### Usuarios administradores activos

Devuelve el número de usuarios administradores activos.

    SELECT uniqueCount(AdminId)
    Transacción FROM
    WHERE appName=&#39;&lt;your_app_name>&#39; DESDE hace 15 minutos

#### Usuarios administradores activos actualmente

Devuelve los nombres de los usuarios administradores activos.

    SELECT uniques(AdminName)
    FROM Transacción
    WHERE appName=&#39;&lt;your_app_name>&#39; DESDE hace 15 minutos
&lt;/your_app_name>
#### Actividad reciente del administrador

Devuelve el número de acciones de administración recientes.

    SELECCIONAR recuento(AdminId)
    Transacción FROM
    WHERE appName =&#39;&lt;your_app_name>&#39; FACET AdminName DESDE hace 1 día

#### Última actividad de administración

Devuelve información detallada sobre las acciones recientes de la administración, incluido el nombre de usuario, la duración y el nombre aplicación del administrador.

    SELECT AdminName, duration, name
    FROM Transacción
    DONDE appName=&#39;&lt;your_app_name>&#39; Y AdminName NO ES NULO
    y AdminName !&lt;/your_app_name>= &#39;N/A&#39; LÍMITE 50

### Eventos Cron

#### Recuento Categoría

Devuelve el número de eventos de aplicación por categoría durante el período de tiempo especificado.

    SELECCIONAR promedio(CatalogCategoryCount)
    DE Cron
    WHERE CatalogCategoryCount NO ES NULO
    AND appName = &#39;&lt;your_app_name>&#39; SERIE TEMPORAL 2 minutos

#### Recuento del catálogo actual

Devuelve el número promedio de eventos de aplicación en el catálogo por categoría durante el período de tiempo especificado.

    SELECCIONAR promedio(CatalogCategoryCount)
    DE Cron
    WHERE CatalogCategoryCount NO ES NULO
    Y CatalogCategoryCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; DESDE hace 2 minutos LÍMITE 1

#### Productos activos

Devuelve el número de eventos de aplicación por producto durante el período de tiempo especificado.

    SELECCIONAR promedio(CatalogProductActiveCount)
    DE Cron
    WHERE CatalogProductActiveCount NO ES NULL
    AND appName = &#39;&lt;your_app_name>&#39; SERIE TEMPORAL 2 minutos

#### Recuento de productos activos

Devuelve el promedio de eventos de aplicación activos por producto durante el período de tiempo especificado.

    SELECCIONAR promedio(CatalogProductActiveCount)
    DE Cron
    WHERE CatalogProductActiveCount NO ES NULL
    AND CatalogProductActiveCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; DESDE hace 2 minutos LÍMITE 1

#### Productos configurables

Devuelve el número promedio de eventos de aplicación para productos configurables durante el período de tiempo especificado.

    SELECCIONAR promedio(CatalogProductConfigurableCount)
    DE Cron
    WHERE CatalogProductConfigurableCount NO ES NULL
    AND appName = &#39;&lt;your_app_name>&#39; SERIE TEMPORAL 2 minutos

#### Recuento de productos configurables

Devuelve el número promedio de eventos de aplicación por producto configurable durante el período de tiempo especificado.

    SELECCIONAR promedio(CatalogProductConfigurableCount)
    DE Cron
    WHERE CatalogProductConfigurableCount NO ES NULL
    AND CatalogProductConfigurableCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; DESDE hace 2 minutos LÍMITE 1

#### Recuento de productos (todos)

Devuelve el número total de eventos de aplicación para todos los productos.

    SELECCIONAR promedio(CatalogProductCount)
    DE Cron
    WHERE CatalogProductCount NO ES NULO
    AND appName = &#39;&lt;your_app_name>&#39; SERIE TEMPORAL 2 minutos

#### Recuento actual de productos (todos)

Devuelve el número promedio de eventos de aplicación para todos los productos durante el período de tiempo especificado.

    SELECCIONAR promedio(CatalogProductCount)
    DE Cron
    WHERE CatalogProductCount NO ES NULO
    Y CatalogProductCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; DESDE hace 2 minutos LÍMITE 1

#### Recuento de clientes

Devuelve el número promedio de eventos de aplicación por cliente.

    SELECCIONAR promedio(CustomerCount)
    DE Cron
    WHERE CustomerCount NO ES NULO
    Y CustomerCount > 0&lt;
    AND appName = &#39;&lt;your_app_name>&#39; SERIE TEMPORAL 2 minutos

#### Recuento de clientes actuales

Devuelve el número promedio de clientes durante el período de tiempo especificado.

    SELECCIONAR promedio(CustomerCount)
    DE Cron
    WHERE CustomerCount NO ES NULO
    Y CustomerCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; DESDE hace 2 minutos LÍMITE 1

#### Estado del módulo

Devuelve el número promedio de veces que los módulos de aplicación están habilitados, deshabilitados o instalados durante el período de tiempo especificado.

    SELECT average(Módulos deshabilitados), average(Módulos habilitados), average
    (Módulos instalados)
    DE Cron&lt;
    WHERE appName = &#39;&lt;your_app_name>&#39; SERIE TEMPORAL 2 minutos

#### Estado actual del módulo

Devuelve el número promedio de veces que los módulos se habilitaron, deshabilitaron o instalaron durante el período de tiempo especificado.

    SELECT average(Módulos deshabilitados), average(Módulos habilitados), average
    (Módulos instalados)
    DE Cron
    WHERE appName = &#39;&lt;your_app_name>&#39; DESDE hace 2 minutos LÍMITE 1

#### Recuentos de sitios web y tiendas

Devuelve el número promedio de eventos de aplicación por sitio web y almacén durante el período de tiempo especificado.

    SELECCIONAR promedio(StoreViewCount), promedio(WebsiteCount)
    DE Cron
    WHERE appName = &#39;&amp;lt;your_app_name&amp;gt;&#39; SERIE TEMPORAL 2 minutos

#### Recuentos actuales de sitios web y tiendas

Devuelve el número promedio de eventos de la aplicación actual durante el período de tiempo especificado.

    SELECCIONAR promedio(StoreViewCount), promedio(WebsiteCount)
    DE Cron
    WHERE appName = &#39;&lt;your_app_name>&#39; DESDE hace 2 minutos LÍMITE 1

#### Cron: todos los datos del evento

Devuelve todos los datos de evento de la aplicación.

    SELECCIONAR *
    DE Cron
    WHERE appName = &#39;&lt;your_app_name>&#39;

### Clientes

#### Recuento de clientes activos

Devuelve el número de clientes activos durante el período de tiempo especificado.

    SELECT uniqueCount(CustomerId)
    Transacción FROM
    WHERE appName = &#39;&lt;your_app_name>&#39; DESDE hace 15 minutos

#### Clientes activos

Devuelve los nombres de los clientes activos durante el período de tiempo especificado.

    SELECT uniques(CustomerName)
    FROM Transacción
    WHERE appName=&#39;&lt;your_app_name>&#39; DESDE hace
 15 minutos&lt;/your_app_name>
#### Clientes principales

Devuelve los clientes principales durante el período de tiempo especificado.

    SELECT count(CustomerId)
    Transacción FROM
    WHERE appName = &#39;&lt;your_app_name>&#39; FACET NombreCliente DESDE hace 1 día

#### Actividad reciente del administrador

Devuelve un número definido de registros de actividad recientes, que incluyen el nombre del cliente y la duración de visita.

    SELECT CustomerName, duration, name
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39;
    And CustomerName IS NOT NULL
    AND CustomerName !&lt;/your_app_name>= &#39;N/A&#39; LÍMITE 50

### Órdenes

#### Número de pedidos asentados

Devuelve el número de pedidos realizados durante el período de tiempo especificado.

    SELECT count(Pedido)
    DESDE Transacción DESDE Hace 1 día

#### Valor de pedido total

Devuelve el número total de elementos de línea pedidos durante el período de tiempo especificado.

    SELECT sum(valorDePedido)
    DESDE Transacción DESDE Hace 1 día

#### Total de elementos de línea pedidos

Devuelve el número total de elementos de línea pedidos durante el período de tiempo especificado.

    SELECT sum(lineItemCount)
    DESDE Transacción DESDE Hace 1 día


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
