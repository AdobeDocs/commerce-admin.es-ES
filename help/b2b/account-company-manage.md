---
title: Administrar cuentas de empresa
description: Aprenda a administrar las cuentas de empresa de su tienda Adobe Commerce mediante la página Compañías y las herramientas disponibles en la cuadrícula.
exl-id: 9e125fc2-d20e-463e-a391-582fa0bcb68d
feature: B2B, Companies, Configuration
source-git-commit: fa8083570a4637c4bf67f7657ef9d0d48f962c50
workflow-type: tm+mt
source-wordcount: '2493'
ht-degree: 0%

---

# Administrar cuentas de empresa

La página _[!UICONTROL Companies]_enumera todas las cuentas de compañía actuales, independientemente del estado. Cualquier solicitud de aprobación pendiente aparecerá en la parte superior de la lista. Los [controles estándar del área de trabajo](../getting-started/admin-workspace.md) se pueden usar para filtrar la lista, cambiar el [diseño de la columna](../getting-started/admin-grid-controls.md), guardar vistas o exportar datos.

El control _[!UICONTROL Actions]_sobre la cuadrícula se puede usar para aplicar una acción a varios registros de compañía. Por ejemplo: en lugar de aprobar cada solicitud individual de empresa, puede seleccionar varias solicitudes y activar las cuentas en una sola acción. Las acciones disponibles dependen de los [permisos](../systems/permissions.md) para la función asignada a su cuenta de usuario administrador.

Utilice la función _[!UICONTROL Search]_para buscar compañías en la cuadrícula **Compañías**por palabra clave. La búsqueda indiza palabras clave de las columnas **Nombre de la compañía**y **Principal**. Puede filtrar por **Tipo de compañía**para mostrar solo compañías individuales, solo compañías principales o solo compañías secundarias.

![Cuadrícula de compañías](./assets/companies-grid-view.png){width="700" zoomable="yes"}

## Recursos de funciones de compañía

La configuración de [Recursos de rol](../systems/permissions-user-roles.md#role-resources) determina la capacidad para:

- Añadir una empresa
- Eliminar una empresa
- Aplicar un reembolso de saldo
- Ver compañías

Estos recursos de rol deben establecerse para la [Función de usuario](../systems/permissions-user-roles.md) asignada para la cuenta de usuario de administrador.

## Aplicar una acción

Las siguientes acciones se pueden aplicar a registros únicos o múltiples.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. En la primera columna de la cuadrícula, active la casilla de verificación de cada registro que desee actualizar y siga las instrucciones de la acción que desee aplicar:

### Activar cuentas de empresa

1. En el control **[!UICONTROL Actions]**, seleccione **[!UICONTROL Set Active]**.

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL OK]**.

### Definir activo/inactivo

Los clientes con cuentas inactivas no pueden iniciar sesión ni realizar compras en sus cuentas. Existen dos métodos para establecer una cuenta de cliente como activa o inactiva:

Método 1: **De la cuadrícula Clientes**

1. En la barra lateral de _Administración_, vaya a [!UICONTROL **Clientes**] > [!UICONTROL **Todos los clientes**].

1. En el menú **[!UICONTROL Actions]**, seleccione una de las siguientes opciones:

   - **[!UICONTROL Active]**
   - **[!UICONTROL Inactive]**

1. Cuando se le pida, seleccione **[!UICONTROL OK]** para aplicar el cambio.

Método 2: **De la página de edición de la cuenta**

1. En la barra lateral de _Administración_, vaya a [!UICONTROL **Clientes**] > [!UICONTROL **Todos los clientes**].

1. En la cuadrícula, busque el registro de cliente que desea editar.

1. En la columna _Acciones_ del extremo derecho, seleccione [!UICONTROL **Editar**].

1. Seleccione la ficha [!UICONTROL **Información de la cuenta**].

1. Establezca [!UICONTROL **Cliente activo**] en `Yes` o `No`.

1. Haga clic en [!UICONTROL **Guardar cliente**].

