---
title: Asignar un administrador de empresa
description: Obtenga información sobre cómo asignar una cuenta de usuario de empresa como administrador de empresa designado para la cuenta de empresa.
exl-id: 26f3a449-6f3a-4078-816d-6248ac6d1e46
feature: B2B, Companies
role: Admin, User
TQID: https://experienceleague.adobe.com/5h4DaxiUVTz9UFOC3BZqd5ESPRLaLgvstCODPEEgCEk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 274
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

   Esta acción borra el formulario y se resaltan los campos obligatorios _[!UICONTROL First Name]_&#x200B;y_[!UICONTROL Last Name]_.

1. Escriba la dirección **[!UICONTROL Email]** del nuevo administrador de la compañía.

   Si el sistema no encuentra la dirección de correo electrónico en la base de datos, se le pedirá que confirme que desea reemplazar al administrador de la empresa.

   - Si no existe una cuenta de usuario para el nuevo administrador de la empresa, el sistema crea una cuenta del tipo `Company Admin`.

   - Si la cuenta de usuario existe en el sistema, se mueve a la posición de administrador de la empresa en la estructura de la empresa.

1. Escriba **[!UICONTROL First Name]** y **[!UICONTROL Last Name]**, así como cualquier otra información que corresponda para el nuevo administrador de la compañía.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

   La cuenta individual del anterior administrador de la empresa permanece en el sistema como una cuenta de usuario activa, asignada a la función de usuario predeterminada. Si esta es la única compañía asociada con la cuenta de usuario, el tipo de cuenta cambia de *[!UICONTROL Company user]* a *[!UICONTROL Individual user]*.

   El sistema envía una notificación por correo electrónico del cambio a los administradores nuevos y anteriores de la empresa.

