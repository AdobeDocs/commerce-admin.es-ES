---
title: Detalles de tienda
description: Aprenda a actualizar la información básica de su tienda.
exl-id: f4910ff7-4fcc-482f-be1d-cad8564cdd86
feature: Configuration
source-git-commit: c9c04d4fb2f51b9bac0de6a172d7bcf35be18a85
workflow-type: tm+mt
source-wordcount: '1895'
ht-degree: 0%

---

# Detalles de tienda

La información básica de la tienda incluye el nombre y la dirección de la tienda, el número de teléfono y la dirección de correo electrónico que aparecen en los mensajes de correo electrónico, las facturas y otras comunicaciones enviadas a los clientes.

![Configuración general - detalles de la tienda](./assets/config-general-store-details.png){width="900" zoomable="yes"}

## [!UICONTROL Store Information]

La sección _[!UICONTROL Store Information]_&#x200B;proporciona la información básica que aparece en los documentos de ventas y en otras comunicaciones.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En **[!UICONTROL General]** en el panel de navegación izquierdo, elija **[!UICONTROL General]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Store Information]**.

   ![Configuración general: información de almacén](./assets/general-store-information.png){width="700"}

1. Configure las opciones según los detalles de la tienda:

   - Escriba el(la) **[!UICONTROL Store Name]** que desee usar en todas las comunicaciones.

   - Escriba **[!UICONTROL Store Phone Number]** con el formato que desea que aparezca.

   - Para **[!UICONTROL Store Hours of Operation]**, ingresa las horas en que tu tienda está abierta por negocios. Por ejemplo: `Mon - Fri, 9-5, Sat 9-noon PST`.

   - Seleccione **[!UICONTROL Country]** donde se encuentra su empresa.

   - Seleccione el(la) **[!UICONTROL Region/State]** con el país.

   - Escriba **[!UICONTROL Store Address]**. Si la dirección es larga, continúe con la dirección en **Línea 2** de la dirección del almacén.

   - Si corresponde, ingrese el **[!UICONTROL VAT Number]** de su tienda.

     Para comprobar el número, haga clic en el botón **[!UICONTROL Validate VAT Number]**. Para obtener más información, consulta [Validación de ID de IVA](../stores-purchase/vat.md#vat-id-validation).

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

Para obtener más información acerca de las opciones de configuración de información de almacén, vea la [_Guía de referencia de configuración_](../configuration-reference/general/general.md#store-information).

## [!UICONTROL Locale Options]

La configuración regional determina la mayoría de las opciones de configuración que se usan en el almacén. Algunos de ellos son:

- Idioma
- País
- Tipo impositivo
- Moneda
- Precio
- Formato de número

La configuración regional determina la zona horaria y el idioma utilizados para cada tienda e identifica los días de la semana laboral en el área.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel de navegación izquierdo bajo **[!UICONTROL General]**, elija **[!UICONTROL General]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Locale Options]**.

   ![Configuración general - opciones de configuración regional](./assets/general-locale-options.png){width="700"}

1. Seleccione su **[!UICONTROL Timezone]** de la lista.

1. Establezca **[!UICONTROL Locale]** en el idioma del almacén.

1. Establezca **[!UICONTROL Weight Unit]** en la unidad de medida que se suele utilizar para los envíos de su configuración regional.

1. Establezca **[!UICONTROL First Day of the Week]** en el día que se considere el primer día de la semana en su área.

1. En la lista **[!UICONTROL Weekend Days]**, seleccione los días que caen en un fin de semana en su área.

   Para seleccionar varios días, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada elemento.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

Para obtener más información acerca de las opciones de configuración regional, consulte la [Guía de referencia de configuración](../configuration-reference/general/general.md#locale-options).

## [!UICONTROL State Options]

En muchos países, el estado, la provincia o la región es una parte obligatoria de una dirección postal. La información se utiliza para la información de envío y facturación, para calcular las tasas de impuestos, etc. En los países en los que el estado no es obligatorio, el campo se puede omitir por completo de la dirección o incluirse como campo opcional.

Dado que los formatos de dirección estándar varían de un país a otro, también puede editar la plantilla que se utiliza para dar formato a la dirección de las facturas, los albaranes y las etiquetas de envío.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En **[!UICONTROL General]** en el panel de navegación izquierdo, elija **[!UICONTROL General]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL State Options]**.

   ![Configuración general - opciones de estado](./assets/general-state-options.png){width="700"}

1. Utilice la lista **[!UICONTROL State is required for]** para seleccionar cada país donde Región/Estado sea una entrada requerida.

1. Establezca **[!UICONTROL Allow to Choose State if it is Optional for Country]** en una de las siguientes opciones:

   `Yes`: en países donde el campo de estado no es obligatorio, incluye el campo de estado como una entrada opcional.

   `No`: en los países donde el campo de estado no es obligatorio, omite el campo de estado.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

Para obtener más información acerca de las opciones de configuración de estado, consulte la [Guía de referencia de configuración](../configuration-reference/general/general.md#state-options).

## [!UICONTROL Country Options]

Las opciones de país identifican el país donde se encuentra su negocio y los países desde los que acepta el pago.

### Establece las opciones de país para tu tienda

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel de navegación izquierdo bajo **[!UICONTROL General]**, elija **[!UICONTROL General]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Country Options]**.

   >[!NOTE]
   >
   >Si es necesario, desactive la casilla de verificación **[!UICONTROL Use system value]** para cada configuración que desee cambiar.

   ![Configuración general - configuración de país](./assets/general-country-options.png){width="700"}

1. Elija **[!UICONTROL Default Country]** donde se encuentra su empresa.

1. En la lista **[!UICONTROL Allow Countries]**, seleccione cada país desde el que acepte pedidos.

   De forma predeterminada, se seleccionan todos los países de la lista. Para seleccionar varios países, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada elemento.

1. Utilice la lista **[!UICONTROL Zip/Postal Code is Optional for]** para seleccionar cada país donde lleve a cabo su actividad comercial sin que sea necesario incluir un código postal como parte de la dirección postal.

1. En la lista **[!UICONTROL European Union Countries]**, seleccione cada país de la UE en el que lleve a cabo su actividad comercial.

   De forma predeterminada, se seleccionan todos los países de la UE. Para seleccionar los países que necesita, mantenga presionada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada elemento.

1. En la lista **[!UICONTROL Top Destinations]**, seleccione los países principales a los que desea destinar las ventas.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

### Definir las opciones de país para un método de envío específico

También puede configurar el envío a determinados países para cada [método de envío](../stores-purchase/delivery.md) disponible (UPS, FedEx, etc.).

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel de navegación izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Delivery Methods]**.

