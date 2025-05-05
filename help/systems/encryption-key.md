---
title: Clave de cifrado
description: Aprenda a cambiar su propia clave de cifrado, lo que debe hacer regularmente para mejorar la seguridad.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# Clave de cifrado

>[!NOTE]
>
>Si ha intentado completar estos pasos y tiene problemas, consulte el artículo de la base de conocimiento [Resolución de problemas de rotación de clave de cifrado: CVE-2024-34102](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/troubleshooting-encryption-key-rotation-cve-2024-34102).

Adobe Commerce y Magento Open Source utilizan una clave de cifrado para proteger contraseñas y otros datos confidenciales. Se utiliza un algoritmo [!DNL ChaCha20-Poly1305] estándar del sector con una clave de 256 bits para cifrar todos los datos que requieren cifrado. Esto incluye datos de tarjetas de crédito y contraseñas de integración (módulo de pago y envío). Además, se utiliza un algoritmo hash seguro (SHA-256) para cifrar todos los datos que no requieren descifrado.

Durante la instalación inicial, se le pedirá que deje que Commerce genere una clave de cifrado o que introduzca una suya. La herramienta de clave de cifrado permite cambiar la clave según sea necesario. La clave de cifrado debe cambiarse regularmente para mejorar la seguridad y, en cualquier momento, la clave original puede verse comprometida.

Para obtener información técnica, consulte [Instalación local avanzada](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) en la _Guía de instalación_ y [Recifrado de datos](https://developer.adobe.com/commerce/php/development/security/data-encryption/) en la _Guía para desarrolladores de PHP_.

>[!IMPORTANT]
>
>- Antes de seguir estas instrucciones para cambiar la clave de cifrado, asegúrese de que el siguiente archivo se puede escribir: `[your store]/app/etc/env.php`
>- La función de cambio de clave de cifrado en la configuración de Administración está obsoleta y se eliminó en la versión 2.4.8. Debe utilizar el comando CLI descrito en esta página para cambiar la clave de cifrado después de actualizar a 2.4.8.

**Para cambiar una clave de cifrado:**

Las siguientes instrucciones requieren acceso a un terminal.

1. Habilitar [modo de mantenimiento](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/setup/application-modes#maintenance-mode).

   ```bash
   bin/magento maintenance:enable
   ```

1. Deshabilitar trabajos cron.

   _Proyectos de infraestructura en la nube:_

   ```bash
   ./vendor/bin/ece-tools cron:disable
   ```

   _Proyectos locales_

   ```bash
   crontab -e
   ```

1. Cambie la clave de cifrado mediante uno de los siguientes métodos.

   +++comando CLI

   Ejecute el siguiente comando de CLI y asegúrese de que se completa sin errores. Si necesita volver a cifrar ciertos valores de configuración del sistema o campos de pago, consulte la [guía detallada sobre el recifrado](https://developer.adobe.com/commerce/php/development/security/data-encryption/) en la _Guía para desarrolladores de PHP_.

   ```bash
   bin/magento encryption:key:change
   ```

   +++

   +++Configuración de administración

   >[!IMPORTANT]
   >
   >Esta función ha quedado obsoleta y se eliminó en la versión 2.4.8. Adobe recomienda cambiar las claves de cifrado con la CLI.

   1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

      ![Clave de cifrado del sistema](./assets/encryption-key.png){width="700" zoomable="yes"}

   1. Realice una de las siguientes acciones:

      - Para generar una clave nueva, establezca **[!UICONTROL Auto-generate Key]** en `Yes`.
      - Para usar una clave diferente, establezca **[!UICONTROL Auto-generate Key]** en `No`. A continuación, en el campo **[!UICONTROL New Key]**, escriba o pegue la clave que desee utilizar.

   1. Haga clic en **[!UICONTROL Change Encryption Key]**.

      >[!NOTE]
      >
      >Mantenga un registro de la nueva clave en una ubicación segura. Es necesario descifrar los datos si se produce algún problema con los archivos.

   +++

1. Vaciar la caché.

   _Proyectos de infraestructura en la nube:_

   ```bash
   magento-cloud cc
   ```

   _Proyectos locales:_

   ```bash
   bin/magento cache:flush
   ```

1. Habilitar trabajos cron.

   _Proyectos de infraestructura en la nube:_

   ```bash
   ./vendor/bin/ece-tools cron:enable
   ```

   _Proyectos locales:_

   ```bash
   crontab -e
   ```

1. Desactive el modo de mantenimiento.

   ```bash
   bin/magento maintenance:disable
   ```
