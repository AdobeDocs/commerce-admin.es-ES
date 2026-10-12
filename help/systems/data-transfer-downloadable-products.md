---
title: Importar productos descargables
description: Consulte un ejemplo de importación de datos de producto para un producto descargable.
exl-id: e0b45ef5-dff1-4ee4-aa7e-2407162669fd
feature: Products, Data Import/Export
TQID: 'https://experienceleague.adobe.com/a62y8GDLpN0PHxlm8EYHHMsHfzzkjB4mSNa-BV78Ra8'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: 601e4abe-d9bf-58de-a779-32ed6794dcbe
    internal-label: Data Import/Export
role_v2:
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
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%
---
# Importar productos descargables

El flujo para importar productos descargables es el mismo que para [Productos agrupados](data-transfer-bundle-products.md) o [Productos configurables](data-transfer-configurable-products.md). La diferencia es que un producto descargable tiene [vínculos descargables](../catalog/product-create-downloadable.md) y [muestras descargables](../catalog/product-create-downloadable.md) con sus imágenes.

El directorio raíz predeterminado para vínculos descargables y ejemplos es `<Magento-root-folder>/pub/media/import`. Si el módulo de almacenamiento remoto está habilitado, el directorio raíz predeterminado para los vínculos descargables y las muestras es el directorio `<remote-storage-root-folder>/media/import`.

El archivo CSV tiene columnas independientes para `downloadable_links` y `downloadable_samples`.

- **Imágenes de vínculos descargables**: en el siguiente ejemplo, las imágenes de vínculos descargables (`red.jpg` y `black.jpg`) se encuentran en la carpeta `<Magento-root-folder>/pub/media/import/test`. Si el almacenamiento remoto está habilitado, estas imágenes se encuentran en la carpeta `<remote-storage-root-folder>/media/import/test`.

  ![Datos de ejemplo: producto descargable con vínculos descargables](./assets/data-import-downloadable-links.png){width="600" zoomable="yes"}

- **Imágenes de muestra descargables**: en el siguiente ejemplo, la imagen de muestra descargable (`white.jpg`) se encuentra en la carpeta `<Magento-root-folder>/pub/media/import/test`. Si el almacenamiento remoto está habilitado, esta imagen se encuentra en la carpeta `<remote-storage-root-folder>/media/import/test`.

  ![Datos de ejemplo: producto descargable con ejemplos descargables](./assets/data-import-downloadable-samples.png){width="400" zoomable="yes"}

Para obtener más información acerca de cómo habilitar y administrar el módulo de almacenamiento remoto, consulte [Configurar almacenamiento remoto](https://experienceleague.adobe.com/es/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage) en la _Guía de configuración_.
