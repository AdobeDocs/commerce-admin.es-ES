---
title: Devuelve la experiencia de tienda
description: Descubra cómo sus clientes pueden administrar las devoluciones de sus productos desde su cuenta en la tienda.
exl-id: c276ca2c-3d8b-4019-a9aa-e7631080f331
feature: Returns, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# Devuelve la experiencia de tienda

{{ee-feature}}

Los clientes pueden utilizar cualquiera de las siguientes opciones para solicitar una autorización de devolución de material a la tienda:

- [Widget de pedidos y devoluciones](../content-design/widget-orders-returns.md) en la barra lateral
- _Pedidos y devoluciones_ vínculo en pie de página

Como práctica recomendada, asegúrese de incluir una descripción de los requisitos y el proceso de la RMA en la política de servicio al cliente.

>[!NOTE]
>
>Si desea recopilar información adicional relacionada con las devoluciones, puede agregar sus propios atributos personalizados [returns](attributes-returns.md).

Toda la información de RMA del cliente se muestra en la página **[!UICONTROL My Returns]** del panel de cuentas del cliente.

![Mis devoluciones](./assets/my-returns-page.png){width="700" zoomable="yes"}

## Solicitar una autorización de devolución

El cliente completa los siguientes pasos en la tienda para enviar una autorización de devolución de material:

1. En el pie de página, hace clic en **[!UICONTROL Orders and Returns]**.

1. Introduce la información del pedido:

   - ID de pedido
   - Apellido de facturación
   - Correo electrónico

1. Clics **[!UICONTROL Continue]**.

   ![Pedidos y devoluciones](./assets/storefront-orders-and-returns.png){width="700" zoomable="yes"}

1. Bajo la fecha de pedido, hace clic en **[!UICONTROL Return]**.

   ![Detalle del pedido](./assets/storefront-orders-and-returns-order-information.png){width="700" zoomable="yes"}

1. Elige el elemento que se va a devolver e introduce **[!UICONTROL Quantity to Return]**.

1. Establece **[!UICONTROL Resolution]** en una de las siguientes opciones:

   - Exchange
   - [Reembolso](../customers/refunds-customer-account.md)
   - [Crédito de tienda](../customers/store-credit-using.md)

1. Establece **[!UICONTROL Item Condition]** en una de las siguientes opciones:

   - `Unopened`
   - `Opened`
   - `Damaged`

1. Establece **[!UICONTROL Reason to Return]** en una de las siguientes opciones:

   - `Wrong Color`
   - `Wrong Size`
   - `Out of Service`
   - `Other`

   ![Crear nueva devolución](./assets/storefront-orders-and-returns-create-new-return.png){width="700" zoomable="yes"}

1. Si es necesario, establece **[!UICONTROL Contact Email Address]** y **[!UICONTROL Comments]**.

   >[!NOTE]
   >
   >Si el pedido contiene varios artículos y el cliente desea devolver otro, puede hacer clic en **[!UICONTROL Add Item To Return]**, seleccionar el artículo y establecer todas las opciones mencionadas.

1. Clics **[!UICONTROL Submit]**.
