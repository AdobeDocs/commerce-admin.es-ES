---
title: Preparación para HIPAA en Adobe Commerce
description: Descubra cómo puede añadir el módulo Adobe Commerce HIPAA-Ready y obtener funciones y funcionalidades adicionales que le permiten cumplir con sus obligaciones HIPAA.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: c21c8b76e37e617885bae3492801b45093a6b5a5
workflow-type: tm+mt
source-wordcount: '1483'
ht-degree: 0%

---

# Preparación para HIPAA en Adobe Commerce

>[!IMPORTANT]
>
>**Descargo de responsabilidad legal**<br/>
>Esta información está pensada para ayudar a los clientes de Adobe a responder a sus preguntas sobre los servicios preparados para HIPAA de Adobe. No constituye asesoramiento jurídico. Los comerciantes deben consultar con su propio asesor legal para comprender sus obligaciones bajo HIPAA y el uso y la configuración apropiados de los productos de Adobe.

## Ley de Portabilidad y Responsabilidad del Seguro de Salud (HIPAA)

La Ley de Portabilidad y Responsabilidad del Seguro de Salud (HIPAA, por sus siglas en inglés) es la ley federal clave de privacidad de la atención médica en Estados Unidos y es aplicada por el Departamento de Salud y Servicios Humanos (HHS, por sus siglas en inglés) de Estados Unidos. La HIPAA se aplica a _Entidades cubiertas_ (como proveedores de atención médica, aseguradoras y cámaras de compensación) y _Asociados empresariales_ (como las entidades que prestan servicios a las entidades cubiertas). Los requisitos de HIPAA se establecen en tres reglas independientes: Regla de privacidad, Regla de seguridad y Regla de notificación de infracciones. Adobe actúa como Asociado Comercial para ciertos productos, que Adobe clasifica como &quot;Servicios preparados para HIPAA&quot;. Los datos regulados por la HIPAA se denominan _Información médica protegida_ o PHI. La PHI es un subconjunto de información de salud que (1) es creada o recibida por un proveedor de atención médica, un plan de salud o un centro de intercambio de información de atención médica, (2) se relaciona con la salud física o mental o la condición pasada, presente o futura de un individuo, la prestación de atención médica a un individuo, o el pago pasado, presente o futuro por la prestación de atención médica a un individuo, y (3) identifica al individuo o con respecto al cual hay una base razonable para creer que la información puede usarse para identificar al individuo. Las Reglas de Privacidad y Seguridad de la HIPAA requieren que una Entidad Cubierta obtenga garantías por escrito de un Asociado Comercial en forma de un Contrato de Asociado Comercial, o BAA, que requiere que el Asociado Comercial salvaguarde la privacidad y seguridad de la PHI de la Entidad Cubierta.

## Adobe Commerce compatible con HIPAA

Adobe Commerce HIPAA-Ready cuenta con funciones y características adicionales que permiten a los comerciantes cumplir con sus respectivas obligaciones HIPAA. Puede instalar el Adobe Commerce HIPAA-Ready (`magento/hipaa-ee`) a su Adobe Commerce en la infraestructura en la nube. También hay algunas funciones que deben deshabilitarse para cumplir con HIPAA.

*Estos materiales están destinados únicamente a fines informativos. El suministro de esta información no da derecho al destinatario a ningún derecho contractual o de otro tipo. Si bien se han hecho esfuerzos para garantizar la exactitud de la información a la fecha en que se ha proporcionado, no se hace ninguna declaración de que dicha información sea exacta y completa, y el Adobe no se compromete a actualizar esta información a medida que cambie la ley o los productos del Adobe. Además, este documento no se debe distribuir a ninguna parte que no sea el destinatario deseado sin el consentimiento por escrito del Adobe.*

## Requisitos del sistema

La preparación para HIPAA en Adobe Commerce tiene los mismos requisitos del sistema que Adobe Commerce con los requisitos adicionales:

