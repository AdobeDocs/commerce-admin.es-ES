---
title: '[!DNL Adobe Commerce Marketplace]'
description: Obtenga información acerca de [!DNL Commerce Marketplace], que ofrece a los comerciantes una selección revisada de soluciones y proporciona a los desarrolladores cualificados las herramientas, la plataforma y la ubicación privilegiada para crear un negocio próspero.
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1282'
ht-degree: 0%

---

# Adobe Commerce Marketplace

[Adobe Commerce Marketplace](https://marketplace.magento.com/) es la tienda de aplicaciones que ofrece a los comerciantes una selección revisada de soluciones y proporciona a los desarrolladores calificados las herramientas, la plataforma y la ubicación idónea para crear un negocio próspero. [!DNL Commerce Marketplace] ofrece una selección de extensiones disponibles de forma gratuita, así como otras que se encuentran a la venta. Las compras se pueden pagar con tarjeta de crédito o con [PayPal](https://www.paypal.com/us/home).

Todas las extensiones disponibles en [!DNL Commerce Marketplace] han pasado una revisión exhaustiva. El [Programa de calidad de extensión](https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/) (EQP) combina la experiencia de [!DNL Commerce], las directrices de desarrollo y las herramientas de verificación para garantizar que todas las extensiones de Commerce Marketplace cumplan los estándares de codificación y las prácticas recomendadas. El proceso de revisión incluye tanto una comprobación automatizada como una revisión manual del control de calidad. Durante el proceso, la estructura y el código de cada extensión se examinan y prueban para detectar pruebas de infección por virus/malware y cualquier indicio de plagio. La revisión incluye un examen técnico profundo y una comprobación de coherencia realizados por un ingeniero de [!DNL Commerce], que se centran en la documentación, la estructura de codificación, el rendimiento, la escalabilidad, la seguridad y la compatibilidad con el núcleo de [!DNL Commerce].

Aunque puede comprar extensiones de otras fuentes, solo las extensiones disponibles en [!DNL Commerce Marketplace] se verifican mediante una amplia revisión técnica y de marketing dentro del Programa de calidad de la extensión.

## Recursos de aplicación

Tradicionalmente, los desarrolladores han utilizado PHP para crear extensiones en proceso para agregar características, funcionalidades, servicios e integraciones a Adobe Commerce. Al crear aplicaciones con extensibilidad fuera de proceso, en lugar de extensiones, puede evitar problemas de compatibilidad.

Los siguientes recursos proporcionan un punto de partida para que los nuevos usuarios se familiaricen con las aplicaciones:

### Recursos de Commerce

- [Configuración de eventos de E/S para Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/)
- [Configuración de eventos para Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [Configurando SDK de IU de administración](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [Conversión de una extensión en una aplicación](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### Recursos de App Builder

- [Información general sobre Commerce App Builder](https://developer.adobe.com/commerce/extensibility/app-development/)
- [Configurando API Mesh para Adobe Developer App Builder](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [Implementando aplicaciones de App Builder](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [CI/CD para aplicaciones de App Builder](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- Introducción a App Builder/Developer Console
   - [Introducción a App Builder](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [Explicación de proyectos y espacios de trabajo](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## Credenciales de [!DNL Marketplace]

Para poder instalar una extensión adquirida en [!DNL Commerce Marketplace], inicie sesión en su cuenta de [!DNL Commerce] y compruebe que dispone de una clave de acceso activa. Puede iniciar sesión en su cuenta de [!DNL Commerce] desde el encabezado de [[!DNL Marketplace]](https://marketplace.magento.com/) o [Magento.com](https://business.adobe.com/products/magento/magento-commerce.html).

La clave de acceso es un conjunto de claves públicas y privadas que se usa para sincronizar la instalación de [!DNL Commerce] con la cuenta de [!DNL Commerce] y comprobar las credenciales. Una vez sincronizada la cuenta, debe escribir la clave privada cada vez que instale una extensión o módulo desde Commerce Marketplace o actualice la instalación de [!DNL Commerce].

Puede crear varias claves de acceso para distintos fines y habilitarlas o deshabilitarlas según sea necesario. Sin embargo, debe utilizar la misma clave de acceso que se utilizó para instalar el software [!DNL Commerce]. Por ejemplo, no puede utilizar una clave de acceso de Magento Open Source para actualizar o actualizar Adobe Commerce, o a la inversa. Tampoco puede usar una clave de acceso que pertenezca a otro usuario o que pertenezca a una [cuenta compartida](commerce-account-share.md).

### Creación de una clave de acceso

1. Inicie sesión en su cuenta de [!DNL Commerce].

1. En la página _[!UICONTROL My Account]_, elija la ficha **[!UICONTROL Marketplace]**.

1. En la esquina superior derecha junto a su nombre, haga clic en la flecha hacia abajo y elija **[!UICONTROL My Profile]**.

   ![Su perfil [!DNL Marketplace]](./assets/marketplace-profile.png){width="600"}

1. En la ficha _[!UICONTROL Marketplace]_en_[!UICONTROL My Products]_, haga clic en **[!UICONTROL Access Keys]** y, a continuación, siga uno de estos procedimientos:

   - Compruebe si ya tiene un conjunto de claves de acceso para sus compras en Marketplace. Puede crear varios conjuntos de claves de acceso para distintos fines.

   ![Claves de acceso](./assets/access-keys.png){width="600"}

   - Haga clic en **[!UICONTROL Create a New Access Key]**. Escriba un nombre para el nuevo par de claves y haga clic en **[!UICONTROL OK]**. Los caracteres válidos incluyen caracteres en mayúsculas y minúsculas y guiones en lugar de espacios.

1. Una vez finalizado, haga clic en **[!UICONTROL OK]**.

   La nueva clave de acceso está habilitada y aparece en la lista.

   Observe el vínculo _Copiar_ después de cada clave pública y privada. En el siguiente paso, copiará y pegará estos valores para sincronizar el almacén con Commerce Marketplace.

## Proceso de instalación

>[!IMPORTANT]
>
>A partir de Adobe Commerce y Magento Open Source 2.4.0, se eliminará el Asistente para instalación web y deberá usar la línea de comandos para [instalar](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) o [actualizar](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html) su instancia. Este requisito también incluye [módulos](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) y [extensiones](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

El proceso de instalación de [!DNL Marketplace] compras es diferente para _instalaciones locales_ de Commerce que para instalaciones hospedadas en [la arquitectura de nube de Adobe](https://www.adobe.com/commerce/magento/enterprise.html).

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## Asistencia

Si necesita ayuda para instalar o utilizar una extensión, consulte primero la documentación que la acompaña. Si no encuentra la respuesta a su pregunta, utilice la información de contacto del listado de extensiones para ponerse en contacto directamente con el desarrollador. Si lo que compras en Marketplace no satisface tus necesidades, puedes [solicitar un reembolso](#refund-requests) en un plazo de 25 días a partir de la fecha de compra. Adobe revisa todas las solicitudes de reembolso y (si está aprobado) emite el reembolso correspondiente. Para problemas relacionados con Commerce Marketplace:

Método 1: enviar una solicitud de soporte técnico desde el formulario [Adobe Commerce Marketplace - Contáctenos](https://commercemarketplace.adobe.com/contact-us/).

Método 2: [Compatibilidad con correo electrónico](mailto:commercemarketplacesupport@adobe.com).

### Problemas de cierre de compra

Los campos de dirección del perfil de su cuenta deben rellenarse con fines de verificación en el sistema de compra de Marketplace.

1. Añada los campos de dirección en el perfil de cuenta de Marketplace.
1. Guarde el perfil actualizado.
1. Continúe con el cierre de compra.

### Problemas de inicio de sesión

Los problemas de inicio de sesión suelen estar relacionados con una discrepancia entre el MAGEID y la dirección de correo electrónico en la base de datos de cuentas. Póngase en contacto con Asistencia de Marketplace para obtener ayuda.

>[!INFO]
>
>Las compras de aplicaciones y extensiones no se pueden [transferir](#purchase-transfers) a una cuenta nueva.

### Preguntas de código abierto

El equipo de soporte técnico de Marketplace resuelve problemas relacionados únicamente con los sitios [commerce.adobe.com/](https://commercemarketplace.adobe.com/) y [commerce.developer.adobe.com/](https://commercedeveloper.adobe.com/). Envíe sus preguntas sobre Magento Open Source al [Foro de la comunidad](https://community.magento.com/) o [póngase en contacto con un socio](https://business.adobe.com/products/magento/partners.html) que pueda ayudarle con Magento Open Source.

### Solicitudes de reembolso

Para solicitar un reembolso por una compra en Marketplace, inicia sesión en tu cuenta y sigue estos pasos:

1. Haga clic en [!UICONTROL **Mi perfil**] > [!UICONTROL **Historial de compras**].
1. Busque la compra y haga clic en [!UICONTROL **Solicitar un reembolso**].
1. Complete el formulario de solicitud de reembolso.

El soporte de Marketplace solicitará información una vez generada la solicitud de reembolso. La opción de reembolso está disponible durante 25 días después de la fecha de compra. Consulte el [Contrato de cliente de Marketplace](https://www.adobe.com/legal/terms/enterprise-licensing/magento-legacy-terms.html).

### Facturas del pedido

Puede descargar facturas de pedidos del [!UICONTROL **Historial de compras**] en su cuenta de Marketplace. La factura no proporciona el IVA o la dirección del vendedor porque no es un requisito del mercado en este momento.

Para descargar una factura de pedido para una compra de Marketplace, inicie sesión en su cuenta de Marketplace y siga estos pasos:

1. Haga clic en [!UICONTROL **Mi perfil**] > [!UICONTROL **Historial de compras**].
1. Busque la compra.
1. Haga clic en el icono de impresora en la esquina superior derecha del pedido.

### Transferencias de compra

El equipo de soporte de Marketplace no tiene la capacidad de transferir compras a una cuenta diferente. Debe adquirir todas las aplicaciones y extensiones en la cuenta principal de Commerce para evitar problemas de instalación e implementación. Adobe Commerce tiene derecho a un identificador único. Dado que Composer se usa para la instalación, solo se puede usar un conjunto de [claves de acceso](#create-an-access-key) vinculadas a la cuenta principal. La única solución disponible es [solicitar un reembolso](#refund-requests) de la cuenta de compra de Marketplace (si lo permite la política de reembolsos de Adobe Commerce).

Puede [compartir](commerce-account-share.md) una instancia de Commerce a través de la cuenta principal. El acceso compartido concede permisos especiales a una cuenta subordinada desde una cuenta principal. El punto de acceso compartido se genera desde la cuenta principal. La cuenta principal puede ser la cuenta de Commerce, la cuenta de comerciante principal o una cuenta compartida dentro de una organización.

Estos permisos especiales otorgan el mismo nivel de acceso en Adobe Commerce que el principal; sin embargo, no se transfieren al mercado de Adobe Commerce ni al portal para desarrolladores. Esto significa que la compra de una extensión desde una cuenta subordinada en Marketplace no se puede compartir con la cuenta principal. El acceso compartido es una calle unidireccional (cuenta principal a subordinada). No funciona cuando una cuenta subordinada intenta volver a compartir con la principal.
