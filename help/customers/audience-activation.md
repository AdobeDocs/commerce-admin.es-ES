---
title: "[!DNL Audience Activation]"
description: Obtenga información sobre cómo activar audiencias de Real-Time CDP en Adobe Commerce para impulsar la personalización en su tienda.
exl-id: b53908f2-c0c1-42ad-bb9e-c762804a744b
feature: Customers, Configuration, Personalization
topic: Commerce, Personalization
level: Experienced
source-git-commit: db8344ab8890c20bb0b3c7d25da95b6007858d6a
workflow-type: tm+mt
source-wordcount: '1409'
ht-degree: 0%

---

# [!DNL Audience Activation]

El [!DNL Audience Activation] La extensión de permite activar audiencias de Real-Time CDP en Adobe Commerce para crear ofertas únicas en el carro de compras. Estas ofertas e incentivos incluyen técnicas comunes de comercialización en comercio electrónico, como _comprar 2 obtener 1 gratis_, banners promocionales dirigidos a ese cliente y precios de productos modificados a través de varias ofertas. Las audiencias creadas en Real-Time CDP se basan en datos de varios sistemas empresariales, como Enterprise Resource Planning (ERP), Customer Relationship Management (CRM), puntos de venta y sistemas de marketing. Debido a que la información del segmento del cliente se actualiza constantemente, los clientes pueden asociarse y desasociarse de un segmento a medida que compran en su tienda.

