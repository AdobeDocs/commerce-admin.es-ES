---
title: Configuración de la integración de AEM Assets
description: Conozca los requisitos y pasos para configurar la integración entre Adobe Commerce y AEM Assets as a Cloud Service.
feature: CMS, Media, Configuration, Integration
source-git-commit: df21ea9a797a4f11d0104cf34134ced3bbabbdf4
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# Configuración de la integración de AEM Assets

Habilite las funciones avanzadas de administración de recursos configurando el entorno de AEM Assets e instalando y configurando la integración de AEM Assets para Commerce.

Cuando la integración está activa, los administradores pueden utilizar Experience Manager Assets as a Cloud Service como la única fuente fiable para la creación y administración de recursos y como una herramienta de administración de recursos digitales (DAM) central para crear, administrar, organizar y distribuir recursos para proyectos de Commerce.

## Requisitos

- Adobe Commerce 2.4.5+
   - PHP 8.1, 8.2, 8.3
   - Compositor: 2.x
- Adobe Experience Manager está aprovisionado con [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/assets/overview)
- El usuario de Adobe Commerce que configuró la integración debe tener acceso a la [organización de IMS](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) en la que se ha aprovisionado el proyecto de AEM Assets.

## Configuración de la integración

>[!BEGINSHADEBOX]

**Requisitos previos**

La configuración de la integración de AEM Assets requiere acceso administrativo para personalizar la configuración de la aplicación y el entorno.

- Acceso administrativo al programa de Cloud Manager donde se proporcionan los entornos as a Cloud Service de AEM Assets.
- Acceso administrativo al entorno de Adobe Commerce y capacidad para recuperar o generar las claves de API necesarias para la autenticación.

>[!ENDSHADEBOX]

Habilitar la integración de Commerce con Experience Manager Assets es un proceso de tres pasos:

1. [Configure su proyecto de Experience Manager Assets para administrar los recursos de Commerce](aem-assets-configure-aem.md).

1. [Instale la extensión Experience Manager Assets Integration y configure Adobe Commerce](aem-assets-configure-aem.md).

1. [Habilitar sincronización de recursos](aem-assets-setup-synchronization.md).
