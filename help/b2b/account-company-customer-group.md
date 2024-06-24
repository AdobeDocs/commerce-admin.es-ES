---
title: Asignar un grupo de clientes a una empresa
description: Obtenga información acerca de cómo asignar un grupo de clientes a una cuenta de compañía en su tienda de Adobe Commerce.
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
source-git-commit: a5a8da076d6cd91eb6c3e573fec5b3fb9d2d3341
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Asignar un grupo de clientes a una empresa

Asignar un grupo de clientes a una empresa es esencialmente lo mismo que asignar un catálogo compartido. Si el catálogo compartido no es [habilitado en la configuración](enable-basic-features.md), un grupo de clientes (en lugar de un catálogo compartido) se asigna a una empresa.

>[!NOTE]
>
> Solo se puede asignar un grupo de clientes o un catálogo compartido a una compañía a la vez. No se puede eliminar un grupo de clientes asociado a un catálogo compartido.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Busque la empresa en la cuadrícula y haga clic en **[!UICONTROL Edit]** en el _[!UICONTROL Action]_columna.

   ![Editar compañía](./assets/companies-grid-edit.png){width="700" zoomable="yes"}

1. En la página de empresa, desplácese hacia abajo y expanda ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Advanced Settings]** sección.

1. Configure las variables apropiadas **[!UICONTROL Customer Group]**.

   >[!NOTE]
   >
   >El [!UICONTROL Customer Group] La lista incluye todos los catálogos compartidos existentes, incluso si Catálogos compartidos está desactivado en la configuración.

   Al cambiar el grupo de clientes asignado a la empresa, se actualizan los perfiles de todos los miembros de la empresa.

   >[!NOTE]
   >
   >Después de cambiar el grupo de la compañía, un usuario de la compañía debe cerrar la sesión e iniciar sesión en la Tienda para ver los nuevos precios en el catálogo.

   ![Cambiar el grupo de clientes o el catálogo compartido](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

   >[!NOTE]
   >
   >Si la asignación del grupo de clientes se cambia de un catálogo compartido a un grupo de clientes normal, los miembros de la empresa pierden el acceso al catálogo compartido y el catálogo principal pasa a estar disponible para ellos desde la tienda.

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL Proceed]**.

1. Clic **[!UICONTROL Save]**.
