---
title: Configurar la rotación del registro
description: Configure la rotación de registros para la integración de AEM Assets para Commerce.
feature: CMS, Media, Integration
exl-id: f735d086-048c-4555-bc58-ac6736c281b0
source-git-commit: c71fd243d809e2b86c5c8e781d527892965838ae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Configuración de Experience Manager Assets

La integración de AEM Assets para Commerce proporciona los siguientes archivos de registro en la instancia de Commerce:

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

Pida al administrador del sistema que compruebe el horario de rotación de archivos de registro para evitar que crezcan demasiado. En algunos entornos, los archivos de registro giran automáticamente, pero en otros entornos es necesario configurar manualmente la rotación de registros. Para obtener más información, consulte los temas siguientes:

- Para las instalaciones locales de Adobe Commerce, pídale al administrador del sistema que configure [rotación del registro](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html#server-settings).
- Para Adobe Commerce sobre proyectos de infraestructura en la nube, consulte [Ver y administrar registros](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/test/log-locations.html).
