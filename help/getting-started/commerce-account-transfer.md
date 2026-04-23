---
title: Transfer a Commerce account
description: Aprenda a transferir su cuenta de Commerce a otro propietario o dirección de correo electrónico.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: e33c207c5c9ba9ca6e82688e28c985cb9b3b7c71
workflow-type: tm+mt
source-wordcount: '1196'
ht-degree: 0%

---

# Transferir una cuenta de Commerce

A medida que cambien las responsabilidades comerciales, es posible que tenga que transferir su cuenta de Commerce a un nuevo propietario o a otra dirección de correo electrónico. This transfer requires a change to the primary user email associated with the account.

The following information describes the process for transferring a Commerce (MAGEID) account. It does not include changes for Cloud account (Cloud project or New Relic) ownership. For more information about cloud project access, see [Manage user access](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=es) in the _Commerce on Cloud Infrastructure Guide_.

>[!IMPORTANT]
>
>If the new account owner has purchased extensions using Shared Access, access to those extensions is lost as soon as the Account Transfer process has been initiated. Before requesting the account transfer, make sure that the new owner retrieves the Order IDs for the purchases from [their Marketplace account](https://commercemarketplace.adobe.com/sales/order/history/) and requests a refund for those extensions from the [Marketplace team](https://experienceleague.adobe.com/es/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case). It is not possible to transfer extension purchases to a different account.

## Identify your transfer type

El tipo de transferencia de cuenta de Commerce depende de las credenciales de cuenta de Commerce disponibles para el propietario actual y el nuevo propietario. Los siguientes escenarios describen los diferentes tipos de transferencia en función de estas credenciales.

| Tipo de transferencia | Propietario actual | Nuevo propietario |
| ------------- | ------------- | --------- |
| [Nuevo cambio de Adobe ID y correo electrónico](#new-adobe-id-and-email-change) | Tiene un MAGEID que **_no se ha conectado_** a una cuenta de inicio de sesión de Adobe | No tiene un MAGEID y no está conectado a una cuenta de inicio de sesión de Adobe. |
| [Cambio de correo electrónico](#email-change) | Tiene un MAGEID **_conectado_** con una cuenta de inicio de sesión de Adobe. | Tiene una cuenta de inicio de sesión de Adobe, pero **_no tiene un MAGEID_** conectado a una cuenta de inicio de sesión de Adobe. |
| [Modificador de cuenta de Adobe ID](#adobe-id-account-switch) | Tiene un MAGEID **_conectado_** a una cuenta de inicio de sesión de Adobe. | Has a MAGEID and is connected to an Adobe login account. |

{style="table-layout:auto"}

>[!NOTE]
>
>As Adobe Commerce continues to integrate with other Adobe solutions, a Commerce account (MAGEID) now requires an association with an Adobe login. This Adobe ID uses the same email address connected to your Commerce account.

## New Adobe ID and email change

>[!IMPORTANT]
>
>Revise los [tipos de transferencia](#identify-your-transfer-type) y asegúrese de cumplir las condiciones previas de esta secuencia de pasos.

Este tipo de transferencia requiere tener un Adobe ID vinculado a la cuenta de Commerce existente y, a continuación, cambiar esa cuenta a la dirección de correo electrónico del nuevo propietario.

1. Vaya a la página [inicio de sesión en la cuenta de Commerce](https://account.magento.com/customer/account/login/).

1. Haga clic en **[!UICONTROL Sign in with Adobe ID]**.

1. Haga clic en **[!UICONTROL Create an account]**.

1. Introduzca la dirección de correo electrónico del propietario actual y una contraseña.

1. Click **[!UICONTROL Continue]**.

   This step creates an Adobe ID and links it to the current Commerce account (MAGEID). With this account link, the _[!UICONTROL Email]_&#x200B;field is blocked from any changes. The configuration of the associated email address is managed from the Adobe ID account.

1. Navigate to [account.adobe.com](https://account.adobe.com/).

1. Click **[!UICONTROL Change Email]**.

1. Enter the new owner&#39;s email address.

   Si la nueva dirección de correo electrónico ya está vinculada a otra cuenta del sistema, no se puede utilizar directamente para la transferencia. En su lugar, el proceso requiere el uso de una [dirección de correo electrónico temporal](#change-to-a-temporary-account) para facilitar el cambio.

1. Haga clic en **[!UICONTROL Change]**.

   This step generates a verification email sent to the new email address. The email contains a confirmation code that is required to complete the email address change.

1. Enter the confirmation code sent to the new email address.

1. Haga clic en **[!UICONTROL Verify]**.

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## Cambio de correo electrónico

>[!IMPORTANT]
>
>Revise los [tipos de transferencia](#identify-your-transfer-type) y asegúrese de cumplir las condiciones previas de esta secuencia de pasos.

Este tipo de transferencia provoca que el propietario de la cuenta actual pierda el acceso a otros productos de Adobe.

1. Vaya a [account.adobe.com](https://account.adobe.com/) y complete el inicio de sesión de Adobe.

1. Under your account name and avatar, click **[!UICONTROL Change Email]**.

1. In the dialog, enter the new owner&#39;s email address.

   If the new email address is already linked to another account in the system, it cannot be directly used for the transfer. Instead, the process requires using a [temporary email address](#change-to-a-temporary-account) to facilitate the change.

1. Click **[!UICONTROL Change]**.

   This step generates a verification email sent to the new email address. The email contains a confirmation code that is required to complete the email address change.

1. Enter the confirmation code sent to the new email address.

1. Click **[!UICONTROL Verify]**.

## Adobe ID account switch

>[!IMPORTANT]
>
>Review the [transfer types](#identify-your-transfer-type) and make sure that you meet the preconditions for this sequence of steps.

This transfer type uses a temporary email address to switch account ownership when both the current owner and new owner have existing Adobe IDs, and you want to retain both accounts. To complete the ownership transfer, you must use a temporary email address that is not associated with an Adobe ID.

### Change to a temporary account

The current owner completes these steps to associate their Adobe ID with another, temporary email address.

1. Navigate to [account.adobe.com](https://account.adobe.com/) and complete the Adobe login.

1. En el nombre de su cuenta y avatar, haga clic en **[!UICONTROL Change Email]**.

1. En el cuadro de diálogo, introduzca una dirección de correo electrónico temporal válida que no utilice un Adobe ID.

>[!NOTE]
>
>You must have access to the email address so that you can retrieve the email with the confirmation code.
>
>If you cannot access the account email, ask your IT team to set up email forwarding for the account email address in your company email system. If email forwarding cannot be configured, ensure the new Account Owner has an Adobe ID and then [submit a Support request](https://experienceleague.adobe.com/es/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) with all necessary details to initiate the account transfer.

1. Click **[!UICONTROL Change]**.

   This step generates a verification email sent to the temporary email address. The email contains a confirmation code that is required to complete the email address change.

1. Enter the confirmation code sent to the temporary email address.

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

### Follow up steps

After the new owner successfully configures their Adobe account with the original email address of the current owner, complete these steps to transfer ownership.

1. Navigate to [account.adobe.com](https://account.adobe.com/), and complete the Adobe login using the email address for the [temporary account](#change-to-a-temporary-account).

1. Under the account name and avatar, click **[!UICONTROL Change Email]**.

1. En el cuadro de diálogo, introduzca la dirección de correo electrónico del nuevo propietario.

1. Haga clic en **[!UICONTROL Change]**.

   Este paso genera un correo electrónico de verificación enviado a la dirección de correo electrónico del nuevo propietario. El correo electrónico contiene un código de confirmación necesario para completar el cambio de dirección de correo electrónico.

1. Introduzca el código de confirmación enviado a la dirección de correo electrónico del nuevo propietario.

1. Haga clic en **[!UICONTROL Verify]**.

## Pasos finales

Una vez que el nuevo propietario completa los pasos del primer o tercer caso de uso, debe [enviar una solicitud de asistencia](https://experienceleague.adobe.com/es/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide?lang=en#support-case) para informar al equipo de asistencia sobre la actualización de la dirección de correo electrónico. A continuación, el equipo de asistencia completa tareas adicionales, como actualizar la dirección de correo electrónico en el perfil [Commerce Marketplace](https://commercemarketplace.adobe.com/). Incluya la dirección de correo electrónico del propietario de la cuenta anterior en la solicitud.
