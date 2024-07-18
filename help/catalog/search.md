---
title: Resumen de búsqueda en catálogo
description: Obtenga información acerca de las herramientas Búsqueda rápida y Búsqueda avanzada que los clientes pueden utilizar para localizar productos en la tienda.
exl-id: a796fa48-212a-47c7-ab6e-98edd4d040f4
feature: Catalog Management, Search
source-git-commit: 65d295694e13be2e0a0de29b8b396faa9f2c9cd4
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# Resumen de búsqueda en catálogo

>[!TIP]
>
>[[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) ofrece una experiencia de búsqueda rápida, relevante e intuitiva, y está disponible para Adobe Commerce sin cargo adicional. Esta sección describe la funcionalidad de búsqueda estándar que podría diferir de [!DNL Live Search].

Los estudios muestran que las personas que utilizan la búsqueda tienen más probabilidades de realizar una compra que los clientes que dependen únicamente de la navegación. De hecho, según algunos estudios, las personas que utilizan la búsqueda tienen casi el doble de probabilidades de realizar una compra.

Las secciones siguientes describen las funciones básicas de búsqueda en el catálogo. Para obtener información sobre cómo configurar y personalizar las funciones de búsqueda del catálogo nativo, consulte:

- [Configurar la búsqueda en el catálogo](search-configuration.md)
- [Resultados de búsqueda](search-results.md)
- [Administrar términos de búsqueda](search-terms.md)

>[!NOTE]
>
>La funcionalidad de búsqueda nativa de Commerce proporciona resultados de búsqueda de coincidencias exactas. Mientras que [!DNL Live Search], un módulo opcional disponible para la instalación y habilitación dentro de Adobe Commerce, se implementa de forma diferente y el resultado no se limita a la cadena de búsqueda exacta. Por ejemplo, donde tiene diez productos etiquetados numéricamente para _Omega_: Una búsqueda de `Omega 1` genera una sola coincidencia para _Omega 1_ con la capacidad de búsqueda nativa. Sin embargo, la misma cadena de búsqueda basada en Live Search genera una coincidencia para varios elementos, _Omega 1_ y _Omega 10_.

## Búsqueda rápida

>[!NOTE]
>
>Cuando [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview) está instalado y el widget [[!DNL Storefront Popover]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/storefront-popover) está habilitado, el cuadro de búsqueda devuelve el resultado &quot;buscar mientras escribe&quot; en una ventana emergente.

El cuadro de búsqueda en el encabezado de la tienda ayuda a los visitantes a encontrar productos en su catálogo. El texto de búsqueda puede ser el nombre completo o parcial del producto o cualquier otra palabra o frase que describa el producto. Los términos de búsqueda que usan los usuarios para encontrar los productos se pueden administrar desde el Administrador.

1. Para **[!UICONTROL Search]**, el cliente escribe las primeras letras de lo que desea encontrar.

   Todas las coincidencias del catálogo aparecen a continuación, con el número de resultados encontrados.

1. El cliente pulsa la tecla Intro o hace clic en un resultado de la lista de productos coincidentes.

   ![Buscar](./assets/storefront-search-box.png){width="700" zoomable="yes"}

## Búsqueda avanzada

>[!NOTE]
>
>La funcionalidad de búsqueda avanzada de formularios descrita aquí no se aplica a [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

La búsqueda avanzada permite a los compradores buscar en el catálogo en función de los valores introducidos en un formulario. Dado que el formulario contiene varios campos, una sola búsqueda puede incluir varios parámetros. El resultado es una lista de todos los productos del catálogo que coinciden con los criterios. Hay un vínculo a Búsqueda avanzada al pie de página de la tienda.

![Búsqueda avanzada](./assets/storefront-search-advanced.png){width="700" zoomable="yes"}

Cada campo del formulario corresponde a un atributo del catálogo de productos. Para agregar un campo, establezca las propiedades de front-end del atributo en `Include in Advanced Search`. Como práctica recomendada, incluya solo los campos que es más probable que los clientes utilicen para encontrar un producto, ya que tener demasiados ralentiza la búsqueda.

1. Al pie de página de la tienda, el cliente hace clic en **[!UICONTROL Advanced Search]**.

1. En el formulario _Búsqueda avanzada_, agrega valores completos o parciales en tantos campos como sea necesario.

1. Hace clic en **[!UICONTROL Search]** para mostrar los resultados.

   ![Resultados de búsqueda](./assets/storefront-search-advanced-results-modify.png){width="700" zoomable="yes"}

1. Si no ve lo que está buscando en los resultados de búsqueda, el cliente hace clic en **[!UICONTROL Modify your search]** e intenta otra combinación de criterios.
