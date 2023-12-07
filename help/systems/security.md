---
title: Seguridad
description: Obtenga información sobre las herramientas disponibles para proteger sus tiendas y datos, y las directrices para un plan de acción de seguridad si detecta un compromiso.
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
source-git-commit: fede05a413428520eec89d46f41a1cdd9c9c3a2e
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Seguridad

Existen varias formas de proteger su tienda y mantener la seguridad de sus datos:

- Configuración de [autenticación de doble factor](security-two-factor-authentication.md)
- Implementación [CAPTCHA](security-captcha.md) o [reCAPTCHA](security-google-recaptcha.md)
- Configuración de un [Análisis de seguridad](security-scan.md) para cada dominio de la instalación de Adobe Commerce o Magento Open Source.

>[!NOTE]
>
>Tiendas que han activado [!DNL Adobe Identity Management Services] La autenticación (IMS) tiene Adobe Commerce nativo y el Magento Open Source 2FA deshabilitado. Los usuarios administradores que han iniciado sesión en su instancia de Commerce con sus credenciales de Adobe no necesitan volver a autenticarse en muchas tareas de administración. La autenticación la gestiona Adobe IMS cuando el usuario administrador inicia sesión en su sesión actual. Consulte [[!DNL Adobe Identity Management Service] (IMS) Resumen de la integración](../getting-started/adobe-ims-integration-overview.md).

Visite la [Centro de seguridad](https://helpx.adobe.com/security.html){:target=&quot;_blank&quot;} para obtener las últimas noticias sobre posibles vulnerabilidades, registrarse para recibir notificaciones de seguridad de Adobe y acceder al Centro de confianza de Adobe.

![Centro de seguridad](./assets/product-security-home.png){width="700" zoomable="yes"}

Para obtener información sobre las prácticas recomendadas de seguridad, consulte [Proteja su sitio de comercio e infraestructura](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html) en el _Guía de implementación_.

## Plan de acción de seguridad

Si cree que el sitio de Adobe Commerce o del Magento Open Source está en peligro, siga este plan de acción sin demora.

1. **Diagnosticar**: ejecute un análisis para establecer el estado de seguridad de su tienda de Commerce. Comercio [Análisis de seguridad](security-scan.md) es un servicio gratuito ofrecido por Adobe que le permite supervisar sus sitios de Commerce en busca de riesgos de seguridad y malware conocidos, así como recibir notificaciones de seguridad.

1. **Limpiar**: Contratar a [consultor cualificado](https://solutionpartners.adobe.com/s/directory/?partner_type=1) o servicio en línea para limpiar el sitio de todo el código malintencionado. Algunos miembros de la comunidad de Commerce recomiendan [[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal). Compruebe la `/media` carpeta para el código ejecutable restante. Elimine todos los usuarios administradores desconocidos y restablezca todas las contraseñas de administración.

1. **Protect**: Mantenga la instalación de Commerce actualizada con la versión más actual. Si utiliza una versión anterior, aplique todos los parches de seguridad a medida que estén disponibles. Revisar y seguir [Prácticas recomendadas de seguridad de Commerce](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). Suscribirse a [Alertas de seguridad comercial](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **Informe**: Si cree que ha encontrado una vulnerabilidad específica en Commerce, [Abrir un problema con el Adobe](https://hackerone.com/adobe?type=team) e incluir detalles técnicos.

1. **Actualizar**: Para obtener la tranquilidad adicional que proporciona la asistencia 24/7, planifique la actualización a [Adobe Commerce en nuestra arquitectura de nube](https://business.adobe.com/products/magento/cloud-delivery.html) ahora.
