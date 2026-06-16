---
title: '[!UICONTROL Services] > [!UICONTROL Magento Web API]'
description: Revise la configuración en la página [!UICONTROL Services] > [!UICONTROL Magento Web API] del administrador de Commerce.
exl-id: 9e9857e7-6f5c-4273-9e82-c861e627827a
feature: Configuration, Integration
TQID: https://experienceleague.adobe.com/62cy3cPVxGeI-W1LElSg1TEBEb0cZN30vGZQ74UNhm8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 325
ht-degree: 1%

---

# [!UICONTROL Services] > [!UICONTROL Magento Web API]

{{config}}

<!-- [X-ref](../systems/integrations.md) -->

## [!UICONTROL SOAP Settings]

![Configuración de SOAP](./assets/web-api-soap-settings.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Default Response Charset] | Vista de tienda | Determina el conjunto de caracteres predeterminado. Si está vacío, se utiliza UTF-8. |

{style="table-layout:auto"}

## [!UICONTROL GraphQl Input Limits]

![Límites de entrada de GraphQl](./assets/web-api-graphql-input-limits.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | Vista de tienda | Determina si los límites de entrada están habilitados para las llamadas de GraphQL. Valor predeterminado: `No`. |
| [!UICONTROL Maximum Page Size] | Vista de tienda | Establece el número máximo de elementos permitidos en un resultado de búsqueda paginada en la respuesta de GraphQL. Esta opción no está disponible cuando _Habilitar límites de entrada_ = `No`. |

{style="table-layout:auto"}

## [!UICONTROL Web Api Input Limits]

![Límites de entrada de Web Api](./assets/web-api-input-limits.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | Vista de tienda | Determina si los límites de entrada están habilitados para las llamadas a la API web. Valor predeterminado: `No`. |
| Límite de lista de entrada | Vista de tienda | Establece el número máximo de elementos permitidos en una propiedad de matriz de entidades en la solicitud de API web. Esta opción no está disponible cuando _Habilitar límites de entrada_ = `No`. |
| [!UICONTROL Maximum Page Size] | Vista de tienda | Establece el número máximo de elementos permitidos en un resultado de búsqueda paginada en la respuesta de la API web. Esta opción no está disponible cuando _Habilitar límites de entrada_ = `No`. |
| [!UICONTROL Default Page Size] | Vista de tienda | Establece el número predeterminado de elementos en un resultado de búsqueda paginada en la respuesta de la API web. |

{style="table-layout:auto"}

## [!UICONTROL Web API Security]

![Seguridad de API web](./assets/web-api-security.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Allow Anonymous Guest Access] | Global | Determina si los invitados pueden acceder de forma anónima a CMS, catálogos y recursos de tienda desde las API de SOAP y REST. De forma predeterminada, no se permite el acceso anónimo de invitados. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL JWT Authentication]

![Autenticación JWT](./assets/web-api-jwt-authentication.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Algorithm to sign/encrypt JWTs used for authentication] | Global | Especifica el tipo de algoritmo JWS o JWE utilizado para el cifrado de JWT (token web JSON) |
| [!UICONTROL Content encryption algorithm for JWEs] | Global | Especifica el tipo de algoritmo de cifrado de contenido utilizado para el cifrado JWT cuando se selecciona el algoritmo JWE. Esta opción se ignora para los algoritmos JWS. |
| [!UICONTROL Customer JWT Expires In] | Global | Establece el tiempo (en minutos) antes de que caduque un token de portador JWT del cliente. El token de portador JWT del cliente caduca en 30 minutos si este campo está vacío o tiene un valor negativo. Valor predeterminado: `60` |
| [!UICONTROL Admin User JWT Expires In] | Global | Establece el tiempo (en minutos) antes de que caduque el token de portador de JWT de administrador. El token de portador JWT de administrador caduca en 30 minutos si este campo está vacío o tiene un valor negativo. Valor predeterminado: `60` |

{style="table-layout:auto"}
