---
title: '[!DNL Inventory Management] notas de la versión'
description: Revise las notas de la versión para obtener información acerca de todos los [!DNL Inventory Management] versiones.
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: 01d8a1d50f574330f3ce7e8bf03a018f0079f5db
workflow-type: tm+mt
source-wordcount: '3445'
ht-degree: 0%

---

# [!DNL Inventory Management] notas de la versión

Estas notas de la versión describen las versiones de [!DNL Inventory Management] e incluir:

![Nuevo](../assets/new.svg) Nuevas funciones
![Problema corregido](../assets/fix.svg) Correcciones y mejoras
![Problema conocido](../assets/bug.svg) Problemas conocidos

[!DNL Inventory Management] es un proyecto especial de Ingeniería Comunitaria Magento Open Source abierto a colaboradores. Para participar y contribuir, consulte la [Proyecto de GitHub](https://github.com/magento/inventory) repositorio y [wiki](https://github.com/magento/inventory/wiki) para empezar. Para discutir el proyecto, únase al [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) canal ([suscripción automática](https://opensource.magento.com/slack)).

[Programación de versiones](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html){target="_blank"} para versiones compatibles.

## Versión 1.2.7

[!DNL Inventory Management] Las notas de la versión 1.2.7 de se incluyen en la [notas de la versión de core 2.4.7](https://experienceleague.adobe.com/en/docs/commerce-operations/release/notes/adobe-commerce/2-4-7#inventory-management-1).

## Versión 1.2.6

[!DNL Inventory Management] 1.2.6 (versión de módulo: `magento/inventory-metapackage = 1.2.6`) es compatible con la versión 2.4.6 y con la versión 2.4.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y la base de código de Magento Open Source.

![Problema corregido](../assets/fix.svg) La tienda ahora muestra los productos compuestos (configurables, agrupados y agrupados) como en stock cuando los productos secundarios que se habían agotado vuelven a estar en stock. Anteriormente, la tienda indicaba que el producto compuesto estaba agotado en estas condiciones. <!-- ACP2E-1106-->

![Problema corregido](../assets/fix.svg) Las opciones de productos configurables ahora se muestran según lo esperado, ya que no hay existencias en la tienda si la opción se creó con la cantidad establecida en 0 y **[!UICONTROL Display out-of-stock products]** está activada. <!-- ACP2E-1148-->

![Problema corregido](../assets/fix.svg) Las cachés de la página Categoría ya no se invalidan cuando cambia la cantidad de existencias y el producto aún está en stock. Adobe Commerce ahora carga las páginas de la caché en lugar de regenerarlas cuando cambia la cantidad de productos (y nada más) en la página de la categoría de la tienda. <!-- ACP2E-118-->

![Problema corregido](../assets/fix.svg) El recuento de productos de la lista de categorías ahora es correcto al utilizar Inventory en modo de fuente única con la variable **[!UICONTROL Display Out-Of-Stock Products]** configuración habilitada. Adobe Commerce ahora comprueba si un producto se puede vender durante el recuento. <!-- ACP2E-1033-->

![Problema corregido](../assets/fix.svg) Las reglas de precios del carro de compras para envíos en tienda ahora funcionan según lo esperado cuando se activa el inventario. Anteriormente, los descuentos generados por reglas de precios de carro de compras no se aplicaban en estas condiciones. <!-- ACP2E-1015-->

![Problema corregido](../assets/fix.svg) Al actualizar el inventario de productos en modo programado, ya no se borran todas las cachés. Anteriormente, el indexador de inventario borraba todas las cachés de configuración. <!-- ACP2E-1003-->

![Problema corregido](../assets/fix.svg) El valor de **[!UICONTROL Allow Multiple Boxes for Shipping]** El atributo para un producto en Inventario avanzado ahora se guarda según lo esperado. <!-- ACP2E-992-->

![Problema corregido](../assets/fix.svg) Adobe Commerce ahora emite una compensación de reserva precisa después de un abono de reembolso parcial para un pedido realizado con recogida en la tienda. Anteriormente, se guardaba una reserva incorrecta en `inventory_reservation` cuando un usuario administrador creó una nota de crédito sin seleccionar la **[!UICONTROL Return to Stock]** casilla de verificación <!-- ACP2E-979-->

![Problema corregido](../assets/fix.svg) Adobe Commerce ya no muestra los productos configurables como agotados en la tienda cuando se devuelve manualmente una de sus variaciones para almacenarla en implementaciones que implementan el inventario de varios orígenes. <!-- ACP2E-952-->

![Problema corregido](../assets/fix.svg) Posición de columna en la cuadrícula de producto (**[!UICONTROL Catalog]** > **[!UICONTROL Products]**) ya no vuelve a su posición anterior después de que la página se recargue en implementaciones con varios orígenes de inventario configurados. <!-- ACP2E-925-->

![Problema corregido](../assets/fix.svg) La cantidad de stock ahora es correcta después de que se emite una nota de abono para un producto virtual cuando la variable **[!UICONTROL Back to stock]** La casilla de verificación no está seleccionada. <!-- ACP2E-908-->

![Problema corregido](../assets/fix.svg) Ahora puede guardar categorías con la ordenación automática de productos y el ámbito asignado a existencias no predeterminadas. Anteriormente, Adobe Commerce no guardaba la categoría y mostraba este error: `Something went wrong while saving the category`. <!-- ACP2E-859-->

![Problema corregido](../assets/fix.svg) El estado de stock del producto configurable ahora se actualiza según lo esperado cuando se crea el producto con todas las variaciones configurables sin existencias. <!-- ACP2E-813-->

![Problema corregido](../assets/fix.svg) La herramienta Analizador de incoherencia de reservas ahora funciona correctamente con pedidos enviados parcialmente que contienen productos configurables, agrupados y agrupados. Ahora se analizan los tipos de productos compuestos. Anteriormente, las cancelaciones y los reembolsos se guardaban solo para los productos principales, no para los artículos de pedidos de subproductos de paquetes configurables y agrupados de envío. <!-- ACP2E-924-->

![Problema corregido](../assets/fix.svg) Adobe Commerce ya no muestra un error cuando un usuario administrador intenta asignar 200 o más orígenes de inventario a un inventario o producto. <!-- ACP2E-1180-->

![Problema corregido](../assets/fix.svg) Adobe Commerce ahora admite la creación de un abono para un pedido del que se ha eliminado un producto. Anteriormente, los comerciantes no podían crear una nota de abono cuando los productos se habían eliminado del pedido después de crearse una factura. La aplicación mostraba este error: `Following products with requested skus were not found: s00001`. t. <!-- ACP2E-1138-->

![Problema corregido](../assets/fix.svg) Las tiendas ahora se filtran según los ID de una o varias tiendas. El `event` el código de atributo del producto se ha añadido a la lista de códigos de atributo reservados. Anteriormente, el informe Bajo stock arrojaba una excepción cuando se instalaba el módulo Inventario. <!-- ACP2E-1017-->

![Problema corregido](../assets/fix.svg) Los filtros de navegación por capas ahora funcionan según lo esperado y los productos sin existencias ahora se anexan a la lista de productos de la categoría de la tienda. El nuevo `is_out_of_stock` el atributo sorting utiliza el asignador de campos dinámicos de Elasticsearch para la colección de productos storefront. <!-- ACP2E-748-->

![Problema corregido](../assets/fix.svg) El estado de stock del producto compuesto (paquete, agrupado y configurable) se actualiza según lo esperado cuando el estado de stock del producto secundario se cambia mediante un REST `POST /rest/V1/inventory/source-items` llamada. <!-- ACP2E-1209-->

## Versión 1.2.5

[!DNL Inventory Management] 1.2.5 (versión de módulo: `magento/inventory-metapackage = 1.2.5`) es compatible con la versión 2.4.5 y con la versión 2.4.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y la base de código de Magento Open Source.

![Problema corregido](../assets/fix.svg) El estado de stock de inventario predeterminado del paquete y los productos agrupados ahora se actualiza según lo esperado cuando un comerciante crea un envío desde el administrador. Anteriormente, el estado de estos productos permanecía sin cambios después de que se creara un envío. <!--- ACP2E-418-->

![Problema corregido](../assets/fix.svg) Los productos configurables ahora vuelven a estar en stock cuando se cumple una de las siguientes condiciones: 1. El producto principal tiene al menos un elemento secundario guardado en stock. 2. El propio producto configurable se actualizó y se configuró como **en stock** y tenía al menos un hijo en existencia. <!--- ACP2E-443-->

![Problema corregido](../assets/fix.svg) Los cambios de inventario implementados a través de la API de REST ahora se reflejan como se espera en las páginas de detalles del producto. La caché de los productos del catálogo ahora se limpia después de comparar los estados de stock último y actual. Anteriormente, omitir la función de llamada de retorno provocaba una evaluación incorrecta de los cambios de estado de las existencias, que no limpiaban la déclencheur necesaria. Como resultado, la tienda no reflejaba los cambios del inventario. <!--- ACP2E-161-->

![Problema corregido](../assets/fix.svg) Los productos asignados a las existencias predeterminadas y que anteriormente estaban agotados ahora están visibles en la tienda después de que el elemento de origen se actualice mediante `/V1/inventory/source-items`. Anteriormente, este extremo de la API de REST establecía el valor incorrecto `stock_status`. <!--- ACP2E-562-->

![Problema corregido](../assets/fix.svg) Anulando asignación de orígenes de inventario mediante acción masiva (**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**) ahora funciona como se espera cuando las fuentes incluyen SKU duplicadas, excepto para un cero a la izquierda (por ejemplo, `01234` y `1234`). Anteriormente, la aplicación no quitaba la asignación de orígenes de inventario y generaba un error. <!--- ACP2E-2641-->

![Problema corregido](../assets/fix.svg) El estado de stock de productos ahora es siempre **en stock** en la tienda cuando se activan infinitos pedidos pendientes y el producto se asigna a un stock personalizado, independientemente de la cantidad no satisfecha. Anteriormente, los productos no estaban disponibles incluso cuando se habilitaban los pedidos pendientes. <!--- ACP2E-664-->

![Problema corregido](../assets/fix.svg) El stock de productos principal y secundario configurables ahora se actualiza correctamente después de que el elemento de origen se actualice con `POST /V1/inventory/source-items`. Una vez que el producto secundario se actualiza a través de la API, un nuevo complemento de inventario para comprobaciones de existencias predeterminadas y actualiza la cantidad y el estado configurables del producto. <!--- ACP2E-442-->

![Problema corregido](../assets/fix.svg) Los productos agrupados agotados ya no aparecen en la página Categoría de la tienda. <!--- ACP2E-2082-->

![Problema corregido](../assets/fix.svg) Se ha corregido el nombre del paquete en `CatalogInventory` `composer.json`. <!--- ACP2E-2914-->

![Problema corregido](../assets/fix.svg) El estado de pedidos pendientes ahora se representa correctamente en el administrador después de realizar un pedido con una cantidad cero de productos en una implementación de varias fuentes/existencias. [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![Problema corregido](../assets/fix.svg) Los productos agrupados sin existencias ya no se muestran en la página Categoría de tienda cuando el producto agrupado se actualiza desde la sección existencias. <!--- ACP2E-2012-->

![Problema corregido](../assets/fix.svg) Se han resuelto los problemas de compatibilidad con PHP 7.4. <!--- AC-3192-->

![Problema corregido](../assets/fix.svg) Se mejora el rendimiento de las operaciones de guardado que incluyen productos agrupados que contienen muchas opciones (varias 100). Anteriormente, el guardado de estos productos de paquete grande tardaba varios minutos y, a veces, resultaba en tiempos de espera en implementaciones con los servicios de inventario habilitados. [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![Problema corregido](../assets/fix.svg) La herramienta de acción masiva de productos (**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**) ahora funciona según lo esperado al asignar un origen de inventario a varios productos cuando los SKU están duplicados, excepto para un `0` (por ejemplo, `01234` y `1234`). Anteriormente, solo se asignaba un producto a un origen de inventario. [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![Problema corregido](../assets/fix.svg) El `ProductInterface.only_x_left_in_stock` ahora, el campo devuelve 0 si el inventario es 0. Anteriormente, devolvía nulo. [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![Problema corregido](../assets/fix.svg) Ahora puede editar las existencias predeterminadas desde Admin **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**. Anteriormente, se mostraba un error de JavaScript en la consola al intentar agregar o quitar orígenes de las existencias predeterminadas, aunque se podían asignar sitios web a las existencias predeterminadas. <!--- ACP2E-545-->

![Problema corregido](../assets/fix.svg) <!--- ACP2E-274--> El recuento de productos de la lista de categorías ahora es correcto al utilizar el modo de un solo origen de inventario con **[!UICONTROL Display Out-Of-Stock Products]** configuración habilitada. Un nuevo complemento ahora utiliza `AreProductsSalableInterface` y `StockConfigurationInterface` para determinar el número total de productos. Anteriormente, la lista de productos de categorías devolvía una cantidad de productos incorrecta.

![Problema corregido](../assets/fix.svg) <!--- ACP2E-322--> Los productos configurables ahora se mueven a la última posición de la lista de productos después de actualizar las existencias cuando el **[!UICONTROL Move out of stock to the bottom]** La configuración está habilitada. Se implementa una nueva consulta de base de datos personalizada para negar el orden de clasificación de índices del Elasticsearch, lo que ignora el orden de clasificación habilitado por el administrador. Anteriormente, los productos configurables y sus productos secundarios no se movían al final de la lista cuando esta configuración estaba habilitada.

## Versión 1.2.4

Inventory management 1.2.4 (versión de módulo: `magento/inventory-metapackage = 1.2.4`) es compatible con la versión 2.4.4 y con la versión 2.4.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y la base de código de Magento Open Source.

![Problema corregido](../assets/fix.svg) Commerce ahora muestra un valor de cantidad vendible preciso para todos los productos en la vista de lista de productos de administración. Anteriormente, mostraba un valor en blanco para la cantidad vendible de productos en existencia con SKU que contenían caracteres especiales. <!--- MC-41936-->

![Problema corregido](../assets/fix.svg) El rendimiento ha mejorado en las acciones de carro de compras y cierre de compra, como agregar productos al carro de compras en implementaciones con muchas fuentes de inventario (aproximadamente 10 000). <!--- MC-42570-->

![Problema corregido](../assets/fix.svg) El `bin/magento inventory:reservation:list-inconsistencies` ahora gestiona correctamente los pedidos con envíos parciales incluso si las reservas se pierden de la base de datos y se ha borrado la caché. Anteriormente, cuando este comando se ejecutaba con una memoria caché previamente borrada, Commerce mostraba el siguiente error: `Area code is not set`. <!--- MC-42142-->

![Problema corregido](../assets/fix.svg) La indexación incremental de productos secundarios agrupados ya no hace que otros productos agrupados se indexen incorrectamente cuando se comparten productos secundarios. <!--- MC-41963-->

![Problema corregido](../assets/fix.svg) La página de categoría de tienda ahora muestra el recuento de productos correcto después de eliminar un producto de una categoría por API. Anteriormente, el recuento de productos de la página de categorías era incorrecto hasta que se produjo la reindexación. <!--- MC-42287-->

![Problema corregido](../assets/fix.svg) Los productos configurables ahora se pueden devolver al stock al crear una nota de abono cuando la variable **[!UICONTROL Manage Stock]** La opción está desactivada. Anteriormente, Commerce no mostraba la variable **Volver a stock** casilla de verificación en la página de creación de nota de abono cuando esta opción estaba desactivada. <!--- MC-42002-->

![Problema corregido](../assets/fix.svg) Se ha mejorado la administración de existencias de inventario que superan los 10.000 artículos. Anteriormente, los problemas de rendimiento a veces impedían que los comerciantes editaran las existencias en el Admin antes de lanzar su sitio web. <!--- MC-42643-->

![Problema corregido](../assets/fix.svg) El **[!UICONTROL User Roles]** La página de administración se actualiza para proporcionar a los administradores permisos restringidos acceso a la configuración de los métodos de envío. El _Métodos de envío_ se ha cambiado el nombre de la sección a _[!UICONTROL Delivery methods]_, y_[!UICONTROL In-Store Pickup]_ se mueve debajo de _[!UICONTROL Delivery methods]_sección. [GitHub-30053](https://github.com/magento/magento2/issues/30053)  <!--- MC-41545-->

![Problema corregido](../assets/fix.svg) Adobe Commerce ya no crea una reserva de producto duplicada después de que la API actualice un abono. <!--- MC-41757-->

![Problema corregido](../assets/fix.svg) Cambio desde el _[!UICONTROL Pick up in Store]_a la pestaña_[!UICONTROL Shipping]_ La pestaña en el flujo de trabajo de cierre de compra ya no déclencheur un error de JavaScript cuando solo está disponible la entrega de recogida en la tienda. <!--- MC-42808-->

![Problema corregido](../assets/fix.svg) La cantidad de productos vendibles y la cantidad de productos en stock ahora se sincronizan correctamente. Anteriormente, la compensación de reserva de inventario no se volvía a crear para pedidos cancelados. <!--- MC-42485-->

![Problema corregido](../assets/fix.svg) El rendimiento del validador se optimiza para evitar que se agregue una nueva fuente al producto secundario de un producto agrupado con tipo de envío `Ship Together`. <!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3 (versión de módulo: `magento/inventory-metapackage = 1.2.3`) es compatible con la versión 2.4.3 y con la versión 2.4.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y la base de código de Magento Open Source.

![Problema corregido](../assets/fix.svg) Se han corregido varios problemas relacionados con la visibilidad del producto compuesto en el front-end.

![Problema corregido](../assets/fix.svg) Se ha mejorado el rendimiento de administración de páginas de carro de compras con la cantidad mínima requerida.

![Problema corregido](../assets/fix.svg) Hay varias correcciones destinadas a resolver problemas con la creación de fuentes, los artículos sin existencias, el abastecimiento de existencias, la ordenación de fuentes asignadas, el envío en tienda y los comandos de inventario.

![Problema corregido](../assets/fix.svg) [!DNL Commerce] ahora admite códigos postales canadienses de tres dígitos para envíos en tienda. Los códigos de seis dígitos no son compatibles debido a las limitaciones establecidas por `geonames.org`.

![Problema corregido](../assets/fix.svg) El administrador ahora muestra la cantidad correcta de existencias predeterminadas para los productos desactivados en la **Productos** cuadrícula y el **Editar producto** para implementaciones de varias tiendas.

![Problema corregido](../assets/fix.svg) [!DNL Commerce] ahora actualiza la caché de productos de la categoría cuando un producto del paquete vuelve a estar disponible.

## 1.2.2

[!DNL Inventory Management] 1.2.2 (versión de módulo: `magento/inventory-metapackage = 1.2.2`) es compatible con la versión 2.4.2 y con la versión 2.4.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y la base de código de Magento Open Source.

![Problema corregido](../assets/fix.svg) Se han corregido varios problemas relacionados con la visibilidad del producto compuesto en el front-end.

![Problema corregido](../assets/fix.svg) Se ha mejorado el rendimiento de la página del carro de compras durante la actualización de cantidades en B2B.

![Problema corregido](../assets/fix.svg) Varias correcciones destinadas a resolver problemas con la recogida en tienda, las actualizaciones masivas y el umbral de inventario.

![Nuevo](../assets/new.svg) **Pruebas funcionales.** Se han introducido nuevas pruebas funcionales y se han proporcionado correcciones para las pruebas existentes a fin de hacerlas más estables.

## 1.2.1

[!DNL Inventory Management] 1.2.1 (versión de módulo: `magento/inventory-metapackage = 1.2.1`) es compatible con la versión 2.4.1 y con la versión 2.4.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y la base de código de Magento Open Source.

![Problema corregido](../assets/fix.svg) Se ha corregido un problema conocido relacionado con `inventory_cleanup_reservations` Se ha solucionado un problema relacionado con la funcionalidad de recogida en tienda para los productos agrupados. Esta actualización también incluye mejoras generales en el cálculo de existencias, compatibilidad con paquetes de productos y funcionalidad de pedidos pendientes.

![Nuevo](../assets/new.svg) **Pruebas funcionales.** Se han introducido nuevas pruebas funcionales para proporcionar una cobertura adicional de la funcionalidad de recogida en tienda.

## 1.2.0

[!DNL Inventory Management] 1.2.0 (versión de módulo: `magento/inventory-metapackage = 1.2.0`) es compatible con la versión 2.4.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y el código base de Magento Open Source.

![Problema corregido](../assets/fix.svg) Numerosas correcciones para resolver problemas con la asignación de fuentes, compatibilidad con funciones de entorno escalable y compatibilidad con PHP 7.4, MySQL 8 y PHPUNIT 9.

![Nuevo](../assets/new.svg) **Método de envío en tienda.** Se ha añadido una opción para que los usuarios seleccionen una fuente que se utilizará como ubicación de recogida durante el cierre de compra. Consulte [Entrega en tienda](../stores-purchase/shipping-in-store-delivery.md) en el _Guía de ventas y experiencia de compra_.

![Nuevo](../assets/new.svg) **Paquete de compatibilidad de productos para el modo multifuente.** El inventario admite todos los tipos de productos con varias fuentes.

![Nuevo](../assets/new.svg) **Reindexación asíncrona de stock.** Se ha añadido la capacidad de reindexar de forma asíncrona las existencias y mejorar el rendimiento de varios escenarios críticos.

![Nuevo](../assets/new.svg) **Interfaces por lotes.** Se han introducido nuevas interfaces masivas para la comprobación de la escalabilidad: `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`, `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![Nuevo](../assets/new.svg) **Mayor cobertura de las pruebas.** La nueva funcionalidad se cubre con pruebas automatizadas, incluida la cobertura ampliada para problemas detectados y corregidos.

![Problema conocido](../assets/bug.svg) **Problema conocido.** La ausencia del `object_id` en los metadatos de las reservas impide que `inventory_cleanup_reservations` el trabajo cron no funciona correctamente. Este problema se introdujo en [magento/inventory#3046](https://github.com/magento/inventory/pull/3046).

**Solución alternativa:** Ejecute las siguientes consultas MySQL para limpiar manualmente las reservas:

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6

[!DNL Inventory Management] 1.1.6 (versión de módulo: `inventory-composer-metapackage = 1.1.6`) es compatible con la versión 2.3.6 y con las versiones 2.3.5, 2.3.4, 2.3.3, 2.3.2, 2.3.1 y 2.3.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y la base de código del Magento Open Source.

![Problema corregido](../assets/fix.svg) Correcciones para resolver problemas relacionados con pedidos no satisfechos, notas de crédito, cuadrícula de informes de existencias bajas, correcciones conectadas a la herramienta CLI &quot;resolver incoherencias&quot; y mejoras generales.

![Nuevo](../assets/new.svg) **Reindexación asíncrona de stock.** Se ha añadido la capacidad de reindexar de forma asíncrona las existencias y mejorar el rendimiento de varios escenarios críticos.

## 1.1.5

[!DNL Inventory Management] 1.1.5 (versión de módulo: `inventory-composer-metapackage = 1.1.5`) es compatible con la versión 2.3.5 y con las versiones 2.3.4, 2.3.3, 2.3.2, 2.3.1 y 2.3.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y la base de código del Magento Open Source.

![Nuevo](../assets/new.svg) **Actualice el inventario una vez que se cambie el SKU del producto.** Se ha introducido una nueva configuración para cambiar al nuevo comportamiento: Sincronizar con el catálogo.

![Nuevo](../assets/new.svg) **Pruebas funcionales.** Se han introducido nuevas pruebas funcionales para eliminar el hueco en la cobertura de las pruebas. Se han corregido varios problemas para que las pruebas fueran más estables y fiables).

![Problema conocido](../assets/bug.svg) Correcciones para evitar la sobreventa de productos, la visibilidad de productos &quot;sin existencias&quot; en la tienda, numerosas correcciones para la compatibilidad con entornos escalables y mejoras en la interfaz de usuario.

## 1.1.4

[!DNL Inventory Management] 1.1.4 (versión de módulo: `inventory-composer-metapackage = 1.1.4`) es compatible con la versión 2.3.4 y con las versiones 2.3.3, 2.3.2, 2.3.1 y 2.3.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y la base de código del Magento Open Source.

![Problema corregido ](../assets/fix.svg)**Mayor rendimiento.** Se ha introducido la lógica de agrupamiento para el comando CLI de reservas de inventario para reducir el uso de memoria y evitar casos en los que el proceso se atasca sin ninguna respuesta.

![Nuevo ](../assets/new.svg)**Mayor cobertura de las pruebas.** Se han introducido muchas nuevas pruebas funcionales. Casi todos los casos de inventario manual se tratan con pruebas automatizadas.

![Problema conocido](../assets/bug.svg) Numerosas correcciones destinadas a resolver problemas con notas de crédito, productos agrupados y acciones masivas de origen y existencias.

## 1.1.3

[!DNL Inventory Management] 1.1.3 (versión de módulo: `inventory-composer-metapackage = 1.1.3`) es compatible con la versión 2.3.3 y con las versiones 2.3.2, 2.3.1 y 2.3.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y la base de código del Magento Open Source.

![Problema corregido ](../assets/fix.svg)**Mejor integración con las funciones de Adobe Commerce y B2B.** [!DNL Inventory Management] ahora funciona correctamente con las siguientes funciones para sitios web que utilizan fuentes de inventario y existencias no predeterminadas:

- Pedido por SKU (Adobe Commerce)
- Pedido rápido (B2B)
- Listas de solicitudes (B2B)

![Nuevo ](../assets/new.svg)**Mayor rendimiento.** El rendimiento de navegación por el catálogo de tiendas se mejora para los sitios web que ejecutan el inventario de stock y la fuente predeterminados.

![Nuevo ](../assets/new.svg)**Mayor cobertura de las pruebas.** La cobertura de las pruebas funcionales e integrales automatizadas ha aumentado significativamente.

## 1.1.2

[!DNL Inventory Management] 1.1.2 (versión de módulo: `inventory-composer-metapackage = 1.1.2`) es compatible con la versión 2.3.2 y con las versiones 2.3.1 y 2.3.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y la base de código del Magento Open Source.

![Problema corregido](../assets/fix.svg) Añadido `source_code` a la respuesta de la GET `/V1/shipments` Extremo REST. <!-- https://github.com/magento/inventory/pull/2142 -->

![Problema corregido](../assets/fix.svg) Se ha resuelto un problema para borrar correctamente las reservas y actualizar las cantidades de productos después de emitir una nota de abono para un pedido no enviado. Al seleccionar la opción para <!-- https://github.com/magento/inventory/pull/2179 -->

![Problema corregido](../assets/fix.svg) Se ha resuelto un problema para guardar correctamente la cantidad de productos secundarios configurables al introducir cantidades durante la creación del producto. <!-- https://github.com/magento/inventory/pull/2158 -->

Nuevos módulos para [!DNL Inventory Management] 1.1.2 Las versiones beta incluyen:

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![Nuevo](../assets/new.svg) **Se ha añadido un punto final parcial de transferencia de stock** - Los puntos finales de transferencia masiva actuales mueven toda la cantidad asignada de un origen a un origen de destino. El nuevo `/rest/V1/inventory/bulk-partial-source-transfer` el punto final permite a los comerciantes transferir existencias parciales del origen al origen como una operación masiva. Para transferir una cantidad específica, introduzca una solicitud al punto de conexión con el `sku`, `qty`, `origin_source_code`, y `destination_source_code`. Las transferencias verifican que el origen esté asignado a `sku`, existe una cantidad suficiente para transferir, etc. Consulte [Acciones masivas de inventario](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} en la documentación de la API de REST. <!-- https://github.com/magento/inventory/pull/2117 -->

![Nuevo](../assets/new.svg) **CLI de reserva agregada** - Los nuevos comandos le ofrecen opciones para detectar y resolver las incoherencias de la reserva. A medida que los pedidos se envían y cambian de estado, [!DNL Inventory Management] genera reservas y actualizaciones iniciales mediante reservas de compensación. Estos comandos devuelven una lista de incoherencias detectadas por ID de pedido, SKU e ID de stock, y crean reservas para resolverlas. Consulte la [Referencia de CLI](cli.md) para obtener más información. <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![Nuevo](../assets/new.svg) **Mejoras de rendimiento para fuentes y opciones de SSA** - La clasificación y selección de las fuentes durante el envío causó una degradación del rendimiento de las existencias con un gran número de fuentes. Esta versión proporciona mejoras de rendimiento significativas para enumerar y ordenar las fuentes disponibles al revisar y seleccionar las opciones de SSA en los envíos. <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![Nuevo](../assets/new.svg) **Se añadió la compatibilidad de GraphQL con Inventory management** - Esta versión instala un nuevo `magento/module-inventory-graph-ql` módulo. El GraphQL [Atributos de ProductInterface](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} ahora incluye el `only_x_left_in_stock` y `stock_status` atributos para [!DNL Inventory Management] soporte. <!-- https://github.com/magento/inventory/pull/2124 -->

![Nuevo](../assets/new.svg) **IU simplificada para orígenes asignados** : la tabla Fuentes asignadas de las páginas de producto ha simplificado el contenido para facilitar las actualizaciones y aumentar el rendimiento al mostrar muchas fuentes. Todas las fuentes enumeran por nombre de origen (coloque el puntero del ratón encima) `source_code`).

![Nuevo](../assets/new.svg) **Exportar servicio de stock agregado** - Esta versión proporciona un nuevo servicio de stock agregado para la exportación (conservando las reservas en el sistema) para admitir Sales Channel externas, como anuncios de Amazon, eBay y Google Shopping.  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0 (versión de módulo: `inventory-composer-metapackage = 1.1.0`) es compatible y compatible con la versión 2.3.0 de Adobe Commerce, Adobe Commerce en la infraestructura en la nube y la base de código de Magento Open Source. [!DNL Inventory Management] 1.1.1 solo se presenta como una actualización de nombre de paquete, compatible con la versión 2.3.1 y con la versión 2.3.0 de Adobe Commerce, Adobe Commerce en la infraestructura de la nube y la base de código de Magento Open Source.

![Problema corregido](../assets/fix.svg) **Se ha agregado compatibilidad con el Elasticsearch para modos de una sola fuente y múltiples fuentes** — Ahora puede configurar y utilizar Elasticsearch con existencias personalizadas. Consulte [Configuración del servicio de Elasticsearch](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html){target="_blank"} para obtener información de instalación. <!-- PR https://github.com/magento/inventory/pull/1943 -->

![Problema corregido](../assets/fix.svg) Se han resuelto problemas de rendimiento con Stock predeterminado para aumentar drásticamente el rendimiento con numerosas operaciones. Las mejoras aumentan el rendimiento para el modo de un solo origen, las páginas Transferir inventario a origen, Categoría de tienda y Cálculos de cantidad vendible.

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![Problema corregido](../assets/fix.svg) Se han resuelto problemas con el estado Sin existencias y la transferencia de inventario en bloque a Existencias para productos configurables y agrupados. La selección de los productos principales y la realización de acciones masivas no afectan al estado del producto. Si el producto principal estaba En stock, permanece En stock.

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![Nuevo](../assets/new.svg) **Algoritmo de prioridad de distancia** — El algoritmo de prioridad de distancia es un nuevo algoritmo de selección de origen listo para usar para las recomendaciones de envío basadas en la distancia. Este algoritmo compara la ubicación de la dirección de destino de envío con las ubicaciones de origen para determinar el origen más cercano para satisfacer los envíos. La distancia puede determinarse por la distancia física o el tiempo que se pasa viajando de un lugar a otro, utilizando datos de ubicación geocodificados importados o indicaciones de Google (conducir, caminar o montar en bicicleta).

![Nuevo](../assets/new.svg) **Lista de cantidades de origen expandida** — Los comerciantes con un número elevado de orígenes pueden pasar el ratón por encima y ver fácilmente todos los orígenes por producto a través de la cuadrícula de producto. Cada producto muestra un mínimo de cinco fuentes y cantidades coincidentes. Al pasar el ratón por encima de los orígenes, puede desplazarse por toda la lista de orígenes y cantidades actuales.

![Problema conocido](../assets/bug.svg) Problema conocido con Magento Open Source y Adobe Commerce v2.3.1: La migración asincrónica de datos entre fuentes encuentra problemas debido a cambios en las API asincrónicas con nombres de temas que reflejan nombres de clases y métodos de PHP. Usar operaciones sincrónicas, establecer **[!UICONTROL Run asynchronously]** hasta `No`, se recomienda.
