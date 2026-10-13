---
source-git-commit: bb5da9eea16601303b62ccc06327c6a832062c49
workflow-type: tm+mt
source-wordcount: '1471'
ht-degree: 0%
---
# Problemas corregidos de Adobe Commerce B2B (v1.5.4-alpha1)

## B2B v1.5.4-alpha1

*13 de octubre de 2026*

Se han corregido 23 problemas en el código Adobe Commerce B2B 1.5.4-alpha1. A continuación, se describe un subconjunto de los problemas corregidos que se incluyen en esta versión.

### IU de administración

#### [B2B] Cantidades de productos del paquete no conservadas después de actualizar precios en presupuestos back-end

Se ha corregido un problema en el cual la cantidad de un elemento de paquete en una oferta negociable de administración se revertía a su valor anterior después de editar la cantidad en la cuadrícula después de un cambio de configuración a través del cuadro de diálogo Configurar.

_ACP2E-5005_

### B2B

#### [B2B] página de detalles de presupuesto (tienda y administrador) pierde la información de artículo/producto cuando el producto relacionado se elimina del catálogo

Se ha corregido el problema por el cual los productos no vendibles desaparecían de las cotizaciones negociables finalizadas

_ACP2E-4680_

#### La cantidad de productos agrupados no se ha actualizado correctamente después de enviar la cotización desde el backend

Se ha corregido el problema en el cual las cantidades de opciones de productos del paquete no se actualizaban al reconfigurar una oferta negociable desde el panel de administración. Anteriormente, los cambios realizados en las cantidades de opciones de paquete mediante el botón Configurar se descartaban de forma silenciosa.

_ACP2E-4801_

#### [CLOUD] [B2B] La cuadrícula de Compañías de administración causa una alta consulta MySQL CPU — correlacionó company_type / COUNT

Se ha corregido el problema en el cual la cuadrícula Compañías de administración (Clientes → Compañías) causaba un alto uso de MySQL CPU y sesiones de base de datos de larga duración. Anteriormente, para determinar el Tipo de compañía (principal/secundario/compañía) para cada fila se requería una subconsulta correlacionada con la tabla company_relation que se activaba una vez por fila company, lo que provocaba que las consultas de listado y recuento total fueran O(N²) a escala; la corrección reemplaza esto con una única JOIN preagregada que se ejecuta una vez, independientemente del tamaño del conjunto de datos.

_ACP2E-4846_

#### Pago a cuenta (B2B): falta el botón Editar pedido para los pedidos pendientes mientras está visible para el COD

El botón Editar pedido ahora está disponible para pedidos realizados con Pago a cuenta. Anteriormente no se podía editar un pedido realizado con Pago a cuenta mientras el pedido estaba pendiente

_ACP2E-4877_

#### Tiempo de espera de PHP que ahorra a la empresa B2B con superusuario de varias empresas

Guardar una empresa B2B o cargar la página de superusuario de la empresa en el administrador ya no supera el tiempo máximo de ejecución de PHP cuando el superusuario de la empresa se asigna a un gran número de empresas.

_ACP2E-4967_

#### Las ofertas negociables de [ON-PREM] no se actualizaron según lo esperado

Se ha corregido el problema por el cual las ofertas negociables no se actualizaban cuando se eliminaba un producto presente en una oferta negociable activa.

_ACP2E-5001_

#### Comprobaciones adicionales volátiles de &quot;Pago a cuenta&quot;

Se ha corregido el problema por el cual los clientes individuales (B2C) podían seleccionar Pago a cuenta, un método de pago destinado exclusivamente a los miembros de la compañía B2B, durante el cierre de compra. Anteriormente, a estos clientes se les permitía incorrectamente proceder con el pago a cuenta en lugar de recibir un error de &quot;método de pago no disponible&quot;.

_ACP2E-5013_

#### La acción de guardar del asistente de catálogo compartido borra la estructura de precios de un catálogo compartido

Se ha corregido un problema que se producía cuando la acción de guardar del asistente de catálogo compartido borra la estructura de precios de un guardado de catálogo compartido

_ACP2E-5015_

