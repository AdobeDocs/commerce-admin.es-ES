---
title: Herramientas de asistencia
description: Obtenga información acerca de las herramientas de soporte proporcionadas que puede utilizar para identificar problemas en el sistema.
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
source-git-commit: 97eeb733836f0336401664c5cfb3df2b9f2f2ccf
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# Herramientas de asistencia

{{ee-feature}}

Las herramientas de soporte están diseñadas para identificar problemas conocidos en su sistema. Pueden utilizarse como recurso durante los procesos de desarrollo y optimización, y como herramienta de diagnóstico para ayudar a nuestro equipo de asistencia a identificar y resolver problemas.

## Recopilador de datos

El recopilador de datos recopila la información sobre el sistema que nuestro equipo de asistencia necesita para solucionar problemas con la instalación de Adobe Commerce. La copia de seguridad creada tarda varios minutos en completarse e incluye un volcado de código y de base de datos. Los datos se pueden exportar a un archivo CSV o a un archivo XML de Excel.

![Sistema - Recopilador de datos](./assets/data-collector.png){width="600" zoomable="yes"}

### Ejecutar el recopilador de datos

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL New Backup]**.

   Se tarda unos minutos en generar la copia de seguridad. Puede monitorizar los resultados del procesamiento haciendo clic en **[!UICONTROL Refresh Status]**. Cuando se completa, la copia de seguridad aparece en el _[!UICONTROL Data Collector]_rejilla.

1. Para ver un registro con los detalles de la copia de seguridad, haga lo siguiente:

   - En el _[!UICONTROL Action]_columna, seleccione **[!UICONTROL Show Log]**.

   - Clic **[!UICONTROL Back]** para volver a la cuadrícula.

   ![registro de recopilación de datos](./assets/data-collector-log.png){width="600" zoomable="yes"}

### Exportar datos de copia de seguridad

1. En la primera columna, seleccione la casilla de la copia de seguridad que desea exportar.

1. Utilice el **[!UICONTROL Export]** para elegir el formato de los datos exportados.

   ![Formato de exportación](./assets/data-collector-export.png){width="600" zoomable="yes"}

1. Acceda al archivo desde la ubicación de descarga del explorador web y **[!UICONTROL Save]** it.

### Descargar datos de copia de seguridad

Una vez generada la copia de seguridad, puede descargar la copia de los datos de código y base de datos.

1. Busque la entidad de copia de seguridad necesaria en la cuadrícula.

1. Asegúrese de que tiene un `Complete` estado.

1. Haga clic en el nombre de la entidad en _[!UICONTROL Code Dump]_o_[!UICONTROL DB Dump]_ columnas.

El proceso de descarga debería iniciarse automáticamente.

## Eliminar datos de copia de seguridad

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Busque y seleccione los datos de copia de seguridad que desea eliminar.

1. En el _[!UICONTROL Action]_, haga clic en **[!UICONTROL Delete]**.

1. Para confirmar la acción, haga clic en **[!UICONTROL OK]**.

## Informes del sistema

La herramienta de sistema de informes le permite realizar instantáneas periódicas completas o parciales del sistema y guardarlas para referencia futura. Puede comparar la configuración de rendimiento antes y después de los ciclos de desarrollo de código o los cambios en la configuración del servidor. La herramienta de sistema de informes puede reducir drásticamente el tiempo empleado en preparar y enviar la información requerida por el Soporte para comenzar una investigación.

Desde la cuadrícula Informes del sistema, puede ver y descargar informes existentes, eliminar informes y crear informes.

### Acceso a informes del sistema

En el _Administrador_ barra lateral, vaya a **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.

![Administrador - Informes del sistema](./assets/reports.png){width="600" zoomable="yes"}

### Generación de un informe

1. Haga clic **[!UICONTROL New Report]**.

1. En el **[!UICONTROL Groups]** , seleccione cada conjunto de información que desee incluir en el informe. De forma predeterminada, se seleccionan todos los grupos.

   ![Informe del sistema - seleccionar grupos](./assets/report-create.png){width="600" zoomable="yes"}

1. En la esquina superior derecha, haga clic en **[!UICONTROL Create]**.

   El informe puede tardar unos minutos en generarse, según el número de tipos de informe seleccionados. Cuando el informe esté listo, aparecerá en la parte superior de la cuadrícula con la fecha y la hora generadas.

### Ver información del módulo

Puede encontrar información útil sobre los módulos instalados.

