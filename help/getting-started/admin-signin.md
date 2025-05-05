---
title: Su cuenta de usuario administrador
description: Obtenga información acerca de su cuenta de administrador y cómo utilizar la autenticación de doble factor para iniciar sesión en el administrador.
exl-id: ad576533-5914-49d1-8e73-3f59c55543a5
feature: Admin Workspace, User Account
source-git-commit: 54fdc97156c602337c983de5fddfafd7c50a67e1
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 0%

---

# Su cuenta de administrador

La cuenta de administrador principal se configuró inicialmente durante la instalación y puede contener información inicial de marcador de posición o información de datos de ejemplo. El propietario designado de esta cuenta puede personalizar el nombre de usuario y la contraseña y actualizar el nombre, los apellidos y la dirección de correo electrónico en cualquier momento. Esta cuenta, un _superusuario_ con todos los permisos de forma predeterminada, generalmente crea las cuentas de usuario de administrador necesarias para la empresa.

- Consulte [Crear un usuario](../systems/permissions-users-all.md#create-a-user) para obtener información sobre cómo agregar o editar usuarios.

- Consulte [Permisos](../systems/permissions.md) y [Funciones de usuario](../systems/permissions-user-roles.md) para obtener información sobre las funciones de administrador y usuario.

{{ims-admin-note}}

## Inicio de sesión de administrador

El [!DNL Commerce] _administrador_ está protegido por múltiples capas de medidas de seguridad para evitar el acceso no autorizado a los datos de tu tienda, pedidos y clientes. La primera vez que inicie sesión en _Admin_, deberá ingresar su nombre de usuario y contraseña y configurar la [autenticación de doble factor](../systems/security-two-factor-authentication.md) (2FA).

Dependiendo de la configuración de tu tienda, podría haber un desafío de [CAPTCHA](../systems/security-google-recaptcha.md) que resolver, como escribir una serie de caracteres de teclado, resolver un rompecabezas o hacer clic en una serie de imágenes con un tema común. Estas pruebas están diseñadas para identificarle como humano, en lugar de como un bot automatizado.

Para mayor seguridad, puede determinar a qué partes del _Administrador_ tiene acceso cada usuario [permiso](../systems/permissions.md), así como limitar el número de [intentos de inicio de sesión](../configuration-reference/advanced/admin.md). De forma predeterminada, después de seis intentos, la cuenta se bloquea y el usuario debe esperar unos minutos antes de intentarlo de nuevo. [Las cuentas bloqueadas](../systems/permissions-users-all.md#locked-users) también se pueden restablecer desde _Admin_.

>[!NOTE]
>
>La primera vez que inicie sesión en _Admin_, se le pedirá que _Permita la recopilación de datos de uso de administración_. Consulte [Recopilación de datos de uso](admin.md#usage-data-collection) para obtener más información.

![Inicio de sesión de administrador](./assets/admin-login.png){width="400"}

### Paso 1: Configurar la autenticación de doble factor

Para poder iniciar sesión en _Admin_ de tu tienda, debes tener configurada una solución de autenticación de doble factor y lista para usar. Para obtener más información acerca del proceso de autenticación usado por cada solución, vea [Usar la autenticación de doble factor](../systems/security-two-factor-authentication-use.md). De manera predeterminada, [!DNL Commerce] admite [Google Authenticator][1].

Pregunte al administrador del sistema [!DNL Commerce] qué soluciones 2FA se admiten en la tienda. A continuación, complete la configuración de su solución 2FA preferida según las instrucciones del proveedor.

### Paso 2: Inicio de sesión en el administrador

1. Escriba la dirección URL _Admin_ que se especificó durante la instalación de [!DNL Commerce].

   La dirección URL predeterminada _Admin_ se parece a `https://www.yourdomain.com/your-custom-admin-domain`.

   >[!NOTE]
   >
   >Aunque esta documentación usa `admin` como dirección URL base en la mayoría de los ejemplos, se recomienda que elija una [dirección URL personalizada](../stores-purchase/store-urls.md) única y difícil de adivinar para el _administrador_ de su tienda.

   Puede agregar un marcador para la página o guardar un acceso directo en el escritorio para facilitar el acceso.

1. Escriba su _administrador_ **[!UICONTROL Username]** y **[!UICONTROL Password]**.

1. (Opcional) Si un CAPTCHA está habilitado para su tienda, siga las instrucciones que aparecen en pantalla para resolver el desafío.

   Para obtener más información, consulte [CAPTCHA](../systems/security-captcha.md) y [reCAPTCHA](../systems/security-google-recaptcha.md).

1. Haga clic en **[!UICONTROL Sign in]**.

   Si es la primera vez que inicia sesión en _Admin_ desde la cuenta, debería recibir un mensaje de correo electrónico con un vínculo a las instrucciones de configuración.

### Paso 3: Completar la configuración de 2FA

El siguiente ejemplo muestra cómo emparejar su cuenta de _Admin_ con Google Authenticator.

1. Cuando aparezca el código QR, use uno de los siguientes métodos para capturar el código y emparejar Google Authenticator con su cuenta de _Admin_.

   ![Configurar el autenticador de Google](./assets/admin-login-google-auth-setup.png){width="400"}

   - Captura de código QR con un smartphone

     En el smartphone, inicie Google Authenticator. Pulse el _signo más_ (+) en la esquina superior derecha de la aplicación. A continuación, en la parte inferior de la pantalla, pulse **[!UICONTROL Scan Barcode]** y tome una imagen del código QR.

   - Capturar código QR desde el explorador

     Si Google Authenticator está instalado como extensión en el explorador, haga clic en el icono **Autenticador** de la barra de herramientas y capture la página.

   - Introducir código QR manualmente

     Copie la cadena de texto debajo del código QR. Inicie Google Authenticator con el teléfono inteligente o el explorador y haga clic en el signo más (+). A continuación, elija **[!UICONTROL Manual Entry]**. En **[!UICONTROL Account]**, escriba la dirección de correo electrónico asociada a su cuenta de _Admin_ y pegue la cadena del código QR en el campo **[!UICONTROL Key]**.

1. Para iniciar sesión en _Admin_ con autenticación de doble factor, ingrese el código de seis dígitos generado por Google Authenticator en el campo **[!UICONTROL Authenticator code]** y luego haga clic en **[!UICONTROL Confirm]**.

   ![Escriba el código de autenticador](./assets/admin-login-2fa-google.png){width="400"}

## Restablecer la contraseña

No se permite la reutilización de las cuatro últimas contraseñas asignadas a la cuenta.

1. Escriba el(la) **[!UICONTROL Email Address]** asociado(a) a la cuenta _Admin_.

   ![Contraseña olvidada](./assets/admin-sign-in-forgot-password.png){width="400"}

1. Haga clic en **[!UICONTROL Retrieve Password]**.

   Si una cuenta está asociada con la dirección de correo electrónico, se envía un correo electrónico para restablecer la contraseña.

   >[!NOTE]
   >
   >Una contraseña de _Admin_ debe contener al menos siete caracteres e incluir letras y números. Consulte [Configuración de la seguridad de _Admin_](../systems/security-admin.md) para obtener información sobre las opciones de contraseña.

## Cerrar sesión del administrador

1. En la esquina superior derecha, haga clic en el icono _Cuenta_ (![Cuenta](../assets/icon-admin-user.png)).

1. Haga clic en **[!UICONTROL Sign Out]**.

   ![Cerrar sesión](./assets/admin-sign-out.png){width="700" zoomable="yes"}

La página _[!UICONTROL Sign In]_&#x200B;muestra un mensaje que indica que ha cerrado la sesión. Cierre la sesión de_ Admin _cada vez que deje su equipo desatendido.

## Editar información de la cuenta

1. Haga clic en el icono _Cuenta_ (![Icono de cuenta](../assets/icon-admin-user.png)).

1. Haga clic en **[!UICONTROL Account Setting]**.

   ![Información de la cuenta](./assets/admin-account-information.png){width="700" zoomable="yes"}

1. Realice los cambios necesarios en la información de su cuenta.

   Si cambia sus credenciales de inicio de sesión, asegúrese de almacenarlas en una ubicación segura.

1. Escriba la contraseña de la cuenta actual.

1. Haga clic en **[!UICONTROL Save Account]**.

## Permitir varios inicios de sesión de administrador

El administrador proporciona acceso para administrar las funciones de pedidos, clientes, productos, envíos y pagos. La configuración predeterminada está establecida para no permitir varios inicios de sesión en una cuenta de usuario de administrador como práctica recomendada de seguridad. Sin embargo, puede cambiar esta configuración para permitir que los usuarios administradores inicien sesión desde varios dispositivos y así dar cabida a los flujos de trabajo empresariales.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel de navegación izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL Admin]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Security]**.

1. Para **Compartir cuenta de administrador**, seleccione `Yes`.

   ![Permitir que se comparta la cuenta de administrador](./assets/multiple-admin-login.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save Config]**.

## Definir nombres de inicio de sesión de usuario de administrador con distinción de mayúsculas y minúsculas

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel de navegación izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL Admin]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Security]**.

