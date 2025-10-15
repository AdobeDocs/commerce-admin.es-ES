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

- Configurar [autenticación de doble factor](security-two-factor-authentication.md)
- Implementar [CAPTCHA](security-captcha.md) o [reCAPTCHA](security-google-recaptcha.md)
- Configure un [análisis de seguridad](security-scan.md) para cada dominio de la instalación de Adobe Commerce o de Magento Open Source.

>[!NOTE]
>
>Las tiendas que han habilitado la autenticación [!DNL Adobe Identity Management Services] (IMS) tienen Adobe Commerce nativo y el Magento Open Source 2FA deshabilitado. Los usuarios administradores que han iniciado sesión en su instancia de Commerce con sus credenciales de Adobe no necesitan volver a autenticarse en muchas tareas de administración. La autenticación la gestiona Adobe IMS cuando el usuario administrador inicia sesión en su sesión actual. Ver [[!DNL Adobe Identity Management Service] (IMS) Descripción general de la integración](../getting-started/adobe-ims-integration-overview.md).

Visite el [Centro de seguridad](https://helpx.adobe.com/es/security.html){:target=&quot;_blank&quot;} para obtener las últimas noticias sobre posibles vulnerabilidades, registrarse para recibir notificaciones de Seguridad de Adobe y acceder al Centro de confianza de Adobe.

![Centro de seguridad](./assets/product-security-home.png){width="700" zoomable="yes"}

Para obtener información acerca de las prácticas recomendadas de seguridad, consulte [Proteger el sitio e infraestructura de Commerce](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html?lang=es) en el _Libro de estrategias de implementación_.

## Plan de acción de seguridad

Si cree que el sitio de Adobe Commerce o del Magento Open Source está en peligro, siga este plan de acción sin demora.

1. **Diagnóstico**: ejecute un análisis para establecer el estado de seguridad de su tienda Commerce. Commerce [Security Scan](security-scan.md) es un servicio gratuito ofrecido por Adobe que le permite supervisar sus sitios Commerce para detectar riesgos de seguridad y malware conocidos, así como recibir notificaciones de seguridad.

1. **Limpiar**: contrata a un [consultor calificado](https://solutionpartners.adobe.com/s/directory/?partner_type=1) o servicio en línea para limpiar tu sitio de todo el código malintencionado. Algunos miembros de la comunidad de Commerce recomiendan [[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal). Compruebe si queda código ejecutable en la carpeta `/media`. Elimine todos los usuarios administradores desconocidos y restablezca todas las contraseñas de administración.

1. **Protect**: Mantenga su instalación de Commerce actualizada con la versión más reciente. Si utiliza una versión anterior, aplique todos los parches de seguridad a medida que estén disponibles. Revise y siga [las prácticas recomendadas de seguridad de Commerce](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). Suscribirse a [alertas de seguridad de Commerce](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **Informe**: Si cree que ha encontrado una vulnerabilidad específica en Commerce, [abra un problema con el Adobe](https://hackerone.com/adobe?type=team) e incluya detalles técnicos.

1. **Actualizar**: Para estar tranquilo con la asistencia las 24 horas del día, los 7 días de la semana, planifique ahora su actualización a [Adobe Commerce en nuestra arquitectura de nube](https://business.adobe.com/es/products/magento/cloud-delivery.html).
