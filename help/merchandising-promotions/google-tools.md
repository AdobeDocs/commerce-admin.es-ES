---
title: Herramientas del sitio de Google
description: Obtenga información sobre las integraciones de herramientas de Google que puede utilizar para optimizar el contenido, analizar el tráfico y conectar el catálogo a los agregadores de compras y mercados.
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Herramientas del sitio de Google

La configuración de su tienda está integrada con las siguientes herramientas de Google para ayudarle a optimizar su contenido, analizar el tráfico y conectar su catálogo a los agregadores de compras y a los mercados.

- [Google Analytics](google-analytics.md): usa _Google Universal Analytics_ para definir métricas y dimensiones personalizadas adicionales para el seguimiento, con compatibilidad para interacciones de aplicaciones móviles y sin conexión, y acceso a actualizaciones en curso.

- [Experimentos de contenido de Google](google-content-experiments.md): configure una prueba A/B para productos, categorías o páginas de contenido mediante Experimentos de contenido para Google Analytics.

- [Administrador de etiquetas de Google](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Use el Administrador de etiquetas de Google para administrar las muchas etiquetas relacionadas con los eventos de campañas de marketing.

- [Google AdWords](google-adwords.md): crea una campaña de Google AdWords y realiza un seguimiento de las conversiones de tu tienda.

{{gtag-api-note}}

## Configuración de privacidad de Google

Si su empresa debe cumplir con las regulaciones de privacidad como el [RGPD](../getting-started/compliance-gdpr.md) o la [CCPA](../getting-started/compliance-ccpa.md), cambie la configuración predeterminada de las herramientas de Google para cumplir con los requisitos de privacidad. Siga estos pasos para asegurarse de que el uso de los datos del cliente sigue siendo compatible.

### Paso 1: Actualizar la configuración de Google

1. [Inicia sesión][1]{: target=&quot;_blank&quot;} en la cuenta de Google Analytics de tu empresa.

1. En la parte inferior de la barra lateral izquierda, elija **[!UICONTROL Admin]** y luego vaya a la cuenta que desee editar (si corresponde).

1. En la columna **[!UICONTROL Account]**, haga clic en **[!UICONTROL Account Settings]**.

1. Desactive el uso compartido de datos para cumplir con los requisitos de la normativa de privacidad.

   La configuración predeterminada de Google Analytics comparte los datos de su empresa con Google y otras partes. Para desactivar el uso compartido de datos, desactive la casilla de verificación de selección de la siguiente configuración:

   - Productos y servicios de Google
   - Referencia
   - Asistencia técnica
   - Especialistas en cuentas

1. Acepte la _enmienda de procesamiento de datos_.

   Los Términos de procesamiento de datos de Google Ads describen cómo Google procesa los datos y las medidas que toma para garantizar la seguridad de los datos empresariales sujetos al RGPD. Con la modificación también se mantiene un registro de sus entidades legales e información de contacto. Para [obtener más información][2]{: target=&quot;_blank&quot;}, haga clic en el vínculo del mensaje en la parte superior de la página.

   - Desplácese hacia abajo de la página hasta **[!UICONTROL Data Processing Amendment]**.
   - Haga clic en **[!UICONTROL Review Amendment]** para leer los _Términos de procesamiento de datos de Google Ads_.
   - Haga clic en **[!UICONTROL Accept]**.
   - Haga clic en **[!UICONTROL Save]**.

1. Complete los detalles de la _administración de DPA_.

   - Haga clic en **[!UICONTROL Manage DPA Details]** para abrir una página de administración de DPA en la que podrá editar contactos y las entidades legales de su organización.

   - En la sección **[!UICONTROL Legal Entities]**, haga clic en el icono _Editar_ ( ![icono de edición de Google](./assets/google-icon-edit.png) ) y agregue uno o más nombres registrados para su organización. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

   - En la sección **Contactos**, haga clic en el icono _Agregar_ ( ![icono Agregar Google](./assets/google-icon-add.png) ) e introduzca la información del primer contacto. A continuación, active la casilla de verificación de cada rol aplicable y haga clic en **[!UICONTROL Add]**.

      - Contacto principal (dirección de correo electrónico de notificación): contacto al que se envían los avisos.
      - Responsable de protección de datos (si procede): la persona designada para facilitar el cumplimiento de la normativa de privacidad.
      - Representante del Espacio Económico Europeo (EEE): (si procede) la persona que representa a clientes fuera de la UE en relación con sus obligaciones en virtud del RGPD.

     Repita el proceso para agregar otro contacto, si corresponde.

### Paso 2: Modificar las bibliotecas JS de Google

Google admite tres bibliotecas JavaScript para medir el uso del sitio web, según el producto Google: `gtag.js`, `analytics.js` y `ga.js`. Para cumplir con los requisitos de privacidad, el código estándar se puede modificar de la siguiente manera:

#### Anonimizar direcciones IP

Para convertir en anónimas las direcciones IP que usa **_Google Universal Analytics_**, agregue el siguiente fragmento a la biblioteca `analytics.js` de su servidor web:

analytics.js

```
: `ga('set', 'anonymizeIp', true);`
```

Para obtener más información, consulte la [Referencia de campo de Analytics.js][3]{: target=&quot;_blank&quot;} en la Ayuda de Google.

Si usa la biblioteca `ga.js` heredada, agregue el siguiente fragmento de código:

ga.js

```
: `ga('set', 'anonymizeIp', true);`
```

Para convertir en anónimas las direcciones IP que usa **_Google Tag Manager_**, establezca el parámetro `anonymize_ip` en `true` en la biblioteca `gtag.js` de su servidor web.

gtag.js

```
: `gtag('event', 'your_event', { 'anonymize_ip': true })`
```

Para obtener más información, consulte [Anonimización de IP en Analytics][4] en la Ayuda de Google.

#### Forzar SSL

Para forzar la transmisión de todos los datos de Google a través de una capa de socket seguro (SSL), agregue el siguiente fragmento a la biblioteca `analytics.js` de su servidor web.

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### Paso 3: Actualizar la política de privacidad

Actualice su [política de privacidad](../getting-started/privacy-policy.md) para indicar que su compañía:

- Utiliza Google Analytics
- Enmascara direcciones IP para ocultar información personal
- Ha desactivado el uso compartido de datos de Google
- No utiliza otros servicios de Google con cookies de Google Analytics

[1]: https://www.google.com/analytics/
[2]: https://support.google.com/analytics/answer/3379636
[3]: https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference
[4]: https://support.google.com/analytics/answer/2763052
