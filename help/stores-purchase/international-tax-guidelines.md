---
title: Directrices fiscales por país
description: Revise la configuración de impuestos recomendada según el país.
exl-id: 027da0a2-0ff4-40a7-9b9c-eefad888bb7a
feature: Taxes
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '1311'
ht-degree: 0%

---

# Directrices fiscales por país

## Configuración de impuestos de EE. UU.

Esta configuración recomendada se puede utilizar para la mayoría de las configuraciones de impuestos de tiendas dentro de Estados Unidos.

| Opción de impuestos | Recomendación |
|--- |--- |
| Cargar precios del catálogo | Impuestos excluidos |
| FPT | No, porque FPT no está gravado. |
| Impuesto basado en | Origen del envío |
| Cálculo de impuestos | En total |
| ¿Envío de impuestos? | No |
| Aplicar descuento | Antes de impuestos |
| Comentario | Todas las zonas fiscales tienen la misma prioridad; lo ideal sería una zona para el estado y una o más zonas para la búsqueda de código postal. |

{style="table-layout:auto"}

### Clases de impuestos

| Clase de impuesto | Configuración recomendada |
|--- |--- |
| Clase de impuesto para envío | Ninguno |

{style="table-layout:auto"}

### Configuración del cálculo

| Opción | Configuración recomendada |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Origin` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### Cálculo de destino de impuestos predeterminado

| Opción | Configuración recomendada |
|--- |--- |
| [!UICONTROL Default Country] | `United States` |
| [!UICONTROL Default State] | Estado donde se encuentra la empresa. |
| [!UICONTROL Default Post Code] | El código postal que se utiliza en sus zonas fiscales. |

{style="table-layout:auto"}

### Configuración de visualización de precios

| Opción | Configuración recomendada |
|--- |--- |
| [!UICONTROL Display Product Prices in Catalog] | `Excluding Tax` |
| [!UICONTROL Display Shipping Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### Configuración de visualización del carro de compras

| Opción | Configuración recomendada |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Display Gift Wrapping Prices] | `Excluding Tax` |
| [!UICONTROL Display Printed Card Prices] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### Pedidos, facturas, notas de abono y configuración de visualización

| Opción | Configuración recomendada |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### Impuestos fijos sobre productos (FPT)

| Opción | Configuración recomendada |
|--- |--- |
| [!UICONTROL Enable FPT] | `No`, excepto en California. |

{style="table-layout:auto"}

## Configuración fiscal del Reino Unido

Esta configuración recomendada se puede utilizar para la mayoría de las configuraciones de impuestos de tiendas dentro del Reino Unido.

### Configuración de impuestos B2C del Reino Unido

| Opción de impuestos | Recomendación |
|--- |--- |
| Cargar precios del catálogo | Impuestos excluidos |
| FPT | Sí, incluyendo FTP y descripción |
| Impuesto basado en | [!UICONTROL Shipping Address] |
| Cálculo de impuestos | En total |
| ¿Envío de impuestos? | Sí |
| Aplicar descuento | Antes de impuestos, descuento en precios, impuestos incluidos. |
| Comentario | Para los comerciantes que valoran facturas de proveedor (IVA incluido). |

{style="table-layout:auto"}

### Configuración de impuestos B2B del Reino Unido

| Opción de impuestos | Recomendación |
|--- |--- |
| Cargar precios del catálogo | Impuestos excluidos |
| FPT | Sí, incluyendo FTP y descripción |
| Impuesto basado en | [!UICONTROL Shipping Address] |
| Cálculo de impuestos | En elemento |
| ¿Envío de impuestos? | Sí |
| Aplicar descuento | Antes de impuestos, descuento en precios, impuestos incluidos. |
| Comentario | Para que los comerciantes B2B aporten consideraciones más sencillas sobre la cadena de suministro de IVA. El cálculo de impuestos en la fila también es válido; sin embargo, consulte con su jurisdicción fiscal. La configuración supone que un comerciante está en la cadena de suministro y que otros proveedores utilizan los bienes vendidos para descuentos de IVA, etc. Esta definición facilita la distinción de impuestos por artículo para una generación de devoluciones más rápida. <br/><br/>**_Nota:_**&#x200B;Algunas jurisdicciones requieren estrategias de redondeo diferentes que Commerce no admite actualmente y que no todas permiten impuestos de nivel de fila o artículo. |

{style="table-layout:auto"}

## Configuración de impuestos de Canadá

>[!IMPORTANT]
>
>Los comerciantes que se encuentran en una provincia de GST/PST (Montreal) deben crear una regla fiscal y mostrar un importe de impuestos combinado. Si tiene alguna pregunta, consulte a una autoridad tributaria calificada.

| Opción de impuestos | Recomendación |
|--- |--- |
| Cargar precios del catálogo | Impuestos excluidos |
| FPT | Sí, incluido el FTP, la descripción y aplicar impuestos al FTP. |
| Impuesto basado en | Origen del envío |
| Cálculo de impuestos | En total |
| ¿Envío de impuestos? | Sí |
| Aplicar descuento | Antes de impuestos |

{style="table-layout:auto"}

El siguiente ejemplo muestra cómo configurar las tasas de impuestos GST para Canadá y las tasas de impuestos PST para Saskatchewan, con reglas fiscales que calculan y muestran las dos tasas de impuestos. Esta información describe un ejemplo de configuración. Asegúrese de comprobar las reglas y los tipos impositivos correctos para sus jurisdicciones fiscales. Al configurar impuestos, establezca el ámbito de la tienda para aplicar la configuración a todas las tiendas y sitios web aplicables.

- El impuesto sobre el producto fijo se incluye para los productos relevantes como atributo del producto.
- En Quebec, PST se conoce como TVQ. Si desea configurar una tarifa para Quebec, asegúrese de utilizar TVQ como identificador.

### Paso 1: Completar la configuración de cálculo de impuestos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Para una configuración de varios sitios, establezca **[!UICONTROL Store View]** en el sitio web y el almacén que es el destino de la configuración.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Tax]**.

1. Haga clic en para expandir cada sección de la página y completar la siguiente configuración:

#### Configuración de cálculo de impuestos

| Campo | Configuración recomendada |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Address` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |
| [!UICONTROL Apply Tax On] | `Custom Price` (si está disponible) |

