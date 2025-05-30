---
title: CAPTCHA
description: Obtenga información sobre cómo configurar CAPTCHA para el acceso de administrador y varias acciones de tienda iniciadas por clientes registrados.
exl-id: b2867ad5-7d48-4e9f-b84e-3cf0a14ec16f
role: Admin
feature: Configuration, Security
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '959'
ht-degree: 0%

---

# CAPTCHA

Un CAPTCHA es un dispositivo visual que garantiza que un ser humano, en lugar de un ordenador (o &quot;bot&quot;), está interactuando con el sitio. CAPTCHA es el acrónimo de _Prueba de Turing pública completamente automatizada para diferenciar entre ordenadores y humanos_. Se puede utilizar tanto para el acceso de administrador como para varias acciones de tienda iniciadas por clientes registrados. Adobe Commerce y Magento Open Source admiten el CAPTCHA estándar descrito en este tema y [Google reCAPTCHA](security-google-recaptcha.md).

Puede volver a cargar el CAPTCHA tantas veces como sea necesario haciendo clic en el icono Recargar en la esquina superior derecha de la imagen. El CAPTCHA es totalmente configurable y se puede configurar para que aparezca cada vez o solo después de un número definido de intentos de inicio de sesión fallidos.

![Iniciar sesión con CAPTCHA](./assets/customer-account-login-captcha.png){width="700" zoomable="yes"}

## Configurar CAPTCHA para el administrador

Para obtener un nivel adicional de seguridad, puede agregar un CAPTCHA a la página Inicio de sesión del administrador y olvido de la contraseña. Los usuarios administradores pueden volver a cargar el CAPTCHA mostrado haciendo clic en el icono _Recargar_ ![Icono de recarga](./assets/CAPTCHA-icon-reload.png) en la esquina superior derecha de la imagen. El número de recargas es ilimitado.

![Administrador - Iniciar sesión con CAPTCHA](./assets/security-captcha-admin.png){width="300"}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Advanced]** y elija **[!UICONTROL Admin]**.

1. En la esquina superior derecha, establezca **[!UICONTROL Store View]** en `Default`.

   Si el [ámbito](../getting-started/websites-stores-views.md#scope-settings) de su instalación de Commerce incluye varios sitios web, elija los sitios web donde desea que se aplique la configuración de CAPTCHA.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL CAPTCHA]**.

1. Establezca **[!UICONTROL Enable CAPTCHA in Admin]** en `Yes`. A continuación, complete las opciones restantes de la siguiente manera:

   ![Administrador - Configuración de CAPTCHA](../configuration-reference/advanced/assets/admin-captcha.png){width="600" zoomable="yes"}

   - Escriba el nombre de **[!UICONTROL Font]** que se usará para los símbolos CAPTCHA (predeterminado: `LinLibertine`).

     Para agregar su propia fuente, el archivo de fuentes debe residir en el mismo directorio que la instalación de Commerce y debe declararse en el archivo `config.xml` del módulo Captcha en `app/code/Magento/Captcha/etc`.

   - Seleccione cualquiera de los(as) siguientes **[!UICONTROL Forms]** donde se usará el CAPTCHA. Para elegir varios formularios, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac).

      - `Admin Login`
      - `Admin Forgot Password`

   - Establezca **[!UICONTROL Displaying Modes]** en una de las siguientes opciones:

      - `Always`: CAPTCHA siempre es necesario para iniciar sesión en el administrador.
      - `After number of attempts to login`: esta opción sólo se aplica al formulario de inicio de sesión de administrador. Cuando se selecciona, aparece el campo _[!UICONTROL Number of Unsuccessful Attempts to Login]_. Introduzca el número de intentos de inicio de sesión que desea permitir. Un valor de 0 (cero) es similar a establecer el modo de visualización en `Always`.

     Para realizar un seguimiento del número de intentos de inicio de sesión erróneos, se contabiliza cada intento de inicio de sesión con una dirección de correo electrónico y desde una dirección IP. El número máximo de intentos de inicio de sesión permitidos desde la misma dirección IP es de 1000. Esta limitación se aplica solamente cuando CAPTCHA está habilitado.

   - Para **[!UICONTROL Number of Unsuccessful Attempts to Login]**, introduzca el número de veces que el administrador puede intentar iniciar sesión antes de que aparezca el CAPTCHA. Si se establece en cero (`0`), siempre se requiere CAPTCHA.

   - Para **[!UICONTROL CAPTCHA Timeout (minutes)]**, ingrese el número de minutos antes de que caduque el CAPTCHA. Cuando caduca el CAPTCHA, el administrador debe volver a cargar la página.

   - Escriba **[!UICONTROL Number of Symbols]** para que aparezca en el CAPTCHA. Se pueden usar hasta ocho símbolos (`8`). Para un número variable de símbolos que cambia con cada CAPTCHA, escriba un intervalo (como `5-8`).

   - Para **[!UICONTROL Symbols Used in CAPTCHA]**, escriba las letras (a-z y A-Z) y los números (0-9) que desee que aparezcan aleatoriamente en el CAPTCHA. Los símbolos que son difíciles de distinguir de otros símbolos, como `i`, `l` o `1`, no se incluyen en el conjunto predeterminado de símbolos CAPTCHA.

   - Establezca **[!UICONTROL Case Sensitive]** en `Yes` si desea que los administradores escriban los caracteres en mayúsculas o minúsculas exactamente como se muestra en el CAPTCHA.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Configurar CAPTCHA para la tienda

