---
title: Informe Liquidación de PayPal
description: Obtenga información sobre el informe Liquidación de PayPal como herramienta para administrar transacciones de PayPal.
exl-id: cd087e15-e6ad-4472-9038-8c64fde316f9
feature: Payments
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
TQID: https://experienceleague.adobe.com/c7v5oSsVPmD6r6obfGEoxPiGkMI4KMWAmfJAW0-CCJk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 233
ht-degree: 0%

---

# Informe Liquidación de PayPal

El informe Liquidación de PayPal proporciona a los comerciantes información sobre cada transacción que afecta a la liquidación de fondos.

>[!NOTE]
>
>Antes de generar los informes de liquidación, el administrador de la tienda debe solicitar a Servicios técnicos de comerciante de PayPal que cree una cuenta de usuario SFTP, que habilite la generación de informes de liquidación y que habilite SFTP en su cuenta comercial de PayPal.

Después de configurar y habilitar los informes de liquidación en la cuenta de comerciante de PayPal, Adobe Commerce y Magento Open Source empezarán a generar informes durante las 24 horas siguientes. La lista de los informes de liquidación disponibles se puede ver desde el Administrador.

**_Para ver los informes de liquidación:_**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**.

   ![Informes de liquidación de PayPal](../getting-started/assets/reports-sales-paypal-settlement.png){width="600" zoomable="yes"}

1. Para las actualizaciones más recientes, haga clic en **[!UICONTROL Fetch Updates]** en la esquina superior derecha.

   El sistema se conecta al servidor SFTP de PayPal para recuperar los informes. Cuando se completa el proceso, aparece un mensaje con el número de informes recuperados. El informe incluye la siguiente información para cada transacción:

   | Columna del informe | Descripción |
   | ------------ | ----------- |
   | [!UICONTROL PayPal Reference ID Type] | Uno de los siguientes códigos de referencia:<br/>- ID de pedido<br/>- ID de transacción<br/>- ID de suscripción |
   | [!UICONTROL Preapproved Payment ID] | **[!UICONTROL Custom]**: el texto escrito por el comerciante en la transacción en PayPal.<br/>**[!UICONTROL Transaction Debit or Credit]**- La dirección del movimiento de dinero de importe bruto.<br/>**[!UICONTROL Fee Debit or Credit]** - La dirección del movimiento de dinero por honorarios. |

   {style="table-layout:auto"}
