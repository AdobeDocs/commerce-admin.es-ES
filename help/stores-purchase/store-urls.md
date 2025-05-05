---
title: URL de tienda
description: Obtenga información sobre las direcciones URL de tienda y cómo configurar la dirección URL base y los códigos de tienda.
exl-id: dd7a6317-b0cf-4d0c-9b31-a963c467026b
feature: Site Management, System
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '1529'
ht-degree: 0%

---

# URL de tienda

Cada sitio web de una instalación de Adobe Commerce o Magento Open Source tiene una dirección URL base asignada a la tienda y otra dirección URL asignada al administrador. Adobe utiliza variables para definir vínculos internos en relación con la dirección URL base, lo que permite mover un almacén completo de una ubicación a otra sin actualizar los vínculos. Las direcciones URL base estándar comienzan por `http` y las direcciones URL base segura comienzan por `https`.

- **URL base** — `http://www.yourdomain.com/magento/`
- **URL base segura** — `https://www.yourdomain.com/magento/`
- **URL con dirección IP** — `http://###.###.###.###/magento/` o `https://###.###.###.###/magento/`

>[!IMPORTANT]
>
>No cambie la URL de administración de la configuración de URL base predeterminada. Para cambiar la dirección URL o la ruta de acceso del administrador, consulte [Usar una dirección URL de administrador personalizada](#use-a-custom-admin-url).

## Usar un protocolo seguro

Las direcciones URL base de su tienda se configuraron inicialmente durante la instalación de Adobe Commerce. Si había un certificado de seguridad disponible en ese momento, podría especificar las direcciones URL de `HTTPS` que se usarán para el almacén, el administrador o ambos. Si la instalación de Adobe Commerce incluye varias tiendas o si planea agregar más tiendas posteriormente, puede incluir el código de la tienda en la dirección URL. Todos los recursos y operaciones de Adobe se pueden utilizar con el protocolo seguro.

Si no había un certificado de seguridad disponible para el dominio en el momento de la instalación, asegúrese de actualizar la configuración antes de iniciar el almacén. Una vez establecido un certificado de seguridad para su dominio, puede configurar una o ambas direcciones URL base para que funcionen con los protocolos Secure Sockets Layer (SSL) y [Transport Layer Security][1] (TLS) cifrados.

>[!IMPORTANT]
>
>Adobe recomienda encarecidamente transmitir todas las páginas de un sitio de producción, incluidas las páginas de contenido y producto, mediante un protocolo seguro.

Adobe Commerce y Magento Open Source se pueden configurar para que entreguen todas las páginas a lo largo de `HTTPS` de manera predeterminada. Si su tienda se ha estado ejecutando con el protocolo estándar, puede mejorar la seguridad habilitando [HTTP Strict Transport Security][2] (HSTS) y actualizando cualquier solicitud de página no segura. HSTS es un protocolo de inclusión que evita que los exploradores procesen páginas estándar `HTTP` que se transmiten con un protocolo no seguro para el dominio especificado. Debido a que es posible que los motores de búsqueda ya hayan indexado cada página de su tienda con las URL estándar de `HTTP`, puede configurar Commerce para que actualice automáticamente cualquier solicitud de página no segura a `HTTPS`, de modo que no pierda ningún tráfico. Cuando Commerce está configurado para usar direcciones URL seguras tanto para la tienda como para el administrador, aparecen dos campos adicionales que le permiten habilitar `HSTS`.

## Configuración de la dirección URL base

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En _General_ en el panel izquierdo, elija **[!UICONTROL Web]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Base URL]**.

   - **[!UICONTROL Base URL]**: escriba la dirección URL base completa para su tienda. Asegúrese de finalizar la dirección URL con una barra diagonal para que se pueda ampliar con claves de URL adicionales de la tienda. Por ejemplo: `http://yourdomain.com/`

     >[!NOTE]
     >
     >No cambie el marcador en el campo _[!UICONTROL Base Link URL]_. Es un marcador de posición que se utiliza para crear vínculos relativos a la dirección URL base.

   - **[!UICONTROL Base URL for Static View Files]** — (Opcional) Especifique una ubicación alternativa para la dirección URL base de los archivos de vista estática especificando la ruta de acceso que comience por el siguiente marcador de posición:

     \{unsecure_base_url}}

   - **[!UICONTROL Base URL for User Media Files]** — (Opcional) Especifique una ubicación alternativa para la dirección URL base de los archivos multimedia del usuario introduciendo la ruta de acceso que comienza por el siguiente marcador de posición:

     \{unsecure_base_url}}

     En una instalación típica, no es necesario actualizar las rutas de los archivos de vista estática o archivos multimedia porque son relativas a la dirección URL base.

   ![Configuración general - URL de base web](../configuration-reference/general/assets/web-base-urls.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Los marcadores de posición entre llaves dobles son etiquetas de marcado para variables.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Configuración de la URL base segura

Si su dominio tiene un certificado de seguridad válido, puede configurar las direcciones URL de la tienda y del administrador para transmitir datos a través de un canal seguro (https). Sin un certificado de seguridad válido, el almacén no puede funcionar con el protocolo seguro (SSL/TLS).

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección _[!UICONTROL Base URLs (Secure])_ y haga lo siguiente:

   ![Configuración general: direcciones URL base seguras](../configuration-reference/general/assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - **[!UICONTROL Secure Base URL]**: escriba la dirección URL base segura completa, seguida de una barra diagonal. Por ejemplo: `https://yourdomain.com/`

   - **[!UICONTROL Secure Base Link URL]**: no cambie el marcador de posición en el campo URL de vínculo base seguro. Se utiliza para crear vínculos relativos a la dirección URL base segura.

   - **[!UICONTROL Secure Base URL for Static View Files]**: (Opcional) especifique una ubicación alternativa para la dirección URL base segura para los archivos de vista estática introduciendo la ruta de acceso que comience por el siguiente marcador de posición:

     \{secure_base_url}}

   - **[!UICONTROL Secure Base URL for User Media Files]** — (Opcional) Especifique una ubicación alternativa para la dirección URL base segura para los archivos multimedia del usuario introduciendo la ruta de acceso que comience por el siguiente marcador de posición:

     \{secure_base_url}}

