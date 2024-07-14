---
title: Impuesto sobre el valor añadido (IVA)
description: '&lt;Agregar descripción aquí&gt;'
exl-id: 20dbcb86-e558-47f2-968d-b5c9ec5f665b
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1990'
ht-degree: 0%

---

# Impuesto sobre el valor añadido (IVA)

Algunos países cobran un impuesto al valor agregado, o IVA, a los bienes y servicios. Puede haber diferentes tipos de IVA según la fase del proceso de fabricación o distribución, los materiales o los servicios que venda a sus clientes. Puede aplicar más de un tipo de IVA para calcular correctamente el impuesto adeudado.

Commerce se puede configurar para que aplique un impuesto sobre el valor añadido basado en la dirección del comerciante o del cliente, si ambos están en el mismo país. Los cálculos del IVA se basan generalmente en el destino del envío, en lugar de en su punto de origen. En la mayoría de los casos, es suficiente una configuración que calcule el IVA en función de la dirección de envío del cliente.

## Casos de ejemplo

- Para una empresa con IVA registrado en un país de la UE que entrega bienes a un particular en otro país de la UE, el IVA se calcula como una &quot;venta a distancia&quot; basada en la ubicación del comerciante.

- Una empresa en los Países Bajos que realiza una compra en una tienda en el Reino Unido que se envía a una dirección en el Reino Unido está obligada a pagar los tipos de IVA del Reino Unido.

