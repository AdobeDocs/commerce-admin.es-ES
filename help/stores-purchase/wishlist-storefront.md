---
title: Experiencia de tienda en lista de deseos
description: Obtenga información acerca de las herramientas de administración de listas de deseos disponibles para sus clientes en la tienda.
exl-id: df8cf89a-c897-4a9a-9e84-3bae946683a4
feature: Customers, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 0%

---

# Experiencia de tienda en lista de deseos

Una lista de deseos es una forma cómoda para que los clientes recuerden productos que les gustan, pero que no están listos para comprar. Los artículos de una lista de artículos deseados se pueden compartir con otros usuarios o agregar al carro de compras. Si el cliente tiene varias listas de deseos, el nombre de la lista de deseos actual aparece en la parte superior de la página. Los clientes pueden administrar sus listas de deseos desde su panel de cuentas. Los administradores de tienda también pueden ayudar a los clientes a administrar sus listas de deseos desde el Administrador.

![Ejemplo de tienda - Mi lista de deseos](./assets/storefront-my-wishlist.png){width="700" zoomable="yes"}

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce admite el uso de varias listas de deseos por cuenta de cliente.

![Magento Open Source](../assets/open-source.svg): la base de código de Magento Open Source admite el uso de una sola lista de artículos deseados por cuenta de cliente.

## Creación de una lista de artículos deseados

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

En la tienda, un cliente puede crear una lista de deseos a partir de su panel de cuentas, una página de producto, una página de catálogo y el carro de compras.

### Método 1: Desde una cuenta de cliente

1. En la barra lateral de su panel de cuentas, el cliente elige **[!UICONTROL My Wish List]**.

1. En la esquina superior derecha, hace clic en **[!UICONTROL Create New Wish List]**.

1. Introduzca el nombre de la lista de deseos.

