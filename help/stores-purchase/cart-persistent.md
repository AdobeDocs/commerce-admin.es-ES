---
title: Persistencia del carro
description: Descubra cómo un carro de compras persistente rastrea artículos de carro de compras no comprados y guarda la información para la próxima visita del cliente.
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
source-git-commit: a6cfcbb5774c0bafc3b7e7c96881329bde837837
workflow-type: tm+mt
source-wordcount: '1038'
ht-degree: 0%

---

# Persistencia del carro

Un carro de compras persistente guarda una referencia a la cuenta del cliente en el dispositivo actual, lo que garantiza que el contenido del carro de compras permanezca accesible cuando caduque la sesión iniciada.

Si se _recuerda_ a un cliente, el contenido de su carro de compras permanece accesible en el dispositivos actual cuando expira la sesión iniciada. Una vez caducada la sesión, se accede al carro de compras del cliente mediante la sesión de carro persistente. Si el mismo cliente inicia sesión en otro dispositivo o explorador y agrega algo al carro de compras y, a continuación, vuelve al dispositivo con una sesión persistente activa, el carro de compras se actualiza con los elementos agregados.

El uso de un carro de compras persistente puede reducir el número de carros de compras abandonados y aumentar las ventas. El carro de compras persistente **no** expone la información confidencial de la cuenta en ningún momento.

