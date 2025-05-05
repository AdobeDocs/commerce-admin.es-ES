---
title: Configuración de la integración de AEM Assets para Commerce
description: Obtenga información sobre cómo configurar su entorno de Experience Manager Assets para administrar los recursos de Commerce de su tienda.
feature: CMS, Media, Configuration
exl-id: 699f517e-1545-4c22-aa8d-9c8d60d352af
source-git-commit: f64975793edc88a34d75965c8fae4967fae801c7
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# Configuración de la integración de AEM Assets para Commerce

La configuración de la integración de Adobe Experience Manager Assets para Commerce requiere acceso administrativo para personalizar la configuración de la aplicación y el entorno.

- Acceso administrativo al programa Cloud Manager donde se aprovisionan los entornos as a Cloud Service de AEM Assets.

- Acceso administrativo al entorno de Adobe Commerce y la capacidad de recuperar o generar las claves de API necesarias para la autenticación.

## Requisitos para utilizar la integración

Para aprovechar esta integración, las empresas deben cumplir los siguientes requisitos:

- Licencias activas para Adobe Commerce, Adobe Experience Manager Assets y [AEM Dynamic Media](https://experienceleague.adobe.com/es/docs/experience-manager-65/content/assets/dynamic/administering-dynamic-media).

- Adobe Commerce 2.4.5+

- Adobe Experience Manager está aprovisionado con [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/es/docs/experience-manager-cloud-service/content/assets/overview)

- El usuario de Adobe Commerce que configuró la integración debe tener acceso a la [organización de IMS](https://experienceleague.adobe.com/es/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) en la que se ha aprovisionado el proyecto de AEM Assets.

## Ventajas principales

- **Sin costo adicional**: esta integración se proporciona de forma gratuita para los comerciantes que cumplan con los requisitos de licencia.

- **Solución oficial de Adobe**: desarrollada, mantenida y totalmente compatible con Adobe, que garantiza estabilidad y alineación con futuras mejoras de la plataforma.

- **Modelo de soporte administrado por Adobe**: Adobe gestiona la asistencia y la solución de problemas, proporcionando tranquilidad y una solución de problemas más sencilla.

## Pasos siguientes

Habilitar la integración de Commerce con Experience Manager Assets es un proceso de tres pasos:

1. [Instalar paquete de AEM Assets](aem-assets-configure-aem.md).

1. [Instalar paquetes de Adobe Commerce](aem-assets-configure-aem.md).

1. [Configurar el recurso de integración](aem-assets-setup-synchronization.md).
