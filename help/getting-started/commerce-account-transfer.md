---
title: Transferir una cuenta de Adobe Commerce
description: Obtenga información sobre cómo transferir una cuenta de Adobe Commerce a un nuevo propietario o dirección de correo electrónico, elegir el tipo de transferencia correcto, comprobar los cambios de los correos electrónicos y ponerse en contacto con el servicio de asistencia.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
TQID: https://experienceleague.adobe.com/CIyzus4f8WcBH-jW9R1nCL-gkl065DLTHbjNn0K6e7E
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: e01cba363eb149286479718e660f8cdf6526e826
workflow-type: tm+mt
source-wordcount: 1553
ht-degree: 0%

---

# Transferir una cuenta de Adobe Commerce

A medida que cambien las responsabilidades comerciales, es posible que tenga que transferir su cuenta de Adobe Commerce a un nuevo propietario o a otra dirección de correo electrónico. Esta transferencia requiere un cambio en el correo electrónico del usuario principal asociado a la cuenta.

La siguiente información describe el proceso para transferir una cuenta de Adobe Commerce (MAGEID). No incluye cambios en Adobe Commerce sobre la propiedad del proyecto de infraestructura en la nube o la propiedad de [!DNL New Relic]. Para obtener más información sobre el acceso a proyectos en la nube, consulte [Administrar el acceso de usuarios](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access) en la _Guía de Commerce en infraestructura en la nube_.

