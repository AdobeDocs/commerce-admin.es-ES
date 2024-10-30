---
title: Estructura de cuenta de compañía
description: Obtenga información sobre las estructuras de la empresa y cómo un administrador de la empresa puede definirlas para admitir sus flujos de trabajo y políticas empresariales.
exl-id: 4724b208-b6ac-4de5-9a4c-bc4d68402506
feature: B2B, Companies
role: Admin
source-git-commit: fec72b792cf3149c05803874795c45f9f4e28673
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---

# Estructura de cuenta de compañía

Se puede configurar una cuenta de compañía para reflejar la estructura de la empresa. Inicialmente, la estructura de la empresa incluye solo el administrador de la empresa, pero se puede expandir para incluir equipos de usuarios. Los usuarios pueden estar asociados a equipos u organizados dentro de una jerarquía de divisiones y subdivisiones dentro de la compañía.

![Estructura de la compañía con divisiones](./assets/company-structure-diagram.svg){width="500"}

En el tablero de cuentas del administrador de la empresa, en la tienda, la estructura de la empresa se representa en forma de árbol y consiste inicialmente únicamente en el administrador de la empresa.

![Estructura de la compañía con el administrador](./assets/company-structure-tree-admin.png){width="700" zoomable="yes"}

Para los comerciantes, la estructura completa de la compañía se refleja en las cuadrículas de _Empresas_ y _Clientes_ dentro del Administrador. La cuadrícula Compañías enumera todas las compañías independientemente de su estado.

![Cuadrícula de compañías](./assets/companies-grid.png){width="700" zoomable="yes"}

En el siguiente ejemplo se muestra la cuadrícula [!UICONTROL Customers] con las cuentas iniciales de administrador de la compañía para cada compañía.

