---
title: Roles de compañía de B2B y permisos de tienda
description: Aprenda a asignar funciones de tienda B2B y permisos para usuarios de la empresa en Adobe Commerce. Defina el acceso a ventas, pedidos, ofertas y otros recursos.
solution: Commerce
feature: B2B, Companies, Roles/Permissions
feature-set: Commerce
role: Admin
level: Intermediate
exl-id: 9fe20d6a-2c9c-4618-a395-805d64dcf0de
source-git-commit: d3c5f0da47bfd951431213050546e865c6ab35ec
workflow-type: tm+mt
source-wordcount: '1193'
ht-degree: 0%

---

# Funciones de la compañía y permisos

Puede configurar funciones para usuarios de la empresa con varios niveles de permisos para acceder a la información y los recursos de ventas. De manera predeterminada, el administrador de la empresa es un *superusuario* con permisos completos. La página [Acceso denegado](../content-design/pages.md#access-denied) aparece si un usuario no tiene permiso para acceder a la página.

![Página de roles y permisos con el rol predeterminado](./assets/company-roles-permissions.png){width="700" zoomable="yes"}

El sistema tiene una función de usuario predeterminado predefinida, que puede usar *tal cual* o modificar para adaptarla a sus necesidades. Puede crear tantas funciones como sea necesario para adaptarse a la estructura de su empresa y a las responsabilidades organizativas, como las siguientes:

- **Usuario predeterminado**: el usuario predeterminado tiene acceso completo a las actividades relacionadas con ventas y presupuestos, así como acceso de sólo lectura al perfil de la compañía y a la información de crédito.

- **Comprador sénior**: Un comprador sénior podría tener acceso a todos los recursos de Ventas y Ofertas y permisos de sólo lectura para el Perfil de la compañía, Usuarios y equipos, Información de pago y Crédito de la compañía.

- **Comprador asistente**: un comprador asistente puede tener permiso para realizar un pedido con **[!UICONTROL Checkout with quote]** y para ver pedidos, ofertas e información en el perfil de la compañía.

## Administración de funciones y permisos

Administre los roles de compañía desde la cuenta de tienda del administrador de la empresa.

**To open Roles and Permissions:**

1. Sign in to the storefront as the company administrator.

1. In the left panel, select **[!UICONTROL Roles and Permissions]**.

1. Complete una de las siguientes tareas.

### Crear una función

1. Haga clic en **[!UICONTROL Add New Role]**.

   ![Agregar nuevo rol](./assets/company-roles-permissions-add-storefront.png){width="600" zoomable="yes"}

1. Escriba un **[!UICONTROL Role Name]** descriptivo.

1. En **[!UICONTROL Role Permissions]**, realice una de las siguientes acciones:

   - Seleccione la casilla de verificación de cada recurso o actividad al que los usuarios asignados a la función tienen permiso de acceso.

   - Seleccione la casilla de verificación **[!UICONTROL All]** y desmarque la casilla de verificación de cada recurso o actividad al que los usuarios asignados a la función no tengan permiso de acceso.

1. Haga clic en **[!UICONTROL Save Role]**.

1. Repita estos pasos para crear tantas funciones como necesite.

### Modificación de un rol

1. Busque la función que desea modificar y haga clic en **[!UICONTROL Edit]** en la columna **[!UICONTROL Actions]**.

1. Realice los cambios necesarios en la configuración de nombre y permisos.

1. Cuando termine, haga clic en **[!UICONTROL Save Role]**.

### Duplicación de un rol

1. Busque la función que desea duplicar y haga clic en **[!UICONTROL Duplicate]** en la columna **[!UICONTROL Actions]**.

1. Realice los cambios necesarios en la configuración de nombre y permisos.

1. Cuando termine, haga clic en **[!UICONTROL Save Role]**.

### Eliminar un rol

1. En la lista de funciones, busque la función que desea eliminar.

   Solo se pueden eliminar los roles sin usuarios asignados.

1. Haga clic en **[!UICONTROL Delete]** en la columna **[!UICONTROL Actions]**.

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL OK]**.

