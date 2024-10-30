---
title: Administración de empresa
description: Optimice la administración y gestión de las organizaciones B2B con modelos operativos complejos.
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 6b06f52eb4ee8ca136a1c60fd6dc04a9ac96bbfa
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# Administración de empresa

La administración de empresas optimiza las operaciones comerciales para empresas con estructuras organizativas complejas. Los usuarios administradores pueden crear una jerarquía de compañías para reflejar una organización B2B asignando compañías a la compañía principal designada. Esta asignación permite al administrador de la empresa matriz ver y administrar las empresas de la organización.

Iniciar tareas de administración de la compañía desde la vista *[!UICONTROL Companies]*. Desde el administrador, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Cuadrícula B2B de administración de compañías](./assets/companies-grid-view.png){width="700" zoomable="yes"}

La columna *[!UICONTROL Company Type]* indica si una empresa está administrada como parte de una organización o como una empresa independiente.

- `Parent` es una organización empresarial con una o más empresas asignadas. No se puede asignar una compañía principal como hijo de otra compañía.

- `Child` es una compañía que se ha asignado a una organización. A una compañía solo se le puede asignar una compañía matriz.

- `Company` representa una sola compañía. Una sola compañía puede formar parte de una organización convirtiéndola en una compañía principal o asignándola a una compañía principal existente.

Cuando edita una compañía principal o secundaria, expanda *[!UICONTROL Company Hierarchy]* para ver todas las compañías de la organización. Un marcador `Current` indica la compañía que está editando.

![Cuadrícula de jerarquía de compañía B2B](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

## Ver y configurar [!UICONTROL Company Hierarchy]

En la creación inicial de la compañía, la cuadrícula *[!UICONTROL Company Hierarchy]* está vacía. También está vacío si la empresa es una sola empresa.

![Cuadrícula de jerarquía de la compañía B2B](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

Si la compañía es una compañía matriz de una organización y las cuentas de compañía de otras empresas de la organización ya se han configurado en Adobe Commerce, los usuarios administradores con los permisos adecuados pueden asignar compañías y utilizar la cuadrícula *[!UICONTROL Company Hierarchy]* para completar otras tareas de administración de la compañía:

- Ver todas las compañías asociadas con la compañía matriz.
- En la página de detalles de una compañía matriz, asigne más compañías a la organización.
- Quitar una compañía de una organización mediante la acción *[!UICONTROL Unassign from parent]*.
- Actualice la configuración de *[!UICONTROL Advanced Settings]* para aplicar la misma configuración a varias empresas.

Para obtener instrucciones detalladas, consulte [Administrar la jerarquía de la compañía](manage-company-hierarchy.md).

