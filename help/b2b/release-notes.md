---
title: '[!DNL Adobe Commerce B2B] notas de la versión'
description: Revise los Notas de la versión para obtener información sobre los cambios en [!DNL Adobe Commerce B2B] las versiones.
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: de145205e5fcdcb49ca7626b2666e82af102344f
workflow-type: tm+mt
source-wordcount: '8702'
ht-degree: 0%

---

# [!DNL Adobe Commerce B2B] Notas

Estos Notas de la versión para la extensión de B2B capturan adiciones y correcciones que Adobe Systems ha agregado durante un ciclo de lanzamiento, incluyendo:

![Nuevas](../assets/new.svg) nuevas características
![Se ha corregido un problema](../assets/fix.svg) Correcciones y mejoras
![Problema conocido](../assets/bug.svg) Problemas conocidos

>[!NOTE]
>
>Consulte [Disponibilidad del producto](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) para obtener información sobre las versiones de la extensión de Commerce B2B compatibles con las versiones de Adobe Commerce disponibles.

## B2B 1.5.2

*8 de abril de 2025*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} versiones de parches de seguridad de Adobe Commerce 2.4.8, 2.4.7-p5 y 2.4.6-p10.
Compatible con Adobe Commerce versiones 2.4.7 a 2.4.7-p4, 2.4.6 a 2.4.6-p9

La versión B2B v1.5.2 incluye mejoras de calidad y correcciones de errores.

### Administración de la empresa

![Los nuevos](../assets/new.svg)<!-- B2B-4123 -->administradores ahora pueden administrar varias compañías desde una sola cuenta usando el conmutador de compañías de tienda. Las ventajas principales incluyen:

- **Administración simplificada de varias compañías**: los administradores ahora pueden supervisar varias compañías desde una cuenta de usuario, lo que elimina la necesidad de crear y administrar inicios de sesión independientes para cada compañía.
- **Cambio de empresa eficiente**: una interfaz intuitiva permite a los administradores cambiar rápidamente entre empresas y realizar actualizaciones, lo que mejora la productividad al administrar varias entidades.
- **Operaciones optimizadas**: los gerentes regionales y los líderes empresariales pueden administrar de manera centralizada todas sus compañías, lo que permite una toma de decisiones más rápida y operaciones comerciales más fluidas.

Esta mejora se basa en la capacidad de pertenencia de varias empresas de B2B 1.5.0, que permitía a los usuarios pertenecer a varias empresas, pero no admitía el acceso de administrador entre empresas. El conmutador de empresa elimina la necesidad de tener cuentas de administrador independientes, a la vez que mantiene los controles de acceso adecuados y las vistas específicas de la empresa.

### Compañía

![Se ha solucionado un problema](../assets/fix.svg)<!-- B2B-4480 --> en el que los clientes invitados veían un mensaje de error de `No such entity with cartId = ?` al iniciar sesión como usuario de una empresa con productos en el carro de compras.

### Cotización negociable

![Problema corregido](../assets/fix.svg) La versión B2B v1.5.2 incluye las siguientes correcciones para presupuestos negociables:

- &#x200B;<!-- B2B-3252 -->El campo [!UICONTROL Line Item Discount Amount] ahora valida la entrada para evitar que se introduzcan valores de descuento negativos.
- &#x200B;<!-- B2B-3224 -->Se ha corregido un problema con la experiencia del usuario en el que las notas de elementos de línea larga se truncaban y eran difíciles de leer para los clientes B2B.
- &#x200B;<!-- B2B-2865 -->Los clientes B2B ahora pueden especificar cantidades de productos utilizando valores decimales (como 1,5 o 2,75) al crear presupuestos.

### Plantilla de presupuesto

![Nuevo](../assets/new.svg)<!-- B2B-4104 -->: nueva capacidad para que los compradores y vendedores de B2B adjunten vínculos de documentos externos a las plantillas de presupuesto. Esta función permite vincularse a documentos alojados en servicios como DocuSign y Adobe Sign directamente desde comillas, lo que complementa la capacidad de archivo adjunto existente. Las ventajas principales incluyen:

- Colaboración optimizada mediante el acceso directo a contratos y acuerdos críticos
- Transparencia mejorada con acceso instantáneo a la documentación más reciente
- Negociaciones de cotización más rápidas al eliminar la necesidad de descargar y cargar archivos
- Administración flexible de documentos mediante servicios de alojamiento de documentos externos

## B2B 1.5.1

*11 de febrero de 2025*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} versiones de parches de seguridad 2.4.7-p4+ y 2.4.6-p9+ de Adobe Commerce.
Compatible con las versiones de Adobe Commerce 2.4.8-beta1 a 2.4.8-beta2, 2.4.7 a 2.4.7-p3, 2.4.6 a 2.4.9-p8

La versión B2B v1.5.1 incluye mejoras de calidad y correcciones de errores.

### Compañía

![Problema corregido](../assets/fix.svg)<!-- B2B-4422 --> Si un cliente intenta cambiar de empresa en la página Detalles del presupuesto, el sistema ahora redirige al cliente a una página *Acceso denegado* para garantizar que un presupuesto creado para una empresa no se pueda usar para realizar un pedido con los precios de otra empresa. Anteriormente, un usuario podía crear una cotización con el precio de una compañía y luego cambiar a otra compañía para realizar un pedido con precios diferentes.

### Descuentos de artículo de línea

![Se corrigió un problema](../assets/fix.svg)<!-- B2B-2938 --> Se mejoró la eficiencia del sistema al abordar una degradación del rendimiento observada en el escenario de recálculo de presupuesto. Anteriormente, se agregaban dos nuevas entidades a cada elemento de línea de carro de compras, lo que provocaba un notable aumento en las solicitudes de base de datos, lo que producía un rendimiento más lento.

### Cotización negociable

![Se ha corregido un problema](../assets/fix.svg)<!-- B2B-3820 --> El sistema ahora mantiene la posición de los elementos de la interfaz de usuario cuando se aplica la validación de JavaScript a los campos *[!UICONTROL min/max qty]* de la página Plantilla de presupuesto de tienda de Luma. Anteriormente, la aplicación de la validación de JavaScript a estos campos provocaba que otros elementos de la interfaz de usuario de la página cambiaran.

### Carro de compras

![Se ha solucionado un problema](../assets/fix.svg)<!-- B2B-4222 -->. Se ha introducido un nuevo sistema de administración del carro de compras diseñado para optimizar la experiencia de compra de los usuarios que administran varias cuentas de compañía. El nuevo sistema asocia los carros de compras con empresas individuales, en lugar de con la cuenta del cliente, para optimizar la experiencia de compra y mejorar el flujo de trabajo mediante la compatibilidad con las siguientes capacidades.

- **Carros de compras específicos de la compañía:**: los carros de compras ahora están vinculados a compañías individuales para admitir precios y opciones de productos específicos de la compañía.
- **Conmutación sin problemas**: los usuarios pueden cambiar fácilmente entre distintas cuentas de compañía sin que el contenido del carro de compras de cada compañía se vea afectado.
- **Integridad contextual**: todos los detalles del carro de compras permanecen en el contexto de la compañía correspondiente, lo que proporciona una experiencia de compra coherente y confiable.

## B2B 1.5.0

