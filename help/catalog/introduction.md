---
title: Introducción a la administración de catálogos
description: Descubra cómo funcionan el catálogo y el ámbito del producto en la administración de catálogos.
exl-id: 3c58fc1c-d7a3-4f51-8a78-6bf2fd0dbeee
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# Introducción a la administración de catálogos

Adobe Commerce y Magento Open Source usan el término _catalogar_ para hacer referencia a la base de datos de productos en su conjunto.

Una de las áreas más importantes en la creación y gestión de su tienda es la creación de productos y categorías. El administrador proporciona varias herramientas que usted utiliza para la configuración inicial de su tienda, y para mantener su tienda y optimizar su negocio.

>[!TIP]
>
>Inventory management para Adobe Commerce y Magento Open Source le ofrece las herramientas para administrar el inventario de productos. Los comerciantes con una sola tienda en varios almacenes, tiendas, ubicaciones de recogida, distribuidores directos entre otros pueden utilizar estas funciones para mantener las cantidades de ventas y gestionar los envíos para completar pedidos. Para obtener más información sobre estas funciones y cómo puede utilizarlas para administrar existencias en varias ubicaciones, consulte la [Guía del usuario de Inventory management](../inventory-management/introduction.md).

## Ámbito del catálogo

El acceso a los datos del catálogo viene determinado por varios factores, entre los que se incluyen los siguientes [ámbito](../getting-started/websites-stores-views.md#scope-settings) , la configuración del catálogo y la [categoría raíz](category-root.md) que se asigna a la tienda. El catálogo incluye productos que están activados y disponibles para la venta, y productos que actualmente no se ofrecen para la venta.

En ventas, el término _catalogar_ normalmente se refiere a una selección revisada de productos que están disponibles para la venta. Por ejemplo, una tienda puede tener un &quot;catálogo de primavera&quot; y un &quot;catálogo de otoño&quot;.

Al igual que la tabla de contenido de un catálogo impreso, el menú principal de su tienda — o _navegación superior_ — organiza los productos por categoría para facilitar a los clientes la búsqueda de lo que desean. El menú principal se basa en una _categoría raíz_, que es un contenedor para el menú asignado al almacén. Dado que las opciones de menú específicas se definen en el nivel de vista de tienda, cada vista puede tener un menú principal diferente basado en la misma categoría raíz. Dentro de cada menú, puede ofrecer una selección revisada de productos que es adecuada para la tienda.

![Diagrama de jerarquía de catálogo](./assets/catalog-hierarchy-scope.svg){width="550"}

## Ámbito del producto

Para instalaciones con varios sitios web, tiendas y vistas, la variable [ámbito](../getting-started/websites-stores-views.md#scope-settings) determina dónde están disponibles los productos para la venta y la información del producto disponible para cada vista de tienda. Inicialmente, todos los productos que cree se publicarán en el sitio web, la tienda y la vista de la tienda predeterminados.

![diagrama de tienda de varios sitios](./assets/scope-multisite.svg){width="550"}

Si solo tiene una tienda con la vista predeterminada, puede ejecutar la tienda en [modo de una sola tienda](../getting-started/websites-stores-views.md#single-store-mode) para ocultar la configuración del ámbito. Sin embargo, si la tienda tiene varias vistas, aparece un indicador de ámbito debajo del nombre de cada campo.

- Para editar la información de un producto para una vista específica, utilice el _Vista de tienda_ en la esquina superior izquierda para elegir la vista. Hay disponibles controles adicionales para cualquier campo que se pueda editar en el nivel de vista de tienda.

- Para definir el ámbito de un producto en una instalación multisitio, consulte la [Producto en sitios web](settings-basic-websites.md) de la información del producto.

El proceso de edición de un producto para una vista de tienda es como añadir una capa de información de producto específica de la vista.

Solo puede editar o asignar productos para el sitio para el que tiene permisos, no para todos los sitios donde está asignado el producto.

Aunque la variable _Español_ la vista de tienda está seleccionada en el siguiente ejemplo, la información del producto sigue apareciendo en el idioma original de la vista de tienda predeterminada. Para traducir la información del producto, debe cambiar a la _Español_ almacenar, ver y traducir los campos de texto, como el título del producto, la descripción y los metadatos. Para obtener más información, consulte [Localizar productos](../stores-purchase/store-localize.md#localize-products).

## Edición de un producto para una vista diferente

>[!NOTE]
>
>El _Todas las vistas de tienda_ El ámbito está deshabilitado para los usuarios administradores que están restringidos a un ámbito específico cuando el producto también se publica fuera del ámbito permitido. El primer ámbito disponible para edición está seleccionado de forma predeterminada porque los usuarios restringidos no pueden realizar _global_ acciones o acciones que afectan a ámbitos en los que no tienen acceso.

1. En la esquina superior izquierda, establezca **[!UICONTROL Store View]** a la vista específica que se va a editar.

1. Para confirmar el cambio de ámbito, haga clic en **[!UICONTROL OK]**.

1. Actualice el campo con el nuevo valor para la vista de tienda.

   Aparece una casilla de verificación debajo de cualquier campo que se pueda editar para la vista de tienda. Para anular el valor predeterminado, anule la selección del **Utilizar valor predeterminado** casilla de verificación

   ![Traducción del nombre del producto para la vista de tienda en español](./assets/product-translate-field-french.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

1. En la esquina superior izquierda, configure el **[!UICONTROL Store View]** volver al valor predeterminado.

1. Para comprobar el cambio en la tienda, haga lo siguiente:

   - En la esquina superior derecha, haga clic _Administrador_ flecha de menú y seleccione **[!UICONTROL Customer View]**.

     ![Vista de cliente](./assets/product-admin-menu-customer-view.png){width="600" zoomable="yes"}

   - En la esquina superior derecha de la tienda, configure el **[!UICONTROL Language Chooser]** vaya a la vista de tienda del producto que ha editado y busque el producto que ha editado para la vista.

     ![Selector de idioma](./assets/storefront-language-chooser.png){width="700" zoomable="yes"}
