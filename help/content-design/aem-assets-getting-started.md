---
title: Configuración de la integración de AEM Assets para Commerce
description: Obtenga información sobre cómo configurar su entorno de Experience Manager Assets para administrar los recursos de Commerce de su tienda.
feature: CMS, Media, Configuration
exl-id: 699f517e-1545-4c22-aa8d-9c8d60d352af
source-git-commit: 934473c5124002b3b0b1bee2da47afff468406dc
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# Configuración de la integración de AEM Assets para Commerce

La configuración de la integración de Adobe Experience Manager Assets para Commerce requiere acceso administrativo para personalizar la configuración de la aplicación y el entorno.

- Acceso administrativo al programa Cloud Manager donde se aprovisionan los entornos as a Cloud Service de AEM Assets.

- Acceso administrativo al entorno de Adobe Commerce y la capacidad de recuperar o generar las claves de API necesarias para la autenticación.

## Requisitos para utilizar la integración

Para aprovechar esta integración, las empresas deben cumplir los siguientes requisitos:

- Licencias activas para Adobe Commerce, Adobe Experience Manager Assets y [AEM Dynamic Media](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/administering-dynamic-media).

- Adobe Commerce 2.4.5+

   - PHP 8.1, 8.2, 8.3
   - Compositor: 2.x

- Adobe Experience Manager está aprovisionado con [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/assets/overview)

- El usuario de Adobe Commerce que configuró la integración debe tener acceso a la [organización de IMS](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) en la que se ha aprovisionado el proyecto de AEM Assets.

## Ventajas principales

- **Sin costo adicional**: esta integración se proporciona de forma gratuita para los comerciantes que cumplan con los requisitos de licencia.

- **Solución oficial de Adobe**: desarrollada, mantenida y totalmente compatible con Adobe, que garantiza estabilidad y alineación con futuras mejoras de la plataforma.

- **Modelo de soporte administrado por Adobe**: Adobe gestiona la asistencia y la solución de problemas, proporcionando tranquilidad y una solución de problemas más sencilla.

## Pasos siguientes

Habilitar la integración de Commerce con Experience Manager Assets es un proceso de tres pasos:

1. [Configure su proyecto de recursos de Adobe Experience Manager para administrar los recursos de Adobe Commerce](aem-assets-configure-aem.md).

1. [Instale la integración de Adobe Experience Manager Assets para la extensión de Commerce y configure Adobe Commerce](aem-assets-configure-aem.md).

1. [Habilitar sincronización de recursos](aem-assets-setup-synchronization.md).
