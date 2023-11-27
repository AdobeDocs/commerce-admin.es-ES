---
title: "Instalar, actualizar y eliminar [!DNL Inventory Management]"
description: Obtenga información sobre cómo administrar el [!DNL Inventory Management] metapaquete.
exl-id: d088ff35-c0e1-41c8-89fb-78180eaefbf7
level: Experienced
feature: Inventory, Install
source-git-commit: d6c81da4b4e0674d6699e9781921ccb2160b9983
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# Instalar, actualizar y quitar [!DNL Inventory Management]

[!DNL Inventory Management] Los módulos de proporcionan todas las funciones y opciones de inventario para que los comerciantes de un solo origen y de varios orígenes administren las cantidades de productos y las existencias para los canales de ventas. Estas funciones están disponibles en las versiones 2.4.x de Adobe Commerce y Magento Open Source.

Estas funciones y extensiones se desarrollaron como parte de la [Proyecto de inventario](https://github.com/magento/inventory) a través del programa Magento Open Source Community Engineering.

[!DNL Inventory Management] se instala en las versiones 2.3.x y 2.4.x de Adobe Commerce y Magento Open Source, con todas las funciones habilitadas de forma predeterminada. No se requieren pasos adicionales para habilitar estas características de inventario. Las actualizaciones desde v2.1.x o 2.2.x pueden requerir pasos adicionales. Consulte [Actualizar Inventory management](#upgrade-inventory-management).

Instalación según [Instalación local de inicio rápido](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html){target="_blank"} se recomienda. Instale con un metapaquete para recibir todo [!DNL Inventory Management] módulos.

La siguiente línea de la `composer.json` instalaciones de metapaquetes [!DNL Inventory Management]:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

Para obtener una lista de [!DNL Inventory Management] versiones de metapaquetes, consulte las [notas de la versión](release-notes.md).

El [!DNL Inventory Management] proceso de instalación añade todos los módulos de a `<Magento_installation_directory>/app/etc/config.php` archivo. A `1` value indica que el módulo correspondiente está habilitado. Se añade la siguiente lista de módulos:

```php
        'Magento_Inventory' => 1,
        'Magento_InventoryAdminUi' => 1,
        'Magento_InventoryAdvancedCheckout' => 1,
        'Magento_InventoryApi' => 1,
        'Magento_InventoryBundleProduct' => 1,
        'Magento_InventoryBundleProductAdminUi' => 1,
        'Magento_InventoryCatalog' => 1,
        'Magento_InventorySales' => 1,
        'Magento_InventoryCatalogAdminUi' => 1,
        'Magento_InventoryCatalogApi' => 1,
        'Magento_InventoryCatalogSearch' => 1,
        'Magento_InventoryConfigurableProduct' => 1,
        'Magento_InventoryConfigurableProductAdminUi' => 1,
        'Magento_InventoryConfigurableProductIndexer' => 1,
        'Magento_InventoryConfiguration' => 1,
        'Magento_InventoryConfigurationApi' => 1,
        'Magento_InventoryDistanceBasedSourceSelection' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionAdminUi' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionApi' => 1,
        'Magento_InventoryElasticsearch' => 1,
        'Magento_InventoryExportStockApi' => 1,
        'Magento_InventoryIndexer' => 1,
        'Magento_InventorySalesApi' => 1,
        'Magento_InventoryGroupedProduct' => 1,
        'Magento_InventoryGroupedProductAdminUi' => 1,
        'Magento_InventoryGroupedProductIndexer' => 1,
        'Magento_InventoryImportExport' => 1,
        'Magento_InventoryCache' => 1,
        'Magento_InventoryLowQuantityNotification' => 1,
        'Magento_InventoryLowQuantityNotificationApi' => 1,
        'Magento_InventoryMultiDimensionalIndexerApi' => 1,
        'Magento_InventoryProductAlert' => 1,
        'Magento_InventoryRequisitionList' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryExportStock' => 1,
        'Magento_InventorySalesAdminUi' => 1,
        'Magento_InventorySalesFrontendUi' => 1,
        'Magento_InventorySetupFixtureGenerator' => 1,
        'Magento_InventoryShipping' => 1,
        'Magento_InventorySourceDeductionApi' => 1,
        'Magento_InventorySourceSelection' => 1,
        'Magento_InventorySourceSelectionApi' => 1,
        'Magento_InventoryLowQuantityNotificationAdminUi' => 1,
        'Magento_InventoryShippingAdminUi' => 1,
        'Magento_InventoryGraphQl' => 1,
```

## Activar [!DNL Inventory Management] características

Cuando se instala, actualiza o actualiza, la variable _[!UICONTROL Manage Stock]_de Administración está activada de forma predeterminada. Esta opción habilita el seguimiento y la administración del inventario, pero no afecta al estado del módulo. Para deshabilitar los módulos, consulte la siguiente sección.

Para obtener más información sobre las configuraciones, consulte [Configuración de Inventory management](configuration.md).

## Deshabilitar Inventory management

>[!IMPORTANT]
>
>Uso del valor predeterminado [!DNL Inventory Management] módulos es muy recomendable. La alternativa [!DNL CatalogInventory] , que se utiliza para los sistemas con [!DNL Inventory Management] módulos, ya no se utiliza. Desactivación de la [!DNL Inventory Management] Los módulos de pueden causar un sistema inestable y provocar varios problemas.

Es posible que desee deshabilitar [!DNL Inventory Management] módulos para:

* Acelere el proceso de actualización para los comerciantes que migran de 2.0.x, 2.1.x, 2.2.x o 2.3.x a 2.4.x.
* Utilice los módulos del sistema de inventario personalizado o de terceros y de gestión de pedidos.

Consulte la [Habilitar o deshabilitar módulos](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html) página en la _Guía de instalación_ para obtener información sobre cómo deshabilitar los módulos aplicables.

Cuando se completa, el sistema proporciona una lista de módulos y valores en `<Magento_installation_directory>/app/etc/config.php`, empezando por:

```php
   'Magento_Inventory' => 0,
   'Magento_InventoryAdminUi' => 0,
   'Magento_InventoryAdvancedCheckout' => 0,
   ...
```

>[!IMPORTANT]
>
>Si tiene instalados los módulos del conector de OMS, asegúrese de no desactivar el `Magento_InventoryMessageBus` module, que es un módulo Conector. Es necesario utilizar el conector con OMS.

## Eliminar Inventory management

>[!IMPORTANT]
>
>Uso del valor predeterminado [!DNL Inventory Management] módulos es muy recomendable. La alternativa [!DNL CatalogInventory] módulo, que se utiliza para sistemas con [!DNL Inventory Management] módulos, ya no se utiliza. Eliminación del [!DNL Inventory Management] Los módulos de pueden causar un sistema inestable y provocar varios problemas.

Si decide no utilizar la variable [!DNL Inventory Management] funcionalidad, puede quitar (desinstalar) estos módulos. Para quitar todos los módulos a través del archivo de composición, agregue lo siguiente a `composer.json`:

```
"replace": {
        "magento/module-inventory": "*",
        "magento/module-inventory-admin-ui": "*",
        "magento/module-inventory-advanced-checkout": "*",
        "magento/module-inventory-api": "*",
        "magento/module-inventory-bundle-product": "*",
        "magento/module-inventory-bundle-product-admin-ui": "*",
        "magento/module-inventory-cache": "*",
        "magento/module-inventory-catalog": "*",
        "magento/module-inventory-catalog-admin-ui": "*",
        "magento/module-inventory-catalog-api": "*",
        "magento/module-inventory-catalog-search": "*",
        "magento/module-inventory-configurable-product": "*",
        "magento/module-inventory-configurable-product-admin-ui": "*",
        "magento/module-inventory-configurable-product-indexer": "*",
        "magento/module-inventory-configuration": "*",
        "magento/module-inventory-configuration-api": "*",
        "magento/module-inventory-distance-based-source-selection": "*",
        "magento/module-inventory-distance-based-source-selection-admin-ui": "*",
        "magento/module-inventory-distance-based-source-selection-api": "*",
        "magento/module-inventory-export-stock": "*",
        "magento/module-inventory-export-stock-api": "*",
        "magento/module-inventory-elasticsearch": "*",
        "magento/module-inventory-graph-ql": "*",
        "magento/module-inventory-grouped-product": "*",
        "magento/module-inventory-grouped-product-admin-ui": "*",
        "magento/module-inventory-grouped-product-indexer": "*",
        "magento/module-inventory-import-export": "*",
        "magento/module-inventory-indexer": "*",
        "magento/module-inventory-low-quantity-notification": "*",
        "magento/module-inventory-low-quantity-notification-admin-ui": "*",
        "magento/module-inventory-low-quantity-notification-api": "*",
        "magento/module-inventory-multi-dimensional-indexer-api": "*",
        "magento/module-inventory-product-alert": "*",
        "magento/module-inventory-requisition-list": "*",
        "magento/module-inventory-reservations": "*",
        "magento/module-inventory-reservations-api": "*",
        "magento/module-inventory-reservation-cli": "*",
        "magento/module-inventory-sales": "*",
        "magento/module-inventory-sales-admin-ui": "*",
        "magento/module-inventory-sales-api": "*",
        "magento/module-inventory-sales-frontend-ui": "*",
        "magento/module-inventory-setup-fixture-generator": "*",
        "magento/module-inventory-shipping": "*",
        "magento/module-inventory-shipping-admin-ui": "*",
        "magento/module-inventory-source-deduction-api": "*",
        "magento/module-inventory-source-selection": "*",
        "magento/module-inventory-source-selection-api": "*",
        "magento/module-inventory-visual-merchandiser": "*",
        "magento/module-inventory-swatches-frontend-ui": "*",
        "magento/module-inventory-quote-graph-ql": "*",
        "magento/module-inventory-in-store-pickup": "*",
        "magento/module-inventory-in-store-pickup-sales": "*",
        "magento/module-inventory-in-store-pickup-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-sales-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-api": "*",
        "magento/module-inventory-in-store-pickup-sales-api": "*",
        "magento/module-inventory-in-store-pickup-frontend": "*",
        "magento/module-inventory-in-store-pickup-shipping": "*",
        "magento/module-inventory-in-store-pickup-graph-ql": "*",
        "magento/module-inventory-in-store-pickup-shipping-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-multishipping": "*",
        "magento/module-inventory-in-store-pickup-shipping-api": "*",
        "magento/module-inventory-in-store-pickup-quote": "*",
        "magento/module-inventory-in-store-pickup-webapi-extension": "*",
        "magento/module-inventory-in-store-pickup-quote-graph-ql": "*",
        "magento/module-inventory-configurable-product-frontend-ui": "*",
        "magento/module-inventory-catalog-search-configurable-product": "*",
        "magento/module-inventory-catalog-search-bundle-product": "*",
        "magento/module-inventory-catalog-frontend-ui": "*",
        "magento/module-inventory-bundle-import-export": "*",
        "magento/module-inventory-bundle-product-indexer": "*"
    }
```

Cuando se complete este cambio, ejecute la instalación del compositor y eliminará automáticamente estos módulos de Inventory management.

## Actualizar Inventory management

### Anterior [!DNL Commerce] versiones

Al actualizar una instalación existente de 2.1.x, 2.2.x o 2.3.x a Adobe Commerce o Magento Open Source 2.4.x o [!DNL Inventory Management] módulos están desactivados de forma predeterminada. Esta configuración predeterminada es una precaución para evitar actualizaciones incompatibles con versiones anteriores y para admitir mejor Order Management (OMS).

>[!NOTE]
>
>Order Management no admite [!DNL Inventory Management]. Al actualizar, [!DNL Inventory Management] Los módulos de están desactivados para permitir OMS y [!DNL Commerce] 2.3.x para funcionar sin problemas.


Para habilitar [!DNL Inventory Management] módulos:

1. Edite el `<Commerce_installation_directory>/app/etc/config.php` archivo.
1. Modificar todos los módulos de inventario de `0` hasta `1` para habilitar.
1. Actualizar la base de datos:

   ```bash
   bin/magento setup:upgrade
   ```

1. Limpie la caché:

   ```bash
   bin/magento cache:clean
   ```

Se recomienda utilizar la variable [comandos de incoherencias de reserva](cli.md) después de la actualización. Al actualizar, todos los productos se añaden al Stock predeterminado. Si tiene pedidos pendientes, los comandos actualizan correctamente la cantidad vendible y las reservas para las ventas y la satisfacción de pedidos.

### Anterior [!DNL Inventory Management] versiones

Al actualizar desde versiones anteriores de [!DNL Inventory Management] a la versión más reciente, siga los pasos normales de actualización de la extensión.

Para obtener la última versión, actualice la versión del metapaquete:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

Consulte las siguientes guías para obtener más información sobre las actualizaciones de Commerce:

* [Guía de actualización de Commerce](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/overview.html){target="_blank"}
* [Habilitar o deshabilitar módulos](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html){target="_blank"}
