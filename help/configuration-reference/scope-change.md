---
title: Ámbito de configuración
description: Obtenga información acerca de la configuración del ámbito de las configuraciones en el Administrador de Commerce.
exl-id: b7b87ac5-dc7d-472f-af24-52b4d12e46c5
source-git-commit: eb61d90c0a3bf5cac976fc8b79b23dc717aca3e6
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# Ámbito de configuración

El selector de Vista de tienda, en la esquina superior izquierda de muchas páginas de configuración, filtra la vista de la página para un ámbito específico y establece el valor de algunas entidades que utiliza Commerce. Muestra cada nivel de la jerarquía por su nombre y se utiliza para cambiar el ámbito a otro nivel. Cualquier configuración que represente el ámbito actual aparece atenuada, por lo que sólo están disponibles las que representan la configuración del ámbito actual. El ámbito se establece inicialmente en _Configuración predeterminada_. Para los usuarios administradores con acceso restringido, la lista de vistas de tienda disponibles incluye solo aquellas a las que el usuario tiene acceso restringido. [permiso](../systems/permissions.md) para acceder a.

| Nivel | Descripción |
|--- |--- |
| [!UICONTROL Default Config] | La configuración predeterminada del sistema. |
| [!UICONTROL Main Website] | Nombre del sitio web en la parte superior de la jerarquía. |
| [!UICONTROL Main Website Store] | El nombre de la tienda predeterminada asociada al sitio web principal. |
| [!UICONTROL Default Store View] | Nombre de la vista de almacén predeterminada asociada al almacén principal. |
| [!UICONTROL Stores Configuration] | Salta a la cuadrícula Tiendas y es lo mismo que elegir [!UICONTROL Stores] > [!UICONTROL All Stores] desde la barra lateral de Administración. |

{:style=&quot;table-layout:auto&quot;}

![Casillas de verificación Usar valor del sistema seleccionadas](./assets/store-view-control.png){width="700" zoomable="yes"}

## [!UICONTROL Use system value]

El _[!UICONTROL Use System Value]_La casilla de verificación a la derecha de muchas opciones de configuración se utiliza para aplicar o anular el valor de campo predeterminado dentro del ámbito de configuración actual. El valor del campo predeterminado no se puede cambiar cuando se selecciona la casilla de verificación. Para cambiar el valor, desactive la casilla de verificación e introduzca el nuevo valor. Se le pedirá que confirme cada vez que cambie el valor del sistema.

La etiqueta de la casilla de verificación cambia según el ámbito actual y siempre hace referencia al nivel principal que está un paso por encima en la jerarquía del ámbito. Dado que el nivel primario es un contenedor para todos los elementos por debajo de ese nivel, la configuración de ámbito del nivel primario se hereda a menos que se anule.

## Opciones de valor predeterminadas

| Casilla | Descripción |
|--- |--- |
| [!UICONTROL Use system value] | Esta casilla de verificación aparece cuando el ámbito de configuración se establece en `Default Config`. |
| [!UICONTROL Use Default] | Esta casilla de verificación aparece cuando el ámbito de configuración se establece en Principal `Website`y hace referencia a la tienda predeterminada asignada al sitio web. |
| [!UICONTROL Use Website] | Esta casilla de verificación aparece cuando el ámbito de configuración se establece en una vista de tienda específica. Cuando se selecciona, utiliza la configuración del sitio web principal asociado a la vista de tienda. En este caso, se omite el nivel de almacén porque se entiende que se aplica al almacén predeterminado asociado al sitio web. |

{:style=&quot;table-layout:auto&quot;}

## Establecer el ámbito

Antes de realizar una configuración que se aplique únicamente a un sitio web, tienda o vista de tienda específicos, haga lo siguiente:

1. En el _Administrador_ En la barra lateral, realice una de las siguientes acciones:

   - Para obtener la mayoría de las configuraciones, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - Para [configuración relacionada con el diseño](../content-design/configuration.md), vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**. A continuación, en la cuadrícula, elija la vista de tienda aplicable.