### Bloquear cuentas de empresa

Los usuarios asociados a una cuenta de empresa bloqueada pueden iniciar sesión en el catálogo y acceder a él, pero no pueden realizar compras. Una compañía con una cuenta que no esté al día podría ser bloqueada temporalmente hasta que se resuelva el asunto.

1. En el control **[!UICONTROL Actions]**, seleccione **[!UICONTROL Block]**.

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL OK]**.

### Eliminar cuentas de empresa

Las cuentas de empresa eliminadas no se pueden restaurar. El estado de las cuentas de usuario asociadas con la compañía se establece en `Inactive` y el Id. de compañía se elimina de los perfiles de las cuentas de usuario. La información sobre la actividad y las transacciones de la empresa se conserva en el sistema.

1. En el control **[!UICONTROL Actions]**, seleccione **[!UICONTROL Delete]**.

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL OK]**.

### Conversión de la moneda de crédito

El crédito en las cuentas de las empresas seleccionadas se convierte al tipo de cambio actual de la divisa seleccionada.

1. En el control **[!UICONTROL Actions]**, seleccione **[!UICONTROL Convert Currency]**.

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL OK]**.

1. Elija **[!UICONTROL Credit Currency]** para usar en las cuentas de compañía seleccionadas.

   Las cantidades se vuelven a calcular según las tasas de conversión actuales, si están disponibles. Si no está disponible, puede introducir manualmente las tasas de conversión personalizadas. El sistema muestra tantos cálculos de conversión como sean necesarios para la divisa de crédito utilizada por las empresas seleccionadas.

1. Haga clic en **[!UICONTROL Proceed]** para completar la conversión.

## Editar una cuenta de empresa

Método 1: **edición rápida**

1. En la primera columna, seleccione la casilla de la cuenta de empresa que desea editar.

1. En el control **[!UICONTROL Actions]**, seleccione **[!UICONTROL Edit]**.

   Cada valor que se puede actualizar aparece en un cuadro de texto.

   ![Edición rápida de una cuenta de compañía](./assets/companies-grid-quick-edit.png){width="700" zoomable="yes"}

1. Actualice cualquiera de los siguientes valores según sea necesario:

   - **[!UICONTROL Company Name]**

   - **[!UICONTROL Company Email]**

   - **[!UICONTROL Phone Number]**

1. Haga clic en **[!UICONTROL Save]**.

Método 2: **edición completa**

1. En la cuadrícula, busque el registro de empresa que desea editar.

1. Seleccione **[!UICONTROL Edit]** de la columna _[!UICONTROL Action]_.

1. Realice los cambios necesarios en la información de la compañía.

Para obtener descripciones de los campos, consulte [Crear una cuenta de empresa](account-company-create.md).

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

## Asignar un representante de ventas

El representante de ventas es un [usuario administrador](../systems/permissions.md) que se asigna como punto de contacto para una cuenta de compañía y recibe todos los [mensajes de correo electrónico](../b2b/enable-basic-features.md#configure-company-email-options) automatizados relacionados con la compañía. Solo se puede asignar un representante de ventas por cuenta de compañía, pero un solo representante de ventas puede administrar varias cuentas de compañía. La cuenta de usuario Admin predeterminada se asigna como representante de ventas, a menos que se asigne un usuario Admin diferente.

El nombre y la dirección de correo electrónico del representante de ventas asignado son visibles para los miembros de la compañía desde la página Cuenta de compañía y presupuestos.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Busque la empresa en la cuadrícula y ábrala en modo de edición.

1. Establezca **[!UICONTROL Sales Representative]** en el usuario administrador que desea asignar como punto de contacto para la compañía.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

   El representante de ventas asignado recibe una notificación por correo electrónico de la asignación.

## Actualización de un perfil de empresa

El administrador de la empresa y también un administrador de la tienda pueden mantener el perfil de la empresa desde la tienda.

![Perfil de la compañía](./assets/company-update.png){width="700" zoomable="yes"}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Busque la empresa en la cuadrícula y haga clic en **[!UICONTROL Edit]** en la columna _[!UICONTROL Action]_.

1. Actualice los valores de campo en cada sección según sea necesario utilizando las descripciones de campo como referencia.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

## Demostración de cuenta de compañía

Para obtener más información sobre la administración de cuentas de empresa, consulte este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/344447?quality=12)

