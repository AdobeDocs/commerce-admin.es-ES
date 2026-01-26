---
title: Crear etiquetas y paquetes de envío
description: Aprenda a empaquetar artículos en un pedido y a crear etiquetas de envío.
exl-id: ed9be72a-0dcd-4dbf-82ba-b1d75a1e76fd
feature: Shipping/Delivery, Orders
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1944'
ht-degree: 0%

---

# Crear etiquetas de envío

Para crear etiquetas de envío, primero debe configurar la cuenta de transportista para que admita las etiquetas. A continuación, siga las indicaciones para introducir una descripción del paquete y su contenido.

Después de configurar la información de etiquetas de envío y enviar un pedido, Commerce se conecta al sistema de transportista, envía un pedido y recibe una etiqueta de envío y un número de seguimiento. Si existe una etiqueta de envío para este envío en el sistema, se sustituye por una nueva. Sin embargo, los números de seguimiento existentes no se sustituyen. Cualquier número de seguimiento nuevo se agrega al existente.

## Paso 1: Póngase en contacto con sus transportistas

Antes de empezar, asegúrese de que sus cuentas de envío están configuradas para procesar etiquetas. Algunos transportistas podrían cobrar una tarifa adicional para agregar etiquetas de envío a su cuenta.

Póngase en contacto con cada transportista que utilice para activar las etiquetas de envío de su tienda.

Siga las instrucciones proporcionadas por cada transportista para agregar compatibilidad con etiquetas de envío a su cuenta.

