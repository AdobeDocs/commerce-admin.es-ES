---
title: Administrar crédito de la empresa
description: Obtenga información sobre las líneas de crédito de la empresa, la configuración de parámetros y el procesamiento de pagos a cuenta.
exl-id: 62ff2a36-053d-4ba0-9969-0f05701afbff
feature: B2B, Companies, Payments
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 0%

---

# Administrar crédito de la empresa

If [Pago a cuenta](../getting-started/../b2b/enable-basic-features.md#configure-payment-on-account) está habilitado en la configuración de, las empresas pueden realizar compras en su cuenta hasta el límite de crédito concedido a la empresa. Cuando se habilita, los clientes pueden comprobar el estado del crédito de su compañía desde su panel de cuentas.

![Crédito de empresa](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

Puede establecer los siguientes parámetros relacionados con el crédito para cada perfil de compañía:

- Divisa de crédito
- Límite de crédito
- Permitir que se supere el límite de crédito
- Motivo del cambio

Si la empresa tiene un saldo pendiente, aparece un aviso al administrador de la tienda en la parte superior del pedido de ventas cuando se consulta desde el administrador. Para obtener más información, consulte [Crear una cuenta de empresa](account-company-create.md).

## Actividad de crédito de empresa

El [!UICONTROL Company Credit] La sección del perfil de la empresa muestra un resumen de la actividad de crédito del cliente, con una cuadrícula del historial de crédito de la empresa.

![Actividad de crédito de empresa](./assets/company-credit-reimbursements-grid.png){width="700" zoomable="yes"}

| Columna | Descripción |
|--- |--- |
| [!UICONTROL Date] | La fecha de la transacción. Para mostrar la fecha y la hora, pase el ratón sobre la fecha. |
| [!UICONTROL Operation] | El tipo de actividad asociada con la transacción. Valores: <br/>**[!UICONTROL Allocated]**- Crédito asignado a la empresa.<br/>**[!UICONTROL Updated]** - Se ha aplicado un cambio a uno de los campos siguientes: [!UICONTROL Credit limit] / [!UICONTROL Credit currency] / [!UICONTROL Allow to exceed credit limit] <br/>**[!UICONTROL Purchased]**- Se ha realizado un pedido.<br/>**[!UICONTROL Reimbursed]** - Se reembolsó el saldo pendiente. <br/>**[!UICONTROL Refunded]**- Se ha reembolsado un importe de nota de abono.<br/>**[!UICONTROL Reverted]** - El pedido fue cancelado y la cantidad devuelta al saldo de crédito. |
| [!UICONTROL Amount] | El importe de la transacción asociada con los siguientes tipos de transacción: `Purchased` / `Reimbursed` / `Refunded` / `Reverted` <br/>Para los importes de compra, el importe aparece en la moneda de visualización del almacén y en el formato de la configuración de la moneda de crédito, seguido del tipo de cambio actual (si corresponde). Por ejemplo: <br/>20.000,00 EUR (22.400,00 USD) <br/>USD/EUR 0,8928 |
| [!UICONTROL Outstanding Balance] | El importe reembolsado, menos el total adeudado de todos los pedidos realizados mediante el método Pago a Cuenta. La cantidad puede aparecer como un valor positivo o negativo. <br/>**[!UICONTROL Positive value]**- El anticipo se representa como un valor positivo.<br/>**[!UICONTROL Negative value]** - Un importe adeudado se representa como un valor negativo. |
| [!UICONTROL Available Credit] | La suma de los _[!UICONTROL Credit Limit]_y el_[!UICONTROL Outstanding Balance]_. Si la empresa ha superado el límite de crédito, el importe aparece como un valor negativo. |
| [!UICONTROL Credit Limit] | El importe del crédito concedido a la empresa. |
| [!UICONTROL Updated By] | Nombre de la persona que inició la operación. |
| [!UICONTROL Custom Reference Number] | Número de referencia personalizado asociado con la transacción. |
| [!UICONTROL Comment] | Una compilación de los valores de `Reason for Change` , según el tipo de operación. <br/>**[!UICONTROL Purchased]**- Incluye comentarios de la compra, el número de pedido y el vínculo al pedido.<br/>**[!UICONTROL Reimbursed]** - Incluye comentarios de la transacción reembolsada. |
| [!UICONTROL Action] | Para `Reimbursed` solo operaciones. **[!UICONTROL Edit]** - Permite actualizar el importe de reembolso. |

{style="table-layout:auto"}

## Actualizar la información de crédito

Cuando el cliente realiza el pago de su crédito pendiente al comerciante, un administrador de tienda debe actualizar la información de crédito del cliente en el Administrador.

1. En el _Administrador_ barra lateral, vaya a **Clientes > Compañías**.

1. Busque la empresa en la cuadrícula y abra en _Editar_ modo.

1. Expanda el **Crédito de empresa** sección.

1. Para **Límite de crédito**, introduzca el nuevo valor.

1. Cambie los demás valores según sea necesario.

1. Cuando se hayan completado las actualizaciones, haga clic en **[!UICONTROL Save]**.

## Recibir pagos

Un saldo reembolsado es un pago fuera de línea que realiza una compañía hacia el saldo de su cuenta. El administrador de tienda introduce la cantidad manualmente en el perfil de la empresa, utilizando _Saldo de reembolso_ botón. Cuando se envía el importe, el sistema vuelve a calcular el saldo pendiente y el crédito disponible de la empresa y registra la acción en el historial de crédito de la empresa. El importe reembolsado se introduce en la divisa de abono, tal como se especifica en la configuración.

### Aplicar un pago a una cuenta de empresa

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Busque el registro de empresa en la lista y abra en **[!UICONTROL Edit]** modo.

1. En la parte superior de la página, haga clic en **Saldo de reembolso**.

1. En el cuadro de diálogo, añada la información de pago:

   ![Saldo de reembolso](./assets/company-reimburse-balance.png){width="500"}

   - Introduzca el **Cantidad** del pago.

     La cantidad se puede introducir como valor positivo o negativo.

   - Si procede, introduzca la variable **Número de referencia personalizado** como referencia.

     Sólo se puede introducir un número de referencia personalizado por cada reembolso. Para aplicar el pago a varios pedidos, cree un reembolso distinto para cada uno.

   - Si es necesario, introduzca un **Comentario** para describir el reembolso.

1. Clic **Reembolso**.

   El saldo pendiente de la empresa y el crédito disponible se vuelven a calcular, y el historial de crédito de la empresa se actualiza para reflejar el reembolso.

### Editar un reembolso

1. Abra el perfil de la empresa en **[!UICONTROL Edit]** modo.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **Crédito de empresa** sección.

1. Busque la transacción de reembolso en la cuadrícula y haga clic en **[!UICONTROL Edit]**.

1. Realice los cambios necesarios en **Número de referencia personalizado** y **Comentario**.

   No se puede cambiar el importe del reembolso.

1. Haga clic **[!UICONTROL Save]**.

## Información de crédito de tienda

Para el administrador de la empresa, el panel de cuentas muestra la variable _Crédito de empresa_ sección. Proporciona el saldo pendiente actual, el crédito disponible y el límite de crédito asignado a su cuenta de compañía seguido de una lista de facturas pendientes.

Si el comerciante cancela un pedido que se cargó al crédito de la empresa, el importe del pedido se devuelve al saldo de la empresa y al _Historial de asignación de crédito_ incluye un registro de la acción.

![Crédito de empresa](./assets/company-credit.png){width="700" zoomable="yes"}

## Demostración de crédito de empresa

Obtenga información acerca de la administración del crédito de la empresa viendo este vídeo de demostración:

>[!VIDEO](https://video.tv.adobe.com/v/344445?quality=12)