*30 de octubre de 2024*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} versiones de parches de seguridad 2.4.7-p3+ y 2.4.6-p8+ de Adobe Commerce.
Compatible con Adobe Commerce versiones 2.4.8-beta1, 2.4.7 a 2.4.7-p2, 2.4.6 a 2.4.6-p7.

La versión 1.5.0 de Adobe Commerce B2B también es compatible con PHP 8.3 y admite [GraphQL Application Server](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).

La versión B2B v1.5.0 incluye nuevas funciones, mejoras de calidad y correcciones de errores.

>[!NOTE]
>
> Obtenga información sobre los cambios incompatibles con versiones anteriores (BIC) introducidos en la versión B2B 1.5.0 revisando los aspectos destacados y la información de referencia del tema [Cambios incompatibles con versiones anteriores](backward-incompatible-changes.md).

### Administración de empresa

![Nuevo](../assets/new.svg) **Administración de la compañía**<!--B2B-2901-->: los comerciantes ahora pueden ver y administrar las compañías de Adobe Commerce como organizaciones jerárquicas al asignar compañías a compañías principales designadas. Una vez asignada una compañía a una matriz, el administrador de la compañía matriz puede administrar la cuenta de la compañía. Solo los usuarios administradores autorizados pueden agregar y administrar asignaciones de la compañía. Para obtener más información, consulte [Administrar la jerarquía de la compañía](manage-company-hierarchy.md).

- Agregue y administre asignaciones de compañía desde la nueva sección *[!UICONTROL Company Hierarchy]* en la página *[!UICONTROL Company Account]* del Administrador.

- Ordenar y filtrar compañías por la nueva configuración de *[!UICONTROL Company Type]*. En la cuadrícula Compañías, la columna *[!UICONTROL Company Type]* indica si una compañía es una compañía individual o parte de una jerarquía organizativa (principal o secundaria).

![](../assets/new.svg) **Nuevo Administrar compañía configuración a escala**<!--B2B-2849-->: cambie rápidamente compañía opciones de configuración para las empresas seleccionadas mediante la *[!UICONTROL Change company setting]* acción masiva ahora disponible al administrar empresas desde la *[!UICONTROL Companies]* cuadrícula O *[!UICONTROL Company Hierarchy]*. Por ejemplo, si crea un nuevo catálogo compartido para un grupo de empresas, puede cambiar la configuración del catálogo compartido en una sola acción en lugar de editar cada compañía individualmente.

![](../assets/new.svg) API de Nuevo Los desarrolladores pueden usar el nuevo punto `/V1/company/{parentId}/relations` final de la API de REST de relaciones de empresa para crear, vista y quitar asignaciones compañía. Consulte [Administración de objetos](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) de compañía en la Guía *para desarrolladores de API* web.

### Cuentas de empresa

![Nuevo](../assets/new.svg)<!--B2B-2828--> **Asignación de varias empresas**: simplifica el acceso a la cuenta de la empresa para los usuarios de la empresa asignando un usuario a varias empresas. Por ejemplo, si tiene un comprador que realiza pedidos desde varias direcciones de empresa, cree una sola cuenta y asigne todas las empresas con las que trabaja el comprador a esa cuenta. A continuación, el comprador puede iniciar sesión una sola vez y cambiar entre las cuentas de la empresa eligiendo la empresa en la tienda.

>[!NOTE]
>
>Un usuario compañía puede asignarse a varias empresas, pero solo puede ser el administrador compañía de una compañía.

![Nuevo](../assets/new.svg) <!--B2B-2747--> **Company ámbito selector**: proporciona la capacidad para que los usuarios compañía que están asignados a varias compañías cambien de compañía en el escaparate. Cuando se cambia el ámbito, los datos se actualizan para mostrar la información basada en el nuevo contexto compañía. Por ejemplo, si el nuevo compañía utiliza un catálogo compartido diferente, el compañía usuario ve productos, precios y otra información basada en el nuevo catálogo compartido. El contenido relacionado con pedidos, presupuestos y plantillas de presupuestos también se actualiza en función del contexto de la empresa seleccionada.

>[!NOTE]
>El contenido del carro de compras refleja los artículos seleccionados por el cliente actual. Si el cliente tiene un carro de compras activo y selecciona una compañía diferente, se le pedirá que actualice el carro de compras para reflejar el surtido de productos, los precios y los descuentos promocionales en función del nuevo contexto de la compañía. Los productos que no están disponibles en el catálogo asociado con la nueva compañía se eliminan del carro de compras. Si el producto tiene un precio o una disponibilidad diferentes, el carro se actualiza para reflejar los datos disponibles en el contexto de la compañía seleccionada.<!--B2B-4222-->

![Se ha corregido un problema](../assets/fix.svg)<!--ACP2E-1933--> Los administradores de la empresa ahora pueden agregar usuarios de la empresa desde la tienda. Anteriormente, Commerce registraba un error cuando un usuario administrador intentaba agregar un nuevo usuario: `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`.

### Plantillas de Ofertas y Ofertas

Las mejoras en las capacidades de cotización ayudan a los compradores y vendedores a gestionar las ofertas y la negociación de presupuestos de forma más eficaz.

![Nuevas](../assets/new.svg) **plantillas de presupuesto**—<!--B2B-3367-->Los compradores y vendedores ahora pueden optimizar el proceso de presupuesto creando plantillas de presupuesto reutilizables y personalizables. Con las plantillas de oferta, el proceso de negociación de oferta puede completarse una vez y los compradores pueden generar ofertas vinculadas preaprobadas para pedidos recurrentes en lugar de pasar por el proceso de negociación de oferta para cada pedido. Las plantillas de oferta amplían la funcionalidad de oferta existente al añadir las siguientes funciones avanzadas:

- **Umbrales de pedidos** permiten a los vendedores establecer compromisos de pedidos mínimos y máximos, lo que garantiza que el comprador se adhiera a los volúmenes de compras acordados.
- **Al establecer las cantidades de pedido de artículo mínimas y máximas**, el comprador tiene la flexibilidad de ajustar las cantidades de pedido en la oferta vinculada sin necesidad de una nueva plantilla o de una negociación posterior.
- **Rastree el número de ofertas vinculadas generadas y completadas correctamente** para obtener información sobre el cumplimiento de los acuerdos negociados.
- **Las ofertas vinculadas** son ofertas aprobadas previamente que el comprador genera a partir de una plantilla de oferta activa para enviar pedidos recurrentes basados en las condiciones negociadas en la plantilla de oferta.

![Nuevo](../assets/new.svg) **Mejoras en las capacidades de presupuesto existentes**

- **Las reglas actualizadas de la Lista de control de acceso (ACL) de Commerce** permiten a los administradores y supervisores de B2B administrar las ofertas y las plantillas de ofertas de los usuarios subordinados. Las reglas independientes admiten la configuración granular para el acceso de visualización, edición y eliminación.

- **Guardar oferta como borrador**<!--B2B-2566-->: al crear una [solicitud de oferta](quote-request.md) desde el carro de compras, los compradores ahora pueden guardar la oferta como borrador para que puedan revisarla y actualizarla antes de iniciar el proceso de negociación de oferta con el vendedor. El borrador de la oferta no tiene fecha de caducidad. Los compradores pueden revisar y actualizar los borradores de presupuestos desde la sección [!UICONTROL My Quotes] de su panel de cuentas.