#### GraphQL customer.role devuelve el &quot;error de servidor interno&quot; para clientes B2C sin compañía

Se ha corregido un problema por el cual al consultar el cliente { role {...} } a través de GraphQL se devolvía un &quot;error interno del servidor&quot; para los clientes B2C no asignados a ninguna compañía. Anteriormente, esta consulta activaba un TypeError de PHP porque se pasaba un ID de empresa nulo a un método con una sugerencia de tipo entero estricta.

_ACP2E-5017_

#### El descuento en artículos de productos del paquete [B2B] no se aplica cuando las cantidades de opciones se actualizan en las ofertas back-end

Se ha corregido un problema en el cual un descuento de nivel de artículo aplicado a un paquete de precios dinámicos en el administrador de ofertas back-end no se reflejaba en el subtotal o subtotal (Excl. Columnas (impuestos) cuando se han actualizado las cantidades de opción del paquete a través del cuadro de diálogo Configurar. Anteriormente, el descuento aparecía en la columna de descuento, pero no reducía el subtotal citado.

_ACP2E-5034_

#### La sección de solicitudes se vuelve a cargar en cada navegación de página

Se ha corregido el problema por el cual la sección de solicitud activaba una recarga de AJAX innecesaria en cada navegación de página de productos y categorías. Anteriormente, la sección se volvía a cargar en cada carga de página para cualquier cliente con datos de lista de solicitudes no vacíos, incluso cuando no se había realizado ningún cambio.

_ACP2E-5037_

#### [Error B2B] cuando faltan datos de región en la dirección de la compañía

Se ha corregido un problema por el cual la página Perfil de compañía y la página Editar cliente de administración mostraban un error cuando se añadía una región a un país en una dirección de empresa después de guardarla sin una región. Ahora, la dirección vuelve correctamente al texto de región almacenado en lugar de provocar un error.

_ACP2E-5092_

#### La actualización de la empresa en el administrador con una configuración regional que no está en inglés restablece el límite de crédito

Se ha corregido un problema en el cual al editar los detalles de una compañía B2B se podía restablecer de forma involuntaria el límite de crédito configurado a 0 cuando la configuración regional del administrador difería de la predeterminada. El límite de crédito ahora se conserva correctamente a menos que se modifique explícitamente.

_ACP2E-5127_

#### [NUBE]: el administrador restringido al sitio web no puede eliminar clientes cuando user_id entra en conflicto con un entity_id de cliente inaccesible

Anteriormente, cuando un administrador restringido a un sitio web intentaba eliminar un cliente, el complemento de comprobación de permisos del sistema comparaba el ID de usuario propio del administrador con
ID de entidad de cliente para aplicar restricciones de jerarquía empresarial, sin comprobar que el usuario que actúa era realmente un cliente; si se produjo el ID de usuario del administrador
para coincidir con el ID de entidad de un cliente no relacionado en un sitio web al que el administrador no podía acceder, el complemento intentó cargar ese registro de cliente inaccesible
y la eliminación falló con el error &quot;se necesitan más permisos&quot;, aunque el administrador tenía derechos válidos para el cliente que se está eliminando. Esto se ha resuelto
al agregar una condición para que la comparación de ID de cliente solo se ejecute cuando el usuario que actúa es realmente un cliente, lo que significa que las eliminaciones iniciadas por el administrador ahora omiten esa comprobación por completo: los administradores restringidos pueden eliminar una vez más a los clientes dentro de sus sitios web asignados sin que los registros de clientes inaccesibles y no relacionados los bloqueen

_ACP2E-5146_

#### El pedido B2B muestra un nombre de compañía incorrecto en los pedidos de ventas de administración

Se ha corregido un problema por el cual se mostraba un nombre de empresa incorrecto para los pedidos de compra B2B en los pedidos de venta de administración cuando se asignaba un usuario a varias empresas.
El nombre de la empresa ahora se muestra correctamente en función de la empresa asociada con el pedido.

_B2B-4656_

### B2B, carro y cierre de compra

#### [EN PREM] [B2B] El cargador de pedidos rápidos se bloquea al intentar cargar un archivo binario que termina en la extensión .CSV

Se ha corregido el problema por el que el cargador de archivos de orden rápida aceptaba cualquier archivo cuyo nombre se hubiera cambiado con la extensión .csv, incluidos los binarios. Anteriormente no se realizaba ninguna validación de contenido o tipo MIME, por lo que los archivos que no eran CSV (por ejemplo, ejecutables) se podían cargar y procesar como si fueran listas SKU/CANT válidas.

_ACP2E-5212_

### B2B, GraphQL

#### Inexactitud de recuento total GQL de lista de solicitudes

Se ha corregido el problema que se producía cuando la consulta de GraphQL reqution_lists devolvía un valor total_count incorrecto que reflejaba únicamente el número de artículos de la página actual en lugar del número total de entidades de lista de solicitudes que coincidían con los criterios de consulta.

_ACP2E-4799_

### B2B, Pedido

#### Ayuda para limpiar más de 59M tablas de presupuesto (sales_clean_quote no se puede ejecutar)

Se corrigió el problema en el cual el trabajo cron de `sales_clean_quotes` agotaba el tiempo de espera en instancias con tablas de comillas grandes. Anteriormente, la consulta de limpieza seleccionaba todas las columnas de la tabla `negotiable_quote` de forma innecesaria, lo que provocaba que MySQL realizara un orden de archivos completo en millones de filas; y cada comilla se eliminaba individualmente a través de la capa del modelo PHP, lo que agravaba el coste de rendimiento.

_ACP2E-4891 - [Contribución de código de GitHub](https://github.com/magento/magento2/commit/b63925d9)_

### B2B, rendimiento

#### [CLOUD] Seguimiento de ACSD-70033 : Bloqueo en la tabla magento_catalogpermissions_index_product. continuación

Anteriormente, la reindexación de permisos de catálogo con Catálogo compartido habilitado podía provocar un error de bloqueo y provocar un error en la reindexación. Ahora, la reindexación se completa correctamente incluso cuando se ejecutan simultáneamente varios procesos de indexación.

_ACP2E-4844_

### Contenido

#### Las páginas de CMS creadas para diferentes sitios web muestran páginas incorrectas en front-end

Anteriormente, en configuraciones de varios sitios web en las que la clave de caché de la página de aterrizaje Restricción del sitio web no tenía ámbito por sitio web, lo que provocaba que se mostrara una página CMS incorrecta en la tienda del sitio web secundario. La clave de caché de WebsiteRestriction/Controller/Index/Stub.php ahora incluye correctamente el ID del sitio web actual resuelto mediante el administrador de tiendas.

_ACP2E-4593_

### Marco

#### [B2B] Los pedidos de compra no se convierten automáticamente en pedidos de venta con ActiveMQ

Se ha corregido un problema en el cual los consumidores iniciados por cron no procesaban mensajes cuando se utilizaba ActiveMQ con el protocolo STOMP. Como resultado, los pedidos de compra aprobados automáticamente no se convirtieron en pedidos de venta. El procesamiento de mensajes para colas STOMP es ahora más fiable y coherente con las implementaciones de colas DB y AMQP.

_ACP2E-4349 - [Contribución de código de GitHub](https://github.com/magento/magento2/commit/08b91f1a) - [Contribución de código de GitHub](https://github.com/magento/inventory/commit/239464da)_

### Instalar y administrar

#### [Corrección en la nube] de códigos de subdivisión ISO existentes obsoletos

Se han actualizado los códigos de región de 13 países para que coincidan con la norma ISO 3166-2. Anteriormente, algunos códigos de región no coincidían con el estándar, lo que podría causar problemas con integraciones de terceros y cumplimiento internacional. Se han añadido nuevas regiones para Bélgica, Colombia, España, Francia, Italia y Letonia. Códigos de región actualizados para Austria, Colombia, Costa Rica, Alemania, Estonia, España, Finlandia, Francia, India, Islandia y Letonia.

_ACP2E-4495 - [Contribución de código de GitHub](https://github.com/magento/magento2/commit/9b6a8bd9)_