>[!IMPORTANT]
>
>Si el nuevo propietario de la cuenta compró extensiones utilizando Acceso compartido, el acceso a esas extensiones se pierde en cuanto se inicia la transferencia de la cuenta.
>
>Antes de solicitar la transferencia de la cuenta, asegúrate de que el nuevo propietario recupera los identificadores de pedido para las compras de [su [!DNL Commerce Marketplace] cuenta](https://commercemarketplace.adobe.com/sales/order/history/) y solicita un reembolso al [[!DNL Commerce Marketplace] equipo](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case). Las compras de extensión no se pueden transferir a una cuenta diferente.

## Identificación del tipo de transferencia

El proceso de transferencia de cuenta de Adobe Commerce adecuado depende del estado de la cuenta del propietario actual y del nuevo propietario, así como de si la dirección de correo electrónico del propietario actual sigue siendo accesible. Por ejemplo, si el propietario actual ha abandonado la empresa, es posible que siga necesitando acceso a los correos electrónicos enviados a esa dirección.

Los siguientes escenarios describen las opciones de transferencia disponibles en función de estas condiciones.

| Tipo de transferencia | Propietario actual | Nuevo propietario |
| ------------- | ------------- | --------- |
| [Nuevo cambio de Adobe ID y correo electrónico](#new-adobe-id-and-email-change) | Tiene un MAGEID que no se ha conectado a una Adobe ID | No tiene un MAGEID y no tiene un Adobe ID. |
| [Solo cambio de correo electrónico](#email-change) | Tiene un MAGEID conectado a una Adobe ID. | Tiene un Adobe ID, pero no tiene un MAGEID conectado a la cuenta. |
| [Modificador de cuenta de Adobe ID](#adobe-id-account-switch) | Tiene un MAGEID conectado a una Adobe ID. | Tiene un MAGEID y está conectado a un Adobe ID. |

{style="table-layout:auto"}

>[!NOTE]
>
>A medida que Adobe Commerce continúa integrándose con otras soluciones de Adobe, una cuenta de Adobe Commerce (MAGEID) ahora requiere una asociación con un Adobe ID. El Adobe ID usa la misma dirección de correo electrónico conectada a tu [cuenta de Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).

## Verificar un cambio de correo electrónico de Adobe ID

Varias rutas de transferencia usan el mismo flujo de trabajo de verificación en [account.adobe.com](https://account.adobe.com/). Después de escribir la dirección de correo electrónico de destino y hacer clic en **[!UICONTROL Change]**, complete estos pasos:

1. Abra el correo electrónico de verificación enviado a la dirección que ha introducido y busque el código de confirmación.

1. Introduzca el código de confirmación.

1. Haga clic en **[!UICONTROL Verify]**.

## Nuevo cambio de Adobe ID y correo electrónico

>[!IMPORTANT]
>
>Revise los [tipos de transferencia](#identify-your-transfer-type) y confirme que esta ruta coincide con su situación:
>
>- El propietario actual sigue perteneciendo a la empresa.
>- El propietario actual no tiene un Adobe ID o tiene un Adobe ID que no está conectado a su [cuenta de Adobe Commerce (MAGEID)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).
>- El nuevo propietario no tiene una cuenta de Adobe ID ni de Adobe Commerce.

Utilice esta ruta cuando el propietario actual tenga un MAGEID que aún no esté vinculado a un Adobe ID. El propietario actual primero crea y vincula un Adobe ID y, a continuación, cambia esa dirección de correo electrónico de Adobe ID por la del nuevo propietario.

1. Vaya a la página [inicio de sesión en la cuenta de Adobe Commerce](https://account.magento.com/customer/account/login/).

1. Haga clic en **[!UICONTROL Sign in with Adobe ID]**.

1. Haga clic en **[!UICONTROL Create an account]**.

1. Introduzca la dirección de correo electrónico y la contraseña del propietario actual.

1. Haga clic en **[!UICONTROL Continue]**.

   Este paso crea un Adobe ID y lo vincula a la cuenta actual de Adobe Commerce (MAGEID). Con este vínculo de cuenta, el campo _[!UICONTROL Email]_&#x200B;está bloqueado frente a cualquier cambio. La configuración de la dirección de correo electrónico asociada se administra desde la cuenta de Adobe ID.

1. Vaya a [account.adobe.com](https://account.adobe.com/).

1. Haga clic en **[!UICONTROL Change Email]**.

1. Introduzca la nueva dirección de correo electrónico del propietario.

   Si la nueva dirección de correo electrónico ya está vinculada a otra cuenta del sistema, no se puede utilizar directamente para la transferencia. En su lugar, sigue la ruta del [cambio de cuenta de Adobe ID](#adobe-id-account-switch) y usa una [dirección de correo electrónico temporal](#change-to-a-temporary-account).

1. Complete los [pasos de verificación por correo electrónico](#verify-an-adobe-id-email-change).

Una vez que el nuevo propietario verifique la dirección de correo electrónico, continúe con [Pasos finales](#final-steps) para que el Soporte técnico de Adobe Commerce pueda actualizar los registros de cuenta como el perfil [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/).

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on){transcript=true}

## Solo cambio de correo electrónico {#email-change}

>[!IMPORTANT]
>
>Revise los [tipos de transferencia](#identify-your-transfer-type) y confirme que esta ruta coincide con su situación:
>
>- El propietario actual sigue perteneciendo a la empresa.
>- El propietario actual tiene un Adobe ID conectado a su [cuenta de Adobe Commerce (MAGEID)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).
>- El nuevo propietario tiene un Adobe ID que no está conectado a una cuenta de Adobe Commerce.

Antes de empezar, tenga en cuenta que este tipo de transferencia provoca que el propietario de la cuenta actual pierda el acceso a otros productos de Adobe vinculados a ese Adobe ID.

1. Vaya a [account.adobe.com](https://account.adobe.com/) y complete el inicio de sesión de Adobe.

1. En el nombre de su cuenta y avatar, haga clic en **[!UICONTROL Change Email]**.

1. En el cuadro de diálogo, introduzca la dirección de correo electrónico del nuevo propietario.

   Si la nueva dirección de correo electrónico ya está vinculada a otra cuenta del sistema, no se puede utilizar directamente para la transferencia. En su lugar, sigue la ruta del [cambio de cuenta de Adobe ID](#adobe-id-account-switch) y usa una [dirección de correo electrónico temporal](#change-to-a-temporary-account).

1. Complete los [pasos de verificación por correo electrónico](#verify-an-adobe-id-email-change).

Una vez que el nuevo propietario verifique la dirección de correo electrónico, continúe con [Pasos finales](#final-steps) para que el Soporte técnico de Adobe Commerce pueda actualizar los registros de cuenta como el perfil [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/).

## Cambio de cuenta de Adobe ID

>[!IMPORTANT]
>
>Revise los [tipos de transferencia](#identify-your-transfer-type) y confirme que esta ruta coincide con su situación:
>
>- El propietario actual ya no pertenece a la empresa, pero se puede acceder a los mensajes de correo electrónico enviados a la dirección de correo electrónico de la empresa del propietario actual o el equipo informático puede reenviar dichos mensajes a un contacto autorizado.
>- El propietario actual tiene un Adobe ID conectado a su [cuenta de Adobe Commerce (MAGEID)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).
>- El nuevo propietario tiene un Adobe ID conectado a su cuenta de Adobe Commerce.

Este tipo de transferencia utiliza una dirección de correo electrónico temporal para cambiar la propiedad de la cuenta cuando el propietario actual y el nuevo propietario tienen un Adobe ID existente y desea conservar ambos Adobe ID. Para completar la transferencia de propiedad, debe utilizar una dirección de correo electrónico temporal que no esté asociada a un Adobe ID.

### Cambiar a una cuenta temporal

Complete estos pasos para asociar la Adobe ID del propietario actual con una dirección de correo electrónico temporal. Debe tener acceso a esa dirección de correo electrónico para poder recuperar el código de confirmación.

>[!NOTE]
>
>Si no puede acceder al correo electrónico del propietario actual, pida a su equipo de TI que configure el reenvío de correo electrónico para la dirección de correo electrónico de la cuenta en el sistema de correo electrónico de su empresa. Si no se puede configurar el reenvío de correo electrónico, asegúrate de que el nuevo propietario de la cuenta tenga un Adobe ID y luego [envía una solicitud de soporte técnico](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) con todos los detalles necesarios para iniciar la transferencia de cuenta.

1. Vaya a [account.adobe.com](https://account.adobe.com/) y complete el inicio de sesión de Adobe.

1. En el nombre de su cuenta y avatar, haga clic en **[!UICONTROL Change Email]**.

1. En el cuadro de diálogo, introduzca una dirección de correo electrónico temporal válida que no utilice un Adobe ID.

1. Complete los [pasos de verificación por correo electrónico](#verify-an-adobe-id-email-change).

1. Cierre la sesión de la cuenta de Adobe.

### Nuevos pasos de propietario

Una vez que el propietario actual completa la transferencia a una dirección de correo electrónico temporal, el nuevo propietario debe completar estos pasos para cambiar su dirección de correo electrónico de Adobe ID por la dirección de correo electrónico original del propietario actual.

1. Vaya a [account.adobe.com](https://account.adobe.com/) y complete el inicio de sesión de Adobe.

1. En el nombre de su cuenta y avatar, haga clic en **[!UICONTROL Change Email]**.

1. En el cuadro de diálogo, introduzca la dirección de correo electrónico original del propietario actual.

1. Complete los [pasos de verificación por correo electrónico](#verify-an-adobe-id-email-change).

1. Cierre la sesión de la cuenta de Adobe.

### Pasos de seguimiento

Una vez que el nuevo propietario haya configurado correctamente su Adobe ID con la dirección de correo electrónico original del propietario actual, complete estos pasos para asignar esa dirección de correo electrónico al nuevo propietario.

1. Vaya a [account.adobe.com](https://account.adobe.com/) y complete el inicio de sesión de Adobe con la dirección de correo electrónico de la [cuenta temporal](#change-to-a-temporary-account).

1. Bajo el nombre y avatar de la cuenta, haga clic en **[!UICONTROL Change Email]**.

1. En el cuadro de diálogo, introduzca la dirección de correo electrónico del nuevo propietario.

1. Complete los [pasos de verificación por correo electrónico](#verify-an-adobe-id-email-change).

Una vez que el nuevo propietario verifique la dirección de correo electrónico, continúe con [Pasos finales](#final-steps) para que el Soporte técnico de Adobe Commerce pueda actualizar los registros de cuenta como el perfil [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/).

## Pasos finales

Complete estos pasos después de completar el proceso de [cambio de Adobe ID y correo electrónico nuevo](#new-adobe-id-and-email-change), [solo cambio de correo electrónico](#email-change) o [cambio de cuenta de Adobe ID](#adobe-id-account-switch).

1. Como nuevo propietario, [envíe una solicitud de soporte técnico](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide?lang=en#support-case).

   Incluya los siguientes detalles:

   - La dirección de correo electrónico del propietario anterior de la cuenta
   - La nueva dirección de correo electrónico del propietario
   - Tenga en cuenta que ha completado una transferencia de cuenta de Adobe Commerce y ha actualizado la dirección de correo electrónico de Adobe ID

1. Espere a que el Soporte técnico de Adobe Commerce confirme la actualización.

   La asistencia técnica también actualiza los registros relacionados, como la dirección de correo electrónico del perfil [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/).

Una vez que el servicio de asistencia técnica haya completado la solicitud, el nuevo propietario podrá iniciar sesión en la cuenta de Adobe Commerce con su Adobe ID. MAGEID sigue siendo el identificador de derecho de la cuenta.
