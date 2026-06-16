---
title: Ámbito de cuenta de cliente
description: El ámbito de las cuentas de cliente puede limitarse al sitio web en el que se creó la cuenta o compartirse con todos los sitios web y tiendas de la jerarquía de tiendas.
exl-id: c401bee2-763e-4fad-88cd-5d5a43c46186
feature: Customers, Configuration
TQID: https://experienceleague.adobe.com/ah5XmCeeX4Kc9czcllRq9zZX4W3rkkqkzcoUXtJjo5I
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 356
ht-degree: 0%

---

# Ámbito de cuenta de cliente

El encabezado de cada página de tu tienda extiende una invitación para que los compradores _inicien sesión o registren_ una cuenta en tu tienda. Los clientes que abren una cuenta de disfrutan de una serie de ventajas, entre las que se incluyen:

* **Crear cuenta de cliente**: los visitantes pueden crear una cuenta de cliente para que puedan usar la tienda como cliente registrado.
* **Crear una cuenta de compañía** Según la configuración, un visitante de su tienda puede elegir crear una cuenta de compañía. Para obtener más información, consulte [Adobe Commerce B2B](../b2b/introduction.md).
* **Cierre de compra más rápido**: Los clientes registrados pasan por el cierre de compra más rápido porque gran parte de la información ya está en sus cuentas.
* **Autoservicio**: los clientes registrados pueden actualizar su información, comprobar el estado de los pedidos e incluso reordenar desde sus cuentas.

Los clientes pueden acceder a su cuenta haciendo clic en el vínculo **[!UICONTROL My Account]** en el encabezado de la tienda. Desde su cuenta, los clientes pueden ver y modificar información, como direcciones actuales y pasadas, preferencias de facturación y envío, suscripciones a boletines informativos, listas de deseos y mucho más.

![Mi cuenta](assets/account-dashboard-my-account.png){width="600" zoomable="yes"}

## Establecer el ámbito de las cuentas de cliente

El ámbito de las cuentas de cliente puede limitarse al sitio web en el que se creó la cuenta o compartirse con todos los sitios web y tiendas de la jerarquía de tiendas.

>[!NOTE]
>
>Si el sitio web se excluye del grupo de clientes, el cliente no puede iniciar sesión en el sitio web cuando el ámbito de las cuentas de cliente se limita al sitio web o se comparte con todos los sitios web. Consulte [Crear un grupo de clientes](customer-groups.md#create-a-customer-group) para obtener más información sobre cómo excluir sitios web de grupos.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > [!UICONTROL _[!UICONTROL Settings]_] > **[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Customer Configuration]**.

1. Expanda la sección **[!UICONTROL Account Sharing Options]**.

   ![Opciones de uso compartido de cuentas](assets/customer-configuration-account-sharing-options.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Share Customer Accounts]** en una de las siguientes opciones:

   | Opción | Descripción |
   | --- | --- |
   | `Global` | Comparte la información de la cuenta del cliente con cada sitio web y almacén de la instalación. |
   | `Per Website` | Limita la información de la cuenta del cliente al sitio web donde se creó la cuenta. |

   {style="table-layout:auto"}

   >[!INFO]
   >
   > Si es necesario, desactive la casilla de verificación **[!UICONTROL User system value]** para realizar el cambio.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

   >[!NOTE]
   >
   >Cuando se selecciona `Global`, se comparte la información del cliente en **Mi cuenta** (direcciones e información de la cuenta como los detalles de contacto).