Se puede requerir que los clientes introduzcan un CAPTCHA cada vez que inicien sesión en sus cuentas o después de varios intentos fallidos de iniciar sesión. Además, numerosos formularios utilizados en toda la tienda pueden configurarse para requerir la verificación por parte de CAPTCHA.

![CAPTCHA durante el cierre de compra](./assets/storefront-checkout-payment-captcha.png){width="700" zoomable="yes"}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Customer Configuration]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL CAPTCHA]**.

![Configuración de CAPTCHA del cliente](../configuration-reference/customers/assets/customer-configuration-captcha.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Enable CAPTCHA on Storefront]** en `Yes`. A continuación, complete las opciones restantes de la siguiente manera:

   - Escriba el nombre de **[!UICONTROL Font]** que se usará para los símbolos CAPTCHA (predeterminado: `LinLibertine`).

     Para agregar su propia fuente, el archivo de fuentes debe residir en el mismo directorio que la instalación de Commerce y debe declararse en el archivo `config.xml` del módulo CAPTCHA.

   - Seleccione cualquiera de los(as) siguientes **[!UICONTROL Forms]** donde se usará el CAPTCHA. Para elegir varios formularios, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac).

      - `Applying coupon code`
      - `Checkout/Placing Order`
      - `Create user`
      - `Login`
      - `Forgot password`
      - `Contact Us`
      - `Change password`
      - `Share Wishlist Form`
      - `Payflow Pro` (ver [parche de seguridad](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html?lang=es) _artículo de la base de conocimiento_)
      - `Send to Friend Form` ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source)
      - `Add Gift Card Code` ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)
      - `Create company` ![Adobe Commerce B2B](../assets/b2b.svg) (disponible solo con Adobe Commerce B2B)

   - Establezca **[!UICONTROL Displaying Mode]** en una de las siguientes opciones:

      - `Always`: CAPTCHA siempre es necesario para acceder a los formularios seleccionados.
      - `After number of attempts to login`: introduzca el número de intentos de inicio de sesión antes de que aparezca el CAPTCHA. Un valor de 0 (cero) es similar a &quot;Siempre&quot;. Cuando se selecciona, aparece el número de intentos de inicio de sesión erróneos. Esta opción no se aplica al formulario Contraseña olvidada, que si está habilitado, siempre muestra el CAPTCHA.

   - Para **[!UICONTROL Number of Unsuccessful Attempts to Login]**, introduzca el número de veces que un cliente puede iniciar sesión incorrectamente antes de que aparezca el CAPTCHA. Si se establece en cero (`0`), siempre se usa CAPTCHA.

   - Para **[!UICONTROL CAPTCHA Timeout (minutes)]**, ingrese el número de minutos antes de que caduque el CAPTCHA. Cuando caduca el CAPTCHA, el cliente debe volver a cargar la página para generar un nuevo CAPTCHA.

   - Escriba **[!UICONTROL Number of Symbols]** para que aparezca en el CAPTCHA. Se pueden usar hasta ocho símbolos (`8`). Para un número variable de símbolos que cambia con cada CAPTCHA, escriba un intervalo (como `5-8`).

   - Para **[!UICONTROL Symbols Used in CAPTCHA]**, escriba las letras (a-z y A-Z) y los números (0-9) que desee que aparezcan aleatoriamente en el CAPTCHA. El conjunto predeterminado de caracteres no incluye símbolos similares como `I` o `1`. Para obtener los mejores resultados, utilice símbolos que los usuarios puedan identificar fácilmente.

   - Establezca **[!UICONTROL Case Sensitive]** en `Yes` si desea que los clientes escriban los caracteres en mayúsculas o minúsculas exactamente como se muestra en el CAPTCHA.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
