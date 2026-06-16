---
title: '[!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Admin Panel]'
description: Revise la configuración en la página [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Admin Panel] del administrador de Commerce.
exl-id: e4e6771a-487a-43ee-8b98-6acee4599aaf
feature: Configuration, Security
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
TQID: https://experienceleague.adobe.com/hUSNxEvyF010uV6Rp4-osf4azLHtOxtTBSR-XW2m1fA
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
source-wordcount: 610
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Admin Panel]

>[!IMPORTANT]
>
>Para poder configurar Google reCAPTCHA, debe asegurarse de que el archivo `PHP.ini` incluya la siguiente configuración: `allow_url_fopen = 1`. Esto puede requerir la asistencia del desarrollador. Consulte [Configuración de PHP requerida](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) en la _Guía de instalación_.

{{config}}

Para obtener más información sobre cómo cambiar esta configuración, consulte [Google reCAPTCHA](../../systems/security-google-recaptcha.md) en la _Guía de sistemas de administración_.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 (&quot;No soy un robot&quot;)](./assets/recaptcha-admin-v2-not-robot.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--|--|--|
| [!UICONTROL Google API Website Key] | Global | Clave del sitio web que se crea al registrar la cuenta de Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Global | La clave secreta asociada a su cuenta de Google reCAPTCHA. |
| [!UICONTROL Size] | Global | El tamaño del cuadro reCAPTCHA de Google que aparece durante el inicio de sesión. Opciones: `Normal` (predeterminado) / `Compact` |
| [!UICONTROL Theme] | Global | Determina el estilo del cuadro reCAPTCHA de Google. Opciones: `Light Theme` (predeterminado) / `Dark Theme` |
| [!UICONTROL Language Code] | Global | Un [código de dos caracteres](https://developers.google.com/recaptcha/docs/language) que especifica el idioma que se usa para el texto y los mensajes de Google reCAPTCHA. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 invisible](./assets/recaptcha-admin-v2-invisible.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--|--|--|
| [!UICONTROL Google API Website Key] | Global | Clave del sitio web que se crea al registrar la cuenta de Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Global | La clave secreta asociada a su cuenta de Google reCAPTCHA. |
| [!UICONTROL Invisible Badge Position] | Global | La posición del distintivo reCAPTCHA invisible en cada página. Opciones: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Global | Determina el estilo del cuadro reCAPTCHA de Google. Opciones: `Light Theme` (predeterminado) / `Dark Theme` |
| [!UICONTROL Language Code] | Global | Un [código de dos caracteres](https://developers.google.com/recaptcha/docs/language) que especifica el idioma que se usa para el texto y los mensajes de Google reCAPTCHA. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 invisible](./assets/recaptcha-admin-v3-invisible.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--|--|--|
| [!UICONTROL Google API Website Key] | Global | Clave del sitio web que se crea al registrar la cuenta de Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Global | La clave secreta asociada a su cuenta de Google reCAPTCHA. |
| [!UICONTROL Minimum Score Threshold] | Global | La puntuación mínima que identifica una interacción de usuario como un riesgo potencial, donde 1,0 es una interacción de usuario típica y 0,0 es probablemente un bot. Predeterminado: `0.5` |
| [!UICONTROL Invisible Badge Position] | Global | La posición del distintivo reCAPTCHA invisible en cada página. Opciones: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Global | Determina el estilo del cuadro reCAPTCHA de Google. Opciones: `Light Theme` (predeterminado) / `Dark Theme` |
| [!UICONTROL Language Code] | Global | Un [código de dos caracteres](https://developers.google.com/recaptcha/docs/language) que especifica el idioma que se usa para el texto y los mensajes de Google reCAPTCHA. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![Mensajes de error](./assets/recaptcha-admin-failure-messages.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | Global | El mensaje que se muestra en el Administrador si la verificación falla. Texto predeterminado: `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | Global | El mensaje que se muestra en el Administrador si reCAPTCHA no devuelve un resultado de verificación. Texto predeterminado: `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Admin Panel]

![Panel de administración](./assets/recaptcha-admin-panel.png)<!-- zoom -->

>[!NOTE]
>
>El tipo de reCAPTCHA que elija debe coincidir con el tipo asociado a la clave de API de su cuenta de Google reCAPTCHA.

>[!WARNING]
>
>Cuando se utiliza la versión 3 de reCAPTCHA, un usuario auténtico con una puntuación baja no puede continuar. Para la versión 2, un usuario auténtico con una puntuación baja recibe un desafío. Considere detenidamente si los usuarios genuinos con una puntuación baja deben tener la oportunidad de resolver un desafío (versión 2) o de ser bloqueados (versión 3).

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--|--|--|
| [!UICONTROL Enable for Login] | Global | Determina el tipo de reCAPTCHA habilitado para [inicio de sesión de administrador](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html). Opciones: <br/>**`No`**- (predeterminado) No valida el inicio de sesión del administrador.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Requiere que el usuario seleccione la casilla de verificación _No soy un robot_.<br />**`Invisible reCAPTCHA v2`**- Valida el comportamiento del usuario en segundo plano sin requerir interacciones basadas en la puntuación.<br/>**`Invisible reCAPTCHA v3`** : (recomendado) valida el comportamiento del usuario en segundo plano en función de la puntuación de interacción. |
| [!UICONTROL Enable for Forgot Password] | Global | Determina el tipo de reCAPTCHA que está habilitado para solicitar un [restablecimiento de contraseña de administrador](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html#reset-your-password). Opciones: <br/>**`No`**- (predeterminado) No valida la solicitud de restablecimiento de contraseña.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Requiere que el usuario seleccione la casilla de verificación _No soy un robot_.<br />**`Invisible reCAPTCHA v2`**- Valida el comportamiento del usuario en segundo plano sin requerir interacciones basadas en la puntuación.<br/>**`Invisible reCaptcha v3`** : (recomendado) valida el comportamiento del usuario en segundo plano en función de la puntuación de interacción. |

{style="table-layout:auto"}