## Administración de empresa

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponible solo para participantes del programa Beta"}

Una vez creada una compañía, los usuarios administradores con los permisos adecuados pueden utilizar la sección [!UICONTROL Company Hierarchy] para crear una organización de compañía principal editando la compañía principal designada y asignando compañías relacionadas.

Si se ha agregado una compañía a una jerarquía, la cuadrícula [!UICONTROL Company Hierarchy] muestra la compañía principal y todas las compañías asignadas en la cuadrícula.

Consulte [Administrar la jerarquía de la compañía](assign-companies.md) para obtener más información.

## Opciones y columnas de la empresa

Las secciones siguientes proporcionan una referencia sobre las acciones, opciones y la información mostrada disponibles para administrar cuentas de empresa.

### Opciones de control de acciones

| Opción | Descripción |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Set Active] | Establece el estado de todos los registros de empresa seleccionados en `Active`. Los administradores de la empresa reciben instrucciones para establecer sus contraseñas de modo que puedan acceder a sus cuentas y administrar sus empresas desde la tienda. |
| [!UICONTROL Block] | Restringe las cuentas de compañía que no están al día, conservando al mismo tiempo la cuenta. Los miembros de la compañía pueden iniciar sesión y acceder al catálogo, pero no pueden realizar pedidos en nombre de la compañía. |
| [!UICONTROL Delete] | Elimina las cuentas de empresa seleccionadas. El estado de las cuentas de usuario asociadas con una compañía eliminada se establece en `Inactive` y el identificador de compañía se elimina de los perfiles de las cuentas de usuario. La información sobre la actividad y las transacciones de la empresa se conserva en el sistema. |
| [!UICONTROL Edit] | Permite editar algunos valores del registro de empresa seleccionado desde la cuadrícula. De forma predeterminada, los valores Nombre de la empresa, Correo electrónico de la empresa y Número de teléfono están disponibles para una edición rápida. |
| [!UICONTROL Convert Credit] | Convierte el crédito a cuenta para las empresas seleccionadas según las tasas de la moneda especificada. |

{style="table-layout:auto"}

### Descripciones de columna


#### Diseño de columna predeterminado

| Columna | Descripción |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Select] | Casillas de verificación utilizadas para seleccionar registros de empresa que deben ser sujetos de una acción o utilizar el control de selección del encabezado de la columna para seleccionar o anular la selección de todos. |
| [!UICONTROL ID] | Identificador numérico único que se asigna cuando se envía la solicitud de creación de una empresa. |
| [!UICONTROL Company Name] | El nombre de la empresa se introduce la primera vez que se crea la cuenta de la empresa y puede ser una versión abreviada del nombre legal completo. |
| [!UICONTROL Company Type] | El tipo de [empresa](manage-companies.md). Opciones: <br/>**[!UICONTROL Company]**: de forma predeterminada, las nuevas compañías se crean como compañías únicas.<br/>**[!UICONTROL Parent]** - La compañía es una compañía matriz de otras compañías. <br/>**[!UICONTROL Child]**- Esta compañía está relacionada con una compañía primaria. |
| [!UICONTROL Parent] | Muestra la compañía matriz de esta línea de compañía específica. |
| [!UICONTROL Company Email] | La dirección de correo electrónico asociada a la cuenta de la empresa. |
| [!UICONTROL Phone Number] | El número de teléfono principal de la empresa. |
| [!UICONTROL Country] | El país donde está registrada la compañía para llevar a cabo sus negocios. |
| [!UICONTROL State Province] | El estado o provincia donde la compañía está registrada para llevar a cabo actividades comerciales. |
| [!UICONTROL City] | La ciudad donde está registrada la compañía para realizar negocios. |
| [!UICONTROL Group/Shared Catalog] | El nombre de la columna depende de si Catálogo compartido está habilitado en la configuración. Opciones: <br/>**[!UICONTROL Customer Group]**- Si el catálogo compartido no está habilitado en la configuración, especifica el nombre del [grupo de clientes](../customers/customer-groups.md) al que pertenece la compañía.<br/>**[!UICONTROL Shared Catalog]**: si Catálogo compartido está habilitado en la configuración, especifica el nombre del catálogo compartido que se asigna al cliente. |
| [!UICONTROL Outstanding Balance] | El saldo pendiente en la cuenta de la compañía. la columna está en blanco si la empresa no tiene historial de crédito y su límite de crédito es cero. |
| [!UICONTROL Company Admin] | El nombre y apellidos del administrador de la empresa. |
| [!UICONTROL Job Title] | El puesto del administrador de la empresa. |
| [!UICONTROL Email] | La dirección de correo electrónico del administrador de la empresa. |
| [!UICONTROL Action] | **[!UICONTROL Edit]** - Abre la cuenta de la compañía en modo de edición. |