- Adobe Commerce versión 2.4.6-p3 o posterior (no beta)
- Adobe Commerce en la infraestructura en la nube o Adobe Commerce en Managed Services
- Última versión de `magento/hipaa-ee` extensión

## Instalación

Los servicios preparados para HIPAA de Adobe son técnicamente un metapaquete de compositor `magento/hipaa-ee` que contiene vínculos a módulos especiales. Este metapaquete reside en el repositorio [repo.magento.com](https://repo.magento.com).

1. Para poder instalar `magento/hipaa-ee` metapackage, debe tener acceso a él. Para generar claves y obtener los derechos necesarios, consulte [Obtener las claves de autenticación](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html?lang=en).

1. Compruebe el entorno en el que va a instalar el paquete y asegúrese de que cumple los requisitos generales [requisitos del sistema](#system-requirements).

1. Añadir el metapaquete `magento/hipaa-ee` a la configuración del compositor.

   La forma más sencilla es usando la CLI del compositor. Por ejemplo:

   ```shell
   composer require magento/hipaa-ee
   ```

1. Si Adobe Commerce aún no está instalado, puede iniciar la instalación (siga el [Instrucciones de instalación](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html?lang=en)).

   Si Adobe Commerce ya está instalado, ejecute después de descargar los módulos `bin/magento setup:upgrade` y luego siga las recomendaciones.

   ```shell
   bin/magento setup:upgrade
   ```

   Cuando se ejecuta este comando, se activan los módulos recién descargados y se inician los scripts para instalarlos. Para obtener más información sobre la administración de módulos, consulte [Habilitar o deshabilitar módulos](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=en).

1. Una vez finalizado el proceso de instalación o actualización, debe comprobar si la variable `Hipaa*` se han incluido los módulos pertinentes.

   Ejecute el comando:

   ```shell
   bin/magento module:status
   ```

   Si el paquete del Compositor de HIPAA se agregó correctamente, verá los módulos HIPAA en la salida del comando. Por ejemplo:

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

El `magento/hipaa-ee` presenta algunos cambios y mejoras en el producto base de Commerce. Las secciones siguientes proporcionan detalles sobre estos cambios y cómo modifican el producto base.

### Registros de acciones

El registro de auditoría es un requisito de HIPAA. En Adobe Commerce, la variable [Registros de acciones](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) registra todos los cambios realizados por un usuario administrador que trabaje en su tienda. Para cumplir los requisitos de la HIPAA sobre el registro de auditoría, se han realizado cambios en la función para registrar todas las acciones de los usuarios y clientes administradores realizadas a través de la IU de administración y de las llamadas a la API.

#### Informe Registros de acciones

El _Registros de acciones_ cuadrícula del informe (**[!UICONTROL System]** > Registros de acciones > Informe) se modifica para dar cabida a las acciones de los clientes realizadas a través de la IU de administración y la API.

1. Dos columnas adicionales:
   - ***Origen***: Muestra dónde se realizó la acción.\
     Valores: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Tipo de cliente***: muestra el tipo de cliente.\
     Valores: Cliente | Administrador | Integración


2. Cambiar nombre ***Nombre de usuario*** hasta ***Identificador de cliente***
   - ***Identificador de cliente***: Muestra el ID de inicio de sesión del usuario que realizó la acción\
     Valores:
      - un mensaje de correo electrónico si el tipo de cliente es Cliente
      - un nombre de usuario si el tipo de cliente es Admin
      - un nombre si el Tipo de cliente es Integración

3. Cambiar nombre ***Nombre completo de la acción*** hasta ***Target***
   - ***Target***: Muestra el nombre de la acción\
     Valores:
      - un punto final si el origen es API de REST o API de SOAP
      - un nombre de consulta/mutación si la API de GraphQL
      - un nombre de acción si la IU de administración o la IU de cliente.

#### Configurar acciones de administración para el registro

Esta función no está disponible porque todas las acciones deben registrarse de forma predeterminada.

### Importación/exportación de funciones

Las mejoras en las funciones de importación y exportación se centran en mejorar la experiencia administrativa y proporcionar una mejor visibilidad de las acciones de los usuarios.

>[!NOTE]
>
>Estos ***Las mejoras no modifican la lógica principal de importación/exportación***; en su lugar, amplían la funcionalidad para ofrecer un registro más completo y una atribución de datos mejorada. La funcionalidad fundamental de la importación y exportación permanece sin cambios. Los usuarios pueden seguir utilizando las funciones y los flujos de trabajo existentes sin sufrir interrupciones.

#### Registro de acciones administrativas

Una de las principales mejoras de las funciones de importación y exportación es el registro mejorado de las acciones administrativas. Esto introduce la capacidad de profundizar en las actividades asociadas con la importación/exportación de datos, lo que contribuye a mejorar el seguimiento y la auditabilidad. Las siguientes acciones ahora se registran y reflejan en la **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**cuadrícula:

| Tipo | Acciones |
| ---- | ------- |
| Importar | <ul><li>Un usuario administrador ejecuta una importación<li>Un usuario administrador descarga un archivo importado<li>Un usuario administrador descarga un archivo de error<ul/> |
| Exportar | <ul><li>Un usuario administrador solicita<li>Un usuario administrador descarga un archivo exportado<ul/> |
| Importaciones y exportaciones programadas | <ul><li>Un usuario administrador programa la exportación<li>Un usuario administrador edita una exportación programada<li>Un usuario administrador ejecuta una exportación programada<li>Un usuario administrador elimina una exportación programada<li>Un usuario administrador programa una importación<li>Un usuario administrador edita una importación programada<li>Un usuario administrador ejecuta una importación programada<li>Un usuario administrador elimina una importación programada<li>Un usuario administrador ejecuta una eliminación en lotes de operaciones de importación y exportación<ul/> |

### Mejoras de visualización y filtrado y ordenación mejorados

Para dotar a los administradores de cuadrículas más informativas, se han introducido varias mejoras en la visualización de los datos y en las funciones de filtrado y clasificación:

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
- Se ha añadido un **[!UICONTROL Scheduled At]** column (_fecha y hora en que se programó la importación o exportación_).
- Se ha añadido un **[!UICONTROL User]** column (_nombre de usuario de un usuario administrador que programó la importación/exportación_).

## Funciones desactivadas para la preparación para HIPAA

### Servicios SaaS

Ninguno de los servicios SaaS ofrecidos para Adobe Commerce está disponible en la oferta de preparación para HIPAA. Esto incluye, entre otras cosas:

- Live Search
- API Mesh
- Generador de aplicaciones
- Servicio de catálogo

### Cierre de compra de invitado deshabilitado de forma predeterminada

- El registro de salida de los huéspedes presenta un riesgo potencial para varios aspectos de la HIPAA, incluyendo el registro, el control de acceso, la higiene y el linaje de la PHI, y potencialmente más.
- El Pago y envío de invitados está desactivado de forma predeterminada en el módulo de preparación para HIPAA, pero los comerciantes pueden habilitarlo bajo su propio riesgo.

### Función de newsletter deshabilitada de forma predeterminada

- La función de boletín informativo está desactivada de forma predeterminada para evitar que se utilice la PHI en un contexto de marketing, pero el comerciante puede habilitarla bajo su propio riesgo.

### Se deshabilitó la configuración predeterminada del servicio Informes avanzados

La configuración del servicio de Informes avanzados está deshabilitada de manera predeterminada para evitar que la PHI se use para análisis e informes, pero el comerciante puede habilitarla bajo su propio riesgo.

### Servicio Sendgrid deshabilitado de forma predeterminada

El servicio Sendgrid está deshabilitado de forma predeterminada porque la aplicación no es compatible con HIPAA. Los comerciantes pueden enviar una solicitud de asistencia para habilitar Sendgrid, pero deben reconocer que asumirán el riesgo de utilizar el servicio.
