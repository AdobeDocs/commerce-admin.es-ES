---
title: Crear y eliminar segmentos de clientes
description: Los clientes pueden ver la información de reembolsos asociada con el pedido en el panel de control de su cuenta de cliente.
exl-id: 8a13271d-d0b5-4fc6-a701-3edfae04bfca
feature: Customers, Configuration
source-git-commit: 079aef1f4d90ecba649ac43e7cbab812da79871a
workflow-type: tm+mt
source-wordcount: '974'
ht-degree: 0%

---

# Crear y eliminar segmentos de clientes

{{ee-feature}}

Crear un segmento de cliente es similar a crear una [regla de precio del carro de compras](../merchandising-promotions/price-rules-cart.md), con la diferencia de que las opciones incluyen [atributos específicos del segmento del cliente](../customers/customer-segments.md).

![Lista de segmentos de clientes](assets/customer-segments.png){width="700" zoomable="yes"}

_&#x200B;**[!UICONTROL Customer Segments]cuadrícula &#x200B;** _

| Columna | Descripción |
|--- |--- |
| **[!UICONTROL ID]** | El ID único del segmento de cliente. |
| **[!UICONTROL Segment]** | El nombre del segmento de cliente. |
| **[!UICONTROL Status]** | Indica si el segmento de clientes es _[!UICONTROL Active]_&#x200B;o&#x200B;_[!UICONTROL Inactive]_. |
| **[!UICONTROL Website]** | Indica el sitio web al que pertenece el segmento de clientes. |

{style="table-layout:auto"}

## Requisito previo: Habilitar segmentos de clientes

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Customer Configuration]**.

1. Expanda la sección **[!UICONTROL Customer Segments]**.

1. Compruebe que **[!UICONTROL Enable Customer Segment Functionality]** está establecido en `Yes`.

   ![Configuración de clientes - segmentos de clientes](../configuration-reference/customers/assets/customer-configuration-customer-segments.png){width="600" zoomable="yes"}

1. (Opcional) Para deshabilitar la validación en tiempo real de los segmentos del cliente, establezca **[!UICONTROL Real-time Check if Customer is Matched by Segment]** en `No`.

   Cuando se desactiva la validación en tiempo real, los segmentos del cliente se validan mediante una única consulta SQL de condición combinada. Deshabilitar esta función mejora el rendimiento de la validación de segmentos si hay muchos segmentos de clientes en el sistema. Sin embargo, la validación no funciona con una base de datos dividida o cuando no hay clientes registrados.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Crear un segmento

Los siguientes pasos utilizan un ejemplo para crear un segmento de cliente dirigido a clientes mujeres en Los Ángeles.

### Paso 1: Añadir un segmento de cliente

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Segments]**.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Add Segment]**.

1. Escriba un **[!UICONTROL Segment Name]** que identifique el segmento de clientes cuando trabaje en el Administrador.

1. Escriba un breve **[!UICONTROL Description]** que explique el propósito del segmento.

1. Establezca **[!UICONTROL Assigned to Website]** en el sitio web donde se puede usar el segmento de cliente.

1. Establezca **[!UICONTROL Status]** en _Activo_ o _Inactivo_.

1. Para identificar los tipos de clientes que desea utilizar para aplicar el segmento, establezca **[!UICONTROL Apply to]** en uno de los siguientes:

   - `Visitors and Registered Customers`: incluye a todos los compradores, independientemente de si han iniciado sesión en una cuenta.
   - `Registered Customers`: incluye solo los compradores que iniciaron sesión en una cuenta.
   - `Visitors`: incluye solo los compradores que no han iniciado sesión en una cuenta.

   >[!TIP]
   >
   >Si está creando un segmento basado en atributos del cliente almacenados en una cuenta de cliente, se recomienda aplicar el segmento solo a clientes registrados.

   >[!NOTE]
   >
   > Si un segmento se aplica a `Visitors and Registered Customers`, [!UICONTROL Matched Customers] solo muestra `Registered Customers`. Este es el caso incluso si los visitantes pueden ser objetivos en función de las condiciones que se les apliquen. No se muestra la ficha `Visitors` para los segmentos que solo son de `Matched Customers`.


1. Haga clic en **[!UICONTROL Save and Continue Edit]**.

   Después de guardar el segmento _[!UICONTROL General Properties]_, hay opciones adicionales disponibles en el panel izquierdo.

   ![Propiedades del segmento](assets/customer-segment-saved.png){width="600" zoomable="yes"}

**_[!UICONTROL General Properties]_**

| Campo | Descripción |
|--- |---|
| **[!UICONTROL Segment Name]** | Un nombre que identifica el segmento de referencia interna. |
| **[!UICONTROL Description]** | Una breve descripción que explica el propósito del segmento para la referencia interna. |
| **[!UICONTROL Assigned to Website]** | El sitio web único donde se puede utilizar el segmento. |
| **[!UICONTROL Status]** | Activa y desactiva el segmento. Cualquier regla de precios y banners asociados se desactivan cuando el segmento está desactivado. Opciones: `Active` / `Inactive` |
| **[!UICONTROL Apply to]** | Define los tipos de cliente a los que se aplica el segmento. La selección influye en el conjunto de condiciones disponibles para crear el segmento. La configuración no se puede cambiar una vez guardado el segmento. |

{style="table-layout:auto"}

### Paso 2: Definición de las condiciones

>[!NOTE]
>
> Para los visitantes, solo se aplican las siguientes condiciones: Condiciones del carro de compras (cantidad del subtotal del carro de compras, artículos de línea del carro de compras y cantidad de productos del carro de compras), Reglas de producto (productos encontrados en el carro de compras y el historial de productos) y combinaciones de estos artículos. Si un segmento se aplica tanto a visitantes como a clientes registrados, el seguimiento de los visitantes se realiza únicamente en función de las condiciones enumeradas.