1. Vaya a la configuración que desea cambiar y haga lo siguiente:

   - En la esquina superior izquierda, establezca **[!UICONTROL Store View]** a la vista específica donde se aplica la configuración. Cuando se le pida que confirme el cambio de ámbito, haga clic en **[!UICONTROL OK]**.

     Después de cada campo aparece una casilla de verificación y podrían estar disponibles campos adicionales.

   - Borre la **[!UICONTROL Use system value]** después de cualquier campo que desee editar. A continuación, actualice el valor de la vista.

   - Repita este proceso para cada campo que necesite actualizarse en la página.

   ![Configuración de las opciones de país de la vista de tienda en francés](./assets/store-view-french.png){width="700" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Referencia rápida del ámbito

| Ámbito | Descripción |
|--- |--- |
| **[!UICONTROL Global]** |  |
| Administrador | Todos los sitios web, tiendas y vistas de tiendas de la instalación se administran desde el mismo administrador. |
| Configuración predeterminada | El global [configuración predeterminada](../getting-started/websites-stores-views.md#scope-settings) Los valores de configuración se utilizan a través de la jerarquía de almacén, a menos que se anulen en un nivel inferior. |
| Catálogo | El término _catalogar_ hace referencia a la base de datos de productos en su conjunto y está disponible durante toda la instalación. |
| Precios de productos | Los precios de los productos se pueden configurar para su aplicación a nivel global o de sitio web. |
| Configuraciones de productos | Atributos que se utilizan como [producto configurable](../catalog/product-create-configurable.md) las opciones deben tener un ámbito global. |
| Clientes | Las cuentas de cliente se pueden configurar para su aplicación a nivel global o de sitio web. Cada sitio web puede tener un conjunto independiente de [cuentas de cliente](../customers/customer-account-scope.md) o compartir cuentas de cliente con otros sitios web en la instalación. |
| **[!UICONTROL Website]** |  |
| Dominio | Adicional [sitios web](../stores-purchase/introduction.md#store-structure) puede configurarse como subdominios del dominio principal o tener direcciones IP y dominios dedicados independientes. |
| Clientes | Las cuentas de cliente se pueden configurar para su aplicación a nivel global o de sitio web. Cada sitio web puede tener un conjunto independiente de [cuentas de cliente](../customers/customer-account-scope.md) o compartir cuentas de cliente con otros sitios web en la instalación. |
| Moneda | A cada sitio web se le puede asignar un diferente [divisa base](../stores-purchase/currency-configuration.md). La divisa de base se utiliza para procesar todas las transacciones, aunque puede aparecer una divisa de visualización diferente para el cliente, según la configuración regional de la vista de tienda. |
| Productos | Los productos individuales se asignan a la jerarquía en el nivel de sitio web. La cuadrícula Productos enumera todos los productos del catálogo y los sitios web donde están disponibles. El [Producto en sitios web](../catalog/settings-basic-websites.md) La configuración de identifica cada sitio web donde el producto está disponible. |
| Precios de productos | [Precios de productos](../catalog/catalog-price-scope.md) se puede configurar para su aplicación a nivel global o de sitio web. |
| Métodos de pago | [Métodos de pago](../stores-purchase/payments.md) se configuran en el nivel de sitio web, aunque el título y las instrucciones se pueden configurar para cada vista de tienda. |
| Finalizar compra | El [proceso de cierre de compra](../stores-purchase/checkout-process.md) tiene lugar en el nivel del sitio web, aunque algunas opciones de visualización se pueden configurar para cada vista de tienda. Todas las tiendas asociadas a un sitio web tienen el mismo [configuración de cierre de compra](../stores-purchase/checkout-process.md#checkout-options). |
| Países permitidos | Los países permitidos se pueden configurar en el nivel de sitio web. El [países permitidos](../getting-started/store-details.md#country-options) La configuración de se utiliza en el cierre de compra para limitar la procedencia de un cliente. |
| **[!UICONTROL Store]** |  |
| Dominio | Con varios almacenes, cada uno puede tener el mismo dominio, un subdominio o dominios claramente diferentes. Para obtener más información, consulte [Agregar tiendas](../stores-purchase/stores.md#add-stores). |
| Categoría raíz | Cada tienda puede tener un conjunto separado de productos y un menú principal que se basa en una categoría &quot;raíz&quot; y subcategorías. Cada catálogo tiene un [categoría raíz](../catalog/category-root.md) que se asigna en el nivel de tienda. |
| **[!UICONTROL Store View]** |  |
| Subcategorías | El [subcategorías](../catalog/category-create.md#category-structure) que conforman el menú principal (bajo la raíz) se asignan en el nivel de vista de tienda. |
| Configuración regional | A cada vista de tienda se le puede asignar una diferente [locale](../getting-started/store-details.md#locale-options). La moneda de visualización, las unidades de medida y la interfaz de administración son específicas de la configuración regional. |
| Idiomas | Para admitir varios idiomas, todo el contenido, incluidas las descripciones de productos, debe ser [traducido](../stores-purchase/store-localize.md#localize-products) para cada vista de tienda. |
| Mostrar divisa | Un elemento diferente [mostrar moneda](../stores-purchase/currency-configuration.md) se puede utilizar para cada vista de tienda, aunque las transacciones se procesan en el nivel de sitio web utilizando la moneda base. |

{:style=&quot;table-layout:auto&quot;}
