---
title: Ámbito de configuración
description: Obtenga información acerca de la configuración del ámbito de las configuraciones en el Administrador de Commerce.
exl-id: b7b87ac5-dc7d-472f-af24-52b4d12e46c5
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 0%

---

# Ámbito de configuración

El selector de Vista de tienda, situado en la esquina superior izquierda de muchas páginas de configuración, filtra la vista de la página para un ámbito específico y define el valor de algunas entidades que utiliza Commerce. Muestra cada nivel de la jerarquía por su nombre y se utiliza para cambiar el ámbito a otro nivel. Cualquier configuración que represente el ámbito actual aparece atenuada, por lo que sólo están disponibles las que representan la configuración del ámbito actual. El ámbito se estableció inicialmente en _Configuración predeterminada_. Para los usuarios administradores con acceso restringido, la lista de vistas de tiendas disponibles incluye solo aquellas a las que el usuario tiene [permiso](../systems/permissions.md) para acceder.

| Nivel | Descripción |
|--- |--- |
| [!UICONTROL Default Config] | La configuración predeterminada del sistema. |
| [!UICONTROL Main Website] | Nombre del sitio web en la parte superior de la jerarquía. |
| [!UICONTROL Main Website Store] | El nombre de la tienda predeterminada asociada al sitio web principal. |
| [!UICONTROL Default Store View] | Nombre de la vista de almacén predeterminada asociada al almacén principal. |
| [!UICONTROL Stores Configuration] | Salta a la cuadrícula de tiendas y equivale a elegir [!UICONTROL Stores] > [!UICONTROL All Stores] en la barra lateral de administración. |

{style="table-layout:auto"}

![Casillas de verificación Usar valor del sistema seleccionadas](./assets/store-view-control.png){width="700" zoomable="yes"}

## [!UICONTROL Use system value]

La casilla de verificación _[!UICONTROL Use System Value]_&#x200B;a la derecha de muchas opciones de configuración se usa para aplicar o anular el valor de campo predeterminado dentro del ámbito de configuración actual. El valor del campo predeterminado no se puede cambiar cuando se selecciona la casilla de verificación. Para cambiar el valor, desactive la casilla de verificación e introduzca el nuevo valor. Se le pedirá que confirme cada vez que cambie el valor del sistema.

La etiqueta de la casilla de verificación cambia según el ámbito actual y siempre hace referencia al nivel principal que está un paso por encima en la jerarquía del ámbito. Dado que el nivel primario es un contenedor para todos los elementos por debajo de ese nivel, la configuración de ámbito del nivel primario se hereda a menos que se anule.

## Opciones de valor predeterminadas

| Casilla | Descripción |
|--- |--- |
| [!UICONTROL Use system value] | Esta casilla de verificación aparece cuando el ámbito de configuración se establece en `Default Config`. |
| [!UICONTROL Use Default] | Esta casilla de verificación aparece cuando el ámbito de configuración está establecido en Principal `Website` y hace referencia al almacén predeterminado asignado al sitio web. |
| [!UICONTROL Use Website] | Esta casilla de verificación aparece cuando el ámbito de configuración se establece en una vista de tienda específica. Cuando se selecciona, utiliza la configuración del sitio web principal asociado a la vista de tienda. En este caso, se omite el nivel de almacén porque se entiende que se aplica al almacén predeterminado asociado al sitio web. |

{style="table-layout:auto"}

## Establecer el ámbito

Antes de realizar una configuración que se aplique únicamente a un sitio web, tienda o vista de tienda específicos, haga lo siguiente:

1. En la barra lateral _Admin_, realice una de las siguientes acciones:

   - Para obtener la mayoría de las opciones de configuración, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - Para la [configuración relacionada con el diseño](../content-design/configuration.md), vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**. A continuación, en la cuadrícula, elija la vista de tienda aplicable.

