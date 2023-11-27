---
title: Revisiones de productos
description: Descubra cómo las revisiones de productos pueden mejorar su tienda y dar más credibilidad a sus productos.
exl-id: 82f96b24-626f-4b2d-be42-3d655d08dfda
feature: Merchandising, Products
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%

---

# Revisiones de productos

Las revisiones de productos ayudan a crear un sentido de comunidad y se consideran más creíbles de lo que cualquier dinero publicitario puede comprar. De hecho, algunos motores de búsqueda dan a los sitios con reseñas de productos una clasificación más alta que los que no lo tienen. Para aquellos que encuentran su sitio buscando un producto específico, una revisión de producto es esencialmente la página de aterrizaje de su tienda. Las revisiones de productos ayudan a las personas a encontrar su tienda, mantenerlas comprometidas y, a menudo, generar ventas.

Commerce incluye una función nativa de revisiones de productos que puede administrar desde el administrador. También puede utilizar una extensión desde el [Commerce Marketplace](../getting-started/commerce-marketplace.md) para utilizar un sistema de administración de revisiones alojado.

>[!NOTE]
>
>Las versiones 2.4.0 a 2.4.3 de Adobe Commerce y Magento Open Source incluían la extensión desarrollada por el proveedor de Yotpo. A partir de la versión 2.4.4, esta extensión ya no se integra con la versión principal y debe instalarse y actualizarse desde el Commerce Marketplace. Marketplace también proporciona acceso a la documentación actual proporcionada por el desarrollador de extensiones.
><br><br>
>Si tiene la extensión agrupada habilitada y configurada, debe actualizar el archivo composer.json como parte del proceso de actualización de la versión 2.4.4 y administrar las actualizaciones de extensión que se realicen. Consulte [Actualización de módulos](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) en el _Guía de actualización_ para obtener más información.

## Reseñas de productos en la tienda

Cuando la función nativa Revisiones de productos está activada, los clientes pueden escribir revisiones para cualquier producto del catálogo. Las críticas se pueden escribir desde la página de producto haciendo clic en:

- **Agregar su opinión** para productos con revisiones existentes.

- **Sea el primero en opinar sobre este producto** para productos sin revisiones existentes.

El [!UICONTROL Reviews] La pestaña enumera todas las revisiones actuales y el formulario utilizado para enviar una revisión.

La configuración determina si los clientes deben abrir una cuenta en la tienda antes de escribir críticas de productos o si pueden enviar críticas como invitados. Exigir a los revisores que abran una cuenta evita los envíos anónimos y mejora la calidad de las revisiones.

![Ejemplo de tienda - Añadir tu opinión](./assets/storefront-review-this-product.png){width="700" zoomable="yes"}

El número de estrellas indica el grado de satisfacción del producto. Los visitantes pueden hacer clic en el vínculo para leer las críticas y escribir sus propios comentarios. Como incentivo, los clientes pueden recibir puntos de recompensa por enviar una revisión. Cuando se envía una revisión, se envía al administrador para que la modere. Cuando se aprueba, la revisión se publica en el almacén.

![Ejemplo de tienda: pestaña Revisiones](./assets/storefront-reviews-tab.png){width="700" zoomable="yes"}

### [!UICONTROL My Product Reviews]

El _[!UICONTROL My Product Reviews]_de la sección del panel de control de cuenta del cliente enumera todas las revisiones enviadas por el cliente y aprobadas para su publicación. Cada resumen de revisión incluye la fecha en la que se envió la revisión, los vínculos a la página del producto y los detalles de la revisión.

![Mis críticas de productos](./assets/account-dashboard-my-product-reviews.png){width="700" zoomable="yes"}

1. En la barra lateral de su cuenta, el cliente elige **[!UICONTROL My Product Reviews]**.

1. Para ver la revisión completa, haga clic en **[!UICONTROL See Details]**.

   ![Revisar detalles](./assets/account-dashboard-my-product-reviews-details.png){width="700" zoomable="yes"}

## Habilitar funciones de revisión del producto

La función de revisiones de producto de Commerce está activada de forma predeterminada.

>[!NOTE]
>
>Para establecer estos campos en `No` y deshabilitar las revisiones de productos de Commerce, debe borrar la **Usar valor del sistema** casillas de verificación.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y seleccione **[!UICONTROL Catalog]** debajo.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Product Reviews]** sección.

   ![Configuración del catálogo: críticas de productos de Commerce](../configuration-reference/catalog/assets/catalog-product-reviews.png){width="600" zoomable="yes"}

1. Establecer **[!UICONTROL Enabled]** hasta `Yes`.

   Esta es la configuración predeterminada que habilita las críticas de producto.

1. Establecer **[!UICONTROL Allow Guests to Write Reviews]** hasta `Yes`.

   Esta es la configuración predeterminada que determina si los clientes deben abrir una cuenta en su tienda para poder escribir críticas de productos.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Crear clasificaciones personalizadas

Con las revisiones de producto de Commerce, los clientes pueden asignar clasificaciones cuando envíen una revisión de producto. Las clasificaciones predeterminadas son calidad, precio y valor. Además de esto, puede agregar sus propias clasificaciones personalizadas. Las clasificaciones de cinco estrellas que aparecen en las páginas del catálogo se calculan según la media de cada producto.

![Ejemplo de tienda: clasificaciones personalizadas](./assets/attribute-custom-ratings-review.png){width="700" zoomable="yes"}

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Rating]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add New Rating]**.

   ![Administrador - Clasificaciones](./assets/product-reviews-rating.png){width="700" zoomable="yes"}

1. En el _[!UICONTROL Rating Title]_, introduzca la **[!UICONTROL Default Value]**para la nueva clasificación.

   Si procede, introduzca también la traducción para cada vista de tienda.

   ![Configuración del título de clasificación](./assets/product-rating-title.png){width="600" zoomable="yes"}

1. En el _Visibilidad de clasificación_ sección, conjunto **[!UICONTROL Visibility In]** a la vista de tienda donde se va a utilizar la clasificación.

   Para seleccionar varias vistas de tienda, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada elemento.

   >[!NOTE]
   >
   >Las clasificaciones no son visibles a menos que se asignen a una vista de tienda.

1. Para **[!UICONTROL Sort Order]**, introduzca un número para determinar el orden de esta clasificación cuando aparezca con otras.

1. Si quieres mostrar tu valoración en la tienda, selecciona la **[!UICONTROL Is Active]** casilla de verificación

   ![Configuración de visibilidad de clasificación](./assets/product-rating-visibility.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save Rating]**.

   La clasificación promedio de todas las revisiones se muestra para cada producto en la página de cuadrícula de productos del catálogo.

   ![Página del catálogo](./assets/catalog-rating-page.png){width="700" zoomable="yes"}
