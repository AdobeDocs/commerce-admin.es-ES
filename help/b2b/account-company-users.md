---
title: Administrar cuentas de usuario de empresa
description: Obtenga información acerca de las cuentas de usuario de compañía y cómo funcionan dentro de la cuenta de compañía asociada.
exl-id: 36b55f61-e579-4eb8-8f67-0156221d378e
feature: B2B, Companies, User Account, Storefront
role: Admin, User
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Administrar cuentas de usuario de empresa

El administrador de la empresa asigna los usuarios de la empresa y estos son visibles desde el Administrador en _[!UICONTROL Customers]_cuadrícula por tipo de cliente,_[!UICONTROL Company User]_. Estas personas suelen ser compradores con diferentes niveles de permiso para acceder a los servicios y recursos de la tienda.

El administrador de la empresa configura primero [estructura de la empresa](account-company-structure.md)y, a continuación, completa las tareas siguientes según sea necesario:

- Crear usuarios de la empresa y asignar usuarios a equipos

- Defina funciones y permisos, y asigne usuarios a funciones

>[!IMPORTANT]
>
>Solamente el administrador de la empresa puede agregar, editar o eliminar usuarios de la empresa. La eliminación no se puede revertir porque el usuario se ha eliminado de la estructura de la compañía.

## Añadir usuarios de la empresa

1. Desde la tienda, el administrador de la empresa inicia sesión en su cuenta.

1. En el panel izquierdo, elija **[!UICONTROL Company Users]**.

   ![Usuarios de empresa](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Clics **[!UICONTROL Add New User]** y hace lo siguiente:

   - Ingresa el **[!UICONTROL Job Title]** del nuevo usuario.

   - Elige el adecuado **[!UICONTROL User Role]** si las funciones y los permisos están definidos. De lo contrario, pueden volver más tarde para asignar la función.

     ![Añadir nuevo usuario](./assets/company-structure-users-add.png){width="700" zoomable="yes"}

   - Completa los campos restantes según sea necesario para el usuario:

      - **[!UICONTROL First Name]** y **[!UICONTROL Last Name]**
      - **[!UICONTROL Email]**
      - **[!UICONTROL Phone Number]**

   De forma predeterminada, la variable **[!UICONTROL Status]** de la cuenta es `Active`.

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

1. Repite el proceso para crear tantos usuarios de la compañía como sea necesario.

   Los nuevos usuarios aparecen en la lista Usuarios de la empresa, junto con el Administrador de la empresa.

Para ahorrar tiempo durante el primer pedido, el administrador de la empresa puede recordar a cada usuario de la empresa que debe añadir la dirección de facturación y envío predeterminada de la empresa a su [agenda](../customers/account-dashboard-address-book.md).

## Editar usuarios de la empresa

1. Desde la tienda, el administrador de la empresa inicia sesión en su cuenta.

1. En el panel izquierdo, elija **[!UICONTROL Company Users]**.

1. Busca el registro de usuario que se va a actualizar y hace clic en **[!UICONTROL Edit]**.

1. Realiza los cambios necesarios.

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

## Eliminar un usuario de la empresa

1. Desde la tienda, el administrador de la empresa inicia sesión en su cuenta.

1. En el panel izquierdo, elija **[!UICONTROL Company Structure]**.

1. Selecciona el usuario de la empresa en la estructura de la empresa.

1. Clics **[!UICONTROL Delete Selected]**.

   ![Eliminar usuario](./assets/company-structure-delete-user.png){width="600" zoomable="yes"}

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL Delete]**.

En el Administrador, el usuario de la empresa permanece en la lista de [Clientes](../customers/customers-all.md) cuadrícula, pero con un `Inactive` estado.

## Descripciones de campos

| Campo | Descripción |
|--------------|---------------|
| [!UICONTROL Job Title] | El puesto del usuario de la empresa. |
| [!UICONTROL User Role] | El [función](account-company-roles-permissions.md) asignado al usuario de la empresa. Opciones: `Default User` / (otras funciones) |
| [!UICONTROL First Name] | El nombre del usuario de la empresa. |
| [!UICONTROL Last Name] | El apellido del usuario de la empresa. |
| [!UICONTROL Email] | La dirección de correo electrónico del usuario de la empresa. |
| [!UICONTROL Phone Number] | Número de teléfono del usuario de la empresa. |
| [!UICONTROL Status] | El estado de la cuenta de usuario de la empresa. Opciones: `Active` / `Inactive` |

{style="table-layout:auto"}