1. Para mejorar la seguridad, establezca las dos opciones siguientes en `Yes`.

   - **[!UICONTROL Use Secure URLs on Storefront]**
   - **[!UICONTROL Use Secure URLs in Admin]**

1. Para _[!UICONTROL Enhanced Security Settings]_, haga lo siguiente:

   - **[!UICONTROL Enable HTTP Strict Transport Security (HSTS)]**: si desea que su tienda muestre solo solicitudes de página HTTPS seguras, establezca en `Yes`.

   - **[!UICONTROL Upgrade Insecure Requests]**: para actualizar cualquier solicitud de páginas HTTP estándar no seguras a HTTPS seguro, establezca `Yes`.

1. Establezca **[!UICONTROL Offloader Header]** para su servidor.

   La mayoría de las instalaciones de Commerce usan el valor predeterminado `X-Forward-Proto` para identificar el protocolo como `HTTP` o `HTTPS`. Si la configuración del servidor utiliza un offloader_header diferente, ingréselo aquí.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Incluir el código de tienda en las direcciones URL

>[!NOTE]
>
>Cuando la opción _Agregar código de tienda a las direcciones URL_ esté establecida en `Yes`, debe incluir códigos de tienda en las direcciones URL del explorador. Esta configuración garantiza que las reescrituras de URL se asignen correctamente y que todas las páginas se abran correctamente, sin _&quot;404 Página no encontrada&quot;_ errores.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En _[!UICONTROL General]_, en el panel izquierdo, elija **[!UICONTROL Web]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL URL Options]**.

1. Establezca **[!UICONTROL Add Store Code]** según sus preferencias:

   - **[!UICONTROL URL with Store Code]**: `http://www.yourdomain.com/magento/[store-code]/index.php/url-identifier`
   - **[!UICONTROL URL without Store Code]**: `http://www.yourdomain.com/magento/index.php/url-identifier`

   ![Configuración general: opciones de URL web](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

1. Haga clic en el vínculo **[!UICONTROL Cache Management]** del mensaje en la parte superior del área de trabajo. A continuación, siga las instrucciones para actualizar la caché.

   ![Mensaje de administración de caché](./assets/msg-cache-management.png)

## Solución de problemas de URL

Si después de seguir las instrucciones de configuración, algunas páginas se siguen usando con la dirección URL no segura (`http://`), haga lo siguiente:

- Cambie la dirección URL base (no segura) a la dirección URL HTTPS segura.
- En el servidor, edite el archivo `.htaccess` (o equilibrador de carga) de modo que la dirección URL no segura se redirija a la dirección URL segura.

## Usar una URL de administrador personalizada

Como [práctica recomendada de seguridad](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html), Adobe recomienda usar una URL de administrador única en lugar de la _administración_ predeterminada o un término común como _backend_. Aunque no protege directamente el sitio de un actor incorrecto determinado, puede reducir la exposición a scripts que intentan obtener acceso no autorizado.

>[!NOTE]
>
>Consulte con su proveedor de alojamiento antes de implementar una URL de administrador personalizada. Algunos proveedores de alojamiento requieren una dirección URL estándar para cumplir las reglas de protección del cortafuegos.

En una instalación típica, la dirección URL de administración y la ruta siguen inmediatamente a la dirección URL base. La ruta del administrador es un directorio por debajo de la raíz.

- **Dirección URL base predeterminada**: `http://yourdomain.com/magento/`
- **Ruta de administración predeterminada**: `admin`
- **Dirección URL y ruta de acceso predeterminadas del administrador**: `http://yourdomain.com/magento/admin`

Aunque es posible cambiar la URL y la ruta de administración a otra ubicación, cualquier error elimina el acceso al administrador y debe corregirse desde el servidor.

>[!NOTE]
>
>Como precaución, no intente cambiar la URL de administración a menos que sepa cómo editar los archivos de configuración en el servidor. Para los proyectos de Adobe Commerce implementados en la infraestructura en la nube, cambie la URL de administración siguiendo las [instrucciones](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html?lang=en#admin-url) de la *Guía de Adobe Commerce en la infraestructura en la nube*.

### Método 1: cambio desde el administrador

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL Admin]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Admin Base URL]**.

