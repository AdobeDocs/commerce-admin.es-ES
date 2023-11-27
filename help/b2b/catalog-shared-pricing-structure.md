---
title: Establecer estructura y precios de catálogo compartido
description: Con B2B para Adobe Commerce, obtenga información sobre la configuración de los precios y la estructura de un catálogo compartido.
exl-id: 67caf56f-1b31-44bb-98dc-ea6ea7d8a4d5
feature: B2B, Companies, Catalog Management
role: Admin
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1300'
ht-degree: 0%

---

# Establecer estructura y precios de catálogo compartido

La configuración de los precios y la estructura de un catálogo compartido es un proceso de dos pasos. El lugar actual en el proceso se resalta con un número en la barra de progreso de la parte superior de la página. Puede ver el otro paso del proceso en cualquier momento haciendo clic en la barra de progreso. Por ejemplo, si está trabajando en precios personalizados, es posible que desee volver a la página de selección de productos para referencia. Simplemente haga clic en **[!UICONTROL Products]** en la barra de progreso de la parte superior de la página y, a continuación, haga clic en **[!UICONTROL Pricing]** para volver a la página precios personalizados. Su trabajo no se pierde en este proceso.

![Productos en el catálogo](./assets/shared-catalog-products-workspace.png){width="700" zoomable="yes"}

