---
title: Administrar la jerarquía de la compañía
description: Cree y gestione jerarquías empresariales para apoyar a las organizaciones B2B con modelos operativos complejos.
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 6b06f52eb4ee8ca136a1c60fd6dc04a9ac96bbfa
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# Administrar [!UICONTROL Company Hierarchy]

Los administradores pueden crear un(a) [!UICONTROL Company Hierarchy] asignando compañías relacionadas a una compañía primaria designada, que es la compañía en la parte superior de la jerarquía organizativa.

Desde el Administrador, cree una compañía principal editando una compañía individual (`[!UICONTROL Company Type] = Company`) y asignando compañías relacionadas en la configuración de [!UICONTROL Company Hierarchy].

![Cuadrícula de jerarquía de la compañía](./assets/company-hierarchy-grid.png){width="700"}


>[!NOTE]
>
>Para obtener más información acerca de la cuadrícula [!UICONTROL Company Hierarchy], consulte las descripciones de los campos [Jerarquía de la compañía](account-company-create.md#company-hierarchy).

Administre las asignaciones de la compañía editando una compañía principal y utilizando la cuadrícula *[!UICONTROL Company Hierarchy]* para agregar o quitar compañías. Use el control *[!UICONTROL Actions]* para administrar la [configuración avanzada](#change-company-settings) para las empresas de la organización.

## Asignar compañías a una compañía matriz

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Cuadrícula de compañías](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. En la cuadrícula [!UICONTROL Companies], abra la página de detalles de la compañía para crear las asignaciones.

   - Para asignar compañías adicionales a una compañía principal existente, seleccione la acción **[!UICONTROL Edit]** para la compañía principal.
   - Para crear una compañía primaria, seleccione la acción **[!UICONTROL Edit]** para la compañía designada como la compañía primaria.

     No se puede crear una nueva empresa principal a partir de una empresa principal o secundaria existente.

1. En la página Detalles de la compañía, expanda **[!UICONTROL Company Hierarchy]** y, a continuación, seleccione **[!UICONTROL Assign Companies]**.

   ![Crear empresa principal](./assets/company-hierarchy-grid.png){width="675" zoomable="yes"}

1. En la lista de empresas disponibles, elija las empresas que desea asignar y, a continuación, seleccione **[!UICONTROL Assign Selected Companies]**.

   ![Seleccionar empresas para asignar](./assets/company-hierarchy-select-companies-assign.png){width="675" zoomable="yes"}

1. Cuando se le solicite, complete la asignación de la compañía seleccionando **[!UICONTROL Assign]**.

## Quitar la asignación de compañías de una compañía matriz

1. En la página Compañías, abra la página de detalles de la compañía para la compañía principal seleccionando la acción **[!UICONTROL Edit]**.

   ![Página de detalles de la empresa principal](./assets/company-update.png){width="700" zoomable="yes"}

1. Vea la lista de empresas asignadas expandiendo **[!UICONTROL Company Hierarchy]**.

1. Elimine la empresa de la organización.

   - En la columna [!UICONTROL Action] para que la compañía elimine, **[!UICONTROL Select]** > **[!UICONTROL Unassign from parent]**.

     ![Quitar una compañía de una organización](./assets/company-hierarchy-grid-unassign.png){width="640" zoomable="yes"}

   - Cuando se le solicite, quite la compañía asignada de la jerarquía seleccionando **[!UICONTROL Unassign]**.

## Administrar la configuración de empresa de una organización

Actualice la configuración [Configuración avanzada](account-company-create.md#advanced-settings) de una organización para aplicar la configuración principal a todas las compañías secundarias o para aplicar la misma configuración a las compañías seleccionadas de la organización.

Durante el proceso de actualización, los valores de configuración inicial se establecen de forma predeterminada en los valores actuales configurados para la empresa principal. Debe cambiar al menos una configuración para actualizar la configuración de las empresas seleccionadas.

**Cambiar la configuración de configuración avanzada para varias empresas**

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. En la cuadrícula [!UICONTROL Companies], edite la compañía principal seleccionando **[!UICONTROL Edit]** en la columna **[!UICONTROL Action]**.

1. En la página de detalles de la empresa principal, expanda la sección **[!UICONTROL Company Hierarchy]** para ver las empresas incluidas en la organización.

1. Seleccione las empresas que desea configurar.

   ![Seleccionar compañías de la jerarquía de compañías](assets/company-hierarchy-select-companies.png){width="675" zoomable="yes"}

1. Desde el control **[!UICONTROL Actions]** situado sobre la cuadrícula, seleccione **[!UICONTROL Change company settings]**.

   ![Cambiar la configuración de la empresa para la jerarquía de la empresa](assets/company-hierarchy-change-company-settings-action.png){width="675" zoomable="yes"}

1. Cambie la configuración.

   - En la página [!UICONTROL Change company settings], busque la opción de configuración que desea modificar.

   - Seleccione la casilla de verificación **[!UICONTROL Change]** para habilitar la configuración.

   - Actualice el valor según sea necesario.

     ![Cambiar la configuración de la empresa para varias empresas](assets/company-hierarchy-change-settings-config.png){width="575" zoomable="yes"}

1. Después de actualizar la configuración, seleccione **[!UICONTROL Apply Changes]**.

1. Cuando se le pida, seleccione **[!UICONTROL Change settings]** para actualizar la configuración de las empresas seleccionadas.

>[!TIP]
>
>Administre la configuración avanzada de una sola empresa editando el elemento de línea de la empresa.
