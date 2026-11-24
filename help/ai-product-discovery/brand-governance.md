---
title: Crear reglas de marca de enriquecimiento de catálogo
description: Obtenga información sobre cómo crear y administrar reglas de gobernanza de marca para el enriquecimiento de catálogo, definir los requisitos de copia de producto y aplicar reglas a los trabajos de enriquecimiento de catálogo.
role: Admin, User, Leader
source-git-commit: 9d7a4f4e98fe2d2d51261d96a2e072c28925babd
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 1%
---
# Crear reglas de marca de enriquecimiento de catálogo

Las reglas de gobernanza de marca y de gobernanza de marca solo están disponibles para el enriquecimiento de catálogo. No se aplican al enriquecimiento de PDP. Estas reglas definen los requisitos para los nombres de productos y las descripciones generadas por [!DNL Commerce Catalog Agent]. Edite o configure una regla predeterminada para los estándares de marca predeterminados y, a continuación, cree reglas personalizadas para campañas, categorías de productos o submarcas específicas. Seleccione una regla cuando cree un trabajo de [Enriquecimiento de catálogo](catalog-enrichment.md).

## Gobernanza de marca abierta

1. En el Administrador, vaya a **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**.
1. Abra la ficha **[!UICONTROL Brand Governance]**.

La pestaña **Brand Governance** contiene la regla predeterminada y cualquier regla personalizada que haya creado. Puede buscar reglas o filtrar la tabla de reglas.

Para cada fila, se ve el **nombre de regla**, **Campos**, **Tono**, **Última modificación** y **Estado**. La regla predeterminada está marcada **[!UICONTROL Default]**.

El área **[!UICONTROL Needs your attention]** resalta las reglas que deben funcionar, como los borradores que necesitan configuración o las reglas con conflictos. Revise los detalles de la regla y use la acción disponible, como **[!UICONTROL Finish setup]** o **[!UICONTROL Fix conflict]**.

## Comprender los tipos de reglas

El enriquecimiento de catálogo admite una regla predeterminada y reglas personalizadas.

### Regla predeterminada

Cada instancia de [!DNL Adobe Commerce] tiene exactamente una regla predeterminada. [!DNL Adobe Commerce] crea esta regla con campos vacíos. Su nombre se corrigió como **[!UICONTROL Global]**. Puede editar la regla, pero no puede eliminarla.

[!DNL Adobe Commerce] aplica la regla predeterminada de forma predeterminada al crear un trabajo de enriquecimiento de catálogo sin seleccionar una regla personalizada. La regla predeterminada proporciona el control de línea de base para el enriquecimiento de catálogo.

### Reglas personalizadas

Puede crear cualquier número de reglas personalizadas para una campaña, categoría de producto o submarca. Una regla personalizada no se aplica automáticamente. Selecciónelo al crear un trabajo de enriquecimiento de catálogo.

Una regla personalizada no hereda valores de la regla predeterminada. Al crear una regla personalizada, puede copiar los valores actuales de la regla predeterminada como punto de partida único. Los cambios posteriores en la regla predeterminada no actualizan la regla personalizada.

Utilice la regla predeterminada para los estándares que deben aplicarse cuando un usuario no selecciona una regla personalizada. Cree una regla personalizada para una campaña o categoría con diferentes requisitos. Añada los requisitos globales que la regla personalizada también necesite, ya que las reglas personalizadas no heredan los valores globales.

## Creación de una regla personalizada

En esta sección, aprenderá a crear una regla de gobernanza de marca.

![Crear regla de control de marca](./assets/brand-gov-create-rule.png)

1. En la ficha **Administración de marcas**, haga clic en **[!UICONTROL Create Rule]**.
1. Elija cómo iniciar la regla:
   - **[!UICONTROL Blank]**: establezca todos los valores usted mismo.
   - **[!UICONTROL Copy Global enrichment]**: Comience con los valores actuales de Regla predeterminada como una copia única.
   - **[!UICONTROL Draft with AI]**: (**Próximamente**) Describa su voz de marca para obtener los valores de reglas sugeridos.
1. Escriba un **nombre de regla** que identifique su propósito, como una campaña, categoría o submarca.
1. En **Campos para mejorar**, configure los requisitos de nombre y descripción del producto.

   Configure los nombres y las descripciones de los productos por separado. Cada campo tiene sus propios requisitos de control y conmutador de activación.

1. Establecer **longitud del nombre del producto**.

   Establezca el intervalo de longitud de nombre mínimo y máximo para un nombre de producto enriquecido. Por ejemplo, una regla puede requerir un mínimo de 20 caracteres y un máximo de 200 caracteres.

1. Establecer la opción **Mayúsculas**:

   - **[!UICONTROL Sentence case]**: `Waterproof hiking boots`
   - **[!UICONTROL Title Case]**: `Waterproof Hiking Boots`
   - **[!UICONTROL As written]**: conserva el uso de mayúsculas en el texto de origen.

1. Describir **tono de marca**. Consulte [establecer tono de marca](#set-brand-tone) para obtener instrucciones.
1. Establecer las frases necesarias y excluidas

   Agregar una frase **[!UICONTROL Must include]**.
   Agregar una frase **[!UICONTROL Never use]**.

1. Haga clic en **[!UICONTROL Save as draft]** para finalizar más tarde o haga clic en **[!UICONTROL Publish rule]** para que la regla esté disponible para su selección al crear una regla de enriquecimiento de catálogo. Haga clic en **[!UICONTROL Cancel]** para salir sin guardar.

1. Ahora puede aplicar la regla a un trabajo de [enriquecimiento del catálogo](catalog-enrichment.md).

### Establecer el tono de marca

Escriba una guía en el campo multilínea **[!UICONTROL Brand tone]** para describir la voz y el estilo del nombre enriquecido.

Estos son algunos ejemplos del tono que podría usar para la **Descripción**:

- **B2B industrial**: `Write for the operator and the buyer. Open with what the unit does and where it fits in the kitchen, then throughput, utility requirements, footprint, and certifications. Plain, technical language. Mention cleaning and maintenance, because total cost of ownership drives the decision. No lifestyle language.`
- **Moda de lujo**: `Quiet confidence. Lead with craftsmanship and provenance (atelier, tannery, technique), then how the piece wears and ages. Short, measured sentences. Sensory detail is fine. Never compare to other brands or mention price or value.`
- **Electrónica de consumo**: `Clear and benefit-led. Turn every spec into what it does for the user. Scannable short paragraphs or bullets. Put compatibility and what's in the box up front. Don't make performance claims without a source, and don't use comparative claims like "fastest"`
- **Comida y alimentos especiales**: `Warm and appetizing, but honest. Describe taste, texture, and aroma in concrete terms, then origin and how it's made, then serving ideas. Plain, friendly language. Put allergens and dietary attributes in a consistent closing line. Don't make health claims.`
- **Mobiliario de casa**: `Inviting and practical. Open with how the piece is used, then dimensions, materials, and care. Help the shopper picture it in their space without overselling. Always mention assembly, delivery, and weight, since those drive returns.`
