---
title: Desactivación de la integración de administración de Commerce con Adobe ID
description: Siga este procedimiento opcional para desactivar la integración de Adobe Commerce Admin con Adobe IMS.
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
TQID: https://experienceleague.adobe.com/KL6Cx3ymElo7ROx5SUJtlqtKivnw7-heqPWGksGP-pg
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
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 351
ht-degree: 0%

---

# Desactivación de la integración de administración de Commerce con Adobe ID

{{ee-feature}}

Es posible que los comerciantes que hayan integrado su instancia de Commerce con el flujo de trabajo de autenticación IMS de Adobe tengan que desactivar esta integración opcional.

Las implementaciones de Commerce vuelven a las directivas predeterminadas de flujo de trabajo y contraseña de autenticación de Commerce después de deshabilitar la integración de IMS. Solo los flujos de trabajo de usuario de administración se ven afectados cuando esta integración está habilitada o deshabilitada.

Consulte [Su cuenta de administrador](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html?lang=es) para obtener una descripción general del inicio de sesión de administrador de Commerce.

## Paso 1: Desactivación de la integración

No puede desactivar esta integración desde el administrador. Para deshabilitar la integración de Adobe IMS con Commerce y devolver la autenticación de Commerce a su estado predeterminado, debe deshabilitar la integración desde la interfaz de línea de comandos.

Para desactivar la integración:

```bash
bin/magento admin:adobe-ims:disable
```

Adobe Commerce muestra el siguiente mensaje una vez completada la prueba:

```
Admin Adobe IMS integration is disabled.
```

## Paso 2: Crear o recuperar la contraseña de Commerce

Después de deshabilitar la integración, los usuarios administradores deben utilizar una contraseña de Commerce para iniciar sesión en Admin.

* Los usuarios administradores de Commerce que recuerden su contraseña de Commerce preexistente (es decir, una contraseña de Commerce creada antes de la integración con IMS) pueden utilizarla para iniciar sesión en Admin.

* Los usuarios administradores de Commerce que no tengan una contraseña de Commerce preexistente o que la hayan olvidado deben crear una nueva contraseña. Para crear una nueva contraseña, los usuarios administradores pueden usar la característica [!UICONTROL Forgot your password?] en la página de inicio de sesión de Commerce para crear una nueva contraseña. Consulte [Restablecer contraseñas de cliente](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html?lang=es). Commerce no aceptará un campo de contraseña vacío.

## Después de deshabilitar la integración

El flujo de trabajo de autenticación predeterminado de Commerce se reanuda después de deshabilitar la integración de IMS y, una vez más, se solicita la contraseña a los usuarios administradores.

Al deshabilitar la integración con IMS, se eliminan de los archivos de configuración de Commerce las credenciales que se escribieron cuando se habilitó la integración (`Organization ID`, `Client ID` y `Client Secret` valores).
