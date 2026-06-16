---
title: Precios de nivel de importación
description: Obtenga información sobre cómo exportar datos de precios de nivel e importar datos actualizados.
exl-id: b19d0208-68b3-45ba-9896-318e12ff4131
feature: Products, Data Import/Export
TQID: https://experienceleague.adobe.com/8eyWhVu-RtuzEYG81xOyqsEFdbz0s7evB-UGepUGCNw
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 346
ht-degree: 0%

---

# Precios de nivel de importación

En lugar de ingresar [precios de nivel](../catalog/product-price-tier.md) manualmente para cada producto, puede ser más eficiente [importar](data-import.md) los datos de precios. Antes de empezar, cree un archivo de muestra de datos de precios de nivel exportados que pueda utilizar como plantilla.

![Ejemplo de tienda - precios por niveles](./assets/storefront-tier-pricing-water-bottle.png){width="700" zoomable="yes"}

## Paso 1: Exportar los datos de precios de nivel

El siguiente ejemplo exporta datos de precios de nivel para un solo producto. A continuación, puede utilizar los datos exportados como plantilla para las importaciones masivas de datos de precios de nivel. Para obtener más información sobre cómo exportar datos de precios avanzados, consulte [Datos de precios avanzados](data-attributes-product.md#advanced-pricing-attributes).

![Precio por niveles del producto](./assets/price-tier-customer-group-discount.png){width="600" zoomable="yes"}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. En _[!UICONTROL Export Settings]_, establezca **[!UICONTROL Entity Type]**en `Advanced Pricing`.

1. En la cuadrícula **[!UICONTROL Entity Attributes]**, desplácese hacia abajo hasta los atributos de SKU y haga lo siguiente:

   - Para los precios de nivel basados en un porcentaje de descuento, introduzca el SKU de cada producto que desea exportar, separados por una coma.

     ![Exportación de datos - SKU del producto](./assets/price-tier-export-sku.png){width="600" zoomable="yes"}

   - Para los precios de nivel basados en una cantidad fija, introduzca el SKU de cada producto.

   - Desplácese hacia abajo y haga clic en **[!UICONTROL Continue]**.

1. Busque el archivo de exportación en la ubicación de descargas del explorador web y abra el archivo.

   ![Ejemplo: datos de precio de nivel de descuento de grupo de clientes exportados](./assets/price-tier-customer-group-discount-export.png){width="600" zoomable="yes"}

**_Datos de precios de nivel exportados_**

En los datos exportados se incluyen las siguientes columnas:

- `sku`
- `tier_price_website`
- `tier_price_customer_group`
- `tier_price_qty`
- `tier_price`
- `tier_price_value_type`

Los datos exportados se utilizan como plantilla para importar datos de precios de nivel.

## Paso 2: Actualización de los datos

1. Actualice los datos de precios de nivel para cada producto, según sea necesario.

   Cualquier producto sin actualizaciones de precios de nivel se puede eliminar del archivo CSV. No es necesario volver a importar productos que no hayan cambiado.

1. **[!UICONTROL Save]** el archivo CSV actualizado.

>[!NOTE]
>
>El tamaño de un archivo de importación no puede ser superior a 2 MB.

## Paso 3: Importación de los datos actualizados

1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. En _Importar configuración_, establezca **[!UICONTROL Entity Type]** en `Advanced Pricing`.

1. Establezca **[!UICONTROL Import Behavior]** en `Add/Update`.

1. En **[!UICONTROL File to Import]**, haga clic en **[!UICONTROL Choose File]** y seleccione el archivo que ha preparado para importar del directorio.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Check Data]**.

1. Si el archivo es válido, haga clic en **[!UICONTROL Import]**.

   De lo contrario, corrija cada problema con los datos que se enumeran en el mensaje e intente importar el archivo de nuevo.
