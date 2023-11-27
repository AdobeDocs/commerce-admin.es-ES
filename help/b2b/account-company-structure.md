---
title: Estructura de cuenta de compañía
description: Obtenga información sobre las estructuras de la empresa y cómo un administrador de la empresa puede definirlas para admitir sus flujos de trabajo y políticas empresariales.
exl-id: 4724b208-b6ac-4de5-9a4c-bc4d68402506
feature: B2B, Companies
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# Estructura de cuenta de compañía

Se puede configurar una cuenta de compañía para reflejar la estructura de la empresa. Inicialmente, la estructura de la empresa incluye solo el administrador de la empresa, pero se puede expandir para incluir equipos de usuarios. Los usuarios pueden estar asociados a equipos u organizados dentro de una jerarquía de divisiones y subdivisiones dentro de la compañía.

![Estructura de la empresa con divisiones](./assets/company-structure-diagram.svg){width="500"}

En el panel de cuentas del administrador de la empresa, la estructura de la empresa se representa como un árbol y consiste inicialmente solo en el administrador de la empresa.

![Estructura de la empresa con el administrador](./assets/company-structure-tree-admin.png){width="600" zoomable="yes"}

Cuando se crea y aprueba la cuenta, el administrador de la empresa puede utilizar la dirección de correo electrónico de la empresa o tener asignada una dirección de correo electrónico diferente.

Es posible que la persona que sirve como administrador de la compañía tenga varias funciones dentro de la compañía. Si se introduce una dirección de correo electrónico independiente para el administrador de la empresa, la estructura inicial de la empresa incluye el administrador de la empresa más una cuenta de usuario individual en el nombre del administrador de la empresa. En tal caso, el administrador de la empresa puede iniciar sesión en la cuenta como empresa o como usuario individual.

![Estructura de la empresa con cuenta de administrador y usuario](./assets/company-structure-tree-admin-user.png){width="600" zoomable="yes"}

Para los comerciantes, la estructura completa de la empresa se refleja en la variable _Compañías_ y _Clientes_ Cuadrículas dentro de Admin. La cuadrícula Compañías enumera todas las compañías independientemente de su estado. El siguiente ejemplo muestra las cuentas de dos compañías: _ACME_ y la _Vendelay_ empresa.

![Cuadrícula de compañías](./assets/companies-grid.png){width="700" zoomable="yes"}

El siguiente ejemplo muestra el [!UICONTROL Customers] cuadrícula con las cuentas iniciales del administrador de la empresa para estas empresas.

![Cuadrícula de clientes con cuenta de administrador de empresa](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

Después de crear la cuenta, el administrador de la empresa debe definir la estructura de la empresa de [equipos](account-company-structure.md), configure el [usuarios de empresa](account-company-users.md), y establecer [funciones y permisos](account-company-roles-permissions.md) para cada uno.

## Iconos de estructura de empresa

| Icono | Descripción |
| ---- | ----------------- |
| ![Icono de administrador de empresa](./assets/company-icon-admin.png) | Representa al administrador de la empresa en la estructura de la empresa. |
| ![Icono de equipo](./assets/company-icon-team.png) | Representa un equipo en la estructura de la compañía. |
| ![Icono de usuario](./assets/company-icon-user.png) | Representa a un usuario en la estructura de la compañía. |
| ![Icono Mover](./assets/company-icon-move.png) | Mueve un equipo a otra posición en la estructura de la compañía. |
| ![Icono de expansión](./assets/company-icon-expand.png) | Amplía un equipo en la estructura de la compañía. |
| ![Contraer icono](./assets/company-icon-collapse.png) | Contrae un equipo en la estructura de la compañía. |

{style="table-layout:auto"}

## Crear equipos de empresa

La estructura de una cuenta de empresa debe reflejar la organización de compra, ya sea simple y plana o una organización compleja con diferentes equipos para cada subdivisión y división de la empresa.

Si el almacén es [configurado](enable-basic-features.md) para permitir que las empresas administren sus propias cuentas, la configuración de la estructura de la empresa es una de las primeras tareas que realiza un administrador de la empresa una vez aprobada la cuenta. En la cuenta de compañía, la estructura de la compañía se representa como un árbol con el administrador de la compañía en la parte superior.

![Estructura de la empresa con equipos](./assets/company-structure-teams-diagram.svg){width="450"}

1. El administrador de la empresa inicia sesión en su cuenta.

1. En el panel izquierdo, elija **[!UICONTROL Company Structure]**.

1. En **[!UICONTROL Business Structure]**, clics **[!UICONTROL Add Team]** y hace lo siguiente:

   - Ingresa el **[!UICONTROL Team Title]** y **[!UICONTROL Description]**.

     El Título de equipo puede ser cualquier elemento que represente la estructura de la compañía, como un equipo, una oficina o una división dentro de la compañía

     ![Agregar equipo](./assets/company-structure-add-team.png){width="700" zoomable="yes"}

   - Cuando termine, haga clic en **[!UICONTROL Save]**.

   - Crea tantos equipos como sea necesario.

     ![Estructura de la empresa con equipos](./assets/company-structure-teams.png){width="600" zoomable="yes"}

1. Para crear una jerarquía de equipos, haga lo siguiente:

   - Selecciona el equipo principal y hace clic en **[!UICONTROL Add Team]**.

     ![Estructura de la empresa con divisiones](./assets/company-structure-northwest-division.png){width="600" zoomable="yes"}

   - Ingresa el **[!UICONTROL Team Title]** y **[!UICONTROL Description]**.

   - Clics **[!UICONTROL Save]**.

1. Repite estos pasos para crear tantos equipos o divisiones y subdivisiones como sea necesario.

   ![Estructura de la empresa con divisiones y subdivisiones](./assets/company-structure-divisions.png){width="600" zoomable="yes"}

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

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL Delete]**.

## Expandir o contraer la estructura del equipo

A medida que el administrador de la empresa trabaja con la estructura de la empresa, puede contraer o expandir el árbol:

- Clics **[!UICONTROL Collapse All]** o **[!UICONTROL Expand All]**.

- Clics ![Icono ampliado](../assets/icon-display-collapse.png) para contraer un equipo o ![Icono contraído](../assets/icon-display-expand.png) para expandir un equipo.

## Asignar usuarios a equipos

Cuando se agregan equipos y usuarios por primera vez a [estructura de la empresa](account-company-structure.md), se colocan en el mismo nivel bajo el administrador de la empresa.

![Estructura de la empresa con usuarios y equipos](./assets/company-users-added.png){width="700" zoomable="yes"}

| Control | Descripción |
|--- |--- |
| [!UICONTROL Collapse All / Expand All] | Contrae o expande el árbol de estructura empresarial |
| [!UICONTROL Add User] | Crea un usuario debajo del equipo actual |
| [!UICONTROL Add Team] | Crea un equipo |
| [!UICONTROL Edit Selected / Delete Selected] | Edita o elimina usuarios del árbol de negocios |

{style="table-layout:auto"}

1. En el panel izquierdo, el administrador de la empresa elige **[!UICONTROL Company Structure]**.

1. Para asignar un usuario a un equipo existente, arrastran (![Icono Mover](../assets/icon-move.png)) el usuario, en el equipo correspondiente.

   ![Asignaciones de equipo](./assets/company-structure-teams-users-assigned.png){width="700" zoomable="yes"}
