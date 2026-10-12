---
title: Importar y exportar inventario
description: Importe y exporte [!DNL Inventory Management] asignaciones de origen y cantidades por origen por SKU mediante herramientas de transferencia de datos del catálogo nativo.
exl-id: cb2d2e0d-aef8-4b18-b013-9a7b0ab448bd
feature: Inventory, Data Import/Export
TQID: 'https://experienceleague.adobe.com/TrH9Ncak4gPMh-4kejFF0NdCIzjT-xT5-M4eETSQ9FM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 8dc0e58b-adf0-51bb-8db5-bb36e3e656fb
    internal-label: Inventory
  - id: 601e4abe-d9bf-58de-a779-32ed6794dcbe
    internal-label: Data Import/Export
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%
---
# Importar y exportar inventario

Para catálogos con muchos productos, use las características nativas de importación y exportación con las opciones expandidas de [!DNL Inventory Management] para actualizar los orígenes y las cantidades por SKU. Con estas opciones, puede agregar nuevos orígenes y actualizar las cantidades de inventario para todos los orígenes o para un origen específico. Por ejemplo, puede exportar productos para una fuente en Alemania sin afectar a la información del producto para fuentes en Francia, Inglaterra o Estados Unidos.

- [!DNL Commerce] asigna automáticamente el Source predeterminado a sus productos al actualizar [!DNL Commerce] o al importar nuevos productos. Si importa productos con un origen personalizado asignado, la Source predeterminada se agrega con una cantidad de 0. Para actualizar orígenes y cantidades, utilice estas instrucciones de importación.

- Los comerciantes de un solo origen utilizan la importación para actualizar solo las cantidades de productos. Todos los productos existentes y añadidos se asignan al Source predeterminado.

- Los comerciantes de varios orígenes utilizan la importación para agregar varios orígenes y cantidades por fila y por SKU.

Para importar actualizaciones, primero exporte un archivo CSV para un origen específico o todos los orígenes. Edite el archivo CSV y añada una fila por SKU para cada origen y cantidad. Necesita el código fuente cuando agregue un origen y agregue cantidades de existencias. No es posible añadir ni actualizar stock mediante funciones de importación y exportación.

## Contenido del archivo CSV

El archivo de exportación e importación incluye la siguiente información según el origen:

- `source_code` - El código para orígenes en [!DNL Commerce]. Hay una fila para cada origen y SKU.
- `sku`: SKU del producto en [!DNL Commerce]. La SKU debe coincidir con un producto de tu tienda para actualizar correctamente los datos de [!DNL Inventory Management].
- `status` - 0 para Agotado. 1 para En existencia. Este valor debe ser 1 para adquirir stock de este origen.
- `quantity`: cantidad total de inventario disponible para este SKU y origen.

Utilice un archivo CSV para actualizar rápidamente varios productos y orígenes asignados a fin de actualizar y corregir cualquier imprecisión en los registros de inventario en lugar de hacerlo de uno en uno a través de la interfaz de la aplicación. Para un archivo base, exporte primero y actualice según sea necesario.

![Archivo CSV de ejemplo para importar: exportar datos de inventario](assets/inventory-import-export-data.png){width="600" zoomable="yes"}

## Exportar datos de productos para todas las fuentes

1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Para **[!UICONTROL Entity Type]**, elija `Stock Sources`.

   La exportación solo extrae datos para productos con un SKU.

1. Haga clic en **[!UICONTROL Continue]**.

   El archivo genera y descarga para abrirlo y editarlo.

Después de actualizar las cantidades de inventario y los datos de productos, vuelva a importar el archivo en [!DNL Commerce].

![Exportar orígenes de existencias para orígenes y datos de productos](assets/inventory-export-stock-sources.png){width="350" zoomable="yes"}

## Exportación de datos de productos para una fuente específica

1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Para **[!UICONTROL Entity Type]**, elija `Stock Sources`.

   La exportación solo extrae datos para productos con un SKU.

1. Use **[!UICONTROL Entity Attributes]** para filtrar los productos exportados para un origen específico.

   Para `source_code`, introduzca el código de origen en el campo de filtro.

1. Haga clic en **[!UICONTROL Continue]**.

   El archivo genera y descarga para abrirlo y editarlo.

Después de actualizar las cantidades de inventario y los datos de productos, vuelva a importar el archivo en [!DNL Commerce].

## Importar datos de productos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Para **[!UICONTROL Entity Type]**, elija `Stock Sources`.

   La exportación solo extrae datos para productos con un SKU.

1. Seleccione configuraciones para **[!UICONTROL Import Behavior]**.

1. Seleccione el archivo .csv que desea importar.

1. Haga clic en **[!UICONTROL Check Data]** y complete la importación.

![Importar datos y orígenes de productos](assets/inventory-import-sources.png){width="600" zoomable="yes"}
