---
title: Configurar etiquetas de envío
description: Aprenda a configurar la tienda para generar etiquetas de envío.
exl-id: 0693d74b-8b36-4a36-8739-c9fe5a934ff0
feature: Shipping/Delivery, Orders
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# Configurar etiquetas de envío

Las siguientes configuraciones deben realizarse en el nivel de producto y en la configuración de cada operador que se utiliza para imprimir etiquetas. Para imprimir etiquetas, todos los operadores requieren que abra una cuenta. A continuación, complete la configuración de la tienda para cada operador que vaya a utilizar.

## Requisitos del operador

| [!UICONTROL Carrier] | Requisitos |
|-------|--------|
| [USPS](usps.md) | Requiere una cuenta de USPS. A partir del 23 de febrero de 2018, USPS requiere que todas las etiquetas de envío incluyan franqueo. |
| [UPS](ups.md) | Requiere una cuenta de UPS. Las etiquetas de envío solo están disponibles para los envíos que se originan en los EE. UU. Se requieren credenciales específicas para las tiendas fuera de los EE. UU. |
| [FedEx](fedex.md) | Requiere una cuenta de FedEx. En tiendas fuera de los EE. UU., las etiquetas de envío solo son compatibles con envíos internacionales. FedEx no permite envíos nacionales que se originen fuera de los Estados Unidos |
| [DHL](dhl.md) | Requiere una cuenta de DHL. Las etiquetas de envío solo son compatibles con los envíos procedentes de EE. UU. |

{style="table-layout:auto"}

## Paso 1: Verificar el país de fabricación

El país de fabricación es obligatorio para todos los productos que son enviados internacionalmente por USPS y FedEx. Si tiene muchos productos que se deben actualizar, puede hacer lo siguiente [importar](../systems/data-import.md) las actualizaciones o utilice la cuadrícula Inventario para actualizar varios registros.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Actualice el registro de etiquetas de envío mediante uno de los métodos siguientes.

### Método 1: Actualización de un solo registro

1. En la cuadrícula, busque el producto que desea actualizar y ábralo en modo de edición.

1. Actualice el **País de fabricación** según sea necesario.

   ![País de fabricación](./assets/product-country-of-manufacture.png){width="700" zoomable="yes"}

1. Haga clic **[!UICONTROL Save]**.

### Método 2: Actualización de varios registros

1. En la cuadrícula, seleccione la casilla de verificación de cada producto que desea actualizar.

   Por ejemplo, todos los productos fabricados en China.

1. Configure las variables **[!UICONTROL Actions]** control a `Update Attributes` y haga clic en **[!UICONTROL Submit]**.

1. En el _Actualizar atributos_ del formulario, busque el **País de fabricación** y seleccione el campo **Cambiar** casilla de verificación

1. Elige el país.

1. Haga clic **[!UICONTROL Save]**.

## Paso 2 Verificar la información del almacén

{{beta2-updates}}

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Shipping Settings]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Origin]** y compruebe que los campos siguientes están completos:

   - **[!UICONTROL Street Address]** - La dirección del lugar desde el que se envían los envíos. Por ejemplo, la ubicación de su compañía o almacén. Este campo es obligatorio para las etiquetas de envío.
   - **[!UICONTROL Street Address Line 2]** - Cualquier información de dirección adicional, como el piso o la entrada. Se recomienda utilizar este campo.

   ![Origen](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. En el _Ventas_ en el panel izquierdo, elija **[!UICONTROL Delivery Methods]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL USPS]** y compruebe que los campos siguientes están completos:

   - **[!UICONTROL Secure Gateway URL]** : el sistema introduce automáticamente la dirección URL de puerta de enlace.
   - **[!UICONTROL Password]** - La contraseña es proporcionada por USPS y le da acceso a su sistema a través de Servicios Web.
   - **Longitud, anchura, altura, circunferencia** : Dimensiones predeterminadas del paquete. Para que aparezcan estos campos, establezca **[!UICONTROL Size]** hasta `Large`.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **FedEx** y compruebe que los campos siguientes están completos:

   - Número de medidor
   - Clave
   - Contraseña

   Esta información es proporcionada por el operador y es necesaria para obtener acceso a su sistema a través de los servicios web.

1. En el panel izquierdo, expanda **[!UICONTROL General]** y elija **[!UICONTROL General]** debajo.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Store Information]** y compruebe que los campos siguientes están completos:

   - **[!UICONTROL Store Name]** : nombre de la tienda o vista de la tienda.
   - **[!UICONTROL Store Contact Telephone]** : número de teléfono del contacto principal de la vista de tienda o tienda.
   - **[!UICONTROL Country]** - El país donde se encuentra su tienda.
   - **[!UICONTROL VAT Number]** - Si procede, el número de IVA de su tienda. (No es necesario en tiendas ubicadas en EE. UU.)
   - **[!UICONTROL Store Contact Address]** : la dirección de la calle del contacto principal de la vista de tienda o tienda.

1. Si tiene varias tiendas y la información de contacto difiere de la predeterminada, establezca **[!UICONTROL Store View]** para cada y compruebe que la información es completa.

   Si falta información, aparece un error al intentar imprimir las etiquetas.

   ![Información de tienda](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. Haga clic **[!UICONTROL Save Config]**.
