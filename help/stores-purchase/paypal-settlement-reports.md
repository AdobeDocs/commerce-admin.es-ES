---
title: Informe Liquidación de PayPal
description: Obtenga información sobre el informe Liquidación de PayPal como herramienta para administrar transacciones de PayPal.
exl-id: cd087e15-e6ad-4472-9038-8c64fde316f9
feature: Payments
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '222'
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
   | [!UICONTROL Preapproved Payment ID] | **[!UICONTROL Custom]**: el texto introducido por el comerciante en la transacción en PayPal.<br/>**[!UICONTROL Transaction Debit or Credit]**: dirección del movimiento de dinero de la cantidad bruta.<br/>**[!UICONTROL Fee Debit or Credit]**: la dirección del movimiento de dinero de pago. |

   {style="table-layout:auto"}
