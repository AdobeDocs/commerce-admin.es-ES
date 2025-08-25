---
title: Crear una cuenta de empresa
description: Obtenga información acerca de la creación de cuentas de empresa en el Administrador de Adobe Commerce y en la tienda.
exl-id: 8c06395b-102b-4a41-8eb3-e6a344feac70
feature: B2B, Companies, Configuration, Storefront
role: Admin, User
source-git-commit: 2e119bcb8278432bde1c12f3f44a112cde59fb18
workflow-type: tm+mt
source-wordcount: '2444'
ht-degree: 0%

---

# Crear una cuenta de empresa

Las cuentas de compañía permiten a las empresas B2B administrar sus compras, usuarios y créditos en Adobe Commerce. Este tema cubre el proceso completo de creación, configuración y activación de cuentas de empresa.

## Resumen de creación de cuenta de compañía

Las cuentas de compañía se pueden crear mediante dos métodos, cada uno adecuado para diferentes escenarios comerciales:

* **Registro de tienda**: solicitudes de cuenta de autoservicio por parte de empresas
* **Creación de administración**: configuración de cuenta con asistencia de ventas con detalles preconfigurados

Todas las cuentas de empresa requieren la aprobación del administrador antes de activarse, lo que garantiza una verificación y configuración adecuadas.

## Requisitos previos

Antes de crear cuentas de empresa, asegúrese de que se cumplen los siguientes requisitos:

* **Requisitos del sistema:**
   * [Las características B2B están habilitadas](enable-basic-features.md) en su instalación de Adobe Commerce
   * El registro de empresa está habilitado para crear tiendas
   * Las notificaciones por correo electrónico están configuradas para flujos de trabajo de aprobación

* **Requisitos empresariales:**
   * Se establecen procesos y políticas de aprobación
   * Se asignan representantes de ventas (para cuentas creadas por el administrador)
   * Se definen las políticas de crédito (si se utiliza el crédito de la compañía)
   * Se han configurado los grupos de clientes y los catálogos compartidos

* **Acceso administrativo:**
   * Permisos adecuados para la administración de empresas
   * Acceso a las secciones de administración de clientes y empresas

El sistema asigna la función [administrador de la empresa](account-company-admin.md) a la persona que configura una cuenta de empresa desde la tienda. Una vez que el administrador del almacén aprueba la solicitud de creación de cuenta de la empresa en Admin, el administrador de la empresa puede establecer una contraseña de cuenta e iniciar sesión en la cuenta.

## Método 1: el cliente crea la cuenta a partir de la tienda

**Cuándo usar este método:**

* Se prefiere el registro empresarial de autoservicio
* Los clientes tienen a su disposición toda la información comercial necesaria
* El flujo de trabajo de aprobación estándar es suficiente
* No se requiere ninguna configuración especial ni rellenado previo

>[!IMPORTANT]
>
>Para admitir este método (que permite a los clientes registrar su compañía desde la tienda), asegúrese de que las [características B2B](enable-basic-features.md) estén habilitadas.

1. En la esquina superior derecha del encabezado de la tienda, el cliente hace clic en **[!UICONTROL Create an Account]** y elige **[!UICONTROL Create New Company Account]**.

   ![Crear nueva cuenta de compañía](./assets/company-account-create-storefront-options.png){width="700" zoomable="yes"}

   >[!NOTE]
   >
   >Si un visitante inició sesión en una cuenta de usuario registrada, puede crear una cuenta de compañía navegando hasta _[!UICONTROL Customer Profile]_>**[!UICONTROL Company Structure]**>**[!UICONTROL Create a Company Account]**.

1. En la sección _[!UICONTROL Company Information]_, el cliente hace lo siguiente:

   * Rellena los campos obligatorios:

      * **[!UICONTROL Company Name]**
      * **[!UICONTROL Company Email]**

   * Completa los campos restantes, según corresponda:

      * **[!UICONTROL Company Legal Name]**
      * **[!UICONTROL VAT/TAX ID]**
      * **[!UICONTROL Reseller ID]**

   ![Información de la compañía](./assets/company-information-storefront.png){width="700" zoomable="yes"}

