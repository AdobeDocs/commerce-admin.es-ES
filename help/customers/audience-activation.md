---
title: '[!DNL Audience Activation]'
description: Obtenga información sobre cómo activar audiencias de Real-Time CDP en Adobe Commerce para impulsar la personalización en su tienda.
exl-id: b53908f2-c0c1-42ad-bb9e-c762804a744b
feature: Customers, Configuration, Personalization
topic: Commerce, Personalization
level: Experienced
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 676081da615d02f8cb2e4896b200b1e4c0855913
workflow-type: tm+mt
source-wordcount: '1688'
ht-degree: 1%

---

# [!DNL Audience Activation]

La extensión [!DNL Audience Activation] le permite activar audiencias de Real-Time CDP en Adobe Commerce para crear ofertas únicas en el carro de compras. Estas ofertas e incentivos incluyen técnicas comunes de comercialización de comercio electrónico, como _comprar 2 y obtener 1 gratis_, banners a pantalla completa dirigidos a ese cliente y precios de productos modificados a través de varias ofertas. Las audiencias creadas en Real-Time CDP se basan en datos de varios sistemas empresariales, como Enterprise Resource Planning (ERP), Customer Relationship Management (CRM), puntos de venta y sistemas de marketing. Debido a que la información del segmento del cliente se actualiza constantemente, los clientes pueden asociarse y desasociarse de un segmento a medida que compran en su tienda.

