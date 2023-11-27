---
title: Clave de cifrado
description: Aprenda a generar o agregar automáticamente su propia clave de cifrado, que debe cambiarse regularmente para mejorar la seguridad.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
source-git-commit: 21be3c7a56cb72d685b2b3605bc27266e8e55f37
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Clave de cifrado

Adobe Commerce y Magento Open Source utilizan una clave de cifrado para proteger contraseñas y otros datos confidenciales. Un estándar del sector [!DNL ChaCha20-Poly1305] algoritmo se utiliza con una clave de 256 bits para cifrar todos los datos que requieren cifrado. Esto incluye datos de tarjetas de crédito y contraseñas de integración (módulo de pago y envío). Además, se utiliza un algoritmo hash seguro (SHA-256) para cifrar todos los datos que no requieren descifrado.

Durante la instalación inicial, se le pedirá que deje que Commerce genere una clave de cifrado o que introduzca una suya. La herramienta de clave de cifrado permite cambiar la clave según sea necesario. La clave de cifrado debe cambiarse regularmente para mejorar la seguridad y, en cualquier momento, la clave original puede verse comprometida. Cada vez que se cambia la clave, todos los datos heredados se vuelven a codificar con la nueva clave.

Para obtener información técnica, consulte [Instalación local avanzada](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) en el _Guía de instalación_.

## Paso 1: Hacer que el archivo sea editable

Para cambiar la clave de cifrado, asegúrese de que el siguiente archivo es grabable: `[your store]/app/etc/env.php`

## Paso 2: Cambiar la clave de cifrado

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

   ![Clave de cifrado del sistema](./assets/encryption-key.png){width="700" zoomable="yes"}

1. Realice una de las siguientes acciones:

   - Para generar una clave nueva, establezca **[!UICONTROL Auto-generate Key]** hasta `Yes`.
   - Para utilizar una clave diferente, establezca **[!UICONTROL Auto-generate Key]** hasta `No`. A continuación, en la **[!UICONTROL New Key]** , introduzca o pegue la clave que desee utilizar.

1. Haga clic **[!UICONTROL Change Encryption Key]**.

1. Mantenga un registro de la nueva clave en una ubicación segura.

   Es necesario descifrar los datos si se produce algún problema con los archivos.