{style="table-layout:auto"}

#### Columnas adicionales

Las siguientes columnas están disponibles si cambia el [diseño de columna](../getting-started/admin-grid-controls.md) de la cuadrícula.

| Columna | Descripción |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | El nombre legal completo de la compañía. |
| [!UICONTROL Street Address] | Dirección de la calle donde está registrada la empresa para realizar actividades comerciales. |
| [!UICONTROL ZIP] | El código postal en el que la empresa está registrada para llevar a cabo actividades comerciales. |
| [!UICONTROL Reseller ID] | El número de reventa asignado a la compañía con fines de información fiscal. |
| [!UICONTROL VAT/TAX ID] | El número de [impuesto al valor agregado](../stores-purchase/vat.md) que algunas jurisdicciones asignan a la compañía con fines de informes de impuestos. Para configurar la identificación fiscal o de IVA del cliente para que aparezca en la tienda, consulta [Crear nuevas opciones de cuenta](../configuration-reference/customers/customer-configuration.md). |
| [!UICONTROL Credit Limit] | El límite de crédito que se amplía a la cuenta de la compañía. |
| [!UICONTROL Credit Currency] | La moneda que acepta el almacén para compras a crédito de la compañía. |
| [!UICONTROL Status] | Indica el [estado](account-company-approve.md) de la cuenta de compañía. Opciones: <br/>**[!UICONTROL Active]**: el administrador del almacén ha aprobado la cuenta de la empresa. El administrador de la empresa y los miembros asociados pueden iniciar sesión en la cuenta desde la tienda y realizar compras.<br/>**[!UICONTROL Pending Approval]** - Se ha enviado una solicitud para abrir una cuenta de compañía, pero el administrador del almacén aún no la ha aprobado. <br/>**[!UICONTROL Rejected]**- Se envió una solicitud para abrir una cuenta de compañía, pero el administrador del almacén no la aprobó. Las credenciales de inicio de sesión iniciales utilizadas para enviar la solicitud están bloqueadas.<br/>**[!UICONTROL Blocked]** - Los miembros de la compañía pueden iniciar sesión y acceder al catálogo, pero no pueden realizar compras. El administrador de la tienda podría bloquear una cuenta de empresa que no esté al día. El administrador de la tienda puede eliminar el bloque de la cuenta en cualquier momento. |
| [!UICONTROL Gender] | El sexo del administrador de la empresa. Opciones: Masculino/Femenino/No especificado |
| [!UICONTROL Comment] | Notas sobre la cuenta de la compañía como referencia y visibles solo desde el administrador. |

{style="table-layout:auto"}

### Barra de botones

