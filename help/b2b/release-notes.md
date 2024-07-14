---
title: '[!DNL Adobe Commerce B2B] notas de la versión'
description: Revise las notas de la versión para obtener información acerca de los cambios en  [!DNL Adobe Commerce B2B] versiones.
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: 35402eda770e59cc2862b204e6e54b55190ded13
workflow-type: tm+mt
source-wordcount: '6867'
ht-degree: 0%

---

# [!DNL Adobe Commerce B2B] notas de la versión

Estas notas de la versión de la extensión B2B recopilan las adiciones y correcciones que Adobe ha añadido durante un ciclo de lanzamiento de, entre las que se incluyen:

![Nuevas](../assets/new.svg) nuevas características
![Se ha corregido un problema](../assets/fix.svg) Correcciones y mejoras
![Problema conocido](../assets/bug.svg) Problemas conocidos

>[!NOTE]
>
>Consulte [Disponibilidad del producto](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) para obtener información sobre las versiones de la extensión de Commerce B2B compatibles con las versiones de Adobe Commerce disponibles.

## B2B 1.5.0-beta

{{$include /help/_includes/b2b-beta-note.md}}

*13 de noviembre de 2023*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

La versión beta B2B v1.5.0 incluye nuevas funciones, mejoras de calidad y correcciones de errores.

![Nuevas](../assets/new.svg) mejoras en las capacidades de cotización ayudan a los compradores y vendedores a administrar las ofertas y la negociación de presupuestos de manera más eficaz.

- **Guardar presupuesto como borrador**<!--B2B-2566-->: al crear una [solicitud de presupuesto](quote-request.md) desde el carro de compras, los compradores ahora pueden guardar el presupuesto como borrador al seleccionar **[!UICONTROL Save as Draft]** en el formulario [!UICONTROL Request a Quote].

  El borrador de la oferta no tiene fecha de caducidad. Los compradores pueden revisar y actualizar los borradores de presupuestos desde la sección [!UICONTROL My Quotes] de su panel de cuentas.

