---
title: Información general sobre la integración de Adobe Identity Management Service (IMS)
description: Presenta la integración opcional del inicio de sesión del administrador de Adobe Commerce con Adobe IMS
exl-id: 106d731c-a541-4a19-a38c-221e80740508
feature: Identity Management
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# Información general sobre la integración de Adobe Identity Management Service (IMS)

{{ee-feature}}

Los usuarios administradores de Adobe Commerce que tengan una cuenta de Adobe ahora pueden utilizar su Adobe ID para iniciar sesión en Adobe Commerce. Adobe El servicio Identity Management (IMS) es una función de administración de identidades basada en OAuth 2.0 de Adobe que admite la autenticación. La integración de la autenticación de administración de Commerce en el flujo de trabajo de autenticación IMS del producto empresarial de Adobe puede optimizar el proceso de autenticación para los usuarios que trabajan con otros productos de Adobe. Esta integración es opcional y se habilita por instancia. Cuando esta integración está habilitada, solo se ven afectados los flujos de trabajo de usuarios administradores. 

Los módulos necesarios para la integración de IMS de administración de Commerce están empaquetados en  `adobe-ims-metapackage`, que está empaquetado con las versiones principales de Adobe Commerce.

Para implementar esta integración, consulte [Configuración de la integración de administración de Commerce con IMS](./adobe-ims-config.md).

## Cambios en los flujos de trabajo de administración y la interfaz después de la integración con IMS

Cuando esta integración está habilitada, los usuarios de administración de Commerce experimentan cambios en el inicio de sesión de administración de Commerce y en el flujo de trabajo de autenticación predeterminados, ya que realizan tareas rutinarias en la administración que requieren volver a autenticarse, como crear un usuario de administración. Se requiere la aplicación de autenticación de doble factor (2FA) en el nivel de organización de Adobe para la habilitación de módulos. El inicio de sesión de administrador predeterminado y los 2FA están deshabilitados, y el _[!UICONTROL Sign In with Adobe ID]_reemplaza el formulario predeterminado de inicio de sesión de administrador. Los derechos se siguen administrando desde el administrador.

## Cómo afecta la integración de administradores con IMS a las contraseñas de Commerce

Las implementaciones de Commerce que se han integrado con Adobe IMS requieren una cuenta de Adobe ID con acceso a la organización IMS de Adobe configurada para la aplicación Commerce durante el proceso de habilitación de IMS.  Cuando la integración de IMS está habilitada, los usuarios administradores se autentican a través de la página de inicio de sesión de Adobe con sus credenciales de Adobe. Las contraseñas y los nombres de usuario de Commerce para los usuarios administradores ya no se utilizan para la autenticación siempre y cuando la integración de Adobe IMS esté habilitada.

Si la integración de IMS está desactivada, los usuarios administradores deben volver a autenticarse a través de Adobe Commerce con su nombre de usuario y contraseña de Commerce. Los usuarios administradores deben guardar sus credenciales de administración de Commerce (nombre de usuario y contraseña) y sus credenciales de 2FA antes de habilitar esta integración.

Algunos componentes back-end que participan en la autenticación de usuarios aún requieren una contraseña que no sea nula. Para cumplir este requisito, Commerce crea contraseñas aleatorias para los usuarios administradores recién creados en `admin_user` tabla.

Las cuentas de usuario y los permisos de funciones para la aplicación de Commerce se siguen administrando desde el administrador de Commerce.


## Generación de tokens de API web con credenciales de IMS

Las API de administración de Commerce se ven afectadas cuando la autenticación de administración con Adobe IMS está habilitada en una instancia de Commerce. Los usuarios administradores ya no pueden utilizar las credenciales emitidas por la instancia de Commerce. Estas son las credenciales necesarias para iniciar sesión en el administrador y para obtener tokens de acceso que los servicios de puedan utilizar para realizar solicitudes a las API de REST y SOAP de administrador.

Una vez habilitada la integración de Adobe IMS, los usuarios administradores deben utilizar [Tokens de OAuth de Adobe IMS](https://developer.adobe.com/developer-console/docs/guides/authentication/OAuthIntegration/) para puntos finales de API de Adobe Commerce que requieren autenticación. Las soluciones de cliente obtienen los tokens de forma dinámica para el uso de API web. Este mecanismo de autenticación está habilitado para las áreas de API web REST y SOAP como parte de la configuración de esta integración.

Consulte [Autenticación basada en tokens](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-token/) para obtener información general sobre cómo las API web utilizan tokens de acceso de Commerce, incluidos los tokens de acceso de IMS.

## Administración de sesiones de Commerce y tokens de acceso de Adobe IMS

Los tokens de acceso contienen credenciales de usuario e información de sesión de inicio de sesión. Una vez que se ha autenticado un usuario y se ha iniciado una sesión, estas dos variables se agregan a la sesión del usuario:

`token_last_check_time`. Identifica la hora actual y la utiliza el `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` plugin.

`adobe_access_token` — Identifica el `ACCESS_TOKEN` valor recibido durante la autorización.

El `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` El complemento comprueba si la variable `token_last_check_time` se actualizó hace 10 minutos. Si la variable `token_last_check_time` se comprobó hace diez minutos, luego el flujo de trabajo de autenticación realiza una llamada de API a IMS para validar el token de acceso y la sesión continúa. Si el token de acceso es válido, la variable `token_last_check_time` El valor de se ha actualizado a la hora actual. Si el token no es válido, la sesión finaliza.

## Archivos importantes

`adminAdobeIms` : Proporciona una implementación del inicio de sesión del administrador en función del `AdobeImsApi` módulo.

`admin_adobe_ims_webapi` : Mantiene un registro de todos los tokens de acceso validados. Cuando se valida o invalida un token, en esta tabla se conserva un registro de su estado.

`adobeIms` : implementa toda la lógica empresarial relacionada con la integración con Adobe IMS (conservada para evitar incompatibilidades con versiones anteriores).

`adobeImsApi` : Declara las interfaces que admiten la integración con Adobe IMS.

`adminadobe-ims.log` - Archivo de registro de errores.

## Habilitar la integración

El metapaquete de Adobe IMS se instala con Adobe Commerce 2.4.5 y versiones posteriores, pero debe configurarse para su uso. Amplía el `AdobeIms` para admitir el módulo que habilita la lógica de autenticación (`AdminAdobeIms`).

Para obtener más información sobre cómo activar la integración, consulte [Configuración de la integración de administración de Commerce con Adobe IMS](./adobe-ims-config.md).
