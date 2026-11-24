---
title: Enriquecimiento de página de detalles del producto
description: Utilice el enriquecimiento de página de detalles del producto [!DNL Adobe Commerce] para revisar la copia de producto sugerida por IA, crear trabajos de enriquecimiento e implementar actualizaciones aprobadas para la detección de LLM e AI.
role: Admin, User, Leader
recommendations: noCatalog
touch: true
badgePaas or on-premises: label="Cloud or on-premises only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed Cloud or on-premises infrastructure) and on-premises projects only."
autotag-review: '2026-06-23T17:36:07.142Z'
TQID: 'https://experienceleague.adobe.com/cjHuva7PP7UzP-yVhe0rkDzHgAYjfSdYEx3g5gorxwk'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c32adafa-ed01-4b31-997e-2413013911b0
    internal-label: Integrations
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9e234eb68fe34171d9e5cf95e8cdab5c31825492
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 0%
---

# Enriquecimiento de página de detalles del producto

El enriquecimiento de la página de detalles del producto (PDP) maximiza la rastreabilidad de los LLM en cada PDP con datos estructurados del producto sin realizar ningún cambio en su experiencia humana visible. Esta capacidad lee el catálogo de productos para crear una carga útil de datos estructurada para cada PDP que los LLM puedan leer y analizar fácilmente.

## Cómo funciona {#how-it-works}

El catálogo de Adobe Commerce contiene información de productos, como atributos, variantes, categorías, precios y disponibilidad. En un trabajo de enriquecimiento de PDP, se seleccionan las páginas de productos y los grupos de hechos de catálogo que se pondrán a disposición de los agentes de IA. La información está organizada para los agentes sin cambiar la experiencia de la tienda.

Con el enriquecimiento de PDP, puede:

- Elija productos habilitados específicos que tengan páginas de productos activas.
- Revise un resumen de las páginas y los hechos seleccionados antes de guardar o ejecutar el trabajo.
- Previsualice la información del producto incluida en el enriquecimiento.

| Dirección | Finalidad |
| --- | --- |
| Catálogo de Commerce -> trabajo de enriquecimiento | Seleccione las páginas de productos en directo y los hechos del catálogo que desea incluir. |
| Trabajo de enriquecimiento -> Agentes de IA | Hacer que la información de producto existente y seleccionada esté disponible en un formulario estructurado. La tienda visible humana no cambia. |

## Acceso a enriquecimiento de PDP

Antes de empezar, revise los [requisitos previos de detección de productos de IA](prerequisites.md) específicos de la implementación. Después de completar la configuración de la plataforma de Commerce, abra **[!UICONTROL AI Product Discovery]** en el Administrador y seleccione **[!UICONTROL Product Details Page Enrichment]**.

## Dos rutas de enriquecimientos de PDP

Existen dos rutas para recibir enriquecimientos PDP:

