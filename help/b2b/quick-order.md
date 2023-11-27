---
title: Pedidos rápidos
description: Obtenga información sobre la funcionalidad de pedidos rápidos y cómo habilitarla para sus clientes.
exl-id: 7007e1b4-a64f-46fe-a235-3ca9f64e77e4
feature: B2B, Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# Pedidos rápidos

El _Pedido rápido_ reduce el proceso de pedido a varios clics para los clientes que conocen el nombre del producto o el SKU de los productos que desean solicitar. Los pedidos con varios SKU se pueden introducir manualmente o importar en el formulario de pedidos rápidos. Los clientes que han iniciado sesión en sus cuentas y los invitados pueden utilizar el orden rápido. Cuando está activada, la variable _Pedido rápido_ Este vínculo aparece en la parte superior de la página, junto al nombre del cliente.

![Enlace de pedido rápido](./assets/quick-order-link.png){width="700" zoomable="yes"}

## Activar pedidos rápidos para tu tienda

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el _[!UICONTROL General]_en el panel izquierdo, elija **[!UICONTROL B2B Features]**.

1. Establecer **[!UICONTROL Enable Quick Order]** hasta `Yes`.

   ![Activar orden rápido](./assets/quick-orders-config.png){width="600" zoomable="yes"}

1. Haga clic **[!UICONTROL Save Config]**.

1. Cuando se le solicite, haga clic en [Administración de caché](../systems/cache-management.md) y actualice cualquier caché no válida.

## Flujos de trabajo de pedidos rápidos

Los clientes pueden especificar productos para pedidos rápidos mediante cualquiera de los siguientes métodos.

### Método 1: Introducir productos individuales

1. El cliente hace clic en **[!UICONTROL Quick Order]** vínculo.

1. Selecciona el producto por SKU o nombre del producto:

   Para colocar un **pedido rápido por SKU**, el cliente hace lo siguiente:

   - Ingresa el **[!UICONTROL SKU]**.

   - Clics **[!UICONTROL Add to List]**.

     El SKU aparece en la línea de entrada, con la información del producto a continuación.

     ![Detalles de pedido rápido](./assets/quick-order-product-detail.png){width="600" zoomable="yes"}

   Para colocar un **orden rápido por el nombre del producto**, el cliente hace lo siguiente:

   - Introduce los primeros caracteres del **[!UICONTROL Product Name]**.

     >[!NOTE]
     >
     >No use el _Entrar_ para elegir el nombre del producto.

   - Cuando aparece la lista de posibles coincidencias, el cliente hace clic en el producto que desea solicitar.

     ![Haga clic para elegir el nombre del producto](./assets/quick-order-product-name.png){width="700" zoomable="yes"}

1. Ingresa el **[!UICONTROL Qty]**.

1. Con la siguiente línea de entrada, repite este proceso tantas veces como sea necesario.

1. Clics **[!UICONTROL Add to Cart]**.

### Método 2: introducir varios productos

1. En el **[!UICONTROL Enter Multiple SKUs]** , el cliente realiza una de las siguientes acciones:

   - Introduce un SKU por línea

   - Introduce todos los SKU en la misma línea, separados por comas y sin espacios.

     ![Introducir varios SKU](./assets/quick-order-skus.png){width="600" zoomable="yes"}

1. Para añadir los productos a la lista, haga clic en **[!UICONTROL Add to List]**.

1. Ingresa el **[!UICONTROL Qty]** para ordenar para cada elemento de la lista.

   ![Lista de pedidos rápidos](./assets/quick-order-skus-detail.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si el producto tiene opciones requeridas, se solicita al cliente que elija las opciones. Pueden esperar hasta que lleguen al carro de compras para agregar opciones de producto.

   ![Elegir opciones](./assets/quick-order-skus-product-options.png){width="600" zoomable="yes"}

### Método 3: cargar una lista de productos

1. En el _[!UICONTROL Add from File]_, haga clic en **[!UICONTROL Download Sample]**para descargar una plantilla de pedido.

   ![Agregar desde archivo](./assets/quick-order-skus-add-from-file.png){width="600" zoomable="yes"}

1. Abre el archivo descargado.

1. Utiliza la plantilla para añadir los SKU del producto que se van a cargar para la lista de pedidos rápidos.

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

   ![SKU que cargar](./assets/quick-order-skus-add-from-file-sample.png){width="400" zoomable="yes"}

1. Para cargar el archivo, haga clic en **[!UICONTROL Choose]** y selecciona el archivo de su sistema.

   Los elementos se agregan a la lista de pedidos rápidos.

1. Cuando esté listo, haga clic en **[!UICONTROL Add to Cart]**.

Una vez que el cliente crea el pedido rápido, puede continuar con el cierre de compra como de costumbre.

![Pedido rápido](./assets/quick-order-add-to-cart.png){width="700" zoomable="yes"}
