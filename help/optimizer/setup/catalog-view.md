---
title: Vistas de catálogo
description: Conozca cuáles son las vistas de catálogo y cómo crearlas para organizar el catálogo de productos por estructura empresarial, políticas y precios.
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="Solo SaaS" type="Positive" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a instancias de Adobe Commerce as a Cloud Service aprovisionadas con CCDM (infraestructura de SaaS administrada por Adobe)."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 8fbcfcdeb13c452a45e872d939e129703ac5abab
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%
---

# Vistas de catálogo

Una vista de catálogo define los productos y los precios que una tienda puede recuperar. En las instancias de Adobe Commerce as a Cloud Service aprovisionadas con el Modelo de datos de catálogo componible (CCDM), las vistas de catálogo utilizan la misma base de catálogo que alimenta Adobe Commerce Optimizer.

Las vistas de catálogo combinan orígenes de catálogo, directivas y libros de precios para definir el contexto de catálogo de una tienda. Las directivas determinan la gama de productos disponible. Las reglas de comercialización controlan cómo se promocionan y clasifican los productos de ese surtido y pueden aplicarse en todas las vistas de catálogo o adaptarse a una vista específica. Consulte [Crear una regla de comercialización](../merchandising/rules/add.md).

Commerce Foundation sigue siendo la fuente fiable de productos y precios. Los datos de productos y precios se sincronizan de una manera con CCDM mediante la integración nativa de Adobe Commerce as a Cloud Service, sin instalación de conectores independiente ni aplicación de App Builder. La configuración del sitio web, la tienda y la vista de tienda permanece en Commerce Foundation, que también administra el carro de compras, el cierre de compra, las promociones, los clientes, los pedidos y los pagos.

>[!NOTE]
>
>Para las instancias aprovisionadas con CCDM, use [Commerce Admin en Adobe Unified Experience](../../getting-started/admin-unified-experience.md) para configurar las vistas y directivas del catálogo y asociar los libros de precios sincronizados con las vistas del catálogo. Las instancias que utilizan el servicio de catálogo con Live Search y Product Recommendations no tienen acceso a estas pantallas de administración de catálogos.

## Funcionamiento de las vistas de catálogo

Una vista de catálogo reúne los datos del catálogo y la configuración para un contexto de tienda. Se puede utilizar para representar una unidad de negocio, marca, región u otra experiencia de tienda.

- **[Las fuentes de catálogo](catalog-sources.md)** proporcionan datos de producto para las experiencias de catálogo.
- **[Directivas](policies.md)** filtran los datos de productos para una vista de catálogo.
- **[Los libros de precios](pricebooks.md)** proporcionan datos de precios asociados con una vista de catálogo.

Las vistas de catálogo no reemplazan la estructura del sitio web, la tienda y la vista de tienda en Adobe Commerce as a Cloud Service. Commerce Foundation sigue administrando esa estructura y las operaciones transaccionales.

Los datos de catálogo se sincronizan de una manera desde Commerce Foundation a CCDM. CCDM admite las experiencias de catálogo de tiendas y la detección de productos. Commerce Foundation sigue encargándose del carro de compras, el cierre de compra, las promociones, los clientes y los pedidos.

## Antes de comenzar

Antes de configurar una vista de catálogo:

- [Confirme que la instancia de Adobe Commerce as a Cloud Service utiliza CCDM](../overview.md).
- Confirme que los datos del catálogo necesarios para la tienda se han rellenado y [sincronizado](data-sync.md).
- Identifique el [origen del catálogo](catalog-sources.md), las [políticas](policies.md) y los [libros de precios](pricebooks.md) necesarios para el contexto de la tienda.
- Determine si necesita crear vistas de catálogo B2C manualmente o revisar las vistas de catálogo B2B generadas por la sincronización nativa.

>[!NOTE]
>
>Para implementaciones B2B, la sincronización nativa genera vistas de catálogo, directivas y libros de precios a partir de la configuración B2B en Commerce Foundation. No cree duplicados manualmente de estas estructuras generadas automáticamente.

## Creación de una vista de catálogo para una implementación B2C

Utilice este flujo de trabajo cuando la implementación B2C requiera que las vistas de catálogo se configuren manualmente.