Puede activar audiencias en una tienda de Luma o [sin encabezado](#headless-support). En una tienda de Luma, la información de audiencia (pertenencia a segmentos) se almacena en una cookie en Commerce. En una tienda sin encabezado, la información de audiencia se pasa en el encabezado de la API de GraphQL como parámetro denominado: `aep-segments-membership`.

## Notas de la versión

Esta sección contiene información sobre las actualizaciones realizadas en la extensión de Audience Activation e incluye:

![Nuevo](../assets/new.svg) - Nuevas características
![Corrección](../assets/fix.svg): correcciones y mejoras
![Error](../assets/bug.svg): problemas conocidos

Consulte [Próximas versiones](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) para obtener más información sobre las programaciones de versiones y la compatibilidad.

Consulte la documentación para desarrolladores para [obtener más información acerca de la compatibilidad del producto](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html).

## Actualizaciones de servicios compatibles

En estas notas de la versión se describen cambios y correcciones de funciones relacionados con las extensiones que utiliza Audience Activation.

+++Actualizaciones de servicios compatibles

_15 de agosto de 2023_

![Corrección](../assets/fix.svg): se ha actualizado el [panel Audiencias de Real-Time CDP](#real-time-cdp-audiences-dashboard) para simplificar el filtrado.

_27 de junio de 2023_

![Corrección](../assets/fix.svg): Se ha agregado compatibilidad con PHP 8.2 en el paquete `magento/module-data-services-graphql`.

_30 de mayo de 2023_

![Nuevo](../assets/new.svg) - Se ha actualizado el [tablero de audiencias de Real-Time CDP](#real-time-cdp-audiences-dashboard) para incluir la capacidad de ordenar, buscar y filtrar las audiencias activas dentro de la instancia de Adobe Commerce.

+++

### 2.4.0

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"} con versiones de Adobe Commerce 2.4.4 y posteriores

_24 de marzo de 2025_

![Nuevo](../assets/new.svg) - Se agregó compatibilidad con PHP 8.4.

### 2.3.1.

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"} con versiones de Adobe Commerce 2.4.4 y posteriores

_12 de noviembre de 2024_

![Corrección](../assets/fix.svg): se corrigió un problema al filtrar las audiencias de Real-Time CDP disponibles para elegir.

### 2.3.0

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"} con versiones de Adobe Commerce 2.4.4 y posteriores

_29 de julio de 2024_

![Nuevo](../assets/new.svg): se ha agregado sintaxis de línea de comandos para que pueda [probar las credenciales](#validate-the-connection) para determinar si es necesario actualizarlas para extraer datos de audiencia de Adobe Experience Platform.

### 2.2.0

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"} con versiones de Adobe Commerce 2.4.4 y posteriores

_12 de junio de 2024_

![Nuevo](../assets/new.svg): versión de GA para [reglas de productos relacionadas](../merchandising-promotions/product-related-rule-create.md) informadas por las audiencias.

### 2.1.1

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"} con versiones de Adobe Commerce 2.4.4 y posteriores

_4 de abril de 2024_

![Nuevo](../assets/new.svg) - Se agregó compatibilidad con PHP 8.3.

### 2.2.0-beta1

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"} con versiones de Adobe Commerce 2.4.4 y posteriores

_16 de febrero de 2024_

![Nuevo](../assets/new.svg) - Si participa en la versión beta, asegúrese de que el archivo `composer.json` tenga lo siguiente en el nivel raíz: ` "minimum-stability": "beta"`.
![Nuevo](../assets/new.svg) - (**Beta**) Se ha agregado la capacidad de crear [reglas de producto relacionadas](../merchandising-promotions/product-related-rule-create.md) informadas por las audiencias.

### 2.1.0

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"} con versiones de Adobe Commerce 2.4.4 y posteriores

_24 de enero de 2024_

![Nuevo](../assets/new.svg) - Se ha actualizado el [panel Audiencias de Real-Time CDP](#real-time-cdp-audiences-dashboard) para incluir los sitios web que contienen las audiencias y especificar qué bloques dinámicos y reglas de precios de carrito están configurados para usar esas audiencias.

### 2.0.1

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"} con versiones de Adobe Commerce 2.4.4 y posteriores

_16 de noviembre de 2023_

![Corrección](../assets/fix.svg): estabilidad mejorada.

### 2.0.0

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"} con versiones de Adobe Commerce 2.4.4 y posteriores

_10 de octubre de 2023_

![Nuevo](../assets/new.svg): Se agregó compatibilidad con OAuth 2.0 al [configurar](#configure-the-extension) la extensión de Audience Activation.
![Corrección](../assets/fix.svg): estabilidad mejorada.

### 1.2.0

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"} con versiones de Adobe Commerce 2.4.4 y posteriores

_15 de agosto de 2023_

![Corrección](../assets/fix.svg): Se ha actualizado la versión de los componentes de la interfaz de usuario.

### 1.1.0

_30 de mayo de 2023_

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"} con versiones de Adobe Commerce 2.4.4 y posteriores

![Nuevo](../assets/new.svg): se agregó compatibilidad con [bloques dinámicos](#headless-support) en una tienda sin encabezado.

### 1.0.1

_11 de mayo de 2023_

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"} con versiones de Adobe Commerce 2.4.4 y posteriores

![Corrección](../assets/fix.svg): se corrigió un problema en el cual no se aplicaba un bloque dinámico o una regla de precio de carro de compras a la tienda.
![Corrección](../assets/fix.svg): se ha corregido un problema por el que una instalación no configurada de la extensión de Audience Activation provocaba un error cuando un comerciante intentaba crear o actualizar un bloque dinámico.

### 1.0.0

_31 de marzo de 2023_

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"} con versiones de Adobe Commerce 2.4.4 y posteriores

![Nuevo](../assets/new.svg): versión de disponibilidad general

## Implementación

Las siguientes tareas se aplican a las implementaciones de tiendas de Luma y sin encabezado. Para activar audiencias en Adobe Commerce, debe:

- Instalar Adobe Commerce versión 2.4.4 o superior
- [Activar](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Adobe Commerce como destino en Real-Time CDP
- [Instalar](#install-the-extension) la extensión [!DNL Audience Activation] en el administrador
- [Configurar](#configure-the-extension) la extensión [!DNL Audience Activation] en el administrador

### Instalación de la extensión

Instale la extensión [!DNL Audience Activation] desde [marketplace](https://commercemarketplace.adobe.com/magento-audiences.html) o ejecute el siguiente comando:

```bash
composer require magento/audiences
```

### Configuración de la extensión

Después de instalar la extensión [!DNL Audience Activation], debe iniciar sesión en el administrador de Commerce y completar lo siguiente:

1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL Commerce Services Connector]**.

1. [Inicia sesión](https://experienceleague.adobe.com/docs/commerce/user-guides/integration-services/saas.html#organizationid) en tu cuenta de Adobe y selecciona tu ID de organización.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL [!DNL Data Connection]]**.

1. En el campo **[!UICONTROL Datastream ID]**, pegue el ID de la secuencia de datos que creó al [activar](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html#parameters) Adobe Commerce como destino en Real-Time CDP.

   Esta secuencia de datos envía datos del sitio web de Commerce a Real-Time CDP para determinar si un comprador pertenece a una audiencia. Si aún no ha creado una secuencia de datos, [cree](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#create) una en Experience Platform, [agréguela](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) al destino de Commerce en Real-Time CDP y a la extensión [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/connect-data.html#data-collection) en el administrador.

   >[!NOTE]
   >
   >Cuando especifica un ID de secuencia de datos, [lo asocia a un sitio web específico](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/connect-data.html#data-collection) en la extensión [!DNL Data Connection]. Si tu tienda Commerce tiene varios sitios web, [crea un destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) para cada sitio web en Real-Time CDP y usa un identificador de flujo de datos diferente para cada uno.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expanda **[!UICONTROL Services]** y seleccione **[!UICONTROL [!DNL Data Connection]]**.

1. [Agregar](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/connect-data.html#add-service-account-and-credential-details) detalles de cuenta de servicio y credenciales.

## Dónde usar las audiencias de Real-Time CDP en Commerce

Con la extensión [!DNL Audience Activation] habilitada, puede:

- [Crear una regla de precios del carro de compras](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) informada por las audiencias
- [Crear un bloque dinámico](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) informado por las audiencias
- [Crear una regla de producto relacionada](../merchandising-promotions/product-related-rule-create.md) informada por las audiencias

>[!TIP]
>
>Para ver un caso de uso completo e integral sobre cómo exportar datos de [!DNL Commerce] a Real-Time CDP, generar una audiencia y activar esa audiencia en [!DNL Commerce], consulte [Crear una audiencia en Real-Time CDP con [!DNL Commerce] datos de evento](https://experienceleague.adobe.com/en/docs/commerce/data-connection/use-cases/create-audience).

## Panel de audiencias de Real-Time CDP

Puede ver todas las [audiencias activas](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html) que están disponibles para personalizar en su instancia de Adobe Commerce mediante el panel **Audiencias de Real-Time CDP**.

Para acceder al panel de **Audiencias de Real-Time CDP**, ve a la barra lateral de _Administración_ y luego ve a **[!UICONTROL Customers]** > **[!UICONTROL Real-time CDP Audience]**.

![Panel de audiencias de Real-Time CDP](./assets/real-time-cdp-dashboard.png){width="700" zoomable="yes"}

El tablero contiene los campos siguientes:

| Columna | Descripción |
|--- |--- |
| `Hide filters` | Permite mostrar u ocultar cualquier filtro que se pueda aplicar al panel. Actualmente, el único filtro que puede aplicar es `Last updated`. Este filtro le permite seleccionar un intervalo de fechas para las audiencias en función de la última actualización. |
| `Search` | Le permite buscar audiencias activas en la instancia de Commerce. |
| `Name` | Nombre proporcionado a la audiencia en Real-Time CDP. |
| `Origin` | Indica la procedencia de la audiencia, como `Experience Platform`. |
| `Websites` | Indica qué sitios web están configurados para utilizar las audiencias. |
| `Dynamic Blocks` | Indica qué bloques dinámicos están configurados para utilizar las audiencias. |
| `Cart Price Rules` | Indica qué reglas de precios del carro de compras están configuradas para usar las audiencias. |
| `Related Product Rules` | Indica qué reglas de producto relacionadas están configuradas para usar las audiencias. |
| `Last updated` | Indica cuándo se modificó la audiencia en Real-Time CDP. |
| `Sync now` | Recupera audiencias nuevas o actualizadas de Real-Time CDP. |
| `Customize table` | Permite mostrar u ocultar las columnas `Origin`, `Websites`, `Dynamic Blocks`, `Cart Price Rules` y `Last updated`. |

{style="table-layout:auto"}

## Compatibilidad sin encabezado

Puede activar audiencias en una instancia de Adobe Commerce sin encabezado, como AEM y PWA, para mostrar reglas de precios del carro de compras, reglas de productos relacionadas o bloques dinámicos basados en las audiencias.

### Reglas de precios del carro de compras y reglas de productos relacionadas

Para las reglas de precios del carro de compras y las reglas de productos relacionadas, una tienda sin encabezado se comunica con Experience Platform a través de [Commerce integration framework (CIF)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html). El marco de trabajo proporciona una API del lado del servidor que se implementa mediante GraphQL. La información de audiencia, como el segmento de un comprador, pasa a Commerce a través de un parámetro de encabezado de GraphQL denominado: `aep-segments-membership`.

La arquitectura general es la siguiente:

![Envío de datos de tienda sin encabezado al servidor](./assets/aem-commerce-architecture.png){width="700" zoomable="yes"}

Después de [instalar](#install-the-extension) y [configurar](#configure-the-extension) la extensión, Experience Platform Web SDK contiene la información de la audiencia en forma de abono a segmentos.

Para capturar esas pertenencias a segmentos desde SDK, consulte este [fragmento de código](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html#example-response-for-custom-personalization-with-attributes).

Una vez recuperado, puede pasar esos segmentos a Commerce dentro del encabezado de GraphQL. Por ejemplo:

```bash
curl 'http://magento.config/graphql' -H 'Authorization: Bearer abc123' -H 'aep-segments-membership: urlencoded_list_of_segments' -H 'Content-Type: application/json' --data-binary '{"query":"query {\ncustomer {\nfirstname\nlastname\nemail\n}\n}"}'
```

### Bloques dinámicos

Para bloques dinámicos, las consultas de GraphQL `dynamicBlocks` pueden contener el atributo de entrada `audience_id`. Si especifica uno o más valores de `audience_id` en una consulta `dynamicBlocks`, devolverá una lista de bloques dinámicos asignados a esas audiencias.

#### Ejemplo de uso

La siguiente consulta devuelve todos los bloques dinámicos asociados con varios ID de audiencia.

**Solicitud:**

```graphql
{
  dynamicBlocks(input:
  {
    type: SPECIFIED
    audience_id: {
      in: [
        "cd29a789-9be8-40ad-a1ef-640c33b3742e"
        "92c3e14d-c72b-40d0-96b7-b96801dcc135"
      ]
    }
  })
  {
    items {
      uid
      audience_id
      content {
        html
      }
    }
    page_info {
      current_page
      page_size
      total_pages
    }
    total_count
  }
}
```

**Respuesta:**

```json
{
  "data": {
    "dynamicBlocks": {
      "items": [
        {
          "uid": "MQ==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e"
          ],
          "content": {
            "html": "<h2><strong>SAVE 20%</strong></h2>\r\n<p>(some restrictions apply)</p>\r\n<p>&nbsp;</p>"
          }
        },
        {
          "uid": "Mg==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e",
            "92c3e14d-c72b-40d0-96b7-b96801dcc135"
          ],
          "content": {
            "html": "<p><img src=\"{{media url=&quot;wysiwyg/save20.png&quot;}}\" alt=\"save 20% red\"></p>"
          }
        }
      ],
      "page_info": {
        "current_page": 1,
        "page_size": 20,
        "total_pages": 1
      },
      "total_count": 2
    }
  }
}
```

Obtenga más información acerca de la consulta de GraphQL `dynamicBlocks` en la [documentación para desarrolladores](https://developer.adobe.com/commerce/webapi/graphql/schema/store/queries/dynamic-blocks/).

## Recuperación de audiencias con Adobe Experience Platform Mobile SDK

Puede recuperar audiencias de Real-Time CDP mediante Adobe Experience Platform Mobile SDK.

1. [Instalar](#install-the-extension) la extensión de Audience Activation.
1. [instale y configure SDK para su sitio de Commerce móvil](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/mobile-sdk-epc.html).

>[!IMPORTANT]
>
>Adobe Experience Platform Mobile SDK para iOS es compatible con iOS 11 o versiones posteriores.

Una vez completada la configuración, utilice las operaciones de SDK móvil para recuperar los datos de audiencia. Por ejemplo:

```swift
Edge.sendEvent(experienceEvent: experienceEvent) { (handles: [EdgeEventHandle]) in
    for handle in handles {
        if handle.type == "activation:pull" {
        let payloadItems = handle.payload ?? []
            for payloadItem in payloadItems {
                if let segments = payloadItem["segments"] as? any Sequence {
                    var segmentsArr = [Any]()
                    for segment in segments {
                        let response = segment as AnyObject?
                        segmentsArr.append(response?.object(forKey: "id")! ?? "")
                    }
                    print("Saving segments ->  \(segments)")
                    storage.set(segmentsArr, forKey: "segments")
                    print("End saving segments")
                }

                // Show segments
                let rSegments = storage.object(forKey: "segments") ?? nil;
                print("Retrieving segments -> \(rSegments)")
            }
        }
    }
}
```

Una vez recuperados los datos, puedes usarlos para crear [reglas de precio del carro de compras](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences), [bloques dinámicos](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) y [reglas de producto relacionadas](../merchandising-promotions/product-related-rule-create.md) basadas en la audiencia en la aplicación Commerce.

## Las audiencias no se muestran en Commerce

Si las audiencias de Real-Time CDP no se muestran en Commerce, puede deberse a lo siguiente:

- Conexión no válida
- Se seleccionó un tipo de autenticación incorrecto en la página de configuración **Conexión de datos**
- Privilegios insuficientes en el token generado

Las secciones siguientes describen cómo solucionar estos problemas.

### Validación de la conexión

Para validar las credenciales y la respuesta de Adobe Experience Platform, ejecute el siguiente comando:

```bash
bin/magento audiences:config:status
```

Este comando devuelve el estado de la conexión. Agregue el indicador `-v` para proporcionar información detallada adicional:

```
./bin/magento audiences:config:status -v
```

Por ejemplo:

```
+----------------------------------+---------------+---------------------------------------------+---------------------------------------------------------+--------------+
| Client ID                        | Client secret | Technical account ID                        | Technical account email                                 | Sandbox name |
+----------------------------------+---------------+---------------------------------------------+---------------------------------------------------------+--------------+
| 1234bd57fac8497d8933327c535347d8 | *****         | 12341E116638D6B00A495C80@techacct.adobe.com | 12345-b95b-4894-a41c-a4130d26bd80@techacct.adobe.com | dev          |
```

### Tipo de autenticación incorrecto seleccionado en la configuración

1. Abra la instancia de Commerce.
1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.
1. Expanda **[!UICONTROL Services]** y seleccione **[!UICONTROL [!DNL Data Connection]]**.
1. Asegúrese de que el método de autorización de servidor a servidor especificado en el campo **[!UICONTROL Authentication Type]** sea correcto. Adobe recomienda usar **OAuth**. [JWT ha quedado obsoleto](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/security/jwt-credentials-deprecation-in-adobe-developer-console), y todos los certificados actuales caducarán el 1 de marzo de 2026.

### Privilegios insuficientes en el token generado

Este problema puede deberse a la falta de privilegios de API para el token generado. Para asegurarse de que el token tenga los privilegios correctos:

1. Identifique al administrador de sistemas de Adobe Experience Platform de su organización.
1. Busque el proyecto y las credenciales que utilizará.
1. Identifique el correo electrónico de la cuenta técnica, por ejemplo: `fe3c9476-1234-1234-abcd-2a51a785009a@techacct.adobe.com`.
1. Pida al administrador de sistemas que inicie Adobe Experience Platform y vaya a **[!UICONTROL Permissions]** -> **[!UICONTROL Users]** -> **[!UICONTROL API credentials]**.
1. Utilizando el correo electrónico de cuenta técnica de arriba, busque las credenciales que desea modificar.
1. Abra las credenciales y seleccione **[!UICONTROL Roles]** -> **[!UICONTROL Add roles]**.
1. Agregue la función que contiene el permiso **[!UICONTROL Manage destinations]**.
1. Haga clic en **[!UICONTROL Save]**.
1. [Regenerar](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html#generate-access-token) el token de acceso en la consola.
1. Compruebe que el token proporciona una respuesta válida mediante la API [Conexiones de Target](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/getTargetConnections).
