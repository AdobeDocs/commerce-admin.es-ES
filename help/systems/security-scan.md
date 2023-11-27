---
title: Análisis de seguridad
description: Obtenga información sobre cómo ejecutar un análisis de seguridad mejorado y monitorizar cada uno de los sitios de Adobe Commerce y de los Magento Open Source.
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# Análisis de seguridad

El análisis de seguridad mejorado le permite supervisar cada uno de sus sitios de Adobe Commerce y Magento Open Source, incluido PWA, para detectar riesgos de seguridad y malware conocidos, así como recibir actualizaciones de parches y notificaciones de seguridad.

- Obtenga información sobre el estado de seguridad en tiempo real de su tienda.
- Reciba sugerencias basadas en las prácticas recomendadas para ayudarle a resolver problemas.
- Programar análisis de seguridad para que se ejecute semanalmente, diariamente o bajo demanda.
- Ejecute más de 21.000 pruebas de seguridad para identificar malware potencial.
- Acceda a informes de seguridad históricos que rastrean y supervisan el progreso de sus sitios.
- Acceda al informe de análisis que muestra las comprobaciones correctas y fallidas, con las acciones recomendadas.

La herramienta de análisis de seguridad está disponible de forma gratuita en el panel de su [Cuenta de Commerce](../getting-started/commerce-account-create.md). Para obtener información técnica, consulte [Configurar el escáner de seguridad](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/launch/overview.html#set-up-the-security-scan-tool) en el _Guía de Commerce en la infraestructura de Cloud_.

![Herramienta de exploración de seguridad](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## Realizar un análisis de seguridad

1. Vaya a la página de inicio de Commerce e inicie sesión en su [Cuenta de Commerce](../getting-started/commerce-account-create.md) y haga lo siguiente:

   - En el panel izquierdo, elija **[!UICONTROL Security Scan]**.
   - Haga clic **[!UICONTROL Go to Security Scan]**.
   - Lea el **[!UICONTROL Terms and Conditions]**.
   - Clic **[!UICONTROL Agree]** para continuar.

1. En el _[!UICONTROL Monitored Websites]_página, haga clic en **[!UICONTROL +Add Site]**.

   Si tiene varios sitios con dominios diferentes, debe configurar un análisis independiente para cada dominio.

   ![Sitios supervisados](./assets/monitored-website.png){width="600" zoomable="yes"}

1. Para comprobar la propiedad del dominio del sitio agregando un código de confirmación, siga uno de estos procedimientos:

   **Tienda de Commerce**:

   - Introduzca el **[!UICONTROL Site URL]** y **[!UICONTROL Site Name]**.
   - Haga clic **[!UICONTROL Generate Confirmation Code]**.
   - Clic **Copiar** para copiar el código de confirmación en el portapapeles.

     ![Generar código de confirmación](./assets/scan-site1.png){width="400" zoomable="yes"}

   - Inicie sesión en el administrador de su tienda como usuario con privilegios de administrador completos y haga lo siguiente:

      - En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.
      - Busque el sitio en la lista y haga clic en **[!UICONTROL Edit]**.
      - Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL HTML Head]** sección.
      - Desplácese hacia abajo hasta **[!UICONTROL Scripts and Style Sheets]** y haga clic en el cuadro de texto al final de cualquier código existente y pegue el código de confirmación en el cuadro de texto.

        ![Scripts y hojas de estilo](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      - Cuando termine, haga clic en **[!UICONTROL Save Configuration]**.

   **tienda de PWA**:

   - Introduzca el **[!UICONTROL Site URL]** y **[!UICONTROL Site Name]**.

   - Para **[!UICONTROL Confirmation Code]**, elija la `META Tag` y luego haga clic en **[!UICONTROL Generate Code]**.

   - Clic **[!UICONTROL Copy]** para copiar el código de confirmación generado META Tag en el portapapeles.

     ![Generar código de confirmación](./assets/scan-site2.png){width="400" zoomable="yes"}

   - Vaya al directorio del proyecto de la tienda del PWA Studio y haga lo siguiente:

      - En el directorio del proyecto del PWA Studio, vaya a `packages > venia-concept > template.html`.
      - Agregue el código de confirmación copiado (la etiqueta meta generada) al encabezado del HTML y guarde los cambios.

        ![Copiar código de confirmación](./assets/code-pwa.png){width="600" zoomable="yes"}

      - Vuelva a la CLI de PWA Studio y utilice un hilo para instalar las dependencias del proyecto y ejecutar el comando de generación del proyecto.

        ```sh
        yarn install &&
        yarn build
        ```

      - *En su proyecto de Cloud*, cree un `pwa` y copie el contenido dentro del proyecto de tienda `dist` carpeta.

        ```sh
        mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
        ```

      - Utilice la herramienta CLI de Git para almacenar en zona intermedia, confirmar e insertar estos cambios en su proyecto de Cloud.

        ```sh
        git add . &&
        git commit -m "Added storefront file bundles" &&
        git push origin
        ```

        Una vez completado el proceso de compilación, los cambios se implementarán en la tienda del PWA.

1. Vuelva a la _[!UICONTROL Security Scan]_en su cuenta de Commerce y haga clic en **[!UICONTROL Verify Confirmation Code]**para establecer su propiedad del dominio.

1. Después de una confirmación correcta, configure el **[!UICONTROL Set Automatic Security Scan]** opciones para uno de los siguientes tipos:

   **Analizar semanalmente (recomendado)**:

   - Elija la **[!UICONTROL Week Day]**, **[!UICONTROL Time]**, y **[!UICONTROL Time Zone]** que la exploración se realizará cada semana.
   - De forma predeterminada, el análisis está programado para comenzar cada semana a medianoche del sábado (UTC) y continuar hasta el domingo a primera hora.

     ![Escanear semanalmente](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **Digitalizar diariamente**:

   - Elija la **[!UICONTROL Time]**, y **[!UICONTROL Time Zone]** que la exploración se realizará todos los días.
   - De forma predeterminada, el análisis está programado para comenzar cada día a medianoche (UTC).

     ![Digitalizar diariamente](./assets/scan-daily.png){width="500" zoomable="yes"}

1. Introduzca el **[!UICONTROL Email Address]** donde desee recibir notificaciones de análisis y actualizaciones de seguridad completados.

   ![Correo electrónico](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Submit]**.

   Una vez verificada la propiedad del dominio, el sitio aparece en la lista de sitios web supervisados de su cuenta de Commerce.

1. Si tiene varios sitios web con dominios diferentes, repita este proceso para configurar un análisis de seguridad para cada uno.
