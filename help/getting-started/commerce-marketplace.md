---
title: '[!DNL Adobe Commerce Marketplace]'
description: Obtenga información acerca de [!DNL Commerce Marketplace], que ofrece a los comerciantes una selección revisada de soluciones y proporciona a los desarrolladores cualificados las herramientas, la plataforma y la ubicación privilegiada para crear un negocio próspero.
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 02e7c71fc47e6850371bfbdc1be50f65ec8015e9
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 0%

---

# Adobe Commerce Marketplace

[Adobe Commerce Marketplace][1] es la tienda de aplicaciones que ofrece a los comerciantes una selección revisada de soluciones y proporciona a los desarrolladores cualificados las herramientas, la plataforma y la ubicación principal para crear un negocio próspero. [!DNL Commerce Marketplace] ofrece una selección de extensiones disponibles de forma gratuita, así como otras que están a la venta. Las compras se pueden pagar con tarjeta de crédito o [PayPal][2].

Todas las extensiones disponibles en [!DNL Commerce Marketplace] ha pasado una extensa revisión. El [Programa de calidad de extensiones][3] (EQP) combina [!DNL Commerce] experiencia, directrices de desarrollo e instrumentos de verificación para garantizar que todas las extensiones de Commerce Marketplace cumplan las normas de codificación y las prácticas recomendadas. El proceso de revisión incluye tanto una comprobación automatizada como una revisión manual del control de calidad. Durante el proceso, la estructura y el código de cada extensión se examinan y prueban para detectar pruebas de infección por virus/malware y cualquier indicio de plagio. La revisión incluye un examen técnico profundo y una comprobación de la salud mental realizada por un [!DNL Commerce] ingeniero, con un enfoque en la documentación, estructura de codificación, rendimiento, escalabilidad, seguridad y compatibilidad con el [!DNL Commerce] Núcleo.

Aunque puede adquirir extensiones de otras fuentes, solo las extensiones disponibles en [!DNL Commerce Marketplace] se verifican mediante una amplia revisión técnica y de marketing dentro del Programa de Calidad de la Extensión.

## Recursos de aplicación

Tradicionalmente, los desarrolladores han utilizado PHP para crear extensiones en proceso para agregar características, funcionalidades, servicios e integraciones a Adobe Commerce. Al crear aplicaciones con extensibilidad fuera de proceso, en lugar de extensiones, puede evitar problemas de compatibilidad.

Los siguientes recursos proporcionan un punto de partida para que los nuevos usuarios se familiaricen con las aplicaciones:

### Recursos de Commerce

