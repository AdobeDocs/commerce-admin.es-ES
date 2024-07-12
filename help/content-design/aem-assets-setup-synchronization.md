---
title: Configuración del servicio de sincronización
description: '"Aprenda a conectar sus proyectos de Adobe Commerce y Experience Manager Assets con el servicio del motor de reglas de Assets para habilitar la sincronización de recursos entre estos dos sistemas".'
feature: CMS, Media
source-git-commit: 9d7b1b58b472a99196213e5ab109142bc57b1692
workflow-type: tm+mt
source-wordcount: '1309'
ht-degree: 0%

---


# Configuración del servicio de sincronización

El servicio del motor de reglas de recursos (ARES) es un servicio de varios inquilinos que integra AEM Assets con Adobe Commerce. Este servicio sincroniza recursos entre Adobe Commerce y Experience Manager. AEM El servicio ARES hace coincidir automáticamente los recursos en la con los productos en Adobe Commerce en función del SKU u otros atributos clave. También garantiza que los recursos y las variaciones de productos más recientes siempre estén disponibles en el sitio de comercio electrónico.

Para configurar el servicio, debe registrar el ID de inquilino mediante la API de GraphQL de ARES y seleccionar la regla de coincidencia para sincronizar recursos.

## Elegir una estrategia de coincidencia

La integración de AEM Assets para Commerce admite dos estrategias coincidentes para sincronizar recursos entre Adobe Commerce y AEM Assets.

- **MatchBySku**-Esta es la regla de coincidencia predeterminada que coincide con los recursos basados en el SKU (código de referencia) del producto. El SKU es un identificador único para cada producto. Esta regla hace coincidir el SKU de los metadatos del recurso con el SKU del producto de Commerce para garantizar que los recursos están asociados con los productos correctos.

- **ExternalMatcher**: esta regla de coincidencia es para escenarios más complejos o requisitos empresariales específicos que requieren una lógica de coincidencia personalizada. Para utilizar esta regla, debe tener implementado en Adobe Developer App Builder un código personalizado que defina cómo se relacionan los recursos con los productos.

Para la incorporación inicial, utilice la estrategia `MatchBySku`. Si es necesario, puede cambiar la estrategia de coincidencia más adelante.

## Registrar un inquilino

>[!BEGINSHADEBOX]

**Requisito previo**

- [El proyecto AEM Assets se ha configurado con los metadatos de Commerce necesarios para asignar recursos](aem-assets-configure-aem.md).

- [Instale y configure la integración de Experience Manager Assets en Adobe Commerce](aem-assets-configure-commerce.md).

>[!ENDSHADEBOX]

## Recopilar credenciales

Necesita las siguientes credenciales para autenticar y conectar el entorno del proyecto de Commerce y el entorno del proyecto de AEM Assets con los servicios SaaS de Commerce.

