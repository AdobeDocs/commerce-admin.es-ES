---
title: Archivos de datos CSV
description: Obtenga información acerca de la estructura utilizada en el archivo CSV para admitir la importación y exportación de datos.
exl-id: 86e362af-2af7-4557-ac49-1efad2f0e976
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 0%

---

# Archivos de datos CSV

El formato de archivo de valores separados por comas (CSV) se utiliza como base de las operaciones de transferencia de datos y lo admiten todas las aplicaciones de hojas de cálculo y bases de datos. Se admiten los siguientes tipos de archivos para la importación y exportación:

- Importar: `CSV` y `ZIP` (un archivo CSV comprimido)
- Exportar: `CSV`

>[!IMPORTANT]
>
>Se recomienda utilizar un programa compatible con la codificación UTF-8, como Notepad++, para editar archivos CSV. Microsoft® Excel inserta caracteres adicionales en el encabezado de columna del archivo CSV, lo que puede impedir que los datos se importen de nuevo en Commerce. Si trabaja en Mac, puede guardar los datos en formato CSV (Windows).

Los archivos CSV tienen una estructura específica que debe coincidir con la base de datos. Cada encabezado de columna corresponde al código de atributo del campo representado por la columna. Para garantizar que Commerce pueda leer los encabezados de columna, primero exporte los datos de su tienda como archivo CSV. A continuación, puede editar los datos y volver a importarlos en Commerce.

Si abre un archivo CSV exportado en un editor de texto, verá que los valores están separados por comas y que varios valores están entre comillas dobles. Durante la importación, puede especificar un carácter separador personalizado, aunque la coma es el valor predeterminado.

## Estructura CSV del producto

Una exportación completa de la base de datos de productos contiene información sobre cada producto del catálogo y las relaciones entre ellos. Cada registro tiene una selección fija de columnas que corresponde a los atributos del catálogo, aunque el orden de los atributos se ignora durante el proceso de importación.

La primera fila de la tabla contiene los nombres de cada atributo, que se utilizan como encabezados de columna. Las filas restantes describen los registros de producto individuales. Cualquier fila que comience con un valor en la columna SKU es el comienzo de un nuevo registro de producto. Un solo producto puede incluir varias filas que contienen información sobre varias imágenes u opciones de producto. La siguiente fila que tiene un valor en la columna SKU inicia un nuevo producto.

La columna category contiene una ruta para cada categoría a la que está asignado el producto. La ruta incluye la categoría raíz, seguida de una barra diagonal (`/`) entre cada nivel. De forma predeterminada, la coma `,` se usa para separar diferentes rutas de categorías. (Puede especificar un carácter separador diferente con la variable _[!UICONTROL Multiple value separator]_opción.) Por ejemplo:

`Default Category/Gear,Default Category/Gear/Bags`

Para importar datos, solo debe incluir el SKU y las columnas con cambios. Las columnas en blanco se omiten durante el proceso de importación. No es posible añadir atributos durante el proceso de importación. Solo se pueden incluir atributos existentes.

Para ver una descripción detallada de cada atributo de producto, consulte [Estructura de archivos CSV del producto](data-attributes-product.md).

| Nombre de columna | Descripción |
| ----------- | ----------- |
| `_<name>` | Los encabezados de columna que comienzan con un guion bajo contienen propiedades de entidad de servicio o datos complejos. Las columnas de servicio no son atributos de producto. |
| `<attribute_name>` | Los encabezados de columna con un código de atributo o un nombre de campo identifican la columna de datos. Una columna puede representar un atributo del sistema o uno que haya creado el administrador del almacén. |

{style="table-layout:auto"}

## Estructura CSV del cliente

El archivo CSV de clientes contiene información de clientes de la base de datos y tiene la siguiente estructura:

La primera fila de la tabla contiene los nombres de las columnas de atributos (que son iguales que los códigos de atributos). Existen dos tipos de nombres de columna, como se muestra en la tabla siguiente. Otras filas contienen valores de atributo, datos de servicio y datos complejos. Cada fila con valores no vacíos en `email` y `_website` columnas inicia la descripción del cliente subsiguiente. Cada fila puede representar los datos del cliente con o sin datos de dirección, o solo los datos de dirección. Si una fila contiene solo los datos de dirección, los valores de las columnas, relacionados con el perfil del cliente, se omiten y pueden estar vacíos.

Para agregar o reemplazar más de una dirección para un cliente, agregue una fila para cada nueva dirección con datos de cliente vacíos y los datos de dirección nuevos o actualizados debajo de la fila de datos de cliente.

Para obtener una descripción detallada de cada atributo del cliente, consulte [Estructura del archivo CSV del cliente](data-attributes-customer.md).

| Nombre de columna | Descripción |
| ----------- | ----------- |
| `_<name>` | Los encabezados de columna que comienzan con un guion bajo contienen propiedades de entidad de servicio o datos complejos. Las columnas de servicio no son atributos del cliente. |
| `<attribute name>` | Nombres de las columnas con valores de atributos creados por el sistema y atributos creados por el administrador del almacén. |

{style="table-layout:auto"}
