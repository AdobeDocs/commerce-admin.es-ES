---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL XML Sitemap]'
description: Revise la configuración en la página [!UICONTROL Catalog] &gt; [!UICONTROL XML Sitemap] del administrador de Commerce.
exl-id: 319c34e9-bd5f-46f8-810f-bc4d5228f9c9
feature: Configuration, Site Navigation
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 2%

---

# [!UICONTROL Catalog] > [!UICONTROL XML Sitemap]

{{config}}

## [!UICONTROL Categories Options]

![Opciones de categorías](./assets/xml-sitemap-categories-options.png)<!-- zoom -->

<!-- [Categories Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Frequency] | Vista de tienda | Determina la frecuencia con la que se actualizan las categorías de mapa del sitio. Opciones: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Vista de tienda | Valor entre `0.0` y `1.0` que determina la prioridad de las actualizaciones del mapa del sitio de categoría en relación con otro contenido. Cero (`0.0`) tiene la prioridad más baja. |

{style="table-layout:auto"}

## [!UICONTROL Products Options]

![Opciones de productos](./assets/xml-sitemap-products-options.png)<!-- zoom -->

<!-- [Products Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Frequency] | Vista de tienda | Determina la frecuencia con la que se actualizan los productos de mapa del sitio. Opciones: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Vista de tienda | Valor entre `0.0` y `1.0` que determina la prioridad de las actualizaciones del mapa del sitio del producto en relación con otro contenido. Cero (`0.0`) tiene la prioridad más baja. |
| [!UICONTROL Add Images into Sitemap] | Vista de tienda | Determina el grado en que las imágenes se incluyen en el mapa del sitio. Opciones: `None` / `Base Only` / `All` |

{style="table-layout:auto"}

## [!UICONTROL CMS Pages Options]

![Opciones de páginas de CMS](./assets/xml-sitemap-cms-pages-options.png)<!-- zoom -->

<!-- [CMS Pages Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Frequency] | Vista de tienda | Determina la frecuencia con la que se actualizan las páginas de CMS de mapa del sitio. Opciones: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Vista de tienda | Valor entre `0.0` y `1.0` que determina la prioridad de las actualizaciones del mapa del sitio de la página de CMS en relación con otro contenido. Cero (`0.0`) tiene la prioridad más baja. |

{style="table-layout:auto"}

## [!UICONTROL Store Url Options]

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Frequency] | Vista de tienda | Determina la frecuencia con la que se actualizan las direcciones URL del almacén. Opciones: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Vista de tienda | Valor entre `0.0` y `1.0` que determina la prioridad de las actualizaciones de la dirección URL del almacén en relación con otro contenido. Cero (`0.0`) tiene la prioridad más baja. |

{style="table-layout:auto"}

## [!UICONTROL Generation Settings]

![Configuración de generación](./assets/xml-sitemap-generation-settings.png)<!-- zoom -->

<!-- [Generation Settings](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enabled] | Vista de tienda | Determina si hay un mapa del sitio XML disponible para el almacén. Opciones: `Yes` / `No` |
| [!UICONTROL Start Time] | Vista de tienda | Especifica la hora, el minuto y el segundo del día en que se actualiza el mapa del sitio. |
| [!UICONTROL Frequency] | Vista de tienda | Determina con qué frecuencia se actualiza el mapa del sitio. Opciones: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | Vista de tienda | La dirección de correo electrónico de la persona que recibe la notificación si se produce un error durante el proceso de actualización del mapa del sitio. Para varias direcciones, sepárelas con una coma. |
| [!UICONTROL Error Email Sender] | Sitio web | Identifica al contacto de almacén que aparece como remitente de la notificación de error. Opciones: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Error Email Template] | Sitio web | Identifica la plantilla de correo electrónico que se utiliza para la notificación de error. Plantilla predeterminada: `Sitemap generate Warnings` |

{style="table-layout:auto"}

## [!UICONTROL Sitemap File Limits]

![Límites de archivos de mapa del sitio](./assets/xml-sitemap-sitemap-file-limits.png)<!-- zoom -->

<!-- [Sitemap File Limits](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Maximum No of URLs Per File] | Vista de tienda | Determina la cantidad máxima de direcciones URL que se pueden incluir en un solo mapa del sitio. |
| [!UICONTROL Maximum File Size] | Vista de tienda | Determina el tamaño máximo del mapa del sitio generado, en bytes. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Submission Settings]

![Configuración de envío del motor de búsqueda](./assets/xml-sitemap-search-engine-submission-settings.png)<!-- zoom -->

<!-- [Search Engine Submission Settings](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable Submission to Robots.txt] | Vista de tienda | Permite enviar directivas para el archivo robots.txt. Opciones: `Yes` / `No` |

{style="table-layout:auto"}
