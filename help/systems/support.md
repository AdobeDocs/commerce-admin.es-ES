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

1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL New Backup]**.

   Se tarda unos minutos en generar la copia de seguridad. Puede supervisar los resultados del procesamiento haciendo clic en **[!UICONTROL Refresh Status]**. Una vez completada, la copia de seguridad aparecerá en la cuadrícula _[!UICONTROL Data Collector]_.

1. Para ver un registro con los detalles de la copia de seguridad, haga lo siguiente:

   - En la columna _[!UICONTROL Action]_, seleccione **[!UICONTROL Show Log]**.

   - Haga clic en **[!UICONTROL Back]** para regresar a la cuadrícula.

   ![registro de recopilador de datos](./assets/data-collector-log.png){width="600" zoomable="yes"}

### Exportar datos de copia de seguridad

1. En la primera columna, seleccione la casilla de la copia de seguridad que desea exportar.

1. Utilice el menú **[!UICONTROL Export]** para elegir el formato de los datos exportados.

   ![Formato de exportación](./assets/data-collector-export.png){width="600" zoomable="yes"}

1. Acceda al archivo desde la ubicación de descarga del explorador web y **[!UICONTROL Save]** desde ella.

### Descargar datos de copia de seguridad

Una vez generada la copia de seguridad, puede descargar la copia de los datos de código y base de datos.

1. Busque la entidad de copia de seguridad necesaria en la cuadrícula.

1. Asegúrese de que tenga un estado `Complete`.

1. Haga clic en el nombre de la entidad en _[!UICONTROL Code Dump]_o_[!UICONTROL DB Dump]_ columnas.

El proceso de descarga debería iniciarse automáticamente.

## Eliminar datos de copia de seguridad

1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Busque y seleccione los datos de copia de seguridad que desea eliminar.

1. En la columna _[!UICONTROL Action]_, haga clic en **[!UICONTROL Delete]**.

1. Para confirmar la acción, haga clic en **[!UICONTROL OK]**.

## Informes del sistema

La herramienta de sistema de informes le permite realizar instantáneas periódicas completas o parciales del sistema y guardarlas para referencia futura. Puede comparar la configuración de rendimiento antes y después de los ciclos de desarrollo de código o los cambios en la configuración del servidor. La herramienta de sistema de informes puede reducir drásticamente el tiempo empleado en preparar y enviar la información requerida por el Soporte para comenzar una investigación.

Desde la cuadrícula Informes del sistema, puede ver y descargar informes existentes, eliminar informes y crear informes.

### Acceso a informes del sistema

En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.

![Administrador - informes del sistema](./assets/reports.png){width="600" zoomable="yes"}

### Generación de un informe

1. Haga clic en **[!UICONTROL New Report]**.

1. En la lista **[!UICONTROL Groups]**, seleccione cada conjunto de información que desee incluir en el informe. De forma predeterminada, se seleccionan todos los grupos.

   ![Informe del sistema - seleccionar grupos](./assets/report-create.png){width="600" zoomable="yes"}

1. En la esquina superior derecha, haga clic en **[!UICONTROL Create]**.

   El informe puede tardar unos minutos en generarse, según el número de tipos de informe seleccionados. Cuando el informe esté listo, aparecerá en la parte superior de la cuadrícula con la fecha y la hora generadas.

### Ver información del módulo

Puede encontrar información útil sobre los módulos instalados.

**_Para ver la información del informe de cada módulo instalado:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.
1. Haga clic en **[!UICONTROL New Report]**.
1. Seleccione `Modules` de la lista **[!UICONTROL Groups]**.
1. Haga clic en **[!UICONTROL Create]**.
1. Una vez generado el informe, haga clic en **[!UICONTROL Select]** y luego en **[!UICONTROL View]** para ver todas las versiones de los módulos.
1. Haga clic en **[!UICONTROL Download]** para descargar el informe.

### Administrar informes del sistema

En la columna **[!UICONTROL Action]** de la cuadrícula, seleccione una de las siguientes opciones:

