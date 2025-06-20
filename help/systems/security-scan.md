---
title: Análisis de seguridad
description: Obtenga información sobre cómo ejecutar un análisis de seguridad mejorado y supervisar cada uno de los sitios de Adobe Commerce y Magento Open Source.
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: eb226a969397bbfa31f72a4ae4fb61b22a0101bc
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 0%

---


# Análisis de seguridad

La Herramienta de análisis de seguridad de Adobe Commerce proporciona supervisión de seguridad gratuita para los sitios de Adobe Commerce y Magento Open Source. La herramienta funciona como un servicio basado en la web al que puedes acceder a través de tu cuenta en línea de Adobe Commerce en [account.magento.com](https://account.magento.com/customer/account/login).

![Herramienta de exploración de seguridad](./assets/magento-security-scan.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Adobe proporciona este servicio sin coste alguno, aunque los comerciantes deben aceptar términos que limiten la responsabilidad de Adobe en función de los resultados del análisis y la configuración del sitio.

## Cobertura del análisis

La Herramienta de análisis de seguridad funciona a través de protocolos HTTP y HTTPS para detectar malware, identificar vulnerabilidades de seguridad y ayudarle a mantener la postura de seguridad de su tienda. La herramienta está disponible para todos los comerciantes, desarrolladores y personal designado responsable de la seguridad del sitio.

La herramienta de análisis de seguridad proporciona funciones completas de supervisión de la seguridad que le ayudan a mantener un entorno de almacenamiento seguro:

- Obtenga insight en el estado de seguridad en tiempo real de su tienda.
- Reciba sugerencias basadas en las prácticas recomendadas para ayudarle a resolver problemas.
- Programe un análisis de seguridad para que se ejecute semanalmente, diariamente o bajo demanda.
- Ejecute más de 21.000 pruebas de seguridad para identificar malware potencial.
- Acceda a informes de seguridad históricos que rastrean y supervisan el progreso de sus sitios.
- Acceda al informe de análisis que muestra las comprobaciones correctas y fallidas, con las acciones recomendadas.

>[!NOTE]
>
>No puede excluir pruebas de seguridad específicas de los análisis de la Herramienta de análisis de seguridad para Adobe Commerce. Sin embargo, puede autoabastecerse en [ignorando errores](#manage-scan-failures) como falsos positivos si corresponde.

## Acceso

La herramienta de análisis de seguridad mantiene estrictos controles de acceso para proteger la información del sitio. Solo usted puede analizar su sitio porque la herramienta requiere la verificación de la propiedad del dominio a través de su cuenta de Adobe Commerce. Cada sitio se conecta a su cuenta a través de un token único, lo que evita el análisis no autorizado por parte de terceros.

La herramienta se centra específicamente en los dominios de Adobe Commerce y sus vulnerabilidades de seguridad. Aunque su tienda web puede incluir páginas de otras plataformas, la herramienta de análisis de seguridad solo debe analizar el contenido generado por Adobe Commerce para garantizar resultados fiables. El análisis de páginas que no son de Adobe Commerce puede producir evaluaciones de vulnerabilidad poco fiables.

>[!NOTE]
>
>La herramienta de análisis de seguridad utiliza las siguientes direcciones IP públicas:
>
>```text
>52.87.98.44
>34.196.167.176
>3.218.25.102
>```
>
>Añada estas direcciones IP a una lista de permitidos de las reglas del cortafuegos de la red para permitir que la herramienta analice el sitio. La herramienta solo publica solicitudes en los puertos `80` y `443`.

## Ejecutar un análisis

El proceso de digitalización comprueba el sitio en busca de problemas de seguridad conocidos e identifica las revisiones y actualizaciones de Adobe Commerce que faltan y que podrían dejar el almacén vulnerable a ataques.

>[!TIP]
>
>Para Commerce sobre proyectos de infraestructura en la nube, consulte [Configuración de la herramienta de exploración de seguridad](https://experienceleague.adobe.com/es/docs/commerce-on-cloud/user-guide/launch/overview#set-up-the-security-scan-tool).

Para ejecutar un análisis:

1. En la página de inicio de Commerce, inicia sesión en tu [cuenta de Commerce/Magento](../getting-started/commerce-account-create.md).

1. Revise y acepte las condiciones de uso de la Herramienta de exploración de seguridad.

   1. En el panel izquierdo, elija **[!UICONTROL Security Scan]**.
   1. Haga clic en **[!UICONTROL Go to Security Scan]**.
   1. Lea **[!UICONTROL Terms and Conditions]**.
   1. Haga clic en **[!UICONTROL Agree]** para continuar.

1. En la página _[!UICONTROL Monitored Websites]_, haga clic en **[!UICONTROL +Add Site]**.

   Si tiene varios sitios con dominios diferentes, configure un análisis independiente para cada dominio.

   ![Sitios supervisados](./assets/monitored-website.png){width="600" zoomable="yes"}

1. Para comprobar la propiedad del dominio del sitio agregando un código de confirmación, siga uno de estos procedimientos:

   **tienda Commerce**:

   1. Escriba **[!UICONTROL Site URL]** y **[!UICONTROL Site Name]**.
   1. Haga clic en **[!UICONTROL Generate Confirmation Code]**.
   1. Haga clic en **Copiar** para copiar el código de confirmación en el portapapeles.

      ![Generar código de confirmación](./assets/scan-site1.png){width="400" zoomable="yes"}

   1. Inicie sesión en el administrador de su tienda como usuario con privilegios de administrador completos y haga lo siguiente:

      1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.
      1. Busque el sitio en la lista y haga clic en **[!UICONTROL Edit]**.
      1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL HTML Head]**.
      1. Desplácese hacia abajo hasta **[!UICONTROL Scripts and Style Sheets]** y haga clic en el cuadro de texto al final de cualquier código existente. Pegue el código de confirmación en el cuadro de texto.

         ![Scripts y hojas de estilo](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      1. Una vez finalizado, haga clic en **[!UICONTROL Save Configuration]**.

   **tienda PWA**:

   1. Escriba **[!UICONTROL Site URL]** y **[!UICONTROL Site Name]**.

   1. Para **[!UICONTROL Confirmation Code]**, elija la opción `META Tag` y haga clic en **[!UICONTROL Generate Code]**.

   1. Haga clic en **[!UICONTROL Copy]** para copiar el código de confirmación generado META Tag en el portapapeles.

      ![Generar código de confirmación](./assets/scan-site2.png){width="400" zoomable="yes"}

   1. Vaya al directorio del proyecto de la tienda PWA Studio y haga lo siguiente:

      1. En el directorio del proyecto de PWA Studio, vaya a `packages > venia-concept > template.html`.
      1. Agregue el código de confirmación copiado (la etiqueta meta generada) al encabezado de HTML y guarde los cambios.

         ![Copiar código de confirmación](./assets/code-pwa.png){width="600" zoomable="yes"}

      1. Vuelva a la CLI de PWA Studio y utilice un hilo para instalar las dependencias del proyecto y ejecutar el comando de generación del proyecto.

         ```sh
         yarn install &&
         yarn build
         ```

      1. *Cree una carpeta `pwa` en su proyecto de Cloud* y copie el contenido en la carpeta `dist` de su proyecto de tienda.

         ```sh
         mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
         ```

      1. Utilice la herramienta CLI de Git para almacenar en zona intermedia, confirmar e insertar estos cambios en su proyecto de Cloud.

         ```sh
         git add . &&
         git commit -m "Added storefront file bundles" &&
         git push origin
         ```

         Una vez completado el proceso de compilación, los cambios se implementarán en la tienda de PWA.

1. Vuelva a la página _[!UICONTROL Security Scan]_&#x200B;de su cuenta de Commerce y haga clic en **[!UICONTROL Verify Confirmation Code]**&#x200B;para establecer la propiedad del dominio.

1. Después de una confirmación correcta, configure las opciones **[!UICONTROL Set Automatic Security Scan]** para uno de los siguientes tipos:

   **Análisis semanal (recomendado)**:

   Elija **[!UICONTROL Week Day]**, **[!UICONTROL Time]** y **[!UICONTROL Time Zone]** en los que se realizará el análisis cada semana.

   De forma predeterminada, el análisis está programado para comenzar cada semana a medianoche del sábado (UTC) y continuar hasta el domingo a primera hora.

   ![Análisis semanal](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **Examen diario**:

   Elija **[!UICONTROL Time]** y **[!UICONTROL Time Zone]** en los que se realizará el análisis cada día.

   De forma predeterminada, el análisis está programado para comenzar cada día a medianoche (UTC).

   ![Examen diario](./assets/scan-daily.png){width="500" zoomable="yes"}

1. Escriba el **[!UICONTROL Email Address]** en el que desea recibir las notificaciones de análisis completados y actualizaciones de seguridad.

   ![Dirección de correo electrónico](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Submit]**.

   Una vez verificada la propiedad del dominio, el sitio aparece en la lista Sitios web supervisados de su cuenta de Commerce.

1. Si tiene varios sitios web con dominios diferentes, repita este proceso para configurar un análisis de seguridad para cada uno.

## Administrar errores de análisis

La herramienta de análisis de seguridad le permite administrar los errores de análisis directamente desde la vista de informe. Puede marcar errores de análisis específicos como falsos positivos y excluirlos de la puntuación de riesgo.

### Ventajas de administrar los errores de análisis

La administración de los errores de análisis le ayuda a mantener una visión general de seguridad más precisa de su tienda mediante:

- Reducción de los falsos positivos en los informes de seguridad.
- Centrarse en las cuestiones de seguridad pertinentes que requieren atención.
- Mantener una visión más clara del verdadero estado de seguridad de tu tienda.
- Se elimina la necesidad de ponerse en contacto con el servicio de asistencia para falsos positivos conocidos.
- Ahorra tiempo gracias a la administración automática de los errores de análisis que ya ha investigado.

Entre los escenarios comunes en los que podría querer marcar un error de análisis como falso positivo se incluyen:

- Cuando ya haya aplicado un parche de seguridad que la herramienta de análisis no haya detectado.
- Cuando un problema detectado no es aplicable a su configuración de tienda específica.
- Cuando haya implementado una medida de seguridad alternativa que solucione el problema.
- Cuando el fallo de análisis se basa en una configuración que ha definido intencionadamente para sus necesidades empresariales.

### Omitir errores de análisis

Para gestionar los errores de análisis identificados como falsos positivos, siga estos pasos:

1. En la página _[!UICONTROL Monitored Websites]_, haga clic en **[!UICONTROL View Report]**&#x200B;para el sitio que desee administrar.

1. En la vista de informe, busque el análisis fallido que desee marcar como falso positivo.

1. Haga clic en **[!UICONTROL Ignore]** para ver el error de análisis específico.

   ![Ignorar errores de análisis](assets/security-scan-ignore-failure.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Apply Changes]** para guardar la selección.

El error de análisis omitido se mueve a la sección _[!UICONTROL Ignored Results]_&#x200B;y se excluye de la puntuación de riesgo.

### Dejar de omitir errores de análisis

Si necesita restaurar un fallo de análisis previamente ignorado a su monitorización activa, siga estos pasos:

1. En la vista de informe, desplácese hasta la sección _[!UICONTROL Ignored Results]_.

1. Haga clic en **[!UICONTROL Stop Ignoring]** para el error de análisis que desea restaurar.

   ![Errores de análisis no detectados](assets/security-scan-stop-ignoring-failure.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Apply Changes]** para guardar la selección.

El error de análisis vuelve a la sección _[!UICONTROL Failed Scans]_&#x200B;y se incluye en la puntuación de riesgo.

### Ver errores de análisis omitidos

Los resultados omitidos aparecen en una sección independiente del informe y la puntuación de riesgo se actualiza automáticamente para reflejar únicamente los errores de análisis activos. Puede administrar varios errores de análisis a la vez seleccionando varios elementos antes de aplicar los cambios.

![Errores de análisis omitidos en la vista](assets/security-scan-view-ignored-failures.png){width="600" zoomable="yes"}
