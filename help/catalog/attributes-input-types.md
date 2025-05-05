---
title: Tipos de entrada de atributos
description: Obtenga información sobre los tipos de entrada disponibles para los atributos de producto, que determinan el tipo de datos que se pueden introducir y el formato del campo o control de entrada.
exl-id: c35b3b9d-57b0-4c33-abdb-662ac6d0260e
feature: Catalog Management, Products
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Tipos de entrada de atributos

Cuando se ven desde el Administrador, los atributos son los campos que se completan al crear un producto. El tipo de entrada asignado a un atributo determina el tipo de datos que se pueden introducir y el formato del campo o control de entrada. Desde el punto de vista del cliente, los atributos proporcionan información sobre el producto y son las opciones y los campos de entrada de datos que deben rellenarse para comprar un producto.

## Tipos de entrada

| Propiedad | Descripción |
|--- |--- |
| [!UICONTROL Text Field] | Campo de entrada de una sola línea para texto. |
| [!UICONTROL Text Area] | Campo de entrada de varias líneas para introducir párrafos de texto, como una descripción del producto. Puede utilizar el Editor WYSIWYG para dar formato al texto con etiquetas de HTML o introducirlas directamente en el texto. |
| [!UICONTROL Text Editor] | Un editor de texto que funcione completamente en la ubicación del atributo. |
| [!UICONTROL Date] | Muestra un valor de fecha en el [formato preferido](#date-and-time-options) y en la [zona horaria](../getting-started/store-details.md#locale-options). Los valores de fecha se pueden seleccionar de una lista o un calendario ( ![Icono de calendario](../assets/icon-calendar.png)). <br/><br/>**_Nota:_**&#x200B;Según la configuración del sistema, los usuarios de_Admin _pueden introducir fechas directamente en un campo o seleccionar una fecha del calendario o lista. Para obtener información acerca de cómo especificar valores de fecha y hora, vea [Opciones de fecha y hora](#date-and-time-options). |
| [!UICONTROL Date and Time] | Muestra un valor de fecha y hora en el [formato preferido](#date-and-time-options) y en la [zona horaria](../getting-started/store-details.md#locale-options). La fecha y la hora se pueden introducir manualmente o seleccionar desde un calendario. Formato de ejemplo: MM/DD/AAAA HH:MM |
| [!UICONTROL Yes/No] | Muestra una lista desplegable con opciones predefinidas de `Yes` y `No`. |
| Desplegable | Muestra una lista desplegable de valores que solo acepta una selección. El tipo de entrada desplegable es un componente clave de [productos configurables](../catalog/product-create-configurable.md). |
| [!UICONTROL Multiple Select] | Muestra una lista desplegable de valores que acepta varias selecciones. |
| [!UICONTROL Price] | Este tipo de entrada se usa para crear campos de precio que se agregan a los atributos predefinidos: `Price`, `Special Price`, `Tier Price` y `Cost`. La moneda utilizada viene determinada por la configuración del sistema. |
| [!UICONTROL Media Image] | Asocia una imagen adicional a un producto, como un logotipo de producto, instrucciones de cuidado o ingredientes de una etiqueta de alimentos. Cuando se agrega un atributo de imagen multimedia al conjunto de atributos de un producto, se convierte en un tipo de imagen adicional, junto con Base, Pequeño y Miniatura. El atributo de imagen multimedia se puede excluir del [explorador multimedia de tienda](catalog-images-video.md#storefront-media-browser). |
| [!UICONTROL Fixed Product Tax] | Le permite definir [tarifas de FTP](../stores-purchase/fixed-product-tax.md) según los requisitos de su configuración regional. |
| [!UICONTROL Visual Swatch] | Muestra una muestra que muestra el color, la textura o el motivo de un producto configurable. Una [muestra visual](swatches.md) se puede rellenar con un valor de color hexadecimal o mostrar una imagen cargada que represente el color, el material, la textura o el motivo de la opción. |
| [!UICONTROL Text Swatch] | Representación basada en texto de una opción de producto configurable que se utiliza frecuentemente para el tamaño. [Las muestras de texto](swatches.md) también pueden incluir valores de color hexadecimales. |
| [!UICONTROL Page Builder] | Un área de trabajo [[!DNL Page Builder]](../page-builder/workspace.md) en la ubicación del atributo que facilita la adición de contenido atractivo a la página de producto. |

{style="table-layout:auto"}

## Opciones de fecha y hora

Puede personalizar el formato de los campos de fecha y hora y seleccionar el control de entrada que se utiliza para la entrada de datos. Los valores de fecha se pueden seleccionar de una lista desplegable o de un calendario emergente.

![Ejemplo: calendario emergente de tienda](./assets/storefront-popup-calendar.png){width="700" zoomable="yes"}

**_Para dar formato a los campos de fecha y hora:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel de la izquierda, expanda **[!UICONTROL Catalog]** y haga clic en el subelemento **[!UICONTROL Catalog]**.

1. Expanda la sección **[!UICONTROL Date & Time Custom Options]**.

   ![Configuración del catálogo: opciones de fecha y hora](../configuration-reference/catalog/assets/catalog-date-time-custom-options.png){width="600" zoomable="yes"}

   Para obtener una lista detallada de estas opciones, consulte [_Opciones personalizadas de fecha y hora_](../configuration-reference/catalog/catalog.md) en la _Referencia de configuración_.

1. Para usar un calendario emergente como control de entrada para los campos de fecha, establezca **[!UICONTROL Use JavaScript Calendar]** en `Yes`.

1. Para establecer **[!UICONTROL Date Fields Order]**, establezca el orden de cada parte del campo de fecha según sea necesario:

   - Mes
   - Día
   - Año

1. Para establecer el formato de hora preferido, establezca **Formato de hora** en uno de los siguientes:

   - `12h AM/PM`
   - `24h`

1. Para establecer **[!UICONTROL Year Range]** para los valores desplegables, escriba el año (AAAA) para establecer las fechas **[!UICONTROL from]** y **[!UICONTROL to]**.

   Si está en blanco, el valor predeterminado del campo es el año actual.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