{style="table-layout:auto"}

#### Clases de impuestos

| Campo | Configuración recomendada |
|--- |--- |
| [!UICONTROL Tax Class for Shipping] | `Shipping` (el envío está gravado) |

{style="table-layout:auto"}

#### Cálculo de Destino de Impuestos por Defecto

| Campo | Configuración recomendada |
|--- |--- |
| [!UICONTROL Default Country] | `Canada` |
| [!UICONTROL Default State] | (según corresponda) |
| [!UICONTROL Default Postal Code] | `*` (asterisco) |

{style="table-layout:auto"}

#### Configuración de visualización del carro de compras

| Campo | Configuración recomendada |
|--- |--- |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero in Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

#### Impuestos fijos de productos

| Campo | Configuración recomendada |
|--- |--- |
| [!UICONTROL Enable FPT] | `Yes` |
| Todos los ajustes de visualización FPT | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `No` |

{style="table-layout:auto"}

### Paso 2: Configurar el impuesto sobre bienes y servicios de Canadá (GST)

Para imprimir el número GST en facturas y otros documentos de venta, inclúyalo en el nombre de los tipos impositivos aplicables. El GST aparece como parte del importe del GST en cualquier resumen de pedidos.

#### Administrar zonas fiscales y tasas

| Campo | Configuración recomendada |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-GST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `*` (asterisco) |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` (asterisco) |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### Paso 3: Configurar el impuesto provincial sobre ventas de Canadá (PST)

Configure otro tipo impositivo para la provincia correspondiente.

#### Información de tipo impositivo

| Campo | Configuración recomendada |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-SK-PST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `Saskatchewan` |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` (asterisco) |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### Paso 4: Crear una regla de impuestos GST

Para no agravar el impuesto y mostrar correctamente el impuesto calculado como elementos de línea independientes para GST y PST, establezca prioridades diferentes para cada regla y marque la casilla de verificación **Calcular solo subtotal**. Cada impuesto aparece como un elemento de línea independiente, pero los importes de impuestos no están compuestos.

#### Información de Regla Fiscal

| Campo | Configuración recomendada |
|--- |--- |
| Nombre | `Retail-Canada-GST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-GST` |
| [!UICONTROL Priority] | `0` |
| [!UICONTROL Calculate off subtotal only] | Seleccione esta casilla de verificación. |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### Paso 5: Crear una regla de impuestos PST para Saskatchewan

Para esta regla de impuestos, asegúrese de establecer la prioridad en 0 y active la casilla de verificación **Calcular sólo el subtotal**. Cada impuesto aparece como un elemento de línea independiente, pero los importes de impuestos no están compuestos.

#### Información de Regla Fiscal

| Campo | Configuración recomendada |
|--- |--- |
| [!UICONTROL Name] | `Retail-Canada-PST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-SK-PT` |
| [!UICONTROL Priority] | `1` |
| [!UICONTROL Calculate off subtotal only] | Seleccione esta casilla de verificación. |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### Paso 6: Guarde y pruebe los resultados

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

1. Vuelva a la tienda y cree un pedido de muestra para probar los resultados.

## Configuración fiscal UE

El siguiente ejemplo muestra una tienda con sede en Francia que vende más de 100 000 euros en Francia y más de 100 000 euros en Alemania.

- Los cálculos de impuestos se administran en el nivel de sitio web.
- Las opciones de conversión de moneda y de presentación de impuestos se controlan individualmente en el nivel de vista de tienda (active la casilla de verificación Usar dirección Web para anular el valor predeterminado).
- Al establecer el país de impuestos predeterminado, puede mostrar dinámicamente el impuesto correcto para la jurisdicción.
- El impuesto sobre el producto fijo se incluye para los productos relevantes como atributo del producto.
- Puede que sea necesario editar el catálogo para asegurarse de que se muestra en la categoría, sitio web o vista de tienda correctos.

### Paso 1: Crear tres clases de impuestos de productos