- **Cambiar nombre de presupuesto**<!--B2B-2596-->: los compradores ahora pueden cambiar el nombre de un presupuesto de la página [Detalle del presupuesto](account-dashboard-my-quotes.md#quote-actions) seleccionando la opción **[!UICONTROL Rename]**. Esta opción está disponible para los compradores autorizados cuando editan la oferta. Los eventos de cambio de nombre se registran en el Registro del historial de ofertas.

- **Oferta duplicada**<!--B2B-2701-->: los compradores y vendedores ahora pueden crear una nueva oferta copiando una oferta existente. Se crea una copia de la vista de detalles de la oferta seleccionando **[!UICONTROL Create Copy]** en la [vista de detalles de la oferta](quote-price-negotiation.md#button-bar) en el Administrador o en la [Tienda](account-dashboard-my-quotes.md#quote-actions).

- **Bloqueo de descuento de artículo de línea**<!--B2B-2597-->: durante la negociación de la oferta, los vendedores pueden usar el bloqueo de descuento de artículo de línea para obtener más flexibilidad al aplicar descuentos. Por ejemplo, un vendedor puede aplicar un descuento especial por artículo de línea a un artículo y bloquearlo para evitar descuentos adicionales. Cuando un artículo está bloqueado, el precio del artículo no se puede actualizar cuando se aplica un descuento de nivel de oferta. Ver [Iniciar presupuesto para un comprador](sales-rep-initiates-quote.md).

![Nueva ](../assets/new.svg)**administración de la compañía**<!--B2B-2901-->: los comerciantes ahora pueden ver y administrar las compañías de Adobe Commerce como organizaciones jerárquicas al asignar compañías a compañías principales designadas. Una vez asignada una compañía a una matriz, el administrador de la compañía matriz puede administrar la cuenta de la compañía. Solo los usuarios administradores autorizados pueden agregar y administrar asignaciones de la compañía. Para obtener más información, consulte [Administrar la jerarquía de la compañía](assign-companies.md).

- En la página Compañías, un nuevo campo **[!UICONTROL Company Type]** identifica las compañías principales y secundarias. Los comerciantes pueden filtrar la vista de la empresa por tipo de empresa y administrar las empresas mediante elementos de línea o acciones masivas.

- Los comerciantes pueden agregar y administrar asignaciones de compañía desde la nueva sección **[!UICONTROL Company Hierarchy]** en la página [!UICONTROL Company Account].

- Los desarrolladores de API pueden usar el nuevo extremo de API de REST de relaciones con la compañía `/V1/company/{parentId}/relations` para crear, ver y quitar asignaciones de la compañía. Consulte [Administrar objetos de empresa](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) en la *Guía para desarrolladores de API web*.

![Problema corregido](../assets/fix.svg)<!--ACP2E-1984-->A los comerciantes que hacen clic en el botón **[!UICONTROL Print]** en la vista de detalles de Oferta en el Administrador se les pide ahora que guarden la oferta como PDF. Anteriormente, se redirigía a los comerciantes a una página que contenía detalles de comillas.

![Se corrigió un problema](../assets/fix.svg) <!--ACP2E-1742-->Anteriormente, al enviar una oferta de cliente con 0 porcentaje y cambiar la cantidad, el administrador emite una excepción, pero guarda la cantidad. Una vez que se aplique esta corrección, se generará una excepción adecuada para `0 percentage` con un mensaje.

![Problema solucionado](../assets/fix.svg) <!--ACP2E-1742-->Durante la negociación del presupuesto, un vendedor ahora puede especificar un descuento de `0%` en el campo de descuento de presupuesto negociado y enviar el presupuesto de vuelta al comprador. Anteriormente, si el vendedor introducía un descuento del 0% y devolvía la oferta al comprador, el administrador devolvía un mensaje de error de `Exception occurred during quote sending`.

![Se ha corregido un problema](../assets/fix.svg) <!--ACP2E-2097-->La validación de ReCaptcha ahora funciona correctamente durante el proceso de cierre de compra de una cotización B2B cuando ReCaptcha V3 está configurado para el cierre de compra de tienda. Anteriormente, la validación fallaba con un mensaje de error `recaptcha validation failed, please try again`.

![Problema corregido](../assets/fix.svg) <!--ACP2E-1825-->Un usuario asociado a la compañía ya no puede realizar pedidos de compra una vez que la compañía ha sido bloqueada. Anteriormente, un usuario asociado a la compañía podía realizar pedidos de compra cuando se bloqueaba la compañía.

![Se ha corregido un problema](../assets/fix.svg)<!--ACP2E-1933-->Los administradores de la empresa ahora pueden agregar usuarios de la empresa desde la tienda. Anteriormente, Commerce registraba un error cuando un usuario administrador intentaba agregar un nuevo usuario: `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`.

## B2B v1.4.2-p1

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevo](../assets/new.svg) Se ha agregado compatibilidad con las versiones de parches de seguridad de Adobe Commerce 2.4.7-p1+ y 2.4.6-p6+.


## B2B v1.4.2

*10 de octubre de 2023*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

La versión B2B v1.4.2 incluye mejoras de calidad y correcciones de errores

![Problema corregido](../assets/fix.svg) <!--B2B-2897-->Si un vendedor crea una oferta de comprador que incluye un SKU de producto no disponible en el catálogo compartido asociado con la empresa del comprador, el sistema muestra el mensaje de error `The SKU you entered is not available in the shared catalog. Please check the SKU and try again`.  El vendedor no puede guardar la cotización hasta que elimine el producto que no está disponible. Anteriormente, la oferta se guardaba con el SKU no disponible incluido y no se podía cargar en la tienda.

## B2B v1.4.1

*7 de agosto de 2023*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}[Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Compatible con Adobe Commerce 2.4.7-beta1.

La versión B2B v1.4.1 incluye mejoras de calidad y correcciones de errores.

![Problema corregido](../assets/fix.svg) <!--ACP2E-1825-->Un usuario asociado a la compañía ya no puede realizar pedidos de compra una vez que la compañía ha sido bloqueada. Anteriormente, un usuario asociado a la compañía podía realizar pedidos de compra cuando se bloqueaba la compañía.

![Se ha corregido un problema](../assets/fix.svg) <!--ACP2E-1943-->El estado de producto no satisfecho ahora se muestra correctamente en la tienda. Anteriormente, los productos disponibles para el envío se identificaban incorrectamente como no pedidos.

![Problema corregido](../assets/fix.svg) <!--ACP2E-1862-->Si el formulario de registro de la empresa incluye un atributo de tipo de archivo de cliente, el archivo cargado durante el proceso de registro ahora se incluye en la información de cuenta del administrador de la empresa una vez creada la empresa. Anteriormente, faltaba el archivo adjunto.

![Problema corregido](../assets/fix.svg) <!--ACP2E-1793-->El selector de muestras para un producto configurable ahora se muestra según lo esperado en la página de configuración del elemento de la lista de solicitudes. Anteriormente, el selector de muestras se mostraba como un campo desplegable en la página de configuración de artículos de la lista de solicitudes.

![Se ha corregido un problema](../assets/fix.svg) <!--ACP2E-1968-->Al usar la [Consulta GraphQL de la empresa](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) para devolver los detalles de la empresa, los resultados ahora se devuelven correctamente sin errores.

## B2B v1.4.0

*13 de junio de 2023*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}[Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Compatible con Adobe Commerce 2.4.7-beta1

Esta versión incluye nuevas funciones y mejoras para presupuestos negociables B2B y varias correcciones de errores.

![Nuevo](../assets/new.svg) agregó compatibilidad con Adobe Commerce 2.4.7-beta1.

![Nuevo](../assets/new.svg) **El vendedor inició presupuestos**—Los vendedores ahora pueden iniciar un presupuesto para un comprador directamente desde las cuadrículas de Oferta y Cliente en el Administrador. Esta capacidad optimiza el proceso de cotización y reduce la complejidad para los clientes. Si un cliente no ha iniciado un pedido, un vendedor puede crear rápidamente una oferta en nombre del cliente e iniciar el proceso de negociación. Anteriormente, las ofertas solo se podían crear desde la tienda por el comprador o por un vendedor que iniciara sesión como cliente.

![Nuevo](../assets/new.svg) **Descuentos y negociación de artículo de línea**—<!--B2B-2440--> Dentro de una oferta, los compradores y vendedores de B2B ahora pueden negociar en el nivel de artículo de línea, aplicando descuentos e intercambiando notas hasta que se llegue a un acuerdo. La creación de notas y las actualizaciones se incluyen en el historial de artículos de línea y presupuestos para rastrear la comunicación. Anteriormente, los compradores y vendedores solo podían intercambiar notas y aplicar descuentos en el nivel de cotización.

![Problema corregido](../assets/fix.svg) Adobe Commerce ahora muestra los detalles correctos durante el pago cuando la opción Pedidos de compra está habilitada y se ha seleccionado una oferta virtual que se creó con la opción de pago PayPal. Anteriormente, los totales se mostraban como cero en estas condiciones.

![Se ha corregido un problema](../assets/fix.svg) <!--ACP2E-1504-->: ya no se producen errores de validación al intentar guardar una empresa con un límite de crédito superior a 999. Anteriormente, para los límites de crédito de empresa superiores a 999, el comercio de Adobe insertaba un separador de comas, lo que provocaba un error de validación que impedía guardar las actualizaciones.

![Problema corregido](../assets/fix.svg) <!--ACP2E-1474--> La dirección de envío seleccionada ahora permanece sin cambios cuando realiza un pedido con un presupuesto negociable. Anteriormente, al realizar un pedido, la dirección de envío seleccionada se cambiaba a la dirección de envío predeterminada.

![Se ha corregido un problema](../assets/fix.svg) <!--ACP2E-1429--> En la configuración de la tienda para las características B2B, el campo **[!UICONTROL Enable Shared Catalog direct products price assigning]** ahora se deshabilita automáticamente. En la tienda, se oculta cuando la configuración **[!UICONTROL Enable Company]** o **[!UICONTROL Enable Shared Catalog]** se establece en **[!UICONTROL No]**.

![Se ha corregido un problema](../assets/fix.svg) <!--ACP2E-1683--> Al crear una cuenta de empresa desde la tienda, Commerce ahora valida la dirección de correo electrónico antes de procesar el registro de empresa. Si la dirección de correo electrónico no es válida, la operación falla y no se procesan las actualizaciones de la cuenta. Anteriormente, se creaba una cuenta de cliente aunque la solicitud para crear una cuenta de empresa fallara debido a una dirección de correo electrónico no válida.

![Se ha corregido un problema](../assets/fix.svg) <!--ACP2E-1664--> Las SKU de producto que incluyen comillas dobles en el catálogo compartido y la estructura de precios ya no causan errores en el administrador.

![Se ha corregido un problema](../assets/fix.svg) <!--ACP2E-1498-->. Se ha actualizado la configuración de Barniz de la aplicación Commerce para evitar que los usuarios invitados vean datos de otros grupos de clientes.

### Problema conocido

Si instala o actualiza B2B 1.4.0 en [Adobe Commerce versión 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html), se producirá el siguiente error:

```terminal
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

Para solucionar este problema, agregue dependencias manuales para el paquete de seguridad B2B. Agregue dependencias manuales para el paquete de seguridad B2B con una [etiqueta de estabilidad](https://getcomposer.org/doc/04-schema.md#package-links). Para obtener instrucciones, consulte la [Base de conocimiento de Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html).

## B2B v1.3.5

*14 de marzo de 2023*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevo](../assets/new.svg) lanzó la versión 1.3.5-p2 de B2B para admitir la compatibilidad con Adobe Commerce 2.4.6-p2.

![Nuevo](../assets/new.svg) lanzó la versión 1.3.5-p1 de B2B para admitir la compatibilidad con Adobe Commerce 2.4.6-p1.

>[!NOTE]
>
>Después de actualizar Commerce de la versión 2.4.6 a la [última versión](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html#2.4.6), asegúrese de actualizar a la versión de parche B2B 1.3.5 compatible. O bien, actualice la extensión B2B de la versión 1.3.5 a la versión 1.4.0 o posterior para obtener las últimas funciones.

![Nuevo](../assets/new.svg) agregó compatibilidad con Adobe Commerce 2.4.6.

![Problema corregido](../assets/fix.svg) <!--- ACP2E-689--> Adobe Commerce ahora muestra los detalles correctos durante el pago cuando la opción Pedidos de compra está habilitada y se ha seleccionado una oferta virtual que se creó con la opción de pago PayPal. Anteriormente, los totales se mostraban como cero en estas condiciones.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-609-->: la lista de grupos de clientes para la configuración **Permitir exploración de categoría** ya no contiene grupos de clientes relacionados con catálogos compartidos.

![Problema corregido](../assets/fix.svg) <!--- ACP2E-1244--> El atributo de cliente Número de IVA/impuesto ahora funciona según lo esperado con las cuentas de administrador de la compañía tanto en el administrador como en la tienda. Los atributos personalizados de impuestos e IVA ya no son necesarios para crear una cuenta de empresa. Anteriormente, cuando un comerciante creaba una cuenta de empresa con un atributo personalizado de impuesto/IVA, Adobe Commerce generaba un error de validación tanto en la tienda como en el administrador.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-1236-->: ahora funciona correctamente el deshabilitar la característica de catálogo compartido en un ámbito específico. Anteriormente, Adobe Commerce establecía un ámbito no válido cuando un comerciante guardaba la configuración del catálogo compartido.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-1203--> Los usuarios administradores ahora pueden guardar valores de atributos personalizados de cliente para los usuarios de la empresa. Anteriormente, no se podían guardar los atributos personalizados de cliente para los usuarios de la empresa.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-1221--> Los problemas de rendimiento se resuelven con la validación de los permisos de la empresa proporcionados a través de GraphQL cuando ya se han asignado muchos permisos de la empresa.

![Problema corregido](../assets/fix.svg) <!--- ACP2E-1242--> Adobe Commerce ya no genera un error en la página del carro de compras cuando se usa el pedido rápido para agregar un producto en una cantidad que excede el inventario disponible.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-1090-->: se ha mejorado el rendimiento de `SELECT` operaciones de permisos de la compañía.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-2456--> Las consultas de categoría ahora devuelven precios de producto según la configuración de la tienda cuando no hay permisos de categoría establecidos explícitamente en la categoría que se está consultando.

![Problema corregido](../assets/fix.svg) <!--- ACP2E-6829--> El botón **[!UICONTROL Place Order]** ahora funciona como se espera al completar una compra con una solicitud de presupuesto aprobada. Se han resuelto los problemas con el complemento de presupuesto negociable `negotiableQuoteCheckoutSessionPlugin`.

## B2B v1.3.4

*9 de agosto de 2022*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevo](../assets/new.svg) agregó compatibilidad con Adobe Commerce 2.4.5.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-453-->Adobe Commerce ya no envía notificaciones por correo electrónico cada vez que una llamada API actualiza una compañía existente. Ahora, los correos electrónicos solo se envían cuando se crea una empresa.

![Problema corregido](../assets/fix.svg) <!--- ACP2E-406-->Adobe Commerce ahora calcula correctamente un total general de una cotización negociable cuando la configuración de cálculo de impuestos de **[!UICONTROL Enable Cross Border Trade]** está habilitada.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-322-->Los productos configurables ahora se mueven a la última posición de la lista de productos después de que se hayan actualizado las existencias cuando la configuración de **[!UICONTROL Move out of stock to the bottom]** esté habilitada. Se implementa una nueva consulta de base de datos personalizada para garantizar que el orden de clasificación de índices de Elasticsearch ahora respeta el orden de clasificación habilitado por el administrador. Anteriormente, los productos configurables y sus productos secundarios no se movían al final de la lista cuando esta configuración estaba habilitada.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-308-->El correo electrónico de la orden de compra ahora respeta la configuración de envío de correo electrónico de cada sitio web en una implementación de varios sitios. Se agregó una comprobación para la configuración **[!UICONTROL Disable Email Communications]** a la lógica personalizada para colas de correo electrónico. Anteriormente, Adobe Commerce no respetaba la configuración de envío de correo electrónico del sitio web secundario.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-302-->El título del campo SKU de la página de pedido rápido se ha cambiado para mayor claridad.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-543-->Adobe Commerce ahora muestra un mensaje de error más informativo cuando un comprador introduce un SKU no válido en el campo **Introducir SKU o nombre del producto**.

![Problema corregido](../assets/fix.svg) <!--- ACP2E-1753-->El campo **[!UICONTROL Account Created in]** de un administrador de empresa ahora conserva su valor como se espera después de guardar la empresa.

![Problema corregido](../assets/fix.svg) <!--- ACP2E-722 -->La consulta `customer` ya no devuelve resultados vacíos cuando recupera listas de solicitudes filtradas por `uid`.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-210 -->Se ha agregado un complemento antes de la llamada a `collectQuoteTotals` para garantizar que los créditos de la tienda se apliquen solo una vez.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-665 -->Ahora se redirige a los clientes a la página de inicio de sesión cuando un administrador elimina su cuenta del Administrador. Anteriormente, Adobe Commerce arrojaba un error. El bloque de código del complemento (`SessionPlugin`) está ahora dentro del bloque `try…catch`. Anteriormente, este código no se agrupaba dentro del bloque genérico de control de excepciones.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-661 --> En la página Pedido rápido en el modo móvil, al presionar **Intro** después de escribir un nombre de producto o SKU válido, ahora el comprador pasa al siguiente campo según lo esperado.

![Problema corregido](../assets/fix.svg) <!--- ACP2E-607 -->El nombre de la compañía ahora está visible como se espera en las secciones de facturación y dirección de envío del flujo de trabajo de cierre de compra.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-375 -->El crédito de la tienda no está disponible cuando el método de pago **[!UICONTROL Zero Subtotal Checkout]** está deshabilitado. Anteriormente, la casilla de verificación de crédito de tienda no funcionaba durante la realización del pedido desde el administrador. La aplicación no realizó el pedido con el crédito de la tienda y mostró este error: `The requested Payment Method is not available`.

## B2B v1.3.3

*9 de agosto de 2022*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevo](../assets/new.svg) agregó compatibilidad con Adobe Commerce 2.4.4.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-41985--> El tiempo necesario para actualizar de Adobe Commerce 2.3.x a Adobe Commerce 2.4.x en implementaciones con más de 100 000 roles de compañía se ha reducido sustancialmente.

![Problema corregido](../assets/fix.svg) <!--- MC-42153--> La solicitud del POST `V1/order/:orderId/invoice` ahora admite la creación de facturas parciales cuando el método de pago **[!UICONTROL Payment on Account]** está habilitado. Anteriormente, Adobe Commerce arrojó este error: `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`. [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![Problema corregido](../assets/fix.svg) <!--- MC-41975--> PayPal Payflow Pro ahora funciona como se espera con un presupuesto negociable B2B cuando el carro de compras del cliente contiene otros productos. Adobe Commerce ahora procesa correctamente el pedido y envía un correo electrónico al cliente según lo esperado. Anteriormente, Adobe Commerce arrojaba un error grave y enviaba un correo electrónico de confirmación al cliente que contenía valores cero.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-41819--> La paginación ahora se muestra correctamente en la página de resultados de búsqueda del catálogo después de excluir algunos productos del catálogo compartido.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-42886--> Los atributos personalizados del cliente ahora se guardan según lo esperado al crear o guardar un usuario de la empresa en el Administrador.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-42927--> El botón **[!UICONTROL Submit]** del formulario Crear nueva compañía ahora está deshabilitado después de un clic para evitar que se envíen varios formularios. Anteriormente, se podía enviar este formulario varias veces haciendo clic en este botón repetidamente, lo que generaba un error.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-42787-->: Adobe Commerce ya no muestra el vínculo de reordenar en la tienda cuando un comprador inicia sesión en una tienda para la cual se han deshabilitado los repedidos.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-43115--> La búsqueda rápida de pedidos por SKU ahora no distingue entre mayúsculas y minúsculas cuando el catálogo compartido está habilitado.

![Problema corregido](../assets/fix.svg) <!--- MC-42203--> Ahora puede actualizar un archivo para un atributo de cliente al crear una compañía. Anteriormente, cuando intentaba crear una compañía con datos adjuntos de tipo `File`, Adobe Commerce no creaba la compañía y registraba este error en el registro de excepciones: `Something went wrong while saving file`.

![Problema corregido](../assets/fix.svg) <!--- MC-42242--> Ahora puede crear una compañía con una cuenta de cliente que tenga un atributo personalizado con un tipo (`File`) o (`Image`). Anteriormente, si la cuenta tenía una de estas opciones personalizables, el cargador de página de edición de la compañía no se resolvía, lo que impedía editar los detalles de la compañía.

![Problema corregido](../assets/fix.svg) <!--- MC-42268--> La consulta `products` ahora devuelve un campo `total_count` preciso cuando el catálogo compartido está habilitado.

![Problema corregido](../assets/fix.svg) <!--- MC-42203--> Ahora puede actualizar un archivo para un atributo de cliente al crear una compañía. Anteriormente, cuando intentaba crear una compañía con datos adjuntos de tipo `File`, Adobe Commerce no creaba la compañía y registraba este error en el registro de excepciones: `Something went wrong while saving file`.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-43178--> Las páginas de _Configuración de la empresa_ y _Crear empresa_ ahora funcionan según lo esperado después de deshabilitar un método de envío en línea. Se ha añadido la verificación para evitar el intento de procesamiento de los módulos de envío desactivados. Anteriormente, Adobe Commerce mostraba este error: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-42214-->: la página _Categoría_ muestra ahora datos de productos coherentes mientras se generan permisos durante la indexación parcial. Se ha agregado un nuevo indizador parcial para permisos de directorio a este proceso. Anteriormente, los datos mostrados mientras se ejecutaba el indizador eran incorrectos.

![Problema corregido](../assets/fix.svg) <!--- MC-42567-->: la consulta `categoryList` devuelve ahora el número correcto de productos cuando se utilizan permisos de catálogo y se asignan productos a un catálogo compartido.

![Problema corregido](../assets/fix.svg) <!--- MC-42528-->: la consulta `categoryList` ahora respeta los permisos de categoría y devuelve solo las categorías permitidas. Anteriormente, devolvía todas las categorías asignadas y no asignadas.

![Problema corregido](../assets/fix.svg) <!--- MC-42399--> La solicitud `rest/V1/company/{id}` ahora devuelve `is_purchase_order_enabled` valores de atributo según lo esperado.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-128--> Ahora los atributos personalizados del cliente se muestran según lo esperado en la ficha _Administrador de la empresa_.

![Problema corregido](../assets/fix.svg) <!--- ACP2E-130--> El bloque Mi lista de deseos de la página Mi cuenta ahora se muestra según lo esperado para Administradores de la compañía y Usuarios de la compañía.

![Se corrigió un problema](../assets/fix.svg) <!--- ACP2E-133--> Los errores de pedidos rápidos ya no se muestran en el carro de compras. Anteriormente, Adobe Commerce mostraba este error en el carro de compras cuando no se encontraba el SKU en el catálogo: `The SKU was not found in the catalog`.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-194--> Las operaciones de guardado del catálogo compartido se han optimizado para ejecutarse más rápido. Anteriormente, guardar un catálogo compartido con muchos grupos de clientes podía tardar varios minutos.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-42240-->: Adobe Commerce ahora elimina todos los permisos de subcategoría de la tabla `sharedcatalog_category_permissions` cuando se elimina la categoría principal. Anteriormente, solo se eliminaban los datos de la categoría principal.

## B2B v1.3.2

*29 de agosto de 2022*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevo](../assets/new.svg) agregó compatibilidad con Adobe Commerce 2.4.3.

![Problema corregido](../assets/fix.svg) <!--- MC-39862--> Adobe Commerce ahora envía correctamente correos electrónicos de actualización sobre presupuestos negociables vencidos. Anteriormente, cuando caducaba una cotización negociable, Adobe Commerce no enviaba correos electrónicos de actualización.

![Se ha corregido el problema](../assets/fix.svg) <!--- MC-40682--> Adobe Commerce ahora envía correctamente correos electrónicos de actualización sobre las ofertas negociables caducadas y que caducan pronto cuando falta un trabajo de `cron`.

### Compañía

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-41542--> El campo desplegable Crear nueva página de cuenta de compañía por país ya no enumera valores de opción vacíos. Anteriormente, los dos primeros valores de opción y el código de país `AN` estaban vacíos.

![Problema corregido](../assets/fix.svg) <!--- MC-41260--> Al hacer clic en el botón **[!UICONTROL Return]** para un pedido creado por un usuario de la compañía, ahora se redirige a un usuario administrativo a la página Crear devolución según lo esperado. Anteriormente, se redirigía al administrador a la página Historial de pedidos.

![Se corrigió un problema](../assets/fix.svg) <!--- MC-40798--> Adobe Commerce ya no produce un error de memoria insuficiente al ejecutar el método `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` durante `bin/magento setup:upgrade`. Anteriormente, Adobe Commerce no utilizaba el tamaño del lote para la colección al inicializar los permisos, sino que cargaba una colección de todas las funciones de la empresa.

![Problema corregido](../assets/fix.svg) <!--- MC-40551--> Los usuarios de la compañía ahora pueden editar y actualizar los valores de atributos personalizados del cliente. Anteriormente, estos atributos no se enlazaban correctamente con el formulario de usuario de creación y edición. Un usuario de la empresa podía introducir valores de atributo diferentes, pero Adobe Commerce no los guardaba correctamente.

![Problema corregido](../assets/fix.svg) <!--- MC-32653--> El árbol de recursos para los permisos de funciones de la compañía ahora se puede traducir según lo esperado. Anteriormente, el árbol de permisos no se traducía aunque hubiera archivos de traducción válidos.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-40358-->: Adobe Commerce ahora guarda los valores de atributos del cliente personalizados para los usuarios de B2B según lo esperado. Anteriormente, al crear una cuenta de empresa que contenía atributos de cliente personalizados se activaba un error de plantilla y Adobe Commerce no cargaba el formulario correctamente. Agregar un argumento al diseño de `company_create_account` resolvió este problema.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-41721--> Los filtros de usuario de la compañía, como Mostrar todos los usuarios, Mostrar usuarios activos y Mostrar usuarios inactivos, ahora funcionan según lo esperado. Anteriormente, el filtrado de acciones en la página de usuario de la empresa provocaba un error de JavaScript.

### Crédito de empresa

![Problema corregido](../assets/fix.svg) <!--- MC-41551--> Los administradores con cuentas restringidas que solo incluyen privilegios de nivel de sitio web ahora pueden crear una compañía que utilice una moneda diferente a la del sitio web.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-41523--> Adobe Commerce ahora envía correos electrónicos de la empresa desde la dirección de correo electrónico y el ámbito correctos de `from`. Anteriormente, Adobe Commerce no tenía en cuenta el ámbito del sitio web al enviar una asignación de crédito de empresa o actualizar un correo electrónico.

### Pedido rápido

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-42104-->: la creación de un pedido mediante el uso de un pedido rápido a partir de un archivo CSV ahora funciona como se espera con SKU que no existen.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-40268-->. Ahora, el uso de un pedido rápido para buscar en varios SKU funciona según lo esperado. Anteriormente, los resultados incluían entradas duplicadas.

![Problema corregido](../assets/fix.svg) <!--- MC-40261--> La visualización de la lista de productos agregados ahora trata los SKU escritos en minúsculas y mayúsculas de la misma manera cuando se usan SKU para seleccionar varios productos durante el pedido rápido.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-40225-->. Ahora, al usar el pedido rápido, se agregan productos en la cantidad especificada por el comprador. Anteriormente, Adobe Commerce agregaba un solo producto incluso cuando las cantidades especificadas por el comprador superaban uno.

![Problema corregido](../assets/fix.svg) <!--- MC-41283-->: la función de autocompletar pedidos rápidos ahora funciona con SKU parciales.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-41299--> Adobe Commerce ahora muestra los productos que se han configurado como **No visibles por separado** en la lista de sugerencias automáticas y los resultados de búsqueda de la página Pedido rápido.

![Problema corregido](../assets/fix.svg) <!--- MC-42402--> Los compradores ahora pueden usar el formulario de pedido rápido para agregar varios productos por SKU que incluyan caracteres en mayúsculas. Anteriormente, solo se añadía el primer producto.

### Cotización negociable

![Problema corregido](../assets/fix.svg) <!--- MC-41232--> Ahora se redirige a los compradores a la página de presupuesto negociable después de pegar el vínculo a un presupuesto negociable en el campo URL e iniciar sesión correctamente. Anteriormente, los compradores se redirigían a la página Mi cuenta.

![Problema corregido](../assets/fix.svg) <!--- MC-39317--> La reordenación ahora funciona según lo esperado para pedidos que contienen un producto con una opción personalizable de fecha para una cuenta de cliente que se creó durante el cierre de compra. Anteriormente, Adobe Commerce no procesaba la reordenación y mostraba este error: `The product has required options. Enter the options and try again`.

![Problema corregido](../assets/fix.svg) <!--- MC-39063--> La dirección de envío de una oferta negociable ya no se puede editar durante el cierre de compra cuando el módulo de pedidos de compra está deshabilitado. Este comportamiento resultó de una corrección anterior en la que `isQuoteAddressLocked` se quitó del procesador de cierre de compra de presupuesto negociable.

![Problema corregido](../assets/fix.svg) <!--- MC-38967--> Los comerciantes ahora pueden agregar productos a una cotización negociable del administrador.

### Pedidos de compra

![Problema corregido](../assets/fix.svg) <!--- MC-39983--> Adobe Commerce ahora muestra un mensaje de error informativo como se espera cuando se realiza un pedido de compra mediante Pago y envío rápido de PayPal cuando el atributo **[!UICONTROL Name Prefix]** está establecido en `required`. Anteriormente, Adobe Commerce no realizaba el pedido ni mostraba un mensaje de error.

![Problema corregido](../assets/fix.svg) <!--- MC-39620-->: el componente de la interfaz de usuario para la dirección de facturación en el módulo de pedidos de compra ahora utiliza la dirección de oferta correctamente cuando Google Tag Manager está habilitado. Anteriormente, se producía un error de JavaScript en la página de pago.

### Listas de solicitudes

![Problema corregido](../assets/fix.svg) <!--- MC-40426--> Los comerciantes ahora pueden usar el extremo del POST `rest/all/V1/requisition_lists` para crear una lista de solicitudes para un cliente. Anteriormente, Adobe Commerce arrojaba este error 400 al intentar crear una lista de solicitudes: `Could not save Requisition List`.

![Problema corregido](../assets/fix.svg) <!--- MC-41123--> El botón **[!UICONTROL Add to Requisition List]** aparece ahora para los productos en stock de un carro de compras cuando el carro también contiene productos sin existencias. Anteriormente, si un carro de compras contenía dos productos, uno de los cuales estaba agotado, el botón _[!UICONTROL Add to Requisition List]_no aparecía en ninguno de los productos.

![Problema corregido](../assets/fix.svg) <!--- MC-40877--> Ahora puede usar la API de REST para agregar un producto a una lista de solicitudes.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-40155--> Los valores de la lista de solicitudes **[!UICONTROL Latest Activity Date]** ahora se adhieren al formato de configuración regional.

![Problema corregido](../assets/fix.svg) <!--- MC-39580--> Adobe Commerce ya no genera un error grave al editar un producto agrupado de una lista de solicitudes.

![Problema corregido](../assets/fix.svg) <!--- MC-40454--> Adobe Commerce ahora muestra el precio de producto correcto cuando agrega un producto con una opción personalizable `(File)` a una lista de deseos desde una lista de solicitudes. El vínculo al archivo cargado también es visible como se espera. Anteriormente, Adobe Commerce mostraba precios de productos incorrectos y no mostraba el vínculo al archivo.

![Problema corregido](../assets/fix.svg) <!--- MC-36383--> Los productos con una opción personalizable `(File)` ahora se pueden agregar a un carro de compras desde una lista de solicitudes.

### Catálogo compartido

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-40497-->: un administrador con una función limitada a un sitio web específico ahora puede crear, ver y editar un catálogo compartido. Anteriormente, Adobe Commerce arrojaba un error grave cuando un administrador con una función limitada intentaba crear un catálogo compartido.

![Problema corregido](../assets/fix.svg) <!--- MC-41337--> Los resultados de navegación por capas ahora incluyen un recuento preciso de productos con atributos filtrados, y los compradores ahora pueden aplicar varios filtros. Anteriormente, solo se podía aplicar un filtro y Adobe Commerce mostraba un recuento de productos impreciso en la navegación por capas.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-40779-->: Adobe Commerce ahora muestra correctamente los recuentos de productos en los filtros de navegación por capas en los resultados de búsqueda. Anteriormente, un complemento para la página de resultados de búsqueda no utilizaba el Elasticsearch, sino que enviaba una nueva consulta a la base de datos.

![Problema corregido](../assets/fix.svg) <!--- MC-39978--> Adobe Commerce ya no elimina los precios de nivel cuando un comerciante elimina todos los productos de un catálogo compartido predeterminado.

![Problema corregido](../assets/fix.svg) <!--- MC-39802--> Los filtros ahora se filtran por la categoría actual y se muestran correctamente en todas las páginas cuando los catálogos compartidos están habilitados. Anteriormente, los filtros se calculaban incorrectamente solo para la página actual y no se filtraban por la categoría actual.

![Problema corregido](../assets/fix.svg) <!--- MC-39522-->: la consulta de GraphQL `products` ya no devuelve el rango de precios y la categoría de un producto para los productos que no están asignados a un catálogo compartido cuando el catálogo compartido está habilitado. Anteriormente, la consulta devolvía las agregaciones del producto, aunque el producto en sí no se devolvía en la matriz `items`.

## B2B v1.3.1

*9 de febrero de 2021*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevo](../assets/new.svg) agregó compatibilidad con Adobe Commerce 2.4.2.

![Nuevos](../assets/new.svg) métodos de pago en línea ahora son compatibles con los pedidos de compra.

![Se ha solucionado un problema](../assets/fix.svg) La adición de un producto configurable al carro de compras directamente desde una lista de solicitudes cuando este producto se utilizaba en un pedido anterior ya no devuelve un error del sistema.

![Problema corregido](../assets/fix.svg) Adobe Commerce ahora muestra correctamente la pestaña Requiere mi aprobación para los pedidos de compra cuando se implementa una configuración de base de datos dividida.

![Problema corregido](../assets/fix.svg) Adobe Commerce ahora muestra detalles acerca de los productos agrupados y la tarjeta regalo al ver los pedidos de compra.

![Problema corregido](../assets/fix.svg): ahora se redirige a los compradores como se espera después de iniciar sesión en su cuenta mientras navegan en una tienda donde **[!UICONTROL Website Restriction]** está habilitado y **[!UICONTROL Restriction Mode]** está establecido en `Private Sales: Login Only`. Anteriormente, los compradores se redirigían a la página principal de la tienda. <!--- MC-38934-->

![Problema corregido](../assets/fix.svg) El historial de pedidos ahora se carga según lo esperado en la página del panel de cuentas del administrador de una empresa en implementaciones con una jerarquía empresarial B2B que contiene muchos clientes (más de 13000). Anteriormente, el historial de pedidos se cargaba lentamente o no se cargaba, y Adobe Commerce mostraba un error 503. <!--- MC-38830-->

![Problema corregido](../assets/fix.svg) Adobe Commerce ya no muestra varios mensajes de advertencia idénticos cuando agrega un producto no configurado con opciones personalizables a una Lista de solicitudes desde una página Categoría. <!--- MC-38342-->

![Se ha corregido un problema](../assets/fix.svg) Los productos nuevos y duplicados ahora están visibles como se esperaba en la página de categoría cuando los catálogos compartidos B2B están habilitados. <!--- MC-38307-->

![Se ha corregido un problema](../assets/fix.svg) Adobe Commerce ahora mantiene el `store_id` correcto que está asociado con un administrador de la empresa cuando se actualiza el grupo de clientes de una empresa. Anteriormente, `store_id` se cambió al almacén predeterminado cuando se actualizó el grupo. <!--- MC-38196-->

![Problema corregido](../assets/fix.svg) Adobe Commerce ahora guarda un producto agrupado en una lista de solicitudes como una lista de productos simples de la misma manera que agrega un producto agrupado a un carro de compras. Anteriormente, debido a cómo Adobe Commerce guardaba los productos agrupados, el vínculo de un producto agrupado de la lista de solicitudes siempre se redirigía a productos simples y no al producto agrupado. <!--- MC-38049-->

![Problema corregido](../assets/fix.svg) Ahora puede filtrar pedidos por el campo **[!UICONTROL Company Name]** al exportar información de pedidos en formato CSV. Anteriormente, Adobe Commerce registró un error en `var/export/{file-id}`. <!--- MC-37785-->

![Se ha corregido un problema](../assets/fix.svg). Adobe Commerce ahora muestra la ventana emergente Crear lista de solicitudes como se esperaba al seleccionar la pestaña Crear nueva lista de solicitudes en la tienda. <!--- MC-37915-->

![Problema corregido](../assets/fix.svg) Las listas de solicitudes ahora incluyen todos los productos agrupados y las cantidades que se han agregado a la lista. Anteriormente, cuando un comerciante navegaba a una lista de solicitudes después de agregarle productos desde una página de detalles de producto, Adobe Commerce mostraba este error: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

![Se ha corregido un problema](../assets/fix.svg): la vista de tienda correcta ahora está asociada al sitio web relevante cuando crea una compañía en una implementación de varios sitios. Anteriormente, no se podía crear una compañía y Adobe Commerce mostraba este error: `The store view is not in the associated website`. <!--- MC-37488-->

![Se ha corregido un problema](../assets/fix.svg). Ya no es posible duplicar cantidades de productos en el archivo CSV si se solicitan productos por SKU mediante un pedido rápido. <!--- MC-37427-->

![Problema corregido](../assets/fix.svg): el botón **[!UICONTROL Add to Cart]** ya no está bloqueado cuando la sección _[!UICONTROL Enter Multiple SKUs]_de la página Pedido rápido contiene un valor vacío. Ahora, Adobe Commerce muestra un mensaje en el que se le solicita que introduzca SKU válidas. <!--- MC-37387-->

![Problema corregido](../assets/fix.svg) Adobe Commerce ahora muestra este mensaje en la página del producto cuando envía una revisión de producto desde una lista de solicitudes: `You submitted your review for moderation`. La revisión también aparece en la página Revisiones pendientes (Administración **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**). Anteriormente, aunque Adobe Commerce agregaba la revisión a la lista de revisiones pendientes, generaba un error 404 en la página del producto. <!--- MC-37119-->

![Se ha corregido un problema](../assets/fix.svg). Se ha mejorado el rendimiento del consumidor `sharedCatalogUpdateCategoryPermissions`. Después de crear un catálogo compartido, el indexador de permisos de catálogo ahora utiliza solo el ID de grupo de clientes del catálogo compartido, no todos los grupos de clientes. <!--- MC-36770-->

![Se ha corregido un problema](../assets/fix.svg). Los campos de atributos personalizados de dirección de cliente asociados con una dirección no predeterminada de comprador ahora se guardan según lo esperado en el flujo de trabajo de cierre de compra de la tienda. <!--- MC-36630-->

![Se ha corregido un problema](../assets/fix.svg). Los pedidos de productos que pertenecen al catálogo compartido predeterminado de una tienda ahora se pueden realizar para compradores a través de la API de REST de administración (`rest/V1/carts/{<CART_ID>/items`) según lo esperado. Adobe Commerce ahora comprueba si el producto se asignó a un catálogo público antes de la validación de los permisos del catálogo compartido en `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave`. Anteriormente, Adobe Commerce no agregaba el producto al carro de compras y arrojaba este error: `No such shared catalog entity`. <!--- MC-36535-->

![Se ha corregido un problema](../assets/fix.svg). Adobe Commerce ahora envía nuevos correos electrónicos de registro de usuarios de la empresa desde la dirección de la tienda Adobe Commerce. Anteriormente, este correo electrónico se enviaba desde la dirección del administrador de la empresa. <!--- MC-36480-->

![Se ha corregido un problema](../assets/fix.svg). Adobe Commerce ahora comprueba los atributos personalizados para la duplicación de nombres de atributos de empresa reservados antes de permitir que un comerciante guarde un nuevo atributo. <!--- MC-36282-->

![Problema corregido](../assets/fix.svg): la consulta `credit_history` ahora devuelve el historial de crédito de la compañía especificada tanto para el importe asignado originalmente como para el importe comprado. Anteriormente, esta consulta devolvía un error.

![Se ha corregido un problema](../assets/fix.svg) Los campos **[!UICONTROL Company]** y **[!UICONTROL Job Title]** de la página Editar información de cuenta ya no se pueden editar.

### Problemas conocidos

- Los compradores de B2B pueden utilizar métodos de pago en línea para evitar el flujo habitual de órdenes de compra. Este escenario se puede producir si el comprador puede reducir todo el total del pago a un 0 (por ejemplo, mediante un código de promoción o una tarjeta regalo) y, a continuación, eliminar el código o la tarjeta regalo. Incluso en estas condiciones, Adobe Commerce sigue realizando el pedido de la cantidad correcta en función de los precios de los artículos en el catálogo asignado. **_Solución alternativa_**: deshabilita las tarjetas regalo y los códigos de cupones cuando los métodos de pago en línea estén habilitados para la aprobación de pedidos de compra. <!--- B2B-1603-->

- Se redirige a los compradores al carro de compras al intentar realizar un pedido a partir de un pedido de compra mediante Pago y envío exprés de PayPal cuando se deshabilita **[!UICONTROL In-Context Mode]**. <!--- B2B-1604-->

- Adobe Commerce a veces muestra un error 404 cuando un comprador crea un pedido y luego navega a la página de pago. Este error se produce cuando un comprador ha creado previamente un pedido de compra diferente con un método de pago en línea antes de navegar a la página de pago sin completar la compra anterior. El comprador aún puede realizar el pedido de compra. **_Trabajar_**: Ninguno. <!--- B2B-1605-->

- Los descuentos de un método de pago concreto persisten durante el proceso de pago de un pedido de compra, incluso cuando el comprador cambia su método de pago durante el proceso de pago final. Como resultado, los clientes pueden recibir un descuento al que no tienen derecho. Este problema se produce porque una regla de carro de compras para el método de pago original se sigue aplicando a pesar del cambio en el método de pago. **_Trabajar_**: Ninguno. Ver el problema conocido de [Adobe Commerce 2.4.2 B2B: queda descuento para pedidos de compra en línea después de cambiar el método de pago](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html) artículo de _Knowledge Base_. <!-- B2B-1012 -->

- La consulta `deleteRequisitionListOutput` devuelve detalles sobre la lista de solicitudes eliminada en lugar de las listas de solicitudes restantes. <!--- MC-39894-->

## B2B v1.3.0

*15 de octubre de 2020*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

Esta versión incluye mejoras en las aprobaciones de pedidos, los métodos de envío, el carro de compras y el registro de acciones del administrador.

![Nuevo](../assets/new.svg) agregó compatibilidad con Adobe Commerce 2.4.1.

![Nuevas](../assets/new.svg) aprobaciones de pedidos B2B se han mejorado para mejorar la usabilidad y permitir acciones masivas en pedidos de compra.

![Los nuevos](../assets/new.svg) comerciantes B2B ahora pueden controlar los métodos de envío que se ofrecen a cada compañía.<!--- BUNDLE-160 161 162 -->

![Los comerciantes nuevos](../assets/new.svg) ahora pueden permitir que los usuarios borren el contenido de su carro de compras en una sola acción y pueden configurar esta capacidad de forma independiente en cada sitio web <!--- BUNDLE-108 -->

![Nuevos](../assets/new.svg) compradores B2B ahora pueden agregar artículos individuales o todo el contenido de su carro de compras directamente a una lista de solicitudes. <!--- BUNDLE-145 144-->

![Nuevos](../assets/new.svg) comerciantes B2B pueden crear pedidos del administrador en nombre de clientes usando Pago a cuenta como método de pago. <!--- BUNDLE-166 178-->

![Nuevos](../assets/new.svg) comerciantes ahora pueden ver directamente todas las ofertas asociadas con un usuario desde la página de detalles del cliente. <!--- BUNDLE-139 -->

![Nuevos](../assets/new.svg) comerciantes ahora pueden filtrar la cuadrícula Clientes ahora en línea por Compañía. <!--- BUNDLE-137 -->

![Nuevos](../assets/new.svg) administradores ahora pueden filtrar clientes en el Administrador por representante de ventas. <!--- BUNDLE-110 -->

![Nuevo](../assets/new.svg) Para reducir la creación de cuentas fraudulentas o de correo no deseado, los comerciantes ahora pueden habilitar Google reCAPTCHA en el formulario de nueva solicitud de la empresa que se encuentra en la tienda. <!--- BUNDLE-154 -->

![Las nuevas](../assets/new.svg) acciones de administración realizadas en los módulos de la compañía ahora se registran en el registro de acciones de administración. Las acciones se registran desde todos los módulos relevantes de la compañía: `Company`, `NegotiableQuote`, `CompanyCredit`, `SharedCatalog`. <!--- BUNDLE-180 181 182 183 -->

![Se ha corregido un problema](../assets/fix.svg): Adobe Commerce ya no muestra el botón **[!UICONTROL Delete customer]** en la página **Clientes** cuando el administrador que ha iniciado sesión no tiene derechos para eliminar clientes en implementaciones en las que B2B está instalado. <!--- MC-35655-->

![Problema corregido](../assets/fix.svg) El grupo de clientes ya no cambia automáticamente para un cliente asignado a una compañía cuando edita el cliente en la cuadrícula Cliente. <!--- MC-35254-->

![Se ha corregido un problema](../assets/fix.svg) Cuando un comerciante crea un catálogo compartido, los permisos ahora se establecen automáticamente en `Allow` para las características de **[!UICONTROL Display Product Prices]** y **[!UICONTROL Add to Cart]** en categorías cuando al grupo de clientes se le asigna este acceso en la configuración de permisos de catálogo. Anteriormente, esta configuración se establecía automáticamente en `Deny` incluso cuando los permisos de catálogo se establecían en `Allow`.<!--- MC-34792-->

![Se ha corregido un problema](../assets/fix.svg). Los permisos de la categoría de catálogo compartido ya no se sobrescriben cuando se edita un producto desde la página de edición del producto.<!--- MC-34777-->

![Problema corregido](../assets/fix.svg) Adobe Commerce ahora envía una notificación por correo electrónico confirmando que un cliente tiene permiso para exceder el límite de crédito designado cuando un comerciante habilita la configuración **[!UICONTROL Allow To Exceed Credit Limit]**. Anteriormente, el correo electrónico de notificación enviado por Adobe Commerce indicaba que el cliente no tenía permiso para superar el límite. <!--- MC-34584-->

![Problema corregido](../assets/fix.svg) El contenedor de HTML que rodea el precio del producto en las listas de solicitudes ahora se representa correctamente para los elementos secundarios de los productos agrupados. <!--- MC-36331-->

![Problema corregido](../assets/fix.svg) Los comerciantes ahora pueden designar el idioma en el que se enviará el correo electrónico de usuario de la compañía al crear una compañía en implementaciones en varios idiomas. Anteriormente, el menú desplegable permitía a los comerciantes seleccionar la vista de tienda e idioma adecuados para que no se mostraran.  <!--- MC-35777-->

![Problema corregido](../assets/fix.svg) Los campos de atributos de dirección de cliente personalizados ahora se muestran según lo esperado en el flujo de trabajo de cierre de compra de la tienda. <!--- MC-35607-->

![Problema corregido](../assets/fix.svg): la pestaña de configuración de características B2B ahora se abre correctamente. <!--- MC-35458-->Los invitados ahora pueden usar QuickOrder para agregar productos al carro de compras y, a continuación, quitar artículos correctamente. Anteriormente, cuando un comprador utilizaba QuickOrder para agregar varios productos al carro de compras y, a continuación, eliminaba un producto, el producto no se eliminaba. <!--- MC-35327-->

![Se ha corregido un problema](../assets/fix.svg) Ahora se puede actualizar una compañía mediante la solicitud de PUT de API de REST `/V1/company/:companyId` sin especificar `region_id` cuando el estado se configura como **no obligatorio**. Anteriormente, aunque `region_id` no era obligatorio, Adobe Commerce arrojaba un error si no se especificaba. <!--- MC-35304-->

![Se ha corregido un problema](../assets/fix.svg) Cuando crea o actualiza una compañía B2B mediante la API de REST (`http://magento.local/rest/V1/company/2`, donde `2` representa el identificador de la compañía), la respuesta ahora incluye la configuración de `applicable_payment_method` o `available_payment_methods` según lo esperado. <!--- MC-35248-->

![Problema corregido](../assets/fix.svg) Adobe Commerce ya no muestra una página 404 cuando un comerciante usa el botón **Introducir** en lugar de hacer clic en el botón **[!UICONTROL Save]** al crear una lista de solicitudes en la tienda.<!--- MC-35094-->

![Se ha corregido un problema](../assets/fix.svg) Los permisos de categoría ya no cambian cuando se asigna un nuevo producto a un catálogo compartido público. Anteriormente, los permisos de categoría estaban duplicados. <!--- MC-34386-->

![Se ha corregido un problema](../assets/fix.svg) El PUT de extremo de API de REST `rest/default/V1/company/{id}`, que se usa para actualizar el correo electrónico de la compañía, ya no distingue entre mayúsculas y minúsculas. <!--- MC-34308-->

![Se ha solucionado un problema](../assets/fix.svg). La desactivación de los módulos de recompensa ya no afecta a las funciones B2B de las cuentas de los clientes. Anteriormente, cuando se deshabilitaban los módulos de recompensa, no se mostraban las siguientes fichas relacionadas con B2B: Perfil de compañía, Usuarios de compañía y Roles y permisos.<!--- MC-34191-->

![Se ha corregido un problema](../assets/fix.svg). Adobe Commerce ahora usa el nombre de remitente correcto en las notificaciones por correo electrónico cuando se realizan cambios en las cuentas de la empresa. Anteriormente, Adobe Commerce utilizaba el nombre general del remitente del contacto definido en el ámbito predeterminado para todos los correos electrónicos. <!--- MC-33917-->

![Problema corregido](../assets/fix.svg) Ahora puede implementar correctamente el envío múltiple para pedidos que contienen productos físicos y virtuales. <!--- MC-33818-->

![Problema corregido](../assets/fix.svg) Los comerciantes ahora pueden crear usuarios de la compañía desde la sección _[!UICONTROL Company Users]_en las páginas Mi cuenta y Estructura de la compañía cuando **[!UICONTROL Access Restriction]**está habilitado y **[!UICONTROL Restriction Mode]**está establecido en `Sales: Login Only`. Anteriormente, Adobe Commerce arrojaba este error cuando un comerciante intentaba crear un usuario: `Can not register new customer due to restrictions are enabled`. <!--- MC-33608-->

![Problema corregido](../assets/fix.svg) Adobe Commerce ya no restablece el grupo de clientes predeterminado de un cliente cuando un cliente guarda su información de cuenta. <!--- MC-33554-->

![Problema corregido](../assets/fix.svg) Adobe Commerce ya no genera un error grave cuando un administrador asigna un cliente que tiene un carro de compras activo a un grupo de clientes. <!--- MC-33313-->

![Problema corregido](../assets/fix.svg) Adobe Commerce ahora proporciona un evento de capa de datos `addToCart` para páginas de listas de pedidos rápidos y solicitudes.  <!--- MC-33295-->

![Se ha corregido un problema](../assets/fix.svg) Los mensajes de correo electrónico de notificación que se envían a los representantes de ventas asignados a una compañía ahora incluyen el logotipo corporativo asignado. Anteriormente, el correo electrónico de notificación incluía el logotipo predeterminado de LUMA, no el logotipo corporativo cargado. <!--- MC-33232-->

![Problema corregido](../assets/fix.svg) Una lista de solicitudes ahora incluye todos los productos agrupados y las cantidades que se han agregado a la lista. Anteriormente, cuando un comerciante navegaba a una lista de solicitudes después de agregarle productos desde una página de detalles de producto, Adobe Commerce mostraba este error: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![Problema corregido](../assets/fix.svg): la consulta `products` ahora devuelve un campo `total_count` preciso cuando el catálogo compartido está habilitado. <!--- MC-42268-->

![Problema corregido](../assets/fix.svg): las páginas Configuración de la empresa y Crear empresa ahora funcionan según lo esperado después de deshabilitar un método de envío en línea. Se ha añadido la verificación para evitar el intento de procesamiento de los módulos de envío desactivados. Anteriormente, Adobe Commerce mostraba este error: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`. <!--- MC-43178-->

![Se ha corregido un problema](../assets/fix.svg) El consumo de memoria de prueba de integración se ha reducido, lo que mejora el rendimiento de la prueba y reduce el tiempo necesario para completarla. <!--- AC-266-->

## B2B v1.2.0

*28 de julio de 2020*

[!BADGE Compatible]{type=Informative tooltip="Admitido"}

![Nuevo](../assets/new.svg) agregó compatibilidad con Adobe Commerce 2.4.0.

![Nueva](../assets/new.svg) búsqueda de pedidos de tiendas, con agradecimiento adicional por la contribución de Marek Mularczyk de [Divante](https://www.divante.com/) y miembros de la comunidad.

Se mejoraron y se volvieron a escribir ![nuevos](../assets/new.svg) pedidos de compra. Ahora se incluyen de forma predeterminada en Adobe Commerce.

![Se han implementado nuevas](../assets/new.svg) reglas de aprobación de pedidos de compra. Estas reglas permiten a los usuarios controlar el flujo de trabajo del pedido de compra mediante la creación de reglas de compra para los pedidos.

![Nuevo](../assets/new.svg) Iniciar sesión como cliente ahora se incluye de forma predeterminada en Adobe Commerce. Esta función permite a los empleados del sitio ayudar a los clientes iniciando sesión como clientes para ver lo que ven.

![Se ha corregido un problema](../assets/fix.svg). Las agregaciones de atributos ahora funcionan correctamente para la navegación por capas con el Elasticsearch

![Se ha solucionado un problema](../assets/fix.svg). La búsqueda de pedidos por caracteres especiales ya funciona correctamente.

![Problema corregido](../assets/fix.svg) Al hacer clic en el botón **[!UICONTROL Clear All]**, ahora se expanden todos los filtros, en lugar de contraerlos.

![Se ha corregido un problema](../assets/fix.svg) El SKU/nombre del producto ahora se incluye en el resumen del filtro de búsqueda Historial de pedidos.

![Problema corregido](../assets/fix.svg) El indicador de ordenación ahora se muestra correctamente en la cuadrícula Mis pedidos de compra.

![Problema corregido](../assets/fix.svg) Ahora, solo puede hacer clic una vez en los botones Aprobar, Cancelar, Rechazar y Pedido de compra. Anteriormente, se podía hacer clic en el botón varias veces.

![Problema corregido](../assets/fix.svg): los botones Aprobar, Rechazar, Cancelar y Validar de la orden de compra ahora se representan correctamente en dispositivos móviles.

![Problema corregido](../assets/fix.svg) Anteriormente, al aprobar un pedido de compra con un descuento que ha caducado, se colocaba el pedido en el importe total y no se actualizaba el total del pedido de compra. Ahora, el total del pedido de compra se actualiza para mostrar el total correcto.

![Problema corregido](../assets/fix.svg) Se introdujo un problema en la versión 2.3.4 donde los atributos de extensión personalizados no se copiaban de la dirección del cliente a la dirección del presupuesto. Este problema se ha corregido.

![Se ha corregido un problema](../assets/fix.svg). Con B2B instalado, aparecía un error SQL al asignar categorías a catálogos compartidos. Este problema se ha corregido.

![Se ha corregido un problema](../assets/fix.svg) Debido a un valor de tipo de variable incorrecto, los administradores no pudieron agregar productos configurables a un pedido. Los desplegables de opciones no se rellenaban. Esta función ahora funciona correctamente.

![Se ha corregido un problema](../assets/fix.svg) Anteriormente, al editar los permisos de categoría para el grupo Sin sesión iniciada, se producía un error al guardar los cambios. Este problema se ha corregido.

![Problema corregido](../assets/fix.svg) Se ha agregado una corrección para permitir a los administradores de tiendas agregar productos a un pedido que no se encuentra en el catálogo compartido. Anteriormente, aparecía un mensaje de error al añadir un elemento que no estaba en el catálogo.

![Se ha corregido un problema](../assets/fix.svg) Anteriormente, después de ejecutar el comando `php bin/magento indexer:set-dimensions-mode catalog_product_price website` y de intentar crear un catálogo compartido, se producía un error. Este problema se ha corregido.

![Se corrigió un problema](../assets/fix.svg) Al agregar una compañía y asignar el administrador de la compañía a un sitio web no predeterminado, se envió el identificador de sitio incorrecto, lo que provocó un error. Este problema se ha corregido.

![Se ha corregido un problema](../assets/fix.svg) Anteriormente, después de que un cliente se moviera a otro grupo de clientes, si agregaba un producto a un pedido mediante _Pedido rápido_ se producía un error. Este problema se ha corregido.

![Se ha corregido un problema](../assets/fix.svg) Anteriormente, al intentar realizar la desprotección con la API web con un presupuesto B2B, se enviaba un valor incorrecto a la API, lo que provocaba que se produjera un error. Este problema se ha corregido.

![Se corrigió un problema](../assets/fix.svg) Anteriormente, al configurar una compañía como &quot;Activa&quot; a través de la API, se producía un error. Este problema se ha corregido.

![Problema corregido](../assets/fix.svg) Debido a una etiqueta `form` innecesaria, la página de pedidos se actualizó automáticamente cuando presionó Intro después de cambiar un cargo de envío propuesto. Este problema se ha corregido.

![Se corrigió un problema](../assets/fix.svg) Anteriormente, al establecer un límite de visualización de productos en una página de catálogo y ese límite era menor que el número total de productos, se produjo un error. Esa función ahora funciona según lo esperado.

![Se ha corregido un problema](../assets/fix.svg) Anteriormente, al cambiar el administrador de una compañía, la dirección de administrador original se copiaba al nuevo administrador, proporcionándole dos direcciones. Ahora, solo se agrega la dirección correcta.

![Se ha corregido un problema](../assets/fix.svg) Anteriormente, el uso de la API para guardar un elemento de presupuesto cuando Git se establecía en &quot;Permitido y notificar al cliente&quot; fallaba. Esta llamada de API ahora funciona según lo esperado.

![Problema corregido](../assets/fix.svg): el impuesto sobre el producto corregido ahora se muestra en la página de detalles Ofertas.

![Problema corregido](../assets/fix.svg) Anteriormente, al hacer clic en un archivo adjunto en la ficha Comentarios de la página Mis comillas, no se podía descargar el archivo. Este comportamiento funciona ahora según lo esperado.

### Problemas conocidos

- Adobe Commerce genera una excepción durante la actualización a B2B 1.2.0 en una implementación de varios sitios web. Cuando se ejecuta `setup:upgrade`, este error se produce en el módulo `PurchaseOrder`: `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder`. **Solución alternativa**: instale la interfaz de `B2B-716 Add NonTransactionableInterface` en la revisión de revisión de datos de `InitPurchaseOrderSalesSequence`, que ahora está disponible en la sección **Mi cuenta** > **Descargas** de `magento.com`.
- Si un código de descuento caduca antes de que se apruebe un pedido de compra, el pedido sigue mostrando el importe descontado, pero una vez aprobado, el pedido se coloca en el total no descontado. **Solución alternativa**: instale la revisión `B2B-709 Purchase Order Discount patch` para este problema, que ahora está disponible en la sección **Mi cuenta** > **Descargas** de `magento.com`.
- Si los artículos de un pedido de compra están agotados, o tienen una cantidad insuficiente cuando el pedido de compra se convierte en un pedido real, se produce un error. Si los pedidos no satisfechos están activados, el pedido se procesa normalmente.
