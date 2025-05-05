---
title: Administrar las cuentas de cliente
description: Utilice la cuadrícula [!UICONTROL Customers] para buscar cualquier cuenta de cliente y obtener acceso a la información de cuentas de cliente individuales.
exl-id: 5f817ca8-9d1f-4498-b3bd-989713f0b6ad
source-git-commit: 0316475a37ee09948b9ba3649e059155212ab1ae
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 0%

---

# Administrar las cuentas de cliente

Utilice la cuadrícula _[!UICONTROL Customers]_&#x200B;para encontrar cualquier cuenta de cliente. Puede usar los [controles de área de trabajo](../getting-started/admin-workspace.md) estándar para filtrar la lista, cambiar el [diseño de la columna](../getting-started/admin-grid-controls.md), guardar vistas y exportar datos. El control [Actions](../getting-started/admin-actions-control.md) sobre la cuadrícula se puede usar para aplicar una operación a varios registros de clientes.

![Todos los clientes](assets/customers-all-customers.png){width="700" zoomable="yes"}

Consulte [Actualizar el perfil del cliente](update-account.md) para obtener información sobre cómo realizar actualizaciones manuales en una cuenta de cliente.

## Acciones de cuenta de cliente

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. En la primera columna de la cuadrícula, active la casilla de verificación de cada registro que desee actualizar.

1. Siga las instrucciones de la acción que desee aplicar.

   >[!INFO]
   >
   >Las siguientes acciones se pueden aplicar a registros únicos o múltiples.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

### Suscribirse a la newsletter

En configuraciones de varias tiendas y sitios con un [ámbito de cuenta de cliente](../customers/customer-account-scope.md) global, se puede suscribir una cuenta de cliente a boletines de varios sitios o tiendas. Si aplica la acción _Suscribirse_ a una cuenta de cliente, se activa la suscripción al boletín informativo únicamente para la vista predeterminada del sitio o la tienda.

* Establezca el control **[!UICONTROL Actions]** en `Subscribe to newsletter`.

Consulte [Administrar suscriptores](../merchandising-promotions/newsletter-subscribers.md) para obtener más información sobre la administración de suscripciones a boletines para un cliente.

### Cancelar suscripción a la newsletter

En configuraciones de varias tiendas y sitios con un [ámbito de cuenta de cliente](customer-account-scope.md) global, se puede suscribir una cuenta de cliente a boletines para varios sitios o tiendas. Si aplica la acción _Cancelar la suscripción_ a una cuenta de cliente, se cancelará la suscripción a todas las suscripciones activas.

1. Establezca el control **[!UICONTROL Actions]** en `Unsubscribe to newsletter`.

1. Cuando se le pida que confirme, haga clic en **Aceptar**.

### Asignar un grupo de clientes

1. Establezca el control **[!UICONTROL Actions]** en `Assign a customer group`.

1. Elija el grupo de clientes al que se deben asignar todos los registros de clientes seleccionados.

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL OK]**.

### Eliminar cuentas de cliente

Las cuentas de cliente eliminadas no se pueden restaurar. La información sobre la actividad y las transacciones del cliente se conserva en el sistema.

1. Establezca el control **[!UICONTROL Actions]** en `Delete`.

1. Cuando se le pida que confirme, haga clic en **[!UICONTROL OK]**.

## Exportar cuentas de clientes

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. En el menú Encabezado de tabla, haga clic en **[!UICONTROL Export]** y seleccione el formato que desee:

   * CSV
   * XML de Excel

1. Haga clic en **[!UICONTROL OK]**.

   El archivo va a la carpeta de descargas predeterminada.

La instrucción anterior exporta todas las cuentas de cliente. Si desea exportar un conjunto limitado, seleccione las casillas de verificación de las cuentas que desee exportar o utilice filtros en el panel de control para seleccionar un rango de cuentas de cliente.

## Acciones/controles

| Opción | Descripción |
|--- |--- |
| **[!UICONTROL Delete]** | Elimina las cuentas de cliente seleccionadas. Si la cuenta de cliente pertenece a un administrador de empresa de un almacén B2B, se debe asignar a otro usuario de empresa como administrador antes de poder eliminar la cuenta de cliente. |
| **[!UICONTROL Subscribe to Newsletter]** | Suscribe a los clientes seleccionados a la newsletter. |
| **[!UICONTROL Unsubscribe from Newsletter]** | Cancela la suscripción de la newsletter de los clientes seleccionados. |
| **[!UICONTROL Assign a Customer Group]** | Asigna los clientes seleccionados a un grupo de clientes. |
| **[!UICONTROL Edit]** | Permite editar algunos valores de un único registro de cliente seleccionado desde la cuadrícula. De forma predeterminada, los siguientes valores están disponibles para una edición rápida: Correo electrónico, Grupo, Teléfono, ZIP, Sitio web, Número de IVA fiscal y Género. |