1. Establezca el campo **[!UICONTROL Login is Case Sensitive]** en `Yes`.

1. Haga clic en **[!UICONTROL Save Config]**.

[1]: https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&amp;hl=en_US

## Mantener un acceso seguro al administrador

Para garantizar la seguridad de su administrador, realice auditorías regulares de los usuarios y las funciones con acceso de administrador.

Además, considere [actualizar la configuración de la URL de Admin Base](https://experienceleague.adobe.com/es/docs/commerce-admin/config/advanced/admin#admin-base-url) para cambiar el punto de conexión `/admin` predeterminado a una ruta de acceso personalizada. La configuración de una ruta personalizada ofrece las siguientes ventajas de seguridad:

**Seguridad mejorada**: La ruta de acceso &quot;admin&quot; predeterminada es ampliamente conocida y a menudo está dirigida por agentes malintencionados que intentan realizar ataques por fuerza bruta. Al cambiarlo a un valor único y personalizado, se reduce significativamente el riesgo de intentos de acceso no autorizados.

**Vulnerabilidad reducida**: los bots automatizados suelen buscar rutas comunes como &quot;admin&quot; para aprovechar las vulnerabilidades. Una ruta personalizada dificulta la localización de la página de inicio de sesión del administrador por parte de estos bots, lo que reduce la probabilidad de ataques.

**Privacidad mejorada**: una ruta de acceso de administrador personalizada agrega una capa adicional de oscuridad, lo que dificulta que los atacantes potenciales identifiquen y segmenten su página de inicio de sesión de administrador.

**Cumplimiento de las prácticas recomendadas**: Las siguientes prácticas recomendadas de seguridad, como personalizar la ruta de administración, muestran un enfoque proactivo para proteger el sitio de comercio electrónico y los datos de los clientes.

>[!NOTE]
>
>Si se sospecha una infracción, asegúrese de eliminar todos los usuarios administradores desconocidos, restablecer todas las contraseñas de administración y revisar el [plan de acción de seguridad](https://experienceleague.adobe.com/es/docs/commerce-admin/systems/security/security) para ver los pasos siguientes.