- **Tráfico de agente**: este tipo de enriquecimiento se inicia automáticamente de 24 a 48 horas después de configurar la instancia de Commerce y muestra los resultados en la ficha **Optimizaciones**.
- **Administrador de enriquecimiento**: estos enriquecimientos los configura el comerciante cuando hace clic en el botón **[!UICONTROL Create enrichment]** y selecciona manualmente las SKU que desea enriquecer. Más información sobre [el administrador de enriquecimiento](#create-an-enrichment-job).

## Revisar actividad de enriquecimiento de PDP

La página de enriquecimiento de PDP se abre en la ficha **[!UICONTROL Optimizations]**. Utilice el tablero para revisar la cobertura del enriquecimiento, la actividad laboral y los trabajos que requieren atención. Use la ficha **[!UICONTROL Settings]** para [vincular](settings.md) su instancia de Commerce al descubrimiento de productos de IA.

### Encuentre trabajos que necesiten atención

La sección **[!UICONTROL Needs your attention]** resalta los trabajos que requieren acción. Una tarjeta puede mostrar el nombre del trabajo, cómo se seleccionaron los productos, el número de páginas de productos, el estado del trabajo y el progreso. Utilice la acción disponible en una tarjeta para continuar con el trabajo.

### Buscar todos los trabajos

Utilice la tabla para buscar y rastrear trabajos. Buscar por detalles de trabajo o filtrar por estado, incluidos **[!UICONTROL Generating]**, **[!UICONTROL Ready to review]**, **[!UICONTROL Deployed]**, **[!UICONTROL Queued]** o **[!UICONTROL Failed]**. En la tabla se muestra el ID, el nombre, el origen, el recuento de páginas de producto, la fecha de inicio, el estado y las acciones disponibles de cada trabajo.

## Creación de un trabajo de enriquecimiento

En esta sección, aprenderá a crear un enriquecimiento de la página de detalles del producto.

![Crear enriquecimiento PDP](./assets/create-cat-enrich.png)

1. En **[!UICONTROL Optimizations]**, haga clic en **[!UICONTROL Create enrichment]**.
1. Escriba un **nombre de enriquecimiento**, como &quot;Black Friday 2026&quot;.
1. Seleccione la **categoría**, como &quot;Café&quot;.
1. Seleccione el **conjunto de atributos**, como &quot;Accesorios&quot;.
1. Seleccione **Tipo de producto**, como &quot;Producto simple&quot;.
1. Seleccione **Intervalo de precios**.
1. Haga clic en **[!UICONTROL Apply filters]**.

   Puede obtener una vista previa de los productos que coinciden con los criterios de enriquecimiento y hacer clic en **Personalizar** para ampliar el ámbito de los productos que desea enriquecer.

1. Haga clic en **[!DNL Next]** para confirmar los productos específicos que desea enriquecer.
1. Haga clic en **[!DNL Run enrichment]**.

   El trabajo de enriquecimiento se ejecuta y se muestra en la tabla **Optimizaciones**. Cuando termine de ejecutarse, puede [Revisar e implementar](#review-and-deploy-an-enrichment-job) las optimizaciones.

### Revisión de un trabajo de enriquecimiento {#review-and-deploy-an-enrichment-job}

Abra un trabajo de enriquecimiento.

![Lista de URL de enriquecimiento de PDP](./assets/pdp-enrich-urls.png)

La tabla **URL con sugerencias** enumera todos los productos con oportunidades de enriquecimiento. Para cada producto puede:

- **Expanda la fila** para ver el análisis de IA y el enriquecimiento propuesto.
- **Edite** el nombre o la descripción del producto propuesto antes de aplicar, para alinearlo con las directrices de comercialización y voz de su marca.
- **Implementar la optimización** para los productos que deseas enriquecer y publicarla directamente en tu tienda de Adobe Commerce.
- **Marcar como fijo** una vez que se haya revisado y aplicado el enriquecimiento.
- **Ignorar** sugerencias que no sean relevantes para su estrategia de catálogo.

Las sugerencias están organizadas en tres vistas: **Sugerencias actuales**, **Sugerencias fijas** y **Sugerencias ignoradas**. Una vez aplicado un enriquecimiento, pasa a **Sugerencias fijas** con un estado de **Aplicado**. Los enriquecimientos aplicados se pueden revertir en cualquier momento.

### Implementación de la optimización

Una vez que haya revisado las sugerencias y seleccionado las páginas de productos que desea optimizar, haga clic en **Implementar optimizaciones** para publicar el enriquecimiento mediante Optimizar en Edge. Un cuadro de diálogo de confirmación de **Implementar en Edge** muestra las direcciones URL del producto seleccionado, el tipo de optimización y el enriquecimiento que se está aplicando. Después de la implementación, una pantalla de confirmación confirma qué páginas de productos se optimizaron correctamente.

La optimización se entrega exclusivamente a los agentes de usuario de IA a través de [Optimizar en Edge](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn). Los visitantes humanos siguen viendo la experiencia existente de la tienda exactamente como antes sin cambios en el diseño de la PDP, el rendimiento de la página o la experiencia de la marca.

## Límites y consideraciones {#limits}

- Solo se pueden seleccionar los productos activados con una página de producto activa.
- El enriquecimiento organiza los hechos que ya están presentes en el catálogo; no agrega información de nuevos productos.
- El flujo de trabajo de enriquecimiento de PDP no cambia la tienda.
- Los trabajos de enriquecimiento de PDP y los trabajos de enriquecimiento de catálogo tienen diferentes propósitos y flujos de trabajo.
- La optimización de PDP usa [Optimizar en Edge](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn)

## Prácticas recomendadas {#best-practices}

- Utilice nombres de trabajo claros que identifiquen el grupo de productos o la campaña.
- Obtenga una vista previa de los hechos incluidos en el trabajo y confirme que son precisos y adecuados para los agentes de IA.
- Compruebe si los productos ya se han enriquecido antes de decidir omitirlos o sobrescribirlos.
- Coordine la sincronización del catálogo y la propiedad de los hechos del producto con los equipos responsables de esos registros.

## Ejemplo: Enriquecimiento de un producto con variantes y especificaciones

Una página de producto suele contener más información del catálogo de la que los agentes de IA pueden leer. Por ejemplo, un comerciante vende una bota de senderismo impermeable. Las opciones de tamaño, anchura y color se encuentran en un selector de variante que se carga con JavaScript. Los materiales, la impermeabilización y las instrucciones de cuidado se ubican en una pestaña de Detalles contraída, y la guía de ajuste se abre en una ventana emergente. Un comprador puede abrir todos estos elementos, pero un rastreador de IA que lea la página cuando se carga por primera vez solo puede ver el nombre del producto, el precio y una breve descripción.

Cuando el trabajo de enriquecimiento se ejecuta en este producto, toma todos los datos del catálogo del producto, incluidos sus atributos y cada variante, y los empaqueta en un formato estructurado que los agentes de IA pueden leer. Un asistente de IA puede responder preguntas como &quot;¿Está disponible esta bota en un ajuste amplio en el tamaño 11?&quot; o &quot;¿Es totalmente impermeable?&quot; a partir de los datos del catálogo del propio comerciante.

El trabajo de enriquecimiento solo utiliza información que ya existe en el catálogo. No crea nuevos hechos del producto y no cambia la página del producto que ven los compradores.
