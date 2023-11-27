---
title: Configurar la seguridad de administración
description: Aprenda a configurar la seguridad del administrador de su tienda.
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
source-git-commit: e301cfaeec3a8427fff6138ba041bdbd7433c137
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%

---

# Configurar la seguridad de administración

Le recomendamos que adopte un enfoque multifacético para proteger la seguridad de su tienda. Puede empezar por usar una [URL de administrador personalizada](../stores-purchase/store-urls.md#use-a-custom-admin-url) esto no es fácil de adivinar, más que el obvio &quot;Admin&quot; o &quot;Backend&quot;. De forma predeterminada, las contraseñas utilizadas para [iniciar sesión](../getting-started/admin-signin.md) para el administrador debe tener siete caracteres o más e incluir letras y números. As a [práctica recomendada](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html), utilice únicamente contraseñas de administrador seguras que incluyan una combinación de letras, números y símbolos. Adobe Commerce y Magento Open Source no permiten la reutilización de las últimas cuatro contraseñas asignadas a la cuenta.

La configuración de seguridad de administración le permite:

- Añadir una clave secreta a las direcciones URL
- Requerir que las contraseñas distingan entre mayúsculas y minúsculas
- Limitar la duración de las sesiones de administración
- Limitar la duración de las contraseñas
- Limitar el número de intentos de inicio de sesión que se pueden realizar antes de que se abra la cuenta de usuario Administrador [bloqueado](permissions-users-all.md#locked-users).

Para aumentar la seguridad, puede configurar la duración de la inactividad del teclado antes de que caduque la sesión actual y requerir que el nombre de usuario y la contraseña distingan entre mayúsculas y minúsculas.

Además de la configuración de seguridad de esta sección, [autenticación de doble factor](security-two-factor-authentication.md) (2FA) es necesario para verificar la identidad de los usuarios con una contraseña única generada por una aplicación o dispositivo. Se le pedirá que configure 2FA la primera vez que inicie sesión en el administrador. Para mayor seguridad, el inicio de sesión de administrador también se puede configurar para requerir una [CAPTCHA](security-captcha.md).

>[!NOTE]
>
>Tiendas que han activado [!DNL Adobe Identity Management Services] La autenticación (IMS) tiene Adobe Commerce nativo y el Magento Open Source 2FA deshabilitado. Los usuarios administradores que han iniciado sesión en su instancia de Commerce con sus credenciales de Adobe no necesitan volver a autenticarse en muchas tareas de administración. La autenticación la gestiona Adobe IMS cuando el usuario administrador inicia sesión en su sesión actual. Consulte [[!DNL Adobe Identity Management Service] (IMS) Resumen de la integración](../getting-started/adobe-ims-integration-overview.md).

Para obtener información técnica, consulte [Información general de seguridad](https://developer.adobe.com/commerce/php/architecture/basics/security/){:target=&quot;_blank&quot;} en la documentación para desarrolladores.

![Seguridad de administración](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## Configurar la seguridad de administración

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, debajo de _[!UICONTROL Advanced]_, elija **[!UICONTROL Admin]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Security]** sección.

1. Para evitar que los usuarios administradores inicien sesión desde la misma cuenta en distintos dispositivos, establezca **[!UICONTROL Admin Account Sharing]** hasta `No`.

1. Para determinar el método que se utiliza para administrar las solicitudes de restablecimiento de contraseña, establezca **[!UICONTROL Password Reset Protection Type]** a uno de los siguientes:

   - `By IP and Email` — La contraseña se puede restablecer en línea después de recibir una respuesta de la notificación a la dirección de correo electrónico asociada a la cuenta de administrador.
   - `By IP` — La contraseña se puede restablecer en línea sin confirmación adicional.
   - `By Email` — La contraseña solo se puede restablecer respondiendo por correo electrónico a la notificación que se envía a la dirección de correo electrónico asociada a la cuenta de administrador.
   - `None` — La contraseña sólo puede ser restablecida por el administrador del almacén.

1. Establecer opciones de seguridad de inicio de sesión:

   - Para **[!UICONTROL Recovery Link Expiration Period (hours)]**, introduzca el número de horas que un vínculo de recuperación de contraseña sigue siendo válido.

   - Para determinar el número máximo de solicitudes de contraseña que se pueden enviar por hora, introduzca el número de **[!UICONTROL Max Number of Password Reset Requests]**.

   - Para **[!UICONTROL Min Time Between Password Reset Requests]**, introduzca el número mínimo de minutos que deben transcurrir entre solicitudes de restablecimiento de contraseña.

   - Para anexar una clave secreta a la URL de administración como medida de precaución frente a ataques de explotación, establezca **[!UICONTROL Add Secret Key to URLs]** hasta `Yes`. Esta opción está habilitada de forma predeterminada.

   - Para requerir que el uso de caracteres en mayúsculas y minúsculas en las credenciales de inicio de sesión especificadas coincidan con lo que se almacena en el sistema, establezca **[!UICONTROL Login is Case Sensitive]** hasta `Yes`.

   - Para determinar la duración de una sesión de administrador antes de que se agote el tiempo de espera, introduzca la duración de la sesión en segundos para **[!UICONTROL Admin Session Lifetime (seconds)]** field. El valor debe ser de 60 segundos o más.

   - Para **[!UICONTROL Maximum Login Failures to Lockout Account]**, introduzca el número de veces que un usuario puede intentar iniciar sesión en el administrador antes de que se bloquee la cuenta. De forma predeterminada, se permiten seis intentos. Deje el campo vacío para intentos de inicio de sesión ilimitados.

   - Para **[!UICONTROL Lockout Time (minutes)]**, introduzca el número de minutos que una cuenta de administrador está bloqueada cuando se cumple el número máximo de intentos.

1. Establecer opciones de contraseña:

   - Para limitar la duración de las contraseñas de administrador, introduzca el número de días durante los cuales una contraseña es válida **[!UICONTROL Password Lifetime (days)]**. Deje el campo en blanco durante un tiempo ilimitado.

   - Establecer **[!UICONTROL Password Change]** a uno de los siguientes:

      - `Forced` — Requiere que los usuarios administradores cambien sus contraseñas después de configurar la cuenta.
      - `Recommended` — Recomienda que los usuarios administradores cambien sus contraseñas después de configurar la cuenta.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Requisitos de contraseña de administrador

De forma predeterminada, una contraseña de administrador debe tener siete caracteres o más e incluir letras y números.
