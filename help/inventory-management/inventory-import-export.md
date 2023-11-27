---
title: Importar y exportar inventario
description: Utilice las funciones nativas de importación y exportación con [!DNL Inventory Management] opciones para actualizar orígenes y cantidades por SKU.
exl-id: cb2d2e0d-aef8-4b18-b013-9a7b0ab448bd
feature: Inventory, Data Import/Export
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Importar y exportar inventario

Para catálogos con muchos productos, utilice las funciones nativas de importación y exportación con [!DNL Inventory Management] opciones para actualizar orígenes y cantidades por SKU. Con estas opciones, puede agregar nuevos orígenes y actualizar las cantidades de inventario para todos los orígenes o para un origen específico. Por ejemplo, puede exportar productos para una fuente en Alemania sin afectar a la información del producto para fuentes en Francia, Inglaterra o Estados Unidos.

- [!DNL Commerce] asigna automáticamente el origen predeterminado a sus productos al actualizar [!DNL Commerce] o importar nuevos productos. Si importa productos con un origen personalizado asignado, el origen predeterminado se agrega con una cantidad de 0. Para actualizar orígenes y cantidades, utilice estas instrucciones de importación.

- Los comerciantes de un solo origen utilizan la importación para actualizar solo las cantidades de productos. Todos los productos existentes y añadidos se asignan al origen predeterminado.

- Los comerciantes de varios orígenes utilizan la importación para agregar varios orígenes y cantidades por fila y por SKU.

Para importar actualizaciones, primero exporte un archivo CSV para un origen específico o todos los orígenes. Edite el archivo CSV y añada una fila por SKU para cada origen y cantidad. Necesita el código fuente cuando agregue un origen y agregue cantidades de existencias. No es posible añadir ni actualizar stock mediante funciones de importación y exportación.

## Contenido del archivo CSV

El archivo de exportación e importación incluye la siguiente información según el origen:

- `source_code` - El código de las fuentes en [!DNL Commerce]. Hay una fila para cada origen y SKU.
- `sku` - El SKU del producto en [!DNL Commerce]. La SKU debe coincidir con un producto de la tienda para que se actualice correctamente [!DNL Inventory Management] datos.
- `status` - 0 para Agotado. 1 para En existencia. Este valor debe ser 1 para adquirir stock de este origen.
- `quantity` : Cantidad total de inventario disponible para este SKU y origen.

Utilice un archivo CSV para actualizar rápidamente varios productos y orígenes asignados a fin de actualizar y corregir cualquier imprecisión en los registros de inventario en lugar de hacerlo de uno en uno a través de la interfaz de la aplicación. Para un archivo base, exporte primero y actualice según sea necesario.

![Archivo CSV de ejemplo para importar: exportar datos de inventario](assets/inventory-import-export-data.png){width="600" zoomable="yes"}

## Exportar datos de productos para todas las fuentes

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Para **[!UICONTROL Entity Type]**, elija `Stock Sources`.

   La exportación solo extrae datos para productos con un SKU.

1. Haga clic **[!UICONTROL Continue]**.

   El archivo genera y descarga para abrirlo y editarlo.

Después de actualizar las cantidades de inventario y los datos de productos, vuelva a importar el archivo a [!DNL Commerce].

![Exportación de fuentes de stock para datos y fuentes de productos](assets/inventory-export-stock-sources.png){width="350" zoomable="yes"}

## Exportación de datos de productos para una fuente específica

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Para **[!UICONTROL Entity Type]**, elija `Stock Sources`.

   La exportación solo extrae datos para productos con un SKU.

1. Utilice el **[!UICONTROL Entity Attributes]** para filtrar los productos exportados para un origen específico.

   Para `source_code`, introduzca el código de la fuente en el campo de filtro.

1. Haga clic **[!UICONTROL Continue]**.

   El archivo genera y descarga para abrirlo y editarlo.

Después de actualizar las cantidades de inventario y los datos de productos, vuelva a importar el archivo a [!DNL Commerce].

## Importar datos de productos

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Para **[!UICONTROL Entity Type]**, elija `Stock Sources`.

   La exportación solo extrae datos para productos con un SKU.

1. Seleccione las configuraciones para la **[!UICONTROL Import Behavior]**.

1. Seleccione el archivo .csv que desea importar.

1. Clic **[!UICONTROL Check Data]** y complete la importación.

![Importación de datos y orígenes de productos](assets/inventory-import-sources.png){width="600" zoomable="yes"}