- **Cambiar nombre de presupuesto**<!--B2B-2596-->: los compradores ahora pueden cambiar el nombre de un presupuesto de la página [Detalle del presupuesto](account-dashboard-my-quotes.md#quote-actions) seleccionando la opción **[!UICONTROL Rename]**. Esta opción está disponible para los compradores autorizados cuando editan la oferta. Los eventos de cambio de nombre se registran en el Registro del historial de ofertas.

- **Oferta duplicada**<!--B2B-2701-->: los compradores y vendedores ahora pueden crear una nueva oferta copiando una oferta existente. Se crea una copia de la vista de detalles de la oferta seleccionando **[!UICONTROL Create Copy]** en la [vista de detalles de la oferta](quote-price-negotiation.md#button-bar) en el Administrador o en la [Tienda](account-dashboard-my-quotes.md#quote-actions).

- **Mover artículo de oferta a la lista de solicitudes**<!--B2B-2755-->: los compradores tienen ahora la flexibilidad de quitar productos de una oferta y guardarlos en una lista de solicitudes si deciden no incluirlos en el proceso de negociación de ofertas.

- **Quitar varios productos de una oferta**<!--B2B-2881-->: en las ofertas con un gran número de productos, los compradores ahora pueden quitar varios productos de la oferta seleccionándolos y utilizando la opción *[!UICONTROL Remove]* del control *[!UICONTROL Actions]* en la página Detalles de la oferta. En versiones anteriores, un comprador tenía que eliminar productos de uno en uno.

- **Bloqueo de descuento de artículo de línea**<!--B2B-2597-->: durante la negociación de la oferta, los vendedores pueden utilizar el bloqueo de descuento de artículo de línea para obtener más flexibilidad al aplicar descuentos durante el proceso de negociación de la oferta. Por ejemplo, un vendedor puede aplicar un descuento especial por artículo de línea a un artículo y bloquearlo para evitar descuentos adicionales. Cuando un artículo está bloqueado, el precio del artículo no se puede actualizar cuando se aplica un descuento de nivel de oferta. Ver [Iniciar presupuesto para un comprador](sales-rep-initiates-quote.md).

![Problema corregido](../assets/fix.svg) **Correcciones para las capacidades de presupuesto existentes**

- Ahora, los comerciantes que hagan clic en el botón *[!UICONTROL Print]* en la vista de detalles de Oferta del Administrador deberán guardar la oferta como PDF. Anteriormente, se redirigía a los comerciantes a una página que contenía detalles de comillas. <!--ACP2E-1984-->

- Anteriormente, al enviar una oferta de cliente con un porcentaje de `0` y cambiar la cantidad, el administrador emite una excepción, pero guarda la cantidad. Una vez que se aplique esta corrección, se generará una excepción adecuada para `0 percentage` con un mensaje. <!--ACP2E-1742-->

- Durante la negociación de la oferta, un vendedor ahora puede especificar un descuento de `0%` en el campo de descuento de oferta negociada y devolver la oferta al comprador. Anteriormente, si el vendedor introducía un descuento del 0% y devolvía la oferta al comprador, el administrador devolvía un mensaje de error de `Exception occurred during quote sending`. <!--ACP2E-1742-->

- La validación de ReCaptcha ahora funciona correctamente durante el proceso de cierre de compra de una cotización B2B cuando ReCaptcha V3 está configurado para el cierre de compra de tienda. Anteriormente, la validación fallaba con un mensaje de error `recaptcha validation failed, please try again`.  <!--ACP2E-2097-->

### Pedidos de compra

![Problema corregido](../assets/fix.svg) <!--ACP2E-1825-->Un usuario asociado a la compañía ya no puede realizar pedidos de compra una vez que la compañía ha sido bloqueada. Anteriormente, un usuario asociado a la compañía podía realizar pedidos de compra cuando se bloqueaba la compañía.

## B2B v1.4.2-p5

*8 de abril de 2025*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} con las versiones de parches de seguridad de Adobe Commerce 2.4.7-p5+ y 2.4.6-p10+.

![Nuevo](../assets/new.svg) Se ha agregado compatibilidad con las versiones de parches de seguridad de Adobe Commerce 2.4.7-p5+ y 2.4.6-p10+.

![Problema corregido](../assets/fix.svg) Incluye las correcciones de seguridad documentadas en [Boletín de seguridad APSB25-26](https://helpx.adobe.com/security/products/magento/apsb25-26.html).

{{b2b-compatibility}}

## B2B v1.4.2-p4

*11 de febrero de 2025*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} con las versiones de parches de seguridad de Adobe Commerce 2.4.7-p4+ y 2.4.6-p9+.

![Se ha agregado compatibilidad con las versiones de parches de seguridad de Adobe Commerce 2.4.7-p4+ y 2.4.6-p9+.](../assets/new.svg)

![Problema](../assets/fix.svg) corregido Incluye las correcciones de seguridad documentadas en [el boletín de seguridad APSB25-08](https://helpx.adobe.com/security/products/magento/apsb25-08.html).

{{b2b-compatibility}}

## B2B v1.4.2-p3

*8 de octubre de 2024*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} con las versiones de parches de seguridad de Adobe Commerce 2.4.7-p3+ y 2.4.6-p8+.

![Nuevo](../assets/new.svg) Se ha agregado compatibilidad con las versiones de parches de seguridad de Adobe Commerce 2.4.7-p3+ y 2.4.6-p8+.

![Problema](../assets/fix.svg) corregido Incluye las correcciones de seguridad documentadas en [el boletín de seguridad APSB24-73](https://helpx.adobe.com/security/products/magento/apsb24-73.html).

{{b2b-compatibility}}

## B2B v1.4.2-p2

[!BADGE Compatible]{type=Informative tooltip="Admitido"} con las versiones de parches de seguridad de Adobe Commerce 2.4.7-p2+ y 2.4.6-p7+.

![Nuevo](../assets/new.svg) Se ha agregado compatibilidad con las versiones de parches de seguridad de Adobe Commerce 2.4.7-p2+ y 2.4.6-p7+.

![Problema corregido](../assets/fix.svg) Incluye las correcciones de seguridad documentadas en el Boletín de seguridad xxxx.

{{b2b-compatibility}}

## B2B v1.4.2-p1

*9 de agosto de 2024*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} con las versiones de parches de seguridad de Adobe Commerce 2.4.7-p1+ y 2.4.6-p6+.

![Nuevo](../assets/new.svg) Se ha agregado compatibilidad con las versiones de parches de seguridad de Adobe Commerce 2.4.7-p1+ y 2.4.6-p6+.

{{b2b-compatibility}}

## B2B v1.4.2

*octubre 10, 2023*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} Adobe Commerce versión 2.4.7 y versión de 2.4.6 a 2.4.6-p5.

La versión B2B v1.4.2 incluye mejoras de calidad y correcciones de errores.

![Problema corregido](../assets/fix.svg) <!--B2B-2897-->Si un vendedor crea una oferta de comprador que incluye un SKU de producto no disponible en el catálogo compartido asociado con la empresa del comprador, el sistema muestra el mensaje de error `The SKU you entered is not available in the shared catalog. Please check the SKU and try again`.  El vendedor no puede guardar la cotización hasta que elimine el producto que no está disponible. Anteriormente, la oferta se guardaba con el SKU no disponible incluido y no se podía cargar en la tienda.