- **FedEx** - Comuníquese con [FedEx Web Integration Services](https://www.fedex.com/en-us/api/get-support.html) para obtener información sobre los requisitos de impresión de etiquetas para su cuenta.
- **USPS**: consulta el [Portal de API de herramientas web](https://www.usps.com/business/web-tools-apis/#ssc) en el Centro de soporte técnico de envío para obtener información sobre cómo configurar tus credenciales de impresión de etiquetas.
- **UPS**- Póngase en contacto con [UPS](https://www.ups.com/us/en/support/contact-us.page) para confirmar que su cuenta admite etiquetas de envío. Para generar etiquetas de envío, debe utilizar la opción XML de UPS.
- **DHL** - Póngase en contacto con [DHL eCommerce Solutions](https://www.dhl.com/us-en/home/our-divisions/ecommerce-solutions.html) para conocer los requisitos de impresión de etiquetas para su cuenta.

## Paso 2: Actualizar la configuración de cada operador

1. Asegúrate de que tu [Información de la tienda](../getting-started/store-details.md#store-information) esté completa.

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y seleccione **[!UICONTROL Shipping Settings]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL Origin]** y configure **[!UICONTROL Shipping Origin Address]**.

1. Siga las instrucciones siguientes para cada cuenta de operador activada para la impresión de etiquetas.

### Configuración de UPS

United Parcel Service envía tanto a nivel nacional como internacional. Sin embargo, las etiquetas de envío solo se pueden generar para envíos que se originen dentro de Estados Unidos.

1. En la sección _[!UICONTROL Sales]_&#x200B;del panel izquierdo, elija **[!UICONTROL Delivery Methods]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL UPS]**.

1. Verifique que su UPS **[!UICONTROL Shipper Number]** sea correcto.

   Su número de transportista aparece solamente cuando [!DNL United Parcel Service XML] está habilitado.

1. Haga clic en **[!UICONTROL Save Config]**.

### Configuración de USPS

[!DNL United States Postal Service] se envía tanto nacional como internacionalmente.

{{$include /help/_includes/usps-api-type-configuration-note.md}}

1. Continuando con la configuración de **[!UICONTROL Delivery Methods]**, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL USPS]**.

1. Seleccione **[!UICONTROL USPS Type]** como `USPS Rest APIs` o `USPS Web Tools API`.

1. Compruebe que **[!UICONTROL Secure Gateway URL]** es correcto.

1. Escriba el(la) **[!UICONTROL Password]** proporcionado(a) por USPS.

1. Compruebe que se ha completado la siguiente configuración en función de los **[!UICONTROL USPS Type]** seleccionados:

   Si utiliza la API de herramientas web de USPS:
   - ID de usuario
   - Contraseña

   Si utiliza las API de REST de USPS:
   - Clave de consumidor
   - Secreto del consumidor
   - Opciones de precios
   - Tipo de cuenta
   - Número de cuenta
   - ID de registro de cliente (CRID)
   - Identificador de correo (MID)
   - MID de manifiesto
   - AES/ITN

1. Establezca **[!UICONTROL Size]** en `Large` e introduzca valores para las siguientes dimensiones:

   - Longitud
   - Ancho
   - Altura
   - Girth

1. Haga clic en **[!UICONTROL Save Config]**.

### Configuración de FedEx

FedEx realiza envíos nacionales e internacionales. Las tiendas ubicadas fuera de Estados Unidos pueden crear etiquetas de FedEx únicamente para envíos internacionales.

1. Continuando con la configuración de **[!UICONTROL Delivery Methods]**, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL FedEx]**.

1. Compruebe que las siguientes credenciales de FedEx sean correctas:

   - Número de medidor
   - Clave
   - Contraseña

1. Haga clic en **[!UICONTROL Save Config]**.

### Configuración de DHL

DHL ofrece servicios de envío internacional.

1. Continuando con la configuración de **[!UICONTROL Delivery Methods]**, expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección **[!UICONTROL DHL]**.

1. Compruebe que **[!UICONTROL Gateway URL]** es correcto.

1. Compruebe que las siguientes credenciales estén completas:

   - Access ID
   - Contraseña
   - Número de cuenta

1. Haga clic en **[!UICONTROL Save Config]**.

## Paso 3: Crear etiquetas de envío

### Método 1: Crear etiqueta para el nuevo envío

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Busque el orden en la cuadrícula y abra el registro.

   El estado del pedido debe ser `Pending` o `Processing`.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Ship]**.

1. Confirme la información de envío según los requisitos del transportista.

1. En la esquina inferior derecha, seleccione la casilla de verificación **[!UICONTROL Create Shipping Label]**.

1. Haga clic en **[!UICONTROL Submit Shipment]**.

1. Agregar o actualizar productos en el paquete:

   - Para agregar productos del pedido al paquete, haga clic en **[!UICONTROL Add Products]**. La columna _[!UICONTROL Quantity]_&#x200B;muestra la cantidad máxima de productos disponibles para el paquete.

   - Seleccione la casilla de verificación de cada producto que se agregará al paquete e introduzca el **[!UICONTROL Quantity]** de cada uno. A continuación, haga clic en **[!UICONTROL Add Selected Product(s) to Package]**.

   - Para agregar un paquete, haga clic en **[!UICONTROL Add Package]**.

   - Para eliminar un paquete, haga clic en **[!UICONTROL Delete Package]**.

   - Para cancelar una solicitud, haga clic en **[!UICONTROL Cancel]**. No se crea una etiqueta de envío y se desactiva la casilla de verificación _[!UICONTROL Create Shipping Label]_.

   >[!NOTE]
   >
   >Si utiliza un tipo de paquete distinto del predeterminado o requiere una firma, el coste de envío puede diferir del que ha cobrado al cliente. Cualquier diferencia en el costo de envío no se refleja en su tienda.

1. Haga clic en **[!UICONTROL OK]**.

   Commerce se conecta al sistema del transportista, envía el pedido y recibe una etiqueta de envío y un número de seguimiento para cada paquete.

### Método 2: Crear etiqueta para envío existente

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Busque el pedido en la cuadrícula y abra el formulario de envío.

1. En la sección _[!UICONTROL Shipping and Tracking Information]_, haga clic en **[!UICONTROL Create Shipping Label]**.

1. Distribuya los productos solicitados en los paquetes apropiados y haga clic en **[!UICONTROL OK]**.

1. Para revisar la información del paquete, haga clic en **[!UICONTROL Show Packages]**.

## Paso 4: Imprimir las etiquetas

Las etiquetas de envío se generan en formato PDF y se pueden imprimir desde el administrador. Cada etiqueta incluye el número de pedido y el número de paquete.

>[!NOTE]
>
>Dado que se crea un pedido de envío individual para cada paquete, se pueden recibir varias etiquetas de envío para un único envío.

### Método 1: Imprimir etiqueta desde el formulario de envío

1. En la _barra lateral de administración_, vaya a una de las siguientes páginas y busque el registro de envío:

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]**: busque el orden en la cuadrícula y abra el registro. En el panel izquierdo, elija **[!UICONTROL Shipments]**. A continuación, abra el registro de envío.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**: busque el envío en la cuadrícula y abra el registro.

