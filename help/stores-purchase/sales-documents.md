---
title: Documentos de ventas
description: Aprenda a configurar los documentos de ventas para satisfacer los pedidos de los clientes y la satisfacción de pedidos de su tienda Commerce.
exl-id: 869d79ca-688a-4032-a95c-c66ebf7f2775
feature: Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Documentos de ventas

Para dar soporte al flujo de trabajo de pedidos y proporcionar documentación a sus clientes sobre los pedidos que envían, configure los documentos de ventas relacionados para reflejar la marca de su tienda e incluir información de referencia.

## Configurar facturas y albaranes

A diferencia de las imágenes de logotipo utilizadas en las páginas de tienda, el logotipo de las facturas de PDF y otros documentos de venta puede ser una imagen de alta resolución y 300 ppp. Tenga cuidado de conservar la relación de aspecto al cambiar el tamaño del logotipo. Cambie el tamaño del logotipo para que se ajuste a la altura y no se preocupe por el espacio no utilizado a la derecha.

![Logotipo de muestra](./assets/logo-pdf.png){width="200"}

Una forma de cambiar el tamaño del logotipo para que se ajuste al tamaño requerido es crear una nueva imagen en blanco con las dimensiones correctas. A continuación, pegue la imagen del logotipo y cambie su tamaño para adaptarla a la altura. Con la mayoría de los programas de edición de imágenes, puede escalarla en un porcentaje para conservar la relación de aspecto o mantener pulsada la tecla Mayús y cambiar manualmente el tamaño de la imagen.

**_Para actualizar el logotipo:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Sales]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Invoice and Packing Slip Design]** y haga lo siguiente:

   ![Configuración de ventas - diseño de factura de ventas y albarán](../configuration-reference/sales/assets/sales-invoice-packing-slip-design.png){width="600" zoomable="yes"}

   - Para cargar **[!UICONTROL Logo for PDF Print-outs]**, haga clic en **[!UICONTROL Choose File]**, busque el logotipo que ha preparado y haga clic en **[!UICONTROL Open]**.

   - Para cargar **[!UICONTROL Logo for HTML Print View]**, haga clic en **[!UICONTROL Choose File]**, busque el logotipo que ha preparado y haga clic en **[!UICONTROL Open]**.

   - Escriba la dirección tal como desea que aparezca en las facturas y en los albaranes.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

   Como referencia, antes de cada campo aparece una miniatura de la imagen cargada. No se preocupe si la miniatura aparece distorsionada. La proporción del logotipo es correcta en la factura.

### Reemplazar una imagen

1. Haga clic en **[!UICONTROL Choose File]** y elija un archivo de logotipo diferente.

1. Seleccione la casilla de verificación **[!UICONTROL Delete Image]** de la imagen que desea reemplazar.

1. Haga clic en **[!UICONTROL Save Config]**.

### Formatos de imagen

| Formato | Requisitos |
|--- |------------------------------------------|
| **_PDF_** |  |
| Formato de archivo | JPG (JPEG), PNG, TIF (TIFF) |
| Tamaño de imagen | Hasta 1080 píxeles de ancho x 270 píxeles de alto |
| Resolución | Se recomiendan 300 PPP |
| **_HTML_** |  |
| Formato de archivo | JPG (JPEG), PNG, GIF |
| Tamaño de imagen | Determinado por tema. |
| Resolución | 72 o 96 ppp |

{style="table-layout:auto"}

## Añadir ID de referencia

El ID de pedido y la dirección IP del cliente se pueden incluir en el encabezado de los documentos de venta que acompañan a un pedido. De forma predeterminada, tanto el ID de pedido como la dirección IP del cliente aparecen en la cabecera de facturas, albaranes de envío y notas de abono.

![Configuración de ventas - impresiones de PDF](./assets/config-sales-pdf-print-outs.png){width="600" zoomable="yes"}

**_Para cambiar la configuración del identificador de pedido:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL PDF Print-outs]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **Factura**.

1. Establezca **[!UICONTROL Display Order ID in Header]** según sus preferencias.

1. Repita el proceso para las secciones **[!UICONTROL Shipment]** y **[!UICONTROL Credit Memo]**.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

**_Para cambiar la configuración de la dirección IP del cliente:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Sales]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL General]**.

   ![Configuración de ventas - configuración general de ventas](../configuration-reference/sales/assets/sales-general.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Hide Customer IP]** según sus preferencias.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