![Cuadrícula de clientes con cuentas de administrador de empresa](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

Después de crear la cuenta, el administrador de la compañía puede definir una estructura de compañía con [equipos](account-company-structure.md), configurar los [usuarios de la compañía](account-company-users.md) y establecer [roles y permisos](account-company-roles-permissions.md) para cada uno.

>[!NOTE]
>
>Cuando se agrega un usuario de compañía, el usuario de compañía se agrega inicialmente a la estructura raíz de la compañía, subordinado al administrador de la compañía. Si el administrador de la empresa desempeña varias funciones dentro de la empresa, cree cuentas de usuario de empresa independientes con una dirección de correo electrónico diferente para cada función.

## Iconos de estructura de empresa

| Icono | Descripción |
| ---- | ----------------- |
| ![Icono de administrador de la empresa](./assets/company-icon-admin.png) | Representa al administrador de la empresa en la estructura de la empresa. |
| ![Icono de equipo](./assets/company-icon-team.png) | Representa un equipo en la estructura de la compañía. |
| ![Icono de usuario](./assets/company-icon-user.png) | Representa a un usuario en la estructura de la compañía. |
| ![Icono de mover](./assets/company-icon-move.png) | Mueve un equipo a otra posición en la estructura de la compañía. |
| ![Icono de expansión](./assets/company-icon-expand.png) | Amplía un equipo en la estructura de la compañía. |
| ![Contraer icono](./assets/company-icon-collapse.png) | Contrae un equipo en la estructura de la compañía. |

{style="table-layout:auto"}

## Crear equipos de empresa

La estructura de una cuenta de empresa debe reflejar la organización de compra, ya sea simple y plana o una organización compleja con diferentes equipos para cada subdivisión y división de la empresa.

Si el almacén está [configurado](enable-basic-features.md) para permitir que las empresas administren sus propias cuentas, configurar la estructura de la empresa es una de las primeras tareas que debe realizar un administrador de empresa una vez aprobada la cuenta. En la cuenta de compañía, la estructura de la compañía se representa como un árbol con el administrador de la compañía en la parte superior.

![Estructura de la compañía con equipos](./assets/company-structure-teams-diagram.svg){width="450"}

1. El administrador de la empresa inicia sesión en su cuenta.

1. En el panel izquierdo, elija **[!UICONTROL Company Structure]**.

1. En **[!UICONTROL Business Structure]**, hace clic en **[!UICONTROL Add Team]** y realiza las siguientes acciones:

   - Escribe **[!UICONTROL Team Title]** y **[!UICONTROL Description]**.

     El Título de equipo puede ser cualquier elemento que represente la estructura de la compañía, como un equipo, una oficina o una división dentro de la compañía

     ![Agregar equipo](./assets/company-structure-add-team.png){width="700" zoomable="yes"}

   - Una vez finalizado, hace clic en **[!UICONTROL Save]**.

   - Crea tantos equipos como sea necesario.

1. Para crear una jerarquía de equipos, el administrador hace lo siguiente:

   - Selecciona el equipo principal y hace clic en **[!UICONTROL Add Team]**.

     ![Estructura de la compañía con divisiones](./assets/company-structure-northwest-division.png){width="600" zoomable="yes"}

   - Escribe **[!UICONTROL Team Title]** y **[!UICONTROL Description]**.

   - Clics **[!UICONTROL Save]**.

1. Repite estos pasos para crear tantos equipos o divisiones y subdivisiones como sea necesario.

   ![Estructura de la compañía con divisiones y subdivisiones](./assets/company-structure-divisions.png){width="600" zoomable="yes"}

## Mover un equipo

A medida que el administrador de la empresa trabaja con la estructura de la empresa, puede arrastrar equipos o divisiones a otras ubicaciones de la estructura.

1. El administrador de la empresa localiza el equipo que se va a mover.

1. Hace clic en y arrastra el equipo a una nueva posición en la estructura de la compañía.

## Eliminación de un equipo

>[!NOTE]
>
>Antes de eliminar un equipo, se recomienda asegurarse de que está seleccionado el equipo correcto: los equipos eliminados no se pueden restaurar.

1. El administrador de la empresa selecciona el equipo que se va a eliminar.

1. Clics **[!UICONTROL Delete Selected]**.

1. Cuando se le pida que confirme, hace clic en **[!UICONTROL Delete]**.

## Expandir o contraer la estructura del equipo

A medida que el administrador de la empresa trabaja con la estructura de la empresa, puede contraer o expandir el árbol:

- Hace clic en **[!UICONTROL Collapse All]** o **[!UICONTROL Expand All]**.

- Hace clic en ![Icono expandido](../assets/icon-display-collapse.png) para contraer un equipo o en ![Icono contraído](../assets/icon-display-expand.png) para expandir un equipo.

## Asignar usuarios a equipos

Cuando los equipos y usuarios se agregan por primera vez a la [estructura de la compañía](account-company-structure.md), se colocan en el mismo nivel bajo el administrador de la compañía.

![Estructura de la compañía con usuarios y equipos](./assets/company-users-added.png){width="700" zoomable="yes"}

| Control | Descripción |
|--- |--- |
| [!UICONTROL Collapse All / Expand All] | Contrae o expande el árbol de estructura empresarial |
| [!UICONTROL Add User] | Crea un usuario debajo del equipo actual |
| [!UICONTROL Add Team] | Crea un equipo |
| [!UICONTROL Edit Selected / Remove from Structure] | Edita la información del usuario o quita usuarios del árbol de negocios. Para obtener más información, consulte [Administrar cuentas de usuario de la compañía](account-company-users.md). |

{style="table-layout:auto"}

1. En el panel izquierdo, el administrador de la empresa elige **[!UICONTROL Company Structure]**.

1. Para asignar un usuario a un equipo existente, arrastra (![Icono de mover](../assets/icon-move.png)) al usuario debajo del equipo correspondiente.

   ![Asignaciones de equipo](./assets/company-structure-teams-users-assigned.png){width="700" zoomable="yes"}