1. Para descargar el archivo de PDF, vaya a la sección _[!UICONTROL Shipping and Tracking]_&#x200B;del formulario y haga clic en **[!UICONTROL Print Shipping Label]**.

   Según la configuración del navegador, las etiquetas de envío pueden verse e imprimirse directamente desde el archivo PDF.

   El botón _[!UICONTROL Print Shipping Label]_&#x200B;solo aparece después de que el transportista genere etiquetas para el envío. Si falta el botón, haga clic en **[!UICONTROL Create Shipping Label]**. El botón aparece después de que Commerce reciba la etiqueta del operador.

### Método 2: Imprimir etiquetas para varios pedidos

1. En la _barra lateral de administración_, vaya a una de las siguientes páginas y seleccione los pedidos o envíos que desea imprimir:

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]**: en la cuadrícula, seleccione la casilla de verificación de cada pedido con etiquetas de envío que desee imprimir.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**: en la cuadrícula, seleccione la casilla de verificación de cada envío con etiquetas que desee imprimir.

1. Establezca el control **[!UICONTROL Actions]** en `Print Shipping Labels`.

1. Haga clic en **[!UICONTROL Submit]**.

Se imprime un juego completo de etiquetas de envío para cada envío relacionado con los pedidos seleccionados.

## Configuración de operador requerida

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Type] | Los tipos de paquete difieren según el operador y el método. El tipo de paquete predeterminado para cada operador se selecciona inicialmente. USPS no requiere el tipo de paquete para los envíos nacionales. |
| [!UICONTROL Customs Value] | (Sólo envíos internacionales) El valor declarado o el precio de venta del contenido de un envío internacional. |
| [!UICONTROL Total Weight] | El peso total de todos los productos añadidos al paquete se calcula automáticamente. El valor también puede cambiarse manualmente e introducirse como libras o kilogramos. |
| [!UICONTROL Length, Width, Height] | (Opcional) Las dimensiones del paquete solo se utilizan para paquetes personalizados. Puede especificar las unidades de medida en pulgadas o centímetros.<br/><br/>**[!UICONTROL Not Required]**: el transportista no envía ninguna confirmación de envío a la tienda.<br/><br/>**[!UICONTROL No Signature]**: el transportista envía a la tienda una confirmación de envío sin la firma del destinatario.<br/><br/>**[!UICONTROL Signature Required]**: el transportista obtiene la firma del destinatario y proporciona a la tienda una copia impresa.<br/><br/>**[!UICONTROL Direct]**: (Solo FedEx) FedEx obtiene una firma de alguien en la dirección de entrega. Si no hay nadie disponible para firmar el paquete, el transportista intenta entregar el paquete en otro momento.<br/><br/>**[!UICONTROL Indirect]**: (Solo entregas residenciales de FedEx) FedEx obtiene la firma de alguien (posiblemente un vecino o administrador de edificio) en la dirección de entrega. El destinatario puede dejar una etiqueta de puerta de FedEx firmada para autorizar que el paquete se quede sin que nadie presente firme por él.<br/><br/>**[!UICONTROL Contents]**: (Solo USPS) Seleccione una de las siguientes descripciones del paquete:<br/>- Regalo<br/>- Documentos<br/>- Muestra comercial<br/>- Productos devueltos<br/>- Mercancía<br/>- Otros <br/><br/>**[!UICONTROL Explanation]**: (Solo USPS) Una descripción detallada del contenido del paquete.<br/><br/>**[!UICONTROL Adult Required]**: el transportista obtiene la firma de un destinatario adulto y proporciona a la tienda una copia impresa. |

{style="table-layout:auto"}

## Creación de paquetes

La ventana _[!UICONTROL Create Packages]_&#x200B;aparece cuando elige crear una etiqueta de envío. Puede comenzar a configurar el primer paquete inmediatamente.

### Configuración de un paquete

>[!NOTE]
>
>Si selecciona el valor no predeterminado para [!UICONTROL Type] o decide requerir una confirmación de firma, el precio de un envío puede diferir del que cargó al cliente.

1. Para ver una lista de los productos enviados y agregarlos al paquete, haga clic en **[!UICONTROL Add Products]**.

   - Especifique los productos y las cantidades.

     La columna _[!UICONTROL Qty]_&#x200B;muestra la cantidad máxima disponible para agregar. Para el primer paquete, el número es la cantidad total del producto que se va a enviar.

   - Para agregar los productos al paquete, haga clic en **[!UICONTROL Add Selected Product(s) to Package]**.

1. Para agregar un paquete, haga clic en **[!UICONTROL Add Package]**.

   Puede añadir varios paquetes y editarlos al mismo tiempo.

1. Para eliminar un paquete, haga clic en **[!UICONTROL Delete Package]**.

Una vez añadidos los productos al paquete, la cantidad no se puede editar directamente.

