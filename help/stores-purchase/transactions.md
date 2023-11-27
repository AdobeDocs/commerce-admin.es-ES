---
title: Transacciones
description: Obtenga información sobre la página Transacciones y cómo utilizarla para realizar un seguimiento de la actividad entre su tienda y un sistema de pago.
exl-id: 5970db88-146d-4caf-aab4-d9315357a4fe
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Transacciones

El _Transacciones_ Esta página enumera todas las actividades de pago que han tenido lugar entre su tienda y un sistema de pago, y proporciona acceso a información más detallada.

## Ver transacciones

En el _Administrador_ barra lateral, vaya a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Transactions]**.

![Cuadrícula de transacciones](./assets/transactions.png){width="600" zoomable="yes"}

| Columna | Descripción |
|--- |--- |
| [!UICONTROL ID] | Identificador numérico único que se asigna a cada transacción. |
| [!UICONTROL Order ID] | Identificador único que se asigna cuando un cliente realiza un pedido. |
| [!UICONTROL Transaction ID] | Identificador numérico único que se asigna cuando se produce una transacción después de que un cliente realice un pedido. |
| [!UICONTROL Parent Transaction ID] | Número de ID de la transacción principal. |
| [!UICONTROL Payment Method] | El método de pago asociado a una transacción. |
| [!UICONTROL Transaction Type] | Tipo de transacción, que puede ser Pedido, Autorización, Captura, Anulación o Devolución. |
| [!UICONTROL Closed] | Si una transacción está cerrada o no. |
| [!UICONTROL Created] | Fecha y hora en la que se creó la transacción. |

{style="table-layout:auto"}

## Ver detalles de la transacción

Haga clic en la entrada que desee ver.

En la página de detalles de transacción, puede ver la cuadrícula de detalles de transacción y transacciones secundarias.

### Datos de transacción

Esta sección incluye información sobre la transacción y proporciona un vínculo a la página de pedidos en la **ID de pedido** columna.

| Columna | Descripción |
|--- |--- |
| [!UICONTROL Transaction ID] | Número de ID de transacción. |
| [!UICONTROL Parent Transaction ID] | Un número de ID correspondiente de la transacción principal, si corresponde. |
| [!UICONTROL Transaction Type] | Tipo de transacción, que puede ser Pedido, Autorización, Captura, Anulación o Devolución. |
| [!UICONTROL Is Closed] | Si una transacción está cerrada o no. |
| [!UICONTROL Created At] | Fecha y hora en la que se creó la transacción. |

{style="table-layout:auto"}

### Transacciones secundarias

Las transacciones secundarias se muestran en la cuadrícula después de crear facturas para [pedidos](orders.md). Este formato le permite realizar un seguimiento del historial de transacciones, siguiendo una jerarquía de transacciones.

### [!UICONTROL Transaction Details]

Esta sección incluye información adicional sobre una transacción determinada. La información se muestra en forma de claves y valores. Las claves disponibles son:

- authAmount
- authCode
- aVSResponse
- billTo
- cardCodeResponse
- cliente
- customerIP
- lineItems
- marketType
- pedido
- pago
- producto
- recurringBilling
- responseCode
- responseReasonCode
- responseReasonDescription
- settAmount
- solución
- submitTimeLocal
- submitTimeUTC
- taxExempt
- transactionStatus

>[!NOTE]
>
>Si los detalles de la transacción no están disponibles o no están actualizados, haga clic en **[!UICONTROL Fetch]** en la barra de botones para actualizarlos.