En el árbol de categorías estándar, la categoría raíz es el contenedor superior y se denomina _Categoría predeterminada_ en los datos de ejemplo. Sin embargo, cuando los catálogos compartidos están habilitados, el árbol de categorías tiene un contenedor externo denominado _Catálogo raíz_. El catálogo raíz incluye todas las demás estructuras de categorías que existen en el sistema. Para obtener más información, consulte [Ámbito del catálogo](../catalog/introduction.md#catalog-scope).

## Paso 1: Abrir la configuración de estructura y precios del catálogo compartido

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**

1. Para el catálogo compartido en la cuadrícula, vaya a _[!UICONTROL Action]_y haga clic en **[!UICONTROL Set Pricing and Structure]**.

   ![Definición de precios y estructura para el catálogo compartido](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. La primera vez que se configure el catálogo compartido, haga clic en **[!UICONTROL Configure]** para continuar con los siguientes pasos.

## Paso 2: Elegir los productos

El primer paso del proceso es elegir los productos que desea incluir en el catálogo compartido. La página de selección de productos incluye lo siguiente [árbol de categorías](../catalog/category-create.md) a la izquierda, y una cuadrícula de producto sincronizada a la derecha. Si hace clic en una categoría del árbol, los productos de la categoría aparecen en la cuadrícula.

Solo aparecen en la lista las categorías con productos seleccionados [navegación superior](../catalog/navigation-top.md) cuando el catálogo compartido se ve desde la tienda. De forma predeterminada, solo se incluyen los tres primeros niveles de categoría en la navegación de tienda, sin incluir la categoría raíz.

1. Utilice el **Almacenar** selector para establecer la variable [ámbito](../catalog/introduction.md#product-scope) de la configuración.

   El ámbito de la configuración solo se puede establecer antes de guardar el catálogo compartido por primera vez. Si posteriormente edita la selección de productos, el selector de Tienda no estará disponible.

   ![Elegir tienda](./assets/shared-catalog-products-scope.png){width="600" zoomable="yes"}

1. En el árbol de categorías, realice una de las acciones siguientes:

   - Para incluir todos los productos, haga clic en **[!UICONTROL Select all]** o marque la casilla de verificación de la categoría principal.
   - Para incluir categorías específicas de productos, seleccione la casilla de verificación de cada categoría que desee incluir.
   - Para incluir o excluir un producto individual, seleccione o anule la selección de la casilla de verificación del producto.

   La notación debajo de cada categoría en el árbol muestra el número de productos de la categoría que están actualmente incluidos en el catálogo compartido. La notación debajo de [categoría raíz](../catalog/category-root.md) muestra el número total de productos de todas las categorías seleccionadas actualmente para el catálogo compartido.

1. Para ver los productos de la categoría en la cuadrícula, haga clic en el nombre de la categoría en el árbol. Cuando se selecciona una categoría, ocurre lo siguiente:

   - La opción de la primera columna de la cuadrícula se establece en verde _Activado_ posición de cada producto seleccionado.
   - Si un producto está asignado a varias categorías y no está seleccionado en una de ellas, permanece disponible a través de las otras categorías y también al utilizar [búsqueda en el catálogo](../catalog/search.md).
   - El sistema establece automáticamente [Permisos de categoría](../catalog/category-permissions.md) hasta `Allow` para los productos seleccionados.

1. Si es necesario, utilice los filtros y otros controles de cuadrícula para buscar los productos que desea incluir en el catálogo compartido.

   Puede seleccionar u omitir productos individuales individualmente haciendo clic en el botón de alternancia en la primera columna.

   Si selecciona una categoría que no tiene productos, pero está vinculada al contenido de CMS o a un vínculo externo, se mostrará en la navegación superior de la tienda.

   Los ajustes de categoría que realice no se registrarán permanentemente en la base de datos hasta que se guarde la configuración. Sin embargo, se guardan temporalmente a medida que trabaja en la estructura y los precios.

1. Haga clic **[!UICONTROL Next]**.

   ![Seleccionar productos para el catálogo](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## Paso 3: Establecer precios personalizados

Puede establecer precios personalizados para cada producto individualmente o usar el _[!UICONTROL Action]_para establecer los precios personalizados como una cantidad fija o un porcentaje para varios registros de productos.

- **[!UICONTROL Fixed]**: especifica el precio final del producto. Por ejemplo, si introduce un precio fijo de 10,00 $, el precio de la tienda de la compañía correspondiente será 10,00 $.

  >[!NOTE]
  >
  >El valor mínimo entre el precio base y el valor fijo introducido se utiliza como precio final del producto.

  >[!NOTE]
  >
  >**_Precio fijo_** Las opciones personalizables del producto son _no_ afectado por las reglas Precio de grupo, Precio de nivel, Precio especial o Precio de catálogo.

- **[!UICONTROL Percentage]**: Determina el precio personalizado en función del porcentaje de descuento. Por ejemplo, para ofrecer un descuento del 10 por ciento, establezca el tipo de precio personalizado en `Percentage` y escriba `10`. El precio personalizado con descuento es el 90 por ciento del precio original del producto.

Para establecer el descuento en un importe fijo o un porcentaje para los siguientes tipos de producto, utilice el _[!UICONTROL Custom Price]_en la cuadrícula:

- [Sencilla](../catalog/product-create-simple.md) (incluidas las variaciones de productos configurables)
- [Paquete](../catalog/product-create-bundle.md)
- [Descargable](../catalog/product-create-downloadable.md)
- [Virtual](../catalog/product-create-virtual.md)

La columna Precio personalizado está en blanco para [configurable](../catalog/product-create-configurable.md) y [agrupado](../catalog/product-create-grouped.md) tipos de productos y para [tarjetas regalo](../catalog/product-gift-card-create.md).

La selección de productos en la cuadrícula no se puede cambiar desde el _Precios personalizados_ página. Sin embargo, puede utilizar el indicador de progreso en la parte superior de la página para volver al paso anterior y cambiar la selección de productos.

![Seleccionar productos para el catálogo](./assets/shared-catalog-custome-prices-step-3.png){width="600" zoomable="yes"}

### Aplicar un precio personalizado

1. Para una instalación de varios sitios, configure **[!UICONTROL Website]** al sitio web donde se aplican los precios personalizados.

   ![Elegir sitio web](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. Utilice uno de los siguientes métodos para seleccionar los productos a los que desea aplicar el precio personalizado.

   - Utilice el árbol de categorías para seleccionar todos los productos de una categoría específica.
   - Configure las variables _[!UICONTROL Mass Actions]_control en el encabezado a `Select All`.
   - Seleccione la casilla de verificación de productos individuales.

   La cuadrícula muestra los productos de las categorías seleccionadas actualmente y puede utilizar los controles estándar para buscar productos y filtrar la lista.

   ![Seleccionar todo](./assets/shared-catalog-custom-pricing-mass-actions.png){width="600" zoomable="yes"}

1. Establecer **[!UICONTROL Actions]** a uno de los siguientes:

   - `Set Discount` - Aplica un porcentaje de descuento a todos los productos seleccionados. Cada precio de producto afectado se muestra como un **_descontado_** precio.
   - `Adjust Fixed Price` - Aplica un porcentaje de descuento de precio fijo a todos los productos seleccionados. Cada precio de producto afectado se muestra como una **_ajustado fijo_** precio.

   ![Control de acciones: establecer descuento](./assets/shared-catalog-set-custom-prices-discount-action.png){width="600" zoomable="yes"}

1. Cuando se le solicite, introduzca el descuento o el ajuste de precio y haga clic en **[!UICONTROL Apply]**.

   ![Establecer descuento](./assets/shared-catalog-set-custom-prices-discount.png){width="400"}<br/>

   ![Ajustar precio fijo](./assets/shared-catalog-set-custom-fixed-prices.png){width="400"}

   El descuento se aplica a todos los productos seleccionados y la variable _Precio personalizado_ refleja el tipo de descuento y el importe aplicado.

   ![Columna de precio personalizado con descuento](./assets/shared-catalog-set-custom-prices-discount-applied.png){width="600" zoomable="yes"}

### Aplicar un precio de nivel

[Precios de nivel](../catalog/product-price-tier.md) permite ofrecer un descuento por cantidad de productos en el catálogo compartido. El _Precio de nivel_ de la cuadrícula contiene un vínculo al _Precios avanzados_ opciones que se aplican específicamente al catálogo compartido. Si el producto ya incluye precios de nivel, el número de niveles existentes aparece entre paréntesis después del vínculo.

Las siguientes instrucciones muestran cómo aplicar precios de nivel a un solo producto. Para aplicar precios de nivel a varios productos, consulte [Precios de nivel de importación](../systems/data-import-price-tier.md).

1. Para el producto en la cuadrícula, vaya a _Precio de nivel_ y haga clic en **[!UICONTROL Configure]**.

   ![Configurar precio de nivel](./assets/shared-catalog-tier-price-configure.png){width="600" zoomable="yes"}

1. En el _Precios avanzados_ página, haga clic en **[!UICONTROL Add Price]** y haga lo siguiente:

   ![Precio de catálogo y de nivel](./assets/shared-catalog-tier-price-configure-add-price.png){width="600" zoomable="yes"}

   - Establecer **[!UICONTROL Website]** al sitio web donde se aplica el precio de nivel.
   - Introduzca la cantidad del producto que debe adquirirse para recibir el descuento.
   - Establecer **[!UICONTROL Price]** a uno de los siguientes tipos de descuento:
      - `Fixed`
      - `Discount`
   - Introduzca el importe del descuento.
   - Para introducir otro nivel, haga clic en **Añadir precio** y repita el proceso para definir el siguiente nivel.

   ![Precios de varios niveles](./assets/shared-catalog-tier-price-configure-multiple-tiers.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Done]**.

   En la cuadrícula, el número de niveles se muestra entre paréntesis en la _[!UICONTROL Tier Price]_columna.

   ![Varios niveles](./assets/shared-catalog-tier-price-configure-parentheses.png){width="600" zoomable="yes"}

## Guardar la estructura y los precios

Una vez completado el precio personalizado, haga clic en **[!UICONTROL Generate Catalog]** entonces **[!UICONTROL Save]**.

El catálogo compartido se guardará ahora en la base de datos. Su nombre aparece en la _[!UICONTROL Shared Catalog]_de la columna_[!UICONTROL Products]_ rejilla. El siguiente paso es [asignar el catálogo compartido a una empresa](./catalog-shared-assign-companies.md).
