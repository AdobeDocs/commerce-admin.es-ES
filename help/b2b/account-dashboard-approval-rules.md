---
title: Reglas de aprobación de pedidos de compra
description: Obtenga información acerca de las reglas de aprobación de pedidos de compra y cómo los administradores de la compañía pueden definirlas en la tienda.
exl-id: e8d8bbc9-41cf-4024-85cc-92f0b0ce32d6
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# Reglas de aprobación de pedidos de compra

La mayoría de las empresas requieren la aprobación de pedidos para los pedidos de compra. Al agregar reglas de aprobación para su cuenta de compañía, pueden controlar quién puede crear pedidos de compra y cuánto pueden gastar. Por ejemplo:

* Cualquier pedido de compra inferior al valor X se aprueba automáticamente.
* Los pedidos superiores al valor X pero inferiores a Q deben ser aprobados por Y.
* Cualquier valor de PO sobre X debe ser aprobado por Y y Z.
* Se aprueba automáticamente un pedido creado por cualquier persona a nivel de Director o superior.

Según la función de la compañía y los permisos, los usuarios pueden crear, editar, eliminar o ver reglas de aprobación.

>[!IMPORTANT]
>
>La configuración de reglas de aprobación requiere un definido [estructura de la empresa](account-company-structure.md) para especificar la aprobación por parte del gestor del cliente comprador.

## Métodos de pago

Los flujos de aprobación de pedidos de compra admiten métodos de pago en línea y sin conexión. Todos los métodos de pago sin conexión predeterminados son compatibles con las aprobaciones de pedidos de compra. Para los pagos en línea, se admiten los siguientes métodos:

* PayPal Express
* pagos de Braintree


## Configuración de regla de aprobación

Con el requerido [permisos para su función](account-company-roles-permissions.md), los clientes B2B pueden configurar reglas de aprobación para aplicar directivas de compañía haciendo clic en **[!UICONTROL Approval Rules]** en el panel izquierdo de su cuenta de cliente.

![Reglas de aprobación de empresa](./assets/approval-rules.png){width="700" zoomable="yes"}

Para crear una regla de aprobación, un cliente completa los siguientes pasos:

1. Clics **[!UICONTROL Add New Rule]** para crear una regla.

1. Si es necesario, cambia la regla de **[!UICONTROL Enabled]** hasta **[!UICONTROL Disabled]**.

   La regla está tan habilitada como la predeterminada, pero un cliente puede crear la regla con una configuración deshabilitada y luego habilitarla más tarde cuando esté listo para aplicarla.

1. Para **[!UICONTROL Rule name]**, introduce un nombre corto pero descriptivo para la regla, como `Orders less than $100`.

   Los nombres de las reglas deben ser únicos.

1. Para **[!UICONTROL Description]**, introduce una explicación más larga de la regla.

1. Para **[!UICONTROL Applies to]**, elige uno o varios roles de compañía utilizados para aplicar la regla.

1. Elige el **[!UICONTROL Rule Type]** y define la regla.

   Las secciones siguientes proporcionan una explicación detallada y un ejemplo para cada tipo de regla.

   ![Creación de una nueva regla de aprobación](./assets/approval-rules-create.png){width="700" zoomable="yes"}

1. Para **[!UICONTROL Requires approval from]**, elige uno o varios aprobadores necesarios según el tipo de aprobación.

   >[!NOTE]
   >
   >* Al asignar una función como aprobador, asegúrese de que haya al menos un usuario en esa función.
   >* Si hay dos o más usuarios con la misma función de aprobador, el creador de la orden de compra no puede aprobarla. En este caso, cualquier otro usuario con esta función de aprobador requiere la aprobación manual. Sin embargo, si `Auto-approve POs created within this role` se configura en la variable [Permisos de roles](account-company-roles-permissions.md), el pedido de compra se aprueba automáticamente.
   >* Si solo hay un usuario con la función de aprobador y ese usuario es el creador, la orden de compra siempre se aprueba automáticamente: `Auto-approve POs created within this role` se omite la configuración de permisos.

1. Haga clic **[!UICONTROL Save]**.

### [!UICONTROL Order Total]

Este tipo de regla se utiliza para requerir una aprobación de pedido de compra basada en el total del pedido, incluidos los impuestos.

1. Elige un **[!UICONTROL Order Total amount]** opción:

   * `is more than`
   * `is less than`
   * `is more than or equal to`
   * `is less than or equal to`

1. Selecciona el tipo de divisa e introduce el importe.

![Regla de aprobación total del pedido](./assets/approval-rules-order-total.png){width="600" zoomable="yes"}

### [!UICONTROL Shipping Cost]

Este tipo de regla se utiliza para requerir una aprobación de pedido de compra basada en los costes de envío, que muchas empresas necesitan.

1. Establece el **[!UICONTROL Shipping cost value]**:

   * `is more than`
   * `is less than`
   * `is more than or equal to`
   * `is less than or equal to`

1. Establece el importe de envío deseado.

![Regla de aprobación de gastos de envío](./assets/approval-rules-shipping-cost.png){width="600" zoomable="yes"}

### [!UICONTROL Number of SKUs]

Este tipo de regla se utiliza para requerir una aprobación de pedido en función del número de SKU o productos únicos del pedido. Controla el número de tipos de elementos distintos, no el número de elementos que se están ordenando. Por ejemplo, un pedido de compra podría incluir:

* Dos grandes camisas blancas
* Tres camisas blancas medianas

Este ejemplo especifica cinco elementos, pero dos SKU distintas.

1. Establece el **[!UICONTROL Number of SKUs]** valor:

   * `is more than`
   * `is less than`
   * `is more than or equal to`
   * `is less than or equal to`

1. Establece la cantidad de SKU.

![Número de reglas de aprobación de SKU](./assets/approval-rules-number-skus.png){width="600" zoomable="yes"}

## Editar reglas de aprobación

Para modificar una regla de aprobación existente, un cliente puede completar los siguientes pasos:

1. En la barra lateral de su cuenta, el cliente selecciona **[!UICONTROL Approval Rules]**.

1. Busca la entrada de regla de aprobación que se va a editar.

1. Clics **[!UICONTROL Edit]**.

1. Realiza todos los cambios y clics necesarios **[!UICONTROL Save]**.

## Eliminar reglas de aprobación

Para eliminar una regla de aprobación existente, un cliente puede completar los siguientes pasos:

1. En la barra lateral de su cuenta, selecciona **[!UICONTROL Approval Rules]**.

1. Busca la entrada de regla de aprobación que se va a eliminar.

1. Clics **[!UICONTROL Delete]**.

1. Para confirmar la acción, haga clic en **[!UICONTROL OK]**.

## Demostración de aprobaciones de pedidos de compra

Vea este vídeo para obtener más información sobre las aprobaciones de pedidos de compra:

>[!VIDEO](https://video.tv.adobe.com/v/344450?quality=12)
