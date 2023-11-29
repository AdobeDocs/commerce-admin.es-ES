---
title: '[!UICONTROL Security] &gt; [!UICONTROL Security.txt]'
description: Revise la configuración de en [!UICONTROL Security] &gt; [!UICONTROL Security.txt] de la administración de Commerce.
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

Para obtener más información sobre cómo cambiar estas opciones de configuración, consulte [Informes de problemas de seguridad](../../systems/security-issue-reporting.md).

{{config}}

## [!UICONTROL General]

![General](./assets/txt-general.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable] | Sitio web | Cuando está habilitada, una `security.txt` que contiene información que es necesaria para que los investigadores de seguridad le informen sobre posibles vulnerabilidades. Opciones:<br />**`Yes`**- Crea el `security.txt` basado en la información introducida en el _Información de contacto_ y _Otra información_ secciones.<br />**`No`** - (predeterminado) No crea el `security.txt` archivo. |

{style="table-layout:auto"}

## [!UICONTROL Contact information]

![Información de contacto](./assets/txt-contact-info.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Email] | Sitio web | Dirección de correo electrónico a la que se pueden enviar los informes de seguridad. |
| [!UICONTROL Phone] | Sitio web | Un número de teléfono que puede utilizarse para informar sobre problemas de seguridad. |
| [!UICONTROL Contact Page] | Sitio web | La dirección URL de una página del sitio que enumera contactos de seguridad o su _Contáctenos._ página. Ejemplos: <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{style="table-layout:auto"}

## [!UICONTROL Other information]

![Otra información](./assets/txt-other-info.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Encryption] | Sitio web | Dirección URL que señala a la ubicación de una clave de cifrado que los investigadores de seguridad pueden utilizar para enviar comunicaciones cifradas. _**No introduzca la clave de cifrado en este campo.**_ <br/><br/>Es responsabilidad del investigador verificar que la clave proviene de una fuente confiable. Los investigadores no deben suponer que la clave es la misma que se utiliza para generar la firma digital. Ejemplo:<br />Clave OpenPGP del servidor web: `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | Sitio web | Dirección URL que apunta a una página de su tienda en la que se reconocen los investigadores de seguridad, como`https://mystore.com/hall-of-fame.html`. Para evitar ataques futuros, incluya solo una descripción general sin revelar información específica sobre problemas de vulnerabilidad. Ejemplo:<br />Queremos agradecer a los siguientes investigadores:<br />(aaaa/mm/dd) Justin Thyme - Inyección SQL |
| [!UICONTROL Preferred Languages] | Sitio web | Especifica al menos un idioma preferido para los informes de seguridad. Separar varios caracteres de dos caracteres [códigos de idioma](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) con una coma. Todos los idiomas especificados tienen la misma prioridad. Por ejemplo, para especificar inglés, español y francés, escriba `en, es, fr`. |
| [!UICONTROL Hiring] | Sitio web | La dirección URL de una página del sitio que enumera las posiciones de trabajo relacionadas con la seguridad. Ejemplo: `https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | Sitio web | Dirección URL de la página que describe las prácticas de informes de vulnerabilidades y políticas de seguridad. Ejemplo: `https://mystore.com/security-reporting.html` Predeterminado: `https://mystore.com/security` |
| [!UICONTROL Signature] | Sitio web | Un vínculo al archivo de firma digital. La firma digital debe generarse desde la línea de comandos y guardarse en `.well-known` en el servidor. Para obtener más información, consulte [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) en GitHub. Ejemplo: `https://mystore.com/.well-known/security.txt.sig` |

{style="table-layout:auto"}
