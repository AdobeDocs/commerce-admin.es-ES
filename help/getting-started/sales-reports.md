---
title: Informes de ventas
description: El [!DNL Commerce] los informes de ventas permiten realizar un seguimiento de pedidos, impuestos, facturas, envíos, reembolsos, cupones y liquidaciones de PayPal.
exl-id: 928a407f-cbed-4114-ad0b-ee227383bf36
feature: Reporting, Orders
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 1%

---

# Informes de ventas

La selección de informes de ventas incluye Pedidos, Impuestos, Facturados, Envíos, Devoluciones, Cupones y Liquidación de PayPal.

## Filtros de informes

Puede generar un informe de ventas para un sitio web completo o para una tienda. Los informes de ventas pueden filtrarse por intervalo de tiempo, fecha y estado.

![Filtros del informe de ventas](./assets/tax-report.png){width="600"}

Para filtrar un informe de ventas, defina las siguientes opciones:

| Opción | Descripción |
|--- |--- |
| [!UICONTROL Date Used] | Establece los datos que se utilizarán para el informe. |
| [!UICONTROL Period] | Período para el que se utilizan los datos: día/mes/año. |
| [!UICONTROL From/To] | Se utiliza para definir los datos de búsqueda por fecha de inicio y finalización. |
| [!UICONTROL Order Status] | Indica el estado del pedido |
| [!UICONTROL Empty Rows] | Indica si se deben agregar filas en blanco al informe. |

## [!UICONTROL Orders Report]

El [!UICONTROL Orders Report] incluye el número de pedidos realizados y cancelados, con totales de ventas, importes facturados, reembolsados, impuestos cobrados, gastos de envío y descuentos.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Orders]**.

1. En el **[!UICONTROL Filter]** , seleccione las opciones del período de informe y el estado del pedido utilizados para rellenar el informe.

1. Haga clic **[!UICONTROL Show Report]**.

![Registros de informe de pedidos](./assets/order-report-records.png){width="600"}

## [!UICONTROL Tax Report]

El [!UICONTROL Tax Report] incluye la regla fiscal aplicada, el tipo impositivo, el número de pedidos y el importe del impuesto cobrado.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Tax]**.

1. En el **[!UICONTROL Filter]** , seleccione las opciones del período de informe y el estado del pedido utilizados para rellenar el informe.


1. Haga clic **[!UICONTROL Show Report]**.

![Informe de impuestos](./assets/tax-report-records.png){width="600"}

## [!UICONTROL Invoice Report]

El [!UICONTROL Invoice Report] incluye el número de pedidos y facturas durante el período de tiempo, con importes facturados, pagados y no pagados.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Invoiced]**.

1. En el **[!UICONTROL Filter]** , seleccione las opciones del período de informe y el estado del pedido utilizados para rellenar el informe.

1. Haga clic **[!UICONTROL Show Report]**.

![Informe de facturas](./assets/sales-invoiced.png){width="600"}

## [!UICONTROL Shipping Report]

El [!UICONTROL Shipping Report] incluye el número de pedidos del transportista o método de envío utilizado, incluidos los importes de las ventas totales y el envío total.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Shipping]**.

1. En el **[!UICONTROL Filter]** , seleccione las opciones del período de informe y el estado del pedido utilizados para rellenar el informe.

1. Haga clic **[!UICONTROL Show Report]**.

![Informe de envío](./assets/shipping.png){width="600"}

## [!UICONTROL Refunds Report]

El [!UICONTROL Refunds Report] incluye el número de pedidos reembolsados y el importe total reembolsado en línea y sin conexión.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Refunds]**.

1. En el **[!UICONTROL Filter]** , seleccione las opciones del período de informe y el estado del pedido utilizados para rellenar el informe.

1. Haga clic **[!UICONTROL Show Report]**.

![Informe de reembolsos](./assets/sales-refunds.png){width="600"}

## [!UICONTROL Coupons Report]

El [!UICONTROL Coupons Report] incluye cada código de cupón utilizado durante el intervalo de tiempo especificado, la regla de precio relacionada y el número de veces utilizado, con totales y subtotales de ventas y descuentos.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Coupons]**.

1. En el **[!UICONTROL Filter]** , seleccione las opciones del período de informe y el estado del pedido utilizados para rellenar el informe.

1. Haga clic **[!UICONTROL Show Report]**.

Para obtener más información sobre el uso de [!UICONTROL Coupons Report] para recopilar datos para sus campañas promocionales, consulte [Informes de cupones](../merchandising-promotions/price-rules-cart-coupon.md#coupons-report) en el _Guía de promociones y comercialización_.

<!--- ![Coupons Report](./assets/sales-coupons.png) need coupon data  -->

## [!UICONTROL PayPal Settlement Reports]

El [Informes de liquidación de PayPal] página incluye el tipo de evento, como una transacción con tarjeta de débito, las fechas de inicio y finalización, el importe bruto y las tarifas relacionadas. El informe se puede actualizar automáticamente con los datos más actuales de PayPal. Existen opciones de filtrado para el intervalo de fechas, la cuenta de comerciante, el ID de transacción, el ID de factura o el ID de referencia de PayPal.

En el _Administrador_ barra lateral, vaya a **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**.

![Informe de liquidación de PayPal](./assets/reports-sales-paypal-settlement.png){width="600"}

Para obtener más información sobre el uso de [!UICONTROL PayPal Settlement Reports] para recuperar información sobre cada transacción de PayPal que afecte a la liquidación de fondos, consulte [Informes de liquidación de PayPal](../stores-purchase/paypal-settlement-reports.md) en el _Guía de experiencia de compra y tienda_.

## [!UICONTROL Braintree Settlement Report]

El [Braintree](../stores-purchase/braintree.md) El informe de liquidación puede filtrarse según la fecha de creación, el importe, el estado, el tipo de transacción, el tipo de pago, el ID de transacción, el ID de pedido, el ID de pago de PayPal, el tipo, el ID de cuenta de comerciante o el ID de lote de liquidación. El informe contiene el ID de transacción, el ID de pedido, el ID de pago de PayPal, el tipo, la fecha de creación, el importe, el código de liquidación, el estado, el texto de respuesta de liquidación, los ID de reembolso, el ID de cuenta de comerciante, el ID de lote de liquidación y la divisa.

En el _Administrador_ barra lateral, vaya a **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Braintree Settlement]**.

<!--- ![Braintree Settlement Report](./assets/braintree-settlement.png) need a Braintree connection to update report screen -->

## Exportación de informes

1. Para exportar el informe, seleccione el tipo de archivo: `Excel XML` o `CSV`

1. Haga clic **[!UICONTROL Export]**.

## Actualizar estadísticas

Para reducir el impacto de la generación de informes de ventas en el rendimiento, [!DNL Commerce] calcula y almacena las estadísticas necesarias para cada informe. En lugar de volver a calcular las estadísticas cada vez que se genera un informe, se utilizan las estadísticas almacenadas, a menos que actualice las estadísticas. Para incluir los datos más recientes, las estadísticas del informe deben actualizarse antes de generar un informe de ventas.

![Actualizar estadísticas](./assets/refresh-stats.png){width="700"}

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Reports]** > _[!UICONTROL Statistics]_>**[!UICONTROL Refresh Statistics]**.

1. En la lista, active la casilla de verificación de cada informe que desee actualizar.

1. Configure las variables **[!UICONTROL Actions]** a una de las siguientes opciones:

   - `Refresh Lifetime Statistics`
   - `Refresh Statistics for the Last Day`

1. Haga clic **[!UICONTROL Submit]**.