| Datos requeridos | Source | ¿Dónde lo encuentro? |
| ---------- | ------ | ------------- |
| Clave de API de la cuenta de Magento | Commerce | Proporcione la clave de API pública para el entorno de Commerce que esté utilizando, el ensayo o la producción. Puede encontrar las claves API para los entornos de Producción y Ensayo en la página [Configuración del conector de servicio de Commerce](aem-assets-configure-commerce.md#configure-the-commerce-services-connector) del Administrador o en la página [!UICONTROL My Account] de la sección [!UICONTROL API Portal]. |
| Identificador Del Proyecto SaaS De Commerce <ul><li>`magento-environment-Id`</li><li>`Project ID`</li></ul> | Administrador de Commerce | Estos valores identifican el entorno de Commerce y el espacio de datos SaaS y el proyecto al que se va a conectar. Los valores provienen de la [configuración del identificador SaaS del conector de servicios de Commerce].(aem-assets-configure-commerce.md#configure-the-commerce-services-connector). |
| AEM `programId`<br>`environmentId` | [Entorno de creación de AEM Assets](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) | Abra la página AEM Sites y seleccione **[!UICONTROL Assets]**.  Copie los identificadores de proyecto y entorno de la dirección URL: `https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/` |
| baseURL | tienda de Commerce | La [URL base](../stores-purchase/store-urls.md) de tu tienda Commerce. |
| Credenciales de OAuth para acceso a API | Administrador de Commerce | Puede encontrar estas credenciales en la configuración de Commerce [para la integración de Assets](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release). |

## Registrar inquilino

Complete el registro de inquilinos enviando una solicitud al servicio del motor de reglas de Assets para agregar credenciales de autenticación e ID de inquilino. La solicitud incluye las credenciales y los identificadores de proyecto necesarios para establecer las conexiones entre el servicio, el proyecto Commerce y el proyecto Experience Manager Assets.

Envíe la solicitud mediante un cliente de GraphQL o una cURL.

>[!BEGINTABS]

>[!TAB Solicitud de GraphQL]

Use un cliente de GraphQL para enviar una solicitud de POST al extremo de API `https://commerce.adobe.io/assets-integration/graphql`

**Encabezados obligatorios**

Especifique los siguientes encabezados HTTP para la solicitud:

- `x-api-key`: clave de API de su cuenta de Magento
- `magento-environment-Id`: identificador de SaaS
- `x-gw-signature`: token JWT asociado con el MAGEID

**Solicitud:**

**Sintaxis**

```graphql
mutation registerTenant($tenantInput: TenantInput!) {
   registerTenant(tenantInput: $tenantInput) {
      tenantId
      userErrors {
         message
         path
      }
    }
}
```

**Ejemplo de uso**

Registre un inquilino y seleccione la regla `matchBySku` para asignar recursos entre Adobe Commerce y el proyecto de AEM Assets.

**Solicitud:**

```graphql
   {
      "tenantInput": {
         "enabled": true,
         "projectId": "8231afb6-90cd-65e8-84ba-d9abac0f94e6",
         "aem": {
               "programId": "11111",
               "environmentId": "222222"
         },
         "commerce": {
               "baseUrl": "***",
               "credentials": {
                  "consumerKey": "***",
                  "consumerSecret": "***",
                  "accessToken": "***",
                  "accessTokenSecret": "***"
               }
         },
         "rule": {
            "type": "matchBySKU"
            "matchBySkuRule": {
               "metadataField": "commerce:skus"
            }
         }
      }
   }
```

**Respuesta**

```graphql
{
    "data": {
        "registerTenant": {
            "tenantId": "b65d5da7-2756-46a1-9ff1-14fb5d925fee",
            "userErrors": []
        }
    }
}
```

>[!TAB solicitud cURL]

```shell
curl --request POST \
  --url https://commerce.adobe.io/assets-integration/graphql \
  --header 'Content-Type: application/json' \
  --header 'Magento-Environment-Id: ****' \
  --header 'x-api-key: ****' \
  --header 'x-gw-signature: *****' \
  --data '{"query":"mutation registerTenant($tenantInput: TenantInput!) {\n\tregisterTenant(tenantInput: $tenantInput) {\n\t\ttenantId\n\t\tuserErrors {\n\t\t\tmessage\n\t\t\tpath\n\t\t}\n\t}\n}\n","operationName":"registerTenant","variables":{"tenantInput":{"enabled":true,"threshold":100,"projectId":"5d6faa03-e200-4623-9008-da144e4eefd8","aem":{"programId":"***","environmentId":"***"},"commerce":{"version":"2.4.6-p2","extensionVersion":"0.0.1","baseUrl":"***","credentials":{"consumerKey":"***","consumerSecret":"***","accessToken":"***","accessTokenSecret":"***"}},"rule":{"type":"matchBySKU","matchBySkuRule":{"metadataField":"commerce:skus"}}}}}'
```

>[!ENDTABS]

### Campos de entrada

#### AemInput

Identifica la instancia de AEM Assets para almacenar recursos de Commerce. Puede obtener esta información desde la vista Mis programas de Cloud Manager o desde la dirección URL de creación de contenido.

| Campo | Tipo de datos | Descripción |
| ----- | --------- | ----------- |
| `programId` | ¡String! | Identificador único del proyecto en AEM Cloud Service |
| `environmentId` | ¡String! | ID del entorno del proyecto que está utilizando, como producción, ensayo o desarrollo |

#### CommerceInput

Este campo de entrada proporciona las credenciales de autenticación de OAuth para el acceso de la API al catálogo de Commerce. Puede encontrar estas credenciales en la configuración de Commerce [para la integración de Assets](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release).

| Campo | Tipo de datos | Descripción |
| ----- | --------- | ----------- |
| `baseUrl` | Cadena | La [URL base](../stores-purchase/store-urls.md) de tu tienda Commerce. |
| `credentials` | [CommerceCredentialsInput](#commercecredentialsinput)! | Especifica las credenciales para acceder a la instancia de Commerce. |
| `extensionVersion` | Cadena | Opcional. Versión de la integración de AEM Assets para la extensión de Commerce instalada en la instancia de Commerce. |
| `version` | Cadena | Opcional. Versión de la aplicación de Commerce instalada en la instancia de Commerce. |

#### CommerceCredentialsInput

Este campo de entrada proporciona las credenciales de OAuth para el acceso API al catálogo de Commerce. Puede encontrar estas credenciales en la configuración de Commerce [para la integración de Assets](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release).

| Campo | Tipo de datos | Descripción |
| ----- | --------- | ----------- |
| `accessToken` | ¡String! | El token de acceso generado para la integración de Assets. |
| `accessTokenSecret` | ¡String! | El secreto del token de acceso generado para la integración de Assets. |
| `consumerKey` | ¡String! | La clave de consumidor generada para la integración de Assets. |
| `consumerSecret` | ¡String! | Secreto de consumidor generado para la integración de Assets. |

#### ExternalMatcherInput

| Campo | Tipo de datos | Descripción |
| ----- | --------- | ----------- |
| assetToProductUrl | ¡String! | <!--Add field description--> |
| productToAssetUrl | ¡String! | <!--Add field description--> |
| credenciales | [ExternalMatcherCredentialsInput](#externalmatchercredentials)! | Credenciales para acceder al proyecto de App Builder para la integración de AEM Assets con Commerce. |

#### ExternalMatcherCredentials

| Campo | Tipo de datos | Descripción |
| ----- | --------- | ----------- |
| `oauthServerUrl` | ¡String! |    |
| `clientId` | ¡String! |      |
| `clientSecret` | ¡String! |    |
| `imsOrgId` | ¡String! | La organización de IMS donde se aprovisionan AEM Assets y Adobe Commerce. |

#### MatchBySkuRuleInput

| Campo | Tipo de datos | Descripción |
| ----- | --------- | ----------- |
| metadataField | ¡String! | Especifique el campo de metadatos del recurso que se utilizará para la coincidencia. Usar `commerce:skus` |

#### RuleInput

Especifica la regla de coincidencia que se utiliza para sincronizar recursos entre Adobe Commerce y AEM Assets.

| Campo | Tipo de datos | Descripción |
| ----- | --------- | ----------- |
| externalMatcher | [ExternalMatcherInput](#externalmatcherinput) | Selecciona la regla externalMatcher para la coincidencia de recursos y especifica los datos necesarios para utilizarla. |
| MatchBySkuRule | [MatchBySkuRuleInput](#matchbyskuruleinput) | Selecciona MatchBySkuRule para la coincidencia de recursos y especifica los datos necesarios para utilizarla. |

#### RuleTypeInput

| Campo | Tipo de datos | Descripción |
| ----- | --------- | ----------- |
| RuleType | enum | Especifica una lista de reglas de coincidencia de recursos disponibles para la integración de AEM Assets con Commerce. Los valores disponibles son `matchBySKU` o `externalMatcher`. |

#### TenantInput

| Campo | Tipo de datos | Descripción |
| ----- | --------- | ----------- |
| `aem` | [AemInput!](#aeminput) | Identifica la instancia de AEM Assets en AEM Cloud Service donde se almacenan los recursos de Commerce. |
| `commerce` | [CommerceInput!](#commerceinput) | Proporciona información y credenciales del proyecto de Commerce para el acceso a la API |
| `enabled` | ¡Booleano! | Active o desactive la sincronización de recursos entre Adobe Commerce y AEM Assets. |
| `projectId` | ¡String! | El Id. de proyecto SaaS de la [configuración del Identificador SaaS de Commerce Services Connector](aem-assets-configure-commerce.md#configure-the-commerce-services-connector). |
| `rule` | [EntradaRegla!](#ruleinput) | Especifica la regla de coincidencia que se utiliza para sincronizar recursos entre Adobe Commerce y AEM Assets. Especifique `[matchBySkuRule](#matchbyskuruleinput)` o `[externalMatcher](#externalmatcherinput)`. |

### Campos de salida

| Campo | Tipo de datos | Descripción |
| ----- | --------- | ----------- |
| datos | [registerTenant] | Devuelve la información de registro del inquilino y los mensajes de error del servidor. |

#### RegisterTenantResponse

| Campo | Tipo de datos | Descripción |
| ----- | --------- | ----------- |
| tenantId | ¡String! | Devuelve el ID de inquilino registrado. Este ID garantiza que los datos de la integración de AEM Assets para Commerce se almacenen y recuperen del espacio de datos SaaS asociado al entorno de Commerce. |
| userErrors | [[userError!]!](#usererror) | Devuelve cualquier mensaje de error generado por la solicitud. |

#### UserError

| Error | Descripción |
|:------|:------------|
| `IMS Org ID not associated to this Commerce` | Este error se produce si el Id. de entorno especificado en el encabezado `Magento-Environment-Id` no está asignado a la cuenta de IMS. Este error se puede producir porque la cuenta de IMS no estaba conectada cuando [Commerce Services Connector](aem-assets-configure-commerce.md#configure-the-commerce-services-connector) se configuró para la instancia de Commerce. |
| `Client ID is invalid` | El encabezado `x-api-key` es incorrecto. |
| `Client ID is missing` | No se proporcionó el encabezado `x-api-key`. |
| `JWT is required` | No se proporcionó el encabezado `x-gw-signature`. |
| `JWT is invalid` | No se proporcionó el encabezado `x-gw-signature`. |
| `Tenant already exists` | Ya se registró un inquilino con el `mageID` proporcionado (tomado del token JWT) y `saasId` (proporcionado por el encabezado `Magento-Environment-Id`). |
| `Unexpected error when connecting with AEM Assets` | Este error se debe a valores `programId` o `environmentId` no válidos o inexistentes. |
| `Unable to connect with AEM Assets` | Hay dos posibles razones para este error:<br>1. AEM La cuenta de recursos de la está asociada a un ID de organización de IMS diferente al proporcionado para Adobe Commerce.<br>2. Los metadatos de `commerce:isCommerce` no existen en AEM Assets, lo que indica que no hay recursos aprobados para enviar desde AEM Assets a la instancia de Commerce. |
| `Unexpected error when connecting with Commerce` | Este error se produce cuando se proporciona un comercio no válido `baseURL`. |
| `Unable to connect with Commerce, unauthorized` | Se han proporcionado credenciales de comercio no válidas, lo que da como resultado acceso no autorizado. |
| `Invalid rule. The value must be matchBySKU or externalMatcher` | El campo `Rule` contiene un valor incorrecto. Para la solicitud RegisterTenant, los tipos de reglas disponibles están definidos por la enumeración [RuleTypeInput](#ruletypeinput). |

## Habilitar la integración de Experience Manager Assets

Después de registrar el inquilino, el último paso del proceso de incorporación es habilitar la extensión de Experience Manager Assets Integration for Commerce en el administrador.

1. Active la extensión de.

   1. Vaya a **Tiendas** > Configuración > **Configuración** > **Catálogo**.

   1. Abra la configuración del catálogo seleccionando **[!UICONTROL Catalog]**.

   1. Expandir **[!UICONTROL AEM Assets integration]**.

   1. Establezca **[!UICONTROL Integration enabled]** en `yes`.

      ![Integración de AEM Assets para la configuración de administración de Commerce](assets/aem-integration-admin-enable.png){width="600" zoomable="yes"}
