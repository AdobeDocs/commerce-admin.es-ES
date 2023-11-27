---
title: Localización de tiendas
description: Obtenga información sobre cómo localizar una tienda o vista de tienda.
exl-id: 64e1b431-f599-444c-9d39-207bb95f0400
topic: Commerce, Localization
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Localización de tiendas

La mayor parte del texto que parece estar codificado en las páginas de la tienda se puede cambiar instantáneamente a un idioma diferente cambiando la configuración regional de la vista. Cambiar la configuración regional no traduce realmente el texto palabra por palabra, sino que simplemente hace referencia a una tabla de traducción diferente que proporciona el texto de la interfaz que se utiliza en todo el almacén. El texto que se puede cambiar incluye títulos de navegación, etiquetas, botones y vínculos como _Mi carro_ y _Mi cuenta_. También puede utilizar la variable [Traducción en línea](../configuration-reference/advanced/developer.md) herramienta para retocar texto en la interfaz.

Los paquetes de idiomas se encuentran en [Traducciones y localización][1]{:target=&quot;_blank&quot;} en el Commerce Marketplace. Las nuevas extensiones se añaden continuamente al Marketplace, por lo que vuelva a consultarlas con frecuencia.

## Paso 1: Instalar un paquete de idioma

Siga las instrucciones estándar para instalar la extensión del paquete de idioma. Para obtener información detallada sobre la instalación de una extensión, consulte [Instalación general de CLI][2] en el _Guía de extensiones_.

## Paso 2: Crear una vista de tienda para el idioma

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Haga clic **[!UICONTROL Create Store View]**.

1. Defina las opciones para la nueva vista de tienda:

   - **[!UICONTROL Store]** — elija el almacén que es el padre de la vista.

   - **[!UICONTROL Name]** — introduzca un nombre para la vista de tienda. Por ejemplo: portugués.

     En el encabezado del almacén, el nombre aparece en la variable _selector de idioma_.

   - **[!UICONTROL Code]** — introduzca un código en minúsculas para identificar la vista. Por ejemplo: `portuguese`.

   - **[!UICONTROL Status]** — Para activar la vista, defina como `Enabled`.

   - **[!UICONTROL Sort Order]** — (Opcional) Introduzca un número para determinar la secuencia en la que esta vista se muestra con otras vistas.

1. Cuando termine, haga clic en **[!UICONTROL Save Store View]**.

## Paso 3: cambiar la configuración regional de la vista de la tienda

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En la esquina superior izquierda, establezca **[!UICONTROL Store View]** a la vista específica donde se aplicará la configuración.

1. Cuando se le pida que confirme el cambio de ámbito, haga clic en **[!UICONTROL OK]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Locale Options]** sección.

1. Borre la **[!UICONTROL Use Website]** casilla de verificación y definir **[!UICONTROL Locale]** al idioma que desee asignar a la vista.

   Si hay varias variaciones del idioma disponible, asegúrese de elegir el de la región o dialecto específico.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

   Después de cambiar el idioma de la configuración regional, el contenido restante que ha creado, incluidos los nombres y descripciones de productos y las categorías, [CMS](../content-design/page-translate.md) las páginas y los bloques deben traducirse por separado para cada vista de tienda.

## Localizar productos

Si la tienda tiene varias vistas en diferentes idiomas, los mismos productos estarán disponibles en cada vista de tienda. Puede utilizar la misma información básica del producto, como SKU, precio y nivel de inventario, independientemente del idioma. A continuación, traduzca solo el nombre del producto, los campos de descripción y los metadatos según sea necesario para cada idioma.

### Paso 1: Traducir campos de producto

1. En el _Administrador_ barra lateral, vaya a  **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. En la cuadrícula, busque el producto que desea traducir y ábralo en modo de edición.

1. En la esquina superior izquierda, establezca **[!UICONTROL Store View]** Vaya a la vista para la traducción y haga clic en **[!UICONTROL OK]** cuando se le pida que confirme.

1. Para cada campo que desea editar, haga lo siguiente:

   - Anule la selección de **[!UICONTROL Use Default Value]** a la derecha del campo.

   - Pegue o escriba el texto traducido en el campo.

   Asegúrese de traducir todos los campos de texto, incluidos los siguientes [imagen](../catalog/catalog-images-video.md) etiquetas y texto alternativo, [Optimización del motor de búsqueda](../catalog/product-search-engine-optimization.md) campos y cualquier [Opciones personalizadas](../catalog/settings-advanced-custom-options.md) información.

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

### Paso 2: Traducir etiquetas de campo

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. En la lista, busque el atributo que desea traducir y abra en modo de edición.

1. En el panel izquierdo, elija **[!UICONTROL Manage Labels]**.

1. En el _[!UICONTROL Manage Titles]_, introduzca una etiqueta traducida para cada vista de tienda.

   ![Introducir etiquetas traducidas](./assets/product-attribute-labels-translate.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save Attribute]**.

### Paso 3: Traducir todas las categorías

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **Categorías**.

1. En la esquina superior izquierda, establezca **[!UICONTROL Store View]** Vaya a la vista para la traducción y haga clic en **[!UICONTROL OK]** cuando se le pida que confirme.

1. En el árbol, busque la categoría que desea traducir y ábrala en modo de edición.

1. Para _Información básica_, traducir **[!UICONTROL Category Name]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el _[!UICONTROL Content]_sección y traducción **[!UICONTROL Description]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Search Engine Optimization Settings]** y traduzca los campos siguientes:

   - **[!UICONTROL Meta Title]**
   - **[!UICONTROL Meta Keywords]**
   - **[!UICONTROL Meta Description]**

1. En el _[!UICONTROL Search Engine Optimization Settings]_, haga lo siguiente para traducir el **[!UICONTROL URL Key]**:

   - Borre la **[!UICONTROL Use Default Value]** a la derecha del campo.

   - Introduzca el texto traducido.

   - Asegúrese de que la variable **[!UICONTROL Create Permanent Redirect for old URL]** La casilla de verificación está seleccionada.

   ![Traducir la clave URL](./assets/category-translate-url-key.png)

1. Cuando termine, haga clic en **[!UICONTROL Save Category]**.

1. Repita el proceso para todas las categorías utilizadas en la tienda.

### Paso 4: Traducir atributos y opciones de atributos del producto

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Seleccione el atributo que desea traducir.

1. Elegir **[!UICONTROL Manage Labels]** a la izquierda y configure el **[!UICONTROL Managed Titles]** opciones para definir las traducciones del título del atributo.

1. Elegir **[!UICONTROL Properties]** a la izquierda e introduzca las opciones de atributo traducidas en **[!UICONTROL Manage Options]** sección.

   ![Administrar opciones](./assets/manage-option-tab.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save Attribute]**.


[1]: https://marketplace.magento.com/extensions/content-customizations/translations-localization.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html
