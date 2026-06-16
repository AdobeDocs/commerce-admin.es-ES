---
title: '[!UICONTROL Services] > [!UICONTROL OAuth]'
description: Revise la configuración en la página [!UICONTROL Services] > [!UICONTROL OAuth] del administrador de Commerce.
exl-id: 984793e0-6ac9-443b-b234-e0cea717dada
feature: Configuration, Security
TQID: https://experienceleague.adobe.com/gwRxAaSnEul4D-LjjoGIcEiUCLl8ZrKjcSaMTvlGUKY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 209
ht-degree: 2%

---

# [!UICONTROL Services] > [!UICONTROL OAuth]

{{config}}

## [!UICONTROL Access Token Expiration]

![Caducidad del token de acceso](./assets/oauth-token-expire.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Customer Token Lifetime (hours]) | Global | Determina el tiempo en horas antes de que caduque un token de API de cliente. El token de cliente nunca caduca si el campo está vacío. Valor predeterminado: `1` |
| [!UICONTROL Admin Token Lifetime (hours)] | Global | Determina el tiempo en horas antes de que caduque un token de API de administrador. El token de administrador nunca caduca si el campo está vacío. Valor predeterminado: `4` |

{style="table-layout:auto"}

>[!NOTE]
>
>Los algoritmos de cifrado y duración de token de API de cliente y administrador están controlados por la configuración de [autenticación JWT](magento-web-api.md#jwt-authentication).

## [!UICONTROL Cleanup Settings]

![Configuración de limpieza](./assets/oauth-cleanup.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Cleanup Probability] | Global | Especifica el número de solicitudes de OAuth antes de iniciar la limpieza. No ingrese `0` para deshabilitar la limpieza. |
| [!UICONTROL Enable WSDL Cache] | Global | Determina la antigüedad de las entradas en minutos antes de que se limpien. |

{style="table-layout:auto"}

## [!UICONTROL Consumer Settings]

![Configuración de consumidor](./assets/oauth-consumer-settings.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL OAuth consumer credentials HTTP Post timeout] | Global | Especifica el número de segundos que tarda el sistema en agotar el tiempo de espera cuando los clientes registran sus credenciales. |
| [!UICONTROL OAuth consumer credentials HTTP Post maxredirects] | Global | Especifica el número máximo de redirecciones relacionadas con un registro de credenciales de consumidor. |
| [!UICONTROL Expiration Period] | Global | Determina el número de segundos antes de que caduque una clave o secreto no utilizado después de que comience el intercambio de tokens de OAuth. |

{style="table-layout:auto"}

## [!UICONTROL Authentication Locks]

![Bloqueos de autenticación](./assets/oauth-locks.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Maximum Login Failures to Lock Out Account] | Global | Especifica el número máximo de errores de autenticación para bloquear la cuenta. |
| [!UICONTROL Lockout Time (seconds)] | Global | Especifica el período de tiempo en segundos tras el cual se desbloquea la cuenta. |

{style="table-layout:auto"}
