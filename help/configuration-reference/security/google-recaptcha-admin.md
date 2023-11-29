---
title: '[!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Admin Panel]'
description: Revise la configuración de en [!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Admin Panel] de la administración de Commerce.
exl-id: e4e6771a-487a-43ee-8b98-6acee4599aaf
feature: Configuration, Security
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Admin Panel]

>[!IMPORTANT]
>
>Antes de poder configurar Google reCAPTCHA, debe asegurarse de que su `PHP.ini` incluye la siguiente configuración: `allow_url_fopen = 1`. Esto puede requerir la asistencia del desarrollador. Consulte [Configuración de PHP requerida](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) en el _Guía de instalación_.

{{config}}

Para obtener más información sobre cómo cambiar esta configuración, consulte [Google reCAPTCHA](../../systems/security-google-recaptcha.md) en el _Guía de sistemas de administración_.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 (&quot;No soy un robot&quot;)](./assets/recaptcha-admin-v2-not-robot.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--|--|--|
| [!UICONTROL Google API Website Key] | Global | Clave del sitio web que se crea al registrar la cuenta de Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Global | La clave secreta asociada a su cuenta de Google reCAPTCHA. |
| [!UICONTROL Size] | Global | El tamaño del cuadro reCAPTCHA de Google que aparece durante el inicio de sesión. Opciones: `Normal` (predeterminado) / `Compact` |
| [!UICONTROL Theme] | Global | Determina el estilo del cuadro reCAPTCHA de Google. Opciones: `Light Theme` (predeterminado) / `Dark Theme` |
| [!UICONTROL Language Code] | Global | A [código de dos caracteres](https://developers.google.com/recaptcha/docs/language) que especifica el idioma que se utiliza para el texto y la mensajería reCAPTCHA de Google. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 invisible](./assets/recaptcha-admin-v2-invisible.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--|--|--|
| [!UICONTROL Google API Website Key] | Global | Clave del sitio web que se crea al registrar la cuenta de Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Global | La clave secreta asociada a su cuenta de Google reCAPTCHA. |
| [!UICONTROL Invisible Badge Position] | Global | La posición del distintivo reCAPTCHA invisible en cada página. Opciones: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Global | Determina el estilo del cuadro reCAPTCHA de Google. Opciones: `Light Theme` (predeterminado) / `Dark Theme` |
| [!UICONTROL Language Code] | Global | A [código de dos caracteres](https://developers.google.com/recaptcha/docs/language) que especifica el idioma que se utiliza para el texto y la mensajería reCAPTCHA de Google. |

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
| [!UICONTROL Language Code] | Global | A [código de dos caracteres](https://developers.google.com/recaptcha/docs/language) que especifica el idioma que se utiliza para el texto y la mensajería reCAPTCHA de Google. |

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
| [!UICONTROL Enable for Login] | Global | Determina el tipo de reCAPTCHA habilitado para [Inicio de sesión de administrador](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html). Opciones:<br/>**`No`**- (predeterminado) No valida el inicio de sesión del administrador.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Requiere que el usuario seleccione _No soy un robot_ casilla de verificación <br />**`Invisible reCAPTCHA v2`**: valida el comportamiento del usuario en segundo plano sin requerir interacciones en función de la puntuación.<br/>**`Invisible reCAPTCHA v3`** : (recomendado) valida el comportamiento del usuario en segundo plano en función de la puntuación de interacción. |
| [!UICONTROL Enable for Forgot Password] | Global | Determina el tipo de reCAPTCHA que está habilitado para solicitar una [Restablecimiento de contraseña de administrador](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html#reset-your-password). Opciones:<br/>**`No`**- (predeterminado) No valida la solicitud de restablecimiento de contraseña.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Requiere que el usuario seleccione _No soy un robot_ casilla de verificación <br />**`Invisible reCAPTCHA v2`**: valida el comportamiento del usuario en segundo plano sin requerir interacciones en función de la puntuación.<br/>**`Invisible reCaptcha v3`** : (recomendado) valida el comportamiento del usuario en segundo plano en función de la puntuación de interacción. |

{style="table-layout:auto"}