Para administrar el uso de la persistencia del carro de compras en el sitio o en vistas de tiendas específicas, puede [configurar la configuración del carro de compras persistente](#configure-a-persistent-cart). Para obtener más información sobre cómo afectan estos ajustes a la experiencia del comprador en su tienda, consulte [Flujo de trabajo persistente del carro de compras](#persistent-cart-workflow).

>[!NOTE]
>
>La función de carro de compras persistente solo está disponible para clientes registrados y conectados. Los compradores invitados no pueden utilizar la función de carro de compras persistente.

## Flujo de trabajo de carro persistente

Cuando el carro de compras persistente está [habilitado](#configure-a-persistent-cart), el flujo de trabajo depende de lo siguiente:

- Los valores de la configuración _[!UICONTROL Enable Remember Me]_y_[!UICONTROL Clear Persistence on Log Out]_
- La decisión del cliente de activar o desactivar la casilla de verificación _[!UICONTROL Remember Me]_
- Cuando se borra la cookie persistente

Cuando caduca la sesión del cliente, se muestra un `Not Jane Smith?` vincular en el encabezado del Página con las siguientes condiciones:
- El cliente conectado ha seleccionado la _[!UICONTROL Remember Me]_opción y se aplica un Cookies persistentes
- El cliente cierra la sesión cuando el sistema se configura con configurado como _[!UICONTROL Clear Persistence on Sign Out]_`No`.

El sistema conserva un registro del contenido del carro de compras en el dispositivos actual, igualado si caduca la sesión iniciada. El `Not Jane Smith?` vincular permite al cliente terminar la sesión persistente y inicio trabajando como invitado, o iniciar sesión como un cliente diferente o el mismo.

Si el cliente marcó la casilla de _[!UICONTROL Remember Me]_verificación al registro entrar, el tienda crea y mantiene un Cookies persistentes separado. Este cookie ayuda a mantener el carro de compras del cliente accesible igualado después de que cierre el explorador o navegue a un sitio diferente y su sesión de inicio de sesión expire.

Si este mismo cliente visita su tienda con varios navegadores mientras está conectado o mientras una sesión persistente está activa, los cambios que el cliente haga en el contenido del carro de compras en un navegador se reflejarán en otros navegadores cuando se actualice la página.

>[!NOTE]
>
>Para garantizar la sincronización del carro de compras en varios dispositivos o exploradores, los clientes deben iniciar sesión en cada dispositivo nuevo que utilicen para realizar compras. Para los clientes que iniciaron sesión, el contenido del carro de compras se sincroniza en varios dispositivos y exploradores siempre y cuando inicien sesión en la misma cuenta, independientemente de la configuración del carro de compras persistente.

### Comportamiento de la casilla de verificación &quot;Recordarme&quot;

Los clientes pueden seleccionar la _[!UICONTROL Remember Me]_casilla de verificación en la inicio de sesión Página, la ventana emergente de autenticación, los inicios de sesión de cierre de compra o al crear un nuevo cuenta para mantener el contenido del carro de compras accesible en el dispositivos actual cuando expire la sesión iniciada.

| ¿Recuérdame? | Resultado |
| ------------ |  ------ |
| Seleccionado | Crea una cookie persistente y mantiene el contenido del carro de compras accesible en el dispositivo actual cuando caduca la sesión de inicio de sesión del cliente. |
| No seleccionado | No crea una cookie persistente y no mantiene el contenido del carro de compras accesible en el dispositivo actual cuando caduca la sesión de inicio de sesión. Tenga en cuenta que el contenido del carro de compras aún se guarda en la cuenta del cliente y se vuelve a cargar la próxima vez que el cliente inicia sesión. |

{style="table-layout:auto"}

![Recordarme inicio de sesión de cliente](./assets/remember-me-customer-login.png){width="600" zoomable="yes"}
![Ventana emergente de autenticación Recordarme](./assets/remember-me-authentication-pop-up.png){width="600" zoomable="yes"}
![Recordar mis inicios de sesión para pagar](./assets/remember-me-checkout-sign-ins.png){width="600" zoomable="yes"}

### Borrar la persistencia al cerrar la sesión

Cuando el cliente inicia sesión o se registra con la opción _Recordarme_ seleccionada, la configuración de la opción _Borrar persistencia al cerrar la sesión_ determina el comportamiento del carro de compras persistente.

|  | Borrar persistencia al cerrar la sesión establecida en Sí | Borrar persistencia al cerrar la sesión establecida en No |
| ------ | ------ | ------ |
| _El cliente recordado_ cierra sesión | Elimina las cookies persistentes y de sesión para que el contenido carro de compras desaparezca en el dispositivos actual hasta que el mismo cliente vuelva a iniciar sesión. | Elimina el cookie de sesión, pero el Cookies persistentes sigue vigente. La contenido carro de compras permanece accesible en el dispositivos actual. |
| _El cliente recordado_ no cierra la sesión, pero el cookie de la sesión caduca | La cookie persistente permanece en vigor y el contenido del carro de compras es accesible desde el dispositivo actual. | La cookie persistente permanece en vigor y el contenido del carro de compras es accesible desde el dispositivo actual. |

### Ejemplo de una sesión abierta en un equipo compartido

Jane está terminando sus compras de vacaciones como _recordada_ que inició sesión como cliente. Ella agrega un regalo para John a su carro de compras, y algo para su madre. Luego, va a la cocina a tomar un refrigerio y su sesión de inicio de sesión expira.

John se sienta frente a la computadora para hacer algunas compras rápidas mientras Jane está en la cocina. Sin darse cuenta de la `Not Jane Smith?` vincular en la parte superior de la Página, John encuentra un buen regalo para Jane y lo agrega al carro de compras. Cuando se retira, se da cuenta de que las direcciones de envío y facturación están precargadas y piensa que ha iniciado sesión. John tiene tanta prisa que no se da cuenta de los elementos adicionales durante _Revisión de pedidos_ y envía el pedido. El carro de Jane está ahora vacío, y John compró todos los regalos.

## Configuración de un carro de compras persistente

Durante la configuración de un carro de compras persistente, puede especificar la duración de las cookies y qué opciones desea poner a disposición de diversas actividades de los clientes.

Para utilizar el carro de compras persistente, el explorador del cliente debe estar configurado para permitir cookies. Existen dos tipos de cookies que se utilizan para las operaciones del carro de compras:

- **Cookie de sesión**: existe una cookie de sesión a corto plazo durante una sola visita al sitio. Este cookie caduca cuando el cliente cierra sesión o cuando caduca la sesión.

- **Cookie** persistente: una Cookies persistentes a largo plazo continúa existiendo después de que finaliza la sesión iniciada. Este cookie garantiza que el contenido del carro de compras de un cliente permanezca accesible cuando el cliente cierre la sesión o caduque la sesión.

Para obtener más información acerca de cómo afectan estas opciones de configuración al flujo de trabajo del cliente, consulte [flujo de trabajo de carro de compras persistentes](#persistent-cart-workflow).

{{$include /help/_includes/persistent-cart-configuration.md}}
