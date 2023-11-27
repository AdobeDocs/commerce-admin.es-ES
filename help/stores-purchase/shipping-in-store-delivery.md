---
title: Envío en tienda
description: Aprenda a configurar una opción de envío en la tienda para su tienda.
exl-id: bd64b110-5c39-41c6-8a0c-38561b2a5bf4
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Envío en tienda

Con el método de entrega en tienda, el cliente puede seleccionar un origen para utilizarlo como ubicación de recogida durante el cierre de compra.

![Método de envío en tienda al finalizar la compra](./assets/luma-in-store-example.png){width="700" zoomable="yes"}

Durante el cierre de compra en la tienda:

1. El cliente hace clic en **[!UICONTROL Pick In Store]** o selecciona la variable _[!UICONTROL In-Store Pickup Delivery]_método de envío.
1. El _[!UICONTROL Pick In Store]_se abre la pestaña cierre de compra.

Si el cliente tiene una dirección o ha rellenado previamente el formulario de dirección de envío antes de cambiar a la _[!UICONTROL Pick In Store]_pestaña:

- La fuente más cercana a la dirección del cliente dentro del radio configurado se preselecciona automáticamente como tienda de recogida.
- Cuando el cliente haga clic en **[!UICONTROL Select Other]**, el _[!UICONTROL Select Store]_se abre el formulario de búsqueda. En la lista solo se muestran las tiendas que se encuentran dentro de la distancia (radio) configurada con respecto a la tienda preseleccionada. Todos los almacenes de la lista se ordenan por la distancia al almacén preseleccionado.
- Cuando el cliente introduce un código postal o un nombre de ciudad en el campo de búsqueda, solo se muestran en la lista las tiendas dentro de la distancia configurada (radio) a la ubicación buscada. Todos los almacenes de la lista se ordenan por la distancia a la ubicación buscada.
- Cuando el cliente borra el código postal o el nombre de la ciudad del campo de búsqueda, todas las tiendas de recogida asignadas a los productos en el carro de compras se muestran al cliente. Todos los almacenes de la lista se ordenan en orden ascendente de los códigos de origen sin ninguna limitación de distancia (radio).

Si el cliente no tiene dirección o no ha rellenado previamente el formulario de dirección de envío antes de cambiar a la _[!UICONTROL Pick In Store]_pestaña:

- La página muestra el _No se pudo preseleccionar la ubicación de recogida según la información disponible_ Mensaje.
- Cuando el cliente haga clic en **[!UICONTROL Select Store]**, el _[!UICONTROL Select Store]_se abre el formulario de búsqueda.
- Todas las tiendas de recogida asignadas a los productos en el carro de compras se muestran en orden ascendente de los códigos fuente sin ninguna limitación de distancia (radio).
- Cuando el cliente introduce un código postal o un nombre de ciudad en el campo de búsqueda, solo se muestran en la lista las tiendas dentro de la distancia configurada (radio) a la ubicación buscada. Todos los almacenes de la lista se ordenan por la distancia a la ubicación buscada.

## Antes de la configuración

- Asegúrese de que tiene un origen y existencias no predeterminados. Para obtener más información sobre cómo configurar un origen como ubicación de recogida, consulte [Añadir una fuente](../inventory-management/sources-add.md).
- Asegúrese de haber configurado un algoritmo de prioridad de distancia. Para obtener más información, consulte [Configuración del algoritmo de prioridad de distancia](../inventory-management/distance-priority-algorithm.md).
- Asegúrese de que tiene [descargado e importado](../inventory-management/cli.md#import-geocodes) todos los geocódigos necesarios para el cálculo sin conexión.
- Asegúrese de que ha configurado [Cálculo de Destino de Impuestos por Defecto](../configuration-reference/sales/tax.md#default-tax-destination-calculation) configuración.

>[!IMPORTANT]
>
>**En la tienda, los resultados de búsqueda se filtran por distancia (radio) para mostrar resultados relevantes:**<br><br>
>Si el cliente tiene una dirección de envío, la ubicación base para calcular la distancia (radio) se toma de la dirección de envío.<br><br>
>Si el cliente no tiene una dirección de envío, la ubicación base para calcular la distancia se toma del [Cálculo de Destino de Impuestos por Defecto](../configuration-reference/sales/tax.md#default-tax-destination-calculation) configuración. Esta configuración se establece por vista de tienda y debe configurar el Cálculo de destino de impuestos predeterminado para garantizar que la búsqueda en la tienda de recogida funcione correctamente.

## Configuración del envío en tienda

En primer lugar, compruebe que la entrega en tienda esté activada.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Sales]** y elija **[!UICONTROL Delivery Methods]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL In-Store Delivery]** sección.

   ![Entrega en tienda](../configuration-reference/sales/assets/delivery-methods-in-store-delivery.png){width="600" zoomable="yes"}

1. Establecer **[!UICONTROL Enabled]** hasta `Yes`.

   >[!NOTE]
   >
   >Si es necesario, borre la **[!UICONTROL Use system value]** para cambiar el valor predeterminado de cualquier campo.

1. Introduzca el **[!UICONTROL Method Name]** que describe el método de cálculo que se utiliza para producir una estimación de envío.

   El nombre del método aparece junto a la tasa estimada calculada en el carro de compras.

1. Introduzca el **[!UICONTROL Title]** que desea que aparezca para _Entrega en tienda_ durante el cierre de compra.

   El título predeterminado es `In-Store Pickup Delivery`.

1. Para cobrar a los clientes por el servicio de recogida en la tienda, introduce la tarifa en la **[!UICONTROL Price]** field.

1. Introduzca el **[!UICONTROL Search Radius]** en kilómetros para la ubicación de recogida de la tienda busca en el pago de la tienda.

1. Para **[!UICONTROL Displayed Error Message]**, introduzca el mensaje que aparece si la entrega en tienda deja de estar disponible.

   El mensaje predeterminado es `In-Store Delivery is not available. To use this delivery method, please contact us.`

1. Haga clic **[!UICONTROL Save Config]**.
