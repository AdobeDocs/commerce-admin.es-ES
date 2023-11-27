---
title: Referencia de atributos de datos del cliente
description: Utilice esta referencia de atributos de datos de clientes cuando trabaje con importaciones y exportaciones de datos de clientes.
exl-id: d22ebfed-f439-4a3f-b39e-e957b65c8c21
feature: Customers, Attributes
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# Referencia de atributos de datos del cliente

En las tablas siguientes se enumeran los atributos de una exportación típica del archivo principal del cliente y de las direcciones del cliente. La instalación utilizada para exportar estos datos tiene dos sitios web y varias vistas de tiendas, con los datos de ejemplo instalados.

Cada atributo, o campo, se representa en el archivo CSV como una columna, y los registros de clientes se representan mediante filas. Las columnas que comienzan con un guion bajo son entidades de servicio que contienen propiedades o datos complejos.

## Archivo principal de los clientes

| Atributo | Descripción |
|--- |--- |
| `email` | La dirección de correo electrónico del cliente. |
| `_website` |  |
| `_store` |  |
| `confirmation` | Indicador de confirmación. |
| `created_at` | La fecha de creación de la cuenta del cliente. |
| `created_in` | La vista de la tienda en la que se creó la cuenta. |
| `disable_auto_group_change` | Determina si los grupos de clientes se pueden asignar dinámicamente durante la validación del IVA. |
| `dob` | La fecha de nacimiento del cliente. <br><br>**_Importante:_**De acuerdo con las prácticas recomendadas actuales de seguridad y privacidad, revise el almacenamiento y el procesamiento de la fecha de nacimiento completa de los clientes (mes, día, año). Cuando se recopilan con otros identificadores personales (como_nombre completo _), es un riesgo legal y de seguridad potencial. Se recomienda limitar el almacenamiento de las fechas de nacimiento completas de los clientes y, en su lugar, sugerir el uso del año de nacimiento del cliente como alternativa. |
| `firstname` | El nombre del cliente. |
| `gender` | El sexo del cliente. |
| `group_id` | El ID del grupo de clientes donde se asigna el cliente. |
| `lastname` | El apellido del cliente. |
| `middlename` | El segundo nombre o la inicial del segundo nombre del cliente. |
| `password_hash` | Hash de contraseña |
| `prefix` | Cualquier prefijo que se utilice con el nombre del cliente (como `Mr.`, `Ms.`, `Mrs.`, y `Dr.`). |
| `rp_token` | Restablecer token de contraseña. |
| `rp_token_created_at` | Fecha en la que se restableció la contraseña. |
| `store_id` | ID de tienda |
| `suffix` | Cualquier sufijo que se utilice con el nombre del cliente (como `Jr.`, `Sr.`, y `Esquire`). |
| `taxvat` |  |
| `website_id` | El ID de sitio web del sitio donde se creó la cuenta de cliente. |
| `password` | La contraseña del cliente. |

{style="table-layout:auto"}

## Direcciones de clientes

| Atributo | Descripción |
|--- |--- |
| `_website` |  |
| `_email` |  |
| `_entity_id` |  |
| `city` | La ciudad donde se encuentra la dirección del cliente. |
| `company` | El nombre de la empresa, si corresponde a esta dirección. |
| `country_id` | El ID de país donde se encuentra la dirección del cliente. |
| `fax` | El número de fax del cliente, si corresponde. |
| `firstname` | El nombre del cliente. |
| `lastname` | El apellido del cliente. |
| `middlename` | El segundo nombre o la inicial del segundo nombre del cliente. |
| `postcode` | El código postal donde se encuentra la dirección del cliente. |
| `prefix` | Cualquier prefijo que se utilice con el nombre del cliente (como `Mr.`, `Ms.`, `Mrs.`, y `Dr.`). |
| `region` | La región donde se encuentra la dirección del cliente. |
| `region_id` | ID de región |
| `street` | La dirección postal del cliente. Una segunda línea de la dirección de la calle está disponible si se especifica en la configuración. |
| `suffix` | Si se utiliza, el sufijo asociado al nombre del cliente (por ejemplo, `Jr.`, `Sr.`, o `III`). |
| `telephone` | Número de teléfono del cliente asociado a la dirección. |
| `vat_id` | El ID de IVA es un identificador interno del número de IVA del cliente cuando se utiliza en la validación del IVA. |
| `vat_is_valid` |  |
| `vat_request_date` |  |
| `vat_request_id` |  |
| `vat_request_success` |  |
| `_address_default_billing_` | Identifica la dirección de facturación predeterminada. Un valor de `1` indica que la dirección es la dirección de facturación predeterminada del cliente. Valores: 1 / 0 |
| `_address_default_shipping_` | Identifica la dirección de envío predeterminada. Un valor de `1` indica que la dirección es la dirección de envío predeterminada del cliente. Valores: `1` / `0` |

{style="table-layout:auto"}
