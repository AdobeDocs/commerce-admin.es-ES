---
title: Agregar un origen de inventario
description: Aprenda a crear un origen para una ubicación, como un almacén, una tienda física, un centro de distribución o un transportista directo.
exl-id: 1bff9986-8722-4fb5-ac83-41de82325f7b
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 0%

---

# Añadir una fuente

Administre el inventario y la satisfacción de pedidos desde varias ubicaciones con fuentes personalizadas. Cree una fuente para cada ubicación, como almacenes, tiendas físicas, centros de distribución y empresas de envío directo. Asignación de orígenes y actualización de cantidades por producto

Si edita el origen predeterminado, puede editar todas las configuraciones excepto el nombre y el código. Se recomienda que los comerciantes de un solo origen agreguen información que coincida con su ubicación.

## Agregar un origen de inventario

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Haga clic **[!UICONTROL Add New Source]**.

   ![Administrar fuentes](assets/inventory-sources.png)

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL General]** y haga lo siguiente:

   - Para identificar el origen del inventario, introduzca un valor único **[!UICONTROL Name]**.

   - Introduzca un único **[!UICONTROL Code]**.

     El código admite letras mayúsculas y minúsculas, números, guiones y guiones bajos. El código es un ID único que se utiliza al asignar a stock y exportar e importar datos.

   - Si este origen de inventario está listo para usarse, establezca **[!UICONTROL Is Enabled]** hasta `Yes`.

   - Escriba una descripción breve **[!UICONTROL Description]** para esta ubicación, para obtener una referencia rápida o más detalles.

   - Para **[!UICONTROL Latitude]** y **[!UICONTROL Longitude]**, introduzca las coordenadas del Sistema de posicionamiento global (GPS) de la ubicación de la instalación.

     Para encontrar las coordenadas GPS con [Mapas de Google][1], introduzca la dirección en el cuadro de búsqueda. Haga clic con el botón derecho en el marcador del mapa y elija **[!UICONTROL What's here?]**. Las coordenadas GPS aparecen en el cuadro de detalles debajo de la dirección.

     ![Opciones generales de origen](assets/inventory-source-general.png)

   - Si este origen de inventario es una ubicación de recogida, establezca **[!UICONTROL Use as Pickup Location]** hasta `Yes`.

     El origen predeterminado no se puede usar como ubicación de recogida para pedidos de recogida en tienda.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Contact Info]** y haga lo siguiente:

   - Para **[!UICONTROL Contact Name]**, introduzca el nombre completo del contacto principal en la ubicación.

   - Introduzca una **[!UICONTROL Email]** dirección para ponerse en contacto con la ubicación.

   - Para **[!UICONTROL Phone]**, introduzca el código de área y el número de teléfono.

   - Para **[!UICONTROL Fax]**, introduzca el código de área y el número de teléfono del fax, si está disponible.

     ![Información de contacto](assets/inventory-source-contact-info.png)

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Address Data]** y haga lo siguiente:

   - Elija la **[!UICONTROL Country]**.

   - Para **[!UICONTROL State/Province]**, introduzca la abreviatura estándar para el estado o la provincia.

   - Introduzca el **[!UICONTROL City]**.

   - Introduzca el físico **[!UICONTROL Street]** dirección.

   - Para **[!UICONTROL Postcode]**, introduzca el código postal.

     ![Datos de dirección](assets/inventory-source-address.png)

1. Si establece el origen como ubicación de recogida en el paso anterior, expanda ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Pickup Location]** y proporcione información descriptiva sobre la ubicación:

   - Introduzca el **[!UICONTROL Frontend Name]** de la ubicación de recogida.

   - Introduzca una **[!UICONTROL Frontend Description]** de la ubicación de recogida. Utilice este cuadro de texto para mostrar las horas de la tienda, la ubicación relativa a otros puntos de referencia u otra información útil que ayude al cliente a seleccionar la ubicación de recogida correcta.

     ![Ubicación de recogida](assets/inventory-pickup-location.png)

   Para obtener más información sobre cómo configurar las notificaciones por correo electrónico al utilizar un origen como ubicación de recogida, consulte [Correos electrónicos de ventas](../configuration-reference/sales/sales-emails.md) en el _Guía de referencia de configuración_.

