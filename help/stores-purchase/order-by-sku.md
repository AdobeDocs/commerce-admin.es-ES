---
title: Ordenar por SKU
description: Aprenda a configurar su tienda para que admita el pedido por SKU como comodidad para sus clientes.
exl-id: cb39554f-ab76-46d5-8217-e43bc8f9f88d
feature: Orders, Storefront, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# Ordenar por SKU

{{ee-feature}}

Un SKU es una &quot;unidad de stock&quot;. Por lo general, las SKU ayudan a los vendedores en línea a identificar las características más importantes del producto, como el tamaño, el color, el precio y el material. Los ID de producto son diferentes de los SKU:

- `Product ID` es una serie secuencial de números que se utilizan internamente para identificar productos y que no están disponibles para los clientes.
- El vendedor genera `SKU`, normalmente en función del nombre del producto y los atributos para marketing o seguimiento interno. Por ejemplo: una camiseta azul de algodón, talla media: T-COT-MED-BL. El vendedor puede cambiar la SKU si es necesario.

Normalmente, un SKU incluye un conjunto de abreviaturas que indican las características distintivas del producto. La longitud máxima de SKU es de 64 caracteres. Las SKU son importantes para realizar un seguimiento y administrar el inventario de forma eficaz, por lo que su configuración correcta es fundamental para el comercio electrónico.

_Pedir por SKU_ es un [widget](../content-design/widgets.md) que se puede mostrar en la tienda para mayor comodidad de todos los compradores, o que solo está disponible para los compradores de grupos específicos de clientes. Los compradores pueden introducir la información de SKU y cantidad directamente en el bloque Ordenar por SKU o cargar un archivo CSV desde su cuenta de cliente. Independientemente de la configuración, ordenar por SKU siempre está disponible para los administradores de tienda.

![Ordenar por SKU en la tienda](./assets/storefront-order-by-sku.png){width="700" zoomable="yes"}

## Configurar pedido por SKU

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda la sección **[!UICONTROL Sales]** y elija **[!UICONTROL Sales]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Order by SKU Settings]**.

1. Establezca **[!UICONTROL Enable Order by SKU on my Account in Storefront]** en una de las siguientes opciones:

   - `Yes, for Everyone`: el bloque Ordenar por SKU está disponible en la tienda para cada comprador.
   - `Yes, for Specified Customer Groups` - Ordenar por SKU solo está disponible para los miembros de un grupo de clientes específico, como `Wholesale`.
   - `No`: el bloque Ordenar por SKU no aparece en la tienda y la página Ordenar por SKU no está disponible en la cuenta de cliente.

   ![Ordenar por configuración de SKU](../configuration-reference/sales/assets/sales-order-by-sku-settings.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save Config]**.

![Adobe Commerce B2B](../assets/b2b.svg) (solo Adobe Commerce B2B) _&#x200B;**Para habilitar la función Ordenar por SKU, deshabilite la función Pedido rápido:**&#x200B;_

1. Vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo bajo _[!UICONTROL General]_, elija **[!UICONTROL B2B Features]**

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL B2B Features]**.

1. Establezca **[!UICONTROL Enable Quick Order]** en `No`.

   La función de orden rápido [Quick Order](../b2b/quick-order.md) permite a clientes e invitados hacer pedidos rápidamente según el SKU o el nombre del producto.

## Experiencia en tienda

Cuando la funcionalidad está configurada para la tienda, los clientes pueden pedir por SKU desde cualquier página que incluya el widget _Ordenar por SKU_ o desde su panel de cuentas.

### Ordenar por SKU desde el bloque de página

1. En el bloque _Ordenar por SKU_, el cliente introduce **[!UICONTROL SKU]** y **[!UICONTROL Qty]** del artículo que se va a pedir.

1. Para agregar otro elemento, haga clic en **[!UICONTROL Add Row]** y repita el proceso.

1. Clics **[!UICONTROL Add to Cart]**.

### Pedido por SKU desde una cuenta de cliente

1. Desde la tienda, el cliente inicia sesión en su cuenta de.

1. En el panel de la izquierda, elija **[!UICONTROL Order by SKU]**.

1. Agrega elementos individuales según la preferencia:

   _&#x200B;**Agrega cada elemento por SKU:**&#x200B;_

   - Introduce **[!UICONTROL SKU]** y **[!UICONTROL Qty]** del elemento que se va a ordenar.

   - Para agregar elementos adicionales según sea necesario, hace clic en _Agregar fila_ ![Botón de signo más](../assets/button-add-item.png) y se repite para tantos elementos como sea necesario.

   - Clics **[!UICONTROL Add to Cart]**.

   _&#x200B;**Carga un archivo CSV de varios elementos:**&#x200B;_

   - Prepara un archivo de [importación de datos CSV](../systems/data-csv.md) (valores separados por comas) que incluye columnas para `SKU` y `Qty`.

   ![SKU que importar](./assets/account-dashboard-order-by-sku-import.png){width="500" zoomable="yes"}

   - Para cargar el archivo CSV, haga clic en **[!UICONTROL Choose File]** y seleccione el archivo que desea cargar.

   - Clics **[!UICONTROL Add to Cart]**.

   Si alguno de los productos tiene opciones adicionales, se pregunta al cliente desde el carro de compras que el producto requiere atención.

   ![El Producto Requiere Atención](./assets/account-dashboard-order-by-sku-cart-product-requires-attention.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si hay SKU duplicadas, las cantidades se combinan en un artículo de línea en el carro de compras. El cliente puede cambiar la cantidad de cualquier artículo y hacer clic en **[!UICONTROL Update Shopping Cart]** para volver a calcular los totales.