1. Vaya a la configuración que desea cambiar y haga lo siguiente:

   - En la esquina superior izquierda, establezca **[!UICONTROL Store View]** en la vista específica donde se aplica la configuración. Cuando se le pida que confirme el cambio de ámbito, haga clic en **[!UICONTROL OK]**.

     Después de cada campo aparece una casilla de verificación y podrían estar disponibles campos adicionales.

   - Desactive la casilla de verificación **[!UICONTROL Use system value]** después de cualquier campo que desee editar. A continuación, actualice el valor de la vista.

   - Repita este proceso para cada campo que necesite actualizarse en la página.

   ![Estableciendo las opciones de país de la vista de la tienda en francés](./assets/store-view-french.png){width="700" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Referencia rápida del ámbito

| Ámbito | Descripción |
|--- |--- |
| **[!UICONTROL Global]** |  |
| Administrador | Todos los sitios web, tiendas y vistas de tiendas de la instalación se administran desde el mismo administrador. |
| Configuración predeterminada | La configuración global [predeterminada](../getting-started/websites-stores-views.md#scope-settings) se usa a través de la jerarquía de almacén, a menos que se anule en un nivel inferior. |
| Catálogo | El término _catálogo_ hace referencia a la base de datos de productos en su conjunto y está disponible durante toda la instalación. |
| Precios de productos | Los precios de los productos se pueden configurar para su aplicación a nivel global o de sitio web. |
| Configuraciones de productos | Los atributos que se usan como opciones de [producto configurable](../catalog/product-create-configurable.md) deben tener un ámbito global. |
| Clientes | Las cuentas de cliente se pueden configurar para su aplicación a nivel global o de sitio web. Cada sitio web puede tener un conjunto separado de [cuentas de cliente](../customers/customer-account-scope.md) o compartir cuentas de cliente con otros sitios web durante la instalación. |
| **[!UICONTROL Website]** |  |
| Dominio | [sitios web](../stores-purchase/introduction.md#store-structure) adicionales se pueden configurar como subdominios del dominio principal o tener direcciones IP y dominios dedicados independientes. |
| Clientes | Las cuentas de cliente se pueden configurar para su aplicación a nivel global o de sitio web. Cada sitio web puede tener un conjunto separado de [cuentas de cliente](../customers/customer-account-scope.md) o compartir cuentas de cliente con otros sitios web durante la instalación. |
| Moneda | A cada sitio web se le puede asignar una [moneda base](../stores-purchase/currency-configuration.md) diferente. La divisa de base se utiliza para procesar todas las transacciones, aunque puede aparecer una divisa de visualización diferente para el cliente, según la configuración regional de la vista de tienda. |
| Productos | Los productos individuales se asignan a la jerarquía en el nivel de sitio web. La cuadrícula Productos enumera todos los productos del catálogo y los sitios web donde están disponibles. La configuración [Producto en sitios web](../catalog/settings-basic-websites.md) identifica cada sitio web donde el producto está disponible. |
| Precios de productos | [Los precios del producto](../catalog/catalog-price-scope.md) se pueden configurar para su aplicación a nivel global o de sitio web. |
| Métodos de pago | [Los métodos de pago](../stores-purchase/payments.md) se configuran en el nivel de sitio web, aunque el título y las instrucciones se pueden configurar para cada vista de tienda. |
| Finalizar compra | El [proceso de cierre de compra](../stores-purchase/checkout-process.md) tiene lugar en el nivel de sitio web, aunque se pueden configurar algunas opciones de visualización para cada vista de tienda. Todas las tiendas asociadas a un sitio web tienen la misma [configuración de cierre de compra](../stores-purchase/checkout-process.md#checkout-options). |
| Países permitidos | Los países permitidos se pueden configurar en el nivel de sitio web. La configuración de [países permitidos](../getting-started/store-details.md#country-options) se usa en el cierre de compra para limitar la procedencia de los clientes. |
| **[!UICONTROL Store]** |  |
| Dominio | Con varios almacenes, cada uno puede tener el mismo dominio, un subdominio o dominios claramente diferentes. Para obtener más información, consulte [Agregar tiendas](../stores-purchase/stores.md#add-stores). |
| Categoría raíz | Cada tienda puede tener un conjunto separado de productos y un menú principal que se basa en una categoría &quot;raíz&quot; y subcategorías. Cada catálogo tiene una [categoría raíz](../catalog/category-root.md) asignada en el nivel de almacén. |
| **[!UICONTROL Store View]** |  |
| Subcategorías | Las [subcategorías](../catalog/category-create.md#category-structure) que conforman el menú principal (debajo de la raíz) se asignan en el nivel de vista de tienda. |
| Configuración regional | A cada vista de tienda se le puede asignar una [configuración regional](../getting-started/store-details.md#locale-options) diferente. La moneda de visualización, las unidades de medida y la interfaz de administración son específicas de la configuración regional. |
| Idiomas | Para admitir varios idiomas, todo el contenido, incluidas las descripciones de productos, debe [traducirse](../stores-purchase/store-localize.md#localize-products) para cada vista de tienda. |
| Mostrar divisa | Se puede usar una [moneda de visualización](../stores-purchase/currency-configuration.md) diferente para cada vista de tienda, aunque las transacciones se procesan en el nivel de sitio web usando la moneda base. |

{style="table-layout:auto"}
