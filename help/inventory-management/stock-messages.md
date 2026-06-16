---
title: Escenarios de mensajes de stock
description: Obtenga información acerca de la combinación de opciones de configuración que controlan los mensajes de disponibilidad de existencias en las páginas de productos y en las listas de productos en las páginas de catálogos.
exl-id: 63114305-e695-445b-91cd-9e0fb2729ec4
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/9kPHtr75C7PkM9vD-2-AeG8JnAfKAao0GKEH9MhkBbU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 353
ht-degree: 1%

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

![Mensaje agotado en la página de categoría](assets/storefront-out-of-stock-catalog-page.png){width="600" zoomable="yes"}

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