1. Seleccione el transportista al que desea aplicar determinados países.

1. Para **[!UICONTROL Ship to Applicable Countries]**, anule la selección de la casilla **[!UICONTROL Use system value]** y seleccione la opción **[!UICONTROL Specific Countries]**.

1. En la lista **[!UICONTROL Top Destinations]**, seleccione los países principales que se van a enviar.

   ![Ejemplo de configuración de las opciones de país para el método de entrega DHL](./assets/country-options-for-specific-delivery-method.png){width="700"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

### Solución de problemas de recursos

Para obtener ayuda con la resolución de problemas de configuración de país, consulte los siguientes artículos de la Base de conocimiento de asistencia de [!DNL Commerce]:

- [Cómo agregar un país](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/how-to-add-a-new-country-to-magento-2.html?lang=es)

## [!UICONTROL Merchant Location]

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."}

La configuración Ubicación del comerciante se usa para configurar [métodos de pago](../stores-purchase/payments.md). Si no hay ningún valor para esta configuración, se usa la configuración [País predeterminado](#uicontrol-country-options).

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel de navegación izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Payment Methods]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **Ubicación del comerciante** y elija su **[!UICONTROL Merchant Country]**.

   ![Configuración de ubicación de comerciante](./assets/payment-methods-merchant-location.png){width="600"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

Para obtener más información acerca de las opciones de configuración de los métodos de pago, consulte la [Guía de referencia de configuración](../configuration-reference/sales/payment-methods.md).

## Moneda

Configuración de moneda: define la [moneda](../stores-purchase/currency-configuration.md) base y cualquier moneda adicional que se acepte como pago. Establece también la conexión y programación de importación que se utiliza para actualizar las tasas de cambio automáticamente.

Símbolos de moneda: define los [símbolos de moneda](../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) que aparecen en los precios de los productos y en los documentos de ventas, como pedidos y facturas. [!DNL Commerce] admite monedas de más de 200 países de todo el mundo.

Actualizando tipos de cambio: los tipos de cambio pueden [actualizarse](../stores-purchase/currency-update.md) manualmente o importarse en su tienda según sea necesario o según una programación predefinida.

Selector de moneda: si hay varias monedas disponibles, el [selector de moneda](../stores-purchase/currency.md) está disponible en el encabezado de la tienda.

## [!UICONTROL Store Email Addresses]

Puede tener hasta cinco direcciones de correo electrónico diferentes para representar funciones o departamentos distintos para cada tienda o vista. Además de las siguientes identidades de correo electrónico predefinidas, hay algunas identidades personalizadas que puede configurar según sus necesidades.

- Contacto general
- Representante de ventas
- Atención al cliente

Cada identidad y su dirección de correo electrónico asociada se pueden asociar con mensajes de correo electrónico automatizados específicos y aparecen como el remitente de los mensajes de correo electrónico que se envían desde la tienda.

### Paso 1: Configurar las direcciones de correo electrónico para su dominio

Para poder configurar las direcciones de correo electrónico de la tienda, debe configurarse cada una de ellas como una dirección de correo electrónico válida para su dominio. Para crear cada dirección de correo electrónico necesaria, siga las instrucciones del administrador del servidor o del proveedor de alojamiento de correo electrónico.

### Paso 2: Establecer la dirección URL base para los vínculos generados

[!BADGE Solo SaaS]{type=Positive url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Solo se aplica a proyectos de Adobe Commerce as a Cloud Service (infraestructura de SaaS administrada por Adobe)."}

Algunos correos electrónicos dirigidos al cliente incluyen vínculos a la tienda, como los que ayudan a los clientes a restablecer sus contraseñas. Para garantizar que los vínculos a la tienda funcionen, debe definir la dirección URL base de la tienda.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En **[!UICONTROL General]** en el panel de navegación izquierdo, elija **[!UICONTROL Store Email Addresses]**.

1. En el campo **[!UICONTROL Storefront Base URL]** **[!UICONTROL General]** sección, ingrese la URL raíz para su tienda, como `https://www.example.com/`. La dirección URL debe finalizar con una barra diagonal.

   ![Configuración general - General](../configuration-reference/general/assets/store-email-addresses-general-general.png){width="600"}

### Paso 3: Configurar las direcciones de correo electrónico de la tienda

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En **[!UICONTROL General]** en el panel de navegación izquierdo, elija **[!UICONTROL Store Email Addresses]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL General Contact]** y haga lo siguiente:

   ![Configuración general: almacenar direcciones de correo electrónico](./assets/store-email-addresses-general-contact.png){width="600"}

   - Para **[!UICONTROL Sender Name]**, escriba el nombre de la persona asociada con la identidad del contacto general para que aparezca como el remitente de los mensajes de correo electrónico.

   - Para **[!UICONTROL Sender Email]**, escriba la dirección de correo electrónico asociada.

1. Repita este proceso para cada dirección de correo electrónico de tienda que vaya a utilizar.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

### Paso 4: Actualizar la configuración del correo electrónico de ventas

Si utiliza direcciones de correo electrónico personalizadas, asegúrese de actualizar la configuración de cualquier mensaje de correo electrónico relacionado para que la identidad correcta aparezca como el remitente.

1. En el panel de navegación izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Sales Emails]**.

   La página tiene una sección independiente para cada una de las siguientes opciones:

   - Comentarios sobre pedidos y pedidos
   - Factura y comentarios de factura
   - Comentarios sobre envíos y envíos
   - Notas de Abono y Comentarios de Notas de Abono
   - RMA, Autorización de RMA, Comentarios del Administrador de RMA y Comentarios del Cliente de RMA ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

1. A partir de **[!UICONTROL Order]**, expanda la sección de cada mensaje y asegúrese de que está seleccionado el remitente correcto.

   ![Configuración de ventas - correos electrónicos de ventas](./assets/sales-emails-order.png){width="600"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

Para obtener más información acerca de las opciones de configuración de los correos electrónicos de ventas, consulte la [_Guía de referencia de configuración_](../configuration-reference/sales/sales-emails.md).

## Formulario de contacto

El vínculo _Contáctenos_ que aparece al pie de página de la tienda es una manera sencilla de que los clientes se mantengan en contacto con usted. Los clientes pueden completar el formulario para enviar un mensaje a su tienda. Una instalación estándar de [!DNL Commerce] muestra el formulario _Contáctenos_ predeterminado. Después de enviar el formulario, aparece un mensaje de agradecimiento

Es importante comprender que el formulario predeterminado Póngase en contacto con nosotros se procesa directamente desde el código en lugar de desde una página de CMS.

![Página de contacto predeterminada](./assets/page-contact-us-default.png){width="700"}

El pie de página de la tienda incluye un vínculo a la página Póngase en contacto con nosotros que está disponible en toda la tienda.

![Vínculo Póngase en contacto con nosotros en el pie de página](./assets/storefront-footer-contact-us.png){width="700"}

Los datos de ejemplo de Luma incluyen información adicional sobre la página Póngase en contacto con nosotros que muestra cómo puede personalizar la página para su tienda.

![Página de contacto](./assets/storefront-contact-us.png){width="700"}

### Configuración del formulario de contacto

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel de navegación izquierdo bajo **[!UICONTROL General]**, elija **[!UICONTROL Contacts]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Contact Us]** y establezca **[!UICONTROL Enable Contact Us]** en `Yes`.

   ![Configuración general: contáctenos](./assets/contacts-contact-us.png){width="600"}

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Email Options]** y establezca las opciones de contacto de correo electrónico:

   ![Configuración general: opciones de correo electrónico](./assets/contacts-email-options.png){width="600"}

   - Para **[!UICONTROL Send Emails to]**, escriba la dirección de correo electrónico a la que se enviarán los mensajes del formulario Contáctenos.

   - Establezca **[!UICONTROL Email Sender]** en la identidad del almacén que aparece como el remitente del mensaje desde el formulario Póngase en contacto con nosotros. Por ejemplo: Correo electrónico personalizado 2.

   - Establezca **[!UICONTROL Email Template]** en la plantilla que se usa para los mensajes enviados desde el formulario Contáctenos.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

