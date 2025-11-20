---
title: Preparación para HIPAA en Adobe Commerce
description: Descubra cómo puede añadir la extensión de preparación para HIPAA de Adobe Commerce y obtener funciones y funcionalidades adicionales que le permiten cumplir con sus obligaciones HIPAA.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: afb6b4ca31675f6e549282749ef032ef1cd2f9f9
workflow-type: tm+mt
source-wordcount: '2391'
ht-degree: 1%

---

# Preparación para HIPAA en Adobe Commerce

{{ee-feature}}

>[!IMPORTANT]
>
>**Descargo de responsabilidad legal**<br/>
>Esta información está diseñada para ayudar a los clientes de Adobe a responder a sus preguntas sobre los servicios preparados para HIPAA de Adobe. No constituye asesoramiento jurídico. Los comerciantes deben consultar con su propio asesor legal para comprender sus obligaciones según HIPAA y el uso y la configuración adecuados de los productos de Adobe.

>[!BEGINSHADEBOX]

**Ley de Portabilidad y Responsabilidad del Seguro de Salud (HIPAA)**

La Ley de Portabilidad y Responsabilidad del Seguro de Salud (HIPAA, por sus siglas en inglés) es la ley federal clave de privacidad de la atención médica en Estados Unidos y es aplicada por el Departamento de Salud y Servicios Humanos (HHS, por sus siglas en inglés) de Estados Unidos. La HIPAA se aplica a _Entidades cubiertas_ (como proveedores de atención médica, aseguradoras y cámaras de compensación) y a _Asociados de negocios_ (como las entidades que brindan servicios a entidades cubiertas). Los requisitos de HIPAA se establecen en tres reglas independientes: Regla de privacidad, Regla de seguridad y Regla de notificación de infracciones. Adobe actúa como socio comercial para determinados productos, que Adobe clasifica como &quot;servicios preparados para HIPAA&quot;. Los datos regulados por la HIPAA se denominan _Información médica protegida_ o PHI. La PHI es un subconjunto de información de salud que (1) es creada o recibida por un proveedor de atención médica, un plan de salud o un centro de intercambio de información de atención médica, (2) se relaciona con la salud física o mental o la condición pasada, presente o futura de un individuo, la prestación de atención médica a un individuo, o el pago pasado, presente o futuro por la prestación de atención médica a un individuo, y (3) identifica al individuo o con respecto al cual hay una base razonable para creer que la información puede usarse para identificar al individuo. Las Reglas de Privacidad y Seguridad de la HIPAA requieren que una Entidad Cubierta obtenga garantías por escrito de un Asociado Comercial en forma de un Contrato de Asociado Comercial, o BAA, que requiere que el Asociado Comercial salvaguarde la privacidad y seguridad de la PHI de la Entidad Cubierta. Para obtener más información, consulte [HIPAA y productos y servicios de Adobe](https://www.adobe.com/trust/compliance/hipaa-hds/hipaa-ready.html) en el Centro de confianza de Adobe.

>[!ENDSHADEBOX]

## Adobe Commerce compatible con HIPAA

La extensión compatible con HIPAA de Adobe Commerce agrega funciones y funcionalidades adicionales a las instalaciones de Adobe Commerce que permiten a los comerciantes cumplir con sus respectivas obligaciones HIPAA.

La extensión compatible con HIPAA de Adobe Commerce, `magento/hipaa-ee`, está disponible para Adobe Commerce en proyectos de infraestructura en la nube o Adobe Managed Services. El proceso de instalación de Adobe Commerce compatible con HIPAA deshabilita algunos servicios y funciones nativos para cumplir con los requisitos de HIPAA. Ver [Servicios y características deshabilitados](#disabled-services-and-features).

>[!NOTE]
>
>El acceso a las funciones y funcionalidades preparadas para HIPAA solo está disponible para los comerciantes que han adquirido el complemento de atención médica para Adobe Commerce.

*Estos materiales están destinados únicamente a fines informativos. El suministro de esta información no da derecho al destinatario a ningún derecho contractual o de otro tipo. Si bien se han hecho esfuerzos para garantizar la exactitud de la información en la fecha en que se ha proporcionado, no se afirma que esa información sea exacta y completa. Adobe no se compromete a actualizar esta información a medida que cambie la ley o los productos de Adobe. Además, este documento no se debe distribuir a ninguna otra parte que no sea el destinatario deseado sin el consentimiento por escrito de Adobe.*

## Requisitos del sistema

La siguiente tabla muestra la compatibilidad entre las versiones de Adobe Commerce y la extensión compatible con HIPAA:

| Adobe Commerce | Admitido | Notas |
|----------------|-----------|-------|
| 2.4.7-p4 y posterior | 1.2.0 | La compatibilidad con 2.4.7-p4 requiere [revisión](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-27147) |
| 2.4.6-p9 - 2.4.6-p10 | 1.2.0 | |
| 2.4.6-p8 | 1.1.0 | La compatibilidad con [servicios de datos](#adobe-commerce-services) se introdujo en 1.1.0 |
| 2.4.6-p3 - 2.4.6-p7 | 1.0.0 | |

>[!IMPORTANT]
>
>- La extensión compatible con HIPAA solo está disponible para proyectos de Adobe Commerce en la nube o Adobe Commerce Managed Services.
>- La extensión está disponible como un metapaquete de Compositor en `repo.magento.com`.
>- El acceso a las funciones y características preparadas para HIPAA requiere el complemento de atención médica de Adobe Commerce.
>- Las versiones beta de Adobe Commerce no son compatibles.

## Instalación

**Requisito previo**

>[!BEGINSHADEBOX]

- Adobe ha aprovisionado su cuenta de Adobe Commerce para acceder a la extensión HIPAA Ready.
- Acceda a [repo.magento.com](https://repo.magento.com) para instalar la extensión. Para obtener la generación de claves y los derechos necesarios, consulta [Obtener tus claves de autenticación](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

>[!ENDSHADEBOX]

Instale la última versión de la extensión de servicios preparados para HIPAA de Adobe (`magento/hipaa-ee`) en una instancia que ejecute Adobe Commerce versión 2.4.7-p5 o 2.4.6-p3 a través de 2.4.6-p8. La extensión se entrega como un metapaquete de composición desde el repositorio [repo.magento.com](https://repo.magento.com). El metapaquete incluye la colección de módulos que habilitan las capacidades HIPAA para una instancia de Adobe Commerce.

>[!NOTE]
>
>Para asegurarse de que los datos de evento de back office enviados a Experience Platform están preparados para HIPAA, consulte la [guía de extensión de conexión de datos](https://experienceleague.adobe.com/en/docs/commerce/data-connection/fundamentals/install#install-the-data-services-hipaa-extension).

1. En la estación de trabajo local, cambie al directorio del proyecto para su proyecto de Adobe Commerce en la nube.

   >[!NOTE]
   >
   >Para obtener información sobre cómo administrar los entornos de proyecto de Commerce localmente, consulte [Administración de ramas con la CLI](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/cli-branches) en la _Guía del usuario de Adobe Commerce on Cloud Infrastructure_.

1. Compruebe la rama de entorno que desea actualizar mediante la CLI de Adobe Commerce Cloud.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Agregue el metapaquete `magento/hipaa-ee` a la configuración del compositor mediante la CLI del compositor.

   ```shell
   composer require "magento/hipaa-ee" --no-update
   ```

1. Actualizar dependencias del paquete.

   ```shell
   composer update "magento/hipaa-ee"
   ```

1. Añada, confirme e inserte el código actualizado en el entorno de la nube.

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

   Al insertar las actualizaciones, se inicia el [proceso de implementación en la nube de Commerce](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/deploy/process) para aplicar los cambios. Compruebe el estado de implementación desde el [registro de implementación](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/test/log-locations).

### Verificar instalación

Una vez implementadas las actualizaciones, compruebe que la extensión `Hipaa*` esté instalada

1. Utilice SSH para iniciar sesión en el entorno remoto de la nube.

   ```shell
   magento-cloud ssh
   ```

1. Desde la línea de comandos, utilice la CLI de Adobe Commerce para comprobar el estado del módulo.

   ```shell
   bin/magento module:status
   ```

1. Compruebe que los módulos HIPAA están incluidos en la lista de módulos habilitados:

   ```text
   List of enabled modules:
   <truncated for brevity>
   Magento_HipaaAnalytics
   Magento_HipaaCheckout
   Magento_HipaaLogging
   Magento_HipaaScheduledImportExport
   Magento_HipaaAdminLogging
   Magento_HipaaCustomerLogging
   Magento_HipaaNewsletter
   Magento_HipaaImportExport
   Magento_HipaaApiLogging
   Magento_HipaaSales
   Magento_HipaaCustomer
   <truncated for brevity>
   ```

   Todos los módulos con el prefijo `Magento_Hipaa` deben estar en la sección de módulos habilitados.

## Mejoras de funciones para la preparación para HIPAA

La extensión `magento/hipaa-ee` introduce algunos cambios y mejoras en el producto base de Commerce. Las secciones siguientes proporcionan detalles sobre estos cambios y cómo modifican el producto base.

### Registros de acciones

El registro de auditoría es un requisito de HIPAA. En Adobe Commerce, la característica [Registros de acciones](../../systems/action-log.md) registra todos los cambios realizados por un usuario administrador que trabaja en su tienda. Para cumplir los requisitos de la HIPAA para el registro de auditoría, la función se ha actualizado para registrar todas las acciones de los usuarios y clientes administradores realizadas a través de la IU de administración y mediante llamadas a la API.

Los registros de acciones también capturan eventos cuando los servicios de Adobe acceden a los datos de su tienda. Estos eventos se pueden identificar filtrando por la acción &quot;Datos enviados fuera&quot; del informe Registros de acciones.

#### Informe Registros de acciones

La cuadrícula del informe _Registros de acciones_ (**[!UICONTROL System]** > Registros de acciones > Informe) se ha modificado para que se ajuste a las acciones de los clientes realizadas a través de la IU de administración y la API.

1. Se agregaron dos columnas:
   - ***Source***: Muestra dónde se realizó la acción.
Valores: `Admin UI` | `Customer UI` | `REST API` | `SOAP API` | `GraphQL API`
   - ***Tipo de cliente***: Muestra el tipo de cliente.
Valores: Cliente | Administrador | Integración

2. Se cambió el nombre de la columna ***Nombre de usuario*** a ***Identificador de cliente***
   - ***Identificador de cliente***: muestra el identificador de inicio de sesión del usuario que realizó la acción.
Valores:
      - un mensaje de correo electrónico si el tipo de cliente es Cliente
      - un nombre de usuario si el tipo de cliente es Admin
      - un nombre si el Tipo de cliente es Integración

3. Se cambió el nombre de la columna ***Nombre de acción completa*** a ***Destino***
   - ***Target***: muestra el nombre de la acción.
Valores:
      - un punto final si Source es una API de REST o una API de SOAP
      - un nombre de consulta o mutación si hay una API de GraphQL
      - un nombre de acción si se trata de una IU de administración o de una IU de cliente.

#### Configurar acciones de administración para el registro

Esta función no está disponible porque todas las acciones deben registrarse de forma predeterminada.

### Restricción de resultados de búsqueda del cliente HIPAA

La funcionalidad de restricción de resultados de búsqueda del cliente de HIPAA en Adobe Commerce garantiza el cumplimiento de las regulaciones de HIPAA al limitar el acceso a la información médica protegida (PHI) y a la información de identificación personal (PII). Esta función restringe la capacidad de buscar y ver registros de clientes en función de los roles de usuario, lo que garantiza que solo los usuarios autorizados puedan acceder a esta información.

#### Características principales

- **Restricciones de búsqueda**: los usuarios sin los roles necesarios no pueden buscar ni ver registros de clientes.
- **Búsqueda obligatoria de acceso**: a diferencia del comportamiento predeterminado de Adobe Commerce, no es posible ver la información del cliente sin realizar una búsqueda. Esto garantiza que los usuarios deben conocer los detalles específicos de un cliente para localizar su información.
- **Resultados de búsqueda limitados**: los resultados de búsqueda que coinciden con los criterios están limitados a 10 registros, lo que garantiza que solo se muestre un número manejable de registros a la vez.
- **Cantidad mínima de filtros**: los usuarios deben aplicar un mínimo de tres filtros (por ejemplo, correo electrónico, apellidos y estado) para realizar una búsqueda, asegurándose de que las búsquedas sean específicas y específicas.
- **Notificaciones de filtro**: cuando las restricciones de búsqueda están habilitadas, se notifica a los usuarios que apliquen filtros para restringir los resultados de búsqueda.

#### Configuración

La configuración para limitar el número de clientes en los resultados de búsqueda se encuentra en el panel de administración en **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Advanced]** > **[!UICONTROL Admin]** > **[!UICONTROL Admin Grids]**. Esta configuración está habilitada de manera predeterminada cuando se instala la extensión `hipaa-ee`.

- **Limitar número de clientes en la cuadrícula**: esta configuración le permite habilitar o deshabilitar la limitación del número de clientes mostrados en los resultados de búsqueda de la cuadrícula.
- **Límite de resultados de búsqueda de cuadrícula de cliente**: esta configuración especifica el número máximo de registros de cliente que se pueden mostrar en los resultados de búsqueda de cuadrícula.

#### Áreas funcionales afectadas

La funcionalidad de restricción de resultados de búsqueda se aplica a las cuadrículas de clientes de la página Administración: Crear pedido (**[!UICONTROL Sales]** > **[!UICONTROL Orders]** > **[!UICONTROL Create New Order]**) y a la página Clientes (**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**).

- Los filtros se abren de forma predeterminada.
- Los usuarios deben aplicar un mínimo de tres filtros para realizar una búsqueda.
- De forma predeterminada, los resultados de búsqueda están limitados a 10 registros.
- Si hay más registros que coincidan con los criterios de búsqueda, las notificaciones informan a los usuarios sobre el límite de resultados y la necesidad de refinar la búsqueda.
- La paginación de cuadrícula no está disponible.
- Los resultados de búsqueda anteriores y los filtros aplicados no se guardan al salir de la página.

La funcionalidad de restricción de resultados de búsqueda también se aplica a la API de REST para la búsqueda de clientes (`/V1/customers/search`).

- Sin filtros aplicados o con filtros insuficientes, la API devuelve un mensaje de error que indica que se necesita el número requerido de filtros para realizar una búsqueda.
- Los usuarios autorizados que apliquen filtros suficientes reciben resultados de la API dentro del límite especificado.
- Cuando los resultados son limitados, se agrega un mensaje a la respuesta que indica el número total de registros encontrados y el límite aplicado actual.

### Importar y exportar funciones

Las mejoras en las funciones de importación y exportación se centran en mejorar la experiencia administrativa y proporcionar una mejor visibilidad de las acciones de los usuarios.

>[!NOTE]
>
>Estas ***mejoras no modifican la lógica principal de importación y exportación***, sino que amplían la funcionalidad para ofrecer un registro más completo y una atribución de datos mejorada. La funcionalidad fundamental de importación y exportación permanece sin cambios. Los usuarios pueden seguir utilizando las funciones y los flujos de trabajo existentes sin sufrir interrupciones.

#### Registro de acciones administrativas

Una de las principales mejoras de las funciones de importación y exportación es el registro mejorado de las acciones administrativas. Esta mejora introduce la capacidad de profundizar en las actividades asociadas con la importación y exportación de datos, lo que contribuye a mejorar el seguimiento y la auditabilidad. Las siguientes acciones ahora se registran y reflejan en la cuadrícula **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**:

| Tipo | Acciones |
| ---- | ------- |
| Importar | <ul><li>Un usuario administrador ejecuta una importación<li>Un usuario administrador descarga un archivo importado<li>Un usuario administrador descarga un archivo de error<ul/> |
| Exportar | <ul><li>Un usuario administrador solicita<li>Un usuario administrador descarga un archivo exportado<ul/> |
| Importaciones y exportaciones programadas | <ul><li>Un usuario administrador programa la exportación<li>Un usuario administrador edita una exportación programada<li>Un usuario administrador ejecuta una exportación programada<li>Un usuario administrador elimina una exportación programada<li>Un usuario administrador programa una importación<li>Un usuario administrador edita una importación programada<li>Un usuario administrador ejecuta una importación programada<li>Un usuario administrador elimina una importación programada<li>Un usuario administrador ejecuta una eliminación en lotes de operaciones de importación y exportación<ul/> |

### Mejoras de visualización, filtrado y ordenación mejorados

Para proporcionar a los usuarios administradores cuadrículas más informativas, el servicio HIPAA-Ready proporciona varias mejoras para mostrar, filtrar y ordenar datos.

#### Historial de importación ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- Se habilitó el filtrado para todas las columnas excepto para **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]** y **[!UICONTROL Summary]**.

#### Exportar ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- Se agregó una columna **[!UICONTROL ID]**.
- Se agregó una columna **[!UICONTROL Requested At]** (_fecha y hora en que se solicitó la exportación_).
- Se agregó una columna **[!UICONTROL User]** (_nombre de usuario de un administrador que realizó la solicitud_).
- Se eliminó una columna **[!UICONTROL Action]**.
- Se ha movido el vínculo **[!UICONTROL Download]** a una columna **[!UICONTROL File name]** (_como la cuadrícula Historial de importación_).
- Se deshabilitó la acción responsable de la eliminación de un archivo exportado (_para mejorar el seguimiento_).
- Se habilitó la ordenación para todas las columnas excepto **[!UICONTROL File name]**.
- Se habilitó el filtrado para todas las columnas.

#### Importaciones y exportaciones programadas ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- Se agregó una columna **[!UICONTROL ID]**.
- Se agregó una columna **[!UICONTROL Scheduled At]** (la _fecha y hora en que se programó la importación o exportación_).
- Se agregó una columna **[!UICONTROL User]** (el _nombre de usuario de un usuario administrador que programó la importación o exportación_).

## Servicios y herramientas preparados para HIPAA

En esta sección se describen los servicios de Adobe preparados para HIPAA que están disponibles para su uso con la oferta HIPAA para Adobe Commerce. También describe las herramientas que puede utilizar para supervisar los controles clave de seguridad y cumplimiento normativo de su tienda.

| Servicio | Producción | Ensayo | staging_for_support | Desarrollo |
|---------------------------------------|------------|---------|---------------------|-------------|
| Adobe Commerce con el complemento para atención sanitaria | Sí | Sí | Sí | No |
| SendGrid | No | No | No | No |
| AWS Simple Email Service | Sí | Sí | Sí | No |

### Servicios de Adobe Commerce

La siguiente tabla identifica los servicios de Adobe Commerce disponibles para la oferta de preparación para HIPAA. Estos servicios incluyen, entre otros:

| Servicio | No producción | Producción |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|------------|
| [Adobe Developer App Builder](https://developer.adobe.com/app-builder/docs/intro_and_overview/) | Sí | Sí |
| [Malla de API para Adobe Developer App Builder](https://developer.adobe.com/graphql-mesh-gateway/) | Sí | Sí |
| [Exportación De Datos SaaS](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview) | Sí | Sí |
| [Búsqueda en directo](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview) | No | No |
| [Recomendaciones de productos](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/overview) | No | No |
| [Servicios de pago](https://experienceleague.adobe.com/en/docs/commerce/payment-services/guide-overview) | No | No |
| [Eventos de Back Office de conexión de datos](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice) | Sí | Sí |
| [Eventos de tienda de conexión de datos](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#storefront-events) | No | No |
| [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) | No | No |

### Herramientas

[Security Scan Tool](../../systems/security-scan.md) para Adobe Commerce le ayuda a supervisar su tienda para asegurarse de que todos los controles de seguridad necesarios estén activados y en funcionamiento. Además de las comprobaciones de seguridad estándar, Adobe ha mejorado la herramienta para mostrar las comprobaciones específicas de HIPAA para los clientes que utilizan la oferta HIPAA para Adobe Commerce. Las comprobaciones HIPAA en el Security Scan Tool están diseñadas para garantizar que:

- Los módulos de auditoría no están desactivados
- La autenticación de doble factor (2FA) no está deshabilitada
- Las funciones de marketing están desactivadas
- Todas las extensiones instaladas coinciden con una lista de permitidos predefinida
- No hay servicios de Adobe instalados que no sean compatibles

Puedes [configurar la herramienta](../../systems/security-scan.md#run-a-security-scan) para enviarte notificaciones por correo electrónico con detalles de análisis programados o [informes de visualización manual](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/launch/overview).

## Funciones desactivadas

Para cumplir con los requisitos de HIPAA, algunas funciones admitidas por Adobe Commerce no están disponibles o están desactivadas de forma predeterminada. Los comerciantes tienen la opción de volver a activar o utilizar estas funciones bajo su propia responsabilidad.

Las siguientes funciones están deshabilitadas de forma predeterminada en el módulo de preparación para HIPAA. Los comerciantes pueden activar cualquiera de estas funciones bajo su propio riesgo.

- **[Correo electrónico transaccional](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/project/sendgrid)**: SendGrid está deshabilitado de forma predeterminada porque el servicio no está preparado para HIPAA. Adobe Commerce proporciona una opción de integración que puede usar con su propia cuenta de [AWS Simple Email Service](https://docs.aws.amazon.com/ses/). Póngase en contacto con el administrador de cuentas técnico del cliente o con la asistencia de Adobe Commerce para obtener más información.

- **[Cierre de compra para invitados](../../stores-purchase/checkout-guest.md)**: Esta función presenta un riesgo potencial para varios aspectos de HIPAA, como el registro, el control de acceso, la higiene y el linaje de la PHI y potencialmente más.

- **[Función de newsletter](../../merchandising-promotions/newsletters.md)**: esta función está deshabilitada para evitar que se utilice PHI en un contexto de marketing.

- **[Configuración del servicio de informes avanzados](../../getting-started/business-intelligence.md)**: esta configuración está deshabilitada para evitar que se use la PHI para análisis e informes.
