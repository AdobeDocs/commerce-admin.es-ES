---
title: Transferir una cuenta de Commerce
description: Aprenda a transferir su cuenta de Commerce a otro propietario o dirección de correo electrónico.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: 00994f506056bf5504df758a44a7cd56f590750d
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 0%

---

# Transferir una cuenta de Commerce

A medida que cambien las responsabilidades comerciales, es posible que tenga que transferir la propiedad de su cuenta de Commerce existente a un nuevo propietario o a otra dirección de correo electrónico. Esta transferencia requiere un cambio en el correo electrónico del usuario principal asociado a la cuenta.

La siguiente información describe el proceso para transferir una cuenta de Commerce (MAGEID). No incluye cambios para la propiedad de la cuenta de Cloud (proyecto en la nube o New Relic). Para obtener más información sobre el acceso a proyectos en la nube, consulte [Administrar el acceso de usuarios](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) en la _Guía de Commerce en infraestructura en la nube_.

## Identificación del tipo de transferencia

La forma de completar esta transferencia depende de cuál de las siguientes situaciones describa su situación como el propietario actual de la cuenta y el nuevo propietario (dirección de correo electrónico) al que desea transferir la cuenta:

| Tipo de transferencia | Propietario actual | Nuevo propietario |
| ------------- | ------------- | --------- |
| [Nuevo cambio de Adobe ID y correo electrónico](#new-adobe-id-and-email-change) | Tiene un MAGEID **_no conectado_** con una cuenta de inicio de sesión de Adobe. | No tiene un MAGEID y no está conectado a una cuenta de inicio de sesión de Adobe. |
| [Cambio de correo electrónico](#email-change) | Tiene un MAGEID **_conectado_** con una cuenta de inicio de sesión de Adobe sin otros productos o servicios de Adobe asociados. | No tiene un MAGEID y no está conectado a una cuenta de inicio de sesión de Adobe. |
| [conmutador de Adobe ID](#adobe-id-account-switch) | Tiene un MAGEID **_conectado_** con una cuenta de inicio de sesión de Adobe sin otros productos o servicios de Adobe asociados. | Tiene un MAGEID y está conectado a una cuenta de inicio de sesión de Adobe sin ningún otro producto o servicio de Adobe asociado. |

{style="table-layout:auto"}

>[!NOTE]
>
>A medida que Adobe Commerce continúa integrándose con otras soluciones de Adobe, una cuenta de Commerce (MAGEID) ahora requiere una asociación con un inicio de sesión con Adobe. Este Adobe ID utiliza la misma dirección de correo electrónico conectada a su cuenta de Commerce.

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

   Esto crea un Adobe ID y lo vincula a la cuenta actual de Commerce (MAGEID). Con este vínculo de cuenta, el campo _[!UICONTROL Email]_está bloqueado frente a cualquier cambio. La dirección de correo electrónico asociada se administra mediante la cuenta de Adobe ID.

1. Vaya a [account.adobe.com](https://account.adobe.com/).

1. Haga clic en **[!UICONTROL Change Email]**.

1. Introduzca la nueva dirección de correo electrónico del propietario.

1. Haga clic en **[!UICONTROL Change]**.

   Esto genera un correo electrónico de verificación enviado a la nueva dirección de correo electrónico. El correo electrónico contiene un código de confirmación necesario para completar el cambio de dirección de correo electrónico.

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

   Esto genera un correo electrónico de verificación enviado a la nueva dirección de correo electrónico. El correo electrónico contiene un código de confirmación necesario para completar el cambio de dirección de correo electrónico.

1. Introduzca el código de confirmación enviado a la nueva dirección de correo electrónico.

1. Haga clic en **[!UICONTROL Verify]**.

## Cambio de cuenta de Adobe ID

>[!IMPORTANT]
>
>Revise los [tipos de transferencia](#identify-your-transfer-type) y asegúrese de cumplir las condiciones previas de esta secuencia de pasos.

En caso de que el propietario actual y el nuevo propietario tengan ID de Adobe existentes, ambas cuentas deben permanecer, pero es necesario cambiar las direcciones de correo electrónico entre ellas. Esto requiere el uso de una dirección de correo electrónico _temporary_ que sea válida, pero que no esté asociada con y Adobe ID.

### Cambiar a una cuenta temporal

El propietario actual completa estos pasos para asociar su Adobe ID con otra dirección de correo electrónico temporal.

1. Vaya a [account.adobe.com](https://account.adobe.com/) y complete el inicio de sesión de Adobe.

1. En el nombre de su cuenta y avatar, haga clic en **[!UICONTROL Change Email]**.

1. En el cuadro de diálogo, introduzca una dirección de correo electrónico temporal válida que no utilice un Adobe ID.

   Debe tener acceso a la dirección de correo electrónico para poder recuperar el correo electrónico con el código de confirmación.

1. Haga clic en **[!UICONTROL Change]**.

   Esto genera un correo electrónico de verificación enviado a la dirección de correo electrónico temporal. El correo electrónico contiene un código de confirmación necesario para completar el cambio de dirección de correo electrónico.

1. Introduzca el código de confirmación enviado a la dirección de correo electrónico temporal.

1. Haga clic en **[!UICONTROL Verify]**.

1. Cierre la sesión de la cuenta de Adobe.

### Nuevos pasos de propietario

Una vez que el propietario actual haya completado la transferencia a una dirección de correo electrónico temporal, complete estos pasos para cambiar su cuenta al propietario actual.

1. Vaya a [account.adobe.com](https://account.adobe.com/) y complete el inicio de sesión de Adobe.

1. En el nombre de su cuenta y avatar, haga clic en **[!UICONTROL Change Email]**.

1. En el cuadro de diálogo, introduzca la dirección de correo electrónico original del propietario actual.

1. Haga clic en **[!UICONTROL Change]**.

   Esto genera un correo electrónico de verificación enviado a esa dirección de correo electrónico. El correo electrónico contiene un código de confirmación necesario para completar el cambio de dirección de correo electrónico.

1. Introduzca el código de confirmación enviado al propietario actual.

1. Haga clic en **[!UICONTROL Verify]**.

1. Cierre la sesión de la cuenta de Adobe.

### Pasos de seguimiento

Una vez que el nuevo propietario transfiera correctamente su cuenta Adobe al propietario actual (ahora anterior), complete estos pasos para transferir la propiedad.

1. Vaya a [account.adobe.com](https://account.adobe.com/) (la primera cuenta utilizada en la serie de pasos) y complete el inicio de sesión con el Adobe.

   Este inicio de sesión requiere el uso de la dirección de correo electrónico temporal.

1. Bajo el nombre y avatar de la cuenta, haga clic en **[!UICONTROL Change Email]**.

1. En el cuadro de diálogo, introduzca la dirección de correo electrónico del nuevo propietario.

1. Haga clic en **[!UICONTROL Change]**.

   Esto genera un correo electrónico de verificación enviado a esa dirección de correo electrónico. El correo electrónico contiene un código de confirmación necesario para completar el cambio de dirección de correo electrónico.

1. Introduzca el código de confirmación enviado al nuevo propietario.

1. Haga clic en **[!UICONTROL Verify]**.

1. **Envíe una solicitud de asistencia** para informar al equipo de asistencia de que ha actualizado la dirección de correo electrónico del propietario de la cuenta. Incluya la dirección de correo electrónico del propietario de la cuenta anterior en su solicitud.

El Soporte técnico debe realizar otros pasos, como actualizar la dirección de correo electrónico en el perfil de [Commerce Marketplace](https://commercemarketplace.adobe.com/).
