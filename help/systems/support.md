---
title: Herramientas de asistencia
description: Obtenga información acerca de las herramientas de soporte proporcionadas que puede utilizar para identificar problemas en el sistema.
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: addde8c3e41b641712f5b08107c1d68b40cd4159
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---

# Herramientas de asistencia

{{ee-feature}}

Las herramientas de soporte están diseñadas para identificar problemas conocidos en su sistema. Pueden utilizarse como recurso durante los procesos de desarrollo y optimización, y como herramienta de diagnóstico para ayudar a nuestro equipo de asistencia a identificar y resolver problemas.

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
- `Download`: utilice esta función para guardar el informe como archivo HTML.

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
| [!UICONTROL Events] | Eventos globales personalizados<br>Eventos de administración personalizados<br>Eventos de front-end personalizados<br>Eventos de documentos personalizados<br>Eventos de crontab personalizados<br>Eventos de REST personalizados<br>Eventos de SOAP personalizados<br>Eventos globales principales<br>Eventos de administración central<br>Eventos de front-end principales<br>Eventos de documentos principales<br>Eventos de Core Crontab<br>Eventos de Core REST<br>Eventos de Core SOAP<br>Todos los eventos globales<br>Todos los eventos de administración<br>Todos los eventos de front-end<br>Todos los eventos de Doc<br>Todos los REST Eventos<br>Todos los eventos de SOAP<br>Todos los eventos de Crontab |
| [!UICONTROL Cron] | Programaciones de Cron por código de estado<br>Programaciones de Cron por código de trabajo<br>Errores en la cola de programaciones de Cron<br>Lista de programaciones de Cron<br>Trabajos de Cron globales personalizados<br>Trabajos de Cron configurables personalizados<br>Trabajos de Cron globales principales<br>Trabajos de Cron configurables principales<br>Todos los trabajos de Cron globales<br>Todos los trabajos de Cron configurables |
| [!UICONTROL Design] | Lista de temas de Adminhtml<br>Lista de temas de FrontEnd |
| [!UICONTROL Stores] | Árbol de sitios web<br>Lista de sitios web<br>Lista de tiendas<br>Lista de vistas de tiendas |
| Conector de OMS <br>_(visible con la integración de OMS)_ | Versión del conector<br>Supervisión del conector<br>Resultados del procesamiento de mensajes |

{style="table-layout:auto"}
