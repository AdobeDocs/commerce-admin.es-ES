---
title: '[!UICONTROL Security] > [!UICONTROL 2FA]'
description: Revise la configuración en la página [!UICONTROL Security] > [!UICONTROL 2FA] del administrador de Commerce.
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
TQID: https://experienceleague.adobe.com/-5t8bTj14iB%2D%2D%2D88TotUNefATWwE80LTswPO3xVWU70
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
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 97a3e3469e45ec9c7e3316f1ce5ca7894ea2ddb7
workflow-type: tm+mt
source-wordcount: 342
ht-degree: 2%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>Las tiendas que han habilitado la autenticación de Adobe Identity Management Services (IMS) tienen deshabilitada la autenticación de doble factor (2FA) nativa de Adobe Commerce y Magento Open Source. Los usuarios administradores que han iniciado sesión en su instancia de Adobe Commerce con sus credenciales de Adobe no necesitan volver a autenticarse en muchas tareas de administración. La autenticación la gestiona Adobe IMS cuando el usuario administrador inicia sesión en su sesión actual. Consulte [Información general sobre la integración de Adobe Commerce con Adobe IMS](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html?lang=es).

{{config}}

Para obtener más información acerca de cómo cambiar esta configuración, consulte [Autenticación de doble factor (2FA)](../../systems/security-two-factor-authentication.md) en la _Guía de sistemas de administración_.

## [!UICONTROL General]

![General](./assets/2fa-general.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Providers to use] | Global | Indica los métodos de autenticación de doble factor que necesita. Si selecciona más de un proveedor, cada usuario deberá configurar cada método 2FA la próxima vez que inicie sesión. |
| [!UICONTROL Configuration Email URL for Web API] | Global | Para implementaciones personalizadas, la URL de un vínculo de configuración de correo electrónico alternativo que se envía a los usuarios de _Admin_ la primera vez que inician sesión. En la plantilla de correo electrónico, utilice el marcador de posición `:tfat` para indicar dónde se ha insertado el token. |
| [!UICONTROL Retry attempt limit for Two-Factor Authentication] | Global | Determina cuántas veces un administrador puede escribir un [!DNL one-time password (OTP)] antes de que su cuenta se deshabilite temporalmente. Predeterminado: `10` |
| [!UICONTROL Two-Factor Authentication lockout time (seconds)] | Global | Determina cuánto tiempo (en segundos) puede esperar un administrador para escribir un [!DNL one-time password (OTP)] antes de que su cuenta se deshabilite temporalmente. Predeterminado: `300` |

{style="table-layout:auto"}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL OTP Window] | Global | Determina cuánto tiempo (en segundos) acepta el sistema un(a) [!DNL one-time-password (OTP)] de administrador después de que haya caducado. No puede ser superior a la duración de un único OTP (normalmente 30 segundos). Predeterminado: `29` |

{style="table-layout:auto"}

## [!UICONTROL Duo Security]

![Seguridad Duo](./assets/2fa-duo-security.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Client Id] | Global | Identificador de cliente de su cuenta de [!DNL Duo Security]. |
| [!UICONTROL Client Secret] | Global | Secreto de cliente de su cuenta de [!DNL Duo Security]. |
| [!UICONTROL Integration Key] | Global | La clave de integración de su cuenta de API [!DNL Duo Security]. |
| [!UICONTROL Secret Key] | Global | La clave secreta de su cuenta de API [!DNL Duo Security]. |
| [!UICONTROL API Hostname] | Global | El nombre de host API de su cuenta de [!DNL Duo Security]. |

{style="table-layout:auto"}

## [!UICONTROL Authy]

![Autoridad](./assets/2fa-authy.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL API Key] | Global | La clave API de su cuenta de [!DNL Authy]. |
| [!UICONTROL OneTouch Message] | Global | El mensaje que aparece en el autenticador [!DNL Authy] al iniciar sesión. Predeterminado: `Login request to your Magento Admin` |

{style="table-layout:auto"}

## [!UICONTROL U2F Key]

![Clave U2F](./assets/2fa-u2f-key.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | Global | Dominio que se usa para emitir y procesar [!DNL WebAuthn] desafíos para implementaciones de WebAPI personalizadas. |

{style="table-layout:auto"}
