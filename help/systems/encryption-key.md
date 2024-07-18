---
title: Clave de cifrado
description: Aprenda a generar o agregar automáticamente su propia clave de cifrado, que debe cambiarse regularmente para mejorar la seguridad.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
source-git-commit: 2469b3853d074f7a7adfe822b645e41d1420259a
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Clave de cifrado

Adobe Commerce y Magento Open Source utilizan una clave de cifrado para proteger contraseñas y otros datos confidenciales. Se utiliza un algoritmo [!DNL ChaCha20-Poly1305] estándar del sector con una clave de 256 bits para cifrar todos los datos que requieren cifrado. Esto incluye datos de tarjetas de crédito y contraseñas de integración (módulo de pago y envío). Además, se utiliza un algoritmo hash seguro (SHA-256) para cifrar todos los datos que no requieren descifrado.

Durante la instalación inicial, se le pedirá que deje que Commerce genere una clave de cifrado o que introduzca una suya. La herramienta de clave de cifrado permite cambiar la clave según sea necesario. La clave de cifrado debe cambiarse regularmente para mejorar la seguridad y, en cualquier momento, la clave original puede verse comprometida. Cada vez que se cambia la clave, todos los datos heredados se vuelven a codificar con la nueva clave.

Para obtener información técnica, consulte [Instalación local avanzada](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) en la _Guía de instalación_.

>[!IMPORTANT]
>
>Antes de seguir estas instrucciones para cambiar la clave de cifrado, asegúrese de que el siguiente archivo se puede escribir: `[your store]/app/etc/env.php`

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

1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

   ![Clave de cifrado del sistema](./assets/encryption-key.png){width="700" zoomable="yes"}

1. Realice una de las siguientes acciones:

   - Para generar una clave nueva, establezca **[!UICONTROL Auto-generate Key]** en `Yes`.
   - Para usar una clave diferente, establezca **[!UICONTROL Auto-generate Key]** en `No`. A continuación, en el campo **[!UICONTROL New Key]**, escriba o pegue la clave que desee utilizar.

1. Haga clic en **[!UICONTROL Change Encryption Key]**.

   >[!NOTE]
   >
   >Mantenga un registro de la nueva clave en una ubicación segura. Es necesario descifrar los datos si se produce algún problema con los archivos.

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