## Acciones de lista de roles {#actions}

| Acción | Descripción |
| --- | --- |
| [!UICONTROL Duplicate] | Crea una copia del rol seleccionado. El nombre de la función duplicada tiene `- Duplicated` agregado al final. |
| [!UICONTROL Edit] | Cambia el nombre y el conjunto de permisos. |
| [!UICONTROL Delete] | Elimina la función. Solo se pueden eliminar los roles sin usuarios asignados. |

{style="table-layout:auto"}

## Permisos de funciones

Las capacidades B2B están cerradas por **permisos** (recursos ACL). Cuando un usuario de una empresa abre una página o ejecuta una acción en la tienda, la aplicación comprueba si su función incluye el permiso requerido.

Los administradores de la compañía pueden actualizar la configuración de permisos para un rol seleccionando **[!UICONTROL Edit]** y, a continuación, seleccionando o borrando permisos en la lista **[!UICONTROL Role Permissions]**.

![Lista de roles y permisos](./assets/role-permissions-list.png){width="700" zoomable="yes"}

Asigne estos recursos cuando **cree o edite un rol de compañía** en la cuenta de compañía. Los usuarios con permiso para administrar funciones pueden abrir el formulario de funciones y establecer el árbol de permisos.

Los permisos de funciones se organizan en una estructura de árbol, con opciones principales y subordinadas. Al seleccionar una opción principal se seleccionan automáticamente todas las opciones subordinadas. Al borrar una opción principal se borran automáticamente todas las opciones subordinadas. También puede seleccionar o borrar opciones subordinadas individualmente.

### Todos los permisos

| Etiqueta de permiso | Descripción |
| --- | --- |
| Todo | Nodo raíz para **todos** los permisos asignados a esta función de tienda. |

### Permisos de ventas

| Etiqueta de permiso | Descripción |
| --- | --- |
| Ventas | Principal para el cierre de compra y la visibilidad del pedido para los usuarios de la empresa. |
| Permitir cierre de compra | Realizar pedidos al finalizar la compra. |
| Utilizar el método de pago a cuenta | Use **Pagar en la cuenta** (crédito de la compañía) al pagar cuando esté disponible. |
| Ver pedidos | Ver los pedidos propios del usuario. |
| Ver pedidos de usuarios subordinados | Ver los pedidos realizados por los usuarios debajo de este usuario en la jerarquía. |

### Permisos de comillas

Parent node in the company permission tree: **Quotes**.

| Permission label | Descripción |
| --- | --- |
| Comillas | Principal para acciones de presupuesto negociable de tienda. |
| Ver (comillas) | Ver ofertas negociables. |
| Solicitar, Editar, Eliminar | Solicite nuevas ofertas, edite las ofertas y elimínelas según las reglas comerciales. |
| Cierre de compra con cotización | Complete el cierre de compra con un presupuesto aprobado. |
| Administrar presupuestos de usuarios subordinados | Principal para acciones en comillas de subordinados. |
| Ver (comillas subordinadas) | Ver ofertas de subordinados. |
| Editar (comillas subordinadas) | Editar las comillas de los subordinados. |
| Eliminar (comillas subordinadas) | Elimine las comillas subordinadas. |

### Plantillas de presupuesto

Nodo principal: **Plantillas de presupuesto** (en **Ofertas** en el árbol de compañías).

| Etiqueta de permiso | Descripción |
| --- | --- |
| Plantillas de presupuesto | Principal para las funciones de plantilla de presupuesto en la tienda. |
| Ver (plantillas) | Ver plantillas de presupuesto. |
| Solicitar, Editar, Eliminar | Cree, actualice, cancele y administre plantillas de presupuesto. |
| Generación de presupuestos a partir de plantillas | Generar presupuestos negociables a partir de plantillas. |
| Administrar plantillas de presupuesto de usuarios subordinados | Principal para acciones de plantilla subordinada. |
| Ver (plantillas de subordinadas) | Ver plantillas de oferta de subordinados. |
| Editar (plantillas de subordinadas) | Editar plantillas de oferta de subordinados. |
| Eliminar (plantillas de subordinadas) | Eliminar plantillas de oferta de subordinados. |

