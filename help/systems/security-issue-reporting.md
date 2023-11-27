---
title: Informes de problemas de seguridad
description: Aprenda a configurar la información de contacto y los vínculos relacionados con la seguridad que pueden utilizar los investigadores de seguridad para informar sobre problemas de seguridad del sitio.
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 1%

---

# Informes de problemas de seguridad

El `security.txt` contiene información de contacto y vínculos relacionados con la seguridad que pueden utilizar los investigadores de seguridad para informar de los problemas de seguridad del sitio. Si la información de seguridad cambia con el tiempo, asegúrese de que la información de la variable `security.txt` El archivo está actualizado.

**_Para configurar security.txt:_**

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, debajo de _[!UICONTROL Security]_, haga clic en **[!UICONTROL Security.txt]**.

1. En el _[!UICONTROL General]_sección, conjunto **[!UICONTROL Enable]**hasta `Yes`.

   ![Configuración general de seguridad](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. En _[!UICONTROL Contact Information]_, introduzca lo siguiente:

   - La dirección de correo electrónico y el número de teléfono de la persona que administra los problemas de seguridad de su tienda.

   - La dirección URL de la tienda **[!UICONTROL Contact Page]**. Esta página puede ser una lista de contactos de seguridad de la tienda o su _Contáctenos._ página.

   ![Configuración de información de contacto](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. En _[!UICONTROL Other Information]_, introduzca lo siguiente:

   - La URL del público **[!UICONTROL Encryption]** clave. Por ejemplo: `https://example.com/pgp-key.txt`

   - La URL de un **[!UICONTROL Acknowledgments]** página en la que se reconoce a los investigadores de seguridad por sus esfuerzos en nombre de su tienda.

   - Su **[!UICONTROL Preferred Languages]** para comunicaciones relacionadas con la seguridad. Introduzca el carácter de dos caracteres estándar [código de idioma](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) para cada idioma admitido, separado por una coma. Por ejemplo, para especificar inglés, español y francés, escriba `en, es, fr`. Todos los idiomas especificados tienen la misma prioridad, independientemente de su orden de aparición.

   - La URL de un **[!UICONTROL Hiring]** que enumera las oportunidades de empleo relacionadas con la seguridad en su tienda.

   - La dirección URL de su seguridad **[!UICONTROL Policy]** página.

   - La URL de un **[!UICONTROL Signature]** que se guarda en el servidor. Por ejemplo: `https://mystore.com/.well-known/security.txt.sig`

   La firma digital debe configurarse desde la CLI (interfaz de línea de comandos) del servidor. Para obtener más información, consulte [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) en GitHub.

   ![Otra información](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.
