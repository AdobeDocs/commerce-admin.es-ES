---
title: Administración de empresa
description: Optimice la administración y gestión de las organizaciones B2B con modelos operativos complejos.
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Administración de empresa

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponible solo para participantes del programa Beta"}

La administración de empresas optimiza las operaciones comerciales para empresas con estructuras organizativas complejas. Los usuarios administradores pueden crear una jerarquía de compañías para reflejar una organización B2B asignando compañías a la compañía principal designada. Esta asignación permite al administrador de la empresa matriz ver y administrar las empresas de la organización.

Iniciar tareas de administración de la compañía desde la vista *[!UICONTROL Companies]*. Desde el administrador, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Cuadrícula B2B de administración de compañías](./assets/companies-grid-view.png){width="700" zoomable="yes"}

En *[!UICONTROL Companies grid]*, la columna *[!UICONTROL Company Type]* indica si una compañía está administrada como parte de una organización o como una compañía independiente.

- `Parent` es una organización empresarial con una o más empresas asignadas. No se puede asignar una compañía principal como hijo de otra compañía.

- `Child` es una compañía que se ha asignado a una organización. A una compañía solo se le puede asignar una compañía matriz.

- `Company` representa una sola compañía. Una sola compañía puede formar parte de una organización convirtiéndola en una compañía principal o asignándola a una compañía principal existente.

Cuando edita una compañía principal o secundaria, expanda *[!UICONTROL Company Hierarchy]* para ver todas las compañías de la organización. Un marcador `Current` indica la compañía que está editando.

![Cuadrícula de jerarquía de compañía B2B](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}


## Ver y configurar [!UICONTROL Company Hierarchy]

En la creación inicial de la compañía, la cuadrícula [!UICONTROL Company Hierarchy] está vacía. También está vacío si la empresa es una sola empresa.

![Cuadrícula de jerarquía de la compañía B2B](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

Para las empresas principales, los usuarios administradores con los permisos adecuados pueden completar las siguientes tareas:

- Genere la jerarquía de compañías creando una nueva organización principal o actualizando una existente.
- Administre una organización existente para agregar o quitar compañías.

Para obtener más información, consulte [Administrar la jerarquía de la compañía](assign-companies.md).
