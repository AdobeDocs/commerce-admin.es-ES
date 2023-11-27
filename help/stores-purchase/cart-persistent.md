---
title: Persistencia del carro
description: Descubra cómo un carro de compras persistente rastrea artículos de carro de compras no comprados y guarda la información para la próxima visita del cliente.
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
source-git-commit: 26d4bb35c6e1878a8ea8c5f05a982559e5d6dc35
workflow-type: tm+mt
source-wordcount: '1473'
ht-degree: 0%

---

# Persistencia del carro

Un carro de compras persistente realiza un seguimiento de los artículos no comprados que quedan en el carro y guarda la información para la siguiente visita del cliente. Clientes que son _recordado_ pueden restaurar el contenido de sus carros de compras la próxima vez que visiten su tienda.

El uso de un carro de compras persistente puede ayudar a reducir el número de carros de compras abandonados y aumentar las ventas. Es importante comprender que el carro de compras persistente no expone la información confidencial de la cuenta en ningún momento. Mientras el carro de compras persistente está en uso, tanto los clientes registrados como los compradores invitados deben iniciar sesión en una cuenta existente o crear una cuenta antes de pasar por el proceso de pago. Para los compradores invitados, un carro de compras persistente es la única manera de recuperar información de una sesión anterior.

Para administrar el uso de la persistencia del carro de compras en el sitio o en vistas de tiendas específicas, puede [configurar carro de compras persistente](#configure-a-persistent-cart) configuración. Para obtener más información sobre cómo afectan estos ajustes a la experiencia del comprador en su tienda, consulte [Flujo de trabajo de carro persistente](#persistent-cart-workflow).

>[!NOTE]
>
>Cuando se utiliza un carro de compras persistente, se recomienda establecer la duración de la sesión del servidor y la cookie de sesión en un período de tiempo largo. Consulte [Duración de sesión](../customers/customer-online-options.md) para obtener más información.

Para utilizar el carro de compras persistente, el explorador del cliente debe estar configurado para permitir cookies. Existen dos tipos de cookies que se utilizan para las operaciones del carro de compras:

- **Cookie de sesión** : existe una cookie de sesión a corto plazo durante una sola visita al sitio y caduca cuando el cliente se marcha o después de un período de tiempo establecido.

- **Cookie persistente** - Una cookie persistente a largo plazo sigue existiendo después del final de la sesión y guarda un registro del contenido del carro de compras del cliente para referencia futura.

## Flujo de trabajo de carro persistente

Cuando el carro de compras persistente esté [activado](#configure-a-persistent-cart), el flujo de trabajo depende de:

- Los valores del _Activar Recordar mis datos_ y _Borrar persistencia al cerrar la sesión_ configuración
- La decisión del cliente de seleccionar o borrar la _Recordar mis datos_ casilla de verificación
- Cuando se borra la cookie persistente

Cuando se aplica una cookie persistente, `Not Jane Smith?` El vínculo aparece en el encabezado de la página. Este mensaje permite al cliente finalizar la sesión persistente y comenzar a trabajar como invitado o iniciar sesión como otro cliente. El sistema conserva un registro del contenido del carro de compras, incluso si el cliente utiliza posteriormente distintos dispositivos para realizar compras en su tienda. Por ejemplo, un cliente puede agregar un artículo al carro de compras desde un equipo portátil, agregar más artículos desde un dispositivo móvil y completar el proceso de cierre de compra desde una tableta.

Existe una cookie persistente independiente independiente independiente independiente para cada explorador. Si el cliente utiliza varios exploradores mientras visita su tienda durante una sola sesión persistente, los cambios realizados en un explorador se reflejarán en cualquier otro al actualizar la página. Mientras que el carro de compras persistente está habilitado, su tienda crea y mantiene una cookie persistente independiente para cada navegador que un cliente utiliza para iniciar sesión o crear una cuenta.

### Ejemplo: una sesión abierta en un equipo compartido

Jane está terminando sus compras de vacaciones con una sesión persistente. Añade un regalo para John a su carrito y algo para su madre. Luego va a la cocina a tomar un aperitivo.

John se sienta en la computadora a hacer algunas compras rápidas mientras Jane está en la cocina. Sin tener en cuenta el `Not Jane Smith?` en la parte superior de la página, encuentra un bonito regalo para Jane y lo añade al carro de compras. Cuando va a pagar y inicia sesión como él mismo, ambos artículos en el carro de Jane se añaden a su carro de compras. John tiene tanta prisa que no se da cuenta de los elementos adicionales durante _Revisión del pedido_ y envía la solicitud. El carro de Jane está ahora vacío, y John compró todos los regalos.

### Recordar mis datos

Los clientes pueden seleccionar _Recordar mis datos_ en la página de inicio de sesión para guardar el contenido de sus carros de compras.

| ¿Me Recuerdas? | Resultado |
| ------------ |  ------ |
| Seleccionado | Crea una cookie persistente y guarda el contenido del carro de compras para la siguiente sesión iniciada por el cliente. |
| No seleccionado | No crea una cookie persistente y no guarda la información del carro de compras para la siguiente sesión iniciada por el cliente. |

{style="table-layout:auto"}

### Continuar persistencia al cerrar la sesión: no

| Acción | Resultado |
| ------ | ------ |
| El cliente inicia sesión | Invoca la cookie persistente además de la cookie de sesión, que ya se está utilizando. |
| El cliente cierra sesión | Elimina la cookie de sesión, pero la cookie persistente permanece en vigor. La próxima vez que el cliente inicia sesión, restaura los elementos del carro de compras o los agrega a cualquier elemento nuevo colocado en el carro de compras. |
| El cliente no cierra la sesión y la cookie de sesión caduca | La cookie persistente permanece en vigor. |

{style="table-layout:auto"}

### Borrar persistencia al cerrar la sesión

| Acción | Resultado |
| ------ | ------ |
| El cliente inicia sesión | Invoca la cookie persistente además de la cookie de sesión, que ya se está utilizando. |
| El cliente cierra sesión | Elimina ambas cookies. |
| El cliente no cierra la sesión, pero la cookie de sesión caduca | La cookie persistente permanece en vigor. |

{style="table-layout:auto"}

## Ajustes y efectos del carro de compras persistente

| Configuración | Efecto |
|----------|--------|
| **[!UICONTROL Enable Remember Me]** se establece en `No`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**tiene cualquier valor.<br/><br/>El** Recordar mis datos **La casilla de verificación no está disponible en la página de inicio de sesión y registro. | No se utiliza la cookie persistente. |
| **[!UICONTROL Enable Remember Me]** se establece en `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**tiene cualquier valor.<br/><br/>** Recordar mis datos **no está seleccionado. | La cookie de sesión se aplica de la forma habitual; no se utiliza la cookie persistente. |
| **[!UICONTROL Enable Remember Me]** se establece en `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**se establece en `Yes`.<br/><br/>** Recordar mis datos **se establece en `Yes`. | Cuando un cliente inicia sesión, se aplican ambas cookies. Cuando un cliente cierra la sesión, ambas cookies se eliminan. Si un cliente no inicia sesión pero la cookie de sesión caduca, se seguirá utilizando la cookie persistente. Además de cerrar la sesión, la cookie persistente se elimina cuando se agota su duración o cuando el cliente hace clic en `Not Jane Smith` vínculo. |
| **[!UICONTROL Enable Remember Me]** se establece en `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**se establece en `No`.<br/><br/>** Recordar mis datos **se establece en `Yes` | Cuando un cliente inicia sesión, se aplican ambas cookies. Cuando un cliente cierra la sesión, se elimina la cookie de sesión y la sesión persistente continúa. La cookie persistente se elimina cuando se agota su duración o cuando el cliente hace clic en el `Not Jane Smith` vínculo. |

{style="table-layout:auto"}

## Configuración de un carro de compras persistente

Durante la configuración de un carro de compras persistente, puede especificar la duración de las cookies y qué opciones desea poner a disposición de diversas actividades de los clientes.

Para obtener más información sobre cómo el flujo de trabajo del cliente está determinado por esta configuración, consulte [Flujo de trabajo de carro persistente](#persistent-cart-workflow).

>[!NOTE]
>
>Si la cookie de sesión caduca mientras el cliente ha iniciado sesión, la cookie persistente permanece activa.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Persistent Shopping Cart]**.

1. Para habilitar el carro de compras persistente y mostrar opciones adicionales, establezca **[!UICONTROL Enable Persistence]** hasta `Yes`.

   ![Activación y configuración de la persistencia del carro de compras](../configuration-reference/customers/assets/persistent-shopping-cart-general.png){width="600" zoomable="yes"}

   Para obtener más información sobre cada una de estas opciones de configuración, consulte la [_Referencia de configuración_](../configuration-reference/customers/persistent-shopping-cart.md)

   >[!NOTE]
   >
   >Si es necesario, borre la **[!UICONTROL Use system value]** para modificar esta configuración.

1. Para **[!UICONTROL Persistence Lifetime (seconds)]**, introduzca el tiempo, en segundos, que desea que dure la cookie persistente.

   El valor predeterminado de 31 536 000 segundos es igual a un año. El tiempo máximo permitido es de 100 años.

1. Establecer **[!UICONTROL Enable "Remember Me"]** a uno de los siguientes:

   - `Yes` - Muestra el _Recordar mis datos_ en la página de inicio de sesión de la tienda, para que los clientes puedan elegir guardar la información del carro de compras.

   - `No` : la persistencia se puede seguir habilitando, pero los clientes no tienen la opción de elegir si desean guardar su información.

1. Para preseleccionar _Recordar mis datos_ casilla de verificación para el cliente, establecer **[!UICONTROL Remember Me Default Value]** hasta `Yes`.

   El cliente puede desactivar esta opción si así lo desea.

1. Establecer **[!UICONTROL Clear Persistence on Log Out]** a uno de los siguientes:

   - `Yes` : el carro de compras se borra cuando un cliente registrado cierra la sesión.

   - `No` : el carro de compras se guarda cuando un cliente registrado cierra la sesión.

   >[!NOTE]
   >
   >Si la cookie de sesión caduca mientras el cliente sigue conectado, la cookie persistente permanece en uso.

1. Establecer **[!UICONTROL Persist Shopping Cart]** a uno de los siguientes:

   - `Yes` : Si caduca la cookie de sesión, se conservará la cookie persistente. Si más tarde un comprador invitado inicia sesión o crea una cuenta, se restaura el carro de compras.

   - `No` : el carro de compras no se conserva para los invitados una vez caducada la cookie de sesión.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Definir **[!UICONTROL Persist Wish List]** para determinar si el estado de las listas de deseos del cliente se conserva al finalizar la sesión:

   - `Yes` - El contenido de la lista de deseos se guarda al finalizar la sesión.

   - `No` - La lista de deseos no se guarda al finalizar la sesión.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Definir **[!UICONTROL Persist Recently Ordered Items]** para determinar si el estado de los artículos pedidos recientemente se conserva al finalizar la sesión:

   - `Yes` - El estado de los artículos pedidos recientemente se guarda al finalizar la sesión.

   - `No` - El estado de los artículos pedidos recientemente no se guarda al finalizar la sesión.

1. Establecer **[!UICONTROL Persist Currently Compared Products]** hasta `Yes` o `No`.

1. Establecer **[!UICONTROL Persist Comparison History]** hasta `Yes` o `No`.

1. Establecer **[!UICONTROL Persist Recently Viewed Products]** hasta `Yes` o `No`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Definir **[!UICONTROL Persist Customer Group Membership and Segmentation]** para determinar si se conserva el estado de los criterios de segmentación y pertenencia a grupos del cliente cuando finaliza la sesión:

   - `Yes` : el estado de los datos de segmentación y pertenencia a grupos del cliente se guarda cuando finaliza la sesión.

   - `No` : el estado de los datos de segmentación y pertenencia a grupos del cliente no se guarda al finalizar la sesión.

1. Haga clic **[!UICONTROL Save Config]**.