- [Configuración de eventos de I/O para Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/)
- [Configuración de eventos para Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [Configuración del SDK de IU de administración](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [Conversión de una extensión en una aplicación](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### Recursos del Generador de aplicaciones

- [Información general sobre Commerce App Builder](https://developer.adobe.com/commerce/extensibility/app-development/)
- [Configuración de la malla de API para el Generador de aplicaciones de Adobe Developer](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [Implementación de aplicaciones de App Builder](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [CI/CD para aplicaciones de App Builder](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- Introducción a App Builder/Developer Console
   - [Introducción al Generador de aplicaciones](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [Explicación de proyectos y espacios de trabajo](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] credenciales

Antes de instalar una extensión comprada a [!DNL Commerce Marketplace], inicie sesión en su [!DNL Commerce] y compruebe que dispone de una clave de acceso activa. Puede iniciar sesión en su [!DNL Commerce] cuenta desde el encabezado de [[!DNL Marketplace]][1] o [Magento.com][6].

La clave de acceso es un conjunto de claves públicas y privadas que se utiliza para sincronizar su [!DNL Commerce] instalación con su [!DNL Commerce] y compruebe sus credenciales. Una vez sincronizada la cuenta, debe introducir la clave privada cada vez que instale una extensión o módulo desde Commerce Marketplace o actualice la cuenta [!DNL Commerce] instalación.

Puede crear varias claves de acceso para distintos fines y habilitarlas o deshabilitarlas según sea necesario. Sin embargo, debe utilizar la misma clave de acceso que se utilizó para instalar el [!DNL Commerce] software. Por ejemplo, no puede utilizar una clave de acceso de Magento Open Source para actualizar o actualizar Adobe Commerce, o a la inversa. Tampoco puede utilizar una clave de acceso que pertenezca a otro usuario o que sea de un [cuenta compartida](commerce-account-share.md).

### Creación de una clave de acceso

1. Inicie sesión en su [!DNL Commerce] cuenta.

1. En el _[!UICONTROL My Account]_, seleccione la **[!UICONTROL Marketplace]**pestaña.

1. En la esquina superior derecha junto a su nombre, haga clic en la flecha hacia abajo y elija **[!UICONTROL My Profile]**.

   ![Su [!DNL Marketplace] perfil](./assets/marketplace-profile.png){width="600"}

1. En el _[!UICONTROL Marketplace]_pestaña debajo de_[!UICONTROL My Products]_, haga clic en **[!UICONTROL Access Keys]** y, a continuación, siga uno de estos procedimientos:

   - Compruebe si ya tiene un conjunto de claves de acceso para sus compras en Marketplace. Puede crear varios conjuntos de claves de acceso para distintos fines.

   ![Claves de acceso](./assets/access-keys.png){width="600"}

   - Clic **[!UICONTROL Create a New Access Key]**. Introduzca un nombre para el nuevo par de claves y haga clic en **[!UICONTROL OK]**. Los caracteres válidos incluyen caracteres en mayúsculas y minúsculas y guiones en lugar de espacios.

1. Cuando termine, haga clic en **[!UICONTROL OK]**.

   La nueva clave de acceso está habilitada y aparece en la lista.

   Observe el _Copiar_ después de cada clave pública y privada. En el siguiente paso, copiará y pegará estos valores para sincronizar el almacén con Commerce Marketplace.

## Proceso de instalación

>[!IMPORTANT]
>
>A partir de Adobe Commerce y Magento Open Source 2.4.0, se quita el Asistente para instalación web y debe utilizar la línea de comandos para [instalar](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) o [actualización](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html) su instancia. Este requisito también incluye [módulos](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) y [extensiones](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

El proceso de instalación de [!DNL Marketplace] compras son diferentes para _on-premise_ instalaciones de Commerce que para instalaciones alojadas en [la arquitectura de Adobe Cloud][4].

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## Asistencia

Si necesita ayuda para instalar o utilizar una extensión, consulte primero la documentación que la acompaña. Si no encuentra la respuesta a su pregunta, utilice la información de contacto del listado de extensiones para ponerse en contacto directamente con el desarrollador. Si lo que compra en Marketplace no satisface sus necesidades, puede [solicitar un reembolso](#refund-requests) en un plazo de 25 días a partir de la fecha de compra. El Adobe revisa todas las solicitudes de reembolso y (si está aprobado) emite el reembolso correspondiente. Para ver los problemas de soporte relacionados con Commerce Marketplace, consulte la [[!DNL Marketplace] Centro de ayuda][5].

### Problemas de cierre de compra

Los campos de dirección del perfil de su cuenta deben rellenarse con fines de verificación en el sistema de compra de Marketplace.

1. Añada los campos de dirección en el perfil de cuenta de Marketplace.
1. Guarde el perfil actualizado.
1. Continúe con el cierre de compra.

### Problemas de inicio de sesión

Los problemas de inicio de sesión suelen estar relacionados con una discrepancia entre el MAGEID y la dirección de correo electrónico en la base de datos de cuentas. Póngase en contacto con Asistencia de Marketplace para obtener ayuda.

>[!INFO]
>
>Las compras de aplicaciones y extensiones no se pueden [transferido](#purchase-transfers) a una nueva cuenta.

### Preguntas de código abierto

El equipo de asistencia de Marketplace resuelve los problemas relacionados con la [commercemarketplace.adobe.com/](https://commercemarketplace.adobe.com/) y [commerce.developer.adobe.com/](https://commercedeveloper.adobe.com/) solo sitios. Dirija sus preguntas sobre el Magento Open Source a [Foro de la comunidad](https://community.magento.com/) o [póngase en contacto con un socio](https://business.adobe.com/products/magento/partners.html) que pueden ayudar con el Magento Open Source.

### Solicitudes de reembolso

Para solicitar un reembolso por una compra en Marketplace, inicia sesión en tu cuenta y sigue estos pasos:

1. Clic [!UICONTROL **Mi perfil**] > [!UICONTROL **Historial de compra**].
1. Busque la compra y haga clic en [!UICONTROL **Solicitar un reembolso**].
1. Complete el formulario de solicitud de reembolso.

El soporte de Marketplace solicitará información una vez generada la solicitud de reembolso. La opción de reembolso está disponible durante 25 días después de la fecha de compra. Consulte la [Contrato de cliente de Marketplace](https://www.adobe.com/legal/terms/enterprise-licensing/magento-legacy-terms.html).

### Facturas del pedido

Puede descargar facturas de pedidos desde [!UICONTROL **Historial de compra**] en su cuenta de Marketplace. La factura no proporciona el IVA o la dirección del vendedor porque no es un requisito del mercado en este momento.

Para descargar una factura de pedido para una compra de Marketplace, inicie sesión en su cuenta de Marketplace y siga estos pasos:

1. Clic [!UICONTROL **Mi perfil**] > [!UICONTROL **Historial de compra**].
1. Busque la compra.
1. Haga clic en el icono de impresora en la esquina superior derecha del pedido.

### Transferencias de compra

El equipo de soporte de Marketplace no tiene la capacidad de transferir compras a una cuenta diferente. Debe adquirir todas las aplicaciones y extensiones en la cuenta principal de Commerce para evitar problemas de instalación e implementación. Adobe Commerce tiene derecho a un identificador único. Dado que Composer se utiliza para la instalación, solo se necesita un conjunto de [claves de acceso](#create-an-access-key) vinculado a la cuenta principal se puede utilizar. La única solución disponible es [solicitar un reembolso](#refund-requests) desde la cuenta de compra de Marketplace (si lo permite la política de reembolsos de Adobe Commerce).

Puede [compartir](commerce-account-share.md) Cree una instancia de Commerce a través de la cuenta principal. El acceso compartido concede permisos especiales a una cuenta subordinada desde una cuenta principal. El punto de acceso compartido se genera desde la cuenta principal. La cuenta principal puede ser la cuenta de Commerce, la cuenta de comerciante principal o una cuenta compartida dentro de una organización.

Estos permisos especiales otorgan el mismo nivel de acceso en Adobe Commerce que el principal; sin embargo, no se transfieren al mercado de Adobe Commerce ni al portal para desarrolladores. Esto significa que la compra de una extensión desde una cuenta subordinada en Marketplace no se puede compartir con la cuenta principal. El acceso compartido es una calle unidireccional (cuenta principal a subordinada). No funciona cuando una cuenta subordinada intenta volver a compartir con la principal.

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[5]: https://marketplacesupport.magento.com/hc/en-us
[6]: https://business.adobe.com/products/magento/magento-commerce.html
