---
title: Los clientes ahora en línea
description: La opción _Ahora en línea_ del menú [!UICONTROL Customers &#x200B;]enumera todos los clientes y visitantes que están actualmente en línea en su tienda.
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
TQID: https://experienceleague.adobe.com/jtyDgy3jFmn0XymAYcpc2AOLLWSTDw-3OGkvG9a1SDc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 342
ht-degree: 0%

---

# Los clientes ahora en línea

La opción **[!UICONTROL Now Online]** del menú [!DNL Customers] enumera todos los clientes y visitantes que están en línea actualmente en su tienda. El intervalo de tiempo que los clientes se muestran como actualmente en línea se establece en la configuración y determina cuánto tiempo se puede ver la actividad [!DNL Customer's] desde el administrador. De forma predeterminada, el intervalo es de 15 minutos. La sesión finaliza si el teclado no se utiliza durante este tiempo y los clientes deben volver a iniciar sesión en sus cuentas para seguir comprando. Es importante tener en cuenta que el contenido de los carros de compras se guarda para su acceso posterior.

![Clientes en línea](assets/customers-now-online.png){width="700" zoomable="yes"}

El estado en línea de los clientes solo se actualiza tras el inicio de sesión del cliente, el registro o cualquier otro evento de cambio de estado. Incluye eventos relacionados con el carro de compras, como añadir, eliminar y modificar productos.

>[!NOTE]
>
>Las visitas a la página por sí solas no actualizan el estado en línea del cliente. Para recopilar esa información, se recomienda [configurar Google Analytics](../merchandising-promotions/google-analytics.md) (solo o con [Google Tag Manager](../merchandising-promotions/google-tag-manager.md)) o usar otro software de análisis con Adobe Commerce.

## Ver todos los clientes actualmente en línea

En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Online Now]**.

>[!TIP]
>
>Para obtener información sobre cómo ayudar a un cliente en línea a completar una compra, consulte [Asistencia para compras](../stores-purchase/introduction.md#shopping-assistance).

## Configuración del intervalo de tiempo

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Customer Configuration]**.

1. Expanda la sección **[!UICONTROL Online Customers Options]** y haga lo siguiente:

   ![Opciones de cliente en línea](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - Para **[!UICONTROL Online Minutes Interval]**, ingrese el número de minutos para que la sesión del cliente sea visible desde el administrador. Deje el campo vacío para aceptar el intervalo predeterminado de 15 minutos.

   - Para **[!UICONTROL Customer Data Lifetime]**, ingrese el número de minutos antes de que expiren los datos sin guardar ingresados por el cliente.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

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
