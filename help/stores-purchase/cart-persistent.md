---
title: Persistencia del carro
description: Descubra cómo un carro de compras persistente rastrea artículos de carro de compras no comprados y guarda la información para la próxima visita del cliente.
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
source-git-commit: 2bddf979333bdafbfb6b445140515942b1115eea
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 0%

---

# Persistencia del carro

Un carro de compras persistente guarda una referencia a la cuenta del cliente en el dispositivo actual, lo que garantiza que el contenido del carro de compras permanezca accesible cuando caduque la sesión iniciada.

Si un cliente es _recordado_, el contenido de su carro de compras permanece accesible en el dispositivo actual cuando caduca la sesión iniciada. Una vez caducada la sesión, se accede al carro de compras del cliente mediante la sesión de carro persistente. Si el mismo cliente inicia sesión en otro dispositivo o explorador y agrega algo al carro de compras y, a continuación, vuelve al dispositivo con una sesión persistente activa, el carro de compras se actualiza con los elementos agregados.

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

Cuando caduca la sesión del cliente, aparece un vínculo `Not Jane Smith?` en el encabezado de la página en las siguientes condiciones:
- el cliente que inició sesión ha seleccionado la opción _[!UICONTROL Remember Me]_y se aplica una cookie persistente
- el cliente cierra la sesión cuando el sistema está configurado con _[!UICONTROL Clear Persistence on Sign Out]_establecido en `No`.

El sistema conserva un registro del contenido del carro de compras en el dispositivo actual, incluso si caduca la sesión iniciada. El vínculo `Not Jane Smith?` permite al cliente finalizar la sesión persistente y comenzar a trabajar como invitado, o iniciar sesión como un cliente diferente o igual.

Si el cliente marcó la casilla de verificación _[!UICONTROL Remember Me]_al iniciar sesión, su tienda crea y mantiene una cookie persistente independiente. Esta cookie ayuda a mantener accesible el carro de compras del cliente incluso después de que cierre el explorador o navegue a un sitio diferente y de que caduque su sesión iniciada.

Si este mismo cliente visita su tienda con varios navegadores mientras está conectado o mientras una sesión persistente está activa, los cambios que el cliente haga en el contenido del carro de compras en un navegador se reflejarán en otros navegadores cuando se actualice la página.

>[!NOTE]
>
>Para garantizar la sincronización del carro de compras en varios dispositivos o exploradores, los clientes deben iniciar sesión en cada dispositivo nuevo que utilicen para realizar compras. Para los clientes que iniciaron sesión, el contenido del carro de compras se sincroniza en varios dispositivos y exploradores siempre y cuando inicien sesión en la misma cuenta, independientemente de la configuración del carro de compras persistente.

### Comportamiento de la casilla &quot;Recordarme&quot;

Los clientes pueden seleccionar la casilla de verificación _[!UICONTROL Remember Me]_en la página de inicio de sesión o al crear una cuenta nueva para mantener el contenido del carro de compras accesible en el dispositivo actual cuando caduca la sesión iniciada.

| ¿Me Recuerdas? | Resultado |
| ------------ |  ------ |
| Seleccionado | Crea una cookie persistente y mantiene el contenido del carro de compras accesible en el dispositivo actual cuando caduca la sesión de inicio de sesión del cliente. |
| No seleccionado | No crea una cookie persistente y no mantiene el contenido del carro de compras accesible en el dispositivo actual cuando caduca la sesión de inicio de sesión. Tenga en cuenta que el contenido del carro de compras aún se guarda en la cuenta del cliente y se vuelve a cargar la próxima vez que el cliente inicia sesión. |

{style="table-layout:auto"}

### Borrar la persistencia al cerrar la sesión

Cuando el cliente inicia sesión o se registra con la opción _Recordarme_ seleccionada, la configuración de la opción _Borrar persistencia al cerrar la sesión_ determina el comportamiento del carro de compras persistente.

|  | Borrar persistencia al cerrar la sesión establecida en Sí | Borrar persistencia al cerrar la sesión establecida en No |
| ------ | ------ | ------ |
| _Recordado_ cliente cierra sesión | Elimina las cookies de sesión y las persistentes de modo que el contenido del carro de compras desaparezca en el dispositivo actual hasta que el mismo cliente vuelva a iniciar sesión. | Elimina la cookie de sesión, pero la cookie persistente permanece en vigor. El contenido del carro de compras permanece accesible en el dispositivo actual. |
| _Recordado_ cliente no cierra sesión pero la cookie de sesión caduca | La cookie persistente permanece en vigor y el contenido del carro de compras es accesible desde el dispositivo actual. | La cookie persistente permanece en vigor y el contenido del carro de compras es accesible desde el dispositivo actual. |

### Ejemplo de una sesión abierta en un equipo compartido

Jane está terminando sus compras de vacaciones como _recordada_ que inició sesión como cliente. Añade un regalo para John a su carrito y algo para su madre. Luego, va a la cocina a tomar un aperitivo y su sesión de inicio de sesión caduca.

John se sienta en la computadora a hacer algunas compras rápidas mientras Jane está en la cocina. Sin fijarse en el vínculo `Not Jane Smith?` de la parte superior de la página, John encuentra un bonito regalo para Jane y lo agrega al carro de compras. Cuando cierra la compra, observa que las direcciones de envío y facturación están rellenadas previamente y piensa que ha iniciado sesión. John tiene tanta prisa que no se da cuenta de los elementos adicionales durante _Revisión de pedidos_ y envía el pedido. El carro de Jane está ahora vacío, y John compró todos los regalos.

## Configuración de un carro de compras persistente

Durante la configuración de un carro de compras persistente, puede especificar la duración de las cookies y qué opciones desea poner a disposición de diversas actividades de los clientes.

Para utilizar el carro de compras persistente, el explorador del cliente debe estar configurado para permitir cookies. Existen dos tipos de cookies que se utilizan para las operaciones del carro de compras:

- **Cookie de sesión**: existe una cookie de sesión a corto plazo durante una sola visita al sitio. Esta cookie caduca cuando el cliente cierra la sesión o cuando caduca la sesión.

- **Cookie persistente**: una cookie persistente a largo plazo continúa existiendo después de que finalice la sesión iniciada. Esta cookie garantiza que el contenido del carro de compras de un cliente permanezca accesible cuando el cliente cierre la sesión o esta caduque.

Para obtener más información sobre cómo afectan estas opciones de configuración al flujo de trabajo del cliente, consulte [Flujo de trabajo persistente del carro de compras](#persistent-cart-workflow).

{{$include /help/_includes/persistent-cart-configuration.md}}