### Personalización del contenido

Puede personalizar el contenido en el formulario _Póngase en contacto con nosotros_ para adaptarlo a las necesidades de sus directivas de tienda y servicio al cliente.

### Método 1: Uso de datos de ejemplo

Los datos de ejemplo de Luma incluyen un bloque de _Información de contacto_ que se puede personalizar para tu tienda. El `contact-us-info` [bloque](../content-design/blocks.md) se puede modificar fácilmente para agregar su propio contenido a la página Contáctenos.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Busque el bloque **[!UICONTROL Contact Us Info]** en la lista y abra en el modo **[!UICONTROL Edit]**.

   ![Bloque de información de contacto](./assets/content-block-contact-us-info.png){width="700"}

1. En la parte inferior de la página de bloque, haga clic en **[!UICONTROL Edit with Page Builder]**.

   ![Bloque de contenido: contáctenos, ejemplo](./assets/content-block-contact-us-content.png){width="700"}

   >[!NOTE]
   >
   >Si ha [[!DNL Page Builder] deshabilitado](../page-builder/setup.md#disable-dnl-page-builder), puede usar el editor [toolbar](../content-design/editor.md) para dar formato al texto y agregar [imágenes](../content-design/editor-insert-image.md) y [vínculos](../content-design/editor-insert-link.md).

1. Pase el ratón sobre el contenedor de HTML para ver la caja de herramientas y elija el icono _Configuración_ (![Icono Configuración](../page-builder/assets/pb-icon-settings.png) ).

1. Edite el código HTML según proporcione la información de contacto de la tienda y haga clic en **[!UICONTROL Save]**.

   ![Bloque de contenido: editar código HTML](./assets/content-block-contact-us-html.png){width="700"}

1. Salga del escenario [!DNL Page Builder] y haga clic en **[!UICONTROL Save Block]**.

### Método 2: Sin datos de ejemplo

>[!IMPORTANT]
>
>A partir de la versión 2.4.0, el formulario de contacto ya no puede llamar a dentro de un bloque de CMS o de una página de CMS. Toda personalización del formulario de contacto debe realizarse utilizando el xml de diseño o plantillas de temas personalizadas.

De manera predeterminada, los compradores tienen acceso al formulario de contacto mediante el _vínculo de contacto_ que aparece al pie de las páginas de la tienda. Para obtener más información sobre cómo personalizar la página de contacto, consulte la [Guía para desarrolladores de FrontEnd][theme-guide].

[theme-guide]: https://developer.adobe.com/commerce/frontend-core/guide/themes/