{style="table-layout:auto"}

## Columnas

| Columna | Descripción |
|--- |--- |
| **[!UICONTROL Select]** | Administra las selecciones de casilla de verificación de los registros del cliente para aplicar una acción. También puede utilizar el control de selección del encabezado de columna para seleccionar o deseleccionar todo. |
| **[!UICONTROL ID]** | Identificador numérico único que se asigna al crear la cuenta del cliente. |
| **[!UICONTROL Name]** | El nombre y los apellidos del cliente. |
| **[!UICONTROL Email]** | La dirección de correo electrónico del cliente. |
| **[!UICONTROL Group]** | El grupo de clientes al que está asignado el cliente. |
| **[!UICONTROL Phone]** | Número de teléfono del cliente. |
| **[!UICONTROL ZIP]** | El código postal del cliente. |
| **[!UICONTROL Country]** | El país donde se encuentra el cliente. |
| **[!UICONTROL State/Province]** | Estado o provincia donde se encuentra el cliente. |
| **[!UICONTROL Customer Since]** | La fecha y la hora de creación de la cuenta del cliente. |
| **[!UICONTROL Web Site]** | El sitio web en la jerarquía de almacén al que está asociada la cuenta de cliente. |
| **[!UICONTROL Confirmed Email]** | Indica si se requiere un correo electrónico de confirmación. |
| **[!UICONTROL Account Created In]** | Indica la vista de tienda desde la que se creó la cuenta de cliente. |
| **[!UICONTROL Date of Birth]** | La fecha de nacimiento del cliente. De acuerdo con las prácticas recomendadas actuales de seguridad y privacidad, tenga en cuenta cualquier posible riesgo legal y de seguridad asociado con el almacenamiento de la fecha de nacimiento completa de los clientes (mes, día, año) con otros identificadores personales. Se recomienda limitar el almacenamiento de las fechas de nacimiento completas de los clientes y sugerir el uso del año de nacimiento del cliente como alternativa. |
| **[!UICONTROL Tax / VAT Number]** | Si corresponde, el número de impuesto o el número de [impuesto al valor agregado](../stores-purchase/vat.md) que se ha asignado al cliente. <br/><br/> Este campo no es el mismo que el número de IVA. |
| **[!UICONTROL Gender]** | El sexo del cliente. |
| **[!UICONTROL Action]** | Editar: abre la cuenta de la empresa en modo de edición. |

{style="table-layout:auto"}

### Columnas adicionales

Estas columnas están disponibles al cambiar el [diseño de columna](../getting-started/admin-grid-controls.md) de la cuadrícula.

| Columna | Descripción |
|--- |--- |
| **[!UICONTROL Company]** | El nombre de empresa del cliente. |
| **[!UICONTROL Street Address]** | La dirección postal del cliente. |
| **[!UICONTROL City]** | La ciudad donde se encuentra el cliente. |
| **[!UICONTROL Fax]** | El número de fax del cliente, si corresponde. |
| **[!UICONTROL Billing Firstname]** | El nombre en la dirección de facturación del cliente. |
| **[!UICONTROL Billing Lastname]** | El apellido en la dirección de facturación del cliente. |
| **[!UICONTROL Billing Address]** | La dirección a la que se enviará la información de facturación. |
| **[!UICONTROL Shipping Address]** | La dirección a la que se enviarán los pedidos. |
| **[!UICONTROL VAT Number]** | El número de impuesto al valor agregado asociado con la dirección del cliente. Para [bienes digitales](../stores-purchase/taxes.md) vendidos en la UE, el IVA se basa en la dirección de facturación del cliente. <br/><br/> Este campo no es el mismo que el número de IVA/impuesto. |
| **[!UICONTROL Account Lock]** | Indica el estado de la cuenta. Como medida de seguridad, las cuentas de cliente pueden [bloquearse](../customers/password-options.md) después de demasiados intentos de inicio de sesión. Valores: `Locked` / `Unlocked` |
| **[!UICONTROL Status]** | El estado del usuario actual. Opciones: `Active` / `Inactive` |
| **[!UICONTROL Customer Type]** | Clasificación del cliente. Opciones: `Individual user` / `Company admin` / `Company user` |
| **[!UICONTROL Sales Representative]** | El representante de ventas asignado como punto de contacto para una cuenta de empresa y que recibe todos los mensajes de correo electrónico automatizados relacionados con la empresa. |

{style="table-layout:auto"}
