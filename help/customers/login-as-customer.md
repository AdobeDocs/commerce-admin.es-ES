---
title: Proporcionar asistencia al comprador
description: Al utilizar la función Iniciar sesión como cliente, puede ver lo que ven los clientes y realizar actualizaciones en su nombre.
exl-id: 6842ae7a-6440-45f1-af18-e6427088d29d
feature: Customers, Customer Service
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Proporcionar asistencia al comprador

A veces, los clientes necesitan ayuda con su pedido. Los administradores de la tienda pueden usar _Iniciar sesión como cliente_, lo cual les permite ver lo que ve el cliente y hacer actualizaciones para ayudarles.

Cualquier acción realizada mientras se inició sesión como cliente se aplica a la cuenta del cliente real.

Cuando está habilitado para un usuario de _Admin_, el botón _[!UICONTROL Login as Customer]_aparece en varias páginas:

* [Página Editar cliente](../customers/update-account.md)
* [Página Vista de pedidos](../stores-purchase/order-processing.md)
* [Página Vista de Facturas](../stores-purchase/invoices.md)
* [Página Vista de Envío](../stores-purchase/shipments.md)
* [Página de visualización de nota de abono](../stores-purchase/credit-memo-create.md)

![Iniciar Sesión Como Cliente](assets/login-as-customer.png){width="600" zoomable="yes"}

## Habilitar inicio de sesión como cliente

Para habilitar _Iniciar sesión como cliente_, es necesario que habilite la característica en la instancia de Commerce y, a continuación, habilite el acceso para los usuarios administradores en los permisos de funciones de usuario.

### Habilitar la función

1. En la barra lateral de Administración, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Login as Customer]**.

   ![Opciones de configuración: iniciar sesión como cliente](../configuration-reference/customers/assets/login-as-customer.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Enable Login as Customer]** en `Yes`.

1. _(Opcional)_ Establezca **[!UICONTROL Disable Page Cache for Admin User]** en `No` para habilitar la caché de la página cuando el usuario administrador inicie sesión como cliente.

   >[!WARNING]
   >
   > Al deshabilitar la caché de la página (`Yes` - predeterminado) se garantiza que el usuario que inicia sesión como cliente obtenga datos nuevos y sin almacenar en caché.

1. _(Opcional)_ Establezca **[!UICONTROL Store View to Log in]** en `Manual Selection` si tiene una configuración de varios sitios o tiendas y desea que el usuario administrador seleccione la vista de la tienda al iniciar sesión como cliente.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

### Habilitar acceso para usuarios administradores

1. En la barra lateral _Admin_, vaya a **[!UICONTROL System]** > _Permisos_ > **[!UICONTROL User Roles]**.

1. Haga clic en el rol de la lista.

1. En el panel izquierdo de [!UICONTROL _Información de la función_], haga clic en **[!UICONTROL Role Resources]**.

1. Cambiar **[!UICONTROL Role Resources]** en la página a `Custom`.

   >[!INFO]
   >
   > Con esta opción seleccionada, la jerarquía de recursos se muestra en la página.

1. Desplácese hasta el elemento principal **[!UICONTROL Customers]** y el elemento **[!UICONTROL Login as Customer]** inferior. A continuación, seleccione los recursos que desea habilitar para la función:

   * **[!UICONTROL Allow Login as Customer]**: permite al usuario administrador usar la función _Iniciar sesión como cliente_.
   * **[!UICONTROL View Login as Customer Log]** - Permite al usuario administrador ver el registro de _Iniciar sesión como cliente_.

   ![Recursos de rol - Iniciar sesión como cliente](assets/customers-login-as-customer-role-resources.png){width="400" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save Role]**.

## Inicie sesión como cliente desde el administrador

1. En la barra lateral de _Administración_, vaya a **[!UICONTROL Customers]** > [!UICONTROL _Todos los clientes_].

1. Abra un usuario en modo de edición.

1. En el panel **[!UICONTROL Customer Information]**, elija la sección **[!UICONTROL Account Information]**.

1. Establezca **[!UICONTROL Allow remote shopping assistance]** en `Yes`.

   >[!INFO]
   >
   >El administrador ahora puede iniciar sesión como un usuario sin su permiso de la tienda.

## Permiso de cuenta de cliente para asistencia de compra remota

Para habilitar el acceso a la cuenta para el personal de asistencia técnica de la tienda desde el administrador, los clientes deben habilitar la siguiente función para su cuenta:

1. El cliente va a la página **[!UICONTROL Account Information]**.

1. Selecciona la casilla de verificación **[!UICONTROL Allow remote shopping assistance]**.

1. El cliente hace clic en **[!UICONTROL Save]**.

![Página de información de la cuenta](assets/permission.png){width="700" zoomable="yes"}

>[!WARNING]
>
>Sin este permiso, un usuario administrador no puede iniciar sesión como este cliente.

## Usar Iniciar sesión como cliente

>[!INFO]
>
>Para usar _Iniciar sesión como cliente_, asegúrese de que su administrador esté configurado tal como se describió anteriormente.

_Iniciar sesión como cliente_ le permite ver el sitio del mismo modo que lo hace el cliente, así como solucionar problemas y llevar a cabo otras acciones para el cliente. Si tiene una función de usuario asignada con los permisos necesarios:

1. Puede hacer clic en **[!UICONTROL Login as Customer]** en las páginas que aparecen en la sección anterior.
1. Las acciones Iniciar sesión como cliente están disponibles en el informe Acciones.

>[!WARNING]
>
>Cualquier acción realizada mientras se inició sesión [!UICONTROL _como cliente_] (como agregar o quitar productos) se aplica al pedido real del cliente. En la tienda, se mostrará un banner cuando usted sea `logged in as customer_name` para proporcionar un recordatorio del estado especial.

## Iniciar sesión como registro de cliente

{{ee-feature}}

Adobe Commerce proporciona un registro para las acciones _Iniciar sesión como cliente_. Enumera todas las sesiones en las que un usuario administrador accede a la función. Para acceder a las acciones registradas, vaya a [Informe de acciones de administración](../systems/action-log-report.md).

Puede filtrar la configuración del informe **[!UICONTROL Action Group]** a `Login As Customer` en la parte superior de la página y hacer clic en **[!UICONTROL Search]**.

![Filtrar el informe de acciones](assets/customers-login-as-customer-log-filter.png){width="700" zoomable="yes"}
