---
title: Administrar la jerarquía de la compañía
description: Aprenda a administrar organizaciones B2B con modelos operativos complejos creando jerarquías empresariales
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# Administrar [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponible solo para participantes del programa Beta"}

Los administradores pueden crear un(a) [!UICONTROL Company Hierarchy] asignando compañías relacionadas a una compañía principal designada, que es la compañía situada en la parte superior de la organización. Si [!UICONTROL Company Type] es `Company`, la empresa no forma parte de una organización y es elegible para convertirse en una empresa principal o para ser asignada a una empresa principal existente.

En el Administrador, puede administrar las asignaciones de la compañía editando una compañía y, a continuación, actualizando la configuración de [!UICONTROL Company Hierarchy] para asignar o cancelar la asignación de compañías.

![Cuadrícula de jerarquía de la compañía](./assets/company-detail-hierarchy-current-flag.png){width="700"}

>[!NOTE]
>
>Para obtener más información acerca de la cuadrícula [!UICONTROL Company Hierarchy], consulte las descripciones de los campos [Jerarquía de la compañía](account-company-create.md#company-hierarchy).

## Asignar empresas a una organización

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Cuadrícula de compañías](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. En la cuadrícula [!UICONTROL Companies], abra la página de detalles de la compañía para crear las asignaciones.

   - Para asignar compañías adicionales a una compañía principal existente, seleccione la acción **[!UICONTROL Edit]** para la compañía principal.
   - Para crear una compañía primaria, seleccione la acción **[!UICONTROL Edit]** para que la compañía designe como la compañía primaria.

     No se puede crear una compañía primaria a partir de una compañía primaria o secundaria existente.

1. En la página de detalles de la compañía, expanda **[!UICONTROL Company Hierarchy]**.

   ![Cuadrícula de jerarquía de la compañía](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

   La cuadrícula muestra las asignaciones existentes de la empresa, si las hay. La compañía primaria siempre se coloca en la parte superior de la cuadrícula [!UICONTROL Company Hierarchy]. El marcador `[!UICONTROL Current]` indica la compañía que se está editando.

1. Agregar compañías a la organización matriz.

   - Seleccione **[!UICONTROL Assign Companies]** para elegir de una lista de empresas disponibles.

   - **Seleccionar todo en esta página** o seleccionar uno o más elementos de línea de compañía específicos.

   - Seleccione **[!UICONTROL Assign Selected Companies]**.

   - Complete la asignación de la compañía seleccionando **[!UICONTROL Assign]**.

     ![Asignar empresas a la organización](./assets/assign-selected-companies-hierarchy.png){width="675" zoomable="yes"}

## Quitar la asignación de compañías de una compañía matriz

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Cuadrícula de compañías](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. En la cuadrícula [!UICONTROL Companies], abra la página de detalles de la compañía para la compañía principal seleccionando **[!UICONTROL Edit]**.

1. Vea la lista de empresas asignadas expandiendo **[!UICONTROL Company Hierarchy]**.

1. En la cuadrícula [!UICONTROL Company Hierarchy], anule la asignación de una compañía mediante el control de acción **[!UICONTROL Select]** para elegir **[!UICONTROL Unassign from parent]**.

   ![Quitar la asignación de compañías de una organización principal](./assets/company-hierarchy-grid-unassign.png){width="700" zoomable="yes"}

1. Cuando se le solicite, quite la compañía asignada de la jerarquía seleccionando **[!UICONTROL Unassign]**.
