---
title: Configuración del producto - [!UICONTROL Related Products, Up-Sells, and Cross-Sells]
description: Para un producto, la variable [!UICONTROL Related Products, Up-Sells, and Cross-Sells] la configuración define bloques promocionales simples en la página de productos que resaltan una selección de productos adicionales.
exl-id: 5bd65fad-4e55-40db-8702-10c366261565
feature: Catalog Management, Products, Page Content
source-git-commit: f6d52b1a3c8dd411ad3aa7c6027e964f9d49d608
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# Configuración del producto - [!UICONTROL Related Products, Up-Sells, and Cross-Sells]

Utilice el _[!UICONTROL Related Products, Up-Sells, and Cross-Sells]_para configurar bloques promocionales simples que presenten una selección de productos adicionales que puedan ser de interés para el cliente. Para obtener más información, consulte [Relaciones de producto](../merchandising-promotions/product-relationships.md).

![Productos relacionados, ampliación de ventas y ventas cruzadas](./assets/product-related-up-sell-cross-sell.png){width="600" zoomable="yes"}

Cada bloque consta de una lista de productos que pertenecen a una opción específica.

| Campo | Descripción |
|--- |--- |
| [!UICONTROL ID] | Identificador numérico único asignado a la entidad del producto. |
| [!UICONTROL Thumbnail] | Imagen en miniatura del producto. |
| [!UICONTROL Name] | El nombre del producto. |
| [!UICONTROL Status] | Indica el estado del producto. Opciones: `Enabled` / `Disabled`. Los productos deshabilitados no se muestran en los bloques del front-end. |
| [!UICONTROL Attribute Set] | El nombre del conjunto de atributos que se utiliza como plantilla para el producto. |
| [!UICONTROL SKU] | La única unidad de stock asignada al producto. |
| [!UICONTROL Price] | El precio unitario del producto. |
| [!UICONTROL Action] | Opciones: `Remove`. Elimina un producto del bloque. |

{style="table-layout:auto"}

>[!TIP]
>
>![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) **Recommendations de productos con tecnología de Adobe Sensei** simplifica el proceso de definición de relaciones de producto mediante el uso de inteligencia artificial y algoritmos de aprendizaje automático para realizar un análisis profundo de los datos de visitante agregados. Estos datos, cuando se combinan con su catálogo de Adobe Commerce, generan experiencias muy atractivas, relevantes y personalizadas para el comprador.
><br/>
>Para obtener más información sobre el uso de esta extensión desarrollada por el Adobe como alternativa a las recomendaciones de productos configuradas manualmente y a las ventas adicionales, consulte la _[Guía de Recommendations del producto](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html)_.

## Productos relacionados

Los productos relacionados están pensados para ser comprados además del artículo que el cliente está viendo. El cliente puede colocar el artículo en el carro de compras simplemente haciendo clic en la casilla de verificación. La ubicación del _Productos relacionados_ El bloque de varía según la temática definida y el diseño de la página. En el ejemplo siguiente, la variable _Productos relacionados_ aparece en la parte inferior de la etiqueta _Vista del producto_ página. Con un diseño de dos columnas, la variable _Productos relacionados_ El bloque de aparece a menudo en la barra lateral derecha.

![Productos relacionados](./assets/storefront-product-related-products.png){width="600" zoomable="yes"}

Para configurar productos relacionados:

1. Abra el producto en modo de edición.

1. Desplazarse hacia abajo y expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** sección.

1. Haga clic **[!UICONTROL Add Related Products]**.

1. Utilice el [controles de filtro](../getting-started/admin-grid-controls.md) para encontrar los productos que desea.

1. En la lista, seleccione la casilla de verificación de cualquier producto que desee presentar como producto relacionado.

   ![Productos relacionados](./assets/products-related-add.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Add Selected Products]**.

## Aumentar ventas

Los productos de ampliación de venta son artículos que el cliente podría preferir en lugar del producto que se está considerando en ese momento. Un artículo ofrecido como venta adicional podría ser de mayor calidad, más popular o tener un mejor margen de beneficio. Los productos de promoción de ventas aparecen en la página de productos bajo un encabezado como _También puede estar interesado en los siguientes productos_.

![Aumentar la venta](./assets/storefront-product-upsell.png){width="600" zoomable="yes"}

Para seleccionar productos de ampliación de venta:

1. Abra el producto en modo de edición.

1. Desplazarse hacia abajo y expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** sección.

1. Haga clic **[!UICONTROL Add Up-Sell Products]**.

1. Utilice el [controles de filtro](../getting-started/admin-grid-controls.md) para encontrar los productos que desea.

1. En la lista, marque la casilla de cualquier producto que desee presentar como producto de ampliación de venta.

   ![Ampliar la venta de productos](./assets/product-up-sell-add.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Add Selected Products]**.

>[!NOTE]
>
>El producto del paquete principal siempre se muestra como un producto de mejora de ventas para todos sus productos secundarios automáticamente.

## Venta cruzada

Los artículos de venta cruzada son similares a las compras por impulso colocadas junto a la caja registradora en la línea de pago. Los productos ofrecidos como venta cruzada aparecen en la página del carro de compras, justo antes de que el cliente inicie el proceso de cierre de compra.

>[!NOTE]
>
>Para mostrar u ocultar artículos de venta cruzada por vista de tienda, consulta la [Cierre de compra > Carro de compra](../configuration-reference/sales/checkout.md) opción llamada _[!UICONTROL Show Cross-sell Items]_en el carro de compras. Es posible que desee ocultar las ventas cruzadas durante ventas específicas o para pruebas A/B en una vista de tienda.

![Ventas cruzadas en el carro de compras](./assets/storefront-cart-cross-sells.png){width="600" zoomable="yes"}

**_Para seleccionar productos de venta cruzada:_**

1. Abra el producto en modo de edición.

1. Desplazarse hacia abajo y expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** sección.

1. Haga clic **[!UICONTROL Add Cross-Sell Products]**.

1. Utilice el [controles de filtro](../getting-started/admin-grid-controls.md) para encontrar los productos que desea.

1. En la lista, marque la casilla de cualquier producto que desee presentar como producto de venta cruzada.

   ![Productos de venta cruzada](./assets/product-cross-sell-add.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Add Selected Products]**.
