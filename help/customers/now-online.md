---
title: Los clientes ahora en línea
description: La opción _Ahora en línea_ de la [!UICONTROL Customers ]El menú enumera todos los clientes y visitantes que están en línea actualmente en su tienda.
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# Los clientes ahora en línea

El **[!UICONTROL Now Online]** opción en la [!DNL Customers] El menú enumera todos los clientes y visitantes que están en línea actualmente en su tienda. El intervalo de tiempo que los clientes se muestran como actualmente en línea se establece en la configuración de y determina cuánto tiempo dura el [!DNL Customer's] La actividad es visible desde el Administrador. De forma predeterminada, el intervalo es de 15 minutos. La sesión finaliza si el teclado no se utiliza durante este tiempo y los clientes deben volver a iniciar sesión en sus cuentas para seguir comprando. Es importante tener en cuenta que el contenido de los carros de compras se guarda para su acceso posterior.

![Clientes en línea](assets/customers-now-online.png){width="700" zoomable="yes"}

El estado en línea de los clientes solo se actualiza tras el inicio de sesión del cliente, el registro o cualquier otro evento de cambio de estado. Incluye eventos relacionados con el carro de compras, como añadir, eliminar y modificar productos.

>[!NOTE]
>
>Las visitas a la página por sí solas no actualizan el estado en línea del cliente. Para recopilar dicha información, se recomienda [configuración de Google Analytics](../merchandising-promotions/google-analytics.md) (solo o con [Google Tag Manager](../merchandising-promotions/google-tag-manager.md)) o utilice otro software de análisis con Adobe Commerce.

## Ver todos los clientes actualmente en línea

En el _Administrador_ barra lateral, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Online Now]**.

>[!TIP]
>
>Para obtener información sobre cómo ayudar a un cliente en línea a realizar una compra, consulte [Asistencia de compras](../stores-purchase/introduction.md#shopping-assistance).

## Configuración del intervalo de tiempo

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Customer Configuration]**.

1. Expanda el **[!UICONTROL Online Customers Options]** y haga lo siguiente:

   ![Opciones del cliente en línea](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - Para **[!UICONTROL Online Minutes Interval]**, introduzca el número de minutos para que la sesión del cliente sea visible desde el administrador. Deje el campo vacío para aceptar el intervalo predeterminado de 15 minutos.

   - Para **[!UICONTROL Customer Data Lifetime]**, introduzca el número de minutos antes de que caduquen los datos sin guardar introducidos por el cliente.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Descripciones de columna

| Columna | Descripción |
| --- | --- |
| **[!UICONTROL ID]** | El ID de cliente de un cliente registrado. |
| **[!UICONTROL First Name]** | El nombre de un cliente registrado. |
| **[!UICONTROL Last Name]** | El apellido de un cliente registrado. |
| **[!UICONTROL Email]** | La dirección de correo electrónico de un cliente registrado. |
| **[!UICONTROL Last Activity]** | La fecha y la hora de la última actividad del cliente en su tienda. |
| **[!UICONTROL Type]** | Opciones: `Customer` / `Visitor` |
| **[!UICONTROL Last URL]** | La última URL que visitó el cliente. |
| **[!UICONTROL Company]** | El nombre de la compañía a la que pertenece el usuario. |

{style="table-layout:auto"}