1. Completa los campos requeridos en la sección _[!UICONTROL Legal Address]_.

   * **[!UICONTROL Street Address]**
   * **[!UICONTROL City]**
   * **[!UICONTROL Country]**
   * **[!UICONTROL State/Province]**
   * **[!UICONTROL ZIP/Postal Code]**
   * **[!UICONTROL Phone Number]**

   ![Dirección Legal](./assets/company-legal-address-storefront.png){width="700" zoomable="yes"}

1. En la sección _[!UICONTROL Company Administrator]_, hace lo siguiente:

   * Escribe el **[!UICONTROL Email address]** del administrador de la empresa.

     La dirección de correo electrónico del administrador de la empresa puede ser la misma que la dirección de correo electrónico de la empresa o una dirección de correo electrónico diferente. Si introduce una dirección de correo electrónico diferente, el sistema crea una cuenta de usuario de la empresa, además de la cuenta de administrador de la empresa.

   * Escribe **[!UICONTROL First Name]** y **[!UICONTROL Last Name]** del administrador de la empresa.

   * Opcionalmente, rellena los campos siguientes:

      * **[!UICONTROL Job Title]**
      * **[!UICONTROL Work Phone Number]**
      * **[!UICONTROL Gender]**

   ![Administrador de la empresa](./assets/company-administrator-account-storefront.png)

1. Completa la validación si reCAPTCHA está habilitado para esta función de tienda.

1. Cuando se complete la información, seleccione **[!UICONTROL Submit]**.

   Cuando el comerciante aprueba la solicitud de creación de una cuenta de empresa, el sistema envía una notificación por correo electrónico al administrador de la empresa.

   ![Correo electrónico de bienvenida de ejemplo](./assets/company-admin-welcome-email.png){width="500"}

   Una vez establecida la contraseña, el administrador de la empresa puede [iniciar sesión](../customers/customer-sign-in.md) en la cuenta.

## Método 2: El comerciante crea la cuenta a partir del administrador

**Cuándo usar este método:**

* Se prefiere la creación de cuentas con asistencia de ventas
* Rellenado previo de detalles de cuenta de relaciones comerciales existentes
* Se requiere una configuración personalizada (límites de crédito, precios especiales)
* Se necesita la activación inmediata sin flujo de trabajo de aprobación

El proceso de creación de una empresa desde el administrador es esencialmente el mismo que desde la tienda, pero con campos adicionales.

![Agregar una nueva compañía del administrador](./assets/company-add-new.png){width="700" zoomable="yes"}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Haga clic en **[!UICONTROL Add New Company]** y haga lo siguiente:

   * Rellene estos campos obligatorios:

      * **[!UICONTROL Company Name]**
      * **[!UICONTROL Company Email]**

   * Si no está listo para que la cuenta se active, establezca **[!UICONTROL Status]** en `Pending Approval`. (De forma predeterminada, se establece en `Active`.)

   * Si corresponde, elija la cuenta de administrador de **[!UICONTROL Sales Representative]** que va a administrar la cuenta.

1. En la sección _[!UICONTROL Account Information]_, haga lo siguiente:

   * Rellene los campos siguientes según corresponda:

      * **[!UICONTROL Company Legal Name]**
      * **[!UICONTROL VAT/TAX ID]**
      * **[!UICONTROL Reseller ID]**

   * Para **[!UICONTROL Comment]**, escriba la información adicional sobre el cliente que pueda ser necesaria.

     Los comentarios solo son visibles desde el administrador.

   ![Información de la cuenta](./assets/company-create-account-information-admin.png){width="700" zoomable="yes"}

