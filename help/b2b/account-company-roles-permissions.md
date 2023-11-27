---
title: Funciones de la compañía y permisos
description: Obtenga información sobre las funciones y los permisos que un administrador de la empresa puede aplicar a los usuarios de la empresa, lo que permite varios niveles de acceso a la información y los recursos de los pedidos.
exl-id: 9fe20d6a-2c9c-4618-a395-805d64dcf0de
feature: B2B, Companies, Roles/Permissions
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# Roles y permisos de la compañía

Las funciones de los usuarios de la empresa se configuran con varios niveles de permisos para acceder a la información y los recursos de ventas. De forma predeterminada, el administrador de la empresa es un _superusuario_ con permisos completos. El [Acceso denegado](../content-design/pages.md#access-denied) página aparece si el usuario no tiene permiso para acceder a la página.

![Página Roles y permisos con rol predeterminado](./assets/company-roles-permissions.png){width="700" zoomable="yes"}

El sistema tiene una función de usuario predeterminado predefinida que puede utilizar _como está_ o modifique para adaptarlo a sus necesidades. Puede crear tantas funciones como sea necesario para adaptarse a la estructura de su empresa y a las responsabilidades organizativas, como las siguientes:

- **Usuario predeterminado** — El usuario por defecto tiene acceso completo a las actividades relacionadas con las ventas y presupuestos, y acceso de sólo consulta a la información de perfil de la empresa y de crédito.

- **Comprador principal** — Un comprador principal podría tener acceso a todos los recursos de Ventas y Ofertas y permisos de sólo consulta para el Perfil de la compañía, el Usuario y los equipos, la Información de pago y el Crédito de la compañía.

- **Comprador asistente** — Es posible que un comprador asistente tenga permiso para realizar un pedido utilizando _Cierre de compra con presupuesto_ y para ver pedidos, presupuestos e información en el perfil de la empresa.

## Administración de funciones y permisos

1. El administrador de la empresa inicia sesión en su cuenta de la tienda.

1. En el panel izquierdo, elija **[!UICONTROL Roles and Permissions]**.

1. Completa cualquiera de las siguientes tareas.

### Crear una función

1. Clics **[!UICONTROL Add New Role]**.

   ![Agregar nuevo rol](./assets/company-roles-permissions-add-storefront.png){width="600" zoomable="yes"}

1. Introduce un elemento descriptivo **[!UICONTROL Role Name]**.

1. En _[!UICONTROL Role Permissions]_, realiza una de las siguientes acciones:

   - Activa la casilla de verificación de cada recurso o actividad para el que los usuarios asignados a la función tienen permiso de acceso.

   - Selecciona el **[!UICONTROL All]** y borra la casilla de verificación de cada recurso o actividad al que los usuarios asignados a la función no tienen permiso de acceso.

1. Clics **[!UICONTROL Save Role]**.

1. Crea tantas funciones como sea necesario repitiendo estos pasos.

### Modificación de un rol

1. Para modificar la función, el administrador de la empresa hace clic en **[!UICONTROL Edit]** en el _[!UICONTROL Actions]_columna.

1. Realiza los cambios necesarios en la configuración de nombre y permisos.

1. Cuando termine, haga clic en **[!UICONTROL Save Role]**.

### Duplicación de un rol

1. Para duplicar la función, el administrador de la empresa hace clic en **[!UICONTROL Duplicate]** en el _[!UICONTROL Actions]_columna.

1. Realiza los cambios necesarios en la configuración de nombre y permisos.

1. Cuando termine, haga clic en **[!UICONTROL Save Role]**.

### Eliminar un rol

1. El administrador de la empresa encuentra la función que se va a eliminar en la lista de funciones.

   Solo se pueden eliminar los roles sin usuarios asignados.

1. Clics **[!UICONTROL Delete]** en el _[!UICONTROL Actions]_columna.

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL OK]**.

## Acciones

| Acción | Descripción |
|-----------| ----------- |
| [!UICONTROL Duplicate] | Crea una copia del rol seleccionado. El nombre de la función duplicada tiene `- Duplicated` se ha añadido al final. |
| [!UICONTROL Edit] | Cambie el nombre o el conjunto de permisos. |
| [!UICONTROL Delete] | Elimine la función. Solo se pueden eliminar los roles sin usuarios asignados. |

{style="table-layout:auto"}

## Permisos de funciones

- Todo
   - Ventas
      - Permitir cierre de compra (realizar pedido)
         - Utilizar el método de pago a cuenta
      - Ver pedidos
         - Ver pedidos de usuarios subordinados
- Comillas
   - Ver
      - Solicitar, Editar, Eliminar
      - Cierre de compra con cotización
      - Ver las comillas de los usuarios subordinados
- Aprobaciones de pedidos
   - Ver mis pedidos de compra
      - Ver para subordinados
      - Ver para toda la compañía
   - Aprobación automática de pedidos creados dentro de este rol
   - Aprobar pedidos sin otras aprobaciones
   - Ver reglas de aprobación
      - Crear, editar y eliminar
- Perfil de empresa
   - Información de la cuenta (vista)
      - Editar
   - Dirección legal
      - Editar
   - Contactos (vista)
   - Información de pago (vista)
   - Información de envío (vista)
- Administración de usuarios de empresa
   - Ver funciones y permisos
      - Administración de funciones y permisos
   - Ver usuarios y equipos
      - Administrar usuarios y equipos
- Crédito de empresa
   - Ver

## Asignar una función a un usuario de la empresa

Después de definir las funciones necesarias, el administrador de la empresa asigna una función a cada usuario de la empresa.

1. Inicia sesión en su cuenta de empresa como administrador de la empresa.

1. En el panel izquierdo, elija **[!UICONTROL Company Users]**.

   ![Usuarios de empresa](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Busca el usuario en la lista y hace clic en **[!UICONTROL Edit]**.

1. Elige el adecuado **[!UICONTROL User Role]** para el usuario.

   ![Editar usuario: elija un rol de usuario](./assets/company-user-assign-role.png){width="700" zoomable="yes"}

1. Clics **[!UICONTROL Save]**.
