---
title: Enriquecimiento de catálogo
description: Utilice el enriquecimiento de catálogo [!DNL Adobe Commerce] para revisar la copia de producto sugerida por IA, crear trabajos de enriquecimiento e implementar actualizaciones aprobadas para la detección de LLM e AI.
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
source-git-commit: b2a1abb72839717a7249e9a34b13266b8e384189
workflow-type: tm+mt
source-wordcount: '1976'
ht-degree: 0%
---
# Enriquecimiento del catálogo

El enriquecimiento del catálogo es una funcionalidad nativa de [!DNL Adobe Commerce] que le ayuda a mejorar los nombres de los productos y las descripciones largas para que el catálogo se represente con mayor precisión cuando los compradores utilizan LLM y asistentes de IA para la investigación y el descubrimiento de productos.

## Cómo funciona {#how-it-works}

El catálogo de productos [!DNL Adobe Commerce] es el sistema de registro de los datos de productos: nombres, descripciones, atributos, precios e inventario. [!DNL Adobe Commerce] conecta los datos del catálogo en vivo con las experiencias de Adobe AI. A partir de ahí, el agente de catálogo puede identificar lagunas en los nombres de los productos y las descripciones largas, proponer mejoras y escribir los cambios aprobados de nuevo en Commerce para que pueda revisarlos en el administrador de Commerce.

Con el enriquecimiento del catálogo, puede:

- Identifique las lagunas e incoherencias en los nombres de los productos y las descripciones largas que afectan a la interpretación de los productos por parte de los LLM.
- Revise las mejoras sugeridas con contexto de soporte, incluidas justificaciones y comparaciones del antes y después.
- Aplique las actualizaciones aprobadas directamente al catálogo de Commerce para que el administrador, la tienda y otros canales que lean esos campos permanezcan alineados.

Dado que los nombres de los productos y las descripciones largas residen en Commerce, la mejora de la copia una vez puede beneficiar a todos los canales que consumen esos datos de productos. La ventaja depende de cómo y cuándo se actualicen los sistemas.

| Dirección | Finalidad |
| --- | --- |
| catálogo Commerce -> análisis | Las señales de tráfico de catálogo y agente descubren oportunidades de sugerencias de enriquecimiento. |
| Enrichment -> Catálogo de Commerce | Después de aprobar una actualización, los cambios en el nombre y la descripción del producto se guardan en el catálogo de Commerce para que el administrador y la tienda reflejen los valores optimizados. |

### Acceso al enriquecimiento del catálogo

Antes de empezar, revise los [requisitos previos de detección de productos de IA](prerequisites.md) específicos de la implementación. Después de completar la configuración de la plataforma de Commerce, vaya a **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]** en Admin.

![Tablero de enriquecimiento de catálogo](assets/catalog-enrich-dashboard.png){zoomable="yes"}

El área de trabajo de enriquecimiento de catálogo incluye las fichas **[!UICONTROL Optimizations]**, **[!UICONTROL Brand governance]** y **[!UICONTROL Settings]**.

- Utilice la ficha **[!UICONTROL Optimizations]** para revisar las señales de detección basadas en tráfico del agente y administrar los trabajos de enriquecimiento.
- Use la ficha **[!UICONTROL Brand Governance]** para [definir requisitos](brand-governance.md) para nombres y descripciones de productos generados por [!DNL Commerce Catalog Agent].
- Use la ficha **[!UICONTROL Settings]** para [conectar su instancia de Commerce](settings.md) al descubrimiento de productos de IA.

La extensión compartida también permite el enriquecimiento de PDP, que tiene un flujo de trabajo independiente para exponer hechos de productos estructurados a agentes de IA. Ver [enriquecimiento de la página de detalles del producto](pdp-enrichment.md).

## Dos rutas de enriquecimientos de catálogo

Existen dos rutas para recibir enriquecimientos de catálogo:

- **Tráfico de agente**: este tipo de enriquecimiento se inicia automáticamente de 24 a 48 horas después de configurar la instancia de Commerce y muestra los resultados en la ficha **Optimizaciones**.
- **Administrador de enriquecimiento**: los comerciantes configuran estos enriquecimientos cuando hacen clic en el botón **[!UICONTROL Create enrichment]** y seleccionan manualmente las SKU que se van a enriquecer. Más información sobre [el administrador de enriquecimiento](#create-an-enrichment-job).

### Revisión y aplicación del enriquecimiento del catálogo {#review-and-apply}

Una vez habilitado y configurado el enriquecimiento del catálogo, utilice la pestaña **[!UICONTROL Optimizations]** para revisar las perspectivas de tráfico de búsqueda y agénticas y administrar los trabajos de enriquecimiento.

### Revisar el tráfico agéntico mensual

Cada auditoría de tráfico auténtica mensual identifica las SKU de alto tráfico y pone a disposición un lote recomendado. Las optimizaciones para revisión se generan automáticamente para los SKU de alto tráfico agéntico. Estas optimizaciones se generan automáticamente en función de la regla de gobernanza &quot;Predeterminada&quot;. Las tarjetas mensuales muestran el recuento de productos, las visitas de los agentes de IA y el estado del trabajo. El tráfico automático y los lotes autoseleccionados utilizan el mismo flujo de trabajo de selección, confirmación, ejecución, revisión e implementación de reglas.

### Revisar trabajos que requieren atención

La sección **[!UICONTROL Needs your attention]** resalta los trabajos que necesitan acción, incluidos los trabajos completados listos para su revisión. Abra un trabajo completado para revisar los cambios de producto propuestos antes de la implementación.

### Buscar trabajos

La tabla **[!UICONTROL All jobs]** enumera cada ID de trabajo, nombre, origen, recuento de SKU, regla utilizada, hora de inicio y estado. Los orígenes identifican si un lote se seleccionó automáticamente o se recomendó a partir del tráfico auténtico. Rastrear estado de procesamiento como **[!UICONTROL Queued]**, **[!UICONTROL Running]**, **[!UICONTROL Completed]** o **[!UICONTROL Failed]**. En el área de trabajo de optimizaciones, estos trabajos también pueden aparecer como **[!UICONTROL Generating]** mientras se ejecutan, **[!UICONTROL Ready to review]** cuando se completa la generación y **[!UICONTROL Deployed]** después de que se implementen los cambios aprobados. Puede ejecutar varios trabajos simultáneamente. Vuelva a intentar un trabajo con error con **[!UICONTROL Retry]**.

### Creación de un trabajo de enriquecimiento

**Para crear un enriquecimiento de catálogo:**

![Crear enriquecimiento de catálogo](./assets/create-cat-enrich.png){zoomable="yes"}

1. En **[!UICONTROL Optimizations]**, haga clic en **[!UICONTROL Create enrichment]**.
1. Escriba un **nombre de enriquecimiento**, como &quot;Black Friday 2026&quot;.
1. Seleccione la **categoría**, como &quot;Café&quot;.
1. Seleccione el **conjunto de atributos**, como &quot;Accesorios&quot;.
1. Seleccione **Tipo de producto**, como &quot;Producto simple&quot;.
1. Seleccione **Intervalo de precios**.
1. Haga clic en **[!UICONTROL Apply filters]**.

   Puede obtener una vista previa de los productos que coinciden con los criterios de enriquecimiento y hacer clic en **Personalizar** para ampliar el ámbito de los productos que desea enriquecer.

1. Haga clic en **[!DNL Next]** y previsualice la [regla de gobernanza](brand-governance.md) que se está aplicando a su enriquecimiento.
1. Haga clic en **[!DNL Next]** para confirmar los productos específicos que desea enriquecer.
1. Haga clic en **[!DNL Run enrichment]**.

   El trabajo de enriquecimiento se ejecuta y se muestra en la tabla Optimizaciones. Cuando termine de ejecutarse, puede [Revisar e implementar](#review-deploy-catalog) las optimizaciones.

### Revisión e implementación de un trabajo de enriquecimiento {#review-deploy-catalog}

Abra un trabajo de enriquecimiento.

![Lista de direcciones URL de enriquecimiento de catálogo](./assets/catalog-enrich-urls.png){zoomable="yes"}

La tabla **URL con sugerencias** enumera todos los productos con oportunidades de enriquecimiento. Para cada producto puede:

- **Expanda la fila** para ver el análisis de IA y el enriquecimiento propuesto.
- **Edite** el nombre o la descripción del producto propuesto antes de aplicar, para alinearlo con las directrices de comercialización y voz de su marca.
- **Implemente la optimización** para los productos que desea enriquecer y publíquelo directamente en su catálogo de Adobe Commerce.
- **Marcar como fijo** una vez que se haya revisado y aplicado el enriquecimiento.
- **Ignorar** sugerencias que no sean relevantes para su estrategia de catálogo.

Las sugerencias están organizadas en tres vistas: **Sugerencias actuales**, **Sugerencias fijas** y **Sugerencias ignoradas**. Una vez aplicado un enriquecimiento, pasa a Fixed Suggestions con un estado de **Applied** y una acción de **View in Catalog** para comprobar la actualización en Adobe Commerce. Los enriquecimientos aplicados se pueden revertir en cualquier momento, restaurando el nombre y la descripción del producto original.

## Verificar enriquecimiento en el administrador {#verify-in-admin}

**Para comprobar el enriquecimiento del catálogo aplicado:**

1. Vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]** en el Administrador de Commerce.
1. Use los filtros y el selector **[!UICONTROL Store View]** según sea necesario (por ejemplo, **[!UICONTROL Default Store View]**).
1. Busque el SKU.
1. Abra el producto en modo de edición.

   El formulario del producto muestra el nombre y/o la descripción del producto enriquecido.

   ![Nombre de producto enriquecido](./assets/enriched-product-name.png){zoomable="yes"}

1. Opcional: seleccione **[!UICONTROL Override Catalog Agent provided Product Name]** si desea conservar un nombre ingresado manualmente en su lugar.

   Las anulaciones manuales afectan a la forma en que las sugerencias permanecen sincronizadas con el catálogo. Para obtener más información, consulte [Anulación manual en Admin](#manual-override-in-the-admin).

1. Expanda la sección **[!UICONTROL Content]** y busque el campo de descripción.

   La descripción enriquecida aparece cuando se aplican cambios de descripción.

   ![Enriquecer descripción del producto](./assets/enrich-product-description.png){zoomable="yes"}

1. Opcional: seleccione **[!UICONTROL Override Catalog Agent provided Description]** si desea conservar una descripción introducida manualmente en su lugar.

Las anulaciones manuales afectan a la forma en que las sugerencias permanecen sincronizadas con el catálogo. Para obtener más información, consulte [Anulación manual en Admin](#manual-override-in-the-admin).

## Verificar enriquecimiento en la tienda {#verify-storefront}

**Para comprobar el enriquecimiento en la tienda:**

1. Busque el SKU en su tienda.
1. Abra la página del producto.
1. Confirme que el nombre y la descripción del producto coinciden con lo que ha aprobado.

   Puede tomar algún tiempo antes de que los enriquecimientos aparezcan en tu tienda.

1. Confirme que las regiones que muestran la descripción larga coinciden con lo que ha aprobado.
1. Opcional: Confirme los canales descendentes que consumen los mismos atributos de catálogo, cuando sean relevantes para el despliegue.

## Invalidaciones, ingesta y sugerencias obsoletas {#overrides-ingestion}

Después de que el enriquecimiento del catálogo actualice el nombre o la descripción de un producto, otros sistemas de ingesta pueden cambiar los mismos campos. Algunos ejemplos son llamadas a la API de REST, importaciones de CSV y fuentes PIM.

### Valor original reintroducido {#original-value-reingested}

Si un proceso externo escribe el nombre o la descripción originales (el valor que existía antes de aplicar el enriquecimiento), Commerce sigue respetando el valor enriquecido para ese campo según las reglas de enriquecimiento del catálogo. Es posible que la sugerencia no se revierta automáticamente solo en función de esa ingesta.

### Nuevo valor reintroducido {#new-value-reingested}

Si el proceso externo envía un nuevo valor que no es una repetición del texto previo al enriquecimiento, Commerce respeta el nuevo valor de catálogo. Por ejemplo, si cambia el nombre de &quot;Zapatos rojos&quot; a &quot;Zapatos rojos icónicos&quot;, se sustituye el valor enriquecido. La sugerencia de enriquecimiento relacionada generalmente se marca como *Obsoleta* porque el catálogo en vivo ya no coincide con el contexto de la sugerencia.

### Anulación manual en el administrador {#manual-override-in-the-admin}

Si edita manualmente el nombre o la descripción del producto en el administrador de [!DNL Adobe Commerce]:

- El valor Admin gana como sistema de registro para ese cambio manual.
- La sugerencia de enriquecimiento está marcada *Desactualizada*.
- El flujo de trabajo de sugerencias vuelve al estado original de ese elemento para que pueda volver a aprobar o aceptar una nueva sugerencia si el análisis se vuelve a ejecutar.

Estas reglas le ayudan a saber si el enriquecimiento del catálogo, las fuentes de ingesta o las ediciones de administración son autorizadas cuando varios canales tocan el mismo SKU.

## Límites y consideraciones {#limits}

- El enriquecimiento solo se aplica a nombres de productos y descripciones largas. No cambia el diseño de página de detalles del producto, los widgets u otro contenido de tienda de nivel de página.
- Los catálogos grandes y los recuentos altos de URL pueden afectar a la rapidez con la que se completa el análisis y a la cantidad de sugerencias que aparecen a la vez.
- Las sugerencias significativas suponen que los bots relevantes para LLM pueden acceder a las direcciones URL del producto que le interesan. Las reglas, la autenticación, el bloqueo geográfico y la personalización avanzada de los robots pueden reducir la cobertura.

## Prácticas recomendadas {#best-practices}

- Documente la propiedad del sistema para el nombre y la descripción del producto de modo que los trabajos de PIM o de fuentes no entren en conflicto involuntariamente con el enriquecimiento del catálogo.
- Coordínese con los equipos de SEO y de marca antes de aplicar títulos o descripciones por lotes.
- Volver a sincronizar o analizar después de las importaciones del catálogo principal para que las sugerencias reflejen el estado del catálogo actual.

## Ejemplos

Los siguientes ejemplos muestran cómo el enriquecimiento del catálogo convierte los atributos técnicos sin procesar en una copia narrativa del producto centrada en el comprador que los LLM pueden utilizar para responder preguntas de compra.

### Ejemplo: Producto de café con atributos técnicos

El catálogo de la retailer de café almacena solamente las especificaciones técnicas de un producto de grano de café tostado mediano: variedad de grano, región de origen, método de procesamiento, nivel de tostado y rango de altitud. Estos campos describen el producto, pero no comunican su valor a un comprador, por lo que un asistente de IA tiene poco con qué trabajar al responder una pregunta como &quot;¿qué café tiene un sabor suave y poco ácido?&quot;

El enriquecimiento del catálogo lee los atributos técnicos y las razones a través de cómo interactúan para inferir características relevantes para el comprador:

| Atributo técnico | Característica deducida | Razonar |
| --- | --- | --- |
| Proceso de miel, asado de Medium | Baja acidez | El mucílago del fruto que queda en el frijol durante el procesamiento de la miel suprime la acidez, y el tostado medio descompone los compuestos ácidos residuales. |
| Proceso de miel, Arábica, Medium asado | Sabor a avellana | Los azúcares de frutas del mucílago se combinan con las notas de frutos secos naturales de Arábica, amplificadas a medio asado. |
| Proceso de miel, Arábica | Sensación de boca rica y cremosa | Los aceites absorbidos por el mucílago durante el secado añaden viscosidad y cuerpo. |
| Proceso de miel, altitud 900-1200m | Troncos de caramelo | Los granos más densos y de gran altitud desarrollan azúcares más complejos, profundizados por el procesamiento de la miel. |

El enriquecimiento del catálogo aplica estas características inferidas a la copia del producto:

- **Antes**: &quot;Granos de café asados Medium - Arabica, Brasil Minas Gerais, Proceso de miel, 900-1200 m&quot;
- **Después**: &quot;Los frijoles árabes cultivados a 900-1200 m en Minas Gerais de Brasil, procesados con miel y tostados medianos, desarrollan un tacto bucal naturalmente dulce y cremoso con un marcado carácter avellana, tonos caramelo y baja acidez. Un café especial consistente y accesible que se experimenta mejor con el vertido&quot;.

El nombre y la descripción actualizados se guardan directamente en el catálogo de Commerce, por lo que la tienda, las fuentes LLM y otros canales que leen esos campos reflejan la misma copia enriquecida.

### Ejemplo: Configuración de muebles modulares

Un mueble retailer vende un sofá de sección modular en el que la descripción del producto solo enumera los códigos de configuración y el nombre de la estructura, por ejemplo, `6 Standard Seats + 6 Standard Sides in Sapphire Navy Corded Velvet`. Este método abreviado es comprensible para un cliente que regresa, pero le da a un asistente de IA poco contexto sobre cómo funciona el producto o qué lo hace duradero o cómodo.

El enriquecimiento de catálogo amplía los atributos de configuración y estructura en una descripción narrativa que explica qué hace cada componente y por qué importa a un comprador:

- **Antes**: &quot;6 asientos estándar + 6 laterales estándar en terciopelo con cable de la marina de zafiro&quot;
- **Después**: &quot;Esta configuración incluye 6 juegos de inserciones de asientos estándar y 6 inserciones laterales estándar que funcionan indistintamente como brazos o respaldos, formando los bloques modulares de construcción de su diseño. Cada asiento cuenta con espuma estándar con tres capas de alta densidad diseñadas para preservar la elevación y resistir la flacidez. La funda de terciopelo con cordones Sapphire Navy es tan duradera como lujosa, con cordones con textura que crean un brillo sutil y una sensación suave y lujosa. Las fundas están cosidas a mano para lograr un aspecto preciso y personalizado, y son lavables a máquina y cambiables, por lo que su sección puede evolucionar con su espacio&quot;.

Debido a que la descripción enriquecida se escribe de nuevo en el catálogo de Commerce, está disponible para bots de IA que rastrean por la página de detalles del producto, así como para cualquier canal descendente o fuente que consuma los datos del catálogo del producto, sin cambiar el diseño que los compradores ven en la página.
