---
title: Impuestos
description: Aprenda a configurar su tienda para calcular los impuestos según los requisitos de su configuración regional.
exl-id: bf807132-416f-497a-82c4-b00dba4d3092
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 0%

---

# Impuestos

Configure su tienda para calcular los impuestos según los requisitos de su configuración regional. Puede configurar [clases de impuestos](tax-class.md) para productos y grupos de clientes, y crear [reglas de impuestos](tax-rules.md) que combinen clases de productos y clientes, zonas de impuestos y tasas. Commerce también proporciona ajustes de configuración para impuestos de productos fijos, impuestos compuestos y visualización de precios a través de fronteras internacionales. Si necesita cobrar un [impuesto al valor agregado](vat.md), puede configurar su tienda para que calcule automáticamente la cantidad apropiada con la validación.

>[!NOTE]
>
>Las versiones 2.4.0 a 2.4.3 de Adobe Commerce y Magento Open Source incluían la extensión desarrollada por el proveedor Vertex que se integraba con Vertex Cloud para proporcionar administración de impuestos y limpieza de direcciones. A partir de la versión 2.4.4, esta extensión ya no se integra con la versión principal y debe instalarse y actualizarse desde el Commerce Marketplace o directamente desde el proveedor. [Póngase en contacto con Vertex](https://marketplace.magento.com/partner/vertex_inc) para obtener información acerca de la extensión y la documentación.<br><br>
>
>Si tiene la extensión agrupada habilitada y configurada, debe actualizar el archivo composer.json como parte del proceso de actualización de la versión 2.4.4 y administrar las actualizaciones de extensión que se realicen. Consulte [Módulos de actualización](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) en la _Guía de actualización_.

## Referencia rápida

Algunas configuraciones de impuestos tienen una selección de opciones que determinan la forma en que se calcula el impuesto y se presenta al cliente. Para obtener más información, consulte [Directrices fiscales internacionales](international-tax-guidelines.md).

Utilice las siguientes tablas como referencia al configurar los ajustes de cálculo de impuestos:

### Métodos de cálculo de impuestos

Las opciones del método de cálculo de impuestos incluyen [!UICONTROL Unit Price], [!UICONTROL Row Total] y [!UICONTROL Total]. En la tabla siguiente se explica cómo se controla el redondeo (de dos dígitos) para diferentes configuraciones.

| Configuración | Cálculo y visualización |
|--- |--- |
| [!UICONTROL Unit Price] | Commerce calcula el impuesto de cada artículo y muestra los precios con impuestos incluidos. Para calcular el total de impuestos, redondea el impuesto de cada artículo y, a continuación, lo suma. |
| [!UICONTROL Row Total] | Commerce calcula el impuesto de cada línea. Para calcular el total de impuestos, redondea el impuesto para cada elemento de línea y, a continuación, lo suma. |
| [!UICONTROL Total] | Commerce calcula el impuesto de cada artículo y suma esos valores de impuestos para calcular el importe total de impuestos no redondeados del pedido. A continuación, aplica el modo de redondeo especificado al impuesto total para determinar el impuesto total del pedido. |

{style="table-layout:auto"}

### Precios de catálogo con o sin impuestos

Los campos de visualización posibles varían según el método de cálculo y si los precios del catálogo incluyen o excluyen impuestos. Los campos de visualización tienen una precisión de dos decimales en los cálculos normales. Algunas combinaciones de configuraciones de precios muestran precios que incluyen y excluyen impuestos. Cuando ambos aparecen en el mismo elemento de línea, puede resultar confuso para los clientes y déclencheur una [advertencia](taxes.md#warning-messages).

| Configuración | Cálculo y visualización |
|--- |--- |
| [!UICONTROL Excluding Tax] | Con esta configuración, se utiliza el precio de artículo base tal como se introduce y se aplican los métodos de cálculo de impuestos. |
| [!UICONTROL IncludingTax] | Con esta configuración, el precio de artículo base que excluye impuestos se calcula primero. Este valor se utiliza como precio base y se aplican los métodos de cálculo de impuestos. |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Hay cambios con respecto a las versiones anteriores para los comerciantes de la UE u otros comerciantes de IVA que muestran precios, incluidos impuestos, y operan en varios países con múltiples vistas de tiendas. Si cargas los precios con más de dos dígitos de precisión, Commerce redondea automáticamente todos los precios a dos dígitos para garantizar que se presenta un precio coherente a los compradores.

### Precios de envío con o sin impuestos

| Configuración | Mostrar | Cálculo |
|--- |--- |--- |
| [!UICONTROL Excluding Tax] | Aparece sin impuestos. | Cálculo normal. El envío se agrega al total del carro de compras, y generalmente se muestra como un artículo independiente. |
| [!UICONTROL Including Tax] | Pueden ser impuestos incluidos o impuestos mostrados por separado. | El envío se trata como otro artículo del carro de compras con impuestos, utilizando los mismos cálculos. |

{style="table-layout:auto"}

### Importes de impuestos como artículos de línea

Para mostrar dos importes de impuestos diferentes como artículos de línea independientes, como GST y PST para tiendas canadienses, debe establecer prioridades diferentes para las reglas de impuestos relacionadas. Sin embargo, en cálculos fiscales anteriores, los impuestos con prioridades diferentes se agravarían automáticamente. Para mostrar correctamente importes de impuestos independientes sin una composición incorrecta de los importes de impuestos, puede establecer prioridades diferentes y también seleccionar la casilla de verificación _Calcular sólo el subtotal_. Esta configuración genera importes de impuestos calculados correctamente que aparecen como elementos de línea independientes.

## Mensajes de advertencia

Algunas combinaciones de opciones relacionadas con impuestos pueden resultar confusas para los clientes y dar déclencheur a una advertencia. Estas condiciones pueden producirse cuando el método de cálculo de impuestos está establecido en `Row` o `Total`, y al cliente se le presentan precios que excluyen e incluyen impuestos. También puede ocurrir cuando hay impuestos por artículo en el carro de compras. Como el cálculo de impuestos se redondea, el importe que aparece en el carro de compras podría diferir del importe que un cliente espera pagar.

Si el cálculo de impuestos se basa en una configuración problemática, aparecen las siguientes advertencias:

![Signo de exclamación](../assets/icon-warning.png) **Advertencia**. `Tax discount configuration might result in different discounts than a customer might expect for store(s); Europe Website (French), Europe Website (German). Please see source for more details.`

![Signo de exclamación](../assets/icon-warning.png) **Advertencia**. `Tax configuration can result in rounding errors for store(s): Europe Websites (French), Europe Websites (German).`

## Lugar de suministro de bienes digitales (UE)

Los comerciantes de la Unión Europea (UE) deben informar de sus productos digitales vendidos por trimestre a cada país miembro. Los bienes digitales se gravan en función de la dirección de envío del cliente. La ley requiere que los comerciantes realicen un informe fiscal e identifiquen los montos de impuestos relevantes para los bienes digitales, en lugar de los bienes físicos.

Los comerciantes deben informar trimestralmente a una administración tributaria central de todos los bienes digitales vendidos por los países miembros de la UE, junto con el pago de los impuestos recaudados durante el período.

Los comerciantes que aún no hayan alcanzado el umbral (50 000/100 000 euros de negocio anual) deben seguir informando de los bienes físicos vendidos a los Estados de la UE en los que hayan registrado números de IVA.

Los comerciantes que son auditados por los impuestos pagados por los bienes digitales, deben proporcionar dos piezas de información de apoyo para establecer el lugar de residencia del cliente.

- La dirección de envío del cliente y un registro de una transacción de pago correcta se pueden utilizar para establecer el lugar de residencia del cliente. (El pago se acepta únicamente si la dirección de envío coincide con la información del proveedor de pago.)
- La información también se puede capturar directamente del almacén de datos en las tablas de la base de datos de Commerce.

_&#x200B;**Para recopilar información de impuestos sobre bienes digitales:**&#x200B;_

1. Cargue los tipos impositivos para todos los países miembros de la UE.

1. Cree una clase de impuestos de productos de bienes digitales.

1. Asigne todos sus bienes digitales a la clase de impuestos de productos de bienes digitales.

1. Cree [reglas de impuestos](tax-rules.md) para sus bienes físicos, utilizando clases de impuestos de productos físicos, y asócielas con las tasas de impuestos correspondientes.

1. Cree reglas fiscales para sus bienes digitales, utilizando la clase de impuestos de productos para bienes digitales, y asócielas con las tasas impositivas apropiadas para los países miembros de la UE.

1. Ejecute el informe de impuestos para el período adecuado y recopile la información de bienes digitales necesaria.

1. Exporte los importes de impuestos relacionados con los tipos impositivos para la clase de impuestos de productos de bienes digitales.

Recursos adicionales:

- [Unión Tributaria y Aduanera de la Comisión Europea][1]
- [Cambios en el lugar de suministro de EU 1015][2]

[1]: https://europa.eu/youreurope/business/taxation/vat/vat-rules-rates/index_en.htm
[2]: https://www2.deloitte.com/global/en/services/tax.html
