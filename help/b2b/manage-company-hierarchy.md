---
title: Administrar jerarquías de empresa
description: Cree y gestione jerarquías empresariales para apoyar a las organizaciones B2B con modelos operativos complejos.
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 1fc1e07f20e2c22ac430f384e9e2b278edae405c
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 0%

---

# Administrar jerarquías de empresa

La característica [!UICONTROL Company Hierarchy] le permite organizar varias empresas relacionadas en una sola estructura de empresa principal. Esto es ideal para empresas con filiales, franquicias, varias ubicaciones o estructuras organizativas complejas que necesitan una administración centralizada y, al mismo tiempo, mantener las identidades de cada empresa.

## Casos de uso

* **Centralizar la administración**: aplique la configuración en varias compañías desde una sola compañía principal
* **Mantener estructura**: organiza las compañías en una jerarquía lógica que refleje su organización empresarial
* **Operaciones optimizadas**: administre ofertas, pedidos de compra, métodos de pago y configuración de envío para toda la organización
* **Conservar autonomía**: las empresas individuales conservan su identidad y se benefician de las configuraciones compartidas

## Requisitos previos

Antes de crear una jerarquía de compañías, asegúrese de lo siguiente:

* Las funciones B2B están habilitadas en la instalación de Commerce
* Tiene acceso de administrador para administrar empresas
* Las compañías principales y secundarias ya se han creado como compañías individuales
* Entiende que la aplicación de la configuración principal anula las configuraciones de empresa secundarias existentes

## Cómo funciona

Los administradores pueden crear una jerarquía de compañías asignando compañías relacionadas a una compañía principal designada, que es la compañía en la parte superior de la jerarquía organizativa.

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

   * Para asignar compañías adicionales a una compañía principal existente, seleccione la acción **[!UICONTROL Edit]** para la compañía principal.
   * Para crear una compañía primaria, seleccione la acción **[!UICONTROL Edit]** para la compañía designada como la compañía primaria.

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

   * En la columna [!UICONTROL Action] para que la compañía elimine, **[!UICONTROL Select]** > **[!UICONTROL Unassign from parent]**.

     ![Quitar una compañía de una organización](./assets/company-hierarchy-grid-unassign.png){width="640" zoomable="yes"}

   * Cuando se le solicite, quite la compañía asignada de la jerarquía seleccionando **[!UICONTROL Unassign]**.

## Administrar la configuración de empresa de una organización

Actualice la configuración de [Configuración avanzada](account-company-create.md#advanced-settings) para una organización. Puede:

* Aplicar las opciones de configuración principales a todas las compañías secundarias
* Aplicar la misma configuración a las empresas seleccionadas de la organización

Puede aplicar cualquiera de las siguientes configuraciones:

* **Administración de presupuestos**: habilita o deshabilita la capacidad de las empresas para solicitar y administrar presupuestos
* **Pedidos de compra**: controla si las empresas pueden crear y administrar pedidos de compra
* **Configuración del método de pago**: define qué métodos de pago están disponibles para las empresas
* **Configuración del método de pago**: configure parámetros y límites específicos del método de pago
* **Disponibilidad del método de envío**: establece los métodos de envío que pueden usar las empresas
* **Configuración del método de envío**: define la configuración y las restricciones del método de envío

Durante el proceso de actualización, los valores de configuración inicial se establecen de forma predeterminada en los valores actuales configurados para la empresa principal. Debe seleccionar la casilla de verificación de cambio de al menos una configuración para aplicar la configuración a las empresas seleccionadas. También puede actualizar el valor predeterminado para cada configuración antes de aplicar los cambios.

>[!WARNING]
>
>La aplicación de la configuración de empresa principal sustituye a las configuraciones de empresa secundarias existentes, incluidos los límites de crédito, los métodos de pago, la configuración de envío y las restricciones personalizadas. Después de aplicar la configuración, aún puede administrar y personalizar la configuración avanzada para compañías principales y secundarias individuales al editar el elemento de línea de la compañía.

### Prácticas recomendadas

Cuando aplique la configuración de empresa principal a empresas secundarias, tenga en cuenta las siguientes prácticas recomendadas:

* Revise la configuración de empresa secundaria existente antes de aplicar las configuraciones principales
* Pruebe primero los cambios de configuración en una compañía secundaria única
* Comunicar los cambios a los administradores de la empresa que puedan verse afectados

### Aplicar la configuración principal a las compañías secundarias

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. En la cuadrícula [!UICONTROL Companies], edite la compañía principal seleccionando **[!UICONTROL Edit]** en la columna **[!UICONTROL Action]**.

1. En la página de detalles de la empresa principal, expanda la sección **[!UICONTROL Company Hierarchy]** para ver las empresas incluidas en la organización.

1. Seleccione las empresas que desea configurar.

   ![Seleccionar compañías de la jerarquía de compañías](assets/company-hierarchy-select-companies.png){width="675" zoomable="yes"}

1. Desde el control **[!UICONTROL Actions]** situado sobre la cuadrícula, seleccione **[!UICONTROL Change company settings]**.

   ![Cambiar la configuración de la empresa para la jerarquía de la empresa](assets/company-hierarchy-change-company-settings-action.png){width="675" zoomable="yes"}

1. Cambie la configuración.

   * En la página [!UICONTROL Change company settings], busque la opción de configuración que desea modificar.

   * Seleccione la casilla de verificación **[!UICONTROL Change]** para habilitar la configuración.

   * Actualice el valor si es necesario.

     ![Cambiar la configuración de la empresa para varias empresas](assets/company-hierarchy-change-settings-config.png){width="575" zoomable="yes"}

1. Después de actualizar la configuración, seleccione **[!UICONTROL Apply Changes]**.

1. Cuando se le pida, seleccione **[!UICONTROL Change settings]** para actualizar la configuración de las empresas seleccionadas.

>[!MORELIKETHIS]
>
>* [Crear una cuenta de compañía](account-company-create.md) - Aprenda a crear compañías individuales antes de crear jerarquías
>* [Roles y permisos de la compañía](account-company-roles-permissions.md): comprenda el acceso de los usuarios dentro de las estructuras de la compañía
>* [Administración de crédito de la compañía](credit-company.md) - Configurar límites de crédito y términos de pago para las compañías
>* [Administrar compañías](manage-companies.md): Información general sobre las funciones de administración de compañías
>* [Habilitar características B2B](enable-basic-features.md) - Habilitar y configurar la funcionalidad B2B
