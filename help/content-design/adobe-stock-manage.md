---
title: Uso de imágenes de Adobe Stock
description: Mejore las páginas de su tienda con imágenes de Adobe Stock.
exl-id: 8f7d6f0a-511f-4f4b-821d-10a06e18041e
feature: CMS, Media
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 0%

---

# Uso de imágenes de Adobe Stock

Se pueden usar [imágenes de Adobe Stock](https://stock.adobe.com) en lugar de cargar el contenido de tu propia imagen. Un caso de uso común es cargar y colocar contenido de imagen al crear una página.

[[!DNL Media Gallery]](media-gallery.md) proporciona una integración directa con Adobe Stock, lo que facilita la obtención de licencias de las imágenes directamente desde la página de la galería.

## Acceso a la cuadrícula de búsqueda de Adobe Stock

Se puede acceder al panel de búsqueda de Adobe Stock al [agregar o editar una página](page-add.md), al [crear o editar una categoría](../catalog/category-create.md) o al [insertar imágenes mediante el editor de contenido](editor-insert-image.md).

**_Para buscar recursos de Adobe Stock y agregar una imagen de archivo a una página:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Haga clic en **[!UICONTROL Add a New Page]**.

   Si desea editar una página existente, puede usar la columna _[!UICONTROL Action]_para hacer clic en **[!UICONTROL Select]**y elegir **[!UICONTROL Edit]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Content]** y haga lo siguiente:

   - Si tiene habilitado [WYSIWYG editor](editor.md), haga clic en **[!UICONTROL Show/Hide Editor]** y luego en **[!UICONTROL Insert Image]**.

   - Si tiene [Page Builder habilitado](../page-builder/setup.md), expanda el panel **[!UICONTROL Media]** y arrastre un marcador de posición **[!UICONTROL Image]** al contenedor de destino. Luego haga clic en **[!UICONTROL Select from Gallery]**.

     ![Arrastrando una imagen a la fase de Page Builder](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Search Adobe Stock]**.

**_Para buscar recursos de Adobe Stock y agregar una imagen de archivo a una categoría:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Haga clic en **[!UICONTROL Add Root Category]** o **[!UICONTROL Add Subcategory]**.

   Si desea agregar la imagen a una categoría existente, haga clic en el nombre de la categoría en la lista de la izquierda.

1. Expanda la sección **[!UICONTROL Content]** y en _[!UICONTROL Category Image]_haga clic en **[!UICONTROL Select from Gallery]**.

1. Haga clic en **[!UICONTROL Search Adobe Stock]**.

Para buscar recursos de Adobe Stock y agregar una imagen estándar desde el Editor de WYSIWYG:

1. haga clic en **[!UICONTROL Show/Hide Editor]**.

1. Haga clic en **[!UICONTROL Insert Image]**.

1. Haga clic en **[!UICONTROL Search Adobe Stock]**.

   ![Resultados de búsqueda de Adobe Stock](./assets/adobe-stock-search-grid.png){width="600" zoomable="yes"}

## Filtrado y búsqueda de recursos de Adobe Stock