1. Para permitir que otros usuarios vean su lista de deseos, marca la casilla de verificación **[!UICONTROL Public Wish List]**.

   >[!NOTE]
   >
   >La principal diferencia entre las listas de deseos de `Public` y `Private` es que las listas de deseos privadas no se pueden [buscar](wishlist-configuration.md#add-wish-list-search) a través de las listas de deseos.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

   ![Crear nueva lista de deseos](./assets/account-dashboard-wishlist-create-new.png){width="700" zoomable="yes"}

### Método 2: desde la página del catálogo

1. Desde la tienda, el cliente va a la página del catálogo que contiene el producto que desea agregar a una lista de artículos deseados.

1. Pase el ratón sobre el producto.

1. El cliente hace clic en la flecha situada junto al icono _Agregar a la lista de deseos_ y selecciona **[!UICONTROL Create New Wish List]**.

1. Introduce el nombre de la lista de deseos.

1. Para permitir que otros usuarios vean su lista de deseos, marca la casilla de verificación **[!UICONTROL Public Wish List]**.

1. Una vez finalizado, hace clic en **[!UICONTROL Save]**.

### Método 3: de la página de detalles del producto

1. Desde la tienda, el cliente va a la página de detalles del producto que desea añadir a una lista de deseos.

1. Hace clic en la flecha situada junto a **[!UICONTROL Add to Wish List]** y elige **[!UICONTROL Create New Wish List]**.

1. Escribe **[!UICONTROL Wish List Name]**.

1. Para permitir que otros usuarios vean su lista de deseos, marca la casilla de verificación **[!UICONTROL Public Wish List]**.

1. Una vez finalizado, hace clic en **[!UICONTROL Save]**.

   ![Crear nueva lista de deseos desde la página de detalles del producto](./assets/account-dashboard-wishlist-create-from-pdp.png){width="700" zoomable="yes"}

### Método 4: del carro de compras

1. El cliente abre la página **[!UICONTROL Shopping Cart]**.

1. En el elemento, haga clic en la flecha situada junto a **[!UICONTROL Move to Wishlist]** y elija **[!UICONTROL Create New Wish List]**.

1. Escribe **[!UICONTROL Wish List Name]**.

1. Para permitir que otros usuarios vean su lista de deseos, marca la casilla de verificación **[!UICONTROL Public Wish List]**.

1. Una vez finalizado, hace clic en **[!UICONTROL Save]**.

![Crear nueva lista de deseos desde la página del carro de compras](./assets/account-dashboard-wishlist-create-from-cart.png){width="700" zoomable="yes"}

## Actualizar la lista de productos

1. Desde la lista de deseos, el cliente señala al producto para mostrar las opciones.

1. Para agregar un(a) **[!UICONTROL Comment]** sobre el producto, escribe el texto en el cuadro debajo del precio.

   ![Editar opciones](./assets/account-dashboard-wishlist-edit-options.png){width="700" zoomable="yes"}

1. Para cambiar la selección de opciones de productos, hace clic en **[!UICONTROL Edit]** y hace lo siguiente:

   - Actualiza las opciones de la página de detalles del producto.
   - Clics **[!UICONTROL Update Wish List]**.

## Añadir un producto de la lista de deseos al carro de compras

1. En la lista de deseos, el cliente señala al producto que desea agregar.

1. Actualiza **[!UICONTROL Qty]** y edita las demás opciones según sea necesario.

1. Clics **[!UICONTROL Add to Cart]**.

## Compartir la lista de deseos

1. El cliente hace clic en **[!UICONTROL Share Wishlist]**.

1. Introduzca la dirección de correo electrónico de cada persona que va a recibir la lista de deseos, separada por una coma.

1. Agrega un(a) **[!UICONTROL Message]** para que se incluya en el correo electrónico.

1. Clics **[!UICONTROL Share Wish List]**.

   ![Compartir la lista de artículos deseados](./assets/account-dashboard-wishlist-sharing.png){width="700" zoomable="yes"}

   El mensaje se envía desde el [contacto principal con la tienda](../getting-started/store-details.md#store-email-addresses) e incluye una imagen en miniatura de cada producto, con vínculos a la tienda.

   ![Correo electrónico de lista de deseos compartidos](./assets/account-dashboard-wishlist-sharing-email.png){width="500" zoomable="yes"}

## Editar listas de deseos

Los clientes pueden modificar su lista de deseos de varias formas desde su panel de cuentas.

### Mover elementos a una lista diferente

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

1. El cliente selecciona la casilla de verificación de cada elemento que se va a mover.

1. Hace clic en **[!UICONTROL Move Selected to Wish List]** y realiza una de las siguientes acciones:

   - Elige una lista de deseos existente.
   - Clics **[!UICONTROL Create New Wish List]**.

### Copiar elementos en una lista diferente

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

1. Selecciona la casilla de verificación de cada elemento que se va a mover.

1. Hace clic en **[!UICONTROL Copy Selected to Wish List]** y realiza una de las siguientes acciones:

   - Elige una lista de deseos existente.
   - Clics **[!UICONTROL Create New Wish List]**.

## Eliminar una lista de artículos deseados

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

1. El cliente abre la lista de deseos que se va a eliminar.

1. Clics **[!UICONTROL Delete Wish List]**.

1. Cuando se le pida que confirme, hace clic en **[!UICONTROL OK]**.

>[!IMPORTANT]
>
>Esta acción no se puede deshacer.

## Transferir artículos de la lista de artículos deseados al carro de compras

Para transferir todos los elementos de la lista de artículos deseados al carro de compras, el cliente hace clic en **[!UICONTROL Add All to Cart]**.

Para añadir un solo artículo, el cliente hace lo siguiente:

1. Pase el ratón sobre el elemento e introduzca los **[!UICONTROL Qty]** que desean agregar al carro de compras.

1. Clics **[!UICONTROL Add to Cart]**.

## Buscar una lista de deseos de clientes

Si el widget de búsqueda de la lista de deseos [Wish List](wishlist-configuration.md#add-wish-list-search) está incluido en las páginas de tu tienda, los clientes podrán buscar por el nombre o la dirección de correo electrónico del propietario de la lista de deseos.

1. Desde el widget de búsqueda de la lista de deseos, el cliente selecciona una opción de búsqueda.

1. Escribe el nombre o la dirección de correo electrónico del propietario de la lista de deseos y hace clic en **[!UICONTROL Search]**.

   Se abre la página _Búsqueda de listas de deseos_ y todas las listas de deseos coincidentes se muestran en la sección de resultados de la búsqueda.

   >[!NOTE]
   >
   >Solo las listas de deseos públicas se muestran en los resultados de búsqueda; las listas de deseos privadas de los clientes no se pueden ver públicamente.

1. Para ver la lista de elementos de la lista de artículos deseados, haga clic en **[!UICONTROL View]**.

   El nombre del propietario y la fecha de la última actualización se muestran para cada lista de deseos.

1. Para agregar un producto al carro de compras, el cliente selecciona la casilla debajo del producto y hace clic en **[!UICONTROL Add to Cart]**.

   También puede añadir artículos que le gusten de la lista de deseos de otro cliente a la suya propia.
