---
title: Cuentas de empresa
description: Descubra cómo las cuentas de empresa administradas en su tienda Adobe Commerce permiten unir varios compradores que pertenecen a la misma empresa en una sola cuenta de empresa.
exl-id: 0b3c3635-a1cf-4ee6-a8bc-e7cbcb4e2e63
feature: B2B, Companies, Configuration
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Cuentas de empresa

Al incorporar cuentas de empresa B2B en su tienda, puede simplificar la experiencia de compra corporativa permitiendo que las empresas creen varias subcuentas con permisos flexibles basados en las funciones de usuario en su organización.

Dependiendo de la empresa, un administrador de tienda puede ajustar las promociones y los precios para adaptarlos a sus necesidades, y crear ofertas altamente personalizadas que se adapten a las demandas de los compradores y aumenten los pedidos.

Añadir una asociación de cuenta de compañía a un [individuo](../customers/account-create.md) estándar permite que el cliente utilice los flujos de trabajo de compra específicos definidos para la compañía.

Ventajas de una cuenta de empresa:

- Ofrece [usuarios empresariales](account-company-users.md) ilimitados y la creación de cuentas adicionales, lo que simplifica las compras corporativas.

- Incluye compatibilidad con una jerarquía de cuentas de compañía _smart_ con diferentes [roles y permisos](account-company-roles-permissions.md) para realizar pedidos.

- Proporciona un mecanismo para que los comerciantes aumenten sus ingresos al ofrecer [crédito de la tienda de la compañía](credit-company.md) como método de pago.

- Admite la [administración](account-company-manage.md) de todas las cuentas de compañía del administrador.

## Ver cuentas de empresa

La cuadrícula _Compañías_ enumera todas las cuentas de compañía activas y las solicitudes pendientes, independientemente de la configuración de estado. También proporciona las herramientas para [crear](account-company-create.md) y [administrar](account-company-manage.md) cuentas de compañía. Utilice los controles de cuadrícula estándar para filtrar la lista y ajustar el diseño de la columna. Para obtener una lista de descripciones de columnas, consulte la sección _Descripciones de columnas_ en [Administración de cuentas de compañía](account-company-manage.md).

Los clientes pueden crear una cuenta de compañía desde la tienda o un comerciante puede crear una desde el administrador. De forma predeterminada, la capacidad de crear cuentas de compañía desde la tienda está habilitada. Si la configuración lo permite, un visitante de la tienda puede solicitar abrir una cuenta de empresa. Una vez aprobada la cuenta de la empresa, el administrador de la empresa puede configurar la estructura de la empresa y los usuarios con varios niveles de permisos.

En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Cuadrícula de compañías](./assets/companies-grid.png){width="700" zoomable="yes"}

La cuadrícula [!UICONTROL Companies] enumera todas las compañías independientemente de su estado. La lista de la compañía indica si una compañía está asociada con una [jerarquía de compañías](manage-company-hierarchy.md) y proporciona [información detallada](/help/b2b/account-company-manage.md#company-options-and-columns) acerca de la compañía, el administrador de la compañía y otra información. Personalice la vista mediante los [controles de cuadrícula de administración](../getting-started/admin-grid-controls.md) para establecer filtros, opciones de vista de columna y mucho más.

## Administrador de empresa

El siguiente ejemplo muestra la cuadrícula _Clientes_ con las cuentas iniciales de administrador de la empresa.

![Cuadrícula de clientes con cuenta de administrador de empresa](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

Cada empresa tiene un único administrador de empresa identificado por la dirección de correo electrónico de la cuenta y el nombre y apellidos del administrador. El administrador puede asignarse a otras empresas como usuario, pero solo puede ser administrador de una empresa.

Después de crear la cuenta, el administrador de la compañía define la estructura de la compañía de [equipos](account-company-structure.md), configura los [usuarios de la compañía](account-company-users.md) y establece [roles y permisos](account-company-roles-permissions.md) para cada uno.

### Establecer la contraseña de administrador de la empresa antes del primer inicio de sesión

1. El administrador de la empresa encuentra un correo electrónico de bienvenida de la tienda.

   ![Correo electrónico de bienvenida de ejemplo](./assets/company-admin-welcome-email.png){width="500"}

   >[!NOTE]
   >
   >Los objetivos de las direcciones de correo electrónico y el contenido del correo electrónico están determinados por las opciones especificadas en la configuración [opciones de correo electrónico de la empresa](email-company-configuration.md).

1. Sigue las instrucciones y hace clic en [!UICONTROL **vínculo**] para establecer la contraseña.

1. Escribe una [!UICONTROL **contraseña nueva**] y una confirmación de contraseña para su cuenta.

   La contraseña debe incluir al menos tres de los siguientes tipos de caracteres:

   - Caracteres en minúsculas (abc...)
   - Caracteres en mayúsculas (ABC...)
   - Números (1234567890)
   - Caracteres especiales (!@#$...)

1. Hace clic en [!UICONTROL **Establecer nueva contraseña**].

   ![Inicio de sesión de cliente - administrador de empresa](./assets/company-admin-account-login.png){width="700" zoomable="yes"}

1. Cuando aparece la página [!UICONTROL Customer Login], el cliente introduce su [!UICONTROL **correo electrónico**] y [!UICONTROL **contraseña**].

1. Hace clic en [!UICONTROL **Iniciar sesión**] para obtener acceso al tablero de su cuenta.

   ![Tablero de cuenta - empresa](./assets/account-dashboard-company.png){width="700" zoomable="yes"}

## Estructura de la empresa

Se puede configurar una cuenta de compañía para reflejar la estructura de la empresa. Inicialmente, la estructura de la empresa incluye solo el administrador de la empresa, pero se puede expandir para incluir equipos de usuarios. Los usuarios pueden estar asociados a equipos u organizados dentro de una jerarquía de divisiones y subdivisiones dentro de la compañía. La estructura está diseñada para admitir el uso de [reglas de aprobación](account-dashboard-approval-rules.md) para [pedidos de compra](purchase-order-flow.md) (PO) asociados a la cuenta de la compañía.

![Estructura de la compañía con divisiones](./assets/company-structure-diagram.svg){width="450"}

En el panel de cuentas del administrador de la empresa, la estructura de la empresa se representa como un árbol y consiste inicialmente solo en el administrador de la empresa.

![Estructura de la compañía con el administrador](./assets/company-structure-tree-admin.png){width="600"}

Cuando se crea la cuenta, el administrador de la empresa puede utilizar la dirección de correo electrónico de la empresa o tener asignada una dirección de correo electrónico diferente.

En el ejemplo siguiente, la estructura inicial de la empresa incluye el administrador de la empresa más una cuenta de usuario individual en el nombre del administrador de la empresa. Sin embargo, las funciones de administrador de la empresa (como la estructura de la empresa y las reglas de aprobación) solo están disponibles cuando se inicia sesión en la cuenta de usuario designada como administrador de la empresa.

![Estructura de la compañía con cuenta de administrador y usuario](./assets/company-structure-tree-admin-user.png){width="600"}