- `View`: utilice esta función para ver los detalles del informe.
- `Delete` - Utilice esta función para eliminar el informe generado de la lista.
- `Download`: utilice esta función para guardar el informe como archivo de HTML.

### Ver detalles del informe del sistema

1. Para el informe que necesita, seleccione **[!UICONTROL View]** en la columna _[!UICONTROL Actions]_.

1. En el panel izquierdo, expanda ![Selector de expansión](../assets/icon-display-expand.png) cada sección del informe para ver los detalles.

   ![Información general del informe del sistema](./assets/report-information.png){width="600" zoomable="yes"}

### Informes del sistema disponibles

| Grupo de informes | Información incluida |
| ------------ | -------------------- |
| [!UICONTROL General] | Versión de Adobe Commerce<br>Recuento de datos<br>Estado de la caché<br>Estado del índice |
| [!UICONTROL Environment] | Información del entorno<br>Estado de MySQL |
| [!UICONTROL Data] | Duplicar categorías por clave URL<br>Duplicar productos por clave URL<br>Duplicar productos por SKU<br>Duplicar pedidos por id. de incremento<br>Duplicar usuarios por correo electrónico<br>Datos de categorías dañadas |
| [!UICONTROL Modules] | Lista de módulos personalizados<br>Lista de módulos deshabilitados<br>Lista de todos los módulos |
| [!UICONTROL Configuration] | Configuración<br>Datos de `app/etc/env.php`<br>Métodos de envío<br>Métodos de pago<br>Matriz de funcionalidad de pagos |
| [!UICONTROL Logs] | Archivos de registro<br>Mensajes principales del sistema<br>Mensajes principales del sistema de hoy<br>Mensajes principales de depuración<br>Mensajes principales de depuración de hoy<br>Mensajes principales de excepción de hoy<br>Mensajes principales de excepción de hoy |
| [!UICONTROL Attributes] | Atributos EAV definidos por el usuario<br>Nuevos atributos EAV<br>Tipos de entidad<br>Todos los atributos EAV<br>Atributos EAV de la categoría<br>Atributos EAV del producto<br>Atributos EAV del cliente<br>Atributo EAV de la dirección del cliente<br>Atributos EAV del elemento RMA |
| [!UICONTROL Events] | SOAP SOAP SOAP Eventos globales personalizados<br>Eventos de administración personalizados<br>Eventos de front-end personalizados<br>Eventos de doc personalizados<br>Eventos de crontab personalizados<br>Eventos de REST personalizados<br>Eventos de administración personalizados<br>Eventos globales de núcleo<br>Eventos de administración de núcleo<br>Eventos de front-end de núcleo<br>Eventos de doc de núcleo<br>Eventos de crontab de núcleo<br>Eventos de rest de núcleo<br>Eventos de núcleo<br>Todos los eventos globales<br>Todos los eventos de administración<br>Todos los eventos de front<br>Todos los eventos de REST 8}Todos los eventos de la<br>Todos los eventos de Crontab<br><br> |
| [!UICONTROL Cron] | Programaciones de Cron por código de estado<br>Programaciones de Cron por código de trabajo<br>Errores en la cola de programaciones de Cron<br>Lista de programaciones de Cron<br>Trabajos de Cron globales personalizados<br>Trabajos de Cron configurables personalizados<br>Trabajos de Cron globales principales<br>Trabajos de Cron configurables principales<br>Todos los trabajos de Cron globales<br>Todos los trabajos de Cron configurables |
| [!UICONTROL Design] | Lista de temas de Adminhtml<br>Lista de temas de FrontEnd |
| [!UICONTROL Stores] | Árbol de sitios web<br>Lista de sitios web<br>Lista de tiendas<br>Lista de vistas de tiendas |
| Conector de OMS <br>_(visible con la integración de OMS)_ | Versión del conector<br>Supervisión del conector<br>Resultados del procesamiento de mensajes |

{style="table-layout:auto"}
