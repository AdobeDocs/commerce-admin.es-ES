---
title: Resumen de servicios de comercialización
description: Obtenga información acerca de la configuración de catálogo, las herramientas de comercialización, creación de informes y monitorización para instancias de Adobe Commerce as a Cloud Service aprovisionadas con CDM.
recommendations: noCatalog
badgeSaas: label="Solo SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a instancias de Adobe Commerce as a Cloud Service aprovisionadas con CCDM (infraestructura de SaaS administrada por Adobe)."
exl-id: f9516d4c-fbae-4db2-a1a9-cda3684a8122
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: a6a5a899ba60097bd6baf2a5de14063a0af2f313
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%
---
# Información general sobre los servicios de comercialización con CCDM

Las instancias de Adobe Commerce as a Cloud Service aprovisionadas con el Modelo de datos de catálogo compuesto (CCDM) proporcionan herramientas de configuración, comercialización, creación de informes y supervisión de catálogo en [Commerce Admin en Adobe Unified Experience](../getting-started/admin-unified-experience.md). CCDM es la misma base de catálogo que alimenta Adobe Commerce Optimizer.

Con los servicios de comercialización, puede:

- Utilice los datos del catálogo de la instancia de as a Cloud Service de Adobe Commerce para admitir experiencias de tienda.
- Configure las vistas de catálogo y las directivas para definir los surtidos de productos de tienda.
- Aplique reglas de comercialización en todas las vistas de catálogo o ajústelas a una vista específica.
- Configure recomendaciones de productos, facetas de búsqueda y sinónimos.
- Revise el rendimiento de la tienda mediante las Métricas de éxito y los informes de rendimiento de búsqueda.
- Monitorice la sincronización de catálogos y los eventos de tienda capturados.

Commerce Foundation sigue siendo la fuente fiable de productos y precios, y continúa administrando el carro de compras, el cierre de compra y otras operaciones transaccionales.

## Recorrido rápido

>[!BEGINTABS]

>[!TAB Configuración del catálogo]

Configurar el contexto de catálogo disponible para una tienda.

- **Vistas de catálogo**: combina fuentes de catálogo, directivas y libros de precios para definir los productos y los precios que una tienda puede recuperar. Ver [vistas de catálogo](./setup/catalog-view.md).
- **Capas de catálogo**: anula los atributos de producto seleccionados sin cambiar los datos de origen. Cuando se utilizan AEM Assets para imágenes de producto, el nivel AEM-Assets se aplica a través de las imágenes del producto. Ver [capas de catálogo](./setup/catalog-layer.md).
- **Vistas de catálogo privado**: habilite Protección de catálogo para requerir un token firmado válido al recuperar datos de vista de catálogo. Ver [vistas de catálogo privado](./setup/private-catalog-view.md).

>[!TAB Directivas]

Las directivas filtran los productos disponibles a través de una vista de catálogo en función de los atributos del producto. Por ejemplo, una directiva puede limitar un surtido a una marca o categoría de producto en particular.

Las directivas determinan la gama de productos disponible. No reemplazan a Protección de catálogo, que controla el acceso a una vista de catálogo privada.

>[!TAB Comercialización]

Configure cómo los compradores descubren los productos y cómo se promocionan los productos dentro del surtido disponible.

- **Oportunidades**: revise el rendimiento del producto, el comportamiento del comprador y las tendencias de búsqueda para identificar áreas en las que se pueden realizar mejoras en la comercialización.
- **Recommendations**: cree y administre unidades de recomendación en el administrador de Commerce. Recommendations utiliza los datos del catálogo y el comportamiento agregado del comprador para sugerir productos relevantes, como &quot;Los clientes que vieron este producto también vieron&quot;.
- **Reglas de comercialización**: controla cómo se promocionan y clasifican los productos. Las reglas se pueden aplicar en todas las vistas de catálogo o adaptarse a una vista específica. Consulte [Crear una regla de comercialización](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/add#create-a-rule).
- **Facetas**: configure los filtros que utilizan los compradores para reducir los resultados de los productos según atributos como marca, tamaño o precio.
- **Sinónimos**: asocie términos de búsqueda equivalentes para ayudar a los compradores a encontrar productos usando palabras diferentes para el mismo concepto.
- **Configuración**: configure las opciones de búsqueda y comercialización, incluidas las facetas de precio, el idioma y la búsqueda avanzada.

Las directivas determinan qué productos están disponibles a través de una vista de catálogo. Las reglas de comercialización controlan cómo se promocionan y clasifican los productos dentro de ese surtido.

Para obtener detalles sobre cómo se comparan y clasifican los resultados de búsqueda, consulte [Coincidencia y clasificación de búsquedas](./manage-results/search-relevance-matching.md).

>[!TAB Informes]

Use informes para revisar la actividad de la tienda e informar las decisiones de comercialización.

- **Métricas de éxito**: revise los ingresos, la conversión, la participación, las adquisiciones y la tasa de devolución en función de la actividad de la tienda.
- **Rendimiento de búsqueda**: revise los términos de búsqueda que usan los compradores y su rendimiento para identificar áreas en las que se pueda refinar la detección de productos.

Los informes dependen de los datos de actividad de tienda recopilados por la implementación.

>[!TAB Configuración del sistema]

Monitorice la sincronización de catálogos y la recopilación de eventos de tienda para investigar los problemas de disponibilidad e implementación de datos.

- **Sincronización de catálogo**: revise el estado de sincronización de los datos de catálogo transferidos desde Commerce Foundation.
- **Eventos**: revisa los eventos de tienda capturados que usan la detección de productos, las recomendaciones y los informes. Utilice la página Eventos para verificar la recopilación de datos de comportamiento e investigar los eventos que faltan o inesperados.

>[!ENDTABS]
<!--
Watch the following video for a high-level overview of [!DNL Adobe Commerce Optimizer]:

>[!VIDEO](https://video.tv.adobe.com/v/3450226)
-->

## Confirme que una instancia utiliza CDM.

1. Inicie sesión en Commerce Admin a través de Unified Shell y seleccione la instancia de Adobe Commerce as a Cloud Service deseada.
1. Confirme que las páginas de comercialización de CCDM, como las vistas de catálogo y las directivas, estén disponibles en la navegación de la instancia.
1. Si esas páginas no están disponibles, confirme que ha seleccionado la instancia correcta y que está utilizando Unified Shell.

   Póngase en contacto con el equipo de Asistencia de Adobe o con el equipo de aprovisionamiento de Commerce para comprobar el estado de aprovisionamiento de la instancia de CCDM.

El estado Listo de la instancia confirma que está aprovisionada, pero no confirma por sí solo que utiliza CDM.