Para este ejemplo, se supone que no se necesitan varias clases de impuestos sobre productos reducidos con IVA.

1. Cree una clase de impuestos de producto estándar con IVA.

1. Cree una clase de impuestos de producto reducidos con IVA.

1. Crear una clase de impuestos de productos sin IVA.

### Paso 2: Creación de tipos impositivos para Francia y Alemania

Cree los siguientes tipos impositivos:

| Tipos impositivos | Configuración |
|--- |--- |
| France-StandardVAT | País: Francia <br/>Estado/Región: * <br/>Código Postal: * <br/>Tarifa: 20% |
| France-ReducedVAT | País: Francia <br/>Estado/Región: * <br/>Código Postal: * <br/>Tarifa: 5% |
| Alemania - StandardVAT | País: Alemania <br/>Estado/Región: * <br/>Código Postal: * Tasa: 19% |
| IVA reducido en Alemania | País: Alemania <br/>Estado/Región: * <br/>Código Postal: * <br/>Tarifa: 7% |

{style="table-layout:auto"}

### Paso 3: Configuración de las reglas fiscales

Cree las siguientes reglas fiscales:

| Reglas fiscales | Configuración |
|--- |--- |
| Retail-France-StandardVAT | Clase de cliente: Cliente minorista <br/>Clase de impuesto: Estándar para IVA <br/>Tipo impositivo: Francia-Estándar para IVA <br/>Prioridad: 0 <br/>Orden de clasificación: 0 |
| Retail-France-ReducedVAT | Clase de cliente: Cliente minorista <br/>Clase de impuesto: IVA reducido <br/>Tipo impositivo: Francia-IVA reducido <br/>Prioridad: 0 <br/>Orden de clasificación: 0 |
| Retail-Germany-StandardVAT | Clase de cliente: Cliente minorista <br/>Clase de impuesto: Estándar de IVA <br/>Tipo impositivo: Alemania-Estándar de IVA <br/>Prioridad: 0 <br/>Orden de clasificación: 0 |
| Retail-Germany-ReducedVAT | Clase de cliente: Cliente minorista <br/>Clase de impuesto: <br/>Reducción de IVA: Tasa de impuesto: AlemaniaReducción de IVA <br/>Prioridad: 0 <br/>Orden de clasificación: 0 |

{style="table-layout:auto"}

### Paso 4: Configurar una vista de tienda para Alemania

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. En el sitio web predeterminado, cree una vista de tienda para **[!UICONTROL Germany]**.

1. A continuación, haga lo siguiente:

   - En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - En la esquina superior izquierda, establezca **[!UICONTROL Default Config]** en la tienda en francés.

   - En la página General, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Countries Options]** y establezca el país predeterminado en `France`.

   - Complete las opciones de configuración regional según sea necesario.

1. En la esquina superior izquierda, elija el alemán **[!UICONTROL Store View]**.

1. En la página _General_, expanda ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Countries Options]** y establezca el país predeterminado en `Germany`.

1. Complete las opciones de configuración regional según sea necesario.

### Paso 5: Configuración de impuestos para Francia

Complete la siguiente configuración general de impuestos:

| Campo | Configuración recomendada |
|--- |--- |
| [[!UICONTROL Tax Classes]](../configuration-reference/sales/tax.md#tax-classes) |  |
| [!UICONTROL Tax Class for Shipping] | `Shipping` (el envío está gravado) |
| [[!UICONTROL Calculation Settings]](../configuration-reference/sales/tax.md#calculation-settings) |  |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Address` |
| [!UICONTROL Catalog Prices] | `Including Tax` |
| [!UICONTROL Shipping Prices] | `Including Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Including Tax` |
| [!UICONTROL Apply Tax On] | `Custom Price if available` |
| [[!UICONTROL Default Tax Destination Calculation]](../configuration-reference/sales/tax.md#default-tax-destination-calculation) |  |
| [!UICONTROL Default Country] | `France` |
| [!UICONTROL Default State] |  |
| [!UICONTROL Default Postal Code] | `*` (asterisco) |
| [[!UICONTROL Fixed Product taxes]](../configuration-reference/sales/tax.md#fixed-product-taxes) |  |
| [!UICONTROL Enable FPT] | `Yes` |
| [!UICONTROL All FPT Display Settings] | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `Yes` |

{style="table-layout:auto"}

### Paso 6: Configuración de impuestos para Alemania

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En la esquina superior derecha, establezca **[!UICONTROL Store View]** en la vista de la tienda en alemán y haga clic en **[!UICONTROL OK]** para confirmar.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Tax]**.

1. En la sección **[!UICONTROL Default Tax Destination Calculation]**, haga lo siguiente:

   - Desactive la casilla de verificación **[!UICONTROL Use Website]** después de cada campo,

   - Para que coincida con la configuración de envío del sitio [punto de origen](shipping-settings.md#point-of-origin), actualice los siguientes valores:

      - País predeterminado
      - Estado predeterminado
      - Código postal predeterminado

     Esta configuración garantiza que el impuesto se calcule correctamente cuando los precios del producto incluyen impuestos.

     ![Cálculo de destino de impuestos predeterminado](./assets/destination-calc-french.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