### Aprobaciones de pedidos

Nodo principal: **Aprobaciones de pedidos**. Los permisos de las reglas de orden de compra y aprobación están anidados en esta rama del árbol.

### Pedidos de compra

| Etiqueta de permiso | Descripción |
| --- | --- |
| Aprobaciones de pedidos | Principal para las funciones de pedido de compra y aprobación. |
| Ver mis pedidos de compra | Ver los pedidos de compra que ha creado este usuario. |
| Ver para subordinados | Ver pedidos de compra de usuarios por debajo de este usuario en la jerarquía. |
| Ver para toda la compañía | Ver pedidos de compra de la compañía. |
| Aprobación automática de pedidos creados dentro de este rol | Apruebe automáticamente los pedidos de compra creados por los usuarios con esta función cuando las reglas lo permitan. |

### Reglas de pedidos de compra

| Etiqueta de permiso | Descripción |
| --- | --- |
| Aprobar pedidos sin otras aprobaciones | Apruebe pedidos de compra incluso cuando normalmente se requerirían otras aprobaciones (por reglas de aprobación). |
| Ver reglas de aprobación | View purchase order approval rules. |
| Create, Edit and Delete | Create, edit, and delete approval rules. |

### Perfil de empresa y contactos

Permisos de tienda para secciones de perfil de empresa. Las entradas de **Edit** anidadas solo se aplican con el permiso **View** por encima de ellas en el árbol de funciones.

| Etiqueta de permiso | Descripción |
| --- | --- |
| Perfil de empresa | Acceda a las áreas de perfil de la empresa como grupo. |
| Información de la cuenta (vista) | Ver información de cuenta de empresa. |
| Editar | Editar la información de cuenta de la empresa (en Información de la cuenta). |
| Dirección legal (Ver) | Ver la dirección legal de la compañía. |
| Edit | Edit the company legal address (under Legal Address). |
| Contacts (View) | View company contacts. |
| Payment Information (View) | Ver información de pago en el perfil de la empresa. |
| Información de envío (vista) | Ver información de envío en el perfil de la empresa. |

## Administración de usuarios de empresa

| Etiqueta de permiso | Descripción |
| --- | --- |
| Administración de usuarios de empresa | Principal para funciones y para usuarios o equipos. |
| Ver funciones y permisos | Ver las funciones de la empresa y sus permisos. |
| Administración de funciones y permisos | Cree o edite funciones y asigne permisos. |
| Ver usuarios y equipos | Ver usuarios y equipos de la empresa. |
| Administrar usuarios y equipos | Agregar, editar o quitar usuarios y equipos. |

## Crédito de empresa

| Etiqueta de permiso | Descripción |
| --- | --- |
| Crédito de empresa | Acceda al área de crédito de la empresa. |
| Ver (historial de crédito) | Ver el historial de crédito de la empresa y la información de saldo relacionada. |

## Asignar una función a un usuario de la empresa

Después de definir las funciones que necesita, asigne una función a cada usuario de la compañía.

**Para asignar un rol:**

1. Inicie sesión en la tienda como administrador de la empresa.

1. En el panel izquierdo, seleccione **[!UICONTROL Company Users]**.

   ![Usuarios de la compañía](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Busque el usuario en la lista y haga clic en **[!UICONTROL Edit]**.

1. Seleccione el(la) **[!UICONTROL User Role]** apropiado(a) para el usuario.

   ![Editar usuario: elija un rol de usuario](./assets/company-user-assign-role.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>- [Administrar usuarios de la compañía](account-company-users.md)
>- [Estructura de cuenta de la compañía](account-company-structure.md)
>- [Función de administrador de la empresa](account-company-admin.md)
>- [Administrar compañías](manage-companies.md)
>- [Habilitar características B2B](enable-basic-features.md)