1. Inicie sesión en [Commerce Admin en Unified Experience](../../getting-started/admin-unified-experience.md) y seleccione la instancia de Adobe Commerce as a Cloud Service aprovisionada con CCDM.
1. En el panel de navegación izquierdo, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Catalog Views]**.
1. Seleccione **[!UICONTROL Create catalog view]**.
1. Introduzca un nombre para la vista de catálogo.
1. Seleccione el [origen o orígenes de catálogo](catalog-sources.md) para el contexto de tienda.
1. Asocie las [directivas](policies.md) relevantes con la vista de catálogo.
1. Asocie los libros de precios relevantes con la vista de catálogo mediante [configuración de la disponibilidad del libro de precios](pricebooks.md).
1. Cree la vista de catálogo.

## Vistas del catálogo B2B

Para implementaciones B2B, la sincronización nativa genera vistas de catálogo, directivas y libros de precios a partir de la configuración B2B en Commerce Foundation. Administre el catálogo B2B subyacente y las relaciones de compañía en Commerce Foundation, en lugar de crear manualmente estructuras duplicadas en CCDM.

Para obtener instrucciones de configuración, consulte [Crear un catálogo compartido](../../b2b/catalog-shared-create.md) y [Asignar compañías a un catálogo compartido](../../b2b/catalog-shared-assign-companies.md).

Después de configurar las relaciones B2B:

1. Confirme que la [sincronización](data-sync.md) se ha completado.
2. Revise las vistas del catálogo, [directivas](policies.md) y [libros de precios](pricebooks.md) que se han generado en [Commerce Admin en Unified Experience](../../getting-started/admin-unified-experience.md).
3. Compruebe que la tienda muestra el surtido de productos y los precios esperados para la empresa.
4. Pruebe el complemento al carro, el carro y el cierre de compra para confirmar que la disponibilidad del producto y los precios de transacción coinciden con la configuración B2B prevista.

## Libros de precios y caja

Los libros de precios proporcionan los datos de precios disponibles a través de una vista de catálogo. En Adobe Commerce as a Cloud Service, Commerce Foundation sigue siendo la fuente fiable de los precios, y los datos de precios se sincronizan con CCDM mediante la integración nativa. Al configurar una vista de catálogo, utilice los libros de precios sincronizados aplicables en lugar de precios de creación independiente en CCDM.

El carro y el cierre de compra utilizan los precios de Commerce Foundation. Verifique que los precios de la tienda mostrados coincidan con los precios aplicables del carro de compras y del cierre de compra.

## Revisión y validación de una vista de catálogo

Después de configurar una vista de catálogo, verifique la experiencia completa de la tienda:

- Confirme que los datos del catálogo deseados están [sincronizados](data-sync.md).
- Confirme que la vista del catálogo está asociada con las [directivas](policies.md) y los [libros de precios](pricebooks.md) deseados.
- Compruebe que la tienda devuelve el surtido de productos esperado.
- Verifique los precios mostrados con los precios correspondientes de Commerce Foundation.
- Probar el complemento al carro, el carro y el cierre de compra.

En el caso de implementaciones B2B, confirme también que las estructuras de catálogo generadas por la sincronización coinciden con la configuración de empresa y catálogo prevista.

## Resolución de problemas

### Faltan productos en la tienda

- [Confirme que la instancia utiliza CCDM](../overview.md).
- Confirme que los datos del catálogo tienen [sincronizado](data-sync.md).
- Compruebe que la tienda esté usando el contexto de catálogo deseado.
- Revise las [directivas](policies.md) asociadas con la vista de catálogo.

### El precio mostrado es inesperado

- Confirme que el [libro de precios](pricebooks.md) deseado esté asociado con la vista del catálogo.
- Compruebe que los datos de precios estén [sincronizados](data-sync.md) y sean coherentes con Commerce Foundation.

  Consulte [Libros de precios](pricebooks.md) para ver las asignaciones de precios del sitio web y del grupo de clientes.

- Valide el precio de nuevo en el carro y cierre de compra.

### Las pantallas del catálogo de CCDM no son visibles en el administrador de Commerce

[Confirme que la instancia seleccionada utiliza CCDM](../overview.md) y que está accediendo a [Commerce Admin en Unified Experience](../../getting-started/admin-unified-experience.md). Una instancia que ejecuta los servicios de catálogo v1 no tiene las pantallas de administración de CCDM.

## Contenido relacionado

- [Introducción a Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/es/docs/commerce/cloud-service/getting-started)
- [Resumen del catálogo compartido Adobe Commerce B2B](../../b2b/catalog-shared.md)
- [Notas de la versión de Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/es/docs/commerce/cloud-service/release-notes)
- [Sincronización de catálogo](data-sync.md)
