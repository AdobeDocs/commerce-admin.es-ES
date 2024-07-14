---
title: Tablero de administración
description: Obtenga información acerca del tablero de administración, que suele ser la primera página que aparece al iniciar sesión.
exl-id: 56957c0a-1618-444b-a37a-ecf0d7b27eae
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# Tablero de administración

El tablero suele ser la primera página que aparece al iniciar sesión en _Admin_ y puede proporcionar información general en tiempo real sobre las ventas y la actividad de los clientes. Los datos del panel de control proporcionan una instantánea de las ventas acumuladas en el tiempo, el importe promedio de los pedidos, los pedidos recientes y los términos de búsqueda. El gráfico muestra los pedidos e importes completados para el intervalo de fechas seleccionado y se puede generar a partir de datos dinámicos, en tiempo real o datos agregados históricos. Las pestañas de la parte inferior proporcionan informes rápidos de sus productos más vendidos, los productos más vistos, los clientes nuevos y los clientes que más han comprado.

Si tiene una cantidad importante de datos para procesar, el gráfico se puede desactivar para mejorar el rendimiento. El panel del siguiente ejemplo está configurado para utilizar datos en tiempo real y muestra los pedidos completados por hora durante las últimas 24 horas. El gráfico se actualiza para cada pedido completado.

![Tablero](./assets/dashboard-full.png){zoomable="yes"}

[Informes avanzados](business-intelligence.md#advanced-reporting) muestra un panel personalizado basado en los datos de productos, pedidos y clientes.

![Informes avanzados](./assets/dashboard-advanced-reporting.png){zoomable="yes"}

## Configuración del tablero

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**y complete cualquiera de las siguientes opciones de configuración.

1. Cuando finalice la configuración, haga clic en **[!UICONTROL Save Config]**.

1. Después de guardar los cambios, haga clic en **[!UICONTROL Cache Management]** y actualice todas las cachés no válidas.

### Habilitar gráficos

Si tiene que procesar una gran cantidad de datos, puede desactivar la visualización del gráfico para mejorar el rendimiento. Cuando no está habilitado, aparece el mensaje &quot;No se encontraron datos&quot; en lugar del gráfico, aunque los totales de resumen que aparecen a continuación siguen generándose.

1. En el panel de navegación izquierdo bajo **[!UICONTROL Advanced]**, elija **[!UICONTROL Admin]**.

1. Si es necesario, expanda la sección **[!UICONTROL Dashboard]**.

   ![Configuración avanzada: habilitar gráficos](./assets/admin-dashboard-config.png){width="600"}

1. Para cambiar el valor predeterminado, desactive la casilla de verificación **[!UICONTROL Use system value]**.

1. Definir **Habilitar gráficos** en `Yes`.

Para obtener más información acerca de las opciones de configuración de administración, consulte la [Guía de referencia de configuración](../configuration-reference/advanced/admin.md).

### Cambiar la página de inicio

El tablero es la [página de inicio](../configuration-reference/advanced/admin.md) predeterminada para el administrador, aunque puede configurar una página de inicio diferente.

1. Si todavía no tiene abiertas las opciones de configuración de administración, elija **[!UICONTROL Admin]** en _[!UICONTROL Advanced]_en el panel de navegación izquierdo.

1. Haga clic para expandir la sección **Página de inicio**.

   ![Panel de administración: configuración de la página de inicio](./assets/admin-startup-page.png){width="600"}

1. Desactive la casilla de verificación **[!UICONTROL Use system value]** y elija la **página de inicio** que desea que aparezca al iniciar sesión en el Administrador.

### Elija las fechas de inicio

1. En el panel de navegación izquierdo bajo **[!UICONTROL General]**, elija **Informes**.

1. En la página, expanda la sección **[!UICONTROL Dashboard]**.

1. Desactive las casillas de verificación **[!UICONTROL Use system value]** de la configuración de fecha y haga lo siguiente:

   - Establezca **El año hasta la fecha comienza** en **Mes** y **Día**.

   - Definir **El mes actual comienza** en **Día**.

   ![Panel de administración: configuración de fecha](./assets/reports-dashboard.png){width="600"}

Para obtener más información acerca de las opciones de configuración de [!UICONTROL Reports], consulte la [_Guía de referencia de configuración_](../configuration-reference/general/reports.md).

### Configuración de la fuente de datos

El gráfico del panel se puede generar en tiempo real o mediante datos históricos agregados. Si el rendimiento es un problema, puede acelerar las cosas mediante el uso de datos agregados.

1. En el panel de navegación izquierdo, haga clic para expandir **Ventas** y elija **Ventas** debajo.

1. En la página, expanda la sección **[!UICONTROL Dashboard]**.

   ![Panel de administración: configuración de la fuente de datos](./assets/config-sales-dashboard.png){width="600"}

1. Desactive la casilla de verificación **[!UICONTROL Use system value]** y establezca **[!UICONTROL Use Aggregated Data]** en una de las siguientes opciones:

   - Para los datos históricos agregados, elija `Yes`.
   - Para datos en tiempo real, elija `No`.

## Secciones de gráfico

| Sección | Descripción |
|--- |--- |
| [!UICONTROL Orders] | Esta pestaña muestra un gráfico en tiempo real de todos los pedidos completados para la vista de tienda actual y el período de tiempo especificado. |
| [!UICONTROL Amounts] | Esta pestaña muestra un gráfico en tiempo real de todos los importes de pedidos completados para la vista de tienda actual y el período de tiempo especificado. |
| [!UICONTROL Time Range] | Determina los datos que se representan en el gráfico y los totales de resumen a continuación. Opciones: `Last 7 Days` / `Current Month` / `YTD` / `2YTD` |
| [!UICONTROL Summary Totals] | Los totales de ingresos, impuestos, envíos y cantidad debajo del gráfico se basan en los datos del gráfico y en la configuración del intervalo de tiempo actual. |

{style="table-layout:auto"}

## Datos de instantánea

| Sección | Descripción |
|--- |--- |
| [!UICONTROL Lifetime Sales] | Las ventas totales agregadas durante la duración de la tienda. |
| [!UICONTROL Average Order] | Cantidad de pedido promedio durante la duración de la tienda. |
| [!UICONTROL Last Orders] | Un resumen de los últimos cinco pedidos realizados. |
| [!UICONTROL Last Search Terms] | Los últimos cinco términos de búsqueda. |
| [!UICONTROL Top Search Terms] | Los cinco términos de búsqueda más utilizados. |

{style="table-layout:auto"}

## Fichas de informe

| Sección | Descripción |
|--- |--- |
| [!UICONTROL Bestsellers] | Los cinco productos más vendidos durante el período de tiempo especificado. |
| [!UICONTROL Most Viewed Products] | Los cinco productos que más se vieron durante el período de tiempo especificado. |
| [!UICONTROL New Customers] | Los cinco clientes más recientes que se registraron para obtener una cuenta durante el período de tiempo especificado. |
| [!UICONTROL Customers] | Los últimos cinco clientes con un pedido que completó el procesamiento durante el período de tiempo especificado. |

{style="table-layout:auto"}

## Botones del panel

| Botón | Descripción |
|--- |--- |
| [!UICONTROL Reload Data] | Actualiza los datos del panel. |
| [!UICONTROL Go to Advanced Reporting] | Muestra un tablero personalizado de gráficos dinámicos e informes en función de los datos de productos, pedidos y clientes. Para obtener un análisis más detallado, consulte [Informes avanzados](business-intelligence.md#advanced-reporting). |

{style="table-layout:auto"}
