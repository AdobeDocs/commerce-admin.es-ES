---
title: Transferir una cuenta de Commerce
description: Aprenda a transferir su cuenta de Commerce a otro propietario o dirección de correo electrónico.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: 674d918dee9fa0a001bf7910ab2531df8dc353af
workflow-type: tm+mt
source-wordcount: '1028'
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
| [Nuevo cambio de Adobe ID y correo electrónico](#new-adobe-id-and-email-change) | Tiene un MAGEID **_no conectado_** con una cuenta de inicio de sesión de Adobe. | No tiene un MAGEID y no está conectado a una cuenta de inicio de sesión de Adobe. |
| [Cambio de correo electrónico](#email-change) | Tiene un MAGEID **_conectado_** con una cuenta de inicio de sesión de Adobe. | No tiene un MAGEID y no está conectado a una cuenta de inicio de sesión de Adobe. |
| [conmutador de Adobe ID](#adobe-id-account-switch) | Tiene un MAGEID **_conectado_** con una cuenta de inicio de sesión de Adobe. | Tiene un MAGEID y está conectado a una cuenta de inicio de sesión de Adobe. |

{style="table-layout:auto"}

>[!NOTE]
>
>A medida que Adobe Commerce continúa integrándose con otras soluciones de Adobe, una cuenta de Commerce (MAGEID) ahora requiere una asociación con un inicio de sesión de Adobe. Este Adobe ID utiliza la misma dirección de correo electrónico conectada a su cuenta de Commerce.

## Nuevo cambio de Adobe ID y correo electrónico

>[!IMPORTANT]
>
>Revise los [tipos de transferencia](#identify-your-transfer-type) y asegúrese de cumplir las condiciones previas de esta secuencia de pasos.

Este tipo de transferencia requiere que cree primero un Adobe ID asociado y, a continuación, cambie esa cuenta a la dirección de correo electrónico del nuevo propietario.

1. Vaya a su [cuenta de Commerce](https://account.magento.com/customer/account/login/).

1. Haga clic en **[!UICONTROL Sign in with Adobe ID]**.

1. Haga clic en **[!UICONTROL Create an account]**.

1. Introduzca la dirección de correo electrónico del propietario actual y una contraseña.

1. Haga clic en **[!UICONTROL Continue]**.

   Este paso crea un Adobe ID y lo vincula a la cuenta actual de Commerce (MAGEID). Con este vínculo de cuenta, el campo _[!UICONTROL Email]_&#x200B;está bloqueado frente a cualquier cambio. La configuración de la dirección de correo electrónico asociada se administra desde la cuenta de Adobe ID.

1. Vaya a [account.adobe.com](https://account.adobe.com/).

1. Haga clic en **[!UICONTROL Change Email]**.

1. Introduzca la nueva dirección de correo electrónico del propietario.

1. Haga clic en **[!UICONTROL Change]**.

   Este paso genera un correo electrónico de verificación enviado a la nueva dirección de correo electrónico. El correo electrónico contiene un código de confirmación necesario para completar el cambio de dirección de correo electrónico.

1. Introduzca el código de confirmación enviado a la nueva dirección de correo electrónico.

1. Haga clic en **[!UICONTROL Verify]**.

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## Cambio de correo electrónico

>[!IMPORTANT]
>
>Revise los [tipos de transferencia](#identify-your-transfer-type) y asegúrese de cumplir las condiciones previas de esta secuencia de pasos.

1. Vaya a [account.adobe.com](https://account.adobe.com/) y complete el inicio de sesión de Adobe.

1. En el nombre de su cuenta y avatar, haga clic en **[!UICONTROL Change Email]**.

1. En el cuadro de diálogo, introduzca la dirección de correo electrónico del nuevo propietario.

1. Haga clic en **[!UICONTROL Change]**.

   Este paso genera un correo electrónico de verificación enviado a la nueva dirección de correo electrónico. El correo electrónico contiene un código de confirmación necesario para completar el cambio de dirección de correo electrónico.

1. Introduzca el código de confirmación enviado a la nueva dirección de correo electrónico.

1. Haga clic en **[!UICONTROL Verify]**.

## Cambio de cuenta de Adobe ID

>[!IMPORTANT]
>
>Revise los [tipos de transferencia](#identify-your-transfer-type) y asegúrese de cumplir las condiciones previas de esta secuencia de pasos.

En caso de que el propietario actual y el nuevo propietario tengan un Adobe ID existente, ambas cuentas deben permanecer, pero es necesario cambiar las direcciones de correo electrónico entre ellas. Esto requiere el uso de una dirección de correo electrónico _temporary_ que sea válida, pero que no esté asociada a un Adobe ID.

### Cambiar a una cuenta temporal

El propietario actual completa estos pasos para asociar su Adobe ID con otra dirección de correo electrónico temporal.

1. Vaya a [account.adobe.com](https://account.adobe.com/) y complete el inicio de sesión de Adobe.

1. En el nombre de su cuenta y avatar, haga clic en **[!UICONTROL Change Email]**.

1. En el cuadro de diálogo, introduzca una dirección de correo electrónico temporal válida que no utilice un Adobe ID.

   Debe tener acceso a la dirección de correo electrónico para poder recuperar el correo electrónico con el código de confirmación.

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

Una vez que el nuevo propietario haya configurado correctamente su cuenta de Adobe con la dirección de correo electrónico original del propietario actual (ahora anterior), complete estos pasos para transferir la propiedad.

1. Vaya a [account.adobe.com](https://account.adobe.com/) y complete el inicio de sesión de Adobe con la dirección de correo electrónico de la [cuenta temporal](#change-to-a-temporary-account).

1. Bajo el nombre y avatar de la cuenta, haga clic en **[!UICONTROL Change Email]**.

1. En el cuadro de diálogo, introduzca la dirección de correo electrónico del nuevo propietario.

1. Haga clic en **[!UICONTROL Change]**.

   Este paso genera un correo electrónico de verificación enviado a la dirección de correo electrónico del nuevo propietario. El correo electrónico contiene un código de confirmación necesario para completar el cambio de dirección de correo electrónico.

1. Introduzca el código de confirmación enviado a la dirección de correo electrónico del nuevo propietario.

1. Haga clic en **[!UICONTROL Verify]**.

>[!IMPORTANT]
>
>Envíe una solicitud de asistencia para informar al equipo de asistencia de que ha actualizado la dirección de correo electrónico del propietario de la cuenta. El equipo debe realizar pasos adicionales para completar la actualización, como actualizar la dirección de correo electrónico en su perfil de [Commerce Marketplace](https://commercemarketplace.adobe.com/). Incluya la dirección de correo electrónico del propietario de la cuenta anterior en su solicitud.
