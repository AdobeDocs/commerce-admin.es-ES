---
title: Asignar un administrador de empresa
description: Obtenga información sobre cómo asignar una cuenta de usuario de empresa como administrador de empresa designado para la cuenta de empresa.
exl-id: 26f3a449-6f3a-4078-816d-6248ac6d1e46
feature: B2B, Companies
role: Admin, User
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# Asignar un administrador de empresa

El administrador de la empresa se asigna inicialmente cuando se crea la cuenta de la empresa por primera vez y solo un administrador de tienda de Admin puede modificarla.

- Cada empresa solo puede tener un administrador asignado.
- Un usuario de empresa solo puede ser el administrador de una empresa.
- Los cambios en el administrador de la empresa asignado debe completarlos un administrador de tienda del administrador.

## Cambiar administrador de empresa asignado

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Compañías](./assets/companies-grid.png){width="700" zoomable="yes"}

1. Busque la empresa en la lista y haga clic en **[!UICONTROL Edit]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Company Admin]**.

   ![Administrador de la empresa](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. Escriba **[!UICONTROL Job Title]** del nuevo administrador de la compañía.

   Esta acción borra el formulario y se resaltan los campos obligatorios _[!UICONTROL First Name]_&#x200B;y&#x200B;_[!UICONTROL Last Name]_.

1. Escriba la dirección **[!UICONTROL Email]** del nuevo administrador de la compañía.

   Si el sistema no encuentra la dirección de correo electrónico en la base de datos, se le pedirá que confirme que desea reemplazar al administrador de la empresa.

   - Si no existe una cuenta de usuario para el nuevo administrador de la empresa, el sistema crea una cuenta del tipo `Company Admin`.

   - Si la cuenta de usuario existe en el sistema, se mueve a la posición de administrador de la empresa en la estructura de la empresa.

1. Escriba **[!UICONTROL First Name]** y **[!UICONTROL Last Name]**, así como cualquier otra información que corresponda para el nuevo administrador de la compañía.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

   La cuenta individual del anterior administrador de la empresa permanece en el sistema como una cuenta de usuario activa, asignada a la función de usuario predeterminada. Si esta es la única compañía asociada con la cuenta de usuario, el tipo de cuenta cambia de *[!UICONTROL Company user]* a *[!UICONTROL Individual user]*.

   El sistema envía una notificación por correo electrónico del cambio a los administradores nuevos y anteriores de la empresa.

