---
title: Desactivación de la integración de administración de Commerce con Adobe ID
description: Siga este procedimiento opcional para desactivar la integración de Adobe Commerce Admin con Adobe IMS.
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
source-git-commit: 53c3b6c9fa9c152e6619528a43580b0acc71a2a5
workflow-type: tm+mt
source-wordcount: '302'
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