**_Para ver la información del informe de cada módulo instalado:_**

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.
1. Haga clic **[!UICONTROL New Report]**.
1. Seleccionar `Modules` desde el **[!UICONTROL Groups]** lista.
1. Haga clic **[!UICONTROL Create]**.
1. Una vez generado el informe, haga clic en **[!UICONTROL Select]** y luego **[!UICONTROL View]** para ver todas las versiones de los módulos.
1. Clic **[!UICONTROL Download]** para descargar el informe.

### Administrar informes del sistema

En el **[!UICONTROL Action]** de la cuadrícula, seleccione una de las siguientes opciones:

- `View` : Utilice esta función para ver los detalles del informe.
- `Delete` : Utilice esta función para eliminar el informe generado de la lista.
- `Download` : Utilice esta función para guardar el informe como archivo de HTML.

### Ver detalles del informe del sistema

1. Para el informe que necesite, seleccione **[!UICONTROL View]** en el _[!UICONTROL Actions]_columna.

1. En el panel izquierdo, expanda ![Selector de expansión](../assets/icon-display-expand.png) cada sección del informe para ver los detalles.

   ![Información general del informe del sistema](./assets/report-information.png){width="600" zoomable="yes"}

### Informes del sistema disponibles

| Grupo de informes | Información incluida |
| ------------ | -------------------- |
| [!UICONTROL General] | Versión de Adobe Commerce<br>Recuento de datos<br>Estado de caché<br>Estado del índice |
| [!UICONTROL Environment] | Información del entorno<br>Estado de MySQL |
| [!UICONTROL Data] | Duplicar categorías por clave de URL<br>Duplicar productos por clave URL<br>Duplicar productos por SKU<br>Duplicar Pedidos Por Id De Incremento<br>Duplicar usuarios por correo electrónico<br>Datos de categorías dañadas |
| [!UICONTROL Modules] | Lista de módulos personalizados<br>Lista de módulos deshabilitados<br>Lista de todos los módulos |
| [!UICONTROL Configuration] | Configuración<br>Datos de `app/etc/env.php`<br>Métodos de envío<br>Métodos de pago<br>Matriz de funciones de pagos |
| [!UICONTROL Logs] | Archivos de registro<br>Mensajes principales del sistema<br>Mensajes principales del sistema de hoy<br>Mensajes de depuración principales<br>Principales mensajes de depuración de hoy<br>Principales mensajes de excepción<br>Principales mensajes de excepción de hoy |
| [!UICONTROL Attributes] | Atributos EAV definidos por el usuario<br>Nuevos atributos de EAV<br>Tipos de entidad<br>Todos los atributos de EAV<br>Atributos de EAV de categoría<br>Atributos EAV del producto<br>Atributos EAV del cliente<br>Atributo EAV de la dirección del cliente<br>Atributos EAV de artículos RMA |
| [!UICONTROL Events] | Eventos globales personalizados<br>Eventos de administración personalizados<br>Eventos de front-end personalizados<br>Eventos de documentos personalizados<br>Eventos personalizados de Crontab<br>Eventos REST personalizados<br>Eventos SOAP personalizados<br>Eventos globales principales<br>Eventos de administración principal<br>Eventos de front-end principales<br>Eventos de documentos principales<br>Eventos principales de Crontab<br>Eventos de REST principales<br>Eventos SOAP principales<br>Todos los eventos globales<br>Todos los eventos de administración<br>Todos los eventos de front-end<br>Todos los eventos del documento<br>Todos los eventos REST<br>Todos los eventos SOAP<br>Todos los eventos de Crontab |
| [!UICONTROL Cron] | Programaciones de Cron por código de estado<br>Programaciones de Cron por código de trabajo<br>Errores en la cola de programaciones de Cron<br>Lista de horarios de Cron<br>Trabajos Cron globales personalizados<br>Trabajos Cron configurables personalizados<br>Trabajos Cron globales principales<br>Trabajos Cron Core Configurables<br>Todos los trabajos de Cron globales<br>Todos los trabajos de Cron configurables |
| [!UICONTROL Design] | Lista de temas de Adminhtml<br>Lista de temas de front-end |
| [!UICONTROL Stores] | Árbol de sitios web<br>Lista de sitios web<br>Lista de tiendas<br>Lista de vistas de tienda |
| Conector de OMS <br>_(visible con la integración de OMS)_ | Versión del conector<br>Supervisión del conector<br>Resultados del procesamiento de mensajes |

{style="table-layout:auto"}
