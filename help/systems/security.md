---
title: Seguridad
description: Obtenga información sobre las herramientas disponibles para proteger sus tiendas y datos, y las directrices para un plan de acción de seguridad si detecta un compromiso.
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
TQID: https://experienceleague.adobe.com/9aJ-ZVqwaIr2IJTY6e2hp3eoZe2v6sxz6WdqP2FiPTc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 412
ht-degree: 0%

---

# Seguridad

Existen varias formas de proteger su tienda y mantener la seguridad de sus datos:

- Configurar [autenticación de doble factor](security-two-factor-authentication.md)
- Implementar [CAPTCHA](security-captcha.md) o [reCAPTCHA](security-google-recaptcha.md)
- Configure un [análisis de seguridad](security-scan.md) para cada dominio de la instalación de Adobe Commerce o Magento Open Source.

>[!NOTE]
>
>Las tiendas que han habilitado la autenticación [!DNL Adobe Identity Management Services] (IMS) tienen Adobe Commerce nativo y Magento Open Source 2FA deshabilitado. Los usuarios administradores que han iniciado sesión en su instancia de Commerce con sus credenciales de Adobe no necesitan volver a autenticarse en muchas tareas de administración. La autenticación la gestiona Adobe IMS cuando el usuario administrador inicia sesión en su sesión actual. Ver [[!DNL Adobe Identity Management Service] (IMS) Descripción general de la integración](../getting-started/adobe-ims-integration-overview.md).

Visite [Security Center](https://helpx.adobe.com/es/security.html){:target="_blank"} para obtener las últimas noticias sobre posibles vulnerabilidades, regístrese para recibir notificaciones de seguridad de Adobe y acceda al Centro de confianza de Adobe.

![Centro de seguridad](./assets/product-security-home.png){width="700" zoomable="yes"}

Para obtener información acerca de las prácticas recomendadas de seguridad, consulte [Proteger el sitio e infraestructura de Commerce](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html?lang=es) en el _Libro de estrategias de implementación_.

## Plan de acción de seguridad

Si sospecha que su sitio de Adobe Commerce o Magento Open Source está en peligro, siga este plan de acción sin demora.

1. **Diagnóstico**: ejecute un análisis para establecer el estado de seguridad de su tienda Commerce. Commerce [Security Scan](security-scan.md) es un servicio gratuito ofrecido por Adobe que le permite supervisar sus sitios Commerce para detectar riesgos de seguridad y malware conocidos, así como recibir notificaciones de seguridad.

1. **Limpiar**: contrata a un [consultor calificado](https://solutionpartners.adobe.com/s/directory/?partner_type=1) o servicio en línea para limpiar tu sitio de todo el código malintencionado. Algunos miembros de la comunidad de Commerce recomiendan [[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal). Compruebe si queda código ejecutable en la carpeta `/media`. Elimine todos los usuarios administradores desconocidos y restablezca todas las contraseñas de administración.

1. **Proteger**: Mantén actualizada tu instalación de Commerce con la versión más reciente. Si utiliza una versión anterior, aplique todos los parches de seguridad a medida que estén disponibles. Revise y siga [las prácticas recomendadas de seguridad de Commerce](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). Suscribirse a [alertas de seguridad de Commerce](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **Informe**: Si cree que ha encontrado una vulnerabilidad específica en Commerce, [abra un problema con Adobe](https://hackerone.com/adobe?type=team) e incluya detalles técnicos.

1. **Actualizar**: Para estar tranquilo con la asistencia las 24 horas del día, los 7 días de la semana, planifique ahora su actualización a [Adobe Commerce en nuestra arquitectura de nube](https://business.adobe.com/es/products/magento/cloud-delivery.html).
