---
title: Licencia de una imagen de Adobe Stock
description: Para garantizar que tenga acceso legal y eliminar la marca de agua de Adobe Stock, conceda una licencia a sus imágenes de Adobe Stock.
exl-id: a2d6b7b8-e9ac-4f3e-bcd1-05e2bb74b6c2
feature: CMS, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Licencia de una imagen de Adobe Stock

Los recursos de Adobe Stock que desee utilizar para sus tiendas de producción de Adobe Commerce y Magento Open Source deben disponer de licencia. Esta licencia garantiza que tenga acceso legal a la imagen y que elimine la marca de agua de Adobe Stock que está presente en todas las [previsualizaciones de imagen][save-preview]. Para obtener una licencia de imágenes o guardar imágenes con licencia, debe iniciar sesión en su cuenta de Adobe.

El nuevo [[!DNL Media Gallery]](media-gallery.md) proporciona una integración directa con Adobe Stock, lo que facilita la licencia de las imágenes directamente desde la página de la galería.

## Requisitos previos

Esta función requiere lo siguiente [Integración de Adobe Stock][adobe-stock-integration] módulo y configuración. Licencias [Adobe Stock][adobe-stock] images requiere un plan Adobe Stock de pago y una [cuenta Adobe][adobe-signin].

## Otorgar licencia a una imagen del nuevo [!DNL Media Gallery]

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Siga los pasos de [Uso de imágenes de Adobe Stock][using-adobe-stock] para iniciar sesión y guardar imágenes de vista previa en [almacenamiento de medios][media-storage].

   ![Imagen de vista previa guardada](./assets/adobe-stock-gallery-unlicensed.png){width="600" zoomable="yes"}

1. Haga clic en los tres puntos situados debajo de la imagen (![Icono de menú de recursos](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}) y haga clic en **[!UICONTROL License]**.

   ![Acciones de imagen de Adobe Stock](./assets/adobe-stock-gallery-image-actions.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si no ha iniciado sesión, aparecerá el formulario de inicio de sesión. Para obtener más información sobre el inicio de sesión, consulte [Uso de imágenes de Adobe Stock][using-adobe-stock].

1. En el cuadro de diálogo de confirmación de licencia, haga clic en **[!UICONTROL Confirm]** para autorizar la imagen.

   ![Confirmación de licencia](./assets/adobe-stock-gallery-license-confirm.png){width="350" zoomable="yes"}

   >[!NOTE]
   >
   >Debe tener disponible [Créditos de Adobe Stock][stock-credits] en su cuenta para autorizar la imagen.

## Otorgar licencia a una imagen desde el almacenamiento de medios estándar

1. [Acceso a la cuadrícula de búsqueda de Adobe Stock][access-search].

1. Hasta [ver los detalles de la imagen][view-details], haga clic en una imagen de la cuadrícula de búsqueda en orden.

1. Según el estado de licencia actual de la imagen, realice una de las siguientes acciones:

   - Si la imagen ya tiene licencia, haga clic en **[!UICONTROL Save]**.

   - Si la imagen es _no_ con licencia, haga clic en **[!UICONTROL License and Save]**.

     >[!NOTE]
     >
     >Debe tener disponible [Créditos de Adobe Stock][stock-credits] en su cuenta para autorizar la imagen.

   Esta acción muestra una solicitud para que especifique un nombre de archivo que se utilice para guardar la imagen en [almacenamiento de medios][media-storage]. Se proporciona un nombre de archivo predeterminado, pero puede personalizarlo según sus preferencias.

   ![Guardar imagen con licencia de Adobe Stock](./assets/adobe-stock-save-licensed.png){width="550" zoomable="yes"}

1. Haga clic **[!UICONTROL Confirm]**.

   La página redirige al almacenamiento de medios y se muestra la previsualización guardada.

[adobe-stock-integration]: adobe-stock.md
[media-storage]: media-storage.md
[using-adobe-stock]: adobe-stock-manage.md
[save-preview]: adobe-stock-save-preview.md
[access-search]: adobe-stock-manage.md#access-the-adobe-stock-search-grid
[view-details]: adobe-stock-manage.md#view-image-details
[stock-credits]: https://helpx.adobe.com/stock/help/credit-packs.html
[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
