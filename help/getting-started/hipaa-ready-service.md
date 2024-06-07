---
title: Preparación para HIPAA en Adobe Commerce
description: Descubra cómo puede añadir la extensión de preparación para HIPAA de Adobe Commerce y obtener funciones y funcionalidades adicionales que le permiten cumplir con sus obligaciones HIPAA.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: b7ce092f843992b1e4d0ca23981c70d854ded5f9
workflow-type: tm+mt
source-wordcount: '1570'
ht-degree: 1%

---

# Preparación para HIPAA en Adobe Commerce

>[!IMPORTANT]
>
>**Descargo de responsabilidad legal**<br/>
>Esta información está pensada para ayudar a los clientes de Adobe a responder a sus preguntas sobre los servicios preparados para HIPAA de Adobe. No constituye asesoramiento jurídico. Los comerciantes deben consultar con su propio asesor legal para comprender sus obligaciones bajo HIPAA y el uso y la configuración apropiados de los productos de Adobe.

>[!BEGINSHADEBOX]

**Ley de Portabilidad y Responsabilidad del Seguro de Salud (HIPAA)**

La Ley de Portabilidad y Responsabilidad del Seguro de Salud (HIPAA, por sus siglas en inglés) es la ley federal clave de privacidad de la atención médica en Estados Unidos y es aplicada por el Departamento de Salud y Servicios Humanos (HHS, por sus siglas en inglés) de Estados Unidos. La HIPAA se aplica a _Entidades cubiertas_ (como proveedores de atención médica, aseguradoras y cámaras de compensación) y _Asociados empresariales_ (como las entidades que prestan servicios a las entidades cubiertas). Los requisitos de HIPAA se establecen en tres reglas independientes: Regla de privacidad, Regla de seguridad y Regla de notificación de infracciones. Adobe actúa como Asociado Comercial para ciertos productos, que Adobe clasifica como &quot;Servicios preparados para HIPAA&quot;. Los datos regulados por la HIPAA se denominan _Información médica protegida_ o PHI. La PHI es un subconjunto de información de salud que (1) es creada o recibida por un proveedor de atención médica, un plan de salud o un centro de intercambio de información de atención médica, (2) se relaciona con la salud física o mental o la condición pasada, presente o futura de un individuo, la prestación de atención médica a un individuo, o el pago pasado, presente o futuro por la prestación de atención médica a un individuo, y (3) identifica al individuo o con respecto al cual hay una base razonable para creer que la información puede usarse para identificar al individuo. Las Reglas de Privacidad y Seguridad de la HIPAA requieren que una Entidad Cubierta obtenga garantías por escrito de un Asociado Comercial en forma de un Contrato de Asociado Comercial, o BAA, que requiere que el Asociado Comercial salvaguarde la privacidad y seguridad de la PHI de la Entidad Cubierta. Para obtener más información, consulte [HIPAA y productos y servicios de Adobe](https://www.adobe.com/trust/compliance/hipaa-ready.html) en el Centro de confianza de Adobe.

>[!ENDSHADEBOX]

## Adobe Commerce compatible con HIPAA

La extensión compatible con HIPAA de Adobe Commerce agrega funciones y funcionalidades adicionales a las instalaciones de Adobe Commerce que permiten a los comerciantes cumplir con sus respectivas obligaciones HIPAA.

La extensión compatible con HIPAA de Adobe Commerce, `magento/hipaa-ee` está disponible para Adobe Commerce en proyectos de infraestructura en la nube o de Adobe Managed Services. El proceso de instalación de Adobe Commerce compatible con HIPAA deshabilita algunos servicios y funciones nativos para cumplir con los requisitos de HIPAA. Consulte [Servicios y funciones desactivados](#disabled-services-and-features).

>[!NOTE]
>
>El acceso a las funciones y funcionalidades preparadas para HIPAA solo está disponible para los comerciantes que han adquirido el complemento de atención médica para Adobe Commerce.

*Estos materiales están destinados únicamente a fines informativos. El suministro de esta información no da derecho al destinatario a ningún derecho contractual o de otro tipo. Si bien se han hecho esfuerzos para garantizar la exactitud de la información en la fecha en que se ha proporcionado, no se afirma que esa información sea exacta y completa. Adobe no se compromete a actualizar esta información a medida que cambie la ley o los productos del Adobe. Además, este documento no se debe distribuir a ninguna parte que no sea el destinatario deseado sin el consentimiento por escrito del Adobe.*

## Requisitos del sistema

Adobe Commerce debe implementarse en Adobe Commerce en la infraestructura en la nube o en Adobe Commerce Managed Services con la versión 2.4.6-p3 o posterior (sin versiones beta).

## Instalación

**Requisito previo**

>[!BEGINSHADEBOX]

- El Adobe ha aprovisionado su cuenta de Adobe Commerce para acceder a la extensión HIPAA Ready.
- Acceso a [repo.magento.com](https://repo.magento.com) para instalar la extensión de. Para obtener la generación de claves y los derechos necesarios, consulte [Obtener las claves de autenticación](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

>[!ENDSHADEBOX]

Instale la última versión de la extensión de servicios preparados para HIPAA de Adobe (`magento/hipaa-ee`) en una instancia que ejecute Adobe Commerce versión 2.4.6-p3 o posterior. La extensión se entrega como un metapaquete de compositor desde el [repo.magento.com](https://repo.magento.com) repositorio. El metapaquete incluye la colección de módulos que habilitan las capacidades HIPAA para una instancia de Adobe Commerce.

1. En la estación de trabajo local, cambie al directorio del proyecto para su proyecto de Adobe Commerce en la nube.

   >[!NOTE]
   >
   >Para obtener información sobre la administración local de entornos de proyecto de Commerce, consulte  [Administración de ramas con CLI](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) en el _Guía del usuario de Adobe Commerce sobre infraestructura en la nube_.

1. Compruebe la rama de entorno que desea actualizar mediante la CLI de Adobe Commerce Cloud.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Añadir el metapaquete `magento/hipaa-ee` a la configuración del compositor mediante la CLI del compositor.

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

   Al insertar las actualizaciones, se inicia el [Proceso de implementación de Commerce Cloud](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) para aplicar los cambios. Compruebe el estado de implementación desde el [implementar registro](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

### Verificar instalación

Una vez implementadas las actualizaciones, compruebe que la variable `Hipaa*` La extensión está instalada

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
   <truncated for brevity>
   ```

   Todos los módulos con el prefijo `Magento_Hipaa` debe estar en la sección módulos habilitados.

## Mejoras de funciones para la preparación para HIPAA

El `magento/hipaa-ee` La extensión de introduce algunos cambios y mejoras en el producto base de Commerce. Las secciones siguientes proporcionan detalles sobre estos cambios y cómo modifican el producto base.

### Registros de acciones

El registro de auditoría es un requisito de HIPAA. En Adobe Commerce, la variable [Registros de acciones](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) registra todos los cambios realizados por un usuario administrador que trabaje en su tienda. Para cumplir los requisitos de la HIPAA para el registro de auditoría, la función se ha actualizado para registrar todas las acciones de los usuarios y clientes administradores realizadas a través de la IU de administración y mediante llamadas a la API.

#### Informe Registros de acciones

El _Registros de acciones_ cuadrícula del informe (**[!UICONTROL System]** > Registros de acciones > Informe) se modifica para dar cabida a las acciones de los clientes realizadas a través de la IU de administración y la API.

1. Se agregaron dos columnas:
   - ***Origen***: Muestra dónde se realizó la acción.
Valores: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Tipo de cliente***: muestra el tipo de cliente.
Valores: Cliente | Administrador | Integración

2. Se ha cambiado el nombre ***Nombre de usuario*** columna a ***Identificador de cliente***
   - ***Identificador de cliente***: Muestra el ID de inicio de sesión del usuario que realizó la acción.
Valores:
      - un mensaje de correo electrónico si el tipo de cliente es Cliente
      - un nombre de usuario si el tipo de cliente es Admin
      - un nombre si el Tipo de cliente es Integración

3. Se ha cambiado el nombre ***Nombre completo de la acción*** columna a ***Target***
   - ***Target***: Muestra el nombre de la acción.
Valores:
      - un punto final si el origen es una API de REST o una API de SOAP
      - un nombre de consulta o mutación si hay una API de GraphQL
      - un nombre de acción si se trata de una IU de administración o de una IU de cliente.

#### Configurar acciones de administración para el registro

Esta función no está disponible porque todas las acciones deben registrarse de forma predeterminada.

### Importar y exportar funciones

Las mejoras en las funciones de importación y exportación se centran en mejorar la experiencia administrativa y proporcionar una mejor visibilidad de las acciones de los usuarios.

>[!NOTE]
>
>Estos ***Las mejoras no modifican la lógica principal de importación y exportación***; en su lugar, amplían la funcionalidad para ofrecer un registro más completo y una atribución de datos mejorada. La funcionalidad fundamental de importación y exportación permanece sin cambios. Los usuarios pueden seguir utilizando las funciones y los flujos de trabajo existentes sin sufrir interrupciones.

#### Registro de acciones administrativas

Una de las principales mejoras de las funciones de importación y exportación es el registro mejorado de las acciones administrativas. Esta mejora introduce la capacidad de profundizar en las actividades asociadas con la importación y exportación de datos, lo que contribuye a mejorar el seguimiento y la auditabilidad. Las siguientes acciones ahora se registran y reflejan en la **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**cuadrícula:

| Tipo | Acciones |
| ---- | ------- |
| Importar | <ul><li>Un usuario administrador ejecuta una importación<li>Un usuario administrador descarga un archivo importado<li>Un usuario administrador descarga un archivo de error<ul/> |
| Exportar | <ul><li>Un usuario administrador solicita<li>Un usuario administrador descarga un archivo exportado<ul/> |
| Importaciones y exportaciones programadas | <ul><li>Un usuario administrador programa la exportación<li>Un usuario administrador edita una exportación programada<li>Un usuario administrador ejecuta una exportación programada<li>Un usuario administrador elimina una exportación programada<li>Un usuario administrador programa una importación<li>Un usuario administrador edita una importación programada<li>Un usuario administrador ejecuta una importación programada<li>Un usuario administrador elimina una importación programada<li>Un usuario administrador ejecuta una eliminación en lotes de operaciones de importación y exportación<ul/> |

### Mejoras de visualización, filtrado y ordenación mejorados

Para proporcionar a los usuarios administradores cuadrículas más informativas, el servicio HIPAA-Ready proporciona varias mejoras para mostrar, filtrar y ordenar datos.

#### Historial de importación ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- Se habilitó el filtrado para todas las columnas excepto para **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]**, y **[!UICONTROL Summary]**.

#### Exportación ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- Se ha añadido un **[!UICONTROL ID]** columna.
- Se ha añadido un **[!UICONTROL Requested At]** column (_fecha y hora en que se solicitó la exportación_).
- Se ha añadido un **[!UICONTROL User]** column (_nombre de usuario de un administrador que realizó la solicitud_).
- Se ha eliminado un **[!UICONTROL Action]** columna.
- Se ha movido el **[!UICONTROL Download]** vínculo a un **[!UICONTROL File name]** column (_como la cuadrícula Historial de importación_).
- Se ha desactivado la acción responsable de la eliminación de un archivo exportado (_para mejorar el seguimiento_).
- Ordenación habilitada para todas las columnas excepto **[!UICONTROL File name]**.
- Se habilitó el filtrado para todas las columnas.

#### Importaciones y exportaciones programadas ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- Se ha añadido un **[!UICONTROL ID]** columna.
- Se ha añadido un **[!UICONTROL Scheduled At]** (la columna _fecha y hora en que se programó la importación o exportación_).
- Se ha añadido un **[!UICONTROL User]** (la columna _nombre de usuario de un usuario administrador que programó la importación o exportación_).

## Servicios y funciones desactivados

Para cumplir con los requisitos de HIPAA, algunos servicios y funciones compatibles con Adobe Commerce no están disponibles o están desactivados de forma predeterminada. Los comerciantes tienen la opción de volver a habilitar o utilizar estos servicios y características bajo su propio riesgo.

### Servicios

- **Servicios de Adobe Commerce**: ninguno de los servicios de Adobe Commerce o de extensibilidad está disponible en la oferta de preparación para HIPAA. Estos servicios incluyen, entre otros:

   - Live Search
   - API Mesh
   - Generador de aplicaciones
   - Servicio de catálogo

- **[Servicio SendGrid](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)**: este servicio está desactivado por defecto porque la aplicación no es compatible con HIPAA.

### Funciones desactivadas de forma predeterminada

Las siguientes funciones están deshabilitadas de forma predeterminada en el módulo de preparación para HIPAA. Los comerciantes pueden activar cualquiera de estas funciones bajo su propio riesgo.

- **[Cierre de compra de invitado](../stores-purchase/checkout-guest.md)**: esta función presenta un riesgo potencial para varios aspectos de la HIPAA, incluidos el registro, el control de acceso, la higiene y el linaje de la PHI y, potencialmente, más.

- **[Función Newsletter](../merchandising-promotions/newsletters.md)**: esta función está desactivada para evitar que se utilice PHI en un contexto de marketing.

- **[Configuración del servicio Informes avanzados](../getting-started/business-intelligence.md)**— Esta opción de configuración está deshabilitada para evitar que se use PHI para análisis e informes.