>[!IMPORTANT]
>
>Adobe Commerce B2B versión 1.4.2+ es compatible con PHP 8.2. Si actualiza la instancia de Commerce a la versión 2.4.7 o posterior, asegúrese de que la instancia utiliza la versión 8.2 de PHP para mantener la compatibilidad con la versión B2B de Adobe Commerce. Además, B2B 1.4.2+ no admite actualmente [GraphQL Application Server](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).

## B2B v1.4.1

*7 de agosto de 2023*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} [Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Compatible con Adobe Commerce 2.4.7-beta1.

La versión B2B v1.4.1 incluye mejoras de calidad y correcciones de errores.

![Problema corregido](../assets/fix.svg) <!--ACP2E-1825-->Un usuario asociado a la compañía ya no puede realizar pedidos de compra una vez que la compañía ha sido bloqueada. Anteriormente, un usuario asociado a la compañía podía realizar pedidos de compra cuando se bloqueaba la compañía.

![Se ha corregido un problema](../assets/fix.svg) <!--ACP2E-1943-->El estado de producto no satisfecho ahora se muestra correctamente en la tienda. Anteriormente, los productos disponibles para el envío se identificaban incorrectamente como no pedidos.

![Problema corregido](../assets/fix.svg) <!--ACP2E-1862-->Si el formulario de registro de la empresa incluye un atributo de tipo de archivo de cliente, el archivo cargado durante el proceso de registro ahora se incluye en la información de cuenta del administrador de la empresa una vez creada la empresa. Anteriormente, faltaba el archivo adjunto.

![Problema corregido](../assets/fix.svg) <!--ACP2E-1793-->El selector de muestras para un producto configurable ahora se muestra según lo esperado en la página de configuración del elemento de la lista de solicitudes. Anteriormente, el selector de muestras se mostraba como un campo desplegable en la página de configuración de artículos de la lista de solicitudes.

![Se ha corregido un problema](../assets/fix.svg) <!--ACP2E-1968-->Al usar la [Consulta GraphQL de la empresa](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) para devolver los detalles de la empresa, los resultados ahora se devuelven correctamente sin errores.

## B2B v1.4.0

*13 de junio de 2023*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} [Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Compatible con Adobe Commerce 2.4.7-beta1

Esta versión incluye nuevas funciones y mejoras para presupuestos negociables B2B y varias correcciones de errores.

![Nuevo](../assets/new.svg) agregó compatibilidad con Adobe Commerce 2.4.7-beta1.

![Nuevo](../assets/new.svg) **El vendedor inició presupuestos**—Los vendedores ahora pueden iniciar un presupuesto para un comprador directamente desde las cuadrículas de Oferta y Cliente en el Administrador. Esta capacidad optimiza el proceso de cotización y reduce la complejidad para los clientes. Si un cliente no ha iniciado un pedido, un vendedor puede crear rápidamente una oferta en nombre del cliente e iniciar el proceso de negociación. Anteriormente, las ofertas solo se podían crear desde la tienda por el comprador o por un vendedor que iniciara sesión como cliente.

![Nuevo](../assets/new.svg) **Descuentos y negociación de artículo de línea**—<!--B2B-2440--> Dentro de una oferta, los compradores y vendedores de B2B ahora pueden negociar en el nivel de artículo de línea, aplicando descuentos e intercambiando notas hasta que se llegue a un acuerdo. La creación de notas y las actualizaciones se incluyen en el historial de artículos de línea y presupuestos para rastrear la comunicación. Anteriormente, los compradores y vendedores solo podían intercambiar notas y aplicar descuentos en el nivel de cotización.

![Problema corregido](../assets/fix.svg) Adobe Commerce ahora muestra los detalles correctos durante el pago cuando la opción Pedidos de compra está habilitada y se ha seleccionado una oferta virtual que se creó con la opción de pago PayPal. Anteriormente, los totales se mostraban como cero en estas condiciones.

![Se ha corregido un problema](../assets/fix.svg) <!--ACP2E-1504-->: ya no se producen errores de validación al intentar guardar una empresa con un límite de crédito superior a 999. Anteriormente, para los límites de crédito de empresa superiores a 999, Adobe Commerce insertaba un separador de comas, lo que provocaba un error de validación que impedía guardar las actualizaciones.

![Problema corregido](../assets/fix.svg) <!--ACP2E-1474--> La dirección de envío seleccionada ahora permanece sin cambios cuando realiza un pedido con un presupuesto negociable. Anteriormente, al realizar un pedido, la dirección de envío seleccionada se cambiaba a la dirección de envío predeterminada.

![Se ha corregido un problema](../assets/fix.svg) <!--ACP2E-1429--> En la configuración de la tienda para las características B2B, el campo **[!UICONTROL Enable Shared Catalog direct products price assigning]** ahora se deshabilita automáticamente. En la tienda, se oculta cuando la configuración **[!UICONTROL Enable Company]** o **[!UICONTROL Enable Shared Catalog]** se establece en **[!UICONTROL No]**.

![Se ha corregido un problema](../assets/fix.svg) <!--ACP2E-1683--> Al crear una cuenta de empresa desde la tienda, Commerce ahora valida la dirección de correo electrónico antes de procesar el registro de empresa. Si la dirección de correo electrónico no es válida, la operación falla y no se procesan las actualizaciones de la cuenta. Anteriormente, se creaba una cuenta de cliente aunque la solicitud para crear una cuenta de empresa fallara debido a una dirección de correo electrónico no válida.

![Se ha corregido un problema](../assets/fix.svg) <!--ACP2E-1664--> Las SKU de producto que incluyen comillas dobles en el catálogo compartido y la estructura de precios ya no causan errores en el administrador.

![Se ha corregido un problema](../assets/fix.svg) <!--ACP2E-1498-->. Se ha actualizado la configuración de Barniz de la aplicación Commerce para evitar que los usuarios invitados vean datos de otros grupos de clientes.

### Problema conocido

Si instala o actualiza B2B 1.4.0 en [Adobe Commerce versión 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html), se producirá el siguiente error:

```
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

Para solucionar este problema, agregue dependencias manuales para el paquete de seguridad B2B. Agregue dependencias manuales para el paquete de seguridad B2B con una [etiqueta de estabilidad](https://getcomposer.org/doc/04-schema.md#package-links). Para obtener instrucciones, consulte la [Base de conocimiento de Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html).

## B2B v1.3.5-p10

*8 de abril de 2025*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} con las versiones de parches de seguridad de Adobe Commerce 2.4.6-p10+.

![Nuevo](../assets/new.svg) Se agregó compatibilidad con las versiones de parches de seguridad de Adobe Commerce 2.4.6-p10.

![Problema](../assets/fix.svg) corregido Incluye las correcciones de seguridad documentadas en [el boletín de seguridad APSB25-26](https://helpx.adobe.com/security/products/magento/apsb25-26.html).

## B2B v1.3.5-p9

*11 de febrero de 2025*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} con las versiones de parches de seguridad de Adobe Commerce 2.4.6-p9+.

![Nuevo](../assets/new.svg) Se agregó compatibilidad con las versiones de parches de seguridad de Adobe Commerce 2.4.6-p9.

![Problema](../assets/fix.svg) corregido Incluye las correcciones de seguridad documentadas en [el boletín de seguridad APSB25-08](https://helpx.adobe.com/security/products/magento/apsb25-08.html).

## B2B v1.3.5-p8

*8 de octubre de 2024*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} con las versiones de parches de seguridad de Adobe Commerce 2.4.6-p8+.

![Nuevo](../assets/new.svg) Se agregó compatibilidad con las versiones de parches de seguridad de Adobe Commerce 2.4.6-p8.

![Problema corregido](../assets/fix.svg) Incluye las correcciones de seguridad documentadas en [Boletín de seguridad APSB24-73](https://helpx.adobe.com/security/products/magento/apsb24-73.html).

## B2B v1.3.5-p7

*9 de agosto de 2024*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} versiones de parches de seguridad de Adobe Commerce 2.4.6-p7+.

![](../assets/new.svg) Nuevo Se ha agregado compatibilidad con las versiones de parche de seguridad de Adobe Systems Commerce 2.4.6-p7.

## B2B v1.3.5

*14 de marzo de 2023*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} Adobe Commerce 2.4.0 - 2.4.6 y versiones más recientes

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

## B2B v1.3.4-p12

*8 de abril de 2025*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} con Adobe Commerce 2.4.0 y versiones más recientes

![Nuevo](../assets/new.svg) agregó compatibilidad con Adobe Commerce 2.4.5-p12.

![Problema corregido](../assets/fix.svg) Incluye las correcciones de seguridad documentadas en [Boletín de seguridad APSB25-26](https://helpx.adobe.com/security/products/magento/apsb25-26.html).

## B2B v1.3.4-p11

*11 de febrero de 2025*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} con Adobe Commerce 2.4.0 y versiones más recientes

![Nuevo](../assets/new.svg) agregó compatibilidad con Adobe Commerce 2.4.5-p11.

![Problema corregido](../assets/fix.svg) Incluye las correcciones de seguridad documentadas en [Boletín de seguridad APSB25-08](https://helpx.adobe.com/security/products/magento/apsb25-08.html).

## B2B v1.3.4-p10

*9 de octubre de 2024*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} con Adobe Commerce 2.4.0 y versiones más recientes

![Nuevo](../assets/new.svg) agregó compatibilidad con Adobe Commerce 2.4.5-p10.

![Problema corregido](../assets/fix.svg) Incluye las correcciones de seguridad documentadas en [Boletín de seguridad APSB24-73](https://helpx.adobe.com/security/products/magento/apsb24-73.html).

## B2B v1.3.4

*9 de agosto de 2022*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} con Adobe Commerce 2.4.0 y versiones más recientes

![Nuevo](../assets/new.svg) agregó compatibilidad con Adobe Commerce 2.4.5.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-453-->Adobe Commerce ya no envía notificaciones por correo electrónico cada vez que una llamada API actualiza una compañía existente. Ahora, los correos electrónicos solo se envían cuando se crea una empresa.

![Problema corregido](../assets/fix.svg) <!--- ACP2E-406-->Adobe Commerce ahora calcula correctamente un total general de una cotización negociable cuando la configuración de cálculo de impuestos de **[!UICONTROL Enable Cross Border Trade]** está habilitada.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-322-->Los productos configurables ahora se mueven a la última posición de la lista de productos después de que se hayan actualizado las existencias cuando la configuración de **[!UICONTROL Move out of stock to the bottom]** esté habilitada. Se implementa una nueva consulta de base de datos personalizada para garantizar que el criterio de ordenación de índices de Elasticsearch ahora respeta el criterio de ordenación habilitado por el administrador. Anteriormente, los productos configurables y sus productos secundarios no se movían al final de la lista cuando esta configuración estaba habilitada.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-308-->El correo electrónico de la orden de compra ahora respeta la configuración de envío de correo electrónico de cada sitio web en una implementación de varios sitios. Se agregó una comprobación para la configuración **[!UICONTROL Disable Email Communications]** a la lógica personalizada para colas de correo electrónico. Anteriormente, Adobe Commerce no respetaba la configuración de envío de correo electrónico del sitio web secundario.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-302-->El título del campo SKU de la página de pedido rápido se ha cambiado para mayor claridad.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-543-->Adobe Commerce ahora muestra un mensaje de error más informativo cuando un comprador introduce un SKU no válido en el campo **Introducir SKU o nombre del producto**.

![Problema corregido](../assets/fix.svg) <!--- ACP2E-1753-->El campo **[!UICONTROL Account Created in]** de un administrador de empresa ahora conserva su valor como se espera después de guardar la empresa.

![Problema corregido](../assets/fix.svg) <!--- ACP2E-722 -->La consulta `customer` ya no devuelve resultados vacíos cuando recupera listas de solicitudes filtradas por `uid`.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-210 -->Se ha agregado un complemento antes de la llamada a `collectQuoteTotals` para garantizar que los créditos de la tienda se apliquen solo una vez.

![Problema](../assets/fix.svg) <!--- ACP2E-665 -->corregido Ahora, se redirige a los clientes al Página inicio de sesión cuando un administrador elimina de Administración su cuenta. Anteriormente, Adobe Systems Commerce arrojaba un error. El bloque de código plug-in (`SessionPlugin`) está ahora dentro del `try…catch` bloque. Anteriormente, este código no se agrupaba dentro del bloque genérico de control de excepciones.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-661 --> En la página Pedido rápido en el modo móvil, al presionar **Intro** después de escribir un nombre de producto o SKU válido, ahora el comprador pasa al siguiente campo según lo esperado.

![Problema corregido](../assets/fix.svg) <!--- ACP2E-607 -->El nombre de la compañía ahora está visible como se espera en las secciones de facturación y dirección de envío del flujo de trabajo de cierre de compra.

![Se ha corregido un problema](../assets/fix.svg) <!--- ACP2E-375 -->El crédito de la tienda no está disponible cuando el método de pago **[!UICONTROL Zero Subtotal Checkout]** está deshabilitado. Anteriormente, la casilla de verificación de crédito de tienda no funcionaba durante la realización del pedido desde el administrador. La aplicación no realizó el pedido con el crédito de la tienda y mostró este error: `The requested Payment Method is not available`.

## B2B v1.3.3

*9 de agosto de 2022*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} con Adobe Commerce 2.4.0 y versiones más recientes

![Nuevo](../assets/new.svg) agregó compatibilidad con Adobe Commerce 2.4.4.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-41985--> El tiempo necesario para actualizar de Adobe Commerce 2.3.x a Adobe Commerce 2.4.x en implementaciones con más de 100 000 roles de compañía se ha reducido sustancialmente.

![Problema corregido](../assets/fix.svg) <!--- MC-42153--> La solicitud POST `V1/order/:orderId/invoice` ahora admite la creación de facturas parciales cuando el método de pago **[!UICONTROL Payment on Account]** está habilitado. Anteriormente, Adobe Commerce arrojó este error: `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`. [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![Se solucionó el problema](../assets/fix.svg) <!--- MC-41975--> PayPal Payflow Pro ahora funciona como se esperaba con B2B cotización negociable cuando la carro de compras del cliente contiene otros productos. Adobe Systems Commerce ahora procesa correctamente el pedido y envía un correo electrónico al cliente según lo esperado. Anteriormente, Adobe Systems Commerce arrojaba un error fatal y enviaba una correo electrónico de confirmación al cliente que contenía cero valores.

![Problema](../assets/fix.svg) <!--- MC-41819--> corregido La paginación ahora se muestra correctamente en el catálogo resultado de búsqueda Página después de excluir algunos productos del catálogo compartido.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-42886--> Los atributos personalizados del cliente ahora se guardan según lo esperado al crear o guardar un usuario de compañía en Administración.

![Problema](../assets/fix.svg) <!--- MC-42927--> corregido La **[!UICONTROL Submit]** botón del formulario de Crear Nuevo Company ahora está deshabilitada después de un clic para evitar que se envíen varios formularios. Anteriormente, se podía enviar este formulario varias veces haciendo clic en este botón repetidamente, lo que generaba un error.

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

[!BADGE Compatible]{type=Informative tooltip="Admitido"} con Adobe Commerce 2.4.0 y versiones más recientes

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

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-41721--> Los filtros de usuario de la empresa, como Mostrar Todos los usuarios, Usuarios activos Mostrar y Usuarios inactivos Mostrar, ahora funcionan como se espera. Anteriormente, las acciones de filtrado en el usuario de compañía Página provocaban un error de JavaScript.

### Crédito de la empresa

![Problema](../assets/fix.svg) <!--- MC-41551--> corregido Los administradores con cuentas restringidas que solo incluyen privilegios de nivel de sitio web ahora pueden crear un compañía que use una moneda diferente a la del sitio web.

![Se ha corregido el problema](../assets/fix.svg) <!--- MC-41523--> Adobe Systems Commerce ahora envía correos electrónicos a compañía desde la dirección correo electrónico y el ámbito correctos `from` . Anteriormente, Adobe Systems Commerce no tenía en cuenta la ámbito del sitio web al enviar compañía asignación de créditos o actualizar correo electrónico.

### Pedido rápido

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-42104-->: la creación de un pedido mediante el uso de un pedido rápido a partir de un archivo CSV ahora funciona como se espera con SKU que no existen.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-40268-->. Ahora, el uso de un pedido rápido para buscar en varios SKU funciona según lo esperado. Anteriormente, los resultados incluían entradas duplicadas.

![Problema corregido](../assets/fix.svg) <!--- MC-40261--> La visualización de la lista de productos agregados ahora trata los SKU escritos en minúsculas y mayúsculas de la misma manera cuando se usan SKU para seleccionar varios productos durante el pedido rápido.

![Solucionado el problema](../assets/fix.svg) <!--- MC-40225--> Uso de pedido rápido ahora agrega productos en la cantidad especificada por el comprador. Anteriormente, Adobe Systems Departamento de Comercio agregaba un solo producto igualado cuando las cantidades especificadas por comprador excedían de uno.

![Problema corregido](../assets/fix.svg) <!--- MC-41283-->: la función de autocompletar pedidos rápidos ahora funciona con SKU parciales.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-41299--> Adobe Commerce ahora muestra los productos que se han configurado como **No visibles por separado** en la lista de sugerencias automáticas y los resultados de búsqueda de la página Pedido rápido.

![Problema corregido](../assets/fix.svg) <!--- MC-42402--> Los compradores ahora pueden usar el formulario de pedido rápido para agregar varios productos por SKU que incluyan caracteres en mayúsculas. Anteriormente, solo se añadía el primer producto.

### Cotización negociable

![Problema](../assets/fix.svg) <!--- MC-41232--> corregido Ahora, se redirige a los compradores al Página de presupuesto negociable después de pegar el vincular en un presupuesto negociable en el campo URL y registro correctamente. Anteriormente, se redirigía a los compradores a la Mi cuenta Página.

![Solucionado el problema](../assets/fix.svg)<!--- MC-39317-->: Reordenar ahora funciona como se espera para pedidos que contienen un producto con una opción personalizable de fecha para un cliente cuenta que se creó durante el cierre de compra. Anteriormente, Adobe Systems Commerce no procesaba la reordenación y mostraba este error: `The product has required options. Enter the options and try again`.

![Problema](../assets/fix.svg) <!--- MC-39063--> corregido La dirección de envío de un presupuesto negociable ya no se puede editar durante el cierre de compra cuando el módulo de orden de compra está desactivado. Este comportamiento era el resultado de una corrección anterior que `isQuoteAddressLocked` se eliminaba del procesador de compra de cotizaciones negociables.

![Problema corregido](../assets/fix.svg) <!--- MC-38967--> Los comerciantes ahora pueden agregar productos a una cotización negociable del administrador.

### Pedidos de compra

![Problema corregido](../assets/fix.svg) <!--- MC-39983--> Adobe Commerce ahora muestra un mensaje de error informativo como se espera cuando se realiza un pedido de compra mediante Pago y envío rápido de PayPal cuando el atributo **[!UICONTROL Name Prefix]** está establecido en `required`. Anteriormente, Adobe Commerce no realizaba el pedido ni mostraba un mensaje de error.

![Problema corregido](../assets/fix.svg) <!--- MC-39620-->: el componente de la interfaz de usuario para la dirección de facturación en el módulo de pedidos de compra ahora utiliza la dirección de oferta correctamente cuando Google Tag Manager está habilitado. Anteriormente, se producía un error de JavaScript en la página de pago.

### Listas de solicitudes

![Problema corregido](../assets/fix.svg) <!--- MC-40426--> Los comerciantes ahora pueden usar el extremo POST `rest/all/V1/requisition_lists` para crear una lista de solicitudes para un cliente. Anteriormente, Adobe Commerce arrojaba este error 400 al intentar crear una lista de solicitudes: `Could not save Requisition List`.

![Problema corregido](../assets/fix.svg) <!--- MC-41123--> El botón **[!UICONTROL Add to Requisition List]** aparece ahora para los productos en stock de un carro de compras cuando el carro también contiene productos sin existencias. Anteriormente, si un carro de compras contenía dos productos, uno de los cuales estaba agotado, el botón _[!UICONTROL Add to Requisition List]_&#x200B;no aparecía en ninguno de los productos.

![Problema corregido](../assets/fix.svg) <!--- MC-40877--> Ahora puede usar la API de REST para agregar un producto a una lista de solicitudes.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-40155--> Los valores de la lista de solicitudes **[!UICONTROL Latest Activity Date]** ahora se adhieren al formato de configuración regional.

![Problema corregido](../assets/fix.svg) <!--- MC-39580--> Adobe Commerce ya no genera un error grave al editar un producto agrupado de una lista de solicitudes.

![Problema corregido](../assets/fix.svg) <!--- MC-40454--> Adobe Commerce ahora muestra el precio de producto correcto cuando agrega un producto con una opción personalizable `(File)` a una lista de deseos desde una lista de solicitudes. El vínculo al archivo cargado también es visible como se espera. Anteriormente, Adobe Commerce mostraba precios de productos incorrectos y no mostraba el vínculo al archivo.

![Problema corregido](../assets/fix.svg) <!--- MC-36383--> Los productos con una opción personalizable `(File)` ahora se pueden agregar a un carro de compras desde una lista de solicitudes.

### Catálogo compartido

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-40497-->: un administrador con una función limitada a un sitio web específico ahora puede crear, ver y editar un catálogo compartido. Anteriormente, Adobe Commerce arrojaba un error grave cuando un administrador con una función limitada intentaba crear un catálogo compartido.

![Problema corregido](../assets/fix.svg) <!--- MC-41337--> Los resultados de navegación por capas ahora incluyen un recuento preciso de productos con atributos filtrados, y los compradores ahora pueden aplicar varios filtros. Anteriormente, solo se podía aplicar un filtro y Adobe Commerce mostraba un recuento de productos impreciso en la navegación por capas.

![Se ha corregido un problema](../assets/fix.svg) <!--- MC-40779-->: Adobe Commerce ahora muestra correctamente los recuentos de productos en los filtros de navegación por capas en los resultados de búsqueda. Anteriormente, un complemento para la página de resultados de búsqueda no utilizaba Elasticsearch, pero sí enviaba una nueva consulta a la base de datos.

![Problema corregido](../assets/fix.svg) <!--- MC-39978--> Adobe Commerce ya no elimina los precios de nivel cuando un comerciante elimina todos los productos de un catálogo compartido predeterminado.

![Problema corregido](../assets/fix.svg) <!--- MC-39802--> Los filtros ahora se filtran por la categoría actual y se muestran correctamente en todas las páginas cuando los catálogos compartidos están habilitados. Anteriormente, los filtros se calculaban incorrectamente solo para la página actual y no se filtraban por la categoría actual.

![Problema corregido](../assets/fix.svg) <!--- MC-39522-->: la consulta de GraphQL `products` ya no devuelve el rango de precios y la categoría de un producto para los productos que no están asignados a un catálogo compartido cuando el catálogo compartido está habilitado. Anteriormente, la consulta devolvía las agregaciones del producto, aunque el producto en sí no se devolvía en la matriz `items`.

## B2B v1.3.1

*9 de febrero de 2021*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} con Adobe Commerce 2.4.0 y versiones más recientes

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

![Problema](../assets/fix.svg) solucionado Ahora puede filtrar los pedidos por el campo al exportar la información de pedidos **[!UICONTROL Company Name]** en CSV formato. Anteriormente, Adobe Systems Commerce registraba un error en `var/export/{file-id}`. <!--- MC-37785-->

![Se ha corregido el problema](../assets/fix.svg) Adobe Systems Comercio ahora muestra la ventana emergente Lista de solicitudes de Crear como se esperaba al seleccionar el Crear Nuevo Lista de solicitudes pestaña en el escaparate. <!--- MC-37915-->

![Problema](../assets/fix.svg) corregido Las listas de solicitudes ahora incluyen todos los productos agrupados y las cantidades que se han agregado al lista. Anteriormente, cuando un comerciante navegaba a un lista de solicitud después de agregarle productos desde un Página detallado del producto, Adobe Systems Commerce mostraba este error: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

![Problema](../assets/fix.svg) solucionado El vista de tienda correcto ahora se asocia al sitio web relevante cuando crea un compañía en un implementación de varios sitios. Anteriormente, no se podía crear una compañía y Adobe Commerce mostraba este error: `The store view is not in the associated website`. <!--- MC-37488-->

![Se ha corregido un problema](../assets/fix.svg). Ya no es posible duplicar cantidades de productos en el archivo CSV si se solicitan productos por SKU mediante un pedido rápido. <!--- MC-37427-->

![Problema corregido](../assets/fix.svg): el botón **[!UICONTROL Add to Cart]** ya no está bloqueado cuando la sección _[!UICONTROL Enter Multiple SKUs]_&#x200B;de la página Pedido rápido contiene un valor vacío. Ahora, Adobe Commerce muestra un mensaje en el que se le solicita que introduzca SKU válidas. <!--- MC-37387-->

![Problema](../assets/fix.svg) corregido Adobe Systems Comercio ahora muestra este mensaje en la página de producto cuando envía una reseña de producto desde un lista de solicitud: `You submitted your review for moderation`. La revisión también aparece en la Página Revisiones pendientes (Administrador **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**). Anteriormente, aunque Adobe Systems Commerce agregó la revisión al lista de revisiones pendientes, arrojó un error 404 en la página de producto. <!--- MC-37119-->

![Se ha corregido un problema](../assets/fix.svg). Se ha mejorado el rendimiento del consumidor `sharedCatalogUpdateCategoryPermissions`. Después de crear un catálogo compartido, el indexador de permisos de catálogo ahora utiliza solo el ID de grupo de clientes del catálogo compartido, no todos los grupos de clientes. <!--- MC-36770-->

![Se ha corregido un problema](../assets/fix.svg). Los campos de atributos personalizados de dirección de cliente asociados con una dirección no predeterminada de comprador ahora se guardan según lo esperado en el flujo de trabajo de cierre de compra de la tienda. <!--- MC-36630-->

![Se ha corregido un problema](../assets/fix.svg). Los pedidos de productos que pertenecen al catálogo compartido predeterminado de una tienda ahora se pueden realizar para compradores a través de la API de REST de administración (`rest/V1/carts/{<CART_ID>/items`) según lo esperado. Adobe Commerce ahora comprueba si el producto se asignó a un catálogo público antes de la validación de los permisos del catálogo compartido en `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave`. Anteriormente, Adobe Commerce no agregaba el producto al carro de compras y arrojaba este error: `No such shared catalog entity`. <!--- MC-36535-->

![Se ha corregido el problema](../assets/fix.svg) Adobe Systems Commerce ahora envía nuevas compañía usuario registro correos electrónicos desde la dirección del tienda de Adobe Systems Commerce. Anteriormente, este correo electrónico se enviaba desde la dirección del administrador de compañía. <!--- MC-36480-->

![Se ha corregido el problema](../assets/fix.svg) Adobe Systems ahora Commerce comprueba los atributos personalizados en busca de duplicación de nombres de atributos de compañía reservados antes de permitir que un comerciante guarde un atributo nuevo. <!--- MC-36282-->

![Problema](../assets/fix.svg) corregido Ahora `credit_history` , el consulta devuelve el historial crediticio del compañía especificado tanto para el importe asignado originalmente como para el importe comprado. Anteriormente, este consulta devolvía un error.

![Problema](../assets/fix.svg) corregido Los **[!UICONTROL Company]** campos y  **[!UICONTROL Job Title]** del Página Información de la cuenta Editar ya no son editables.

### Problemas conocidos

- Los compradores de B2B pueden utilizar métodos de pago en línea para evitar el flujo habitual de órdenes de compra. Este escenario se puede producir si el comprador puede reducir todo el total del pago a un 0 (por ejemplo, mediante un código de promoción o una tarjeta regalo) y, a continuación, eliminar el código o la tarjeta regalo. Incluso en estas condiciones, Adobe Commerce sigue realizando el pedido de la cantidad correcta en función de los precios de los artículos en el catálogo asignado. **_Solución alternativa_**: deshabilita las tarjetas regalo y los códigos de cupones cuando los métodos de pago en línea estén habilitados para la aprobación de pedidos de compra. <!--- B2B-1603-->

- Se redirige a los compradores al carro de compras al intentar realizar un pedido a partir de un pedido de compra mediante Pago y envío exprés de PayPal cuando se deshabilita **[!UICONTROL In-Context Mode]**. <!--- B2B-1604-->

- Adobe Commerce a veces muestra un error 404 cuando un comprador crea un pedido y luego navega a la página de pago. Este error se produce cuando un comprador ha creado previamente un pedido de compra diferente con un método de pago en línea antes de navegar a la página de pago sin completar la compra anterior. El comprador aún puede realizar el pedido de compra. **_Trabajar_**: Ninguno. <!--- B2B-1605-->

- Los descuentos de un método de pago concreto persisten durante el proceso de pago de un pedido de compra, incluso cuando el comprador cambia su método de pago durante el proceso de pago final. Como resultado, los clientes pueden recibir un descuento al que no tienen derecho. Este problema se produce porque una regla de carro de compras para el método de pago original se sigue aplicando a pesar del cambio en el método de pago. **_Trabajar_**: Ninguno. Ver el problema conocido de [Adobe Commerce 2.4.2 B2B: queda descuento para pedidos de compra en línea después de cambiar el método de pago](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html) artículo de _Knowledge Base_. <!-- B2B-1012 -->

- La consulta `deleteRequisitionListOutput` devuelve detalles sobre la lista de solicitudes eliminada en lugar de las listas de solicitudes restantes. <!--- MC-39894-->

## B2B v1.3.0

*15 de octubre de 2020*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} con Adobe Commerce 2.4.0 y versiones más recientes

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

![Se ha corregido un problema](../assets/fix.svg) Ahora se puede actualizar una compañía mediante la solicitud de PUT `/V1/company/:companyId` de la API de REST sin especificar `region_id` cuando el estado se configura como **no obligatorio**. Anteriormente, aunque `region_id` no era obligatorio, Adobe Commerce arrojaba un error si no se especificaba. <!--- MC-35304-->

![Se ha corregido un problema](../assets/fix.svg) Cuando crea o actualiza una compañía B2B mediante la API de REST (`http://magento.local/rest/V1/company/2`, donde `2` representa el identificador de la compañía), la respuesta ahora incluye la configuración de `applicable_payment_method` o `available_payment_methods` según lo esperado. <!--- MC-35248-->

![Se ha corregido un problema](../assets/fix.svg) Adobe Systems Comercio ya no muestra un Página 404 cuando un comerciante utiliza el **botón Intro** en lugar de hacer clic en el **[!UICONTROL Save]** botón al crear un lista de solicitud en el escaparate.<!--- MC-35094-->

![Se ha corregido un problema](../assets/fix.svg) Categoría los permisos dejaban de cambiar cuando se asignaba un producto nuevo a un catálogo público compartido. Anteriormente, categoría permisos estaban duplicados. <!--- MC-34386-->

![Problema](../assets/fix.svg) corregido El punto final de la API de REST PUT `rest/default/V1/company/{id}`, que se utiliza para actualizar las correo electrónico de la empresa, ya no distingue entre mayúsculas y minúsculas. <!--- MC-34308-->

![Problema](../assets/fix.svg) corregido La desactivación de los módulos de recompensas ya no afecta a B2B funciones de las cuentas de los clientes. Anteriormente, cuando los módulos de recompensa estaban deshabilitados, las siguientes pestañas relacionadas con B2B no se mostraban: Perfil de la empresa, Usuarios de la empresa y Roles y permisos.<!--- MC-34191-->

![Se ha corregido un problema](../assets/fix.svg). Adobe Commerce ahora usa el nombre de remitente correcto en las notificaciones por correo electrónico cuando se realizan cambios en las cuentas de la empresa. Anteriormente, Adobe Commerce utilizaba el nombre general del remitente del contacto definido en el ámbito predeterminado para todos los correos electrónicos. <!--- MC-33917-->

![Problema corregido](../assets/fix.svg) Ahora puede implementar correctamente el envío múltiple para pedidos que contienen productos físicos y virtuales. <!--- MC-33818-->

![Problema corregido](../assets/fix.svg) Los comerciantes ahora pueden crear usuarios de la compañía desde la sección _[!UICONTROL Company Users]_&#x200B;en las páginas Mi cuenta y Estructura de la compañía cuando **[!UICONTROL Access Restriction]**&#x200B;está habilitado y **[!UICONTROL Restriction Mode]**&#x200B;está establecido en `Sales: Login Only`. Anteriormente, Adobe Commerce arrojaba este error cuando un comerciante intentaba crear un usuario: `Can not register new customer due to restrictions are enabled`. <!--- MC-33608-->

![Se ha corregido un problema](../assets/fix.svg) Adobe Systems Comercio ya no restablecía el grupo de cliente de un cliente a la opción predeterminada cuando un cliente guardaba la información de cuenta. <!--- MC-33554-->

![Problema corregido](../assets/fix.svg) Adobe Commerce ya no genera un error grave cuando un administrador asigna un cliente que tiene un carro de compras activo a un grupo de clientes. <!--- MC-33313-->

![Problema corregido](../assets/fix.svg) Adobe Commerce ahora proporciona un evento de capa de datos `addToCart` para páginas de listas de pedidos rápidos y solicitudes.  <!--- MC-33295-->

![Se ha corregido un problema](../assets/fix.svg) Los mensajes de correo electrónico de notificación que se envían a los representantes de ventas asignados a una compañía ahora incluyen el logotipo corporativo asignado. Anteriormente, el correo electrónico de notificación incluía el logotipo predeterminado de LUMA, no el logotipo corporativo cargado. <!--- MC-33232-->

![Problema corregido](../assets/fix.svg) Una lista de solicitudes ahora incluye todos los productos agrupados y las cantidades que se han agregado a la lista. Anteriormente, cuando un comerciante navegaba a una lista de solicitudes después de agregarle productos desde una página de detalles de producto, Adobe Commerce mostraba este error: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![Problema](../assets/fix.svg) corregido Ahora, la `products` consulta devuelve un campo preciso `total_count` cuando el catálogo compartido está habilitado. <!--- MC-42268-->

![Se ha corregido un problema](../assets/fix.svg) Las páginas Configuración de empresa y Crear página Empresa ahora funcionan según lo esperado después de desactivar un método de envío en línea. Se ha añadido la verificación para evitar que se intente procesar los módulos de envío deshabilitados. Anteriormente, Adobe Systems Commerce mostraba este error: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`. <!--- MC-43178-->

![Problema](../assets/fix.svg) solucionado Se ha reducido la integración prueba el consumo de memoria, lo que mejora prueba rendimiento y reduce el tiempo necesario para prueba finalización. <!--- AC-266-->

## B2B v1.2.0

*28 de julio de 2020*

[!BADGE Compatible]{type=Informative tooltip="Admitido"} con Adobe Commerce 2.4.0 y versiones más recientes

![Nuevo](../assets/new.svg) agregó compatibilidad con Adobe Commerce 2.4.0.

![Nueva](../assets/new.svg) búsqueda de pedidos de tiendas, con agradecimiento adicional por la contribución de Marek Mularczyk de [Divante](https://www.divante.com/) y miembros de la comunidad.

Se mejoraron y se volvieron a escribir ![nuevos](../assets/new.svg) pedidos de compra. Ahora se incluyen de forma predeterminada en Adobe Commerce.

![Se han implementado nuevas](../assets/new.svg) reglas de aprobación de pedidos de compra. Estas reglas permiten a los usuarios controlar el flujo de trabajo del pedido de compra mediante la creación de reglas de compra para los pedidos.

![Nuevo](../assets/new.svg) Iniciar sesión como cliente ahora se incluye de forma predeterminada en Adobe Commerce. Esta función permite a los empleados del sitio ayudar a los clientes iniciando sesión como clientes para ver lo que ven.

![Se ha corregido un problema](../assets/fix.svg). Las agregaciones de atributos ahora funcionan correctamente para la navegación por capas con Elasticsearch

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
