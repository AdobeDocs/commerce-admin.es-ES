---
title: Transferir una cuenta de Commerce
description: Aprenda a transferir su cuenta de Commerce a otro propietario o dirección de correo electrónico.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: a7b23834b00b2ae0f5fd98de47fdc6f4aa00c010
workflow-type: tm+mt
source-wordcount: '1196'
ht-degree: 0%

---

# Transferir una cuenta de Commerce

A medida que cambien las responsabilidades comerciales, es posible que tenga que transferir su cuenta de Commerce a un nuevo propietario o a otra dirección de correo electrónico. Esta transferencia requiere un cambio en el correo electrónico del usuario principal asociado a la cuenta.

La siguiente información describe el proceso para transferir una cuenta de Commerce (MAGEID). No incluye cambios para la propiedad de la cuenta de Cloud (proyecto en la nube o New Relic). Para obtener más información sobre el acceso a proyectos en la nube, consulte [Administrar el acceso de usuarios](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) en la _Guía de Commerce en infraestructura en la nube_.

>[!IMPORTANT]
>
>Si el nuevo propietario de la cuenta ha comprado extensiones utilizando el acceso compartido, el acceso a esas extensiones se pierde en cuanto se inicia el proceso de transferencia de cuenta. Antes de solicitar la transferencia de cuenta, asegúrese de que el nuevo propietario recupera los identificadores de pedido para las compras de [su cuenta de Marketplace](https://commercemarketplace.adobe.com/sales/order/history/) y solicita un reembolso por esas extensiones al [equipo de Marketplace](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case). No es posible transferir compras de extensión a una cuenta diferente.

## Identificación del tipo de transferencia

El tipo de transferencia de cuenta de Commerce depende de las credenciales de cuenta de Commerce disponibles para el propietario actual y el nuevo propietario. Los siguientes escenarios describen los diferentes tipos de transferencia en función de estas credenciales.

| Tipo de transferencia | Propietario actual | Nuevo propietario |
| ------------- | ------------- | --------- |
| [Nuevo cambio de Adobe ID y correo electrónico](#new-adobe-id-and-email-change) | Tiene un MAGEID que **_no se ha conectado_** a una cuenta de inicio de sesión de Adobe | No tiene un MAGEID y no está conectado a una cuenta de inicio de sesión de Adobe. |
| [Cambio de correo electrónico](#email-change) | Tiene un MAGEID **_conectado_** con una cuenta de inicio de sesión de Adobe. | Tiene una cuenta de inicio de sesión de Adobe, pero **_no tiene un MAGEID_** conectado a una cuenta de inicio de sesión de Adobe. |
| [Modificador de cuenta de Adobe ID](#adobe-id-account-switch) | Tiene un MAGEID **_conectado_** a una cuenta de inicio de sesión de Adobe. | Tiene un MAGEID y está conectado a una cuenta de inicio de sesión de Adobe. |

{style="table-layout:auto"}

>[!NOTE]
>
>A medida que Adobe Commerce continúa integrándose con otras soluciones de Adobe, una cuenta de Commerce (MAGEID) ahora requiere una asociación con un inicio de sesión de Adobe. Este Adobe ID utiliza la misma dirección de correo electrónico conectada a su cuenta de Commerce.

## Nuevo cambio de Adobe ID y correo electrónico

>[!IMPORTANT]
>
>Revise los [tipos de transferencia](#identify-your-transfer-type) y asegúrese de cumplir las condiciones previas de esta secuencia de pasos.

Este tipo de transferencia requiere tener un Adobe ID vinculado a la cuenta de Commerce existente y, a continuación, cambiar esa cuenta a la dirección de correo electrónico del nuevo propietario.

1. Vaya a la página [inicio de sesión en la cuenta de Commerce](https://account.magento.com/customer/account/login/).

1. Haga clic en **[!UICONTROL Sign in with Adobe ID]**.

1. Haga clic en **[!UICONTROL Create an account]**.

1. Introduzca la dirección de correo electrónico del propietario actual y una contraseña.

1. Haga clic en **[!UICONTROL Continue]**.

   Este paso crea un Adobe ID y lo vincula a la cuenta actual de Commerce (MAGEID). Con este vínculo de cuenta, el campo _[!UICONTROL Email]_&#x200B;está bloqueado frente a cualquier cambio. La configuración de la dirección de correo electrónico asociada se administra desde la cuenta de Adobe ID.

1. Vaya a [account.adobe.com](https://account.adobe.com/).

1. Haga clic en **[!UICONTROL Change Email]**.

1. Introduzca la nueva dirección de correo electrónico del propietario.

   Si la nueva dirección de correo electrónico ya está vinculada a otra cuenta del sistema, no se puede utilizar directamente para la transferencia. En su lugar, el proceso requiere el uso de una [dirección de correo electrónico temporal](#change-to-a-temporary-account) para facilitar el cambio.

1. Haga clic en **[!UICONTROL Change]**.

   Este paso genera un correo electrónico de verificación enviado a la nueva dirección de correo electrónico. El correo electrónico contiene un código de confirmación necesario para completar el cambio de dirección de correo electrónico.

1. Introduzca el código de confirmación enviado a la nueva dirección de correo electrónico.

1. Haga clic en **[!UICONTROL Verify]**.

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## Cambio de correo electrónico

>[!IMPORTANT]
>
>Revise los [tipos de transferencia](#identify-your-transfer-type) y asegúrese de cumplir las condiciones previas de esta secuencia de pasos.

Este tipo de transferencia provoca que el propietario de la cuenta actual pierda el acceso a otros productos de Adobe.

1. Vaya a [account.adobe.com](https://account.adobe.com/) y complete el inicio de sesión de Adobe.

1. En el nombre de su cuenta y avatar, haga clic en **[!UICONTROL Change Email]**.

1. En el cuadro de diálogo, introduzca la dirección de correo electrónico del nuevo propietario.

   Si la nueva dirección de correo electrónico ya está vinculada a otra cuenta del sistema, no se puede utilizar directamente para la transferencia. En su lugar, el proceso requiere el uso de una [dirección de correo electrónico temporal](#change-to-a-temporary-account) para facilitar el cambio.

1. Haga clic en **[!UICONTROL Change]**.

   Este paso genera un correo electrónico de verificación enviado a la nueva dirección de correo electrónico. El correo electrónico contiene un código de confirmación necesario para completar el cambio de dirección de correo electrónico.

1. Introduzca el código de confirmación enviado a la nueva dirección de correo electrónico.

1. Haga clic en **[!UICONTROL Verify]**.

## Cambio de cuenta de Adobe ID

>[!IMPORTANT]
>
>Revise los [tipos de transferencia](#identify-your-transfer-type) y asegúrese de cumplir las condiciones previas de esta secuencia de pasos.

Este tipo de transferencia utiliza una dirección de correo electrónico temporal para cambiar la propiedad de la cuenta cuando el propietario actual y el nuevo propietario tienen un Adobe ID existente y desea conservar ambas cuentas. Para completar la transferencia de propiedad, debe utilizar una dirección de correo electrónico temporal que no esté asociada a un Adobe ID.

### Cambiar a una cuenta temporal

El propietario actual completa estos pasos para asociar su Adobe ID con otra dirección de correo electrónico temporal.

1. Vaya a [account.adobe.com](https://account.adobe.com/) y complete el inicio de sesión de Adobe.

1. En el nombre de su cuenta y avatar, haga clic en **[!UICONTROL Change Email]**.

1. En el cuadro de diálogo, introduzca una dirección de correo electrónico temporal válida que no utilice un Adobe ID.

>[!NOTE]
>
>Debe tener acceso a la dirección de correo electrónico para poder recuperar el correo electrónico con el código de confirmación.
>
>Si no puede acceder al correo electrónico de la cuenta, pida a su equipo de TI que configure el reenvío de correo electrónico para la dirección de correo electrónico de la cuenta en el sistema de correo electrónico de su empresa. Si no se puede configurar el reenvío de correo electrónico, asegúrate de que el nuevo propietario de la cuenta tenga un Adobe ID y luego [envía una solicitud de soporte técnico](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) con todos los detalles necesarios para iniciar la transferencia de cuenta.

1. Haga clic en **[!UICONTROL Change]**.

   Este paso genera un correo electrónico de verificación enviado a la dirección de correo electrónico temporal. El correo electrónico contiene un código de confirmación necesario para completar el cambio de dirección de correo electrónico.

1. Introduzca el código de confirmación enviado a la dirección de correo electrónico temporal.

1. Haga clic en **[!UICONTROL Verify]**.

1. Cierre la sesión de la cuenta de Adobe.

### Nuevos pasos de propietario

Una vez que el propietario actual completa la transferencia a una dirección de correo electrónico temporal, el nuevo propietario debe completar estos pasos para cambiar la configuración de su cuenta de modo que apunte a la dirección de correo electrónico original del propietario actual.

1. Vaya a [account.adobe.com](https://account.adobe.com/) y complete el inicio de sesión de Adobe.

1. En el nombre de su cuenta y avatar, haga clic en **[!UICONTROL Change Email]**.

1. En el cuadro de diálogo, introduzca la dirección de correo electrónico original del propietario actual.

1. Haga clic en **[!UICONTROL Change]**.

   Este paso genera un correo electrónico de verificación enviado a la dirección de correo electrónico original del propietario actual. El correo electrónico contiene un código de confirmación necesario para completar el cambio de dirección de correo electrónico.

1. Introduzca el código de confirmación enviado a la dirección de correo electrónico original del propietario actual.

1. Haga clic en **[!UICONTROL Verify]**.

1. Cierre la sesión de la cuenta de Adobe.

### Pasos de seguimiento

Una vez que el nuevo propietario haya configurado correctamente su cuenta de Adobe con la dirección de correo electrónico original del propietario actual, complete estos pasos para transferir la propiedad.

1. Vaya a [account.adobe.com](https://account.adobe.com/) y complete el inicio de sesión de Adobe con la dirección de correo electrónico de la [cuenta temporal](#change-to-a-temporary-account).

1. Bajo el nombre y avatar de la cuenta, haga clic en **[!UICONTROL Change Email]**.

1. En el cuadro de diálogo, introduzca la dirección de correo electrónico del nuevo propietario.

1. Haga clic en **[!UICONTROL Change]**.

   Este paso genera un correo electrónico de verificación enviado a la dirección de correo electrónico del nuevo propietario. El correo electrónico contiene un código de confirmación necesario para completar el cambio de dirección de correo electrónico.

1. Introduzca el código de confirmación enviado a la dirección de correo electrónico del nuevo propietario.

1. Haga clic en **[!UICONTROL Verify]**.

## Pasos finales

Una vez que el nuevo propietario completa los pasos del primer o tercer caso de uso, debe [enviar una solicitud de asistencia](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide?lang=en#support-case) para informar al equipo de asistencia sobre la actualización de la dirección de correo electrónico. A continuación, el equipo de asistencia completa tareas adicionales, como actualizar la dirección de correo electrónico en el perfil [Commerce Marketplace](https://commercemarketplace.adobe.com/). Incluya la dirección de correo electrónico del propietario de la cuenta anterior en la solicitud.