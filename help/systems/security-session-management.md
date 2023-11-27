---
title: Administración de sesiones
description: Obtenga información sobre cómo configurar la administración de sesiones para proteger el administrador y la tienda.
exl-id: ad954218-aa3e-44e6-b23f-008de7fc7543
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Administración de sesiones

[Administración de sesiones](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html) es una práctica recomendada contra la denegación de servicio (DoS) para la seguridad de la API. Una sesión representa la cantidad de tiempo que un visitante emplea en el sitio y no está relacionada con el tiempo que los usuarios administradores o clientes inician sesión en sus cuentas.

Una sesión es una secuencia de transacciones de solicitud y respuesta HTTP de red asociadas al mismo usuario. Es una forma de asociar un cliente (administrador) con sus datos cuando accede al servidor. Las sesiones se utilizan para establecer variables, como derechos de acceso y configuración de localización, que se aplican a cada interacción que un usuario tiene con una aplicación web durante la sesión.

## Tamaño de sesión

Utilice las siguientes opciones de configuración para limitar el tamaño máximo de sesión para los usuarios administradores y los visitantes de tiendas:

- **[!UICONTROL Max Session Size in Admin]**: permite limitar el tamaño máximo de las sesiones en bytes. Uso `0` para deshabilitar.
- **[!UICONTROL Max Session Size in Storefront]**: permite limitar el tamaño máximo de las sesiones en bytes. Uso `0` para deshabilitar.

>[!TIP]
>
>Ambas configuraciones se miden en bytes y el valor predeterminado es `256000` bytes (o 256 KB).

**_Para configurar el tamaño máximo de la sesión:_**

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]**  > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL System]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Security]** para acceder a la configuración de la sesión.

   ![Configuración de sesión](../configuration-reference/advanced/assets/system-security.png){width="600" zoomable="yes"}

1. Introduzca nuevos tamaños de sesión en bytes.

   >[!WARNING]
   >
   >Configurar el valor demasiado bajo puede causar problemas. Si establece cualquiera de las opciones debajo del valor predeterminado de 256000 bytes, verá un mensaje de advertencia. Si hace clic **[!UICONTROL No]**, el sistema cambia el valor a `256000`.

1. Haga clic **[!UICONTROL Save Config]**.

### Sesiones de administración

Si supera el tamaño máximo de sesión, aparecerá un mensaje de error y el sistema registrará la restricción de tamaño de sesión en `var/log` directorio.

Si pierde el acceso al administrador después de establecer el tamaño de la sesión demasiado bajo, utilice la CLI para restablecer la configuración:

```bash
bin/magento config:set system/security/max_session_size_admin 256000
```

### Sesiones de tienda

Si supera el tamaño máximo de sesión, no se muestra ningún error, pero el sistema registra la restricción de tamaño de sesión en `var/log` directorio.

## Validación de sesión

Adobe Commerce y Magento Open Source permiten validar variables de sesión como medida de protección contra posibles ataques de fijación de sesión o intentos de envenenar o secuestrar sesiones de usuario. La configuración de validación de sesión determina cómo se validan las variables de sesión durante cada visita al almacén y si el ID de sesión se incluye en la dirección URL del almacén.

Para obtener información técnica, consulte [Usar Redis para el almacenamiento de sesión](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-session.html) en el _Guía de configuración_.

![Configuración general: validación de sesiones web](../configuration-reference/general/assets/web-session-validation-settings.png){width="600" zoomable="yes"}

La validación comprueba que los visitantes son quienes dicen ser comparando el valor de las variables de validación con los datos de sesión almacenados en `$_SESSION` datos del usuario. La validación falla si la información no se transmite según lo esperado y la variable correspondiente está vacía. Según la configuración de validación de sesión, si una variable de sesión falla en el proceso de validación, la sesión del cliente finaliza inmediatamente.

Habilitar todas las variables de validación puede ayudar a evitar ataques, pero también puede afectar al rendimiento del servidor. De forma predeterminada, toda la validación de variables de sesión está deshabilitada. Le recomendamos que experimente con la configuración para encontrar la mejor combinación para su instalación de Adobe Commerce o de Magento Open Source. La activación de todas las variables de validación puede resultar indebidamente restrictiva e impedir el acceso a los clientes que tienen conexiones a Internet que pasan a través de un servidor proxy o se originan detrás de un cortafuegos. Para obtener más información sobre las variables de sesión y su uso, consulte la documentación de administración del sistema para su sistema Linux®.

**_Para configurar la validación de la sesión:_**

1. En el _Administrador_ barra lateral, vaya a  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda _[!UICONTROL General]_y elija **[!UICONTROL Web]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Session Validation Settings]** sección.

1. Establezca cada una de las opciones de configuración:

   - **[!UICONTROL Validate REMOTE_ADDR]** — Definir como `Yes` para verificar que la dirección IP de una solicitud coincide con lo que se almacena en la variable `$_SESSION` variable.

   - **[!UICONTROL Validate HTTP_VIA]** — Definir como `Yes` para comprobar que la dirección proxy de una solicitud entrante coincide con lo que se almacena en la variable `$_SESSION` variable.

   - **[!UICONTROL Validate HTTP_X_FORWARDED_FOR]** — Definir como `Yes` para comprobar que la dirección de reenvío de una solicitud coincide con lo que se almacena en la variable `$_SESSION` variable.

   - **[!UICONTROL Validate HTTP_USER_AGENT]** — Definir como `Yes` para comprobar que el explorador o dispositivo utilizado para acceder al almacén durante una sesión coincide con lo almacenado en el `$_SESSION` variable.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Duración de sesión de administrador

Como medida de seguridad, la variable _Administrador_ se establece inicialmente para agotar el tiempo de espera después de 900 segundos (15 minutos) de inactividad del teclado. Puede ajustar la duración de la sesión para adaptarla al estilo de trabajo.

**_Para ajustar la duración de la sesión de administración:_**

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Desplazarse hacia abajo y expandir **[!UICONTROL Advanced]** en el panel lateral izquierdo.

1. Haga clic **[!UICONTROL Admin]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el _[!UICONTROL Security]_sección.

1. Para **[!UICONTROL Admin Session Lifetime (seconds)]**, introduzca el número de segundos que una sesión permanece activa antes de que se agote el tiempo de espera.

   ![Configuración avanzada: configuración de seguridad de administración](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.## Duración de la sesión de administrador

Como medida de seguridad, la variable _Administrador_ se establece inicialmente para agotar el tiempo de espera después de 900 segundos (15 minutos) de inactividad del teclado. Puede ajustar la duración de la sesión para adaptarla al estilo de trabajo.

**_Para ajustar la duración de la sesión de administración:_**

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Desplazarse hacia abajo y expandir **[!UICONTROL Advanced]** en el panel lateral izquierdo.

1. Haga clic **[!UICONTROL Admin]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el _Seguridad_ sección.

1. Para **[!UICONTROL Admin Session Lifetime (seconds)]**, introduzca el número de segundos que una sesión permanece activa antes de que se agote el tiempo de espera.

   ![Configuración avanzada: configuración de seguridad de administración](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.
