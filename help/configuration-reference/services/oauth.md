---
title: '[!UICONTROL Services] &gt; [!UICONTROL OAuth]'
description: Revise la configuración en la página [!UICONTROL Services] &gt; [!UICONTROL OAuth] del administrador de Commerce.
exl-id: 984793e0-6ac9-443b-b234-e0cea717dada
feature: Configuration, Security
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '211'
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