| Botón | Descripción |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Back] | Vuelve a la página Compañías sin guardar los cambios. |
| [!UICONTROL Login as Customer] | Permite que un usuario administrador [inicie sesión en la tienda como cliente](../customers/login-as-customer.md) y le ayude con sus pedidos. |
| [!DNL Delete Company] | Elimina la cuenta de compañía. El estado de las cuentas de usuario asociadas con la compañía se establece en `Inactive` y el Id. de compañía se elimina de los perfiles de las cuentas de usuario. La información sobre la actividad y las transacciones de la empresa se conserva en el sistema. |
| [!DNL Reset] | Restaura los valores originales en cualquier campo con cambios no guardados. |
| [!DNL Reimburse Balance] | Permite al administrador reembolsar el saldo del crédito del almacén, al que se hace referencia mediante el número de pedido. |
| [!DNL Save] | Guarda los cambios en la empresa y mantiene el perfil abierto. |
| [!UICONTROL Save & Close] | Guarda los cambios realizados en la empresa y cierra el perfil. |

{style="table-layout:auto"}

### Descripciones de campos

| Campo | Descripción |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Name] | El nombre de la empresa se introduce la primera vez que se crea la cuenta de la empresa y puede ser una versión abreviada del nombre legal completo. |
| [!UICONTROL Status] | Indica el [estado](account-company-approve.md) de la cuenta de compañía. Opciones: <br/>**[!UICONTROL Active]**: el administrador del almacén ha aprobado la cuenta de la empresa. El administrador de la empresa y los miembros asociados pueden iniciar sesión en la cuenta desde la tienda y realizar compras.<br/>**[!UICONTROL Pending Approval]** - Se ha enviado una solicitud para abrir una cuenta de compañía, pero el administrador del almacén aún no la ha aprobado. <br/>**[!UICONTROL Rejected]**- Se envió una solicitud para abrir una cuenta de compañía, pero el administrador del almacén no la aprobó. Las credenciales de inicio de sesión iniciales utilizadas para enviar la solicitud están bloqueadas.<br/>**[!UICONTROL Blocked]** - Los miembros de la compañía pueden iniciar sesión y acceder al catálogo, pero no pueden realizar compras. El administrador de la tienda podría bloquear una cuenta de empresa que no esté al día. El administrador de la tienda puede eliminar el bloque de la cuenta en cualquier momento. |
| [!UICONTROL Company Email] | La dirección de correo electrónico asociada a la cuenta de la empresa. |
| [!UICONTROL Sales Representative] | El usuario administrador, que es el contacto principal de la cuenta de la compañía. |

{style="table-layout:auto"}

#### [!UICONTROL Account Information]

| Campo | Descripción |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | El nombre legal completo de la compañía. |
| [!UICONTROL VAT / TAX ID] | El número de impuesto o [impuesto al valor agregado](../stores-purchase/vat.md) que se ha asignado a la compañía con fines de informes de impuestos. |
| [!UICONTROL Reseller ID] | El número de reventa asignado a la compañía con fines de información fiscal. |
| [!UICONTROL Comment] | Estas notas sobre la cuenta de la compañía son de referencia y visibles solo desde el administrador. |
| **[!UICONTROL Legal Address]** |                                                                                                                            |
| [!UICONTROL Street Address] | Dirección de la calle donde está registrada la empresa para realizar actividades comerciales. |
| [!UICONTROL City] | La ciudad donde está registrada la compañía para realizar negocios. |
| [!UICONTROL Country] | El país donde está registrada la compañía para llevar a cabo sus negocios. |
| [!UICONTROL State/Province] | El estado o provincia donde la compañía está registrada para llevar a cabo actividades comerciales. |
| [!UICONTROL ZIP/Postal Code] | El código postal en el que la empresa está registrada para llevar a cabo actividades comerciales. |
| [!UICONTROL Phone Number] | El número de teléfono principal de la empresa. |

{style="table-layout:auto"}

#### [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponible solo para participantes del programa Beta"}

