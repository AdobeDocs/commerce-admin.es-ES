---
title: Administrar cuentas de usuario de empresa
description: Obtenga información acerca de las cuentas de usuario de compañía y cómo funcionan dentro de la cuenta de compañía asociada.
exl-id: 36b55f61-e579-4eb8-8f67-0156221d378e
feature: B2B, Companies, User Account, Storefront
role: Admin, User
source-git-commit: fec72b792cf3149c05803874795c45f9f4e28673
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 0%

---

# Administrar cuentas de usuario de empresa

En la tienda, el administrador de la empresa asigna los usuarios de la empresa y estos se pueden ver desde la página _[!UICONTROL Company Users]_. Estas personas suelen ser compradores con diferentes niveles de permiso para acceder a los servicios y recursos de la tienda.

El administrador de la empresa configura primero la [estructura de la empresa](account-company-structure.md) y, a continuación, completa las tareas siguientes según sea necesario:

- Crear usuarios de la empresa y asignar usuarios a equipos

- Defina funciones y permisos, y asigne usuarios a funciones

Solo el administrador de la empresa puede agregar, editar, inactivar o eliminar usuarios de la empresa.

- Cuando se elimina un usuario, el estado de la cuenta cambia a *inactivo* y el cliente ya no puede iniciar sesión en la compañía. Los administradores aún pueden acceder a todo el contenido asociado con el usuario. El administrador de cuentas puede restaurar el acceso cambiando el estado de la cuenta a *[!UICONTROL Active]* desde la página [!UICONTROL Company Users].

- Cuando se elimina una cuenta de usuario, la cuenta y el contenido asociado se eliminan de la tienda. Esta acción no se puede revertir.

## Añadir usuarios de la empresa

1. Desde la tienda, el administrador de la empresa inicia sesión en su cuenta.

1. En el panel izquierdo, elija **[!UICONTROL Company Users]**.

   ![Usuarios de la compañía](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Hace clic en **[!UICONTROL Add New User]** y realiza las siguientes acciones:

   - Escribe el(la) **[!UICONTROL Job Title]** del nuevo usuario.

   - Elige el(la) **[!UICONTROL User Role]** apropiado(a) si se definen los roles y permisos. De lo contrario, pueden volver más tarde para asignar la función.

     ![Agregar nuevo usuario](./assets/company-structure-users-add.png){width="700" zoomable="yes"}

   - Agrega la información del usuario en los campos restantes:
      - **[!UICONTROL First Name]** y **[!UICONTROL Last Name]**
      - **[!UICONTROL Email]**
      - **[!UICONTROL Phone Number]**

   De manera predeterminada, **[!UICONTROL Status]** de la cuenta es `Active`.

1. Una vez finalizado, hace clic en **[!UICONTROL Save]**.

1. Repite el proceso para crear tantos usuarios de la compañía como sea necesario.

   Los nuevos usuarios aparecen en la lista Usuarios de la empresa, junto con el Administrador de la empresa.

Para ahorrar tiempo durante el primer pedido, el administrador de la compañía puede recordarle a cada usuario de la compañía que agregue la dirección de facturación y envío predeterminada de la compañía a su [libreta de direcciones](../customers/account-dashboard-address-book.md).

## Quitar un usuario de [!UICONTROL Company structure]

Los administradores de la compañía pueden quitar un usuario de [!UICONTROL Company Structure].

Una vez eliminada una cuenta, el estado de la cuenta de usuario cambia a *inactiva* y el usuario ya no podrá iniciar sesión en la tienda.
El administrador puede reactivar una cuenta editando la información de la cuenta de usuario desde la página Usuarios de la compañía.

1. Desde la tienda, el administrador de la empresa inicia sesión en su cuenta.

1. En el panel izquierdo, elija **[!UICONTROL Company Structure]**.

1. Selecciona el usuario de la empresa en la estructura de la empresa.

1. Clics **[!UICONTROL Remove from Structure]**.

   ![Eliminar usuario](./assets/company-structure-delete-user.png){width="600" zoomable="yes"}

1. Cuando se le pida que confirme, hace clic en **[!UICONTROL Remove]**.

   En el Administrador, el usuario de la compañía permanece en la lista de la cuadrícula [Clientes](../customers/customers-all.md), pero con el estado `Inactive`.

## Ver y administrar las cuentas de usuario de la empresa

Los administradores de la empresa pueden ver y administrar las cuentas de usuario de la empresa mediante los filtros de vista de la página [!UICONTROL Company Users].

![Usuarios de la compañía](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

- Ver solamente los usuarios inactivos seleccionando **[!UICONTROL Show Inactive Users]**.
- Ver solamente los usuarios activos seleccionando **[!UICONTROL Show Active Users]**.
- Ver todos los usuarios seleccionando **[!UICONTROL Show All Users]**.

El administrador de la empresa puede administrar una cuenta individual mediante el elemento de línea *[!UICONTROL Actions]* para editar la información de la cuenta, administrar el estado de la cuenta o eliminar una cuenta.

### Editar información de cuenta de usuario de empresa

Los administradores de la empresa pueden actualizar la información del perfil de la cuenta de usuario y cambiar el estado de la cuenta.

1. En la página [!UICONTROL Company Users], busque la cuenta de usuario que desea actualizar. Haga clic en **[!UICONTROL Edit]**.

1. Realice los cambios necesarios en la información de la cuenta de usuario, incluido el cambio del estado de la cuenta.

1. Aplique los cambios haciendo clic en **[!UICONTROL Save]**.

>[!NOTE]
>
>Si edita una cuenta de usuario de empresa y observa que en el perfil falta la información necesaria de la cuenta, como el puesto y el número de teléfono, indica que la cuenta la agregó un administrador del sitio de Commerce. Estas cuentas no se pueden editar desde la tienda. Para actualizar la información o cambiar el estado de la cuenta, póngase en contacto con el administrador del sitio.

### Desactivar o eliminar una cuenta activa

1. En la página [!UICONTROL Company Users], busque la cuenta de usuario que desea actualizar. Haga clic en **[!UICONTROL Manage]**.

   ![Administrar usuario desde la página Usuarios de la compañía](./assets/company-users-manage-storefront.png){width="600" zoomable="yes"}

1. Cuando se le solicite, desactive o elimine la cuenta de usuario según sea necesario.

>[!IMPORTANT]
>
>Al eliminar una cuenta de usuario de empresa, se elimina la cuenta de y todo el contenido asociado del sistema. Esta acción no se puede revertir.

## Descripciones de los campos de perfil de cuenta de usuario de compañía

| Campo | Descripción |
|--------------|---------------|
| [!UICONTROL Job Title] | El puesto del usuario de la empresa. |
| [!UICONTROL User Role] | [rol](account-company-roles-permissions.md) asignado al usuario de la compañía. Opciones: `Default User` / (otros roles) |
| [!UICONTROL First Name] | El nombre del usuario de la empresa. |
| [!UICONTROL Last Name] | El apellido del usuario de la empresa. |
| [!UICONTROL Email] | La dirección de correo electrónico del usuario de la empresa. |
| [!UICONTROL Phone Number] | Número de teléfono del usuario de la empresa. |
| [!UICONTROL Status] | El estado de la cuenta de usuario de la empresa. Opciones: `Active` / `Inactive` |

{style="table-layout:auto"}
