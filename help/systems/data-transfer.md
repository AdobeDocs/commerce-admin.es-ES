---
title: Transferencia de datos
description: Obtenga información sobre la compatibilidad con la transferencia de datos, incluida la validación de datos.
exl-id: 5057e398-c458-42e9-8ec0-bf116a667a3c
feature: System, Data Import/Export
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# Transferencias de datos

Utilice las herramientas de importación y exportación para administrar varios registros en una sola operación. Puede importar nuevos elementos, así como actualizar, reemplazar y eliminar conjuntos de productos existentes.

Por ejemplo, puede agregar nuevos productos al inventario, actualizar los datos de productos y los datos de precios avanzados, y reemplazar un conjunto de productos existentes con nuevos productos. Las herramientas de importación y exportación ayudan a administrar los catálogos de productos grandes de forma más eficaz, ya que pueden exportarse los datos, editarse en una hoja de cálculo e importarse de nuevo en la tienda en lugar de realizar varias operaciones en el administrador.


>[!NOTE]
>
>Adobe Commerce también admite la exportación de datos SaaS para transferir datos de productos del servidor de Commerce a los servicios SaaS. La exportación de datos SaaS está integrada con los servicios SaaS de Commerce, que incluyen [Recomendaciones de productos](https://experienceleague.adobe.com/docs/commerce/product-recommendations/overview.html?lang=es), [Live Search](https://experienceleague.adobe.com/es/docs/commerce/live-search/overview) y [Servicio de catálogo](https://experienceleague.adobe.com/es/docs/commerce/catalog-service/guide-overview). Para obtener más información, consulte la [Guía de exportación de datos SaaS](https://experienceleague.adobe.com/es/docs/commerce/saas-data-export/overview).

## Validación de datos

Todos los datos deben pasar la validación para garantizar la calidad, precisión e integridad de los valores antes de importarlos al almacén. La validación comienza al hacer clic en **[!UICONTROL Check Data]**. Durante el proceso, se comprueba lo siguiente en todas las entidades del archivo de importación:

- **Atributos**: los nombres de los encabezados de columna se verifican para garantizar que coinciden con los atributos correspondientes de la base de datos del sistema. El valor de cada atributo se comprueba para garantizar que cumple los requisitos del tipo de datos (decimal, entero, varchar, texto y fecha y hora).
- **Datos complejos**: los valores que se originan en un conjunto definido, como un tipo de entrada de selección múltiple o desplegable, se verifican para garantizar que los valores existan en el conjunto definido.
- **Datos de servicio**: los valores de las columnas de datos de servicio se verifican para garantizar que las propiedades o los valores de datos complejos sean coherentes con lo que ya se ha definido en la base de datos del sistema.
- **Valores requeridos**: para las nuevas entidades, se comprueba la presencia de valores de atributo requeridos en el archivo. Para las entidades existentes, no es necesario volver a comprobar la existencia de los valores de atributo requeridos.
- **Separadores**: aunque los separadores no están visibles cuando se ven en una hoja de cálculo, los valores de datos de un archivo CSV están separados por comas y los valores de texto están entre comillas dobles. Durante el proceso de validación, se comprueba el formato de los separadores y de cada conjunto de comillas que encierran cadenas de caracteres.

Los resultados de la validación aparecen en la sección Resultados de validación e incluyen la siguiente información:

- El número de entidades comprobadas
- Número de filas no válidas
- El número de errores encontrados

Si los datos son válidos, aparecerá un mensaje _Éxito de importación_.

![Mensaje del sistema - el archivo es válido](./assets/data-import-validation-message.png){width="500" zoomable="yes"}

Si la validación falla, lea la descripción de cada error y corrija el problema en el archivo CSV. Por ejemplo, si una fila contiene un SKU no válido, el proceso de importación se detiene, y esa fila y todas las filas posteriores no se importan. Una vez solucionado correctamente el problema, vuelva a importar los datos. Si se encuentran muchos errores, es posible que se necesiten varios intentos para pasar la validación.

### Mensajes de validación de datos

#### Validación

- `Product with specified SKU not found in rows: 1`
- `URL key for specified store already exists`
- `'7z' file extension is not supported`
- `TXT file extension is not supported`

#### Errores

- `Wrong field type. Type in the imported file %decimal%, expected type is %text%.`
- `Value is not allowed. Attribute value does not exist in the system.`
- `Field %column name% is required.Wrong value separator is used.`
- `Wrong encoding used. Supported character encoding is UTF-8 and Windows-1252.`
- `Imported file does not contain SKU field.`
- `SKU does not exist in the system.`
- `Column name %column name% is invalid. Should start with a letter. Alphanumeric.`
- `Imported file does not contain a header.`
- `%website name% website does not exist in the system.`
- `%storeview name% storeview does not exist in the system.`
- `Imported attribute %attribute name% does not exist in the system.`
- `Imported resource (image) could not be downloaded from external resource due to timeout or access permissions.`
- `Imported resource (image) does not exist in the local media storage.`
- `Product creation error displayed to the user equal to the one seen during manual product save.`
- `Advanced Price creation error displayed to the user equal to the one seen during the manual product save.`
- `Customer creation error displayed to the user equal to the one seen during the manual customer save.`