### Aumentar la cantidad

1. Haga clic en **[!UICONTROL Add Selection]**.

1. Introduzca la cantidad adicional.

   El número se añade a la cantidad anterior del producto en el paquete.

### Disminuir la cantidad

1. Elimine el producto del paquete.

1. Haga clic en **[!UICONTROL Add Selection]**.

1. Introduzca el nuevo valor más pequeño.

### Generar etiquetas de envío

Después de distribuir todos los productos, el número total de paquetes que va a utilizar es igual al número del último paquete de la lista. El botón _Aceptar_ está deshabilitado hasta que se distribuyan todos los artículos enviados a los paquetes y se complete toda la información necesaria.

Para generar las etiquetas, haga clic en **[!UICONTROL OK]**.

Puede hacer clic en **[!UICONTROL Cancel]** para detener el proceso, si es necesario. Los paquetes no se guardan y el proceso de etiqueta de envío se cancela.

### Descripciones de campos

| Campo | Descripción |
|--- |--- |
| [!UICONTROL Type] | Especifica el tipo de paquete. Seleccione uno de los valores predefinidos. Los tipos de paquetes disponibles son diferentes para cada transportista. Cuando se abre la ventana emergente Crear paquetes, el paquete predeterminado del transportista aparece en el campo Tipo. Si selecciona un paquete que no está diseñado por un transportista, debe introducir las dimensiones del paquete. Para las etiquetas de envío creadas para envíos de DHL, FedEx y UPS, el campo Tipo de productos está establecido en `Merchandise`. Para USPS, el campo refleja el valor del campo _Contents_ en la ventana _[!UICONTROL Create Packages]_. |
| [!UICONTROL Total Weight] | El peso total de un paquete. El campo se rellena previamente con el peso total de los productos de un paquete. La unidad de medida se puede establecer en libras o kilogramos. |
| [!UICONTROL Length] | La longitud de un paquete, números enteros y números de coma flotante. El campo está habilitado si se utiliza el tipo de paquete personalizado. La unidad de medida se puede establecer en pulgadas o centímetros. |
| [!UICONTROL Width] | Anchura de un paquete, números enteros y números de coma flotante. El campo está habilitado si se utiliza el tipo de paquete personalizado. Las unidades de medida se pueden especificar mediante el menú desplegable situado junto al campo Altura; seleccione entre pulgadas y centímetros. |
| [!UICONTROL Height] | Altura de un paquete, números enteros y números de coma flotante. El campo está habilitado si se utiliza el tipo de paquete personalizado. Las unidades de medida se pueden especificar mediante el menú desplegable situado junto al campo Altura; seleccione entre pulgadas y centímetros. |
| [!UICONTROL Signature] | Define la confirmación de envío. Opciones:<br/><br/>**[!UICONTROL Not Required]**: no se le enviará ninguna carta de confirmación de envío.<br/><br/>**[!UICONTROL No Signature]**: se le envía una carta de confirmación de envío sin la firma de un destinatario.<br/><br/>**[!UICONTROL Signature Required]**: el transportista obtiene la firma del destinatario y le proporciona su copia impresa.<br/><br/>**[!UICONTROL Adult Required]**: el transportista obtiene la firma del destinatario adulto y le proporciona su copia impresa.<br/><br/>**[!UICONTROL Direct (FedEx only)]**: FedEx obtiene una firma de alguien en la dirección de entrega y vuelve a intentar la entrega si no hay nadie disponible para firmar el paquete.<br/><br/>**[!UICONTROL Indirect (FedEx only)]**: FedEx obtiene una firma de una de las tres maneras siguientes: <br/>(1) de alguien en la dirección de entrega; <br/>(2) de un vecino, administrador de edificio u otra persona en la dirección; o <br/>(3) el destinatario puede dejar una etiqueta de puerta de FedEx firmada que autorice el lanzamiento del paquete sin que nadie esté presente. Disponible solo para envíos residenciales. Las opciones pueden variar ligeramente según los distintos métodos de envío. Para obtener la información más reciente, consulte los recursos del transportista. |
| [!UICONTROL Contents] | (Disponible solo para envíos de USPS) Descripción del contenido del paquete. Opciones: `Gift` / `Documents` / `Commercial Sample` / `Returned Goods` / `Merchandise` / `Other` |
| [!UICONTROL Explanation] | (Solo envíos de USPS) Descripción detallada del contenido del paquete. |

{style="table-layout:auto"}


<!-- Last updated from includes: 2025-11-26 10:55:00 -->
