---
title: '[!UICONTROL Security] > [!UICONTROL Security.txt]'
description: Revise la configuración en la página [!UICONTROL Security] > [!UICONTROL Security.txt] del administrador de Commerce.
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
TQID: https://experienceleague.adobe.com/fXStEab1k6GKC5Tj7CStSGou3uNB-wJk5rZ-7EiFkcg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 360
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

Para obtener más información sobre cómo cambiar esta configuración, consulte [Informes de problemas de seguridad](../../systems/security-issue-reporting.md).

{{config}}

## [!UICONTROL General]

![General](./assets/txt-general.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable] | Sitio web | Cuando se habilita, se guarda un archivo de `security.txt` que contiene información necesaria para que los investigadores de seguridad le informen de posibles vulnerabilidades. Opciones:<br />**`Yes`**- Crea el archivo `security.txt` basándose en la información especificada en las secciones _Información de contacto_ y _Otra información_.<br />**`No`** - (predeterminado) No crea el archivo `security.txt`. |

{style="table-layout:auto"}

## [!UICONTROL Contact information]

![Información de contacto](./assets/txt-contact-info.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Email] | Sitio web | Dirección de correo electrónico a la que se pueden enviar los informes de seguridad. |
| [!UICONTROL Phone] | Sitio web | Un número de teléfono que puede utilizarse para informar sobre problemas de seguridad. |
| [!UICONTROL Contact Page] | Sitio web | Dirección URL de una página del sitio que enumera contactos de seguridad o la página _Contáctenos_. Ejemplos: <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{style="table-layout:auto"}

## [!UICONTROL Other information]

![Otra información](./assets/txt-other-info.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Encryption] | Sitio web | Dirección URL que señala a la ubicación de una clave de cifrado que los investigadores de seguridad pueden utilizar para enviar comunicaciones cifradas. _&#x200B;**No escriba la clave de cifrado en este campo.**&#x200B;_ <br/><br/>Es responsabilidad del investigador verificar que la clave proviene de una fuente de confianza. Los investigadores no deben suponer que la clave es la misma que se utiliza para generar la firma digital. Ejemplo:<br />Clave OpenPGP del servidor web: `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | Sitio web | Dirección URL que apunta a una página de su almacén en la que se reconoce a los investigadores de seguridad, como `https://mystore.com/hall-of-fame.html`. Para evitar ataques futuros, incluya solo una descripción general sin revelar información específica sobre problemas de vulnerabilidad. Ejemplo:<br />Queremos agradecer a los siguientes investigadores:<br />(aaaa/mm/dd) Justin Thyme - Inyección SQL |
| [!UICONTROL Preferred Languages] | Sitio web | Especifica al menos un idioma preferido para los informes de seguridad. Separe los [códigos de idioma](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) de varios caracteres con una coma. Todos los idiomas especificados tienen la misma prioridad. Por ejemplo, para especificar inglés, español y francés, escriba `en, es, fr`. |
| [!UICONTROL Hiring] | Sitio web | La dirección URL de una página del sitio que enumera las posiciones de trabajo relacionadas con la seguridad. Ejemplo: `https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | Sitio web | Dirección URL de la página que describe las prácticas de informes de vulnerabilidades y políticas de seguridad. Ejemplo: `https://mystore.com/security-reporting.html` Predeterminado: `https://mystore.com/security` |
| [!UICONTROL Signature] | Sitio web | Un vínculo al archivo de firma digital. La firma digital debe generarse desde la línea de comandos y guardarse en la carpeta `.well-known` del servidor. Para obtener más información, consulte [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) en GitHub. Ejemplo: `https://mystore.com/.well-known/security.txt.sig` |

{style="table-layout:auto"}
