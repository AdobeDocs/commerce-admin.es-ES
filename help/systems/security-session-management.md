---
title: Administración de sesiones
description: Obtenga información sobre cómo configurar la administración de sesiones para proteger el administrador y la tienda.
exl-id: ad954218-aa3e-44e6-b23f-008de7fc7543
role: Admin
feature: Configuration, Security
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# Administración de sesiones

[La administración de sesiones](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html) es una práctica recomendada para la seguridad de la API que impide la denegación de servicio (DoS). Una sesión representa la cantidad de tiempo que un visitante emplea en el sitio y no está relacionada con el tiempo que los usuarios administradores o clientes inician sesión en sus cuentas.

Una sesión es una secuencia de transacciones de solicitud y respuesta HTTP de red asociadas al mismo usuario. Es una forma de asociar un cliente (administrador) con sus datos cuando accede al servidor. Las sesiones se utilizan para establecer variables, como derechos de acceso y configuración de localización, que se aplican a cada interacción que un usuario tiene con una aplicación web durante la sesión.

## Tamaño de sesión

Utilice las siguientes opciones de configuración para limitar el tamaño máximo de sesión para los usuarios administradores y los visitantes de tiendas:

- **[!UICONTROL Max Session Size in Admin]**: limitar el tamaño máximo de sesiones en bytes. Use `0` para deshabilitar.
- **[!UICONTROL Max Session Size in Storefront]**: limitar el tamaño máximo de sesiones en bytes. Use `0` para deshabilitar.

>[!TIP]
>
>Ambas configuraciones se miden en bytes y el valor predeterminado es `256000` bytes (o 256 KB).

**_Para configurar el tamaño máximo de la sesión:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL System]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Security]** para obtener acceso a la configuración de la sesión.

   ![Configuración de sesión](../configuration-reference/advanced/assets/system-security.png){width="600" zoomable="yes"}

1. Introduzca nuevos tamaños de sesión en bytes.

   >[!WARNING]
   >
   >Configurar el valor demasiado bajo puede causar problemas. Si establece cualquiera de las opciones debajo del valor predeterminado de 256000 bytes, verá un mensaje de advertencia. Si hace clic en **[!UICONTROL No]**, el sistema cambia el valor a `256000`.

1. Haga clic en **[!UICONTROL Save Config]**.

### Sesiones de administración

Si supera el tamaño máximo de sesión, aparecerá un mensaje de error y el sistema registrará la restricción de tamaño de sesión en el directorio `var/log`.

Si pierde el acceso al administrador después de establecer el tamaño de la sesión demasiado bajo, utilice la CLI para restablecer la configuración:

```bash
bin/magento config:set system/security/max_session_size_admin 256000
```

### Sesiones de tienda

Si se supera el tamaño máximo de sesión, no se muestra ningún error, pero el sistema registra la restricción de tamaño de sesión en el directorio `var/log`.

## Validación de sesión

Adobe Commerce y Magento Open Source permiten validar variables de sesión como medida de protección contra posibles ataques de fijación de sesión o intentos de envenenar o secuestrar sesiones de usuario. La configuración de validación de sesión determina cómo se validan las variables de sesión durante cada visita al almacén y si el ID de sesión se incluye en la dirección URL del almacén.

Para obtener información técnica, consulte [Usar Redis para el almacenamiento de sesión](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-session.html?lang=es) en la _Guía de configuración_.

![Configuración general: validación de sesión web](../configuration-reference/general/assets/web-session-validation-settings.png){width="600" zoomable="yes"}

La validación comprueba que los visitantes son quienes dicen ser comparando el valor de las variables de validación con los datos de sesión almacenados en `$_SESSION` para el usuario. La validación falla si la información no se transmite según lo esperado y la variable correspondiente está vacía. Según la configuración de validación de sesión, si una variable de sesión falla en el proceso de validación, la sesión del cliente finaliza inmediatamente.

Habilitar todas las variables de validación puede ayudar a evitar ataques, pero también puede afectar al rendimiento del servidor. De forma predeterminada, toda la validación de variables de sesión está deshabilitada. Le recomendamos que experimente con la configuración para encontrar la mejor combinación para su instalación de Adobe Commerce o Magento Open Source. La activación de todas las variables de validación puede resultar indebidamente restrictiva e impedir el acceso a los clientes que tienen conexiones a Internet que pasan a través de un servidor proxy o se originan detrás de un cortafuegos. Para obtener más información sobre las variables de sesión y su uso, consulte la documentación de administración del sistema para su sistema Linux®.

**_Para configurar la validación de la sesión:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda _[!UICONTROL General]_&#x200B;y elija **[!UICONTROL Web]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Session Validation Settings]**.

1. Establezca cada una de las opciones de configuración:

   - **[!UICONTROL Validate REMOTE_ADDR]** — Se establece en `Yes` para comprobar que la dirección IP de una solicitud coincide con lo almacenado en la variable `$_SESSION`.

   - **[!UICONTROL Validate HTTP_VIA]** — Se establece en `Yes` para comprobar que la dirección proxy de una solicitud entrante coincide con lo que está almacenado en la variable `$_SESSION`.

   - **[!UICONTROL Validate HTTP_X_FORWARDED_FOR]** — Se establece en `Yes` para comprobar que la dirección de reenvío de una solicitud coincide con lo almacenado en la variable `$_SESSION`.

   - **[!UICONTROL Validate HTTP_USER_AGENT]** — Se establece en `Yes` para comprobar que el explorador o dispositivo que se usa para tener acceso al almacén durante una sesión coincide con lo que se almacena en la variable `$_SESSION`.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Duración de sesión de administrador

Como medida de seguridad, _Admin_ se ha configurado inicialmente para que agote el tiempo de espera tras 900 segundos (15 minutos) de inactividad del teclado. Puede ajustar la duración de la sesión para adaptarla al estilo de trabajo.

**_Para ajustar la duración de la sesión de administración:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Desplácese hacia abajo y expanda **[!UICONTROL Advanced]** en el panel lateral izquierdo.

1. Haga clic en **[!UICONTROL Admin]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Security]**.

1. Para **[!UICONTROL Admin Session Lifetime (seconds)]**, escriba el número de segundos que una sesión permanecerá activa antes de que se agote el tiempo de espera.

   ![Configuración avanzada - Configuración de seguridad de administración](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
