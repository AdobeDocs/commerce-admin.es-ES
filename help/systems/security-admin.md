---
title: Configurar la seguridad de administración
description: Aprenda a configurar la seguridad del administrador de su tienda.
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
TQID: https://experienceleague.adobe.com/UFK-C-W5E0DngIy4VncIVRzM2f6tNS5RgNqaNVk9GJc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
subfeature_v2:
  - id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 864
ht-degree: 0%

---

# Configurar la seguridad de administración

Le recomendamos que adopte un enfoque multifacético para proteger la seguridad de su tienda. Puede empezar por usar una [URL de administrador personalizada](../stores-purchase/store-urls.md#use-a-custom-admin-url) que no sea fácil de adivinar, en lugar de las obvias &quot;Admin&quot; o &quot;Backend&quot;. De manera predeterminada, las contraseñas que se usan para [iniciar sesión](../getting-started/admin-signin.md) en el administrador deben contener siete o más caracteres e incluir letras y números. Puede configurar el requisito de longitud mínima de contraseña para mejorar la seguridad según las necesidades de su organización. Como [práctica recomendada](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html), use solamente contraseñas de administrador seguras que incluyan una combinación de letras, números y símbolos. Adobe Commerce y Magento Open Source no permiten la reutilización de las cuatro últimas contraseñas asignadas a la cuenta.

La configuración de seguridad de administración le permite:

- Añadir una clave secreta a las direcciones URL
- Requerir que las contraseñas distingan entre mayúsculas y minúsculas
- Configurar el requisito de longitud mínima de contraseña
- Limitar la duración de las sesiones de administración
- Limitar la duración de las contraseñas
- Limite el número de intentos de inicio de sesión que pueden realizarse antes de que la cuenta de usuario administrador esté [bloqueada](permissions-users-all.md#locked-users).

Para aumentar la seguridad, puede configurar la duración de la inactividad del teclado antes de que caduque la sesión actual y requerir que el nombre de usuario y la contraseña distingan entre mayúsculas y minúsculas.

Además de la configuración de seguridad de esta sección, se requiere [autenticación de doble factor](security-two-factor-authentication.md) (2FA) para comprobar la identidad de los usuarios con una contraseña de un solo uso generada por una aplicación o dispositivo. Se le pedirá que configure 2FA la primera vez que inicie sesión en el administrador. Para mayor seguridad, el inicio de sesión de administrador también puede configurarse para requerir un [CAPTCHA](security-captcha.md).

>[!NOTE]
>
>Las tiendas que han habilitado la autenticación [!DNL Adobe Identity Management Services] (IMS) tienen Adobe Commerce nativo y Magento Open Source 2FA deshabilitado. Los usuarios administradores que han iniciado sesión en su instancia de Commerce con sus credenciales de Adobe no necesitan volver a autenticarse en muchas tareas de administración. La autenticación la gestiona Adobe IMS cuando el usuario administrador inicia sesión en su sesión actual. Ver [[!DNL Adobe Identity Management Service] (IMS) Descripción general de la integración](../getting-started/adobe-ims-integration-overview.md).

Para obtener información técnica, consulte [Información general de seguridad](https://developer.adobe.com/commerce/php/architecture/basics/security/){:target="_blank"} en la documentación para desarrolladores.

![Seguridad de administración](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## Configurar la seguridad de administración

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo bajo _[!UICONTROL Advanced]_, elija **[!UICONTROL Admin]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Security]**.

1. Para evitar que los usuarios administradores inicien sesión desde la misma cuenta en distintos dispositivos, establezca **[!UICONTROL Admin Account Sharing]** en `No`.

1. Para determinar el método que se usa para administrar las solicitudes de restablecimiento de contraseña, establezca **[!UICONTROL Password Reset Protection Type]** en uno de los siguientes:

   - `By IP and Email`: la contraseña se puede restablecer en línea después de recibir una respuesta de la notificación y enviarla a la dirección de correo electrónico asociada a la cuenta de administrador.
   - `By IP`: la contraseña se puede restablecer en línea sin confirmación adicional.
   - `By Email`: la contraseña solo se puede restablecer respondiendo por correo electrónico a la notificación que se envía a la dirección de correo electrónico asociada a la cuenta de administrador.
   - `None`: la contraseña solo la puede restablecer el administrador del almacén.

1. Establecer opciones de seguridad de inicio de sesión:

   - Para **[!UICONTROL Recovery Link Expiration Period (hours)]**, escriba el número de horas que un vínculo de recuperación de contraseña será válido.

   - Para determinar la cantidad máxima de solicitudes de contraseña que se pueden enviar por hora, ingrese el número de **[!UICONTROL Max Number of Password Reset Requests]**.

   - Para **[!UICONTROL Min Time Between Password Reset Requests]**, escriba el número mínimo de minutos que deben transcurrir entre solicitudes de restablecimiento de contraseña.

   - Para anexar una clave secreta a la dirección URL del administrador como medida de precaución contra ataques de explotación, establezca **[!UICONTROL Add Secret Key to URLs]** en `Yes`. Esta opción está habilitada de forma predeterminada.

   - Para requerir que el uso de caracteres en mayúsculas y minúsculas en las credenciales de inicio de sesión especificadas coincidan con lo que está almacenado en el sistema, establezca **[!UICONTROL Login is Case Sensitive]** en `Yes`.

   - Para determinar la duración de una sesión de administrador antes de que se agote el tiempo de espera, escriba la duración de la sesión en segundos para el campo **[!UICONTROL Admin Session Lifetime (seconds)]**. El valor debe ser de 60 segundos o más.

   - Para **[!UICONTROL Maximum Login Failures to Lockout Account]**, escriba el número de veces que un usuario puede intentar iniciar sesión en el Administrador antes de que se bloquee la cuenta. De forma predeterminada, se permiten seis intentos. Deje el campo vacío para intentos de inicio de sesión ilimitados.

   - Para **[!UICONTROL Lockout Time (minutes)]**, introduzca el número de minutos que una cuenta de administrador está bloqueada cuando se cumple el número máximo de intentos.

1. Establecer opciones de contraseña:

   - Para **[!UICONTROL Minimum Admin Password Length]**, introduzca el número mínimo de caracteres requeridos para las contraseñas de administrador. El valor predeterminado es 7 y el mínimo permitido es 7.

     >[!WARNING]
     >
     >Cambiar este valor del predeterminado puede introducir problemas de compatibilidad con versiones anteriores con servicios existentes. Esta configuración afecta a los cambios de contraseña de administrador, a la creación de nuevos usuarios de administrador desde la interfaz de administración y la CLI, y a las operaciones de restablecimiento de contraseña desde el administrador.

   - Para limitar la duración de las contraseñas de administrador, escriba el número de días durante los cuales una contraseña será válida para **[!UICONTROL Password Lifetime (days)]**. Deje el campo en blanco durante un tiempo ilimitado.

   - Establezca **[!UICONTROL Password Change]** en una de las siguientes opciones:

      - `Forced` — Requiere que los usuarios administradores cambien sus contraseñas después de configurar la cuenta.
      - `Recommended` — Recomienda que los usuarios administradores cambien sus contraseñas después de configurar la cuenta.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Requisitos de contraseña de administrador

De forma predeterminada, una contraseña de administrador debe tener siete caracteres o más e incluir letras y números. Puede usar la configuración **[!UICONTROL Minimum Admin Password Length]** para configurar el requisito mínimo de longitud de contraseña para cumplir con los estándares de seguridad de su organización. Sin embargo, aumentar este valor puede afectar a la compatibilidad con los servicios e integraciones existentes.
