---
title: Experiencia de tienda en lista de deseos
description: Obtenga información acerca de las herramientas de administración de listas de deseos disponibles para sus clientes en la tienda.
exl-id: df8cf89a-c897-4a9a-9e84-3bae946683a4
feature: Customers, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 0%

---

# Experiencia de tienda en lista de deseos

Una lista de deseos es una forma cómoda para que los clientes recuerden productos que les gustan, pero que no están listos para comprar. Los artículos de una lista de artículos deseados se pueden compartir con otros usuarios o agregar al carro de compras. Si el cliente tiene varias listas de deseos, el nombre de la lista de deseos actual aparece en la parte superior de la página. Los clientes pueden administrar sus listas de deseos desde su panel de cuentas. Los administradores de tienda también pueden ayudar a los clientes a administrar sus listas de deseos desde el Administrador.

![Ejemplo de tienda - Mi lista de deseos](./assets/storefront-my-wishlist.png){width="700" zoomable="yes"}

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce admite el uso de varias listas de deseos por cuenta de cliente.

![Magento Open Source](../assets/open-source.svg) La base de código de Magento Open Source admite el uso de una sola lista de deseos por cuenta de cliente.

## Creación de una lista de artículos deseados

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

En la tienda, un cliente puede crear una lista de deseos a partir de su panel de cuentas, una página de producto, una página de catálogo y el carro de compras.

### Método 1: Desde una cuenta de cliente

1. En la barra lateral de su panel de cuentas, el cliente elige **[!UICONTROL My Wish List]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Create New Wish List]**.

1. Introduzca el nombre de la lista de deseos.

