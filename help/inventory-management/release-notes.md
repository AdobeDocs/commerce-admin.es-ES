---
title: '[!DNL Inventory Management] notas de la versión'
description: Revise las notas de la versión para obtener información acerca de todas las  [!DNL Inventory Management] versiones.
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: fdc14758788fa5cd0391371ebfafb478dadec8a4
workflow-type: tm+mt
source-wordcount: '3462'
ht-degree: 0%

---

# [!DNL Inventory Management] notas de la versión

Estas notas de la versión describen las versiones de [!DNL Inventory Management] e incluyen:

![Nuevas](../assets/new.svg) nuevas características
![Se ha corregido un problema](../assets/fix.svg) Correcciones y mejoras
![Problema conocido](../assets/bug.svg) Problemas conocidos

[!DNL Inventory Management] es un proyecto especial de ingeniería de la comunidad de Magento Open Source abierto a los colaboradores. Para participar y contribuir, consulta el repositorio [GitHub project](https://github.com/magento/inventory) y la [wiki](https://github.com/magento/inventory/wiki) para comenzar. Para discutir el proyecto, únete al canal [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) ([suscripción automática](https://opensource.magento.com/slack)).

[Programación de versiones](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html?lang=es){target="_blank"} para versiones compatibles.

## Versión 1.2.7

Las notas de la versión 1.2.7 de [!DNL Inventory Management] se incluyen en las [notas de la versión core 2.4.7](https://experienceleague.adobe.com/es/docs/commerce-operations/release/notes/adobe-commerce/2-4-7#inventory-management-1).

## Versión 1.2.6

[!DNL Inventory Management] 1.2.6 (versión de módulo: `magento/inventory-metapackage = 1.2.6`) es compatible con la versión 2.4.6 y con la versión 2.4.0 de Adobe Commerce, Adobe Commerce en la infraestructura de la nube y Magento Open Source code base.

![Problema corregido](../assets/fix.svg) La tienda ahora muestra productos compuestos (configurables, agrupados y agrupados) como en stock cuando los productos secundarios que se habían agotado se devuelven al stock. Anteriormente, la tienda indicaba que el producto compuesto estaba agotado en estas condiciones. <!-- ACP2E-1106-->

![Se ha corregido un problema](../assets/fix.svg). Ahora las opciones de productos configurables se muestran según lo esperado, ya que no hay existencias en la tienda si la opción se creó con la cantidad establecida en 0 y **[!UICONTROL Display out-of-stock products]** está habilitado. <!-- ACP2E-1148-->

![Se ha corregido un problema](../assets/fix.svg). Las cachés de la página Categoría ya no se invalidan cuando cambia la cantidad de existencias y el producto aún está en existencias. Adobe Commerce ahora carga las páginas de la caché en lugar de regenerarlas cuando cambia la cantidad de productos (y nada más) en la página de la categoría de la tienda. <!-- ACP2E-118-->

![Problema corregido](../assets/fix.svg): el recuento de productos de la lista de categorías ahora es correcto al usar Inventario en modo de origen único con la configuración **[!UICONTROL Display Out-Of-Stock Products]** habilitada. Adobe Commerce ahora comprueba si un producto se puede vender durante el recuento. <!-- ACP2E-1033-->

![Problema corregido](../assets/fix.svg) Las reglas de precio del carro de compras para la entrega en tienda ahora funcionan según lo esperado cuando el inventario está habilitado. Anteriormente, los descuentos generados por reglas de precios de carro de compras no se aplicaban en estas condiciones. <!-- ACP2E-1015-->

![Se ha corregido un problema](../assets/fix.svg). Al actualizar el inventario de productos en modo programado, ya no se borran todas las cachés. Anteriormente, el indexador de inventario borraba todas las cachés de configuración. <!-- ACP2E-1003-->

![Problema corregido](../assets/fix.svg) El valor del atributo **[!UICONTROL Allow Multiple Boxes for Shipping]** de un producto en el inventario avanzado ahora se guarda según lo esperado. <!-- ACP2E-992-->

![Problema solucionado](../assets/fix.svg) Adobe Commerce ahora emite una compensación de reserva precisa después de un abono de reembolso parcial por un pedido realizado con recogida en tienda. Anteriormente, se guardaba una reserva incorrecta en la tabla `inventory_reservation` cuando un usuario administrador creaba un abono sin seleccionar la casilla de verificación **[!UICONTROL Return to Stock]**. <!-- ACP2E-979-->

![Se ha corregido un problema](../assets/fix.svg) por el que Adobe Commerce ya no muestra los productos configurables como agotados en la tienda cuando una de sus variaciones se ha devuelto manualmente para que esté disponible en las implementaciones que implementan el inventario de varios orígenes. <!-- ACP2E-952-->

![Se ha corregido un problema](../assets/fix.svg) La posición de la columna en la cuadrícula del producto (**[!UICONTROL Catalog]** > **[!UICONTROL Products]**) ya no vuelve a su posición anterior después de que la página se vuelva a cargar en implementaciones con varios orígenes de inventario configurados. <!-- ACP2E-925-->

![Problema corregido](../assets/fix.svg) La cantidad de existencias ahora es correcta después de que se emita un abono para un producto virtual cuando la casilla de verificación **[!UICONTROL Back to stock]** no está seleccionada. <!-- ACP2E-908-->

![Problema corregido](../assets/fix.svg) Ahora puede guardar categorías con la ordenación automática de productos y el ámbito asignado a existencias no predeterminadas. Anteriormente, Adobe Commerce no guardaba la categoría y mostraba este error: `Something went wrong while saving the category`. <!-- ACP2E-859-->

![Se ha corregido un problema](../assets/fix.svg). El estado de existencias de productos configurables ahora se actualiza según lo esperado cuando el producto se crea con todas las variaciones configurables sin existencias. <!-- ACP2E-813-->

![Problema corregido](../assets/fix.svg): la herramienta Analizador de incoherencia de reservas ahora funciona correctamente con pedidos enviados parcialmente que contienen productos configurables, agrupados y agrupados. Ahora se analizan los tipos de productos compuestos. Anteriormente, las cancelaciones y los reembolsos se guardaban solo para los productos principales, no para los artículos de pedidos de subproductos de paquetes configurables y agrupados de envío. <!-- ACP2E-924-->

![Se ha corregido un problema](../assets/fix.svg) Adobe Commerce ya no muestra un error cuando un usuario administrador intenta asignar 200 o más orígenes de inventario a un inventario o producto. <!-- ACP2E-1180-->

![Problema corregido](../assets/fix.svg) Adobe Commerce ahora admite la creación de un abono para un pedido del que se ha eliminado un producto. Anteriormente, los comerciantes no podían crear una nota de abono cuando los productos se habían eliminado del pedido después de crearse una factura. La aplicación mostró este error: `Following products with requested skus were not found: s00001`. t. <!-- ACP2E-1138-->

![Problema solucionado](../assets/fix.svg) Las tiendas ahora se filtran según los ID de una o varias tiendas. El código de atributo de producto `event` se ha agregado a la lista de códigos de atributo reservados. Anteriormente, el informe Bajo stock arrojaba una excepción cuando se instalaba el módulo Inventario. <!-- ACP2E-1017-->

![Se ha corregido un problema](../assets/fix.svg) Los filtros de navegación por capas ahora funcionan según lo esperado y los productos sin existencias ahora se anexan a la lista de productos de la categoría de tienda. El nuevo atributo de ordenación `is_out_of_stock` usa el asignador de campos dinámicos de Elasticsearch para la colección de productos de la tienda. <!-- ACP2E-748-->

![Se corrigió el problema](../assets/fix.svg) El estado de las existencias del producto compuesto (paquete, agrupado y configurable) se actualiza como se espera cuando el estado de las existencias del producto secundario se cambia mediante una llamada de REST `POST /rest/V1/inventory/source-items`. <!-- ACP2E-1209-->

## Versión 1.2.5

[!DNL Inventory Management] 1.2.5 (versión de módulo: `magento/inventory-metapackage = 1.2.5`) es compatible con la versión 2.4.5 y con la versión 2.4.0 de Adobe Commerce, Adobe Commerce en la infraestructura de la nube y Magento Open Source code base.

![Problema corregido](../assets/fix.svg) El estado de inventario predeterminado de existencias del paquete y los productos agrupados ahora se actualiza según lo esperado cuando un comerciante crea un envío desde el administrador. Anteriormente, el estado de estos productos permanecía sin cambios después de que se creara un envío. <!--- ACP2E-418-->

![Se ha solucionado un problema](../assets/fix.svg) Los productos configurables vuelven a estar en existencias cuando se cumple una de las siguientes condiciones: 1. El producto principal tiene al menos un elemento secundario guardado en stock. 2. El producto configurable en sí se actualizó y se estableció como **en stock** y tenía al menos un producto secundario en stock. <!--- ACP2E-443-->

![Se ha corregido un problema](../assets/fix.svg) Los cambios de inventario implementados a través de la API de REST ahora se reflejan según lo esperado en las páginas de detalles del producto. La caché de los productos del catálogo ahora se limpia después de comparar los estados de stock último y actual. Anteriormente, omitir la función de llamada de retorno provocaba una evaluación incorrecta de los cambios de estado de las existencias, que no limpiaban la déclencheur necesaria. Como resultado, la tienda no reflejaba los cambios del inventario. <!--- ACP2E-161-->

![Se ha corregido un problema](../assets/fix.svg) Los productos que están asignados a existencias predeterminadas y que anteriormente estaban sin existencias ahora están visibles en la tienda después de que el elemento de origen se actualice mediante `/V1/inventory/source-items`. Anteriormente, este extremo de API de REST establecía el `stock_status` incorrecto. <!--- ACP2E-562-->

![Se ha corregido un problema](../assets/fix.svg) La anulación de la asignación de orígenes de inventario mediante una acción en masa (**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**) ahora funciona según lo esperado cuando los orígenes incluyen SKU duplicadas excepto un cero a la izquierda (por ejemplo, `01234` y `1234`). Anteriormente, la aplicación no quitaba la asignación de orígenes de inventario y generaba un error. <!--- ACP2E-2641-->

![Problema corregido](../assets/fix.svg) El estado de existencias del producto ahora siempre está **en existencias** en la tienda cuando se habilitan infinitos pedidos no satisfechos y el producto se asigna a un inventario personalizado, independientemente de la cantidad no satisfecha. Anteriormente, los productos no estaban disponibles incluso cuando se habilitaban los pedidos pendientes. <!--- ACP2E-664-->

![Se ha corregido un problema](../assets/fix.svg). El stock de productos principal y secundario configurables ahora se actualiza correctamente después de que el elemento de origen se actualice con `POST /V1/inventory/source-items`. Una vez que el producto secundario se actualiza a través de la API, un nuevo complemento de inventario para comprobaciones de existencias predeterminadas y actualiza la cantidad y el estado configurables del producto. <!--- ACP2E-442-->

![Se ha corregido un problema](../assets/fix.svg) Los productos agrupados que no están disponibles ya no aparecen en la página Categoría de la tienda. <!--- ACP2E-2082-->

![Se ha corregido un problema](../assets/fix.svg) que corregía el nombre del paquete en `CatalogInventory` `composer.json`. <!--- ACP2E-2914-->

![Se ha corregido un problema](../assets/fix.svg) El estado de pedidos pendientes ahora se representa correctamente en el administrador después de realizar un pedido con una cantidad cero de productos en una implementación de varias fuentes/existencias. [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![Se ha corregido un problema](../assets/fix.svg) Los productos del paquete sin existencias ya no se muestran en la página Categoría de tienda cuando se actualiza el producto del paquete desde la sección de existencias. <!--- ACP2E-2012-->

![Se ha corregido un problema](../assets/fix.svg). Se han resuelto los problemas de compatibilidad con PHP 7.4. <!--- AC-3192-->

![Problema corregido](../assets/fix.svg) Se ha mejorado el rendimiento de las operaciones de guardado que incluyen productos agrupados que contienen muchas opciones (varias 100). Anteriormente, el guardado de estos productos de paquete grande tardaba varios minutos y, a veces, resultaba en tiempos de espera en implementaciones con los servicios de inventario habilitados. [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![Problema corregido](../assets/fix.svg) La herramienta de acción masiva de productos (**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**) ahora funciona como se espera al asignar un origen de inventario a varios productos cuando se duplican SKU, excepto para `0` (por ejemplo, `01234` y `1234`). Anteriormente, solo se asignaba un producto a un origen de inventario. [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![Problema corregido](../assets/fix.svg) El campo `ProductInterface.only_x_left_in_stock` ahora devuelve 0 si el inventario es 0. Anteriormente, devolvía nulo. [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![Problema corregido](../assets/fix.svg) Ahora puede editar las existencias predeterminadas desde el Administrador **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**. Anteriormente, se mostraba un error de JavaScript en la consola al intentar añadir o eliminar orígenes de existencias predeterminadas, aunque se podían asignar sitios web a existencias predeterminadas. <!--- ACP2E-545-->

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-274-->: el recuento de productos de la lista de categorías ahora es correcto al usar el modo de un solo origen de inventario con la configuración **[!UICONTROL Display Out-Of-Stock Products]** habilitada. Un nuevo complemento ahora usa `AreProductsSalableInterface` y `StockConfigurationInterface` para determinar la cantidad total de productos. Anteriormente, la lista de productos de categorías devolvía una cantidad de productos incorrecta.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-322--> Los productos configurables ahora se mueven a la última posición de la lista de productos después de que se hayan actualizado las existencias cuando la configuración de **[!UICONTROL Move out of stock to the bottom]** esté habilitada. Se implementa una nueva consulta de base de datos personalizada para negar el orden de clasificación de índices de Elasticsearch, que ignora el orden de clasificación habilitado por el administrador. Anteriormente, los productos configurables y sus productos secundarios no se movían al final de la lista cuando esta configuración estaba habilitada.

## Versión 1.2.4

Inventory management 1.2.4 (versión de módulo: `magento/inventory-metapackage = 1.2.4`) es compatible con la versión 2.4.4 y con la versión 2.4.0 de Adobe Commerce, Adobe Commerce en la infraestructura de la nube y Magento Open Source code base.

![Problema corregido](../assets/fix.svg) Commerce ahora muestra un valor de cantidad vendible preciso para todos los productos en la vista de lista de productos de administración. Anteriormente, mostraba un valor en blanco para la cantidad vendible de productos en existencia con SKU que contenían caracteres especiales. <!--- MC-41936-->

![Se ha corregido un problema](../assets/fix.svg). El rendimiento ha mejorado para las acciones de carro de compras y cierre de compra, como agregar productos al carro de compras en implementaciones con muchos (aproximadamente 10.000) orígenes de inventario. <!--- MC-42570-->

![Se ha corregido un problema](../assets/fix.svg) [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."} El comando `bin/magento inventory:reservation:list-inconsistencies` ahora gestiona correctamente los pedidos con envíos parciales incluso si se omiten las reservas de la base de datos y se ha borrado la caché. Anteriormente, cuando este comando se ejecutaba con una memoria caché previamente borrada, Commerce mostraba el siguiente error: `Area code is not set`. <!--- MC-42142-->


![Se ha corregido un problema](../assets/fix.svg) La indexación incremental de productos secundarios agrupados ya no hace que otros productos agrupados se indexen incorrectamente cuando se comparten productos secundarios. <!--- MC-41963-->

![Problema corregido](../assets/fix.svg): la página de categoría de tienda ahora muestra el recuento de productos correcto después de quitar un producto de una categoría mediante API. Anteriormente, el recuento de productos de la página de categorías era incorrecto hasta que se produjo la reindexación. <!--- MC-42287-->

![Se ha corregido un problema](../assets/fix.svg). Ahora se pueden devolver los productos configurables a las existencias al crear una nota de crédito si la opción **[!UICONTROL Manage Stock]** está deshabilitada. Anteriormente, Commerce no mostraba la casilla de verificación **Volver a stock** en la página de creación de nota de abono cuando se deshabilitó esta opción. <!--- MC-42002-->

![Se ha corregido un problema](../assets/fix.svg) Se ha mejorado la administración de existencias de inventario que supera los 10.000 elementos. Anteriormente, los problemas de rendimiento a veces impedían que los comerciantes editaran las existencias en el Admin antes de lanzar su sitio web. <!--- MC-42643-->

![Se ha corregido un problema](../assets/fix.svg): la página **[!UICONTROL User Roles]** del Administrador se ha actualizado para proporcionar a los administradores permisos restringidos para acceder a la configuración de los métodos de envío. Se cambió el nombre de la sección _Métodos de envío_ a _[!UICONTROL Delivery methods]_&#x200B;y se movió&#x200B;_[!UICONTROL In-Store Pickup]_ a la sección _[!UICONTROL Delivery methods]_. [GitHub-30053](https://github.com/magento/magento2/issues/30053) <!--- MC-41545-->

![Se ha corregido un problema](../assets/fix.svg) por el que Adobe Commerce ya no crea una reserva de producto duplicada después de que la API actualice un abono. <!--- MC-41757-->

![Se ha corregido un problema](../assets/fix.svg) El cambio de la pestaña _[!UICONTROL Pick up in Store]_&#x200B;a la pestaña&#x200B;_[!UICONTROL Shipping]_ en el flujo de trabajo de cierre de compra ya no genera un déclencheur de error de JavaScript cuando solo está disponible la entrega de recogida en la tienda. <!--- MC-42808-->

![Problema corregido](../assets/fix.svg): la cantidad de productos vendibles y la cantidad de productos en existencias ahora se sincronizan correctamente. Anteriormente, la compensación de reserva de inventario no se volvía a crear para pedidos cancelados. <!--- MC-42485-->

![Se ha corregido un problema](../assets/fix.svg). El rendimiento del validador está optimizado para evitar que se agregue una nueva fuente al producto secundario de un producto agrupado con el tipo de envío `Ship Together`. <!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3 (versión de módulo: `magento/inventory-metapackage = 1.2.3`) es compatible con la versión 2.4.3 y con la versión 2.4.0 de Adobe Commerce, Adobe Commerce en la infraestructura de la nube y Magento Open Source code base.

![Se ha corregido un problema](../assets/fix.svg) Se han corregido varios problemas relacionados con la visibilidad del producto compuesto en el front-end.

![Se corrigió un problema](../assets/fix.svg) Se mejoró el rendimiento de la administración de páginas del carro de compras con la cantidad mínima requerida.

![Se ha corregido un problema](../assets/fix.svg) Varias correcciones destinadas a resolver problemas con la creación de orígenes, artículos sin existencias, abastecimiento de existencias, ordenación de orígenes asignados, envío en tienda y comandos de inventario.

![Problema corregido](../assets/fix.svg) [!DNL Commerce] ahora admite códigos postales canadienses de tres dígitos para la entrega en tienda. Los códigos de seis dígitos no son compatibles debido a las limitaciones establecidas por `geonames.org`.

![Se ha corregido un problema](../assets/fix.svg). El administrador ahora muestra la cantidad correcta de existencias predeterminadas para los productos deshabilitados en la cuadrícula de **Productos** y en la página **Editar producto** para las implementaciones de varias tiendas.

![Se ha corregido un problema](../assets/fix.svg) [!DNL Commerce] que ahora actualiza la caché de productos de la categoría cuando un producto del paquete vuelve a estar disponible.

## 1.2.2

[!DNL Inventory Management] 1.2.2 (versión de módulo: `magento/inventory-metapackage = 1.2.2`) es compatible con la versión 2.4.2 y con la versión 2.4.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y Magento Open Source code base.

![Se ha corregido un problema](../assets/fix.svg) Se han corregido varios problemas relacionados con la visibilidad del producto compuesto en el front-end.

![Se corrigió un problema](../assets/fix.svg): se mejoró el rendimiento de la página del carro de compras durante la actualización de la cantidad en B2B.

![Se ha corregido un problema](../assets/fix.svg) Varias correcciones destinadas a resolver problemas con la recogida en la tienda, las actualizaciones masivas y el umbral de inventario.

![Nuevas](../assets/new.svg) **pruebas funcionales.** introdujo nuevas pruebas funcionales y proporcionó correcciones para las pruebas existentes a fin de hacerlas más estables.

## 1.2.1

[!DNL Inventory Management] 1.2.1 (versión de módulo: `magento/inventory-metapackage = 1.2.1`) es compatible con la versión 2.4.1 y con la versión 2.4.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y Magento Open Source code base.

![Se ha corregido un problema](../assets/fix.svg) Se ha corregido un problema conocido relacionado con el trabajo cron de `inventory_cleanup_reservations` y se ha solucionado un problema relacionado con la funcionalidad de recogida en tienda para los productos agrupados. Esta actualización también incluye mejoras generales en el cálculo de existencias, compatibilidad con paquetes de productos y funcionalidad de pedidos pendientes.

![Nuevas](../assets/new.svg) **pruebas funcionales.** ha introducido nuevas pruebas funcionales para proporcionar una cobertura adicional de la funcionalidad de recogida en tienda.

## 1.2.0

[!DNL Inventory Management] 1.2.0 (versión de módulo: `magento/inventory-metapackage = 1.2.0`) es compatible con la versión 2.4.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y Magento Open Source code base.

![Se ha solucionado un problema](../assets/fix.svg) con numerosas correcciones para resolver problemas con la asignación de fuentes, compatibilidad con funciones de entorno escalable y compatibilidad con PHP 7.4, MySQL 8 y PHPUNIT 9.

![Nuevo](../assets/new.svg) **método de envío en tienda.** agregó una opción para que los usuarios seleccionen un origen para utilizarlo como ubicación de recogida durante el cierre de compra. Consulte [Envío en tienda](../stores-purchase/shipping-in-store-delivery.md) en la _Guía de ventas y compras_.

![Nuevo](../assets/new.svg) **Paquete de soporte técnico para el modo multiorigen.** El inventario admite todos los tipos de productos con múltiples orígenes.

![Nueva](../assets/new.svg) **reindexación asíncrona de existencias.** agregó la capacidad de reindexar de manera asincrónica las existencias y mejoró el rendimiento de varios escenarios críticos.

![Nuevas](../assets/new.svg) **interfaces masivas.** introdujo nuevas interfaces masivas para la comprobación de ventas: `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`, `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![Nuevo](../assets/new.svg) **Aumento en la cobertura de pruebas.** La nueva funcionalidad está cubierta por pruebas automatizadas, incluida la cobertura extendida para problemas detectados y corregidos.

![Problema conocido](../assets/bug.svg) **Problema conocido.**: la ausencia del campo `object_id` en los metadatos de las reservas impide que el trabajo cron de `inventory_cleanup_reservations` funcione correctamente. Este problema se presentó en [magento/inventory#3046](https://github.com/magento/inventory/pull/3046).

**Solución alternativa:** Ejecute las siguientes consultas MySQL para limpiar manualmente las reservas:

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6

[!DNL Inventory Management] 1.1.6 (versión de módulo: `inventory-composer-metapackage = 1.1.6`) es compatible con la versión 2.3.6 y con las versiones 2.3.5, 2.3.4, 2.3.3, 2.3.2, 2.3.1 y 2.3.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y Magento Open Source code base.

![Se corrigió el problema](../assets/fix.svg) Se solucionaron los problemas relacionados con pedidos pendientes, notas de crédito, cuadrícula de informes de existencias bajas, correcciones relacionadas con la herramienta CLI &quot;resolver incoherencias&quot; y mejoras generales.

![Nueva](../assets/new.svg) **reindexación asíncrona de existencias.** agregó la capacidad de reindexar de manera asincrónica las existencias y mejoró el rendimiento de varios escenarios críticos.

## 1.1.5

[!DNL Inventory Management] 1.1.5 (versión de módulo: `inventory-composer-metapackage = 1.1.5`) es compatible con la versión 2.3.5 y con las versiones 2.3.4, 2.3.3, 2.3.2, 2.3.1 y 2.3.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y Magento Open Source code base.

![Nuevo](../assets/new.svg) **Actualizar inventario una vez que se cambie la SKU del producto.** introdujo un nuevo ajuste de configuración para cambiar al nuevo comportamiento: &quot;Sincronizar con el catálogo&quot;.

![Nuevas](../assets/new.svg) **pruebas funcionales.** introdujo nuevas pruebas funcionales para eliminar el intervalo de cobertura de prueba. Se han corregido varios problemas para que las pruebas fueran más estables y fiables).

![Problema conocido](../assets/bug.svg) Correcciones para evitar la sobreventa de productos, visibilidad de productos &quot;Sin existencias&quot; en la tienda, numerosas correcciones para compatibilidad con entornos escalables y mejoras en la interfaz de usuario.

## 1.1.4

[!DNL Inventory Management] 1.1.4 (versión de módulo: `inventory-composer-metapackage = 1.1.4`) es compatible con la versión 2.3.4 y con las versiones 2.3.3, 2.3.2, 2.3.1 y 2.3.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y Magento Open Source code base.

![Se corrigió un problema &#x200B;](../assets/fix.svg)**Mayor rendimiento.** Introdujo la lógica de agrupamiento para el comando CLI de reservas de inventario para reducir el uso de memoria y evitar casos en los que el proceso se atasca sin ninguna respuesta.

![Nuevo &#x200B;](../assets/new.svg)**Aumento en la cobertura de pruebas.** introdujo muchas pruebas funcionales nuevas. Casi todos los casos de inventario manual se tratan con pruebas automatizadas.

![Problema conocido](../assets/bug.svg) Numerosas correcciones destinadas a resolver problemas con notas de crédito, productos agrupados y acciones masivas de origen y existencias.

## 1.1.3

[!DNL Inventory Management] 1.1.3 (versión de módulo: `inventory-composer-metapackage = 1.1.3`) es compatible con la versión 2.3.3 y con las versiones 2.3.2, 2.3.1 y 2.3.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y Magento Open Source code base.

![Se ha corregido un problema &#x200B;](../assets/fix.svg)**Mejor integración con las características de Adobe Commerce y B2B.** [!DNL Inventory Management] ahora funciona correctamente con las siguientes características para sitios web que usan recursos de inventario y existencias no predeterminados:

- Pedido por SKU (Adobe Commerce)
- Pedido rápido (B2B)
- Listas de solicitudes (B2B)

![Nuevo &#x200B;](../assets/new.svg)**Rendimiento mejorado.** El rendimiento de exploración del catálogo de tiendas se ha mejorado en los sitios web que ejecutan el origen y las existencias de inventario predeterminados.

![Nuevo &#x200B;](../assets/new.svg)**Aumento en la cobertura de pruebas.**: la cobertura de pruebas de integración y funciones automatizadas ha aumentado significativamente.

## 1.1.2

[!DNL Inventory Management] 1.1.2 (versión de módulo: `inventory-composer-metapackage = 1.1.2`) es compatible con la versión 2.3.2 y con la versión 2.3.1 y 2.3.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y Magento Open Source code base.

![Se ha corregido un problema](../assets/fix.svg) que agregó a `source_code` a la respuesta del extremo REST `/V1/shipments` de GET. <!-- https://github.com/magento/inventory/pull/2142 -->

![Se ha corregido un problema](../assets/fix.svg) que se ha resuelto para borrar correctamente las reservas y actualizar las cantidades de los productos después de emitir un abono para un pedido no enviado. Al seleccionar la opción para <!-- https://github.com/magento/inventory/pull/2179 -->

![Se ha corregido un problema](../assets/fix.svg). Se ha resuelto un problema para guardar correctamente la cantidad de productos secundarios configurables al introducir cantidades durante la creación del producto. <!-- https://github.com/magento/inventory/pull/2158 -->

Los nuevos módulos de [!DNL Inventory Management] 1.1.2 Beta incluyen:

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![Nuevo](../assets/new.svg) **Se agregó un punto final de transferencia parcial de existencias en lotes**: los puntos finales de transferencia en lotes actuales mueven toda la cantidad asignada de un origen a un origen de destino. El nuevo extremo `/rest/V1/inventory/bulk-partial-source-transfer` permite a los comerciantes transferir existencias parciales del origen al origen como una operación masiva. Para transferir una cantidad específica, escriba una solicitud al extremo con los valores `sku`, `qty`, `origin_source_code` y `destination_source_code`. Las transferencias comprueban que el origen está asignado a `sku`, que existe una cantidad suficiente para transferir, etc. Consulte [Acciones masivas de inventario](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} en la documentación de la API de REST. <!-- https://github.com/magento/inventory/pull/2117 -->

![Nuevo](../assets/new.svg) **CLI de reserva agregado**: los nuevos comandos le ofrecen opciones para detectar y resolver incoherencias en las reservas. A medida que los pedidos se envían y cambian de estado, [!DNL Inventory Management] genera reservas y actualizaciones iniciales mediante reservas de compensación. Estos comandos devuelven una lista de incoherencias detectadas por ID de pedido, SKU e ID de stock, y crean reservas para resolverlas. Consulte la [referencia de CLI](cli.md) para obtener más información. <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![Nuevo](../assets/new.svg) **Mejoras de rendimiento para fuentes y opciones de SSA**: ordenar y seleccionar fuentes durante el envío causó una degradación del rendimiento para las existencias con un alto número de fuentes. Esta versión proporciona mejoras de rendimiento significativas para enumerar y ordenar las fuentes disponibles al revisar y seleccionar las opciones de SSA en los envíos. <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![Nuevo](../assets/new.svg) **Se agregó compatibilidad con GraphQL para Inventory management**. Esta versión instala un nuevo módulo `magento/module-inventory-graph-ql`. Los atributos de GraphQL [ProductInterface](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} ahora incluyen los atributos `only_x_left_in_stock` y `stock_status` para la compatibilidad con [!DNL Inventory Management]. <!-- https://github.com/magento/inventory/pull/2124 -->

![Nueva](../assets/new.svg) **IU simplificada para orígenes asignados**: la tabla Orígenes asignados de las páginas de productos ha simplificado el contenido para facilitar las actualizaciones y aumentar el rendimiento al mostrar muchos orígenes. Todos los orígenes se enumeran por nombre de origen (pase el ratón sobre `source_code`).

![Nuevo](../assets/new.svg) **Servicio de exportación de existencias acumuladas**: esta versión ofrece un nuevo servicio de exportación de existencias acumuladas (conservando las reservas en el sistema) para admitir canales de ventas externos, como Amazon, eBay y anuncios de Google Shopping.  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0 (versión de módulo: `inventory-composer-metapackage = 1.1.0`) es compatible y compatible con la versión 2.3.0 de Adobe Commerce, Adobe Commerce en la infraestructura de la nube y la base de código de Magento Open Source. [!DNL Inventory Management] 1.1.1 solo se presenta como una actualización de nombre de paquete, compatible con la versión 2.3.1 y compatible con la versión 2.3.0 de Adobe Commerce, Adobe Commerce en la infraestructura de la nube y Magento Open Source code base.

![Se ha corregido un problema](../assets/fix.svg) **Se ha agregado compatibilidad con Elasticsearch para los modos de un solo origen y de varios orígenes**. Ahora puede configurar y usar Elasticsearch con existencias personalizadas. Consulte [Configurar el servicio Elasticsearch](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html?lang=es){target="_blank"} para obtener información sobre la instalación. <!-- PR https://github.com/magento/inventory/pull/1943 -->

![Se ha corregido un problema](../assets/fix.svg) que resolvía problemas de rendimiento con Stock predeterminado para aumentar drásticamente el rendimiento con numerosas operaciones. Las mejoras mejoran el rendimiento para el modo de un solo origen, las páginas Transferencia de inventario a Source, Categoría de tienda y Cálculos de cantidad vendible.

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![Se ha solucionado un problema](../assets/fix.svg) que resolvía problemas con el estado Agotado y la transferencia de inventario en bloque a Stock para productos configurables y agrupados. La selección de los productos principales y la realización de acciones masivas no afectan al estado del producto. Si el producto principal estaba En stock, permanece En stock.

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![Nuevo](../assets/new.svg) **Algoritmo de prioridad de distancia**: el algoritmo de prioridad de distancia es un nuevo algoritmo de selección de Source listo para usar para recomendaciones de envío basadas en la distancia. Este algoritmo compara la ubicación de la dirección de destino de envío con las ubicaciones de origen para determinar el origen más cercano para satisfacer los envíos. La distancia puede determinarse por la distancia física o el tiempo que se pasa viajando de un lugar a otro, utilizando datos de ubicación geocodificados importados o indicaciones de Google (conducir, caminar o montar en bicicleta).

![Nueva](../assets/new.svg) **lista de cantidad de origen ampliada**: los comerciantes con un número elevado de orígenes pueden pasar el ratón por encima y ver fácilmente todas las fuentes por producto a través de la cuadrícula de productos. Cada producto muestra un mínimo de cinco fuentes y cantidades coincidentes. Al pasar el ratón por encima de los orígenes, puede desplazarse por toda la lista de orígenes y cantidades actuales.

![Problema conocido](../assets/bug.svg) Problema conocido con Magento Open Source y Adobe Commerce v2.3.1: la migración asincrónica de datos entre orígenes encuentra problemas debido a cambios en las API asincrónicas con nombres de temas que reflejan nombres de clases y métodos de PHP. Se recomienda usar operaciones sincrónicas estableciendo **[!UICONTROL Run asynchronously]** en `No`.
