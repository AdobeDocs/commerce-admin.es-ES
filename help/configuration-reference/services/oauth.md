---
title: '[!UICONTROL Services] &gt; [!UICONTROL OAuth]'
description: Revise la configuración de en [!UICONTROL Services] &gt; [!UICONTROL OAuth] de la administración de Commerce.
exl-id: 984793e0-6ac9-443b-b234-e0cea717dada
feature: Configuration, Security
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 1%

---

# [!UICONTROL Services] > [!UICONTROL OAuth]

{{config}}

## [!UICONTROL Access Token Expiration]

![Caducidad del token de acceso](./assets/oauth-token-expire.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Customer Token Lifetime (hours]) | Global | Determina el tiempo en horas antes de que caduque un token de API de cliente. El token de cliente nunca caduca si el campo está vacío. Valor predeterminado: `1` |
| [!UICONTROL Admin Token Lifetime (hours)] | Global | Determina el tiempo en horas antes de que caduque un token de API de administrador. El token de administrador nunca caduca si el campo está vacío. Valor predeterminado: `4` |

{:style=&quot;table-layout:auto&quot;}

>[!NOTE]
>
>Los algoritmos de cifrado y duración del token de API de cliente y administrador están controlados por [Autenticación JWT](magento-web-api.md#jwt-authentication) opciones de configuración.

## [!UICONTROL Cleanup Settings]

![Configuración de limpieza](./assets/oauth-cleanup.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Cleanup Probability] | Global | Especifica el número de solicitudes de OAuth antes de iniciar la limpieza. No introducir `0` para deshabilitar la limpieza. |
| [!UICONTROL Enable WSDL Cache] | Global | Determina la antigüedad de las entradas en minutos antes de que se limpien. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Consumer Settings]

![Configuración de consumidor](./assets/oauth-consumer-settings.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL OAuth consumer credentials HTTP Post timeout] | Global | Especifica el número de segundos que tarda el sistema en agotar el tiempo de espera cuando los clientes registran sus credenciales. |
| [!UICONTROL OAuth consumer credentials HTTP Post maxredirects] | Global | Especifica el número máximo de redirecciones relacionadas con un registro de credenciales de consumidor. |
| [!UICONTROL Expiration Period] | Global | Determina el número de segundos antes de que caduque una clave o secreto no utilizado después de que comience el intercambio de tokens de OAuth. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Authentication Locks]

![Bloqueos de autenticación](./assets/oauth-locks.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Maximum Login Failures to Lock Out Account] | Global | Especifica el número máximo de errores de autenticación para bloquear la cuenta. |
| [!UICONTROL Lockout Time (seconds)] | Global | Especifica el período de tiempo en segundos tras el cual se desbloquea la cuenta. |

{:style=&quot;table-layout:auto&quot;}
