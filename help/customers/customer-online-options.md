---
title: Duración de sesión del cliente
description: La duración de la sesión del cliente determina la duración de una sesión de compra del cliente.
exl-id: 7180631a-3233-40f3-92bf-b329fc260cf9
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Duración de sesión del cliente

La duración de una sesión de compra de un cliente está determinada por varios factores, entre los que se incluyen la duración de la sesión del servidor, el uso de un [carro de compras persistente](../stores-purchase/cart-persistent.md) y la duración de la información almacenada en el explorador. Aunque están relacionados con la misma experiencia del cliente, son procesos independientes con diferentes eventos de caducidad y duraciones.

| Proceso | Descripción |
| --- | --- |
| Session | Información que se almacena en el servidor, como el contenido del carro de compras. Si la sesión del servidor caduca antes de que caduque la cookie, los clientes podrían perder el contenido del carro de compras y reducir el riesgo de seguridad. |
| Cookie de sesión | Información almacenada en el explorador como un número o una cadena de caracteres. Si la cookie de sesión caduca antes de la sesión del servidor, se cerrará la sesión del cliente. La cookie de sesión se elimina cuando el cliente cierra la ventana del explorador. De forma predeterminada, la duración de la cookie se establece en 3600 segundos o una hora. Si no hay actividad de teclado durante ese tiempo, la sesión actual finaliza y los clientes deben volver a iniciar sesión en sus cuentas para seguir comprando. |

{style="table-layout:auto"}

Si [Carro persistente](../stores-purchase/cart-persistent.md) está habilitado, el contenido del carro se guardará la próxima vez que los clientes inicien sesión en sus cuentas. Cuando se utiliza un carro de compras persistente, se recomienda establecer la duración de la sesión del servidor y la cookie de sesión en un período de tiempo largo.

En el servidor, la duración de la sesión está controlada por el archivo `php.ini` y varias variables. Actualmente, Adobe Commerce no tiene una configuración de administración que controle la duración de la sesión del servidor.

## Configuración de la duración de la cookie

1. En la barra lateral de _Admin_, vaya a [!UICONTROL **Tiendas**] > _[!UICONTROL Settings]_>[!UICONTROL **Configuración**].

1. Si tiene varias tiendas, establezca el selector **[!UICONTROL Store View]** en la esquina superior derecha, en la tienda donde se aplica la configuración.

1. En el panel izquierdo bajo **[!UICONTROL General]**, elija **[!UICONTROL Web]**.

1. Expanda la sección **[!UICONTROL Default Cookie Settings]**.

   ![Configuración de cookies predeterminada](../configuration-reference/general/assets/web-default-cookie-settings.png){width="600" zoomable="yes"}

1. Para cambiar el valor predeterminado, desactive la casilla de verificación **[!UICONTROL Use system value]** e introduzca el nuevo valor en segundos.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Configurar la funcionalidad de _Recordarme_

Para facilitar el inicio de sesión, la función **[!UICONTROL Remember Me]** permite a los titulares de cuentas de usuario evitar introducir sus credenciales cada vez que entran en la tienda. Por motivos de seguridad, la función de persistencia está desactivada de forma predeterminada.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Persistent Shopping Cart]**.

1. Expanda la sección **[!UICONTROL General Options]**.

1. Para **[!UICONTROL Enable Persistence]**, establecer en `Yes`. (Desactive la casilla de verificación **[!UICONTROL Use system value]** para poder cambiar la configuración predeterminada).

1. Para **[!UICONTROL Enable "Remember Me"]**, establézcalo en `Yes` o `No` según sus necesidades.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
