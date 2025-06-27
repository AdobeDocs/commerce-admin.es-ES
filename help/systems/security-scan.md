---
title: Análisis de seguridad
description: Obtenga información sobre cómo ejecutar un análisis de seguridad mejorado y supervisar cada uno de los sitios de Adobe Commerce y Magento Open Source.
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 8e634311cd84a9e797a36218c29abb4699d72835
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# Análisis de seguridad

El análisis de seguridad mejorado le permite supervisar cada uno de sus sitios de Adobe Commerce y Magento Open Source, incluido PWA, para detectar riesgos de seguridad y malware conocidos, así como recibir actualizaciones de parches y notificaciones de seguridad.

- Obtenga insight en el estado de seguridad en tiempo real de su tienda.
- Reciba sugerencias basadas en las prácticas recomendadas para ayudarle a resolver problemas.
- Programar análisis de seguridad para que se ejecute semanalmente, diariamente o bajo demanda.
- Ejecute más de 21.000 pruebas de seguridad para identificar malware potencial.
- Acceda a informes de seguridad históricos que rastrean y supervisan el progreso de sus sitios.
- Acceda al informe de análisis que muestra las comprobaciones correctas y fallidas, con las acciones recomendadas.

La herramienta de análisis de seguridad está disponible de forma gratuita en el panel de tu [cuenta de Commerce/Magento](../getting-started/commerce-account-create.md). Para obtener información técnica, consulte [Configurar la herramienta de análisis de seguridad](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/launch/overview.html?lang=es#set-up-the-security-scan-tool) en la _Guía de infraestructura de Commerce en la nube_.

![Herramienta de exploración de seguridad](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## Realizar un análisis de seguridad

1. Inicia sesión en tu [cuenta de Commerce/Magento](../getting-started/commerce-account-create.md).

1. En el panel izquierdo, haga clic en la ficha [!UICONTROL Security Scan]. (Si es necesario, revise y acepte los términos actualizados de uso de la herramienta de exploración de seguridad.)

   - En el panel izquierdo, elija **[!UICONTROL Security Scan]**.
   - Haga clic en **[!UICONTROL Go to Security Scan]**.
   - Lea **[!UICONTROL Terms and Conditions]**.
   - Haga clic en **[!UICONTROL Agree]** para continuar.

1. En la página _[!UICONTROL Monitored Websites]_, haga clic en **[!UICONTROL +Add Site]**.

   Si tiene varios sitios con dominios diferentes, configure un análisis independiente para cada dominio.

   ![Sitios supervisados](./assets/monitored-website.png){width="600" zoomable="yes"}

1. Para comprobar la propiedad del dominio del sitio agregando un código de confirmación, siga uno de estos procedimientos:

   **tienda Commerce**:

   - Escriba **[!UICONTROL Site URL]** y **[!UICONTROL Site Name]**.
   - Haga clic en **[!UICONTROL Generate Confirmation Code]**.
   - Haga clic en **Copiar** para copiar el código de confirmación en el portapapeles.

     ![Generar código de confirmación](./assets/scan-site1.png){width="400" zoomable="yes"}

   - Inicie sesión en el administrador de su tienda como usuario con privilegios de administrador completos y haga lo siguiente:

      - En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.
      - Busque el sitio en la lista y haga clic en **[!UICONTROL Edit]**.
      - Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL HTML Head]**.
      - Desplácese hacia abajo hasta **[!UICONTROL Scripts and Style Sheets]**, haga clic en el cuadro de texto al final de cualquier código existente y pegue el código de confirmación en el cuadro de texto.

        ![Scripts y hojas de estilo](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      - Una vez finalizado, haga clic en **[!UICONTROL Save Configuration]**.

   **tienda PWA**:

   - Escriba **[!UICONTROL Site URL]** y **[!UICONTROL Site Name]**.

   - Para **[!UICONTROL Confirmation Code]**, elija la opción `META Tag` y haga clic en **[!UICONTROL Generate Code]**.

   - Haga clic en **[!UICONTROL Copy]** para copiar el código de confirmación generado META Tag en el portapapeles.

     ![Generar código de confirmación](./assets/scan-site2.png){width="400" zoomable="yes"}

   - Vaya al directorio del proyecto de la tienda PWA Studio y haga lo siguiente:

      - En el directorio del proyecto de PWA Studio, vaya a `packages > venia-concept > template.html`.
      - Agregue el código de confirmación copiado (la etiqueta meta generada) al encabezado de HTML y guarde los cambios.

        ![Copiar código de confirmación](./assets/code-pwa.png){width="600" zoomable="yes"}

      - Vuelva a la CLI de PWA Studio y utilice un hilo para instalar las dependencias del proyecto y ejecutar el comando de generación del proyecto.

        ```sh
        yarn install &&
        yarn build
        ```

      - *Cree una carpeta `pwa` en su proyecto de Cloud* y copie el contenido en la carpeta `dist` de su proyecto de tienda.

        ```sh
        mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
        ```

      - Utilice la herramienta CLI de Git para almacenar en zona intermedia, confirmar e insertar estos cambios en su proyecto de Cloud.

        ```sh
        git add . &&
        git commit -m "Added storefront file bundles" &&
        git push origin
        ```

        Una vez completado el proceso de compilación, los cambios se implementarán en la tienda de PWA.

1. Vuelva a la página _[!UICONTROL Security Scan]_&#x200B;de su cuenta de Commerce y haga clic en **[!UICONTROL Verify Confirmation Code]**&#x200B;para establecer la propiedad del dominio.

1. Después de una confirmación correcta, configure las opciones **[!UICONTROL Set Automatic Security Scan]** para uno de los siguientes tipos:

   **Análisis semanal (recomendado)**:

   - Elija **[!UICONTROL Week Day]**, **[!UICONTROL Time]** y **[!UICONTROL Time Zone]** en los que se realizará el análisis cada semana.
   - De forma predeterminada, el análisis está programado para comenzar cada semana a medianoche del sábado (UTC) y continuar hasta el domingo a primera hora.

     ![Análisis semanal](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **Examen diario**:

   - Elija **[!UICONTROL Time]** y **[!UICONTROL Time Zone]** en los que se realizará el análisis cada día.
   - De forma predeterminada, el análisis está programado para comenzar cada día a medianoche (UTC).

     ![Examen diario](./assets/scan-daily.png){width="500" zoomable="yes"}

1. Escriba el **[!UICONTROL Email Address]** en el que desea recibir las notificaciones de análisis completados y actualizaciones de seguridad.

   ![Dirección de correo electrónico](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Submit]**.

   Una vez verificada la propiedad del dominio, el sitio aparece en la lista Sitios web supervisados de su cuenta de Commerce.

1. Si tiene varios sitios web con dominios diferentes, repita este proceso para configurar un análisis de seguridad para cada uno.

## Eliminar un análisis de seguridad

>[!NOTE]
>
>Solo la persona que configuró originalmente el análisis puede eliminarlo de la cuenta. Si no han iniciado sesión en su [cuenta](https://account.magento.com) desde agosto de 2022, primero deben asegurarse de que se han [registrado en un Adobe ID](https://account.magento.com).

**Eliminar un análisis**

1. Inicie sesión en la [cuenta de Commerce/Magento](../getting-started/commerce-account-create.md).

1. En el panel izquierdo, haga clic en la ficha [!UICONTROL Security Scan]. (Si es necesario, revise y acepte los términos actualizados de uso de la herramienta de exploración de seguridad.)

   - Haga clic en **[!UICONTROL Go to Security Scan]**.
   - Lea **[!UICONTROL Terms and Conditions]**.
   - Haga clic en **[!UICONTROL Agree]** para continuar.

1. En la página _[!UICONTROL Monitored Websites]_, busque el menú desplegable en la columna [!UICONTROL Actions] y, a continuación, seleccione **[!UICONTROL Delete]**&#x200B;para los sitios web correspondientes.