- Para la venta de [productos descargables](../catalog/product-create-downloadable.md) o _bienes digitales_, la tasa de IVA se basa en el destino de envío, en lugar de en la ubicación del comerciante. Ver [Lugar de suministro de artículos digitales](taxes.md#place-of-supply-for-digital-goods-eu).

>[!TIP]
>
>Algunos envíos transfronterizos y B2B tienen requisitos fiscales más complejos. Para ampliar las capacidades nativas de su instalación de Commerce, considere la posibilidad de agregar una solución de administración de impuestos desde [Marketplace](https://marketplace.magento.com/extensions/accounting-finance/taxes.html).

## Configurar IVA

Las siguientes instrucciones incluyen un procedimiento de ejemplo para configurar un IVA del 20 % en el Reino Unido para las ventas a clientes minoristas. Para otros tipos impositivos y países, siga el procedimiento general, pero introduzca información específica que corresponda a su país, tipo de IVA, tipos de clientes, etc.

>[!NOTE]
>
>Antes de continuar, asegúrate de averiguar qué reglas y regulaciones se aplican al IVA en tu área.

En determinadas transacciones entre empresas, el IVA no se evalúa. Commerce puede validar el ID de IVA de un cliente para asegurarse de que el IVA se evalúa (o no) correctamente. Consulte [Validación de ID de IVA](#vat-id-validation).

### Paso 1: Configurar clases de impuestos de cliente

El proceso de creación de una regla fiscal comienza añadiendo una tasa impositiva.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

   ![Configurar clases de impuestos de clientes](./assets/vat-zones.png){width="600" zoomable="yes"}

1. Asegúrese de que haya una clase de impuestos de cliente adecuada para usar con el IVA.

   Para este ejemplo, asegúrese de que haya una clase de impuestos de cliente llamada _Cliente comercial_. Si esta clase de impuestos no existe, haga clic en **[!UICONTROL Add New Tax Rate]**.

1. Escriba **[!UICONTROL Tax Identifier]** para la nueva clase de impuestos.

   Todas las tasas de impuestos se muestran en el campo _Tasa de impuestos_ en la _Información de regla de impuestos_ al crear reglas de impuestos.

1. Para establecer el intervalo del código postal (desde / hasta), active la casilla de verificación **[!UICONTROL Zip/Post is Range]**.

1. Elija **[!UICONTROL Country]** donde se aplica la tasa de impuestos.

1. Escriba el(la) **[!UICONTROL Rate Percent]** que se usaría para el cálculo de tasa de impuestos en la compra.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Rate]**.

Según el tipo impositivo enviado, puede crear reglas fiscales posteriores. A falta de tasas impositivas, la creación de reglas fiscales se vuelve imposible.

### Paso 2: Configurar clases de impuestos de productos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Haga clic en **[!UICONTROL Add New Tax Rule]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Additional Settings]**.

   ![Configurar clases de impuestos de productos](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. En _Clase de impuestos del producto_, haga clic en **[!UICONTROL Add New Tax Class]**.

1. Para agregar la nueva clase a la lista de clases de impuestos de productos disponibles y crear tres nuevas clases, escriba el **[!UICONTROL Name]** de la nueva clase de impuestos y haga clic en la marca de verificación:

   - `VAT Standard`
   - `VAT Reduced`
   - `VAT Zero`

1. Haga clic en **[!UICONTROL Save Class]** para cada nueva clase que agregue.

1. Haga clic en **[!UICONTROL Save Rule]**.

### Paso 3: Configuración de zonas y tipos impositivos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

   Para este ejemplo, puede eliminar las tasas de impuestos de EE. UU. o dejarlas tal cual.

1. Haga clic en **[!UICONTROL Add New Tax Rate]**.

   ![Configurar zonas y tasas de impuestos](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

1. Defina nuevas tasas de la siguiente manera:

   **Estándar de IVA**

   - Identificador fiscal: `VAT Standard`
   - País y estado: `United Kingdom`
   - Porcentaje de tarifa: `20.00`

   **IVA reducido**

   - Identificador fiscal: `VAT Reduced`
   - País y estado: `United Kingdom`
   - Porcentaje de tarifa: `5.00`

1. Haga clic en **[!UICONTROL Save Rate]** para cada tarifa.

### Paso 4: Configuración de reglas de impuestos

Una regla fiscal es una combinación de una clase de impuestos de cliente, una clase de impuestos de producto y un tipo impositivo.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Añada nuevas reglas fiscales como se indica a continuación:

   **Estándar de IVA**

   - Nombre: `VAT Standard`
   - Clase de impuestos del cliente: `Retail Customer`
   - Clase de impuestos del producto: `VAT Standard`
   - Tasa de impuestos: `VAT Standard Rate`

   **Iva Reducida**

   - Nombre: `VAT Reduced`
   - Clase de impuestos del cliente: `Retail Customer`
   - Clase de impuestos del producto: `VAT Reduced`
   - Tasa de impuestos: `VAT Reduced Rate`

1. Haga clic en **[!UICONTROL Save Rule]** para cada tarifa.

### Paso 5: Aplicar clases de impuestos a los productos

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Manage Products]**.

1. Abra un producto del catálogo en modo de edición.

1. En la página _General_, busque la opción **[!UICONTROL Tax Class]** y seleccione **[!UICONTROL VAT Class]** que se aplica al producto.

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

   ![Aplicar clases de impuestos a productos](./assets/vat-apply-classes.png){width="600" zoomable="yes"}

## Descripciones de campos

### Almacenar información

Commerce usa los siguientes [ajustes de configuración de información de tienda](../configuration-reference/general/general.md#store-information) para calcular el IVA según la información del comerciante.

**[!UICONTROL VAT Number]**: número de impuesto al valor agregado asignado al comerciante.

**[!UICONTROL Validate VAT Number]** - [Validación de IVA](#vat-id-validation) confirma que el número de IVA coincide con el registro correspondiente en la base de datos de [Comisión Europea](https://ec.europa.eu/taxation_customs/vies/).

### Información del cliente

Commerce usa los campos siguientes para calcular el IVA según [información del cliente](../customers/account-dashboard-account-information.md)).

#### Información de cuenta

**[!UICONTROL Tax/VAT Number]**: si corresponde, el número de impuesto o el número de impuesto al valor agregado asignado al cliente.

#### Direcciones

**[!UICONTROL VAT Number]**: si corresponde, el número de impuesto al valor agregado asociado con una dirección de facturación o envío específica del cliente. Para la venta de [bienes digitales](taxes.md#place-of-supply-for-digital-goods-eu)) dentro de la UE, el monto del IVA se basa en el destino de envío.

### Cuenta de cliente

Commerce usa los siguientes [ajustes de configuración del cliente](../customers/account-options-new.md) para calcular el IVA.

**[!UICONTROL Show VAT Number on Storefront]**: determina si el campo Número de IVA de cliente está incluido en la Libreta de direcciones que está disponible en la cuenta de cliente.

**[!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID]** - ID de IVA es un identificador interno del número de IVA del cliente cuando se utiliza en la validación de IVA. Durante la validación del IVA, Commerce confirma que el número coincide con la base de datos de [European Commission](https://ec.europa.eu/taxation_customs/vies/). Los clientes se pueden asignar automáticamente a uno de los cuatro grupos de clientes predeterminados en función de los resultados de validación.

## Validación de ID de IVA

_Validación de ID de IVA_ calcula automáticamente el impuesto requerido para las transacciones B2B que tienen lugar dentro de la Unión Europea (UE), según la configuración regional del comerciante y del cliente. Commerce realiza la validación de ID de IVA utilizando los servicios web del servidor [European Commission][1].

>[!NOTE]
>
>Las normas fiscales relacionadas con el IVA no influyen en otras normas fiscales y no impiden la aplicación de otras normas fiscales. Solo se puede aplicar una regla fiscal a la vez.

- El IVA se cobra si el comerciante y el cliente se encuentran en el mismo país de la UE.
- El IVA no se cobra si el comerciante y el cliente están en diferentes países de la UE, y ambas partes son entidades comerciales registradas en la UE.

El administrador de la tienda crea más de un grupo de clientes predeterminado que se puede asignar automáticamente al cliente durante la creación de la cuenta, la creación o actualización de la dirección y el cierre de compra. El resultado es que se utilizan distintas normas fiscales para las ventas dentro de los países (nacionales) y dentro de la UE.

>[!IMPORTANT]
>
>Si vende productos virtuales o descargables, que no requieren envío, el tipo de IVA del país de ubicación de un cliente debe utilizarse tanto para las ventas dentro de la unión como para las ventas nacionales. Cree reglas de impuestos individuales adicionales para las clases de impuestos de productos que correspondan a los productos virtuales.

### Flujo de trabajo de registro de clientes

Si la validación del IVA está activada, después del registro se propone a cada cliente que introduzca el número de IVA. Sin embargo, solo los compradores que son clientes de IVA registrados deben rellenar este campo.

Una vez que un cliente especifica el número de IVA y otros campos de dirección y decide guardarlos, el sistema guarda la dirección y envía la solicitud de validación del ID de IVA al servidor de la Comisión Europea. Según los resultados de la validación, uno de los grupos predeterminados se asigna a un cliente. Este grupo se puede cambiar si un cliente o un administrador cambia el ID de IVA de la dirección por defecto o cambia la dirección por defecto completa. A veces, el grupo se puede cambiar temporalmente (se emula el cambio de grupo) durante la desprotección de una página.

Si está activada, puede anular la validación de ID de IVA para clientes individuales seleccionando la casilla de verificación en la página _[!UICONTROL Customer Information]_.

### Flujo de trabajo de retirada

Si la validación del IVA de un cliente se realiza durante el cierre de compra, el identificador de la solicitud de IVA y la fecha de la solicitud de IVA se guardan en la sección Historial de comentarios del pedido.

El comportamiento del sistema en relación con la validación del IVA y el cambio del grupo de clientes durante el cierre de compra depende de cómo se configuren los ajustes Validar en cada transacción y Desactivar cambio automático de grupo. En esta sección se describe la implementación de la funcionalidad de validación de ID de IVA para el cierre de compra en el front-end.

Si el cliente utiliza Google Express Checkout, PayPal Express Checkout u otro método de pago externo, el pago se realiza completamente en el lado de la puerta de enlace de pago externa. En este escenario, no se puede aplicar la configuración _Validar en cada transacción_ y el grupo de clientes no puede cambiar durante el cierre de compra.

![Flujo de trabajo de cierre de validación de IVA](./assets/vat-id-validation2.png){width="550" zoomable="yes"}

### Configurar validación de ID de IVA

Para configurar la validación del ID de IVA, primero debe configurar los grupos de clientes necesarios y crear las clases de impuestos, los tipos impositivos y las reglas relacionadas. A continuación, habilite la validación del ID de IVA para la tienda y complete la configuración.

Los siguientes ejemplos muestran cómo se utilizan las clases y los tipos impositivos para la validación de ID de IVA. Revise los ejemplos y siga las instrucciones para configurar las clases de impuestos y las reglas necesarias para su tienda.

#### Ejemplo: Reglas de impuestos mínimas requeridas para la validación del ID de IVA

| #1 de regla fiscal |  |
|--- |--- |
| Clase de impuestos del cliente | Las clases de impuestos del cliente deben incluir: <br />Una clase para clientes nacionales. <br />Clase para clientes con ID de IVA con formato incorrecto.<br />Clase para clientes cuya validación de identificación de IVA ha fallado. |
| Clase de impuestos del producto | Las clases de impuestos de productos deben incluir una clase para productos de todos los tipos, excepto paquete y virtual. |
| Tipo Impositivo | El tipo impositivo debe incluir el tipo del IVA del país del comerciante. |

{style="table-layout:auto"}

| #2 de regla fiscal |   |
|--- |--- |
| Clase de impuestos del cliente | Una clase para clientes dentro de la unión. |
| Clase de impuestos del producto | Una clase para productos de todo tipo, excepto virtuales. |
| Tipo Impositivo | Tipos de IVA para todos los países de la UE, excepto el país del comerciante. Actualmente, esta tasa es del 0 %. |

{style="table-layout:auto"}

| #3 de regla fiscal | (Necesario para productos virtuales y descargables) |
|--- |--- |
| Clase de impuestos del cliente | Las clases de impuestos del cliente deben incluir: <br/>Una clase para clientes nacionales <br/>Una clase para clientes con Id. de IVA no válido Clase para clientes en los que no se pudo validar el Id. de IVA |
| Clase de impuestos del producto | Una clase para productos virtuales. |
| Tipo Impositivo | Tipo del IVA del país del comerciante. |

{style="table-layout:auto"}

| #4 de regla fiscal | (Necesario para productos virtuales y descargables) |
|--- |--- |
| Clase de impuestos del cliente | Una clase para clientes dentro de la unión. |
| Clase de impuestos del producto | Una clase para productos virtuales. |
| Tipo Impositivo | Tipos de IVA para todos los países de la UE, excepto el país del comerciante. Actualmente, esta tasa es del 0 %. |

{style="table-layout:auto"}

#### Paso 1: Crear grupos de clientes relacionados con el IVA

La validación de ID de IVA asigna automáticamente uno de los cuatro grupos de clientes predeterminados a los clientes según los resultados de validación de ID de IVA:

- Nacional
- Dentro de la UE
- ID de IVA no válido
- Error de validación

Puede crear grupos de clientes para la validación de IVA ID o utilizar grupos existentes, si cumplen con su lógica empresarial. Al configurar la validación de ID de IVA, debe asignar cada uno de los grupos de clientes creados como valor por defecto para los clientes con los resultados de validación de ID de IVA adecuados.

#### Paso 2: Crear clases, tipos y reglas relacionadas con el IVA

Cada regla fiscal se define mediante tres entidades:

- Clases de Impuestos del Cliente
- Clases de impuestos de productos
- Tipos impositivos

Cree las [reglas de impuestos](tax-rules.md) para usar la validación de ID de IVA de forma efectiva.

- Las reglas de impuestos incluyen tasas de impuestos y [clases de impuestos](tax-class.md).
- Las clases de impuestos se asignan a [grupos de clientes](../customers/customer-groups.md).

#### Paso 3: Habilitar y configurar la validación de ID de IVA

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Si es necesario, establezca **[!UICONTROL Store View]** para la configuración.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Customer Configuration]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Create New Account Options]**.

   En el ejemplo siguiente, la configuración general del cliente que no está relacionada con la validación del IVA es tenue.

   ![Crear nuevas opciones de cuenta](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Enable Automatic Assignment to Customer Group]** en `Yes` y complete los campos siguientes según sea necesario.

   - **[!UICONTROL Default Group]**
   - **[!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID]**
   - **[!UICONTROL Show VAT Number on Storefront]**

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

#### Paso 4: Establece tu número de IVA y tu país de ubicación

1. En el panel izquierdo, expanda **[!UICONTROL General]** y elija **[!UICONTROL General]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Store Information]**.

   ![Información de la tienda](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. Seleccione su **[!UICONTROL Country]**.

1. Escriba su **[!UICONTROL VAT Number]** y haga clic en **[!UICONTROL Validate VAT Number]**.

   El resultado aparece inmediatamente.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

#### Paso 5: Verificar la lista de países miembros de la UE

1. Continuando en la página de configuración _General_, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Countries Options]**.

   ![Opciones de países](../configuration-reference/general/assets/general-country-options.png){width="600" zoomable="yes"}

1. En la lista **[!UICONTROL European Union Countries]**, compruebe que está seleccionado cada país miembro de la UE.

   Para cambiar la configuración predeterminada, desactive la casilla de verificación **Usar valores del sistema**. Mantenga pulsada la tecla Ctrl (PC) o la tecla Comando (Mac) y haga clic en cada país que desee añadir o quitar.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.


[1]: https://ec.europa.eu/taxation_customs/vies/