Puede activar audiencias en una tienda de Luma o [acéfalo](#headless-support) tienda. En una tienda de Luma, la información de audiencia (pertenencia a segmentos) se almacena en una cookie en el lado del comercio. En una tienda sin encabezado, la información de audiencia se pasa en el encabezado de la API de GraphQL como parámetro denominado: `aep-segments-membership`.

## Notas de la versión

Esta sección contiene información sobre las actualizaciones realizadas en la extensión de Audience Activation e incluye:

![Nuevo](../assets/new.svg) - Nuevas funciones
![Fix](../assets/fix.svg) - Correcciones y mejoras
![Error](../assets/bug.svg) - Problemas conocidos

Consulte [Próximas versiones](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) para obtener más información sobre las programaciones de versiones y la compatibilidad.

Consulte la documentación para desarrolladores para [obtenga información acerca de la compatibilidad del producto](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html).

## Actualizaciones de servicios compatibles

En estas notas de la versión se describen cambios y correcciones de funciones relacionados con las extensiones que utiliza Audience Activation.

+++Actualizaciones de servicios compatibles

_15 de agosto de 2023_

![Fix](../assets/fix.svg) - Se ha actualizado el [Panel de audiencias de Real-Time CDP](#real-time-cdp-audiences-dashboard) para simplificar el filtrado.

_27 de junio de 2023_

![Fix](../assets/fix.svg) - Se ha agregado compatibilidad con PHP 8.2 en el `magento/module-data-services-graphql` paquete.

_30 de mayo de 2023_

![Nuevo](../assets/new.svg) - Se ha actualizado el [Panel de audiencias de Real-Time CDP](#real-time-cdp-audiences-dashboard) para incluir la capacidad de ordenar, buscar y filtrar las audiencias activas dentro de la instancia de Adobe Commerce.

+++

### 2.2.0-beta1

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

_16 de febrero de 2024_

![Nuevo](../assets/new.svg) - Si participa en la versión beta, asegúrese de que `composer.json` tiene lo siguiente en el nivel raíz: ` "minimum-stability": "beta"`.
![Nuevo](../assets/new.svg) - (**Beta**) Capacidad añadida para crear [reglas de producto relacionadas](../merchandising-promotions/product-related-rule-create.md) informado por las audiencias.

### 2.1.0

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

_24 de enero de 2024_

![Nuevo](../assets/new.svg) - Se ha actualizado el [Panel de audiencias de Real-Time CDP](#real-time-cdp-audiences-dashboard) para incluir los sitios web que contienen las audiencias y especificar qué bloques dinámicos y reglas de precios del carro de compras están configuradas para utilizar esas audiencias.

### 2.0.1

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

_16 de noviembre de 2023_

![Fix](../assets/fix.svg) - Mayor estabilidad.

### 2.0.0

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

_10 de octubre de 2023_

![Nuevo](../assets/new.svg) - Se ha agregado compatibilidad con OAuth 2.0 al [configurar](#configure-the-extension) la extensión de Audience Activation.
![Fix](../assets/fix.svg) - Mayor estabilidad.

### 1.2.0

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

_15 de agosto de 2023_

![Fix](../assets/fix.svg) : se ha actualizado la versión de los componentes de IU.

### 1.1.0

_30 de mayo de 2023_

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

![Nuevo](../assets/new.svg) - Se ha agregado compatibilidad con [bloques dinámicos](#headless-support) en una tienda sin encabezado.

### 1.0.1

_11 de mayo de 2023_

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

![Fix](../assets/fix.svg) - Se ha corregido un problema por el cual una regla de precio de carro o bloque dinámico no se aplicaba a la tienda.
![Fix](../assets/fix.svg) - Se ha corregido un problema por el cual una instalación no configurada de la extensión de Audience Activation provocaba un error cuando un comerciante intentaba crear o actualizar un bloque dinámico.

### 1.0.0

_31 de marzo de 2023_

[!BADGE Compatibilidad]{type=Informative tooltip="Compatibilidad"}

![Nuevo](../assets/new.svg) - Versión de disponibilidad general

## Implementación

Las siguientes tareas se aplican a las implementaciones de tiendas de Luma y sin encabezado. Para activar audiencias en Adobe Commerce, debe:

- Instalar Adobe Commerce versión 2.4.4 o superior
- [Activar](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Adobe Commerce como destino en Real-Time CDP
- [Instalar](#install-the-extension) el [!DNL Audience Activation] Extensión en el administrador
- [Configurar](#configure-the-extension) el [!DNL Audience Activation] Extensión en el administrador

### Instalación de la extensión

Instale el [!DNL Audience Activation] extensión desde el [mercado](https://commercemarketplace.adobe.com/magento-audiences.html), o ejecute el siguiente comando:

```bash
composer require magento/audiences
```

### Configuración de la extensión

Después de instalar el [!DNL Audience Activation] Con la extensión, debe iniciar sesión en su administrador de Commerce y completar lo siguiente:

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL Commerce Services Connector]**.

1. [Iniciar sesión](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#organizationid) a su cuenta de Adobe y seleccione su ID de organización.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL [!DNL Data Connection]]**.

1. En el **[!UICONTROL Datastream ID]** , pegue el ID de la secuencia de datos que creó al [activado](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html#parameters) Adobe Commerce como destino en Real-Time CDP.

   Esta secuencia de datos envía datos del sitio web de Commerce a Real-Time CDP para determinar si un comprador pertenece a una audiencia. Si todavía no ha creado un conjunto de datos, [crear](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#create) uno en Experience Platform, [añadir](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) al destino de Commerce en Real-Time CDP y al de [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) en el Administrador de.

   >[!NOTE]
   >
   >Al especificar un ID de secuencia de datos, [asociarlo a un sitio web específico](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) en el [!DNL Data Connection] extensión. Si su tienda de Commerce tiene varios sitios web, [crear un destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) para cada sitio web en Real-Time CDP y utilice un ID de flujo de datos diferente para cada uno.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandir **[!UICONTROL Services]** y seleccione **[!UICONTROL [!DNL Data Connection]]**.

1. [Añadir](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#add-service-account-and-credential-details) cuenta de servicio y detalles de credenciales.

## Dónde usar las audiencias de Real-Time CDP en Commerce

Con el [!DNL Audience Activation] con la extensión habilitada, puede:

- [Crear una regla de precios de carro](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) informado por audiencias
- [Creación de un bloque dinámico](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) informado por audiencias
- [(**Beta**) Crear una regla de producto relacionada](../merchandising-promotions/product-related-rule-create.md) informado por audiencias

## Panel de audiencias de Real-Time CDP

Puede ver todos los [activo](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html) audiencias que están disponibles para personalizar en la instancia de Adobe Commerce mediante el **Audiencias de Real-Time CDP** panel.

Para acceder a **Audiencias de Real-Time CDP** panel, vaya a _Administrador_ barra lateral y vaya a **[!UICONTROL Customers]** > **[!UICONTROL Real-time CDP Audience]**.

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
| `Last updated` | Indica cuándo se modificó la audiencia en Real-Time CDP. |
| `Sync now` | Recupera audiencias nuevas o actualizadas de Real-Time CDP. |
| `Customize table` | Permite mostrar u ocultar el `Origin`, `Websites`, `Dynamic Blocks`, `Cart Price Rules`, y `Last updated` columnas. |

{style="table-layout:auto"}

## Compatibilidad sin encabezado

Puede activar audiencias en una instancia de Adobe Commerce AEM sin encabezado, como el de la aplicación y el de PWA, para mostrar reglas de precios del carro de compras, reglas de productos relacionadas o bloques dinámicos basados en las audiencias.

### Reglas de precios del carro de compras y reglas de productos relacionadas

Para las reglas de precios de carro de compras y las reglas de productos relacionadas, una tienda sin encabezado se comunica al Experience Platform a través de la [Commerce integration framework CIF ()](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html). El marco de trabajo proporciona una API del lado del servidor que se implementa mediante GraphQL. La información de audiencia, como el segmento de un comprador, pasa a Commerce a través de un parámetro de encabezado de GraphQL denominado: `aep-segments-membership`.

La arquitectura general es la siguiente:

![Envío de datos de una tienda sin encabezado al servidor](./assets/aem-commerce-architecture.png){width="700" zoomable="yes"}

Después de usted [instalar](#install-the-extension) y [configurar](#configure-the-extension) Con la extensión, el SDK web de Experience Platform contiene la información de audiencia en forma de abono a segmentos.

Para capturar esas pertenencias a segmentos desde el SDK, consulte lo siguiente [fragmento de código](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html#example-response-for-custom-personalization-with-attributes).

Una vez recuperado, puede pasar esos segmentos a Commerce dentro del encabezado de GraphQL. Por ejemplo:

```bash
curl 'http://magento.config/graphql' -H 'Authorization: Bearer abc123' -H 'aep-segments-membership: urlencoded_list_of_segments' -H 'Content-Type: application/json' --data-binary '{"query":"query {\ncustomer {\nfirstname\nlastname\nemail\n}\n}"}'
```

### Bloques dinámicos

Para bloques dinámicos, GraphQL `dynamicBlocks` las consultas pueden contener el `audience_id` atributo de entrada. Si especifica una o más `audience_id` valores en una `dynamicBlocks` consulta, devuelve una lista de bloques dinámicos asignados a esas audiencias.

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

Obtenga más información acerca de `dynamicBlocks` Consulta de GraphQL en [documentación para desarrolladores](https://developer.adobe.com/commerce/webapi/graphql/schema/store/queries/dynamic-blocks/).

## Recuperación de audiencias mediante el SDK para móviles de Adobe Experience Platform

Para poder recuperar audiencias de Real-Time CDP mediante el SDK para móviles de Adobe Experience Platform, debe [instalar y configurar el SDK para su sitio de Mobile Commerce](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/mobile-sdk-epc.html).

>[!IMPORTANT]
>
>El SDK de Adobe Experience Platform Mobile para iOS es compatible con iOS 11 o posterior.

Una vez completada la configuración, utilice las operaciones del SDK móvil para recuperar los datos de audiencia. Por ejemplo:

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

Una vez recuperados los datos, puede utilizarlos para crear audiencias informadas [reglas de precios de carrito](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences), [bloques dinámicos](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) y  [reglas de producto relacionadas](../merchandising-promotions/product-related-rule-create.md) en la aplicación Commerce.

## Las audiencias no se muestran en Commerce

Si las audiencias de Real-Time CDP no se muestran en Commerce, puede deberse a lo siguiente:

- Tipo de autenticación incorrecto seleccionado en la **Conexión de datos** página de configuración
- Privilegios insuficientes en el token generado

Las dos secciones siguientes describen cómo solucionar problemas en cualquiera de los casos.

### Tipo de autenticación incorrecto seleccionado en la configuración

1. Abra la instancia de Commerce.
1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.
1. Expandir **[!UICONTROL Services]** y seleccione **[!UICONTROL [!DNL Data Connection]]**.
1. Asegúrese del método de autorización de servidor a servidor especificado en la **[!UICONTROL Authentication Type]** El campo es correcto. Adobe recomienda utilizar **OAuth**. JWT se ha desaprobado. [Más información](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/).

### Privilegios insuficientes en el token generado

Este problema puede deberse a la falta de privilegios de API para el token generado. Para asegurarse de que el token tenga los privilegios correctos:

1. Identifique al administrador de sistemas de Adobe Experience Platform de su organización.
1. Busque el proyecto y las credenciales que utilizará.
1. Identifique el correo electrónico de la cuenta técnica, por ejemplo: `fe3c9476-1234-1234-abcd-2a51a785009a@techacct.adobe.com`.
1. Pida al administrador de sistemas que inicie Adobe Experience Platform y vaya a **[!UICONTROL Permissions]** -> **[!UICONTROL Users]** -> **[!UICONTROL API credentials]**.
1. Utilizando el correo electrónico de cuenta técnica de arriba, busque las credenciales que desea modificar.
1. Abra las credenciales y seleccione **[!UICONTROL Roles]** -> **[!UICONTROL Add roles]**.
1. Añadir **Acceso a todo en producción**.
1. Clic **[!UICONTROL Save]**.
1. [Regenerar](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html#generate-access-token) el token de acceso en la consola.
1. Compruebe que el token proporciona una respuesta válida utilizando [API de conexiones de Target](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/getTargetConnections).