1. Para permitir que otros vean su lista de deseos, selecciona la opción **[!UICONTROL Public Wish List]** casilla de verificación

   >[!NOTE]
   >
   >La principal diferencia entre `Public` y `Private` las listas de deseos privadas no están disponibles [investigable](wishlist-configuration.md#add-wish-list-search) a través de listas de deseos.

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

   ![Crear nueva lista de deseos](./assets/account-dashboard-wishlist-create-new.png){width="700" zoomable="yes"}

### Método 2: desde la página del catálogo

1. Desde la tienda, el cliente va a la página del catálogo que contiene el producto que desea agregar a una lista de artículos deseados.

1. Pase el ratón sobre el producto.

1. El cliente hace clic en la flecha situada junto a _Añadir a la lista de deseos_ y selecciona la variable **[!UICONTROL Create New Wish List]**.

1. Introduce el nombre de la lista de deseos.

1. Para permitir que otros vean su lista de deseos, selecciona la opción **[!UICONTROL Public Wish List]** casilla de verificación

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

### Método 3: de la página de detalles del producto

1. Desde la tienda, el cliente va a la página de detalles del producto que desea añadir a una lista de deseos.

1. Hace clic en la flecha situada junto a **[!UICONTROL Add to Wish List]** y elige **[!UICONTROL Create New Wish List]**.

1. Ingresa el **[!UICONTROL Wish List Name]**.

1. Para permitir que otros vean su lista de deseos, selecciona la opción **[!UICONTROL Public Wish List]** casilla de verificación

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

   ![Crear una nueva lista de deseos desde la página de detalles del producto](./assets/account-dashboard-wishlist-create-from-pdp.png){width="700" zoomable="yes"}

### Método 4: del carro de compras

1. El cliente abre el **[!UICONTROL Shopping Cart]** página.

1. En el elemento, haga clic en la flecha situada junto a **[!UICONTROL Move to Wishlist]** y elige **[!UICONTROL Create New Wish List]**.

1. Ingresa el **[!UICONTROL Wish List Name]**.

1. Para permitir que otros vean su lista de deseos, selecciona la opción **[!UICONTROL Public Wish List]** casilla de verificación

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

![Crear una nueva lista de deseos desde la página Carro de compras](./assets/account-dashboard-wishlist-create-from-cart.png){width="700" zoomable="yes"}

## Actualizar la lista de productos

1. Desde la lista de deseos, el cliente señala al producto para mostrar las opciones.

1. Para agregar un **[!UICONTROL Comment]** sobre el producto, introduce el texto en el cuadro debajo del precio.

   ![Opciones de edición](./assets/account-dashboard-wishlist-edit-options.png){width="700" zoomable="yes"}

1. Para cambiar la selección de opciones de producto, haga clic en **[!UICONTROL Edit]** y hace lo siguiente:

   - Actualiza las opciones de la página de detalles del producto.
   - Clics **[!UICONTROL Update Wish List]**.

## Añadir un producto de la lista de deseos al carro de compras

1. En la lista de deseos, el cliente señala al producto que desea agregar.

1. Actualiza el **[!UICONTROL Qty]** y edite las demás opciones según sea necesario.

1. Clics **[!UICONTROL Add to Cart]**.

## Compartir la lista de deseos

1. El cliente hace clic en **[!UICONTROL Share Wishlist]**.

1. Introduzca la dirección de correo electrónico de cada persona que va a recibir la lista de deseos, separada por una coma.

1. Agrega un **[!UICONTROL Message]** para incluir en el correo electrónico.

1. Clics **[!UICONTROL Share Wish List]**.

   ![Compartir la lista de deseos](./assets/account-dashboard-wishlist-sharing.png){width="700" zoomable="yes"}

   El mensaje se envía desde la página principal [contacto de tienda](../getting-started/store-details.md#store-email-addresses) e incluye una imagen en miniatura de cada producto, con vínculos a su tienda.

   ![Correo electrónico de lista de deseos compartidos](./assets/account-dashboard-wishlist-sharing-email.png){width="500" zoomable="yes"}

## Editar listas de deseos

Los clientes pueden modificar su lista de deseos de varias formas desde su panel de cuentas.

### Mover elementos a una lista diferente

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

1. El cliente selecciona la casilla de verificación de cada elemento que se va a mover.

1. Clics **[!UICONTROL Move Selected to Wish List]** y realiza una de las siguientes acciones:

   - Elige una lista de deseos existente.
   - Clics **[!UICONTROL Create New Wish List]**.

### Copiar elementos en una lista diferente

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

1. Selecciona la casilla de verificación de cada elemento que se va a mover.

1. Clics **[!UICONTROL Copy Selected to Wish List]** y realiza una de las siguientes acciones:

   - Elige una lista de deseos existente.
   - Clics **[!UICONTROL Create New Wish List]**.

## Eliminar una lista de artículos deseados

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

1. El cliente abre la lista de deseos que se va a eliminar.

1. Clics **[!UICONTROL Delete Wish List]**.

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL OK]**.

>[!IMPORTANT]
>
>Esta acción no se puede deshacer.

## Transferir artículos de la lista de artículos deseados al carro de compras

Para transferir todos los artículos de la lista de artículos deseados al carro de compras, el cliente hace clic en **[!UICONTROL Add All to Cart]**.

Para añadir un solo artículo, el cliente hace lo siguiente:

1. Pase el ratón sobre el elemento e introduzca el **[!UICONTROL Qty]** que desean agregar al carro de compras.

1. Clics **[!UICONTROL Add to Cart]**.

## Buscar una lista de deseos de clientes

Si la variable [Widget de búsqueda de lista de deseos](wishlist-configuration.md#add-wish-list-search) en incluido en las páginas de la tienda, los clientes pueden buscar por el nombre o la dirección de correo electrónico del propietario de la lista de deseos.

1. Desde el widget de búsqueda de la lista de deseos, el cliente selecciona una opción de búsqueda.

1. Introduzca el nombre o la dirección de correo electrónico del propietario de la lista de deseos y haga clic en **[!UICONTROL Search]**.

   El _Búsqueda en lista de deseos_ se abre la página y las listas de deseos coincidentes se muestran en la sección de resultados de la búsqueda.

   >[!NOTE]
   >
   >Solo las listas de deseos públicas se muestran en los resultados de búsqueda; las listas de deseos privadas de los clientes no se pueden ver públicamente.

1. Para ver la lista de elementos de la lista de artículos deseados, haga clic en **[!UICONTROL View]**.

   El nombre del propietario y la fecha de la última actualización se muestran para cada lista de deseos.

1. Para añadir un producto al carro de compras, el cliente selecciona la casilla debajo del producto y hace clic en **[!UICONTROL Add to Cart]**.

   También puede añadir artículos que le gusten de la lista de deseos de otro cliente a la suya propia.