Las condiciones posibles se organizan en los siguientes grupos:

| Grupo | Descripción |
|--- |--- |
| **[!UICONTROL Customer]** | Condiciones basadas en atributos de cuenta de cliente. Disponible solo si el segmento se aplica a clientes registrados. |
| **[!UICONTROL Shopping Cart]** | Condiciones basadas en el contenido del carro de compras. Estas condiciones están disponibles para todos los tipos de segmentos. |
| **[!UICONTROL Products]** | Condiciones basadas en productos del carro de compras o en el historial de navegación de productos. Estas condiciones están disponibles para todos los tipos de segmentos. |
| **[!UICONTROL **Sales]** | Condiciones basadas en pedidos completados. Disponible solo si el segmento se aplica a clientes registrados. |

1. En el panel izquierdo, haga clic en **[!UICONTROL Conditions]**.

   La condición predeterminada comienza con _[!UICONTROL If ALL of these conditions are TRUE:]_&#x200B;en la página.

   ![Condiciones](assets/customer-segment-conditions.png){width="600" zoomable="yes"}

1. Cree una condición que se dirija a clientes mujeres:

   - Haga clic en el icono **[!UICONTROL Add]** para mostrar la lista de condiciones y seleccione `Gender`.

   - Deje la opción de control de condición predeterminada **is**.

   - Haga clic en **...** y seleccione `female`.

   ![Línea de condición 1](assets/customer-segment-condition-line1.png){width="600" zoomable="yes"}

1. Cree otra condición que se dirija a los residentes de Los Ángeles:

   - En la línea siguiente, haga clic en el icono **[!UICONTROL Add]** y seleccione `Customer Address`.

     Esta acción crea una condición principal en la que se pueden definir uno o varios campos de dirección para que coincidan.

   - Haga clic en el icono **[!UICONTROL Add]** para mostrar la lista de campos de dirección y seleccione `City`.

   - Haga clic en **is** para mostrar las opciones de control de condición y seleccione `contains`.

   - Haga clic en **...** y escriba `Los Angeles`.

   - En la línea siguiente, haga clic en el icono **[!UICONTROL Add]** y seleccione `State/Province`.

   - Deje la opción de control de condición predeterminada **is**.

   - Haga clic en **...** y seleccione `United States > California`.

   ![Condiciones para las mujeres en Los Ángeles, California](assets/customer-segment-conditions-la-ladies.png){width="600" zoomable="yes"}

1. Haga clic en **[!UICONTROL Save and Continue Edit]**.

### Paso 3: Revisar la lista de clientes coincidentes

1. En el panel izquierdo, haga clic en **[!UICONTROL Matched Customers]** para mostrar todos los clientes que cumplen la condición.

   ![Clientes coincidentes](assets/customer-segment-matched-customers.png){width="600" zoomable="yes"}

1. Si la lista de clientes cumple su objetivo, haga clic en **[!UICONTROL Save]** para completar el segmento de clientes.

1. El segmento de clientes ahora se puede utilizar para dirigir promociones, contenido y envíos de correo.

_&#x200B;**[!UICONTROL Matched Customers]cuadrícula &#x200B;** _

| Columna | Descripción |
|--- |--- |
| **[!UICONTROL ID]** | El ID de cliente de un cliente registrado. |
| **[!UICONTROL Name]** | El nombre de un cliente registrado. |
| **[!UICONTROL Email]** | La dirección de correo electrónico de un cliente registrado. |
| **[!UICONTROL Group]** | El grupo de clientes al que está asignado el cliente. |
| **[!UICONTROL Phone]** | Número de teléfono del cliente. |
| **[!UICONTROL ZIP]** | El código postal del cliente. |
| **[!UICONTROL Country]** | El país donde se encuentra el cliente. |
| **[!UICONTROL State / Province]** | Estado o provincia donde se encuentra el cliente. |
| **[!UICONTROL Customer Since]** | La fecha y la hora de creación de la cuenta del cliente. |

{style="table-layout:auto"}

## Quitar un segmento de cliente

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Customers]** > **[!UICONTROL Segments]**.

1. Busque el segmento que desea eliminar y selecciónelo.

1. En la barra de menús, haga clic en el botón **[!UICONTROL Delete]**.

1. Para confirmar la acción, haga clic en **[!UICONTROL OK]**.

## Barra de botones

| Botón | Descripción |
|--- |--- |
| **[!UICONTROL Back]** | Vuelve a la página _[!UICONTROL Customer Segments]_&#x200B;sin guardar los cambios. |
| **[!UICONTROL Delete]** | Elimina el segmento de cliente actual. Los clientes o los pedidos completados asociados con el cliente en el segmento no se eliminan. |
| **[!UICONTROL Reset]** | Restablece los cambios no guardados en el formulario de segmentos del cliente a sus valores anteriores. |
| **[!UICONTROL Refresh Segment Data]** | Actualiza los datos del segmento a los valores guardados más recientemente. Relevante si algún dato de segmento no está disponible o no está actualizado. |
| **[!UICONTROL Save and Continue Edit]** | Guarda los cambios y mantiene abierto el segmento de cliente. |
| **[!UICONTROL Save]** | Guarda los cambios y cierra el segmento de clientes. |

{style="table-layout:auto"}

## Demostración de segmentos de clientes

Vea este vídeo para ver una demostración de la creación de segmentos de clientes:

>[!VIDEO](https://video.tv.adobe.com/v/3411828/?quality=12&learn=on&captions=spa)