1. Cuando crea una compañía por primera vez, la cuadrícula _[!UICONTROL Company Hierarchy]_aparece vacía al expandirla. Una vez guardada la compañía, puede incluirla en una jerarquía de compañías. Consulte [Administración de la compañía](manage-companies.md).

1. En la sección _[!UICONTROL Legal Address]_, complete estos campos obligatorios:

   * **[!UICONTROL Street Address]**
   * **[!UICONTROL City]**
   * **[!UICONTROL Country]**
   * **[!UICONTROL ZIP/Postal Code]**
   * **[!UICONTROL Phone Number]**

1. En la sección _[!UICONTROL Company Admin]_, haga lo siguiente:

   * Rellene estos campos obligatorios:

      * **[!UICONTROL Email]**
      * **[!UICONTROL First Name]**
      * **[!UICONTROL Last Name]**

   * Complete las siguientes partes opcionales del nombre, que pueden aplicarse a algunos nombres de clientes más que a otros y pueden utilizarse a su discreción:

      * **[!UICONTROL Prefix]**
      * **[!UICONTROL Middle Name/Initial]**
      * **[!UICONTROL Suffix]**

   * Si la información está disponible, rellene los campos restantes para describir al administrador de la empresa:

      * **[!UICONTROL Website]**
      * **[!UICONTROL Job Title]**
      * **[!UICONTROL Work Phone Number]**
      * **[!UICONTROL Gender]**
      * **[!UICONTROL Send Welcome Email From]**

   ![Administrador de la empresa](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. En la sección _[!UICONTROL Company Credit]_, que muestra un resumen de la actividad de crédito del cliente, complete tantos campos de la parte inferior de la sección como corresponda:

   * **[!UICONTROL Credit Currency]**
   * **[!UICONTROL Credit Limit]**
   * **[!UICONTROL Allow to Exceed Credit Limit]**
   * **[!UICONTROL Reason for Change]**

   ![Crédito de la compañía](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

1. En la sección _[!UICONTROL Advanced Settings]_, haga lo siguiente:

   >[!NOTE]
   >
   >La asignación del grupo de clientes determina qué catálogo compartido está disponible para la compañía y sus empleados. De forma predeterminada, el sistema asigna la empresa al grupo de clientes configurado como predeterminado.

   * Puede cambiar la asignación **[!UICONTROL Customer Group]** para la compañía y sus empleados a un grupo que tenga acceso a un catálogo compartido diferente o a un grupo de clientes estándar. El sistema le pedirá que confirme antes de cambiar el grupo.

     ![Cambiando el grupo de clientes](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

   * Si desea permitir que los empleados de la compañía generen presupuestos a partir de su cuenta, establezca **[!UICONTROL Allow Quotes]** en `Yes`.

   * Si desea permitir que los empleados de la compañía creen y usen pedidos de compra desde su cuenta, establezca **[!UICONTROL Enable Purchase Orders]** en `Yes`.

   * Para cambiar los **[!UICONTROL Applicable Payment Methods]** que están disponibles para la compañía, desactive la casilla de verificación **[!UICONTROL Use config settings]** y elija una de las siguientes opciones:

     | Opción | Descripción |
     |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
     | `B2B Payment Methods` | (Predeterminado) Habilita todos los [métodos de pago establecidos como predeterminados](../configuration-reference/general/b2b-features.md#default-b2b-payment-methods) para pedidos B2B. |
     | `All Enabled Payment Methods` | Hace que todos los [métodos de pago habilitados](../configuration-reference/sales/payment-methods.md) estén disponibles para las cuentas de cliente asociadas con la cuenta de la compañía. |
     | `Selected Payment Methods` | Permite seleccionar los métodos de pago disponibles para las cuentas de cliente asociadas a la cuenta de compañía. Para seleccionar varios métodos de pago, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y seleccione cada opción. |

     {style="table-layout:auto"}

   * Para cambiar los **[!UICONTROL Applicable Shipping Methods]** que están disponibles para la compañía, desactive la casilla de verificación **[!UICONTROL Use config settings]** y elija una de las siguientes opciones:

     | Opción | Descripción |
     |--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
     | `B2B Shipping Methods` | (Predeterminado) Habilita todos los [métodos de envío establecidos como predeterminados](../configuration-reference/general/b2b-features.md#default-b2b-shipping-methods) para pedidos B2B. |
     | `All Enabled Shipping Methods` | Hace que todos los [métodos de envío habilitados](../configuration-reference/sales/delivery-methods.md) estén disponibles para las cuentas de cliente asociadas con la cuenta de compañía. |
     | `Selected Shipping Methods` | Permite seleccionar los métodos de envío disponibles para las cuentas de cliente asociadas a la cuenta de compañía. Para seleccionar varios métodos de envío, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y seleccione cada opción. |

     {style="table-layout:auto"}

1. Una vez finalizado, seleccione **[!UICONTROL Save]**.

   Cuando el comerciante aprueba la solicitud de creación de una cuenta de empresa, se envía una notificación por correo electrónico a la dirección de correo electrónico del administrador de la empresa.

   Una vez establecida la contraseña, el administrador de la empresa puede [iniciar sesión](../customers/customer-sign-in.md) en la cuenta.

## Después de la creación de cuenta

Una vez creada una cuenta de compañía, se produce el siguiente proceso:

### &#x200B;1. Flujo de trabajo de aprobación

* **Estado pendiente**: las nuevas cuentas esperan la revisión del administrador
* **Proceso de revisión**: los administradores del almacén comprueban la información empresarial y aprueban o rechazan las solicitudes
* **Actualizaciones de estado**: las empresas reciben notificaciones por correo electrónico sobre cambios de estado de aprobación

### &#x200B;2. Activación de la cuenta

* **Correo electrónico de bienvenida**: los administradores de la empresa aprobados reciben instrucciones de configuración
* **Configuración de contraseña**: los administradores crean contraseñas seguras para el acceso a la cuenta
* **Inicio de sesión inicial**: acceso por primera vez al tablero y las características de la empresa

### &#x200B;3. Pasos siguientes para los administradores de la empresa

Después de la activación, los administradores de la empresa deben:

* **[Configurar la estructura de la compañía](account-company-structure.md)**: configure los departamentos y la jerarquía de usuarios
* **[Administrar usuarios de la compañía](account-company-users.md)**—Agregar empleados y asignar funciones
* **[Configurar pedidos](purchase-order-flow.md)**: configure los flujos de trabajo de aprobación si es necesario
* **[Revisar la configuración de crédito](credit-company.md)**: comprender y administrar el crédito de la compañía (si está habilitado)

## Problemas comunes y solución de problemas

### Problemas de creación de cuentas

**Error al enviar el formulario de registro**

* Verifique que todos los campos obligatorios se hayan completado correctamente
* Compruebe que las direcciones de correo electrónico sean válidas y únicas
* Asegúrese de que las funciones B2B estén habilitadas y de que se permita el registro de empresa
* Borre la caché del explorador e inténtelo de nuevo

**El Nombre De La Empresa Ya Existe**

* Elija un nombre de empresa único.
* Póngase en contacto con el administrador si cree que se trata de un error
* Considere la posibilidad de agregar una ubicación o un identificador de unidad empresarial

**Problemas con la dirección de correo electrónico**

* Utilice direcciones de correo electrónico comerciales en lugar de personales
* Asegúrese de que el correo electrónico del administrador de la empresa sea accesible
* Compruebe que los filtros de correo electrónico no hayan bloqueado el dominio

### Problemas de aprobación y activación

**Correo electrónico de aprobación no recibido**

* Comprobar carpetas de correo no deseado
* Verifique que la dirección de correo electrónico se haya introducido correctamente durante el registro
* Póngase en contacto con el administrador de la tienda para comprobar manualmente el estado de aprobación
* Conceda un margen de 24 a 48 horas para el procesamiento durante los días laborables

**No Se Puede Establecer La Contraseña Después De La Aprobación**

* Utilice el vínculo exacto proporcionado en el correo electrónico de aprobación
* Compruebe si el vínculo de activación ha caducado
* Solicite un nuevo correo electrónico de activación al administrador

**Problemas De Acceso Después De La Activación**

* Compruebe que está iniciando sesión a través del portal correcto de la cuenta de la compañía
* Compruebe que su estado de cuenta sea &quot;Activo&quot;
* Asegúrese de que está utilizando las credenciales de administrador de la empresa
* Póngase en contacto con el servicio de asistencia si los permisos parecen incorrectos

## Prácticas recomendadas de seguridad

Al crear y administrar cuentas de empresa:

* **Usar contraseñas sólidas**: requiere contraseñas complejas para los administradores de la empresa
* **Verificar información empresarial**: valide los detalles de la compañía durante el proceso de aprobación
* **Supervisar la actividad de la cuenta**: revise con regularidad el acceso y los permisos de los usuarios de la empresa
* **Proteger datos confidenciales**: Asegúrese de que la información financiera y de crédito esté protegida correctamente

## Referencia de interfaz de usuario de cuenta de compañía

### Barra de botones

| Botón | Descripción |
|---------------------------|------------------------------------------------------------------|
| [!UICONTROL Back] | Vuelve a la página Compañías sin guardar los cambios. |
| [!UICONTROL Reset] | Restaura los valores originales en cualquier campo con cambios no guardados. |
| [!UICONTROL Save] | Guarda los cambios en la empresa y mantiene el perfil abierto. |
| [!UICONTROL Save & Close] | Guarda los cambios realizados en la empresa y cierra el perfil. |

{style="table-layout:auto"}

### Descripciones de campos

| Campo | Descripción |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Name] | El nombre de la empresa se introduce la primera vez que se crea la cuenta de la empresa y puede ser una versión abreviada del nombre legal completo. |
| [!UICONTROL Status] | (Solo administrador) Indica el estado actual de la cuenta de la compañía. Opciones: <br/>**[!UICONTROL Active]**: el administrador del almacén ha aprobado la cuenta de la empresa. El administrador de la empresa y los miembros asociados pueden iniciar sesión en la cuenta desde la tienda y realizar compras.<br/>**[!UICONTROL Pending Approval]** - Se ha enviado una solicitud para abrir una cuenta de compañía, pero el administrador del almacén aún no la ha aprobado. <br/>**[!UICONTROL Rejected]**- Se envió una solicitud para abrir una cuenta de compañía, pero el administrador del almacén no la aprobó. Las credenciales de inicio de sesión iniciales utilizadas para enviar la solicitud están bloqueadas.<br/>** Bloqueado **: los miembros de la compañía pueden iniciar sesión y acceder al catálogo, pero no pueden realizar compras. El administrador de la tienda podría bloquear una cuenta de empresa que no esté al día. El administrador de la tienda puede eliminar el bloque de la cuenta en cualquier momento. |
| [!UICONTROL Company Email] | La dirección de correo electrónico asociada a la cuenta de la empresa. |
| [!UICONTROL Sales Representative] | (Solo administrador) El usuario administrador que es el contacto principal de la cuenta de la compañía. |

{style="table-layout:auto"}

#### [!UICONTROL Account Information]

| Campo | Descripción |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | El nombre legal completo de la compañía. |
| [!UICONTROL VAT / TAX ID] | El número de [impuesto al valor agregado](../stores-purchase/vat.md) que algunas jurisdicciones asignan a la compañía con fines de informes de impuestos. Para configurar el ID. IVA/IMPUESTO del cliente para que aparezca en la tienda, consulte [Crear nuevas opciones de cuenta](../configuration-reference/customers/customer-configuration.md). <br/> **_Nota:_** El administrador de la compañía y otros usuarios de la compañía no tienen sus propios números de identificación fiscal/IVA separados en sus cuentas de cliente. |
| [!UICONTROL Reseller ID] | El número de reventa asignado a la compañía con fines de información fiscal. |
| [!UICONTROL Comment] | (Solo administrador) Estas notas sobre la cuenta de la compañía son de referencia y visibles solo desde el administrador. |

{style="table-layout:auto"}

#### [!UICONTROL Company Hierarchy]

| Campo | Descripción |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company ID] | El número de ID de la empresa. |
| [!UICONTROL Company Name] | El nombre completo de la empresa. <br/>Aparece un(a) `current company indicator` en la línea de compañía que se está editando. |
| [!UICONTROL Company Email] | La dirección de correo electrónico asociada a la cuenta de la empresa. |
| [!UICONTROL Phone Number] | El número de teléfono principal de la empresa. |
| [!UICONTROL Country] | El país donde está registrada la compañía para llevar a cabo sus negocios. |
| [!UICONTROL State/Province] | El estado o provincia donde la compañía está registrada para llevar a cabo actividades comerciales. |
| [!UICONTROL City] | La ciudad donde está registrada la compañía para realizar negocios. |
| [!UICONTROL Group/Shared Catalog] | (Solo administrador) Muestra el [grupo de clientes](../customers/customer-groups.md) o el [catálogo compartido](catalog-shared.md) asignado a la compañía. |
| [!UICONTROL Company Admin] | Nombre completo del administrador de la empresa. |
| [!UICONTROL Action] | La lista de posibles acciones para esa línea de compañía. |

{style="table-layout:auto"}

#### [!UICONTROL Legal Address]

| Campo | Descripción |
|------------------------------|-----------------------------------------------------------------------------|
| [!UICONTROL Street Address] | Dirección de la calle donde está registrada la empresa para realizar actividades comerciales. |
| [!UICONTROL City] | La ciudad donde está registrada la compañía para realizar negocios. |
| [!UICONTROL Country] | El país donde está registrada la compañía para llevar a cabo sus negocios. |
| [!UICONTROL State/Province] | El estado o provincia donde la compañía está registrada para llevar a cabo actividades comerciales. |
| [!UICONTROL ZIP/Postal Code] | El código postal en el que la empresa está registrada para llevar a cabo actividades comerciales. |
| [!UICONTROL Phone Number] | El número de teléfono principal de la empresa. |

{style="table-layout:auto"}

#### [!UICONTROL Company Admin]

| Campo | Descripción |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Website] | Determina el sitio web al que pertenece el administrador de la empresa. |
| [!UICONTROL Job Title] | El título del administrador de la empresa que administra la cuenta de la empresa. |
| [!UICONTROL Work Phone Number] | Número de teléfono del administrador de la empresa que administra la cuenta de la empresa. |
| [!UICONTROL Email] | La dirección de correo electrónico del administrador de la empresa puede ser la misma que la dirección de correo electrónico de la empresa. Si introduce una dirección de correo electrónico diferente, el sistema crea una cuenta individual independiente para el administrador de la empresa, además de la cuenta de la empresa. |
| [!UICONTROL Prefix] | Si corresponde, el prefijo asociado con el nombre del administrador de la empresa (como `Mr.`, `Ms.`, `Mrs.` o `Dr.`). Según la configuración, el campo de entrada puede ser un campo de texto o una lista. |
| [!UICONTROL First Name] | El nombre del administrador de la empresa. |
| [!UICONTROL Middle Name/Initial] | El segundo nombre o la inicial del administrador de la empresa. |
| [!UICONTROL Last Name] | Apellidos del administrador de la empresa. |
| [!UICONTROL Suffix] | Si procede, el sufijo asociado al nombre del administrador de la empresa (como `Jr.`, `Sr.` o `III.`). Según la configuración, el campo de entrada puede ser un campo de texto o una lista. |
| [!UICONTROL Gender] | El sexo del administrador de la empresa. Opciones: `Male` / `Female` / `Not Specified` |
| [!UICONTROL Send Welcome Email From] | La vista de tienda desde la que el sistema envía el correo electrónico de bienvenida. |

{style="table-layout:auto"}

#### [!UICONTROL Company Credit]

| Campo | Descripción |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Credit Currency] | (Solo administrador) La moneda que acepta la tienda para compras a crédito de la empresa. |
| [!UICONTROL Credit Limit] | (Solo administrador) El límite de crédito que se amplía a la cuenta de la compañía. |
| [!UICONTROL Allow to Exceed Credit Limit] | (Solo administrador) Indica si la empresa tiene permiso para superar el límite de crédito. Opciones: `Yes` / `No` |
| [!UICONTROL Reason for Change] | (Solo administrador) Una nota que explica por qué se permite a la compañía o no exceder el límite de crédito. Este campo solo está activo si cambia el permiso para superar el límite de crédito. |

{style="table-layout:auto"}

#### [!UICONTROL Advanced Settings]

Puede establecer la configuración avanzada para empresas individuales. Si crea una jerarquía de compañías, puede optimizar la configuración configurando las opciones de la compañía principal y aplicando esas opciones a todas las compañías secundarias o a las seleccionadas, en lugar de configurar cada compañía secundaria individualmente. Para obtener más información, consulte [Administrar la jerarquía de la compañía](manage-company-hierarchy.md).

| Campo | Descripción |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Customer Group] | (Solo administrador) Muestra el [grupo de clientes](../customers/customer-groups.md) o el [catálogo compartido](catalog-shared.md) asignado a la compañía. |
| [!UICONTROL Allow Quotes] | (Solo administrador) Determina si los miembros de la compañía pueden preparar y enviar presupuestos negociables en nombre de la compañía. |
| [!UICONTROL Enable Purchase Orders] | (Solo administrador) Determina si los miembros de la compañía pueden enviar pedidos como [pedidos de compra](account-dashboard-my-purchase-orders.md) en nombre de la compañía. |
| Métodos de pago aplicables | (Solo administrador) Indica los métodos de pago disponibles para las compras de la empresa. Opciones: `B2B Payment Methods` / `All Enabled Payment Methods` / `Selected Payment Methods` |
| [!UICONTROL Payment Methods] | (Solo administrador) Se activa si activa métodos de pago específicos. Para que varios métodos de pago estén disponibles en la cuenta de la empresa, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y seleccione cada opción. |
| [!UICONTROL Applicable Shipping Methods] | (Solo administrador) Indica los métodos de envío disponibles para las compras de la empresa. Opciones: `B2B Shipping Methods` / `All Enabled Shipping Methods` / `Selected Shipping Methods` |
| [!UICONTROL Shipping Methods] | (Solo administrador) Se activa si activa métodos de envío específicos. Para que varios métodos de envío estén disponibles en la cuenta de la empresa, mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y seleccione cada opción. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Habilitar características B2B](enable-basic-features.md): configure la funcionalidad B2B básica
>* [Estructura de cuenta de la compañía](account-company-structure.md): organiza a los usuarios y departamentos desde la tienda
>* [Administrar usuarios de la compañía](account-company-users.md)—Agregar y configurar cuentas de empleado desde la tienda
>* [Función de administrador de la empresa](account-company-admin.md): comprenda las responsabilidades de administrador
>* [Administrar compañías](manage-companies.md): información general administrativa sobre la administración de compañías
>* [Administración de crédito de la compañía](credit-company.md): configure y administre el crédito de la compañía del administrador
>* [Flujo de trabajo de pedidos de compra](purchase-order-flow.md): configure los procesos de aprobación del administrador
>* [Roles y permisos de la compañía](account-company-roles-permissions.md): controle los niveles de acceso de los usuarios desde el administrador
>* [Referencia de configuración B2B](../configuration-reference/general/b2b-features.md): configuración detallada del sistema
