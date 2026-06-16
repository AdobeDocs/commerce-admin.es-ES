---
title: Devuelve la experiencia de tienda
description: Descubra cómo sus clientes pueden administrar las devoluciones de sus productos desde su cuenta en la tienda.
exl-id: c276ca2c-3d8b-4019-a9aa-e7631080f331
feature: Returns, Storefront
TQID: https://experienceleague.adobe.com/erAT7FtUSif5CxrBLlANMQY2aowkv0MDzkqXQnzzF7Q
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
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
source-wordcount: 208
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