La [cuadrícula de búsqueda de Adobe Stock](#access-the-adobe-stock-search-grid) proporciona funcionalidad de consulta y filtrado para ayudarle a encontrar la imagen perfecta para sus tiendas de [!DNL Commerce].

De forma predeterminada, los resultados de búsqueda mostrados proceden de una galería depurada por Adobe Stock de unos cientos de resultados. Al aplicar su propia búsqueda de palabras clave, está buscando en los millones de recursos disponibles a través de Adobe Stock.

### Buscar recursos de Adobe Stock por palabras clave

1. [Acceder a la cuadrícula de búsqueda de Adobe Stock](#access-the-adobe-stock-search-grid).

1. Escriba su búsqueda de palabras clave en el campo de entrada **[!UICONTROL Search by keyword]** en la parte superior izquierda y haga clic en la lupa o presione **Entrar**.

   ![Resultados de búsqueda de Adobe Stock para la palabra clave &quot;mango&quot;](./assets/adobe-stock-search-keyword.png){width="600" zoomable="yes"}

### Filtrar recursos de Adobe Stock

1. [Ejecute una búsqueda de palabras clave en los recursos de Adobe Stock](#search-for-adobe-stock-assets-by-keywords).

1. Haga clic en **[!UICONTROL Filters]**.

   Hay varios filtros disponibles para restringir los resultados de búsqueda:

   | Filtrar | Descripción |
   |---|---|
   | [!UICONTROL Subcategory] | Filtra por imágenes que sean **Fotos** o **Ilustraciones** |
   | [!UICONTROL Orientation] | Filtrar imágenes por tamaño, forma y aspecto |
   | [!UICONTROL Color] | Uso de una paleta de colores para filtrar imágenes por color |
   | [!UICONTROL Price] | Filtro de imágenes según su coste |
   | [!UICONTROL Safe search] | Habilitar o deshabilitar la búsqueda segura |
   | [!UICONTROL Isolated Assets] | Limite la visualización únicamente a _recursos aislados_, que tienen sujetos que aparecen solos en un fondo sólido |

   {style="table-layout:auto"}

   ![Filtros de búsqueda de Adobe Stock](./assets/adobe-stock-filters.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Apply Filters]**.

   La cuadrícula de resultados de la búsqueda se actualiza con la búsqueda refinada.

## Ver detalles de la imagen

Cada imagen tiene detalles disponibles para su visualización. A través de esta vista detallada, hay disponibles más acciones específicas para la imagen, como [guardar vistas previas de imágenes](adobe-stock-save-preview.md) o [guardar (y, opcionalmente, autorizar) imágenes](adobe-stock-license-image.md).

1. [Acceder a la cuadrícula de búsqueda de Adobe Stock](#access-the-adobe-stock-search-grid).

1. Haga clic en una imagen de los resultados de búsqueda.

   Se muestran más detalles de la imagen, como:

   - Una versión más grande de la imagen
   - Metadatos de imagen, como _[!UICONTROL Dimensions]_,_[!UICONTROL File type]_, _[!UICONTROL Category]_,_[!UICONTROL File]_ y _palabras clave_
   - Imágenes relacionadas, como imágenes de la misma _serie_ o _modelo_
   - Botones de acción, como [[!UICONTROL Save Preview]](adobe-stock-save-preview.md) y [[!UICONTROL Save (and optionally license) Image]](adobe-stock-license-image.md)

     ![Detalles de la imagen de Adobe Stock](./assets/adobe-stock-image-details.png){width="600" zoomable="yes"}

## Inicie sesión en su cuenta de Adobe

Para obtener acceso completo a una imagen y eliminar la marca de agua de Adobe Stock, debe [iniciar sesión con una cuenta de Adobe](https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html) y comprar créditos para obtener derechos de licencia para utilizar una imagen.

1. [Acceder a la cuadrícula de búsqueda de Adobe Stock](#access-the-adobe-stock-search-grid).

1. Haga clic en **[!UICONTROL Sign In]** en la parte superior derecha.

   Una nueva ventana del explorador lo guiará a través del [proceso de inicio de sesión de Adobe](https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html).

   Después de completar el proceso de inicio de sesión, el estado de licencia de las imágenes se muestra en los resultados de búsqueda como una etiqueta.

   ![Adobe inició sesión](./assets/adobe-stock-account-login.png){width="600" zoomable="yes"}

### Ver el estado con licencia de los resultados de búsqueda

[Inicia sesión en tu cuenta de Adobe](#log-in-to-your-adobe-account).

Todas las imágenes con licencia asociadas a su cuenta de Adobe tienen una etiqueta mostrada, lo que deja claro qué imágenes tiene licencia.

![Resultados de búsqueda de Adobe Stock con imágenes con licencia](./assets/adobe-stock-licensed-images.png){width="600" zoomable="yes"}

### Guardar imágenes en el almacenamiento de medios

Las imágenes buscadas mediante la integración de Adobe Stock se pueden guardar en el [!DNL Commerce] [almacenamiento de medios](media-storage.md) para facilitar su reutilización en toda la tienda [!DNL Commerce].

Puede guardar dos tipos de imágenes: una [vista previa de imagen](adobe-stock-save-preview.md) o una [imagen con licencia](adobe-stock-license-image.md).

#### Guardar una previsualización de imagen

Una previsualización de imagen es una versión con marca de agua de un recurso de Adobe Stock. Las vistas previas de imágenes son gratuitas y son una buena manera de experimentar con diferentes imágenes antes de decidir comprar una licencia para imágenes específicas y utilizarlas en sus tiendas de producción.

1. [Acceder a la cuadrícula de búsqueda de Adobe Stock](#access-the-adobe-stock-search-grid).

1. Para [ver los detalles de la imagen](#view-image-details), haga clic en una imagen en la cuadrícula de búsqueda.

1. Haga clic en **[!UICONTROL Save Preview]**.

   Esta acción muestra una solicitud para que especifique un nombre de archivo que se utilice para guardar la imagen en el almacenamiento de medios. Se proporciona un nombre de archivo predeterminado, pero puede personalizarlo según sus preferencias.

   ![Guardar imagen de vista previa de Adobe Stock](./assets/adobe-stock-save-preview.png){width="500" zoomable="yes"}

1. Haga clic en **[!UICONTROL Confirm]**.

   La página redirige al almacenamiento de medios y se muestra la previsualización guardada.

#### Guardar una imagen con licencia

Los recursos de Adobe Stock que desee usar en las tiendas de producción [!DNL Commerce] deben tener licencia. Las licencias garantizan que tenga acceso legal a la imagen y que pueda eliminar la marca de agua de Adobe Stock que está presente en todas las [vistas previas de imágenes](adobe-stock-save-preview.md). Para obtener una licencia de imágenes o guardar imágenes con licencia, debe iniciar sesión en su cuenta de Adobe.

1. [Inicia sesión en tu cuenta de Adobe](#log-in-to-your-adobe-account).

1. Para [ver los detalles de la imagen](#view-image-details), haga clic en una imagen en la cuadrícula de búsqueda.

1. Según el estado de licencia actual de la imagen, realice una de las siguientes acciones:

   - Si la imagen ya tiene licencia, haga clic en **[!UICONTROL Save]**.

   - Si la imagen tiene licencia para _not_, haga clic en **[!UICONTROL License and Save]**.

     >[!NOTE]
     >
     >Debe tener [créditos de Adobe Stock](https://helpx.adobe.com/stock/help/credit-packs.html) disponibles en su cuenta para autorizar la imagen.

   Esta acción muestra una solicitud para que especifique un nombre de archivo que se use para guardar la imagen en el [almacenamiento de medios](media-storage.md). Se proporciona un nombre de archivo predeterminado, pero puede personalizarlo según sus preferencias.

1. Haga clic en **[!UICONTROL Confirm]**.

   La página redirige al almacenamiento de medios y se muestra la previsualización guardada.
