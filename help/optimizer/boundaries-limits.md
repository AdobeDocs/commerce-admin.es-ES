---
title: Límites y límites de los servicios de comercialización
description: Obtenga información acerca de los límites de licencias de Adobe Commerce Optimizer y los límites del sistema. Planifique la capacidad, rastree el uso y evite la latencia y la limitación al superar los límites.
role: Admin, Developer
hide: true
badgeSaas: label="Solo SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a instancias de Adobe Commerce as a Cloud Service aprovisionadas con CCDM (infraestructura de SaaS administrada por Adobe)."
autotag-review: '2026-11-02T18:48:38.168Z'
TQID: 'https://experienceleague.adobe.com/KoRp--G2sMvv-Hr7KiHriZrFmtEm0BhGoGWVQQK-ofE'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: 8d0b446f-5b16-5a10-b272-01143504a11c
    internal-label: System
  - id: d3b92bef-63fa-5031-a925-d04d9362d616
    internal-label: Saas
source-git-commit: 71df9ad673f2e7dff802e4b26d8e169c42d9c063
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 1%
---

# Los límites y limitaciones de los servicios de comercialización con el modelo de datos de catálogo maquetable (CCDM)

Adobe Commerce Merchandising Services con CCDM aplica límites de licencia y de sistema que definen la capacidad que puede utilizar su proyecto:

- **Límites de licencias**: según la capacidad que haya adquirido; se puede ampliar comprando paquetes adicionales.
- **Límites del sistema**: límites fijos que protegen los recursos del sistema y garantizan un rendimiento confiable para todos los usuarios.

Su uso debe permanecer dentro de estos límites. Excederlos puede causar un aumento de la latencia y la limitación de solicitudes.

## Solicitar capacidad adicional

