---
title: Configuración de la integración de AEM Assets para Commerce
description: Obtenga información sobre cómo configurar su entorno de Experience Manager Assets para administrar los recursos de Commerce de su tienda.
feature: CMS, Media, Configuration
exl-id: 699f517e-1545-4c22-aa8d-9c8d60d352af
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
TQID: https://experienceleague.adobe.com/loyCmoFINQvC-13BGzAUKmcF7gY6T2e6mV-lK-SnVxo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 298
ht-degree: 3%

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