| Columnas | Descripción |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company ID] | El número de ID de la empresa. |
| [!UICONTROL Company Name] | El nombre completo de la empresa. <br/>Aparece un(a) `current company indicator` en la línea de compañía que se está editando. |
| [!UICONTROL Company Email] | La dirección de correo electrónico asociada a la cuenta de la empresa. |
| [!UICONTROL Phone Number] | El número de teléfono principal de la empresa. |
| [!UICONTROL State/Province] | El estado o provincia donde la compañía está registrada para llevar a cabo actividades comerciales. |
| [!UICONTROL City] | La ciudad donde está registrada la compañía para realizar negocios. |
| [!UICONTROL Customer Group] | (Solo administrador) Indica el [grupo de clientes](../customers/customer-groups.md) o el [catálogo compartido](catalog-shared.md) que se ha asignado a la compañía. |
| [!UICONTROL Company Admin] | Nombre completo del administrador de la empresa. |
| [!UICONTROL Action] | La lista de posibles acciones para esa línea de compañía. |

{style="table-layout:auto"}

#### [!UICONTROL Company Admin]

| Campo | Descripción |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Job Title] | El título del administrador de la empresa que administra la cuenta de la empresa. |
| [!UICONTROL Email] | La dirección de correo electrónico del administrador de la empresa puede ser la misma que la dirección de correo electrónico de la empresa. Si se introduce una dirección de correo electrónico diferente, se crea una cuenta individual independiente para el administrador de la empresa además de la cuenta de la empresa. |
| [!UICONTROL Prefix] | Si corresponde, el prefijo asociado al nombre del administrador de la empresa (como `Mr.`, `Ms.`, `Mrs.` o `Dr.`). Según la configuración, el campo de entrada puede ser un campo de texto o una lista. |
| [!UICONTROL First Name] | El nombre del administrador de la empresa. |
| [!UICONTROL Middle Name/Initial] | El segundo nombre o la inicial del administrador de la empresa. |
| [!UICONTROL Last Name] | Apellidos del administrador de la empresa. |
| [!UICONTROL Suffix] | Si procede, el sufijo asociado al nombre del administrador de la empresa (como `Jr.`, `Sr.` o `III`). Según la configuración, el campo de entrada puede ser un campo de texto o una lista. |
| [!UICONTROL Gender] | El sexo del administrador de la empresa. Opciones: `Male` / `Female` / `Not Specified` |

{style="table-layout:auto"}

#### [!UICONTROL Company Credit]

| Campo | Descripción |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Credit Currency] | La moneda que acepta el almacén para compras a crédito de la compañía. |
| [!UICONTROL Credit Limit] | El límite de crédito que se amplía a la cuenta de la compañía. |
| [!UICONTROL Allow to Exceed Credit Limit] | Indica si la empresa tiene permiso para superar el límite de crédito. Opciones: Sí / No |
| [!UICONTROL Reason for Change] | Una nota que explica las circunstancias en las que la empresa puede superar o no el límite de crédito. Este campo solo está activo si cambia el permiso para superar el límite de crédito. |

{style="table-layout:auto"}

#### [!UICONTROL Advanced Settings]

| Campo | Descripción |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Customer Group] | Indica el [grupo de clientes](../customers/customer-groups.md) o el [catálogo compartido](catalog-shared.md) que se ha asignado a la compañía. |
| [!UICONTROL Allow Quotes] | Determina si los miembros de la compañía pueden preparar y enviar ofertas negociables en nombre de la compañía. |
| [!UICONTROL Enable Purchase Orders] | Determina si se permiten pedidos de compra para la empresa. Para que los pedidos de compra funcionen para las cuentas de miembro de la empresa, el administrador de la empresa también debe habilitar esta función en la tienda. |
| [!UICONTROL Applicable Payment Methods] | Indica los métodos de pago disponibles para las compras de la empresa. Opciones: `B2B Payment Methods` / `All Enabled Payment Methods` / `Specific Payment Methods` |
| [!UICONTROL Payment Methods] | (Solo administrador) Se activa si se indican métodos de pago específicos. Para seleccionar varios métodos de pago, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada opción. |

{style="table-layout:auto"}
