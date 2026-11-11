---
title: Tareas de comercialización de catálogo por función
description: Encuentre orientación sobre tareas para administradores, desarrolladores y comerciantes que trabajan con instancias de Adobe Commerce as a Cloud Service aprovisionadas con CDM.
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="Solo SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a instancias de Adobe Commerce as a Cloud Service aprovisionadas con CCDM (infraestructura de SaaS administrada por Adobe)."
TQID: 'https://experienceleague.adobe.com/0PmobUkdEWspxuRSaIPL8vS1ojDDZ3gw-L-3SfPmJAg'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: cc04bd17-78d5-5120-8c3d-1b8a57e49280
    internal-label: Integration
  - id: dec06508-d41f-555a-87e8-29e8bcdfa95a
    internal-label: Recommendations
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
  - id: f37757d8-3174-5335-b977-1161792f965d
    internal-label: Personalization
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: dba482e5-29a8-4127-afa2-c4b913512ef8
    internal-label: Data and analytics
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 742236e7fdb26c56a80f66a44b0a4960210f4dac
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%
---

# Tareas de comercialización de catálogo por función

Utilice esta referencia de tarea para encontrar instrucciones para configurar los datos del catálogo, integrar la tienda, administrar la comercialización y revisar el rendimiento en las instancias de Adobe Commerce as a Cloud Service aprovisionadas con el Modelo de datos de catálogo compuesto (CCDM).

Las responsabilidades varían según la implementación. Las siguientes secciones agrupan las tareas según las funciones que generalmente las realizan.

- Los administradores administran productos, precios y la configuración B2B en Commerce Foundation.
- Los desarrolladores configuran la integración de tiendas y verifican las solicitudes de catálogo y la recopilación de datos de comportamiento.
- Los comerciantes configuran el descubrimiento de productos y las recomendaciones, y utilizan la creación de informes para informar las decisiones de comercialización.

Los datos de productos y precios se sincronizan con CCDM mediante la integración nativa de Adobe Commerce as a Cloud Service. No es necesario instalar el conector por separado ni la aplicación de App Builder.

## Preparar el catálogo y la tienda

Complete las tareas que se aplican a su implementación. Las vistas del catálogo B2C se pueden crear manualmente. Las vistas de catálogo, las políticas y los libros de precios B2B se generan a partir de la configuración B2B en Commerce Foundation.

| Tarea | Descripción | Recursos |
| --- | --- | --- |
| **Configurar productos y precios** | Administrar productos y precios en Commerce Foundation. Los datos de precios se sincronizan con el CCDM como libros de precios; no cree precios de forma independiente en el CCDM. | [Lista de productos](../catalog/products-list.md), [Crear un producto](../catalog/product-create.md), [Precios](../catalog/catalog-price-scope.md) y [Precios avanzados](../catalog/pricing-advanced.md) |
| **Configurar vistas de la tienda** | Configure las vistas de tienda y los datos de productos localizados necesarios para su tienda en Commerce Foundation. | [Vistas de tienda](../stores-purchase/store-views.md) |
| **Configurar empresas y catálogos compartidos B2B** | Para implementaciones B2B, configure los catálogos compartidos y las relaciones con la empresa en Commerce Foundation antes de revisar la configuración del catálogo generada. | [Catálogos compartidos](../b2b/catalog-shared.md) y [Compañías](../b2b/account-companies.md) |
| **Configurar vistas y directivas del catálogo B2C** | Cree vistas de catálogo y seleccione las directivas que definen el surtido de productos disponible. Asocie los libros de precios sincronizados aplicables a cada vista. | [Vistas de catálogo](./setup/catalog-view.md) |
| **Revisar vistas del catálogo B2B** | Confirme que la sincronización nativa ha generado las vistas de catálogo, las directivas y los libros de precios esperados. Administre la configuración B2B subyacente en Commerce Foundation en lugar de crear estructuras duplicadas manualmente. | [Vistas del catálogo B2B](./setup/catalog-view.md#b2b-catalog-views) |
| **Configurar la tienda** | Configure la tienda para solicitar el contexto de catálogo deseado. Para integraciones de tienda personalizadas o de otro tipo, revise los encabezados de solicitud de catálogo aplicables. | [Configuración de tienda](https://experienceleague.adobe.com/en/tools/commerce-storefront/setup/configuration/commerce-configuration/) |

Antes de configurar la comercialización, confirme que la tienda devuelve los productos y precios esperados. Pruebe el complemento al carro, el carro y el cierre de compra para verificar que los precios de transacción coincidan con la configuración de Commerce Foundation deseada.

## Configurar el rendimiento de comercialización y revisión

| Tarea | Descripción | Recursos |
| --- | --- | --- |
| **Configurar la detección de productos** | Configurar reglas, facetas y sinónimos de comercialización. Las reglas se pueden aplicar en todas las vistas de catálogo o adaptarse a una vista específica. | [Resumen de comercialización](./merchandising/overview.md) |
| **Revisar la configuración de búsqueda** | Revise la configuración de búsqueda y las opciones de búsqueda semántica disponibles para la implementación. | [Configuración de comercialización](./settings.md) y [Búsqueda semántica](./setup/semantic-search.md) |
| **Configurar recomendaciones** | Cree unidades de recomendación y compruebe que la tienda recopila los datos de comportamiento requeridos por la implementación. | [Resumen de recomendaciones](./merchandising/recommendations/overview.md) |
| **Revisar rendimiento** | Utilice las métricas de éxito y los informes de rendimiento de búsqueda para evaluar la actividad de la tienda e informar las decisiones de comercialización. | [Métricas de éxito](./manage-results/success-metrics.md) y [Rendimiento de búsqueda](./manage-results/search-performance.md) |

## Pasos siguientes

Después de configurar la comercialización y revisar el rendimiento, siga supervisando y ajustando las reglas, facetas y recomendaciones según sea necesario para optimizar la experiencia de la tienda.
