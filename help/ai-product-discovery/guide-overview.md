---
title: Detección de productos de IA
description: Descubra cómo el enriquecimiento del catálogo [!DNL Adobe Commerce] y el enriquecimiento del PDP resuelven las lagunas en los datos estructurados del producto y en la copia centrada en el comprador para la detección de productos de IA.
role: Admin, User, Leader
source-git-commit: f2cf82dad7ec3c86a3b9a0a5635556ac2e77dd05
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%
---
# Detección de productos de IA

El descubrimiento de productos es la forma en que los compradores encuentran y evalúan productos que satisfacen sus necesidades. En herramientas de inteligencia artificial aplicada a la conversación como [!DNL ChatGPT] y [!DNL Gemini], los compradores pueden describir lo que desean en el lenguaje cotidiano y utilizar respuestas generadas por IA para explorar y comparar productos. La utilidad de estas respuestas depende en parte de si los agentes de IA pueden acceder a los datos relevantes del producto e interpretarlos.

## Para quién es esta guía {#who-this-guide-is-for}

- Especialistas en marketing digital y distribuidores que deseen que los datos de los productos sean precisos y útiles para la detección de productos asistidos por IA.
- Comerciantes que necesitan una forma controlada de enriquecer los productos seleccionados o de preparar copias para una campaña.
- [!DNL Adobe Commerce] administradores responsables de los datos del catálogo, los servicios y el acceso de administrador.

## Por qué importa el descubrimiento del producto

Los compradores suelen describir una necesidad, un uso o una preferencia en lugar de buscar un nombre de producto o un atributo técnico exacto. Para hacer coincidir esas solicitudes con los productos relevantes, los agentes de IA necesitan información del producto que esté estructurada y sea significativa para los compradores.

Cuando los registros de productos son incompletos, incoherentes o se centran únicamente en especificaciones técnicas, los agentes pueden tener dificultades para comprender qué productos se ajustan a la intención de un comprador. Los compradores pueden echar de menos los productos relevantes y los comerciantes pueden necesitar pasar tiempo corrigiendo y enriqueciendo el contenido del catálogo manualmente.

Además, las consultas de compradores sin marca crean nuevas oportunidades para la detección de productos. Cuando los compradores describen sus necesidades sin especificar una marca, las superficies de IA muestran productos relevantes en todas las marcas de la competencia en función de cómo coinciden esos productos con la intención del comprador. Para los comerciantes, esto crea una oportunidad para llegar a nuevos clientes que pueden no estar familiarizados con su marca, lo que amplía la visibilidad del producto más allá de la imagen de marca existente.

Sin embargo, existen algunos desafíos en la detección de productos en superficies de IA, como lagunas en el catálogo que pueden limitar la detección de productos asistidos por IA.

[!DNL Adobe Commerce] resuelve estos problemas de lagunas de catálogo proporcionando dos flujos de trabajo de enriquecimiento complementarios: enriquecimiento de la página de detalles del producto y enriquecimiento del catálogo. Estos dos enriquecimientos mejoran la forma en que los agentes de IA acceden, comprenden y relacionan los productos con la intención del comprador. Se puede acceder a ellos desde el menú _Administrador_ > **Descubrimiento de productos de IA**.

## Los hechos del producto son difíciles de acceder e interpretar

La información del producto suele distribuirse entre atributos, variantes, opciones, categorías y otros campos de catálogo. Aunque esta información puede estar disponible para los compradores en la tienda, no siempre es accesible o fácilmente interpretada por los rastreadores de IA. Los detalles del producto presentados a través de contenido procesado dinámicamente, componentes dependientes de JavaScript, asistentes de compras interactivos, ventanas emergentes o páginas vinculadas pueden ser difíciles de recuperar para los rastreadores.

Incluso cuando esta información es accesible, puede no estar estructurada de manera que los agentes de IA puedan interpretar de manera fiable. Como resultado, es posible que los agentes de IA no comprendan completamente las funciones, las opciones disponibles y las capacidades de un producto, lo que limita su capacidad para adaptar con precisión los productos a las necesidades del comprador.

### Hacer que los hechos estructurados estén disponibles con el enriquecimiento de página de detalles del producto

Enriquecimiento de PDP crea una carga útil de datos estructurada que contiene información de producto relevante, incluidos atributos, variantes, opciones, viñetas de características, relaciones de categoría, precios y disponibilidad. Esto proporciona a los agentes de IA una comprensión más completa y estructurada de las funciones, las capacidades y las configuraciones disponibles de un producto.

Con la tecnología [Optimize at Edge](#prerequisites), los rastreadores de IA pueden acceder directamente a la información de los productos enriquecidos sin necesidad de realizar cambios en la tienda visible para las personas. Los comerciantes pueden mejorar la forma en que se presenta la información del producto a los agentes de IA sin modificar los diseños de las tiendas, introducir nuevos componentes orientados al comprador o requerir el desarrollo de tiendas personalizadas.

Ver [enriquecimiento de la página de detalles del producto](pdp-enrichment.md).

## El catálogo de productos no refleja la intención del comprador

Los compradores describen cada vez más sus necesidades, problemas y casos de uso previstos en lenguaje natural en lugar de buscar nombres de productos específicos o especificaciones técnicas. Sin embargo, los nombres y las descripciones de los productos a menudo se centran en atributos técnicos sin comunicar claramente los beneficios, casos de uso o problemas reales que aborda un producto.

Esto crea una brecha entre la forma en que los compradores expresan sus necesidades y la forma en que se describen los productos en el catálogo. Sin un contenido claro y centrado en el comprador, los agentes de IA pueden tener dificultades para interpretar el valor y la relevancia de un producto para la intención de un comprador, lo que podría pasar por alto productos adecuados en favor de alternativas cuyas descripciones se alineen más claramente con las necesidades del comprador.

### Optimizar el contenido del catálogo de productos con la intención del comprador mediante Enriquecimiento del catálogo

El enriquecimiento de catálogos transforma los atributos técnicos de los productos y la información existente del catálogo en nombres y descripciones de productos centrados en el comprador que comunican claramente los beneficios, las capacidades y los casos de uso reales de un producto. Los nombres y las descripciones de los productos se encuentran entre las fuentes más influyentes de información que utilizan las superficies de IA para comprender las capacidades de los productos y determinar su relevancia para la intención del comprador.

Al conectar las especificaciones técnicas del producto con las necesidades y los problemas que los compradores describen en lenguaje natural, el enriquecimiento de catálogo ayuda a los agentes de IA a comprender mejor el valor de un producto, reducir la ambigüedad al interpretar sus capacidades y hacer coincidir con mayor precisión los productos relevantes con la intención del comprador.

Los comerciantes pueden revisar y aprobar las mejoras sugeridas antes de aplicarlas directamente a su catálogo de productos de Adobe Commerce. Esto garantiza que las tiendas y los canales de ventas con tecnología del catálogo puedan comunicar de forma consistente la misma información de producto enriquecida y basada en el valor a los compradores a través de puntos de contacto.

Consulte [Enriquecimiento de catálogo](catalog-enrichment.md).

#### Reglas de gobernanza de marca

Las reglas de gobernanza de marca permiten definir los requisitos de copia de productos para el enriquecimiento del catálogo, incluida la longitud, las frases, el tono y el uso de mayúsculas y minúsculas. Estas reglas solo se aplican al enriquecimiento de catálogo, no al enriquecimiento de PDP.

Consulte [Crear reglas de marca de enriquecimiento de catálogo](brand-governance.md).
