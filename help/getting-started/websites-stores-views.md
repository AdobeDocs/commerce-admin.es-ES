---
title: Sitio, almacén y ámbito de visualización
description: Obtenga información acerca de la jerarquía de sitios web, tiendas y vistas de tiendas que puede utilizar para ofrecer experiencias de compra a sus clientes.
exl-id: 80fc1b73-c869-4f1c-b1a1-d61823b91d83
feature: System, Site Management
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Sitio, almacén y ámbito de visualización

Cada instalación de Adobe Commerce y Magento Open Source tiene una [jerarquía](../stores-purchase/stores.md) de sitios web, tiendas y vistas de tiendas. El término _ámbito_ determina en qué parte de la jerarquía se aplica una entidad de base de datos (como un producto, atributo o categoría), un elemento de contenido o una configuración. Los sitios web, las tiendas y las vistas de las tiendas tienen relaciones principales/secundarias de uno a varios. Una sola instalación puede tener varios sitios web, y cada sitio web puede tener varias tiendas y vistas de tiendas.

>[!NOTE]
>
>Para obtener más información, consulte [Varios sitios web o tiendas](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) en la documentación para desarrolladores de [!DNL Commerce].

## Sitios web

Las instalaciones comienzan con un solo [sitio web](../stores-purchase/stores.md#add-websites), que se llama _sitio web principal_ de forma predeterminada. También puede configurar varios sitios web para una sola instalación, cada uno con su propia dirección IP y dominio.

## Tiendas

Un solo sitio web puede tener varias [tiendas](../stores-purchase/stores.md#add-stores), cada una con su propio menú principal. Las tiendas comparten el catálogo de productos, pero pueden tener una selección diferente de productos y diseños. Todas las tiendas del mismo sitio web comparten el administrador y el cierre de compra.

## Vistas de tienda

Cada tienda disponible para los clientes se presenta de acuerdo con una _[vista](../stores-purchase/store-views.md)_ específica. Inicialmente, una tienda tiene una sola vista predeterminada. Se pueden agregar vistas de tienda adicionales para admitir diferentes idiomas o para otros fines. Los clientes pueden utilizar el selector de idioma del encabezado para cambiar la vista del almacén.

Cuando trabaje con sitios web, tiendas y vistas de tiendas, tenga en cuenta lo siguiente:

- Las instancias de Commerce tienen un modelo en cascada: sitio web de → global → almacenar → vista de tienda.
- Cada sitio web tiene al menos una tienda y una vista de tienda predeterminadas.
- Cada vista de tienda puede tener una dirección URL base diferente.
- La función principal de un sitio web es la configuración de funciones de nivel superior.
- La función principal de un almacén es la configuración de la categoría raíz.
- La función principal de una vista de tienda es la configuración de información de conversión y símbolo de moneda.

## Configuración del ámbito

Si la instalación de Adobe Commerce o Magento Open Source tiene una jerarquía de sitios web, tiendas o vistas, puede establecer el contexto o el _ámbito_ de una configuración. Al contexto de muchas entidades de base de datos también se le puede asignar un ámbito específico para determinar cómo se utiliza en la jerarquía de almacén. Para obtener más información, consulte [Ámbito del producto](../catalog/introduction.md#product-scope) y [Ámbito del precio](../catalog/catalog-price-scope.md).

Algunos ajustes de configuración, como el código postal, tienen un alcance global porque se utiliza el mismo valor en todo el sistema. El ámbito [sitio web](../stores-purchase/stores.md#add-websites) se aplica a cualquier tienda por debajo de ese nivel en la jerarquía, incluidas todas las tiendas y sus vistas. Cualquier elemento con el ámbito de [vista de tienda](../stores-purchase/store-views.md) se puede establecer de forma diferente para cada vista de tienda, que normalmente se usa para admitir varios idiomas. Para anular los valores predeterminados de las opciones de configuración, vea [Establecer el ámbito](../configuration-reference/scope-change.md#set-the-scope).

A menos que el almacén se esté ejecutando en [modo de almacén único](#single-store-mode), el ámbito de cada valor de configuración aparece en un pequeño texto debajo de la etiqueta de campo. Si su instalación incluye varios sitios web, tiendas o vistas, elija la [vista de tienda](../stores-purchase/store-views.md) donde se aplica la configuración antes de realizar los cambios.

![Jerarquía de sitios web, tiendas y vistas de tiendas](./assets/scope-multisite.svg){width="550"}

| Ámbito | Descripción |
|--- |--- |
| [!UICONTROL Global] | Recursos y configuración de todo el sistema disponibles durante toda la instalación. |
| [!UICONTROL Website] | Configuración y recursos limitados al sitio web actual. Cada sitio web tiene una tienda predeterminada. |
| [!UICONTROL Store] | Configuración y recursos limitados a la tienda actual. Cada tienda tiene una categoría raíz predeterminada (menú principal) y una vista de tienda predeterminada. |
| [!UICONTROL Store View] | Configuración y recursos limitados a la vista de tienda actual. |

{style="table-layout:auto"}

## Modo de tienda única

Si la instalación de Commerce tiene una sola vista de tienda y tienda, puede simplificar la visualización desactivando todas las opciones de vista de tienda y los indicadores de ámbito. El modo de tienda única se reemplaza si [agrega más vistas de la tienda](../stores-purchase/store-views.md) más adelante.

![Ámbito - vista única](./assets/scope-single-view.svg){width="550"}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En **[!UICONTROL General]**, desplácese hacia abajo hasta la parte inferior de la página y expanda la sección **[!UICONTROL Single-Store Mode]**.

1. Establezca **[!UICONTROL Enable Single-Store Mode]** en `Yes`.

   ![Configuración general: habilitar el modo de almacenamiento único](./assets/general-single-store-mode.png){width="400"}

1. Haga clic en **[!UICONTROL Save Config]**.

1. Cuando se le pida que actualice la caché, haga lo siguiente:

   - Haga clic en el vínculo **[!UICONTROL Cache Management]** en el mensaje del sistema, en la parte superior de la página.

     ![Mensaje del sistema - administración de caché](../catalog/assets/msg-cache-management.png){width="600" zoomable="yes"}

   - Seleccione la casilla de verificación **[!UICONTROL Page Cache]**.

   - Con **[!UICONTROL Actions]** establecido en `Refresh`, haga clic en **[!UICONTROL Submit]**
