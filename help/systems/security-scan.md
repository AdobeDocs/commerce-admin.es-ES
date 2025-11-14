---
title: Análisis de seguridad
description: Obtenga información sobre cómo ejecutar un análisis de seguridad mejorado y supervisar cada uno de los sitios de Adobe Commerce y Magento Open Source.
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 425004ece49f96fa102e9f46b9c5d15c89233334
workflow-type: tm+mt
source-wordcount: '1185'
ht-degree: 0%

---

# Análisis de seguridad

Supervise los sitios de Adobe Commerce y Magento Open Source en busca de riesgos de seguridad y malware, y reciba actualizaciones y notificaciones de seguridad.

- Obtenga insight en el estado de seguridad en tiempo real de su tienda.
- Reciba sugerencias basadas en las prácticas recomendadas para ayudarle a resolver problemas.
- Programe un análisis de seguridad para que se ejecute semanalmente, diariamente o bajo demanda.
- Ejecute más de 21.000 pruebas de seguridad para identificar malware potencial.
- Acceda a informes de seguridad históricos que rastrean y supervisan el progreso de sus sitios.
- Acceda al informe de análisis que muestra las comprobaciones correctas y fallidas, con las acciones recomendadas.

La herramienta Security Scan Tool está disponible de forma gratuita en el tablero de su [cuenta de Commerce/Magento](../getting-started/commerce-account-create.md). Para obtener información técnica, consulte [Configuración de Security Scan Tool](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/launch/overview#set-up-the-security-scan-tool) en la _Guía de Commerce en la infraestructura de la nube_.

![Herramienta de exploración de seguridad](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## Flujo de trabajo

Para configurar la Herramienta de análisis de seguridad para su sitio de Adobe Commerce o Magento Open Source, siga dos pasos:

1. [Configurar el sitio para el análisis de seguridad](#step-1-set-up-your-site-for-security-scanning)
2. [Configurar análisis de seguridad automáticos](#step-2-configure-automatic-security-scans)

### Paso 1: Configurar el sitio para el análisis de seguridad

1. En la página de inicio de Commerce, inicia sesión en tu [cuenta de Commerce/Magento](../getting-started/commerce-account-create.md).

2. Revise y acepte las condiciones de uso de la Herramienta de exploración de seguridad.

   1. En el panel izquierdo, elija **[!UICONTROL Security Scan]**.
   1. Haga clic en **[!UICONTROL Go to Security Scan]**.
   1. Lea **[!UICONTROL Terms and Conditions]**.
   1. Haga clic en **[!UICONTROL Agree]** para continuar.

3. En la página _[!UICONTROL Monitored Websites]_, haga clic en **[!UICONTROL +Add Site]**.

   Si tiene varios sitios con dominios diferentes, configure un análisis independiente para cada dominio.

   ![Sitios supervisados](./assets/monitored-website.png){width="600" zoomable="yes"}

4. Compruebe que es propietario del dominio del sitio generando y agregando un código de confirmación a la herramienta de análisis de seguridad.

   El proceso para agregar el código de confirmación varía según el tipo de tienda que uses. Sigue los pasos para el tipo de tienda.

>[!BEGINTABS]

>[!TAB tienda de Commerce]

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

1. Vuelva a la página _[!UICONTROL Security Scan]_de su cuenta de Commerce y haga clic en **[!UICONTROL Verify Confirmation Code]**para establecer la propiedad del dominio.

>[!TAB tienda de PWA]

1. Escriba **[!UICONTROL Site URL]** y **[!UICONTROL Site Name]**.

1. Para **[!UICONTROL Confirmation Code]**, elija la opción `META Tag` y haga clic en **[!UICONTROL Generate Code]**.

1. Haga clic en **[!UICONTROL Copy]** para copiar el código de confirmación generado META Tag en el portapapeles.

   ![Generar código de confirmación](./assets/scan-site2.png){width="400" zoomable="yes"}

1. Vaya al directorio del proyecto de la tienda PWA Studio y haga lo siguiente:

   1. En el directorio del proyecto de PWA Studio, vaya a `packages > venia-concept > template.html`.
   1. Agregue el código de confirmación copiado (la etiqueta de META generada) al encabezado de HTML y guarde los cambios.

      ![Copiar código de confirmación](./assets/code-pwa.png){width="600" zoomable="yes"}

   1. Vuelva a la CLI de PWA Studio y utilice un hilo para instalar las dependencias del proyecto y ejecutar el comando de generación del proyecto.

      ```sh
      yarn install &&
      yarn build
      ```

   1. *Cree una carpeta* en su proyecto de Cloud`pwa` y copie el contenido en la carpeta `dist` de su proyecto de tienda.

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

1. Vuelva a la página _[!UICONTROL Security Scan]_de su cuenta de Commerce y haga clic en **[!UICONTROL Verify Confirmation Code]**para establecer la propiedad del dominio.

>[!TAB Tienda AEM]

1. Escriba **[!UICONTROL Site URL]** y **[!UICONTROL Site Name]**.

1. Para **[!UICONTROL Confirmation Code]**, elija la opción `HTML Content` o `META Tag` y haga clic en **[!UICONTROL Generate Code]**.

1. Haga clic en **[!UICONTROL Copy]** para copiar el código de confirmación generado en el portapapeles.

   ![Generar código de confirmación](./assets/scan-site3.png){width="400" zoomable="yes"}

1. Vaya al directorio del proyecto de la tienda AEM y haga lo siguiente:

   1. En el directorio del proyecto de la tienda AEM, vaya a `head.html`.
   1. Agregue el código de confirmación copiado (el contenido de HTML generado o la etiqueta de META) al archivo `head.html` y guarde los cambios.

   >[!NOTE]
   >
   >La comprobación de la propiedad del sitio solo funciona si la confirmación se agrega directamente al archivo `head.html` en el directorio del proyecto de tienda de AEM. No se puede agregar a través de herramientas de edición de páginas web como la creación de documentos o el editor universal.

   ![Copiar código de confirmación](./assets/code-aem.png){width="600" zoomable="yes"}

1. Utilice la herramienta CLI de Git para almacenar en zona intermedia, confirmar e insertar estos cambios en el repositorio del proyecto.

   ```sh
   git add . &&
   git commit -m "Added security scan confirmation code" &&
   git push origin
   ```

   Una vez completado el proceso de compilación, los cambios se implementarán en la tienda de AEM.

1. Vuelva a la página _[!UICONTROL Security Scan]_de su cuenta de Commerce y haga clic en **[!UICONTROL Verify Confirmation Code]**para establecer la propiedad del dominio.

>[!ENDTABS]

### Paso 2: Configurar análisis de seguridad automáticos

1. Después de comprobar correctamente la propiedad del sitio, configure las opciones **[!UICONTROL Set Automatic Security Scan]** para uno de los siguientes tipos:

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

1. En la página _[!UICONTROL Monitored Websites]_, haga clic en **[!UICONTROL View Report]**para el sitio que desee administrar.

1. En la vista de informe, busque el análisis fallido que desee marcar como falso positivo.

1. Haga clic en **[!UICONTROL Ignore]** para ver el error de análisis específico.

   ![Ignorar errores de análisis](assets/security-scan-ignore-failure.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Apply Changes]** para guardar la selección.

El error de análisis omitido se mueve a la sección _[!UICONTROL Ignored Results]_y se excluye de la puntuación de riesgo.

### Dejar de omitir errores de análisis

Si necesita restaurar un fallo de análisis previamente ignorado a su monitorización activa, siga estos pasos:

1. En la vista de informe, desplácese hasta la sección _[!UICONTROL Ignored Results]_.

1. Haga clic en **[!UICONTROL Stop Ignoring]** para el error de análisis que desea restaurar.

   ![Errores de análisis no detectados](assets/security-scan-stop-ignoring-failure.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Apply Changes]** para guardar la selección.

El error de análisis vuelve a la sección _[!UICONTROL Failed Scans]_y se incluye en la puntuación de riesgo.

### Ver errores de análisis omitidos

Los resultados omitidos aparecen en una sección independiente del informe y la puntuación de riesgo se actualiza automáticamente para reflejar únicamente los errores de análisis activos. Puede administrar varios errores de análisis a la vez seleccionando varios elementos antes de aplicar los cambios.

![Errores de análisis omitidos en la vista](assets/security-scan-view-ignored-failures.png){width="600" zoomable="yes"}
