---
title: Aprobar una cuenta de compañía
description: Obtenga información sobre cómo aprobar solicitudes de cuenta de empresa en Admin.
exl-id: c7123383-0e94-4d6c-be3c-b6ca84145a59
feature: B2B, Companies, Configuration
role: Admin, User
TQID: 'https://experienceleague.adobe.com/ZpDdYMYaSnG1lOwV22mmrkYjBvf90pUJVZxP2r526pw'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e9004f3c-09ae-5d24-acd2-fa0987fdb66e
    internal-label: Companies
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%
---
# Aprobar una cuenta de compañía

El estado de las solicitudes recibidas de la tienda para crear una empresa es `Pending Approval` hasta que el administrador de la tienda revise la solicitud y la apruebe o rechace. El estado de una cuenta de compañía puede establecerse en cualquiera de las siguientes opciones:

- [!UICONTROL Active]
- [!UICONTROL Pending Approval]
- [!UICONTROL Rejected]
- [!UICONTROL Blocked]

También puede usar el control [Acciones](account-company-manage.md) para aprobar varias solicitudes de la compañía.

![Aprobación pendiente](./assets/companies-pending-approval.png){width="700" zoomable="yes"}

## Aprobar una cuenta de empresa pendiente

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   Puede usar el selector _[!UICONTROL Columns]_sobre la cuadrícula para mostrar la columna **[!UICONTROL Status]**.

1. En la columna _[!UICONTROL Action]_, haga clic en **[!UICONTROL Edit]**.

1. Establezca **[!UICONTROL Company Status]** en `Active`.

   ![Establecer el estado de la compañía](./assets/company-status-active.png){width="700" zoomable="yes"}

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL Change status]**.

   El administrador de la empresa recibe una notificación por correo electrónico avisando que la empresa está activa.

1. Si corresponde, establezca **[!UICONTROL Sales Representative]** en una cuenta de usuario de administrador específica.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Account Information]** y use el campo **[!UICONTROL Comment]** para escribir notas sobre la cuenta.

   Los comentarios no son visibles desde la tienda.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

   Se envía un correo electrónico de confirmación al administrador de la empresa y a la empresa para confirmar que la cuenta de la empresa está aprobada.

## Estado de compañía

| Estado | Descripción |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Active] | La empresa está aprobada y el administrador de la empresa puede administrarla desde la tienda. |
| [!UICONTROL Pending Approval] | Se ha enviado una solicitud para crear una cuenta de compañía desde la tienda, pero aún no se ha revisado. |
| [!UICONTROL Rejected] | La solicitud para crear una cuenta de empresa fue rechazada por el administrador del almacén. |
| [!UICONTROL Blocked] | La cuenta de la compañía ya no está al día. El cliente puede acceder a la cuenta desde la tienda, pero no puede realizar compras. |

{style="table-layout:auto"}