Los límites de licencia se pueden aumentar comprando los paquetes de licencia descritos en la sección [Límites de licencia y límites del sistema](#license-limits-and-system-boundaries), o negociando licencias personalizadas para casos de uso únicos. Póngase en contacto con su representante de cuentas de Adobe para hablar sobre sus necesidades.

Si tiene alguna pregunta sobre los límites del sistema, comuníquese con la [atención al cliente de Adobe](https://experienceleague.adobe.com/home?lang=en#support).

## Evitar problemas de rendimiento

Siga estas prácticas recomendadas para mantenerse dentro de los límites y evitar problemas operativos:

- **Revisa tus límites**: comprende tus [límites de capacidad](#license-limits-and-system-boundaries) antes de lanzar nuevas tiendas o campañas.
- **Rastree su uso**: use paneles de métricas integrados o registros de CDN.

## Límites de licencias y límites del sistema

En las tablas siguientes se resumen los límites de licencia y de sistema por área de capacidad e incluyen información sobre cómo agregar licencias adicionales para ampliar la capacidad cuando corresponda.


### Catálogo

| **Capacidad** | **Descripción** | **Asignación base** | **Ampliable?** |
| --- | --- | --- | --- |
| Tasa de ingesta de productos | El número de productos creados o actualizados | 1K actualizaciones por minuto<p>Un máximo de 100 000 actualizaciones al día</p> | Sí<p>Agregar un paquete de licencias:</p><ul><li>Actualizaciones de 5K por minuto<br>Un máximo de 500K actualizaciones por día</li> <li>10 000 actualizaciones por minuto<br>Un máximo de 1 millón de actualizaciones por día</li></ul><p>La capacidad máxima de ingesta de datos es de 1 millón de actualizaciones al día.</p> |
| Tamaño de carga útil del producto | Cantidad máxima de datos permitida al crear, actualizar o ingerir información de producto mediante la API | 200 KB | No |
| Variaciones de catálogo | El número de vistas de un catálogo disponibles para los usuarios de tienda,<p>que se cuentan como (*Número de vistas del catálogo × Número de libros de precios*)</p> | 100 variaciones | Sí<p>Agregar paquete de licencias de 100 variaciones de catálogo</p> |
| Productos en un único origen de catálogo | SKU admitidas en el catálogo | SKU de 250.000 | Sí<p>Añadir paquete de licencias de SKU a 100.000</p> |
| Variantes por producto | Número de variantes de producto (tamaño, combinaciones de colores) permitidas por producto | 10K | No |
| Fuentes de catálogo | El número de contextos de datos de catálogo (por ejemplo, configuraciones regionales o fuentes de datos como PIM y ERP) | 50 | No |

{style="table-layout:auto"}

### Libros de precios

| **Capacidad** | **Descripción** | **Asignación base** | **Ampliable?** |
| --- | --- | --- | --- |
| Libros de precios | Número de libros de precios permitidos por instancia | Según la cantidad de [variaciones de catálogo](#catalog) | Sí<br>Aumentar las variaciones del catálogo |
| Descuentos por registro de precios | El número de descuentos que se pueden aplicar a un precio de producto dentro de un único libro de precios | 10 | No |

{style="table-layout:auto"}

### Vistas de catálogo y políticas

| **Capacidad** | **Descripción** | **Asignación base** | **Ampliable?** |
| --- | --- | --- | --- |
| Vistas de catálogo | Número de subconjuntos configurables del catálogo maestro | Según la cantidad de [variaciones de catálogo](#catalog) | Sí<br>Aumentar las variaciones del catálogo |
| Políticas por vista de catálogo | Número de filtros de datos permitidos | 10 | No |
| Valores de atributo en una directiva | Número de características del producto que se pueden configurar para el filtrado | 100 | No |
| [Asignación restringida de clave de acceso](setup/private-catalog-view.md) | Número de claves de acceso restringido que se pueden asignar a una sola vista de catálogo | 3 | No |
| Tamaño de clave RSA (claves de acceso restringido) | Se acepta la seguridad mínima y máxima de una clave de acceso restringido. | Mínimo de 2048 bits, máximo de 8192 bits | No |
| Claves de acceso restringido | Retraso de propagación de revocación de claves | Hasta 5 minutos debido al almacenamiento en caché. Los tokens firmados con una clave eliminada se deniegan una vez transcurrido el tiempo de espera. | No aplicable |

{style="table-layout:auto"}

### Tienda de catálogo

La asignación base para las capacidades de tienda de catálogo se determina en función del nivel GMV (valor bruto de mercancía). La tabla indica la asignación mínima para cada capacidad.

| **Capacidad** | **Descripción** | **Asignación base** | **Ampliable?** |
| --- | --- | --- | --- |
| Tasa de recuperación del catálogo | Número de veces que un sistema (tienda, sistema de transacciones, ERP u otro) llama mensualmente a una API de catálogo para recuperar datos del catálogo | Basado en el nivel de GMV<p>Asignación mínima: 10M/mes</p> | Sí<p>Agregar un millón de solicitudes al mes en paquetes de licencias</p> |
| Solicitudes de contenido | Solicitudes a la tienda para vistas de página de HTML o llamadas a la API JSON. Se cuenta como 1 vista de página o 5 llamadas a la API. | Basado en el nivel de GMV<p>Asignación mínima: 2M/mes</p> | Sí<p>Añadir un paquete de licencias de 1 millón al mes</p> |
| Variaciones GenAI de Storefront | Asignación para la generación de contenido basado en texto | Basado en el nivel de GMV<p>Asignación mínima: 1K variaciones/mes</p> | Sí<p>Compre créditos de IA generativos por separado</p> |

{style="table-layout:auto"}

>[!NOTE]
>
>La generación de imágenes requiere una licencia de [!DNL Adobe Firefly] aprovisionada para la misma organización de IMS que [!DNL Adobe Commerce Optimizer].


### Descubrimiento de productos

Los límites siguientes se aplican a la configuración de búsqueda de productos, listados y comercialización de tiendas.

| **Capacidad** | **Descripción** | **Asignación base** | **Ampliable?** |
| --- | --- | --- | --- |
| Recuperación de productos | Número máximo de SKU por solicitud de GraphQL de [!DNL Catalog Service] al recuperar datos de productos con `products`, `productSearch`, `refineProduct` y `variants`. Dividir solicitudes más grandes en varias llamadas. | 100 | No |
| Atributos filtrables | El número de características del producto (como color, tamaño, marca o material) que se pueden habilitar para la navegación por capas y las facetas | 200 | No |
| Atributos de búsqueda | El número de características del producto que se pueden indexar para la búsqueda en el catálogo | 200 | No |
| Atributos ordenables | El número de características del producto disponibles como opciones de ordenación en las páginas de búsqueda y categoría. | 50 | No |
| Profundidad de paginación de búsqueda | Máximo de productos accesibles a través de la paginación de búsqueda (por ejemplo, página 100 × 100 productos/página) | 10K | No |
| Facetas | El número de atributos de producto filtrables (como marca, color, tamaño y precio) que se pueden configurar para ayudar a los compradores a refinar los resultados de búsqueda y examinar las categorías | 100<p>Deben ser atributos filtrables</p> | No |
| Opciones por faceta | El número de valores de atributos de producto filtrables que los compradores pueden seleccionar dentro de una faceta (por ejemplo, &quot;Rojo&quot;, &quot;Azul&quot; para Color; &quot;Pequeño&quot;, &quot;Medium&quot; para Tamaño) | 100 | Sí<p>Puede aumentar mediante una solicitud de asistencia</p> |

{style="table-layout:auto"}

### Recommendations

Las siguientes funciones están disponibles para recomendaciones de productos. Algunas características disponibles en otros productos de Adobe Commerce no son compatibles con [!DNL Adobe Commerce Optimizer].

| **Capacidad** | **Descripción** | **Asignación base** | **Ampliable?** |
| --- | --- | --- | --- |
| Unidades de recomendación activas | Número de componentes de recomendaciones activas en la tienda (como &quot;Los clientes también vieron&quot; o &quot;Es posible que también te guste&quot;) | 50 | No |
| Inclusiones/exclusiones de categorías o atributos | Filtre los productos a un conjunto específico que cumpla los requisitos para las recomendaciones | No compatible | — |

{style="table-layout:auto"}
