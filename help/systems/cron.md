---
title: Cron (tareas programadas)
description: Aprenda a controlar la ejecución y la programación de los trabajos cron de Commerce desde el administrador.
exl-id: e0da08ab-212f-4977-9387-0b4b40560cfb
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Cron (tareas programadas)

Adobe Commerce y Magento Open Source realizan algunas operaciones según lo programado ejecutando periódicamente una secuencia de comandos. Puede controlar la ejecución y la programación de los trabajos cron de Commerce desde el administrador. Las operaciones de almacenamiento que se ejecutan según una programación de cron incluyen, entre otras:

- [Correo electrónico](email-communications.md)
- [Reglas de precio de catálogo](../merchandising-promotions/price-rules-catalog.md)
- [Newsletters](../merchandising-promotions/newsletters.md)
- [Generación de mapa del sitio XML](../merchandising-promotions/sitemap-xml.md)
- [Actualizaciones de tipos de cambio](../stores-purchase/currency-update.md)
- [Inventory management](../inventory-management/introduction.md)

>[!IMPORTANT]
>
>Los servicios de Commerce deben instalarse en crontab para garantizar que los componentes principales y algunas extensiones de terceros funcionen según lo esperado. Consulte las [instrucciones de la _Guía de instalación_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html) para obtener información detallada sobre cómo instalar los servicios en crontab.

Además, puede configurar lo siguiente para que se ejecute según una programación cron:

- Ordenar actualizaciones y reindexación de la cuadrícula del sistema
- Duración del pago pendiente

Asegúrese de que las [direcciones URL base](../stores-purchase/store-urls.md) de la tienda estén configuradas correctamente para que las direcciones URL generadas durante las operaciones cron sean correctas. Para Adobe Commerce sobre la infraestructura en la nube, consulte [Configuración de trabajos cron](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html) en la _Guía de Commerce sobre la infraestructura en la nube_. Para obtener acceso local, consulte [Configurar y ejecutar con](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html) en la _Guía de configuración_.

## Configuración de cron

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL System]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Cron]**.

   ![Configuración avanzada: tareas cron](../configuration-reference/advanced/assets/system-cron.png){width="600" zoomable="yes"}

1. Complete la siguiente configuración para los grupos **[!UICONTROL Index]** y **[!UICONTROL Default]**.

   La configuración es la misma en cada sección.

   - **[!UICONTROL Generate Schedules Every]**: define la frecuencia con la que se genera la programación (en minutos). Las programaciones se almacenan en la base de datos.
   - **[!UICONTROL Schedule Ahead for]**: define con qué anticipación se programan los trabajos cron (en minutos). Por ejemplo, si esta configuración se establece en `10` y se ejecuta cron, los trabajos cron se programan para los próximos 10 minutos.
   - **[!UICONTROL Missed if not Run Within]**: define el tiempo (en minutos) utilizado para determinar un trabajo perdido. Si el trabajo cron no se ejecuta a su hora programada y transcurre el tiempo especificado, no se puede ejecutar y su estado se establece en `Missed`.
   - **[!UICONTROL History Cleanup Every]**: define el tiempo (en minutos) que se borra el historial de tareas finalizadas de la base de datos.
   - **[!UICONTROL Success History Lifetime]**: define el tiempo (en minutos) que el historial de trabajos cron con un estado `Successful` permanece en la base de datos.
   - **[!UICONTROL Failure History Lifetime]**: define el tiempo (en minutos) que el historial de trabajos cron con un estado `Error` permanece en la base de datos.
   - **[!UICONTROL Use Separate Process]**: define si todos los trabajos cron del grupo se ejecutan en un proceso del sistema independiente. Opciones: `Yes` / `No`

   ![Configuración avanzada: índice de grupo cron](../configuration-reference/advanced/assets/system-cron-group-index.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
