---
title: Actualización de un perfil de cliente
description: Acceda a información sobre la actividad de los clientes, como cuándo iniciaron sesión o salieron de su cuenta por última vez y actualice el perfil del cliente.
exl-id: 8e805095-76b2-4237-98dc-aa32f15f2637
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 0%

---

# Actualización de un perfil de cliente

El panel izquierdo de la página _[!UICONTROL Customer Information]_incluye información sobre la actividad del cliente, las direcciones, las estadísticas de pedidos, los pedidos recientes, el contenido del carro de compras, las revisiones de productos y las suscripciones al boletín informativo.

![Perfil del cliente](assets/cust-profile.png){width="700" zoomable="yes"}

## Editar una cuenta de cliente

Método 1: **_edición rápida_**

1. En la primera columna, seleccione la casilla de verificación de la cuenta de cliente que desea editar.

1. Establezca la columna **[!UICONTROL Actions]** en `Edit`.

   >[!INFO]
   >
   >El valor de cada valor que se puede actualizar aparece en un cuadro de texto. Sólo algunos valores del registro de cliente seleccionado pueden editarse desde la cuadrícula.

   ![Edición rápida](assets/customers-grid-quick-edit.png){width="700" zoomable="yes"}

1. Actualice cualquiera de los siguientes valores, según sea necesario:

   * **[!UICONTROL Email]**
   * **[!UICONTROL Web Site]**
   * **[!UICONTROL Tax/VAT Number]**
   * **[!UICONTROL Gender]**

1. Haga clic en **[!UICONTROL Save]**.

Método 2: **_edición completa_**

1. En la cuadrícula, busque el registro de cliente que desea editar.

1. En la columna _Acciones_ del extremo derecho, haga clic en **[!UICONTROL Edit]**.

1. Realice los cambios necesarios en la información de la compañía.

   >[!INFO]
   >
   >Para obtener más información, consulte [Actualizar el perfil de un cliente](../customers/update-account.md).

1. Una vez finalizado, haga clic en **[!UICONTROL Save Customer]**.

>[!INFO]
>
>Si desea deshacer todas las ediciones antes de guardar, haga clic en **[!UICONTROL Reset]** en la barra de botones superior para devolver todos los cambios a la última versión guardada.

## Información del cliente

### [!UICONTROL Customer View]

La ficha _Vista del cliente_ muestra información sobre el cliente, que incluye **[!UICONTROL Personal Information]**, **[!UICONTROL Reward Points Balance]** y **[!UICONTROL Store Credit Balance]**.

### [!UICONTROL Account Information]

La pestaña [Información de la cuenta](../customers/account-dashboard-account-information.md) proporciona información detallada sobre el cliente, donde un usuario administrador puede editar la información personal, el correo electrónico, la asistencia de compras remotas, la fecha de nacimiento y adjuntar al cliente a un sitio web o compañía.

### [!UICONTROL Addresses]

La ficha [Direcciones](../customers/account-dashboard-address-book.md) contiene las direcciones de facturación y envío predeterminadas del cliente, así como las direcciones adicionales que utilice con frecuencia.

### [!UICONTROL Orders]

La cuadrícula [Pedidos](../stores-purchase/orders.md) contiene una lista de todos los pedidos actuales de los clientes, el administrador puede realizar un seguimiento de su progreso.

### [!UICONTROL Returns]

{{ee-feature}}

La ficha [Devuelve](../stores-purchase/returns.md) enumera las solicitudes de cliente devueltas actualmente.

### [!UICONTROL Shopping cart]

La ficha [carro de compras](../stores-purchase/cart.md) muestra los productos que se encuentran actualmente en el carro de compras, pero por alguna razón la compra no se completó.

### [!UICONTROL Wish List]

Una [lista de artículos deseados](../stores-purchase/wishlists.md) muestra una lista de productos que un cliente puede transferir al carro de compras más tarde.

### [!UICONTROL Gift Registry]

{{ee-feature}}

La sección [Registro de regalos](../merchandising-promotions/gift-registry-storefront.md) enumera los registros de regalos actuales del cliente y el evento asociado.


### [!UICONTROL Store Credit]

{{ee-feature}}

La pestaña [Crédito de tienda](../customers/store-credit.md) muestra una cantidad que se restaura en una cuenta de cliente; el administrador puede administrar este valor.

### [!UICONTROL Newsletter]

La pestaña [Newsletter](../merchandising-promotions/newsletters.md) muestra todos los correos electrónicos enviados al cliente actual.

### [!UICONTROL Billing Agreements]

La pestaña [Acuerdos de facturación](../stores-purchase/paypal-billing-agreements.md) enumera todos los acuerdos de facturación de PayPal entre la tienda y el cliente.

### [!UICONTROL Product Reviews]

La ficha [Críticas de productos](../catalog/settings-advanced-product-reviews.md) muestra todas las críticas enviadas por este cliente.

### [!UICONTROL Reward Points]

{{ee-feature}}

La sección [Puntos de recompensa](../merchandising-promotions/rewards-loyalty.md) muestra el saldo actual de puntos de recompensa del cliente. Un usuario administrador puede administrar este valor.

## Barra de botones

| Botón | Descripción |
|----------|--------------|
| **[!UICONTROL Back]** | Vuelve a la página Clientes sin guardar los cambios. |
| **[!UICONTROL Login as Customer]** | Permite que el comerciante inicie sesión como cliente. |
| **[!UICONTROL Delete Customer]** | Elimina la cuenta del cliente. |
| **[!UICONTROL Reset]** | Restablece los cambios no guardados en el formulario del cliente a sus valores anteriores. |
| **[!UICONTROL Create Order]** | [Crea un pedido](../stores-purchase/customer-account-create-order.md) asociado a la cuenta de cliente. |
| **[!UICONTROL Reset Password]** | Restablece la contraseña del cliente. |
| **[!UICONTROL Force Sign-In]** | Borra los tokens asociados con la contraseña del cliente y proporciona al administrador acceso a la cuenta. |
| **[!UICONTROL Manage Shopping Cart]** | Proporciona acceso al carro de compras de un cliente. |
| **[!UICONTROL Save and Continue Edit]** | Guarda los cambios y mantiene abierta la cuenta del cliente. |
| **[!UICONTROL Save Customer]** | Guarda los cambios y cierra la cuenta del cliente. |

{style="table-layout:auto"}
