---
title: Transacciones
description: Obtenga información sobre la página Transacciones y cómo utilizarla para realizar un seguimiento de la actividad entre su tienda y un sistema de pago.
exl-id: 5970db88-146d-4caf-aab4-d9315357a4fe
feature: Payments
TQID: https://experienceleague.adobe.com/WyZwtVw-F-pGxxfcHMU-UTz8GVROVyM-YYaLzivMLBM
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 318
ht-degree: 0%

---

# Transacciones

La página _Transacciones_ enumera toda la actividad de pago que se ha realizado entre su tienda y un sistema de pago, y proporciona acceso a información más detallada.

## Ver transacciones

En la barra lateral _Admin_, vaya a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Transactions]**.

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

Esta sección incluye información sobre la transacción y proporciona un vínculo a la página de pedidos en la columna **Id. de pedido**.

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
