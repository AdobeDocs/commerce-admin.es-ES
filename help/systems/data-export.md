---
title: Exportación de datos
description: Obtenga información sobre los filtros y atributos de exportación de datos y cómo exportar datos desde su tienda.
exl-id: 80e7a2fc-beaa-416e-a00f-a3cad5055975
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# Exportación de datos

La mejor manera de familiarizarse con la estructura de la base de datos es exportar los datos y abrirlos en una hoja de cálculo. Después de familiarizarse con el proceso, puede utilizarlo como una forma eficaz de administrar grandes cantidades de información.

Los caracteres especiales, como el signo igual, mayor y menor que los símbolos, las comillas simples y dobles, la barra invertida, la barra vertical y los símbolos ampersand, pueden causar problemas durante la transferencia de datos. Para garantizar que estos caracteres especiales se interpreten correctamente, pueden marcarse como un _secuencia de escape_. Por ejemplo, si los datos incluyen una cadena de texto como `code="str"`, `code="str2"`, escribir el texto entre comillas dobles garantiza que las comillas dobles originales se entiendan como parte de los datos: `"code="str""`. Cuando el sistema encuentra un conjunto doble de comillas dobles, entiende que el conjunto exterior de comillas dobles está encerrando los datos reales.

La exportación de datos es una operación asincrónica, que se ejecuta en segundo plano para que pueda seguir trabajando en el administrador sin esperar a que finalice la operación. El sistema muestra un mensaje cuando se completa la tarea.

## Exportar criterios

Los filtros de exportación se utilizan para especificar los datos que desea incluir en el archivo de exportación, según el valor del atributo. Además, puede especificar qué datos de atributo desea incluir o excluir de la exportación.

![Criterios de exportación de datos](./assets/data-export-entity-attributes-exclude.png){width="600" zoomable="yes"}

### Exportar filtros

Puede utilizar filtros para determinar qué SKU se incluyen en el archivo de exportación. Por ejemplo, si se introduce un valor en el filtro País de fabricación, el archivo CSV exportado solo incluirá los productos fabricados en ese país.

El tipo de filtro corresponde al tipo de datos. Para los campos de fecha, puede elegir la fecha del Calendario ![Icono de calendario](../assets/icon-calendar.png). Consulte [Tipos de entrada de atributos](../catalog/attributes-input-types.md) para obtener más información.

El formato de la fecha viene determinado por la variable [locale](../getting-started/store-details.md#locale-options).

Para incluir solo registros con un valor específico, como un SKU, introduzca el valor en el campo Filtro. Algunos campos, como Precio, Peso y Definir producto como nuevo, tienen un rango de valores de origen y destino.

### Excluir atributos

La casilla de verificación de la primera columna se utiliza para excluir atributos del archivo de exportación. Si se excluye un atributo, se incluye la columna asociada en los datos de exportación, pero vacía.

| Excluir | Filtrar | Resultado |
|--- |--- |--- |
| ![Casilla desactivada](../assets/checkbox-clear.png) | No | El archivo exportado contiene cada atributo para todos los registros existentes. |
| ![Casilla desactivada](../assets/checkbox-clear.png) | Sí | El archivo de exportación contiene cada atributo con solo los registros permitidos por el filtro. |
| ![Casilla seleccionada](../assets/checkbox-selected.png) | No | El archivo de exportación no incluye la columna para el atributo excluido, pero sí incluye todos los registros existentes. |
| ![Casilla seleccionada](../assets/checkbox-selected.png) | Sí | El archivo de exportación no incluye la columna para el atributo excluido y contiene solo los registros permitidos por el filtro. |

{style="table-layout:auto"}

## Exportación de datos

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. En el _Configuración de exportación_ sección, conjunto **[!UICONTROL Entity Type]** a uno de los siguientes:

   - `Advanced Pricing`
   - `Products`
   - `Customer Finances`
   - `Customers Main File`
   - `Customer Addresses`
   - `Stock Sources`

   ![Configuración de exportación de datos](./assets/data-export-settings.png){width="600" zoomable="yes"}

1. Aceptar el valor predeterminado **[!UICONTROL Export File Format]** de CSV.

1. Si desea incluir cualquier carácter especial que se pueda encontrar en los datos como un _secuencia de escape_, seleccione la **[!UICONTROL Fields Enclosure]** casilla de verificación

1. Si es necesario, cambie la visualización de los atributos de entidad.

   De forma predeterminada, la sección Atributos de entidad enumera todos los atributos disponibles en orden alfabético. Puede utilizar el estándar de [controles de lista](../getting-started/admin-grid-controls.md) para buscar atributos específicos y ordenar la lista. Los controles Filtro de búsqueda y restablecimiento controlan la visualización de la lista, pero no tienen ningún efecto en la selección de atributos que se van a incluir en el archivo de exportación.

   ![Atributos de entidad filtrados de exportación de datos](./assets/data-export-filter-entity-attributes.png){width="600" zoomable="yes"}

1. Para filtrar los datos exportados en función del valor del atributo, haga lo siguiente:

   - Para exportar solo registros con valores de atributo específicos, introduzca el valor requerido en la variable **[!UICONTROL Filter]** columna. En el siguiente ejemplo, se exporta únicamente un SKU específico.

   - Para omitir un atributo de la exportación, seleccione la opción **[!UICONTROL Exclude]** al principio de la fila. Por ejemplo, para exportar solo los `sku` y `image` , active la casilla de verificación de cada atributo. La columna aparece en el archivo de exportación, pero sin ningún valor.

1. Desplácese hacia abajo y haga clic **[!UICONTROL Continue]** en la esquina inferior derecha de la página.

   Una vez finalizada la tarea, el archivo se procesa a través de una cola de mensajes (asegúrese de que el trabajo cron se esté ejecutando). El archivo exportado se guarda en la `var/export/ folder`. Para obtener más información sobre la cola de mensajes, consulte [Administrar colas de mensajes](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) en el _Guía de configuración_.

   Puede guardar o abrir el archivo CSV exportado como hoja de cálculo y, a continuación, editar los datos e importarlos de nuevo en su tienda.

   >[!NOTE]
   >
   >De forma predeterminada, todos los archivos exportados se encuentran en `<Magento-root-directory>/var/export` carpeta. Si el módulo Almacenamiento remoto está habilitado, todos los archivos exportados se encuentran en la `<remote-storage-root-directory>/import_export/export` carpeta.

## Solución de problemas de recursos

Para obtener ayuda sobre la resolución de problemas de exportación de datos, consulte los siguientes artículos de la Base de conocimiento de asistencia técnica de Commerce:

- [El archivo .csv de productos exportados no aparece](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/exported-products-.csv-file-does-not-appear.html)
- [El archivo de exportación del producto no se muestra en el administrador](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-31168-magento-patch-product-export-file-does-not-show-in-admin.html)
- [Problema al exportar pedidos en formato CSV](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31242-magento-patch-issue-in-exporting-orders-in-csv-format.html)
