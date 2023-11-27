---
title: Integraciones
description: Obtenga información sobre cómo configurar credenciales de OAuth y redirigir URL para integraciones de terceros.
exl-id: b7632994-b07b-4cdb-b62c-79bc7a3a01c8
role: Admin, Developer
feature: System, Integration, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# Integraciones

La definición de una integración en el administrador de Commerce establece la ubicación de las credenciales de OAuth y la URL de redireccionamiento para integraciones de terceros, e identifica los recursos de API disponibles que se necesitan para la integración. Para obtener información más detallada sobre el proceso de registro de la integración, consulte [Autenticación basada en OAuth](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) en la documentación para desarrolladores de Commerce.

![Integraciones](./assets/integrations.png){width="700" zoomable="yes"}

## Flujo de trabajo de incorporación

1. **Autorizar la integración** - Vaya a la **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**, busque la integración adecuada y autorice.
1. **Verificar y establecer inicio de sesión** - Cuando se le solicite, acepte el acceso solicitado. Si se le redirige a un tercero, inicie sesión en el sistema o cree una cuenta. Después de iniciar sesión correctamente, vuelve a la página de integración.
1. **Recibir confirmación de integración autorizada** : el sistema envía una notificación avisando de que la integración se ha autorizado correctamente. Después de configurar una integración y recibir las credenciales, ya no es necesario realizar llamadas para acceder a tokens o solicitarlos.

## Añadir una integración

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

   ![Nueva integración](./assets/integration-new.png){width="600" zoomable="yes"}

1. Introduzca la siguiente información de integración:

   - Introduzca el **[!UICONTROL Name]** de la integración y el contacto **[!UICONTROL Email]** dirección.

   - Introduzca el **[!UICONTROL Callback URL]** donde se pueden enviar credenciales de OAuth al utilizar OAuth para el intercambio de tokens. Uso de `https://` se recomienda encarecidamente.

   - Introduzca el **[!UICONTROL Identity Link URL]** para redirigir a los usuarios a una cuenta de terceros con estas credenciales de integración de Adobe Commerce o Magento Open Source.

   >[!NOTE]
   >
   > El `Integration not secure` etiqueta de advertencia aparece cerca de cada nombre de integración en la [!UICONTROL Integrations] como recordatorio, hasta que las direcciones URL HTTPS se guarden en [!UICONTROL Callback URL] y [!UICONTROL Identity Link URL] campos.

   - Cuando se le pida, introduzca su contraseña para confirmar su identidad.

1. En el panel izquierdo, elija **[!UICONTROL API]** y haga lo siguiente:

   - Establecer **[!UICONTROL Resource Access]** a uno de los siguientes:

      - `All`
      - `Custom`

   - Para el acceso personalizado, seleccione la casilla de verificación de cada recurso necesario.

     ![Integraciones: API disponible](./assets/integrations-available-api.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

## Activación de una integración

De forma predeterminada, aparece una integración guardada en la cuadrícula con un `Inactive` estado. Para activarla, complete los siguientes pasos:

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. Busque la integración recién creada y haga clic en **[!UICONTROL Activate]** vínculo.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Allow]**.

   Esta acción muestra los tokens de integración para extensiones. Copie esta información en una ubicación segura y cifrada para usarla con su integración.

   ![Tokens de integración para extensiones](./assets/integration-tokens-for-extensions.png){width="600" zoomable="yes"}

1. En la esquina superior derecha, haga clic en **[!UICONTROL Done]**.

## Reautorización de una integración

Para generar un nuevo token de acceso de integración y un secreto de token de acceso, vuelva a autorizar la integración desde el administrador:

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. Búsqueda de la integración con **[!UICONTROL Active]** estado.

1. Entrada _[!UICONTROL Activate]_Haga clic en la columna **[!UICONTROL Reauthorize]**.

1. Clic **[!UICONTROL Reauthorize]** para aprobar el acceso a los recursos de la API.

1. Guarde los nuevos tokens de integración para las extensiones y haga clic en **[!UICONTROL Done]**.

## Cambiar la configuración de seguridad del acceso de invitado de API

De forma predeterminada, el sistema no permite el acceso anónimo de invitados a CMS, catálogos y otros recursos de la tienda. Si debe cambiar la configuración, haga lo siguiente:

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Services]** y elija **[!UICONTROL Magento Web API]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Web API Security Setting]** sección.

   ![Configuración de servicios: configuración de seguridad de API web](../configuration-reference/services/assets/web-api-security.png){width="600" zoomable="yes"}

1. Establecer **[!UICONTROL Allow Anonymous Guest Access]** hasta `Yes`.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

Para obtener más información, consulte [Restricción del acceso a las API web anónimas](https://developer.adobe.com/commerce/webapi/rest/use-rest/anonymous-api-security/) en la documentación para desarrolladores de Commerce.

## Eliminación de una integración

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. Busque la integración existente y haga clic en el icono ( ![icono de papelera](../assets/icon-delete-trashcan-solid.png) ) en el **[!UICONTROL Delete]** columna.

1. Para confirmar la acción, haga clic en **[!UICONTROL OK]**.
