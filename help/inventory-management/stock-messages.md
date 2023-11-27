---
title: Escenarios de mensajes de stock
description: Obtenga información acerca de la combinación de opciones de configuración que controlan los mensajes de disponibilidad de existencias en las páginas de productos y en las listas de productos en las páginas de catálogos.
exl-id: 63114305-e695-445b-91cd-9e0fb2729ec4
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 2%

---

# Escenarios de mensajes de stock

Puede utilizar una combinación de opciones de configuración para controlar los mensajes de disponibilidad de existencias en las páginas de productos y en los listados de productos en las páginas del catálogo.

![Producto agrupado con el mensaje &quot;Agotado&quot;](assets/storefront-out-of-stock-message.png){width="600" zoomable="yes"}

## Mensajes de stock de página de producto

Hay varias variaciones de mensajes disponibles para la página de producto, según la combinación de las opciones Administrar existencias y Disponibilidad de existencias.

### Ejemplo 1: Mostrar mensaje de disponibilidad

#### Escenario 1

Esta combinación de configuraciones hace que el mensaje de disponibilidad aparezca en la página del producto, según la disponibilidad de stock de cada producto.

| Opciones de Stock | Configuración | Mensaje |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` | |
| [!UICONTROL Manage Stock] | `Yes` | |
| [!UICONTROL Stock Availability] | `In Stock` | _[!UICONTROL Availability: In Stock]_ |
| | `Out of Stock` | _[!UICONTROL Availability: Out of Stock]_ |

#### Escenario 2

Cuando las existencias no se gestionan para un producto, esta combinación de configuraciones se puede utilizar para mostrar el mensaje de disponibilidad en la página del producto.

| Opciones de Stock | Configuración | Mensaje |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` |  |
| [!UICONTROL Manage Stock] | `No` | _[!UICONTROL Availability: In Stock]_ |

### Ejemplo 2: Ocultar mensaje de disponibilidad

#### Escenario 1

Esta combinación de configuración y configuración de producto evita que aparezca el mensaje de disponibilidad en la página del producto.

| Opciones de Stock | Configuración | Mensaje |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |
| [!UICONTROL Manage Stock] | `Yes` |  |
| [!UICONTROL Stock Availability] | `In Stock` | Ninguno |
|  | `Out of Stock` | Ninguno |

#### Escenario 2

Cuando las existencias no se administran para un producto, esta combinación de configuración y configuración del producto evita que aparezca el mensaje de disponibilidad en la página del producto.

| Opciones de Stock | Configuración | Mensaje |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |
| [!UICONTROL Manage Stock] | `No` | Ninguno |

## Mensajes de stock de página de catálogo

Las siguientes opciones de visualización son posibles para las listas de categorías y resultados de búsqueda, según la disponibilidad del producto y la configuración.

![Mensaje agotado en la página Categoría](assets/storefront-out-of-stock-catalog-page.png){width="600" zoomable="yes"}

### Ejemplo 1: Mostrar producto con el mensaje &quot;Agotado&quot;

Esta combinación de ajustes de configuración incluye productos sin existencias en las listas de categorías y resultados de búsqueda, y muestra el mensaje &quot;sin existencias&quot;.

| Opciones de Stock | Configuración | Mensaje |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `Yes` |  |
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` | _[!UICONTROL Out of stock]_ |
| [!UICONTROL Display Out of Stock Products] | `Yes` |  |
| [!UICONTROL Display product availability in stock in the frontend] | `No` | Ninguno |

### Ejemplo 2: Mostrar el producto sin el mensaje &quot;Agotado&quot;

Esta combinación de ajustes de configuración incluye productos sin existencias en las listas de categorías y resultados de búsqueda, pero no muestra un mensaje.

| Opciones de Stock | Configuración | Mensaje |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `Yes` | Ninguno |
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |

### Ejemplo 3: ocultar el producto hasta que vuelva a estar disponible

Esta configuración omite los productos sin existencias por completo de las listas de categorías y resultados de búsqueda, hasta que vuelvan a estar disponibles.

| Opciones de Stock | Configuración | Mensaje |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `No` | Ninguno |
