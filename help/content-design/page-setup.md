---
title: Configuración de página
description: Obtenga información sobre cómo configurar los valores predeterminados de las partes principales de una página de la tienda.
exl-id: a4310940-0d4f-4948-a271-382f03905bfd
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Configuración de página

Las secciones principales de la página están controladas, en parte, por un conjunto de etiquetas de HTML estándar. Algunas de estas etiquetas se pueden utilizar para determinar la selección de fuentes, colores, tamaño, colores de fondo e imágenes que se utilizan en cada sección de la página. Otros elementos de página de control de configuración, como el logotipo del encabezado y el aviso de copyright del pie de página. Estas secciones corresponden a la estructura subyacente de la página HTML y muchas de las propiedades básicas se pueden establecer desde Admin.

- [Cabeza de HTML](#html-head)
- [Header](#header)
- [Pie](#footer)

![Secciones de página del HTML](./assets/storefront-home-html-inspect.png){width="700" zoomable="yes"}

## Cabeza de HTML

Los ajustes de la sección Cabezal de HTML corresponden a la variable `<head>` de una página de HTML y se puede configurar para cada vista de tienda. Además de los metadatos del título de página, la descripción y las palabras clave, la sección incluye un vínculo al icono de favoritos y varios scripts. Las instrucciones para los robots de motores de búsqueda y la visualización del aviso de demostración de la tienda también se configuran en esta sección.

### Configuración del encabezado del HTML

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Busque la vista de tienda que desee configurar y haga clic en **[!UICONTROL Edit]** en el _[!UICONTROL Action]_columna.

1. En _Otra configuración_, expanda ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL HTML Head]** sección.

   ![Ajustes de configuración de cabezal de HTML](./assets/configuration-html-head.png){width="500" zoomable="yes"}

1. Actualice el [favicon](../getting-started/storefront-branding.md#add-a-favicon) si es necesario.

1. Actualice la configuración del título de página según sus necesidades:

   - **[!UICONTROL Default Page Title]**
   - **[!UICONTROL Page Title Prefix]**
   - **[!UICONTROL Page Title Suffix]**

   Puede utilizar un sufijo o un prefijo con el título predeterminado para crear un título de dos o tres partes. Puede agregar una barra vertical o dos puntos como separador entre el prefijo o sufijo y el título predeterminado.

1. Añada o modifique metadatos que admitan la optimización de los motores de búsqueda (SEO) y ayuden a dirigir a los clientes a su tienda desde los resultados de búsqueda:

   - **[!UICONTROL Default Meta Description]**
   - **[!UICONTROL Default Meta Keywords]**

1. Introduzca cualquiera **[!UICONTROL Scripts and Style Sheets]** según sea necesario.

1. Habilitar o deshabilitar el [aviso de almacén de demostración](../getting-started/storefront-branding.md#set-the-store-demo-notice) si es necesario.

1. Cuando termine, haga clic en **[!UICONTROL Save Configuration]**.

### Descripciones de los campos de Cabeza de HTML

| Campo | Ámbito | Descripción |
|--- |--- |--- |
| [!UICONTROL Favicon Icon] | Vista de tienda | Carga la imagen gráfica pequeña que aparece en la barra de direcciones y en la pestaña del explorador. Tipos de archivo permitidos: ICO, PNG, APNG, GIF y JPG (JPEG). No todos los exploradores admiten estos formatos. |
| [!UICONTROL Default Page Title] | Vista de tienda | Título que aparece en la barra de título de cada página cuando se ve en un explorador. El título predeterminado se utiliza para todas las páginas, a menos que se especifique otro título para páginas individuales. |
| [!UICONTROL Page Title Prefix] | Vista de tienda | Se puede agregar un prefijo antes del título para crear un título de dos o tres partes. Se puede utilizar una barra vertical o dos puntos como separador al final del prefijo para diferenciarlo del texto del título principal. |
| [!UICONTROL Page Title Suffix] | Vista de tienda | Se puede agregar un sufijo después del título para crear un título de dos o tres partes. Se puede utilizar una barra vertical o dos puntos como separador al final del prefijo para diferenciarlo del texto del título principal. |
| [!UICONTROL Default Meta Description] | Vista de tienda | La descripción proporciona un resumen del sitio para los anuncios de motores de búsqueda y no debe tener más de 160 caracteres de longitud. |
| [!UICONTROL Default Meta Keywords] | Vista de tienda | Una serie de palabras clave que describen el almacén, cada una separada por una coma. |
| [!UICONTROL Scripts and Style Sheets] | Vista de tienda | Contiene secuencias de comandos que deben incluirse en el HTML antes de la `<head>` etiqueta. Por ejemplo, cualquier JavaScript de terceros que deba colocarse antes de `<body>` puede introducirse la etiqueta aquí. |
| [!UICONTROL Display Demo Store Notice] | Vista de tienda | Controla la visualización del aviso de almacén de demostración en la parte superior de la página. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## Header

La configuración del encabezado identifica la ruta al logotipo de la tienda y especifica el texto alternativo del logotipo y el mensaje de bienvenida.

![Ajustes de configuración de encabezado](./assets/configuration-header.png){width="400" zoomable="yes"}

### Configuración del encabezado

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Busque la vista de tienda que desee configurar y haga clic en **[!UICONTROL Edit]** en el _[!UICONTROL Action]_columna.

1. En _Otra configuración_, expanda ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Header]** sección.

1. Realice los cambios necesarios en la vista de la tienda:

   - [Logotipo](../getting-started/storefront-branding.md#upload-your-logo) configuración
   - [Mensaje de bienvenida](../getting-started/storefront-branding.md#change-the-welcome-message) configuración

1. Cuando termine, haga clic en **[!UICONTROL Save Configuration]**.

### Descripciones de campos de encabezado

| Campo | Ámbito | Descripción |
|--- |--- |--- |
| [!UICONTROL Logo Image] | Vista de tienda | Identifica la ruta al logotipo que aparece en el encabezado. Tipos de archivo admitidos: PNG, GIF, JPG (JPEG) |
| [!UICONTROL Logo Attribute Width] | Vista de tienda | Ancho de la imagen del logotipo en píxeles. |
| [!UICONTROL Logo Attribute Height] | Vista de tienda | Altura de la imagen del logotipo en píxeles. |
| [!UICONTROL Welcome Text] | Vista de tienda | El mensaje de bienvenida aparece en el encabezado de la página e incluye el nombre de los clientes que han iniciado sesión. |
| [!UICONTROL Logo Image Alt] | Vista de tienda | Texto alternativo asociado con el logotipo. |
| [!UICONTROL Translate Title] | Vista de tienda | Determina si la variable `Page Title` o `Meta Title` debe traducirse. |

{style="table-layout:auto"}

## Pie

En la sección Configuración del pie de página es donde puede actualizar el [aviso de copyright](../getting-started/storefront-branding.md#change-the-copyright-notice) que aparece en la parte inferior de la página e introduzca varios scripts que deben colocarse antes de la `<body>` etiqueta.

![Ajustes de configuración del pie](./assets/configuration-footer.png){width="400" zoomable="yes"}

### Configuración del pie de página

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Busque la vista de tienda que desee configurar y haga clic en **[!UICONTROL Edit]** en el _[!UICONTROL Action]_columna.

1. En _Otra configuración_, expanda ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Footer]** sección.

1. Realice los cambios necesarios en la **[!UICONTROL Copyright]** y **[!UICONTROL Miscellaneous HTML]** configuración.

1. Cuando termine, haga clic en **[!UICONTROL Save Configuration]**.

## Descripciones de campos de pie

| Campo | Ámbito | Descripción |
|--- |--- |--- |
| [!UICONTROL Miscellaneous HTML] | Vista de tienda | Un cuadro de entrada en el que puede cargar scripts varios en el servidor que deben colocarse justo antes del cierre `<body>` etiqueta. |
| [!UICONTROL Copyright] | Vista de tienda | Declaración de copyright que aparece en la parte inferior de cada página. Para incluir el símbolo de copyright, utilice la entidad de carácter HTML `\&copy;` como en el siguiente ejemplo: `\&copy; 2021 Commerce Demo Store. All Rights Reserved.` Asegúrese de reemplazar el aviso de copyright de ejemplo por el suyo propio. |
| [!UICONTROL Display Report Bugs Link] | Vista de tienda | Determina si el vínculo del informe de errores (compatible con algunas temáticas) está habilitado o deshabilitado. |

{style="table-layout:auto"}
