---
title: Asignar un grupo de clientes a una empresa
description: Obtenga información acerca de cómo asignar un grupo de clientes a una cuenta de compañía en su tienda de Adobe Commerce.
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
TQID: https://experienceleague.adobe.com/O03eRkYyE78HIHjmwYRXqfOR2A7k1KFL11AspJGCi-U
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
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
source-wordcount: 236
ht-degree: 0%

---

# Asignar un grupo de clientes a una empresa

Asignar un grupo de clientes a una empresa es esencialmente lo mismo que asignar un catálogo compartido. Si el catálogo compartido no está [habilitado en la configuración](enable-basic-features.md), se asignará un grupo de clientes a una compañía en lugar de un catálogo compartido.

- Solo se puede asignar un grupo de clientes o un catálogo compartido a una compañía a la vez. No se puede eliminar un grupo de clientes asociado a un catálogo compartido.
- Al cambiar el grupo de clientes asignado a la empresa, se actualizan los perfiles de todos los miembros de la empresa.
- Si la asignación del grupo de clientes se cambia de un catálogo compartido a un grupo de clientes normal, los miembros de la empresa pierden el acceso al catálogo compartido y el catálogo principal pasa a estar disponible para ellos desde la tienda.
- Después de cambiar el grupo de la compañía, un usuario de la compañía debe cerrar la sesión e iniciar sesión en la Tienda para ver los nuevos precios en el catálogo.

## Cambiar el grupo de clientes

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Busque la empresa en la cuadrícula y haga clic en **[!UICONTROL Edit]** en la columna _[!UICONTROL Action]_.

   ![Editar compañía](./assets/companies-grid-edit.png){width="700" zoomable="yes"}

1. En la página de empresa, desplácese hacia abajo y expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Advanced Settings]**.

1. Establezca el(la) **[!UICONTROL Customer Group]** apropiado(a).

   La lista [!UICONTROL Customer Group] incluye todos los catálogos compartidos existentes, incluso si Catálogos compartidos está deshabilitado en la configuración.

   ![Cambiar grupo de clientes o catálogo compartido](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL Proceed]**.

1. Haga clic en **[!UICONTROL Save]**.