1. Para guardar el trabajo, realice una de las siguientes acciones:

   - Para guardar el trabajo y seguir editando, haga clic en **[!UICONTROL Save & Continue]**.

   - Para guardar su trabajo y volver a la página Administrar fuentes, haga clic en la flecha abajo (![Flecha de menú](../assets/icon-menu-down-arrow-red.png)) y elija **[!UICONTROL Save & Close]**.

   - Para guardar el trabajo en el registro de origen actual e introducir un nuevo origen, elija **[!UICONTROL Save & New]**.

## Barra de botones

| Botón | Descripción |
|--|--|
| [!UICONTROL Back] | Vuelve a la página Administrar fuentes. |
| [!UICONTROL Reset] | Restaura todos los campos del formulario a sus valores en el momento de la última vez que se guardaron. |
| [!UICONTROL Save & Continue] | Guarda todos los cambios y mantiene el formulario abierto para seguir editándolo. Haga clic en la flecha hacia abajo para ver opciones adicionales:<br/>**[!UICONTROL Save & Close]**: Guarda los cambios realizados en el registro actual, cierra el formulario y vuelve a la página Administrar orígenes.<br/>**[!UICONTROL Save & New]** - Guarda los cambios, cierra el registro actual y abre un nuevo formulario en blanco. |

## Descripciones de campos

| Campo | Descripción |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | (Obligatorio) Un nombre único que identifica el origen de inventario para los usuarios administradores. |
| [!UICONTROL Code] | (Obligatorio) Un código alfanumérico único que utiliza el sistema para identificar el origen del inventario. Introduzca el código en caracteres en mayúsculas o minúsculas y/o números, sin espacios. Si es necesario, se puede utilizar un guion o un guion bajo en lugar de un espacio. El código no se puede editar después de crear el origen. Se trata de un ID único que se utiliza al asignar fuentes a las existencias y exportar o importar datos de productos. |
| [!UICONTROL Is Enabled] | Determina si el origen de inventario está disponible para utilizarse. Opciones: Sí / No |
| [!UICONTROL Description] | Breve descripción de la ubicación de origen del inventario. Incluya detalles útiles para los usuarios administradores. |
| [!UICONTROL Latitude] | Especifica la coordenada de latitud del origen de inventario para GPS. Introduzca el valor como un número, precedido por un signo más o menos según sea necesario. No se permiten el símbolo de grado ni las letras. Por ejemplo: Latitude 32.7555 |
| [!UICONTROL Longitude] | Especifica la coordenada de longitud del origen de inventario para GPS. Introduzca el valor como un número, precedido por un signo más o menos según sea necesario. No se permiten el símbolo de grado ni las letras. Por ejemplo: `-97.3308` |
| **[!UICONTROL Contact Info]** | |
| [!UICONTROL Contact Name] | Nombre del contacto principal en la ubicación de origen de inventario. |
| [!UICONTROL Email] | Correo electrónico del contacto principal. |
| [!UICONTROL Phone] | El código de área y el número de teléfono del contacto principal, utilizando el formato que prefiera. Por ejemplo: `(123) 456-7890` o `123-456-7890` |
| [!UICONTROL Fax] | El código de área y el número de fax del contacto principal. |
| **[!UICONTROL Address Data]** | |
| [!UICONTROL Country] | (Obligatorio) El país donde se encuentra el origen del inventario. |
| [!UICONTROL State/Province] | Estado o provincia donde se encuentra el origen de inventario. |
| [!UICONTROL City] | Ciudad donde se encuentra el origen del inventario. |
| [!UICONTROL Street] | La dirección de la calle del origen de inventario. |
| [!UICONTROL Postcode] | (Obligatorio) El código postal del origen de inventario. |
| **[!UICONTROL Pickup Location]** | |
| [!UICONTROL Frontend Name] | Nombre de la ubicación de recogida del origen que se muestra en la tienda. |
| [!UICONTROL Frontend Description] | La descripción de la ubicación de recogida para el origen que se muestra en la tienda. Puede contener imágenes adjuntas. |

[1]: https://www.google.com/maps
