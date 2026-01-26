---
title: Licencia de una imagen de Adobe Stock
description: Para garantizar que tenga acceso legal y eliminar la marca de agua de Adobe Stock, conceda una licencia a sus imágenes de Adobe Stock.
exl-id: a2d6b7b8-e9ac-4f3e-bcd1-05e2bb74b6c2
feature: CMS, Media
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Licencia de una imagen de Adobe Stock

Los recursos de Adobe Stock que desee utilizar para sus tiendas de producción de Adobe Commerce y Magento Open Source deben tener licencia. Esta licencia garantiza que tenga acceso legal a la imagen y que elimine la marca de agua de Adobe Stock que está presente en todas las [previsualizaciones de imagen](./adobe-stock-save-preview.md). Para obtener una licencia de imágenes o guardar imágenes con licencia, debe iniciar sesión en su cuenta de Adobe.

El nuevo [[!DNL Media Gallery]](media-gallery.md) proporciona una integración directa con Adobe Stock, lo que facilita la licencia de las imágenes directamente desde la página de la galería.

>[!BEGINSHADEBOX]

**Requisitos previos**

La característica de licencias de Adobe Stock solo está disponible si [Adobe Stock Integration](./adobe-stock.md) está instalado y configurado. Para autorizar [imágenes de Adobe Stock](https://stock.adobe.com) se necesita un plan Adobe Stock de pago y una [cuenta de Adobe](https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html).

>[!ENDSHADEBOX]

## Otorgar licencia a una imagen del nuevo [!DNL Media Gallery]

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Siga los pasos de [Uso de imágenes de Adobe Stock](./adobe-stock-manage.md) para iniciar sesión y guardar imágenes de vista previa en el [almacenamiento de medios](./media-storage.md).

   ![Imagen de vista previa guardada](./assets/adobe-stock-gallery-unlicensed.png){width="600" zoomable="yes"}

1. Haga clic en los tres puntos situados debajo de la imagen (![icono del menú de recursos](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}) y, a continuación, haga clic en **[!UICONTROL License]**.

   ![Acciones de imagen de Adobe Stock](./assets/adobe-stock-gallery-image-actions.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si no ha iniciado sesión, aparecerá el formulario de inicio de sesión. Para obtener más información sobre el inicio de sesión, consulte [Uso de imágenes de Adobe Stock](./adobe-stock-manage.md).

1. En el cuadro de diálogo de confirmación de licencia, haga clic en **[!UICONTROL Confirm]** para obtener la licencia de la imagen.

   ![Confirmación de licencia](./assets/adobe-stock-gallery-license-confirm.png){width="350" zoomable="yes"}

   >[!NOTE]
   >
   >Debe tener [créditos de Adobe Stock](https://helpx.adobe.com/stock/help/credit-packs.html) disponibles en su cuenta para autorizar la imagen.

## Otorgar licencia a una imagen desde el almacenamiento de medios estándar

1. [Acceder a la cuadrícula de búsqueda de Adobe Stock][adobe-stock-manage.md].

1. Para [ver los detalles de la imagen][adobe-stock-manage.md#view-image-details], haga clic en una imagen de la cuadrícula de búsqueda en orden.

1. Según el estado de licencia actual de la imagen, realice una de las siguientes acciones:

   - Si la imagen ya tiene licencia, haga clic en **[!UICONTROL Save]**.

   - Si la imagen tiene licencia para _not_, haga clic en **[!UICONTROL License and Save]**.

     >[!NOTE]
     >
     >Debe tener [créditos de Adobe Stock](https://helpx.adobe.com/stock/help/credit-packs.html) disponibles en su cuenta para autorizar la imagen.

   Esta acción muestra una solicitud para que especifique un nombre de archivo que se use para guardar la imagen en el [almacenamiento de medios](./media-storage.md). Se proporciona un nombre de archivo predeterminado, pero puede personalizarlo según sus preferencias.

   ![Guardar imagen con licencia de Adobe Stock](./assets/adobe-stock-save-licensed.png){width="550" zoomable="yes"}

1. Haga clic en **[!UICONTROL Confirm]**.

   La página redirige al almacenamiento de medios y se muestra la previsualización guardada.