1. Defina las opciones de configuración para la URL personalizada:

   ![Configuración avanzada: URL de base de administración](../configuration-reference/advanced/assets/admin-admin-base-url.png){width="600" zoomable="yes"}

   Si es necesario, desactive la casilla de verificación **[!UICONTROL Use system value]** para cambiar la configuración.

   - Establezca **[!UICONTROL Use Custom Admin URL]** en `Yes`.

   - Escriba **[!UICONTROL Custom Admin URL]**: `http://yourdomain.com/magento/`

     >[!NOTE]
     >
     >La URL de administrador debe estar en la misma instalación de Commerce y tener la misma raíz de documento que la tienda.

   - Establezca **[!UICONTROL Custom Admin Path]** en `Yes`.

   - Para **[!UICONTROL Custom Admin Path]**, escriba la ruta de acceso que se usará como nombre de la carpeta de administración personalizada.

     Ejemplo: `sample_custom_admin`

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

1. Una vez guardados los cambios, cierre la sesión de Admin y vuelva a iniciarla con la nueva dirección URL y ruta de Admin.

### Método 2: cambiar la ruta de administración desde la línea de comandos del servidor

1. Abra el archivo `app/etc/env.php` en un editor de texto y cambie el valor del parámetro `frontName` de la sección `backend`. A continuación, guarde el archivo.

   Asegúrese de utilizar solo caracteres en minúsculas.

   >[!NOTE]
   >
   >   Este método permite cambiar la ruta de administración, pero no la dirección URL de administración.

   >[!TIP]
   >
   >Para Adobe Commerce en la infraestructura en la nube, puede configurar una ruta de administración personalizada mediante la variable `ADMIN_URL` en la interfaz de usuario de la nube. Consulte el tema [Variables de administración](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html) en la _Guía de infraestructura de Commerce en la nube_.

   - **Ruta de administración predeterminada**

     ```php?start_inline=1
     'backend' => [
      'frontName' => 'admin'
     ],
     ```

   - **Nueva ruta de administración**

     ```php?start_inline=1
     'backend' => [
         'frontName' => 'backend'
     ],
     ```

1. Utilice uno de los siguientes métodos para borrar la caché:

   - En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**. A continuación, haga clic en **[!UICONTROL Flush Magento Cache]**.
   - En el servidor, ejecute lo siguiente:

     ```bash
     php bin/magento cache:flush
     ```

   >[!NOTE]
   >
   >Los cambios realizados con el Método 1 tienen prioridad sobre los cambios realizados en el archivo `app/etc/env.php`.

### Método 3: Cambio de la ruta del administrador mediante la CLI de Commerce

Puede utilizar el comando CLI `setup:config:set` para cambiar la ruta de administración. El ejemplo siguiente utiliza la opción `--backend-frontname` para cambiar la ruta de acceso de la raíz de Commerce a una nueva ruta de acceso de administrador:

```bash
bin/magento setup:config:set --backend-frontname="backend_front_name"
```

Este comando actualiza la opción de configuración `backend` > `frontName` en el archivo `app/etc/env.php`.

## Restaure la URL de administración y la ruta de administración predeterminadas

Si ha establecido una URL de administración no válida o una Ruta de administración y ha perdido el acceso al servidor, existe una forma de solucionarlo desde la línea de comandos.

1. Para volver a la URL de administración predeterminada, ejecute este comando:

   ```bash
   php bin/magento config:set admin/url/use_custom 0
   ```

1. Para volver a la ruta de acceso de administración predeterminada (establecida en `app/etc/env.php` como se describe en el Método 2), ejecute este comando:

   ```bash
   php bin/magento config:set admin/url/use_custom_path 0
   ```

1. Utilice uno de los siguientes métodos para borrar la caché:

   - En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**. A continuación, haga clic en **[!UICONTROL Flush Magento Cache]**.
   - En el servidor, ejecute lo siguiente:

     ```bash
     php bin/magento cache:flush
     ```


[1]: https://en.wikipedia.org/wiki/Transport_Layer_Security
[2]: https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
