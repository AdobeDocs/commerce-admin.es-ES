---
title: Administración de empresa
description: Optimice la administración y gestión de las organizaciones B2B con modelos operativos complejos.
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 1fc1e07f20e2c22ac430f384e9e2b278edae405c
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# Administración de empresa

La administración de empresas en Adobe Commerce proporciona herramientas completas para que los administradores organicen, configuren y supervisen las relaciones comerciales B2B. Esta función es esencial para las empresas que trabajan con varios clientes corporativos, filiales o estructuras organizativas complejas.

La administración de la empresa le permite:

* **Organizar relaciones empresariales**: cree y administre cuentas de compañía individuales para sus clientes B2B
* **Crear jerarquías organizativas**: estructura relaciones principal-secundario que reflejan organizaciones empresariales reales
* **Centralizar la administración**: administre varias compañías y su configuración desde una sola interfaz administrativa
* **Operaciones optimizadas**: aplique configuraciones y políticas coherentes en todas las empresas relacionadas
* **Estructuras complejas de soporte**: administre filiales, franquicias, negocios de varias ubicaciones y divisiones corporativas

Los usuarios administradores pueden crear una jerarquía de compañías para reflejar una organización B2B asignando compañías a una compañía principal designada. Esta asignación permite al administrador de la empresa matriz ver y administrar las empresas de la organización.

Iniciar tareas de administración de la compañía desde la vista *[!UICONTROL Companies]*. Desde el administrador, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Cuadrícula B2B de administración de compañías](./assets/companies-grid-view.png){width="700" zoomable="yes"}

## Requisitos previos

Antes de administrar compañías, asegúrese de lo siguiente:

* Las funciones B2B están habilitadas en la instalación de Adobe Commerce
* Tiene acceso administrativo con permisos de administración de la compañía
* Las cuentas de compañía están correctamente configuradas con la información empresarial necesaria
* Los roles y permisos de usuario se definen para los administradores y usuarios de la empresa

## Casos de uso

La gestión de la empresa es ideal para:

* **Empresas con múltiples ubicaciones** con compras centralizadas pero con necesidades específicas de cada ubicación
* **Operaciones de franquicia** que requieren supervisión corporativa y autonomía local
* **subsidiarias corporativas** con directivas compartidas pero operaciones independientes
* **Grandes empresas** con varias divisiones o unidades de negocio
* **Redes de distribución** con distribuidores, distribuidores o partners de canal

## Explicación de la jerarquía y los tipos de compañía

La jerarquía de compañías estructura las relaciones de negocio organizando varias compañías bajo una sola compañía matriz. Esta función refleja las estructuras organizativas del mundo real, a la vez que permite una administración centralizada y preserva las identidades individuales de la empresa.

### Tipos de empresa

La columna *[!UICONTROL Company Type]* de la cuadrícula Compañías muestra cómo encaja cada compañía dentro de su organización B2B:

* **Principal**: concentrador central con una o más empresas asignadas
   * Controla varias compañías secundarias, pero no se pueden asignar a otra compañía principal
   * **Caso de uso**: sede corporativa, organización principal de la franquicia o compañía matriz

* **Secundario**: compañía asignada a una organización principal
   * Funciona bajo control principal y puede heredar configuraciones
   * Solo puede pertenecer a un elemento principal a la vez
   * **Caso de uso**: oficinas subsidiarias, ubicaciones de franquicias o divisiones regionales

* **Compañía**: compañía única independiente
   * Funciona de forma independiente sin relaciones de jerarquía
   * Puede convertir a principal (asignando compañías) o secundario (asignando a principal)
   * **Caso de uso**: clientes empresariales individuales o clientes independientes

### Conversión de tipos de empresa

* **Compañía única → Compañía principal**—Asigne otras compañías a ella
* **Empresa única → secundaria**: asígnela a una empresa principal existente
* **→ secundario individual**—Anule la asignación de la compañía secundaria de su compañía primaria
* **Principal → Secundario**: no es posible sin quitar primero todas las empresas asignadas

### Administración de jerarquías de empresa

Al editar compañías dentro de una jerarquía, expanda *[!UICONTROL Company Hierarchy]* para ver todas las compañías relacionadas. Una marca `Current` indica la compañía que se está editando.

![Cuadrícula de jerarquía de compañía B2B](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

Para obtener instrucciones detalladas paso a paso, consulte [Administrar la jerarquía de la compañía](manage-company-hierarchy.md).

## Tareas de gestión empresarial

Al administrar compañías desde la cuadrícula de la compañía, los administradores pueden realizar las siguientes tareas desde la cuadrícula *[!UICONTROL Company Hierarchy]*:

* **Ver y administrar las relaciones con la compañía**
   * **Ver compañías asociadas**: vea todas las compañías vinculadas a una organización principal en una vista centralizada
   * **Supervisar el estado de la compañía**: efectúe el seguimiento de compañías activas, pendientes e inactivas dentro de la jerarquía
   * **Acceder a los detalles de la empresa**: vaya directamente a las páginas de configuración de cada empresa

* **Generar y modificar jerarquías**
   * **Asignar compañías**: agregue compañías existentes a una organización principal desde la página de detalles de la compañía
   * **Crear relaciones entre padres e hijos**—Estructurar compañías para que reflejen las relaciones comerciales reales
   * **Reorganizar estructuras**: mueva compañías entre distintas organizaciones principales a medida que cambien las necesidades empresariales

* **Administración de configuración en lotes**
   * **Aplicar configuración a todas las empresas**: actualice la configuración avanzada de varias empresas simultáneamente mediante el control [!UICONTROL Actions] en la cuadrícula Compañía
   * **Estandarizar configuraciones**: garantice políticas coherentes en todas las organizaciones relacionadas
   * **Anular la configuración individual**: inserta configuraciones de empresa principal en empresas secundarias seleccionadas

* **Acciones administrativas**
   * **Quitar relaciones de compañía**: use la acción *[!UICONTROL Unassign from parent]* para disolver los vínculos de organización
   * **Administrar el acceso a la compañía**—Controlar qué administradores pueden ver y modificar las relaciones con la compañía
   * **Supervisar cambios de jerarquía**: efectúe el seguimiento de las modificaciones de las estructuras organizativas

## Prácticas recomendadas

Al administrar compañías, tenga en cuenta las siguientes prácticas recomendadas:

* **Creación de jerarquías empresariales**: cuando administre estructuras empresariales complejas, planifique la jerarquía para que coincida con las relaciones comerciales reales, manteniendo las estructuras simples para evitar la confusión del usuario. Documente todas las relaciones con la compañía y sus conexiones comerciales para referencia futura.

* **Administración de configuración**: pruebe los cambios de configuración en empresas individuales antes de aplicarlos a jerarquías completas y documente siempre la configuración actual antes de realizar cambios masivos. Comunique los cambios planificados a los administradores de la empresa afectados con antelación.

* **Seguridad**: limita los permisos de administración de la compañía únicamente a los administradores de confianza, realiza revisiones periódicas de las relaciones con la compañía y los permisos de acceso, y supervisa todos los cambios de jerarquía con fines de auditoría.

>[!MORELIKETHIS]
>
>* [Crear una cuenta de compañía](account-company-create.md)
>* [Administrar jerarquías de empresa](manage-company-hierarchy.md)
>* [Roles y permisos de la compañía](account-company-roles-permissions.md)
>* [Administración de crédito de la compañía](credit-company.md)
>* [Habilitar características B2B](enable-basic-features.md)
