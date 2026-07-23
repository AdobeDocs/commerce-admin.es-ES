---
title: Enriquecimiento del catálogo
description: Utilice la capacidad de enriquecimiento del catálogo nativo en Adobe Commerce para revisar y aplicar mejoras sugeridas por IA a los nombres de productos y descripciones largas para la detección asistida por LLM y IA.
role: Admin, User, Leader
recommendations: noCatalog
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
autotag-review: '2026-06-23T17:36:07.142Z'
TQID: 'https://experienceleague.adobe.com/cjHuva7PP7UzP-yVhe0rkDzHgAYjfSdYEx3g5gorxwk'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: a5d9ef32b56d3f422e7af6352002ed5827fc185c
workflow-type: tm+mt
source-wordcount: 2182
ht-degree: 0%

---

# Enriquecimiento del catálogo

El enriquecimiento del catálogo es una funcionalidad nativa de [!DNL Adobe Commerce] que le ayuda a mejorar los nombres de los productos y las descripciones largas para que el catálogo se represente con mayor precisión cuando los compradores utilizan LLM y asistentes de IA para la investigación y el descubrimiento de productos.

>[!NOTE]
>
>El enriquecimiento del catálogo funciona con [!DNL Commerce Catalog Agent] y [!DNL Adobe LLM Optimizer] entre bastidores. El enriquecimiento se utiliza como parte del flujo de trabajo del catálogo de Commerce. No administra una integración de LLM Optimizer independiente para aplicar actualizaciones de nombre y descripción aprobadas. Para obtener una supervisión y optimización LLM más amplia fuera de Commerce, consulte la [documentación del producto LLM Optimizer](https://experienceleague.adobe.com/en/docs/llm-optimizer/using/home).

## Cómo funciona {#how-it-works}

El catálogo de productos [!DNL Adobe Commerce] es el sistema de registro de los datos de productos: nombres, descripciones, atributos, precios e inventario. [!DNL Adobe Commerce] El MCP (protocolo de contexto de modelo) de Storefront conecta los datos del catálogo en directo con las experiencias de Adobe AI. A partir de ahí, el agente de catálogo puede identificar lagunas en los nombres de los productos y las descripciones largas, proponer mejoras y escribir los cambios aprobados de nuevo en Commerce para que pueda revisarlos en el administrador de Commerce.

Con el enriquecimiento del catálogo, puede:

- Identifique las lagunas e incoherencias en los nombres de los productos y las descripciones largas que afectan a la interpretación de los productos por parte de los LLM.
- Revise las mejoras sugeridas con contexto de soporte, incluidas justificaciones y comparaciones del antes y después.
- Aplique las actualizaciones aprobadas directamente al catálogo de Commerce para que el administrador, la tienda y otros canales que lean esos campos permanezcan alineados.

Dado que los nombres de los productos y las descripciones largas residen en Commerce, la mejora de la copia una vez puede beneficiar a todos los canales que consumen esos datos de productos. La ventaja depende de cómo y cuándo se actualicen los sistemas.

| Dirección | Finalidad |
| --- | --- |
| catálogo Commerce -> análisis | Sugerencias de enriquecimiento de fuentes de señales de catálogo y URL. |
| Enrichment -> Catálogo de Commerce | Después de aprobar una actualización, los cambios en el nombre y la descripción del producto se guardan en el catálogo de Commerce para que el administrador y la tienda reflejen los valores optimizados. |

## Para quién es esto {#who-this-is-for}

- Especialistas en marketing digital y distribuidores que deseen que los datos de los productos sean precisos y coherentes en las respuestas basadas en LLM.
- Comerciantes y especialistas en marketing digital que necesiten una forma controlada de mejorar las copias de catálogo a escala.
- Administradores de Commerce propietarios de la integridad del catálogo, procesos de administración e integraciones (API, CSV, PIM) que alimentan atributos de producto.

## Requisitos previos {#prerequisites}

Los siguientes requisitos previos se aplican cuando tiene acceso al enriquecimiento del catálogo.

- Su tienda puede ser rastreada por bots agénticos y orientados a LLM donde se requiere rastrear la cobertura de las sugerencias según el catálogo.
- Los servicios de Commerce y la conectividad del catálogo requeridos están habilitados y en buen estado. Consulte [Habilitar enriquecimiento de catálogo](#enable-catalog-enrichment) para obtener más información.
- [IMS está configurado](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations).
- Tiene acceso a [Adobe Admin Console](https://helpx.adobe.com/business/enterprise/plan-your-deployment/basic-concepts/admin-console.html).
- Su organización ha firmado al usuario de GenAI o se ha excluido explícitamente de los servicios de IA subyacentes.

>[!NOTE]
>
>Como parte de la configuración, Commerce comprueba si su organización ha firmado el controlador GenAI que cubre los servicios de IA subyacentes al enriquecimiento del catálogo. Si todavía no ha firmado al usuario o no ha optado por excluirse, se le pedirá que firme o actualice el usuario antes de poder utilizar el enriquecimiento del catálogo.

## Habilitar enriquecimiento de catálogo {#enable-catalog-enrichment}

Póngase en contacto con el administrador de Commerce o con su socio de implementación para asegurarse de lo siguiente antes de revisar o aplicar las sugerencias:

### Instalación de extensiones de enriquecimiento de catálogo y servicios de catálogo

1. Instale la extensión de enriquecimiento de catálogo en la instancia de Commerce ejecutando el siguiente comando:

   ```bash
   composer require magento/module-catalog-enrichment --no-update
   composer update magento/module-catalog-enrichment
   ```

1. Si aún no ha instalado los servicios de catálogo, [hágalo](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/installation#install-the-catalog-service-extension).

   **[!UICONTROL Catalog enrichment]** ya está disponible en su instancia de Commerce.

### Acceso al enriquecimiento del catálogo

Después de instalar las extensiones de enriquecimiento de catálogo y servicios de catálogo, la capacidad de enriquecimiento de catálogo está disponible en el Administrador en **[!UICONTROL Catalog]** > **[!UICONTROL Catalog Enrichment]**.

![Enriquecimiento de catálogo](./assets/catalog-enrichment-menu.png)

### Configuración del enriquecimiento del catálogo

Configure el enriquecimiento de catálogo en la ficha **[!UICONTROL Settings]** para que [!DNL Commerce Catalog Agent] pueda conectarse a su entorno [!DNL Adobe Commerce] y mostrar sugerencias en el administrador de Commerce.

1. En el Administrador, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Catalog Enrichment]**.
1. En la lista **[!UICONTROL Scope]** de la parte superior de la página, seleccione la vista de tienda que desee configurar o deje **[!UICONTROL All Store Views]** para administrar la configuración en las vistas de tienda.
1. Abra la ficha **[!UICONTROL Settings]**.
1. En **[!UICONTROL Commerce Configuration]**, expanda el panel de vista de tienda etiquetado con su dirección URL.

   Proporcione los detalles de su entorno [!DNL Adobe Commerce] para habilitar el servicio Catalog LLM Optimizer y los flujos de trabajo de auditoría.

   ![Configuración de Commerce en la ficha Configuración de enriquecimiento del catálogo](./assets/catalog-enrichment-commerce-config.png)

1. Introduzca los detalles de conexión necesarios para la vista de tienda.

   - **[!UICONTROL Store View URL]**: dirección URL correspondiente a la vista de la tienda (por ejemplo, `https://brand.example.com/fr/`).
   - **[!UICONTROL Environment ID]**: Identificador único del entorno [!DNL Adobe Commerce] al que accede la conexión.
   - **[!UICONTROL Website Code]**, **[!UICONTROL Store Code]** y **[!UICONTROL Store View Code]**: Sitio web, tienda y códigos de vista de tienda para el sitio web de Commerce. Estos valores deben coincidir con los códigos del administrador de Commerce.
   - **[!UICONTROL Host Name]**: nombre de host de su instancia [!DNL Adobe Commerce].

1. Haga clic en **[!UICONTROL Save]**.

Después de guardar, espere a que se complete cualquier trabajo de sincronización o validación inicial antes de depender de los resultados del catálogo o de la auditoría para esa vista de tienda. Las sugerencias de productos pueden tardar hasta 24 horas en aparecer en la página **[!UICONTROL Catalog Enrichment]**.

Para quitar una configuración de vista de tienda, expanda esa entrada y haga clic en **[!UICONTROL Delete]**.

#### Descripciones de campos {#commerce-connection-fields}

Los campos obligatorios están marcados con un asterisco (*) en el formulario **[!UICONTROL Commerce Configuration]**.

| Campo | Requerido | Descripción |
| --- | --- | --- |
| URL de vista de tienda | Sí | URL correspondiente a la vista de tienda (por ejemplo, `https://brand.example.com/fr/`). |
| ID de entorno | Sí | Identificador único del entorno [!DNL Adobe Commerce] al que tiene acceso la conexión. |
| Código del sitio web | Sí | Código del sitio web de Commerce. |
| Código de tienda | Sí | Código de tienda del sitio web de Commerce. |
| Código de vista de tienda | Sí | Vista de tienda del sitio web de Commerce. |
| Nombre de host | Sí | Nombre de host de su instancia [!DNL Adobe Commerce]. |

### Revisión y aplicación del enriquecimiento del catálogo {#review-and-apply}

Una vez habilitado y configurado el enriquecimiento del catálogo, las sugerencias de productos se muestran en la pestaña **[!UICONTROL Agentic Opportunities]**. Desde aquí puede revisar sugerencias y aplicar actualizaciones aprobadas a nombres de productos y descripciones largas en su catálogo de Commerce.

El enriquecimiento del catálogo utiliza las siguientes vistas de flujo de trabajo:

- **[!UICONTROL Current Suggestions]**: elementos nuevos o activos para revisar.
- **[!UICONTROL Fixed Suggestions]**: elementos que ya aplicó o resolvió.
- **[!UICONTROL Ignored Suggestions]**: elementos que ha excluido intencionadamente de la acción.

![Enriquecimiento de catálogo](./assets/agentic-opportunities.png)

### Implementar sugerencias aprobadas {#review-deploy-catalog}

Para implementar sugerencias aprobadas:

1. Seleccione **[!UICONTROL Current Suggestions]**.
1. Haga clic en el control de expansión de la fila URL o SKU para mostrar las actualizaciones propuestas del nombre y la descripción del producto.
1. Revise la sugerencia y confirme que coincide con su estrategia de comercialización y optimización de los motores de búsqueda.

Puede editar una sugerencia antes de implementarla o moverla a **[!UICONTROL Ignored Suggestions]** si no coincide con su estrategia.

1. Seleccione la fila de la URL o SKU que desea actualizar.
1. Haga clic en **[!UICONTROL Deploy optimizations]** y confirme.

Los cambios de nombre y descripción aprobados se guardan en el catálogo [!DNL Adobe Commerce] como otras actualizaciones de productos.

>[!IMPORTANT]
>
>Trate cada actualización aplicada como un cambio en el catálogo de producción. Utilice sus prácticas normales de control de cambios, ensayo y control de calidad. Aplique las actualizaciones solo después de que las partes interesadas en la comercialización y la SEO acuerden la copia final.

Después de aplicar una actualización, las sugerencias pasan a **[!UICONTROL Fixed Suggestions]** con el estado **Marcado como fijo**.

## Verificar enriquecimiento en el administrador {#verify-in-admin}

**Para comprobar el enriquecimiento del catálogo aplicado:**

1. Vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]** en el Administrador de Commerce.
1. Use los filtros y el selector **[!UICONTROL Store View]** según sea necesario (por ejemplo, **[!UICONTROL Default Store View]**).
1. Busque el SKU.
1. Abra el producto en modo de edición.

   El formulario del producto muestra el nombre y/o la descripción del producto enriquecido.

   ![Nombre de producto enriquecido](./assets/enriched-product-name.png)

1. Opcional: seleccione **[!UICONTROL Override Catalog Agent provided Product Name]** si desea conservar un nombre ingresado manualmente en su lugar.

   Las anulaciones manuales afectan a la forma en que las sugerencias permanecen sincronizadas con el catálogo. Para obtener más información, consulte [Anulación manual en Admin](#manual-override-in-the-admin).

1. Expanda la sección **[!UICONTROL Content]** y busque el campo de descripción.

   La descripción enriquecida aparece cuando se aplican cambios de descripción.

   ![Enriquecer descripción del producto](./assets/enrich-product-description.png)

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

- El enriquecimiento solo se aplica a nombres de productos y descripciones largas. No cambia el diseño de la PDP, los widgets u otro contenido de tienda de nivel de página.
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
