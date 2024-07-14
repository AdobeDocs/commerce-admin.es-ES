---
title: Ámbito de cuenta de cliente
description: El ámbito de las cuentas de cliente puede limitarse al sitio web en el que se creó la cuenta o compartirse con todos los sitios web y tiendas de la jerarquía de tiendas.
exl-id: c401bee2-763e-4fad-88cd-5d5a43c46186
feature: Customers, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '355'
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
